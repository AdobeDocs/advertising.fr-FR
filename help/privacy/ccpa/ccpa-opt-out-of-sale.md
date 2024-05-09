---
title: 'Prise en charge des Adobes Advertising pour le California Consumer Privacy Act : prise en charge de l’exclusion de la vente pour les consommateurs'
description: Découvrez la prise en charge de la capture des demandes d’opposition à la vente des consommateurs.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# Prise en charge des Adobes Advertising pour le California Consumer Privacy Act : prise en charge de l’exclusion de la vente par les consommateurs

*Pour Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à remplacer un avis juridique. Consultez votre service juridique pour obtenir des conseils concernant le California Consumer Privacy Act.

Le California Consumer Privacy Act (CCPA) est la nouvelle loi californienne sur la protection de la vie privée, qui est entrée en vigueur le 1er janvier 2020. Le CCPA accorde aux résidents de Californie de nouveaux droits concernant leurs informations personnelles et impose des responsabilités en matière de protection des données à certaines entités qui exercent des activités en Californie. Le CCPA accorde aux consommateurs le droit d’accéder à leurs données et de les supprimer ainsi que le droit de se désinscrire de certaines activités qualifiées de &quot;vente&quot; d’informations personnelles à un tiers.

En tant qu’entreprise, vous déterminerez les données personnelles que Adobe Experience Cloud traite et stocke pour vous.

En tant que fournisseur de services, Adobe Advertising fournit une assistance à votre entreprise pour qu’elle remplisse ses obligations en vertu de la CCPA qui s’appliquent à l’utilisation des produits et services d’Adobe Advertising, y compris la gestion des demandes des consommateurs d’accès et de suppression des informations personnelles et la gestion des demandes des consommateurs de se désinscrire de la vente des informations personnelles.

Ce document décrit comment Adobe Advertising Demand Side Platform (DSP), en tant que fournisseur de services, soutient le droit du consommateur de se désinscrire de la &quot;vente&quot; des &quot;informations personnelles&quot;, car chaque terme est défini par la CCPA. Elle comprend des informations sur la manière de communiquer les demandes d’opposition à la vente à l’Adobe Advertising et de récupérer les rapports des demandes d’opposition à la vente de votre organisation.

Pour plus d’informations sur la manière dont [!DNL Advertising Search, Social, & Commerce]; Advertising Creative ; et [!DNL Advertising DCO] prendre en charge les droits d’accès et de suppression des informations personnelles des consommateurs, voir [Prise en charge des Adobes Advertising pour le California Consumer Privacy Act : prise en charge de l’accès aux données et de la suppression des clients](/help/privacy/ccpa/ccpa-access-delete.md).

Pour plus d’informations sur les services de confidentialité Adobe pour le CCPA, voir la section [Centre de traitement des données personnelles Adobe](https://www.adobe.com/privacy/ccpa.html).

## Communication aux Adobes Advertising de demandes d’opposition à la vente aux consommateurs

Vous pouvez communiquer les demandes d’opposition à la vente des consommateurs à l’aide de l’une des méthodes suivantes :

* un segment d’opposition à la vente des informations personnelles créé dans Advertising DSP
* API ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE

### Méthode 1 : communication des demandes d’opposition à la vente des informations personnelles du CCPA à l’aide d’une [!UICONTROL CCPA Opt-Out-of-Sale] Segment dans le DSP de publicité

>[!NOTE]
>
>Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente des informations personnelles du CCPA.

1. Connectez-vous au compte de l’annonceur dans le DSP Advertising à l’adresse [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Créez un segment d’opposition à la vente des informations personnelles (CCPA) et implémentez le pixel de segment pour capturer les demandes d’opposition.](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Méthode 2 : communication des demandes d’opposition à la vente des informations personnelles du CCPA à l’aide de l’API Adobe Experience Platform Privacy Service

*Les annonceurs ont affecté un ID d’organisation Adobe Experience Cloud uniquement*

1. Déployez une bibliothèque JavaScript pour récupérer les cookies de votre client. La même bibliothèque, `AdobePrivacy.js`, est utilisé pour toutes les solutions Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Les requêtes envoyées à certaines solutions Adobe Experience Cloud ne nécessitent pas la bibliothèque JavaScript, mais les requêtes d’Adobe Advertising le nécessitent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos clients peuvent envoyer des demandes d’opposition à la vente, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer les cookies d’Adobe (ID d’espace de noms : `gsurferID`) afin que vous puissiez soumettre ces identités dans le cadre de demandes d’opposition à la vente via l’API Adobe Experience Platform Privacy Service.

1. Identifiez l’ID d’organisation de votre Experience Cloud et assurez-vous qu’il est lié à vos comptes d’Adobe Advertising.

   Un ID d’organisation Experience Cloud est une chaîne alphanumérique de 24 caractères accompagnée de &quot;@AdobeOrg&quot;. Un ID d’organisation a été attribué à la plupart des clients Experience Cloud. Si votre équipe marketing ou votre administrateur système d’Adobes interne ne connaît pas votre ID d’organisation ou ne sait pas s’il a été configuré, contactez votre équipe de compte d’Adobe. Vous aurez besoin de l’ID d’organisation pour envoyer des requêtes à l’API de confidentialité à l’aide de la variable `imsOrgID` espace de noms.

   >[!IMPORTANT]
   >
   >Contactez le représentant de l’Adobe Advertising de votre entreprise pour confirmer que tous les comptes d’Adobe Advertising de votre entreprise — y compris [!DNL DSP] des comptes ou des annonceurs, [!DNL Search, Social, & Commerce] les comptes et [!DNL Creative] ou [!DNL DCO] comptes : sont liés à l’ID d’organisation Experience Cloud.

1. Utilisez l’API Adobe Experience Platform Privacy Service pour [envoi de demandes d’exclusion de la vente](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) pour Adobe Advertising au nom des consommateurs et pour vérifier le statut des demandes existantes.

   Consultez l’ Annexe ci-dessous pour obtenir un exemple de demande d’opposition à la vente.

   >[!NOTE]
   >
   >Si votre entreprise dispose de plusieurs ID d’organisation Experience Cloud, vous devez envoyer des demandes d’API distinctes pour chacun d’eux. Vous pouvez toutefois effectuer une requête d’API sur plusieurs sous-solutions Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], et [!DNL DCO]), avec un compte par sous-solution.

Toutes ces étapes sont nécessaires pour recevoir le soutien d’Adobe Advertising. Pour plus d’informations sur ces tâches et d’autres tâches connexes que vous devez effectuer à l’aide de Adobe Experience Platform Privacy Service et où trouver les éléments nécessaires, voir [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Récupération des rapports des consommateurs qui ont soumis des demandes d’exclusion de la vente

Adobe Advertising génère des rapports mensuels sur les identifiants que les clients ont envoyés pour les demandes d’exclusion de la vente pour le compte. Chaque rapport est disponible sous la forme d’un fichier texte de données séparées par des tabulations compressé au format GZIP. Les données consolident les demandes capturées à l’aide des segments d’opposition à la vente des CCPA qui ont été créés dans Advertising DSP et tous les envois effectués via l’API du Privacy Service. Les identifiants utilisateur capturés dans les segments d’opposition à la vente des informations personnelles (CCPA) sont identifiés par le segment et par l’annonceur. Les rapports sont générés le premier de chaque mois pour le mois précédent. Par exemple, la liste mensuelle des utilisateurs pour juin est disponible le 1er juillet.

Vous pouvez récupérer des liens vers les rapports mensuels créés au cours des trois mois précédents, soit à partir de l’DSP Advertising, soit à l’aide de l’DSP Advertising [!DNL Trafficking API]. Chaque lien est valide pendant sept jours, mais est actualisé chaque fois qu’un client tente d’en récupérer un.

### Méthode 1 : récupération des rapports d’exclusion de la vente par les consommateurs dans les DSP de publicité

1. Connectez-vous au compte de l’annonceur dans le DSP Advertising à l’adresse [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Récupération des rapports](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Méthode 2 : récupération des rapports d’exclusion de la vente pour les consommateurs à l’aide de la DSP de publicité [!DNL Trafficking API]

Cette fonctionnalité est disponible pour les organisations qui utilisent la variable [!DNL Trafficking API]. Reportez-vous à la documentation de la section [!DNL Trafficking API] pour plus d’informations.<!-- Add link to API doc once it's published. -->

Si votre entreprise n’utilise pas la variable [!DNL Trafficking API] mais pour plus d’informations, contactez votre équipe de compte d’Adobe.

## Annexe : Exemple [!UICONTROL CCPA Opt-Out-of-Sale] Demande d’utilisateurs d’API Privacy Service

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
            "namespace": "adCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

où :

* `"namespace": "adCloud"` indique que la variable `adCloud` espace de cookie et la valeur correspondante est l’ID de cookie du client tel qu’il est récupéré à partir de `AdobePrivacy.js`
* `"include": ["adCloud"]` indique que la demande s’applique à Adobe Advertising
