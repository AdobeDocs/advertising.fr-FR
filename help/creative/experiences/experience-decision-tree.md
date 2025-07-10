---
title: Disposition de l’arborescence de décision
description: Découvrez l’arborescence de décision pour les expériences de ciblage.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Disposition de l’arborescence de décision pour les expériences [!DNL Creative]

*Version bêta fermée*

Lorsque vous activez l’option « [!UICONTROL Targeting] » pour une expérience, vous configurez l’expérience à l’aide d’une arborescence de décision.

Au départ, chaque arborescence de décision commence par le niveau racine « Tous ». Vous pouvez ajouter un ou plusieurs nœuds cibles, puis attribuer des lots créatifs aux nœuds finaux dans chaque branche de l’arborescence de décision. Par défaut, l’arborescence de décision est affichée verticalement, mais vous pouvez éventuellement la visualiser horizontalement à la place.

![Exemple d’arborescence de décision verticale sans cibles](/help/creative/assets/experience-decision-tree-no-targets.png "Exemple d’arborescence de décision verticale sans cibles")

![Exemple d’arbre de décision horizontal sans cibles](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Exemple d’arbre de décision horizontal sans cibles")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
-->

## Termes

**Arborescence :** structure de prise de décision globale sous la forme d’une arborescence avec des branches.

**Nœud cible :** cible dans une branche.

**Nœud feuille :** ensemble de contenus publicitaires affectés à un nœud cible final.

## Cibles dans une arborescence de décision

Chaque arborescence de décision peut comporter jusqu’à cinq niveaux de cibles. Chaque niveau cible peut inclure plusieurs branches, chacune avec un ou plusieurs nœuds avec le même type de cible (segment d’audience, type d’emplacement géographique, valeurs pour des clés de passe de données spécifiées, attributs pour un pixel de reciblage spécifié ou catégorie d’appareils). Vous pouvez affecter des lots de contenu créatif dans chaque taille d’annonce publicitaire pour laquelle vous avez spécifié un contenu créatif d’image ou vidéo par défaut aux nœuds cibles de niveau inférieur.

![Exemple d’arborescence de décision avec cibles](/help/creative/assets/experience-decision-tree.png "Exemple d’arborescence de décision avec cibles")

Lorsque vous ajoutez un nœud cible au niveau final, vous spécifiez la cible du nouveau nœud. Un nœud frère supplémentaire, « Tout le reste », est automatiquement créé pour toutes les personnes qui ne correspondent pas à la cible spécifiée. Vous pouvez ensuite ajouter d’autres nœuds frères avec différentes cibles du même type.

Cependant, lorsque vous insérez un nœud cible entre des niveaux existants, le premier nœud du nouveau niveau est initialement affecté à « Tous ». Pour identifier une cible spécifique, créez un nœud cible frère au même niveau, pour lequel vous spécifiez la cible réelle. Cette action crée le nœud cible et remplace le nœud « Tous » par un nœud « Tout le reste » (qui inclut tous les lots créatifs précédemment affectés à Tous). Vous pouvez ensuite ajouter d’autres nœuds frères avec différentes cibles du même type.

Pour tous les nœuds parents, vous pouvez éventuellement copier tous les nœuds cibles enfants et les lots de création et les coller dans un autre nœud au même niveau. Vous pouvez ajouter les nœuds collés au framework existant ou remplacer le framework existant par ceux-ci.

## Éléments créatifs dans un arbre de décision

Attribuez des lots créatifs à chaque nœud cible final de l’expérience.

Dans chaque nœud avec des lots de contenu publicitaire, vous pouvez éventuellement faire pivoter les contenus publicitaires inclus a) en fonction de poids spécifiés ou b) de manière algorithmique afin d’optimiser le taux de clic publicitaire ou un objectif personnalisé. Vous pouvez également faire pivoter les contenus publicitaires dans une séquence temporelle spécifiée à l’aide des mêmes options.

Vous pouvez éventuellement personnaliser les URL de page de destination, de suivi des impressions et de suivi des clics, selon les besoins des créatifs individuels. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [À propos des expériences dans Advertising Creative 2.0](experience-about.md)
>* [Créer une expérience avec le ciblage](/help/creative/experiences/experience-create-targeting.md)
>* [Paramètres d’expérience ciblés](/help/creative/experiences/experience-settings-targeting.md)
