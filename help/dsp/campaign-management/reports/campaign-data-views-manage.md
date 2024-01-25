---
title: Gestion des vues de données de campagne
description: Découvrez comment personnaliser les vues de données pour les campagnes, les packages, les emplacements et les publicités.
feature: DSP Campaign Data Views
source-git-commit: 14da2c26a6a6c3820f691cd752c22c982278314d
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# Gestion des vues de données de campagne

## Gestion des visualisations des données

Vous pouvez modifier les mesures et le mode graphique pour toutes les visualisations de données sur les campagnes ou pour une seule campagne. Les modifications apportées à une seule campagne sont appliquées à toutes les visualisations de données de la campagne, y compris la variable [!UICONTROL Packages], [!UICONTROL Placements], et [!UICONTROL Ads] onglets.

### Modification des mesures d’une visualisation de données

1. Dans le coin supérieur droit de la visualisation de données, cliquez sur ![Paramètres](/help/dsp/assets/settings-chart.png).
1. Sélectionnez les mesures.
Vous ne pouvez pas sélectionner deux fois la même mesure.
1. Cliquez sur **[!UICONTROL Apply]**.

### Modification du mode d’affichage d’une visualisation de données

* Dans le coin supérieur droit de la visualisation des données, cliquez sur le bouton [!UICONTROL Overlay] switch (![Interrupteur de recouvrement](/help/dsp/assets/overlay.png)) pour passer du mode superposition (tous les graphiques superposés ensemble) au mode graphique en courbes (trois graphiques distincts).

## Gestion des tableaux de données

Dans toutes les vues de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], et [!UICONTROL Ads]), vous pouvez personnaliser les données qui apparaissent dans le tableau de données.

### Modification du mode Colonnes

* Dans le sélecteur d’affichage, cliquez sur ![Flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur le nom du mode Colonne souhaité.

### Création d’un mode Colonnes personnalisé

1. Dans le sélecteur d’affichage, cliquez sur ![Flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur **[!UICONTROL Create View]**.

1. Spécifiez les mesures à inclure dans la vue :

   1. Dans la liste des mesures disponibles, cochez la case en regard de chaque mesure à inclure.

   1. Modifiez l’ordre des colonnes, le cas échéant, en cliquant sur les noms de colonne dans le panneau de droite et en les faisant glisser aux emplacements requis.

   Certaines colonnes ont des positions fixes et ne peuvent pas être déplacées ni supprimées.

1. Appliquez ou enregistrez les paramètres :

   * Pour appliquer temporairement les paramètres sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply].**

   * Pour enregistrer les paramètres dans un nouveau mode de colonne personnalisé, cliquez sur **[!UICONTROL Save As]**. Dans le [!UICONTROL Save View] , saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

### Modifier un mode Colonnes personnalisé

>[!NOTE]
>
>Vous ne pouvez pas modifier un mode Colonne standard (prédéfini).

1. Dans le sélecteur d’affichage, cliquez sur ![Flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur le nom du mode Colonne existant.

1. Dans le sélecteur d’affichage, cliquez sur ![Flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur **[!UICONTROL Edit View]**.

1. Modifiez les mesures à inclure dans la vue :

   1. Dans la liste des mesures disponibles, cochez la case en regard de chaque mesure à inclure et décochez la case en regard de chaque mesure à exclure.

   1. Modifiez l’ordre des colonnes, le cas échéant, en cliquant sur les noms de colonne dans le panneau de droite et en les faisant glisser aux emplacements requis.

   Certaines colonnes ont des positions fixes et ne peuvent pas être déplacées ni supprimées.

1. Appliquez ou enregistrez les paramètres :

   * Pour appliquer temporairement les paramètres sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply].**

   * Pour enregistrer les paramètres dans un nouveau mode de colonne personnalisé, cliquez sur **[!UICONTROL Save As]**. Dans le [!UICONTROL Save View] , saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

### Filtrage des données de campagne

1. Dans la barre d’outils principale, cliquez sur ![Bouton Filtrer](/help/dsp/assets/filter.png).
1. Pour chaque filtre à appliquer, cliquez sur le nom du filtre dans la colonne de gauche, puis indiquez la ou les valeurs du filtre.
1. Cliquez sur **[!UICONTROL Apply]**.

#### Filtres disponibles

Les filtres suivants sont disponibles pour votre [!UICONTROL Campaigns], [!UICONTROL Packages], et [!UICONTROL Placements] views :

* [!UICONTROL Campaigns] afficher les filtres :
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] afficher les filtres :
   * [!UICONTROL Custom flights] (qu&#39;elles existent ou non)
   * [!UICONTROL Custom goal] (le cas échéant)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] afficher les filtres :
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (le cas échéant)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than], ou [!UICONTROL equal to] une valeur spécifiée)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] ou [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] afficher les filtres :
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### Tri d’une colonne de données

Vous pouvez trier n’importe quelle colonne de données par ordre croissant (de A à Z ou de 1 à 10) ou par ordre décroissant (de Z à A ou de 10 à 1).

* Cliquez sur l’en-tête de colonne pour basculer entre l’ordre croissant et l’ordre décroissant.

<!-- add more links-->

>[!MORELIKETHIS]
>
>* [À propos des rapports In-Platform](campaign-reports-about.md)
>* [Gestion des visualisations des données](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [Modification du mode Colonnes](column-view-change.md)
>* [Création d’un mode Colonnes personnalisé](column-view-create.md)
>* [Modifier un mode Colonnes personnalisé](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [Filtrage des données de campagne](campaign-data-filter.md)
>* [Tri d’une colonne de données](campaign-data-sort.md)
>* [Affichage des sites, publicités et détails de fréquence d’un emplacement](placement-details-view.md)
>* [Afficher le rapport Prévision de positionnement](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Affichage des rapports de diagnostic d’emplacement](placement-diagnostics.md)
>* [Exportation de données à partir d’une vue Campaign Management](campaign-export-data.md)
>* [Vidéo : DSP structure de compte et interface utilisateur](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
