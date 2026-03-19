---
title: À propos des sources d’audience propriétaires
description: Découvrez comment convertir d’autres identifiants d’utilisateur de vos segments propriétaires en identifiants universels pour le ciblage sans cookie.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 7f9b118ffe0b8e972296f79b19f6dcd2a9dedabe
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# À propos des sources d’audience propriétaires

*Fonction Beta*

DSP peut ingérer des segments propriétaires composés d’identifiants d’e-mail hachés créés dans votre plateforme de données client (CDP) et les convertir en segments composés d’identifiants universels. Chaque identifiant obtenu est basé sur les personnes et des limites de fréquence des annonces sont appliquées au niveau de l’identifiant<!-- Move that info. to somewhere else? -->.

Les détails du segment incluent la taille de chaque type d’identifiant universel ainsi que la taille de chaque type d’appareil suivi par des cookies ou des identifiants d’appareil.

## Types d’ID universels {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Vous pouvez traduire vos segments propriétaires en segments avec des identifiants authentifiés (déterministes) provenant des partenaires d’ID universels suivants.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution) :

   * Pour le reciblage des utilisateurs connectés.

     [!DNL RampIDs] sont disponibles pour les utilisateurs en Amérique du Nord, en Australie et en Nouvelle-Zélande.

     Les frais sont de 0,15 USD par impression publicitaire diffusée et de 0,25 USD par impression publicitaire vidéo diffusée.

   * Pour la mesure à l’aide de [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com) :

   * Pour le reciblage des utilisateurs connectés.

     [!DNL UID2 IDs] ne sont pas disponibles pour les utilisateurs dans l&#39;Espace économique européen et dans certains autres pays. Voir la [liste des pays interdits](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Les frais sont de 0,15 USD par impression publicitaire diffusée et de 0,25 USD par impression publicitaire vidéo diffusée.

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Plateformes de données client prises en charge pour les segments propriétaires

DSP a établi des connecteurs vers les CDP suivants afin d’ingérer rapidement vos segments propriétaires.

DSP peut également se connecter à des CDP supplémentaires à l’aide du partage de données par lots, en flux continu ou basé sur les API. Pour l’intégration à une nouvelle plateforme de données clients, contactez votre équipe de compte Adobe.

### [!DNL Adobe Real-Time CDP]

DSP est une *destination* intégrée pour [le [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), qui fait partie de Adobe Experience Platform.

Dans [!DNL Real-Time CDP], les destinations sont des connexions à des plateformes de données externes qui permettent une activation transparente des données. Vous pouvez utiliser les destinations pour activer vos adresses e-mail hachées pour la publicité ciblée dans DSP. Pour plus d’informations sur les destinations, consultez le guide Experience Platform [Guide des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), qui comprend une présentation du produit, des instructions pour [créer des espaces de travail de destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) et [créer des connexions de destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) et [activer des données vers les destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Pour permettre à DSP d’ingérer vos [!DNL Adobe] [!DNL Real-time CDP] segments propriétaires et de convertir vos adresses e-mail hachées en ID universels, consultez la section « [Convertir les ID utilisateur de [!DNL Adobe Real-Time CDP] en ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md) ».

### [!DNL ActionIQ]

Vous pouvez partager les données propriétaires de votre organisation de la plateforme de données clients [!DNL ActionIQ] avec DSP pour convertir vos adresses e-mail hachées en identifiants universels pour la publicité ciblée dans DSP. Cette intégration nécessite une personnalisation. Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

### [!DNL Amperity]

Vous pouvez partager les données propriétaires de votre organisation de la plateforme de données clients [!DNL Amperity] avec DSP pour convertir vos adresses e-mail hachées en identifiants universels pour la publicité ciblée dans DSP. Pour plus d’informations, voir « [Convertir les ID utilisateur de [!DNL Amperity] en ID universels](/help/dsp/audiences/sources/source-amperity.md) ».

### [!DNL Optimizely]

Vous pouvez partager les données propriétaires de votre organisation de la plateforme de données clients [!DNL Optimizely] avec DSP pour convertir vos adresses e-mail hachées en identifiants universels pour la publicité ciblée dans DSP. Pour plus d’informations, voir « [Convertir les ID utilisateur de [!DNL Optimizely] en ID universels](/help/dsp/audiences/sources/source-optimizely.md) ».

### [!DNL Tealium]

Vous pouvez partager les données propriétaires de votre organisation à partir de la plateforme de données client [!DNL Tealium] à l’aide de [!DNL Amazon Web Services]. Pour plus d’informations sur la conversion de vos adresses e-mail hachées en identifiants universels pour la publicité ciblée dans DSP, voir « [Convertir les ID utilisateur de [!DNL Tealium] en identifiants universels](/help/dsp/audiences/sources/source-tealium.md) ».

>[!MORELIKETHIS]
>
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](source-manage.md)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [Convertir les ID utilisateur de  [!DNL Adobe Real-Time CDP]  en ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir les ID utilisateur de  [!DNL Amperity]  en ID universels](/help/dsp/audiences/sources/source-amperity.md)
>* [Convertir les ID utilisateur de  [!DNL Optimizely]  en ID universels](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convertir les ID utilisateur de  [!DNL Tealium]  en ID universels](/help/dsp/audiences/sources/source-tealium.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
