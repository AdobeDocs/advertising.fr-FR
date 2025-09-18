---
title: Gérer les multiplicateurs d’offres pour les placements
description: Découvrez comment créer et modifier des multiplicateurs d’enchères pour vos cibles de placement.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Gérer les multiplicateurs d’offres pour les placements

Vous pouvez créer et gérer des multiplicateurs d&#39;enchères, par lesquels une enchère calculée par algorithme est multipliée pour augmenter ou diminuer l&#39;enchère, pour vos cibles d&#39;emplacement existantes de [types de cible éligibles](#bid-multiplier-by-target). Vous pouvez modifier manuellement les valeurs du multiplicateur d’enchères pour un emplacement ou charger une feuille de calcul avec des valeurs pour un ou plusieurs emplacements.

Par défaut, le multiplicateur d’enchères pour une cible est de 1,00, ce qui signifie que l’enchère n’est pas ajustée pour cette cible. Les valeurs peuvent être comprises entre 0,10 et 10,00. Par exemple, un multiplicateur d’enchères de 0,5 réduit une enchère de 6 USD à 3 USD (0,5 x 6). Lorsqu&#39;une mise aux enchères est admissible pour plusieurs conditions commerciales d&#39;offre, tous les multiplicateurs d&#39;offre applicables sont multipliés. Par exemple, si la Californie a un multiplicateur d’enchères de 2 et que San Francisco a un multiplicateur d’enchères de 3, le multiplicateur d’enchères final pour les publicités diffusées à San Francisco est de 6.

>[!NOTE]
>
>Les multiplicateurs d&#39;enchères n&#39;augmentent jamais l&#39;enchère au-delà de l&#39;enchère maximum.

Vous pouvez définir des multiplicateurs d&#39;enchères (avec des valeurs autres que 1,00) pour un [nombre limité de cibles](#bid-multiplier-limits-by-target).

Cette fonctionnalité fonctionne avec vos cibles d’emplacement existantes. Pour modifier les cibles sélectionnées pour vos emplacements, voir « [ Modifier les emplacements ](/help/dsp/campaign-management/placements/placement-edit.md). »

## Gérer les multiplicateurs d’offres pour un emplacement unique

Vous pouvez modifier manuellement les valeurs ou charger une feuille de calcul pour un emplacement unique.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]** > **[!UICONTROL Bid Multiplier]**.

1. Ajustez les multiplicateurs d&#39;enchères pour les cibles éligibles :

   * Pour ajuster manuellement les valeurs du multiplicateur d&#39;enchères, déplacez-vous vers chaque [onglet spécifique à la cible](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience] et [!UICONTROL Brand Safety]) et modifiez les valeurs existantes pour les cibles d&#39;emplacement.

     La plupart des catégories cibles répertorient les sous-catégories sur la gauche. Cliquez sur une sous-catégorie pour gérer les multiplicateurs d&#39;enchères de cette sous-catégorie, le cas échéant.

   * Pour charger un fichier CSV avec des valeurs de multiplicateur d’enchères afin de remplacer toutes les valeurs existantes :

      1. Cliquez sur **[!UICONTROL CSV File Edit]** en haut à droite.

      1. Soit a) cliquez sur **[!UICONTROL Download Template]** et modifiez le fichier, soit b) modifiez un modèle téléchargé précédemment. Enregistrez le fichier modifié sur votre appareil ou réseau.

         Les feuilles de calcul téléchargées comprennent une feuille pour chaque type de cible (par exemple, pays, sources et catégorie de site). Seuls les multiplicateurs d&#39;enchères existants dont les valeurs sont &lt; 1,0 ou > 1,0 sont inclus.

         * Pour ajouter un multiplicateur d&#39;enchères pour une cible existante, saisissez la cible en utilisant la même syntaxe que celle visible dans l&#39;interface utilisateur et la valeur du multiplicateur d&#39;enchères correspondant.

         * Pour supprimer un modificateur d&#39;offre, définissez la valeur du multiplicateur d&#39;offre sur 1,0 ou supprimez toutes les informations de la ligne.

         ![Exemple de ligne dans un fichier de feuille de calcul du multiplicateur d&#39;enchères](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemple de ligne dans un fichier de feuille de calcul du multiplicateur d&#39;enchères")

      1. Cliquez sur **[!UICONTROL Next]** pour accéder à la section [!UICONTROL Upload File] et a) faites glisser et déposez le fichier modifié dans la zone ou b) cliquez à l’intérieur de la zone pour sélectionner le fichier sur votre appareil ou réseau.

      1. Vérifiez les données chargées dans la section [!UICONTROL Review & Submit], puis cliquez sur **[!UICONTROL Save]**.

## Charger les multiplicateurs d’offres pour un ou plusieurs emplacements

Chargez une feuille de calcul pour appliquer les mêmes valeurs à tous les emplacements sélectionnés.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez gérer les multiplicateurs d’enchères.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. Chargez un fichier CSV avec des valeurs de multiplicateur d’enchères pour remplacer toutes les valeurs existantes pour tous les emplacements sélectionnés.

   1. Soit a) cliquez sur **[!UICONTROL Download Template]** et modifiez le fichier, soit b) modifiez un modèle téléchargé précédemment. Enregistrez le fichier modifié sur votre appareil ou réseau.

      Les feuilles de calcul téléchargées comprennent une feuille pour chaque type de cible (par exemple, pays, sources et catégorie de site). Seuls les multiplicateurs d&#39;enchères existants dont les valeurs sont &lt; 1,0 ou > 1,0 sont inclus.

      * Pour ajouter un multiplicateur d&#39;enchères pour une cible existante, saisissez la cible en utilisant la même syntaxe que celle visible dans l&#39;interface utilisateur et la valeur du multiplicateur d&#39;enchères correspondant.

      * Pour supprimer un modificateur d&#39;offre, définissez la valeur du multiplicateur d&#39;offre sur 1,0 ou supprimez toutes les informations de la ligne.

      ![Exemple de ligne dans un fichier de feuille de calcul du multiplicateur d&#39;enchères](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemple de ligne dans un fichier de feuille de calcul du multiplicateur d&#39;enchères")

   1. Cliquez sur **[!UICONTROL Next]** pour accéder à la section [!UICONTROL Upload File] et a) faites glisser et déposez le fichier modifié dans la zone ou b) cliquez à l’intérieur de la zone pour sélectionner le fichier sur votre appareil ou réseau.

   1. Vérifiez les données chargées dans la section [!UICONTROL Review & Submit], puis cliquez sur **[!UICONTROL Save]**.

## Types de cible éligibles aux multiplicateurs d&#39;offres {#bid-multiplier-by-target}

Vous pouvez configurer des modificateurs d&#39;enchères uniquement pour les cibles incluses et non pour les cibles exclues.

* **Cibles géographiques** : géographie (pays, états et villes), codes postaux et DMA.

* **Cibles d&#39;inventaire** : sources et sources pour l&#39;inventaire public et l&#39;inventaire [!UICONTROL On Demand]

* **Cibles du site :** sites/applications ciblés (mais non exclus), catégories de sites

* **Cibles d’audience :** de segments, de tranches horaires et de rubriques

* **publicités.txt cibles :** (lorsque vous vous désinscrivez de ads.txt, qui vous permet d’acheter des stocks auprès de tous les vendeurs) vendeurs ads.txt uniquement, vendeurs directs ads.txt et vendeurs ads.txt plus sites sans ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Nombre maximal de multiplicateurs d&#39;offres par type cible {#bid-multiplier-limits-by-target}

Vous pouvez définir des multiplicateurs d&#39;enchères (avec des valeurs autres que 1,00) pour un nombre limité de cibles. Par exemple, vous pouvez définir des multiplicateurs d’enchères pour un maximum de 20 cibles de pays. Le nombre maximal de cibles pour chaque type de cible pouvant avoir des multiplicateurs d&#39;enchères est indiqué ci-dessous.

| Catégorie | Paramètre | Nombre maximum |
| -------- | --------- | ----- |
| Géo | Pays | 20 |
| Géo | État | 100 |
| Géo | Ville | 100 |
| Géo | Métro | 100 |
| Géo | Codes postaux | 100 |
| Inventaire | Sources | 100 |
| Inventaire | Flux | 100 |
| Sites | Catégorie de site | 100 |
| Sites | Sites/Applications | 100 |
| Audience | Segments | 500 |
| Audience | Sujets | 100 |
| Sécurité de marque | Ads.txt | S.O. |

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Modifier les emplacements](placement-edit.md)
>* [Afficher le journal des modifications pour un emplacement](placement-change-log.md)
>* [Paramètres d’emplacement](placement-settings.md)
