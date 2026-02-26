---
title: Création d’une expérience avec le ciblage d’arborescence de décision
description: Découvrez comment créer une expérience d’annonce publicitaire ciblée à l’aide d’une arborescence de décision.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: 24ae6f65552a2c958488be4f1363c08c3f387d37
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Création d’une expérience avec le ciblage d’arborescence de décision

Créez une expérience d’annonce publicitaire ciblée à l’aide d’une arborescence de décision. Chaque expérience utilise les annonces d’une seule bibliothèque de contenu créatif.

>[!NOTE]
>
>* Une fois que vous avez créé une expérience ciblée, vous ne pouvez pas la modifier ultérieurement en une expérience non ciblée, qui utilise un autre workflow.
>* Assurez-vous que vos expériences publicitaires incluent un ciblage compatible avec les campagnes dans lesquelles vous allez le mettre en œuvre. Le comportement de ciblage hiérarchique peut varier en fonction du DSP. Lorsque vous chargez une balise d’expérience de publicité vers Advertising DSP et que vous la joignez à un emplacement, le ciblage au niveau des annonces s’applique en plus (et non à la place) du ciblage au niveau des emplacements. Par exemple, si un emplacement cible des utilisateurs en Australie et qu’une annonce cible des utilisateurs au Japon, l’annonce cible la branche « Tout le monde ».

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Cliquez sur **[!UICONTROL Create New Experience]**.

1. Saisissez les [paramètres généraux de l’expérience](experience-settings-targeting.md).

1. Cliquez sur **[!UICONTROL Create]**.

1. Dans l’arborescence de décision, procédez comme suit :

   1. (Facultatif) Modifiez les paramètres d’affichage de l’arborescence de décision.

      Vos paramètres sont enregistrés jusqu’à la déconnexion.

      * Effectuez un zoom avant ou arrière en déplaçant le curseur.

      * Basculez entre l&#39;affichage d&#39;une liste verticale et d&#39;une liste horizontale en cliquant sur ![Afficher en tant qu&#39;arborescence verticale](/help/creative/assets/tree-vertical.png "Afficher en tant qu&#39;arborescence verticale") ou ![Afficher comme arborescence horizontale](/help/creative/assets/tree-horizontal.png "Afficher comme arborescence horizontale"), respectivement.

   1. (Facultatif) Configurez les cibles d’annonces publicitaires et les contenus publicitaires correspondants de l’une des manières suivantes :

      * Cibles :

         * [Ajoutez un nœud cible au niveau final](experience-target-node-add-final.md).

         * [Insérez un nœud cible entre les nœuds](experience-target-node-add-inner.md).

         * [Ajoutez un nœud cible frère entre les nœuds](experience-target-node-add-sibling.md).

         * [Copiez les nœuds enfants et les contenus publicitaires dans un autre nœud au même niveau](experience-target-node-copy.md).

      * Lots Creative :

         * [Affectez et annulez l’affectation de contenus publicitaires à un nœud final](experience-assign-creative-bundles.md).

           Si vous n’affectez pas au moins une offre groupée à chaque nœud final, vous pouvez choisir d’utiliser les contenus publicitaires par défaut pour chaque nœud non affecté lorsque vous enregistrez l’expérience. Pour publier une expérience, vous devez attribuer des lots ou utiliser les contenus publicitaires par défaut pour chaque nœud final.

         * [Personnalisez l’optimisation et la planification de la création](experience-optimization-scheduling-targeting.md) pour les lots affectés.

         * [Personnalisez les URL de tracking pour les contenus publicitaires des lots attribués](experience-tracking-urls-targeting.md).

1. (Facultatif) Basculez entre l’arborescence de décision et les paramètres généraux :

   * Pour ouvrir les paramètres généraux à partir de l’arborescence de décision, cliquez sur **[!UICONTROL Experience Form]** dans le coin supérieur droit.

   * Pour ouvrir l’arborescence de décision à partir des paramètres généraux, cliquez sur **[!UICONTROL Decision Tree]** dans le coin supérieur droit.

1. Cliquez sur **[!UICONTROL Save]**, puis procédez comme suit.

   * (Si chaque nœud au niveau le plus bas comprend au moins un lot de contenu créatif) Cliquez sur **[!UICONTROL OK]**.

   * (Si chaque nœud au niveau le plus bas n’inclut pas au moins un lot de contenu créatif) Effectuez l’une des opérations suivantes :

      * Pour enregistrer l’expérience sans tous les lots de création requis, cliquez sur **[!UICONTROL Save as Draft]**.

        Vous ne pouvez pas créer de balise publicitaire pour une expérience [brouillon](experience-about.md#experience-statuses).

      * Pour attribuer le contenu créatif par défaut à chaque cible qui n’a pas encore reçu de lot de contenu créatif, cliquez sur **[!UICONTROL Assign Default Creatives]**. Après avoir consulté l’arborescence mise à jour avec les contenus publicitaires par défaut attribués, cliquez sur **[!UICONTROL Save]** et **[!UICONTROL OK]**.

      * Pour continuer à modifier l’arborescence de décision, cliquez sur **[!UICONTROL Continue Edit]**.

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
