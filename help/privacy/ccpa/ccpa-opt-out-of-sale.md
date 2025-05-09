---
title: Prise en charge d’Adobe Advertising pour la Loi sur la protection de la vie privée des consommateurs de Californie et
description: Découvrez la prise en charge de la capture des requêtes de désinscription à la vente des clients.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Prise en charge par Adobe Advertising de la Loi sur la protection des informations personnelles des consommateurs de Californie : assistance pour le désabonnement des consommateurs

*Pour Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à en remplacer un. Consultez votre service juridique pour obtenir des conseils concernant la Loi sur la protection des renseignements personnels des consommateurs de Californie.

Le California Consumer Privacy Act (CCPA) est la nouvelle loi californienne sur la protection de la vie privée, qui entre en vigueur le 1er janvier 2020. Le CCPA offre aux Californiens de nouveaux droits sur leurs informations personnelles et impose des responsabilités en matière de protection des données à certaines entités qui exercent des activités en Californie. Le CCPA offre aux consommateurs le droit d’accéder à leurs données et de les supprimer, ainsi que le droit de se désinscrire de certaines activités qualifiées de « vente » d’informations personnelles à un tiers.

En tant qu’entreprise, vous déterminerez les données personnelles que Adobe Experience Cloud traite et stocke pour vous.

En tant que fournisseur, Adobe Advertising fournit une assistance à votre entreprise afin qu’elle remplisse ses obligations en vertu du CCPA qui s’appliquent à l’utilisation des produits et services Adobe Advertising, y compris la gestion des demandes de consommateurs souhaitant accéder à des informations personnelles et les supprimer, et la gestion des demandes de consommateurs souhaitant se désabonner de la vente d’informations personnelles.

Ce document décrit comment Adobe Advertising Demand Side Platform (DSP), en tant que fournisseur de services, prend en charge le droit des consommateurs de se désinscrire de la « vente » des « informations personnelles », comme chaque terme est défini par le CCPA. Elle contient des informations sur la manière de communiquer les requêtes d’opposition à la vente des informations personnelles à Adobe Advertising et sur la manière de récupérer des rapports sur les requêtes d’opposition à la vente des informations personnelles de votre entreprise.

Pour plus d’informations sur la façon dont [!DNL Advertising Search, Social, & Commerce], Advertising Creative et [!DNL Advertising DCO] prennent en charge les droits d’accès et de suppression des informations personnelles des consommateurs, consultez [Prise en charge d’Adobe Advertising pour la Loi sur la protection de la vie privée des consommateurs de Californie : prise en charge de l’accès et de la suppression des données client](/help/privacy/ccpa/ccpa-access-delete.md).

Pour plus d’informations sur Adobe Privacy Services pour le CCPA, consultez le [Centre de traitement des données personnelles d’Adobe](https://www.adobe.com/privacy/ccpa.html).

## Communication des requêtes de désinscription de la vente des clients à Adobe Advertising

Vous pouvez communiquer les demandes de désinscription de la vente des clients à l’aide de l’une des méthodes suivantes :

* un segment d’exclusion de la vente du CCPA créé dans Advertising DSP
* l’API Adobe Experience Platform Privacy Service

### Méthode 1 : communiquer les demandes de désinscription de la vente du CCPA à l’aide d’un segment [!UICONTROL CCPA Opt-Out-of-Sale] dans Advertising DSP

>[!NOTE]
>
>Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente du CCPA.

1. Connectez-vous au compte de l’annonceur dans Advertising DSP sur [https://advertising.adobe.com/](https://advertising.adobe.com/).

1. [Créez un segment d’exclusion de la vente du CCPA et implémentez le pixel de segment pour capturer les requêtes d’exclusion](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Méthode 2 : communiquer les demandes de désinscription de la vente du CCPA à l’aide de l’API Adobe Experience Platform Privacy Service

*Les annonceurs se sont vu attribuer un ID d’organisation Adobe Experience Cloud uniquement*

1. Déployez une bibliothèque JavaScript pour récupérer les cookies de votre client. La même bibliothèque, `AdobePrivacy.js`, est utilisée pour toutes les solutions Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Les requêtes adressées à certaines solutions Adobe Experience Cloud ne nécessitent pas la bibliothèque JavaScript, mais les requêtes adressées à Adobe Advertising la requièrent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos clients peuvent envoyer des requêtes d’opposition à la vente, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer les cookies Adobe (identifiant d’espace de noms : `gsurferID`) afin que vous puissiez envoyer ces identités dans le cadre de requêtes d’opposition à la vente via l’API Adobe Experience Platform Privacy Service.

1. Identifiez votre ID d’organisation Experience Cloud et assurez-vous qu’il est lié à vos comptes Adobe Advertising.

   Un ID d’organisation Experience Cloud consiste en une chaîne alphanumérique de 24 caractères suivie de « @AdobeOrg ». Un identifiant d’organisation a été attribué à la plupart des clients Experience Cloud. Si votre équipe marketing ou votre administrateur système interne Adobe ne connaît pas votre identifiant d’organisation ou ne sait pas s’il a été configuré, contactez l’équipe chargée de votre compte Adobe. Vous aurez besoin de l’ID d’organisation pour envoyer des requêtes à l’API de confidentialité à l’aide de l’espace de noms `imsOrgID`.

   >[!IMPORTANT]
   >
   >Contactez le représentant Adobe Advertising de votre société pour confirmer que tous les comptes Adobe Advertising de votre organisation, y compris les comptes [!DNL DSP] ou les annonceurs, les comptes [!DNL Search, Social, & Commerce] et les comptes [!DNL Creative] ou [!DNL DCO], sont liés à votre ID d’organisation Experience Cloud.

1. Utilisez l’API Adobe Experience Platform Privacy Service pour [envoyer des requêtes d’opposition à la vente](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) à Adobe Advertising au nom des consommateurs et consommatrices, et pour vérifier le statut des requêtes existantes.

   Consultez l’annexe ci-dessous pour obtenir un exemple de demande d’opposition à la vente.

   >[!NOTE]
   >
   >Si votre entreprise dispose de plusieurs identifiants d’organisation Experience Cloud, vous devez envoyer des requêtes d’API distinctes pour chacun d’eux. Vous pouvez toutefois effectuer une requête d’API vers plusieurs sous-solutions Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] et [!DNL DCO]), avec un compte par sous-solution.

Toutes ces étapes sont nécessaires pour bénéficier de l’assistance d’Adobe Advertising. Pour plus d&#39;informations sur ces tâches et d&#39;autres tâches connexes que vous devez effectuer à l&#39;aide du Adobe Experience Platform Privacy Service, et pour savoir où trouver les éléments nécessaires, consultez [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Récupération des rapports des consommateurs et consommatrices qui ont soumis des requêtes d’opposition à la vente

Adobe Advertising génère des rapports mensuels sur les identifiants que les clients et clientes ont envoyés pour des requêtes d’opposition à la vente des informations personnelles pour le compte. Chaque rapport est disponible sous la forme d’un fichier texte séparé par des tabulations compressé au format GZIP. Les données consolident les requêtes capturées à l’aide des segments d’opposition à la vente du CCPA qui ont été créés dans Advertising DSP et de tous les envois effectués via l’API Privacy Service. Les identifiants d’utilisateur capturés dans les segments d’opposition à la vente du CCPA sont identifiés par segment et par annonceur. Les rapports sont générés le premier de chaque mois du mois précédent. Par exemple, la liste mensuelle des utilisateurs de juin est disponible le 1er juillet.

Vous pouvez récupérer des liens vers les rapports mensuels créés au cours des trois mois précédents, depuis Advertising DSP ou à l’aide de l’[!DNL Trafficking API] Advertising DSP. Chaque lien est valide pendant sept jours, mais est actualisé chaque fois qu’un client tente d’en récupérer un.

### Méthode 1 : récupération des rapports de désinscription de la vente des clients dans Advertising DSP

1. Connectez-vous au compte de l’annonceur dans Advertising DSP sur [https://advertising.adobe.com/](https://advertising.adobe.com/).

1. [Récupérer les rapports](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Méthode 2 : récupération des rapports de désinscription de la vente des clients à l’aide de l’[!DNL Trafficking API] Advertising DSP

Cette fonctionnalité est disponible pour les organisations qui utilisent le [!DNL Trafficking API]. Pour plus d’informations, consultez la documentation de la [!DNL Trafficking API] . <!-- Add link to API doc once it's published. -->

Si votre entreprise n’utilise pas le [!DNL Trafficking API], mais souhaite obtenir plus d’informations, contactez l’équipe chargée de votre compte Adobe.

## Annexe : exemple [!UICONTROL CCPA Opt-Out-of-Sale] requête pour les utilisateurs de l’API Privacy Service

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

où, conformément aux spécifications de l’API [Privacy Service ](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix) :

* `"namespace": "AdCloud"` indique l’espace du cookie `AdCloud` et la valeur correspondante est l’identifiant de cookie du client tel qu’il est récupéré depuis `AdobePrivacy.js`
* `"include": ["adCloud"]` indique que la requête s’applique au produit Adobe Advertising
