---
title: À propos des expériences dans Advertising Creative
description: Découvrez comment configurer des expériences publicitaires personnalisées et optimiser les éléments publicitaires en fonction des performances.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 9e9fe26213fb2d5e6aaffe6d9e4f1688efebc480
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 0%

---

# À propos des expériences dans Advertising Creative 2.0

Chaque expérience d’annonce publicitaire peut inclure un type d’annonce (affichage standard, vidéo standard ou affichage dynamique). [!DNL Advertising Creative 2.0] fournit deux structures d’expérience publicitaire différentes pour les publicités dans une seule bibliothèque de contenu créatif.

* **Expériences de ciblage d’arborescence de décision :** [!DNL Creative] vous permet de configurer des expériences publicitaires personnalisées dans l’ensemble du parcours client à l’aide d’un modèle d’arborescence de décision. Vous pouvez personnaliser tous les éléments publicitaires (images, titres, offres et pages de destination) en fonction de l’audience cible.

  Par exemple, vous pouvez spécifier le même lot de création pour les personnes de Chicago et de New York qui se trouvent dans un segment d’audience Adobe Analytics spécifique, mais qui envoient des personnes de Chicago vers des pages de destination différentes de celles de New Yorker. Vous pouvez également spécifier un lot différent pour les personnes du segment qui vivent n’importe où sauf à Chicago et New York, et un troisième lot pour les autres personnes qui ne se trouvent pas dans le segment.

  Les options de ciblage sont les suivantes :

   * Vos segments d’audience provenant de Adobe Audience Manager, Adobe Analytics et Advertising DSP ; tous les autres segments propriétaires importés pour le compte ; vos segments personnalisés provenant d’Advertising DSP ; les segments tiers fournis par Advertising DSP ; et toutes les audiences Advertising DSP existantes créées dans la bibliothèque d’audiences

   * Emplacements géographiques spécifiques, notamment les pays, les États, les DMA aux États-Unis, les villes et les codes postaux

   * Les visionneuses pour lesquelles des paires clé-valeur spécifiques (cibles de transmission de données) sont transmises par le DSP, l’éditeur ou le partenaire (SKU=01234567890123 ou Cart=vide, par exemple)

   * [!DNL Creative] le reciblage des pixels et des valeurs d’attribut spécifiées

   * Types d’appareils, systèmes d’exploitation et navigateurs spécifiques

  Une fois que vous avez créé une branche d’audience cible dans l’arborescence de décision, vous pouvez associer l’audience cible à des contenus publicitaires potentiels en attribuant des lots de contenu créatif à la branche. Pour chaque expérience, vous pouvez personnaliser l’optimisation et la planification des offres groupées de contenu créatif et modifier les pages de destination et les URL de suivi par défaut<!-- later: and any flexible attributes --> pour chaque contenu créatif de chaque offre groupée.

* **Expériences sans ciblage d’arborescence de décision :** [!DNL Creative] optimise les éléments publicitaires pour l’expérience publicitaire sans réduire l’audience. Pour chaque expérience, vous spécifiez des dates de début et de fin, ainsi que certains paramètres par défaut, mais la plupart des workflows ne sont pas directement liés à l’expérience. Au lieu d’ajouter directement des créatifs à l’expérience, utilisez [!UICONTROL Tag Manager] pour créer une balise d’annonce pour chaque taille d’annonce pour l’expérience, puis ajoutez des créatifs à l’expérience, configurez l’optimisation et la planification des créations et personnalisez les pages de destination et les URL de suivi<!-- later: and any flexible attributes -->.

>[!NOTE]
>
> Les deux types d’expériences ayant des workflows différents, vous ne pouvez pas modifier une expérience non ciblée en expérience ciblée ou une expérience ciblée en expérience non ciblée.

## Diffusion et optimisation des publicités

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative] diffuse des annonces propriétaires et déclenche des annonces tierces pour l’expérience en fonction des options d’objectif de ciblage (le cas échéant), de planification, de rotation des annonces et d’optimisation spécifiées, ainsi que de l’inventaire des annonces disponibles.

* **Planification :** (facultatif) planifiez l’exécution de contenus publicitaires spécifiques pendant des périodes séquentielles spécifiées.

* **Rotation de l’annonce publicitaire :** permet de faire pivoter les contenus publicitaires de manière algorithmique en fonction de l’objectif d’optimisation spécifié, d’une séquence de lots spécifiée ou de poids relatifs.

* **Objectif d’optimisation :** optimisez les éléments publicitaires pour obtenir le meilleur taux de clic publicitaire ou pour un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md)

  [!DNL Creative] optimise les expériences publicitaires en donnant un partage d’impression aux ressources les plus performantes de l’expérience. Pour les expériences ciblées sur des audiences spécifiques, les annonces peuvent être optimisées en fonction des performances des éléments d’annonce individuels des ensembles d’audiences cibles. Pour les expériences sans cibles d’audience spécifiques, les éléments publicitaires sont optimisés en fonction uniquement des performances des éléments publicitaires individuels.

Par exemple, vous pouvez planifier l’exécution de Creative 1 pendant les deux premières semaines afin d’optimiser le taux de clic publicitaire et l’exécution de Creative 2 pendant les deux semaines suivantes pour optimiser l’objectif personnalisé spécifié.

## Implémentation et gestion des expériences

Une fois que vous avez créé une expérience en direct (avec tous les éléments publicitaires requis), vous pouvez [générer une balise JavaScript ou iframe pour l’expérience entière](experience-tag-export.md). Vous pouvez charger la balise d’expérience en tant qu’annonce publicitaire dans une campagne dans Adobe Advertising DSP ou l’implémenter en tant qu’annonce publicitaire dans un DSP tiers.

>[!NOTE]
>
>Le comportement de ciblage hiérarchique peut varier en fonction du DSP. Advertising DSP applique le ciblage au niveau des annonces en plus du ciblage au niveau des emplacements.

## Données de performances pour vos expériences

Les données de performances disponibles sont les suivantes :

* Lorsque vous activez l’option [!UICONTROL Metrics] dans la vue [!UICONTROL Creative] > [!UICONTROL Experiences] , chaque carte ou ligne d’expérience indique le nombre d’impressions et de clics reçus par l’expérience.

  ![Option Mesures](/help/creative/assets/metrics-option.png "Option Mesures")

* Vous pouvez [afficher des données de performances détaillées pour n’importe quelle expérience](experience-performance-details.md) à partir de la vue [!UICONTROL Experiences].

* Pour surveiller les performances de l’ensemble de vos expériences, créez un [rapport Creative personnalisé](/help/creative/report-manage.md).

## Statuts des expériences {#experience-statuses}

Le statut d’une expérience est défini automatiquement, à l’exception de *Supprimé* que vous définissez manuellement.

| Statut | Description |
| ------ | ----------- |
| [!UICONTROL Live] | L’expérience comprend tous les éléments requis afin que vous puissiez générer une balise d’expérience à implémenter en tant qu’annonce publicitaire dans un DSP. Il est possible que le démarrage d’une expérience en direct soit planifié dans le futur. |
| [!UICONTROL Draft] | Toutes les branches de l’expérience ne sont pas dotées de contenu créatif. L’expérience est donc incomplète et vous ne pouvez pas générer de balise d’expérience. |
| [!UICONTROL Processing] | Une expérience précédemment active a été modifiée, mais elle est désormais incomplète. Vous ne pouvez pas générer de balise d’expérience pour cette tâche. **Remarque :** si vous avez déjà implémenté une balise d’expérience pour l’expérience, la version précédemment active peut toujours être diffusée. Si vous terminez l’expérience ultérieurement (en la rendant à nouveau active), la nouvelle version peut être diffusée à l’aide de l’implémentation de balise existante. |
| [!UICONTROL Deleted] | L’expérience a été supprimée de [!DNL Creative] et n’est plus visible dans les vues [!UICONTROL Experiences]. |

>[!NOTE]
>
>Vous pouvez modifier le statut d’une annonce publicitaire dans un DSP sans affecter le statut de l’expérience dans [!DNL Creative].

## La vue [!UICONTROL Experiences]

La vue [!UICONTROL Experiences] affiche toutes vos expériences ciblées et non ciblées. Vous pouvez voir les noms d’expérience, le statut, les dates de début et de fin, le nombre et les dimensions des contenus publicitaires ou créatifs attribués, et si l’expérience inclut des annonces dynamiques. Lorsque vous activez l’option [!UICONTROL Metrics] dans la vue [!UICONTROL Experiences], chaque carte ou ligne d’expérience indique le nombre d’impressions et de clics que l’expérience a reçus. Lorsque vous êtes en mode Carte, vous pouvez faire défiler les contenus publicitaires d’une expérience comportant plusieurs contenus publicitaires à l’aide des boutons &lt; et >.

Vous pouvez créer et gérer vos expériences, créer et renommer des balises d’expérience et exporter les balises aux formats JavaScript et iframe pour les implémenter sur vos DSP. Les annonceurs qui utilisent Advertising DSP ont la possibilité de charger des balises directement dans une campagne Advertising DSP.

### Actions disponibles

Voici les principales actions disponibles. Pour obtenir la liste complète, reportez-vous à la table des matières du chapitre Creatives > Expériences .

* [Télécharger des données dans la vue](experience-download-view.md)

* [Créer](/help/creative/experiences/experience-create-targeting.md) et [modifier](/help/creative/experiences/experience-edit-targeting.md) une expérience avec le ciblage

* [Créer](/help/creative/experiences/experience-create-no-targeting.md), [modifier](/help/creative/experiences/experience-edit-no-targeting.md) et [créer manuellement une balise d’annonce publicitaire](/help/creative/experiences/experience-tag-create-manually.md) pour une expérience sans ciblage

* [Cloner](experience-clone.md) une expérience

* [Aperçu](experience-preview.md) une expérience

* [Partager une URL de démonstration](experience-share-demo-url.md) pour une expérience

* [Exporter des balises de publicité pour une expérience](experience-tag-export.md), y compris éventuellement le chargement direct de balises de publicité dans une campagne Advertising DSP

* [Supprimer](experience-delete.md) une expérience

>[!MORELIKETHIS]
>
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Créer une expérience sans ciblage](experience-create-no-targeting.md)
