---
title: À propos de l’activation de segments authentifiés à partir des sources d’audience
description: Découvrez comment ingérer des segments propriétaires à partir d’une plateforme de données client.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: e3e8753db31bc835c49eb2037fdcd7696a895a8c
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# À propos de l’activation de segments authentifiés à partir des sources d’audience

DSP peut ingérer des segments propriétaires composés d’ID de courrier électronique haché ou d’ID universels créés dans une plateforme de données client (CDP). Vous pouvez utiliser les segments ingérés comme cibles pour vos emplacements.

Les CDP suivantes ont établi des connecteurs, mais la DSP peut également se connecter à n’importe quelle CDP à l’aide du partage de données par lots, par flux ou à l’aide d’API. Pour l’intégrer à une nouvelle plateforme de données clients, contactez votre équipe de compte d’Adobe.

## [!DNL Adobe Real-Time Customer Data Platform]

DSP est intégré à [la valeur [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), qui fait partie de Adobe Experience Platform.

Dans [!DNL Real-Time CDP], *destinations* sont des connexions à des plateformes de données externes qui permettent une activation transparente des données. Par exemple, vous pouvez utiliser des destinations pour activer vos relations client connues (telles que des adresses électroniques hachées) pour la publicité ciblée dans des formats numériques pris en charge par DSP. Pour plus d’informations sur les destinations, voir l’Experience Platform [Guide des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), y compris un aperçu du produit, des instructions pour [création d’espaces de travail de destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) et [création de connexions à destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), et [activation des données vers les destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Voir &quot;[Processus d’utilisation de l’intégration DSP avec [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

## [!DNL ActionIQ]

Vous pouvez partager les données propriétaires de votre entreprise à partir du [!DNL Action IQ] plateforme de données client avec DSP. Vous pouvez ensuite cibler vos emplacements de DSP sur les segments à l’aide de [!DNL RampIDs] ou [!DNL Unified IDs 2.0].

Cette intégration nécessite une personnalisation. Pour plus d’informations, contactez votre équipe de compte d’Adobe.

## [!DNL Tealium]

Vous pouvez partager les données propriétaires de votre entreprise à partir du [!DNL Tealium] plateforme de données client à l’aide de [!DNL Amazon Web Services]. Vous pouvez ensuite cibler vos emplacements de DSP sur les segments à l’aide de [!DNL RampIDs]. Voir &quot;[Processus d’utilisation de l’intégration DSP avec [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [Processus d’utilisation de l’intégration DSP avec [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Processus d’utilisation de l’intégration DSP avec [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Création d’une source d’audience pour activer les audiences propriétaires](source-create.md)
>* [Paramètres de la source d’audience](source-settings.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
