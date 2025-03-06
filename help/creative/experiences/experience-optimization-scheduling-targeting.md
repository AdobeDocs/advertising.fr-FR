---
title: Personnaliser l’optimisation et la planification de la création pour une expérience
description: Découvrez comment
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 4abb83d08a6633c36aa47b5acd67df3d4cc0923b
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# Personnaliser l’optimisation créative et la planification d’une expérience avec le ciblage de l’arborescence de décision

*Nœuds Target avec contenu publicitaire existant uniquement*
*Version bêta fermée*

Par défaut, la rotation des créations pour une expérience est déterminée par algorithme pour optimiser le taux de clic publicitaire global, et les paramètres d’optimisation des créations s’appliquent à tous les lots affectés. Vous pouvez personnaliser la rotation des créations pour exécuter manuellement les créations de chaque lot en fonction des poids relatifs ou pour les optimiser par algorithme pour un objectif personnalisé Advertising DSP spécifié. Vous pouvez également planifier l’exécution de lots de contenu créatif spécifiques pendant des périodes séquentielles spécifiées et appliquer des paramètres de rotation de contenu créatif personnalisés pour chaque planification.

>[!NOTE]
>
>Ces fonctionnalités ne sont pas disponibles pour les nœuds qui utilisent les contenus publicitaires d’image par défaut au lieu des contenus publicitaires attribués.

## Configurer l’optimisation de la création sans planification

Lorsque la planification des créations est désactivée, les paramètres d’optimisation des créations s’appliquent à tous les créatifs affectés.

1. Placez le curseur au-dessus du nœud feuille de création sous le nœud cible, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Désactivez **[!UICONTROL Schedule]**.

1. Sélectionnez le type de rotation de contenu créatif :

   * *[!UICONTROL Weighted]:* Fait pivoter manuellement les contenus publicitaires de chaque lot en fonction de leur poids relatif. Saisissez le poids de chaque lot sous la forme d’un pourcentage. Le poids de tous les lots doit être égal à 100.

   * *[!UICONTROL Algorithmic]:* Fait pivoter les contenus publicitaires de chaque lot de manière algorithmique en fonction d’un objectif d’optimisation spécifié.

      * Pour le **[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

1. Cliquez sur **[!UICONTROL Save]**.

## Configurer l’optimisation créative avec la planification créative

Vous pouvez éventuellement planifier l’exécution de lots de contenu créatif spécifiques pendant des périodes séquentielles spécifiées entre les dates de début et de fin de l’expérience, et appliquer des paramètres de rotation de contenu créatif personnalisés pour chaque planification. Par exemple, vous pouvez planifier l’exécution du bundle 1 pendant les deux premières semaines afin d’optimiser le taux de clic publicitaire et l’exécution du bundle 2 pendant les deux semaines suivantes afin d’optimiser pour un objectif personnalisé spécifié.

Lorsque vous utilisez la planification, vous devez planifier les lots pendant toute la durée de l’expérience.

1. Placez le curseur au-dessus du nœud feuille de création sous le nœud cible, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Activez **[!UICONTROL Schedule]**.

1. Pour le premier planning :

   1. Dans la colonne de gauche, cochez la case en regard de chaque lot de contenu créatif à ajouter au premier planning.

   1. Spécifiez les dates de début et de fin du planning.

   1. Sélectionnez le type de rotation de contenu créatif :

      * *[!UICONTROL Weighted]:* Fait pivoter manuellement les contenus publicitaires de chaque lot en fonction de leur poids relatif. Saisissez le poids de chaque lot sous la forme d’un pourcentage. Le poids de tous les lots sélectionnés doit être égal à 100.

      * *[!UICONTROL Algorithmic]:* Fait pivoter les contenus publicitaires de chaque lot de manière algorithmique en fonction d’un objectif d’optimisation spécifié.

         * Pour le **[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

1. Pour chaque planning supplémentaire :

   1. Cliquez sur **[!UICONTROL + Add Schedule]**.

   1. Dans la colonne de gauche, cochez la case en regard de chaque lot de contenu créatif à ajouter au premier planning.

   1. Spécifiez les dates de début et de fin du planning.

   1. Sélectionnez le type de rotation de contenu créatif :

      * *[!UICONTROL Weighted]:* Fait pivoter manuellement les contenus publicitaires de chaque lot en fonction de leur poids relatif. Saisissez le poids de chaque lot sous la forme d’un pourcentage. Le poids de tous les lots sélectionnés doit être égal à 100.

      * *[!UICONTROL Algorithmic]:* Fait pivoter les contenus publicitaires de chaque lot de manière algorithmique en fonction d’un objectif d’optimisation spécifié.

         * Pour le **[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Affectez et annulez l’affectation des lots de contenu créatif à un nœud final d’une expérience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personnaliser les URL de tracking pour les créatifs](/help/creative/experiences/experience-tracking-urls-targeting.md)
