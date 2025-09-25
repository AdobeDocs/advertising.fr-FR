---
title: Workflows pour les publicités dynamiques
description: Découvrez les workflows de gestion des annonces dynamiques.
feature: Creative Dynamic Creatives
source-git-commit: 6f2f6580e8d4fc11f52a97b086ce453e423ab4e6
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Workflows pour les publicités dynamiques

*Utilisateurs autorisés à créer des annonces dynamiques*

Vous pouvez configurer des annonces dynamiques de deux manières :

* Processus 1 : chargez un modèle d’annonce publicitaire et un catalogue de variantes d’annonces directement dans les paramètres d’annonce dynamique lorsque vous ajoutez des annonces dynamiques à une bibliothèque de contenu créatif. Vous pouvez télécharger un modèle de flux existant pour créer le catalogue.

  Utilisez ce workflow lorsque la même personne peut fournir toutes les informations (à l’exception du modèle de flux) pour créer les annonces. Les fichiers chargés restent disponibles pour une utilisation ultérieure.

* Workflow 2 : configurez un modèle d’annonce publicitaire et des catalogues de variantes d’annonce publicitaire dans des vues distinctes, puis ajoutez séparément des annonces dynamiques à un contenu publicitaire à l’aide du modèle d’annonce publicitaire et des catalogues déjà disponibles.

  Utilisez ce workflow lorsque différentes personnes doivent effectuer différentes tâches ou lorsque vous ne souhaitez effectuer qu’une seule tâche à la fois.

## Workflow 1

>[!PREREQUISITES]
>
>* Modèles publicitaires au format HTML5
>* Catalogues de produits au format CSV, TSV ou feuille de calcul Microsoft Excel (XLSX)

1. [Créer des contenus publicitaires dynamiques](/help/creative/creative-libraries/creative-add-dynamic.md) pour une bibliothèque de contenus publicitaires. Pour les publicités dynamiques d’HTML5, chargez un modèle de publicité et des catalogues.

1. Utilisez les contenus publicitaires dynamiques pour créer des expériences publicitaires :

   1. [Créez des offres groupées d’annonces dynamiques](/help/creative/creative-libraries/bundle-manage.md) que vous pouvez joindre en une seule fois à une expérience publicitaire.

   1. Créez des expériences publicitaires dynamiques [avec ciblage](/help/creative/experiences/experience-create-targeting.md) ou [sans ciblage](/help/creative/experiences/experience-create-no-targeting.md) et [affectez les bundles de création aux expériences](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Générez et implémentez des balises d’expérience publicitaire](/help/creative/experiences/experience-tag-export.md) pour les exécuter en tant que publicités dans votre DSP.

      Pour utiliser une expérience d’annonce publicitaire comme annonce publicitaire dans Adobe Advertising DSP, chargez la balise d’expérience publicitaire dans une campagne Advertising DSP. Pour utiliser une expérience d’annonce publicitaire comme annonce publicitaire dans un autre DSP, implémentez la balise d’expérience publicitaire dans ce DSP.

## Workflow 2

1. [Créez un modèle d’annonce publicitaire](/help/creative/ad-templates/ad-template-manage.md) pour vos annonces dynamiques en fonction des ressources disponibles.

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

1. Utilisez les contenus publicitaires dynamiques pour créer des expériences publicitaires :

   1. [Créez des offres groupées d’annonces dynamiques](/help/creative/creative-libraries/bundle-manage.md) que vous pouvez joindre en une seule fois à une expérience publicitaire.

   1. Créez des expériences publicitaires dynamiques [avec ciblage](/help/creative/experiences/experience-create-targeting.md) ou [sans ciblage](/help/creative/experiences/experience-create-no-targeting.md) et [affectez les bundles de création aux expériences](/help/creative/experiences/experience-assign-creative-bundles.md).

   1. [Générez et implémentez des balises d’expérience publicitaire](/help/creative/experiences/experience-tag-export.md) pour les exécuter en tant que publicités dans votre DSP.

      Pour utiliser une expérience d’annonce publicitaire comme annonce publicitaire dans Adobe Advertising DSP, chargez la balise d’expérience publicitaire dans une campagne Advertising DSP. Pour utiliser une expérience d’annonce publicitaire comme annonce publicitaire dans un autre DSP, implémentez la balise d’expérience publicitaire dans ce DSP.
