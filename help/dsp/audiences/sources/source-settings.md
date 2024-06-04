---
title: Paramètres de la source d’audience
description: Découvrez les paramètres des sources d’audience.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Paramètres de la source d’audience

*Fonction bêta*

**[!UICONTROL Data Visibility Level]:** Si les segments sont disponibles pour un seul annonceur ayant accès au compte (*[!UICONTROL Advertiser]*) ou à tous les annonceurs ayant accès au compte *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Visibilité au niveau du annonceur uniquement) Annonceur pour lequel les segments sont disponibles. Sélectionnez-en un dans la liste des annonceurs ayant accès au compte.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] sources uniquement) L’ID d’organisation Adobe Experience Cloud pour la variable [!DNL Adobe Experience Platform] compte .

**[!UICONTROL Convert PII to the following IDs]:** Les types d’ID vers lesquels vous allez convertir vos informations d’identification personnelle (PII). Si vous sélectionnez plusieurs types, le segment généré est renseigné avec des valeurs pour chaque type d’ID sélectionné (par exemple, un [!DNL RampID] et un [!DNL Unified ID2.0] pour chaque adresse électronique). Les taxes sur les données sont appliquées en conséquence.

Pour [!DNL RampID] et [!DNL Unified ID2.0], le fournisseur recherche chaque adresse électronique pour voir si un ID existe déjà et convertit l’adresse en un ID correspondant lorsqu’il est disponible. Si aucun identifiant n’existe pour l’adresse, un nouvel identifiant est créé.

>[!NOTE]
>
>Vous ne pouvez cibler qu’un seul type d’ID au sein d’un seul emplacement. Pour tester les performances par type d’ID, procédez comme suit : [créer un emplacement distinct ;](/help/dsp/campaign-management/placements/placement-create.md) pour chaque type d’identifiant dans le segment.

* *[!DNL RampID]:* Pour convertir des informations d’identification personnelles en [!DNL RampID]. Vous pouvez utiliser [!DNL RampIDs] pour le reciblage des utilisateurs qui se connectent et pour [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) mesure.

* *[!DNL Unified ID2.0](Version bêta) :* Pour convertir des informations d’identification personnelles en [ID unifié 2.0](https://unifiedid.com) ID pour le reciblage des utilisateurs qui se connectent.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Conditions d’utilisation pour la conversion des PII en identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les termes une fois avant de pouvoir convertir les données en un nouveau type d’ID. Pour les clients disposant de contrats de service géré, votre équipe de compte d’Adobe obtiendra votre consentement et acceptera les conditions pour le compte de votre organisation. Pour lire les termes, cliquez sur **>**. Pour accepter les termes, faites défiler l’écran jusqu’au bas des termes et cliquez sur **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Lecture seule ; généré automatiquement) Clé source que vous pouvez utiliser pour créer une connexion de destination dans la plateforme de données client afin de pousser les audiences vers le DSP de publicité. Vous pouvez copier la valeur dans le presse-papiers pour la coller dans les paramètres de connexion de destination ou dans un fichier.

>[!MORELIKETHIS]
>
>* [Création d’une source d’audience pour activer les audiences d’ID universelles](source-create.md)
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [Importation manuelle de segments authentifiés depuis [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP la connexion](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
