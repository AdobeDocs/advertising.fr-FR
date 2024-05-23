---
title: Gestion des multiplicateurs d’offre pour les emplacements
description: Découvrez xxx
feature: DSP Placements
source-git-commit: b6758541b59f1fd924a2fe83c769f5ba385409aa
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# XXX

## Gestion des multiplicateurs d’offre pour un emplacement unique

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Ajustez les multiplicateurs d’offres pour les cibles éligibles :

   * Pour ajuster manuellement les valeurs du multiplicateur d’offre, déplacez-vous vers chaque [onglet spécifique à la cible](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], et [!UICONTROL Brand Safety]) et modifiez les valeurs existantes pour les cibles de placement.

     La plupart des catégories cibles répertorient les sous-catégories sur la gauche. Cliquez sur une sous-catégorie pour gérer les multiplicateurs d’offre pour cette sous-catégorie, le cas échéant.

   * Pour charger un fichier CSV avec des valeurs de multiplicateur d’offre afin de remplacer toutes les valeurs existantes :

      1. Cliquez sur **[!UICONTROL CSV File Edit]** en haut à droite.

      1. a) cliquez sur **[!UICONTROL Download Template]** et modifiez le fichier ou b) modifiez un modèle précédemment téléchargé. Enregistrez le fichier modifié sur votre périphérique ou réseau.

         Les modèles téléchargés incluent une feuille pour chaque type de cible (par exemple, Pays, Sources et Catégorie de site). Seuls les multiplicateurs d’offre existants avec des valeurs autres que 1.0 sont inclus.

         * Pour ajouter un multiplicateur d&#39;offre pour une cible existante, saisissez la cible en utilisant la même syntaxe que celle visible dans l&#39;interface utilisateur et la valeur du multiplicateur d&#39;offre correspondante.

         * Pour supprimer un modificateur d’offre, définissez la valeur du multiplicateur d’offre sur 1,0 ou supprimez toutes les informations de la ligne.

         ![Exemple de ligne dans un fichier de feuille de calcul de multiplicateur d’offre](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemple de ligne dans un fichier de feuille de calcul de multiplicateur d’offre")

      1. Cliquez sur **[!UICONTROL Next]** pour accéder au [!UICONTROL Upload File] et a) faites glisser et déposez le fichier modifié dans la zone ou b) cliquez dans la zone pour sélectionner le fichier à partir de votre appareil ou de votre réseau.

      1. Vérifiez les données chargées dans le [!UICONTROL Review & Submit] , puis cliquez sur **[!UICONTROL Save]**.

## Gestion des multiplicateurs d’offre pour un ou plusieurs emplacements

<!-- verify all and edit accordingly -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez gérer les multiplicateurs d’offre.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

<!-- Check the following this functionality when available in UAT -->

1. Ajustez les multiplicateurs d’offres pour les cibles éligibles :

   * Pour ajuster manuellement les valeurs du multiplicateur d&#39;offre, déplacez-vous vers chaque onglet spécifique à la cible ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], et[!UICONTROL Brand Safety]) et modifiez les valeurs existantes pour les cibles de placement.

   Les mêmes modifications s’appliquent à tous les emplacements sélectionnés.

* Pour charger un fichier CSV avec des valeurs de multiplicateur d’offre afin de remplacer toutes les valeurs existantes :

   1. Cliquez sur **[!UICONTROL CSV File Edit]** en haut à droite.

   1. a) cliquez sur **[!UICONTROL Download Template]** et modifiez le fichier ou b) modifiez un modèle précédemment téléchargé. Enregistrez le fichier modifié sur votre périphérique ou réseau.

      Les modèles téléchargés incluent une feuille pour chaque type de cible (par exemple, Pays, Sources et Catégorie de site). Seuls les multiplicateurs d’offre existants avec des valeurs autres que 1.0 sont inclus.

      * Pour ajouter un multiplicateur d&#39;offre pour une cible existante, saisissez la cible en utilisant la même syntaxe que celle visible dans l&#39;interface utilisateur et la valeur du multiplicateur d&#39;offre correspondante.

      * Pour supprimer un modificateur d’offre, définissez la valeur du multiplicateur d’offre sur 1,0 ou supprimez toutes les informations de la ligne.

      ![Exemple de ligne dans un fichier de feuille de calcul de multiplicateur d’offre](/help/dsp/assets/bid-multiplier-spreadsheet.png "Exemple de ligne dans un fichier de feuille de calcul de multiplicateur d’offre")

   1. Cliquez sur **[!UICONTROL CSV Edit]** en haut à droite.

   1. a) cliquez sur **[!UICONTROL Download Template]** et modifiez les valeurs du multiplicateur d&#39;offre ou b) modifiez un modèle téléchargé précédemment. Enregistrez le fichier modifié sur votre périphérique ou réseau.

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
