---
title: À propos des expériences dans Advertising Creative
description: Découvrez comment configurer des expériences publicitaires personnalisées et optimiser les éléments publicitaires en fonction des performances.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 0a6cd8e32ae87c7fda9ed0e1b50f9b54cd337192
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# À propos des expériences dans Advertising Creative 2.0

*Version bêta fermée*

<!-- Revisit Description metadata  -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] fournit deux structures d’expérience publicitaire différentes pour les publicités d’une bibliothèque de contenu créatif <!-- can use a single library only --> :

* **Expériences de ciblage d’arborescence de décision :** [!DNL Creative] vous permet de configurer des expériences publicitaires personnalisées dans l’ensemble du parcours client à l’aide d’un modèle d’arborescence de décision. Vous pouvez personnaliser tous les éléments publicitaires (images, titres, offres et pages de destination) en fonction de l’audience cible.

  Par exemple, vous pouvez spécifier le même lot de création pour les personnes de Chicago et de New York qui se trouvent dans un segment d’audience Adobe Analytics spécifique, mais qui envoient des personnes de Chicago vers des pages de destination différentes de celles de New Yorker. Vous pouvez également spécifier un lot différent pour les personnes du segment qui vivent n’importe où sauf à Chicago et New York, et un troisième lot pour les autres personnes qui ne se trouvent pas dans le segment.

  Les options de ciblage sont les suivantes :

   * Vos segments d’audience propriétaires depuis Adobe Audience Manager, Adobe Analytics et Advertising Cloud DSP

   * Emplacements géographiques spécifiques, notamment les pays, les États, les DMA aux États-Unis, les villes et les codes postaux

   * Visionneuses pour lesquelles des paires clé-valeur spécifiques (cibles de transmission de données) sont transmises par le DSP, l’éditeur ou le partenaire

   * [!DNL Creative] le reciblage des pixels et des valeurs d’attribut spécifiées

   * Types d’appareils, systèmes d’exploitation et navigateurs spécifiques

  Vous pouvez affecter des lots créatifs à chaque expérience. Pour chaque expérience, vous pouvez personnaliser l’optimisation et la planification des offres groupées de contenu créatif et modifier les pages de destination et les URL de suivi par défaut<!-- and any flexible attributes --> pour chaque contenu créatif de chaque offre groupée.

* **Expériences sans ciblage d’arborescence de décision :** [!DNL Creative] optimise les éléments publicitaires pour l’expérience publicitaire sans réduire l’audience.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> Pour chaque expérience, vous spécifiez des dates de début et de fin, ainsi que certains paramètres par défaut, mais la plupart des workflows ne sont pas directement liés à l’expérience. Au lieu d’ajouter directement des contenus publicitaires à l’expérience, utilisez [!UICONTROL Tag Manager] pour créer une balise d’annonce pour chaque taille d’annonce pour l’expérience, puis ajoutez des contenus publicitaires à l’expérience, configurez l’optimisation et la planification des contenus créatifs et personnalisez les pages de destination et les URL de suivi.

## Optimisation des publicités

<!-- MORE -->
[!DNL Creative] optimise les éléments publicitaires pour toute expérience en fonction des performances. Pour les expériences ciblées sur des audiences spécifiques, les annonces peuvent être optimisées en fonction des performances des éléments d’annonce individuels des ensembles d’audiences cibles. Pour les expériences sans cibles d’audience spécifiques, les éléments publicitaires sont optimisés en fonction uniquement des performances des éléments publicitaires individuels.

## Implémentation et gestion des expériences

Une fois une expérience en direct créée (avec tous les éléments publicitaires requis), vous pouvez [générer une balise JavaScript ou iframe pour l’ensemble de l’expérience](experience-tag-export.md). Vous pouvez charger la balise d’expérience en tant qu’annonce publicitaire dans une campagne dans Adobe Advertising DSP ou l’implémenter en tant qu’annonce publicitaire dans un DSP tiers. [!DNL Creative] diffuse des annonces pour l’expérience en fonction des options de ciblage et de rotation des annonces, ainsi que de l’inventaire des annonces disponibles.

## Données de performances pour vos expériences

Lorsque vous activez l’option [!UICONTROL Metrics] dans la vue [!UICONTROL Creative] > [!UICONTROL Experiences] , chaque carte ou ligne d’expérience indique le nombre d’impressions et de clics reçus par l’expérience.

![Option Mesures](/help/creative/assets/metrics-option.png "Option Mesures")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

Vous pouvez [afficher des données de performances détaillées pour n’importe quelle expérience](experience-performance-details.md) à partir de la vue [!UICONTROL Experiences].

Pour surveiller les performances de l’ensemble de vos expériences, créez un [rapport Creative personnalisé](/help/creative/report-custom-creative.md).

## Statuts des expériences {#experience-statuses}

<!-- verify that these are all still the same -->

Le statut d’une expérience est défini automatiquement, à l’exception de *supprimé* que vous définissez manuellement.

*En direct :* l’expérience comprend tous les éléments requis. Vous pouvez donc générer une balise d’expérience à implémenter en tant qu’annonce publicitaire dans un DSP. <!-- A live experience may be scheduled to start in the future -->

*Brouillon :* aucune composante créative n’est affectée aux branches de l’expérience. L’expérience est donc incomplète et vous ne pouvez pas générer de balise d’expérience.

*Traitement :* une expérience précédemment active a été modifiée, mais elle est désormais incomplète. Vous ne pouvez pas générer de balise d’expérience pour cette tâche. **Remarque :** si vous avez déjà implémenté une balise d’expérience pour l’expérience, la version précédemment active peut toujours être diffusée. Si vous terminez l’expérience ultérieurement (en la rendant à nouveau active), la nouvelle version peut être diffusée à l’aide de l’implémentation de balise existante.

*Supprimé :* l’expérience a été supprimée de [!DNL Creative] et n’est plus visible dans les vues [!UICONTROL Experiences].

>[!NOTE]
>
>Vous pouvez modifier le statut d’une annonce publicitaire dans un DSP sans affecter le statut de l’expérience dans [!DNL Creative].

## La vue [!UICONTROL Experiences]

La vue [!UICONTROL Experiences] affiche toutes vos expériences ciblées et non ciblées. Vous pouvez voir les noms d’expérience, le statut, les dates de début et de fin, le nombre et les dimensions des contenus publicitaires ou créatifs attribués, et si l’expérience inclut des annonces dynamiques. Lorsque vous activez l’option [!UICONTROL Metrics] dans la vue [!UICONTROL Experiences], chaque carte ou ligne d’expérience indique le nombre d’impressions et de clics que l’expérience a reçus.

Vous pouvez créer et gérer vos expériences , y compris l’optimisation et l’affectation de contenus créatifs et de bundles de création à vos expériences. Vous pouvez également créer et renommer des balises d’expérience et exporter les balises aux formats JavaScript et iframe pour les implémenter sur vos DSP. Les annonceurs qui utilisent Advertising DSP ont la possibilité de charger des balises directement dans une campagne Advertising DSP sous forme de publicités.

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Créer une expérience sans ciblage](experience-create-no-targeting.md)
