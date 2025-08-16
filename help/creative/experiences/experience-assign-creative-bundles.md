---
title: Affectez et annulez l’affectation des bundles de création à un nœud final d’une expérience
description: Découvrez comment affecter des contenus publicitaires à chaque cible dans vos expériences publicitaires.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Affectez et annulez l’affectation des bundles de création à un nœud final d’une expérience

*Expériences avec ciblage d’arborescence de décision uniquement*

Vous pouvez affecter des lots créatifs à un nœud cible au niveau le plus bas d’une arborescence de décision d’expérience. Pour les expériences pour lesquelles vous n’avez pas configuré de cibles, le niveau inférieur se trouve sous « Tous ».

Pour les expériences publicitaires standard, vous ne pouvez affecter que des lots de création standard. Pour les expériences publicitaires dynamiques, vous ne pouvez affecter que des lots créatifs dynamiques.

>[!NOTE]
>
>Si vous n’affectez pas au moins une offre groupée de contenu créatif à chaque nœud final, vous pouvez choisir d’utiliser les contenus créatifs par défaut pour chaque nœud non affecté lorsque vous [enregistrez l’expérience](experience-create-targeting.md). Pour publier une expérience, vous devez attribuer des lots ou utiliser les contenus publicitaires par défaut pour chaque nœud final.

<!-- 1. [ways to get to the decision tree] -->

1. Effectuez l’une des opérations suivantes :

   * (Nœuds finaux sans contenu publicitaire) Sous le nœud, cliquez sur ![Ajouter](/help/creative/assets/add.png "Ajouter"), puis sélectionnez **[!UICONTROL Assign Bundles]**.

   * (Nœuds avec contenu créatif existant) Placez le curseur sur la zone du lot de contenu créatif sous le nœud cible<!-- wording???? --> puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Cochez la case en regard de chaque lot à affecter au nœud cible, puis décochez la case en regard de chaque lot à annuler.

   Seules les offres groupées du type correspondant à l’expérience (standard ou dynamique) sont répertoriées.

1. Cliquez sur **[!UICONTROL Attach to Bundles]**.

1. (Facultatif) [Personnalisez les URL de tracking pour les contenus publicitaires des lots attribués](experience-tracking-urls-targeting.md).

1. (Facultatif) [Personnalisez l’optimisation créative et la planification](experience-optimization-scheduling-targeting.md) pour les lots affectés.

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Ajoutez un nœud cible au niveau final](experience-target-node-add-final.md)
>* [Insérez un nœud cible entre les nœuds](experience-target-node-add-inner.md)
>* [Ajouter un nœud cible frère entre les nœuds](experience-target-node-add-sibling.md)
>* [Copiez les nœuds enfants et les contenus publicitaires dans un autre nœud au même niveau](experience-target-node-copy.md)
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Modifier une expérience avec le ciblage d’arborescence de décision](experience-edit-targeting.md)
>* [Paramètres d’expérience ciblés](experience-settings-targeting.md)
>* [Exporter et implémenter une balise d’expérience publicitaire pour une expérience en direct](experience-tag-export.md)
