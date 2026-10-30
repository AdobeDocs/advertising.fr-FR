---
title: Création d’une expérience avec le ciblage d’arborescence de décision
description: Découvrez comment créer une expérience publicitaire ciblée à l’aide de l’éditeur d’arborescence de décision manuel ou piloté par l’IA.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
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
source-wordcount: '715'
ht-degree: 0%
---
# Création d’une expérience avec le ciblage d’arborescence de décision

Créez une expérience d’annonce publicitaire ciblée à l’aide d’une arborescence de décision. Chaque expérience utilise les annonces d’une seule bibliothèque de contenu créatif.

L’éditeur piloté par l’IA (Beta) s’ouvre par défaut. Vous pouvez configurer l’arborescence par le biais de l’agent AI ou modifier directement sa zone de travail. Vous pouvez également passer à l’éditeur manuel existant.

>[!NOTE]
>
>* Une fois que vous avez créé une expérience ciblée, vous ne pouvez pas la modifier ultérieurement en une expérience non ciblée, qui utilise un autre workflow.
>* Assurez-vous que vos expériences publicitaires incluent un ciblage compatible avec les campagnes dans lesquelles vous allez le mettre en œuvre. Le comportement de ciblage hiérarchique peut varier en fonction du DSP. Lorsque vous chargez une balise d’expérience de publicité vers Advertising DSP et que vous la joignez à un emplacement, le ciblage au niveau des annonces s’applique en plus (et non à la place) du ciblage au niveau des emplacements. Par exemple, si un emplacement cible des utilisateurs en Australie et qu’une annonce cible des utilisateurs au Japon, l’annonce cible la branche « Tout le monde ».

## Création de l’expérience

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Cliquez sur **[!UICONTROL Create New Experience]**.

1. Renseignez les [paramètres généraux de l’expérience](experience-settings-targeting.md), avec les **[!UICONTROL Targeting]** activés.

1. Cliquez sur **[!UICONTROL Create]**.

   L’éditeur d’arborescence de décision piloté par l’IA s’ouvre pour la nouvelle expérience.

1. Configurez l’arborescence en suivant l’une des procédures suivantes.

## Configurer l’arborescence à l’aide de l’éditeur piloté par l’IA (Beta) {#ai-editor}

1. Au cours de la conversation, décrivez la structure de ciblage de votre choix, y compris les critères de chaque branche et la manière de gérer les visionneuses qui ne correspondent pas à une cible spécifiée.

1. Examinez l’arborescence dans la zone de travail. Pour demander des modifications, décrivez-les dans la conversation. Attendez que l’assistant ait terminé le traitement avant d’interagir avec la zone de travail.

1. (Facultatif) Affinez l’arborescence directement dans la zone de travail :

   * [Ajouter une cible de niveau final](experience-target-node-add-final.md#ai-editor), [insérer un niveau cible](experience-target-node-add-inner.md#ai-editor) ou [ajouter une cible sœur](experience-target-node-add-sibling.md#ai-editor).

   * [Copiez les nœuds enfants et les éléments créatifs](experience-target-node-copy.md#ai-editor) ou [supprimez un nœud](experience-target-node-delete.md#ai-editor).

1. [Attribuez des lots créatifs aux nœuds finaux](experience-assign-creative-bundles.md#ai-editor) et, éventuellement[&#x200B; personnalisez l’optimisation et la planification de la création](experience-optimization-scheduling-targeting.md) ainsi que les [URL de suivi](experience-tracking-urls-targeting.md#ai-editor).

   Pour publier l’expérience, vous devez affecter des lots à chaque nœud final ou utiliser les contenus publicitaires par défaut de l’expérience. Lors de l’enregistrement, vous pouvez affecter des valeurs par défaut aux nœuds non affectés.

1. (Facultatif) Modifiez les paramètres généraux de l’expérience :

   1. Pour enregistrer les modifications d’arborescence que vous souhaitez conserver, cliquez sur **[!UICONTROL Save]**.

   1. Cliquez sur **[!UICONTROL Experience Form]**, puis sur **[!UICONTROL Yes]** pour ignorer les modifications d’arborescence non enregistrées et ouvrir le formulaire.

   1. Modifiez le [paramètres généraux de l’expérience](experience-settings-targeting.md), puis cliquez sur **[!UICONTROL Save]**.

      L’éditeur piloté par l’IA s’ouvre.

1. [Enregistrez l’expérience](#save).

## Configuration de l’arborescence à l’aide de l’éditeur manuel {#manual-editor}

1. Dans l’éditeur piloté par l’IA, cliquez sur **[!UICONTROL Manual Decision Tree]**, puis sur **[!UICONTROL Yes]** pour quitter l’éditeur piloté par l’IA.

   Enregistrez toutes les modifications de l’éditeur d’IA que vous souhaitez conserver avant de changer. Confirmer le changement ignore les modifications d’arborescence non enregistrées.

1. (Facultatif) Modifiez les paramètres d’affichage :

   * Effectuez un zoom avant ou arrière en déplaçant le curseur.

   * Basculez entre les vues verticale et horizontale en cliquant sur ![Afficher en tant qu&#39;arborescence verticale](/help/creative/assets/tree-vertical.png "Afficher en tant qu&#39;arborescence verticale") ou ![Afficher comme arborescence horizontale](/help/creative/assets/tree-horizontal.png "Afficher comme arborescence horizontale").

   Vos paramètres d’affichage sont enregistrés jusqu’à votre déconnexion.

1. Configurez les cibles d’annonces publicitaires et les contenus publicitaires correspondants :

   * [Ajoutez une cible de niveau final](experience-target-node-add-final.md#manual-editor), [insérez une cible entre des nœuds](experience-target-node-add-inner.md#manual-editor) ou [ajoutez une cible sœur](experience-target-node-add-sibling.md#manual-editor).

   * [Copiez les nœuds enfants et les éléments créatifs](experience-target-node-copy.md#manual-editor) ou [supprimez un nœud](experience-target-node-delete.md#manual-editor).

   * [Attribuez des lots de contenu créatif](experience-assign-creative-bundles.md#manual-editor) et, éventuellement[&#x200B; personnalisez l’optimisation et la planification de la création](experience-optimization-scheduling-targeting.md) ainsi que les [URL de suivi](experience-tracking-urls-targeting.md#manual-editor).

1. (Facultatif) Pour modifier les paramètres généraux de l’expérience, cliquez sur **[!UICONTROL Experience Form]** et modifiez les [paramètres généraux de l’expérience](experience-settings-targeting.md).

1. [Enregistrez l’expérience](#save).

## Enregistrer l’expérience {#save}

Les étapes suivantes s’appliquent aux deux éditeurs.

{{$include /help/_includes/experience-save.md}}

## Balises publicitaires et transcodage vidéo pour les expériences enregistrées

Lorsque l’expérience est en ligne, [!DNL Creative] crée automatiquement une balise d’annonce publicitaire pour chaque taille de contenu créatif ou durée de vidéo applicable. Vous pouvez ensuite [exporter une balise publicitaire et l’implémenter dans un DSP](/help/creative/experiences/experience-tag-export.md).

Pour les expériences publicitaires vidéo, les contenus publicitaires vidéo sont automatiquement transcodés par Adobe Advertising DSP sous la forme de balises VAST 2.0 afin que vous puissiez les prévisualiser. Vous pouvez éventuellement [appliquer un transcodage pour un autre DSP](experience-tag-video-transcoding.md) à n’importe quelle balise d’expérience d’annonce vidéo.

>[!MORELIKETHIS]
>
>* [Paramètres d’expérience ciblés](experience-settings-targeting.md)
>* [Ajoutez un nœud cible au niveau final](experience-target-node-add-final.md)
>* [Insérez un nœud cible entre les nœuds](experience-target-node-add-inner.md)
>* [Ajouter un nœud cible frère entre les nœuds](experience-target-node-add-sibling.md)
>* [Copiez les nœuds enfants et les contenus publicitaires dans un autre nœud au même niveau](experience-target-node-copy.md)
>* [Affecter des contenus publicitaires à un nœud final](experience-assign-creative-bundles.md)
>* [Personnaliser les URL de tracking pour les contenus publicitaires dans les lots attribués](experience-tracking-urls-targeting.md)
>* [Personnaliser l’optimisation et la planification de la création](experience-optimization-scheduling-targeting.md)
>* [Exporter et implémenter une balise d’expérience publicitaire pour une expérience en direct](/help/creative/experiences/experience-tag-export.md)
>* [Modifier une expérience avec le ciblage d’arborescence de décision](experience-edit-targeting.md)
>* [Afficher le journal des modifications d’une expérience](/help/creative/experiences/experience-view-change-log.md)
