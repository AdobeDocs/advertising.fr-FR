---
title: Gestion des offres groupées de création
description: En savoir plus sur xxxx.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '1464'
ht-degree: 0%

---

# Gestion des offres groupées de création

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

Les bundles sont des groupes de contenus publicitaires que vous pouvez ajouter à une expérience en tant qu’unité. Après avoir créé un conteneur de bundle, vous pouvez joindre des contenus publicitaires au bundle. Les lots d’affichage standard ne peuvent contenir que des publicités display standard. Les lots de vidéos standard ne peuvent contenir que des publicités video standard. Quant aux lots d’affichage dynamique, ils ne peuvent contenir que des publicités display dynamiques. Vous pouvez remplacer les pages de destination, les balises de suivi d’impression et les balises de suivi des clics pour tous les contenus publicitaires d’un lot affecté à une expérience à partir de l’arborescence de décision d’expérience, sans affecter les contenus publicitaires de base.

[!DNL Creative] fait pivoter les contenus publicitaires du lot comme indiqué pour chaque expérience à laquelle le lot est affecté. Vous pouvez éventuellement [!DNL Creative] permettre d’optimiser les éléments publicitaires de n’importe quelle expérience en fonction des performances à l’aide de la rotation algorithmique des publicités, optimisée par Adobe Sensei.

Pour activer l’optimisation des éléments d’annonce publicitaire entre les lots dans une expérience d’annonce publicitaire, chaque lot ne peut inclure qu’une seule de chaque combinaison \[taille de création ou durée + langue\]. Par exemple, si une offre groupée comprend un élément créatif de 250 x 250 avec une langue par défaut « Français », vous ne pouvez pas ajouter un second élément créatif de 250 x 250 avec une langue par défaut « Français ». Si vous disposez de plusieurs contenus publicitaires de la même taille dans la même langue, ajoutez-les séparément à l’expérience.

Les contenus publicitaires associés à des offres groupées sont toujours disponibles en tant que contenus publicitaires individuels. Vous pouvez ajouter un élément créatif unique à plusieurs lots. Si vous modifiez les paramètres d’une création associée à un lot, les modifications sont propagées au lot. Cependant, toutes les pages de destination personnalisées, les balises de suivi des impressions et les balises de suivi des clics configurées pour les créatifs dans une expérience sont toujours utilisées pour l’expérience.

<!-- multiselect only to duplicate and delete -->

## Création d’un lot pour une bibliothèque de contenu créatif

Vous pouvez joindre un élément créatif à plusieurs lots.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**.

1. Saisissez un **[!UICONTROL Bundle Name]** unique et les **[!UICONTROL Bundle Type]:** *Affichage standard* (pour les contenus publicitaires d’affichage standard), *Affichage dynamique* (pour les contenus publicitaires d’affichage dynamique), *Vidéo standard* (pour les contenus publicitaires de vidéo standard).

1. Cliquez sur **[!UICONTROL Create]**.

## Répertorier les contenus publicitaires d’un lot

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des bibliothèques spécifiques.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Cliquez sur la carte ou la ligne du lot pour afficher tous les contenus publicitaires qu’il contient.

## Dupliquer les lots

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des bibliothèques spécifiques.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Sélectionnez les lots à dupliquer :

   * Pour dupliquer un seul lot :

      * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom du lot, puis cliquez sur **[!UICONTROL Duplicate]**.

      * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Duplicate]**.

   * Pour dupliquer un ou plusieurs lots, cochez la case correspondant à chaque lot à dupliquer. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Duplicate].**

     Pour sélectionner toutes les lignes, cochez la case globale dans le coin supérieur gauche.

   Les nouveaux lots sont nommés `<original name> (copy) # 1` (ou le numéro suivant dans la séquence). Par exemple, si vous créez deux doublons de « Test bundle », les doublons sont nommés « Test bundle (copy) # 1 » et « Test bundle (copy) # 2 ».

## Modifier le nom d’un lot

Les modifications apportées à un nom de lot sont propagées à toutes les expériences associées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Sélectionnez le lot :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de la bibliothèque, puis cliquez sur **[!UICONTROL Edit]**.

   * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Edit]**.

1. Modifiez le **[!UICONTROL Bundle Name]**.

   Le [!UICONTROL Bundle Name] doit être unique.

1. Cliquez sur **[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## Joindre des contenus publicitaires à une offre groupée

Vous pouvez joindre des contenus publicitaires d’affichage standard existants à une offre groupée d’affichage standard, des contenus vidéo standard à des offres groupées de vidéo standard et des contenus publicitaires d’affichage dynamique à une offre groupée dynamique. L’association d’un contenu créatif à un lot rend le contenu créatif disponible dans toutes les expériences auxquelles le lot est affecté. Chaque lot ne peut inclure qu’une seule de chaque combinaison \[taille de création ou durée + langue\].

>[!NOTE]
>
>Vous pouvez également [joindre des contenus publicitaires aux lots à partir des vues Publicités standard et Publicités dynamiques](creative-attach-detach-bundles.md).

### Joignez des contenus publicitaires à une offre groupée à partir de la liste Offres groupées .

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des bibliothèques spécifiques.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Sélectionnez le lot :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom du lot, puis cliquez sur **[!UICONTROL Attach Creatives]**.

   * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Attach Creatives]**.

   Chaque élément créatif éligible pour le type de bundle est répertorié dans le cadre de droite. Les contenus publicitaires déjà associés au lot sont répertoriés, mais ne peuvent pas être sélectionnés.

1. (Facultatif) Basculez entre la vue Tableau par défaut et une vue Carte des lots disponibles en cliquant sur ![Vue Carte](/help/creative/assets/card-view-button.png "Vue Carte") pour ouvrir la vue Carte ou ![Vue Tableau/liste](/help/creative/assets/table-view-button.png "Vue Tableau") pour revenir à la vue Tableau.

1. Dans le cadre de droite, cochez la case en regard de chaque élément créatif à joindre au lot, puis cliquez sur **[!UICONTROL Attach Creative to Bundle]**.

### Associez des contenus publicitaires à une offre groupée à partir de la liste des contenus publicitaires de l’offre groupée

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des bibliothèques spécifiques.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Cliquez sur la carte ou la ligne du lot pour afficher tous les contenus publicitaires qu’il contient.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Attach Creatives]**.

1. Dans le panneau de droite, cochez la case correspondant à chaque élément créatif à joindre.

1. Cliquez sur **[!UICONTROL Attach Creatives to Bundle]**.

## Désolidarisation de contenus publicitaires d’une offre groupée {#bundle-detach-creatives}

La désolidarisation d’un élément créatif d’un lot supprime l’association entre les deux, de sorte que l’élément créatif n’est plus utilisé pour les expériences qui ciblent le lot.

La désolidarisation d’un contenu créatif de l’offre groupée ne supprime pas le contenu créatif de l’onglet Contenu créatif de votre bibliothèque de contenus créatifs.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des bibliothèques spécifiques.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Cliquez sur la carte ou la ligne du lot pour afficher tous les contenus publicitaires qu’il contient.

1. Sélectionnez les contenus publicitaires à désolidariser du lot :

   * Pour désolidariser un élément créatif unique :

      * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom du contenu créatif, puis cliquez sur **[!UICONTROL Detach]**.

      * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Detach]**.

   * Pour désolidariser un ou plusieurs contenus publicitaires, cochez la case correspondant à chacun des contenus publicitaires que vous souhaitez désolidariser. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Detach]**.

     Pour sélectionner toutes les lignes, cochez la case globale dans le coin supérieur gauche.

## Prévisualisation d’un élément créatif unique dans une offre groupée

Vous pouvez prévisualiser une création telle que les visiteurs la verront, y compris sous forme de liens hypertexte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des bibliothèques spécifiques.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Cliquez sur la carte ou la ligne du lot pour afficher tous les contenus publicitaires qu’il contient.

1. Sélectionnez le contenu créatif :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom du contenu créatif, puis cliquez sur **[!UICONTROL Preview]**.

   * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Preview]**.

1. (Facultatif) Pour redimensionner l’image à l’écran, sélectionnez une option dans la liste **[!UICONTROL Zoom]**, de 10 % à 100 % de la taille de l’image.

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. (Facultatif) Pour ouvrir la page de destination du contenu créatif, cliquez sur le contenu créatif.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Facultatif) Pour télécharger le contenu créatif, cliquez sur ![Télécharger](/help/creative/assets/download.png "Télécharger").

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

## Prévisualiser toutes les créations d’un lot

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Sélectionnez le lot :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom du lot, puis cliquez sur **[!UICONTROL Preview]**.

   * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Preview]**.

1. (Facultatif) Pour filtrer les contenus publicitaires par langue, sélectionnez une option dans la liste **[!UICONTROL Language]**, puis cliquez sur **[!UICONTROL Preview]** dans le coin supérieur droit de l’aperçu.

1. (Facultatif) Pour filtrer les contenus publicitaires par taille, sélectionnez une option dans la liste **[!UICONTROL Size]**, puis cliquez sur **[!UICONTROL Preview]** dans le coin supérieur droit de l’aperçu.

1. (Facultatif) Pour redimensionner les images à l’écran, sélectionnez une option dans la liste **[!UICONTROL Zoom]**, de 10 % à 100 % de la taille de l’image.

1. (Facultatif) Pour ouvrir la page de destination d’un élément créatif, cliquez dessus.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Facultatif) Pour partager une URL de démonstration afin que d’autres personnes sans connexion à [!DNL Creative] puissent prévisualiser les contenus publicitaires :

   1. Cliquez sur ![Partager](/help/creative/assets/share.png "Partager") dans l’angle supérieur droit de l’aperçu.

   1. Dans la boîte de dialogue [!UICONTROL Share Demo URL], cliquez sur **[!UICONTROL Copy]** pour copier l’URL dans le presse-papiers afin de la partager avec une autre personne.

<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## Supprimer des lots

Vous pouvez supprimer des lots qui ne sont pas affectés à une expérience [en ligne](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses). Si un lot est affecté à une expérience active, [supprimez le lot de l’arborescence de décision](/help/creative/experiences/experience-target-node-delete.md) pour l’expérience avant de continuer.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des bibliothèques spécifiques.

1. Cliquez sur le nom de la bibliothèque.

1. Cliquez sur l’onglet **[!UICONTROL Bundles]** .

1. Sélectionnez les lots à supprimer :

   * Pour supprimer un seul lot :

      * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom du lot, puis cliquez sur **[!UICONTROL Delete]**.

      * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Delete]**.

   * Pour supprimer un ou plusieurs lots, cochez la case correspondant à chaque lot à supprimer. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete].**

     Pour sélectionner toutes les lignes, cochez la case globale dans le coin supérieur gauche.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Affectez et annulez l’affectation des lots de contenu créatif à un nœud final d’une expérience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Prévisualisation d’une création](/help/creative/creative-libraries/creative-preview.md)
>* [Ajouter des contenus publicitaires standard à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-standard.md)
>* [Gestion des bibliothèques de création](/help/creative/creative-libraries/creative-library-manage.md)
>* [À propos de vos bibliothèques de création](/help/creative/creative-libraries/creative-libraries-about.md)
