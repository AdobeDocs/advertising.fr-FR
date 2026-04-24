---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer opt-out-of-sale support
description: Learn about support for capturing consumer opt-out-of-sale requests.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
TQID: https://experienceleague.adobe.com/16JkyKVsVoBIGKEbhEIH7HWZ-H-XkjBad7yq9-NhY3s
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
source-wordcount: 1101
ht-degree: 0%

---

# Adobe Advertising support for the California Consumer Privacy Act: Consumer opt-out of sale support

*For Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the California Consumer Privacy Act.

The California Consumer Privacy Act (CCPA) is California’s new privacy law, which is effective January 1, 2020. CCPA provides California residents new rights regarding their personal information and imposes data protection responsibilities on certain entities who conduct business in California. CCPA provides consumers with the right to access and delete their data as well as the right to opt out of certain activities that qualify as “selling” personal information to a third party.

As a business, you will determine the personal data that Adobe CX Enterprise processes and stores on your behalf.

As your service provider, Adobe Advertising provides support for your business to fulfill its obligations under CCPA that are applicable to the use of Adobe Advertising products and services, including managing consumer requests to access and delete personal information and managing consumer requests to opt out of the sale of personal information.

This document describes how Adobe Advertising Demand Side Platform (DSP), as a service provider, supports the consumer right to opt out of the &quot;sale&quot; of &quot;personal information,&quot; as each term is defined by the CCPA. It includes information on how to communicate opt-out-of-sale requests to Adobe Advertising and how to retrieve reports of your organization&#39;s opt-out-of-sale requests.

For information about how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; and [!DNL Advertising DCO] support consumers&#39; personal information access and deletion rights, see [Adobe Advertising support for the California Consumer Privacy Act: Consumer data access and delete support](/help/privacy/ccpa/ccpa-access-delete.md).

For more information about the Adobe Privacy services for CCPA, see the [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Communicating consumer opt-out-of-sale requests to Adobe Advertising

You can communicate consumer opt-out-of-sale requests by using either:

* a CCPA opt-out-of-sale segment created in Advertising DSP
* the Adobe Experience Platform Privacy Service API

### Méthode 1 : communiquer les demandes d’opposition à la vente du CCPA à l’aide d’un segment [!UICONTROL CCPA Opt-Out-of-Sale] dans Advertising DSP

>[!NOTE]
>
>Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente du CCPA.

1. Connectez-vous au compte de l’annonceur dans Advertising DSP sur [https://advertising.adobe.com/](https://advertising.adobe.com/).

1. [Créez un segment d’exclusion de la vente du CCPA et implémentez le pixel de segment pour capturer les requêtes d’exclusion](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Méthode 2 : communiquer les demandes d’opposition à la vente du CCPA à l’aide de l’API Adobe Experience Platform Privacy Service

*Les annonceurs se sont vu attribuer un ID d’organisation Adobe CX Enterprise uniquement*

1. Déployez une bibliothèque JavaScript pour récupérer les cookies de votre client. La même bibliothèque, `AdobePrivacy.js`, est utilisée pour toutes les solutions Adobe CX Enterprise.

   >[!IMPORTANT]
   >
   >Les requêtes adressées à certaines solutions Adobe CX Enterprise ne nécessitent pas la bibliothèque JavaScript, mais les requêtes adressées à Adobe Advertising la requièrent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos clients peuvent envoyer des requêtes d’opposition à la vente, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer les cookies Adobe (identifiant d’espace de noms : `gsurferID`) afin que vous puissiez envoyer ces identités dans le cadre de requêtes d’opposition à la vente via l’API Adobe Experience Platform Privacy Service.

1. Identifiez votre ID d’organisation CX Enterprise et assurez-vous qu’il est lié à vos comptes Adobe Advertising.

   Un ID d’organisation CX Enterprise consiste en une chaîne alphanumérique de 24 caractères suivie de « @AdobeOrg ». Un identifiant d’organisation a été attribué à la plupart des clients CX Enterprise. Si votre équipe marketing ou votre administrateur système interne Adobe ne connaît pas votre identifiant d’organisation ou ne sait pas s’il a été configuré, contactez l’équipe chargée de votre compte Adobe. Vous aurez besoin de l’ID d’organisation pour envoyer des requêtes à l’API de confidentialité à l’aide de l’espace de noms `imsOrgID`.

   >[!IMPORTANT]
   >
   >Contactez le représentant Adobe Advertising de votre société pour confirmer que tous les comptes Adobe Advertising de votre organisation, y compris les comptes [!DNL DSP] ou les annonceurs, les comptes [!DNL Search, Social, & Commerce] et les comptes [!DNL Creative] ou [!DNL DCO], sont liés à votre ID d’organisation CX Enterprise.

1. Utilisez l’API Adobe Experience Platform Privacy Service pour [envoyer des requêtes d’opposition à la vente](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html?lang=fr) à Adobe Advertising au nom des consommateurs et consommatrices, et pour vérifier le statut des requêtes existantes.

   Consultez l’annexe ci-dessous pour obtenir un exemple de demande d’opposition à la vente.

   >[!NOTE]
   >
   >Si votre entreprise dispose de plusieurs identifiants d’organisation CX Enterprise, vous devez envoyer des requêtes d’API distinctes pour chacun d’eux. Vous pouvez toutefois effectuer une requête d’API vers plusieurs sous-solutions Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] et [!DNL DCO]), avec un compte par sous-solution.

Toutes ces étapes sont nécessaires pour bénéficier de l’assistance d’Adobe Advertising. Pour plus d&#39;informations sur ces tâches et d&#39;autres tâches connexes que vous devez effectuer à l&#39;aide du Adobe Experience Platform Privacy Service, et pour savoir où trouver les éléments nécessaires, consultez [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=fr](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=fr).

## Récupération des rapports des consommateurs qui ont soumis des demandes d’opposition à la vente

Adobe Advertising génère des rapports mensuels sur les identifiants que les clients et clientes ont envoyés pour des requêtes d’opposition à la vente des informations personnelles pour le compte. Chaque rapport est disponible sous la forme d’un fichier texte séparé par des tabulations compressé au format GZIP. Les données consolident les requêtes capturées à l’aide des segments d’opposition à la vente du CCPA qui ont été créés dans Advertising DSP et de tous les envois effectués via l’API Privacy Service. Les identifiants d’utilisateur capturés dans les segments d’opposition à la vente du CCPA sont identifiés par segment et par annonceur. Les rapports sont générés le premier de chaque mois du mois précédent. Par exemple, la liste mensuelle des utilisateurs de juin est disponible le 1er juillet.

Vous pouvez récupérer des liens vers les rapports mensuels créés au cours des trois mois précédents, depuis Advertising DSP ou à l’aide de l’[!DNL Trafficking API] Advertising DSP. Chaque lien est valide pendant sept jours, mais est actualisé chaque fois qu’un client tente d’en récupérer un.

### Méthode 1 : récupération des rapports de désinscription de la vente des clients dans Advertising DSP

1. Connectez-vous au compte de l’annonceur dans Advertising DSP sur [https://advertising.adobe.com/](https://advertising.adobe.com/).

1. [Récupérer les rapports](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Méthode 2 : récupération des rapports de désinscription de la vente des clients à l’aide de l’[!DNL Trafficking API] Advertising DSP

Cette fonctionnalité est disponible pour les organisations qui utilisent le [!DNL Trafficking API]. Pour plus d’informations, consultez la documentation de la [!DNL Trafficking API] . <!-- Add link to API doc once it's published. -->

Si votre entreprise n’utilise pas le [!DNL Trafficking API], mais souhaite obtenir plus d’informations, contactez l’équipe chargée de votre compte Adobe.

## Annexe : exemple de requête [!UICONTROL CCPA Opt-Out-of-Sale] pour les utilisateurs de l’API Privacy Service

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

où, conformément aux spécifications de l’API [Privacy Service &#x200B;](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/api/appendix) :

* `"namespace": "AdCloud"` indique l’espace du cookie `AdCloud` et la valeur correspondante est l’identifiant de cookie du client tel qu’il est récupéré depuis `AdobePrivacy.js`
* `"include": ["adCloud"]` indique que la requête s’applique au produit Adobe Advertising
