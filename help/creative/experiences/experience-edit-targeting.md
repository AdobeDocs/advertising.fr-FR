---
title: Modification d’une expérience avec le ciblage d’arborescence de décision
description: Découvrez comment modifier une expérience publicitaire ciblée à l’aide de l’éditeur d’arborescence de décision manuel ou piloté par l’IA.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
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
source-wordcount: '655'
ht-degree: 0%
---
# Modification d’une expérience avec le ciblage d’arborescence de décision

L’éditeur piloté par l’IA (Beta) s’ouvre par défaut pour les expériences avec le ciblage. Vous pouvez utiliser l’agent d’IA, modifier directement la zone de travail ou ouvrir l’éditeur manuel existant.

## Ouvrir l’expérience {#experience-open}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facultatif) [Personnaliser la vue](/help/creative/introduction/customize-data-views.md) pour inclure des expériences spécifiques.

1. Effectuez l’une des opérations suivantes :

   * Pour ouvrir l’éditeur piloté par l’IA :

     * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Edit]**.

     * En mode Tableau, maintenez le curseur sur la ligne, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Edit]**.

   * Pour ouvrir l’éditeur manuel :

     * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * En mode Tableau, maintenez le curseur sur la ligne, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * Dans l’éditeur piloté par l’IA,

## Modifier à l’aide de l’éditeur piloté par l’IA (Beta) {#ai-editor}

1. [Ouvrez l’expérience](#experience-open).

1. Décrivez les changements de ciblage que vous souhaitez apporter à la conversation. Identifiez la branche concernée par ses cibles ou, lorsqu’elle est affichée sur la zone de travail, son identifiant de nœud.

1. Passez en revue l’arborescence mise à jour et décrivez toute autre modification. Attendez que l’assistant ait terminé le traitement avant d’interagir avec la zone de travail.

1. (Facultatif) Apportez des modifications directement dans la zone de travail :

   * [Ajouter une cible de niveau final](experience-target-node-add-final.md#ai-editor), [insérer un niveau cible](experience-target-node-add-inner.md#ai-editor) ou [ajouter une cible sœur](experience-target-node-add-sibling.md#ai-editor).

   * Modifiez les critères d’une cible en cliquant sur **[!UICONTROL ...]** > **[!UICONTROL Edit]** à côté de celle-ci, modifiez les valeurs, puis cliquez sur **[!UICONTROL Edit Node]**.

   * [Copiez les nœuds enfants et les éléments créatifs](experience-target-node-copy.md#ai-editor) ou [supprimez un nœud](experience-target-node-delete.md#ai-editor).

   * [Attribuez ou annulez l’attribution des bundles de création](experience-assign-creative-bundles.md#ai-editor).

   * [Personnalisez l’optimisation et la planification de la création](experience-optimization-scheduling-targeting.md) ou [URL de suivi](experience-tracking-urls-targeting.md#ai-editor).

1. [Enregistrez l’expérience](#save).

## Modifier à l’aide de l’éditeur manuel {#manual-editor}

1. [Ouvrez l’expérience](#experience-open).

1. (Expériences avec `[processing](experience-about.md#experience-statuses)` de statut) Si vous êtes invité à propos d’un brouillon existant et non publié, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Continue editing draft]** pour réviser et continuer à modifier le brouillon.

   * Cliquez sur **[!UICONTROL Discard and start again]** pour ignorer le brouillon et commencer à partir de la version active.

   * Cliquez sur **[!UICONTROL Cancel this edit]** pour arrêter la modification.

1. (Facultatif) Ajustez le curseur de zoom ou cliquez sur ![Afficher en tant qu’arborescence verticale](/help/creative/assets/tree-vertical.png "Afficher en tant qu’arborescence verticale") ou ![Afficher comme arborescence horizontale](/help/creative/assets/tree-horizontal.png "Afficher comme arborescence horizontale") pour modifier l’orientation.

   Vos paramètres d’affichage sont enregistrés jusqu’à votre déconnexion.

1. Modifiez les cibles et les éléments créatifs selon les besoins :

   * [Ajoutez une cible de niveau final](experience-target-node-add-final.md#manual-editor), [insérez une cible entre des nœuds](experience-target-node-add-inner.md#manual-editor) ou [ajoutez une cible sœur](experience-target-node-add-sibling.md#manual-editor).

   * [Copiez les nœuds enfants et les éléments créatifs](experience-target-node-copy.md#manual-editor) ou [supprimez un nœud](experience-target-node-delete.md#manual-editor).

   * [Attribuez ou annulez l’attribution des bundles de création](experience-assign-creative-bundles.md#manual-editor).

   * [Personnalisez l’optimisation et la planification de la création](experience-optimization-scheduling-targeting.md) ou [URL de suivi](experience-tracking-urls-targeting.md#manual-editor).

1. [Enregistrez l’expérience](#save).

## Changement d’éditeurs ou modification des paramètres d’expérience {#switch-editors}

>[!IMPORTANT]
>
>Avant de quitter l’éditeur piloté par l’IA, enregistrez les modifications d’arborescence que vous souhaitez conserver. Le passage à l’éditeur manuel ou au formulaire d’expérience ne transfère pas les modifications non enregistrées.

* **Éditeur piloté par l’IA en éditeur manuel :** cliquez sur **[!UICONTROL Manual Decision Tree]**. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Yes]** pour ignorer les modifications non enregistrées et ouvrir l’éditeur manuel, ou **[!UICONTROL No]** pour rester.

* **Éditeur piloté par l’IA pour les paramètres généraux :** cliquez sur **[!UICONTROL Experience Form]**, puis sur **[!UICONTROL Yes]** pour ignorer les modifications d’arborescence non enregistrées et ouvrir le formulaire. Modifiez le [paramètres généraux de l’expérience](experience-settings-targeting.md), puis cliquez sur **[!UICONTROL Save]**.

* **Éditeur manuel pour les paramètres généraux :** enregistrez les modifications d’arborescence à conserver, puis cliquez sur **[!UICONTROL Experience Form]**. Modifiez le [paramètres généraux de l’expérience](experience-settings-targeting.md), puis cliquez sur **[!UICONTROL Save]**.

* **Paramètres généraux de l’éditeur piloté par l’IA :** cliquez sur **[!UICONTROL Decision Tree]**. L’enregistrement des modifications dans les paramètres généraux d’une expérience ciblée ouvre également l’éditeur piloté par l’IA.

* **Éditeur manuel vers l’éditeur piloté par l’IA :** enregistrez vos modifications d’arborescence, revenez à la vue [!UICONTROL Experiences] et sélectionnez **[!UICONTROL Edit]** pour l’expérience.

Pour quitter l’éditeur piloté par l’IA sans ouvrir un autre éditeur, cliquez sur **[!UICONTROL Cancel]**. Cliquez sur **[!UICONTROL Yes]** pour ignorer les modifications d’arborescence non enregistrées ou sur **[!UICONTROL No]** pour continuer la modification.

## Enregistrer l’expérience {#save}

Les étapes suivantes s’appliquent aux deux éditeurs.

{{$include /help/_includes/experience-save.md}}

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
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Afficher le journal des modifications d’une expérience](/help/creative/experiences/experience-view-change-log.md)
