<<<<<<< ヘッド ms です。TocTitle: Office 365 の API リファレンス タイトル: Office 365 の API リファレンスの説明: Office 365 の API を検索する参照し、メール、連絡先、および予定表データ、ファイルを操作する Api と、探索サービスの残りの部分とクライアント ライブラリについての情報です。ms です。ContentId: 6736150c-641e-4e1b-bcc0-6cce0996779d ms.topic: ms.date を参照 (API): 2016 年 4 月 21 日=======
---
ms です。Toctitle: Office 365 の API リファレンス タイトル: Office 365 の API リファレンスの説明: Office 365 の API を検索する参照し、残りの部分とクライアント ライブラリの Api についての情報です。ms です。ContentId: 6736150c-641e-4e1b-bcc0-6cce0996779d ms.date: 2016 年 9 月 20 日
>>>>>>> ステージング

[!INCLUDE [Add the O365API repo styles](../includes/controls/addo365apistyles.html)]

# <a name="office-365-api-reference"></a>Office 365 の API リファレンス 
    
 _**に適用されます:**オンライン交換 |Office 365 |ビジネスの OneDrive_

<<<<<<< ヘッド
<a name="p-classpreviewnotethis-documentation-covers-features-that-are-currently-in-preview-for-information-about-working-with-preview-features-see-preview-developer-features-on-the-office-365-platformhowtoplatform-development-preview-features-overviewmdp"></a><p class="previewnote">このドキュメントでは、現在プレビューされている機能について説明します。プレビュー機能の操作方法の詳細については、 [Office 365 のプラットフォームで開発機能のプレビュー](..\howto\platform-development-preview-features-overview.md)を参照してください。</p>
=======
[!INCLUDE [Use Microsoft Graph](../includes/use-msgraph-note.md)]

Office 365 の Api を使用すると、関心がほとんど--、メール、予定表、連絡先、ユーザーとグループ、ファイル、およびフォルダー - すべての右から、アプリケーション自体の内でする、といった、お客様の Office 365 のデータへのアクセスを提供します。 
            
間でのすべてのモバイル ソリューション、web、およびデスクトップ ・ プラットフォームから Office 365 の Api にアクセスできます。ツール、開発プラットフォームに関係なく。レールに沿って、.NET、PHP、Java、Python や Ruby を使用して Windows 汎用アプリ、iOS のアプリを作成する web アプリケーションを構築するかどうか、Android の場合、または別のデバイス プラットフォームでは、選択します。
    
### <a name="office-365-sdks-make-app-development-easier"></a>Office 365 Sdk 簡単にアプリケーションの開発

Office 365 との対話、書き込み、および認証トークン、アクセスする API の適切な Url とクエリを作成するその他のタスクを管理するコードを管理する他の Api を直接プログラミングすることができます。Visual Studio や Eclipse および Android Studio は、統合、Office 365 の Sdk では、Office 365 の Api にアクセスするのには記述する必要のあるコードの複雑さを軽減を支援します。

[Visual Studio の Office 開発ツール](http://aka.ms/OfficeDevToolsForVS2013)にはには、.NET が提供する Sdk および Office 365 の他のサービスをラップし、Office 365 のデータへの接続も簡単な方法を提供する JavaScript ライブラリが含まれます。Sdk は、Visual Studio で ASP.NET MVC、ASP.NET Web フォーム、WPF、フォームの獲得、汎用アプリケーション、Cordova と Xamarin のプロジェクトの種類に対して使用できます。 

Android 開発者は、Eclipse および Android Studio Android SDK 現在一般的に利用可能なも同様です。 参照してください、 [Office 365 の Android SDK](https://github.com/OfficeDev/Office-365-SDK-for-Android)。 
>>>>>>> ステージング

IOS アプリ、iOS (プレビュー) を統合の SDK では、[統合 6](https://developer.apple.com/xcode/)内で目的の C と Swift の両方の言語をサポートしています。[IOS の Office 365 の SDK](https://github.com/OfficeDev/Office-365-SDK-for-iOS)を参照してください。 


<!--
<a href="#bk_groups"><img alt="Groups API (preview) icon" src="office/office365/api/images/O365APIs_REST_Reference_icons_groups.png" /></a>
-->

<!--
<a href="#bk_mail" id="Mail">
    <img title="Mail API" src="http://i.imgur.com/qhjA7Qy.png" onmouseover="this.src='http://i.imgur.com/s5rJ51y.png'" onmouseout="this.src='http://i.imgur.com/qhjA7Qy.png'" />
</a>
<a href="#bk_contacts" id="Contacts">
    <img title="Contacts API" src="http://i.imgur.com/xJbLQcp.png" onmouseover="this.src='http://i.imgur.com/idZpJmq.png'" onmouseout="this.src='http://i.imgur.com/xJbLQcp.png'" />
</a>
<a href="#bk_calendar" id="Calendar">
    <img title="Calendar API" src="http://i.imgur.com/dKrWDZ2.png" onmouseover="this.src='http://i.imgur.com/9D0eQGe.png'" onmouseout="this.src='http://i.imgur.com/dKrWDZ2.png'" />
</a>
-->


## <a name="batching-outlook-rest-requests-preview"></a>Outlook の他の要求 (プレビュー) をバッチ処理

[バッチで Outlook の他の要求を送信します。](..\api\batch-outlook-rest-requests.md)


## <a name="outlook-task"></a>Outlook のタスク
[タスク API](..\api\task-rest-operations.md)

**タスクの操作**&nbsp; 
[を作成するタスク](..\api\task-rest-operations.md#CreateTasks) | [のタスクを取得する](..\api\task-rest-operations.md#GetTasks) | [タスクを更新する](..\api\task-rest-operations.md#UpdateTasks) | [のタスクを削除](..\api\task-rest-operations.md#DeleteTasks) | 
[タスクを完了](..\api\task-rest-operations.md#CompleteTasks) | [同期タスクまたはタスク フォルダー](..\api\task-rest-operations.md#SyncTasks) 


**タスク フォルダーの操作**&nbsp; 
[タスク フォルダーを作成する](..\api\task-rest-operations.md#CreateTaskFolders) | [タスク フォルダーを取得する](..\api\task-rest-operations.md#GetTaskFolders) | [タスク フォルダーを更新](..\api\task-rest-operations.md#UpdateTaskFolders) | 
[タスク フォルダーを削除する](..\api\task-rest-operations.md#DeleteTaskFolders) | [同期タスクまたはタスク フォルダー](..\api\task-rest-operations.md#SyncTasks) 


**タスク グループの操作**&nbsp; 
[を作成するタスクのグループ](..\api\task-rest-operations.md#CreateTaskGroups) | [タスク グループを取得する](..\api\task-rest-operations.md#GetTaskGroups) | [タスク グループを更新](..\api\task-rest-operations.md#UpdateTaskGroups) | 
[タスク グループを削除](..\api\task-rest-operations.md#DeleteTaskGroups)


<a name="bk_people"> </a>

##<a name="outlook-people-preview"></a>Outlook ユーザー (プレビュー)

[API の人](..\api\people-rest-operations.md)

**参照:**&nbsp;  
[閲覧](..\api\people-rest-operations.md#BrowsePeople) | [ページング](..\api\people-rest-operations.md#BrowsePaging) | 
[並べ替え](..\api\people-rest-operations.md#BrowseSort) | [制限する](..\api\people-rest-operations.md#BrowsePageSize) |
[選択](..\api\people-rest-operations.md#BrowseSelecting) | [フィルター](..\api\people-rest-operations.md#BrowseFiltering) |
[フィルタ リングと選択](..\api\people-rest-operations.md#BrowseSelectingAndFiltering)

**検索:**&nbsp; 
[トピックを選択して](..\api\people-rest-operations.md#SearchTopic) |
[、検索のフィルター](..\api\people-rest-operations.md#SearchFilter) |
[あいまい検索](..\api\people-rest-operations.md#FuzzySearch)



## <a name="office-365-data-extensions"></a>Office 365 のデータ拡張機能

[データ拡張機能 API](..\api\extensions-rest-operations.md)

**の種類の拡張子を開く:**&nbsp; [で既存の項目を作成する](..\api\extensions-rest-operations.md#CreateExtensionInExistingItem) | [に新しい項目を作成する](..\api\extensions-rest-operations.md#CreateExtensionInNewItem) |
[を取得](..\api\extensions-rest-operations.md#GetExtension) | [項目は展開](..\api\extensions-rest-operations.md#GetExpandedExtension) |
[更新](..\api\extensions-rest-operations.md#UpdateExtension) | [削除](..\api\extensions-rest-operations.md#DeleteExtension)


## <a name="outlook-extended-properties"></a>Outlook の拡張プロパティ

[拡張 API のプロパティ](..\api\extended-properties-rest-operations.md)

**拡張プロパティ**  &nbsp;  [で既存の項目を作成する](..\api\extended-properties-rest-operations.md#CreateExtendedPropertyInExistingItem) | 
[に新しい項目を作成する](..\api\extended-properties-rest-operations.md#CreateExtendedPropertyInNewItem) | 
[項目は展開](..\api\extended-properties-rest-operations.md#GetExpandedExtendedProperty) | 
[フィルター](..\api\extended-properties-rest-operations.md#GetItemByFilteringExtendedProperty)



<a name="bk_mail"> </a>

##<a name="outlook-mail"></a>Outlook メール

[メール API](..\api\mail-rest-operations.md) 

**メッセージ:**&nbsp; [を取得](..\api\mail-rest-operations.md#Getmessages) | [の作成と送信](..\api\mail-rest-operations.md#Sendmessages) |
 [への返信](..\api\mail-rest-operations.md#Replytomessages) | [転送](..\api\mail-rest-operations.md#Forwardmessages) |
 [更新](..\api\mail-rest-operations.md#Updatemessages) | [削除](..\api\mail-rest-operations.md#DeleteMessages) |
 [を移動またはコピー](..\api\mail-rest-operations.md#MoveCopymessages)

**添付ファイル:**&nbsp;  [を取得](..\api\mail-rest-operations.md#GetAttachments) |
 [作成](..\api\mail-rest-operations.md#CreateAttachments) | [削除](..\api\mail-rest-operations.md#DeleteAttachments)

**フォルダー:**&nbsp;  [を取得](..\api\mail-rest-operations.md#GetFolders) | [を作成する](..\api\mail-rest-operations.md#CreateFolders) | [更新](..\api\mail-rest-operations.md#UpdateFolders) |
 [削除](..\api\mail-rest-operations.md#DeleteFolders) | [を移動またはコピー](..\api\mail-rest-operations.md#MoveCopyFolders)


<a name="bk_contacts"> </a>

##<a name="outlook-contacts"></a>Outlook の連絡先

[連絡先 API](..\api\contacts-rest-operations.md)

**連絡先:**&nbsp;  [を取得](..\api\contacts-rest-operations.md#GetContacts) | [作成](..\api\contacts-rest-operations.md#CreateContacts) |
 [更新](..\api\contacts-rest-operations.md#UpdateContacts) | [削除](..\api\contacts-rest-operations.md#DeleteContacts) 
 

**フォルダーの連絡先:**&nbsp;  [を取得](..\api\contacts-rest-operations.md#GetContactFolders)


<a name="bk_calendar"> </a>

##<a name="outlook-calendar"></a>Outlook の予定表

[カレンダー API](..\api\calendar-rest-operations.md)

**カレンダー ビュー:**  &nbsp;  [を取得](..\api\calendar-rest-operations.md#GetCalendarView) | [同期](..\api\calendar-rest-operations.md#SyncCalendarView)

**イベント:**&nbsp;[を取得](..\api\calendar-rest-operations.md#GetEvents) | [同期](..\api\calendar-rest-operations.md#SyncCalendarView) |
 [作成](..\api\calendar-rest-operations.md#CreateEvents) |
 [更新](..\api\calendar-rest-operations.md#UpdateEvents) | [対応](..\api\calendar-rest-operations.md#RespondToEvents) | 
 [削除](..\api\calendar-rest-operations.md#DeleteEvents)  

**の添付ファイル:**&nbsp; 
 [Get](..\api\calendar-rest-operations.md#GetAttachments) | [Create](..\api\calendar-rest-operations.md#reateAttachments) |
 [Delete](..\api\calendar-rest-operations.md#DeleteAttachments)
 
 **アラーム:**&nbsp; 
 [を取得](..\api\calendar-rest-operations.md#GetReminders) | 
 [再通知](..\api\calendar-rest-operations.md#SnoozeReminders) | 
 [を閉じる](..\api\calendar-rest-operations.md#DismissReminders)

**カレンダー:**&nbsp;[を取得](..\api\calendar-rest-operations.md#GetCalendars) |
 [作成](..\api\calendar-rest-operations.md#CreateCalendars) | [更新](..\api\calendar-rest-operations.md#UpdateCalendars) |
 [削除](..\api\calendar-rest-operations.md#DeleteCalendars)  

**グループの予定表:**&nbsp;   [を取得](..\api\calendar-rest-operations.md#GetCalendarGroups) |
 [を作成する](..\api\calendar-rest-operations.md#CreateCalendarGroups) | [更新](..\api\calendar-rest-operations.md#UpdateCalendarGroups) |
 [削除](..\api\calendar-rest-operations.md#DeleteCalendarGroups)



##<a name="resource-reference-for-the-mail-calendar-contacts-and-task-apis"></a>メール、予定表、連絡先、およびタスクの Api のリソースの参照

[リソースの参照](..\API\complex-types-for-mail-contacts-calendar.md) 
 
 **エンティティ:**&nbsp;[カレンダー](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource) |
 [CalendarGroup](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource) | [連絡先](..\api\complex-types-for-mail-contacts-calendar.md#ContactResource) |
 [ContactFolder](..\api\complex-types-for-mail-contacts-calendar.md#ContactFolderResource) | [イベント](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) |
 [EventMessage](..\api\complex-types-for-mail-contacts-calendar.md#EventMessageResource) | [拡張プロパティ](..\api\complex-types-for-mail-contacts-calendar.md#ExtendedProperties) | 
 [FileAttachment](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource) | [フォルダー](..\api\complex-types-for-mail-contacts-calendar.md#FolderResource) |
 [ItemAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource) | [メッセージ](..\api\complex-types-for-mail-contacts-calendar.md#MessageResource) |
 [タスク (プレビュー)](..\api\complex-types-for-mail-contacts-calendar.md#TaskResource) | [TaskFolder (プレビュー)](..\api\complex-types-for-mail-contacts-calendar.md#TaskFolderResource) | 
 [(プレビュー) をタスク グループ](..\api\complex-types-for-mail-contacts-calendar.md#TaskGroupResource) | 
 [ユーザー](..\api\complex-types-for-mail-contacts-calendar.md#UserResource)   
 
 **複合型:**&nbsp;[参加者](..\api\complex-types-for-mail-contacts-calendar.md#Attendee) | 
 [AttendeeBase](..\api\complex-types-for-mail-contacts-calendar.md#AttendeeBase) (プレビュー)。 [AttendeeAvailability](..\api\complex-types-for-mail-contacts-calendar.md#AttendeeAvailability)(プレビュー)。 [DateTimeTimeZone](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZoneBeta) | 
  [EmailAddress](..\api\complex-types-for-mail-contacts-calendar.md#EmailAddress) | 
 [GeoCoordinates](..\api\complex-types-for-mail-contacts-calendar.md#GeoCoordinates) | 
 [ItemBody](..\api\complex-types-for-mail-contacts-calendar.md#ItemBody)  | 
 [場所](..\api\complex-types-for-mail-contacts-calendar.md#Location)(プレビュー)。 [LocationConstraint](..\api\complex-types-for-mail-contacts-calendar.md#LocationConstraint)(プレビュー)。 [MeetingTimeCandidate](..\api\complex-types-for-mail-contacts-calendar.md#MeetingTimeCandidate)(プレビュー)。 [PatternedRecurrence](..\api\complex-types-for-mail-contacts-calendar.md#PatternedRecurrence) | 
  [PhysicalAddress](..\api\complex-types-for-mail-contacts-calendar.md#PhysicalAddress) | 
 [受信者](..\api\complex-types-for-mail-contacts-calendar.md#Recipient) | 
 [RecurrencePattern](..\api\complex-types-for-mail-contacts-calendar.md#RecurrencePattern) | 
 [RecurrenceRange](..\api\complex-types-for-mail-contacts-calendar.md#RecurrenceRange) | 
 [ResponseStatus](..\api\complex-types-for-mail-contacts-calendar.md#ResponseStatus) | 
 [TimeConstraint](..\api\complex-types-for-mail-contacts-calendar.md#TimeConstraint) (プレビュー)。 [タイム スロット](..\api\complex-types-for-mail-contacts-calendar.md#TimeSlot)(プレビュー)。 [タイムスタンプ](..\api\complex-types-for-mail-contacts-calendar.md#TimeStamp)(プレビュー)    
 
 
 **OData クエリ パラメーター:**&nbsp; [$search](..\api\complex-types-for-mail-contacts-calendar.md#Search) | 
 [$filter](..\api\complex-types-for-mail-contacts-calendar.md#Filter) | [$select](..\api\complex-types-for-mail-contacts-calendar.md#Select) | 
 [$orderby](..\api\complex-types-for-mail-contacts-calendar.md#OrderBy) | [$top と $skip](..\api\complex-types-for-mail-contacts-calendar.md#TopSkip)  | 
 $ を展開します。[$count](..\api\complex-types-for-mail-contacts-calendar.md#Count)   

<a name="bk_notify"> </a>

##<a name="outlook-notifications"></a>Outlook の通知

[プッシュ通知 API](../api/notify-rest-operations.md)

[通知 API のストリーミング](../api/notify-streaming-rest-operations.md)(プレビュー)


<a name="bk_photo"> </a>

##<a name="outlook-user-photo"></a>Outlook ユーザーの写真

[API のユーザーの写真](../api/photo-rest-operations.md)
 

<a name="bk_discovery"> </a>

##<a name="discovery-service"></a>探索サービス

[探索サービスの API](..\api\discovery-service-rest-operations.md)

[最初のサインイン](..\api\discovery-service-rest-operations.md#DiscoveryServiceoperationsInitialsignin) |
 [特定のサービスを検出](..\api\discovery-service-rest-operations.md#DiscoveryServiceoperationsDiscoverspecificservices) | [についてはどのようなサービスが検出可能](..\api\discovery-service-rest-operations.md#DiscoveryServiceoperationsLearnwhatservicesarediscoverable)


<a name="bk_files"> </a>

##<a name="files"></a>ファイル

[OneDrive API](https://dev.onedrive.com/)


<a name="bk_video"> </a>

##<a name="video"></a>ビデオ 

[ビデオの API](../api/video-rest-operations.md)

**ビデオ ポータル:**&nbsp;  
  [の情報を取得します。](..\api\video-rest-operations.md#GetPortalInformation)
  
**チャネル:**&nbsp;  
  [の情報を取得します。](..\api\video-rest-operations.md#GetChannelsInfo) 
  
**ビデオ情報:**&nbsp;  
  [を取得](..\api\video-rest-operations.md#GetVideoInfo) | [ビデオのメタデータを更新します。](..\api\video-rest-operations.md#UpdateVideo) 
  
**ビデオ:**&nbsp;  
  [アップロード](..\api\video-rest-operations.md#UploadVideos) | [削除](..\api\video-rest-operations.md#DeleteVideos) 

##<a name="api-resource-and-service-endpoints-of-office-365-operated-by-21vianet"></a>21Vianet によって運営されて Office 365 のリソースとサービス エンドポイントを API
[21Vianet によって運営されて Office 365 の API エンドポイント](..\api\o365-china-endpoints.md)

##<a name="office-365-management-apis"></a>Office 365 管理 Api
[はじめに](https://msdn.microsoft.com/library/office/dn707383.aspx) | [サービス通信 API (プレビュー)](https://msdn.microsoft.com/EN-US/library/dn707386.aspx) | [管理アクティビティ API リファレンス (プレビュー)](https://msdn.microsoft.com/library/office/mt227394.aspx) | [レポート web サービス](https://msdn.microsoft.com/en-us/library/office/jj984325.aspx) 

##<a name="additional-resources"></a>その他のリソース

###<a name="api-sandbox"></a>API のサンド ボックス
[この対話型コンソールを使用して Office 365 の Api を表示します。](http://apisandbox.msdn.microsoft.com/)

###<a name="rest-api-response-status-codes"></a>REST API 応答ステータス コード

[HTTP 応答ステータス コード](..\howto\http-response-status-codes.md)


<<<<<<< ヘッド
<!--
**Get started:** &nbsp; <a href="setup-development-environment?aspnet"> ASP.NET MVC apps </a> | <a href="setup-development-environment?javascript"> JavaScript web apps </a> | <a href="setup-development-environment?iOS"> iOS </a> | <a href="setup-development-environment?android"> Android </a>
-->


<a name="get-started-nbsp-aspnet-mvc-appshowtogetting-started-office-365-apismdaspnet-javascript-web-appshowtogetting-started-office-365-apismdjavascript-ioshowtogetting-started-office-365-apismdios-androidhowtogetting-started-office-365-apismdandroid"></a>**開始:**&nbsp; [ASP.NET MVC アプリケーション](..\howto\getting-started-Office-365-APIs.md?aspnet) | [web アプリケーションを JavaScript](..\howto\getting-started-Office-365-APIs.md?javascript) | [iOS](..\howto\getting-started-Office-365-APIs.md?iOS) | [Android](..\howto\getting-started-Office-365-APIs.md?android)  
=======
###<a name="office-365-platform-overview"></a>Office 365 のプラットフォームの概要
>>>>>>> ステージング

[Office 365 のプラットフォーム上での開発の概要](..\howto\platform-development-overview.md) | [、Office 365 の開発環境をセットアップします。](..\howTo\setup-development-environment.md) 

[Office 365APIs の概要](..\howto\getting-started-Office-365-APIs.md) 

###<a name="office-365-permission-scopes"></a>Office 365 のためのアクセス許可のスコープ
[すべての Office 365 のアクセス許可のスコープの詳細については](..\howto\application-manifest.md)

###<a name="microsoft-partner-center-api-reference"></a>マイクロソフト ・ パートナー ・ センターの API リファレンス
パートナーは、 [CSP Commerce REST API](https://msdn.microsoft.com/en-us/library/partnercenter/dn974944.aspx)を使用して、顧客アカウントを作成、Microsoft Commerce プラットフォームで顧客プロファイルの管理を購入し、受注および顧客のマイクロソフト製品のサブスクリプションを管理します。 



