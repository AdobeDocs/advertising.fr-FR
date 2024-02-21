---
title: Types de rapports de performances dans les vues Campaign Management
description: Découvrez les données du rapport incluses dans les vues de gestion de campagne.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: c7860d98edbf44b71d97c3800edf47a409606b74
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Types de rapports de performances dans les vues Campaign Management

Les vues de gestion de campagne incluent des données de rapport complètes. Les rapports disponibles vous aident à identifier les packages et emplacements performants et ceux qui nécessitent votre attention. Les boutons d’action rapide vous rendent également plus productif.

## Vue Toutes les campagnes

La variable [!UICONTROL Campaigns] La vue s’ouvre sur un ensemble de graphiques de données de performances et une liste de toutes les campagnes de votre compte.

### Affichage du graphique {#chart-view}

Vous pouvez [personnaliser les graphiques de tendance des séries temporelles ;](campaign-data-views-manage.md#data-visualizations-manage) pour toutes les campagnes à l’aide de trois mesures. Par défaut, les données pour [!UICONTROL Net Spend], [!UICONTROL Impressions], et [!UICONTROL Net CPM] sont inclus dans des graphiques distincts (graphiques en courbes). Vous pouvez éventuellement modifier les mesures. Pour activer les données horaires dans les graphiques de tendance de série temporelle, définissez votre sélection de date sur un seul jour ([!UICONTROL Today], [!UICONTROL Yesterday]ou un jour spécifique).

![graphiques de tendances distincts pour trois mesures](/help/dsp/assets/trend-chart-separate.png)

Vous pouvez également, si vous le souhaitez, superposer les trois mesures afin de détecter facilement les anomalies et les domaines dans lesquels améliorer l’échelle ou les performances.

![graphique des tendances avec superposition](/help/dsp/assets/trend-chart.png)

### Vue Tableau

![Liste des campagnes](/help/dsp/assets/campaigns-list.png)

Par défaut, chaque ligne de campagne comprend les mesures de fréquence et de diffusion. Les mesures de fréquence incluent [!UICONTROL Gross Spend (Lifetime)], qui inclut une jauge des dépenses réelles sur cible par rapport aux dépenses prévues sur cible pour tous les modules de la campagne, afin que vous puissiez identifier les campagnes sous-performantes d’un seul coup d’oeil. Vous pouvez [modification du mode Colonnes](campaign-data-views-manage.md#column-view-change) ou même [création d’un affichage de colonne personnalisé](campaign-data-views-manage.md#column-view-create).

Vous pouvez en savoir plus [personnaliser les tableaux de données ;](campaign-data-views-manage.md#data-tables-manage) par d’autres moyens et [filtrer les données visibles](campaign-data-views-manage.md#filter-data-tables).

Pour afficher une campagne plus en détail, cliquez sur son nom.

#### Indicateurs d’alerte

*Fonction bêta*

Un &quot;[!UICONTROL Alerts]La colonne &quot; indique lorsqu’une campagne, ou toute entité enfant sous celle-ci, présente un problème. A [!UICONTROL Pulse Panel] L’icône située à droite de la barre d’outils indique également si des alertes sont disponibles pour les entités répertoriées. Voir &quot;[Affichage des alertes](campaign-alerts.md)&quot; pour plus d’informations.

## Création de rapports de campagne unique {#single-campaign-reporting}

Au sein d’une campagne, vous pouvez filtrer les données en fonction de l’entité de campagne : [!UICONTROL Packages], [!UICONTROL Placements], et [!UICONTROL Ads]. Vous pouvez en savoir plus [filtrer les données visibles](campaign-data-views-manage.md#filter-data-tables) pour inclure uniquement les modules, emplacements ou annonces que vous souhaitez afficher.

![Onglets des entités de Campaign](/help/dsp/assets/campaign-subtabs.png)

### Affichage du graphique

Pour chaque campagne, vous pouvez : [personnaliser les graphiques de tendance des séries temporelles ;](campaign-data-views-manage.md#data-visualizations-manage) avec trois mesures, disponibles dans chaque vue d’entité. Les mêmes mesures sont conservées dans tous les graphiques de tendance de la campagne.

Voir [Section &quot;Affichage du graphique&quot; sur les mesures entre campagnes](#chart-view) pour plus d’informations.

### Vue Tableau

Dans chaque onglet d’entité, chaque ligne comprend par défaut des mesures de fréquence et de diffusion, mais vous pouvez [modification du mode Colonnes](campaign-data-views-manage.md#column-view-change) ou même [création d’un affichage de colonne personnalisé](campaign-data-views-manage.md#column-view-create) pour appliquer à tous les sous-onglets de la campagne. Vous pouvez en savoir plus [personnaliser les tableaux de données ;](campaign-data-views-manage.md#data-tables-manage) par d’autres moyens. Chaque tableau de données comprend une [!UICONTROL Subtotals] qui affiche soit la somme, soit la valeur moyenne de chaque mesure sur toutes les lignes visibles.

#### Indicateurs d’alerte

*Fonction bêta*

Un &quot;[!UICONTROL Alerts]&quot;colonne indique lorsqu’un package, un emplacement ou une publicité — ou toute entité enfant sous un package ou un emplacement — a un problème. Un &quot;[!UICONTROL Alerts]La colonne &quot; indique lorsqu’une campagne, ou toute entité enfant sous celle-ci, présente un problème. A [!UICONTROL Pulse Panel] L’icône située à droite de la barre d’outils indique également si des alertes sont disponibles pour les entités répertoriées. Voir &quot;[Affichage des alertes](campaign-alerts.md)&quot; pour plus d’informations.

### Autres types de rapports au niveau des campagnes

Pour d’autres ventilations de données, voir [les pages de rapports au niveau de la campagne ;](/help/dsp/campaign-management/campaigns/campaign-view-report.md). Le rapport comprend des sections sur [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], et [!UICONTROL Audience Performance] data.

### Autres types de rapports au niveau de l’emplacement

Pour d’autres ventilations de données, voir [les pages de rapports au niveau de l’emplacement ;](/help/dsp/campaign-management/placements/placement-view-report.md). Le rapport comprend des sections sur [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications], et [!UICONTROL Ads] data.

En outre, vous pouvez afficher les données suivantes dans les paramètres d’emplacement :

* [A (vue détaillée [!UICONTROL Inspector])](placement-details-view.md), qui affiche tous les sites, publicités, données de fréquence et offres ciblés pour un emplacement.

* A [rapport des prévisions de placement](/help/dsp/campaign-management/reports/placement-forecast.md)

* [Rapports de diagnostic de placement](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Autres types de rapports au niveau des annonces

Pour d’autres ventilations de données, voir [les pages de création de rapports au niveau des annonces ;](/help/dsp/campaign-management/ads/ad-view-report.md). Le rapport comprend : [!UICONTROL Overview], [!UICONTROL Geography], et [!UICONTROL Viewability] data.

>[!MORELIKETHIS]
>
>* [Affichage des sites, publicités et détails de fréquence d’un emplacement](placement-details-view.md)
>* [Gestion des vues de données de campagne](campaign-data-views-manage.md)
>* [Exportation de données à partir d’une vue Campaign Management](campaign-export-data.md)
>* [Affichage d’un rapport détaillé pour une campagne](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Affichage des alertes](campaign-alerts.md)
