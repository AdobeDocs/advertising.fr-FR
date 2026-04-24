---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer data access and delete support
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
TQID: https://experienceleague.adobe.com/g7Klc5k3qEPYDKIbTmsQcnklUPVvbN6qqhXaHCHvn3A
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1111
ht-degree: 0%

---

# Adobe Advertising support for the California Consumer Privacy Act: Consumer data access and delete support

*For [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; and Adobe Advertising DCO*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the California Consumer Privacy Act.

The California Consumer Privacy Act (CCPA) is California’s new privacy law, which is effective January 1, 2020. CCPA provides California residents new rights regarding their personal information and imposes data protection responsibilities on certain entities who conduct business in California. CCPA provides consumers with the right to access and delete their personal information as well as the right to opt out of certain activities that qualify as “selling” personal information to a third party.

As a business, you will determine the personal data that Adobe CX Enterprise processes and stores on your behalf.

As your service provider, Adobe Advertising provides support for your business to fulfill its obligations under CCPA that are applicable to the use of Adobe Advertising products and services, including managing requests to access and delete personal information and managing requests to opt out of the sale of personal information.

This document describes how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); and [!DNL Advertising DCO] — as service providers — support consumers&#39; rights to access and delete personal information using the Adobe [!DNL Experience Platform Privacy Service API] and [!DNL Privacy Service UI].

For information about how Advertising DSP supports the consumer right to opt-out of the sale of personal information, see [Adobe Advertising support for the California Consumer Privacy Act: Consumer opt-out of sale support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

For more information about the Adobe Privacy services for CCPA, see the [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Supported data request types for Adobe Advertising

Adobe Experience Platform provides the ability for businesses to complete the following tasks:

* Access a consumer&#39;s cookie-level data or device ID-level data (for ads in mobile apps) within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO].
* Delete cookie-level data stored within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for consumers using a browser; or delete ID-level data stored within [!DNL DSP] for consumers using apps on mobile devices.
* Check the status of one or all existing requests.

## Configuration requise pour envoyer des requêtes pour Adobe Advertising

Pour envoyer des demandes d’accès et de suppression d’informations personnelles de clients à partir d’Adobe Advertising, vous devez :

1. Déployez une bibliothèque JavaScript pour récupérer et supprimer les cookies de votre client. La même bibliothèque, `AdobePrivacy.js`, est utilisée pour toutes les solutions Adobe CX Enterprise.

   >[!IMPORTANT]
   >
   >Les requêtes adressées à certaines solutions CX Enterprise ne nécessitent pas la bibliothèque JavaScript, mais les requêtes adressées à Adobe Advertising la requièrent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos clients peuvent envoyer des demandes d’accès et de suppression, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous permet de récupérer les cookies Adobe (identifiant d’espace de noms : `gsurferID`) afin que vous puissiez soumettre ces identités dans le cadre des demandes d’accès et de suppression via l’[!DNL Adobe Experience Platform Privacy Service API] .

   Lorsque le client ou la cliente demande la suppression de ses données personnelles, la bibliothèque supprime également le cookie du client ou de la cliente de son navigateur.

   >[!NOTE]
   >
   >La suppression des données personnelles est différente de la désinscription, qui arrête le ciblage d’un utilisateur final avec des segments d’audience. Cependant, lorsqu’un client demande à supprimer des données personnelles de [!DNL Creative], [!DNL DSP] ou [!DNL DCO], la bibliothèque envoie également une demande à Adobe Advertising pour exclure le client du ciblage de segment. Pour les annonceurs avec [!DNL Search, Social, & Commerce], nous vous recommandons de fournir à vos clients un lien vers [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), qui explique comment se désabonner du ciblage des segments d’audience.

1. Identifiez votre ID d’organisation CX Enterprise et assurez-vous qu’il est lié à vos comptes Adobe Advertising.

   Un ID d’organisation CX Enterprise consiste en une chaîne alphanumérique de 24 caractères suivie de « @AdobeOrg ». Un identifiant d’organisation a été attribué à la plupart des clients CX Enterprise. Si votre équipe marketing ou votre administrateur système de [!DNL Adobe] interne ne connaît pas votre identifiant d’organisation ou ne sait pas s’il a été configuré, contactez l’équipe chargée de votre compte Adobe. Vous aurez besoin de l’ID d’organisation pour envoyer des requêtes à l’API de confidentialité à l’aide de l’espace de noms `imsOrgID`.

   >[!IMPORTANT]
   >
   >Contactez le représentant Adobe Advertising de votre société pour confirmer que tous les comptes Adobe Advertising de votre organisation, y compris les comptes [!DNL DSP] ou les annonceurs, les comptes [!DNL Search, Social, & Commerce] et les comptes [!DNL Creative] ou [!DNL DCO], sont liés à votre ID d’organisation CX Enterprise.

1. Utilisez l’API [Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html?lang=fr) (pour les demandes automatisées) ou l’interface utilisateur [Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr) (pour les demandes ad hoc) pour envoyer des demandes d’accès et de suppression d’informations personnelles à Adobe Advertising au nom des consommateurs et consommatrices, et pour vérifier le statut des demandes existantes.

   Pour les annonceurs qui disposent d’une application mobile afin d’interagir avec les clients et de lancer des campagnes avec [!DNL DSP], vous devez télécharger les SDK mobiles compatibles avec la confidentialité pour CX Enterprise. Les SDK mobiles permettent aux entreprises de définir des indicateurs de statut d’opt-out, de récupérer l’identifiant de l’appareil du client (identifiant de l’espace de noms : `deviceID`) et d’envoyer des requêtes à l’API Privacy Service. Votre application mobile nécessite une version de SDK 4.15.0 ou ultérieure.

   Lorsque vous soumettez une demande d’accès aux clients, l’API Privacy Service renvoie les informations d’un client en fonction du cookie ou de l’ID d’appareil spécifié, que vous devez ensuite renvoyer au client.

   Lorsque vous soumettez une requête de suppression de consommateurs, l’ID de cookie ou l’ID d’appareil ainsi que toutes les données de coût, de clic et de chiffre d’affaires associées au cookie sont supprimées du serveur.

   >[!NOTE]
   >
   >Si votre entreprise dispose de plusieurs identifiants d’organisation CX Enterprise, vous devez envoyer des requêtes d’API distinctes pour chacun d’eux. Vous pouvez toutefois effectuer une requête d’API vers plusieurs sous-solutions Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] et [!DNL DCO]), avec un compte par sous-solution.

All steps are necessary to receive support from Adobe Advertising. Pour plus d&#39;informations sur ces tâches et d&#39;autres tâches connexes que vous devez effectuer à l&#39;aide du Adobe Experience Platform Privacy Service, et pour savoir où trouver les éléments nécessaires, consultez [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=fr](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=fr).

## Valeurs de champ obligatoires dans les requêtes JSON Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*l’identifiant de votre organisation CX Enterprise*>

&quot;users&quot;:

* `"key":` &lt;*usually the name of the customer*>

* `"action":` `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (which indicates the [[!DNL AdCloud] cookie space](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/api/appendix))

   * `"value":` &lt;*the actual customer’s cookie ID value as retrieved from`AdobePrivacy.js`*>

* `"include": **adCloud**` (which is the [[!DNL Adobe] product](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/api/appendix) that applies to the request)

* `"regulation": **ccpa**` (qui est la réglementation de confidentialité qui s’applique à la demande)

## Example of request submitted by a consumer using an Adobe Advertising user ID retrieved from AdobePrivacy.js

```
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
```

## Champs de données renvoyés pour les demandes d’accès

The following is an example of a personal information access response for Adobe Advertising.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
