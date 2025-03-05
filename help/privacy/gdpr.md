---
title: Prise en charge du Règlement général sur la protection des données par Adobe Advertising
description: Découvrez les types de demandes de données pris en charge, la configuration et les valeurs de champ requises, ainsi que des exemples de demandes d’accès aux API à l’aide des identifiants de produit hérités et des champs de données renvoyés
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Prise en charge du Règlement général sur la protection des données par Adobe Advertising

*Par [!DNL Adobe Advertising Search, Social, & Commerce] ; Adobe Advertising DSP ; Adobe Advertising Creative ; et Adobe Advertising DCO*

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à en remplacer un. Consultez votre service juridique pour obtenir des conseils concernant le Règlement général sur la protection des données.

Le Règlement général sur la protection des données (RGPD), une loi en vigueur le 25 mai 2018, donne à tous les individus (personnes concernées) à l&#39;intérieur des frontières de l&#39;Union européenne (UE) le contrôle de leurs données personnelles et simplifie l&#39;environnement réglementaire pour les affaires internationales. Cette loi s&#39;applique à toutes les entreprises (responsables du traitement des données) qui offrent des biens ou des services aux personnes physiques à l&#39;intérieur des frontières de l&#39;UE au moment du traitement de leurs données personnelles, surveillent leur comportement ou collectent des données personnelles à leur sujet, quel que soit le lieu d&#39;activité du responsable du traitement des données.

Adobe Experience Cloud agit en tant que responsable du traitement des données pour toutes les données personnelles qu’il reçoit et stocke pour le compte de ses clients. En tant que contrôleur de données, vous déterminez les données personnelles que Adobe Experience Cloud traite et stocke pour vous.

Ce document décrit comment [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) et [!DNL Advertising DCO] prennent en charge les droits d’accès et de suppression des données des titulaires de données selon le RGPD à l’aide de l’API Adobe Experience Platform Privacy Service et de l’interface utilisateur de Privacy Service.

Pour plus d’informations sur ce que le RGPD signifie pour votre entreprise, consultez [RGPD et votre entreprise](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Types de requêtes de données pris en charge pour Adobe Advertising

Adobe Experience Platform permet aux entreprises d’effectuer les tâches suivantes :

* Accédez aux données au niveau des cookies ou des identifiants d’appareil d’un titulaire de données (pour les annonces dans les applications mobiles) dans [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] ou [!DNL DCO].
* Supprimez les données au niveau des cookies stockées dans [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] ou [!DNL DCO] pour les titulaires de données à l’aide d’un navigateur ou supprimez les données au niveau des identifiants stockées dans [!DNL DSP] pour les titulaires de données à l’aide d’applications sur des appareils mobiles.
* Vérifiez le statut d’une ou de toutes les requêtes existantes.

## Configuration requise pour envoyer des demandes pour Adobe Advertising

Pour envoyer des demandes d’accès et de suppression de données pour Adobe Advertising, vous devez :

1. Déployez une bibliothèque JavaScript pour récupérer et supprimer les cookies de votre titulaire de données. La même bibliothèque, `AdobePrivacy.js`, est utilisée pour toutes les solutions Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Les requêtes adressées à certaines solutions Experience Cloud ne nécessitent pas la bibliothèque JavaScript, mais les requêtes adressées à Adobe Advertising la requièrent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos titulaires de données peuvent soumettre des demandes d’accès et de suppression, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer les cookies [!DNL Adobe] (identifiant d’espace de noms : `gsurferID`) afin que vous puissiez envoyer ces identités dans le cadre des demandes d’accès et de suppression via l’API Adobe Experience Platform Privacy Service.

   Lorsque la personne concernée demande la suppression de données personnelles, la bibliothèque supprime également le cookie de la personne concernée du navigateur de la personne concernée.

   >[!NOTE]
   >
   >La suppression des données personnelles est différente de l’opt-out, qui arrête le ciblage d’un utilisateur final avec des segments d’audience. Cependant, lorsqu’un titulaire de données demande à supprimer des données personnelles de [!DNL Creative], [!DNL DSP] ou [!DNL DCO], la bibliothèque envoie également une demande à Adobe Advertising pour exclure le titulaire de données du ciblage de segment. Pour les annonceurs avec [!DNL Search, Social, & Commerce], nous vous recommandons de fournir aux titulaires de données un lien vers [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), qui explique comment se désabonner du ciblage des segments d’audience.

1. Identifiez votre ID d’organisation Experience Cloud et assurez-vous qu’il est lié à vos comptes Adobe Advertising.

   Un ID d’organisation Experience Cloud consiste en une chaîne alphanumérique de 24 caractères suivie de « @AdobeOrg ». Un identifiant d’organisation a été attribué à la plupart des clients Experience Cloud. Si votre équipe marketing ou votre administrateur système de [!DNL Adobe] interne ne connaît pas votre identifiant d’organisation ou ne sait pas s’il a été configuré, contactez l’assistance clientèle d’Adobe à l’adresse gdprsupport@adobe.com. Vous aurez besoin de l’ID d’organisation pour envoyer des requêtes à l’API de confidentialité à l’aide de l’espace de noms `imsOrgID`.

   >[!IMPORTANT]
   >
   >Contactez le représentant Adobe Advertising de votre société pour confirmer que tous les comptes Adobe Advertising de votre organisation, y compris les comptes [!DNL DSP] ou les annonceurs, les comptes [!DNL Search, Social, & Commerce] et les comptes [!DNL Creative] ou [!DNL DCO], sont liés à votre ID d’organisation Experience Cloud.

1. Utilisez l’API [Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (pour les requêtes automatisées) ou l’interface utilisateur [Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr) (pour les requêtes ad hoc) pour envoyer des requêtes d’accès et de suppression à Adobe Advertising au nom des titulaires de données et pour vérifier le statut des requêtes existantes.

   Pour les annonceurs qui disposent d’une application mobile afin d’interagir avec les titulaires de données et de lancer des campagnes avec DSP, vous devez télécharger les SDK mobiles compatibles avec la confidentialité pour Experience Cloud. Les SDK mobiles permettent aux contrôleurs de données de définir des indicateurs de statut d’opt-out, de récupérer l’identifiant de l’appareil du titulaire de données (identifiant de l’espace de noms : `deviceID`) et d’envoyer des requêtes à l’API Privacy Service. Votre application mobile nécessite une version de SDK 4.15.0 ou ultérieure.

   Lorsque vous soumettez la demande d’accès d’un titulaire de données, l’API Privacy Service renvoie les informations d’un titulaire de données en fonction du cookie ou de l’ID d’appareil spécifié, que vous devez ensuite renvoyer au titulaire de données.

   Lorsque vous soumettez la demande de suppression d’un titulaire de données, l’ID de cookie ou l’ID d’appareil ainsi que toutes les données de coût, de clic et de chiffre d’affaires associées au cookie sont supprimés du serveur.

   >[!NOTE]
   >
   >Si votre société dispose de plusieurs identifiants d’organisation Experience Cloud, vous devez envoyer des requêtes d’API distinctes pour chacun d’eux. Vous pouvez toutefois effectuer une requête d’API vers plusieurs sous-solutions Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] et [!DNL DCO]), avec un compte par sous-solution.

Toutes les étapes sont nécessaires pour Adobe Advertising. Pour plus d’informations sur ces tâches et d’autres tâches connexes que vous devez effectuer à l’aide de Adobe Experience Platform Privacy Service, et pour savoir où trouver les éléments nécessaires, consultez « [Présentation de Privacy Service ](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) ».

## Valeurs de champ requises dans les requêtes JSON Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*l’identifiant de votre organisation Experience Cloud*>

`"users":`

* `"key":` &lt;*généralement le nom du titulaire de données*>

* `"action":` `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (qui indique l’espace du cookie [!DNL adcloud])

   * `"value":` &lt;*la valeur de l’ID de cookie du titulaire de données a été extraite de`AdobePrivacy.js`*>

* `"include": **adCloud**` (qui est le produit [!DNL Adobe] qui s’applique à la requête)

* `"regulation": **gdpr**` (qui est la réglementation de confidentialité qui s’applique à la demande)

## Exemple de demande soumise par le titulaire de données à l’aide d’un identifiant utilisateur Adobe Advertising récupéré de `AdobePrivacy.js`

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
