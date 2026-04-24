---
title: Adobe Advertising support for the General Data Protection Regulation
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
TQID: https://experienceleague.adobe.com/qR5H-xgBKdtWcMYfrdGdk1y5s9PEA0-hNGZADbR6TuM
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
source-wordcount: 1046
ht-degree: 0%

---

# Adobe Advertising support for the General Data Protection Regulation

*For [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; and Adobe Advertising DCO*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the General Data Protection Regulation.

The General Data Protection Regulation (GDPR), a law in effect May 25, 2018, gives all individuals (data subjects) within the borders of the European Union (EU) control of their personal data and simplifies the regulatory environment for international business. This law applies to all businesses (data controllers) that offer goods or services to, monitor the behavior of, or collect personal data from individuals within the borders of the EU at the time their personal data is processed, regardless of the data controller&#39;s business location.

Adobe CX Enterprise acts as a data processor for any personal data it receives and stores on behalf of its customers. As a data controller, you determine the personal data that Adobe CX Enterprise processes and stores on your behalf.

This document describes how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); and [!DNL Advertising DCO] support your data subjects&#39; GDPR data access and deletion rights using the Adobe Experience Platform Privacy Service API and Privacy Service UI.

For more information about what GDPR means for your business, see [GDPR and Your Business](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Supported data request types for Adobe Advertising

Adobe Experience Platform provides the ability for businesses to complete the following tasks:

* Access a data subject&#39;s cookie-level data or device ID-level data (for ads in mobile apps) within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO].
* Delete cookie-level data stored within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for data subjects using a browser; or delete ID-level data stored within [!DNL DSP] for data subjects using apps on mobile devices.
* Check the status of one or all existing requests.

## Required setup to send requests for Adobe Advertising

To make requests to access and delete data for Adobe Advertising, you must:

1. Deploy a JavaScript library to retrieve and remove your data subject cookies. The same library, `AdobePrivacy.js`, is used for all Adobe CX Enterprise solutions.

   >[!IMPORTANT]
   >
   >Les requêtes adressées à certaines solutions CX Enterprise ne nécessitent pas la bibliothèque JavaScript, mais les requêtes adressées à Adobe Advertising la requièrent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos titulaires de données peuvent soumettre des demandes d’accès et de suppression, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer les cookies [!DNL Adobe] (identifiant d’espace de noms : `gsurferID`) afin que vous puissiez envoyer ces identités dans le cadre des demandes d’accès et de suppression via l’API Adobe Experience Platform Privacy Service.

   Lorsque la personne concernée demande la suppression de données personnelles, la bibliothèque supprime également le cookie de la personne concernée du navigateur de la personne concernée.

   >[!NOTE]
   >
   >La suppression des données personnelles est différente de l’opt-out, qui arrête le ciblage d’un utilisateur final avec des segments d’audience. Cependant, lorsqu’un titulaire de données demande à supprimer des données personnelles de [!DNL Creative], [!DNL DSP] ou [!DNL DCO], la bibliothèque envoie également une demande à Adobe Advertising pour exclure le titulaire de données du ciblage de segment. Pour les annonceurs avec [!DNL Search, Social, & Commerce], nous vous recommandons de fournir aux titulaires de données un lien vers [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), qui explique comment se désabonner du ciblage des segments d’audience.

1. Identifiez votre ID d’organisation CX Enterprise et assurez-vous qu’il est lié à vos comptes Adobe Advertising.

   Un ID d’organisation CX Enterprise consiste en une chaîne alphanumérique de 24 caractères suivie de « @AdobeOrg ». Un identifiant d’organisation a été attribué à la plupart des clients CX Enterprise. Si votre équipe marketing ou votre administrateur système de [!DNL Adobe] interne ne connaît pas votre identifiant d’organisation ou ne sait pas s’il a été configuré, contactez l’assistance clientèle d’Adobe à l’adresse gdprsupport@adobe.com. Vous aurez besoin de l’ID d’organisation pour envoyer des requêtes à l’API de confidentialité à l’aide de l’espace de noms `imsOrgID`.

   >[!IMPORTANT]
   >
   >Contactez le représentant Adobe Advertising de votre société pour confirmer que tous les comptes Adobe Advertising de votre organisation, y compris les comptes [!DNL DSP] ou les annonceurs, les comptes [!DNL Search, Social, & Commerce] et les comptes [!DNL Creative] ou [!DNL DCO], sont liés à votre ID d’organisation CX Enterprise.

1. Utilisez l’API [Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (pour les requêtes automatisées) ou l’interface utilisateur [Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr) (pour les requêtes ad hoc) pour envoyer des requêtes d’accès et de suppression à Adobe Advertising au nom des titulaires de données et pour vérifier le statut des requêtes existantes.

   Pour les annonceurs qui disposent d’une application mobile afin d’interagir avec les titulaires de données et de lancer des campagnes avec DSP, vous devez télécharger les SDK mobiles compatibles avec la confidentialité pour CX Enterprise. Les SDK mobiles permettent aux contrôleurs de données de définir des indicateurs de statut d’opt-out, de récupérer l’identifiant de l’appareil du titulaire de données (identifiant de l’espace de noms : `deviceID`) et d’envoyer des requêtes à l’API Privacy Service. Votre application mobile nécessite une version de SDK 4.15.0 ou ultérieure.

   Lorsque vous soumettez la demande d’accès d’un titulaire de données, l’API Privacy Service renvoie les informations d’un titulaire de données en fonction du cookie ou de l’ID d’appareil spécifié, que vous devez ensuite renvoyer au titulaire de données.

   Lorsque vous soumettez la demande de suppression d’un titulaire de données, l’ID de cookie ou l’ID d’appareil ainsi que toutes les données de coût, de clic et de chiffre d’affaires associées au cookie sont supprimés du serveur.

   >[!NOTE]
   >
   >Si votre société dispose de plusieurs identifiants d’organisation CX Enterprise, vous devez envoyer des requêtes d’API distinctes pour chacun d’eux. Vous pouvez toutefois effectuer une requête d’API vers plusieurs sous-solutions Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] et [!DNL DCO]), avec un compte par sous-solution.

Toutes les étapes sont nécessaires pour Adobe Advertising. Pour plus d’informations sur ces tâches et d’autres tâches connexes que vous devez effectuer à l’aide de Adobe Experience Platform Privacy Service, et pour savoir où trouver les éléments nécessaires, consultez « [Présentation de Privacy Service &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) ».

## Valeurs de champ obligatoires dans les requêtes JSON Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*l’identifiant de votre organisation CX Enterprise*>

`"users":`

* `"key":` &lt;*généralement le nom du titulaire de données*>

* `"action":` `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (qui indique l’espace du cookie [!DNL adcloud])

   * `"value":` &lt;*la valeur de l’ID de cookie du titulaire de données a été récupérée à partir de`AdobePrivacy.js`*>

* `"include": **adCloud**` (qui est le produit [!DNL Adobe] qui s’applique à la requête)

* `"regulation": **gdpr**` (qui est la réglementation de confidentialité qui s’applique à la demande)

## Exemple de requête soumise par le titulaire de données à l’aide d’un identifiant utilisateur Adobe Advertising récupéré dans `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
```

## Champs de données renvoyés pour les demandes d’accès

Voici un exemple de réponse d’accès pour Adobe Advertising.

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

<!-- Changed example from BlueKai (no longer supported) to Exelate -->
