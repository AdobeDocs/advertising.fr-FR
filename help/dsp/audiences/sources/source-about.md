---
title: À propos des sources d’audience propriétaires
description: Découvrez comment convertir d’autres identifiants d’utilisateur dans vos segments propriétaires en identifiants universels pour un ciblage sans cookie.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 78ee6ddbfb87915475bcf84bd7cd405a58eccf14
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# À propos des sources d’audience propriétaires

*Fonction bêta*

DSP peut ingérer des segments propriétaires composés d’ID de courrier électronique haché créés dans votre plateforme de données client (CDP) et les convertir en segments composés d’ID universels. Chaque ID obtenu est basé sur les personnes et des limites de fréquence des publicités sont appliquées au niveau de l’ID.<!-- Move that info. to somewhere else? -->.

Les détails du segment incluent la taille de chaque type d’identifiant universel ainsi que la taille de chaque type d’appareil suivi par des cookies ou des identifiants d’appareil.

## Types d’ID universels {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

Vous pouvez traduire vos segments propriétaires en segments avec des identifiants authentifiés (déterministes) provenant des partenaires d’identification universels suivants.

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution):

   * Pour recibler les utilisateurs connectés.

     [!DNL RampIDs] sont disponibles pour les utilisateurs en Amérique du Nord, en Australie et en Nouvelle-Zélande.

     Les frais sont de 0,15 USD par impression de publicité display diffusée et de 0,25 USD par impression de publicité vidéo diffusée.

   * Pour la mesure à l’aide de [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com):

   * Pour recibler les utilisateurs connectés.

     [!DNL UID2 IDs] ne sont pas disponibles pour les utilisateurs de l’Espace économique européen et de certains pays supplémentaires. Voir [liste des pays interdits](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     Les frais sont de 0,15 USD par impression de publicité display diffusée et de 0,25 USD par impression de publicité vidéo diffusée.

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

DSP a établi des connecteurs aux CDP suivantes pour ingérer rapidement vos segments propriétaires.

DSP peut également se connecter à d’autres CDP à l’aide du partage de données par lots, par flux ou à l’aide d’API. Pour l’intégrer à une nouvelle plateforme de données clients, contactez votre équipe de compte d’Adobe.

### [!DNL Adobe Real-Time Customer Data Platform]

DSP est intégré à *destination* pour [la valeur [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), qui fait partie de Adobe Experience Platform.

Dans [!DNL Real-Time CDP], les destinations sont des connexions à des plateformes de données externes qui permettent une activation transparente des données. Vous pouvez utiliser des destinations pour activer vos adresses électroniques hachées pour la publicité ciblée dans DSP. Pour plus d’informations sur les destinations, voir l’Experience Platform [Guide des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), y compris un aperçu du produit, des instructions pour [création d’espaces de travail de destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) et [création de connexions à destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), et [activation des données vers les destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Pour permettre DSP d’ingérer votre [!DNL Adobe] [!DNL Real-time CDP] segments propriétaires et convertissez vos adresses électroniques hachées en identifiants universels. voir &quot;[Convertir les ID utilisateur à partir de [!DNL Adobe Real-Time CDP] vers des ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

### [!DNL ActionIQ]

Vous pouvez partager les données propriétaires de votre entreprise à partir du [!DNL ActionIQ] plateforme de données client avec DSP pour convertir vos adresses électroniques hachées en identifiants universels pour la publicité ciblée dans DSP. Cette intégration nécessite une personnalisation. Pour plus d’informations, contactez votre équipe de compte d’Adobe.

### [!DNL Amperity]

Vous pouvez partager les données propriétaires de votre entreprise à partir du [!DNL Amperity] plateforme de données client avec DSP pour convertir vos adresses électroniques hachées en identifiants universels pour la publicité ciblée dans DSP. Pour plus d’informations, voir &quot;[Convertir les ID utilisateur à partir de [!DNL Amperity] vers des ID universels](/help/dsp/audiences/sources/source-amperity.md).&quot;

### [!DNL Optimizely]

Vous pouvez partager les données propriétaires de votre entreprise à partir du [!DNL Optimizely] plateforme de données client avec DSP pour convertir vos adresses électroniques hachées en identifiants universels pour la publicité ciblée dans DSP. Pour plus d’informations, voir &quot;[Convertir les ID utilisateur à partir de [!DNL Optimizely] vers des ID universels](/help/dsp/audiences/sources/source-optimizely.md).&quot;

### [!DNL Tealium]

Vous pouvez partager les données propriétaires de votre entreprise à partir du [!DNL Tealium] plateforme de données client à l’aide de [!DNL Amazon Web Services]. Pour plus d’informations sur la conversion de vos adresses électroniques hachées en identifiants universels pour la publicité ciblée dans DSP, voir &quot;[Convertir les ID utilisateur à partir de [!DNL Tealium] vers des ID universels](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [Gestion des sources d’audience pour activer les audiences d’ID universelles](source-manage.md)
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [Convertir les ID utilisateur à partir de [!DNL Adobe Real-Time CDP] vers des ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir les ID utilisateur à partir de [!DNL Amperity] vers des ID universels](/help/dsp/audiences/sources/source-amperity.md)
>* [Convertir les ID utilisateur à partir de [!DNL Optimizely] vers des ID universels](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convertir les ID utilisateur à partir de [!DNL Tealium] vers des ID universels](/help/dsp/audiences/sources/source-tealium.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
