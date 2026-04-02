---
title: Affectez et annulez l’affectation des bundles de création à un nœud final d’une expérience
description: Découvrez comment affecter des contenus publicitaires à chaque cible dans vos expériences publicitaires.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
TQID: https://experienceleague.adobe.com/HqTq2fiJadk-QIBwYkOxC2N9sTMm29LIXRzSubPuv9M
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 305
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

   * (Nœuds finaux sans contenu publicitaire) Sous le nœud , cliquez sur **[!UICONTROL Assign Bundles]**.

   * (Nœuds avec contenu créatif existant) Placez le curseur sur la zone du lot de contenu créatif sous le nœud cible, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Cochez la case en regard de chaque lot à affecter au nœud cible, puis décochez la case en regard de chaque lot à annuler.

   Seules les offres groupées du type correspondant à l’expérience (standard ou dynamique) sont répertoriées.

1. Cliquez sur **[!UICONTROL Save]**.

1. (Facultatif) [Personnalisez l’optimisation créative et la planification](experience-optimization-scheduling-targeting.md) pour les lots affectés.

1. (Facultatif) [Personnalisez les URL de tracking pour les contenus publicitaires des lots attribués](experience-tracking-urls-targeting.md).

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
>* [Afficher le journal des modifications d’une expérience](/help/creative/experiences/experience-view-change-log.md)
