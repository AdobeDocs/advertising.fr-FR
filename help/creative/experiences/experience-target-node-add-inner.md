---
title: Ajouter un nœud cible entre les nœuds d’une expérience
description: Découvrez comment ajouter un nœud cible entre les nœuds cibles dans une expérience publicitaire.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
TQID: 'https://experienceleague.adobe.com/lPQtymUs3okctV2t6ZEE2rMG-F-BA2tJZO1GuceTxtY'
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
source-wordcount: '1117'
ht-degree: 0%
---
# Ajouter un nœud cible entre les nœuds d’une expérience

*Expériences avec ciblage d’arborescence de décision uniquement*

Lorsque vous insérez un nœud cible entre des niveaux existants, le nouveau nœud cible conserve toutes les cibles enfants et les éléments créatifs existants et le nouveau nœud est initialement appelé « All ». Vous pouvez éventuellement conserver le nouveau nœud sans ajouter de cibles plus spécifiques.

Pour définir une cible spécifique, ajoutez un nœud cible frère supplémentaire au même niveau, spécifiez la nouvelle cible, puis affectez des contenus publicitaires uniquement à cette cible. L’ajout d’un nœud cible frère crée le nouveau nœud cible et déplace toutes les cibles enfants et les contenus publicitaires précédemment affectés à « All » vers un nouveau nœud « Tout le reste » au même niveau. Ainsi, l’ajout de la nouvelle cible n’affecte pas les branches enfants existantes, car seul le nouveau nœud frère inclut les nouvelles informations de ciblage.

>[!NOTE]
>
>Pour ajouter un nœud cible au niveau inférieur d’une arborescence de décision, voir « [&#x200B; Ajouter un nœud cible au niveau final d’une expérience &#x200B;](experience-target-node-add-final.md) ».

## Utilisation de l’éditeur piloté par l’IA (Beta) {#ai-editor}

Pendant que vous [créez](experience-create-targeting.md#ai-editor) ou [modifiez](experience-edit-targeting.md#ai-editor) l’expérience, vous pouvez demander à l’agent d’IA d’insérer un niveau cible. Identifiez où l’insérer et les branches et contenus publicitaires existants à conserver, puis passez en revue le résultat. Pour insérer le niveau directement dans la zone de travail :

1. A la limite où vous voulez insérer le niveau, cliquez sur **[!UICONTROL Add targeting level]**.

   En mode horizontal, ce contrôle est une icône portant le même libellé.

1. Dans **[!UICONTROL New targeting level]**, sélectionnez la catégorie cible, puis cliquez sur **[!UICONTROL Add targeting level]**.

   * Pour les cibles d’audience, sélectionnez **[!UICONTROL Audience]**.

   * Pour les cibles géographiques, sélectionnez une seule catégorie géographique (par exemple, **[!UICONTROL Geo: Country]**).

   * Pour les cibles de transfert de données, sélectionnez **[!UICONTROL Data Pass]**.

   * Pour recibler les cibles de pixels, sélectionnez **[!UICONTROL RT Pixel]**.

   * Pour les cibles d’appareil, sélectionnez une seule catégorie cible (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** ou **[!UICONTROL Device: Browser]**).

   L’insertion d’un niveau n’invite pas à saisir des valeurs cibles. Le nouveau niveau utilise initialement « Tous » et conserve les enfants cibles et les éléments créatifs existants.

1. (Facultatif) Pour définir une cible spécifique au nouveau niveau, [ajoutez un nœud cible frère](experience-target-node-add-sibling.md#ai-editor). Sinon, conservez le nouveau nœud « All » sans ajouter de cibles spécifiques.

1. (Facultatif) Pour renommer un nœud cible défini par l’utilisateur, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, saisissez le **[!UICONTROL Node Name]**, puis cliquez sur **[!UICONTROL Save]**.

   Vous ne pouvez pas renommer un nœud « Tous » ou « Tous les autres ».

1. Passez en revue les branches conservées et [affectez des lots créatifs](experience-assign-creative-bundles.md#ai-editor) à tous les nouveaux nœuds finaux.

1. [Enregistrez l’expérience](#save).

## Utilisation de l’éditeur manuel {#manual-editor}

[Ouvrez l’éditeur manuel](experience-edit-targeting.md#experience-open) avant de suivre ces étapes.

1. Sous le nœud où vous souhaitez insérer la cible, cliquez sur ![Ajouter](/help/creative/assets/add.png "Ajouter"), puis sélectionnez **[!UICONTROL Insert New Target]**.

1. Effectuez l’une des opérations suivantes :

   * Si les nœuds frères n’existent pas déjà, procédez comme suit :

     1. Sélectionnez le type de cible, puis cliquez sur **[!UICONTROL Apply]** :

        * Pour les cibles d’audience, sélectionnez **[!UICONTROL Audience]**.

        * Pour les cibles géographiques, sélectionnez une seule catégorie géographique (par exemple, **[!UICONTROL Geo: Country]**).

        * Pour les cibles de transfert de données, sélectionnez **[!UICONTROL Data Pass]**.

        * Pour recibler les cibles de pixels, sélectionnez **[!UICONTROL RT Pixel]**.

        * Pour les cibles d’appareil, sélectionnez une seule catégorie cible (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** ou **[!UICONTROL Device: Browser]**).

   * Si des nœuds frères existent déjà, procédez comme suit :

     * Pour les cibles d’audience :

       1. Cliquez sur **[!UICONTROL Click to Browse]** pour ouvrir les options de **[!UICONTROL Audience Targeting]**.

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

     * Pour les cibles géographiques, procédez comme suit :

       1. Cliquez sur **[!UICONTROL Click to Browse]** pour ouvrir les options de votre [!UICONTROL Geo Targeting], spécifiez une ou plusieurs cibles géographiques, puis cliquez sur **[!UICONTROL Save]**.

          Les cibles Code postal comportent des options de modification en bloc. Pour coller plusieurs codes postaux, cliquez sur l’onglet **[!UICONTROL Paste postal codes]** , sélectionnez le pays, collez ou saisissez des codes postaux séparés par des virgules ou sur des lignes distinctes, puis cliquez sur **[!UICONTROL Include All]**. Pour supprimer une cible de code postal incluse, placez le curseur sur la cible et cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer") **[!UICONTROL Remove]**.

       1. (Facultatif) Pour créer plusieurs nœuds cible lorsque plusieurs cibles géographiques sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

          Cette fonction crée un nœud cible distinct (avec des lots de création distincts) pour chaque cible géographique spécifiée. Si vous ne divisez pas les cibles, l’utilisateur doit appartenir à tous les emplacements spécifiés (instruction [!DNL Boolean] `AND`).

       1. Cliquez sur **[!UICONTROL Apply]**.

     * Pour une cible de transfert de données, personnalisez éventuellement la clé de transfert de données, saisissez une valeur de transfert de données unique, puis cliquez sur **[!UICONTROL Apply]**.

       La clé de transfert de données par défaut est configurée dans le champ **[!UICONTROL Data Pass]** de la section **[!UICONTROL Advanced]** des [paramètres généraux de l’expérience](experience-settings-targeting.md). Si nécessaire, personnalisez la clé de la cible.

     * Pour une cible de pixel de reciblage, sélectionnez un seul pixel de reciblage à utiliser et les valeurs de l’un des attributs de pixel requis pour afficher les contenus publicitaires, puis cliquez sur **[!UICONTROL Apply]**.

       Les attributs disponibles sont configurés dans les [paramètres des pixels de reciblage](/help/creative/pixels/retargeting-pixel-manage.md).

     * Pour les cibles d’appareil, procédez comme suit :

       1. Sélectionnez les cibles.

       1. (Facultatif) Pour créer plusieurs nœuds cible lorsque plusieurs cibles géographiques sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

          Cette fonction crée un nœud cible distinct (avec des lots de création distincts) pour chaque cible géographique spécifiée. Si vous ne divisez pas les cibles, l’utilisateur doit appartenir à tous les emplacements spécifiés (instruction [!DNL Boolean] `AND`).

       1. (Facultatif) Pour créer plusieurs nœuds cible lorsque plusieurs cibles géographiques sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

       1. Cliquez sur **[!UICONTROL Apply]**.

1. (Facultatif) Spécifiez un nom de branche personnalisé pour une branche définie par l’utilisateur.

   Par défaut, les branches définies par l’utilisateur sont étiquetées avec les cibles appliquées.

   Vous ne pouvez pas créer de nom de branche personnalisé pour une branche « Tous » ou « Tous les autres ».

   1. Placez le curseur sur le nœud cible, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Saisissez le **[!UICONTROL Node Name]**, puis cliquez sur **[!UICONTROL Save]**.

1. (Facultatif) [Attribuez des bundles de création](experience-assign-creative-bundles.md#manual-editor) au nouveau nœud cible et au nœud « Tout le reste ».

1. (Facultatif) [Ajoutez un nœud cible frère](experience-target-node-add-sibling.md#manual-editor) du type de cible spécifié.

## Enregistrer l’expérience {#save}

Les étapes suivantes s’appliquent aux deux éditeurs.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Ajoutez un nœud cible au niveau final](experience-target-node-add-final.md)
>* [Ajouter un nœud cible frère entre les nœuds](experience-target-node-add-sibling.md)
>* [Copiez les nœuds enfants et les contenus publicitaires dans un autre nœud au même niveau](experience-target-node-copy.md)
>* [Affecter des contenus publicitaires à un nœud final](experience-assign-creative-bundles.md)
>* [Supprimer un nœud cible ou un nœud feuille de contenu créatif](/help/creative/experiences/experience-target-node-delete.md)
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Modifier une expérience avec le ciblage d’arborescence de décision](experience-edit-targeting.md)
>* [Paramètres d’expérience ciblés](experience-settings-targeting.md)
