---
title: Prise en charge des Adobes Advertising par le Règlement général sur la protection des données
description: Découvrez les types de requêtes de données pris en charge, les valeurs de configuration et de champ requises, ainsi que des exemples de requêtes d’accès aux API utilisant des ID de produit hérités et des champs de données renvoyés.
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# Prise en charge des Adobes Advertising par le Règlement général sur la protection des données

*Pour [!DNL Adobe Advertising Search, Social, & Commerce] ; Adobe Advertising DSP ; Adobe Advertising Creative ; et Adobe Advertising DCO*

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à remplacer un avis juridique. Consultez votre service juridique pour obtenir des conseils concernant le Règlement général sur la protection des données.

Le Règlement général sur la protection des données (RGPD), qui est entré en vigueur le 25 mai 2018, donne à tous les individus (personnes concernées) à l’intérieur des frontières de l’Union européenne (UE) le contrôle de leurs données personnelles et simplifie l’environnement réglementaire pour les affaires internationales. Cette loi s’applique à toutes les entreprises (contrôleurs de données) qui offrent des biens ou des services pour, surveiller le comportement ou collecter des données personnelles de personnes à l’intérieur des frontières de l’UE au moment du traitement de leurs données personnelles, quel que soit le lieu d’activité du contrôleur de données.

Adobe Experience Cloud agit en tant qu’entité de traitement des données pour toutes les données personnelles qu’il reçoit et stocke pour le compte de ses clients. En tant que contrôleur des données, vous déterminez les données personnelles qu’Adobe Experience Cloud traite et stocke pour vous.

Ce document décrit comment [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) et [!DNL Advertising DCO] prennent en charge les droits d’accès et de suppression des données des titulaires de données en vertu du RGPD à l’aide de l’API Adobe Experience Platform Privacy Service et de l’interface utilisateur du Privacy Service.

Pour plus d’informations sur ce que le RGPD signifie pour votre entreprise, voir [RGPD et votre entreprise](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Types de requête de données pris en charge pour Adobe Advertising

Adobe Experience Platform permet aux entreprises d’effectuer les tâches suivantes :

* Accédez aux données au niveau du cookie d’un sujet de données ou aux données au niveau de l’identifiant de l’appareil (pour les publicités dans les applications mobiles) dans [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] ou [!DNL DCO].
* Supprimez les données au niveau du cookie stockées dans [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] ou [!DNL DCO] pour les sujets des données utilisant un navigateur ou supprimez les données au niveau de l’ID stockées dans [!DNL DSP] pour les sujets des données utilisant des applications sur des périphériques mobiles.
* Vérifiez l’état d’une ou de toutes les requêtes existantes.

## Configuration requise pour envoyer des demandes d’Adobe Advertising

Pour envoyer des demandes d’accès et de suppression de données pour Adobe Advertising, vous devez :

1. Déployez une bibliothèque JavaScript pour récupérer et supprimer vos cookies de sujet de données. La même bibliothèque, `AdobePrivacy.js`, est utilisée pour toutes les solutions Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Les demandes à certaines solutions Experience Cloud ne nécessitent pas la bibliothèque JavaScript, mais les demandes d’Adobe Advertising en ont besoin.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos sujets des données peuvent envoyer des requêtes d’accès et de suppression, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer [!DNL Adobe] cookies (ID d’espace de noms : `gsurferID`) afin que vous puissiez envoyer ces identités dans le cadre de demandes d’accès et de suppression via l’API Adobe Experience Platform Privacy Service.

   Lorsque le sujet des données demande la suppression de données personnelles, la bibliothèque supprime également le cookie du sujet des données du navigateur du sujet des données.

   >[!NOTE]
   >
   >La suppression des données personnelles est différente de l’exclusion, qui arrête le ciblage d’un utilisateur final avec des segments d’audience. Cependant, lorsqu’un sujet de données demande de supprimer des données personnelles de [!DNL Creative], [!DNL DSP] ou [!DNL DCO], la bibliothèque envoie également une demande à l’Adobe Advertising pour exclure le sujet de données du ciblage de segments. Pour les annonceurs disposant de [!DNL Search, Social, & Commerce], nous vous recommandons de fournir aux sujets des données un lien vers [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), qui explique comment exclure le ciblage des segments ciblés.

1. Identifiez l’ID d’organisation de votre Experience Cloud et assurez-vous qu’il est lié à vos comptes d’Adobe Advertising.

   Un ID d’organisation Experience Cloud est une chaîne alphanumérique de 24 caractères accompagnée de &quot;@AdobeOrg&quot;. Un ID d’organisation a été attribué à la plupart des clients Experience Cloud. Si votre équipe marketing ou votre administrateur système interne [!DNL Adobe] ne connaît pas votre ID d’organisation ou n’est pas certain qu’il a été configuré, contactez l’Assistance clientèle d’Adobe à l’adresse gdprsupport@adobe.com. Vous aurez besoin de l’ID d’organisation pour envoyer des demandes à l’API de confidentialité à l’aide de l’espace de noms `imsOrgID`.

   >[!IMPORTANT]
   >
   >Contactez le représentant de l’Adobe Advertising de votre entreprise pour confirmer que tous les comptes d’Adobe Advertising de votre entreprise — y compris les comptes [!DNL DSP] ou les annonceurs, les comptes [!DNL Search, Social, & Commerce] et les comptes [!DNL Creative] ou [!DNL DCO] — sont liés à l’ID d’organisation de votre Experience Cloud.

1. Utilisez l’ [API Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (pour les requêtes automatisées) ou l’ [ interface utilisateur du Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr) (pour les requêtes ad hoc) pour envoyer des requêtes d’accès et de suppression à l’Adobe Advertising pour le compte des sujets des données, et pour vérifier l’état des requêtes existantes.

   Pour les annonceurs qui disposent d’une application mobile afin d’interagir avec les sujets des données et de lancer des campagnes avec DSP, vous devez télécharger les SDK mobiles prêts pour la confidentialité pour Experience Cloud. Les SDK mobiles permettent aux contrôleurs de données de définir des indicateurs d’état d’exclusion, de récupérer l’identifiant de l’appareil du sujet de données (ID d’espace de noms : `deviceID`) et d’envoyer des requêtes à l’API du Privacy Service. Votre application mobile requiert un SDK version 4.15.0 ou supérieure.

   Lorsque vous soumettez une demande d’accès d’un sujet de données, l’API du Privacy Service renvoie les informations d’un sujet de données en fonction du cookie spécifié ou de l’ID d’appareil, que vous devez ensuite renvoyer au sujet de données.

   Lorsque vous soumettez une demande de suppression d’un sujet de données, l’ID de cookie ou l’ID d’appareil, ainsi que toutes les données sur les coûts, les clics et les recettes associés au cookie, sont supprimés du serveur.

   >[!NOTE]
   >
   >Si votre société dispose de plusieurs ID d’organisation Experience Cloud, vous devez envoyer des demandes d’API distinctes pour chacun d’eux. Vous pouvez toutefois effectuer une requête d’API sur plusieurs sous-solutions d’Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] et [!DNL DCO]), avec un compte par sous-solution.

Toutes ces étapes sont nécessaires à l&#39;Adobe Advertising. Pour plus d’informations à ce sujet et sur d’autres tâches connexes que vous devez effectuer à l’aide de Adobe Experience Platform Privacy Service, et où trouver les éléments nécessaires, voir &quot;[Présentation du Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)&quot;.

## Valeurs de champ requises dans les demandes JSON d’Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*ID de votre organisation Experience Cloud*>

`"users":`

* `"key":` &lt;*généralement le nom du sujet de données*>

* `"action":` `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (qui indique l’espace de cookie [!DNL adcloud])

   * `"value":` &lt;*la valeur de l’ID de cookie du sujet de données réel telle qu’elle est extraite de`AdobePrivacy.js`*>

* `"include": **adCloud**` (qui est le produit [!DNL Adobe] qui s’applique à la requête)

* `"regulation": **gdpr**` (qui est la réglementation sur la confidentialité qui s’applique à la demande)

## Exemple de demande envoyée par le titulaire de données à l’aide d’un identifiant utilisateur Adobe Advertising récupéré de `AdobePrivacy.js`

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
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
