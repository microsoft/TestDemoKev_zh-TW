ms です。TocTitle: Outlook 残りのバッチ要求 (プレビュー) タイトル: バッチの説明の (プレビュー) で Outlook の他の送信を要求: 残りの部分を複数のバッチを処理する方法を 1 つの HTTP 要求を形成し、複数の HTTP 接続のオーバーヘッドを軽減する同時要求します。ms です。ContentId: a842854e-46b3-47d9-8899-c27b481f4e78 <<<<<<< ヘッド ms.topic: 参照 (API) ms.date: 2016 5 月 16 日=======
ms.date: 2016 年 9 月 13 日
>>>>>>> ステージング

[!INCLUDE [Add the O365API repo styles](../includes/controls/addo365apistyles.html)]

# <a name="send-outlook-rest-requests-in-batches-preview"></a>バッチ (プレビュー) で Outlook の他の要求を送信します。

[!INCLUDE [Add the Outlook REST API filters--beta default v1 v2 disabled](../includes/controls/addOutlookversion_betadefault_v1v2disabled.html)]    


 _**に適用されます:**オンライン交換 |Office 365 |Hotmail.com |Live.com |MSN.com |Outlook.com |Passport.com_

<p class="previewnote">このドキュメントでは、プレビューである 1 つのバッチ要求として Outlook の他の複数の要求を送信することについて説明します。プレビュー機能では、ファイナライズする前に変更されることし、それらを使用するコードを中断することがあります。このため、一般的にする必要がありますを使用する API の生産バージョンのみ、実稼働コードで。可能な場合、バージョン 2.0 は現在推奨されるバージョンです。</p>

バッチ処理を使用すると、HTTP 接続とオーバーヘッドの数を減らすこと、1 つの HTTP のバッチ要求で複数の Outlook の他の要求を配置します。バッチ内の要求は、サインインしているユーザーのまたは (、Live.com、MSN.com、Outlook.com、または Passport.com) は、Microsoft アカウントに、Office 365 では、Azure Active Directory によってセキュリティで保護されたデータにアクセスします。 


**メモ**参照のわかりやすくするため、この資料の残りの部分は、**これらの Microsoft アカウントのドメインを含めるには、「Outlook.com」**を使用します。 

## <a name="overview"></a>概要

残りの要求には、クライアントとサーバーは、一定量のオーバーヘッドが発生するとの間の HTTP 接続が必要です。バッチ処理では、$batch エンドポイントを 1 つの HTTP POST 要求に複数の REST API 呼び出しを組み合わせることにより、接続のオーバーヘッドを削減できます。  
```
POST https://outlook.office.com/api/{version}/$batch
```
バッチ要求は、最大 20 個別 REST API コール、データのクエリをすることができますを含めることができます (GET など) を変更するか (例: POST) 操作です。バッチの残りの部分の 1 つまたは複数の呼び出しが失敗する場合でもを続行する[選択](#PreferContinueOnError)ヘッダーを指定することができます。

バッチ処理は、大量のデータを同期中に特に便利ですが。同じバッチ内の API 呼び出しは、メッセージやイベントは、同じサインイン中のユーザーのメールボックスに属しているなど、さまざまなリソースにアクセスできます。 

20 件以上の呼び出しを行う必要がある場合、または呼び出しを完了する順序が重要な場合は、複数のバッチ要求を使用します。


## <a name="example"></a>例

最も簡単な例では、バッチ処理を示しています。次のバッチ要求では、1 つのバッチで 2 つの Outlook の他の API 呼び出しを配置します。
1. サインイン中のユーザーのすべてのイベントを取得します。
2. メッセージを投稿します。

### <a name="batch-request"></a>バッチ要求

```
POST https://outlook.office.com/api/beta/$batch HTTP/1.1

Authorization: Bearer aGFwcHlnQGRr==
Host: outlook.office.com
Content-Type: multipart/mixed; boundary=batch_myBatchId


--batch_myBatchId
Content-Type: application/http
Content-Transfer-Encoding: binary

GET  /api/beta/me/events?$select=subject,organizer    HTTP/1.1


--batch_myBatchId
Content-Type: application/http
Content-Transfer-Encoding: binary

POST  /api/beta/me/sendmail    HTTP/1.1
Content-Type: application/json

{
  "Message": {
    "Subject": "Meet for lunch?",
    "Body": {
      "ContentType": "Text",
      "Content": "The new cafeteria is open."
    },
    "ToRecipients": [
      {
        "EmailAddress": {
          "Address": "rufus@contoso.com"
        }
      }
    ]
  }
}


--batch_myBatchId--
```

### <a name="batch-response"></a>バッチ応答

バッチ応答には、該当する場合、バッチ要求および個々 のコールの個別の応答コードと本文が含まれています。 

```
HTTP/1.1 200 OK
Content-Type: multipart/mixed; boundary=batchresponse_8faca3a8-183c-4dea-b396-25ac7dd77e09
Content-Length: 12898

--batchresponse_8faca3a8-183c-4dea-b396-25ac7dd77e09
Content-Type: application/http
Content-Transfer-Encoding: binary

HTTP/1.1 200 OK
OData-Version: 4.0
Content-Type: application/json;odata.metadata=minimal;odata.streaming=true;IEEE754Compatible=false;charset=utf-8

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events(Subject,Organizer)",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/Events('AAMkAGEtk-hAAA=')",
            "@odata.etag": "W/\"mODEKWhc/Um6lA3uPm7PPAAAX791Eg==\"",
            "Id": "AAMkAGEtk-hAAA=",
            "Subject": "Standup meeting",
            "Organizer": {
                "EmailAddress": {
                    "Address": "rufus@contoso.com",
                    "Name": "Rufus Tallent"
                }
            }
        },

        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/Events('AAMkAGED3CAAA=')",
            "@odata.etag": "W/\"mODEKWhc/Um6lA3uPm7PPAAAD6Ir3g==\"",
            "Id": "AAMkAGED3CAAA=",
            "Subject": "Discuss the campaign",
            "Organizer": {
                "EmailAddress": {
                    "Address": "basil@contoso.com",
                    "Name": "Basil Pearsall"
                }
            }
        }
    ]
}
--batchresponse_8faca3a8-183c-4dea-b396-25ac7dd77e09
Content-Type: application/http
Content-Transfer-Encoding: binary

HTTP/1.1 202 Accepted

--batchresponse_8faca3a8-183c-4dea-b396-25ac7dd77e09--
```

****

## <a name="batch-details"></a>バッチの詳細

### <a name="endpoint-url"></a>エンドポイントの URL

Outlook の他の複数の要求のバッチを送信するには、投稿 $batch エンドポイントでの操作を行います。
```
POST https://outlook.office.com/api/{version}/$batch HTTP/1.1
```

**注意** ルート URL https://outlook.office.com を使用して、最適なパフォーマンスと**x AnchorMailbox**ヘッダーを追加ユーザーの電子メール アドレス] に設定します。また、大文字と小文字、Outlook.com のユーザーのメールボックスがまだ有効になっていない Outlook の REST API のエラー コード MailboxNotEnabledForRESTAPI と MailboxNotSupportedForRESTAPI のチェックを処理します。詳細についてを参照してください[ここで](..\api\use-outlook-rest-api.md#OutlookRESTCaution)。 

**中国の開発者用のメモ** 

- アプリケーションを開発する場合は_Office 365 の_中国で、[中国向けの Office 365 の API のエンドポイント](..\api\o365-china-endpoints.md)を使用する続行する必要があります。

- アプリケーションを作成する場合は_Outlook.com の_中国では、 [v2 アプリケーション モデルのプレビュー](..\api\use-outlook-rest-api.md#RegAuthConverged)、および次の Outlook の REST エンドポイントを使用する必要があります。`https://outlook.office.com/api/{version}`


###<a name="version-of-api"></a>API のバージョン

バッチ処理プレビュー状態では、現在ベータ版の名前空間でのみ使用可能なこれを指定`{version}`と`beta`。

`https://outlook.office.com/api/beta/$batch`

バッチ要求とその他の呼び出しあるため、バッチには、ホストと API のバージョンを使用する必要があります、現在ベータ版で公開されている Outlook の他の呼び出しだけをバッチ処理することができます。 

**注意**バッチに含めることがいくつかの API 呼び出し応答よりも全般的な可用性を実現するなど、バージョン 2.0 と v1.0 のバージョンのベータ版で異なることを注意してをください。一般に、ベータ版のプレビューの状態で、API 関数を使用する場合は、アプリの機能を確認して、変更可能な点への対応を計画します。
 

###<a name="target-user"></a>ターゲット ユーザー

同じバッチ内でサインインしているユーザーのメールボックスに対して Outlook の他の API 呼び出しをグループ化することができます。メールボックスを Office 365 または Outlook.com にあってもかまいません。

### <a name="authentication"></a>認証

個々 の要求として[Outlook の他の API](..\api\use-outlook-rest-api.md#DefineOutlookRESTAPI)呼び出しを送信することと同様に、有効なアクセス トークンは、**認証**要求のヘッダーに含める必要があります。バッチ要求のヘッダーを指定する場合は、アクセス トークンがそのバッチ内のすべての呼び出しに必要なアクセス許可を提供します。必要に応じてその呼び出しが別のアクセス トークンを必要とする場合、バッチ内、特定の呼び出し用のアクセス トークンを指定できます。
 
アクセス トークンを取得するには、登録されていると、アプリケーションを識別し、適切な承認を取得する必要があります。いくつかについての[詳細について](..\api\use-outlook-rest-api.md#ShortRegAuthWorkflow)は、登録および承認オプションが合理化されました。要求をバッチ処理の詳細の学習には、この点に留意してください。

### <a name="batch-request-headers"></a>バッチ要求のヘッダー

バッチ要求ごとに次のヘッダーが含まれます。

```
Host: outlook.office.com
Content-Type: multipart/mixed; boundary=batch_<batchId> 
```

場所`{batchId}`バッチを識別し、バッチ内で要求を区切るために使用されます。GUID または任意の識別用文字列を指定できます。

適切な場所は、他のヘッダーを含めることができます。以外のコンテンツに関連する**コンテンツの種類**などのヘッダー、バッチ要求のヘッダーは、一般に、バッチ内のすべての操作に適用されます。バッチ要求と、バッチ内の特定の操作の両方のヘッダーを指定する場合、後者が優先され、操作に適用されます。   


### <a name="batch-request-body"></a>バッチ要求の本体

次の行を含むバッチ内の各操作を開始します。
```
--batch_{batchId} 
Content-Type: application/http 
Content-Transfer-Encoding: binary 
```
このバッチ内の最後の操作を終了します。
```
--batch_{batchId}--
```


### <a name="operations-in-a-batch"></a>バッチ内での操作
バッチ要求では、最大 20 個の操作を指定できます。

バッチ内の操作は、データのクエリ、変更、アクション、または関数の呼び出し要求できます。完全な Url と状態すべてのヘッダーをバッチ内の各操作を繰り返す必要はありません、中には、特定のヘッダーを含めるし、操作に必要な場合は、本文を要求してください。

### <a name="relative-urls-within-a-batch"></a>バッチ内での相対 Url
操作の完全な URL を指定する代わりに、相対 URL を含めることができます。次の例では GET 要求で URL を指定するたとえば、 `/api/beta/me/events` 、バッチ要求で指定されたホストからの相対`https://outlook.office.com`。

```
POST https://outlook.office.com/api/beta/$batch HTTP/1.1

User-Agent: YouRock
Authorization: Bearer {accessToken}
Host: outlook.office.com
Content-Type: multipart/mixed; boundary=batch_<myBatchID>

--batch_{batchID}
Content-Type: application/http
Content-Transfer-Encoding: binary

GET  /api/beta/me/events?$select=subject,organizer    HTTP/1.1

--batch_{batchID>}--

```

### <a name="processing-a-batch-request"></a>バッチ要求の処理
バッチ要求では、1 つの要求として独自に処理され、独自の応答コードを返します。正しいヘッダーを含む整形式のバッチ要求は HTTP 200 OK を返します。これは、ただしわけでは、バッチ内のすべての要求が成功しました。バッチ要求の本体では、各要求は別々 に処理される順と、独自の応答コードおよび応答の本文とエラー メッセージを返します。

サーバーは、任意の順序で、バッチ内での操作を実行する可能性があります。特定の順序で実行される操作が必要な場合同じバッチ要求内に配置する必要がありますがないです。代わりに、単独で 1 回の操作を送信する、次のいずれかを送信する前に応答を待機します。

<a name="PreferContinueOnError"></a>

既定では、処理エラーが返される最初の操作を停止しています。処理エラーを無視し、バッチ内の次の操作を続行して次のヘッダーを指定することができます。

```
Prefer: odata.continue-on-error
```



<a name="NextSteps"> </a>
## <a name="next-steps"></a>次のステップ

アプリケーションの構築を開始、あるいは詳細については、準備が整ったら、かどうかお任せします。

- [メール、カレンダー、および連絡先の他の Api を使用](http://dev.outlook.com/RestGettingStarted)します。

- 対話型の[API のサンド ボックス](https://apisandbox.msdn.microsoft.com/)を使用して Office 365 の Api について説明します。

- サンプルをしますか。[きました](..\howto\starter-projects-and-code-samples.md)。


または、Office 365 のプラットフォームを使用する方法の詳細について説明します。

- [REST API を outlook で Outlook のデベロッパー センター](http://dev.outlook.com/RestGettingStarted/Overview)

- [Office 365 のプラットフォーム上での開発の概要](..\howto\platform-development-overview.md)

- [Office 365 アプリケーションの認証およびリソースの承認](..\howto\common-app-authentication-tasks.md)

- [Azure AD で Office 365 の Api にアクセスできるように、アプリケーションを手動で登録します。](..\howto\add-common-consent-manually.md)

- [メールの残りの部分の Api を参照します。](..\api\mail-rest-operations.md)

- [REST Api の予定表を参照します。](..\api\calendar-rest-operations.md)

- [REST Api リファレンスを取引先担当者します。](..\api\contacts-rest-operations.md)

- [タスクの残りの部分の API (プレビュー)](..\api\task-rest-operations.md) 

- [メール、予定表、連絡先、およびタスクの残りの部分の Api のリソースの参照](..\api\complex-types-for-mail-contacts-calendar.md)

- [Office 365 のデータ拡張機能の残りの部分の API リファレンス](..\api\extensions-rest-operations.md)

- [人の残りの部分の API リファレンス](..\api\people-rest-operations.md)

- [通知の残りの部分の API リファレンス](..\api\notify-rest-operations.md)

- [ユーザーの写真の残りの部分の API リファレンス](..\api\photo-rest-operations.md)

[!INCLUDE [Enable filtering functionality ](../includes/controls/enablefiltering.html)]
