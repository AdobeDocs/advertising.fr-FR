---
title: Disposition de l’arborescence de décision
description: Découvrez les éditeurs d’arborescence de décision manuels et pilotés par l’IA pour des expériences avec le ciblage.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
TQID: 'https://experienceleague.adobe.com/JFrcVBHxv90Fchk-VfkmxAITQJswboszNMFOfaAQlL4'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%
---
# Disposition de l’arborescence de décision pour les expériences [!DNL Creative]

Lorsque vous activez l’option « [!UICONTROL Targeting] » pour une expérience, vous configurez l’expérience à l’aide d’une arborescence de décision.

Au départ, chaque arborescence de décision commence par le niveau racine « Tous ». Vous pouvez ajouter un ou plusieurs nœuds cibles, puis attribuer des lots créatifs aux nœuds finaux dans chaque branche de l’arborescence de décision.

## Éditeur piloté par l’IA (Beta) {#ai-editor}

L’éditeur piloté par l’IA s’ouvre par défaut lorsque vous créez ou modifiez une expérience avec le ciblage. Il combine une conversation avec l’agent d’IA et une zone de travail interactive d’arbre de décision.

* Décrivez la structure de ciblage ou les modifications que vous souhaitez apporter à la conversation, puis passez en revue l’arborescence obtenue avant d’enregistrer.

* Modifiez directement la zone de travail pour ajouter des niveaux et des nœuds cibles, attribuer des lots et configurer l’optimisation créative et les URL de suivi. Il n’est pas nécessaire de passer à l’éditeur manuel pour utiliser ces commandes.

* Affichez le nom de l’expérience, le statut et l’annonceur dans l’en-tête et utilisez les identifiants de nœud, le cas échéant, pour identifier les nœuds cibles lorsque vous décrivez des modifications.

* Utilisez **[!UICONTROL Zoom in]**, **[!UICONTROL Zoom out]** et **[!UICONTROL Change orientation]** pour ajuster la vue. **[!UICONTROL Reset tree]** efface l’arborescence après confirmation ; il ne se contente pas de réinitialiser le zoom.

Lorsque l’assistant traite une modification, la zone de travail et son bouton **[!UICONTROL Save]** sont temporairement désactivés. Attendez la fin du traitement avant d’effectuer une autre modification de la zone de travail.

## Éditeur manuel {#manual-editor}

Pour ouvrir l’éditeur manuel existant à partir de l’éditeur piloté par l’IA, cliquez sur **[!UICONTROL Manual Decision Tree]**. Vous pouvez également sélectionner des **[!UICONTROL Create Decision Tree Manually (Legacy)]** à partir des actions de l’expérience dans la vue [!UICONTROL Experiences]. Voir [Changement d’éditeur ou modification des paramètres d’expérience](experience-edit-targeting.md#switch-editors).

Dans l’éditeur manuel, l’arborescence est affichée verticalement par défaut. Vous pouvez passer à une vue horizontale et ajuster le zoom à l’aide d’un curseur. Vos paramètres d’affichage sont enregistrés jusqu’à votre déconnexion.

Les exemples suivants illustrent l’éditeur manuel :

![Exemple d’arborescence de décision verticale sans cibles](/help/creative/assets/experience-decision-tree-no-targets.png "Exemple d’arborescence de décision verticale sans cibles")

![Exemple d’arbre de décision horizontal sans cibles](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Exemple d’arbre de décision horizontal sans cibles")

>[!IMPORTANT]
>
>Enregistrez les modifications que vous souhaitez conserver avant de quitter l’éditeur piloté par l’IA. Cliquez sur **[!UICONTROL Manual Decision Tree]**, **[!UICONTROL Experience Form]** ou **[!UICONTROL Cancel]** pour ouvrir une boîte de dialogue de confirmation. Cliquer sur **[!UICONTROL Yes]** ignore les modifications d’arborescence non enregistrées ; cliquer sur **[!UICONTROL No]** vous maintient dans l’éditeur.

## Termes

**Arborescence :** structure de prise de décision globale sous la forme d’une arborescence avec des branches.

**Nœud cible :** cible dans une branche.

**Nœud feuille :** ensemble de contenus publicitaires affectés à un nœud cible final.

## Cibles dans une arborescence de décision

Chaque arborescence de décision peut comporter jusqu’à cinq niveaux de cibles. Les cibles au niveau de l’expérience sont appliquées conjointement avec vos options de ciblage DSP. Le comportement de ciblage hiérarchique peut varier selon DSP. Assurez-vous que vos expériences publicitaires incluent un ciblage compatible avec les campagnes dans lesquelles vous allez le mettre en œuvre.

Chaque niveau cible peut inclure plusieurs branches, chacune avec un ou plusieurs nœuds avec le même type de cible (segment d’audience, type d’emplacement géographique, valeurs pour des clés de passe de données spécifiées, attributs pour un pixel de reciblage spécifié ou catégorie d’appareils). Vous pouvez affecter des lots de contenu créatif dans chaque taille d’annonce publicitaire pour laquelle vous avez spécifié un contenu créatif d’image ou vidéo par défaut aux nœuds cibles de niveau inférieur.

<!-- Add a screen shot of the AI editor -->L’exemple suivant illustre des cibles dans l’éditeur manuel :

![Exemple d’arborescence de décision avec cibles](/help/creative/assets/experience-decision-tree.png "Exemple d’arborescence de décision avec cibles")

Lorsque vous ajoutez un nœud cible au niveau final, vous spécifiez la cible du nouveau nœud. Un nœud frère supplémentaire, « Tout le reste », est automatiquement créé pour toutes les personnes qui ne correspondent pas à la cible spécifiée. Vous pouvez ensuite ajouter d’autres nœuds frères avec différentes cibles du même type.

Cependant, lorsque vous insérez un nœud cible entre des niveaux existants, le premier nœud du nouveau niveau est initialement affecté à « Tous ». Pour identifier une cible spécifique, créez un nœud cible frère au même niveau, pour lequel vous spécifiez la cible réelle. Cette action crée le nœud cible et remplace le nœud « Tous » par un nœud « Tout le reste » (qui inclut tous les lots créatifs précédemment affectés à Tous). Vous pouvez ensuite ajouter d’autres nœuds frères avec différentes cibles du même type.

Pour tous les nœuds parents, vous pouvez éventuellement copier tous les nœuds cibles enfants et les lots de création et les coller dans un autre nœud au même niveau. Vous pouvez ajouter les nœuds collés au framework existant ou remplacer le framework existant par ceux-ci.

## Éléments créatifs dans un arbre de décision

Attribuez des lots créatifs à chaque nœud cible final de l’expérience.

Dans chaque nœud avec des lots de contenu publicitaire, vous pouvez éventuellement faire pivoter les contenus publicitaires inclus a) de manière algorithmique pour optimiser le taux de clic publicitaire ou un objectif personnalisé, b) en fonction de poids spécifiés, ou c) dans une séquence spécifique. Vous pouvez également faire pivoter les contenus publicitaires dans une séquence temporelle spécifiée à l’aide d’une combinaison des mêmes options.

Vous pouvez éventuellement personnaliser les URL de page de destination, de suivi des impressions et de suivi des clics, selon les besoins des créatifs individuels. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [À propos des expériences dans Advertising Creative 2.0](experience-about.md)
>* [Créer une expérience avec le ciblage](/help/creative/experiences/experience-create-targeting.md)
>* [Paramètres d’expérience ciblés](/help/creative/experiences/experience-settings-targeting.md)
