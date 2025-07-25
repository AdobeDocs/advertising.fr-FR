---
title: Ajouter un nœud cible entre les nœuds d’une expérience
description: Découvrez comment ajouter un nœud cible entre les nœuds cibles dans une expérience publicitaire.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
source-git-commit: 81cbb3cdac21f4b4899b0c07d1eb0686b7b3c7d4
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# Ajouter un nœud cible entre les nœuds d’une expérience

*Expériences avec ciblage d’arborescence de décision uniquement*
*Version bêta fermée*

Lorsque vous insérez un nœud cible entre des niveaux existants, le nouveau nœud cible conserve toutes les cibles enfants et les éléments créatifs existants et le nouveau nœud est initialement appelé « All ». Vous pouvez éventuellement conserver le nouveau nœud sans ajouter de cibles plus spécifiques.

Pour définir une cible spécifique, ajoutez un nœud cible frère supplémentaire au même niveau, spécifiez la nouvelle cible, puis affectez des contenus publicitaires uniquement à cette cible. L’ajout d’un nœud cible frère crée le nouveau nœud cible et déplace toutes les cibles enfants et les contenus publicitaires précédemment affectés à « All » vers un nouveau nœud « Tout le reste » au même niveau. Ainsi, l’ajout de la nouvelle cible n’affecte pas les branches enfants existantes, car seul le nouveau nœud frère inclut les nouvelles informations de ciblage.

>[!NOTE]
>
>Pour ajouter un nœud cible au niveau inférieur d’une arborescence de décision, voir « [ Ajouter un nœud cible au niveau final d’une expérience ](experience-target-node-add-final.md) ».

<!-- 1. [ways to get to the decision tree] -->

1. Sous le nœud où vous souhaitez insérer la cible, cliquez sur ![Ajouter](/help/creative/assets/add.png "Ajouter"), puis sélectionnez **[!UICONTROL Insert New Target]**.

1. Effectuez l’une des opérations suivantes :

   * Si les nœuds frères n’existent pas déjà, procédez comme suit :

      1. Sélectionnez le type de cible, puis cliquez sur **[!UICONTROL Apply]** :

         * Pour les cibles Audience Adobe, sélectionnez **[!UICONTROL Adobe Audience]**.

         * Pour les cibles géographiques, sélectionnez une seule catégorie géographique (par exemple, [!UICONTROL Geo: Country]).

         * Pour les cibles de transfert de données, sélectionnez **[!UICONTROL Data Pass]**.

         * Pour recibler les cibles de pixels, sélectionnez **[!UICONTROL RT Pixel].

         * Pour les cibles d’appareil, sélectionnez une seule catégorie cible (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** ou **[!UICONTROL Device: Browser]**).

   * Si des nœuds frères existent déjà, procédez comme suit :

      * Pour les cibles Audience d’Adobe, procédez comme suit :

         1. Cliquez sur **[!UICONTROL Click to Browse]** pour ouvrir vos options de [!UICONTROL Audience Targeting], ouvrez l’onglet **[!UICONTROL Adobe Segments]**, spécifiez une ou plusieurs des cibles d’audience [!DNL Adobe] de l’annonceur, puis cliquez sur **[!UICONTROL Create]**<!-- Why not "Save" like for the other node types/use cases? -->.

         1. (Facultatif) Pour créer plusieurs nœuds cibles lorsque plusieurs audiences sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

            Cette fonctionnalité crée un nœud cible distinct (avec des lots de création distincts) pour chaque audience spécifiée. Si vous ne fractionnez pas les cibles, l’utilisateur doit appartenir à toutes les audiences spécifiées (instruction [!DNL Boolean] `AND`).

         1. Cliquez sur **[!UICONTROL Apply]**.

      * Pour les cibles géographiques, procédez comme suit :

         1. Cliquez sur **[!UICONTROL Click to Browse]** pour ouvrir les options de votre [!UICONTROL Geo Targeting], spécifiez une ou plusieurs cibles géographiques, puis cliquez sur **[!UICONTROL Save]**.

            Les cibles Code postal comportent des options de modification en bloc. Pour coller plusieurs codes postaux, cliquez sur l’onglet **[!UICONTROL Paste postal codes]** , sélectionnez le pays, collez ou saisissez des codes postaux séparés par des virgules ou sur des lignes distinctes, puis cliquez sur **[!UICONTROL Include All]**. Pour supprimer une cible de code postal incluse, placez le curseur sur la cible et cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer") **[!UICONTROL Remove]**.

         1. (Facultatif) Pour créer plusieurs nœuds cible lorsque plusieurs cibles géographiques sont spécifiées, sélectionnez **[!UICONTROL Split targets to create nodes]**.

            Cette fonction crée un nœud cible distinct (avec des lots de création distincts) pour chaque cible géographique spécifiée. Si vous ne divisez pas les cibles, l’utilisateur doit appartenir à tous les emplacements spécifiés (instruction [!DNL Boolean] `AND`).

         1. Cliquez sur **[!UICONTROL Apply]**.

      * Pour une cible de transfert de données, personnalisez éventuellement la clé de transfert de données, saisissez une valeur de transfert de données unique, puis cliquez sur **[!UICONTROL Apply]**.

        Une valeur par défaut pour la clé de la paire clé-valeur est déjà définie dans le champ **[!UICONTROL Data Pass]** de la section [!UICONTROL Advanced] des [paramètres d’expérience](experience-settings-targeting.md). Vous pouvez éventuellement personnaliser la clé .

      * Pour une cible de pixel de reciblage, sélectionnez un seul pixel de reciblage à utiliser et les valeurs de l’un des attributs de pixel requis pour afficher les contenus publicitaires, puis cliquez sur **[!UICONTROL Apply]**.

        Les attributs du pixel de reciblage sont configurés dans les [paramètres du pixel de reciblage](/help/creative/pixels/retargeting-pixel-manage.md).

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

1. Effectuez l’une des opérations suivantes :

   * (Facultatif) [Attribuez des contenus publicitaires](experience-assign-creative-bundles.md) au nouveau nœud cible et au nœud « Tout le reste ».

   * (Facultatif) [Ajoutez un nœud cible frère](experience-target-node-add-sibling.md) du type de cible spécifié.

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
>* [Ajouter un nœud cible frère entre les nœuds](experience-target-node-add-sibling.md)
>* [Copiez les nœuds enfants et les contenus publicitaires dans un autre nœud au même niveau](experience-target-node-copy.md)
>* [Affecter des contenus publicitaires à un nœud final](experience-assign-creative-bundles.md)
>* [Supprimer un nœud cible ou un nœud feuille de contenu créatif](/help/creative/experiences/experience-target-node-delete.md)
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Modifier une expérience avec le ciblage d’arborescence de décision](experience-edit-targeting.md)
>* [Paramètres d’expérience ciblés](experience-settings-targeting.md)
