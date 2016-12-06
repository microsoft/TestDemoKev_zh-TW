MS. TocTitle : Les demandes de lot Outlook RESTE (aperçu) titre : RESTE de Outlook envoyer des demandes de lots (aperçu) Description : comment lot RESTE plusieurs demandes ensemble pour former une requête HTTP unique et réduire la charge des connexions multiples à HTTP. MS. ContentId : a842854e-46b3-47d9-8899-c27b481f4e78 <<<<<<< ms.topic de TÊTE : ms.date de référence (API) : 16 mai 2016, =======
ms.date : 13 septembre 2016
>>>>>>> la zone de transit

[!INCLUDE [Add the O365API repo styles](../includes/controls/addo365apistyles.html)]

# <a name="send-outlook-rest-requests-in-batches-preview"></a>Envoyer les demandes Outlook RESTE par lots (aperçu)

[!INCLUDE [Add the Outlook REST API filters--beta default v1 v2 disabled](../includes/controls/addOutlookversion_betadefault_v1v2disabled.html)]    


 _**S’applique à :** Exchange Online | Office 365 | Hotmail.com | Live.com | MSN.com | Outlook.com | Passport.com_

<p class="previewnote">Cette documentation traite l’envoi de plusieurs demandes d’Outlook RESTE sous la forme d’une requête de lot unique qui est actuellement en mode Aperçu. Aperçu des fonctionnalités peuvent être modifiées avant la finalisation et peuvent endommager le code qui les utilise. De ce fait, en général vous devez utiliser une version de production d’une API dans votre code de production. Le cas échéant, v2.0 est actuellement la version par défaut.</p>

Le traitement par lots vous permet de placer plusieurs demandes Outlook RESTE dans une seule demande de traitement par lots HTTP, réduisant le nombre de connexions HTTP et les frais généraux. Les demandes dans un lot d’accéder aux données de l’utilisateur connecté, sécurisé par Azure Active Directory dans Office 365, ou dans un compte Microsoft (Hotmail.com, Live.com, MSN.com, Outlook.com ou Passport.com). 


**Remarque** Pour plus de simplicité de référence, le reste de cet article utilise **« Outlook.com » pour inclure ces domaines de compte Microsoft**. 

## <a name="overview"></a>Vue d’ensemble

Une demande RESTE requiert une connexion HTTP entre le client et le serveur, ce qui entraîne une certaine surcharge. Le traitement par lots vous permet de réduire les frais de connexion en associant plusieurs appels de l’API REST dans une requête HTTP POST au point de terminaison $batch :  
```
POST https://outlook.office.com/api/{version}/$batch
```
Une demande de traitement par lots peut inclure jusqu'à 20 appels API REST individuelles, qui peuvent être des requêtes de données (par exemple, GET) ou modifier (par exemple POST) opérations. Vous pouvez spécifier un en-tête [Prefer](#PreferContinueOnError) pour que le traitement par lots à continuer même lors de l’échouent d’un ou plusieurs appels de RESTE.

Le traitement par lots est particulièrement utile lors de la synchronisation de grandes quantités de données. Appels d’API dans le même lot peuvent accéder aux différentes ressources, telles que les messages et les événements, qui appartiennent à la même boîte aux lettres de l’utilisateur connecté. 

Si vous avez besoin de plus de 20 appels, ou si l’ordre de lancement d’appels est important, utilisez plusieurs requêtes de lots.


## <a name="example"></a>Exemple

Un exemple simple de meilleur illustre le traitement par lots. La requête de lots suivant place 2 appels de l’API REST de Outlook dans un seul lot :
1. OBTENIR tous les événements de l’utilisateur connecté
2. ENVOYER un message.

### <a name="batch-request"></a>Demande de traitement par lots

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

### <a name="batch-response"></a>Réponse par lot

La réponse par lot inclut des codes de réponse distincts et des organismes, le cas échéant, pour la requête de lots et appels individuels. 

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

## <a name="batch-details"></a>Détails de lot

### <a name="endpoint-url"></a>URL du point de terminaison

Pour envoyer un lot de plusieurs demandes d’Outlook RESTE, effectuez une PUBLICATION sur le point de terminaison $batch :
```
POST https://outlook.office.com/api/{version}/$batch HTTP/1.1
```

**Attention**  Lorsque vous utilisez la https://outlook.office.com URL racine, pour des performances optimales, ajouter un en-tête **x-AnchorMailbox** et lui affecter une adresse de messagerie de l’utilisateur. En outre, gérer le cas où la boîte aux lettres de l’utilisateur d’un Outlook.com n'a pas encore été activée pour l’API REST de Outlook - vérifier les codes d’erreur MailboxNotEnabledForRESTAPI et MailboxNotSupportedForRESTAPI. En savoir plus [ici](..\api\use-outlook-rest-api.md#OutlookRESTCaution). 

**Notes pour les développeurs en Chine** 

- Si vous développez des applications _pour Office 365_ en Chine, vous devez continuer à utiliser les [points de terminaison API d’Office 365 pour la Chine](..\api\o365-china-endpoints.md).

- Si vous créez des applications _pour Outlook.com_ en Chine, vous devez utiliser l' [Aperçu de modèle v2 app](..\api\use-outlook-rest-api.md#RegAuthConverged)et le point de terminaison Outlook RESTE suivant :`https://outlook.office.com/api/{version}`


###<a name="version-of-api"></a>Version de l’API

Le traitement par lots en cours d’aperçu et est uniquement disponible dans l’espace de noms bêta, vous devez spécifier `{version}` en tant que `beta`:

`https://outlook.office.com/api/beta/$batch`

Dans la mesure où une demande de traitement par lots et les AUTRES appels dans le traitement par lots doit utiliser le même hôte et la même version de l’API, vous pouvez de lot actuellement que des appels Outlook RESTE exposées dans la version bêta. 

**Attention** Notez que certains appels API que vous pouvez inclure dans un lot de répondent différemment dans la version bêta que dans les versions pour une disponibilité générale, telles que la version 2.0 et la version 1.0. En général, si vous décidez d’utiliser des appels API dans l’état de l’aperçu dans la version bêta, planifier sur la vérification des fonctionnalités dans votre application et la prise en compte des modifications avec rupture possibles.
 

###<a name="target-user"></a>Utilisateur cible

Vous pouvez regrouper les appels API REST de Outlook pour la même boîte aux lettres de l’utilisateur connecté dans un lot. La boîte aux lettres peut être sur Office 365 ou Outlook.com.

### <a name="authentication"></a>Authentification

Similaire à l’envoi d’appels de [l’API REST de Outlook](..\api\use-outlook-rest-api.md#DefineOutlookRESTAPI) comme des requêtes individuelles, vous devez inclure un jeton d’accès valide dans un en-tête de demande **d’autorisation** . Si vous spécifiez cet en-tête pour la requête de lots, le jeton d’accès doit fournir l’autorisation nécessaire pour tous les appels dans ce lot. Vous pouvez éventuellement spécifier un jeton d’accès pour un appel spécifique dans le lot si cet appel requiert un jeton d’accès différents.
 
L’obtention d’un jeton d’accès nécessite que vous avez enregistré identifié votre application et obtenu l’autorisation appropriée. [En savoir plus](..\api\use-outlook-rest-api.md#ShortRegAuthWorkflow) sur certains rationalisée des options d’enregistrement et d’autorisation pour vous. Gardez à l’esprit que vous plus d’informations sur le traitement par lots des demandes.

### <a name="batch-request-headers"></a>En-têtes de demande de traitement par lots

Inclure les en-têtes suivants pour chaque demande de traitement par lots :

```
Host: outlook.office.com
Content-Type: multipart/mixed; boundary=batch_<batchId> 
```

où `{batchId}` identifie un lot et est utilisé pour délimiter les demandes dans le lot. Il peut être un GUID ou n’importe quelle chaîne distinctif.

Vous pouvez inclure les autres en-têtes le cas échéant. À l’exception des en-têtes liés au contenu comme **Type de contenu**, les en-têtes de la requête de lots s’appliquent généralement à chaque opération dans le lot. Si vous spécifiez un en-tête dans la demande de traitement par lots et une opération spécifique dans le lot, ce dernier est prioritaire et s’applique à cette opération.   


### <a name="batch-request-body"></a>Corps de demande de traitement par lots

Démarrez chaque opération au sein d’un lot avec les lignes suivantes :
```
--batch_{batchId} 
Content-Type: application/http 
Content-Transfer-Encoding: binary 
```
Fin de la dernière opération du lot à cela :
```
--batch_{batchId}--
```


### <a name="operations-in-a-batch"></a>Opérations d’un lot
Vous pouvez spécifier jusqu'à 20 opérations dans une requête de lots.

Une opération d’un lot peut être une requête de données, une modification, une action ou une demande d’appel de fonction. Alors que vous n’êtes pas obligé de répéter URL complètes et l’état de tous les en-têtes pour chaque opération dans le lot, veillez à inclure des en-têtes spécifiques et de corps de requête s’ils sont requis pour une opération.

### <a name="relative-urls-within-a-batch"></a>URL relatives au sein d’un lot
Comme alternative à la spécification d’une URL complète pour une opération, vous pouvez inclure une URL relative. Par exemple, la requête GET dans l’exemple ci-dessous spécifie une URL `/api/beta/me/events` par rapport à l’hôte spécifié dans la requête de lots, `https://outlook.office.com`.

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

### <a name="processing-a-batch-request"></a>Traitement d’une demande de traitement par lots
Une requête de lots est traitée comme une demande et renvoie son propre code de réponse. Une demande de lot correct avec en-têtes corrects renvoie HTTP 200 OK. Cela ne toutefois signifie que toutes les requêtes dans le lot ont réussi. Chaque requête dans le corps de la demande de traitement par lots est traitée à son tour séparément et renvoie son propre code de réponse et tout message d’erreur et les corps de réponse.

Le serveur peut exécuter des opérations au sein d’un lot dans n’importe quel ordre. Si vous devez avoir des opérations effectuées dans un ordre spécifique, vous ne devez pas les placer dans la même demande de traitement par lots. Au lieu de cela, envoyez une seule opération par lui-même, attendre la réponse avant l’envoi suivant.

<a name="PreferContinueOnError"></a>

Par défaut, le traitement s’arrête à la première opération qui renvoie une erreur. Vous pouvez spécifier l’en-tête suivant pour ignorer l’erreur et poursuivre l’opération suivante dans le lot de traitement :

```
Prefer: odata.continue-on-error
```



<a name="NextSteps"> </a>
## <a name="next-steps"></a>Étapes suivantes

Si vous êtes prêt à commencer la conception d’une application ou que vous souhaitez simplement en savoir plus, nous avons tout prévu.

- [Mise en route avec la messagerie, de calendrier et de Contacts RESTE API](http://dev.outlook.com/RestGettingStarted).

- Explorez les API d’Office 365 à l’aide des [API Sandbox](https://apisandbox.msdn.microsoft.com/)interactive.

- Choix des exemples ? [Nous avons](..\howto\starter-projects-and-code-samples.md).


Ou, pour en savoir plus sur l’utilisation de la plate-forme Office 365 :

- [Outlook API REST sur le centre de développement d’Outlook](http://dev.outlook.com/RestGettingStarted/Overview)

- [Vue d’ensemble du développement sur la plate-forme Office 365](..\howto\platform-development-overview.md)

- [Autorisation de l’authentification et les ressources d’application Office 365](..\howto\common-app-authentication-tasks.md)

- [Enregistrer manuellement votre application avec AD Azure afin qu’il puisse accéder à Office 365 API](..\howto\add-common-consent-manually.md)

- [Référence des API de messagerie RESTE](..\api\mail-rest-operations.md)

- [Référence des API du RESTE de calendrier](..\api\calendar-rest-operations.md)

- [Référence des API du RESTE des contacts](..\api\contacts-rest-operations.md)

- [API REST de tâche (aperçu)](..\api\task-rest-operations.md) 

- [Référence à une ressource pour la tâche RESTE API, calendrier, des Contacts et messagerie](..\api\complex-types-for-mail-contacts-calendar.md)

- [Référence des API de données Extensions RESTE de Office 365](..\api\extensions-rest-operations.md)

- [Référence de l’API d’AUTRES personnes](..\api\people-rest-operations.md)

- [Référence des API REST de notifications](..\api\notify-rest-operations.md)

- [Référence API REST de Photo de l’utilisateur](..\api\photo-rest-operations.md)

[!INCLUDE [Enable filtering functionality ](../includes/controls/enablefiltering.html)]
