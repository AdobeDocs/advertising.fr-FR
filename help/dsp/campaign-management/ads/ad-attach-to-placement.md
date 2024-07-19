---
title: Joindre des publicités à des emplacements
description: Découvrez comment joindre des publicités à des emplacements.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Joindre des publicités à des emplacements

Utilisez la vue [!UICONTROL Ad Tools] pour joindre des publicités à des emplacements, joindre des pixels de suivi tiers aux publicités et détacher les pixels de suivi tiers existants des publicités.

>[!NOTE]
>
>Les publicités vidéo universelles ne peuvent être associées qu’à des emplacements vidéo universels.

## Ouvrez la vue [!UICONTROL Ad Tools]. {#ad-tools-open}

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Ouvrez la vue [!UICONTROL Ad Tools] de l’une des manières suivantes :

   * (Dans la vue [!UICONTROL Packages] , [!UICONTROL Placements] ou [!UICONTROL Ads]) Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (Dans la vue [!UICONTROL Placements]) En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (Dans la vue [!UICONTROL Ads]) En regard du nom de la publicité, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   L’onglet [!UICONTROL Attach Ads] est sélectionné par défaut.

## Joindre des publicités à des emplacements {#attach-ads-campaign}

1. [Ouvrez la vue [!UICONTROL Ad Tools]](#ad-tools-open).

1. Dans la sous-vue [!UICONTROL Edit], procédez comme suit pour chaque groupe de publicités que vous souhaitez joindre à des emplacements :

   1. (Facultatif) Recherchez des emplacements et des publicités spécifiques de l’une des façons suivantes :

      * Au-dessus du tableau de gauche, cliquez sur ![Filtrer](/help/dsp/assets/filter.png) et filtrez les listes par package, type d’emplacement, état d’emplacement, type de publicité ou état de publicité.

      * Au-dessus des tableaux de droite et de gauche, recherchez des chaînes de texte spécifiques dans les noms des emplacements et des publicités.

   1. Dans le tableau de gauche, cochez la case en regard de chaque emplacement auquel joindre les publicités.

   1. Dans le tableau de droite, cochez la case en regard de chaque publicité à joindre aux emplacements sélectionnés.

      Seules les publicités applicables au type d’emplacement et qui ne sont pas déjà jointes aux emplacements sélectionnés peuvent être sélectionnées.

   1. En bas à droite, cliquez sur **[!UICONTROL Attach]**.

1. (Facultatif) Pour revenir aux vues détaillées de la campagne, cliquez sur ![Revenir au dossier](/help/dsp/assets/breadcrumb-return.png "Revenir au dossier") à gauche de [!UICONTROL Ad Tools] et sélectionnez le nom de la campagne.

## Afficher les publicités liées aux emplacements {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Ouvrez la vue [!UICONTROL Ad Tools]](#ad-tools-open).

1. Passez à l’option **[!UICONTROL View]** en haut à droite.

1. (Facultatif) Recherchez des emplacements et des publicités spécifiques si nécessaire :

   * Au-dessus du tableau de gauche, cliquez sur ![Filtrer](/help/dsp/assets/filter.png) et filtrez les listes par package, type d’emplacement, état d’emplacement, type de publicité ou état de publicité.

   * Dans les tableaux de droite et de gauche, recherchez des chaînes de texte spécifiques dans le nom de l’emplacement ou de la publicité.

1. Cliquez sur n’importe quelle ligne d’emplacement dans le tableau de gauche pour afficher les publicités jointes dans le tableau de droite.

1. (Facultatif) Pour joindre davantage de publicités aux emplacements de la campagne, basculez vers la vue **[!UICONTROL Edit]** en haut à droite. Voir l’étape 2 de la procédure précédente, &quot;[Joindre des publicités à des emplacements](#attach-ads-campaign)&quot;, pour obtenir des instructions.

## Joindre des pixels de suivi tiers à des publicités dans un emplacement {#attach-pixels-ads}

1. [Ouvrez la vue [!UICONTROL Ad Tools]](#ad-tools-open).

1. Cliquez sur l’onglet **[!UICONTROL Attach Pixels]** .

1. Dans la sous-vue [!UICONTROL Edit] :

   1. (Facultatif) Recherchez des publicités et des pixels tiers de l’une des manières suivantes :

      * Au-dessus du tableau de gauche, cliquez sur ![Filtrer](/help/dsp/assets/filter.png) et filtrez les listes par état de publicité, type de publicité, événement d’intégration de pixel ou type de pixel.

      * Au-dessus des tableaux de droite et de gauche, recherchez des chaînes de texte spécifiques dans les noms de publicité et de pixel.

   1. (S’il n’existe aucun pixel de suivi tiers pour la campagne) Créez un pixel :

      1. Dans la table de droite, cliquez sur **[!UICONTROL Create pixel]**.

      1. Spécifiez les paramètres :

         **[!UICONTROL Integration Event]:** événement qui déclenche le déclenchement du pixel, par exemple *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** URL de l’image de pixel, au format approprié pour le type de pixel spécifié.

         **[!UICONTROL Pixel Name]:** Nom du pixel. Utilisez un nom qui vous aide à identifier facilement le pixel.

         **[!UICONTROL Pixel Provider]:** Fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

      1. Cliquez sur **[!UICONTROL Save]**.

   1. Dans le tableau de gauche, cochez la case en regard de chaque publicité pour laquelle vous souhaitez joindre des pixels de suivi tiers.

   1. Dans le tableau de droite, cochez la case en regard de chaque pixel de suivi tiers que vous souhaitez joindre aux publicités sélectionnées.

      Seuls les pixels qui ne sont pas déjà attachés aux publicités sélectionnées peuvent être sélectionnés.

   1. En bas à droite, cliquez sur **[!UICONTROL Attach]**.

1. (Facultatif) Pour revenir aux vues détaillées de la campagne, cliquez sur ![Revenir au dossier](/help/dsp/assets/breadcrumb-return.png "Revenir au dossier") à gauche de [!UICONTROL Ad Tools] et sélectionnez le nom de la campagne.

## Désolidariser des pixels de suivi tiers des publicités dans un emplacement {#detach-pixels-ads}

1. [Ouvrez la vue [!UICONTROL Ad Tools]](#ad-tools-open).

1. Cliquez sur l’onglet **[!UICONTROL Attach Pixels]** .

1. Dans la sous-vue [!UICONTROL Edit] :

   1. (Facultatif) Recherchez des publicités et des pixels tiers de l’une des manières suivantes :

      * Au-dessus du tableau de gauche, cliquez sur ![Filtrer](/help/dsp/assets/filter.png) et filtrez les listes par état de publicité, type de publicité, événement d’intégration de pixel ou type de pixel.

      * Au-dessus des tableaux de droite et de gauche, recherchez des chaînes de texte spécifiques dans les noms de publicité et de pixel.

   1. Dans le tableau de gauche, cochez la case en regard de chaque publicité à partir de laquelle vous souhaitez détacher les pixels de suivi tiers.

   1. Dans le tableau de droite, cochez la case en regard de chaque pixel de suivi tiers que vous souhaitez dissocier des publicités sélectionnées.

      Seuls les pixels attachés à toutes les publicités sélectionnées peuvent être sélectionnés.

   1. En bas à droite, cliquez sur **[!UICONTROL Detach]**.

1. (Facultatif) Pour revenir aux vues détaillées de la campagne, cliquez sur ![Revenir au dossier](/help/dsp/assets/breadcrumb-return.png "Revenir au dossier") à gauche de [!UICONTROL Ad Tools] et sélectionnez le nom de la campagne.

## Afficher les pixels attachés aux publicités {#view-pixels-ads}

1. [Ouvrez la vue [!UICONTROL Ad Tools]](#ad-tools-open).

1. Cliquez sur l’onglet **[!UICONTROL Attach Pixels]** .

1. Passez à l’option **[!UICONTROL View]** en haut à droite.

1. (Facultatif) Recherchez des publicités et des pixels tiers si nécessaire :

   * Au-dessus du tableau de gauche, cliquez sur ![Filtrer](/help/dsp/assets/filter.png) et filtrez les listes par état de publicité, type de publicité, événement d’intégration de pixel ou type de pixel.

   * Au-dessus des tableaux de droite et de gauche, recherchez des chaînes de texte spécifiques dans les noms de publicité et de pixel.

1. Cliquez sur n’importe quelle ligne d’annonce dans le tableau de gauche pour afficher les pixels joints dans le tableau de droite.

1. (Facultatif) Pour attacher davantage de pixels aux publicités, basculez vers la vue **[!UICONTROL Edit]** dans l’angle supérieur droit. Voir l’étape 3 de la procédure précédente, &quot;[Joindre des pixels de suivi tiers à des publicités dans un emplacement](#attach-pixels-ads)&quot;, pour obtenir des instructions.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Créer plusieurs publicités tierces](ad-create-multiple.md)
>* [Modifier une publicité](ad-edit.md)
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Modifier les planifications de publicité pour les emplacements](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [ Questions fréquentes à propos de la vidéo universelle ](/help/dsp/campaign-management/faq-universal-video.md)
