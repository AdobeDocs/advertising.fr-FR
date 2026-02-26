---
title: Personnaliser l’optimisation et la planification de la création pour une expérience
description: Découvrez comment configurer l’optimisation et la planification des annonces publicitaires pour les expériences sans ciblage.
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 24ae6f65552a2c958488be4f1363c08c3f387d37
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 0%

---

# Personnaliser l’optimisation créative et la planification d’une expérience sans ciblage d’arbre de décision

*Expériences avec des contenus publicitaires existants uniquement*

Par défaut, la rotation des créations pour une balise d’expérience publicitaire est déterminée par algorithme afin d’optimiser le taux de clic publicitaire global, et les paramètres d’optimisation des créations s’appliquent à toutes les créations attribuées. Vous pouvez personnaliser la rotation des contenus publicitaires afin de les exécuter manuellement en fonction du poids relatif ou de les optimiser par algorithme pour un objectif personnalisé Advertising DSP spécifié. Vous pouvez également planifier l’exécution de contenus publicitaires spécifiques pendant des périodes séquentielles spécifiées et appliquer des paramètres de rotation de contenu publicitaire personnalisés pour chaque planning.

## Configurer l’optimisation de la création sans planification

Lorsque la planification des créations est désactivée, les paramètres d’optimisation des créations s’appliquent à tous les créatifs affectés.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Effectuez l’une des opérations suivantes :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Tag Manager]**.

   * En mode Tableau, maintenez le curseur sur la ligne, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Tag Manager]**.

1. Placez le curseur sur la ligne de la balise d’annonce publicitaire applicable et cliquez sur ![Modifier l’optimisation de la création](/help/creative/assets/edit-gray.png "Modifier l’optimisation de la création") **[!UICONTROL Creative Optimization]**.&lt;!— Tag Manager n’a qu’une vue Liste, mais pas de vue Carte, à partir du 2/2. >

1. Désactivez **[!UICONTROL Schedule]**.

1. Sélectionnez le type de rotation de contenu créatif pour les variantes d’annonces dans les lots associés :

   * *[!UICONTROL Weighted]:* affiche les variantes d’annonces publicitaires dans les lots de contenu créatif associés en fonction des poids relatifs. Saisissez le poids de chaque lot sous la forme d’un pourcentage. Pour appliquer des poids égaux à tous les lots associés, cliquez sur (![Appliquer un poids égal](/help/creative/assets/apply-equal-weight.png "Appliquer un poids égal")). Le poids de tous les lots sélectionnés doit être égal à 100,<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->

   * *[!UICONTROL Algorithmic]:* affiche les variantes d’annonce publicitaire les plus efficaces plus souvent, en fonction d’un objectif spécifié.

      * Pour l’**[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]*, (expériences publicitaires vidéo standard) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:* affiche les lots de création associés dans un ordre spécifié (le lot 1 étant servi en premier, le lot 2 étant servi en deuxième, etc.), avec un nombre total spécifié d’impressions sur chaque séquence de lots. Les tailles des annonces diffusées sont déterminées par l’inventaire disponible. Vous pouvez configurer le lot final de la séquence pour qu’il s’affiche indéfiniment (valeur par défaut) ou qu’il reboucle sur le premier lot. Par exemple, vous pouvez afficher l’une des variantes d’annonce publicitaire de l’offre groupée 1 pour trois (3) impressions, puis afficher toute variante d’annonce publicitaire de l’offre groupée 2 pour une (1) impression, puis afficher l’une des variantes d’annonce publicitaire de l’offre groupée 3 pour deux (2) impressions, puis recommencer la boucle. Vous pouvez également continuer à afficher indéfiniment les variantes d’annonces du lot 3 une fois qu’elles sont affichées dans le lot 3, au lieu de créer une boucle. Lorsque vous activez le séquencement :

      1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

     Par défaut, les lots affectés sont séquencés dans l’ordre dans lequel ils ont été ajoutés à l’expérience.

      1. Saisissez le nombre d’impressions pour chaque séquence.

      1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Cliquez sur **[!UICONTROL Save]**.

## Configurer l’optimisation créative avec la planification créative

Vous pouvez éventuellement planifier l’exécution de contenus publicitaires spécifiques utilisés pour une balise d’expérience publicitaire pendant des périodes séquentielles spécifiées entre les dates de début et de fin de l’expérience, et appliquer des paramètres de rotation des contenus publicitaires personnalisés pour chaque planification. Par exemple, vous pouvez planifier l’exécution de Creative 1 pendant les deux premières semaines afin d’optimiser le taux de clic publicitaire et l’exécution de Creative 2 pendant les deux semaines suivantes pour optimiser l’objectif personnalisé spécifié.

Lorsque vous utilisez la planification, vous devez planifier les contenus publicitaires tout au long de l’expérience.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Effectuez l’une des opérations suivantes :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Tag Manager]**.

   * En mode Tableau, maintenez le curseur sur la ligne, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Tag Manager]**.

1. Placez le curseur sur la ligne de la balise d’annonce publicitaire applicable et cliquez sur ![Modifier l’optimisation de la création](/help/creative/assets/edit-gray.png "Modifier l’optimisation de la création") **[!UICONTROL Creative Optimization]**. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— Tag Manager n’a qu’une vue Liste, mais pas de vue Carte, à partir du 2/2. >

1. Activez **[!UICONTROL Schedule]**.

1. Pour le premier planning :

   1. Dans la colonne de gauche, cochez la case en regard de chaque élément créatif à ajouter au premier planning.

   1. Spécifiez la date et l’heure de début, ainsi que la date et l’heure de fin du planning.

   1. Sélectionnez le type de rotation de contenu créatif :

      * *[!UICONTROL Weighted]:* fait pivoter les contenus publicitaires manuellement en fonction des poids relatifs. Saisissez le poids de chaque contenu publicitaire sous la forme d’un pourcentage. Pour appliquer des poids égaux à tous les lots de la planification, cliquez sur (![Appliquer un poids égal](/help/creative/assets/apply-equal-weight.png "Appliquer un poids égal")). Le poids de tous les contenus publicitaires sélectionnés doit être égal à 100.

      * *[!UICONTROL Algorithmic]:* fait pivoter les contenus publicitaires de manière algorithmique en fonction d’un objectif d’optimisation spécifié.

         * Pour l’**[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]*, (expériences publicitaires vidéo standard) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un [objectif personnalisé Advertising DSP existant](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

      * *[!UICONTROL Sequencing]:* fait pivoter les lots de création associés dans un ordre spécifié (le lot 1 étant servi en premier, le lot 2 étant servi en deuxième, etc.), avec un nombre total spécifié d’impressions sur chaque séquence de lots. Les tailles des annonces diffusées sont déterminées par l’inventaire disponible. Vous pouvez configurer le lot final de la séquence pour qu’il s’affiche indéfiniment (valeur par défaut) ou qu’il reboucle sur le premier lot. Par exemple, vous pouvez afficher l’un des contenus publicitaires du lot 1 pour trois (3) impressions, puis afficher l’un des contenus publicitaires du lot 2 pour une (1) impression, puis afficher l’un des contenus publicitaires du lot 3 pour deux (2) impressions, et recommencer la boucle. Vous pouvez également continuer à afficher les contenus publicitaires du lot 3 indéfiniment une fois qu’ils sont affichés, au lieu de créer une boucle. Lorsque vous activez le séquencement :

         1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

            Par défaut, les lots affectés sont séquencés dans l’ordre dans lequel ils ont été ajoutés à l’expérience.

         1. Saisissez le nombre d’impressions pour chaque séquence.

         1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Pour chaque planning supplémentaire :

   1. Cliquez sur **[!UICONTROL + Add Schedule]**.

   1. Dans la colonne de gauche, cochez la case en regard de chaque élément créatif à ajouter au premier planning.

   1. Spécifiez les dates de début et de fin du planning.

   1. Sélectionnez le type de rotation de contenu créatif :

      * *[!UICONTROL Weighted]:* fait pivoter les contenus publicitaires manuellement en fonction des poids relatifs. Saisissez le poids de chaque contenu publicitaire sous la forme d’un pourcentage. Le poids de tous les contenus publicitaires sélectionnés doit être égal à 100.

      * *[!UICONTROL Algorithmic]:* fait pivoter les contenus publicitaires de manière algorithmique en fonction d’un objectif d’optimisation spécifié.

         * Pour le **[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*.  Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un [objectif personnalisé Advertising DSP existant](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

      * *[!UICONTROL Sequencing]:* fait pivoter les lots de création associés dans un ordre spécifié, avec un nombre total spécifié d’impressions sur chaque séquence de lots. Lorsque vous activez le séquencement :

         1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

            Par défaut, les lots affectés sont séquencés dans l’ordre dans lequel ils ont été ajoutés à l’expérience.

         1. Saisissez le nombre d’impressions pour chaque séquence.

         1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Créez manuellement une balise d’annonce publicitaire pour une taille de contenu créatif applicable](/help/creative/experiences/experience-tag-create-manually.md)
>* [Affecter des contenus publicitaires à une balise publicitaire pour des expériences sans ciblage](experience-tag-assign-creatives.md)
>* [Personnaliser les URL de tracking pour une expérience sans ciblage d’arborescence de décision](experience-tracking-urls-no-targeting.md)
