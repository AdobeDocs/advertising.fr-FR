---
title: Types de rapports de performances dans les vues Campaign Management
description: Découvrez les données du rapport incluses dans les vues de gestion de campagne.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
source-git-commit: 4e82caa995286635b4a181f186d6a1fabb09847d
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Types de rapports de performances dans les vues Campaign Management

Les vues de gestion de campagne incluent des données de rapport complètes. Les rapports disponibles vous aident à identifier les packages et emplacements performants et ceux qui nécessitent votre attention. Les boutons d’action rapide vous rendent également plus productif.

## Vue Toutes les campagnes

La vue [!UICONTROL Campaigns] s’ouvre sur un ensemble de graphiques de données de performances et une liste de toutes les campagnes de votre compte.

### Affichage du graphique {#chart-view}

Vous pouvez [personnaliser les graphiques de tendance de séries temporelles](campaign-data-views-manage.md#data-visualizations-manage) dans toutes les campagnes à l’aide de trois mesures. Par défaut, les données de [!UICONTROL Net Spend], [!UICONTROL Impressions] et [!UICONTROL Net CPM] sont incluses dans des graphiques distincts (graphiques à courbes). Vous pouvez éventuellement modifier les mesures. Pour activer les données horaires dans les graphiques de tendance de série temporelle, modifiez votre sélection de date en un seul jour ([!UICONTROL Today], [!UICONTROL Yesterday] ou un jour spécifique).

![Graphiques de tendance distincts pour trois mesures](/help/dsp/assets/trend-chart-separate.png)

Vous pouvez également, si vous le souhaitez, superposer les trois mesures afin de détecter facilement les anomalies et les domaines dans lesquels améliorer l’échelle ou les performances.

![diagramme de tendance avec superposition](/help/dsp/assets/trend-chart.png)

### Vue Tableau

![Liste des campagnes](/help/dsp/assets/campaigns-list.png)

Par défaut, chaque ligne de campagne comprend les mesures de fréquence et de diffusion. Les mesures de rythme incluent [!UICONTROL Gross Spend (Lifetime)], qui inclut une évaluation des dépenses réelles sur la cible par rapport aux dépenses prévues sur la cible pour tous les modules de la campagne, afin que vous puissiez identifier les campagnes sous-performantes d’un seul coup d’oeil. Vous pouvez éventuellement [modifier le mode Colonne](campaign-data-views-manage.md#column-view-change) ou même [créer un mode Colonne personnalisé](campaign-data-views-manage.md#column-view-create).

Vous pouvez [personnaliser davantage les tables de données](campaign-data-views-manage.md#data-tables-manage) et [filtrer les données visibles](campaign-data-views-manage.md#filter-data-tables).

Pour afficher une campagne plus en détail, cliquez sur son nom.

#### Indicateurs d’alerte

*Fonctionnalité Beta*

Une colonne &quot;[!UICONTROL Alerts]&quot; indique lorsqu’une campagne, ou toute entité enfant sous celle-ci, présente un problème. Une icône [!UICONTROL Pulse Panel] située à droite de la barre d’outils indique également si des alertes sont disponibles pour les entités répertoriées. Pour plus d’informations, voir &quot;[Affichage des alertes](campaign-alerts.md)&quot;.

## Création de rapports de campagne unique {#single-campaign-reporting}

Dans une campagne, vous pouvez filtrer les données en fonction de l’entité de campagne : [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]. Vous pouvez également [filtrer les données visibles](campaign-data-views-manage.md#filter-data-tables) pour inclure uniquement les modules, emplacements ou annonces que vous souhaitez voir.

![Onglets d’entité Campaign](/help/dsp/assets/campaign-subtabs.png)

### Affichage du graphique

Pour chaque campagne, vous pouvez [ personnaliser les graphiques de tendance de série temporelle ](campaign-data-views-manage.md#data-visualizations-manage) avec trois mesures, disponibles dans chaque vue d’entité. Les mêmes mesures sont conservées dans tous les graphiques de tendance de la campagne.

Pour plus d’informations, reportez-vous à la section [ &quot;Affichage du graphique&quot; sur les mesures entre campagnes ](#chart-view).

### Vue Tableau

Dans chaque onglet d’entité, chaque ligne comprend des mesures de fréquence et de diffusion, par défaut, mais vous pouvez [modifier le mode Colonne](campaign-data-views-manage.md#column-view-change) ou même [créer un mode Colonne personnalisé](campaign-data-views-manage.md#column-view-create) à appliquer à tous les sous-onglets de la campagne. Vous pouvez [personnaliser davantage les tables de données](campaign-data-views-manage.md#data-tables-manage) de différentes manières. Chaque tableau de données comprend une ligne [!UICONTROL Subtotals], qui indique soit la somme, soit la valeur moyenne de chaque mesure sur toutes les lignes visibles.

#### Indicateurs d’alerte

*Fonctionnalité Beta*

Une colonne &quot;[!UICONTROL Alerts]&quot; indique lorsqu’un package, un emplacement ou une publicité — ou toute entité enfant sous un package ou un emplacement — présente un problème. Une colonne &quot;[!UICONTROL Alerts]&quot; indique lorsqu’une campagne, ou toute entité enfant sous celle-ci, présente un problème. Une icône [!UICONTROL Pulse Panel] située à droite de la barre d’outils indique également si des alertes sont disponibles pour les entités répertoriées. Pour plus d’informations, voir &quot;[Affichage des alertes](campaign-alerts.md)&quot;.

### Autres types de rapports au niveau des campagnes

Pour les autres ventilations de données, consultez [les pages de création de rapports au niveau de la campagne](/help/dsp/campaign-management/campaigns/campaign-view-report.md). Le rapport comprend des sections sur les données [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] et [!UICONTROL Audience Performance].

### Autres types de rapports au niveau de l’emplacement

Pour les autres ventilations de données, consultez [les pages de rapports au niveau de l’emplacement](/help/dsp/campaign-management/placements/placement-view-report.md). Le rapport comprend des sections sur les données [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications] et [!UICONTROL Ads].

En outre, vous pouvez afficher les données suivantes dans les paramètres d’emplacement :

* [A (vue détaillée [!UICONTROL Inspector])](placement-details-view.md), qui affiche tous les sites, publicités, données de fréquence et offres ciblés pour un emplacement.

* Un [rapport de prévision de placement](/help/dsp/campaign-management/reports/placement-forecast.md).

* [Rapports de diagnostic de placement](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Autres types de rapports au niveau des annonces

Pour les autres ventilations de données, consultez [les pages de création de rapports au niveau de l’annonce ](/help/dsp/campaign-management/ads/ad-view-report.md). Le rapport comprend les données [!UICONTROL Overview], [!UICONTROL Geography] et [!UICONTROL Viewability].

>[!MORELIKETHIS]
>
>* [Affichage des sites, publicités et détails de fréquence pour un emplacement](placement-details-view.md)
>* [Gérer vos vues de données de campagne](campaign-data-views-manage.md)
>* [Exporter des données d’une vue Campaign Management](campaign-export-data.md)
>* [Afficher un rapport détaillé pour une campagne](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
>* [Afficher les alertes](campaign-alerts.md)
