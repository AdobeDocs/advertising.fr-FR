---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: En savoir plus sur les [!UICONTROL Forecast Accuracy (Actuals) Report], y compris les colonnes de données.
exl-id: ff49284a-2d13-48bf-a172-3bd461db7a3c
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# La variable [!UICONTROL Forecast Accuracy (Actuals) Report]

Ce rapport présente les données réelles d’impression, de clics, de coûts et de recettes provenant du réseau publicitaire par jour pour chaque portefeuille.

## Colonnes disponibles

Vous trouverez ci-dessous les colonnes qui sont automatiquement incluses dans chaque rapport. Vous ne pouvez pas ajouter de colonnes supplémentaires.

| Colonne | Par défaut ? | Description |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Par défaut | Nom du groupe de portefeuille auquel appartient le portfolio. |
| [!UICONTROL Portfolio ID] | Par défaut | Identifiant numérique de portefeuille. |
| [!UICONTROL EF Portfolio Group ID] | Par défaut | Identifiant numérique pour le groupe de portefeuille auquel appartient le portfolio. |
| [!UICONTROL Portfolio] | Par défaut | Le portefeuille. |
| [!UICONTROL Portfolio Status] | Par défaut | État du portfolio :<ul><li><i>[!UICONTROL Optimize]:</i> La fonctionnalité d’optimisation collecte les données de clics et de recettes pour les campagnes pertinentes, modélise les données afin d’optimiser les offres et/ou les budgets de campagne (en fonction du type d’optimisation et des stratégies d’offres de la campagne).</li><li><i>[!UICONTROL Active]:</i> La fonctionnalité d’optimisation collecte les données de clics et de recettes pour les campagnes pertinentes et modélise les données, mais elle n’optimise pas les offres ni les budgets de campagne.</li><li><i>[!UICONTROL Inactive]:</i> La fonctionnalité d’optimisation collecte les données de clics pour les campagnes pertinentes à des fins de création de rapports, mais elle ne modélise pas les données, ni n’optimise les offres ou les budgets de campagne. |
| [!UICONTROL Day of Week] | Par défaut | Le jour de la semaine rapportait : <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, ou <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Par défaut | Date indiquée. |
| [!UICONTROL Device] | Par défaut | (Publicités Google, publicité Microsoft®, Yahoo! Réseau d’affichage, Yahoo! Japan Ads et Yahoo Native campaigns) Type d’appareil sur lequel les publicités ont été affichées : <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>, ou <i>[!UICONTROL N/A]</i> (aucune valeur). Les lignes d’autres réseaux publicitaires ont des valeurs de <i>[!UICONTROL N/A]</i>.<br><br>Dans les campagnes de recherche, si les modèles de suivi ou les URL de destination des mots-clés, des publicités et/ou des extensions de publicité incluaient des paramètres pour suivre les données par appareil (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) au moment où vous avez cliqué sur la publicité, les données de conversion sont également incluses dans la ligne pour chaque type d’appareil. Sinon, si les données de conversion ne peuvent pas être attribuées à un type d’appareil, elles sont agrégées dans une ligne distincte avec un &quot;[!UICONTROL Device]&quot; valeur de <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Par défaut | Chiffre d’affaires total. |
| [!UICONTROL Impressions] | Par défaut | Nombre total d’impressions. |
| [!UICONTROL Clicks] | Par défaut | Nombre total de clics. |
| [!UICONTROL Cost] | Par défaut | Le coût total. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [À propos des rapports de précision des modèles](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [La variable [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Génération d’un rapport de précision de modèle](model-accuracy-report-generate.md)
>* [Paramètres du rapport Précision des modèles](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
