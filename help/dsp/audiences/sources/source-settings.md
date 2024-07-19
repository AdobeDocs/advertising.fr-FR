---
title: Paramètres d’Audience Source
description: Découvrez les paramètres des sources d’audience.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Paramètres d’Audience Source

*Fonctionnalité Beta*

**[!UICONTROL Data Visibility Level]:** Indique si les segments sont disponibles pour un seul annonceur ayant accès au compte (*[!UICONTROL Advertiser]*) ou pour tous les annonceurs ayant accès au compte *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Visibilité au niveau de l’annonceur uniquement) L’annonceur pour lequel les segments sont disponibles. Sélectionnez-en un dans la liste des annonceurs ayant accès au compte.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] sources uniquement) ID d’organisation Adobe Experience Cloud pour le compte [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** Types d’ID dans lesquels vous convertirez vos informations d’identification personnelle (PII). Si vous sélectionnez plusieurs types, le segment généré est renseigné avec des valeurs pour chaque type d’ID sélectionné (par exemple, [!DNL RampID] et [!DNL Unified ID2.0] pour chaque adresse électronique). Les taxes sur les données sont appliquées en conséquence.

Pour [!DNL RampID] et [!DNL Unified ID2.0], le fournisseur recherche chaque adresse électronique pour voir si un ID existe déjà et convertit l’adresse en un ID correspondant le cas échéant. Si aucun identifiant n’existe pour l’adresse, un nouvel identifiant est créé.

>[!NOTE]
>
>Vous ne pouvez cibler qu’un seul type d’ID au sein d’un seul emplacement. Pour tester les performances par type d’identifiant, [ créez un emplacement](/help/dsp/campaign-management/placements/placement-create.md) distinct pour chaque type d’identifiant dans le segment.

* *[!DNL RampID]:* Pour convertir les PII en [!DNL RampID]. Vous pouvez utiliser [!DNL RampIDs] pour recibler les utilisateurs qui se connectent et pour la mesure [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0](Beta) :* Pour convertir les PII en [ ID unifié 2.0](https://unifiedid.com) pour recibler les utilisateurs qui se connectent.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Conditions d’utilisation pour la conversion des PII en identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les termes une fois avant de pouvoir convertir les données en un nouveau type d’ID. Pour les clients disposant de contrats de service géré, votre équipe de compte d’Adobe obtiendra votre consentement et acceptera les conditions pour le compte de votre organisation. Pour lire les termes, cliquez sur **>**. Pour accepter les termes, faites défiler l’écran jusqu’au bas des termes et cliquez sur **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Lecture seule ; généré automatiquement) clé source que vous pouvez utiliser pour créer une connexion de destination dans la plateforme de données client afin de pousser des audiences vers Advertising DSP. Vous pouvez copier la valeur dans le presse-papiers pour la coller dans les paramètres de connexion de destination ou dans un fichier.

>[!MORELIKETHIS]
>
>* [Gérer les sources d’audience pour activer les audiences d’ID universels](source-manage.md)
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [ Importation manuelle de segments authentifiés à partir de  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP la connexion](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)
