---
title: Gestion des multiplicateurs d’offre pour les emplacements
description: Découvrez comment créer et modifier des multiplicateurs d’offre pour des cibles d’emplacement spécifiées.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 3%

---

# Gestion des multiplicateurs d’offre pour les emplacements

Cette fonctionnalité vous permet de modifier les multiplicateurs d’offre pour vos cibles d’emplacement existantes. Vous pouvez gérer les multiplicateurs d’offre pour un emplacement à la fois.<!-- remove that line once we can edit multiple -->

Pour modifier les cibles sélectionnées pour vos emplacements, voir &quot;[Modifier les emplacements](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Déplacer vers chaque [onglet spécifique à la cible](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], et [!UICONTROL Brand Safety]) et modifiez les valeurs existantes pour les cibles de placement. La plupart des catégories cibles répertorient les sous-catégories sur la gauche. Cliquez sur une sous-catégorie pour gérer les multiplicateurs d’offre pour cette sous-catégorie, le cas échéant.

   Par défaut, le multiplicateur d’offre pour une cible est de 1,00, ce qui signifie que l’offre n’est pas ajustée pour cette cible. Les valeurs peuvent être comprises entre 0,10 et 10,00. Par exemple, un modificateur d’offre de 0,5 réduit une offre de 6 USD à 3 (0,5 x 6). Les modificateurs d’offre n’augmentent jamais l’offre à plus que l’offre maximale.

   Lorsqu’une enchère est admissible pour plusieurs modificateurs d’offre, tous les modificateurs d’offre applicables sont multipliés.

   Vous pouvez définir des multiplicateurs d’offre (avec des valeurs autres que 1,00) pour un événement [Nombre limité de cibles](#bid-multiplier-limits-by-target).

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

## Types de cible éligibles pour les multiplicateurs d’offre {#bid-multiplier-by-target}

Vous pouvez configurer des modificateurs d’offre uniquement pour les cibles incluses, et non les cibles exclues.

* **Cibles géographiques**: géographie (pays, états et villes), codes postaux et zones desservie

* **Cibles du stock**: sources et flux pour l’inventaire public et [!UICONTROL On Demand] stock

* **Cibles du site :** sites/applications ciblés (mais non exclus), catégories de sites

* **Cibles d’audience :** segments, tranches horaires et rubriques

* **ads.txt cibles :** (Lorsque vous vous désabonnez de ads.txt, ce qui vous permet d’acheter des stocks à tous les vendeurs) ads.txt uniquement, ads.txt direct sellers, ads.txt sellers plus sites sans ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Nombre maximal de multiplicateurs d’offre par type de cible {#bid-multiplier-limits-by-target}

Vous pouvez définir des multiplicateurs d’offre (avec des valeurs autres que 1,00) pour un nombre limité de cibles. Vous pouvez, par exemple, définir des multiplicateurs d’offre pour 20 cibles de pays au maximum. Le nombre maximal de cibles pour chaque type de cible pouvant avoir des multiplicateurs d’offre est répertorié ci-dessous.

| Catégorie | Paramètre | Nombre maximal |
| -------- | --------- | ----- |
| Géo | Pays | 20 |
| Géo | État | 100 |
| Géo | Ville | 100 |
| Géo | Métro | 100 |
| Géo | Codes postaux | 100 |
| Inventaire | Sources | 100 |
| Inventaire | Flux | 100 |
| Sites | Catégorie de site | 100 |
| Sites | Sites/applications | 100 |
| Audience | Segments | 500 |
| Audience | Sujets | 100 |
| Sécurité des marques | Ads.txt | N/A |

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Modifier les emplacements](placement-edit.md)
>* [Affichage du journal des modifications d’un emplacement](placement-change-log.md)
>* [Paramètres d’emplacement](placement-settings.md)
