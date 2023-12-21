---
title: "Processus d’utilisation de l’intégration DSP avec [!DNL Adobe] [!DNL Real-time CDP]"
description: "Découvrez comment activer DSP d’ingérer votre [!DNL Adobe] [!DNL Real-time CDP] segments propriétaires."
feature: DSP Audiences
source-git-commit: fb42e4aacaf0ea22890e0b4a46719725c99fffdc
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Processus d’utilisation de l’intégration DSP avec [!DNL Adobe Real-Time CDP]

1. [Autoriser DSP traduire les segments de données client en [!DNL LiveRamp RampIDs]](source-universal-id.md) qui sont reconnaissables dans un environnement admissible.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Création d’une source d’audience](source-create.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire.

1. Dans Experience Platform, configurez une connexion de destination de DSP Advertising à l’aide du [!UICONTROL Source Key] qui a été généré dans les paramètres source DSP.

   Pour obtenir des instructions sur l’activation de la connexion DSP destination, la sélection de segments et l’accès aux autorisations de contrôle, voir &quot;[Connexion Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

Pour obtenir une assistance supplémentaire, contactez votre équipe de compte d’Adobe ou `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [Activation des segments authentifiés à partir des partenaires d’ID universels](source-universal-id.md)
>* [Création d’une source d’audience pour activer les audiences propriétaires](source-create.md)
>* [Paramètres de la source d’audience](source-settings.md)
>* [Adobe Advertising DSP la connexion](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Présentation du catalogue des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Processus d’utilisation de l’intégration DSP avec [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
