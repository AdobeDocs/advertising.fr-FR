---
title: Workflow pour les publicités dynamiques
description: Découvrez le workflow de gestion des annonces dynamiques.
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Workflow pour les publicités dynamiques

1. [Créez un modèle d’annonce publicitaire](/help/creative/ad-templates/ad-template-manage.md) pour vos annonces dynamiques en fonction des ressources disponibles

1. Configurez vos éléments publicitaires :

   * (Pour les publicités HTML5 statiques uniques) Collectez et [chargez les ressources d’image](/help/creative/feeds/asset-manage.md) pour vos publicités.

   * (Pour les publicités dynamiques d’HTML5) Créez des catalogues de vos éléments publicitaires :

      1. Créez un fichier de flux au format de feuille de calcul Microsoft Excel (XLSX), avec une ligne pour chaque variation publicitaire. Incluez un nom d’image ou une référence à un Adobe Experience Manager dans chaque ligne. Collectez séparément les ressources d’image associées.

      1. [Chargez le fichier de flux et les ressources d’image](/help/creative/feeds/asset-manage.md).

      1. [Créez un modèle de flux](/help/creative/feeds/feed-template-manage.md) pour mapper les champs de votre fichier de flux (feuille de calcul) aux champs du serveur principal d’Advertising Creative.

      1. [Créez un catalogue](/help/creative/feeds/catalog-manage.md#feed-catalog-create) à partir d’un fichier de flux spécifié et d’un modèle de flux spécifié, puis [traitez le catalogue](/help/creative/feeds/catalog-manage.md#feed-catalog-process) pour afficher les variations de publicité qui peuvent être créées à partir de celui-ci.

         Vous ne pouvez utiliser chaque fichier de flux que pour un seul catalogue.

         Vous pouvez [suivre le statut des tâches de traitement du catalogue](/help/creative/feeds/job-status-track.md) sur l’onglet [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status] .

1. [Créer des contenus publicitaires dynamiques](/help/creative/creative-libraries/creative-add-dynamic.md) pour une bibliothèque de contenus publicitaires. Pour les annonces HTML5 dynamiques, utilisez un modèle d’annonce spécifié et des catalogues spécifiés.

1. [Créez des offres groupées d’annonces dynamiques](/help/creative/creative-libraries/bundle-manage.md) que vous pouvez joindre en une seule fois à une expérience publicitaire.

1. Créez des expériences publicitaires dynamiques [avec ciblage](/help/creative/experiences/experience-create-targeting.md) ou [sans ciblage](/help/creative/experiences/experience-create-no-targeting.md) et [affectez les bundles de création aux expériences](/help/creative/experiences/experience-assign-creative-bundles.md).

1. [Générez et implémentez des balises d’expérience publicitaire](/help/creative/experiences/experience-tag-export.md) pour les exécuter en tant que publicités dans votre DSP.

   Pour utiliser une expérience d’annonce publicitaire comme annonce publicitaire dans Adobe Advertising DSP, chargez la balise d’expérience publicitaire dans une campagne Advertising DSP. Pour utiliser une expérience d’annonce publicitaire comme annonce publicitaire dans un autre DSP, implémentez la balise d’expérience publicitaire dans ce DSP.
