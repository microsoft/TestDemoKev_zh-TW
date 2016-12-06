<<<<<<< Ms de TÊTE. TocTitle : Référence des API Office 365 titre : référence d’API de Office 365 Description : références de trouver les API d’Office 365 et d’informations sur la bibliothèque de client et d’AUTRES API, pour interagir avec les fichiers de messages, les contacts et les données du calendrier et le Service de découverte. MS. ContentId : 6736150c-641e-4e1b-bcc0-6cce0996779d ms.topic : ms.date de référence (API) : le 21 avril 2016=======
---
MS. Toctitle : Titre de référence API Office 365 : description de la référence Office 365 API : références de trouver les API d’Office 365 et d’informations sur la bibliothèque de client et d’AUTRES API. MS. ContentId : 6736150c-641e-4e1b-bcc0-6cce0996779d ms.date : le 20 septembre 2016
>>>>>>> la zone de transit

[!INCLUDE [Add the O365API repo styles](../includes/controls/addo365apistyles.html)]

# <a name="office-365-api-reference"></a>Référence des API Office 365 
    
 _**S’applique à :** Exchange Online | Office 365 | OneDrive pour les entreprises_

<<<<<<< TÊTE
<a name="p-classpreviewnotethis-documentation-covers-features-that-are-currently-in-preview-for-information-about-working-with-preview-features-see-preview-developer-features-on-the-office-365-platformhowtoplatform-development-preview-features-overviewmdp"></a><p class="previewnote">Cette documentation traite des fonctionnalités qui sont actuellement dans l’aperçu. Pour plus d’informations sur l’utilisation des fonctions de visualisation, voir [fonctionnalités de développement d’aperçu sur la plate-forme Office 365](..\howto\platform-development-preview-features-overview.md).</p>
=======
[!INCLUDE [Use Microsoft Graph](../includes/use-msgraph-note.md)]

Les API d’Office 365 vous permettent de vous permet de fournir l’accès aux données de Office 365 de votre client, y compris les choses qu’elles intéressent le plus : leur courrier, calendriers, contacts, utilisateurs et groupes, fichiers et dossiers--tous les directement à partir de votre application lui-même. 
            
Vous pouvez accéder à l’API d’Office 365 à partir des plates-formes de bureau, web et mobile de toutes les solutions. Quelle que soit la plate-forme de développement des outils. Donc si vous créez des applications web à l’aide de .NET, PHP, Java, Python ou Ruby sur Rails ou la création d’applications pour Windows, applications universel, iOS, Android, ou sur une autre plate-forme de périphérique, il s’agit de votre choix.
    
### <a name="office-365-sdks-make-app-development-easier"></a>Kits de développement logiciel Office 365 facilitent le développement de l’application

Vous pouvez programmer directement sur les API RESTE à interagir avec Office 365, écrire et mettre à jour le code autour de la gestion des jetons d’authentification, construire les URL correctes et les requêtes de l’API que vous souhaitez accéder, et autres tâches. Les kits de développement logiciel Office 365 pour Visual Studio, Eclipse et Android Studio ou Xcode, réduire la complexité du code, que vous devez écrire pour accéder à l’API d’Office 365.

Les [Outils de développement Office de Visual Studio](http://aka.ms/OfficeDevToolsForVS2013) comprennent les kits de développement logiciel qui fournissent de .NET et des bibliothèques JavaScript qui encapsuler les services Office 365 RESTE et offrent un moyen encore plus simple pour vous connecter à vos données d’Office 365. Les kits de développement sont disponibles pour les types de projet ASP.NET MVC, ASP.NET Web Forms, WPF, formulaires Win Forms, une application universelle, Cordova et Xamarin dans Visual Studio. 

Pour les développeurs de Android, le SDK Android pour Eclipse et Android Studio sont désormais disponible également.  Consultez le [Office 365 SDK pour Android](https://github.com/OfficeDev/Office-365-SDK-for-Android). 
>>>>>>> la zone de transit

Pour les applications d’e/s, iOS SDK pour Xcode (aperçu) prend en charge les langues à la fois Objective C et Swift dans [Xcode 6](https://developer.apple.com/xcode/). Consultez le [Kit de développement de Logiciel de Office 365 pour les e/s](https://github.com/OfficeDev/Office-365-SDK-for-iOS). 


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


## <a name="batching-outlook-rest-requests-preview"></a>Le traitement par lots de demandes d’Outlook RESTE (aperçu)

[Envoyer les demandes Outlook RESTE par lots](..\api\batch-outlook-rest-requests.md)


## <a name="outlook-task"></a>Tâche Outlook
[API de tâche](..\api\task-rest-operations.md)

**Opérations de tâche** &nbsp; 
 [Tâches de création](..\api\task-rest-operations.md#CreateTasks) | [obtenir des tâches](..\api\task-rest-operations.md#GetTasks) | [mise à jour de tâches](..\api\task-rest-operations.md#UpdateTasks) | [Supprimer des tâches](..\api\task-rest-operations.md#DeleteTasks) | 
[Terminer les tâches](..\api\task-rest-operations.md#CompleteTasks) | [synchroniser des tâches ou des dossiers de tâches](..\api\task-rest-operations.md#SyncTasks) 


**Opérations de dossier de tâche** &nbsp; 
 [Créer des dossiers de tâches](..\api\task-rest-operations.md#CreateTaskFolders) | [obtenir les dossiers de tâches](..\api\task-rest-operations.md#GetTaskFolders) | [mettre à jour les dossiers de tâches](..\api\task-rest-operations.md#UpdateTaskFolders) | 
[Supprimer des dossiers de tâches](..\api\task-rest-operations.md#DeleteTaskFolders) | [synchroniser des tâches ou des dossiers de tâches](..\api\task-rest-operations.md#SyncTasks) 


**Opérations de groupe de tâches** &nbsp; 
 [Créer les groupes de tâches](..\api\task-rest-operations.md#CreateTaskGroups) | [obtenir des groupes de tâches](..\api\task-rest-operations.md#GetTaskGroups) | [mise à jour des groupes de tâches](..\api\task-rest-operations.md#UpdateTaskGroups) | 
[Supprimer les groupes de tâches](..\api\task-rest-operations.md#DeleteTaskGroups)


<a name="bk_people"> </a>

##<a name="outlook-people-preview"></a>Personnes d’Outlook (aperçu)

[API de personnes](..\api\people-rest-operations.md)

**Rechercher :** &nbsp;  
 [Navigation](..\api\people-rest-operations.md#BrowsePeople) | [d’échange](..\api\people-rest-operations.md#BrowsePaging) | 
[tri](..\api\people-rest-operations.md#BrowseSort) | [limitation](..\api\people-rest-operations.md#BrowsePageSize) |
[sélection](..\api\people-rest-operations.md#BrowseSelecting) | [filtrage](..\api\people-rest-operations.md#BrowseFiltering) |
[de filtrage et de sélection](..\api\people-rest-operations.md#BrowseSelectingAndFiltering)

**Recherche :** &nbsp; 
 [Sélectionnez rubrique](..\api\people-rest-operations.md#SearchTopic) |
[filtrer une recherche](..\api\people-rest-operations.md#SearchFilter) |
[recherche floue](..\api\people-rest-operations.md#FuzzySearch)



## <a name="office-365-data-extensions"></a>Extensions de données Office 365

[Extensions de données API](..\api\extensions-rest-operations.md)

**Ouvrir les Extensions de Type :** &nbsp; [Créer un élément existant dans le](..\api\extensions-rest-operations.md#CreateExtensionInExistingItem) | [créer avec un nouvel élément](..\api\extensions-rest-operations.md#CreateExtensionInNewItem) |
[obtenir](..\api\extensions-rest-operations.md#GetExtension) | [obtenir de développé élément](..\api\extensions-rest-operations.md#GetExpandedExtension) |
[mise à jour](..\api\extensions-rest-operations.md#UpdateExtension) | [Supprimer](..\api\extensions-rest-operations.md#DeleteExtension)


## <a name="outlook-extended-properties"></a>Les propriétés étendues de Outlook

[API de propriétés étendues](..\api\extended-properties-rest-operations.md)

**Propriétés étendues**  &nbsp;  [créer un élément existant dans le](..\api\extended-properties-rest-operations.md#CreateExtendedPropertyInExistingItem) | 
[créer avec un nouvel élément](..\api\extended-properties-rest-operations.md#CreateExtendedPropertyInNewItem) | 
[obtenir de développé élément](..\api\extended-properties-rest-operations.md#GetExpandedExtendedProperty) | 
[filtre](..\api\extended-properties-rest-operations.md#GetItemByFilteringExtendedProperty)



<a name="bk_mail"> </a>

##<a name="outlook-mail"></a>Courrier d’Outlook

[API de messagerie](..\api\mail-rest-operations.md) 

**Messages :** &nbsp; [Obtenir](..\api\mail-rest-operations.md#Getmessages) | [créer et envoyer](..\api\mail-rest-operations.md#Sendmessages) |
 [réponse à](..\api\mail-rest-operations.md#Replytomessages) | [vers](..\api\mail-rest-operations.md#Forwardmessages) |
 [mise à jour](..\api\mail-rest-operations.md#Updatemessages) | [Supprimer](..\api\mail-rest-operations.md#DeleteMessages) |
 [déplacer ou copier](..\api\mail-rest-operations.md#MoveCopymessages)

**Pièces jointes :**&nbsp;  [obtenir](..\api\mail-rest-operations.md#GetAttachments) |
 [créer](..\api\mail-rest-operations.md#CreateAttachments) | [Supprimer](..\api\mail-rest-operations.md#DeleteAttachments)

**Dossiers :**&nbsp;  [obtenir](..\api\mail-rest-operations.md#GetFolders) | [créer](..\api\mail-rest-operations.md#CreateFolders) | [mise à jour](..\api\mail-rest-operations.md#UpdateFolders) |
 [Supprimer](..\api\mail-rest-operations.md#DeleteFolders) | [déplacer ou copier](..\api\mail-rest-operations.md#MoveCopyFolders)


<a name="bk_contacts"> </a>

##<a name="outlook-contacts"></a>Contacts Outlook

[API de contacts](..\api\contacts-rest-operations.md)

**Contacts :**&nbsp;  [obtenir](..\api\contacts-rest-operations.md#GetContacts) | [créer](..\api\contacts-rest-operations.md#CreateContacts) |
 [mise à jour](..\api\contacts-rest-operations.md#UpdateContacts) | [Supprimer](..\api\contacts-rest-operations.md#DeleteContacts) 
 

**Dossiers de contacts :**&nbsp;  [obtenir](..\api\contacts-rest-operations.md#GetContactFolders)


<a name="bk_calendar"> </a>

##<a name="outlook-calendar"></a>Calendrier Outlook

[API de calendrier](..\api\calendar-rest-operations.md)

**Affichage Calendrier :**  &nbsp;  [obtenir](..\api\calendar-rest-operations.md#GetCalendarView) | [la synchronisation](..\api\calendar-rest-operations.md#SyncCalendarView)

**Événements :** &nbsp; [Obtenir](..\api\calendar-rest-operations.md#GetEvents) | [Sync](..\api\calendar-rest-operations.md#SyncCalendarView) |
 [créer](..\api\calendar-rest-operations.md#CreateEvents) |
 [mise à jour](..\api\calendar-rest-operations.md#UpdateEvents) | [répondre](..\api\calendar-rest-operations.md#RespondToEvents) | 
 [Supprimer](..\api\calendar-rest-operations.md#DeleteEvents)  

**Les pièces jointes :** &nbsp; 
 [Get](..\api\calendar-rest-operations.md#GetAttachments) | [Create](..\api\calendar-rest-operations.md#reateAttachments) |
 [Delete](..\api\calendar-rest-operations.md#DeleteAttachments)
 
 **Rappels :** &nbsp; 
  [Obtenir](..\api\calendar-rest-operations.md#GetReminders) | 
 [Répéter](..\api\calendar-rest-operations.md#SnoozeReminders) | 
 [faire disparaître](..\api\calendar-rest-operations.md#DismissReminders)

**Les calendriers :** &nbsp; [Obtenir](..\api\calendar-rest-operations.md#GetCalendars) |
 [créer](..\api\calendar-rest-operations.md#CreateCalendars) | [mise à jour](..\api\calendar-rest-operations.md#UpdateCalendars) |
 [Supprimer](..\api\calendar-rest-operations.md#DeleteCalendars)  

**Calendrier des groupes :**&nbsp;   [obtenir](..\api\calendar-rest-operations.md#GetCalendarGroups) |
 [créer](..\api\calendar-rest-operations.md#CreateCalendarGroups) | [mise à jour](..\api\calendar-rest-operations.md#UpdateCalendarGroups) |
 [Supprimer](..\api\calendar-rest-operations.md#DeleteCalendarGroups)



##<a name="resource-reference-for-the-mail-calendar-contacts-and-task-apis"></a>Référence à une ressource pour la messagerie, calendrier, Contacts et API de tâches

[Référence de ressource](..\API\complex-types-for-mail-contacts-calendar.md) 
 
 **Entités :** &nbsp; [Calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource) |
 [CalendarGroup](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource) | [Contact](..\api\complex-types-for-mail-contacts-calendar.md#ContactResource) |
 [ContactFolder](..\api\complex-types-for-mail-contacts-calendar.md#ContactFolderResource) | [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) |
 [EventMessage](..\api\complex-types-for-mail-contacts-calendar.md#EventMessageResource) | [Propriétés étendues](..\api\complex-types-for-mail-contacts-calendar.md#ExtendedProperties) | 
 [FileAttachment](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource) | [dossier](..\api\complex-types-for-mail-contacts-calendar.md#FolderResource) |
 [ItemAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource) | [Message](..\api\complex-types-for-mail-contacts-calendar.md#MessageResource) |
 [tâche (aperçu)](..\api\complex-types-for-mail-contacts-calendar.md#TaskResource) | [TaskFolder (aperçu)](..\api\complex-types-for-mail-contacts-calendar.md#TaskFolderResource) | 
 [TaskGroup (aperçu)](..\api\complex-types-for-mail-contacts-calendar.md#TaskGroupResource) | 
 [utilisateur](..\api\complex-types-for-mail-contacts-calendar.md#UserResource)   
 
 **Des types complexes :** &nbsp; [Participant](..\api\complex-types-for-mail-contacts-calendar.md#Attendee) | 
 [AttendeeBase](..\api\complex-types-for-mail-contacts-calendar.md#AttendeeBase) (aperçu) |  [AttendeeAvailability](..\api\complex-types-for-mail-contacts-calendar.md#AttendeeAvailability) (aperçu de) |  [DateTimeTimeZone](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZoneBeta)  | 
  [EmailAddress](..\api\complex-types-for-mail-contacts-calendar.md#EmailAddress) | 
 [coordonnées géographiques](..\api\complex-types-for-mail-contacts-calendar.md#GeoCoordinates) | 
 [ItemBody](..\api\complex-types-for-mail-contacts-calendar.md#ItemBody)  | 
 [emplacement](..\api\complex-types-for-mail-contacts-calendar.md#Location) (aperçu) |  [LocationConstraint](..\api\complex-types-for-mail-contacts-calendar.md#LocationConstraint) (aperçu de) |  [MeetingTimeCandidate](..\api\complex-types-for-mail-contacts-calendar.md#MeetingTimeCandidate) (aperçu de) |  [PatternedRecurrence](..\api\complex-types-for-mail-contacts-calendar.md#PatternedRecurrence)  | 
  [PhysicalAddress](..\api\complex-types-for-mail-contacts-calendar.md#PhysicalAddress) | 
 [destinataire](..\api\complex-types-for-mail-contacts-calendar.md#Recipient) | 
 [RecurrencePattern](..\api\complex-types-for-mail-contacts-calendar.md#RecurrencePattern) | 
 [RecurrenceRange](..\api\complex-types-for-mail-contacts-calendar.md#RecurrenceRange) | 
 [ResponseStatus](..\api\complex-types-for-mail-contacts-calendar.md#ResponseStatus) | 
 [TimeConstraint](..\api\complex-types-for-mail-contacts-calendar.md#TimeConstraint) (aperçu) |  [Plage horaire](..\api\complex-types-for-mail-contacts-calendar.md#TimeSlot) (aperçu de) |  [Horodatage](..\api\complex-types-for-mail-contacts-calendar.md#TimeStamp) (aperçu)    
 
 
 **Des paramètres de requête OData :** &nbsp; [$search](..\api\complex-types-for-mail-contacts-calendar.md#Search) | 
 [$filter](..\api\complex-types-for-mail-contacts-calendar.md#Filter) | [$select](..\api\complex-types-for-mail-contacts-calendar.md#Select) | 
 [$orderby](..\api\complex-types-for-mail-contacts-calendar.md#OrderBy) | [$top et $skip](..\api\complex-types-for-mail-contacts-calendar.md#TopSkip)  | 
 $expand | [$count](..\api\complex-types-for-mail-contacts-calendar.md#Count)   

<a name="bk_notify"> </a>

##<a name="outlook-notifications"></a>Notifications d’Outlook

[API de Notifications de transmission](../api/notify-rest-operations.md)

[API des Notifications de transmission en continu](../api/notify-streaming-rest-operations.md) (aperçu)


<a name="bk_photo"> </a>

##<a name="outlook-user-photo"></a>Photo de l’utilisateur Outlook

[Photo de l’utilisateur API](../api/photo-rest-operations.md)
 

<a name="bk_discovery"> </a>

##<a name="discovery-service"></a>Service de découverte

[API du Service de découverte](..\api\discovery-service-rest-operations.md)

[Initiale de connexion](..\api\discovery-service-rest-operations.md#DiscoveryServiceoperationsInitialsignin) |
 [découvrir des services spécifiques](..\api\discovery-service-rest-operations.md#DiscoveryServiceoperationsDiscoverspecificservices) | [savoir quels sont les services détectables](..\api\discovery-service-rest-operations.md#DiscoveryServiceoperationsLearnwhatservicesarediscoverable)


<a name="bk_files"> </a>

##<a name="files"></a>Les fichiers

[API de OneDrive](https://dev.onedrive.com/)


<a name="bk_video"> </a>

##<a name="video"></a>Vidéo 

[API de vidéo](../api/video-rest-operations.md)

**Portal de vidéo :** &nbsp;  
   [Obtenir des informations](..\api\video-rest-operations.md#GetPortalInformation)
  
**Canaux :** &nbsp;  
   [Obtenir des informations](..\api\video-rest-operations.md#GetChannelsInfo) 
  
**Informations de vidéo :** &nbsp;  
   [Obtenir](..\api\video-rest-operations.md#GetVideoInfo) | [mettre à jour les métadonnées de la vidéo](..\api\video-rest-operations.md#UpdateVideo) 
  
**Vidéo :** &nbsp;  
   [Télécharger](..\api\video-rest-operations.md#UploadVideos) | [Supprimer](..\api\video-rest-operations.md#DeleteVideos) 

##<a name="api-resource-and-service-endpoints-of-office-365-operated-by-21vianet"></a>Points de terminaison API ressources et service d’Office 365, exploités par 21Vianet
[Points de terminaison API d’Office 365, exploités par 21Vianet](..\api\o365-china-endpoints.md)

##<a name="office-365-management-apis"></a>API de gestion d’Office 365
[Mise en route](https://msdn.microsoft.com/library/office/dn707383.aspx) | [API de Communications Service (aperçu)](https://msdn.microsoft.com/EN-US/library/dn707386.aspx) | [Gestion de référence de l’API activité (aperçu)](https://msdn.microsoft.com/library/office/mt227394.aspx) | [service web de création de rapports](https://msdn.microsoft.com/en-us/library/office/jj984325.aspx) 

##<a name="additional-resources"></a>Ressources supplémentaires

###<a name="api-sandbox"></a>API de Sandbox
[Explorez l’API d’Office 365 à l’aide de cette console interactive](http://apisandbox.msdn.microsoft.com/)

###<a name="rest-api-response-status-codes"></a>Codes de statut de réponse API REST

[Codes de statut de réponse HTTP](..\howto\http-response-status-codes.md)


<<<<<<< TÊTE
<!--
**Get started:** &nbsp; <a href="setup-development-environment?aspnet"> ASP.NET MVC apps </a> | <a href="setup-development-environment?javascript"> JavaScript web apps </a> | <a href="setup-development-environment?iOS"> iOS </a> | <a href="setup-development-environment?android"> Android </a>
-->


<a name="get-started-nbsp-aspnet-mvc-appshowtogetting-started-office-365-apismdaspnet-javascript-web-appshowtogetting-started-office-365-apismdjavascript-ioshowtogetting-started-office-365-apismdios-androidhowtogetting-started-office-365-apismdandroid"></a>**Mise en route :** &nbsp; [Les applications ASP.NET MVC](..\howto\getting-started-Office-365-APIs.md?aspnet) | [les applications web JavaScript](..\howto\getting-started-Office-365-APIs.md?javascript) | [e](..\howto\getting-started-Office-365-APIs.md?iOS) | [Android](..\howto\getting-started-Office-365-APIs.md?android)  
=======
###<a name="office-365-platform-overview"></a>Présentation de la plate-forme Office 365
>>>>>>> la zone de transit

[Vue d’ensemble du développement sur la plate-forme Office 365](..\howto\platform-development-overview.md) | [configurer votre environnement de développement d’Office 365](..\howTo\setup-development-environment.md) 

[Mise en route avec Office 365APIs](..\howto\getting-started-Office-365-APIs.md) 

###<a name="office-365-permission-scopes"></a>Office 365 autorisation étendues
[Pour plus d’informations sur toutes les étendues d’autorisation Office 365](..\howto\application-manifest.md)

###<a name="microsoft-partner-center-api-reference"></a>Référence de l’API Microsoft Partner Center
Partenaires peuvent utiliser l' [API REST de Commerce CSP](https://msdn.microsoft.com/en-us/library/partnercenter/dn974944.aspx) pour créer des comptes clients, gestion des profils de client sur la plate-forme de Commerce de Microsoft et d’achat et gestion des commandes et abonnements des produits Microsoft pour leurs clients. 



