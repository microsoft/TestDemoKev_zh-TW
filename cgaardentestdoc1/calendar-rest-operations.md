MS. TocTitle : Référence des API REST de calendrier Outlook titre : référence de l’API REST de calendrier Outlook Description : comment interagir avec la bibliothèque de l’API REST de calendrier et le client API qui fournissent l’accès aux groupes de calendrier dans Exchange Online, des calendriers et des événements de référence. MS. ContentId : 443f1cdf-1adb-46a2-b299-228c6f429954 ms.topic : ms.date de référence (API) : le 29 juin 2016

[!INCLUDE [Add the O365API repo styles](../includes/controls/addo365apistyleshtml)]

# <a name="outlook-calendar-rest-api-reference"></a>Référence des API REST de calendrier Outlook


[!INCLUDE [Add the Outlook REST API filters--v2 default](../includes/controls/addOutlookVersion_v2defaulthtml)]

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<p class="previewnote">Cette documentation traite de l’API pour rechercher les horaires de la réunion, l’annulation des événements et des pièces jointes de référence qui se trouvent dans l’aperçu. Aperçu des fonctionnalités peuvent être modifiées avant la finalisation et peuvent endommager le code qui les utilise. De ce fait, en général vous devez utiliser une version de production d’une API dans votre code de production. Le cas échéant, v2.0 est actuellement la version par défaut.</p>

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

   
 _**S’applique à :** Exchange Online | Office 365 | Hotmail.com | Live.com | MSN.com | Outlook.com | Passport.com_

L’API de calendrier permet d’accéder aux événements, calendrier et les données de groupe calendrier sécurisées par Azure Active Directory sur Office 365 et des données similaires dans des comptes de Microsoft en particulier dans ces domaines : Hotmail.com, Live.com, MSN.com, Outlook.com et Passport.com. 
  

<!-- Can add the following sentence back once the client libraries have been updated for converged auth and outlook.com

You can access the Calendar API by calling the corresponding REST APIs directly in your apps, or by using the Office 365 client libraries and SDKs.
-->

**Remarque** 

- L’exception est l’API pour [déterminer l’heure de la réunion](#FindMeetingTimesPreview), qui s’applique à uniquement Office 365 boîtes aux lettres (sur Azure AD) et non à des comptes de Microsoft. 
- Pour plus de simplicité de référence, le reste de cet article utilise **« Outlook.com » pour inclure les domaines de compte Microsoft répertoriés ci-dessus**.


<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

**Ne pas intéressé par la version bêta de l’API ?** Utiliser le contrôle dans le coin supérieur droit et sélectionnez la version souhaitée.

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


<!-- ==================================== End BETA content ====================================================== -->


<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

**Ne pas intéressé par la version 2.0 de l’API ?** Utiliser le contrôle dans le coin supérieur droit et sélectionnez la version souhaitée.

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->




<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

**Ne pas intéressé par la version 1.0 de l’API ?** Utiliser le contrôle dans le coin supérieur droit et sélectionnez la version souhaitée.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->
 
 
 
## <a name="all-calendar-api-operations"></a>Toutes les opérations d’API de calendrier

<a name="EventOperations"></a> 
 **Des opérations d’événements** un événement représente un rendez-vous ou une réunion dans le calendrier de l’utilisateur. Un événement peut être une série master (pour des événements récurrents), une occurrence, une seule instance ou une exception.

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

[Obtenir des événements de](#GetEvents) | [les événements de synchronisation](#SyncCalendarView) | [déterminer l’heure de la réunion (aperçu)](#FindMeetingTimesPreview) | [créer événements](#CreateEvents) | 
[mettre à jour les événements](#UpdateEvents) | [répondre aux événements](#RespndToEvents) | [Supprimer les événements](#DeleteEvents) | [Annuler les événements (aperçu)](#CancelEvents) | 
[extraire les pièces jointes](#GetAttachments) | [les pièces jointes de créer](#CreateAttachments) | [Supprimer les pièces jointes](#DeleteAttachments) | 
[obtenir des rappels](#GetReminders) | [Répéter les rappels](#SnoozeReminders)] | [Faire disparaître le rappel](#DismissReminders)


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->



<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

[Obtenir des événements de](#GetEvents) | [les événements de synchronisation](#SyncCalendarView) | [créer événements](#CreateEvents) | 
[mettre à jour les événements](#UpdateEvents) | [répondre à des événements](#RespndToEvents) | [Supprimer des événements](#DeleteEvents) | 
[obtenir les pièces jointes](#GetAttachments) | [les pièces jointes de créer](#CreateAttachments) | [Supprimer les pièces jointes](#DeleteAttachments) | 
[obtenir des rappels](#GetReminders) | [Répéter les rappels](#SnoozeReminders)] | [Faire disparaître le rappel](#DismissReminders)


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->


[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

[Obtenir des événements de](#GetEvents) | [les événements de synchronisation](#SyncCalendarView) | [créer événements](#CreateEvents) | 
[mettre à jour les événements](#UpdateEvents) | [répondre à des événements](#RespndToEvents) | [Supprimer des événements](#DeleteEvents) | 
[obtenir les pièces jointes](#GetAttachments) | [les pièces jointes de créer](#CreateAttachments) | [Supprimer les pièces jointes](#DeleteAttachments) | 
[obtenir des rappels](#GetReminders) | [Répéter les rappels](#SnoozeReminders)] | [Faire disparaître le rappel](#DismissReminders)

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->




<a name="CalendarOperations"> </a>
**Opérations de calendrier** Un calendrier sert de conteneur pour les événements. Un utilisateur peut avoir plusieurs calendriers. Dans Office 365, chaque calendrier peut être attribué à un groupe de calendriers.

[Obtenir les calendriers](#GetCalendars) | [créer calendriers](#CreateCalendars) | [mise à jour des calendriers](#UpdateCalendars) | [Supprimer des calendriers](#DeleteCalendars) 

<a name="CalendarGroupOperations"></a> 
Groupes de calendrier des **opérations du groupe de calendrier** sont une façon d’organiser plusieurs calendriers. Les utilisateurs peuvent ajouter plusieurs calendriers dans un groupe unique de calendrier dans Outlook ou Outlook Web App. Cela rend plus facile pour les utilisateurs d’afficher rapidement tous les calendriers au sein du groupe.


**Remarque** Outlook.com prend en charge uniquement le groupe de calendrier par défaut qui est accessible par le `../me/calendars` raccourci. Vous ne peut pas supprimer ce groupe de calendriers ou créer un autre groupe de calendriers.


[Obtenir les groupes calendrier](#GetCalendarGroups) | [groupes de calendrier créer](#CreateCalendarGroups) | 
[mettre à jour les groupes de calendrier](#UpdateCalendarGroups) | [Supprimer des groupes de calendrier](#DeleteCalendarGroups)  

Voir aussi :

[Ressource d’événement API REST](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) | 
[ressource de calendrier API REST](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource) |
[ressource de groupe calendrier API REST](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource)



<a name="Overview"> </a>
## <a name="using-the-calendar-rest-api"></a>À l’aide de l’API REST de calendrier

### <a name="authentication"></a>Authentification

Comme les autres [API REST de Outlook](..\api\use-outlook-rest-api.md#DefineOutlookRESTAPI), pour chaque demande à l’API de calendrier, vous devez inclure un jeton d’accès valide. L’obtention d’un jeton d’accès nécessite que vous avez enregistré identifié votre application et obtenu l’autorisation appropriée. Vous pouvez [en savoir plus](..\api\use-outlook-rest-api.md#ShortRegAuthWorkflow) sur certains rationalisée d’enregistrement et les options d’autorisation pour vous. Gardez à l’esprit pendant que vous procédez à des opérations spécifiques dans l’API de calendrier.

<a name="SupportedVersions"> </a>

###<a name="version-of-api"></a>Version de l’API

L’API REST de calendrier est pris en charge dans toutes les versions de l’API REST de Outlook. La fonctionnalité peut différer en fonction de la version spécifique.

###<a name="target-user"></a>Utilisateur cible

Les demandes de calendrier API sont toujours effectuées pour le compte de l’utilisateur actuel. 

Pour plus d’informations communes à tous les sous-ensembles de l’API REST de Outlook, reportez-vous à la section [utilisation de l’API REST de Outlook](..\api\use-outlook-rest-api.md) .

****

<a name="GetEvents"> </a>
## <a name="get-events"></a>Obtenir des événements

Obtenir une collection des événements ou un événement. 

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

Toutes les opérations qui obtiennent des événements de calendrier peuvent utiliser le _Prefer : outlook.timezone_ en-tête HTTP pour spécifier le fuseau horaire pour les heures de début et de fin dans la réponse. Par exemple, la suivante _Prefer : outlook.timezone_ en-tête définit les heures de début et de fin dans la réponse à l’heure.

```
Prefer: outlook.timezone="Eastern Standard Time"
``` 

Si vous ne spécifiez pas la _Prefer : outlook.timezone_ en-tête les heures de début et de fin dans la réponse sont retournées en heure UTC.

Vous pouvez utiliser les propriétés _OriginalStartTimeZone_ et _OriginalEndTimeZone_ sur la ressource de _l’événement_ pour déterminer le fuseau horaire utilisé lors de la création de l’événement.

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->
<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

Toutes les opérations qui obtiennent des événements de calendrier peuvent utiliser le _Prefer : outlook.timezone_ en-tête HTTP pour spécifier le fuseau horaire pour les heures de début et de fin dans la réponse. Par exemple, la suivante _Prefer : outlook.timezone_ en-tête définit les heures de début et de fin dans la réponse à l’heure.

```
Prefer: outlook.timezone="Eastern Standard Time"
``` 

Si vous ne spécifiez pas la _Prefer : outlook.timezone_ en-tête les heures de début et de fin dans la réponse sont retournées en heure UTC. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. 

Vous pouvez utiliser les propriétés _OriginalStartTimeZone_ et _OriginalEndTimeZone_ sur la ressource de _l’événement_ pour déterminer le fuseau horaire utilisé lors de la création de l’événement.

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->


L’API REST : [obtenir un affichage de calendrier (RESTE)](#GetCalendarView) |  
[Obtenir le masque de la série et événements uniques (RESTE)](#GetEventCollection) |
 [obtenir des instances d’événements (RESTE)](#GetEventInstances) | [obtenir un événement (RESTE)](#GetEvent) 

Les bibliothèques clientes : [obtenir des événements de calendrier de l’utilisateur (Client)](#GetEventsClient)

****

<a name="GetCalendarView"> </a>
###<a name="get-a-calendar-view-rest"></a>Obtenir une vue de calendrier (RESTE) 

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Obtenir les occurrences, les exceptions et les instances d’événements dans un calendrier défini par une plage de temps dans le calendrier principal de l’utilisateur (`../me/calendarview`) ou à partir d’un autre calendrier.
   

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
GET https://outlook.office.com/api/beta/me/calendars/{calendar_id}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|calendar_id|string|L’ID de calendrier, si vous obtenez un affichage de calendrier à partir d’un calendrier spécifique.|
|start_datetime|DateTimeOffset|La date et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date et l’heure de fin de l’événement.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont retournées en heure UTC.

**Remarque** Par défaut, chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

Par exemple, obtenir l’affichage de calendrier pour le mois d’octobre, pour retourner uniquement la propriété Subject pour chaque événement. En supposant que la _Prefer : outlook.timezone_ en-tête n’est pas inclus dans la demande, le fuseau horaire UTC. 

```
GET https://outlook.office.com/api/beta/me/calendarview?startDateTime=2014-10-01T01:00:00Z&endDateTime=2014-10-31T23:00:00Z&$select=Subject
```

 **Type de réponse**

Les [événements](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) étendue dans la plage spécifiée.


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->


<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


```no-highlight
GET https://outlook.office.com/api/v2.0/me/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
GET https://outlook.office.com/api/v2.0/me/calendars/{calendar_id}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|calendar_id|string|L’ID de calendrier, si vous obtenez un affichage de calendrier à partir d’un calendrier spécifique.|
|start_datetime|DateTimeOffset|La date et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date et l’heure de fin de l’événement.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont retournées en heure UTC.

**Remarque** Par défaut, chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

Par exemple, obtenir l’affichage de calendrier pour le mois d’octobre, pour retourner uniquement la propriété Subject pour chaque événement. En supposant que la _Prefer : outlook.timezone_ en-tête n’est pas inclus dans la demande, le fuseau horaire UTC. 

```
GET https://outlook.office.com/api/v2.0/me/calendarview?startDateTime=2014-10-01T01:00:00&endDateTime=2014-10-31T23:00:00&$select=Subject
```

 **Type de réponse**

Les [événements](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) étendue dans la plage spécifiée.


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v1.0/me/calendarview?start={start_datetime}&end={end_datetime}
GET https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|L’ID de calendrier, si vous obtenez un affichage de calendrier à partir d’un calendrier spécifique.|
|start_datetime|DateTimeOffset|La date et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date et l’heure de fin de l’événement.|

**Remarque** Par défaut, chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

Par exemple, obtenir l’affichage de calendrier pour le mois d’octobre, pour retourner uniquement la propriété Subject pour chaque événement : 

```
GET https://outlook.office.com/api/v1.0/me/calendarview?startDateTime=2014-10-01T01:00:00Z&endDateTime=2014-10-31T23:00:00Z&$select=Subject
```

 **Type de réponse**

Les [événements](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) étendue dans la plage spécifiée.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->


****

<a name="GetEventCollection"> </a>
###<a name="get-series-master-and-single-events-rest"></a>Obtenir le masque de la série et événements uniques (RESTE) 

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Obtenir une collection d’événements d’instance principale et une série de calendrier principal de l’utilisateur (`../me/events`) ou à partir d’un autre calendrier. Pour obtenir des instances de l’événement de développé, vous pouvez  [obtenir l’affichage Calendrier](#GetCalendarView) ou [obtenir les instances d’un événement](#GetEventInstances).



<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
GET https://outlook.office.com/api/beta/me/events
GET https://outlook.office.com/api/beta/me/calendars/{calendar_id}/events
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|Paramètres de _Header|
|Préférez :|Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|calendar_id|string|L’ID de calendrier, si vous recevez des événements à partir d’un calendrier spécifique.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont renvoyés en UTC.

**Remarque** Chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Consultez l’exemple suivant. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

L’exemple suivant montre comment utiliser **$select** pour spécifier le retourner uniquement les propriétés **Subject**, la **bibliothèque multimédia**, le **début** et la **fin** de chaque événement dans la réponse. Reportez-vous à la première réponse d’exemple dans [obtenir un événement (REST)](#GetEvent) pour une liste complète de propriétés qui seraient renvoyés pour un événement si vous n’utilisez pas **$select**.


**Exemple de requête**

```
GET https://outlook.office.com/api/beta/me/events?$select=Subject,Organizer,Start,End
```

**Exemple de réponse**

Code d’état : 200

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|calendar_id|string|L’ID de calendrier, si vous recevez des événements à partir d’un calendrier spécifique.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont retournées en heure UTC.

**Remarque** Chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Consultez l’exemple suivant. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

L’exemple suivant montre comment utiliser **$select** pour spécifier le retourner uniquement les propriétés **Subject**, la **bibliothèque multimédia**, le **début** et la **fin** de chaque événement dans la réponse. Reportez-vous à la première réponse d’exemple dans [obtenir un événement (REST)](#GetEvent) pour une liste complète de propriétés qui seraient renvoyés pour un événement si vous n’utilisez pas **$select**.


**Exemple de requête**

```
GET https://outlook.office.com/api/v2.0/me/events?$select=Subject,Organizer,Start,End
```

**Exemple de réponse**

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|L’ID de calendrier, si vous recevez des événements à partir d’un calendrier spécifique.|

**Remarque** Chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Consultez l’exemple suivant. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

L’exemple suivant montre comment utiliser **$select** pour spécifier le retourner uniquement les propriétés **Subject**, la **bibliothèque multimédia**, le **début** et la **fin** de chaque événement dans la réponse. Reportez-vous à la première réponse d’exemple dans [obtenir un événement (REST)](#GetEvent) pour une liste complète de propriétés qui seraient renvoyés pour un événement si vous n’utilisez pas **$select**.


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
###<a name="get-event-instances-rest"></a>Obtenir des instances d’événements (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Vous pouvez obtenir les instances (occurrences) d’un événement pour une plage de temps spécifiée. Si l’événement est un type **SeriesMaster** , cela renvoie les occurrences et les exceptions de cet événement dans la plage de temps spécifiée.


<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}/instances?startDateTime={start_datetime}&endDateTime={end_datetime}
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|start_datetime|DateTimeOffset|La date de l’UTC et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date de l’UTC et l’heure de fin de l’événement.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont retournées en heure UTC.

 **Type de réponse**

La collection demandée [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) .

**Remarque** Par défaut, chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée.  
Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

Par exemple, obtenir des instances d’un événement particulier pour le mois d’octobre, incluez uniquement les propriétés **Subject**, le **début** et la **fin** de chaque instance : 

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|start_datetime|DateTimeOffset|La date de l’UTC et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date de l’UTC et l’heure de fin de l’événement.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont retournées en heure UTC.

 **Type de réponse**

La collection demandée [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) .

**Remarque** Par défaut, chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée.  
Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

Par exemple, obtenir des instances d’un événement particulier pour le mois d’octobre, incluez uniquement les propriétés **Subject**, le **début** et la **fin** de chaque instance : 

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|start_datetime|DateTimeOffset|La date de l’UTC et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date de l’UTC et l’heure de fin de l’événement.|


 **Type de réponse**

La collection demandée [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) .

**Remarque** Par défaut, chaque événement dans la réponse inclut toutes ses propriétés. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée.  
Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

Par exemple, obtenir des instances d’un événement particulier pour le mois d’octobre, incluez uniquement les propriétés **Subject**, le **début** et la **fin** de chaque instance : 

<!--don't use httprequest for this because it renders as lowercase, which breaks the call-->
```
GET https://outlook.office.com/api/v1.0/me/events/AAMkAGE0MGM1Y2M5LWEAAA=/instances?startDateTime=2014-10-01T01:00:00Z&endDateTime=2014-10-31T23:00:00Z&$select=Subject,Start,End
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->

****


<a name="GetEvent"> </a>
###<a name="get-an-event-rest"></a>Obtenir un événement (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Obtenir un événement en code.


<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont retournées en heure UTC.

**Exemple de requête**

```
GET https://outlook.office.com/api/beta/me/events/AAMkAGI2TG93AAA=
```

**Exemple de réponse**

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


**Type de réponse**

L' [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)demandé.

**Remarque** Par défaut, la réponse inclut toutes les propriétés de l’événement. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

L’exemple suivant montre comment utiliser **$select** pour spécifier renvoyant les propriétés **Subject**, la **bibliothèque multimédia**, le **début** et la **fin** de l’événement. 


**Exemple de requête**

```
GET https://outlook.office.com/api/beta/me/events/AAMkAGI2TG93AAA=?$select=Subject,Organizer,Start,End
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont retournées en heure UTC.

**Exemple de requête**

```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGI2TG93AAA=
```

**Exemple de réponse**

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


**Type de réponse**

L' [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)demandé.

**Remarque** Par défaut, la réponse inclut toutes les propriétés de l’événement. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

L’exemple suivant montre comment utiliser **$select** pour spécifier renvoyant les propriétés **Subject**, la **bibliothèque multimédia**, le **début** et la **fin** de l’événement. 

**Exemple de requête**

```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGI2TG93AAA=?$select=Subject,Organizer,Start,End
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|

```REST-i
[!INCLUDE [calendar_api_get_event_by_id](./_data/calendar_api_get_event_by_id.json)]
```


**Type de réponse**

L' [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)demandé.

**Remarque** Par défaut, la réponse inclut toutes les propriétés de l’événement. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

L’exemple suivant montre comment utiliser **$select** pour spécifier renvoyant les propriétés **Subject**, la **bibliothèque multimédia**, le **début** et la **fin** de l’événement. 

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
### <a name="get-events-from-the-users-calendar-client"></a>Obtenir des événements de calendrier de l’utilisateur (Client)

Obtenez les événements du calendrier par défaut de l’utilisateur. Pour obtenir les événements à partir d’un autre calendrier, appelez la propriété des **événements** du calendrier.

Exemple :`outlookClient.Me.Calendars[calendarId].Events.ExecuteAsync()`


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


Pour obtenir un événement particulier, vous pouvez spécifier l’ID d’événement en tant que l’index de la collection des **événements** ou utilisez la méthode **GetById** .

**Remarque** Collections d’événement prend en charge les expressions de requête par exemple **Sélectionner**, **OrderBy**et **prendre**.

Cet exemple appelle la méthode qui [crée le client Outlook](..\api\use-outlook-rest-api.md#GetClient).

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


Cet appel renvoie la série d’événements, pas les instances de développé individuelles pour des événements récurrents (par exemple, une réunion d’équipe hebdomadaire).

Interrogation des instances d’événements n’est actuellement pas pris en charge dans la bibliothèque cliente. Vous pouvez utiliser l’API REST pour interroger la propriété **CalendarView** sur le  [calendrier](..\api\calendar-rest-operations.md#CalendarResource) de ressource ou la propriété **Instances** sur la ressource de [l’événement](..\api\calendar-rest-operations.md#EventResource) :


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
##<a name="sync-events"></a>Événements de synchronisation  

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Synchroniser et obtenir de nouveaux, mis à jour ou supprimé des événements dans une plage de temps spécifiée dans le calendrier principal de l’utilisateur (`../me/calendarview`) ou à partir d’un autre calendrier. Ensemble d’événements dans une plage de temps est également appelé un affichage de calendrier. Les événements retournés peuvent inclure des occurrences et des exceptions d’une série périodique et des instances uniques. 

Synchronisation d’un affichage de calendrier en général nécessite un arrondi de deux ou plusieurs requêtes de synchronisation, qui est un appel GET. Pour synchroniser un affichage de calendrier, utilisez la méthode GET comme la façon dont vous [Obtenez un affichage de calendrier](#GetCalendarView), à ceci près que vous incluez certains en-têtes de requête et _deltaToken_ ou un _skipToken_ le cas échéant.  

**En-têtes de demande**

- Vous devez spécifier le « Prefer : odata.track-modifications » en-tête dans la synchronisation de toutes les demandes, à l’exception de celles qui comportent une `skipToken` qui est retourné à partir d’une précédente demande de synchronisation. Dans la première réponse, recherchez le _appliqué à la préférence : odata.track-modifications_ en-tête pour confirmer que la ressource prend en charge la synchronisation avant de continuer. (Plus d’informations sur un `skipToken` dans des [données de réponse deuxième exemple](#SyncCalendarViewSampleSecondResponse) ci-dessous.)
- Vous pouvez spécifier le « Prefer : odata.maxpagesize={x} » en-tête pour indiquer le nombre maximal d’événements de synchronisation demande renvoie.

Voici un cycle typique de la synchronisation d’événements dans un calendrier :

1. Rendre la demande GET initiale avec obligatoire _Prefer : odata.track-modifications_ en-tête. La première réponse à une demande de synchronisation retourne toujours un _deltaToken_. (Les demandes GET deuxième différent de la première requête GET en incluant soit un _deltaToken_ ou un _skipToken_ a reçu une réponse précédente.)

2. Si la première réponse retourne le _appliqué à la préférence : odata.track-modifications_ en-tête, vous pouvez procéder à la synchronisation.

  - Effectuez une deuxième demande GET. Spécifier la _Prefer : odata.track-modifications_ en-tête et l' _deltaToken_ retourné par la premier GET pour déterminer s’il existe des événements supplémentaires. La deuxième demande renvoie des événements supplémentaires et un _skipToken_ s’il y a plus d’événements ou un _deltaToken_ si le dernier événement a été synchronisé, auquel cas vous pouvez l’arrêter.

  - Poursuivre la synchronisation en envoyant un appel GET et comprenant un _skipToken_ qui est retourné par l’appel précédent. Arrêter lorsque vous obtenez une réponse finale qui contient un en-tête de _@odata.deltaLink_ avec un _deltaToken_ , qui indique la synchronisation est terminée.

Examinons la syntaxe pour les appels initiales et ultérieures dans un cycle de synchronisation.

<!-- ==================================== Begin beta content ======================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

**Pour une synchronisation dans le calendrier par défaut**

Requête initiale : 

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```

Deuxième demande ou première demande d’un arrondi suivant :

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```

Demande de l’arrondi même tiers ou ultérieure  

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**Pour une synchronisation dans un calendrier spécifique**

Requête initiale :

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


Deuxième demande ou première demande d’un arrondi suivant :

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```


Demande de tiers ou ultérieure dans la même série :

```no-highlight
GET https://outlook.office.com/api/beta/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**Paramètres**

|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|user_context|string|Le contexte de l’utilisateur. Vous pouvez utiliser la valeur de 'me' pour indiquer que le contexte de l’utilisateur actuel. Vous pouvez également utiliser les utilisateurs / nom de format {upn} où l' **upn** est le principal de l’utilisateur qui est en général adresse de messagerie l’utilisateur.|
|calendar_id|string|L’ID de calendrier, si vous obtenez un affichage de calendrier à partir d’un calendrier spécifique.|
|start_datetime|DateTimeOffset|La date et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date et l’heure de fin de l’événement.|
|delta_token|string|Le `deltaToken` chaîne retournée en tant que partie de la valeur de @odata.deltaLink dans la réponse de synchronisation précédente.|
|skip_token|string|Le `skipToken` chaîne retournée en tant que partie de la valeur de @odata.nextLink dans la réponse de synchronisation précédente. |

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, les heures de début et de fin sont retournées en heure UTC.

**Remarque** 

- Lors de la spécification « Prefer : odata.track-modifications » dans la requête initiale, si la réponse prend en charge la synchronisation, la réponse inclut » appliqué à la préférence : odata.track-modifications » dans l’en-tête.
- Si vous tentez de synchroniser une ressource qui n’est pas pris en charge, ou s’il ne s’agit pas de la demande de synchronisation initiale, vous ne verrez pas l’en-tête « Préférence-appliqué » dans la réponse.
- Vous pouvez modifier la période de modification en modifiant les paramètres de requête startdatetime et enddatetime.  
- Chaque événement dans la réponse inclut toutes ses propriétés. 
- Pour une série périodique, une réponse de synchronisation contient l’événement entier pour le maître d’abonnement et les événements d’exception. 
- Les instances d’une série périodique sont abrégés et contiennent uniquement les propriétés **Start** et **End** . Vous pouvez capturer le reste des informations événement occurrence de l’événement principal périodique. Pour plus d’informations, reportez-vous à la section [ressource de l’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) .
- Vous ne pouvez pas utiliser le $filter $count, $select, $skip, $top et $search les paramètres de requête. 

**Type de réponse**

Les [événements](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) développé et les événements abrégés dans la plage spécifiée.

**Exemple**

L’exemple suivant affiche les demandes de synchronisation initiale et la seconde pour synchroniser le calendrier par défaut pour l’utilisateur. Chaque demande spécifie pour ne renvoyer qu’un seul événement complète à la fois :
- La réponse initiale renvoie un événement, une `deltaLink` et `deltaToken`. 
- La seconde requête utilise `deltatoken`. La seconde réponse renvoie un événement, une `nextLink` et `skipToken`. 

Pour effectuer la synchronisation, utilisez la `skipToken` retourné à partir de la demande de synchronisation précédente jusqu'à ce que la réponse de synchronisation renvoie une `deltaLink` et `deltaToken`, auquel cas cette phase de la synchronisation est terminée. Enregistrer le `deltaToken` pour le lot suivant de synchronisation. 

Pour plus d’informations, consultez [synchronisation d’événements dans un affichage de calendrier Outlook](..\howto\sync-calendar-view.md).
 
<a name="SyncCalendarViewSampleInitialRequest"></a>

**Exemple de demande initiale**

```
    GET https://outlook.office.com/api/beta/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z HTTP/1.1
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
    Prefer: outlook.timezone="Pacific Standard Time"
```

**Exemple de données de réponse initiale**

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

**Exemple de deuxième demande**

```
    GET https://outlook.office.com/api/beta/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z&$deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
    Prefer: outlook.timezone="Pacific Standard Time"
```

<a name="SyncCalendarViewSampleSecondResponse"></a>

**Données de réponse deuxième exemple**

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


**Pour une synchronisation dans le calendrier par défaut**

Requête initiale : 

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```

Deuxième demande ou première demande d’un arrondi suivant :

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```

Demande de l’arrondi même tiers ou ultérieure  

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**Pour une synchronisation dans un calendrier spécifique**

Requête initiale :

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


Deuxième demande ou première demande d’un arrondi suivant :

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```


Demande de tiers ou ultérieure dans la même série :

```no-highlight
GET https://outlook.office.com/api/v2.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**Paramètres**

|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|user_context|string|Le contexte de l’utilisateur. Vous pouvez utiliser la valeur de 'me' pour indiquer que le contexte de l’utilisateur actuel. Vous pouvez également utiliser les utilisateurs / nom de format {upn} où l' **upn** est le principal de l’utilisateur qui est en général adresse de messagerie l’utilisateur.|
|calendar_id|string|L’ID de calendrier, si vous obtenez un affichage de calendrier à partir d’un calendrier spécifique.|
|start_datetime|DateTimeOffset|La date et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date et l’heure de fin de l’événement.|
|delta_token|string|Le `deltaToken` chaîne retournée en tant que partie de la valeur de @odata.deltaLink dans la réponse de synchronisation précédente.|
|skip_token|string|Le `skipToken` chaîne retournée en tant que partie de la valeur de @odata.nextLink dans la réponse de synchronisation précédente. |

**Remarque** 

- Lors de la spécification « Prefer : odata.track-modifications » dans la requête initiale, si la réponse prend en charge la synchronisation, la réponse inclut » appliqué à la préférence : odata.track-modifications » dans l’en-tête.
- Si vous tentez de synchroniser une ressource qui n’est pas pris en charge, ou s’il ne s’agit pas de la demande de synchronisation initiale, vous ne verrez pas l’en-tête « Préférence-appliqué » dans la réponse.
- Vous pouvez modifier la période de modification en modifiant les paramètres de requête startdatetime et enddatetime.  
- Chaque événement dans la réponse inclut toutes ses propriétés. 
- Pour une série périodique, une réponse de synchronisation contient l’événement entier pour le maître d’abonnement et les événements d’exception. 
- Les instances d’une série périodique sont abrégés et contiennent uniquement les propriétés **Start** et **End** . Vous pouvez capturer le reste des informations événement occurrence de l’événement principal périodique. Pour plus d’informations, reportez-vous à la section [ressource de l’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) .
- Vous ne pouvez pas utiliser le $filter $count, $select, $skip, $top et $search les paramètres de requête. 

**Type de réponse**

Les [événements](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) développé et les événements abrégés dans la plage spécifiée.

**Exemple**

L’exemple suivant affiche les demandes de synchronisation initiale et la seconde pour synchroniser le calendrier par défaut pour l’utilisateur. Chaque demande spécifie pour ne renvoyer qu’un seul événement complète à la fois :
- La réponse initiale renvoie un événement, une `deltaLink` et `deltaToken`. 
- La seconde requête utilise `deltatoken`. La seconde réponse renvoie un événement, une `nextLink` et `skipToken`. 

Pour effectuer la synchronisation, utilisez la `skipToken` retourné à partir de la demande de synchronisation précédente jusqu'à ce que la réponse de synchronisation renvoie une `deltaLink` et `deltaToken`, auquel cas cette phase de la synchronisation est terminée. Enregistrer le `deltaToken` pour le lot suivant de synchronisation. 

Pour plus d’informations, consultez [synchronisation d’événements dans un affichage de calendrier Outlook](..\howto\sync-calendar-view.md).
 
<a name="SyncCalendarViewSampleInitialRequest"></a>

**Exemple de demande initiale**

```
    GET https://outlook.office.com/api/v2.0/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z HTTP/1.1
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
```

**Exemple de données de réponse initiale**

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

**Exemple de deuxième demande**

```
    GET https://outlook.office.com/api/v2.0/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z&$deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
```

<a name="SyncCalendarViewSampleSecondResponse"></a>

**Données de réponse deuxième exemple**

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


**Pour une synchronisation dans le calendrier par défaut**

Requête initiale : 

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```

Deuxième demande ou première demande d’un arrondi suivant :

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```

Demande de l’arrondi même tiers ou ultérieure  

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**Pour une synchronisation dans un calendrier spécifique**

Requête initiale :

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}
```


Deuxième demande ou première demande d’un arrondi suivant :

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$deltatoken={delta_token}
```


Demande de tiers ou ultérieure dans la même série :

```no-highlight
GET https://outlook.office.com/api/v1.0/{user_context}/calendars('{calendar_id}')/calendarview?startDateTime={start_datetime}&endDateTime={end_datetime}&$skiptoken={skip_token}
```

**Paramètres**

|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|user_context|string|Le contexte de l’utilisateur. Vous pouvez utiliser la valeur de 'me' pour indiquer que le contexte de l’utilisateur actuel. Vous pouvez également utiliser les utilisateurs / nom de format {upn} où l' **upn** est le principal de l’utilisateur qui est en général adresse de messagerie l’utilisateur.|
|calendar_id|string|L’ID de calendrier, si vous obtenez un affichage de calendrier à partir d’un calendrier spécifique.|
|start_datetime|DateTimeOffset|La date et l’heure à laquelle l’événement démarre.|
|end_datetime|DateTimeOffset|La date et l’heure de fin de l’événement.|
|delta_token|string|Le `deltaToken` chaîne retournée en tant que partie de la valeur de @odata.deltaLink dans la réponse de synchronisation précédente.|
|skip_token|string|Le `skipToken` chaîne retournée en tant que partie de la valeur de @odata.nextLink dans la réponse de synchronisation précédente. |

**Remarque** 

- Lors de la spécification « Prefer : odata.track-modifications » dans la requête initiale, si la réponse prend en charge la synchronisation, la réponse inclut » appliqué à la préférence : odata.track-modifications » dans l’en-tête.
- Si vous tentez de synchroniser une ressource qui n’est pas pris en charge, ou s’il ne s’agit pas de la demande de synchronisation initiale, vous ne verrez pas l’en-tête « Préférence-appliqué » dans la réponse.
- Vous pouvez modifier la période de modification en modifiant les paramètres de requête startdatetime et enddatetime.  
- Chaque événement dans la réponse inclut toutes ses propriétés. 
- Pour une série périodique, une réponse de synchronisation contient l’événement entier pour le maître d’abonnement et les événements d’exception. 
- Les instances d’une série périodique sont abrégés et contiennent uniquement les propriétés **Start** et **End** . Vous pouvez capturer le reste des informations événement occurrence de l’événement principal périodique. Pour plus d’informations, reportez-vous à la section [ressource de l’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) .
- Vous ne pouvez pas utiliser le $filter $count, $select, $skip, $top et $search les paramètres de requête. 

**Type de réponse**

Les [événements](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) développé et les événements abrégés dans la plage spécifiée.

**Exemple**

L’exemple suivant affiche les demandes de synchronisation initiale et la seconde pour synchroniser le calendrier par défaut pour l’utilisateur. Chaque demande spécifie pour ne renvoyer qu’un seul événement complète à la fois :
- La réponse initiale renvoie un événement, une `deltaLink` et `deltaToken`. 
- La seconde requête utilise `deltatoken`. La seconde réponse renvoie un événement, une `nextLink` et `skipToken`. 

Pour effectuer la synchronisation, utilisez la `skipToken` retourné à partir de la demande de synchronisation précédente jusqu'à ce que la réponse de synchronisation renvoie une `deltaLink` et `deltaToken`, auquel cas cette phase de la synchronisation est terminée. Enregistrer le `deltaToken` pour le lot suivant de synchronisation. 

Pour plus d’informations, consultez [synchronisation d’événements dans un affichage de calendrier Outlook](..\howto\sync-calendar-view.md).
 
<a name="SyncCalendarViewSampleInitialRequest"></a>

**Exemple de demande initiale**

```
    GET https://outlook.office.com/api/v1.0/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z HTTP/1.1
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
```

**Exemple de données de réponse initiale**

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

**Exemple de deuxième demande**

```
    GET https://outlook.office.com/api/v1.0/me/calendarview?startdatetime=2015-01-01T00:00:00Z&enddatetime=2015-04-10T00:00:00Z&$deltatoken=v2%2cH4roCAAA%3d%2c1.0%2cFalse%2cA00%2c
    Authorization: Bearer <token>
    Prefer: odata.track-changes
    Prefer: odata.maxpagesize=1
```

<a name="SyncCalendarViewSampleSecondResponse"></a>

**Données de réponse deuxième exemple**

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
## <a name="find-meeting-times-preview"></a>Déterminer l’heure de la réunion (aperçu)

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Chercher suggestions de l’heure de la réunion en fonction de l’organisateur et le participant les contraintes de disponibilité et heure ou l’emplacement spécifiés en tant que paramètres. 

Cette opération est actuellement en mode Aperçu et disponible dans uniquement dans la version bêta. Il s’applique à uniquement Office 365 boîtes aux lettres (sur Azure AD) et non à des comptes de Microsoft.

```no-highlight
POST https://outlook.office.com/api/{version}/me/findmeetingtimes
```

Tous les paramètres pris en charge sont répertoriés ci-dessous. En fonction de votre scénario, spécifiez les paramètres nécessaires dans le corps de la demande de l’action **FindMeetingTimes** . 

|**Paramètre**|**Type de**|**Description**|**Obligatoire ?**|
|:-----|:-----|:-----|:-----|
| Participants | Collection ([AttendeeBase](complex-types-for-mail-contacts-calendar.md#AttendeeBase)) | Participants ou les ressources de la réunion. Une collection vide entraîne **FindMeetingTimes** rechercher les créneaux horaires gratuitement pour seulement l’organisateur. | Facultatif |
| LocationConstraint | [LocationConstraint](complex-types-for-mail-contacts-calendar.md#LocationConstraint) | Exigences de l’organisateur à propos de l’emplacement de la réunion, telles que si une suggestion pour un emplacement de la réunion est nécessaire, ou il y a des emplacements spécifiques uniquement où la réunion peut avoir lieu. | Facultatif |
| TimeConstraint | [TimeConstraint](complex-types-for-mail-contacts-calendar.md#TimeConstraint) | La plage de temps de début et de fin dans lequel la réunion doit avoir lieu. | Facultatif |
| MeetingDuration | Edm.Duration |La durée de la réunion, exprimée dans le format ISO 8601, des durées, par exemple, `PT1H` représente 1 heure. Si aucune durée de la réunion n’est spécifiée, **FindMeetingTimes** utilise la valeur par défaut de 30 minutes. | Facultatif |
| MaxCandidates | Edm.Int32 |Le nombre maximal de suggestions de réunion à renvoyer dans la réponse. | Facultatif |
| IsOrganizerOptional | Edm.Boolean | Spécifier `true` si l’organisateur n’a pas nécessairement d’assister à. La valeur par défaut est `false`. | Facultatif |
| ReturnSuggestionHints | Edm.Boolean | Spécifier `true` pour renvoyer une raison pour chaque suggestion de réunion dans la propriété **SuggestionHint** . La valeur par défaut est `false` pour ne pas retourner cette propriété. | Facultatif |

Selon les paramètres spécifiés, **FindMeetingTimes** vérifie l’état de disponibilité dans les calendriers principaux de l’organisateur et les participants. L’action calcule le meilleur possible aux heures de réunion et renvoie des suggestions de réunion.

**Type de réponse**

Un [MeetingTimeCandidatesResult](complex-types-for-mail-contacts-calendar.md#MeetingTimeCandidatesResult) qui inclut un ensemble de suggestions de réunion, chacune de type [MeetingTimeCandidate](#MeetingTimeCandidate)et une propriété **EmptySuggestionsHint** .

<!-- Location suggestions are based on the organizer's booking history during the past 7 days and next 2 days. If the organizer doesn't have sufficient booking history 
in the corresponding time window, the request returns HTTP 200 OK, but does not include any meeting suggestions in the response. -->

Chaque suggestion est définie comme une [MeetingTimeCandidate](complex-types-for-mail-contacts-calendar.md#MeetingTimeCandidate), avec des participants sur [la moyenne de 50 % de chance ou plus de participer à un niveau de confiance](complex-types-for-mail-contacts-calendar.md#ConfidenceScoreDetails). Par défaut, chaque heure de la réunion suggestion est renvoyée en UTC. Appliquer les `Prefer: outlook.timezone` en-tête de demande pour que les suggestions de temps retournées dans un fuseau horaire différent, par exemple de réunion :

```no-highlight
Prefer: outlook.timezone="Pacific Standard Time"
```

Si **FindMeetingTimes** ne peut pas retourner des suggestions de réunion, la réponse indique un motif dans la propriété **EmptySuggestionsHint** . En fonction de cette valeur, vous pouvez mieux ajuster les paramètres et appelez de nouveau la **FindMeetingTimes** .


**Remarque**

Actuellement, **FindMeetingTimes** suppose les conditions suivantes :

- Tout [participant](..\api\complex-types-for-mail-contacts-calendar.md#Attendee) qui est une personne (et non d’une ressource) est un participant requis. Par conséquent, spécifiez `Required` pour une personne et `Resource` pour une ressource dans la propriété de **Type** correspondante, dans le cadre de la collection parameter de **participants** .
- Toute suggestion de réunion se produit pendant les heures de travail de l’organisateur ou un participant. Vous pouvez ignorer la spécification de la propriété **ActivityDomain** d’un [TimeConstraint](..\api\complex-types-for-mail-contacts-calendar.md#TimeConstraint). 

Chaque exemple ci-dessous appelle **FindMeetingTimes**et varie selon les contraintes de disponibilité, de temps et d’emplacement participant comme décrit ci-dessous :

- [Trouver l’heure et le lieu de rencontrer participants (RESTE)](#FindTimeToMeet) 
- [Trouver le temps de répondre à un emplacement connu et obtenir une raison pour chaque suggestion (RESTE)](#FindTimeToMeetAtKnownLocation) 
- [Temps de recherche pour répondre aux mais aucun participant n’est disponible (RESTE)](#FindTimeToMeetButNobodyAvailable) 
- [Rechercher les heure de réunion, mais seulement certains participants disponibles (RESTE)](#FindTimeToMeetSomeAvailable)
- [Rechercher le temps disponible pour l’utilisateur connecté (RESTE)](#FindFreeSlots)


<a name="FindTimeToMeet"></a>

### <a name="find-time-and-location-to-meet-with-specific-attendees-rest"></a>Rechercher les temps et l’emplacement de réunions avec des participants spécifiques (RESTE)

Le temps de rechercher et atteindre en spécifiant les paramètres suivants dans le corps de la demande :
- **Participants**
- **TimeConstraint**
- **MeetingDuration**

**Exemple de requête**

L’exemple suivant indique le temps de réunion et tenant compte de l’organisateur de l’et un temps de disponibilité du participant au cours de la réunion demandée plage et la durée demandée.

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



**Exemple de réponse**

Code d’état : 200

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

### <a name="find-time-to-meet-at-a-known-location-and-get-a-reason-for-each-suggestion-rest"></a>Trouver le temps de répondre à un emplacement connu et obtenir une raison pour chaque suggestion (RESTE)

Trouver heure de réunion à un emplacement prédéterminé et demander une raison pour chaque proposition, en spécifiant les paramètres suivants dans le corps de la demande :
- **Participants**
- **LocationConstraint**
- **TimeConstraint**
- **MeetingDuration**
- **ReturnSuggestionHints**

En définissant le paramètre **ReturnSuggestionHints** , vous obtenez également une explication de chaque suggestion dans la propriété **SuggestionHint** , si **FindMeetingTimes** retourne toute suggestion.


**Exemple de requête**

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



**Exemple de réponse**

Code d’état : 200

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

### <a name="find-time-to-meet-but-no-attendee-is-available-rest"></a>Temps de recherche pour répondre aux mais aucun participant n’est disponible (RESTE)

Trouver les heure de réunion à un emplacement prédéterminé, en spécifiant les paramètres suivants dans le corps de la demande :
- **Participants**
- **LocationConstraint**
- **TimeConstraint**
- **MeetingDuration**

Dans cet exemple, en fonction des paramètres spécifiés et de la disponibilité des participants, **FindMeetingTimes** ne peut pas retourner des suggestions et retourne à la place d’un motif `AttendeesUnavailable` dans la propriété **EmptySuggestionsHint** . 

Voir les autres [raisons possibles pour des suggestions de réunion ne revient ne pas](..\api\complex-types-for-mail-contacts-calendar.md#ReasonsNoMeetingSuggestion).


**Exemple de requête**

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



**Exemple de réponse**

Code d’état : 200

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
### <a name="find-time-to-meet-but-only-some-attendees-are-available-rest"></a>Temps de recherche pour répondre aux mais uniquement certains participants sont disponible (RESTE)

Trouver les heure de réunion à un emplacement prédéterminé, en spécifiant les paramètres suivants dans le corps de la demande :
- **Participants**
- **LocationConstraint**
- **TimeConstraint**
- **MeetingDuration**
- **ReturnSuggestionHints**

Dans cet exemple, un seul des 2 participants est disponible. Chaque suggestion de réunion qui renvoie des **FindMeetingTimes** comprend :
- La disponibilité de chaque participant
- Un niveau de confiance de réunion calculée de 50 %
- Un **SuggestionHInt**, dans la mesure où le paramètre **ReturnSuggestionHints** est défini. 

Trouver plus d’informations sur la [confiance d’une réunion](..\api\complex-types-for-mail-contacts-calendar.md#ConfidenceScoreDetails).


**Exemple de requête**

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



**Exemple de réponse**

Code d’état : 200
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
###<a name="find-free-time-slots-for-just-the-signed-in-user-rest"></a>Trouver des créneaux horaires libres pour que l’utilisateur connecté (RESTE)

Trouver des créneaux horaires libres dans le calendrier principal de la signature de l’utilisateur au sein d’une plage de dates, en spécifiant les paramètres suivants dans le corps de la demande :

- **TimeConstraint**
- **MeetingDuration**

**Exemple de requête**

Cet exemple recherche les emplacements de temps libre à 1 heure, comme spécifié par **MeetingDuration**, dans le calendrier principal de la signature de l’utilisateur dans le délai spécifié par **TimeConstraint**.

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



**Exemple de réponse**

Code d’état : 200
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

Cette fonctionnalité est actuellement disponible dans uniquement dans la version bêta. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **bêta**. 

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->


[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

Cette fonctionnalité est actuellement disponible dans uniquement dans la version bêta. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **bêta**. 

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->




****

<a name="CreateEvents"> </a>
## <a name="create-events"></a>Créer des événements

L’API REST : [créer un événement de calendrier](#CreateAnEvent)

Les bibliothèques clientes : [créer un événement de calendrier (Client)](#CreateEventsClient)

<a name="CreateAnEvent"></a>
###<a name="create-a-calendar-event-rest"></a>Créer un événement de calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Créer un événement dans le calendrier principal de l’utilisateur ou d’un calendrier spécifique par validation du calendrier `events` point de terminaison. Lorsque l’événement est créé, le serveur envoie des invitations à tous les participants.

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/events
POST https://outlook.office.com/api/beta/me/calendars/{calendar_id}/events
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|

**Exemple de requête**

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

**Exemple de réponse**

Code d’état : 201

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


**Type de réponse**

Le nouvel [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource).

Par défaut, la réponse inclut toutes les propriétés du nouvel événement. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Voici un exemple d’inclure uniquement les propriétés **Start** et **End** de l’événement new dans la réponse.

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|

**Exemple de requête**

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

**Exemple de réponse**

Code d’état : 201

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


**Type de réponse**

Le nouvel [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource).

Par défaut, la réponse inclut toutes les propriétés du nouvel événement. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Voici un exemple d’inclure uniquement les propriétés **Start** et **End** de l’événement new dans la réponse.

```
POST https://outlook.office.com/api/v2.0/me/events?$Select=Start,End
```


[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->

<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]


Par défaut, les valeurs d’heure de **début** et de **fin** sont en UTC. Vous pouvez spécifier les fuseaux horaires de **début** et de **fin**, express, l’heure dans le fuseau horaire correspondant et inclure un décalage de l’heure UTC. L’exemple ci-dessous montre comment affecter les valeurs d’heure en heure du Pacifique. Notez que si vous spécifiez un fuseau horaire, vous devez spécifier une valeur pour l’autre ainsi.


```no-highlight
POST https://outlook.office.com/api/v1.0/me/events
POST https://outlook.office.com/api/v1.0/me/calendars/{calendar_id}/events
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|

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


**Type de réponse**

Le nouvel [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource).

Par défaut, la réponse inclut toutes les propriétés du nouvel événement. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. Voici un exemple d’inclure uniquement les propriétés **Start** et **End** de l’événement new dans la réponse.

```
POST https://outlook.office.com/api/v1.0/me/events?$Select=Start,End
```


[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->

****

<a name="CreateEventsClient"></a>
### <a name="create-a-calendar-event-client"></a>Créer un événement de calendrier (Client)

Créer un événement. Pour ajouter un événement à un calendrier différent, utilisez la propriété **d’événement** du calendrier de destination.

Exemple :`await client.Me.Calendars["AQMkADE3..."].Events.AddEventAsync(newEvent);`


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- CHUCK, feel free to provide client library example that reflects the event breaking changes for beta.  --> 

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->

<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient).

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


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient).

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
## <a name="update-events"></a>Événements de mise à jour

L’API REST : [mise à jour d’un événement de calendrier](#UpdateAnEvent)

Les bibliothèques clientes : [mise à jour d’un événement de calendrier (Client)](#UpdateEventsClient)

<a name="UpdateAnEvent"></a>
###<a name="update-a-calendar-event-rest"></a>Mise à jour d’un événement de calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Un événement de modification. Uniquement les propriétés que vous spécifiez sont modifiées. Si l’utilisateur est l’organisateur, le serveur envoie les mises à jour de la réunion à tous les participants.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
PATCH https://outlook.office.com/api/beta/me/events/{event_id}
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|

Spécifier des propriétés de [l’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) accessible en écriture dans le corps de la demande.

```
PATCH https://outlook.office.com/api/beta/me/events/AAMkAGE1MFKPQWAAA=?$select=Location
```

**Exemple de requête**

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

**Exemple de réponse**

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

**Type de réponse**

[L’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)de mise à jour. Si l’utilisateur est l’organisateur, le serveur envoie les mises à jour de la réunion à tous les participants.

Par défaut, la réponse inclut toutes les propriétés de l’événement de mise à jour. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. 




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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|

Spécifier des propriétés de [l’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) accessible en écriture dans le corps de la demande.

**Exemple de requête**

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

**Exemple de réponse**

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

**Type de réponse**

[L’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)de mise à jour. Si l’utilisateur est l’organisateur, le serveur envoie les mises à jour de la réunion à tous les participants.

Par défaut, la réponse inclut toutes les propriétés de l’événement de mise à jour. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. 

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|

Spécifier des propriétés de [l’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource) accessible en écriture dans le corps de la demande.

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

**Type de réponse**

[L’événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)de mise à jour. Si l’utilisateur est l’organisateur, le serveur envoie les mises à jour de la réunion à tous les participants.

Par défaut, la réponse inclut toutes les propriétés de l’événement de mise à jour. **$Select** permet de spécifier uniquement les propriétés que vous avez besoin pour optimiser les performances. La propriété **Id** est toujours renvoyée. 

```
PATCH https://outlook.office.com/api/v1.0/me/events/AAMkAGE1MFKPQWAAA=?$select=Location
```

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->






****

<a name="UpdateEventsClient"></a>
### <a name="update-a-calendar-event-client"></a>Mise à jour d’un événement de calendrier (Client)

Un événement de modification.

Vous pouvez définir plusieurs mises à jour côté client et envoyer les demandes de tous à la fois (traitement par lots les) en utilisant le modèle suivant :
1. Appelez `UpdateAsync(true)` pour chaque entité que vous souhaitez mettre à jour. Spécification de `true` enregistre les mises à jour localement sur le client, mais ne les publier sur le serveur.
2. Appelez `client.Context.SaveChangesAsync()` pour valider toutes les mises à jour sont enregistrés localement.


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


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


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient) et [a obtenu l’ID d’événement](#GetEvents).

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

Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient) et [a obtenu l’ID d’événement](#GetEvents).

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
## <a name="respond-to-events"></a>Répondre à des événements

L’API REST : [accepter, événement (RESTE)](#AcceptEvent) | [Accepter provisoirement un événement (RESTE)](#TentAcceptEvent) | [l’événement refuser (RESTE)](#DeclineEvent)

<a name="AcceptEvent"></a>
###<a name="accept-event-rest"></a>Accepter un événement (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Accepter l’événement spécifié.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/accept
```


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/beta/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/accept

Content-Type: application/json

{
  "Comment": "Great idea!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.


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


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/v2.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/accept

Content-Type: application/json

{
  "Comment": "Great idea!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.


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


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/v1.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/accept

Content-Type: application/json

{
  "Comment": "Great idea!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->





****

<a name="TentAcceptEvent"></a>
###<a name="tentatively-accept-event-rest"></a>Accepter provisoirement l’événement (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Accepter provisoirement l’événement spécifié.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/tentativelyaccept
```


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/beta/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/tentativelyaccept

Content-Type: application/json

{
  "Comment": "I'll confirm later!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.


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


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/v2.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/tentativelyaccept

Content-Type: application/json

{
  "Comment": "I'll confirm later!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.


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


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/v1.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/tentativelyaccept

Content-Type: application/json

{
  "Comment": "I'll confirm later!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


****

<a name="DeclineEvent"></a>
###<a name="decline-event-rest"></a>Événement de diminution (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Décliner l’invitation à l’événement spécifié.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]



```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/decline
```


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/beta/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/decline

Content-Type: application/json

{
  "Comment": "Sorry, maybe next time!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.


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


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/v2.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/decline

Content-Type: application/json

{
  "Comment": "Sorry, maybe next time!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.


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


|**Paramètre**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement. Obligatoire.|
|_Paramètres de corps_|
|Commentaire|string|Texte inclus dans la réponse. Facultatif.|
|SendResponse|boolean| `true`Si une réponse est envoyée à l’organisateur ; dans le cas contraire, `false`. Facultatif. Valeur par défaut est `true`.|
 
**Exemple de requête**

```
POST https://outlook.office.com/api/v1.0/me/events('AAMkAGE1M2IyNGNmLTI5MT_bs88AAAXDJwEAAA=')/decline

Content-Type: application/json

{
  "Comment": "Sorry, maybe next time!",
  "SendResponse": "true"
}
```

**Réponse**

Une réponse correcte est indiquée par un code de réponse HTTP accepté de 202.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->



****

<a name="DeleteEvents"> </a>
## <a name="delete-events"></a>Supprimer des événements

L’API REST : [Supprimer un événement de calendrier (RESTE)](#DeleteAnEvent)

Les bibliothèques clientes : [Supprimer un événement de calendrier (Client)](#DeleteEventsClient)

<a name="DeleteAnEvent"></a>
###<a name="delete-a-calendar-event-rest"></a>Supprimer un événement de calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Un événement de déplacement vers le dossier éléments supprimés de l’utilisateur connecté. Si l’événement est une réunion et que l’utilisateur connecté est l’organisateur, le serveur envoie les annulations à tous les participants.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

Cette action est différente de [l’Annuler](#CancelEvents) **Supprimer** n’est disponible pour l’organisateur et les participants de la réunion. Si l’utilisateur connecté est l’organisateur de la réunion, l’utilisateur annule simplement la réunion sans fournir un message d’annulation personnalisé aux participants.

```no-highlight
DELETE https://outlook.office.com/api/beta/me/events/{event_id}
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|


**Exemple de requête**

```
DELETE https://outlook.office.com/api/beta/me/events/AAMkAGE0M4v1OAAA=
```

**Exemple de réponse**

Code d’état : 204


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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|

**Exemple de requête**

```
DELETE https://outlook.office.com/api/v2.0/me/events/AAMkAGE0M4v1OAAA=
```

**Exemple de réponse**

Code d’état : 204



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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|

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
### <a name="delete-a-calendar-event-client"></a>Supprimer un événement de calendrier (Client)

Un événement de déplacement vers le dossier éléments supprimés.


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient) et [a obtenu l’ID d’événement](#GetEvents).

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
## <a name="cancel-events-preview"></a>Annuler les événements (aperçu)

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Cette action permet à l’organisateur d’une réunion pour envoyer un message d’annulation et d’annuler l’événement. 

L’action déplace l’événement vers le dossier éléments supprimés. L’organisateur peut également annuler une occurrence d’une réunion périodique en fournissant l’ID d’événement occurrence. Un participant à l’appel de cette action Obtient une erreur (HTTP 400 Requête incorrecte), le message d’erreur suivant :

« Impossible de traiter votre demande. Vous devez être un organisateur d’annuler une réunion. »

Cette action est différente de [Supprimer](#DeleteEvents) **Annuler** est disponible pour seulement l’organisateur et l’organisateur de vous permet d’envoyer un message personnalisé aux participants à propos de l’annulation.

```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/Cancel
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|_Paramètres de corps_|
|Commentaire|string|Un commentaire sur l’annulation envoyé à tous les participants.|

**Exemple de requête**

```
POST https://outlook.office.com/api/beta/me/events/AAMkAGE0M4v1OAAA=/Cancel

Content-Type: application/json
{
  "Comment": "Cancelling this meeting as there is a time conflict for most folks."
}
```

**Exemple de réponse**

Code d’état : 202 accepté


[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->



<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

Cette fonctionnalité est actuellement disponible dans uniquement dans la version bêta. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **bêta**. 

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->


[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

Cette fonctionnalité est actuellement disponible dans uniquement dans la version bêta. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **bêta**. 

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->


****

<a name="GetAttachments"> </a>
## <a name="get-attachments"></a>Extraire les pièces jointes

Vous pouvez obtenir une collection de pièces jointes ou recevez une pièce jointe.

L’API REST : [obtenir une collection de pièces jointes (RESTE)](#GetAttachmentCollection) | [obtenir une pièce jointe (RESTE)](#GetAttachment)

<a name="GetAttachmentCollection"> </a>
###<a name="get-an-attachment-collection-rest"></a>Obtenir une collection de pièces jointes (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Obtenir les pièces jointes à partir d’un événement particulier.

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}/attachments
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|


**Type de réponse**

Une collection de pièces jointes qui peut être de type [FileAttachment](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource), [ItemAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)ou [ReferenceAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource).


**Exemple de requête**

```
GET https://outlook.office.com/api/beta/me/events/AAMkAGI2NGTG9yAAA=/attachments
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|


**Type de réponse**

Une collection de pièces jointes qui peut être de type [FileAttachment](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource) ou [ItemAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource).


**Exemple de requête**

```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGI2NGTG9yAAA=/attachments
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|


**Type de réponse**

Une collection de pièces jointes qui peut être de type [FileAttachment](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource) ou [ItemAttachment](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource).


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
###<a name="get-an-attachment-rest"></a>Recevez une pièce jointe (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Recevez une pièce jointe à partir d’un événement particulier.

<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
GET https://outlook.office.com/api/beta/me/events/{event_id}/attachments/{attachment_id}
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|attachment_id|string|L’ID de pièce jointe.|

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


**Type de réponse**

Demandé de [pièce jointe](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource), [pièce jointe d’élément](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)ou [pièce jointe de référence](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource).


**Exemple de requête**

L’exemple suivant obtient le fichier associé à un événement spécifique.

```
GET https://outlook.office.com/api/beta/me/events/AAMkAGI2WRAAADTG9yAAA=/attachments/AAMkAGI2TG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=
```

**Exemple de réponse**

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

**Exemple de requête (référence pièce jointe)**

L’exemple suivant obtient la pièce jointe de référence d’un événement.

```
GET https://outlook.office.com/api/beta/me/events('AAMkAGE1Mbs88AADggYEcAAA=')/attachments('AAMkAGE1Mbs88AADggYEcAAABEgAQAABWAoLgP3REt_LWRG8ORv4=')
```

**Exemple de réponse**

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


**Exemple de demande ($expand sur les pièces jointes)**

L’exemple suivant obtient et développe la 2 référence pièces jointes en ligne avec les propriétés de l’événement.

```
GET https://outlook.office.com/api/beta/me/events('AAMkAGE1Mbs88AADggYEcAAA=')?$expand=attachments
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|attachment_id|string|L’ID de pièce jointe.|

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


**Type de réponse**

Le demandé de [pièce jointe](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource) ou une [pièce jointe d’élément](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource).


**Exemple de requête**

```
GET https://outlook.office.com/api/v2.0/me/events/AAMkAGI2WRAAADTG9yAAA=/attachments/AAMkAGI2TG9yAAABEgAQALxJtn1LwydGuOzcHf1FBlo=
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|attachment_id|string|L’ID de pièce jointe.|

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


**Type de réponse**

Le demandé de [pièce jointe](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource) ou une [pièce jointe d’élément](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource).


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
## <a name="create-attachments"></a>Créer des pièces jointes
Vous pouvez créer une pièce jointe ou [créer une pièce jointe d’élément](#CreateItemAttachment) pour un événement.

L’API REST : [créer une pièce jointe (RESTE)](#CreateFileAttachment) | [créer une pièce jointe d’élément (RESTE)](#CreateItemAttachment) | 
[créer une pièce jointe de référence (RESTE)](#CreateReferenceAttachment)


<a name="CreateFileAttachment"></a>
###<a name="create-a-file-attachment-rest"></a>Créer une pièce jointe (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Ajouter une pièce jointe à un événement.


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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|_Paramètres de corps_|
|@odata.type| string | #Microsoft.OutlookServices.FileAttachment |
|Nom|string|Le nom de la pièce jointe.|
|ContentBytes|fichier binaire|Le fichier à joindre.|
 
<!-- Add post GA
```REST
[!INCLUDE [calendar_api_create_file_attachment](./_data/calendar_api_create_file_attachment.json)]
``` -->

**Type de réponse**

Nouvelle [pièce jointe](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource).

****


<a name="CreateItemAttachment"></a>
###<a name="create-an-item-attachment-rest"></a>Créer une pièce jointe d’élément (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Ajouter une pièce jointe d’élément à un événement.


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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|_Paramètres de corps_|
|@odata.type| string | #Microsoft.OutlookServices.ItemAttachment |
|Nom|string|Le nom de la pièce jointe.|
|Item|Une entité [Contact](..\api\complex-types-for-mail-contacts-calendar.md#ContactResource) , [événement](..\api\complex-types-for-mail-contacts-calendar.md#EventResource)ou [Message](..\api\complex-types-for-mail-contacts-calendar.md#MessageResource).|L’élément à joindre.|
 

<!--Post GA
```REST
[!INCLUDE [calendar_api_create_item_attachment](./_data/calendar_api_create_item_attachment.json)]
``` -->


**Type de réponse**

Nouvelle [pièce jointe d’élément](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource).

****

<a name="CreateReferenceAttachment"></a>

###<a name="create-a-reference-attachment-rest"></a>Créer une pièce jointe de référence (RESTE)

<!-- ==================================== Start beta content ====================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

_**Requis étendue**: https://outlook.office.com/mail.readwrite_

Ajouter une pièce jointe de référence à un événement.

```no-highlight
POST https://outlook.office.com/api/beta/me/events/{event_id}/attachments
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|String|L’ID d’événement.|
|_Paramètres de corps_|
|@odata.type|String|```#Microsoft.OutlookServices.ReferenceAttachment```|
|Name|String|Le nom complet de la pièce jointe. Obligatoire.|
|SourceUrl|String | URL vers le contenu de la pièce jointe. S’il s’agit d’une URL vers un dossier, puis le dossier pour s’afficher correctement dans Outlook ou Outlook sur le web, la valeur **IsFolder** true. Obligatoire.|

Spécifier les paramètres de **nom** et **SourceUrl** et toutes les propriétés accessibles en écriture [référence jointe](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource) dans le corps de la demande.



**Type de réponse**

[Pièce jointe de référence](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource).


**Exemple de requête**

L’exemple suivant ajoute une pièce jointe de référence à un événement existant. La pièce jointe est un lien vers un fichier sur OneDrive pour les entreprises.

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


**Exemple de réponse**

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


**Exemple de requête**

L’exemple suivant ajoute une pièce jointe de référence dans le même appel en tant que la création d’un événement. La pièce jointe est un lien vers un fichier sur OneDrive pour les entreprises.

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


**Exemple de réponse**

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

Cette fonctionnalité est actuellement disponible dans uniquement dans la version bêta. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **bêta**.

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->


[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

Cette fonctionnalité est actuellement disponible dans uniquement dans la version bêta. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **bêta**.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->



****


<a name="DeleteAttachments"> </a>
## <a name="delete-attachments"></a>Supprimer les pièces jointes

Supprimer les pièces jointes d’un événement.

L’API REST : [Supprimer la pièce jointe de l’événement (RESTE)](#DeleteAnEventAttachment)

<a name="DeleteAnEventAttachment"></a>
###<a name="delete-an-event-attachment-rest"></a>Supprimer la pièce jointe de l’événement (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

Supprimer la pièce jointe spécifiée d’un événement. La pièce jointe peut être une [pièce jointe](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource), [pièce jointe d’élément](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource)ou une [pièce jointe de référence](..\api\complex-types-for-mail-contacts-calendar.md#ReferenceAttachmentResource).

```no-highlight
DELETE https://outlook.office.com/api/beta/me/events/{event_id}/attachments/{attachment_id}
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|attachment_id|string|L’ID de pièce jointe.|

**Exemple de requête**

```
DELETE https:/outlook.office.com/api/beta/me/events/AAMkAGE0MG4v1OAAA=/attachments/AAMkAGITG9yAAA=
```

**Exemple de réponse**

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

Supprimer la pièce jointe spécifiée d’un événement. La pièce jointe peut être un [fichier joint](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource) ou la [pièce jointe d’élément](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource).

```no-highlight
DELETE https://outlook.office.com/api/v2.0/me/events/{event_id}/attachments/{attachment_id}
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|attachment_id|string|L’ID de pièce jointe.|

**Exemple de requête**

```
DELETE https:/outlook.office.com/api/v2.0/me/events/AAMkAGE0MG4v1OAAA=/attachments/AAMkAGITG9yAAA=
```

**Exemple de réponse**

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

Supprimer la pièce jointe spécifiée d’un événement. La pièce jointe peut être un [fichier joint](..\api\complex-types-for-mail-contacts-calendar.md#FileAttachmentResource) ou la [pièce jointe d’élément](..\api\complex-types-for-mail-contacts-calendar.md#ItemAttachmentResource).

```no-highlight
DELETE https://outlook.office.com/api/v1.0/me/events/{event_id}/attachments/{attachment_id}
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|ID_événement|string|L’ID d’événement.|
|attachment_id|string|L’ID de pièce jointe.|

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
##Recevez des rappels

Obtenir une liste des rappels d’événements entre deux dates et heures dans un calendrier.

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
GET https://outlook.office.com/api/beta/me/ReminderView(StartDateTime='{DateTime}',EndDateTime='{DateTime}')
```
|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|StartDateTime|string|Date et heure de rappels retournés de départ.|
|EndDateTime|string|La date et l’heure pour les rappels retournés.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, le fuseau horaire est réglé à l’heure UTC.

[!INCLUDE [END Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

<!-- ==================================== End BETA content ====================================================== -->


<!-- ==================================== Start v2 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

```no-highlight
GET https://outlook.office.com/api/v2.0/me/ReminderView(StartDateTime='{DateTime}',EndDateTime='{DateTime}')
```
|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres d’en-tête_|
|Préférez : |Outlook.TimeZone|Le fuseau horaire par défaut pour les événements dans la réponse.|
|_Paramètres de l’URL_|
|StartDateTime|string|Date et heure de rappels retournés de départ.|
|EndDateTime|string|La date et l’heure pour les rappels retournés.|

Utilisez le _Prefer : outlook.timezone_ en-tête pour spécifier le fuseau horaire à utiliser pour le début de l’événement et la fin des heures dans la réponse. Si l’événement a été créé dans un autre fuseau horaire, les heures de début et de fin seront ajustées au fuseau horaire spécifié. Consultez [cette liste](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone) pour les noms des fuseaux horaires pris en charge. Si le _Prefer : outlook.timezone_ en-tête n’est pas spécifié, le fuseau horaire est réglé à l’heure UTC.

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ==================================== End v2 content ======================================================== -->



<!-- ==================================== Start v1 content ====================================================== -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

Cette fonctionnalité est disponible dans les seules les versions bêta et la version 2.0. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **v2.0** ou la **version bêta**.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ==================================== End v1 content ======================================================== -->


<a name="SnoozeReminders"> </a>
##Répéter les rappels

Répéter un rappel pour reporter le rappel jusqu'à une nouvelle heure.

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

<!-- ==================================== Start beta content ==================================================== -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
POST https://outlook.office.com/api/beta/me/Events('{id}')/SnoozeReminder
```

|**Paremeters requis**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|id|string|L’ID de l’événement.|
|_Paramètres de corps_|
|NewReminderTime|[DateTimeTimeZone](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)|La nouvelle date et heure pour déclencher la relance.|

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

|**Paremeters requis**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|id|string|L’ID de l’événement.|
|_Paramètres de corps_|
|NewReminderTime|[DateTimeTimeZone](..\api\complex-types-for-mail-contacts-calendar.md#DateTimeTimeZone)|La nouvelle date et heure pour déclencher la relance.|

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

Cette fonctionnalité est disponible dans les seules les versions bêta et la version 2.0. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **v2.0** ou la **version bêta**.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->

<a name="DismissReminders"> </a>
##Faire disparaître les rappels

Dissmiss un rappel qui a été déclenché.

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
POST https://outlook.office.com/api/beta/me/Events({id})/DismissReminder
```

|**Paremeters requis**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|id|string|L’ID de l’événement.|


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

|**Paremeters requis**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|id|string|L’ID de l’événement.|

[!INCLUDE [END Outlook v2 section](../includes/controls/outlookrestapiv2sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v2 content ======================================================== -->

<!-- ============================================================================================================ -->



<!-- ============================================================================================================ -->

<!-- ==================================== Start v1 content ====================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

Cette fonctionnalité est disponible dans les seules les versions bêta et la version 2.0. Pour en savoir plus, utilisez le contrôle dans le coin supérieur droit de l’article et le sélectionnez **v2.0** ou la **version bêta**.

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->


<a name="GetCalendars"> </a>
##Obtenir des calendriers

Vous pouvez obtenir une collection de calendrier ou obtenir un calendrier.

L’API REST : [obtenir une collection de calendrier (RESTE)](#GetCalendarCollection) | [obtenir un calendrier (RESTE)](#GetCalendar)

Les bibliothèques clientes : [obtenir une collection de calendrier ou d’un calendrier (Client)](#GetCalendarsClient)

<a name="GetCalendarCollection"> </a>
###<a name="get-a-calendar-collection-rest"></a>Obtenir une collection de calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Obtenir les calendriers de tous les utilisateurs (`calendars`) ou obtenir les calendriers d’un groupe spécifique de calendrier.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]



```no-highlight
GET https://outlook.office.com/api/beta/me/calendars
GET https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}/calendars
```

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#UseOdataQueryParameters) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calender_group_id|string|Le code du groupe de calendrier.|


**Exemple de requête**

```
https://outlook.office.com/api/beta/me/calendars
```

**Exemple de réponse**

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

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#UseOdataQueryParameters) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calender_group_id|string|Le code du groupe de calendrier.|

**Exemple de requête**

```
https://outlook.office.com/api/v2.0/me/calendars
```

**Exemple de réponse**

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

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#UseOdataQueryParameters) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calender_group_id|string|Le code du groupe de calendrier.|


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

**Type de réponse**

La collection demandée de [calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource) .

[!INCLUDE [END Outlook v1 section](../includes/controls/outlookrestapiv1sectionhtml)]

<!-- ============================================================================================================ -->

<!-- ==================================== End v1 content ======================================================== -->

<!-- ============================================================================================================ -->



****

<a name="GetCalendar"> </a>
###<a name="get-a-calendar-rest"></a>Obtenir un calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Obtenir un calendrier par code. Vous pouvez obtenir le calendrier principal de l’utilisateur à l’aide de la `../me/calendar` point de terminaison.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/calendars/{calendar_id}
```

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|


**Exemple de requête**

```
GET https://outlook.office.com/api/beta/me/calendars/AAMkAGI2TGuLAAA=
```

**Exemple de réponse**

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

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|


**Exemple de requête**

```
GET https://outlook.office.com/api/v2.0/me/calendars/AAMkAGI2TGuLAAA=
```

**Exemple de réponse**

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

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|


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

**Type de réponse**

Le [calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource)demandé.

****

<a name="GetCalendarsClient"> </a>
###<a name="get-a-calendar-collection-or-a-calendar-client"></a>Obtenir une collection de calendrier ou d’un calendrier (Client)

Obtenir des calendriers de l’utilisateur. Pour obtenir le calendrier par défaut de l’utilisateur, utilisez la `client.Me.Calendar` propriété shortcut. Pour obtenir un autre calendrier, spécifiez l’ID de calendrier que l’index de la collection **Calendars** , ou utilisez la méthode **GetById** .

Exemple :`client.Me.Calendars[calendarId].ExecuteAsync()`


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


**Remarque** Collections de calendrier prend en charge les expressions de requête par exemple **Sélectionner**, **OrderBy**et **prendre**.

Cet exemple appelle la méthode qui [Obtient le client Outlook](..\api\use-outlook-rest-api.md#GetClient).

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
## <a name="create-calendars"></a>Créer des calendriers

L’API REST : [Création d’un calendrier (RESTE)](#CreateACalendar)

Les bibliothèques clientes : [Création d’un calendrier (Client)](#CreateCalendarsClient)

<a name="CreateACalendar"></a>
###<a name="create-a-calendar-rest"></a>Créer un calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Créer un calendrier du groupe de calendrier par défaut à l’aide de la `../me/calendars` raccourci, ou dans un groupe particulier de calendrier par la validation du groupe `calendars` point de terminaison.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
POST https://outlook.office.com/api/beta/me/calendars
POST https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}/calendars
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calender_group_id|string|L’ID du groupe de calendrier, si vous recevez des calendriers à partir d’un groupe spécifique.|
|_Paramètres de corps_|
|Nom|string|Le nom du nouveau calendrier.|
 

**Exemple de requête**

```
POST https://outlook.office.com/api/beta/me/calendars
Content-Type: application/json

{
  "Name": "Social"
}

```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calender_group_id|string|L’ID du groupe de calendrier, si vous recevez des calendriers à partir d’un groupe spécifique.|
|_Paramètres de corps_|
|Nom|string|Le nom du nouveau calendrier.|
 

**Exemple de requête**

```
POST https://outlook.office.com/api/v2.0/me/calendars
Content-Type: application/json

{
  "Name": "Social"
}
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calender_group_id|string|L’ID du groupe de calendrier, si vous recevez des calendriers à partir d’un groupe spécifique.|
|_Paramètres de corps_|
|Nom|string|Le nom du nouveau calendrier.|
 


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



**Type de réponse**

Le nouveau [calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource).

****

<a name="CreateCalendarsClient"> </a>
### <a name="create-a-calendar-client"></a>Créer un calendrier (Client)

Créer un calendrier. Afficher les [événements de création](#CreateEventsClient) pour obtenir un exemple de création d’un événement.


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient).

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
## <a name="update-calendars"></a>Mettre à jour les calendriers

L’API REST : [mise à jour d’un calendrier (RESTE)](#UpdateACalendar)

Les bibliothèques clientes : [mettre à jour un calendrier (Client)](#UpdateCalendarsClient)

<a name="UpdateACalendar"></a>
###<a name="update-a-calendar-rest"></a>Mettre à jour un calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Modifier le nom d’un calendrier. **Name** est la propriété uniquement accessible en écriture [calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource) .


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]

```no-highlight
PATCH https://outlook.office.com/api/beta/me/calendars/{calendar_id}
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|
|_Paramètres de corps_|
|Nom|string|Le nouveau nom du calendrier.|


**Exemple de requête**

```
PATCH https://outlook.office.com/api/beta/me/calendars/AAMkAGE4xLIAAA=
Content-Type: application/json

{
  "Name": "Social events"
}
```

**Exemple de réponse**

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|
|_Paramètres de corps_|
|Nom|string|Le nouveau nom du calendrier.|


**Exemple de requête**

```
PATCH https://outlook.office.com/api/v2.0/me/calendars/AAMkAGE4xLIAAA=
Content-Type: application/json

{
  "Name": "Social events"
}
```

**Exemple de réponse**

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|
|_Paramètres de corps_|
|Nom|string|Le nouveau nom du calendrier.|

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



**Type de réponse**

Le [calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarResource)de la mise à jour.

****

<a name="UpdateCalendarsClient"> </a>
### <a name="update-a-calendar-client"></a>Mettre à jour un calendrier (Client)

Modifier le nom d’un calendrier. **Nom** est la propriété uniquement accessible en écriture pour un calendrier.


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient) et [a obtenu l’ID du calendrier](#GetCalendars).

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


Vous pouvez définir plusieurs mises à jour côté client et envoyer les demandes de tous à la fois (traitement par lots les) en utilisant le modèle suivant :
1. Appelez `UpdateAsync(true)` pour chaque entité que vous souhaitez mettre à jour. Spécification de `true` enregistre les mises à jour localement sur le client, mais ne les publier sur le serveur.
2. Appelez `client.Context.SaveChangesAsync()` pour valider toutes les mises à jour sont enregistrés localement.

****

<a name="DeleteCalendars"> </a>
## <a name="delete-calendars"></a>Supprimer des calendriers

Supprimer un calendrier.

L’API REST : [Supprimer un calendrier (RESTE)](#DeleteACalendar)

Les bibliothèques clientes : [Supprimer un calendrier (Client)](#DeleteCalendarsClient)

<a name="DeleteACalendar"></a>
###<a name="delete-a-calendar-rest"></a>Supprimer un calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]



```no-highlight
DELETE https://outlook.office.com/api/beta/me/calendars/{calendar_id}
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|


**Exemple de requête**

```
DELETE https://outlook.office.com/api/beta/me/calendars/AAMkAGE4xLIAAA=
```

**Exemple de réponse**

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|


**Exemple de requête**

```
DELETE https://outlook.office.com/api/v2.0/me/calendars/AAMkAGE4xLIAAA=
```

**Exemple de réponse**

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_id|string|Le code de calendrier.|

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
### <a name="delete-a-calendar-client"></a>Supprimer un calendrier (Client)


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient) et [a obtenu l’ID du calendrier](#GetCalendars).

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
## <a name="get-calendar-groups"></a>Obtenir les groupes de calendrier

Vous pouvez obtenir une collection de groupe de calendrier ou [d’obtenir un groupe de calendriers](#GetCalendarGroup).


**Remarque** Outlook.com prend en charge uniquement le groupe de calendrier par défaut qui est accessible par le `../me/calendars` raccourci.


L’API REST : [obtenir une collection de groupes de calendrier (RESTE)](#GetCalendarGroupCollection) | [obtenir un groupe calendrier (RESTE)](#GetCalendarGroup)

Les bibliothèques clientes : [obtenir les groupes de calendrier (Client)](#GetCalendarGroupsClient)


****


<a name="GetCalendarGroupCollection"> </a>
###<a name="get-a-calendar-group-collection-rest"></a>Obtenir une collection de groupes de calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Obtenir les groupes de calendrier dans une boîte aux lettres. 


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/calendargroups
```

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

**Exemple de requête**

```
GET https://outlook.office.com/api/beta/me/calendargroups
```

**Exemple de réponse**

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

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.

**Exemple de requête**

```
GET https://outlook.office.com/api/v2.0/me/calendargroups
```

**Exemple de réponse**

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

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


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


**Type de réponse**

La collection demandée [groupe calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource) .

****


<a name="GetCalendarGroup"> </a>
###<a name="get-a-calendar-group-rest"></a>Obtenir un groupe calendrier (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.Read_
- _WL.Calendars_
- _WL.contacts\_les calendriers_

Obtenir un groupe calendrier par code.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
GET https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}
```

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|


**Exemple de requête**

```
GET https://outlook.office.com/api/beta/me/calendargroups/AAMkAGI2TGuKAAA=
```

**Exemple de réponse**

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

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|


**Exemple de requête**

```
GET https://outlook.office.com/api/v2.0/me/calendargroups/AAMkAGI2TGuKAAA=
```

**Exemple de réponse**

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

**Remarque** Reportez-vous à la section [paramètres de la requête OData](..\api\complex-types-for-mail-contacts-calendar.md#OdataQueryParams) de filtrage, de tri et de paramètres de pagination.


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|


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


**Type de réponse**

Le [groupe du calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource)demandé.

****

<a name="GetCalendarGroupsClient"> </a>
### <a name="get-calendar-groups-client"></a>Obtenir les groupes de calendrier (Client)

Obtenir les groupes du calendrier d’un utilisateur. Pour obtenir un groupe de calendriers différents, spécifier l’ID de groupe du calendrier en tant que l’index de la collection **CalendarGroups** , ou utilisez la méthode **GetById** .

Exemple :`client.Me.CalendarGroups[calendarGroupId].ExecuteAsync()`


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


**Remarque** Collections de groupe calendrier prend en charge les expressions de requête par exemple **Sélectionner**, **OrderBy**et **prendre**.

Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient).

<!-- BEGINSECTION class="tabbedCodeSnippets" -->

```cs
IPagedCollection<ICalendarGroup> calendarGroupsResults = await client.Me.CalendarGroups.ExecuteAsync();

// Get the ID of the first calendar group
string groupId = calendarGroupsResults.CurrentPage[0].Id;
```

<!-- ENDSECTION -->

****


<a name="CreateCalendarGroups"> </a>
## <a name="create-calendar-groups"></a>Créer des groupes de calendrier

Créer un groupe de calendriers. **Nom** est la propriété uniquement accessible en écriture pour un groupe de calendriers.


**Remarque** Outlook.com prend en charge uniquement le groupe de calendrier par défaut qui est accessible par le `../me/calendars` raccourci. Vous ne pouvez pas créer un autre groupe de calendriers dans Outlook.com.


L’API REST : [créer un groupe de calendriers (RESTE)](#CreateACalendarGroup)

Les bibliothèques clientes : [créer un groupe de calendriers (Client)](#CreateCalendarGroupsClient)

<a name="CreateACalendarGroup"></a>
###<a name="create-a-calendar-group-rest"></a>Créer un groupe de calendriers (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_



<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
POST https://outlook.office.com/api/beta/me/calendargroups
```

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètre d’URL_|
|_Paramètres de corps_|
|Nom|string|Le nom du groupe de calendrier.|


**Exemple de requête**

```
POST https://outlook.office.com/api/beta/me/calendargroups
Content-Type: application/json

{
  "Name": "Birthdays"
}
```

**Exemple de réponse**

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètre d’URL_|
|_Paramètres de corps_|
|Nom|string|Le nom du groupe de calendrier.|


**Exemple de requête**

```
POST https://outlook.office.com/api/v2.0/me/calendargroups
Content-Type: application/json

{
  "Name": "Birthdays"
}
```

**Exemple de réponse**

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

|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètre d’URL_|
|_Paramètres de corps_|
|Nom|string|Le nom du groupe de calendrier.|


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


**Type de réponse**

Le nouveau [groupe de calendriers](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource).


****

<a name="CreateCalendarGroupsClient"> </a>
### <a name="create-a-calendar-group-client"></a>Créer un groupe de calendriers (Client)


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient).

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
## <a name="update-calendar-groups"></a>Mettre à jour les groupes de calendrier

L’API REST : [mise à jour d’un groupe de calendriers (RESTE)](#UpdateACalendarGroup)

Les bibliothèques clientes : [mise à jour d’un groupe de calendriers (Client)](#UpdateCalendarGroupsClient)

<a name="UpdateACalendarGroup"></a>
### <a name="update-a-calendar-group-rest"></a>Mise à jour d’un groupe de calendriers (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_

Modifier le nom d’un calendrier de groupe. **Nom** est la propriété de [groupe de calendriers](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource) de uniquement accessible en écriture.


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
PATCH https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|
|_Paramètres de corps_|
|Nom|string|Le nom du groupe de calendrier mis à jour.|


**Exemple de requête**

```
PATCH https://outlook.office.com/api/beta/me/calendargroups/AAMkAGE0M4xLGAAA=
Content-Type: application/json

{
  "Name": "Holidays"
}
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|
|_Paramètres de corps_|
|Nom|string|Le nom du groupe de calendrier mis à jour.|


**Exemple de requête**

```
PATCH https://outlook.office.com/api/v2.0/me/calendargroups/AAMkAGE0M4xLGAAA=
Content-Type: application/json

{
  "Name": "Holidays"
}
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|
|_Paramètres de corps_|
|Nom|string|Le nom du groupe de calendrier mis à jour.|


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

**Type de réponse**

La mise à jour [groupe calendrier](..\api\complex-types-for-mail-contacts-calendar.md#CalendarGroupResource).

****

<a name="UpdateCalendarGroupsClient"> </a>
### <a name="update-a-calendar-group-client"></a>Mise à jour d’un groupe de calendriers (Client)

Modifier le nom d’un calendrier de groupe. **Nom** est la propriété uniquement accessible en écriture pour un groupe de calendriers.


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient) et [a obtenu l’ID de groupe du calendrier](#GetCalendarGroups).

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


Vous pouvez définir plusieurs mises à jour côté client et envoyer les demandes de tous à la fois (traitement par lots les) en utilisant le modèle suivant :
1. Appelez `UpdateAsync(true)` pour chaque entité que vous souhaitez mettre à jour. Spécification de `true` enregistre les mises à jour localement sur le client, mais ne les publier sur le serveur.
2. Appelez `client.Context.SaveChangesAsync()` pour valider toutes les mises à jour sont enregistrés localement.


****


<a name="DeleteCalendarGroups"> </a>
## <a name="delete-calendar-groups"></a>Supprimer des groupes de calendrier

Supprimer un calendrier de groupe.


**Remarque** Outlook.com prend en charge uniquement le groupe de calendrier par défaut qui est accessible par le `../me/calendars` raccourci. Ne supprimez pas ce groupe calendrier.


L’API REST : [Supprimer un groupe de calendriers (RESTE)](#DeleteACalendarGroup)

Les bibliothèques clientes : [Supprimer un groupe de calendriers (Client)](#DeleteCalendarGroupsClient)

<a name="DeleteACalendarGroup"></a>
###<a name="delete-a-calendar-group-rest"></a>Supprimer un groupe de calendriers (RESTE)

_**Portée au minimum**: une des opérations suivantes :_
- _https://Outlook.Office.com/calendars.ReadWrite_
- _WL.Calendars\_mise à jour_
- _WL.Events\_créer_


<!-- ============================================================================================================ -->

<!-- ==================================== Start beta content ==================================================== -->

<!-- ============================================================================================================ -->

[!INCLUDE [BEGIN Outlook beta section](../includes/controls/outlookrestapibetasectionhtml)]


```no-highlight
DELETE https://outlook.office.com/api/beta/me/calendargroups/{calendar_group_id}
```


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|


**Exemple de requête**

```
DELETE https://outlook.office.com/api/beta/me/calendargroups/AAMkAGE0MGM4xLGAAA=
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|

**Exemple de requête**

```
DELETE https://outlook.office.com/api/v2.0/me/calendargroups/AAMkAGE0MGM4xLGAAA=
```

**Exemple de réponse**

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


|**Paramètre obligatoire**|**Type de**|**Description**|
|:-----|:-----|:-----|
|_Paramètres de l’URL_|
|calendar_group_id|string|Le code du groupe de calendrier.|


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
### <a name="delete-a-calendar-group-client"></a>Supprimer un groupe de calendriers (Client)


**Attention** Si vous accédez à des données de boîte aux lettres sur Outlook.com, ne pas utiliser les bibliothèques client et appeler l’API REST directement.


Cet exemple suppose que vous déjà [obtenu le client Outlook](..\api\use-outlook-rest-api.md#GetClient) et [a obtenu l’ID de groupe du calendrier](#GetCalendarGroups).

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
## <a name="next-steps"></a>Étapes suivantes

Si vous êtes prêt à commencer la conception d’une application ou que vous souhaitez simplement en savoir plus, nous avons tout prévu.


- [Mise en route avec la messagerie, de calendrier et de Contacts RESTE API](http://dev.outlook.com/RestGettingStarted).
  
- Explorez les API RESTE de Office à l’aide des [API Sandbox](http://apisandbox.msdn.microsoft.com/)interactive.
    
- Choix des exemples ? [Nous avons](..\howto\starter-projects-and-code-samples.md).
    

Ou, pour en savoir plus sur l’utilisation de la plate-forme Office 365 :

- [Outlook API REST sur le centre de développement d’Outlook](http://dev.outlook.com/RestGettingStarted/Overview)

- [Vue d’ensemble du développement sur la plate-forme Office 365](..\howto\platform-development-overview.md)
    
- [Autorisation de l’authentification et les ressources d’application Office 365](..\howto\common-app-authentication-tasks.md)
    
- [Enregistrer manuellement votre application avec AD Azure afin qu’il puisse accéder à Office 365 API](..\howto\add-common-consent-manually.md)
  
- [Référence de l’API de messagerie](..\api\mail-rest-operations.md)
  
- [Référence des API de contacts](..\api\contacts-rest-operations.md)

- [API REST de tâche (aperçu)](..\api\task-rest-operations.md)

- [API de OneDrive](https://dev.onedrive.com/)

- [Référence des opérations de Service RESTE API découverte](..\api\discovery-service-rest-operations.md)

- [Référence à une ressource pour la tâche RESTE API, calendrier, des Contacts et messagerie](..\api\complex-types-for-mail-contacts-calendar.md)



[!INCLUDE [Enable filtering functionality ](../includes/controls/enablefilteringhtml)]

