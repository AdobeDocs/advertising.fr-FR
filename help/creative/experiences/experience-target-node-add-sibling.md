---
title: Ajouter un nœud cible frère entre les nœuds d’une expérience
description: Découvrez comment ajouter un nœud frère à tout nœud qui a une cible ou qui se trouve au même niveau qu’un nœud avec une cible.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: f71747a4973ec3f3e2c3a8a5913d27311849883c
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Ajouter un nœud cible frère entre les nœuds d’une expérience

*Expériences avec ciblage d’arborescence de décision uniquement*
*Version bêta fermée*

Vous pouvez ajouter un nœud frère à tout nœud qui a une cible ou qui se trouve au même niveau qu’un nœud ayant une cible.

<!-- 1. Open the decision tree:


In a new experience


In an existing experience,
 -->

1. Au-dessus du nœud auquel vous souhaitez ajouter le nœud frère, cliquez sur ![Ajouter](/help/creative/assets/add.png "Ajouter"), puis sélectionnez **[!UICONTROL Insert Sibling Target]**.

1. Spécifiez les cibles :

   * Pour les cibles d’audience, procédez comme suit :

      1. Cliquez sur **[!UICONTROL Click to Browse]** pour ouvrir les options de votre [!UICONTROL Audience Targeting], puis procédez comme suit :

         * Pour ajouter le premier segment, localisez le segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

         * Pour ajouter un segment à un groupe de segments existant :

            1. Cliquez sur le groupe de segments dans le panneau de droite.

            1. (Facultatif) Modifiez la logique de groupe en *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, selon les besoins.

               *[!UICONTROL Exclude All]* n’est pas disponible pour le premier groupe de segments. Dans le cas d’une audience qui comprend uniquement des exclusions, créez cette audience sous la forme *[!UICONTROL Include Any]*, puis excluez-la lorsque vous l’ajoutez à un emplacement de votre DSP.

            1. Recherchez le nouveau segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

               Le groupe de segments est automatiquement mis à jour avec le nouveau segment.

         * Pour ajouter un nouveau groupe de segments :

         1. Cliquez sur **[!UICONTROL + New Group]** dans le panneau de droite.

         1. (Facultatif) Modifiez la logique entre le groupe précédent et le nouveau groupe en *[!UICONTROL And]* ou *[!UICONTROL Or]*, selon les besoins.

         1. Recherchez les segments du nouveau groupe dans le panneau de gauche, puis cochez les cases en regard des noms de segment.

         1. (Facultatif) Modifiez la logique de groupe en *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, selon les besoins.

      1. Cliquez sur **[!UICONTROL Create]**.

      1. Cliquez sur **[!UICONTROL Apply]**.

   * Pour les cibles géographiques, procédez comme suit :

      1. Cliquez sur **[!UICONTROL Click to Browse]** pour ouvrir les options de votre [!UICONTROL Geo Targeting], spécifiez une ou plusieurs cibles géographiques, puis cliquez sur **[!UICONTROL Save]**.

         Les cibles Code postal comportent des options de modification en bloc. Pour coller plusieurs codes postaux, cliquez sur l’onglet **[!UICONTROL Paste postal codes]** , sélectionnez le pays, collez ou saisissez des codes postaux séparés par des virgules ou sur des lignes distinctes, puis cliquez sur **[!UICONTROL Include All]**. Pour supprimer une cible de code postal incluse, placez le curseur sur la cible et cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer") **[!UICONTROL Remove]**.

      1. (Facultatif) Pour créer plusieurs nœuds cible lorsque plusieurs cibles géographiques sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

         Cette fonction crée un nœud cible distinct (avec des lots de création distincts) pour chaque cible géographique spécifiée. Si vous ne divisez pas les cibles, l’utilisateur doit appartenir à tous les emplacements spécifiés (instruction [!DNL Boolean] `AND`).

      1. Cliquez sur **[!UICONTROL Apply]**.

   * Pour les cibles de transfert de données, vous pouvez éventuellement personnaliser la clé de transfert de données, saisir une valeur de transfert de données unique, puis cliquer sur **[!UICONTROL Apply]**.

     Une valeur par défaut pour la clé de la paire clé-valeur est déjà définie dans le champ **[!UICONTROL Data Pass]** de la section [!UICONTROL Advanced] des [paramètres d’expérience](experience-settings-targeting.md). Vous pouvez éventuellement personnaliser la clé .

   * Pour le reciblage des cibles de pixels, sélectionnez le pixel de reciblage à utiliser et les valeurs requises pour l’un des attributs de pixel devant être présent pour afficher les éléments créatifs. Cliquez ensuite sur **[!UICONTROL Apply]**.

     Les attributs du pixel de reciblage sont configurés dans les [paramètres du pixel de reciblage](/help/creative/pixels/retargeting-pixel-manage.md).

   * Pour les cibles d’appareil, procédez comme suit :

      1. Sélectionnez les cibles.

      1. (Facultatif) Pour créer plusieurs nœuds cible lorsque plusieurs cibles géographiques sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

         Cette fonction crée un nœud cible distinct (avec des lots de création distincts) pour chaque cible géographique spécifiée. Si vous ne divisez pas les cibles, l’utilisateur doit appartenir à tous les emplacements spécifiés (instruction [!DNL Boolean] `AND`).

      1. Cliquez sur **[!UICONTROL Apply]**.

1. (Facultatif) Spécifiez un nom de branche personnalisé pour une branche définie par l’utilisateur.

   Par défaut, les branches définies par l’utilisateur sont étiquetées avec les cibles appliquées.

   Vous ne pouvez pas créer de nom de branche personnalisé pour une branche « Tous » ou « Tous les autres ».

   1. Placez le curseur sur le nœud cible, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Saisissez le **[!UICONTROL Node Name]**, puis cliquez sur **[!UICONTROL Save]**.

1. Effectuez l’une des opérations suivantes :

   * (Facultatif) [Attribuez des contenus publicitaires](experience-assign-creative-bundles.md) au nouveau nœud cible.

   * (Facultatif) Pour enregistrer l’expérience :

      1. Cliquez sur **[!UICONTROL Save]**, puis sur **[!UICONTROL OK]**.

      1. (Si chaque nœud du niveau le plus bas n’inclut pas au moins un élément créatif) : Effectuez l’une des opérations suivantes :

         * Pour enregistrer l’expérience sans tous les lots de création requis, cliquez sur **[!UICONTROL Save as Draft]**.

           Vous ne pouvez pas créer de balise publicitaire pour une expérience de brouillon.

         * Pour attribuer le contenu créatif par défaut à chaque cible qui n’a pas encore reçu de lot de contenu créatif, cliquez sur **[!UICONTROL Assign Default Creatives]**. Après avoir consulté l’arborescence mise à jour avec les contenus publicitaires par défaut attribués, cliquez sur **[!UICONTROL Save]** et **[!UICONTROL OK]**.

         * Pour continuer à modifier l’arborescence de décision, cliquez sur **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Ajoutez un nœud cible au niveau final](experience-target-node-add-final.md)
>* [Insérez un nœud cible entre les nœuds](experience-target-node-add-inner.md)
>* [Copiez les nœuds enfants et les contenus publicitaires dans un autre nœud au même niveau](experience-target-node-copy.md)
>* [Affecter des contenus publicitaires à un nœud final](experience-assign-creative-bundles.md)
>* [Supprimer un nœud cible ou un nœud feuille de contenu créatif](/help/creative/experiences/experience-target-node-delete.md)
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Modifier une expérience avec le ciblage d’arborescence de décision](experience-edit-targeting.md)
>* [Paramètres d’expérience ciblés](experience-settings-targeting.md)
