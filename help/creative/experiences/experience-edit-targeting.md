---
title: Modification d’une expérience avec le ciblage d’arborescence de décision
description: Découvrez comment modifier les paramètres d’une expérience publicitaire ciblée à l’aide d’une arborescence de décision.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Modification d’une expérience avec le ciblage d’arborescence de décision

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facultatif) [Personnaliser la vue](/help/creative/introduction/customize-data-views.md) pour inclure des expériences spécifiques.

1. Effectuez l’une des opérations suivantes :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Edit]**.

   * En mode Tableau, maintenez le curseur sur la ligne, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Edit]**.

   L’arborescence de décision s’ouvre par défaut.

1. (Facultatif) Basculez entre l’arborescence de décision et les paramètres généraux selon les besoins :

   * Pour ouvrir les paramètres généraux à partir de l’arborescence de décision, cliquez sur **[!UICONTROL Experience Form]** dans le coin supérieur droit.

   * Pour ouvrir l’arborescence de décision à partir des paramètres généraux, cliquez sur **[!UICONTROL Decision Tree]** dans le coin supérieur droit.

1. (Facultatif) Pour modifier l’arborescence de décision, effectuez l’une des opérations suivantes :

   * ([Traitement](experience-about.md#experience-statuses) expériences) Effectuez l’une des opérations suivantes :

      * Pour ignorer les modifications existantes non publiées de l’expérience en direct, cliquez sur **[!UICONTROL Discard and start again]**.

      * Pour conserver les modifications existantes non validées, cliquez sur **[!UICONTROL Continue editing draft]**.

      * Pour modifier les détails de l’expérience, cliquez sur **[!UICONTROL Edit Experience Details]**.

   * (Facultatif) Modifiez les paramètres d’affichage de l’arborescence de décision.

     Vos paramètres sont enregistrés jusqu’à la déconnexion.

   * Effectuez un zoom avant ou arrière en déplaçant le curseur.

   * Basculez entre l&#39;affichage d&#39;une liste verticale et d&#39;une liste horizontale en cliquant sur ![Afficher en tant qu&#39;arborescence verticale](/help/creative/assets/tree-vertical.png "Afficher en tant qu&#39;arborescence verticale") ou ![Afficher comme arborescence horizontale](/help/creative/assets/tree-horizontal.png "Afficher comme arborescence horizontale"), respectivement.

   * (Facultatif) Modifiez les cibles d’annonces publicitaires et les contenus publicitaires correspondants de l’une des manières suivantes :

      * Cibles :

        *[Ajoutez un nœud cible au niveau final](experience-target-node-add-final.md) dans une expérience.

         * [Insérez un nœud cible entre les nœuds](experience-target-node-add-inner.md).

         * [Ajoutez un nœud cible frère entre les nœuds](experience-target-node-add-sibling.md).

         * [Copiez les nœuds enfants et les contenus publicitaires dans un autre nœud au même niveau](experience-target-node-copy.md).

      * Lots Creative :

         * [Affectez et annulez l’affectation de contenus publicitaires à un nœud final](experience-assign-creative-bundles.md).

           Si vous n’affectez pas au moins une offre groupée à chaque nœud final, vous pouvez choisir d’utiliser les contenus publicitaires par défaut pour chaque nœud non affecté lorsque vous enregistrez l’expérience. Pour publier une expérience, vous devez attribuer des lots ou utiliser les contenus publicitaires par défaut pour chaque nœud final.

         * [Personnalisez les URL de tracking pour les contenus publicitaires des lots attribués](experience-tracking-urls-targeting.md).

         * [Personnalisez l’optimisation et la planification de la création](experience-optimization-scheduling-targeting.md) pour les lots affectés.

1. (Facultatif) Modifiez les [paramètres généraux de l’expérience](experience-settings-targeting.md).

1. Cliquez sur **[!UICONTROL Save]**, puis procédez comme suit.

   * (Si chaque nœud au niveau le plus bas comprend au moins un lot de contenu créatif) Cliquez sur **[!UICONTROL OK]**.

   * (Si chaque nœud au niveau le plus bas n’inclut pas au moins un lot de contenu créatif) Effectuez l’une des opérations suivantes :

      * Pour enregistrer l’expérience sans tous les lots de création requis, cliquez sur **[!UICONTROL Save as Draft]**.

        Vous ne pouvez pas créer de balise publicitaire pour une expérience [brouillon](experience-about.md#experience-statuses).

      * Pour attribuer le contenu créatif par défaut à chaque cible qui n’a pas encore reçu de lot de contenu créatif, cliquez sur **[!UICONTROL Assign Default Creatives]**. Après avoir consulté l’arborescence mise à jour avec les contenus publicitaires par défaut attribués, cliquez sur **[!UICONTROL Save]** et **[!UICONTROL OK]**.

      * Pour continuer à modifier l’arborescence de décision, cliquez sur **[!UICONTROL Continue Edit]**.

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
