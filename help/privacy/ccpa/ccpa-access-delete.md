---
title: Prise en charge d’Adobe Advertising pour la Loi sur la confidentialité des consommateurs de Californie &#58; Prise en charge de l’accès et de la suppression des données client
description: Découvrez les types de demandes de données pris en charge, la configuration et les valeurs de champ requises, ainsi que des exemples de demandes d’accès aux API à l’aide des identifiants de produit hérités et des champs de données renvoyés.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# Prise en charge d’Adobe Advertising pour la Loi sur la confidentialité des consommateurs de Californie : assistance pour l’accès et la suppression des données client

*Par [!DNL Adobe Advertising Search, Social, & Commerce] ; Adobe Advertising DSP ; Adobe Advertising Creative ; et Adobe Advertising DCO*

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à en remplacer un. Consultez votre service juridique pour obtenir des conseils concernant la Loi sur la protection des renseignements personnels des consommateurs de Californie.

Le California Consumer Privacy Act (CCPA) est la nouvelle loi californienne sur la protection de la vie privée, qui entre en vigueur le 1er janvier 2020. Le CCPA offre aux Californiens de nouveaux droits sur leurs informations personnelles et impose des responsabilités en matière de protection des données à certaines entités qui exercent des activités en Californie. Le CCPA offre aux consommateurs le droit d’accéder à leurs informations personnelles et de les supprimer, ainsi que le droit de se désinscrire de certaines activités qualifiées de « vente » d’informations personnelles à un tiers.

En tant qu’entreprise, vous déterminerez les données personnelles que Adobe Experience Cloud traite et stocke pour vous.

En tant que fournisseur, Adobe Advertising fournit une assistance à votre entreprise afin qu’elle remplisse ses obligations en vertu du CCPA qui s’appliquent à l’utilisation des produits et services Adobe Advertising, y compris la gestion des demandes d’accès et de suppression des informations personnelles et la gestion des demandes de refus de la vente des informations personnelles.

Ce document décrit comment [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) et [!DNL Advertising DCO], en tant que fournisseurs de services, prennent en charge les droits des consommateurs d’accéder et de supprimer des informations personnelles à l’aide des [!DNL Experience Platform Privacy Service API] et [!DNL Privacy Service UI] d’Adobe.

Pour plus d’informations sur la manière dont Advertising DSP prend en charge le droit des consommateurs de se désinscrire de la vente de leurs informations personnelles, consultez [Prise en charge d’Adobe Advertising en vertu de la Loi sur la protection des informations personnelles des consommateurs de Californie : Prise en charge du droit de désinscription des consommateurs](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Pour plus d’informations sur Adobe Privacy Services pour le CCPA, consultez le [Centre de traitement des données personnelles d’Adobe](https://www.adobe.com/privacy/ccpa.html).

## Types de requêtes de données pris en charge pour Adobe Advertising

Adobe Experience Platform permet aux entreprises d’effectuer les tâches suivantes :

* Accédez aux données au niveau des cookies ou des identifiants d’appareil d’un client (pour les annonces dans les applications mobiles) dans [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] ou [!DNL DCO].
* Supprimez les données au niveau des cookies stockées dans [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] ou [!DNL DCO] pour les clients qui utilisent un navigateur ou supprimez les données au niveau des identifiants stockées dans [!DNL DSP] pour les clients qui utilisent des applications sur des appareils mobiles.
* Vérifiez le statut d’une ou de toutes les requêtes existantes.

## Configuration requise pour envoyer des demandes pour Adobe Advertising

Pour envoyer des demandes d’accès et de suppression d’informations personnelles de clients à partir d’Adobe Advertising, vous devez :

1. Déployez une bibliothèque JavaScript pour récupérer et supprimer les cookies de votre client. La même bibliothèque, `AdobePrivacy.js`, est utilisée pour toutes les solutions Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Les requêtes adressées à certaines solutions Experience Cloud ne nécessitent pas la bibliothèque JavaScript, mais les requêtes adressées à Adobe Advertising la requièrent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos clients peuvent envoyer des demandes d’accès et de suppression, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous permet de récupérer les cookies Adobe (identifiant d’espace de noms : `gsurferID`) afin que vous puissiez soumettre ces identités dans le cadre des demandes d’accès et de suppression via l’[!DNL Adobe Experience Platform Privacy Service API] .

   Lorsque le client ou la cliente demande la suppression de ses données personnelles, la bibliothèque supprime également le cookie du client ou de la cliente de son navigateur.

   >[!NOTE]
   >
   >La suppression des données personnelles est différente de la désinscription, qui arrête le ciblage d’un utilisateur final avec des segments d’audience. Cependant, lorsqu’un client demande à supprimer des données personnelles de [!DNL Creative], [!DNL DSP] ou [!DNL DCO], la bibliothèque envoie également une demande à Adobe Advertising pour exclure le client du ciblage de segment. Pour les annonceurs avec [!DNL Search, Social, & Commerce], nous vous recommandons de fournir à vos clients un lien vers [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), qui explique comment se désabonner du ciblage des segments d’audience.

1. Identifiez votre ID d’organisation Experience Cloud et assurez-vous qu’il est lié à vos comptes Adobe Advertising.

   Un ID d’organisation Experience Cloud consiste en une chaîne alphanumérique de 24 caractères suivie de « @AdobeOrg ». Un identifiant d’organisation a été attribué à la plupart des clients Experience Cloud. Si votre équipe marketing ou votre administrateur système de [!DNL Adobe] interne ne connaît pas votre identifiant d’organisation ou ne sait pas s’il a été configuré, contactez l’équipe chargée de votre compte Adobe. Vous aurez besoin de l’ID d’organisation pour envoyer des requêtes à l’API de confidentialité à l’aide de l’espace de noms `imsOrgID`.

   >[!IMPORTANT]
   >
   >Contactez le représentant Adobe Advertising de votre société pour confirmer que tous les comptes Adobe Advertising de votre organisation, y compris les comptes [!DNL DSP] ou les annonceurs, les comptes [!DNL Search, Social, & Commerce] et les comptes [!DNL Creative] ou [!DNL DCO], sont liés à votre ID d’organisation Experience Cloud.

1. Utilisez l’API [Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (pour les demandes automatisées) ou l’interface utilisateur [Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr) (pour les demandes ad hoc) pour envoyer des demandes d’accès et de suppression d’informations personnelles à Adobe Advertising au nom des consommateurs et consommatrices, et pour vérifier le statut des demandes existantes.

   Pour les annonceurs qui disposent d’une application mobile afin d’interagir avec les clients et de lancer des campagnes avec [!DNL DSP], vous devez télécharger les SDK mobiles compatibles avec les informations personnelles pour Experience Cloud. Les SDK mobiles permettent aux entreprises de définir des indicateurs de statut d’opt-out, de récupérer l’identifiant de l’appareil du client (identifiant de l’espace de noms : `deviceID`) et d’envoyer des requêtes à l’API Privacy Service. Votre application mobile nécessite une version de SDK 4.15.0 ou ultérieure.

   Lorsque vous soumettez une demande d’accès aux clients, l’API Privacy Service renvoie les informations d’un client en fonction du cookie ou de l’ID d’appareil spécifié, que vous devez ensuite renvoyer au client.

   Lorsque vous soumettez une requête de suppression de consommateurs, l’ID de cookie ou l’ID d’appareil ainsi que toutes les données de coût, de clic et de chiffre d’affaires associées au cookie sont supprimées du serveur.

   >[!NOTE]
   >
   >Si votre entreprise dispose de plusieurs identifiants d’organisation Experience Cloud, vous devez envoyer des requêtes d’API distinctes pour chacun d’eux. Vous pouvez toutefois effectuer une requête d’API vers plusieurs sous-solutions Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] et [!DNL DCO]), avec un compte par sous-solution.

Toutes les étapes sont nécessaires pour recevoir une assistance d’Adobe Advertising. Pour plus d&#39;informations sur ces tâches et d&#39;autres tâches connexes que vous devez effectuer à l&#39;aide du Adobe Experience Platform Privacy Service, et pour savoir où trouver les éléments nécessaires, consultez [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valeurs de champ requises dans les requêtes JSON Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*l’identifiant de votre organisation Experience Cloud*>

« users »:

* `"key":` &lt;*généralement le nom du client*>

* `"action":` `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (qui indique l’espace du cookie [!DNL adCloud])

   * `"value":` &lt;*la valeur de l’ID de cookie du client réel, extraite de`AdobePrivacy.js`*>

* `"include": **adCloud**` (qui est le produit [!DNL Adobe] qui s’applique à la requête)

* `"regulation": **ccpa**` (qui est la réglementation de confidentialité qui s’applique à la demande)

## Exemple de demande envoyée par un client à l’aide d’un identifiant utilisateur Adobe Advertising récupéré d’AdobePrivacy.js

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

Voici un exemple de réponse d’accès aux informations personnelles pour Adobe Advertising.

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
