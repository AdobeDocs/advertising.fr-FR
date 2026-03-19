---
title: Types de rapports de performances dans les vues de gestion de campagnes
description: Découvrez les données de rapport incluses dans les vues de gestion de campagne.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 7f9b118ffe0b8e972296f79b19f6dcd2a9dedabe
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Types de rapports de performances dans les vues de gestion de campagnes

Les vues de gestion de campagne incluent des données de rapport complètes. Les rapports disponibles vous aident à identifier les packages et les emplacements qui fonctionnent bien et ceux qui nécessitent votre attention. Les boutons d’action rapide vous rendent également plus productif.

## Vue Toutes les campagnes

La vue [!UICONTROL Campaigns] s’ouvre à un ensemble de graphiques de données de performances et à une liste de toutes les campagnes de votre compte.

### Mode Graphique {#chart-view}

Vous pouvez [personnaliser des graphiques de tendance de série temporelle](campaign-data-views-manage.md#data-visualizations-manage) sur toutes les campagnes à l’aide de trois mesures. Par défaut, les données relatives à [!UICONTROL Net Spend], [!UICONTROL Impressions] et [!UICONTROL Net CPM] sont incluses dans des graphiques distincts (graphiques en treillis). Vous avez la possibilité de modifier les mesures. Pour activer les données horaires dans les graphiques de tendance de série temporelle, modifiez votre sélection de date en un seul jour ([!UICONTROL Today], [!UICONTROL Yesterday] ou un jour spécifique).

![des graphiques de tendance distincts pour trois mesures](/help/dsp/assets/trend-chart-separate.png)

Vous pouvez également superposer les trois mesures pour faciliter la détection des anomalies et des zones dans lesquelles améliorer l’échelle ou les performances.

![graphique de tendances avec recouvrement](/help/dsp/assets/trend-chart.png)

### Vue Tableau

![Liste des campagnes](/help/dsp/assets/campaigns-list.png)

Par défaut, chaque ligne de campagne comprend des mesures de fréquence et de diffusion. Les mesures de fréquence comprennent les [!UICONTROL Gross Spend (Lifetime)], qui incluent une jauge des dépenses réelles et prévues dans tous les packages de la campagne, afin que vous puissiez identifier rapidement les campagnes sous-performantes. Vous pouvez éventuellement [modifier la vue des colonnes](campaign-data-views-manage.md#column-view-change) ou même [créer une vue des colonnes personnalisée](campaign-data-views-manage.md#column-view-create).

Vous pouvez [personnaliser les tableaux de données](campaign-data-views-manage.md#data-tables-manage) de différentes manières et [filtrer les données visibles](campaign-data-views-manage.md#filter-data-tables).

Pour afficher une campagne plus en détail, cliquez sur son nom.

#### Indicateurs d’alerte

Une colonne « [!UICONTROL Alerts] » indique lorsqu’une campagne ou toute entité enfant située en dessous rencontre un problème. Une icône [!UICONTROL Pulse Panel] à droite de la barre d’outils indique également si des alertes sont disponibles pour les entités répertoriées. Voir « [&#x200B; Afficher les alertes &#x200B;](campaign-alerts.md) pour plus d’informations.

## Création de rapports de campagne unique {#single-campaign-reporting}

Dans une campagne, vous pouvez filtrer les données en fonction de l’entité de la campagne : [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]. Vous pouvez en outre [filtrer les données visibles](campaign-data-views-manage.md#filter-data-tables) pour inclure uniquement les packages, les emplacements ou les annonces que vous souhaitez voir.

![Onglets des entités de Campaign](/help/dsp/assets/campaign-subtabs.png)

### Mode Graphique

Pour chaque campagne, vous pouvez [personnaliser des graphiques de tendances de série temporelle](campaign-data-views-manage.md#data-visualizations-manage) avec trois mesures disponibles dans chaque vue d’entité. Les mêmes mesures sont conservées dans tous les graphiques de tendance de la campagne.

Pour plus d’informations[&#x200B; consultez la section &#x200B;](#chart-view) « Vue du graphique » sur les mesures inter-campagnes.

### Vue Tableau

Dans chaque onglet d’entité, chaque ligne comprend les mesures de fréquence et de diffusion, par défaut, mais vous pouvez [modifier la vue des colonnes](campaign-data-views-manage.md#column-view-change) ou même [créer une vue des colonnes personnalisée](campaign-data-views-manage.md#column-view-create) à appliquer dans tous les sous-onglets de la campagne. Vous pouvez [personnaliser les tableaux de données](campaign-data-views-manage.md#data-tables-manage) de différentes manières. Chaque tableau de données comprend une ligne [!UICONTROL Subtotals], qui affiche la somme ou la valeur moyenne de chaque mesure sur toutes les lignes visibles.

#### Indicateurs d’alerte

Une colonne « [!UICONTROL Alerts] » indique lorsqu’un package, un emplacement ou une annonce publicitaire (ou toute entité enfant sous un package ou un emplacement) rencontre un problème. Une colonne « [!UICONTROL Alerts] » indique lorsqu’une campagne ou toute entité enfant située en dessous rencontre un problème. Une icône [!UICONTROL Pulse Panel] à droite de la barre d’outils indique également si des alertes sont disponibles pour les entités répertoriées. Voir « [&#x200B; Afficher les alertes &#x200B;](campaign-alerts.md) pour plus d’informations.

### Autres types de rapports au niveau des campagnes

Pour d’autres répartitions de données, consultez [les pages de rapports au niveau de la campagne](/help/dsp/campaign-management/campaigns/campaign-view-report.md). Le rapport comprend des sections sur les données [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] et [!UICONTROL Audience Performance].

### Autres types de rapports au niveau des emplacements

Pour d’autres répartitions de données, consultez [les pages de rapports au niveau de l’emplacement](/help/dsp/campaign-management/placements/placement-view-report.md). Le rapport comprend des sections sur les données [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications] et [!UICONTROL Ads].

En outre, vous pouvez afficher les données suivantes dans les paramètres d’emplacement :

* [A (vue détaillée [!UICONTROL Inspector])](placement-details-view.md), qui affiche tous les sites, publicités, données de fréquence et offres ciblés pour un emplacement.

* Un [rapport de prévision d’emplacement](/help/dsp/campaign-management/reports/placement-forecast.md).

* [Rapports de diagnostic d’emplacement](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Autres types de rapports au niveau des annonces

Pour d’autres répartitions de données, consultez [les pages de rapports au niveau des annonces](/help/dsp/campaign-management/ads/ad-view-report.md). Le rapport comprend des données [!UICONTROL Overview], [!UICONTROL Geography] et [!UICONTROL Viewability].

>[!MORELIKETHIS]
>
>* [Afficher les sites, les publicités et les détails de fréquence pour un emplacement](placement-details-view.md)
>* [Gérer les vues de données de votre campagne](campaign-data-views-manage.md)
>* [Exporter des données à partir d&#39;une vue de gestion de campagne](campaign-export-data.md)
>* [Afficher un rapport détaillé pour une campagne](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Afficher les alertes](campaign-alerts.md)
