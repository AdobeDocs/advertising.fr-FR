---
title: Ajouter un nœud cible au niveau final d’une expérience
description: Découvrez comment ajouter un nœud cible au niveau cible final d’une expérience publicitaire.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
TQID: 'https://experienceleague.adobe.com/1T0Jwc8noxF-uaTA2cN78uOBsgHDjSnoD9Scmmw4L3s'
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
source-wordcount: '1225'
ht-degree: 0%
---
# Ajouter un nœud cible au niveau final d’une expérience

*Expériences avec ciblage d’arborescence de décision uniquement*

Lorsque vous ajoutez un nœud cible au niveau le plus bas de l’expérience, qu’il s’agisse du nœud racine « Tous », d’un nœud spécifique à la cible ou d’un nœud « Tout le reste », vous définissez directement la cible et n’avez pas besoin de créer de nœud frère. L’ajout d’un nœud de niveau inférieur crée le nœud cible et un nœud « Tout le reste » supplémentaire au même niveau.

>[!NOTE]
>
>Pour insérer un nœud cible entre les niveaux existants d’une arborescence de décision, consultez « [&#x200B; Insérer un nœud cible entre les nœuds d’une expérience &#x200B;](experience-target-node-add-inner.md) ».

## Utilisation de l’éditeur piloté par l’IA (Beta) {#ai-editor}

Pendant que vous [créez](experience-create-targeting.md#ai-editor) ou [modifiez](experience-edit-targeting.md#ai-editor) l’expérience, vous pouvez décrire la nouvelle cible et sa branche parente à l’agent d’IA. Examinez l’arborescence résultante avant d’enregistrer. Pour ajouter la cible directement dans la zone de travail :

1. Placez le curseur au-dessus du nœud parent à la fin de la branche, puis cliquez sur **[!UICONTROL +]**.

1. Dans **[!UICONTROL New targeting level]**, sélectionnez la catégorie cible, puis cliquez sur **[!UICONTROL Add targeting level]**.

1. Indiquez les valeurs cibles pour la catégorie :

   * Pour les cibles d’audience :

     * Pour ajouter le premier segment, recherchez et sélectionnez le segment ciblé.

     * Pour ajouter des segments à un groupe de segments existant :

       1. Sélectionnez le groupe de segments.

       1. (Facultatif) Modifiez la logique de groupe en **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**, selon les besoins.

          **[!UICONTROL Include Any]** correspond aux utilisateurs d’au moins un segment sélectionné ; **[!UICONTROL Include All]** nécessite une adhésion à tous les segments sélectionnés.

          **[!UICONTROL Exclude All]** n’est pas disponible pour le premier groupe de segments. Dans le cas d’une audience qui comprend uniquement des exclusions, créez l’audience à l’aide de **[!UICONTROL Include Any]**, puis excluez cette audience lorsque vous l’ajoutez à un emplacement de votre DSP.

       1. Recherchez et sélectionnez les segments supplémentaires.

     * Pour ajouter un nouveau groupe de segments :

       1. Ajoutez un groupe.

       1. (Facultatif) Modifiez la logique entre le groupe précédent et le nouveau groupe en **[!UICONTROL And]** ou **[!UICONTROL Or]**, selon les besoins.

          **[!UICONTROL And]** exige que les utilisateurs et utilisatrices remplissent les conditions des deux groupes ; **[!UICONTROL Or]** exige qu’ils remplissent au moins les conditions d’un groupe.

       1. Recherchez et sélectionnez les segments pour le nouveau groupe.

       1. (Facultatif) Modifiez la logique de groupe en **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**, selon les besoins.

   * Pour les objectifs géographiques :

     * Sélectionnez les emplacements au sein de la catégorie géographique que vous avez choisie, tels que les pays, les régions ou les villes.

     * Pour les cibles de code postal, sélectionnez le pays et saisissez les codes postaux à inclure. Pour saisir plusieurs codes postaux en bloc, séparez-les par des virgules ou placez chaque code sur une ligne distincte.

   * Pour les cibles de transfert de données, saisissez la clé et la valeur à faire correspondre.

     La clé de transfert de données par défaut est configurée dans le champ **[!UICONTROL Data Pass]** de la section **[!UICONTROL Advanced]** des [paramètres généraux de l’expérience](experience-settings-targeting.md). Si nécessaire, personnalisez la clé de la cible.

   * Pour le reciblage des cibles de pixels, sélectionnez le pixel de reciblage et spécifiez les valeurs de tous les attributs de pixel requis pour afficher les éléments créatifs.

     Les attributs disponibles sont configurés dans les [paramètres des pixels de reciblage](/help/creative/pixels/retargeting-pixel-manage.md).

   * Pour les cibles d’appareil, sélectionnez les valeurs dans la catégorie d’appareil choisie : types d’appareil, systèmes d’exploitation ou navigateurs.

1. (Si disponible ; facultatif) Sélectionnez **[!UICONTROL Split Nodes]** pour créer un nœud cible distinct pour chaque valeur sélectionnée, avec ses propres affectations de lot de création. Dans le cas contraire, les valeurs sélectionnées seront regroupées dans un nœud cible.

1. Cliquez sur **[!UICONTROL Add Node]**.

1. (Facultatif) Pour renommer un nœud cible défini par l’utilisateur, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, saisissez le **[!UICONTROL Node Name]**, puis cliquez sur **[!UICONTROL Save]**.

   Vous ne pouvez pas renommer un nœud « Tous » ou « Tous les autres ».

1. [Attribuez des lots de contenu créatif](experience-assign-creative-bundles.md#ai-editor) aux nouveaux nœuds finaux, y compris la branche de secours, ou utilisez des contenus créatifs par défaut lorsque vous [enregistrez l’expérience](#save).

## Utilisation de l’éditeur manuel {#manual-editor}

[Ouvrez l’éditeur manuel](experience-edit-targeting.md#experience-open) avant de suivre ces étapes.

1. Sous le nœud où vous souhaitez insérer la cible, cliquez sur ![Ajouter](/help/creative/assets/add.png "Ajouter"), puis sélectionnez **[!UICONTROL Insert New Target]**.

1. Indiquez les valeurs cibles pour la catégorie :

   * Pour les cibles d’audience :

     1. Sélectionnez **[!UICONTROL Audience]**, puis cliquez sur **[!UICONTROL Click to Browse]** pour ouvrir les options **[!UICONTROL Audience Targeting]**.

     1. Configurez les segments et groupes d’audience :

        * Pour ajouter le premier segment, localisez le segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

        * Pour ajouter des segments à un groupe de segments existant :

          1. Cliquez sur le groupe de segments dans le panneau de droite.

          1. (Facultatif) Modifiez la logique de groupe en **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**, selon les besoins.

             **[!UICONTROL Include Any]** correspond aux utilisateurs d’au moins un segment sélectionné ; **[!UICONTROL Include All]** nécessite une adhésion à tous les segments sélectionnés.

             **[!UICONTROL Exclude All]** n’est pas disponible pour le premier groupe de segments. Dans le cas d’une audience qui comprend uniquement des exclusions, créez l’audience à l’aide de **[!UICONTROL Include Any]**, puis excluez cette audience lorsque vous l’ajoutez à un emplacement de votre DSP.

          1. Recherchez le nouveau segment dans le panneau de gauche, puis cochez la case en regard du nom du segment. Répétez l’opération pour chaque segment supplémentaire.

             Le groupe de segments est automatiquement mis à jour avec les nouveaux segments.

        * Pour ajouter un nouveau groupe de segments :

          1. Cliquez sur **[!UICONTROL + New Group]** dans le panneau de droite.

          1. (Facultatif) Modifiez la logique entre le groupe précédent et le nouveau groupe en **[!UICONTROL And]** ou **[!UICONTROL Or]**, selon les besoins.

             **[!UICONTROL And]** exige que les utilisateurs et utilisatrices remplissent les conditions des deux groupes ; **[!UICONTROL Or]** exige qu’ils remplissent au moins les conditions d’un groupe.

          1. Recherchez les segments du nouveau groupe dans le panneau de gauche, puis cochez les cases en regard des noms de segment.

          1. (Facultatif) Modifiez la logique de groupe en **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**, selon les besoins.

     1. Cliquez sur **[!UICONTROL Create]**.

     1. Cliquez sur **[!UICONTROL Apply]**.

   * Pour les cibles géographiques, sélectionnez une seule catégorie géographique (par exemple, **[!UICONTROL Geo: Country]**), puis procédez comme suit :

     1. Cliquez sur **[!UICONTROL Click to Browse]** pour ouvrir les options de votre [!UICONTROL Geo Targeting], spécifiez une ou plusieurs cibles géographiques, puis cliquez sur **[!UICONTROL Save]**.

        Les cibles Code postal comportent des options de modification en bloc. Pour coller plusieurs codes postaux, cliquez sur l’onglet **[!UICONTROL Paste postal codes]** , sélectionnez le pays, collez ou saisissez des codes postaux séparés par des virgules ou sur des lignes distinctes, puis cliquez sur **[!UICONTROL Include All]**. Pour supprimer une cible de code postal incluse, placez le curseur sur la cible et cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer") **[!UICONTROL Remove]**.

     1. (Facultatif) Pour créer plusieurs nœuds cible lorsque plusieurs cibles géographiques sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

        Cette fonction crée un nœud cible distinct (avec des lots de création distincts) pour chaque cible géographique spécifiée. Si vous ne divisez pas les cibles, l’utilisateur doit appartenir à tous les emplacements spécifiés (instruction [!DNL Boolean] `AND`).

     1. Cliquez sur **[!UICONTROL Apply]**.

   * Pour une cible de transfert de données, sélectionnez **[!UICONTROL Data Pass]**, personnalisez éventuellement la clé de transfert de données, saisissez une valeur de transfert de données unique, puis cliquez sur **[!UICONTROL Apply]**.

     La clé de transfert de données par défaut est configurée dans le champ **[!UICONTROL Data Pass]** de la section **[!UICONTROL Advanced]** des [paramètres généraux de l’expérience](experience-settings-targeting.md). Si nécessaire, personnalisez la clé de la cible.

   * Pour une cible de pixel de reciblage, sélectionnez **[!UICONTROL RT Pixel]**, sélectionnez un seul pixel de reciblage à utiliser et les valeurs de l’un des attributs de pixel requis pour afficher les contenus publicitaires, puis cliquez sur **[!UICONTROL Apply]**.

     Les attributs disponibles sont configurés dans les [paramètres des pixels de reciblage](/help/creative/pixels/retargeting-pixel-manage.md).

   * Pour les cibles d’appareil, procédez comme suit :

     1. Sélectionnez une seule catégorie cible (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** ou **[!UICONTROL Device: Browser]**), puis sélectionnez les cibles.

     1. (Facultatif) Pour créer plusieurs nœuds cible lorsque plusieurs cibles géographiques sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

        Cette fonction crée un nœud cible distinct (avec des lots de création distincts) pour chaque cible géographique spécifiée. Si vous ne divisez pas les cibles, l’utilisateur doit appartenir à tous les emplacements spécifiés (instruction [!DNL Boolean] `AND`).

     1. Cliquez sur **[!UICONTROL Apply]**.

1. (Facultatif) Spécifiez un nom de branche personnalisé pour une branche définie par l’utilisateur.

   Par défaut, les branches définies par l’utilisateur sont étiquetées avec les cibles appliquées.

   Vous ne pouvez pas créer de nom de branche personnalisé pour une branche « Tous » ou « Tous les autres ».

   1. Placez le curseur sur le nœud cible, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Saisissez le **[!UICONTROL Node Name]**, puis cliquez sur **[!UICONTROL Save]**.

1. (Facultatif) [Attribuez des bundles de création](experience-assign-creative-bundles.md#manual-editor) au nouveau nœud cible et au nœud « Tout le reste ».

## Enregistrer l’expérience {#save}

Les étapes suivantes s’appliquent aux deux éditeurs.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Insérez un nœud cible entre les nœuds](experience-target-node-add-inner.md)
>* [Ajouter un nœud cible frère entre les nœuds](experience-target-node-add-sibling.md)
>* [Copiez les nœuds enfants et les contenus publicitaires dans un autre nœud au même niveau](experience-target-node-copy.md)
>* [Affecter des contenus publicitaires à un nœud final](experience-assign-creative-bundles.md)
>* [Supprimer un nœud cible ou un nœud feuille de contenu créatif](/help/creative/experiences/experience-target-node-delete.md)
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Modifier une expérience avec le ciblage d’arborescence de décision](experience-edit-targeting.md)
>* [Paramètres d’expérience ciblés](experience-settings-targeting.md)
