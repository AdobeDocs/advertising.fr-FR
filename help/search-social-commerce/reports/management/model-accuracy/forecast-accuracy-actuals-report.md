---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Découvrez [!UICONTROL Forecast Accuracy (Actuals) Report], y compris les colonnes de données.
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Le [!UICONTROL Forecast Accuracy (Actuals) Report]

Ce rapport présente les données réelles d’impression, de clics, de coûts et de recettes provenant du réseau publicitaire par jour pour chaque portefeuille.

## Colonnes disponibles

Vous trouverez ci-dessous les colonnes qui sont automatiquement incluses dans chaque rapport. Vous ne pouvez pas ajouter de colonnes supplémentaires.

| Colonne | Par défaut ? | Description |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Par défaut | Nom du groupe de portefeuille auquel appartient le portfolio. |
| [!UICONTROL Portfolio ID] | Par défaut | Identifiant numérique de portefeuille. |
| [!UICONTROL EF Portfolio Group ID] | Par défaut | Identifiant numérique pour le groupe de portefeuille auquel appartient le portfolio. |
| [!UICONTROL Portfolio] | Par défaut | Le portefeuille. |
| [!UICONTROL Portfolio Status] | Par défaut | État du portfolio :<ul><li><i>[!UICONTROL Optimize] : </i> La fonctionnalité d’optimisation collecte les données de clics et de recettes pour les campagnes pertinentes, en modélisant les données utilisées pour l’optimisation et en optimisant les offres, les budgets de campagne et les cibles de stratégie d’offre de campagne (en fonction du type d’optimisation et des stratégies d’offre).</li><li><i>[!UICONTROL Active] : </i> La fonctionnalité d’optimisation collecte les données de clics et de recettes pour les campagnes pertinentes et modélise les données, mais elle n’optimise pas les offres ni les budgets de campagne.</li><li><i>[!UICONTROL Inactive] : </i> La fonctionnalité d’optimisation collecte des données de clics pour les campagnes pertinentes à des fins de création de rapports, mais elle ne modélise pas les données, ni n’optimise les offres ou les budgets de campagne. |
| [!UICONTROL Day of Week] | Par défaut | Le jour de la semaine signalé : <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> ou <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Par défaut | Date indiquée. |
| [!UICONTROL Device] | Par défaut | (Publicités Google, Microsoft Advertising, Yahoo! Réseau d’affichage, Yahoo! Japan Ads et Yahoo Native campaigns) Type d’appareil sur lequel les publicités ont été affichées : <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i> ou <i>[!UICONTROL N/A]</i> (aucune valeur). Les lignes d’autres réseaux publicitaires ont des valeurs de <i>[!UICONTROL N/A]</i>.<br><br> Dans les campagnes de recherche, si les modèles de suivi ou les URL de destination des mots-clés, publicités et/ou extensions de publicités incluaient des paramètres pour suivre les données par appareil (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel})</code>) au moment où vous avez cliqué sur la publicité, les données de conversion sont également incluses dans la ligne pour chaque type d’appareil. Sinon, si les données de conversion ne peuvent pas être attribuées à un type d’appareil, elles sont agrégées dans une ligne distincte avec une valeur &quot;[!UICONTROL Device]&quot; de <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Par défaut | Chiffre d’affaires total. |
| [!UICONTROL Impressions] | Par défaut | Nombre total d’impressions. |
| [!UICONTROL Clicks] | Par défaut | Nombre total de clics. |
| [!UICONTROL Cost] | Par défaut | Le coût total. |

>[!MORELIKETHIS]
>
>* [À propos des rapports de précision de modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [ [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Générer un rapport de précision de modèle](model-accuracy-report-generate.md)
>* [ Paramètres de rapport de précision du modèle ](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
