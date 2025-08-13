---
title: À propos des informations
description: Découvrez les informations sur les performances des visualisations.
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
source-git-commit: 99b9c110de5efbf646e35979eee6baac1d34f6ed
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# À propos des informations

*Fonction Beta*

Grâce aux visualisations, vous obtenez des informations de haut niveau sur les performances qui vous permettent d’optimiser efficacement vos campagnes et de découvrir de nouvelles opportunités d’optimisation des performances. Vous pouvez afficher les données de plusieurs campagnes pour un annonceur spécifié ou effectuer une analyse vers le bas à un niveau inférieur.

Utilisez les informations sur les performances pour :

* Suivre les tendances à long terme pour la planification stratégique et la prise de décisions éclairées.

* Identifier les opportunités pour obtenir de meilleurs résultats.

* Améliorez l’efficacité en réduisant le temps entre l’obtention des données brutes et l’obtention d’informations exploitables.

Vous pouvez exporter toutes les visualisations d’un onglet dans un fichier PDF ou télécharger les données d’une insight spécifique sans les visualiser au format de feuille de calcul Excel Microsoft (XLSX).

Vous pouvez également [modifier la période, configurer la vue et enregistrer une vue personnalisée](/help/dsp/campaign-management/reports/campaign-data-views-manage.md){target="_blank"} comme vous le pouvez pour les vues de gestion de campagne.

## Types d’informations

### Onglet [!UICONTROL Home]

L’onglet [!UICONTROL Home] fournit des mesures clés de norme, de performances et de visibilité sur toutes les campagnes d’un annonceur. Par défaut, les données d’emplacement croisé pour un annonceur spécifique et un objectif personnalisé s’affichent. Vous pouvez éventuellement configurer des filtres pour afficher les données d’un autre annonceur, d’un autre objectif personnalisé ou d’un emplacement spécifique. <!-- I don't see campaigns or packages anymore:  You can optionally configure filters to show data for a different advertiser or data for only specific campaigns, packages, custom goals, and placements. --> Les informations incluent :

* **[!UICONTROL Trends]:** graphique de tendance pour trois mesures spécifiées par le client (par défaut, [!UICONTROL Net Spend], [!UICONTROL Impressions] et [!UICONTROL Net CPM]).

* **[!UICONTROL Delivery Breakdown]:** répartition des données pour des mesures spécifiques selon trois dimensions spécifiées par le client, telles que par campagne, éditeur et type de média. Pour chaque répartition dimensionnelle, vous pouvez choisir une mesure différente.

### Onglet [!UICONTROL Household Reach]

L’onglet [!UICONTROL Household Reach] fournit des mesures de portée des ménages pour toutes les campagnes d’un annonceur. Par défaut, les données sur plusieurs campagnes s’affichent. Vous pouvez éventuellement configurer des filtres pour afficher les données d’un autre annonceur, d’une campagne spécifique, de plusieurs packages ou emplacements, ou d’un package ou emplacement spécifique. Ces informations incluent :

* **[!UICONTROL Trends]:** graphique de tendances par jour ou par semaine pour trois mesures spécifiées par le client (par défaut, [!UICONTROL Net Spend], [!UICONTROL Unique Reach] et [!UICONTROL Net CPM]).

* **[!UICONTROL Incremental Household Reach]:** graphique en anneau indiquant la portée incrémentielle des ménages par [!UICONTROL Media Type], [!UICONTROL Device Type] ou [!UICONTROL Inventory Type]. La *portée incrémentielle des ménages* est définie comme un ménage atteint exclusivement par le biais d’un seul type de média, d’appareil ou d’inventaire.

* **[!UICONTROL Reach Breakdown]:** portée incrémentielle unique par rapport à la portée chevauchante des ménages par [!UICONTROL Media Type], [!UICONTROL Device Type] ou [!UICONTROL Inventory Type].

  La *portée incrémentielle des ménages* est définie comme un ménage atteint exclusivement par le biais d’un seul type de média, d’appareil ou d’inventaire. La *portée chevauchante des ménages* est définie comme un ménage atteint par plusieurs types de médias, d’appareils ou d’inventaire.

* **[!UICONTROL Top Performers]:** campagnes, emplacements, packages, éditeurs, sites/applications, types de médias, types d’inventaire ou types d’appareils les plus performants par [!UICONTROL Unique Reach], [!UICONTROL Net Spend] et [!UICONTROL Cost per Reach].

* **[!UICONTROL Performance Analysis]:** [!UICONTROL Cost per Reach] et [!UICONTROL Net Spend] par package, éditeur ou site/application. Utilisez cette insight pour voir quels packages, éditeurs ou sites/applications présentent le potentiel d’une portée incrémentielle significative.

  La taille de chaque bulle indique le score de portée incrémentielle, les bulles plus grandes indiquant une portée incrémentielle plus élevée en moyenne. Pour afficher le nom complet de l’entité et les mesures clés d’une bulle, placez le curseur sur la bulle.

  Les niveaux d&#39;impact sont les suivants :

   * **Impact important :** envisager d’augmenter le budget.
   * **Impact modéré**
   * **Impact limité :** attention requise

### Onglet [!UICONTROL Household Conversion]

L’onglet [!UICONTROL Household Conversion] fournit des mesures de conversion des ménages pour toutes les campagnes d’un annonceur<!-- active only? -->. Par défaut, les données sur plusieurs campagnes pour un annonceur spécifique et une mesure de conversion spécifique s’affichent. Vous pouvez éventuellement configurer des filtres pour afficher les données d’un autre annonceur ou d’une autre mesure de conversion, pour une campagne spécifique, entre des packages ou des emplacements, ou pour un package ou un emplacement spécifique. Ces informations incluent :

* **[!UICONTROL Trends]:** graphique de tendances par jour ou par semaine pour trois mesures spécifiées par le client (par défaut, [!UICONTROL Net Spend], [!UICONTROL Conversions] et [!UICONTROL Net CPM]).

* **[!UICONTROL Conversion Participation Overview]:** graphique à barres indiquant les types de médias, de stocks et d’appareils qui génèrent la plupart des conversions de ménages.

  Les impressions diffusées pendant la période de recherche en amont (30 jours) sont considérées comme valides pour la participation à la conversion.

* **[!UICONTROL Top Performers]:** tableau des campagnes, packages, emplacements, éditeurs, sites/applications, types de médias et types d’inventaire qui génèrent les performances de trois mesures spécifiées par le client (par défaut, [!UICONTROL Net Spend], [!UICONTROL CPA] et [!UICONTROL Conversions]). La meilleure est répertoriée en premier.

* **[!UICONTROL Performance Analysis]:** [!UICONTROL CPA] et [!UICONTROL Net Spend] par package, éditeur ou site/application. Utilisez cette insight pour voir quels packages, éditeurs ou sites/applications présentent le potentiel d’une portée incrémentielle significative.

  La taille de chaque bulle indique le score de portée incrémentielle, les bulles plus grandes indiquant une portée incrémentielle plus élevée en moyenne. Pour afficher le nom complet de l’entité et les mesures clés d’une bulle, placez le curseur sur la bulle.

  Les niveaux d&#39;impact sont les suivants :

   * **Impact important :** envisager d’augmenter le budget.
   * **Impact modéré**
   * **Impact limité :** attention requise

## Ouvrir les informations sur les performances

* (Pour ouvrir les insights pour toutes les campagnes) Dans le menu principal, cliquez sur **[!UICONTROL Insights BETA]**.

* (Pour ouvrir des informations pour une campagne, un package ou un emplacement spécifique) En regard du nom de l’entité dans la vue [!UICONTROL Campaigns], [!UICONTROL Packages] ou [!UICONTROL Placements], cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Insights]**.

## Application de filtres à un onglet

1. Dans la barre d’outils située en haut de l’onglet, cliquez sur ![bouton Filtrer](/help/dsp/assets/filter.png).

1. Dans la colonne de gauche, sélectionnez une dimension, puis une ou plusieurs valeurs dans la colonne de droite, selon le cas.

   Vous ne pouvez sélectionner qu’un seul annonceur à la fois.

1. Cliquez sur **[!UICONTROL Apply]**.

1. (Facultatif) Pour réduire davantage les données, sélectionnez le type d’entité dans la barre d’outils, puis sélectionnez une valeur d’entité spécifique (une campagne, un package ou un emplacement unique).

## Modification du Dimension signalé pour une Insight

* Dans le menu déroulant situé dans le coin supérieur gauche d’insight, sélectionnez la dimension.

## Modification des mesures signalées pour un Insight

1. Dans le coin supérieur droit d’insight, cliquez sur ![Paramètres des mesures](/help/dsp/assets/metric-settings.png "Paramètres des mesures").

1. Sélectionnez les mesures, puis cliquez sur **[!UICONTROL Apply]**.

## Exporter toutes les visualisations d’un onglet dans un fichier PDF

* Au-dessus de l’onglet, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Export]**.

  Le fichier est enregistré dans le dossier Téléchargements par défaut de votre navigateur.

## Téléchargement d’un Insight spécifique dans un fichier XLSX

* Dans le coin supérieur droit d’insight, cliquez sur ![Télécharger](/help/creative/assets/download.png "Télécharger").

  Le fichier est enregistré dans le dossier Téléchargements par défaut de votre navigateur.

>[!MORELIKETHIS]
>
>* [À propos des rapports personnalisés](/help/dsp/reports/report-about.md)
>* [Types de rapports de performances dans les vues de gestion de campagnes](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)
>* [Gestion Des Vues De Données De Campaign](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
