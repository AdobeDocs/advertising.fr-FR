---
title: Gestion Des Vues De Données De Campaign
description: Découvrez comment personnaliser vos vues de données pour les campagnes, les packages, les emplacements et les annonces.
feature: DSP Campaign Data Views
exl-id: a22da10b-104d-4860-a23f-f2a6e59b637c
source-git-commit: 40cfd72c0f295ab1b6b7743828dded4032d435d4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Gestion Des Vues De Données De Campaign

Vous pouvez personnaliser les données qui apparaissent dans les vues de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]).

## Gérer les visualisations de données {#data-visualizations-manage}

Vous pouvez modifier les mesures et le mode graphique pour toutes les visualisations de données dans les campagnes ou pour une seule campagne. Les modifications apportées à une seule campagne sont appliquées à toutes les visualisations de données de la campagne, y compris celles des vues [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads].

### Modification des mesures d’une visualisation de données

1. Dans l’angle supérieur droit de la visualisation de données, cliquez sur ![Paramètres](/help/dsp/assets/settings-chart.png).

1. Sélectionnez les mesures.

   Vous ne pouvez pas sélectionner la même mesure deux fois.

1. Cliquez sur **[!UICONTROL Apply]**.

### Modification du mode d’affichage d’une visualisation de données

* Dans l’angle supérieur droit de la visualisation de données, cliquez sur le commutateur de [!UICONTROL Overlay] (![commutateur de recouvrement](/help/dsp/assets/overlay.png)) pour basculer entre le mode de recouvrement (tous les graphiques sont superposés ensemble) et le mode graphique en treillis (trois graphiques distincts).

## Gérer les tables de données {#data-tables-manage}

Dans toutes les vues de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]), vous pouvez personnaliser les données qui apparaissent dans le tableau de données.

### Gérer les vues de colonnes {#column-views-manage}

Chaque niveau de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]) comprend des vues [!UICONTROL Pacing] et [!UICONTROL Performance] intégrées qui incluent des mesures pertinentes pour cette entité. Par défaut, la vue [!UICONTROL Pacing] s’affiche afin que vous puissiez identifier rapidement les campagnes et composants de campagne sous-performants. Vous pouvez éventuellement créer et modifier des jeux de colonnes personnalisés.

![sélecteur du mode Colonnes](/help/dsp/assets/column-view-selector.png)

DSP enregistre votre vue la plus récente en tant que vue par défaut, de sorte que, chaque fois que vous revenez à la page, vous visualisez toujours les mesures qui vous intéressent.

#### Modifier le mode Colonnes {#column-view-change}

* Dans le sélecteur d’affichage, cliquez sur ![flèche vers le bas](/help/dsp/assets/chevron-down.png), puis sur le nom de l’affichage des colonnes souhaité.

#### Création d’un mode Colonnes personnalisé {#column-view-create}

1. Dans le sélecteur d&#39;affichage, cliquez sur ![flèche vers le bas](/help/dsp/assets/chevron-down.png), puis sur **[!UICONTROL Create View]**.

1. Spécifiez les mesures à inclure dans la vue :

   1. Dans la liste des mesures disponibles, cochez la case en regard de chaque mesure à inclure.

      Toutes les mesures sont classées par ordre alphabétique : [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (mesures standard suivies par DSP), [!UICONTROL Viewability] et [!UICONTROL Conversions]. Les mesures ajoutées avec « ([!UICONTROL Lifetime]) » renvoient des valeurs depuis le début de la campagne, quelle que soit la période sélectionnée sur la page.

   1. Modifiez l’ordre des colonnes, si nécessaire, en cliquant sur les noms des colonnes dans le panneau de droite et en les faisant glisser vers les positions requises.

   Certaines colonnes ont des positions fixes et ne peuvent pas être déplacées ni supprimées.

1. Appliquez ou enregistrez les paramètres :

   * Pour appliquer les paramètres temporairement sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply].**

   * Pour enregistrer les paramètres dans une nouvelle vue de colonne personnalisée, cliquez sur **[!UICONTROL Save As]**. Dans la fenêtre [!UICONTROL Save View], saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

#### Modification d’un mode Colonnes {#column-view-edit}

>[!NOTE]
>
>Vous ne pouvez pas enregistrer les modifications apportées à une vue de colonne standard (prédéfinie), mais vous pouvez les appliquer temporairement ou les enregistrer dans une nouvelle vue personnalisée.

1. Dans le sélecteur d’affichage, cliquez sur ![flèche vers le bas](/help/dsp/assets/chevron-down.png), puis sur le nom de l’affichage des colonnes existant.

1. Dans le sélecteur d&#39;affichage, cliquez sur ![flèche vers le bas](/help/dsp/assets/chevron-down.png), puis sur **[!UICONTROL Edit View]**.

1. Modifiez les mesures à inclure dans la vue :

   1. Dans la liste des mesures disponibles, cochez la case en regard de chaque mesure à inclure et décochez la case en regard de chaque mesure à exclure.

      Toutes les mesures sont classées par ordre alphabétique : [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (mesures standard suivies par DSP), [!UICONTROL Viewability] et [!UICONTROL Conversions]. Les mesures ajoutées avec « ([!UICONTROL Lifetime]) » renvoient des valeurs depuis le début de la campagne, quelle que soit la période sélectionnée sur la page.

   1. Modifiez l’ordre des colonnes, si nécessaire, en cliquant sur les noms des colonnes dans le panneau de droite et en les faisant glisser vers les positions requises.

   Certaines colonnes ont des positions fixes et ne peuvent pas être déplacées ni supprimées.

1. Appliquez ou enregistrez les paramètres :

   * (Vues personnalisées uniquement) Pour enregistrer les paramètres, cliquez sur **[!UICONTROL Save]**.

   * Pour appliquer les paramètres temporairement sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply].**

   * Pour enregistrer les paramètres dans une nouvelle vue de colonne personnalisée, cliquez sur **[!UICONTROL Save As]**. Dans la fenêtre [!UICONTROL Save View], saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

### Filtrer les données de la campagne {#filter-data-tables}

Les filtres modifient les données affichées sur l’onglet actif. Les filtres disponibles varient selon le type d’entité mais peuvent inclure le nom de l’entité, le statut et des colonnes de propriétés supplémentaires.

1. Dans la barre d’outils principale, cliquez sur ![bouton Filtrer](/help/dsp/assets/filter.png).
1. Pour chaque filtre à appliquer, cliquez sur le nom du filtre dans la colonne de gauche, puis spécifiez la ou les valeurs du filtre.
1. Cliquez sur **[!UICONTROL Apply]**.

#### Filtres disponibles

Les filtres suivants sont disponibles pour vos vues [!UICONTROL Campaigns], [!UICONTROL Packages] et [!UICONTROL Placements] :

* Filtres d’affichage [!UICONTROL Campaigns] :
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* Filtres d’affichage [!UICONTROL Packages] :
   * [!UICONTROL Custom flights] (qu&#39;ils existent ou non)
   * [!UICONTROL Custom goal] (le cas échéant)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* Filtres d’affichage [!UICONTROL Placements] :
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (le cas échéant)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than] ou [!UICONTROL equal to] une valeur spécifiée)
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
* Filtres d’affichage [!UICONTROL Ads] :
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]

### Modifier la plage de dates

Modifiez la période utilisée dans toutes les vues standard et personnalisées à l’aide du sélecteur de période situé au-dessus de tout tableau de données.

![Sélecteur de période](/help/dsp/assets/date-range-selector.png "Sélecteur de période")

* Pour une plage prédéfinie : sélectionnez-en une dans la liste des incréments temporels courants. La valeur par défaut est [!UICONTROL Last 30 days]*.

* Pour une plage spécifique, effectuez l’une des opérations suivantes :

   * Cliquez sur ![Calendrier](/help/dsp/assets/calendar.png "Calendrier"), puis sur la date de début et la date de fin dans le calendrier.

   * Cliquez dans la période, puis entrez une date de début et une date de fin, ou sélectionnez-les dans le calendrier.

     Vous pouvez saisir des valeurs numériques (du JJ-MM-AAAA au JJ-MM-AAAA) et/ou des noms ou abréviations de mois (tels que Jan ou Janvier).

### Trier une colonne de données

Vous pouvez trier n’importe quelle colonne de données par ordre croissant (A à Z, ou 1 à 10) ou décroissant (Z à A, ou 10 à 1).

* Cliquez sur l’en-tête de colonne pour basculer entre l’ordre croissant et l’ordre décroissant.


### Spécifier le nombre de lignes de données

En bas à droite d’une page, à côté de **[!UICONTROL Items per page]** , sélectionnez *[!UICONTROL 25]*, *[!UICONTROL 50]* ou *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues de gestion de campagnes](campaign-reports-about.md)
>* [Affichage des détails sur les sites, les publicités et la fréquence pour un emplacement](placement-details-view.md)
>* [Afficher l&#39;état de prévision d&#39;emplacement](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Afficher les rapports de diagnostic d&#39;emplacement](placement-diagnostics.md)
>* [Exporter des données à partir d’une vue de gestion de campagne](campaign-export-data.md)
>* [Vidéo : structure du compte DSP et interface utilisateur](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html?lang=fr)
