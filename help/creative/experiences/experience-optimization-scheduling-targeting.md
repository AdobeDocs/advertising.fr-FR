---
title: Personnaliser l’optimisation et la planification de la création pour une expérience
description: Découvrez comment
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '1073'
ht-degree: 0%

---

# Personnaliser l’optimisation créative et la planification d’une expérience avec le ciblage de l’arborescence de décision

*Nœuds Target avec contenu publicitaire existant uniquement*

Par défaut, la rotation des créations pour une expérience est déterminée par algorithme pour optimiser le taux de clic publicitaire global, et les paramètres d’optimisation des créations s’appliquent à tous les lots affectés. Vous pouvez personnaliser la rotation des créations pour exécuter manuellement les créations de chaque lot afin de les optimiser par algorithme pour un objectif personnalisé Advertising DSP spécifié ; selon une séquence de lots spécifiée, avec un nombre spécifié d’impressions sur chaque séquence de lots ; ou selon des poids relatifs. Vous pouvez également planifier l’exécution de lots de contenu créatif spécifiques pendant des périodes séquentielles spécifiées et appliquer des paramètres de rotation de contenu créatif personnalisés pour chaque planification.

>[!NOTE]
>
>Ces fonctionnalités ne sont pas disponibles pour les nœuds qui utilisent les contenus publicitaires par défaut au lieu des contenus publicitaires attribués.

## Configurer l’optimisation de la création sans planification

Lorsque la planification des créations est désactivée, les paramètres d’optimisation des créations s’appliquent à tous les créatifs affectés.

1. Placez le curseur au-dessus du nœud feuille de création sous le nœud cible, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Désactivez **[!UICONTROL Schedule]**.

1. Sélectionnez le type de rotation de contenu créatif :

   * *[!UICONTROL Weighted]:* Fait pivoter manuellement les contenus publicitaires de chaque lot en fonction de leur poids relatif. Saisissez le poids de chaque lot sous la forme d’un pourcentage. Le poids de tous les lots doit être égal à 100.

   * *[!UICONTROL Algorithmic]:* Fait pivoter les contenus publicitaires de chaque lot de manière algorithmique en fonction d’un objectif d’optimisation spécifié.

      * Pour l’**[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]*, (expériences publicitaires vidéo standard) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:* fait pivoter les lots de création associés dans un ordre spécifié (le lot 1 étant servi en premier, le lot 2 étant servi en deuxième, etc.), avec un nombre total spécifié d’impressions sur chaque séquence de lots. Les tailles des annonces diffusées sont déterminées par l’inventaire disponible. Vous pouvez configurer le lot final de la séquence pour qu’il s’affiche indéfiniment (valeur par défaut) ou qu’il reboucle sur le premier lot. Par exemple, vous pouvez afficher l’un des contenus publicitaires du lot 1 pour trois (3) impressions, puis afficher l’un des contenus publicitaires du lot 2 pour une (1) impression, puis afficher l’un des contenus publicitaires du lot 3 pour deux (2) impressions, et recommencer la boucle. Vous pouvez également continuer à afficher les contenus publicitaires du lot 3 indéfiniment une fois qu’ils sont affichés, au lieu de créer une boucle. Lorsque vous activez le séquencement :

      1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

     Par défaut, les lots affectés sont séquencés dans l’ordre dans lequel ils ont été ajoutés à l’expérience.

      1. Saisissez le nombre d’impressions pour chaque séquence.

      1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Cliquez sur **[!UICONTROL Save]**.

## Configurer l’optimisation créative avec la planification créative

Vous pouvez éventuellement planifier l’exécution de lots de contenu créatif spécifiques pendant des périodes séquentielles spécifiées entre les dates de début et de fin de l’expérience, et appliquer des paramètres de rotation de contenu créatif personnalisés pour chaque planification. Par exemple, vous pouvez planifier l’exécution du bundle 1 pendant les deux premières semaines afin d’optimiser le taux de clic publicitaire et l’exécution du bundle 2 pendant les deux semaines suivantes afin d’optimiser pour un objectif personnalisé spécifié.

Lorsque vous utilisez la planification, vous devez planifier les lots pendant toute la durée de l’expérience.

1. Placez le curseur au-dessus du nœud feuille de création sous le nœud cible, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Activez **[!UICONTROL Schedule]**.

1. Pour le premier planning :

   1. Dans la colonne de gauche, cochez la case en regard de chaque lot de contenu créatif à ajouter au premier planning.

   1. Spécifiez les dates de début et de fin du planning.

   1. Sélectionnez le type de rotation de contenu créatif :

      * *[!UICONTROL Weighted]:* Fait pivoter manuellement les contenus publicitaires de chaque lot en fonction de leur poids relatif. Saisissez le poids de chaque lot sous la forme d’un pourcentage. Le poids de tous les lots sélectionnés doit être égal à 100.

      * *[!UICONTROL Algorithmic]:* Fait pivoter les contenus publicitaires de chaque lot de manière algorithmique en fonction d’un objectif d’optimisation spécifié.

         * Pour l’**[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]*, (expériences publicitaires vidéo standard) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* fait pivoter les lots de création associés dans un ordre spécifié (le lot 1 étant servi en premier, le lot 2 étant servi en deuxième, etc.), avec un nombre total spécifié d’impressions sur chaque séquence de lots. Les tailles des annonces diffusées sont déterminées par l’inventaire disponible. Vous pouvez configurer le lot final de la séquence pour qu’il s’affiche indéfiniment (valeur par défaut) ou qu’il reboucle sur le premier lot. Par exemple, vous pouvez afficher l’un des contenus publicitaires du lot 1 pour trois (3) impressions, puis afficher l’un des contenus publicitaires du lot 2 pour une (1) impression, puis afficher l’un des contenus publicitaires du lot 3 pour deux (2) impressions, et recommencer la boucle. Vous pouvez également continuer à afficher les contenus publicitaires du lot 3 indéfiniment une fois qu’ils sont affichés, au lieu de créer une boucle. Lorsque vous activez le séquencement :

         1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

            Par défaut, les lots affectés sont séquencés dans l’ordre dans lequel ils ont été ajoutés à l’expérience.

         1. Saisissez le nombre d’impressions pour chaque séquence.

         1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Pour chaque planning supplémentaire :

   1. Cliquez sur **[!UICONTROL + Add Schedule]**.

   1. Dans la colonne de gauche, cochez la case en regard de chaque lot de contenu créatif à ajouter au premier planning.

   1. Spécifiez les dates de début et de fin du planning.

   1. Sélectionnez le type de rotation de contenu créatif :

      * *[!UICONTROL Weighted]:* Fait pivoter manuellement les contenus publicitaires de chaque lot en fonction de leur poids relatif. Saisissez le poids de chaque lot sous la forme d’un pourcentage. Le poids de tous les lots sélectionnés doit être égal à 100.

      * *[!UICONTROL Algorithmic]:* Fait pivoter les contenus publicitaires de chaque lot de manière algorithmique en fonction d’un objectif d’optimisation spécifié.

         * Pour le **[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* fait pivoter les lots de création associés dans un ordre spécifié, avec un nombre total spécifié d’impressions sur chaque séquence de lots. Lorsque vous activez le séquencement :

         1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

            Par défaut, les lots affectés sont séquencés dans l’ordre dans lequel ils ont été ajoutés à l’expérience.

         1. Saisissez le nombre d’impressions pour chaque séquence.

         1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Affectez et annulez l’affectation des lots de contenu créatif à un nœud final d’une expérience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personnaliser les URL de tracking pour les créatifs](/help/creative/experiences/experience-tracking-urls-targeting.md)
