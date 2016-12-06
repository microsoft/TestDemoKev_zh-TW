ms です。TocTitle: Outlook の予定表の残りの部分の API リファレンス タイトル: Outlook の予定表の残りの部分の API リファレンスの説明: カレンダーの残りの部分の API は、クライアント ライブラリのイベント、予定表、および Exchange Online で予定表のグループへのアクセスを提供する Api と対話する方法を参照します。ms です。ContentId: 443f1cdf-1adb-46a2-b299-228c6f429954 ms.topic: ms.date を参照 (API): 2016 年 6 月 29 日

[!INCLUDE [Add the O365API repo styles](../includes/controls/addo365apistyleshtml)]

# <a name="outlook-calendar-rest-api-reference"></a>Outlook 予定表の残りの部分の API リファレンス


[!INCLUDE [Add the Outlook REST API filters--v2 default](../includes/controls/addOutlookVersion_v2defaulthtml)]

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<p class="previewnote">このドキュメントでは、会議の時間を検索、イベント、およびプレビューする添付ファイルを参照をキャンセルするための API について説明します。プレビュー機能では、ファイナライズする前に変更されることし、それらを使用するコードを中断することがあります。このため、一般的にする必要がありますを使用する API の生産バージョンのみ、実稼働コードで。可能な場合、バージョン 2.0 は現在推奨されるバージョンです。</p>

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

   
 _**に適用されます:**オンライン交換 |Office 365 |Hotmail.com |Live.com |MSN.com |Outlook.com |Passport.com_

カレンダー API は、イベント、カレンダー、および予定表に、Office 365 の Azure Active Directory によってセキュリティで保護されたデータをグループ化およびこれらのドメインで具体的には Microsoft アカウントの類似したデータへのアクセスを提供: Hotmail.com、Live.com である MSN.com、Outlook.com、および Passport.com。 
  

<!-- Can add the following sentence back once the client libraries have been updated for converged auth and outlook.com

You can access the Calendar API by calling the corresponding REST APIs directly in your apps, or by using the Office 365 client libraries and SDKs.
-->

**メモ** 

- 例外は、[会議の時刻を検索](#FindMeetingTimesPreview)するのみ Office 365 のメールボックス (Azure AD) と Microsoft アカウントに適用される API です。 
- 参照のわかりやすくするため、この資料の残りの部分**を上記の一覧に Microsoft アカウントのドメインを含めるには、"Outlook.com"**を使用します。


<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

**API のベータ版では関係ないですか?**右上隅にコントロールを使用し、バージョンを選択します。

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


<!-- ==================================== End BETA content ====================================================== -->


<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

**API のバージョン 2.0 では関係ないですか?**右上のコントロールを使用し、使用バージョンを選択します。

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->




<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

**API の v1.0 では関係ないですか?**右上のコントロールを使用し、使用バージョンを選択します。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->
 
 
 
## <a name="all-calendar-api-operations"></a>カレンダー API のすべての操作

<a name="EventOperations"></a>
イベントの**イベント処理**は、予定またはユーザーの予定表で会議を表します。イベント (定期的なイベントの場合) の系列のマスター、発生、1 つのインスタンス、または例外を使用できます。

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

[イベントを取得](#GetEvents) | [同期イベント](#SyncCalendarView) | [会議の時刻を検索する (プレビュー)](#FindMeetingTimesPreview) | [作成イベント](#CreateEvents) | 
[更新イベント](#UpdateEvents) | [イベントに応答](#RespndToEvents) | [イベントを削除](#DeleteEvents) | [(プレビュー) のイベントをキャンセル](#CancelEvents) | 
[添付ファイルを取得する](#GetAttachments) | [を作成する添付ファイル](#CreateAttachments) | [添付ファイルを削除](#DeleteAttachments) | 
[アラームを取得](#GetReminders) | [アラームの再通知](#SnoozeReminders)] |[アラームのアラームを消す](#DismissReminders)


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->



<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

[イベントを取得](#GetEvents) | [同期イベント](#SyncCalendarView) | [作成イベント](#CreateEvents) | 
[イベントを更新](#UpdateEvents) | [イベントに応答](#RespndToEvents) | [イベントを削除](#DeleteEvents) | 
[添付ファイルを取得する](#GetAttachments) | [を作成する添付ファイル](#CreateAttachments) | [添付ファイルを削除](#DeleteAttachments) | 
[のアラーム](#GetReminders) | [アラームの再通知](#SnoozeReminders)] |[アラームのアラームを消す](#DismissReminders)


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->


[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

[イベントを取得](#GetEvents) | [同期イベント](#SyncCalendarView) | [作成イベント](#CreateEvents) | 
[イベントを更新](#UpdateEvents) | [イベントに応答](#RespndToEvents) | [イベントを削除](#DeleteEvents) | 
[添付ファイルを取得する](#GetAttachments) | [を作成する添付ファイル](#CreateAttachments) | [添付ファイルを削除](#DeleteAttachments) | 
[のアラーム](#GetReminders) | [アラームの再通知](#SnoozeReminders)] |[アラームのアラームを消す](#DismissReminders)

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->




<a name="CalendarOperations"> </a>
**予定表の操作**カレンダーは、イベント用のコンテナーとして機能します。ユーザーは、複数の予定表を持つことができます。、Office 365 で予定表のグループに各カレンダーを割り当てることができます。

[カレンダーを取得する](#GetCalendars) | [を作成する予定表](#CreateCalendars) | [予定表を更新](#UpdateCalendars) | [の予定表を削除](#DeleteCalendars) 

<a name="CalendarGroupOperations"></a>
グループの予定表の**予定表グループの操作**は、複数の予定表を整理する方法です。ユーザーは、Outlook または Outlook Web App 内の 1 つの予定表グループに複数の予定表を追加できます。これにより、グループ内のすべての予定表をすばやく表示するのにはユーザーが容易になります。


**メモ**Outlook.com がアクセス可能な既定の予定表のグループのみがサポートされています、`../me/calendars`のショートカットです。その予定表グループを削除したり、別の予定表グループを作成できません。


[予定表グループを取得する](#GetCalendarGroups) | [を作成する予定表グループ](#CreateCalendarGroups) | 
[グループの予定表を更新](#UpdateCalendarGroups) | [カレンダー グループを削除](#DeleteCalendarGroups)  

参照してください。

[REST API イベントのリソース](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) | 
[カレンダー リソースの REST API](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource) |
[REST API の予定表グループのリソース](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource)



<a name="Overview"> </a>
## <a name="using-the-calendar-rest-api"></a>カレンダー REST API を使用してください。

### <a name="authentication"></a>認証

他の[Outlook の他の API](..\api\use-outlook-rest-api.md#DefineOutlookRESTAPI)、カレンダー API へのすべての要求のように、有効なアクセス トークンを含める必要があります。アクセス トークンを取得するには、登録されていると、アプリケーションを識別し、適切な承認を取得する必要があります。一部簡素化された登録および承認オプションについての[詳細を確認](..\api\use-outlook-rest-api.md#ShortRegAuthWorkflow)できます。カレンダー API では、特定の操作を続行するには、この点に留意してください。

<a name="SupportedVersions"> </a>

###<a name="version-of-api"></a>API のバージョン

カレンダーの REST API は、Outlook の REST API のすべてのバージョンでサポートされてです。機能は、特定のバージョンによって異なる場合があります。

###<a name="target-user"></a>ターゲット ユーザー

カレンダー API 要求は、現在のユーザーに代わって実行されます。 

Outlook REST API の詳細についてはすべてのサブセットに一般的な[Outlook の REST API の使用](..\api\use-outlook-rest-api.md)を参照してください。

****

<a name="GetEvents"> </a>
## <a name="get-events"></a>イベントを取得します。

イベントの収集、またはイベントを取得します。 

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

カレンダー イベントを取得するすべての操作を使用できます、_選択: outlook.timezone_応答の開始と終了の時刻のタイム ゾーンを指定する HTTP ヘッダー。たとえば、次_選択: outlook.timezone_ヘッダーは、東部標準時への応答で、開始時刻と終了時刻を設定します。

```
Prefer: outlook.timezone="Eastern Standard Time"
``` 

指定しない場合、_選択: outlook.timezone_応答の開始と終了時刻が UTC で返されるヘッダー。

_イベント_のリソースに、 _OriginalStartTimeZone_プロパティと_OriginalEndTimeZone_プロパティを使用するにはイベントが作成されたときに使用するタイム ゾーンを確認します。

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->
<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

カレンダー イベントを取得するすべての操作を使用できます、_選択: outlook.timezone_応答の開始と終了の時刻のタイム ゾーンを指定する HTTP ヘッダー。たとえば、次_選択: outlook.timezone_ヘッダーは、東部標準時への応答で、開始時刻と終了時刻を設定します。

```
Prefer: outlook.timezone="Eastern Standard Time"
``` 

指定しない場合、_選択: outlook.timezone_応答の開始と終了時刻が UTC で返されるヘッダー。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。 

_イベント_のリソースに、 _OriginalStartTimeZone_プロパティと_OriginalEndTimeZone_プロパティを使用するにはイベントが作成されたときに使用するタイム ゾーンを確認します。

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->


REST API: の[予定表ビュー (残りの部分) を取得します。](#GetCalendarView) |  
[シリーズのマスターと 1 つのイベント (REST)](#GetEventCollection) |
 [(REST) イベントのインスタンスを取得する](#GetEventInstances) | [イベント (残りの部分) を取得します。](#GetEvent) 

クライアント ライブラリ:[ユーザーの予定表 (クライアント) からのイベントを取得します。](#GetEventsClient)

****

<a name="GetCalendarView"> </a>
###<a name="get-a-calendar-view-rest"></a>予定表ビュー (残りの部分) を取得します。 

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

ユーザーのプライマリの予定表からの時間の範囲で定義されている予定表ビューで出現する、例外、およびイベントの 1 つのインスタンスを取得 (`../me/calendarview`) または別のカレンダーからです。
   

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
GET https://outlook.office.com/api/beta/me/calendars/{calendar_id}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントの既定のタイム ゾーンです。|
|_URL パラメーター_|
|calendar_id|string|カレンダー ID、特定の予定表から予定表ビューを取得している場合です。|
|start_datetime|datetimeoffset|日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|日付と時刻、イベントが終了します。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、開始時刻と終了時刻は UTC で返されます。

**メモ**既定では、応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

たとえば、各イベントの件名のプロパティのみを返す 10 月の月間予定表ビューを取得します。仮定すると、_選択: outlook.timezone_ヘッダーが要求に含まれていない、タイム ゾーンは UTC です。 

```
GET https://outlook.office.com/api/beta/me/calendarview?startDateTime=2014-10-01T01:00:00Z&endDateTime=2014-10-31T23:00:00Z&$select=Subject
```

 **応答の種類**

指定した時間範囲内で展開されている[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->


<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v2.0/me/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
GET https://outlook.office.com/api/v2.0/me/calendars/{calendar_id}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントの既定のタイム ゾーンです。|
|_URL パラメーター_|
|calendar_id|string|カレンダー ID、特定の予定表から予定表ビューを取得している場合です。|
|start_datetime|datetimeoffset|日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|日付と時刻、イベントが終了します。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、開始時刻と終了時刻は UTC で返されます。

**メモ**既定では、応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

たとえば、各イベントの件名のプロパティのみを返す 10 月の月間予定表ビューを取得します。仮定すると、_選択: outlook.timezone_ヘッダーが要求に含まれていない、タイム ゾーンは UTC です。 

```
GET https://outlook.office.com/api/v2.0/me/calendarview?startDateTime=2014-10-01T01:00:00&endDateTime=2014-10-31T23:00:00&$select=Subject
```

 **応答の種類**

指定した時間範囲内で展開されている[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/calendarview?start={start_datetime}&end={end_datetime}
GET https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダー ID、特定の予定表から予定表ビューを取得している場合です。|
|start_datetime|datetimeoffset|日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|日付と時刻、イベントが終了します。|

**メモ**既定では、応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

10 月の月間予定表ビューをたとえば、取得する各イベントの件名のプロパティのみを返します。 

```
GET https://outlook.office.com/api/v1.0/me/calendarview?startDateTime=2014-10-01T01:00:00Z&endDateTime=2014-10-31T23:00:00Z&$select=Subject
```

 **応答の種類**

指定した時間範囲内で展開されている[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->


****

<a name="GetEventCollection"> </a>
###<a name="get-series-master-and-single-events-rest"></a>シリーズのマスターと 1 つのイベント (残りの部分) を取得します。 

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

ユーザーのプライマリの予定表からシリーズのマスターと 1 つのインスタンスのイベントのコレクションを取得する (`../me/events`) または別のカレンダーからです。拡張されたイベントのインスタンスを取得するには、 [予定表ビューを取得する](#GetCalendarView)か、[イベントのインスタンスを取得する](#GetEventInstances)ことができます。



<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
GET https://outlook.office.com/api/beta/me/events
GET https://outlook.office.com/api/beta/me/calendars/{calendar_id}/events
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_Header パラメーター|
|希望します。|outlook.timezone|応答内のイベントの既定のタイム ゾーンです。|
|_URL パラメーター_|
|calendar_id|string|カレンダー ID、特定の予定表からイベントを取得している場合です。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定しない場合、開始時刻と終了時刻が UTC で返されます。

**メモ**応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。次の使用例を参照してください。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

**$Select**を使用して応答の各イベントの**件名**、**開催者**、**開始**および**終了**のプロパティのみを返すことを指定するのには次の例を次に示します。**$Select**を使用しない場合、イベントに返されるプロパティの完全なリストの[イベント (残りの部分) を取得](#GetEvent)することで最初のサンプル応答を参照してください。


**要求のサンプル**

```
GET https://outlook.office.com/api/beta/me/events?$select=Subject,Organizer,Start,End
```

**応答の例**

状態コード: 200

```
{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events(Subject,Organizer,Start,End)",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI28tEyDAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAA/LpDWw==\"",
            "Id": "AAMkAGI28tEyDAAA=",
            "Subject": "Scrum",
            "Start": {
                "DateTime": "2015-11-02T17:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2015-11-02T17:30:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "user0TestUser",
                    "Address": "user0@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI28tEyCAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAA/LpDWg==\"",
            "Id": "AAMkAGI28tEyCAAA=",
            "Subject": "team lunch",
            "Start": {
                "DateTime": "2015-11-02T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2015-11-03T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "user0TestUser",
                    "Address": "user0@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2ADTG93AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x49w==\"",
            "Id": "AAMkAGI2G93AAA=",
            "Subject": "Weekly Meeting on Contoso Project",
            "Start": {
                "DateTime": "2014-10-13T21:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-10-13T22:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG92AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x49g==\"",
            "Id": "AAMkAGI2TG92AAA=",
            "Subject": "Daily Team Meeting",
            "Start": {
                "DateTime": "2014-10-13T18:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-10-13T18:30:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG91AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x47Q==\"",
            "Id": "AAMkAGI2TG91AAA=",
            "Subject": "Rob:Alex 1:1",
            "Start": {
                "DateTime": "2014-10-15T16:30:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-10-15T17:30:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG90AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x46g==\"",
            "Id": "AAMkAGI2TG90AAA=",
            "Subject": "Thanksgiving Holiday",
            "Start": {
                "DateTime": "2015-11-26T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2015-11-27T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG9zAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x46Q==\"",
            "Id": "AAMkAGI2TG9zAAA=",
            "Subject": "Thanksgiving Holiday",
            "Start": {
                "DateTime": "2014-11-27T00:00:00"
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-11-28T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG9yAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x49Q==\"",
            "Id": "AAMkAGI2TG9yAAA=",
            "Subject": "New Year's Day Holiday",
            "Start": {
                "DateTime": "2015-01-01T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2015-01-02T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG9xAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x45w==\"",
            "Id": "AAMkAGI2TG9xAAA=",
            "Subject": "Christmas Holiday",
            "Start": {
                "DateTime": "2014-12-25T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-12-26T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        }
    ]
}
```

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->


<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v2.0/me/events
GET https://outlook.office.com/api/v2.0/me/calendars/{calendar_id}/events
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントの既定のタイム ゾーンです。|
|_URL パラメーター_|
|calendar_id|string|カレンダー ID、特定の予定表からイベントを取得している場合です。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、開始時刻と終了時刻は UTC で返されます。

**メモ**応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。次の使用例を参照してください。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

**$Select**を使用して応答の各イベントの**件名**、**開催者**、**開始**および**終了**のプロパティのみを返すことを指定するのには次の例を次に示します。**$Select**を使用しない場合、イベントに返されるプロパティの完全なリストの[イベント (残りの部分) を取得](#GetEvent)することで最初のサンプル応答を参照してください。


**要求のサンプル**

```
GET https://outlook.office.com/api/v2.0/me/events?$select=Subject,Organizer,Start,End
```

**応答の例**

```
{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events(Subject,Organizer,Start,End)",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI28tEyDAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAA/LpDWw==\"",
            "Id": "AAMkAGI28tEyDAAA=",
            "Subject": "Scrum",
            "Start": {
                "DateTime": "2015-11-02T17:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2015-11-02T17:30:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "user0TestUser",
                    "Address": "user0@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI28tEyCAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAA/LpDWg==\"",
            "Id": "AAMkAGI28tEyCAAA=",
            "Subject": "team lunch",
            "Start": {
                "DateTime": "2015-11-02T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2015-11-03T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "user0TestUser",
                    "Address": "user0@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2ADTG93AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x49w==\"",
            "Id": "AAMkAGI2G93AAA=",
            "Subject": "Weekly Meeting on Contoso Project",
            "Start": {
                "DateTime": "2014-10-13T21:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-10-13T22:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG92AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x49g==\"",
            "Id": "AAMkAGI2TG92AAA=",
            "Subject": "Daily Team Meeting",
            "Start": {
                "DateTime": "2014-10-13T18:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-10-13T18:30:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG91AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x47Q==\"",
            "Id": "AAMkAGI2TG91AAA=",
            "Subject": "Rob:Alex 1:1",
            "Start": {
                "DateTime": "2014-10-15T16:30:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": "2014-10-15T17:30:00Z",
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG90AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x46g==\"",
            "Id": "AAMkAGI2TG90AAA=",
            "Subject": "Thanksgiving Holiday",
            "Start": {
                "DateTime": "2015-11-26T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2015-11-27T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG9zAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x46Q==\"",
            "Id": "AAMkAGI2TG9zAAA=",
            "Subject": "Thanksgiving Holiday",
            "Start": {
                "DateTime": "2014-11-27T00:00:00"
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-11-28T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG9yAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x49Q==\"",
            "Id": "AAMkAGI2TG9yAAA=",
            "Subject": "New Year's Day Holiday",
            "Start": {
                "DateTime": "2015-01-01T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2015-01-02T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG9xAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x45w==\"",
            "Id": "AAMkAGI2TG9xAAA=",
            "Subject": "Christmas Holiday",
            "Start": {
                "DateTime": "2014-12-25T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "End": {
                "DateTime": "2014-12-26T00:00:00",
                "TimeZone": "Pacific Standard Time"
            },
            "Organizer": {
                "EmailAddress": {
                    "Name": "Alex D",
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com"
                }
            }
        }
    ]
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/events
GET https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}/events
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダー ID、特定の予定表からイベントを取得している場合です。|

**メモ**応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。次の使用例を参照してください。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

**$Select**を使用して応答の各イベントの**件名**、**開催者**、**開始**および**終了**のプロパティのみを返すことを指定するのには次の例を次に示します。**$Select**を使用しない場合、イベントに返されるプロパティの完全なリストの[イベント (残りの部分) を取得](#GetEvent)することで最初のサンプル応答を参照してください。


```REST-i
{
   "method": "GET",
   "resourceFormat": "https://outlook.office.com/api/v1.0/me/events?$select=Subject,Organizer,Start,End",
   "requestUrl": "https://outlook.office.com/api/v1.0/me/events?$select=Subject,Organizer,Start,End",
   "requestHeaders": {
      "Accept": "application/json"
   },
   "parameterDetails": [],
   "statusCode": 200,
   "responseBody": {
    "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/Events",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG93AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x48w==\"",
            "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG93AAA=",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x48w==",
            "Categories": [],
            "DateTimeCreated": "2014-10-19T23:13:47.3959685Z",
            "DateTimeLastModified": "2014-10-19T23:13:47.6772234Z",
            "Subject": "Weekly Meeting on Contoso Project",
            "BodyPreview": "Setting up some time to review the budget and planning on the Contoso Project",
            "Body": {
                "ContentType": "HTML",
                "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nSetting up some time to review the budget and planning on the Contoso Project\r\n</body>\r\n</html>\r\n"
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": "2014-10-13T21:00:00Z",
            "StartTimeZone": "Pacific Standard Time",
            "End": "2014-10-13T22:00:00Z",
            "EndTimeZone": "Pacific Standard Time",           
            "Location": {
                "DisplayName": "Alex's Office"
            },
            "ShowAs": "Busy",
            "IsAllDay": false,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SeriesMaster",
            "SeriesMasterId": null,
            "Attendees": [
                {
                    "EmailAddress": {
                        "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
                        "Name": "Janet Schorr"
                    },
                    "Status": {
                        "Response": "None",
                        "Time": "0001-01-01T00:00:00Z"
                    },
                    "Type": "Required"
                },
                {
                    "EmailAddress": {
                        "Address": "pavelb@a830edad9050849NDA1.onmicrosoft.com",
                        "Name": "Pavel Bansky"
                    },
                    "Status": {
                        "Response": "None",
                        "Time": "0001-01-01T00:00:00Z"
                    },
                    "Type": "Required"
                }
            ],
            "Recurrence": {
                "Pattern": {
                    "Type": "Weekly",
                    "Interval": 1,
                    "Month": 0,
                    "Index": "First",
                    "FirstDayOfWeek": "Sunday",
                    "DayOfMonth": 0,
                    "DaysOfWeek": [
                        "Monday"
                    ]
                },
                "Range": {
                    "Type": "NoEnd",
                    "StartDate": "2014-10-13T00:00:00-07:00",
                    "EndDate": "0001-01-01T00:00:00Z",
                    "NumberOfOccurrences": 0
                }
            },
            "Organizer": {
                "EmailAddress": {
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Alex D"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG92AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x48A==\"",
            "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG92AAA=",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x48A==",
            "Categories": [],
            "DateTimeCreated": "2014-10-19T23:13:01.9733945Z",
            "DateTimeLastModified": "2014-10-19T23:13:02.426753Z",
            "Subject": "Daily Team Meeting",
            "BodyPreview": "Daily sync on project progress and team member status",
            "Body": {
                "ContentType": "HTML",
                "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nDaily sync on project progress and team member status\r\n</body>\r\n</html>\r\n"
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": "2014-10-13T18:00:00Z",
            "StartTimeZone": "Pacific Standard Time",
            "End": "2014-10-13T18:30:00Z",
            "EndTimeZone": "Pacific Standard Time",            
            "Location": {
                "DisplayName": "Team Room"
            },
            "ShowAs": "Busy",
            "IsAllDay": false,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SeriesMaster",
            "SeriesMasterId": null,
            "Attendees": [
                {
                    "EmailAddress": {
                        "Address": "roby@a830edad9050849NDA1.onmicrosoft.com",
                        "Name": "Rob Young"
                    },
                    "Status": {
                        "Response": "None",
                        "Time": "0001-01-01T00:00:00Z"
                    },
                    "Type": "Required"
                },
                {
                    "EmailAddress": {
                        "Address": "pavelb@a830edad9050849NDA1.onmicrosoft.com",
                        "Name": "Pavel Bansky"
                    },
                    "Status": {
                        "Response": "None",
                        "Time": "0001-01-01T00:00:00Z"
                    },
                    "Type": "Required"
                },
                {
                    "EmailAddress": {
                        "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
                        "Name": "Janet Schorr"
                    },
                    "Status": {
                        "Response": "None",
                        "Time": "0001-01-01T00:00:00Z"
                    },
                    "Type": "Required"
                },
                {
                    "EmailAddress": {
                        "Address": "garthf@a830edad9050849NDA1.onmicrosoft.com",
                        "Name": "Garth Fort"
                    },
                    "Status": {
                        "Response": "None",
                        "Time": "0001-01-01T00:00:00Z"
                    },
                    "Type": "Required"
                },
                {
                    "EmailAddress": {
                        "Address": "katiej@a830edad9050849NDA1.onmicrosoft.com",
                        "Name": "Katie Jordan"
                    },
                    "Status": {
                        "Response": "None",
                        "Time": "0001-01-01T00:00:00Z"
                    },
                    "Type": "Required"
                }
            ],
            "Recurrence": {
                "Pattern": {
                    "Type": "Weekly",
                    "Interval": 1,
                    "Month": 0,
                    "Index": "First",
                    "FirstDayOfWeek": "Sunday",
                    "DayOfMonth": 0,
                    "DaysOfWeek": [
                        "Monday",
                        "Tuesday",
                        "Wednesday",
                        "Thursday",
                        "Friday"
                    ]
                },
                "Range": {
                    "Type": "NoEnd",
                    "StartDate": "2014-10-13T00:00:00-07:00",
                    "EndDate": "0001-01-01T00:00:00Z",
                    "NumberOfOccurrences": 0
                }
            },
            "Organizer": {
                "EmailAddress": {
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Alex D"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG91AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x47Q==\"",
            "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG91AAA=",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x47Q==",
            "Categories": [],
            "DateTimeCreated": "2014-10-19T23:12:40.7543183Z",
            "DateTimeLastModified": "2014-10-19T23:12:41.0043215Z",
            "Subject": "Rob:Alex 1:1",
            "BodyPreview": "Let's meet every month to engage in project review and career discussion",
            "Body": {
                "ContentType": "HTML",
                "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<style type=\"text/css\" style=\"display:none\"><!-- p { margin-top: 0px; margin-bottom: 0px; }--></style>\r\n</head>\r\n<body dir=\"ltr\" style=\"font-size:12pt;color:#000000;background-color:#FFFFFF;font-family:Calibri,Arial,Helvetica,sans-serif;\">\r\n<p>Let's meet every month to engage in project review and career discussion<br>\r\n</p>\r\n</body>\r\n</html>\r\n"
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": "2014-10-15T16:30:00Z",
            "StartTimeZone": "Pacific Standard Time",            
            "End": "2014-10-15T17:30:00Z",
            "EndTimeZone": "Pacific Standard Time",                      
            "Location": {
                "DisplayName": "Alex's Office"
            },
            "ShowAs": "Busy",
            "IsAllDay": false,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SeriesMaster",
            "SeriesMasterId": null,
            "Attendees": [
                {
                    "EmailAddress": {
                        "Address": "roby@a830edad9050849NDA1.onmicrosoft.com",
                        "Name": "Rob Young"
                    },
                    "Status": {
                        "Response": "None",
                        "Time": "0001-01-01T00:00:00Z"
                    },
                    "Type": "Required"
                }
            ],
            "Recurrence": {
                "Pattern": {
                    "Type": "RelativeMonthly",
                    "Interval": 1,
                    "Month": 0,
                    "Index": "Third",
                    "FirstDayOfWeek": "Sunday",
                    "DayOfMonth": 0,
                    "DaysOfWeek": [
                        "Wednesday"
                    ]
                },
                "Range": {
                    "Type": "NoEnd",
                    "StartDate": "2014-10-15T00:00:00-07:00",
                    "EndDate": "0001-01-01T00:00:00Z",
                    "NumberOfOccurrences": 0
                }
            },
            "Organizer": {
                "EmailAddress": {
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Alex D"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG90AAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x46g==\"",
            "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG90AAA=",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x46g==",
            "Categories": [],
            "DateTimeCreated": "2014-10-19T08:48:13.6271741Z",
            "DateTimeLastModified": "2014-10-19T08:48:13.6427985Z",
            "Subject": "Thanksgiving Holiday",
            "BodyPreview": "",
            "Body": {
                "ContentType": "HTML",
                "Content": ""
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": "2015-11-26T00:00:00Z",
            "StartTimeZone": "Pacific Standard Time",
            "End": "2015-11-27T00:00:00Z",
            "EndTimeZone": "Pacific Standard Time",            
            "Location": {
                "DisplayName": ""
            },
            "ShowAs": "Free",
            "IsAllDay": true,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SingleInstance",
            "SeriesMasterId": null,
            "Attendees": [],
            "Recurrence": null,
            "Organizer": {
                "EmailAddress": {
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Alex D"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9zAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x46Q==\"",
            "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9zAAA=",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x46Q==",
            "Categories": [],
            "DateTimeCreated": "2014-10-19T08:46:18.8700566Z",
            "DateTimeLastModified": "2014-10-19T08:46:18.8856803Z",
            "Subject": "Thanksgiving Holiday",
            "BodyPreview": "",
            "Body": {
                "ContentType": "HTML",
                "Content": ""
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": "2014-11-27T00:00:00Z",
            "StartTimeZone": "Pacific Standard Time",
            "End": "2014-11-28T00:00:00Z",
            "EndTimeZone": "Pacific Standard Time",            
            "Location": {
                "DisplayName": ""
            },
            "ShowAs": "Free",
            "IsAllDay": true,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SingleInstance",
            "SeriesMasterId": null,
            "Attendees": [],
            "Recurrence": null,
            "Organizer": {
                "EmailAddress": {
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Alex D"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x46A==\"",
            "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAA=",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x46A==",
            "Categories": [],
            "DateTimeCreated": "2014-10-19T08:43:37.2138006Z",
            "DateTimeLastModified": "2014-10-19T08:43:37.2450436Z",
            "Subject": "New Year's Day Holiday",
            "BodyPreview": "",
            "Body": {
                "ContentType": "HTML",
                "Content": ""
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": "2015-01-01T00:00:00Z",
            "StartTimeZone": "Pacific Standard Time",            
            "End": "2015-01-02T00:00:00Z",
            "EndTimeZone": "Pacific Standard Time",            
            "Location": {
                "DisplayName": ""
            },
            "ShowAs": "Free",
            "IsAllDay": true,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SingleInstance",
            "SeriesMasterId": null,
            "Attendees": [],
            "Recurrence": null,
            "Organizer": {
                "EmailAddress": {
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Alex D"
                }
            }
        },
        {
            "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9xAAA=')",
            "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x45w==\"",
            "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9xAAA=",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x45w==",
            "Categories": [],
            "DateTimeCreated": "2014-10-19T08:33:45.1538198Z",
            "DateTimeLastModified": "2014-10-19T08:33:45.200696Z",
            "Subject": "Christmas Holiday",
            "BodyPreview": "",
            "Body": {
                "ContentType": "HTML",
                "Content": ""
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": "2014-12-25T00:00:00Z",
            "StartTimeZone": "Pacific Standard Time",            
            "End": "2014-12-26T00:00:00Z",
            "EndTimeZone": "Pacific Standard Time",            
            "Location": {
                "DisplayName": ""
            },
            "ShowAs": "Free",
            "IsAllDay": true,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SingleInstance",
            "SeriesMasterId": null,
            "Attendees": [],
            "Recurrence": null,
            "Organizer": {
                "EmailAddress": {
                    "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Alex D"
                }
            }
        }
    ]
}
}

```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->

****


<a name="GetEventInstances"></a>
###<a name="get-event-instances-rest"></a>(REST) イベントのインスタンスを取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

指定の時間範囲のイベントのインスタンス (文字列) を取得できます。イベントが**SeriesMaster**型の場合が返されます、出現するイベントの例外の時間の範囲内。


<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントのデフォルトのタイム ゾーンです。|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|start_datetime|datetimeoffset|UTC 日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|UTC 日付と時刻、イベントが終了します。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、開始時刻と終了時刻は UTC で返されます。

 **応答の種類**

要求された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)のコレクションです。

**メモ**既定では、応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。  
フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

たとえば、10 月の月の特定のイベントのインスタンスを取得する、**件名**、**開始**と**終了**の各インスタンス プロパティのみが含まれます。 

<!--don't use httprequest for this because it renders as lowercase, which breaks the call-->
```
GET https://outlook.office.com/api/beta/me/events/AAMkAGE0MGM1Y2M5LWEAAA=/instances?startDateTime=2014-10-01T01:00:00Z&endDateTime=2014-10-31T23:00:00Z&$select=Subject,Start,End
```



[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->


<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v2.0/me/events/{event_id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントの既定のタイム ゾーンです。|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|start_datetime|datetimeoffset|UTC 日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|UTC 日付と時刻、イベントが終了します。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、開始時刻と終了時刻は UTC で返されます。

 **応答の種類**

要求された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)のコレクションです。

**メモ**既定では、応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。  
フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

たとえば、10 月の月の特定のイベントのインスタンスを取得する、**件名**、**開始**と**終了**の各インスタンス プロパティのみが含まれます。 

<!--don't use httprequest for this because it renders as lowercase, which breaks the call-->
```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGE0MGM1Y2M5LWEAAA=/instances?startDateTime=2014-10-01T01:00:00Z&endDateTime=2014-10-31T23:00:00Z&$select=Subject,Start,End
```



[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->

<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v1.0/me/events/{event_id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|start_datetime|datetimeoffset|UTC 日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|UTC 日付と時刻、イベントが終了します。|


 **応答の種類**

要求された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)のコレクションです。

**メモ**既定では、応答内の各イベントには、すべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。  
フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

たとえば、10 月の月の特定のイベントのインスタンスを取得する、**件名**、**開始**と**終了**の各インスタンス プロパティのみが含まれます。 

<!--don't use httprequest for this because it renders as lowercase, which breaks the call-->
```
GET https://outlook.office.com/api/v1.0/me/events/AAMkAGE0MGM1Y2M5LWEAAA=/instances?startDateTime=2014-10-01T01:00:00Z&endDateTime=2014-10-31T23:00:00Z&$select=Subject,Start,End
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->

****


<a name="GetEvent"> </a>
###<a name="get-an-event-rest"></a>(REST) イベントを取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

ID によってイベントを取得します。


<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントのデフォルトのタイム ゾーンです。|
|_URL パラメーター_|
|event_id|string|イベント id です。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、開始時刻と終了時刻は UTC で返されます。

**要求のサンプル**

```
GET https://outlook.office.com/api/beta/me/events/AAMkAGI2TG93AAA=
```

**応答の例**

```
    {
        "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events/$entity",
        "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG93AAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x48w==\"",
        "Id": "AAMkAGI2TG93AAA=",
        "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x48w==",
        "Categories": [],
        "CreatedDateTime": "2014-10-19T23:13:47.3959685Z",
        "LastModifiedDateTime": "2014-10-19T23:13:47.6772234Z",
        "Subject": "Weekly Meeting on Contoso Project",
        "BodyPreview": "Setting up some time to review the budget and planning on the Contoso Project",
        "Body": {
            "ContentType": "HTML",
            "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nSetting up some time to review the budget and planning on the Contoso Project\r\n</body>\r\n</html>\r\n"
        },
        "Importance": "Normal",
        "HasAttachments": false,
        "Start": {
            "DateTime": "2014-10-13T21:00:00",
            "TimeZone": "Pacific Standard Time"
        },
        "End": {
            "DateTime": "2014-10-13T22:00:00",
            "TimeZone": ""Pacific Standard Time"
        },        
        "Location": {
            "DisplayName": "Alex's Office",
            "Address": null,
            "Coordinates": null,
            "LocationEmailAddress": "",
            "LocationUri": ""
        },
        "ShowAs": "Busy",
        "IsAllDay": false,
        "IsCancelled": false,
        "IsOrganizer": true,
        "ResponseRequested": true,
        "Type": "SeriesMaster",
        "SeriesMasterId": null,
        "Attendees": [
            {
                "EmailAddress": {
                    "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Janet Schorr"
                },
                "Status": {
                    "Response": "None",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "Type": "Required"
            },
            {
                "EmailAddress": {
                    "Address": "pavelb@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Pavel Bansky"
                },
                "Status": {
                    "Response": "None",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "Type": "Required"
            }
        ],
        "Recurrence": {
            "Pattern": {
                "Type": "Weekly",
                "Interval": 1,
                "Month": 0,
                "Index": "First",
                "FirstDayOfWeek": "Sunday",
                "DayOfMonth": 0,
                "DaysOfWeek": [
                    "Monday"
                ]
            },
            "RecurrenceTimeZone": "Pacific Standard Time",
            "Range": {
                "Type": "NoEnd",
                "StartDate": "2014-10-13",
                "EndDate": "2014-11-13",
                "NumberOfOccurrences": 0
            }
        },
        "OriginalEndTimeZone": "Pacific Standard Time",
        "OriginalStartTimeZone": "Pacific Standard Time",
        "Organizer": {
            "EmailAddress": {
                "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                "Name": "Alex D"
            }
        },
        "OnlineMeetingUrl": null
    }
```


**応答の種類**

要求された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。

**メモ**既定では、応答には、イベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

**$Select**を使用して、**件名**、**開催者**、**開始**および**終了**イベントのプロパティのみを返すことを指定するには次の例を次に示します。 


**要求のサンプル**

```
GET https://outlook.office.com/api/beta/me/events/AAMkAGI2TG93AAA=?$select=Subject,Organizer,Start,End
```

**応答の例**

```
    {
        "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events/$entity",
        "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG93AAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x48w==\"",
        "Id": "AAMkAGI2TG93AAA=",
        "Subject": "Weekly Meeting on Contoso Project",
        "Start": {
            "DateTime": "2014-10-13T21:00:00",
            "TimeZone": "Pacific Standard Time"
        },
        "End": {
            "DateTime": "2014-10-13T22:00:00",
            "TimeZone": ""Pacific Standard Time"
        }, 
        "Organizer": {
            "EmailAddress": {
                "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                "Name": "Alex D"
            }
        }
    }
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->

<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v2.0/me/events/{event_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントの既定のタイム ゾーンです。|
|_URL パラメーター_|
|event_id|string|イベント id です。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、開始時刻と終了時刻は UTC で返されます。

**要求のサンプル**

```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGI2TG93AAA=
```

**応答の例**

```
    {
        "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events/$entity",
        "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG93AAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x48w==\"",
        "Id": "AAMkAGI2TG93AAA=",
        "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x48w==",
        "Categories": [],
        "CreatedDateTime": "2014-10-19T23:13:47.3959685Z",
        "LastModifiedDateTime": "2014-10-19T23:13:47.6772234Z",
        "Subject": "Weekly Meeting on Contoso Project",
        "BodyPreview": "Setting up some time to review the budget and planning on the Contoso Project",
        "Body": {
            "ContentType": "HTML",
            "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nSetting up some time to review the budget and planning on the Contoso Project\r\n</body>\r\n</html>\r\n"
        },
        "Importance": "Normal",
        "HasAttachments": false,
        "Start": {
            "DateTime": "2014-10-13T21:00:00",
            "TimeZone": "Pacific Standard Time"
        },
        "End": {
            "DateTime": "2014-10-13T22:00:00",
            "TimeZone": ""Pacific Standard Time"
        },        
        "Location": {
            "DisplayName": "Alex's Office",
            "Address": null
        },
        "ShowAs": "Busy",
        "IsAllDay": false,
        "IsCancelled": false,
        "IsOrganizer": true,
        "ResponseRequested": true,
        "Type": "SeriesMaster",
        "SeriesMasterId": null,
        "Attendees": [
            {
                "EmailAddress": {
                    "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Janet Schorr"
                },
                "Status": {
                    "Response": "None",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "Type": "Required"
            },
            {
                "EmailAddress": {
                    "Address": "pavelb@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Pavel Bansky"
                },
                "Status": {
                    "Response": "None",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "Type": "Required"
            }
        ],
        "Recurrence": {
            "Pattern": {
                "Type": "Weekly",
                "Interval": 1,
                "Month": 0,
                "Index": "First",
                "FirstDayOfWeek": "Sunday",
                "DayOfMonth": 0,
                "DaysOfWeek": [
                    "Monday"
                ]
            },
            "RecurrenceTimeZone": "Pacific Standard Time",
            "Range": {
                "Type": "NoEnd",
                "StartDate": "2014-10-13",
                "EndDate": "2014-11-13",
                "NumberOfOccurrences": 0
            }
        },
        "OriginalEndTimeZone": "Pacific Standard Time",
        "OriginalStartTimeZone": "Pacific Standard Time",
        "Organizer": {
            "EmailAddress": {
                "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                "Name": "Alex D"
            }
        }
    }
```


**応答の種類**

要求された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。

**メモ**既定では、応答には、イベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

**$Select**を使用して、**件名**、**開催者**、**開始**および**終了**イベントのプロパティのみを返すことを指定するには次の例を次に示します。 

**要求のサンプル**

```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGI2TG93AAA=?$select=Subject,Organizer,Start,End
```

**応答の例**

```
    {
        "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events/$entity",
        "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2TG93AAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x48w==\"",
        "Id": "AAMkAGI2TG93AAA=",
        "Subject": "Weekly Meeting on Contoso Project",
        "Start": {
            "DateTime": "2014-10-13T21:00:00",
            "TimeZone": "Pacific Standard Time"
        },
        "End": {
            "DateTime": "2014-10-13T22:00:00",
            "TimeZone": ""Pacific Standard Time"
        }, 
        "Organizer": {
            "EmailAddress": {
                "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                "Name": "Alex D"
            }
        }
    }
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->

<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v1.0/me/events/{event_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|

```REST-i
[!INCLUDE [calendar_api_get_event_by_id](./_data/calendar_api_get_event_by_id.json)]
```


**応答の種類**

要求された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。

**メモ**既定では、応答には、イベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

**$Select**を使用して、**件名**、**開催者**、**開始**および**終了**イベントのプロパティのみを返すことを指定するには次の例を次に示します。 

```REST-i
{
    "method": "GET",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/events/{event_id}?$select=Subject,Organizer,Start,End",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/events/AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG93AAA=?$select=Subject,Organizer,Start,End",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "event_id",
            "type": "string",
            "description": "The event ID.",
            "defaultValue": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG93AAA="
        }
    ],
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/Events/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG93AAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x48w==\"",
        "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG93AAA=",
        "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x48w==",
        "Categories": [],
        "DateTimeCreated": "2014-10-19T23:13:47.3959685Z",
        "DateTimeLastModified": "2014-10-19T23:13:47.6772234Z",
        "Subject": "Weekly Meeting on Contoso Project",
        "BodyPreview": "Setting up some time to review the budget and planning on the Contoso Project",
        "Body": {
            "ContentType": "HTML",
            "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nSetting up some time to review the budget and planning on the Contoso Project\r\n</body>\r\n</html>\r\n"
        },
        "Importance": "Normal",
        "HasAttachments": false,
        "Start": "2014-10-13T21:00:00Z",
        "StartTimeZone": "Pacific Standard Time",        
        "End": "2014-10-13T22:00:00Z",
        "EndTimeZone": "Pacific Standard Time",        
        "Location": {
            "DisplayName": "Alex's Office"
        },
        "ShowAs": "Busy",
        "IsAllDay": false,
        "IsCancelled": false,
        "IsOrganizer": true,
        "ResponseRequested": true,
        "Type": "SeriesMaster",
        "SeriesMasterId": null,
        "Attendees": [
            {
                "EmailAddress": {
                    "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Janet Schorr"
                },
                "Status": {
                    "Response": "None",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "Type": "Required"
            },
            {
                "EmailAddress": {
                    "Address": "pavelb@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Pavel Bansky"
                },
                "Status": {
                    "Response": "None",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "Type": "Required"
            }
        ],
        "Recurrence": {
            "Pattern": {
                "Type": "Weekly",
                "Interval": 1,
                "Month": 0,
                "Index": "First",
                "FirstDayOfWeek": "Sunday",
                "DayOfMonth": 0,
                "DaysOfWeek": [
                    "Monday"
                ]
            },
            "Range": {
                "Type": "NoEnd",
                "StartDate": "2014-10-13T00:00:00-07:00",
                "EndDate": "0001-01-01T00:00:00Z",
                "NumberOfOccurrences": 0
            }
        },
        "Organizer": {
            "EmailAddress": {
                "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                "Name": "Alex D"
            }
        }
    }
}
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->

****

<a name="GetEventsClient"></a>
### <a name="get-events-from-the-users-calendar-client"></a>(クライアント) のユーザーの予定表からイベントを取得します。

ユーザーの既定の予定表からイベントを取得します。別の予定表からイベントを取得するには、カレンダーの**イベント**のプロパティを呼び出します。

例:`outlookClient.Me.Calendars[calendarId].Events.ExecuteAsync()`


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


特定のイベントを取得するには、**イベント**コレクションのインデックスとして、イベント ID を指定したり、 **GetById**メソッドを使用できます。

**メモ**イベントのコレクションは、**選択**、**並べ替え**、および**実行**のようなクエリ式をサポートします。

次の使用例は、 [Outlook のサービス クライアントを作成](..\api\use-outlook-rest-api.md#GetClient)するメソッドを呼び出します。

<!-- BEGINSECTION class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar" -->

```cs-i
var outlookClient = await CreateOutlookClientAsync("Calendar");
var events = await outlookClient.Me.Events
  .Take(10)
  .ExecuteAsync();
 
foreach(var calendarEvent in events.CurrentPage)
{
  System.Diagnostics.Debug.WriteLine("Event '{0}'.", calendarEvent.Subject);
}
 
```

```javascript-i
outlookClient.me.events.getEvents().fetch().then(function (result) {
    result.currentPage.forEach(function (event) {
console.log('Event "' + event.subject + '"')
    });
}, function(error) {
    console.log(error);
});
```

<!-- ENDSECTION -->


この呼び出しは、イベントのシリーズ、毎週のチーム ミーティング) などの定期的なイベントの個々 の展開されているインスタンスにないを返します。

イベントのインスタンスのクエリを実行する現在サポートされていません、クライアント ライブラリで。 [カレンダー](..\api\calendar-rest-operations.md#CalendarResource)リソースの**予定表ビュー**のプロパティまたは[イベント](..\api\calendar-rest-operations.md#EventResource)のリソースの**インスタンス**のプロパティを照会するのには、REST API を使用できます。


<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->

<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v2.0/me/events/{event_id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->

<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/events/{event_id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->
 
<!--Update c# example to get instance-->
<!--Update js example and remove note when this works in js-->

****

<a name="SyncCalendarView"> </a>
##<a name="sync-events"></a>同期イベント  

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

同期し、取得、更新、または、ユーザーのプライマリの予定表から指定した時間範囲内のイベントを削除 (`../me/calendarview`) または別のカレンダーからです。このような一連の時間の範囲内のイベントは、予定表ビューとも呼ばれます。返されるイベントには、出現して、一連の定期的なと 1 つのインスタンスの例外があります。 

通常の予定表ビューを同期するには、GET の呼び出しは、それぞれ 2 つ以上の同期要求のラウンドが必要です。予定表ビューを同期する方法と同様に、GET メソッドを使用する[予定表ビューを取得する](#GetCalendarView)には、特定の要求ヘッダーと_deltaToken_や、 _skipToken_該当する場合を含めることを除いて。  

**要求ヘッダー**

- 指定する必要があります、"選択: odata.track の変更」を含むものを除くすべての同期でヘッダーを要求、 `skipToken` 、前回の同期要求に返されます。最初の応答での調査、_優先順位で適用した: odata.track 変更_リソースが開始する前に同期をサポートしていることを確認するヘッダー。(の詳細については、`skipToken`で以下の[2 番目の応答データをサンプル](#SyncCalendarViewSampleSecondResponse)します)。
- 指定すること、"選択: odata.maxpagesize={x}"ヘッダーが返されますを同期するイベントの最大数を示す。

[カレンダー] ビューでイベントを同期する際の一般的なラウンドです。

1. 必須の最初の GET 要求を行う_選択: odata.track 変更_ヘッダー。同期要求に対する初回の応答は、常に、 _deltaToken_を返します。(2 番目およびそれ以降の GET 要求とは異なる最初の GET 要求によって、 _deltaToken_または前の応答で受信した_skipToken_のいずれかを含むします。)

2. 最初の応答が返された場合、_の設定で適用した: odata.track 変更_ヘッダー、同期を続行することができます。

  - 2 つ目の GET 要求を行います。指定、_選択: odata.track 変更_、その他のイベントがあるかどうかを決定する最初の取得からヘッダーと_deltaToken_が返されます。2 番目の要求を返します他のイベントとするか、 _skipToken_がある場合より多くのイベントが利用可能なまたは_deltaToken_を停止する場合、最後のイベントが同期された場合。

  - GET の呼び出しを送信し、前の呼び出しから返される_skipToken_を含む同期を続行します。同期が完了することを示すの_deltaToken_ 、 _@odata.deltaLink_ヘッダーを含む最終的な応答を取得する場合を停止します。

見て初期とそれ以降の呼び出しの構文で同期のラウンドです。

<!-- ==================================== Begin beta content ======================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

**既定のカレンダーで同期するには**

最初の要求。 

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```

2 番目の要求、またはそれ以降のラウンドの最初の要求。

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```

同じラウンドの 3 つ目以降の要求  

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**特定のカレンダーで同期するには**

最初の要求。

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


2 番目の要求、またはそれ以降のラウンドの最初の要求。

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```


同じラウンドの 3 つ目以降の要求:

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**パラメーター**

|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントのデフォルトのタイム ゾーンです。|
|_URL パラメーター_|
|user_context|string|ユーザー コンテキストです。'Me' の値は、現在のユーザーのコンテキストを示すために使用できます。ユーザーを使用することもできます/{upn} 形式が、 **upn**は、ユーザー プリンシパル名には、通常、ユーザーの電子メール アドレスです。|
|calendar_id|string|カレンダー ID、特定の予定表から予定表ビューを取得している場合です。|
|start_datetime|datetimeoffset|日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|日付と時刻、イベントが終了します。|
|delta_token|string|`deltaToken`前の同期応答の @odata.deltaLink の値の一部として文字列が返されます。|
|skip_token|string|`skipToken`前の同期応答の @odata.nextLink の値の一部として文字列が返されます。 |

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、開始時刻と終了時刻は UTC で返されます。

**メモ** 

- 指定するとき」選択: odata.track 変更」最初の要求に応答が同期をサポートしている場合、応答が含まれます」優先で適用した: odata.track 変更"ヘッダーにします。
- 、サポートされていないリソースを同期しようとする場合、または初期同期の要求がない場合は、応答に「優先順位で適用した」ヘッダーは表示されません。
- させると enddatetime クエリのパラメーターを変更することによって時間の変更] ウィンドウを変更できます。  
- 応答内の各イベントには、すべてのプロパティが含まれています。 
- 一連定期的なには同期応答には、定期的なマスターの全体のイベントと例外のイベントが含まれます。 
- 定期的な一連のインスタンスでは、短縮したし、 **Start**および**End**プロパティのみが含まれています。出現イベントについては、定期的なイベントのマスターからの残りの部分をキャプチャすることができます。リファレンス情報については、[イベントのリソース](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)を参照してください。
- $Filter、$count、$select、$skip、$top、および $search のクエリ パラメーターを使用することはできません。 

**応答の種類**

拡張[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)と、指定した時間範囲内でイベントを省略します。

**使用例**

次の例では、ユーザーの既定のカレンダーを同期するのには最初と 2 番目の同期要求を示します。各要求は、一度に 1 つだけの全イベントを返すを指定します。
- 初期の応答が 1 つのイベントを返します、`deltaLink`と`deltaToken`。 
- 2 番目の要求を使用している`deltatoken`。2 番目の応答が 1 つのイベントを返す、`nextLink`と`skipToken`。 

完了するには、同期を使用して、`skipToken`同期応答を返すまでに、前回の同期要求から返される、`deltaLink`と`deltaToken`、同期の現在のラウンドが完了する場合。保存、`deltaToken`の同期は、次のラウンドにします。 

詳細については、 [Outlook の予定表ビューでの同期イベント](..\howto\sync-calendar-view.md)を参照してください。
 
<a name="SyncCalendarViewSampleInitialRequest"></a>

**初期要求のサンプル**

```
    GET https://outlook.office.com/api/beta/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z HTTP/1.1
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
    Prefer: outlook.timezone="Pacific Standard Time"
```

**初期応答のサンプル データ**

```
Preference-Applied: odata.track-changes

    {
        "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/CalendarView",
        "value": [
            {
                "@odata.id": "https://outlook.office.com/api/beta/Users('user0@contoso.com')/Events('asdas==')",
                "@odata.etag": "W/\"L8Z+4Y4u7k+97uRKg==\"",
                "Id": "AQMkANJAAAAA==",
                "ChangeKey": "L8Z+AAAAARKg==",
                "Categories": [
                ],
                "DateTimeCreated": "2015-04-10T17:54:49.2725912Z",
                "DateTimeLastModified": "2015-04-10T17:54:49.3038538Z",
                "Subject": "Discuss the Calendar REST API",
                "BodyPreview": "I think it will meet our requirements!",
                "Body": {
                    "ContentType": "HTML",
                    "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
                },
                "Importance": "Normal",
                "HasAttachments": false,
                "Start": {
                    "DateTime": "2015-04-05T18:00:00",
                    "TimeZone": "Pacific Standard Time"
                }
                "End": {
                    "DateTime": "2015-04-05T19:00:00",
                    "TimeZone": "Pacific Standard Time"
                }
                "ReminderMinutesBeforeStart": "15",
                "IsReminderOn": "true",
                "Location": {
                    "DisplayName": "",
                    "Address": null,
                    "Coordinates": null,
                    "LocationEmailAddress": "",
                    "LocationUri": ""
                },
                "ResponseStatus": {
                    "Response": "Organizer",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "ShowAs": "Busy",
                "IsAllDay": false,
                "IsCancelled": false,
                "IsOrganizer": true,
                "ResponseRequested": true,
                "Type": "SingleInstance",
                "SeriesMasterId": null,
                "Attendees": [
                ],
                "Recurrence": null,
                "OriginalEndTimeZone": "Pacific Standard Time",
                "OriginalStartTimeZone": "Pacific Standard Time",
                "Organizer": {
                    "EmailAddress": {
                        "Address": "user0@contoso.com",
                        "Name": "user0"
                    }
                },
                "iCalUId": "040000008200E9888E07599CCFA23",
                "WebLink": "https://outlook.office.com/owa/?ItemID=AAAINJAAAAA%3D%3D&exvsurl=1&viewmodel=ICalendarItemDetailsViewModelFactory",
                "OnlineMeetingUrl": null
            }
        ],
        "@odata.deltaLink": "https://outlook.office.com/api/beta/me/calendarview/?startdatetime=2015-01-01T00%3a00%3a00Z&enddatetime=2015-04-10T00%3a00%3a00Z&%24deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c"
    }
```

**サンプルの 2 番目の要求**

```
    GET https://outlook.office.com/api/beta/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z&$deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
    Prefer: outlook.timezone="Pacific Standard Time"
```

<a name="SyncCalendarViewSampleSecondResponse"></a>

**応答データの 2 番目の例**

```
{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/CalendarView/$delta",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('user0@contoso.com')/Events('AAMkAD0jAAA=')",
            "@odata.etag": "W/\"P2fd7QAAAAAVFA==\"",
            "Id": "AAMkADNkNmVlOTITVAAAAAA0jAAA=",
            "ChangeKey": "P2fdmIU1QAAAAAVFA==",
            "Categories": [
            ],
            "DateTimeCreated": "2015-04-15T18:59:11.0226221Z",
            "DateTimeLastModified": "2015-04-15T18:59:11.0694979Z",
            "Subject": "1 hour",
            "BodyPreview": "\u200b",
            "Body": {
                "ContentType": "HTML",
                "Content": "<html><body>content</body></html>"
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": {
                "DateTime": "2015-04-16T18:00:00",
                "TimeZone": "Pacific Standard Time"
            }
            "End": {
                "DateTime": "2015-04-16T19:00:00",
                "TimeZone": Pacific Standard Time"
            }
            "ReminderMinutesBeforeStart": "15",
            "IsReminderOn": "true",
            "Location": {
                "DisplayName": "",
                "Address": {
                    "Street": "",
                    "City": "",
                    "State": "",
                    "CountryOrRegion": "",
                    "PostalCode": ""
                },
                "Coordinates": {
                    "Accuracy": "NaN",
                    "Altitude": "NaN",
                    "AltitudeAccuracy": "NaN",
                    "Latitude": "NaN",
                    "Longitude": "NaN"
                },
                "LocationEmailAddress": "",
                "LocationUri": ""
            },
            "ResponseStatus": {
                "Response": "Organizer",
                "Time": "0001-01-01T00:00:00Z"
            },
            "ShowAs": "Busy",
            "IsAllDay": false,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SingleInstance",
            "SeriesMasterId": null,
            "Attendees": [
            ],
            "Recurrence": null,
            "OriginalEndTimeZone": "Pacific Standard Time",
            "OriginalStartTimeZone": "Pacific Standard Time",
            "Organizer": {
                "EmailAddress": {
                    "Address": "user0@contoso.com",
                    "Name": "user0"
                }
            },
            "iCalUId": "040000008200E09BB89A316862",
            "WebLink": "https://outlook.office.com/owa/?ItemID=AAMkADNkNmVlOAA%3D&exvsurl=1&viewmodel=ICalendarItemDetailsViewModelFactory",
            "OnlineMeetingUrl": null
        }
    ],
    "@odata.nextLink": "https://outlook.office.com/api/beta/me/calendarview/?startdatetime=2015-01-01T00%3a00%3a00Z&enddatetime=2015-08-10T00%3a00%3a00Z&%24skipToken=530c9d02ae1a4d96804538bd4d381546"
}
```

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->

<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


**既定のカレンダーで同期するには**

最初の要求。 

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```

2 番目の要求、またはそれ以降のラウンドの最初の要求。

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```

同じラウンドの 3 つ目以降の要求  

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**特定のカレンダーで同期するには**

最初の要求。

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


2 番目の要求、またはそれ以降のラウンドの最初の要求。

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```


同じラウンドの 3 つ目以降の要求:

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**パラメーター**

|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|user_context|string|ユーザー コンテキストです。'Me' の値は、現在のユーザーのコンテキストを示すために使用できます。ユーザーを使用することもできます/{upn} 形式が、 **upn**は、ユーザー プリンシパル名には、通常、ユーザーの電子メール アドレスです。|
|calendar_id|string|カレンダー ID、特定の予定表から予定表ビューを取得している場合です。|
|start_datetime|datetimeoffset|日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|日付と時刻、イベントが終了します。|
|delta_token|string|`deltaToken`前の同期応答の @odata.deltaLink の値の一部として文字列が返されます。|
|skip_token|string|`skipToken`前の同期応答の @odata.nextLink の値の一部として文字列が返されます。 |

**メモ** 

- 指定するとき」選択: odata.track 変更」最初の要求に応答が同期をサポートしている場合、応答が含まれます」優先で適用した: odata.track 変更"ヘッダーにします。
- 、サポートされていないリソースを同期しようとする場合、または初期同期の要求がない場合は、応答に「優先順位で適用した」ヘッダーは表示されません。
- させると enddatetime クエリのパラメーターを変更することによって時間の変更] ウィンドウを変更できます。  
- 応答内の各イベントには、すべてのプロパティが含まれています。 
- 一連定期的なには同期応答には、定期的なマスターの全体のイベントと例外のイベントが含まれます。 
- 定期的な一連のインスタンスでは、短縮したし、 **Start**および**End**プロパティのみが含まれています。出現イベントについては、定期的なイベントのマスターからの残りの部分をキャプチャすることができます。リファレンス情報については、[イベントのリソース](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)を参照してください。
- $Filter、$count、$select、$skip、$top、および $search のクエリ パラメーターを使用することはできません。 

**応答の種類**

拡張[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)と、指定した時間範囲内でイベントを省略します。

**使用例**

次の例では、ユーザーの既定のカレンダーを同期するのには最初と 2 番目の同期要求を示します。各要求は、一度に 1 つだけの全イベントを返すを指定します。
- 初期の応答が 1 つのイベントを返します、`deltaLink`と`deltaToken`。 
- 2 番目の要求を使用している`deltatoken`。2 番目の応答が 1 つのイベントを返す、`nextLink`と`skipToken`。 

完了するには、同期を使用して、`skipToken`同期応答を返すまでに、前回の同期要求から返される、`deltaLink`と`deltaToken`、同期の現在のラウンドが完了する場合。保存、`deltaToken`の同期は、次のラウンドにします。 

詳細については、 [Outlook の予定表ビューでの同期イベント](..\howto\sync-calendar-view.md)を参照してください。
 
<a name="SyncCalendarViewSampleInitialRequest"></a>

**初期要求のサンプル**

```
    GET https://outlook.office.com/api/v2.0/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z HTTP/1.1
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
```

**初期応答のサンプル データ**

```
Preference-Applied: odata.track-changes

    {
        "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/CalendarView",
        "value": [
            {
                "@odata.id": "https://outlook.office.com/api/v2.0/Users('user0@contoso.com')/Events('asdas==')",
                "@odata.etag": "W/\"L8Z+4Y4u7k+97uRKg==\"",
                "Id": "AQMkANJAAAAA==",
                "ChangeKey": "L8Z+AAAAARKg==",
                "Categories": [
                ],
                "DateTimeCreated": "2015-04-10T17:54:49.2725912Z",
                "DateTimeLastModified": "2015-04-10T17:54:49.3038538Z",
                "Subject": "Discuss the Calendar REST API",
                "BodyPreview": "I think it will meet our requirements!",
                "Body": {
                    "ContentType": "HTML",
                    "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
                },
                "Importance": "Normal",
                "HasAttachments": false,
                "Start": {
                    "DateTime": "2015-04-05T18:00:00",
                    "TimeZone": "Pacific Standard Time"
                }
                "End": {
                    "DateTime": "2015-04-05T19:00:00",
                    "TimeZone": "Pacific Standard Time"
                }
                "ReminderMinutesBeforeStart": "15",
                "IsReminderOn": "true",
                "Location": {
                    "DisplayName": "",
                    "Address": null
                },
                "ResponseStatus": {
                    "Response": "Organizer",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "ShowAs": "Busy",
                "IsAllDay": false,
                "IsCancelled": false,
                "IsOrganizer": true,
                "ResponseRequested": true,
                "Type": "SingleInstance",
                "SeriesMasterId": null,
                "Attendees": [
                ],
                "Recurrence": null,
                "OriginalEndTimeZone": "Pacific Standard Time",
                "OriginalStartTimeZone": "Pacific Standard Time",
                "Organizer": {
                    "EmailAddress": {
                        "Address": "user0@contoso.com",
                        "Name": "user0"
                    }
                },
                "iCalUId": "040000008200E9888E07599CCFA23",
                "WebLink": "https://outlook.office.com/owa/?ItemID=AAAINJAAAAA%3D%3D&exvsurl=1&viewmodel=ICalendarItemDetailsViewModelFactory"
            }
        ],
        "@odata.deltaLink": "https://outlook.office.com/api/v2.0/me/calendarview/?startdatetime=2015-01-01T00%3a00%3a00Z&enddatetime=2015-04-10T00%3a00%3a00Z&%24deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c"
    }
```

**サンプルの 2 番目の要求**

```
    GET https://outlook.office.com/api/v2.0/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z&$deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
```

<a name="SyncCalendarViewSampleSecondResponse"></a>

**応答データの 2 番目の例**

```
{
    "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/CalendarView/$delta",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/v2.0/Users('user0@contoso.com')/Events('AAMkAD0jAAA=')",
            "@odata.etag": "W/\"P2fd7QAAAAAVFA==\"",
            "Id": "AAMkADNkNmVlOTITVAAAAAA0jAAA=",
            "ChangeKey": "P2fdmIU1QAAAAAVFA==",
            "Categories": [
            ],
            "DateTimeCreated": "2015-04-15T18:59:11.0226221Z",
            "DateTimeLastModified": "2015-04-15T18:59:11.0694979Z",
            "Subject": "1 hour",
            "BodyPreview": "\u200b",
            "Body": {
                "ContentType": "HTML",
                "Content": "<html><body>content</body></html>"
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": {
                "DateTime": "2015-04-16T18:00:00",
                "TimeZone": "Pacific Standard Time"
            }
            "End": {
                "DateTime": "2015-04-16T19:00:00",
                "TimeZone": Pacific Standard Time"
            }
            "ReminderMinutesBeforeStart": "15",
            "IsReminderOn": "true",
            "Location": {
                "DisplayName": "",
                "Address": {
                    "Street": "",
                    "City": "",
                    "State": "",
                    "CountryOrRegion": "",
                    "PostalCode": ""
                }
             },
            "ResponseStatus": {
                "Response": "Organizer",
                "Time": "0001-01-01T00:00:00Z"
            },
            "ShowAs": "Busy",
            "IsAllDay": false,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SingleInstance",
            "SeriesMasterId": null,
            "Attendees": [
            ],
            "Recurrence": null,
            "OriginalEndTimeZone": "Pacific Standard Time",
            "OriginalStartTimeZone": "Pacific Standard Time",
            "Organizer": {
                "EmailAddress": {
                    "Address": "user0@contoso.com",
                    "Name": "user0"
                }
            },
            "iCalUId": "040000008200E09BB89A316862",
            "WebLink": "https://outlook.office.com/owa/?ItemID=AAMkADNkNmVlOAA%3D&exvsurl=1&viewmodel=ICalendarItemDetailsViewModelFactory"
        }
    ],
    "@odata.nextLink": "https://outlook.office.com/api/v2.0/me/calendarview/?startdatetime=2015-01-01T00%3a00%3a00Z&enddatetime=2015-08-10T00%3a00%3a00Z&%24skipToken=530c9d02ae1a4d96804538bd4d381546"
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->

<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


**既定のカレンダーで同期するには**

最初の要求。 

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```

2 番目の要求、またはそれ以降のラウンドの最初の要求。

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```

同じラウンドの 3 つ目以降の要求  

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**特定のカレンダーで同期するには**

最初の要求。

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


2 番目の要求、またはそれ以降のラウンドの最初の要求。

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```


同じラウンドの 3 つ目以降の要求:

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**パラメーター**

|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|user_context|string|ユーザー コンテキストです。'Me' の値は、現在のユーザーのコンテキストを示すために使用できます。ユーザーを使用することもできます/{upn} 形式が、 **upn**は、ユーザー プリンシパル名には、通常、ユーザーの電子メール アドレスです。|
|calendar_id|string|カレンダー ID、特定の予定表から予定表ビューを取得している場合です。|
|start_datetime|datetimeoffset|日付とイベントが開始する時刻。|
|end_datetime|datetimeoffset|日付と時刻、イベントが終了します。|
|delta_token|string|`deltaToken`前の同期応答の @odata.deltaLink の値の一部として文字列が返されます。|
|skip_token|string|`skipToken`前の同期応答の @odata.nextLink の値の一部として文字列が返されます。 |

**メモ** 

- 指定するとき」選択: odata.track 変更」最初の要求に応答が同期をサポートしている場合、応答が含まれます」優先で適用した: odata.track 変更"ヘッダーにします。
- 、サポートされていないリソースを同期しようとする場合、または初期同期の要求がない場合は、応答に「優先順位で適用した」ヘッダーは表示されません。
- させると enddatetime クエリのパラメーターを変更することによって時間の変更] ウィンドウを変更できます。  
- 応答内の各イベントには、すべてのプロパティが含まれています。 
- 一連定期的なには同期応答には、定期的なマスターの全体のイベントと例外のイベントが含まれます。 
- 定期的な一連のインスタンスでは、短縮したし、 **Start**および**End**プロパティのみが含まれています。出現イベントについては、定期的なイベントのマスターからの残りの部分をキャプチャすることができます。リファレンス情報については、[イベントのリソース](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)を参照してください。
- $Filter、$count、$select、$skip、$top、および $search のクエリ パラメーターを使用することはできません。 

**応答の種類**

拡張[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)と、指定した時間範囲内でイベントを省略します。

**使用例**

次の例では、ユーザーの既定のカレンダーを同期するのには最初と 2 番目の同期要求を示します。各要求は、一度に 1 つだけの全イベントを返すを指定します。
- 初期の応答が 1 つのイベントを返します、`deltaLink`と`deltaToken`。 
- 2 番目の要求を使用している`deltatoken`。2 番目の応答が 1 つのイベントを返す、`nextLink`と`skipToken`。 

完了するには、同期を使用して、`skipToken`同期応答を返すまでに、前回の同期要求から返される、`deltaLink`と`deltaToken`、同期の現在のラウンドが完了する場合。保存、`deltaToken`の同期は、次のラウンドにします。 

詳細については、 [Outlook の予定表ビューでの同期イベント](..\howto\sync-calendar-view.md)を参照してください。
 
<a name="SyncCalendarViewSampleInitialRequest"></a>

**初期要求のサンプル**

```
    GET https://outlook.office.com/api/v1.0/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z HTTP/1.1
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
```

**初期応答のサンプル データ**

```
Preference-Applied: odata.track-changes

    {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/CalendarView",
        "value": [
            {
                "@odata.id": "https://outlook.office.com/api/v1.0/Users('user0@contoso.com')/Events('asdas==')",
                "@odata.etag": "W/\"L8Z+4Y4u7k+97uRKg==\"",
                "Id": "AQMkANJAAAAA==",
                "ChangeKey": "L8Z+AAAAARKg==",
                "Categories": [
                ],
                "DateTimeCreated": "2015-04-10T17:54:49.2725912Z",
                "DateTimeLastModified": "2015-04-10T17:54:49.3038538Z",
                "Subject": "Discuss the Calendar REST API",
                "BodyPreview": "I think it will meet our requirements!",
                "Body": {
                    "ContentType": "HTML",
                    "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
                },
                "Importance": "Normal",
                "HasAttachments": false,
                "Start": "2015-04-05T18:00:00Z",
                "StartTimeZone": "Pacific Standard Time",
                "End": "2015-04-05T19:00:00Z",
                "EndTimeZone": "Pacific Standard Time",
                "Reminder": 15,
                "Location": {
                    "DisplayName": "",
                    "Address": null
                },
                "ResponseStatus": {
                    "Response": "Organizer",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "ShowAs": "Busy",
                "IsAllDay": false,
                "IsCancelled": false,
                "IsOrganizer": true,
                "ResponseRequested": true,
                "Type": "SingleInstance",
                "SeriesMasterId": null,
                "Attendees": [
                ],
                "Recurrence": null,
                "Organizer": {
                    "EmailAddress": {
                        "Address": "user0@contoso.com",
                        "Name": "user0"
                    }
                },
                "iCalUId": "040000008200E9888E07599CCFA23",
                "WebLink": "https://outlook.office.com/owa/?ItemID=AAAINJAAAAA%3D%3D&exvsurl=1&viewmodel=ICalendarItemDetailsViewModelFactory"
            }
        ],
        "@odata.deltaLink": "https://outlook.office.com/api/v1.0/me/calendarview/?startdatetime=2015-01-01T00%3a00%3a00Z&enddatetime=2015-04-10T00%3a00%3a00Z&%24deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c"
    }
```

**サンプルの 2 番目の要求**

```
    GET https://outlook.office.com/api/v1.0/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z&$deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
```

<a name="SyncCalendarViewSampleSecondResponse"></a>

**応答データの 2 番目の例**

```
{
    "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/CalendarView/$delta",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/v1.0/Users('user0@contoso.com')/Events('AAMkAD0jAAA=')",
            "@odata.etag": "W/\"P2fd7QAAAAAVFA==\"",
            "Id": "AAMkADNkNmVlOTITVAAAAAA0jAAA=",
            "ChangeKey": "P2fdmIU1QAAAAAVFA==",
            "Categories": [
            ],
            "DateTimeCreated": "2015-04-15T18:59:11.0226221Z",
            "DateTimeLastModified": "2015-04-15T18:59:11.0694979Z",
            "Subject": "1 hour",
            "BodyPreview": "\u200b",
            "Body": {
                "ContentType": "HTML",
                "Content": "<html><body>content</body></html>"
            },
            "Importance": "Normal",
            "HasAttachments": false,
            "Start": "2015-04-16T18:00:00Z",
            "StartTimeZone": "Pacific Standard Time",
            "End": "2015-04-16T19:00:00Z",
            "EndTimeZone": "Pacific Standard Time",
            "Reminder": 15,
            "Location": {
                "DisplayName": "",
                "Address": {
                    "Street": "",
                    "City": "",
                    "State": "",
                    "CountryOrRegion": "",
                    "PostalCode": ""
                }
            },
            "ResponseStatus": {
                "Response": "Organizer",
                "Time": "0001-01-01T00:00:00Z"
            },
            "ShowAs": "Busy",
            "IsAllDay": false,
            "IsCancelled": false,
            "IsOrganizer": true,
            "ResponseRequested": true,
            "Type": "SingleInstance",
            "SeriesMasterId": null,
            "Attendees": [
            ],
            "Recurrence": null,
            "Organizer": {
                "EmailAddress": {
                    "Address": "user0@contoso.com",
                    "Name": "user0"
                }
            },
            "iCalUId": "040000008200E09BB89A316862",
            "WebLink": "https://outlook.office.com/owa/?ItemID=AAMkADNkNmVlOAA%3D&exvsurl=1&viewmodel=ICalendarItemDetailsViewModelFactory"
        }
    ],
    "@odata.nextLink": "https://outlook.office.com/api/v1.0/me/calendarview/?startdatetime=2015-01-01T00%3a00%3a00Z&enddatetime=2015-08-10T00%3a00%3a00Z&%24skipToken=530c9d02ae1a4d96804538bd4d381546"
}
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->

****

<a name="FindMeetingTimesPreview"></a>
## <a name="find-meeting-times-preview"></a>会議の時刻を検索する (プレビュー)

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

会議の時間の提案に基づいて開催者と出席者のパラメーターとして指定された可用性、および時間や場所の制約を検索します。 

この操作は、現在プレビューおよびベータ版のみで利用可能です。のみ Office 365 のメールボックス (Azure AD) に、Microsoft アカウントに適用されます。

```no-highlight
POST https://outlook.office.com/api/{version}/me/findmeetingtimes
```

サポートされているすべてのパラメーターは次のとおりです。シナリオによっては、 **FindMeetingTimes**アクションの要求の本文で必要なパラメーターを指定します。 

|**パラメーター**|**タイプ**|**説明**|**必須。**|
|:-----|:-----|:-----|:-----|
| 出席者 | コレクション ([AttendeeBase](complex-types-for-mail-contacts-calendar.md#AttendeeBase)) | 参加者または会議のためのリソースです。空のコレクションには、開催者だけに無料で時間帯を検索するのには**FindMeetingTimes**が発生します。 | オプション |
| LocationConstraint | [LocationConstraint](complex-types-for-mail-contacts-calendar.md#LocationConstraint) | 会議の場所の開催者の要件、会議の場所の候補が必要かどうかなど、か、特定の場所だけで会議を行います。 | オプション |
| TimeConstraint | [TimeConstraint](complex-types-for-mail-contacts-calendar.md#TimeConstraint) | 開始と終了時間の範囲、会議が発生する必要があります。 | オプション |
| MeetingDuration | Edm.Duration |期間、たとえば、ISO 8601 形式で表された会議の長さ`PT1H`1 時間を表します。ミーティングの継続時間を指定しない場合、 **FindMeetingTimes**は、デフォルトの 30 分を使用します。 | オプション |
| MaxCandidates | Edm.Int32 |会議の提案で応答を返すの最大数です。 | オプション |
| IsOrganizerOptional | Edm.Boolean | 指定`true`場合は、出席する構成内容の変更はありません。既定値は、 `false`。 | オプション |
| ReturnSuggestionHints | Edm.Boolean | 指定`true` **SuggestionHint**プロパティ内の各会議提案の理由を取得します。既定値は、`false`に、そのプロパティを返しません。 | オプション |

指定されたパラメーターに基づいて、 **FindMeetingTimes**は、開催者と出席者のプライマリの予定表の空き時間情報のステータスをチェックします。アクションでは、最高では、会議を計算し、すべての会議の提案を返します。

**応答の種類**

それぞれの会議の提案が含まれています[MeetingTimeCandidatesResult](complex-types-for-mail-contacts-calendar.md#MeetingTimeCandidatesResult)は、 [MeetingTimeCandidate](#MeetingTimeCandidate)、および**EmptySuggestionsHint**プロパティを入力します。

<!-- Location suggestions are based on the organizer's booking history during the past 7 days and next 2 days. If the organizer doesn't have sufficient booking history 
in the corresponding time window, the request returns HTTP 200 OK, but does not include any meeting suggestions in the response. -->

各候補は、[平均率 50% 以上の参加には、信頼レベル](complex-types-for-mail-contacts-calendar.md#ConfidenceScoreDetails)を持つ参加者との[MeetingTimeCandidate](complex-types-for-mail-contacts-calendar.md#MeetingTimeCandidate)と定義されます。既定では、各会議の候補が返されます (utc)。適用、`Prefer: outlook.timezone`して、会議の時間のご提案など、別のタイム ゾーンで返さ要求ヘッダー。

```no-highlight
Prefer: outlook.timezone="Pacific Standard Time"
```

**FindMeetingTimes**は、すべての会議の提案を返すことはできません、する場合の応答、 **EmptySuggestionsHint**プロパティで理由を示します。この値に基づいてよりのパラメーターを調整してもう一度**FindMeetingTimes**を呼び出します。


**メモ**

現在、 **FindMeetingTimes**は、次の内容を前提とします。

- (リソース) ではなく人である任意の[出席者](..\api\complex-types-for-mail-contacts-calendar.md#Attendee)は、必須の出席者です。指定では、`Required`人の`Resource`**型**の対応するプロパティの [**出席者**のコレクションのパラメーターの一部として、リソースの。
- 提案された会議は、開催者または出席者の稼働時間のみで発生します。の[TimeConstraint](..\api\complex-types-for-mail-contacts-calendar.md#TimeConstraint)の**ActivityDomain**プロパティを指定するを無視することができます。 

次の各例では、 **FindMeetingTimes**を呼び出し、出席者の可用性、時間と場所上の制約が次のように異なります。

- [時刻と出席者 (残りの部分) に対応する場所を検索します。](#FindTimeToMeet) 
- [既知の場所でお会いする日時を検索し、各候補 (残りの部分) の理由を取得します。](#FindTimeToMeetAtKnownLocation) 
- [満たすために検索時間がない参加者は、利用可能な (他)](#FindTimeToMeetButNobodyAvailable) 
- [満たすために時間がいくつか出席者だけ利用可能な (他)](#FindTimeToMeetSomeAvailable)
- [(REST) サインイン中のユーザーの空き時間帯を検索します。](#FindFreeSlots)


<a name="FindTimeToMeet"></a>

### <a name="find-time-and-location-to-meet-with-specific-attendees-rest"></a>時刻と特定の参加者 (残りの部分) と対応する場所を検索します。

検索の時間と、要求の本文に次のパラメーターを指定する条件を満たすために場所を。
- **出席者**
- **TimeConstraint**
- **MeetingDuration**

**要求のサンプル**

会議の時間と場所が開催者のも考慮して次の使用例を提案し、要求された会議で出席者の時刻の範囲、および要求された時間の長さです。

```
POST https://outlook.office.com/api/beta/me/findmeetingtimes

Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json 

{ 
  "Attendees": [ 
    { 
      "Type": "Required",  
      "EmailAddress": { 
        "Address": "fannyd@prosewareltd.onmicrosoft.com" 
      } 
    } 
  ],  
  "TimeConstraint": { 
    "Timeslots": [ 
       { 
        "Start": { 
          "Date": "2016-05-20",  
          "Time": "7:00:00",  
          "TimeZone": "Pacific Standard Time" 
        },  
        "End": { 
          "Date": "2016-05-20",  
          "Time": "17:00:00",  
          "TimeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "MeetingDuration": "PT1H" 
} 
```



**応答の例**

状態コード: 200

```
{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Microsoft.OutlookServices.MeetingTimeCandidatesResult",
    "MeetingTimeSlots": [
        {
            "MeetingTimeSlot": {
                "Start": {
                    "Date": "2016-05-20",
                    "Time": "10:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                },
                "End": {
                    "Date": "2016-05-20",
                    "Time": "11:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                }
            },
            "Confidence": 100.0,
            "OrganizerAvailability": "Free",
            "AttendeeAvailability": [
                {
                    "Attendee": {
                        "Type": "Required",
                        "EmailAddress": {
                            "Address": "fannyd@prosewareltd.onmicrosoft.com"
                        }
                    },
                    "Availability": "Free"
                }
            ],
            "Locations": [
               {
                    "DisplayName": "Tokyo conference room",
                    "LocationEmailAddress": "",
                    "LocationUri": "",
                    "Address": null,
                    "Coordinates": null
                }
            ]
        },
        {
            "MeetingTimeSlot": {
                "Start": {
                    "Date": "2016-05-20",
                    "Time": "11:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                },
                "End": {
                    "Date": "2016-05-20",
                    "Time": "12:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                }
            },
            "Confidence": 100.0,
            "OrganizerAvailability": "Free",
            "AttendeeAvailability": [
                {
                    "Attendee": {
                        "Type": "Required",
                        "EmailAddress": {
                            "Address": "fannyd@prosewareltd.onmicrosoft.com"
                        }
                    },
                    "Availability": "Free"
                }
            ],
            "Locations": [
               {
                    "DisplayName": "Paris conference room",
                    "LocationEmailAddress": "",
                    "LocationUri": "",
                    "Address": null,
                    "Coordinates": null
                }
            ]
        }
    ],
    "EmptySuggestionsHint": ""
}
```


****

<a name="FindTimeToMeetAtKnownLocation"></a>

### <a name="find-time-to-meet-at-a-known-location-and-get-a-reason-for-each-suggestion-rest"></a>既知の場所でお会いする日時を検索し、各候補 (残りの部分) の理由を取得します。

、あらかじめ決められた場所でお会いする日時を検索し、要求の本体で次のパラメーターを指定することで各候補の理由を要求します。
- **出席者**
- **LocationConstraint**
- **TimeConstraint**
- **MeetingDuration**
- **ReturnSuggestionHints**

**ReturnSuggestionHints**パラメーターを設定するには、取得することも、 **SuggestionHint**プロパティで各候補の説明**FindMeetingTimes**は、ご意見を返す場合。


**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/findmeetingtimes

Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json 

{ 
  "Attendees": [ 
    { 
      "Type": "Required",  
      "EmailAddress": { 
        "Address": "fannyd@prosewareltd.onmicrosoft.com" 
      } 
    } 
  ],  
  "LocationConstraint": { 
    "IsRequired": "false",  
    "SuggestLocation": "false",  
    "Locations": [ 
      { 
        "DisplayName": "Conf room Hood" 
      } 
    ] 
  },  
  "TimeConstraint": { 
    "Timeslots": [ 
      { 
        "Start": { 
          "Date": "2016-05-20",  
          "Time": "7:00:00",  
          "TimeZone": "Pacific Standard Time" 
        },  
        "End": { 
          "Date": "2016-05-20",  
          "Time": "17:00:00",  
          "TimeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "MeetingDuration": "PT2H",
  "ReturnSuggestionHints": "true"
} 
```



**応答の例**

状態コード: 200

```
{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Microsoft.OutlookServices.MeetingTimeCandidatesResult",
    "MeetingTimeSlots": [
        {
            "MeetingTimeSlot": {
                "Start": {
                    "Date": "2016-05-20",
                    "Time": "10:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                },
                "End": {
                    "Date": "2016-05-20",
                    "Time": "12:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                }
            },
            "Confidence": 100.0,
            "OrganizerAvailability": "Free",
            "AttendeeAvailability": [
                {
                    "Attendee": {
                        "Type": "Required",
                        "EmailAddress": {
                            "Address": "fannyd@prosewareltd.onmicrosoft.com"
                        }
                    },
                    "Availability": "Free"
                }
            ],
            "Locations": [
                {
                    "DisplayName": "Conf room Hood"
                }
            ],
            "SuggestionHint": "Suggested because it is one of the nearest times when all attendees are available."
        }
    ],
    "EmptySuggestionsHint": ""
}
```


****

<a name="FindTimeToMeetButNobodyAvailable"></a>

### <a name="find-time-to-meet-but-no-attendee-is-available-rest"></a>満たすために検索時間がない参加者は、利用可能な (他)

要求の本文で次のパラメーターを指定することによって、あらかじめ決められた場所にある対応する時間を見つけます。
- **出席者**
- **LocationConstraint**
- **TimeConstraint**
- **MeetingDuration**

指定されたパラメーターと、出席者の空き時間に基づいて、この例では**FindMeetingTimes**は意見を返すことはできません、理由を返す`AttendeesUnavailable` **EmptySuggestionsHint**プロパティにします。 

その他の[会議提案を返さないの考えられる原因](..\api\complex-types-for-mail-contacts-calendar.md#ReasonsNoMeetingSuggestion)を参照してください。


**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/findmeetingtimes

Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json 

{ 
  "Attendees": [ 
    { 
      "Type": "Required",  
      "EmailAddress": { 
        "Address": "fannyd@prosewareltd.onmicrosoft.com" 
      } 
    } 
  ],  
  "LocationConstraint": { 
    "IsRequired": "false",  
    "SuggestLocation": "false",  
    "Locations": [ 
      { 
        "DisplayName": "Conf room Hood" 
      } 
    ] 
  },  
  "TimeConstraint": { 
    "Timeslots": [ 
      { 
        "Start": { 
          "Date": "2016-05-20",  
          "Time": "7:00:00",  
          "TimeZone": "Pacific Standard Time" 
        },  
        "End": { 
          "Date": "2016-05-20",  
          "Time": "14:00:00",  
          "TimeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "MeetingDuration": "PT2H" 
}
```



**応答の例**

状態コード: 200

```
{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Microsoft.OutlookServices.MeetingTimeCandidatesResult",
    "MeetingTimeSlots": [
    ],
    "EmptySuggestionsHint": "AttendeesUnavailable"
}
```

****

<a name="FindTimeToMeetSomeAvailable"></a>
### <a name="find-time-to-meet-but-only-some-attendees-are-available-rest"></a>満たすために検索時間が一部の参加者だけは、利用可能な (他)

要求の本文で次のパラメーターを指定することによって、あらかじめ決められた場所にある対応する時間を見つけます。
- **出席者**
- **LocationConstraint**
- **TimeConstraint**
- **MeetingDuration**
- **ReturnSuggestionHints**

この例では、2 つの参加者の 1 つだけがあります。**FindMeetingTimes**を返す各会議の提案が含まれています。
- 各出席者の可用性
- 50% の計算の会議の信頼性
- **SuggestionHInt**、 **ReturnSuggestionHints**パラメーターが設定されているので。 

[会議の信頼](..\api\complex-types-for-mail-contacts-calendar.md#ConfidenceScoreDetails)の詳細についてを検索します。


**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/findmeetingtimes

Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json 

{ 
  "Attendees": [ 
    { 
      "Type": "Required",  
      "EmailAddress": { 
        "Address": "fannyd@prosewareltd.onmicrosoft.com" 
      } 
    },
   { 
      "Type": "Optional",  
      "EmailAddress": { 
        "Address": "danas@prosewareltd.onmicrosoft.com" 
      } 
    } 
  ],  
  "LocationConstraint": { 
    "IsRequired": "false",  
    "SuggestLocation": "false",  
    "Locations": [ 
      { 
        "DisplayName": "Conf room Hood" 
      } 
    ] 
  },  
  "TimeConstraint": { 
    "Timeslots": [ 
      { 
        "Start": { 
          "Date": "2016-05-20",  
          "Time": "9:00:00",  
          "TimeZone": "Pacific Standard Time" 
        },  
        "End": { 
          "Date": "2016-05-20",  
          "Time": "17:00:00",  
          "TimeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "MeetingDuration": "PT1H",
  "ReturnSuggestionHints": "true"
}
```



**応答の例**

状態コード: 200
```
{
   "@odata.context":"https://outlook.office.com/api/beta/$metadata#Microsoft.OutlookServices.MeetingTimeCandidatesResult",
   "MeetingTimeSlots":[
      {
         "MeetingTimeSlot":{
            "Start":{
               "Date":"2016-05-20",
               "Time":"10:00:00.0000000",
               "TimeZone":"Pacific Standard Time"
            },
            "End":{
               "Date":"2016-05-20",
               "Time":"11:00:00.0000000",
               "TimeZone":"Pacific Standard Time"
            }
         },
         "Confidence":50.0,
         "OrganizerAvailability":"Free",
         "AttendeeAvailability":[
            {
               "Attendee":{
                  "Type":"Required",
                  "EmailAddress":{
                     "Address":"fannyd@prosewareltd.onmicrosoft.com"
                  }
               },
               "Availability":"Free"
            },
            {
               "Attendee":{
                  "Type":"Required",
                  "EmailAddress":{
                     "Address":"danas@prosewareltd.onmicrosoft.com"
                  }
               },
               "Availability":"Busy"
            }
         ],
         "Locations":[
            {
               "DisplayName":"Conf room Hood"
            }
         ],
         "SuggestionHint":"Suggested because it is one of the nearest times when most attendees are available."
      },
      {
         "MeetingTimeSlot":{
            "Start":{
               "Date":"2016-05-20",
               "Time":"11:00:00.0000000",
               "TimeZone":"Pacific Standard Time"
            },
            "End":{
               "Date":"2016-05-20",
               "Time":"12:00:00.0000000",
               "TimeZone":"Pacific Standard Time"
            }
         },
         "Confidence":50.0,
         "OrganizerAvailability":"Free",
         "AttendeeAvailability":[
            {
               "Attendee":{
                  "Type":"Required",
                  "EmailAddress":{
                     "Address":"fannyd@prosewareltd.onmicrosoft.com"
                  }
               },
               "Availability":"Free"
            },
            {
               "Attendee":{
                  "Type":"Required",
                  "EmailAddress":{
                     "Address":"danas@prosewareltd.onmicrosoft.com"
                  }
               },
               "Availability":"Busy"
            }
         ],
         "Locations":[
            {
               "DisplayName":"Conf room Hood"
            }
         ],
         "SuggestionHint":"Suggested because it is one of the nearest times when most attendees are available."
      }
   ],
   "EmptySuggestionsHint":""
}
```

****

<a name="FindFreeSlots"></a>
###<a name="find-free-time-slots-for-just-the-signed-in-user-rest"></a>だけでログインしているユーザー (残りの部分) の空き時間帯を検索します。

日付の範囲内でサインインしているユーザーのプライマリの予定表の空き時間帯を検索するには、要求の本文で次のパラメーターを指定します。

- **TimeConstraint**
- **MeetingDuration**

**要求のサンプル**

次の使用例は、 **TimeConstraint**によって指定された期間内で、サインイン中のユーザーのプライマリの予定表で、 **MeetingDuration**で指定された、1 時間の空き時間のスロットを探します。

```
POST https://outlook.office.com/api/beta/me/findmeetingtimes

Prefer: outlook.timezone="Pacific Standard Time"
Content-Type: application/json 

{ 
  "Attendees": [],
  "TimeConstraint": { 
    "Timeslots": [ 
      { 
        "Start": { 
          "Date": "2016-05-20",  
          "Time": "7:00:00",  
          "TimeZone": "Pacific Standard Time" 
        },  
        "End": { 
          "Date": "2016-05-20",  
          "Time": "17:00:00",  
          "TimeZone": "Pacific Standard Time" 
        } 
      } 
    ] 
  },  
  "MeetingDuration": "PT1H"
}
```



**応答の例**

状態コード: 200
```
{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Microsoft.OutlookServices.MeetingTimeCandidatesResult",
    "MeetingTimeSlots": [
        {
            "MeetingTimeSlot": {
                "Start": {
                    "Date": "2016-05-20",
                    "Time": "08:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                },
                "End": {
                    "Date": "2016-05-20",
                    "Time": "09:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                }
            },
            "Confidence": 100.0,
            "OrganizerAvailability": "Free",
            "AttendeeAvailability": [
            ],
            "Locations": [
            ]
        },
        {
            "MeetingTimeSlot": {
                "Start": {
                    "Date": "2016-05-20",
                    "Time": "09:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                },
                "End": {
                    "Date": "2016-05-20",
                    "Time": "10:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                }
            },
            "Confidence": 100.0,
            "OrganizerAvailability": "Free",
            "AttendeeAvailability": [
            ],
            "Locations": [
            ]
        },
        {
            "MeetingTimeSlot": {
                "Start": {
                    "Date": "2016-05-20",
                    "Time": "12:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                },
                "End": {
                    "Date": "2016-05-20",
                    "Time": "13:00:00.0000000",
                    "TimeZone": "Pacific Standard Time"
                }
            },
            "Confidence": 100.0,
            "OrganizerAvailability": "Free",
            "AttendeeAvailability": [
            ],
            "Locations": [
            ]
        }
    ],
    "EmptySuggestionsHint": ""
}
```

****


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


<!-- ==================================== End BETA content ====================================================== -->

<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

この機能は、ベータ版だけで現在利用可能です。詳細については、**ベータ版**の選択、記事の右上隅にコントロールを使用します。 

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->


[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

この機能は、ベータ版だけで現在利用可能です。詳細については、**ベータ版**の選択、記事の右上隅にコントロールを使用します。 

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->




****

<a name="CreateEvents"> </a>
## <a name="create-events"></a>イベントを作成します。

REST API:[予定表のイベントを作成します。](#CreateAnEvent)

クライアント ライブラリ:[予定表のイベント (クライアント) を作成します。](#CreateEventsClient)

<a name="CreateAnEvent"></a>
###<a name="create-a-calendar-event-rest"></a>(REST) イベントを作成します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

カレンダーへの投稿、ユーザーのプライマリの予定表または特定のカレンダーにイベントを作成`events`エンドポイントです。イベントが作成されると、サーバーはすべての参加者に招待状を送信します。

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/events
POST https://outlook.office.com/api/beta/me/calendars/{calendar_id}/events
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|

**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/events
Content-Type: application/json
```

```
{
  "Subject": "Discuss the Calendar REST API",
  "Body": {
    "ContentType": "HTML",
    "Content": "I think it will meet our requirements!"
  },
  "Start": {
      "DateTime": "2014-02-02T18:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "End": {
      "DateTime": "2014-02-02T19:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "Attendees": [
    {
      "EmailAddress": {
        "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
        "Name": "Janet Schorr"
      },
      "Type": "Required"
    }
  ]
}
```

**応答の例**

状態コード: 201

```
{
  "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events/$entity",
  "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGE4v1RAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeNheA==\"",
  "Id": "AAMkAGE4v1RAAA=",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeNheA==",
  "Categories": [],
  "CreatedDateTime": "2014-01-22T20:56:10.1058291Z",
  "LastModifiedDateTime": "2014-01-22T20:56:10.3402186Z",
  "Subject": "Discuss the Calendar REST API",
  "BodyPreview": "I think it will meet our requirements!",
  "Body": {
    "ContentType": "HTML",
    "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
  },
  "Importance": "Normal",
  "HasAttachments": false,
  "Start": {
      "DateTime": "2014-02-02T18:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "End": {
      "DateTime": "2014-02-02T19:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "Location": {
    "DisplayName": "",
    "Address": null,
    "Coordinates": null,
    "LocationEmailAddress": "",
    "LocationUri": ""
  },
  "ShowAs": "Busy",
  "IsAllDay": false,
  "IsCancelled": false,
  "IsOrganizer": true,
  "ResponseRequested": true,
  "Type": "SingleInstance",
  "SeriesMasterId": null,
  "Attendees": [
    {
      "EmailAddress": {
        "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
        "Name": "Janet Schorr"
      },
      "Status": {
        "Response": "None",
        "Time": "0001-01-01T00:00:00Z"
      },
      "Type": "Required"
    }
  ],
  "Recurrence": null,
  "OriginalEndTimeZone": "Pacific Standard Time",
  "OriginalStartTimeZone": "Pacific Standard Time",
  "Organizer": {
    "EmailAddress": {
      "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
      "Name": "alexd"
    }
  },
  "OnlineMeetingUrl": null
}
```


**応答の種類**

新しい[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。

既定では、応答には、新しいイベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。次に、応答に新しいイベントの**開始**と**終了**のプロパティのみを含める例を示します。

```
POST https://outlook.office.com/api/beta/me/events?$Select=Start,End
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->

<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/v2.0/me/events
POST https://outlook.office.com/api/v2.0/me/calendars/{calendar_id}/events
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|

**要求のサンプル**

```
POST https://outlook.office.com/api/v2.0/me/events
Content-Type: application/json
```

```
{
  "Subject": "Discuss the Calendar REST API",
  "Body": {
    "ContentType": "HTML",
    "Content": "I think it will meet our requirements!"
  },
  "Start": {
      "DateTime": "2014-02-02T18:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "End": {
      "DateTime": "2014-02-02T19:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "Attendees": [
    {
      "EmailAddress": {
        "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
        "Name": "Janet Schorr"
      },
      "Type": "Required"
    }
  ]
}
```

**応答の例**

状態コード: 201

```
{
  "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events/$entity",
  "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGE4v1RAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeNheA==\"",
  "Id": "AAMkAGE4v1RAAA=",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeNheA==",
  "Categories": [],
  "CreatedDateTime": "2014-01-22T20:56:10.1058291Z",
  "LastModifiedDateTime": "2014-01-22T20:56:10.3402186Z",
  "Subject": "Discuss the Calendar REST API",
  "BodyPreview": "I think it will meet our requirements!",
  "Body": {
    "ContentType": "HTML",
    "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
  },
  "Importance": "Normal",
  "HasAttachments": false,
  "Start": {
      "DateTime": "2014-02-02T18:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "End": {
      "DateTime": "2014-02-02T19:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "Location": {
    "DisplayName": "",
    "Address": null
  },
  "ShowAs": "Busy",
  "IsAllDay": false,
  "IsCancelled": false,
  "IsOrganizer": true,
  "ResponseRequested": true,
  "Type": "SingleInstance",
  "SeriesMasterId": null,
  "Attendees": [
    {
      "EmailAddress": {
        "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
        "Name": "Janet Schorr"
      },
      "Status": {
        "Response": "None",
        "Time": "0001-01-01T00:00:00Z"
      },
      "Type": "Required"
    }
  ],
  "Recurrence": null,
  "OriginalEndTimeZone": "Pacific Standard Time",
  "OriginalStartTimeZone": "Pacific Standard Time",
  "Organizer": {
    "EmailAddress": {
      "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
      "Name": "alexd"
    }
  }
}
```


**応答の種類**

新しい[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。

既定では、応答には、新しいイベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。次に、応答に新しいイベントの**開始**と**終了**のプロパティのみを含める例を示します。

```
POST https://outlook.office.com/api/v2.0/me/events?$Select=Start,End
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->

<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


既定では、**開始**と**終了**時刻の値は UTC では。指定のタイム ゾーンの**開始**および**終了**、エクスプレス、対応するタイム ゾーンの時刻、および UTC からのタイム オフセットを含むできます。次の例では、太平洋標準時の時刻の値を割り当てる方法を示します。1 つのタイム ゾーンを指定する場合する必要がありますを指定する値、他の 1 つも注意してください。


```no-highlight
POST https://outlook.office.com/api/v1.0/me/events
POST https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}/events
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|

```REST
{
    "method": "POST",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/events",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/events",
    "requestHeaders": {
        "Accept": "application/json",
        "Content-Type": "application/json",
        "Content-Length": 529
    },
    "parameterDetails": [],
    "requestBody": {
        "Subject": "Discuss the Calendar REST API",
        "Body": {
            "ContentType": "HTML",
            "Content": "I think it will meet our requirements!"
        },
        "Start": "2014-02-02T18:00:00-08:00",
        "StartTimeZone": "Pacific Standard Time",
        "End": "2014-02-02T19:00:00-08:00",
        "EndTimeZone": "Pacific Standard Time",
        "Attendees": [
            {
                "EmailAddress": {
                    "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Janet Schorr"
                },
                "Type": "Required"
            }
        ]
    },
    "statusCode": 201,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/Events/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1RAAA=')",
        "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeNheA==\"",
        "Id": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1RAAA=",
        "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeNheA==",
        "Categories": [],
        "DateTimeCreated": "2014-01-22T20:56:10.1058291Z",
        "DateTimeLastModified": "2014-01-22T20:56:10.3402186Z",
        "Subject": "Discuss the Calendar REST API",
        "BodyPreview": "I think it will meet our requirements!",
        "Body": {
            "ContentType": "HTML",
            "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
        },
        "Importance": "Normal",
        "HasAttachments": false,
        "Start": "2014-02-02T18:00:00-08:00",
        "StartTimeZone": "Pacific Standard Time",
        "End": "2014-02-02T19:00:00-08:00",
        "EndTimeZone": "Pacific Standard Time",
        "Location": {
            "DisplayName": ""
        },
        "ShowAs": "Busy",
        "IsAllDay": false,
        "IsCancelled": false,
        "IsOrganizer": true,
        "ResponseRequested": true,
        "Type": "SingleInstance",
        "SeriesMasterId": null,
        "Attendees": [
            {
                "EmailAddress": {
                    "Address": "janets@a830edad9050849NDA1.onmicrosoft.com",
                    "Name": "Janet Schorr"
                },
                "Status": {
                    "Response": "None",
                    "Time": "0001-01-01T00:00:00Z"
                },
                "Type": "Required"
            }
        ],
        "Recurrence": null,
        "Organizer": {
            "EmailAddress": {
                "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                "Name": "alexd"
            }
        }
    }
}
```


**応答の種類**

新しい[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。

既定では、応答には、新しいイベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。次に、応答に新しいイベントの**開始**と**終了**のプロパティのみを含める例を示します。

```
POST https://outlook.office.com/api/v1.0/me/events?$Select=Start,End
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->

****

<a name="CreateEventsClient"></a>
### <a name="create-a-calendar-event-client"></a>イベント (クライアント) の作成します。

イベントを作成します。別のカレンダーにイベントを追加するには、移動先の予定表の**イベント**のプロパティを使用します。

例:`await client.Me.Calendars["AQMkADE3..."].Events.AddEventAsync(newEvent);`


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- CHUCK, feel free to provide client library example that reflects the event breaking changes for beta.  --> 

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->

<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Create a location for the event
Location location = new Location 
{ 
    DisplayName = "Water cooler" 
}; 

// Create a description for the event   
ItemBody body = new ItemBody 
{ 
    Content = "Status updates, blocking issues, and next steps", 
    ContentType = BodyType.Text 
}; 
    
// Create an attendee for the event 
Attendee[] attendees =  
{  
    new Attendee  
    {  
        Type = AttendeeType.Required,  
        EmailAddress = new EmailAddress  
        {  
            Address = "katiej@a830edad9050849NDA1.onmicrosoft.com"  
        },  
    },  
}; 
    
// Create the event object
Event newEvent = new Event 
{ 
    Subject = "Sync up", 
    Location = location, 
    Attendees = attendees, 
    Start = new DateTimeTimeZone()
    {
        TimeZone = TimeZoneInfo.Local.Id,
        DateTime = new DateTime(2015, 12, 1, 9, 30, 0).ToString("s")
    },
    End = new DateTimeTimeZone()
    {
        TimeZone = TimeZoneInfo.Local.Id,
        DateTime = new DateTime(2015, 12, 1, 10, 30, 0).ToString("s")
    },    
    Body = body 
};
    
// Add the event to the default calendar
await client.Me.Events.AddEventAsync(newEvent);

// Get the event ID.
string eventId = newEvent.Id;
```
```javascript
        var event = new Microsoft.OutlookServices.Event();
        event.subject = 'Your Subject';
        event.start = new Date("October 30, 2014 11:13:00").toISOString();
        event.end = new Date("October 30, 2014 12:13:00").toISOString();

        // Body
        event.body = new Microsoft.OutlookServices.ItemBody();
        event.body.content = 'Body Content';
        event.body.contentType = Microsoft.OutlookServices.BodyType.Text;

        // Location
        event.location = new Microsoft.OutlookServices.Location();
        event.location.displayName = 'Location';

        // Attendee
        var attendee1 = new Microsoft.OutlookServices.Attendee();
        var emailAddress1 = new Microsoft.OutlookServices.EmailAddress();
        emailAddress1.name = "Katie Jordan";
        emailAddress1.address = "katiej@a830edad9050849NDA1.onmicrosoft.com";

        attendee1.emailAddress = emailAddress1;

        event.attendees.push(attendee1);
        
        outlookClient.me.calendar.events.addEvent(event)
        .then(function (response) {
            console.log(response._Id);
        });    

```
<!-- ENDSECTION -->


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Create a location for the event
Location location = new Location 
{ 
    DisplayName = "Water cooler" 
}; 

// Create a description for the event   
ItemBody body = new ItemBody 
{ 
    Content = "Status updates, blocking issues, and next steps", 
    ContentType = BodyType.Text 
}; 
    
// Create an attendee for the event 
Attendee[] attendees =  
{  
    new Attendee  
    {  
        Type = AttendeeType.Required,  
        EmailAddress = new EmailAddress  
        {  
            Address = "katiej@a830edad9050849NDA1.onmicrosoft.com"  
        },  
    },  
}; 
    
// Create the event object
Event newEvent = new Event 
{ 
    Subject = "Sync up", 
    Location = location, 
    Attendees = attendees, 
    Start = new DateTimeOffset(new DateTime(2014, 12, 1, 9, 30, 0)), 
    End = new DateTimeOffset(new DateTime(2014, 12, 1, 10, 0, 0)), 
    Body = body 
}; 
    
// Add the event to the default calendar
await client.Me.Events.AddEventAsync(newEvent);

// Get the event ID.
string eventId = newEvent.Id;
```
```javascript
        var event = new Microsoft.OutlookServices.Event();
        event.subject = 'Your Subject';
        event.start = new Date("October 30, 2014 11:13:00").toISOString();
        event.end = new Date("October 30, 2014 12:13:00").toISOString();

        // Body
        event.body = new Microsoft.OutlookServices.ItemBody();
        event.body.content = 'Body Content';
        event.body.contentType = Microsoft.OutlookServices.BodyType.Text;

        // Location
        event.location = new Microsoft.OutlookServices.Location();
        event.location.displayName = 'Location';

        // Attendee
        var attendee1 = new Microsoft.OutlookServices.Attendee();
        var emailAddress1 = new Microsoft.OutlookServices.EmailAddress();
        emailAddress1.name = "Katie Jordan";
        emailAddress1.address = "katiej@a830edad9050849NDA1.onmicrosoft.com";

        attendee1.emailAddress = emailAddress1;

        event.attendees.push(attendee1);
        
        outlookClient.me.calendar.events.addEvent(event)
        .then(function (response) {
            console.log(response._Id);
        });    

```
<!-- ENDSECTION -->

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->






****


<a name="UpdateEvents"> </a>
## <a name="update-events"></a>更新イベント

REST API:[予定表のイベントの更新](#UpdateAnEvent)

クライアント ライブラリ:[予定表のイベント (クライアント) の更新](#UpdateEventsClient)

<a name="UpdateAnEvent"></a>
###<a name="update-a-calendar-event-rest"></a>予定表のイベント (残りの部分) を更新します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

イベントを変更します。指定したプロパティのみが変更されます。ユーザーが開催者の場合は、サーバーは、すべての出席者に会議の更新を送信します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
PATCH https://outlook.office.com/api/beta/me/events/{event_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|

要求の本文で、書き込み可能な[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)プロパティを指定します。

```
PATCH https://outlook.office.com/api/beta/me/events/AAMkAGE1MFKPQWAAA=?$select=Location
```

**要求のサンプル**

```
PATCH https://outlook.office.com/api/beta/me/events/AAMkAGE0M4v1OAAA=
Content-Type: application/json

{
  "Location": {
    "DisplayName": "Your office",
    "Address": null,
    "Coordinates": null,
    "LocationEmailAddress": "",
    "LocationUri": ""
  }
}
```

**応答の例**

```
Status code: 200

{
  "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events/$entity",
  "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGE0M4v1OAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeNheQ==\"",
  "Id": "AAMkAGE0M4v1OAAA=",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeNheQ==",
  "Categories": [],
  "CreatedDateTime": "2014-01-22T20:49:05.5657528Z",
  "LastModifiedDateTime": "2014-01-22T21:14:17.4886416Z",
  "Subject": "Discuss the Calendar REST API",
  "BodyPreview": "I think it will meet our requirements!",
  "Body": {
    "ContentType": "HTML",
    "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
  },
  "Importance": "Normal",
  "HasAttachments": false,
  "Start": {
      "DateTime": "2014-02-02T18:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "End": {
      "DateTime": "2014-02-02T19:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "Location": {
    "DisplayName": "Your office",
    "Address": null,
    "Coordinates": null,
    "LocationEmailAddress": "",
    "LocationUri": ""
  },
  "ShowAs": "Busy",
  "IsAllDay": false,
  "IsCancelled": false,
  "IsOrganizer": true,
  "ResponseRequested": true,
  "Type": "SingleInstance",
  "SeriesMasterId": null,
  "Attendees": [],
  "Recurrence": null,
  "OriginalEndTimeZone": "Pacific Standard Time",
  "OriginalStartTimeZone": "Pacific Standard Time",
  "Organizer": {
    "EmailAddress": {
      "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
      "Name": "alexd"
    }
  },
  "OnlineMeetingUrl": null
}
```

**応答の種類**

更新された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。ユーザーが開催者の場合は、サーバーは、すべての出席者に会議の更新を送信します。

既定では、応答には、更新されたイベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。 




[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
PATCH https://outlook.office.com/api/v2.0/me/events/{event_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|

要求の本文で、書き込み可能な[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)プロパティを指定します。

**要求のサンプル**

```
PATCH https://outlook.office.com/api/v2.0/me/events/AAMkAGE0M4v1OAAA=
Content-Type: application/json

{
  "Location": {
    "DisplayName": "Your office",
    "Address": null
  }
}
```

**応答の例**

```
Status code: 200

{
  "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/Events/$entity",
  "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGE0M4v1OAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeNheQ==\"",
  "Id": "AAMkAGE0M4v1OAAA=",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeNheQ==",
  "Categories": [],
  "CreatedDateTime": "2014-01-22T20:49:05.5657528Z",
  "LastModifiedDateTime": "2014-01-22T21:14:17.4886416Z",
  "Subject": "Discuss the Calendar REST API",
  "BodyPreview": "I think it will meet our requirements!",
  "Body": {
    "ContentType": "HTML",
    "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
  },
  "Importance": "Normal",
  "HasAttachments": false,
  "Start": {
      "DateTime": "2014-02-02T18:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "End": {
      "DateTime": "2014-02-02T19:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "Location": {
    "DisplayName": "Your office",
    "Address": null
  },
  "ShowAs": "Busy",
  "IsAllDay": false,
  "IsCancelled": false,
  "IsOrganizer": true,
  "ResponseRequested": true,
  "Type": "SingleInstance",
  "SeriesMasterId": null,
  "Attendees": [],
  "Recurrence": null,
  "OriginalEndTimeZone": "Pacific Standard Time",
  "OriginalStartTimeZone": "Pacific Standard Time",
  "Organizer": {
    "EmailAddress": {
      "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
      "Name": "alexd"
    }
  }
}
```

**応答の種類**

更新された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。ユーザーが開催者の場合は、サーバーは、すべての出席者に会議の更新を送信します。

既定では、応答には、更新されたイベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。 

```
PATCH https://outlook.office.com/api/v2.0/me/events/AAMkAGE1MFKPQWAAA=?$select=Location
```




[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
PATCH https://outlook.office.com/api/v1.0/me/events/{event_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|

要求の本文で、書き込み可能な[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)プロパティを指定します。

```REST
{
    "method": "PATCH",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/events/{event_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/events/AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1OAAA=",
    "requestHeaders": {
        "Accept": "application/json",
        "Content-Type": "application/json",
        "Content-Length": 62
    },
    "parameterDetails": [
        {
            "name": "event_id",
            "type": "string",
            "description": "The event ID.",
            "defaultValue": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1OAAA="
        }
    ],
    "requestBody": {
        "Location": {
            "DisplayName": "Your office"
        }
    },
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/Events/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Events('AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1OAAA=')",
        "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeNheQ==\"",
        "Id": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1OAAA=",
        "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeNheQ==",
        "Categories": [],
        "DateTimeCreated": "2014-01-22T20:49:05.5657528Z",
        "DateTimeLastModified": "2014-01-22T21:14:17.4886416Z",
        "Subject": "Discuss the Calendar REST API",
        "BodyPreview": "I think it will meet our requirements!",
        "Body": {
            "ContentType": "HTML",
            "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n</head>\r\n<body>\r\nI think it will meet our requirements!\r\n</body>\r\n</html>\r\n"
        },
        "Importance": "Normal",
        "HasAttachments": false,
        "Start": "2014-02-02T18:00:00-08:00",
        "StartTimeZone": "Pacific Standard Time",
        "End": "2014-02-02T19:00:00-08:00",
        "EndTimeZone": "Pacific Standard Time",
        "Location": {
            "DisplayName": "Your office"
        },
        "ShowAs": "Busy",
        "IsAllDay": false,
        "IsCancelled": false,
        "IsOrganizer": true,
        "ResponseRequested": true,
        "Type": "SingleInstance",
        "SeriesMasterId": null,
        "Attendees": [],
        "Recurrence": null,
        "Organizer": {
            "EmailAddress": {
                "Address": "alexd@a830edad9050849NDA1.onmicrosoft.com",
                "Name": "alexd"
            }
        }
    }
}
```

**応答の種類**

更新された[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)です。ユーザーが開催者の場合は、サーバーは、すべての出席者に会議の更新を送信します。

既定では、応答には、更新されたイベントのすべてのプロパティが含まれています。**$Select**を使用すると、パフォーマンスを最適化する必要があるプロパティだけを指定します。**Id**プロパティが常に返されます。 

```
PATCH https://outlook.office.com/api/v1.0/me/events/AAMkAGE1MFKPQWAAA=?$select=Location
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->






****

<a name="UpdateEventsClient"></a>
### <a name="update-a-calendar-event-client"></a>予定表のイベント (クライアント) の更新します。

イベントを変更します。

複数の更新プログラムでクライアント側を定義し、要求を送信するすべてを一度に (それらのバッチ)、以下のパターンを使用しています。
1. 呼び出す`UpdateAsync(true)`の各エンティティを更新します。指定する`true`、クライアント上でローカルに更新プログラムを登録するが、サーバーにポストされません。
2. 呼び出す`client.Context.SaveChangesAsync()`ローカルに登録されているすべての更新プログラムを投稿します。


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

<!-- CHUCK, feel free to provide client library example that reflects the event breaking changes for beta.  --> 

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)し、[イベント ID を取得](#GetEvents)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Get an existing event by ID
IEvent eventToUpdate = await client.Me.Events[eventId].ExecuteAsync();

// Add attendees
eventToUpdate.Attendees.Add(new Attendee
{
    Type = AttendeeType.Required,
    EmailAddress = new EmailAddress
    {
        Address = "garthf@a830edad9050849NDA1.onmicrosoft.com",
    },
});

// Make other changes
eventToUpdate.Start = new DateTimeOffset(new DateTime(2014, 12, 1, 14, 30, 0));
eventToUpdate.End = new DateTimeOffset(new DateTime(2014, 12, 1, 15, 0, 0));
eventToUpdate.Subject = "New event name";
    
// Commit all changes to the event
await eventToUpdate.UpdateAsync();

// Get an updated property.
string newEventName = eventToUpdate.Subject;
```

<!-- ENDSECTION -->


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)し、[イベント ID を取得](#GetEvents)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Get an existing event by ID
IEvent eventToUpdate = await client.Me.Events[eventId].ExecuteAsync();

// Add attendees
eventToUpdate.Attendees.Add(new Attendee
{
    Type = AttendeeType.Required,
    EmailAddress = new EmailAddress
    {
        Address = "garthf@a830edad9050849NDA1.onmicrosoft.com",
    },
});

// Make other changes
eventToUpdate.Start = new DateTimeOffset(new DateTime(2014, 12, 1, 14, 30, 0));
eventToUpdate.End = new DateTimeOffset(new DateTime(2014, 12, 1, 15, 0, 0));
eventToUpdate.Subject = "New event name";
    
// Commit all changes to the event
await eventToUpdate.UpdateAsync();

// Get an updated property.
string newEventName = eventToUpdate.Subject;
```

<!-- ENDSECTION -->

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->








****

<a name="RespndToEvents"></a>
## <a name="respond-to-events"></a>イベントに応答します。

REST API:[同意」イベント (REST)](#AcceptEvent) | [イベント (残りの部分) を仮承諾](#TentAcceptEvent) | [拒否イベント (他)](#DeclineEvent)

<a name="AcceptEvent"></a>
###<a name="accept-event-rest"></a>イベント (残りの部分) をそのまま使用します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

指定したイベントをそのまま使用します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/accept
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/accept

Content-Type: application/json

{
  "Comment": "Great idea!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
POST https://outlook.office.com/api/v2.0/me/events/{event_id}/accept
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/v2.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/accept

Content-Type: application/json

{
  "Comment": "Great idea!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/v1.0/me/events/{event_id}/accept
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/v1.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/accept

Content-Type: application/json

{
  "Comment": "Great idea!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->





****

<a name="TentAcceptEvent"></a>
###<a name="tentatively-accept-event-rest"></a>イベント (残りの部分) を仮承諾します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

指定されたイベントを仮承諾します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/tentativelyaccept
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/tentativelyaccept

Content-Type: application/json

{
  "Comment": "I'll confirm later!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
POST https://outlook.office.com/api/v2.0/me/events/{event_id}/tentativelyaccept
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/v2.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/tentativelyaccept

Content-Type: application/json

{
  "Comment": "I'll confirm later!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/v1.0/me/events/{event_id}/tentativelyaccept
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/v1.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/tentativelyaccept

Content-Type: application/json

{
  "Comment": "I'll confirm later!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


****

<a name="DeclineEvent"></a>
###<a name="decline-event-rest"></a>拒否イベント (他)

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

指定されたイベントへの招待を辞退します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]



```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/decline
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/decline

Content-Type: application/json

{
  "Comment": "Sorry, maybe next time!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]



```no-highlight
POST https://outlook.office.com/api/v2.0/me/events/{event_id}/decline
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/v2.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/decline

Content-Type: application/json

{
  "Comment": "Sorry, maybe next time!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


```no-highlight
POST https://outlook.office.com/api/v1.0/me/events/{event_id}/decline
```


|**パラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。必須。|
|_本文パラメーター_|
|コメント|string|応答に含まれるテキストです。省略可能です。|
|SendResponse|ブール型| `true`応答では、開催者に送信する場合それ以外の場合、 `false`。省略可能です。既定値は、 `true`。|
 
**要求のサンプル**

```
POST https://outlook.office.com/api/v1.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/decline

Content-Type: application/json

{
  "Comment": "Sorry, maybe next time!",
  "SendResponse": "true"
}
```

**応答**

正常な応答は、HTTP 202 の承諾の応答コードが表示されます。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->



****

<a name="DeleteEvents"> </a>
## <a name="delete-events"></a>イベントを削除します。

REST API: の[予定表のイベント (残りの部分) を削除します。](#DeleteAnEvent)

クライアント ライブラリ:[予定表のイベント (クライアント) を削除します。](#DeleteEventsClient)

<a name="DeleteAnEvent"></a>
###<a name="delete-a-calendar-event-rest"></a>予定表のイベント (残りの部分) を削除します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

イベントは、サインイン中のユーザーの削除済みアイテム フォルダーに移動します。イベントが会議で、サインイン中のユーザーは、開催者の場合、サーバーは、すべての出席者にキャンセルを送信します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

このアクションは、その開催者と会議の出席者には**削除**に、[キャンセル](#CancelEvents)とは異なります。署名ユーザーが会議の開催者の場合は、ユーザーは単に出席者にキャンセル通知のカスタム メッセージを提供することがなく、会議をキャンセルします。

```no-highlight
DELETE https://outlook.office.com/api/beta/me/events/{event_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|


**要求のサンプル**

```
DELETE https://outlook.office.com/api/beta/me/events/AAMkAGE0M4v1OAAA=
```

**応答の例**

状態コード: 204


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
DELETE https://outlook.office.com/api/v2.0/me/events/{event_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|

**要求のサンプル**

```
DELETE https://outlook.office.com/api/v2.0/me/events/AAMkAGE0M4v1OAAA=
```

**応答の例**

状態コード: 204



[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
DELETE https://outlook.office.com/api/v1.0/me/events/{event_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|

```REST
{
    "method": "DELETE",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/events/{event_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/events/AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1OAAA=",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [ 
                {
            "name": "event_id",
            "type": "string",
            "description": "The event ID.",
            "defaultValue": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1OAAA="
        }
    ],
    
    "statusCode": 204
    
}

```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->



****

<a name="DeleteEventsClient"></a>
### <a name="delete-a-calendar-event-client"></a>予定表のイベント (クライアント) を削除します。

イベントは、削除済みアイテム フォルダーに移動します。


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)し、[イベント ID を取得](#GetEvents)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Get an existing event by ID
IEvent eventToDelete = await client.Me.Events[eventId].ExecuteAsync();

//Delete the event
await eventToDelete.DeleteAsync();
```

<!-- ENDSECTION -->

****

<a name="CancelEvents"> </a>
## <a name="cancel-events-preview"></a>(プレビュー) のイベントをキャンセルします。

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

このアクションでは、キャンセル通知を送信し、イベントをキャンセルする会議の開催者を使用します。 

アクションは、イベントを削除済みアイテム フォルダーに移動します。開催者出現のイベント ID を入力しての定期的な会議を取り消すこともこの操作を呼び出すこと、出席者は、(HTTP 400 正しくない要求)、次のエラー メッセージとエラーを取得します。

"要求を完了できません。必要があります会議をキャンセルするのには開催者である。」

この操作が異なる[削除](#DeleteEvents)**キャンセル**は、開催者のみに使用され、構成内容の変更キャンセルについて出席者にカスタム メッセージを送信することができます。

```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/Cancel
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|_本文パラメーター_|
|コメント|string|すべての出席者に送信の取り消しについてのコメントです。|

**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/events/AAMkAGE0M4v1OAAA=/Cancel

Content-Type: application/json
{
  "Comment": "Cancelling this meeting as there is a time conflict for most folks."
}
```

**応答の例**

状態コード: 202 の承諾


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->



<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

この機能は、ベータ版だけで現在利用可能です。詳細については、**ベータ版**の選択、記事の右上隅にコントロールを使用します。 

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->


[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

この機能は、ベータ版だけで現在利用可能です。詳細については、**ベータ版**の選択、記事の右上隅にコントロールを使用します。 

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->


****

<a name="GetAttachments"> </a>
## <a name="get-attachments"></a>添付ファイルを取得します。

添付ファイルのコレクションを取得するか、添付ファイルを取得します。

REST API: は[(残りの部分) の添付データのコレクションを取得する](#GetAttachmentCollection) | [(残りの部分) の添付ファイルを取得します。](#GetAttachment)

<a name="GetAttachmentCollection"> </a>
###<a name="get-an-attachment-collection-rest"></a>(REST) の添付データのコレクションを取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

特定のイベントから添付ファイルを取得します。

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}/attachments
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|


**応答の種類**

[FileAttachment](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)、 [ItemAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)、または[ReferenceAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource)の型の可能性がある添付ファイルのコレクションです。


**要求のサンプル**

```
GET https://outlook.office.com/api/beta/me/events/AAMkAGI2NGTG9yAAA=/attachments
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events('AAMkAGI2NG9yAAA%3D')/Attachments",
    "value": [
        {
            "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2NGTG9yAAA=')/Attachments('AAMkAGI2NGLwydGuOzcHf1FBlo=')",
            "Id": "AAMkAGI2NGLwydGuOzcHf1FBlo=",
            "LastModifiedDateTime": "2014-10-22T00:30:26Z",
            "Name": "Company Party.docx",
            "ContentType": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
            "Size": 11647,
            "IsInline": false,
            "ContentId": null,
            "ContentLocation": null,
            "ContentBytes": "UEsDBBQABgAIAAAAIQDfpNJs...AAF4pAAAAAA=="
        }
    ]
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v2.0/me/events/{event_id}/attachments
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|


**応答の種類**

[FileAttachment](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)または[ItemAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)の種類の添付ファイルのコレクションです。


**要求のサンプル**

```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGI2NGTG9yAAA=/attachments
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/Events('AAMkAGI2NG9yAAA%3D')/Attachments",
    "value": [
        {
            "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
            "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2NGTG9yAAA=')/Attachments('AAMkAGI2NGLwydGuOzcHf1FBlo=')",
            "Id": "AAMkAGI2NGLwydGuOzcHf1FBlo=",
            "LastModifiedDateTime": "2014-10-22T00:30:26Z",
            "Name": "Company Party.docx",
            "ContentType": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
            "Size": 11647,
            "IsInline": false,
            "ContentId": null,
            "ContentLocation": null,
            "ContentBytes": "UEsDBBQABgAIAAAAIQDfpNJs...AAF4pAAAAAA=="
        }
    ]
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|


**応答の種類**

[FileAttachment](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)または[ItemAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)の種類の添付ファイルのコレクションです。


```REST-i
{
    "method": "GET",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/events/AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAA=/attachments",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "event_id",
            "type": "string",
            "description": "The event ID.",
            "defaultValue": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAA="
        }
    ],
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/CalendarGroups/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/CalendarGroups('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x0+g==\"",
        "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=",
        "Name": "My Calendars",
        "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+g==",
        "ClassId": "0006f0b7-0000-0000-c000-000000000046"
    }
}
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->



****


<a name="GetAttachment"> </a>
###<a name="get-an-attachment-rest"></a>(REST) の添付ファイルを取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

特定のイベントから添付ファイルを取得します。

<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}/attachments/{attachment_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|attachment_id|string|添付ファイルの id。|

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


**応答の種類**

要求された[ファイルの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)、[アイテムの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)、または[添付ファイルの参照](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource)。


**要求のサンプル**

次の例では、特定のイベントに添付ファイルを取得します。

```
GET https://outlook.office.com/api/beta/me/events/AAMkAGI2WRAAADTG9yAAA=/attachments/AAMkAGI2TG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Events('AAMkAGI2WRAAADTG9yAAA%3D')/Attachments/$entity",
    "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
    "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2WRAAADTG9yAAA=')/Attachments('AAMkAGI2TG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=')",
    "Id": "AAMkAGI2TG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=",
    "LastModifiedDateTime": "2014-10-22T00:30:26Z",
    "Name": "Company Party.docx",
    "ContentType": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
    "Size": 11647,
    "IsInline": false,
    "ContentId": null,
    "ContentLocation": null,
    "ContentBytes": "UEsDBBQABgAIAAAAIQD...AAF4pAAAAAA=="
}
```

**サンプル リクエスト (添付ファイルを参照)**

次の例では、イベントで添付ファイルの参照を取得します。

```
GET https://outlook.office.com/api/beta/me/events('AAMkAGE1Mbs88AADggYEcAAA=')/attachments('AAMkAGE1Mbs88AADggYEcAAABEgAQAABWAoLgP3REt_LWRG8ORv4=')
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#users('ddfcd489-628b-40d7-b48b-57002df800e5')/events('AAMkAGE1Mbs88AADggYEcAAA%3D')/attachments/$entity",
    "@odata.type": "#Microsoft.OutlookServices.ReferenceAttachment",
    "id": "AAMkAGE1Mbs88AADggYEcAAABEgAQAABWAoLgP3REt_LWRG8ORv4=",
    "lastModifiedDateTime": "2016-03-22T22:27:20Z",
    "name": "Hydrangea picture",
    "contentType": null,
    "size": 412,
    "isInline": false,
    "sourceUrl": "https://contoso-my.spoppe.com/personal/danas_contoso_onmicrosoft_com/Documents/Pics/hydrangea.jpg",
    "providerType": "oneDriveBusiness",
    "thumbnailUrl": null,
    "previewUrl": null,
    "permission": "edit",
    "isFolder": false
}

```


**($ は、添付ファイルの展開) 要求のサンプル**

次の例では、取得し、イベントのプロパティを持つ 2 つの参照の添付ファイルのインラインを展開します。

```
GET https://outlook.office.com/api/beta/me/events('AAMkAGE1Mbs88AADggYEcAAA=')?$expand=attachments
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#users('ddfcd489-628b-40d7-b48b-57002df800e5')/events/$entity",
    "@odata.etag": "W/\"mODEKWhc/Um6lA3uPm7PPAAA4KZrtA==\"",
    "id": "AAMkAGE1Mbs88AADggYEcAAA=",
    "createdDateTime": "2016-03-22T22:19:58.1359352Z",
    "lastModifiedDateTime": "2016-03-22T22:39:09.9335289Z",
    "changeKey": "mODEKWhc/Um6lA3uPm7PPAAA4KZrtA==",
    "categories": [
    ],
    "originalStartTimeZone": "Pacific Standard Time",
    "originalEndTimeZone": "Pacific Standard Time",
    "responseStatus": {
        "response": "organizer",
        "time": "0001-01-01T00:00:00Z"
    },
    "iCalUId": "040000008200E00074C5B7101A82E008000000005895FCF78884D10100000000000000001000000099DD7CA6BCF37C4F9F7DAACCADDD6B89",
    "reminderMinutesBeforeStart": 15,
    "isReminderOn": true,
    "hasAttachments": true,
    "subject": "Plan Easter egg hunt!",
    "body": {
        "contentType": "html",
        "content": "<html>\r\n<body>\r\nLet's get organized for this weekend's gathering.\r\n</body>\r\n</html>\r\n"
    },
    "bodyPreview": "Let's get organized for this weekend's gathering.",
    "importance": "normal",
    "sensitivity": "normal",
    "start": {
        "dateTime": "2016-03-26T17:00:00.0000000",
        "timeZone": "UTC"
    },
    "end": {
        "dateTime": "2016-03-26T18:00:00.0000000",
        "timeZone": "UTC"
    },
    "location": {
        "displayName": "",
        "address": {
            "type": "unknown"
        },
        "coordinates": {
        }
    },
    "isAllDay": false,
    "isCancelled": false,
    "isOrganizer": true,
    "recurrence": null,
    "responseRequested": true,
    "seriesMasterId": null,
    "showAs": "busy",
    "type": "singleInstance",
    "attendees": [
        {
            "status": {
                "response": "none",
                "time": "0001-01-01T00:00:00Z"
            },
            "type": "required",
            "emailAddress": {
                "name": "Randi Welch",
                "address": "randiw@contoso.onmicrosoft.com"
            }
        }
    ],
    "organizer": {
        "emailAddress": {
            "name": "Dana Swope",
            "address": "danas@contoso.onmicrosoft.com"
        }
    },
    "webLink": "https://outlook.office.com/owa/?ItemID=AAMkAGE1Mbs88AADggYEcAAA%3D&exvsurl=1&viewmodel=ICalendarItemDetailsViewModelFactory",
    "onlineMeetingUrl": null,
    "attachments@odata.context": "https://outlook.office.com/api/beta/$metadata#users('ddfcd489-628b-40d7-b48b-57002df800e5')/events('AAMkAGE1Mbs88AADggYEcAAA%3D')/attachments",
    "attachments": [
        {
            "@odata.type": "#Microsoft.OutlookServices.ReferenceAttachment"",
            "id": "AAMkAGE1Mbs88AADggYEcAAABEgAQAABWAoLgP3REt_LWRG8ORv4=",
            "lastModifiedDateTime": "2016-03-22T22:27:20Z",
            "name": "Hydrangea picture",
            "contentType": null,
            "size": 412,
            "isInline": false,
            "sourceUrl": "https://contoso-my.spoppe.com/personal/danas_contoso_onmicrosoft_com/Documents/Pics/hydrangea.jpg",
            "providerType": "oneDriveBusiness",
            "thumbnailUrl": null,
            "previewUrl": null,
            "permission": "edit",
            "isFolder": false
        },
        {
            "@odata.type": "#Microsoft.OutlookServices.ReferenceAttachment"",
            "id": "AAMkAGE1Mbs88AADggYEcAAABEgAQAE1rHHth7YNLlR9WsgnODy0=",
            "lastModifiedDateTime": "2016-03-22T22:39:09Z",
            "name": "Koala picture",
            "contentType": null,
            "size": 382,
            "isInline": false,
            "sourceUrl": "https://contoso-my.spoppe.com/personal/danas_contoso_onmicrosoft_com/Documents/Pics/koala.jpg",
            "providerType": "oneDriveBusiness",
            "thumbnailUrl": null,
            "previewUrl": null,
            "permission": "edit",
            "isFolder": false
        }
    ]
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v2.0/me/events/{event_id}/attachments/{attachment_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|attachment_id|string|添付ファイルの id。|

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


**応答の種類**

要求された[ファイルの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)または[アイテムの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)の場合です。


**要求のサンプル**

```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGI2WRAAADTG9yAAA=/attachments/AAMkAGI2TG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/Events('AAMkAGI2WRAAADTG9yAAA%3D')/Attachments/$entity",
    "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
    "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Events('AAMkAGI2WRAAADTG9yAAA=')/Attachments('AAMkAGI2TG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=')",
    "Id": "AAMkAGI2TG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=",
    "LastModifiedDateTime": "2014-10-22T00:30:26Z",
    "Name": "Company Party.docx",
    "ContentType": "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
    "Size": 11647,
    "IsInline": false,
    "ContentId": null,
    "ContentLocation": null,
    "ContentBytes": "UEsDBBQABgAIAAAAIQD...AAF4pAAAAAA=="
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments/{attachment_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|attachment_id|string|添付ファイルの id。|

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


**応答の種類**

要求された[ファイルの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)または[アイテムの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)の場合です。


```REST-i
{
    "method": "GET",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments/{attachment_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/events/AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAA=/attachments/AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "event_id",
            "type": "string",
            "description": "The event ID.",
            "defaultValue": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAA="
        },
        {
            "name": "attachment_id",
            "type": "string",
            "description": "The attachment ID.",
            "defaultValue": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo="
        }
    ],
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/CalendarGroups/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/CalendarGroups('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x0+g==\"",
        "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=",
        "Name": "My Calendars",
        "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+g==",
        "ClassId": "0006f0b7-0000-0000-c000-000000000046"
    }
}
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->




****


<a name="CreateAttachments"> </a>
## <a name="create-attachments"></a>添付ファイルを作成します。
添付ファイルまたは[アイテムの添付ファイルを作成する](#CreateItemAttachment)イベントを作成できます。

REST API:[添付ファイル (残りの部分) を作成する](#CreateFileAttachment) | [(REST) アイテムの添付ファイルを作成する](#CreateItemAttachment) | 
[を参照の添付ファイル (残りの部分) を作成します。](#CreateReferenceAttachment)


<a name="CreateFileAttachment"></a>
###<a name="create-a-file-attachment-rest"></a>(REST) 添付ファイルを作成します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

イベントに添付ファイルを追加します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/attachments
```

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
POST https://outlook.office.com/api/v2.0/me/events/{event_id}/attachments
```

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|_本文パラメーター_|
|@odata.type| string | #Microsoft.OutlookServices.FileAttachment |
|名前|string|添付ファイルの名前です。|
|ContentBytes|バイナリ|添付するファイルです。|
 
<!-- Add post GA
```REST
[!INCLUDE [calendar_api_create_file_attachment](./_data/calendar_api_create_file_attachment.json)]
``` -->

**応答の種類**

新しい[添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)。

****


<a name="CreateItemAttachment"></a>
###<a name="create-an-item-attachment-rest"></a>(REST) アイテムの添付ファイルを作成します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

イベント アイテムの添付ファイルを追加します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/attachments
```

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
POST https://outlook.office.com/api/v2.0/me/events/{event_id}/attachments
```

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|_本文パラメーター_|
|@odata.type| string | #Microsoft.OutlookServices.ItemAttachment |
|名前|string|添付ファイルの名前です。|
|アイテム|[メッセージ](..\api\complex-types-for-mail-contacts-calendar.md#MessageResource)、[イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)、または[取引先担当者](..\api\complex-types-for-mail-contacts-calendar.md#ContactResource)エンティティです。|添付する項目。|
 

<!--Post GA
```REST
[!INCLUDE [calendar_api_create_item_attachment](./_data/calendar_api_create_item_attachment.json)]
``` -->


**応答の種類**

新しい[アイテムの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)です。

****

<a name="CreateReferenceAttachment"></a>

###<a name="create-a-reference-attachment-rest"></a>(REST) 添付ファイルの参照を作成します。

<!-- ==================================== Start beta content ====================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

_**スコープが必要です**: https://outlook.office.com/mail.readwrite_

イベントの添付ファイル、参照を追加します。

```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/attachments
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|String|イベント id です。|
|_本文パラメーター_|
|@odata.type|String|```#Microsoft.OutlookServices.ReferenceAttachment```|
|名前|文字列|添付ファイルの表示名。必須。|
|直すこと|String | 添付ファイルのコンテンツを取得する URL です。フォルダーへの URL の場合は、し、Outlook または Outlook web 上で正しく表示されるフォルダーの**IsFolder** true に設定します。必須。|

要求の本体で、パラメーター**の名前**と**発行し直すこと**と、書き込み可能な[添付ファイルの参照](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource)のプロパティを指定します。



**応答の種類**

[添付ファイルの参照](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource)。


**要求のサンプル**

次の例では、既存のイベントへの参照の添付ファイルを追加します。添付ファイルは、ビジネスの OneDrive 上のファイルへのリンクです。

```
POST https://outlook.office.com/api/beta/me/events('AAMkAGE1Mbs88AADggYEcAAA=')/attachments
Content-Type: application/json

{
    "@odata.type": "#Microsoft.OutlookServices.ReferenceAttachment"", 
    "Name": "Hydrangea picture", 
    "SourceUrl": "https://contoso-my.spoppe.com/personal/danas_contoso_onmicrosoft_com/Documents/Pics/hydrangea.jpg", 
    "ProviderType": "oneDriveBusiness", 
    "Permission": "Edit", 
    "IsFolder": "False" 
 }
```


**応答の例**

```
Status code: 201 Created

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#users('ddfcd489-628b-40d7-b48b-57002df800e5')/events('AAMkAGE1Mbs88AADggYEcAAA%3D')/attachments/$entity",
    "@odata.type": "#Microsoft.OutlookServices.ReferenceAttachment"",
    "Id": "AAMkAGE1Mbs88AADggYEcAAABEgAQAABWAoLgP3REt_LWRG8ORv4=",
    "LastModifiedDateTime": "2016-03-22T22:27:20Z",
    "Name": "Hydrangea picture",
    "ContentType": null,
    "Size": 412,
    "IsInline": false,
    "SourceUrl": "https://contoso-my.spoppe.com/personal/danas_contoso_onmicrosoft_com/Documents/Pics/hydrangea.jpg",
    "ProviderType": "oneDriveBusiness",
    "ThumbnailUrl": null,
    "PreviewUrl": null,
    "Permission": "edit",
    "IsFolder": false
}
```


**要求のサンプル**

イベントを作成する場合と同じ呼び出し内の参照の添付ファイルを追加する例を次にします。添付ファイルは、ビジネスの OneDrive 上のファイルへのリンクです。

```
POST https://outlook.office.com/api/beta/me/events
Content-Type: application/json

{
  "Subject": "Plan Easter egg hunt!",
  "Body": {
    "ContentType": "HTML",
    "Content": "Let's get organized for this weekend's gathering."
  },
  "Start": {
      "DateTime": "2016-03-25T10:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "End": {
      "DateTime": "2016-03-25T11:00:00",
      "TimeZone": "Pacific Standard Time"
  },
  "Attendees": [
    {
      "EmailAddress": {
        "Address": "randiw@contoso.onmicrosoft.com",
        "Name": "Randi Welch"
      },
      "Type": "Required"
    }
  ],
  "Attachments": [
      {
        "@odata.type": "#Microsoft.OutlookServices.ReferenceAttachment"", 
        "Name": "Hydrangea picture", 
        "SourceUrl": "https://contoso-my.spoppe.com/personal/danas_contoso_onmicrosoft_com/Documents/Pics/hydrangea.jpg", 
        "ProviderType": "oneDriveBusiness", 
        "Permission": "Edit", 
        "IsFolder": "False" 
      }
  ]
}
```


**応答の例**

```
Status code: 201 Created

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#users('ddfcd489-628b-40d7-b48b-57002df800e5')/events/$entity",
    "@odata.etag": "W/\"mODEKWhc/Um6lA3uPm7PPAAA4KZrrg==\"",
    "Id": "AAMkAGE1Mbs88AADggYEbAAA=",
    "CreatedDateTime": "2016-03-22T22:09:26.2918604Z",
    "LastModifiedDateTime": "2016-03-22T22:09:27.0754806Z",
    "ChangeKey": "mODEKWhc/Um6lA3uPm7PPAAA4KZrrg==",
    "Categories": [
    ],
    "OriginalStartTimeZone": "Pacific Standard Time",
    "OriginalEndTimeZone": "Pacific Standard Time",
    "ResponseStatus": {
        "Response": "Organizer",
        "Time": "0001-01-01T00:00:00Z"
    },
    "iCalUId": "040000008200E00074C5B7101A82E0080000000043FB607F8784D101000000000000000010000000B3A31CD7479252448ECE77242DE92587",
    "ReminderMinutesBeforeStart": 15,
    "IsReminderOn": true,
    "HasAttachments": true,
    "Subject": "Plan Easter egg hunt!",
    "Body": {
        "contentType": "html",
        "content": "<html>\r\n<body>\r\nLet's get organized for this weekend's gathering.\r\n</body>\r\n</html>\r\n"
    },
    "BodyPreview": "Let's get organized for this weekend's gathering.",
    "Importance": "normal",
    "Sensitivity": "normal",
    "Start": {
        "DateTime": "2016-03-25T10:00:00.0000000",
        "TimeZone": "Pacific Standard Time"
    },
    "End": {
        "DateTime": "2016-03-25T11:00:00.0000000",
        "TimeZone": "Pacific Standard Time"
    },
    "Location": {
        "DisplayName": "",
        "Address": {
            "Type": "unknown"
        },
        "Coordinates": {
        }
    },
    "IsAllDay": false,
    "IsCancelled": false,
    "IsOrganizer": true,
    "Recurrence": null,
    "ResponseRequested": true,
    "SeriesMasterId": null,
    "ShowAs": "busy",
    "Type": "singleInstance",
    "Attendees": [
        {
            "Status": {
                "Response": "none",
                "Time": "0001-01-01T00:00:00Z"
            },
            "Type": "required",
            "EmailAddress": {
                "Name": "Randi Welch",
                "Address": "randiw@contoso.onmicrosoft.com"
            }
        }
    ],
    "Organizer": {
        "EmailAddress": {
            "Name": "Dana Swope",
            "Address": "danas@contoso.onmicrosoft.com"
        }
    },
    "WebLink": "https://outlook.office.com/owa/?ItemID=AAMkAGE1Mbs88AADggYEbAAA%3D&exvsurl=1&viewmodel=ICalendarItemDetailsViewModelFactory",
    "OnlineMeetingUrl": null,
    "Attachments@odata.context": "https://outlook.office.com/api/beta/$metadata#users('ddfcd489-628b-40d7-b48b-57002df800e5')/events('AAMkAGE1Mbs88AADZ0CU9AAA%3D')/attachments",
    "Attachments": [
    {
      "@odata.type": "#Microsoft.OutlookServices.ReferenceAttachment",
      "Id": "AAMkAGE1Mbs88AADZ0CU9AAABEgAQAGe4H1iqXwtLsrCCLLkDxqo=",
      "LastModifiedDateTime": null,
      "Name": Hydrangea picture,
      "ContentType": null,
      "Size": 0,
      "IsInline": false,
      "SourceUrl": "https://contoso-my.spoppe.com/personal/danas_contoso_onmicrosoft_com/Documents/Pics/hydrangea.jpg",
      "ProviderType": "oneDriveBusiness",
      "ThumbnailUrl": null,
      "PreviewUrl": null,
      "Permission": "edit",
      "IsFolder": false
    }
    ]
}

```

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End beta content ====================================================== -->

<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

この機能は、ベータ版だけで現在利用可能です。詳細については、**ベータ版**の選択、記事の右上隅にコントロールを使用します。

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->


[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

この機能は、ベータ版だけで現在利用可能です。詳細については、**ベータ版**の選択、記事の右上隅にコントロールを使用します。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->



****


<a name="DeleteAttachments"> </a>
## <a name="delete-attachments"></a>添付ファイルを削除します。

イベントの添付ファイルを削除します。

REST API: は[、イベントの添付ファイル (残りの部分) を削除](#DeleteAnEventAttachment)

<a name="DeleteAnEventAttachment"></a>
###<a name="delete-an-event-attachment-rest"></a>(REST) イベントの添付ファイルを削除します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

イベントの指定した添付ファイルを削除します。添付ファイルには、[添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)、[アイテムの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)、または[添付ファイルの参照](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource)ができます。

```no-highlight
DELETE https://outlook.office.com/api/beta/me/events/{event_id}/attachments/{attachment_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|attachment_id|string|添付ファイルの id。|

**要求のサンプル**

```
DELETE https:/outlook.office.com/api/beta/me/events/AAMkAGE0MG4v1OAAA=/attachments/AAMkAGITG9yAAA=
```

**応答の例**

```
Status code: 204
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

イベントの指定した添付ファイルを削除します。添付ファイル[添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)または[アイテムの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)を使用できます。

```no-highlight
DELETE https://outlook.office.com/api/v2.0/me/events/{event_id}/attachments/{attachment_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|attachment_id|string|添付ファイルの id。|

**要求のサンプル**

```
DELETE https:/outlook.office.com/api/v2.0/me/events/AAMkAGE0MG4v1OAAA=/attachments/AAMkAGITG9yAAA=
```

**応答の例**

```
Status code: 204
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

イベントの指定した添付ファイルを削除します。添付ファイル[添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource)または[アイテムの添付ファイル](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)を使用できます。

```no-highlight
DELETE https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments/{attachment_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|event_id|string|イベント id です。|
|attachment_id|string|添付ファイルの id。|

```REST
{
    "method": "DELETE",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments/{attachment_id}",
    "requestUrl": "https:/outlook.office.com/api/v1.0/me/events/AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1OAAA=/attachments/AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAA=",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "event_id",
            "type": "string",
            "description": "The event ID.",
            "defaultValue": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAENAAAmP1Ln1wcHRariNdTMGAO9AAAV4v1OAAA="
        },
        {
            "name": "event_id",
            "type": "string",
            "description": "The attachment ID.",
            "defaultValue": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAENAACd9nJ-tVysQos2hTfspaWRAAADTG9yAAA="
        }
    ],
    "statusCode": 204

}

```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->

<a name="GetReminders" > </a>
##アラームを取得します。

予定表から 2 つの日付と時刻の間でイベントの通知の一覧を取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
GET https://outlook.office.com/api/beta/me/ReminderView(StartDateTime='{DateTime}',EndDateTime='{DateTime}')
```
|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントのデフォルトのタイム ゾーンです。|
|_URL パラメーター_|
|させる|string|開始日付と時刻の確認メッセージが返される。|
|EndDateTime|string|終了日付と時刻の確認メッセージが返される。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、UTC にタイム ゾーンを設定します。

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->


<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v2.0/me/ReminderView(StartDateTime='{DateTime}',EndDateTime='{DateTime}')
```
|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_ヘッダーのパラメーター_|
|希望します。 |outlook.timezone|応答内のイベントのデフォルトのタイム ゾーンです。|
|_URL パラメーター_|
|させる|string|開始日付と時刻の確認メッセージが返される。|
|EndDateTime|string|終了日付と時刻の確認メッセージが返される。|

使用して、_選択: outlook.timezone_イベントの開始および終了に使用するタイム ゾーンを指定するのにはヘッダーが応答に時間です。イベントは、別のタイム ゾーンで作成されている場合は、指定されたタイム ゾーンに、開始時刻と終了時刻が調整されます。サポートされているタイム ゾーン名の[一覧](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)を参照してください。場合、_選択: outlook.timezone_ヘッダーが指定されていない、UTC にタイム ゾーンを設定します。

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

この機能は、ベータ版と v2.0 のバージョンのみで利用可能です。詳細については、資料および選択の**バージョン 2.0**または**ベータ版**の右上隅にコントロールを使用します。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->


<a name="SnoozeReminders"> </a>
##アラームの再通知します。

までは新しいアラームを延期するのには、アラーム再通知します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
POST https://outlook.office.com/api/beta/me/Events('{id}')/SnoozeReminder
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|id|string|イベントの ID です。|
|_本文パラメーター_|
|NewReminderTime|[DateTimeTimeZone](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)|アラームをトリガーする新しい日付と時刻。|

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/beta/me/Events('{id}')/SnoozeReminder
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|id|string|イベントの ID です。|
|_本文パラメーター_|
|NewReminderTime|[DateTimeTimeZone](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)|アラームをトリガーする新しい日付と時刻。|

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

この機能は、ベータ版と v2.0 のバージョンのみで利用可能です。詳細については、資料および選択の**バージョン 2.0**または**ベータ版**の右上隅にコントロールを使用します。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->

<a name="DismissReminders"> </a>
##アラームを消す

Dissmiss トリガーされたアラームを設定します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
POST https://outlook.office.com/api/beta/me/Events({id})/DismissReminder
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|id|string|イベントの ID です。|


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/beta/me/Events({id})/DismissReminder
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|id|string|イベントの ID です。|

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

この機能は、ベータ版と v2.0 のバージョンのみで利用可能です。詳細については、資料および選択の**バージョン 2.0**または**ベータ版**の右上隅にコントロールを使用します。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


<a name="GetCalendars"> </a>
##カレンダーを取得します。

カレンダーのコレクションを取得するか、カレンダーを取得します。

REST API: [(残りの部分) のカレンダーのコレクションを取得](#GetCalendarCollection)の | [カレンダー (残りの部分) を取得します。](#GetCalendar)

クライアント ライブラリ: [(クライアント) の予定表またはカレンダー コレクションを取得します。](#GetCalendarsClient)

<a name="GetCalendarCollection"> </a>
###<a name="get-a-calendar-collection-rest"></a>(REST) のカレンダーのコレクションを取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

すべてのユーザーの予定表の取得 (`calendars`) または特定の予定表グループの予定表を取得します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]



```no-highlight
GET https://outlook.office.com/api/beta/me/calendars
GET https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}/calendars
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#UseOdataQueryParameters)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calender_group_id|string|予定表グループの id。|


**要求のサンプル**

```
https://outlook.office.com/api/beta/me/calendars
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Calendars",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Calendars('AAMkAGI2TGuLAAA=')",
            "Id": "AAMkAGI2TGuLAAA=",
            "Name": "Calendar",
            "Color": "Auto",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w=="
        }
    ]
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]



```no-highlight
GET https://outlook.office.com/api/v2.0/me/calendars
GET https://outlook.office.com/api/v2.0/me/calendargroups/{calendar_group_id}/calendars
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#UseOdataQueryParameters)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calender_group_id|string|予定表グループの id。|

**要求のサンプル**

```
https://outlook.office.com/api/v2.0/me/calendars
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/Calendars",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Calendars('AAMkAGI2TGuLAAA=')",
            "Id": "AAMkAGI2TGuLAAA=",
            "Name": "Calendar",
            "Color": "Auto",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w=="
        }
    ]
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v1.0/me/calendars
GET https://outlook.office.com/api/v1.0/me/calendargroups/{calendar_group_id}/calendars
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#UseOdataQueryParameters)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calender_group_id|string|予定表グループの id。|


```REST-i
{
    "method": "GET",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendars",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendars",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/Calendars",
        "value": [
            {
                "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Calendars('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuLAAA=')",
                "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x0+w==\"",
                "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuLAAA=",
                "Name": "Calendar",
                "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w=="
            }
        ]
    }
}
```

**応答の種類**

要求された[カレンダー](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource)のコレクションです。

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->



****

<a name="GetCalendar"> </a>
###<a name="get-a-calendar-rest"></a>カレンダー (残りの部分) を取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

ID でカレンダーを取得します。使用して、ユーザーのプライマリの予定表を表示できるよう、`../me/calendar`エンドポイントです。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/calendars/{calendar_id}
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|


**要求のサンプル**

```
GET https://outlook.office.com/api/beta/me/calendars/AAMkAGI2TGuLAAA=
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Calendars/$entity",
    "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Calendars('AAMkAGI2TGuLAAA=')",
    "Id": "AAMkAGI2TGuLAAA=",
    "Name": "Calendar",
    "Color": "Auto",
    "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w=="
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v2.0/me/calendars/{calendar_id}
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|


**要求のサンプル**

```
GET https://outlook.office.com/api/v2.0/me/calendars/AAMkAGI2TGuLAAA=
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/Calendars/$entity",
    "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Calendars('AAMkAGI2TGuLAAA=')",
    "Id": "AAMkAGI2TGuLAAA=",
    "Name": "Calendar",
    "Color": "Auto",
    "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w=="
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|


```REST-i
{
    "method": "GET",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendars/AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuLAAA=",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "calendar_id",
            "type": "string",
            "description": "The calendar ID.",
            "defaultValue": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuLAAA="
        }
    ],
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/Calendars/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Calendars('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuLAAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x0+w==\"",
        "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuLAAA=",
        "Name": "Calendar",
        "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w=="
    }
}
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->

**応答の種類**

要求された[カレンダー](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource)です。

****

<a name="GetCalendarsClient"> </a>
###<a name="get-a-calendar-collection-or-a-calendar-client"></a>(クライアント) の予定表またはカレンダー コレクションを取得します。

ユーザーのカレンダーを取得します。ユーザーの既定のカレンダーを取得するを使用して、`client.Me.Calendar`のショートカットのプロパティです。別のカレンダーを取得するには、**カレンダー**のコレクションのインデックスとして予定表の ID を指定または**GetById**メソッドを使用します。

例:`client.Me.Calendars[calendarId].ExecuteAsync()`


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


**メモ**カレンダーのコレクションは、**選択**、**並べ替え**、および**実行**のようなクエリ式をサポートします。

次の使用例は、 [Outlook のサービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)するメソッドを呼び出します。

<!-- BEGINSECTION class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar" -->

```cs-i
var outlookClient = await CreateOutlookClientAsync("Calendar");
var calendars = await outlookClient.Me.Calendars
  .Take(10)
  .ExecuteAsync();

foreach(var calendar in calendars.CurrentPage)
{
  System.Diagnostics.Debug.WriteLine("Calendar '{0}'.", calendar.Name);
}

```
```javascript-i
outlookClient.me.calendars.getCalendars().fetchAll(100).then(function(result) {
    result.forEach(function (calendar) {
        console.log('Calendar "' + calendar.name + '", URL ' + calendar.path)
    });
}, function(error) {
    console.log(error);
});
```

<!-- ENDSECTION -->

****

<a name="CreateCalendars"> </a>
## <a name="create-calendars"></a>予定表を作成します。

REST API: [(残りの部分) の予定表を作成します。](#CreateACalendar)

クライアント ライブラリ: [(クライアント) の予定表を作成します。](#CreateCalendarsClient)

<a name="CreateACalendar"></a>
###<a name="create-a-calendar-rest"></a>(REST) カレンダーを作成します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

使用して既定の予定表グループの予定表を作成、`../me/calendars`のショートカット、または特定の予定表グループのグループへの投稿で`calendars`エンドポイントです。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
POST https://outlook.office.com/api/beta/me/calendars
POST https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}/calendars
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calender_group_id|string|予定表グループ ID、特定のグループの予定表を取得している場合です。|
|_本文パラメーター_|
|名前|string|新しいカレンダーの名前です。|
 

**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/calendars
Content-Type: application/json

{
  "Name": "Social"
}

```

**応答の例**

```
Status code: 201

{
  "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Calendars/$entity",
  "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Calendars('AAMkAGE4xLHAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SQ==\"",
  "Id": "AAMkAGE4xLHAAA=",
  "Name": "Social",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SQ=="
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
POST https://outlook.office.com/api/v2.0/me/calendars
POST https://outlook.office.com/api/v2.0/me/calendargroups/{calendar_group_id}/calendars
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calender_group_id|string|予定表グループ ID、特定のグループの予定表を取得している場合です。|
|_本文パラメーター_|
|名前|string|新しいカレンダーの名前です。|
 

**要求のサンプル**

```
POST https://outlook.office.com/api/v2.0/me/calendars
Content-Type: application/json

{
  "Name": "Social"
}
```

**応答の例**

```
Status code: 201

{
  "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/Calendars/$entity",
  "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Calendars('AAMkAGE4xLHAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SQ==\"",
  "Id": "AAMkAGE4xLHAAA=",
  "Name": "Social",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SQ=="
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/v1.0/me/calendars
POST https://outlook.office.com/api/v1.0/me/calendargroups/{calendar_group_id}/calendars
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calender_group_id|string|予定表グループ ID、特定のグループの予定表を取得している場合です。|
|_本文パラメーター_|
|名前|string|新しいカレンダーの名前です。|
 


```REST
{
    "method": "POST",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendars",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendars",
    "requestHeaders": {
        "Accept": "application/json",
        "Content-Type": "application/json",
        "Content-Length": 22
    },
    "parameterDetails": [],
    "requestBody": {
        "Name": "Social"
    },
    "statusCode": 201,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/Calendars/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Calendars('AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLHAAA=')",
        "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SQ==\"",
        "Id": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLHAAA=",
        "Name": "Social",
        "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SQ=="
    }
}
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->



**応答の種類**

新しい[カレンダー](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource)です。

****

<a name="CreateCalendarsClient"> </a>
### <a name="create-a-calendar-client"></a>カレンダー (クライアント) を作成します。

カレンダーを作成します。イベントを作成する方法の例については、[作成するイベント](#CreateEventsClient)を参照してください。


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
Calendar newCal = new Calendar
{
    Name = "Personal"
};

// Add the calendar to the Calendars collection
await client.Me.Calendars.AddCalendarAsync(newCal);

// Get the ID of the calendar
string calendarId = newCal.Id;
```

<!-- ENDSECTION -->

****


<a name="UpdateCalendars"> </a>
## <a name="update-calendars"></a>予定表を更新します。

REST API: [(残りの部分) の予定表を更新](#UpdateACalendar)

クライアント ライブラリ: [(クライアント) の予定表を更新](#UpdateCalendarsClient)

<a name="UpdateACalendar"></a>
###<a name="update-a-calendar-rest"></a>(REST) の予定表を更新します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

カレンダーの名前を変更します。**名前**は、のみ書き込み可能な[カレンダー](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource)プロパティです。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
PATCH https://outlook.office.com/api/beta/me/calendars/{calendar_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|
|_本文パラメーター_|
|名前|string|カレンダーの新しい名前です。|


**要求のサンプル**

```
PATCH https://outlook.office.com/api/beta/me/calendars/AAMkAGE4xLIAAA=
Content-Type: application/json

{
  "Name": "Social events"
}
```

**応答の例**

```
Status code: 200

{
  "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/Calendars/$entity",
  "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Calendars('AAMkAGE4xLIAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Sw==\"",
  "Id": "AAMkAGE4xLIAAA=",
  "Name": "Social events",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Sw=="
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
PATCH https://outlook.office.com/api/v2.0/me/calendars/{calendar_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|
|_本文パラメーター_|
|名前|string|カレンダーの新しい名前です。|


**要求のサンプル**

```
PATCH https://outlook.office.com/api/v2.0/me/calendars/AAMkAGE4xLIAAA=
Content-Type: application/json

{
  "Name": "Social events"
}
```

**応答の例**

```
Status code: 200

{
  "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/Calendars/$entity",
  "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/Calendars('AAMkAGE4xLIAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Sw==\"",
  "Id": "AAMkAGE4xLIAAA=",
  "Name": "Social events",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Sw=="
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
PATCH https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|
|_本文パラメーター_|
|名前|string|カレンダーの新しい名前です。|

```REST
{
    "method": "PATCH",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendars/{calender_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendars/AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLIAAA=",
    "requestHeaders": {
        "Accept": "application/json",
        "Content-Type": "application/json",
        "Content-Length": 29
    },
    "parameterDetails": [
        {
            "name": "calender_id",
            "type": "string",
            "description": "The calendar ID.",
            "defaultValue": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLIAAA="
        }
    ],
    "requestBody": {
        "Name": "Social events"
    },
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/Calendars/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/Calendars('AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLIAAA=')",
        "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Sw==\"",
        "Id": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLIAAA=",
        "Name": "Social events",
        "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Sw=="
    }
}
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->



**応答の種類**

更新の[予定表](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource)です。

****

<a name="UpdateCalendarsClient"> </a>
### <a name="update-a-calendar-client"></a>(クライアント) の予定表を更新します。

カレンダーの名前を変更します。**名**は、予定表にのみ書き込み可能なプロパティです。


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)し、[カレンダーの ID を取得](#GetCalendars)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Get an existing calendar by ID
ICalendar calendarToUpdate = await client.Me.Calendars[calendarId].ExecuteAsync();
calendarToUpdate.Name = "Family";

// Commit the change
await calendarToUpdate.UpdateAsync();

// Get the updated property
string newCalendarName = calendarToUpdate.Name;
```

<!-- ENDSECTION -->


複数の更新プログラムでクライアント側を定義し、要求を送信するすべてを一度に (それらのバッチ)、以下のパターンを使用しています。
1. 呼び出す`UpdateAsync(true)`の各エンティティを更新します。指定する`true`、クライアント上でローカルに更新プログラムを登録するが、サーバーにポストされません。
2. 呼び出す`client.Context.SaveChangesAsync()`ローカルに登録されているすべての更新プログラムを投稿します。

****

<a name="DeleteCalendars"> </a>
## <a name="delete-calendars"></a>予定表を削除します。

カレンダーを削除します。

REST API: は[(残りの部分) の予定表を削除します。](#DeleteACalendar)

クライアント ライブラリ: [(クライアント) の予定表を削除します。](#DeleteCalendarsClient)

<a name="DeleteACalendar"></a>
###<a name="delete-a-calendar-rest"></a>(REST) の予定表を削除します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]



```no-highlight
DELETE https://outlook.office.com/api/beta/me/calendars/{calendar_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|


**要求のサンプル**

```
DELETE https://outlook.office.com/api/beta/me/calendars/AAMkAGE4xLIAAA=
```

**応答の例**

```
Status code: 204
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]



```no-highlight
DELETE https://outlook.office.com/api/v2.0/me/calendars/{calendar_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|


**要求のサンプル**

```
DELETE https://outlook.office.com/api/v2.0/me/calendars/AAMkAGE4xLIAAA=
```

**応答の例**

```
Status code: 204
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


```no-highlight
DELETE https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_id|string|カレンダーの id。|

```REST
{
    "method": "DELETE",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendars/{calender_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendars/AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLIAAA=",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "calender_id",
            "type": "string",
            "description": "The calendar ID.",
            "defaultValue": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLIAAA="
        }
    ],
    "statusCode": 204

}
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->




****

<a name="DeleteCalendarsClient"> </a>
### <a name="delete-a-calendar-client"></a>(クライアント) の予定表を削除します。


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)し、[カレンダーの ID を取得](#GetCalendars)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Get an existing calendar by ID
ICalendar calendarToDelete = await client.Me.Calendars[calendarId].ExecuteAsync();
    
// Delete the calendar
await calendarToDelete.DeleteAsync(false);
```

<!-- ENDSECTION -->

****

<a name="GetCalendarGroups"> </a>
## <a name="get-calendar-groups"></a>予定表グループを取得します。

予定表グループのコレクションまたは[予定表グループを取得](#GetCalendarGroup)する取得できます。


**メモ**Outlook.com がアクセス可能な既定の予定表のグループのみがサポートされています、`../me/calendars`のショートカットです。


REST API: は[(残りの部分) の予定表グループのコレクションを取得する](#GetCalendarGroupCollection) | [(以降) の予定表グループを取得します。](#GetCalendarGroup)

クライアント ライブラリ:[予定表のグループ (クライアント) を取得します。](#GetCalendarGroupsClient)


****


<a name="GetCalendarGroupCollection"> </a>
###<a name="get-a-calendar-group-collection-rest"></a>(REST) の予定表グループのコレクションを取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

メールボックスの予定表グループを取得します。 


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/calendargroups
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

**要求のサンプル**

```
GET https://outlook.office.com/api/beta/me/calendargroups
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/CalendarGroups",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGI2TGuKAAA=')",
            "Id": "AAMkAGI2TGuKAAA=",
            "Name": "My Calendars",
            "ClassId": "0006f0b7-0000-0000-c000-000000000046",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+g=="
        },
        {
            "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGI2TGuMAAA=')",
            "Id": "AAMkAGI2TGuMAAA=",
            "Name": "Other Calendars",
            "ClassId": "0006f0b8-0000-0000-c000-000000000046",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0/A=="
        }
    ]
}
```

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v2.0/me/calendargroups
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。

**要求のサンプル**

```
GET https://outlook.office.com/api/v2.0/me/calendargroups
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/CalendarGroups",
    "value": [
        {
            "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGI2TGuKAAA=')",
            "Id": "AAMkAGI2TGuKAAA=",
            "Name": "My Calendars",
            "ClassId": "0006f0b7-0000-0000-c000-000000000046",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+g=="
        },
        {
            "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGI2TGuMAAA=')",
            "Id": "AAMkAGI2TGuMAAA=",
            "Name": "Other Calendars",
            "ClassId": "0006f0b8-0000-0000-c000-000000000046",
            "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0/A=="
        }
    ]
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/calendargroups
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


```REST-i
{
    "method": "GET",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendargroups",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendargroups",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/CalendarGroups",
        "value": [
            {
                "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/CalendarGroups('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=')",
                "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x0+g==\"",
                "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=",
                "Name": "My Calendars",
                "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+g==",
                "ClassId": "0006f0b7-0000-0000-c000-000000000046"
            },
            {
                "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/CalendarGroups('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuMAAA=')",
                "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x0/A==\"",
                "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuMAAA=",
                "Name": "Other Calendars",
                "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0/A==",
                "ClassId": "0006f0b8-0000-0000-c000-000000000046"
            }
        ]
    }
}
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


**応答の種類**

要求された[予定表グループ](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource)のコレクションです。

****


<a name="GetCalendarGroup"> </a>
###<a name="get-a-calendar-group-rest"></a>予定表グループ (残りの部分) を取得します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.read_
- _wl.calendars_
- _wl.contacts\_カレンダー_

ID での予定表グループを取得します。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|


**要求のサンプル**

```
GET https://outlook.office.com/api/beta/me/calendargroups/AAMkAGI2TGuKAAA=
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/CalendarGroups/$entity",
    "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGI2TGuKAAA=')",
    "Id": "AAMkAGI2TGuKAAA=",
    "Name": "My Calendars",
    "ClassId": "0006f0b7-0000-0000-c000-000000000046",
    "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+g=="
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v2.0/me/calendargroups/{calendar_group_id}
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|


**要求のサンプル**

```
GET https://outlook.office.com/api/v2.0/me/calendargroups/AAMkAGI2TGuKAAA=
```

**応答の例**

```
Status code: 200

{
    "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/CalendarGroups/$entity",
    "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGI2TGuKAAA=')",
    "Id": "AAMkAGI2TGuKAAA=",
    "Name": "My Calendars",
    "ClassId": "0006f0b7-0000-0000-c000-000000000046",
    "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+g=="
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/calendargroups/{calendar_group_id}
```

**メモ**フィルター処理、並べ替え、およびページングのパラメーターには、 [OData クエリのパラメーター](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams)を参照してください。


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|


```REST-i
{
    "method": "GET",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendargroups/{calendar_group_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendargroups/AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "calendar_group_id",
            "type": "string",
            "description": "The calendar group ID.",
            "defaultValue": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA="
        }
    ],
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/CalendarGroups/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/CalendarGroups('AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=')",
        "@odata.etag": "W/\"nfZyf7VcrEKLNoU37KWlkQAAA0x0+g==\"",
        "Id": "AAMkAGI2NGVhZTVlLTI1OGMtNDI4My1iZmE5LTA5OGJiZGEzMTc0YQBGAAAAAADUuTJK1K9aTpCdqXop_4NaBwCd9nJ-tVysQos2hTfspaWRAAAAAAEGAACd9nJ-tVysQos2hTfspaWRAAADTGuKAAA=",
        "Name": "My Calendars",
        "ChangeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+g==",
        "ClassId": "0006f0b7-0000-0000-c000-000000000046"
    }
}

```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


**応答の種類**

要求された[予定表のグループ](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource)です。

****

<a name="GetCalendarGroupsClient"> </a>
### <a name="get-calendar-groups-client"></a>予定表グループ (クライアント) を取得します。

ユーザーの予定表グループを取得します。別の予定表グループを取得するには、 **CalendarGroups**コレクションのインデックスとして予定表のグループ ID を指定または**GetById**メソッドを使用します。

例:`client.Me.CalendarGroups[calendarGroupId].ExecuteAsync()`


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


**メモ**予定表グループのコレクションでは、**選択**、**並べ替え**、および**実行**のようなクエリ式をサポートします。

この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
IPagedCollection<ICalendarGroup> calendarGroupsResults = await client.Me.CalendarGroups.ExecuteAsync();

// Get the ID of the first calendar group
string groupId = calendarGroupsResults.CurrentPage[0].Id;
```

<!-- ENDSECTION -->

****


<a name="CreateCalendarGroups"> </a>
## <a name="create-calendar-groups"></a>予定表グループを作成します。

予定表グループを作成します。**名**は、予定表グループにのみ書き込み可能なプロパティです。


**メモ**Outlook.com がアクセス可能な既定の予定表のグループのみがサポートされています、`../me/calendars`のショートカットです。Outlook.com には、別の予定表グループを作成できません。


REST API: [(残りの部分) の予定表グループの作成](#CreateACalendarGroup)

クライアント ライブラリ:[予定表グループ (クライアント) を作成します。](#CreateCalendarGroupsClient)

<a name="CreateACalendarGroup"></a>
###<a name="create-a-calendar-group-rest"></a>(REST) 予定表グループを作成します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_



<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/calendargroups
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|_本文パラメーター_|
|名前|string|予定表グループの名前。|


**要求のサンプル**

```
POST https://outlook.office.com/api/beta/me/calendargroups
Content-Type: application/json

{
  "Name": "Birthdays"
}
```

**応答の例**

```
Status code: 201

{
  "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/CalendarGroups/$entity",
  "@odata.id": "https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGE0M4xLGAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Rw==\"",
  "Id": "AAMkAGE0M4xLGAAA=",
  "Name": "Birthdays",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Rw==",
  "ClassId": "4d969bba-8942-42a0-ae33-c7d4410d1e11"
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
POST https://outlook.office.com/api/v2.0/me/calendargroups
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|_本文パラメーター_|
|名前|string|予定表グループの名前。|


**要求のサンプル**

```
POST https://outlook.office.com/api/v2.0/me/calendargroups
Content-Type: application/json

{
  "Name": "Birthdays"
}
```

**応答の例**

```
Status code: 201

{
  "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/CalendarGroups/$entity",
  "@odata.id": "https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGE0M4xLGAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Rw==\"",
  "Id": "AAMkAGE0M4xLGAAA=",
  "Name": "Birthdays",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Rw==",
  "ClassId": "4d969bba-8942-42a0-ae33-c7d4410d1e11"
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
POST https://outlook.office.com/api/v1.0/me/calendargroups
```

|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|_本文パラメーター_|
|名前|string|予定表グループの名前。|


```REST
{
    "method": "POST",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendargroups",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendargroups",
    "requestHeaders": {
        "Accept": "application/json",
        "Content-Type": "application/json",
        "Content-Length": 23
    },
    "parameterDetails": [],
    "requestBody": {
        "Name": "Birthdays"
    },
    "statusCode": 201,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/CalendarGroups/$entity",
        "@odata.id": "https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/CalendarGroups('AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLGAAA=')",
        "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Rw==\"",
        "Id": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLGAAA=",
        "Name": "Birthdays",
        "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/Rw==",
        "ClassId": "4d969bba-8942-42a0-ae33-c7d4410d1e11"
    }
}
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


**応答の種類**

新しい[予定表グループ](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource)です。


****

<a name="CreateCalendarGroupsClient"> </a>
### <a name="create-a-calendar-group-client"></a>予定表グループ (クライアント) を作成します。


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
CalendarGroup newCalendarGroup = new CalendarGroup
{
    Name = "Business"
};

// Add it to the CalendarGroups collection
await client.Me.CalendarGroups.AddCalendarGroupAsync(newCalendarGroup);

// Get the ID of the calendar group
string calendarGroupId = newCalendarGroup.Id;
```

<!-- ENDSECTION -->


****


<a name="UpdateCalendarGroups"> </a>
## <a name="update-calendar-groups"></a>グループの予定表を更新します。

REST API:[更新予定表グループ (他)](#UpdateACalendarGroup)

クライアント ライブラリ:[予定表グループ (クライアント) の更新](#UpdateCalendarGroupsClient)

<a name="UpdateACalendarGroup"></a>
### <a name="update-a-calendar-group-rest"></a>予定表グループ (残りの部分) を更新します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_

予定表グループの名前を変更します。**名前**は、のみ書き込み可能な[グループの予定表](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource)のプロパティです。


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
PATCH https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|
|_本文パラメーター_|
|名前|string|更新された予定表グループの名前です。|


**要求のサンプル**

```
PATCH https://outlook.office.com/api/beta/me/calendargroups/AAMkAGE0M4xLGAAA=
Content-Type: application/json

{
  "Name": "Holidays"
}
```

**応答の例**

```
{
  "@odata.context": "https://outlook.office.com/api/beta/$metadata#Me/CalendarGroups/$entity",
  "@odata.id": "https://https://outlook.office.com/api/beta/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGE0MGM4xLGAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SA==\"",
  "Id": "AAMkAGE0MGM4xLGAAA=",
  "Name": "Holidays",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SA==",
  "ClassId": "4d969bba-8942-42a0-ae33-c7d4410d1e11"
}
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
PATCH https://outlook.office.com/api/v2.0/me/calendargroups/{calendar_group_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|
|_本文パラメーター_|
|名前|string|更新された予定表グループの名前です。|


**要求のサンプル**

```
PATCH https://outlook.office.com/api/v2.0/me/calendargroups/AAMkAGE0M4xLGAAA=
Content-Type: application/json

{
  "Name": "Holidays"
}
```

**応答の例**

```
{
  "@odata.context": "https://outlook.office.com/api/v2.0/$metadata#Me/CalendarGroups/$entity",
  "@odata.id": "https://https://outlook.office.com/api/v2.0/Users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/CalendarGroups('AAMkAGE0MGM4xLGAAA=')",
  "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SA==\"",
  "Id": "AAMkAGE0MGM4xLGAAA=",
  "Name": "Holidays",
  "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SA==",
  "ClassId": "4d969bba-8942-42a0-ae33-c7d4410d1e11"
}
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
PATCH https://outlook.office.com/api/v1.0/me/calendargroups/{calendar_group_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|
|_本文パラメーター_|
|名前|string|更新された予定表グループの名前です。|


```REST
 {
    "method": "PATCH",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendargroups/{calendar_group_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendargroups/AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLGAAA=",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "calendar_group_id",
            "type": "string",
            "description": "The calendar group ID.",
            "defaultValue": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLGAAA="
        }
    ],
    "requestBody": {
        "Name": "Holidays"
    },
    "statusCode": 200,
    "responseBody": {
        "@odata.context": "https://outlook.office.com/api/v1.0/$metadata#Me/CalendarGroups/$entity",
        "@odata.id": "https://https://outlook.office.com/api/v1.0/Users('alexd@a830edad9050849NDA1.onmicrosoft.com')/CalendarGroups('AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLGAAA=')",
        "@odata.etag": "W/\"Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SA==\"",
        "Id": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLGAAA=",
        "Name": "Holidays",
        "ChangeKey": "Jj9S59cHB0Wq4jXUzBgDvQAAFeN/SA==",
        "ClassId": "4d969bba-8942-42a0-ae33-c7d4410d1e11"
    }
}
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->

**応答の種類**

更新された[予定表のグループ](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource)です。

****

<a name="UpdateCalendarGroupsClient"> </a>
### <a name="update-a-calendar-group-client"></a>予定表グループ (クライアント) の更新します。

予定表グループの名前を変更します。**名**は、予定表グループにのみ書き込み可能なプロパティです。


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)し、[予定表のグループ ID を取得](#GetCalendarGroups)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Get an existing calendar group by ID
ICalendarGroup groupToUpdate = await client.Me.CalendarGroups[groupId].ExecuteAsync();
groupToUpdate.Name = "Contoso";

// Commit the change
await groupToUpdate.UpdateAsync();

// Get the updated property
string newCalendarGroupName = groupToUpdate.Name;
```

<!-- ENDSECTION -->


複数の更新プログラムでクライアント側を定義し、要求を送信するすべてを一度に (それらのバッチ)、以下のパターンを使用しています。
1. 呼び出す`UpdateAsync(true)`の各エンティティを更新します。指定する`true`、クライアント上でローカルに更新プログラムを登録するが、サーバーにポストされません。
2. 呼び出す`client.Context.SaveChangesAsync()`ローカルに登録されているすべての更新プログラムを投稿します。


****


<a name="DeleteCalendarGroups"> </a>
## <a name="delete-calendar-groups"></a>予定表グループを削除します。

予定表グループを削除します。


**メモ**Outlook.com がアクセス可能な既定の予定表のグループのみがサポートされています、`../me/calendars`のショートカットです。この予定表グループを削除しないでください。


REST API: の[予定表グループ (残りの部分) を削除します。](#DeleteACalendarGroup)

クライアント ライブラリ: [(クライアント) の予定表グループを削除します。](#DeleteCalendarGroupsClient)

<a name="DeleteACalendarGroup"></a>
###<a name="delete-a-calendar-group-rest"></a>(REST) 予定表グループを削除します。

_**必要な範囲の最小値**: 次のいずれか。_
- _https://outlook.office.com/calendars.readwrite_
- _wl.calendars\_を更新_
- _wl.events\_の作成_


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
DELETE https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|


**要求のサンプル**

```
DELETE https://outlook.office.com/api/beta/me/calendargroups/AAMkAGE0MGM4xLGAAA=
```

**応答の例**

```
Status code: 204
```


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End BETA content ====================================================== -->

<!-- ============================================================================================================ -->


<!-- ============================================================================================================ -->

<!-- ==================================== Start v2 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
DELETE https://outlook.office.com/api/v2.0/me/calendargroups/{calendar_group_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|

**要求のサンプル**

```
DELETE https://outlook.office.com/api/v2.0/me/calendargroups/AAMkAGE0MGM4xLGAAA=
```

**応答の例**

```
Status code: 204
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
DELETE https://outlook.office.com/api/v1.0/me/calendargroups/{calendar_group_id}
```


|**必要なパラメーター**|**タイプ**|**説明**|
|:-----|:-----|:-----|
|_URL パラメーター_|
|calendar_group_id|string|予定表グループの id。|


```REST
{
    "method": "DELETE",
    "resourceFormat": "https://outlook.office.com/api/v1.0/me/calendargroups/{calendar_group_id}",
    "requestUrl": "https://outlook.office.com/api/v1.0/me/calendargroups/AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLGAAA=",
    "requestHeaders": {
        "Accept": "application/json"
    },
    "parameterDetails": [
        {
            "name": "calendar_group_id",
            "type": "string",
            "description": "The calendar group ID.",
            "defaultValue": "AAMkAGE0MGM1Y2M5LWEzMmUtNGVlNy05MjRlLTk0YmJjYzVkN2I5MABGAAAAAAC_0WfqSjt_SqLtNkuO-bj1BwAmP1Ln1wcHRariNdTMGAO9AAAAAAEGAAAmP1Ln1wcHRariNdTMGAO9AAAV4xLGAAA="
        }
    ],
    "statusCode": 204

}
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


****

<a name="DeleteCalendarGroupsClient"> </a>
### <a name="delete-a-calendar-group-client"></a>(クライアント) の予定表グループを削除します。


**注意**Outlook.com 上のメールボックス データにアクセスする場合はクライアント ライブラリを使用されず、REST API を直接呼び出します。


この例では、既に[Outlook サービス クライアントを取得](..\api\use-outlook-rest-api.md#GetClient)し、[予定表のグループ ID を取得](#GetCalendarGroups)します。

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
// Get an existing calendar group by ID
ICalendarGroup groupToDelete = await client.Me.CalendarGroups[groupId].ExecuteAsync();

// Delete the group
await groupToDelete.DeleteAsync(); 
```

<!-- ENDSECTION -->

****

<a name="NextSteps"> </a>
## <a name="next-steps"></a>次のステップ

アプリケーションの構築を開始、あるいは詳細については、準備が整ったら、かどうかお任せします。


- [メール、カレンダー、および連絡先の他の Api を使用](http://dev.outlook.com/RestGettingStarted)します。
  
- 対話型の[API のサンド ボックス](http://apisandbox.msdn.microsoft.com/)を使用して Office の残り Api について説明します。
    
- サンプルをしますか。[きました](..\howto\starter-projects-and-code-samples.md)。
    

または、Office 365 のプラットフォームを使用する方法の詳細について説明します。

- [REST API を outlook で Outlook のデベロッパー センター](http://dev.outlook.com/RestGettingStarted/Overview)

- [Office 365 のプラットフォーム上での開発の概要](..\howto\platform-development-overview.md)
    
- [Office 365 アプリケーションの認証およびリソースの承認](..\howto\common-app-authentication-tasks.md)
    
- [Azure AD で Office 365 の Api にアクセスできるように、アプリケーションを手動で登録します。](..\howto\add-common-consent-manually.md)
  
- [メール API リファレンス](..\api\mail-rest-operations.md)
  
- [連絡先 API リファレンス](..\api\contacts-rest-operations.md)

- [タスクの残りの部分の API (プレビュー)](..\api\task-rest-operations.md)

- [OneDrive API](https://dev.onedrive.com/)

- [探索サービスの REST API の操作を参照します。](..\api\discovery-service-rest-operations.md)

- [メール、予定表、連絡先、およびタスクの残りの部分の Api のリソースの参照](..\api\complex-types-for-mail-contacts-calendar.md)



[!INCLUDE [Enable filtering functionality ](../includes/controls/enablefilteringhtml)]

