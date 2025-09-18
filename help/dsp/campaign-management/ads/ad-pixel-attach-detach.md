---
title: Joindre et supprimer des pixels des publicités
description: Découvrez comment joindre et supprimer des pixels de suivi tiers des publicités.
feature: DSP Ads
source-git-commit: a3bd04da6c6f428fdb6e1f05187ea3de0174c9d7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Joindre et supprimer des pixels des publicités

Vous pouvez joindre et désolidariser les pixels de suivi tiers des publicités.

## Ouvrir la vue [!UICONTROL Ad Tools] {#ad-tools-open}

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Ouvrez la vue [!UICONTROL Ad Tools] de l’une des manières suivantes :

   * (Dans la vue [!UICONTROL Campaigns]) En regard du nom de la campagne, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Ad Tools].**

   * (Dans la vue [!UICONTROL Packages] , [!UICONTROL Placements] ou [!UICONTROL Ads] ) Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

## Association de pixels de suivi tiers aux publicités dans un emplacement {#attach-pixels-ads}

1. [Ouvrez la vue [!UICONTROL Ad Tools]](#ad-tools-open).

   L’onglet **[!UICONTROL Attach Pixels]** s’ouvre.

1. Dans le sous-affichage [!UICONTROL Edit] :

   1. (Facultatif) Localisez les annonces publicitaires et les pixels tiers de l’une des manières suivantes :

      * Au-dessus du tableau de gauche, cliquez sur ![Filtrer](/help/dsp/assets/filter.png) et filtrez les listes par statut publicitaire, type d’annonce, événement d’intégration de pixels ou type de pixels.

      * Au-dessus des tableaux de droite et de gauche, recherchez des chaînes de texte spécifiques dans les noms des annonces publicitaires et les noms des pixels.

   1. (S’il n’existe aucun pixel de suivi tiers pour la campagne) Créez un pixel :

      1. Dans le tableau de droite, cliquez sur **[!UICONTROL Create pixel]**.

      1. Spécifiez les paramètres :

         **[!UICONTROL Integration Event]:** événement qui déclenche le déclenchement du pixel, tel que *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image de 1x1 pixel), un *[!UICONTROL HTML]* ou un *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour le type de pixel spécifié.

         **[!UICONTROL Pixel Name]:** nom du pixel. Utilisez un nom qui vous permet d’identifier facilement le pixel.

         **[!UICONTROL Pixel Provider]:** fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

      1. Cliquez sur **[!UICONTROL Save]**.

   1. Dans le tableau de gauche, cochez la case en regard de chaque publicité pour laquelle vous souhaitez joindre des pixels de tracking tiers.

   1. Dans le tableau de droite, cochez la case en regard de chaque pixel de suivi tiers que vous souhaitez joindre aux annonces sélectionnées.

      Seuls les pixels qui ne sont pas déjà associés aux annonces sélectionnées peuvent être sélectionnés.

   1. En bas à droite, cliquez sur **[!UICONTROL Attach]**.

1. (Facultatif) Pour revenir aux vues détaillées de la campagne, cliquez sur ![Retour au dossier](/help/dsp/assets/breadcrumb-return.png "Retour au dossier") à gauche de [!UICONTROL Ad Tools] et sélectionnez le nom de la campagne.

## Désolidarisation des pixels de tracking tiers des publicités dans un emplacement {#detach-pixels-ads}

1. [Ouvrez la vue [!UICONTROL Ad Tools]](#ad-tools-open).

   L’onglet **[!UICONTROL Attach Pixels]** s’ouvre.

1. Dans le sous-affichage [!UICONTROL Edit] :

   1. (Facultatif) Localisez les annonces publicitaires et les pixels tiers de l’une des manières suivantes :

      * Au-dessus du tableau de gauche, cliquez sur ![Filtrer](/help/dsp/assets/filter.png) et filtrez les listes par statut publicitaire, type d’annonce, événement d’intégration de pixels ou type de pixels.

      * Au-dessus des tableaux de droite et de gauche, recherchez des chaînes de texte spécifiques dans les noms des annonces publicitaires et les noms des pixels.

   1. Dans le tableau de gauche, cochez la case en regard de chaque publicité dont vous souhaitez désolidariser les pixels de tracking tiers.

   1. Dans le tableau de droite, cochez la case en regard de chaque pixel de tracking tiers que vous souhaitez désolidariser des annonces sélectionnées.

      Seuls les pixels associés à toutes les publicités sélectionnées peuvent être sélectionnés.

   1. En bas à droite, cliquez sur **[!UICONTROL Detach]**.

1. (Facultatif) Pour revenir aux vues détaillées de la campagne, cliquez sur ![Retour au dossier](/help/dsp/assets/breadcrumb-return.png "Retour au dossier") à gauche de [!UICONTROL Ad Tools] et sélectionnez le nom de la campagne.

## Afficher les pixels associés aux publicités {#view-pixels-ads}

1. [Ouvrez la vue [!UICONTROL Ad Tools]](#ad-tools-open).

   L’onglet **[!UICONTROL Attach Pixels]** s’ouvre.

1. Passez à l’option **[!UICONTROL View]** dans le coin supérieur droit.

1. (Facultatif) Localisez les publicités et les pixels tiers selon les besoins :

   * Au-dessus du tableau de gauche, cliquez sur ![Filtrer](/help/dsp/assets/filter.png) et filtrez les listes par statut publicitaire, type d’annonce, événement d’intégration de pixels ou type de pixels.

   * Au-dessus des tableaux de droite et de gauche, recherchez des chaînes de texte spécifiques dans les noms des annonces publicitaires et les noms des pixels.

1. Cliquez sur n’importe quelle ligne d’annonce du tableau de gauche pour afficher les pixels joints dans le tableau de droite.

1. (Facultatif) Pour joindre plus de pixels aux publicités, passez à la vue **[!UICONTROL Edit]** en haut à droite. Pour obtenir des instructions, reportez-vous à l’étape 3 de la procédure précédente, « [Joindre des pixels de suivi tiers aux publicités dans un emplacement](#attach-pixels-ads) ».

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Joindre des annonces à des emplacements](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)
>* [Créer une publicité unique](ad-create.md)
>* [Créer plusieurs annonces publicitaires tierces](ad-create-multiple.md)
>* [Modifier une publicité](ad-edit.md)
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Modifier les plannings de publicités pour les emplacements](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [FAQ sur Universal Video](/help/dsp/campaign-management/faq-universal-video.md)

