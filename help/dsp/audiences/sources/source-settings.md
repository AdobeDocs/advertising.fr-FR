---
title: Paramètres de la source d’audience
description: Découvrez les paramètres des sources d’audience.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Paramètres de la source d’audience

*Fonction Beta*

**[!UICONTROL Data Visibility Level]:** indique si les segments sont disponibles pour un seul annonceur ayant accès au compte (*[!UICONTROL Advertiser]*) ou pour tous les annonceurs ayant accès au compte *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (visibilité au niveau de l’annonceur uniquement) Annonceur pour lequel les segments sont disponibles. Sélectionnez-en un dans la liste des annonceurs ayant accès au compte.

**[!UICONTROL Enter IMS Org Id]:** (sources de [!DNL Real-Time CDP] uniquement) ID d’organisation Adobe Experience Cloud pour le compte [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** types d’ID auxquels vous convertirez vos informations d’identification personnelle (PII). Si vous sélectionnez plusieurs types, le segment généré est renseigné avec des valeurs pour chaque type d’identifiant sélectionné (par exemple un [!DNL RampID] et un [!DNL Unified ID2.0] pour chaque adresse e-mail). Les frais de données sont appliqués en conséquence.

Pour [!DNL RampID] et [!DNL Unified ID2.0], le fournisseur recherche chaque adresse e-mail pour voir si un ID existe déjà et traduit l’adresse en un ID correspondant le cas échéant. S’il n’existe pas d’ID pour l’adresse, un nouvel ID est créé.

>[!NOTE]
>
>Vous ne pouvez cibler qu’un seul type d’identifiant dans un seul emplacement. Pour tester les performances par type d’identifiant, [créez un emplacement distinct](/help/dsp/campaign-management/placements/placement-create.md) pour chaque type d’identifiant du segment.

* *[!DNL RampID]:* pour convertir des informations d’identification personnelles en [!DNL RampID]. Vous pouvez utiliser [!DNL RampIDs] pour recibler les utilisateurs connectés et pour mesurer les [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0](Beta) :* pour convertir les informations d’identification personnelles en un [identifiant unifié 2.0](https://unifiedid.com) pour le reciblage des utilisateurs connectés.

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Conditions d’utilisation de la conversion des informations d’identification personnelles en identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les conditions une seule fois avant de pouvoir convertir des données en un nouveau type d’identifiant. Pour les clients qui disposent de contrats de service géré, l’équipe chargée de votre compte Adobe obtiendra votre consentement et acceptera les conditions au nom de votre entreprise. Pour lire les termes, cliquez sur **>**. Pour accepter les conditions, faites défiler l’écran jusqu’au bas des conditions et cliquez sur **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Lecture seule ; générée automatiquement) Clé source que vous pouvez utiliser pour créer une connexion de destination dans la plateforme de données client afin de pousser les audiences vers Advertising DSP. Vous pouvez copier la valeur dans le presse-papiers pour la coller dans les paramètres de connexion de destination ou dans un fichier.

>[!MORELIKETHIS]
>
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](source-manage.md)
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [Importer manuellement des segments authentifiés depuis  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Connexion Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
