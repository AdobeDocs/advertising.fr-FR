---
title: Paramètres de la source d’audience
description: Découvrez les paramètres des sources d’audience.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Paramètres de la source d’audience

**[!UICONTROL Data Visibility Level]:** Si les segments sont disponibles pour un seul annonceur ayant accès au compte (*[!UICONTROL Advertiser]*) ou à tous les annonceurs ayant accès au compte *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Visibilité au niveau du annonceur uniquement) Annonceur pour lequel les segments sont disponibles. Sélectionnez-en un dans la liste des annonceurs ayant accès au compte.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] sources uniquement) L’ID d’organisation Adobe Experience Cloud pour la variable [!DNL Adobe Experience Platform] compte .

**[!UICONTROL Convert PII to the following IDs]:** ([!DNL ActionIQ] et [!DNL Tealium] sources uniquement) Type d’ID vers lequel vous souhaitez convertir vos informations d’identification personnelle (PII). Les taxes sur les données sont appliquées en conséquence.

* *[!DNL RampID]:* Pour convertir des PII en RampID. Si vous choisissez *[!DNL RampID]*, vos segments sont traduits en [!DNL RampIDs] automatiquement.

* *[!DNL Unified ID2.0]:* ([!DNL ActionIQ] sources uniquement) Pour convertir des informations d’identification personnelles en [ID unifié 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]:** (Lecture seule ; généré automatiquement) Clé source que vous pouvez utiliser pour créer une connexion de destination dans la plateforme de données client afin de pousser les audiences vers le DSP de publicité. Vous pouvez copier la valeur dans le presse-papiers pour la coller dans les paramètres de connexion de destination ou dans un fichier.

>[!MORELIKETHIS]
>
>* [Création d’une source d’audience pour activer les audiences propriétaires](source-create.md)
>* [À propos de l’activation de segments authentifiés à partir des sources d’audience](source-about.md)
>* [Activation des segments authentifiés à partir des partenaires d’ID universels](source-universal-id.md)
>* [Adobe Advertising DSP la connexion](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
