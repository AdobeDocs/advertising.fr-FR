---
title: Personnaliser l’optimisation et la planification de la création pour une expérience
description: Découvrez comment configurer l’optimisation et la planification des annonces publicitaires pour les expériences ciblées.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%
---
# Personnaliser l’optimisation créative et la planification d’une expérience avec le ciblage de l’arborescence de décision

*Nœuds Target avec contenu publicitaire existant uniquement*

Par défaut, une expérience optimise la rotation créative pour le taux de clic publicitaire global sur tous les lots affectés. Vous pouvez personnaliser les paramètres de rotation ou planifier des lots spécifiques à exécuter pendant des périodes séquentielles, avec des paramètres de rotation distincts pour chaque planification.

>[!NOTE]
>
>Ces fonctionnalités ne sont pas disponibles pour les nœuds qui utilisent les contenus publicitaires par défaut au lieu des contenus publicitaires attribués.

Vous pouvez configurer ces paramètres directement dans la zone de travail de l’éditeur piloté par l’IA (Beta) ou dans l’éditeur manuel. Dans l’un ou l’autre des éditeurs, l’enregistrement de la boîte de dialogue met à jour l’arborescence de travail. Vous devez également [enregistrer l’expérience](#save) à partir de l’en-tête de l’arborescence.

## Paramètres de rotation {#rotation-settings}

* **[!UICONTROL Weighted]:** affiche les variantes d’annonces publicitaires dans les lots de contenu créatif associés en fonction des poids relatifs.

* **[!UICONTROL Algorithmic]:** affiche plus souvent les variantes d’annonce publicitaire les plus efficaces, en fonction d’un objectif d’optimisation spécifié, tel que le taux de clic publicitaire ou un objectif personnalisé Advertising DSP.

* **[!UICONTROL Sequence] (éditeur piloté par l’IA) ou [!UICONTROL Sequencing] (éditeur manuel) :** affiche les lots de création associés dans un ordre spécifié, avec un nombre spécifié d’impressions pour chaque lot de la séquence. Par défaut, les lots sont séquencés dans l’ordre dans lequel ils ont été ajoutés à l’expérience. Les tailles des annonces diffusées sont déterminées par l’inventaire disponible. Le lot final peut servir indéfiniment (valeur par défaut) ou la séquence peut revenir au premier lot.

  Par exemple, une séquence peut servir de variantes d’annonces du lot 1 pour trois impressions, du lot 2 pour une impression et du lot 3 pour deux impressions, puis se répéter. Sans bouclage, le lot 3 continue à servir indéfiniment.

## Configurer l’optimisation de la création sans planification

Lorsque la planification des créations est désactivée, les paramètres d’optimisation des créations s’appliquent à tous les créatifs affectés.

### Utilisation de l’éditeur piloté par l’IA (Beta) {#without-scheduling-ai}

1. Pendant que vous [créez](experience-create-targeting.md#ai-editor) ou [modifiez](experience-edit-targeting.md#ai-editor) l’expérience, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** dans le nœud de page de création.

   Pour un dernier nœud sans lots, cliquez d’abord sur **[!UICONTROL Assign Bundles]** et [affectez les lots](experience-assign-creative-bundles.md#ai-editor).

1. Ouvrez l’onglet **[!UICONTROL Creative optimisation]** .

1. Désactivez **[!UICONTROL Schedule]**.

1. Sélectionnez le type de rotation de contenu créatif et configurez ses paramètres :

   * **[!UICONTROL Weighted]:** permet de saisir le poids relatif de chaque ligne de lot. Les poids doivent totaliser 100. Pour répartir équitablement les poids, cliquez sur **[!UICONTROL Apply equal weight]**.

   * **[!UICONTROL Algorithmic]:** sélectionnez une option de **[!UICONTROL Optimization goals]**. Si vous choisissez un objectif personnalisé, sélectionnez l’objectif personnalisé [Advertising DSP existant](/help/dsp/optimization/custom-goal.md) dans **[!UICONTROL Custom objective]**.

   * **[!UICONTROL Sequence]:** faites glisser les lots dans l’ordre souhaité, puis saisissez le nombre d’impressions pour chaque séquence. Activez **[!UICONTROL Keep in loop]** pour répéter la séquence ou laissez-la désactivée pour définir les impressions du dernier lot sur **[!UICONTROL Infinite]**.

1. Cliquez sur **[!UICONTROL Save]** dans la boîte de dialogue.

1. [Enregistrez l’expérience](#save).

### Utilisation de l’éditeur manuel {#without-scheduling-manual}

[Ouvrez l’éditeur manuel](experience-edit-targeting.md#experience-open) avant de suivre ces étapes.

1. Pendant que vous [créez](experience-create-targeting.md) ou [modifiez](experience-edit-targeting.md) l’expérience, ouvrez les paramètres d’optimisation créative :

   1. Placez le curseur sur le nœud feuille de création sous le nœud cible et procédez comme suit :

      * Pour les lots existants, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Pour créer des lots, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** et [attribuez les lots](experience-assign-creative-bundles.md).

   1. Cliquez sur l’onglet **[!UICONTROL Creative Optimization]** .

1. Désactivez **[!UICONTROL Schedule]**.

1. Sélectionnez le type de rotation de contenu créatif pour les variantes d’annonces dans les lots associés :

   * *[!UICONTROL Weighted]:* Permet d’entrer le poids de chaque lot en pourcentage. Pour appliquer des poids égaux à tous les lots associés, cliquez sur (![Appliquer un poids égal](/help/creative/assets/apply-equal-weight.png "Appliquer un poids égal")). Le poids de tous les lots sélectionnés doit être égal à 100.

   * *[!UICONTROL Algorithmic]:* pour le **[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]*, (expériences publicitaires vidéo standard) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*. Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:*

     1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

     1. Saisissez le nombre d’impressions pour chaque séquence.

     1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Cliquez sur **[!UICONTROL Save]**.

## Configurer l’optimisation créative avec la planification créative

Vous pouvez éventuellement planifier l’exécution de lots de contenu créatif spécifiques pendant des périodes séquentielles spécifiées entre les dates de début et de fin de l’expérience, et appliquer des paramètres de rotation de contenu créatif personnalisés pour chaque planification. Par exemple, vous pouvez planifier l’exécution du bundle 1 pendant les deux premières semaines afin d’optimiser le taux de clic publicitaire et l’exécution du bundle 2 pendant les deux semaines suivantes afin d’optimiser pour un objectif personnalisé spécifié.

Lorsque vous utilisez la planification, vous devez planifier les lots pendant toute la durée de l’expérience.

### Utilisation de l’éditeur piloté par l’IA (Beta) {#with-scheduling-ai}

1. Pendant que vous [créez](experience-create-targeting.md#ai-editor) ou [modifiez](experience-edit-targeting.md#ai-editor) l’expérience, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** dans le nœud de page de création.

   Pour un dernier nœud sans lots, cliquez d’abord sur **[!UICONTROL Assign Bundles]** et [affectez les lots](experience-assign-creative-bundles.md#ai-editor).

1. Ouvrez l’onglet **[!UICONTROL Creative optimisation]** et activez **[!UICONTROL Schedule]**.

1. Sélectionnez la **[!UICONTROL Timezone]** du planning.

1. Pour le premier planning :

   1. Cochez la case en regard de chaque lot à inclure dans la colonne de gauche.

   1. Spécifiez les dates et heures de début et de fin.

   1. Sélectionnez le type de rotation de contenu créatif et configurez ses paramètres :

      * **[!UICONTROL Weighted]:** Permet d&#39;entrer le poids relatif de chaque ligne de lot dans le planning. Les poids doivent totaliser 100. Pour répartir équitablement les poids, cliquez sur **[!UICONTROL Apply equal weight]**.

      * **[!UICONTROL Algorithmic]:** sélectionnez une option de **[!UICONTROL Optimization goals]**. Si vous choisissez un objectif personnalisé, sélectionnez l’objectif personnalisé [Advertising DSP existant](/help/dsp/optimization/custom-goal.md) dans **[!UICONTROL Custom objective]**.

      * **[!UICONTROL Sequence]:** faites glisser les lots dans l’ordre souhaité, puis saisissez le nombre d’impressions pour chaque séquence. Activez **[!UICONTROL Keep in loop]** pour répéter la séquence ou laissez-la désactivée pour définir les impressions du dernier lot sur **[!UICONTROL Infinite]**.

1. Pour chaque planification supplémentaire, cliquez sur **[!UICONTROL + Add Schedule]**, sélectionnez sa carte de planification, puis configurez ses lots, ses dates et heures, ainsi que ses paramètres de rotation.

   Les cases à cocher groupées s&#39;appliquent à la planification sélectionnée, et non à toutes les planifications. Assurez-vous que les plannings couvrent toute la durée de l’expérience avec les lots attribués.

1. Cliquez sur **[!UICONTROL Save]** dans la boîte de dialogue.

1. [Enregistrez l’expérience](#save).

### Utilisation de l’éditeur manuel {#with-scheduling-manual}

[Ouvrez l’éditeur manuel](experience-edit-targeting.md#experience-open) avant de suivre ces étapes.

1. Pendant que vous [créez](experience-create-targeting.md) ou [modifiez](experience-edit-targeting.md) l’expérience, ouvrez les paramètres d’optimisation créative :

   1. Placez le curseur sur le nœud feuille de création sous le nœud cible et procédez comme suit :

      * Pour les lots existants, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

      * Pour créer des lots, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** et [attribuez les lots](experience-assign-creative-bundles.md).

   1. Cliquez sur l’onglet **[!UICONTROL Creative Optimization]** .

1. Activez **[!UICONTROL Schedule]**.

1. Pour le premier planning :

   1. Dans la colonne de gauche, cochez la case en regard de chaque lot de contenu créatif à ajouter au premier planning.

   1. Spécifiez la date et l’heure de début, ainsi que la date et l’heure de fin du planning.

   1. Sélectionnez le type de rotation de contenu créatif :

      * *[!UICONTROL Weighted]:* Permet d’entrer le poids de chaque lot en pourcentage. Pour appliquer des poids égaux à tous les lots de la planification, cliquez sur (![Appliquer un poids égal](/help/creative/assets/apply-equal-weight.png "Appliquer un poids égal")). Le poids de tous les lots sélectionnés doit être égal à 100.

      * *[!UICONTROL Algorithmic]:* pour le **[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]*, (expériences publicitaires vidéo standard) *[!UICONTROL Completion Rate]* ou *[!UICONTROL Custom Objective]*. Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:*

        1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

        1. Saisissez le nombre d’impressions pour chaque séquence.

        1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Pour chaque planning supplémentaire :

   1. Cliquez sur **[!UICONTROL + Add Schedule]**.

   1. Dans la colonne de gauche, cochez la case en regard de chaque lot de contenu créatif à ajouter au premier planning.

   1. Spécifiez les dates de début et de fin du planning.

   1. Sélectionnez le type de rotation de contenu créatif :

      * *[!UICONTROL Weighted]:* Permet d’entrer le poids de chaque lot en pourcentage. Le poids de tous les lots sélectionnés doit être égal à 100.

      * *[!UICONTROL Algorithmic]:* Pour le **[!UICONTROL Optimization Goal]**, sélectionnez *[!UICONTROL Click Through Rate]* ou *[!UICONTROL Custom Objective]*. Si vous sélectionnez *[!UICONTROL Custom Objective]*, sélectionnez un objectif personnalisé Advertising DSP [existant](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:*

        1. Faites glisser et déposez les lots affectés dans l’ordre souhaité.

        1. Saisissez le nombre d’impressions pour chaque séquence.

        1. Pour la dernière séquence, indiquez si a\) doit afficher le lot final de la séquence indéfiniment (*[!UICONTROL Infinite]* (valeur par défaut) ou b\) en boucle sur le premier lot une fois le lot final affiché (*[!UICONTROL Keep in Loop]*).

1. Cliquez sur **[!UICONTROL Save]**.

## Enregistrer l’expérience {#save}

Les étapes suivantes s’appliquent aux deux éditeurs.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Affectez et annulez l’affectation des lots de contenu créatif à un nœud final d’une expérience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personnaliser les URL de tracking pour les créatifs](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [Afficher le journal des modifications d’une expérience](/help/creative/experiences/experience-view-change-log.md)
