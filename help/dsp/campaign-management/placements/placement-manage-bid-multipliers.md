---
title: Gestion des multiplicateurs d’offre pour les emplacements
description: Découvrez comment créer et modifier des multiplicateurs d’offre pour vos cibles d’emplacement.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 28f1b799daaa4e511abab1102a639e72b3a32d18
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Gestion des multiplicateurs d’offre pour les emplacements

Vous pouvez créer et gérer des multiplicateurs d’offre, par lesquels une offre calculée algorithmiquement est multipliée pour augmenter ou diminuer l’offre, pour vos cibles d’emplacement existantes de [types de cible éligibles](#bid-multiplier-by-target). Vous pouvez modifier manuellement les valeurs du multiplicateur d’offre pour un emplacement ou charger une feuille de calcul avec les valeurs d’un ou de plusieurs emplacements.

Par défaut, le multiplicateur d’offre pour une cible est de 1,00, ce qui signifie que l’offre n’est pas ajustée pour cette cible. Les valeurs peuvent être comprises entre 0,10 et 10,00. Par exemple, un multiplicateur d’offre de 0,5 réduit une offre de 6 USD à 3 (0,5 x 6). Lorsqu’une enchère est admissible pour plusieurs modificateurs d’offre, tous les multiplicateurs d’offre applicables sont multipliés. Par exemple, si la Californie a un multiplicateur d’offre de 2 et que San Francisco a un multiplicateur d’offre de 3, le multiplicateur d’offre final pour les publicités qui s’exécutent à San Francisco est de 6.

>[!NOTE]
>
>Les multiplicateurs d’offre n’augmentent jamais l’offre à plus que l’offre maximale.

Vous pouvez définir des multiplicateurs d’offre (avec des valeurs autres que 1,00) pour un [nombre limité de cibles](#bid-multiplier-limits-by-target).

Cette fonctionnalité fonctionne avec vos cibles d’emplacement existantes. Pour modifier les cibles sélectionnées pour vos emplacements, voir &quot;[Modifier les emplacements](/help/dsp/campaign-management/placements/placement-edit.md)&quot;.

## Gestion des multiplicateurs d’offre pour un emplacement unique

Vous pouvez modifier manuellement les valeurs ou charger une feuille de calcul pour un seul emplacement.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Ajustez les multiplicateurs d’offres pour les cibles éligibles :

   * Pour ajuster manuellement les valeurs du multiplicateur d’offre, déplacez-vous vers chaque [ onglet spécifique à la cible](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience] et [!UICONTROL Brand Safety]) et modifiez les valeurs existantes pour les cibles d’emplacement.

     La plupart des catégories cibles répertorient les sous-catégories sur la gauche. Cliquez sur une sous-catégorie pour gérer les multiplicateurs d’offre pour cette sous-catégorie, le cas échéant.

   * Pour charger un fichier CSV avec des valeurs de multiplicateur d’offre afin de remplacer toutes les valeurs existantes :

      1. Cliquez sur **[!UICONTROL CSV File Edit]** en haut à droite.

      1. A) cliquez sur **[!UICONTROL Download Template]** et modifiez le fichier ou b) modifiez un modèle précédemment téléchargé. Enregistrez le fichier modifié sur votre périphérique ou réseau.

         Les feuilles de calcul téléchargées comprennent une feuille pour chaque type de cible (par exemple, Pays, Sources et Catégorie de site). Seuls les multiplicateurs d’offre existants avec des valeurs &lt; 1.0 ou > 1.0 sont inclus.

         * Pour ajouter un multiplicateur d&#39;offre pour une cible existante, saisissez la cible en utilisant la même syntaxe que celle visible dans l&#39;interface utilisateur et la valeur du multiplicateur d&#39;offre correspondante.

         * Pour supprimer un modificateur d’offre, définissez la valeur du multiplicateur d’offre sur 1,0 ou supprimez toutes les informations de la ligne.

         ![Exemple de ligne dans un fichier de feuille de calcul du multiplicateur d’offre](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemple de ligne dans un fichier de feuille de calcul du multiplicateur d’offre")

      1. Cliquez sur **[!UICONTROL Next]** pour passer à la section [!UICONTROL Upload File] et a) faites glisser le fichier modifié dans la zone ou b) cliquez dans la zone pour sélectionner le fichier sur votre appareil ou votre réseau.

      1. Vérifiez les données chargées dans la section [!UICONTROL Review & Submit], puis cliquez sur **[!UICONTROL Save]**.

## Chargement de multiplicateurs d’offres pour un ou plusieurs emplacements

Téléchargez une feuille de calcul pour appliquer les mêmes valeurs à tous les emplacements sélectionnés.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez gérer les multiplicateurs d’offre.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. Transférez un fichier CSV contenant des valeurs de multiplicateur d’offre afin de remplacer toutes les valeurs existantes pour tous les emplacements sélectionnés.

   1. A) cliquez sur **[!UICONTROL Download Template]** et modifiez le fichier ou b) modifiez un modèle précédemment téléchargé. Enregistrez le fichier modifié sur votre périphérique ou réseau.

      Les feuilles de calcul téléchargées comprennent une feuille pour chaque type de cible (par exemple, Pays, Sources et Catégorie de site). Seuls les multiplicateurs d’offre existants avec des valeurs &lt; 1.0 ou > 1.0 sont inclus.

      * Pour ajouter un multiplicateur d&#39;offre pour une cible existante, saisissez la cible en utilisant la même syntaxe que celle visible dans l&#39;interface utilisateur et la valeur du multiplicateur d&#39;offre correspondante.

      * Pour supprimer un modificateur d’offre, définissez la valeur du multiplicateur d’offre sur 1,0 ou supprimez toutes les informations de la ligne.

      ![Exemple de ligne dans un fichier de feuille de calcul du multiplicateur d’offre](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemple de ligne dans un fichier de feuille de calcul du multiplicateur d’offre")

   1. Cliquez sur **[!UICONTROL Next]** pour passer à la section [!UICONTROL Upload File] et a) faites glisser le fichier modifié dans la zone ou b) cliquez dans la zone pour sélectionner le fichier sur votre appareil ou votre réseau.

   1. Vérifiez les données chargées dans la section [!UICONTROL Review & Submit], puis cliquez sur **[!UICONTROL Save]**.

## Types de cible éligibles pour les multiplicateurs d’offre {#bid-multiplier-by-target}

Vous pouvez configurer des modificateurs d’offre uniquement pour les cibles incluses, et non les cibles exclues.

* **Cibles géographiques** : géographie (pays, états et villes), codes postaux et zones desservie

* **Cibles de l’inventaire** : sources et flux pour l’inventaire public et [!UICONTROL On Demand] inventaire

* **Cibles du site :** sites/applications ciblés (mais non exclus), catégories de site

* **Cibles d’audience :** segments, tranches horaires et rubriques

* **ads.txt cibles :** (lorsque vous vous désabonnez de ads.txt, ce qui vous permet d’acheter des stocks à tous les vendeurs) ads.txt uniquement, ads.txt direct sellers et ads.txt sellers plus sites sans ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

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
>* [Modifier des emplacements](placement-edit.md)
>* [Afficher le journal des modifications d’un emplacement](placement-change-log.md)
>* [Paramètres de placement](placement-settings.md)
