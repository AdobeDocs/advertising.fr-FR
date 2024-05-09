---
title: Gestion des multiplicateurs d’offre pour les emplacements
description: Découvrez comment créer et modifier des multiplicateurs d’offre pour des cibles d’emplacement spécifiées.
feature: DSP Placements
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Gestion des multiplicateurs d’offre pour les emplacements


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

Cette fonctionnalité vous permet de modifier les multiplicateurs d’offre pour vos cibles d’emplacement existantes.

Pour modifier les cibles sélectionnées pour vos emplacements, voir &quot;[Modifier les emplacements](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Gestion des multiplicateurs d’offre pour un ou plusieurs emplacements

Pour tous les emplacements sélectionnés, vous pouvez soit modifier manuellement les valeurs, soit charger une feuille de calcul contenant des valeurs.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez gérer les multiplicateurs d’offre.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Réglez manuellement les multiplicateurs d’offres pour la cible éligible ou en chargeant un fichier CSV avec des valeurs cibles :

   * Pour ajuster manuellement les valeurs du multiplicateur d&#39;offre, déplacez-vous vers chaque onglet spécifique à la cible ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], et[!UICONTROL Brand Safety]) et modifiez les valeurs existantes pour les cibles de placement.

   Les mêmes modifications s’appliquent à tous les emplacements sélectionnés.

   * Pour charger un fichier CSV avec des valeurs de multiplicateur d’offre qui remplaceront les valeurs existantes :

     >[!NOTE]
     >
     >Si vous laissez un champ vide, toutes les valeurs de ce type de cible sont supprimées.<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there will be only one data row applicable for all. -->

      1. Cliquez sur **[!UICONTROL CSV Edit]** en haut à droite.

      1. a) cliquez sur **[!UICONTROL Download Template]** et modifiez les valeurs du multiplicateur d&#39;offre ou b) modifiez un modèle téléchargé précédemment. Enregistrez le fichier modifié sur votre périphérique ou réseau.

      1. A) faites glisser et déposez le fichier modifié dans la zone ou b) cliquez dans la zone pour sélectionner le fichier sur votre périphérique ou réseau.

   1. Cliquez sur **[!UICONTROL Upload]**.

   Par défaut, le multiplicateur d’offre pour une cible est de 1,00, ce qui signifie que l’offre n’est pas ajustée pour cette cible. Les valeurs peuvent être comprises entre 0,10 et 10,00. Par exemple, un modificateur d’offre de 0,5 réduit une offre de 6 USD à 3 (0,5 x 6). Vous pouvez définir des multiplicateurs d’offre (avec des valeurs autres que 1,00) pour un événement [Nombre limité de cibles](#bid-multiplier-limits-by-target).

   Lorsqu’une enchère est admissible pour plusieurs modificateurs d’offre, tous les modificateurs d’offre applicables sont multipliés.

   Les modificateurs d’offre n’augmentent jamais l’offre à plus que l’offre maximale.

1. Cliquez sur **[!UICONTROL Save]**.

-->

## Chargement d’une feuille de calcul pour gérer les multiplicateurs d’offre pour un emplacement unique<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

Les modifications apportées au fichier chargé remplacent les valeurs du multiplicateur d’offre existantes.<!-- what if you delete a row? -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. a) cliquez sur **[!UICONTROL Download Template]** et modifiez les valeurs du multiplicateur d&#39;offre ou b) modifiez un modèle téléchargé précédemment. Enregistrez le fichier modifié sur votre périphérique ou réseau.

   Par défaut, le multiplicateur d’offre pour une cible est de 1,00, ce qui signifie que l’offre n’est pas ajustée pour cette cible. Les valeurs peuvent être comprises entre 0,10 et 10,00. Par exemple, un modificateur d’offre de 0,5 réduit une offre de 6 USD à 3 (0,5 x 6). Vous pouvez définir des multiplicateurs d’offre (avec des valeurs autres que 1,00) pour un événement [Nombre limité de cibles](#bid-multiplier-limits-by-target).

   Lorsqu’une enchère est admissible pour plusieurs modificateurs d’offre, tous les modificateurs d’offre applicables sont multipliés.

   Les modificateurs d’offre n’augmentent jamais l’offre à plus que l’offre maximale.

1. A) faites glisser et déposez le fichier modifié dans la zone ou b) cliquez dans la zone pour sélectionner le fichier sur votre périphérique ou réseau.

1. Cliquez sur **[!UICONTROL Upload]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Types de cible éligibles pour les multiplicateurs d’offre {#bid-multiplier-by-target}

pas ici en double

## Nombre maximal de multiplicateurs d’offre par type de cible {#bid-multiplier-limits-by-target}

pas ici en double

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
