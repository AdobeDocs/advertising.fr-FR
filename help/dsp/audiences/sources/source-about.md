---
title: À propos des sources d’audience propriétaires
description: Découvrez comment convertir d’autres identifiants d’utilisateur de vos segments propriétaires en identifiants universels pour le ciblage sans cookie.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
TQID: https://experienceleague.adobe.com/8wdjwhNF-KDspEa1wSYWwlDOJxc3LiyqnSwEE-Fq9bY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 710
ht-degree: 0%

---

# À propos des sources d’audience propriétaires

La fonctionnalité de source d’audience vous permet d’importer des segments propriétaires contenant des identifiants universels en l’état ou de les convertir en segments contenant des types d’identifiants universels spécifiés :

* En Australie, les annonceurs peuvent importer des segments propriétaires qui contiennent déjà des identifiants universels [!DNL AdFixus].

* DSP peut ingérer des segments propriétaires composés d’identifiants d’e-mail, de cookies et d’identifiants de publicité mobile (MAID) hachés créés dans d’autres plateformes de données client (CDP) et les convertir en segments composés d’identifiants d’[!DNL RampIDs] et de [!DNL Unified ID 2.0 (UID2.0)] [!DNL LiveRamp].

Pour tous les types d’ID, chaque ID obtenu est basé sur les personnes et des limites de fréquence des annonces sont appliquées au niveau de l’ID<!-- Move that info. to somewhere else? -->. Les détails du segment incluent la taille de chaque type d’identifiant universel et la taille de chaque type d’appareil suivi par des cookies ou des identifiants d’appareil.

## Types d’identifiants universels vers lesquels vous pouvez traduire les segments propriétaires {#universal-id-types}

<!--
  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Vous pouvez traduire vos segments propriétaires à partir de [!DNL ActionIQ], [!DNL Adobe] [!DNL Real-time CDP], [!DNL Amperity], [!DNL Optimizely] et [!DNL Tealium] en segments avec des identifiants authentifiés (déterministes) provenant des partenaires d’ID universels suivants.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Pour le reciblage des utilisateurs connectés.

     [!DNL RampIDs] sont disponibles pour les utilisateurs en Amérique du Nord, en Australie et en Nouvelle-Zélande.

     Les frais sont de 0,15 USD par impression publicitaire diffusée et de 0,25 USD par impression publicitaire vidéo diffusée.

   * Pour la mesure à l’aide de [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] IDs](https://unifiedid.com) :

   * Pour le reciblage des utilisateurs connectés.

     [!DNL UID2 IDs] ne sont pas disponibles pour les utilisateurs dans l&#39;Espace économique européen et dans certains autres pays. Voir la [liste des pays interdits](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Les frais sont de 0,15 USD par impression publicitaire diffusée et de 0,25 USD par impression publicitaire vidéo diffusée.

<!--
 Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. Contact your Adobe Account Team for instructions.
-->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Plateformes de données client prises en charge pour les segments propriétaires

DSP a établi des connecteurs vers les CDP suivants afin d’ingérer rapidement vos segments propriétaires.

DSP peut également se connecter à des CDP supplémentaires à l’aide du partage de données par lots, en flux continu ou basé sur les API. Pour l’intégration à une nouvelle plateforme de données clients, contactez votre équipe de compte Adobe.

### [!DNL ActionIQ]

Vous pouvez partager les données propriétaires de votre organisation de la plateforme de données clients [!DNL ActionIQ] avec DSP pour convertir vos adresses e-mail hachées en identifiants universels pour la publicité ciblée dans DSP. Cette intégration nécessite une personnalisation. Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

### [!DNL Adobe Real-Time CDP]

DSP est une *destination* intégrée pour [le [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), qui fait partie de Adobe Experience Platform.

Dans [!DNL Real-Time CDP], les destinations sont des connexions à des plateformes de données externes qui permettent une activation transparente des données. Vous pouvez utiliser les destinations pour activer vos adresses e-mail hachées, vos cookies et vos identifiants de publicité mobile pour la publicité ciblée dans DSP. Pour plus d’informations sur les destinations, consultez le [Guide des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html) d’Experience Platform, qui comprend une présentation du produit, des instructions pour [créer des espaces de travail de destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) et [créer des connexions de destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) et [activer des données vers les destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Pour permettre à DSP d’ingérer vos [!DNL Adobe] [!DNL Real-time CDP] segments propriétaires et de convertir vos adresses e-mail hachées, cookies et identifiants publicitaires mobiles en identifiants universels, consultez la section « [Convertir les identifiants d’utilisateur de [!DNL Adobe Real-Time CDP] en identifiants universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md) ».

### [!DNL AdFixus]

Les annonceurs australiens peuvent utiliser l’intégration d’Advertising DSP à [!DNL AdFixus] pour importer des segments propriétaires contenant des identifiants universels [!DNL AdFixus]. Ce chemin d’accès est distinct de la traduction des ID d’e-mail ou des MAID hachés dans un connecteur CDP en ID [!DNL RampIDs] ou [!DNL UID2]. Pour plus d’informations, voir « [Importer des segments propriétaires depuis [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md) ».

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
>* [Importer des segments propriétaires depuis [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
