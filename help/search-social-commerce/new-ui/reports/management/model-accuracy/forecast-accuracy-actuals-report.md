---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Découvrez les [!UICONTROL Forecast Accuracy (Actuals) Report], y compris les colonnes de données.
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# Le [!UICONTROL Forecast Accuracy (Actuals) Report]

Ce rapport affiche les données réelles sur l’impression, le clic, le coût et le chiffre d’affaires du réseau publicitaire par jour pour chaque portfolio.

## Colonnes disponibles

Voici les colonnes qui sont automatiquement incluses dans chaque rapport. Vous ne pouvez pas ajouter de colonnes supplémentaires.

| Colonne | Par défaut ? | Description |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Par défaut | Nom du groupe de portefeuilles auquel le portefeuille appartient. |
| [!UICONTROL Portfolio ID] | Par défaut | Identifiant numérique de portfolio. |
| [!UICONTROL EF Portfolio Group ID] | Par défaut | Identifiant numérique du groupe de portefeuilles auquel appartient le portefeuille. |
| [!UICONTROL Portfolio] | Par défaut | Le portfolio. |
| [!UICONTROL Portfolio Status] | Par défaut | Statut du portefeuille :<ul><li><i>[!UICONTROL Optimize] :</i> la fonctionnalité d’optimisation collecte les données sur les clics et le chiffre d’affaires pour les campagnes appropriées, modélise les données utilisées pour l’optimisation et optimise les enchères, les budgets de campagne et les cibles de stratégie d’enchères de campagne (selon le type d’optimisation et les stratégies d’enchères).</li><li><i>[!UICONTROL Active] :</i> la fonctionnalité d’optimisation collecte les données sur les clics et le chiffre d’affaires pour les campagnes appropriées et modélise les données, mais elle n’optimise pas les enchères ni les budgets de campagne.</li><li><i>[!UICONTROL Inactive] :</i> la fonctionnalité d’optimisation collecte les données de clics pour les campagnes appropriées à des fins de création de rapports, mais elle ne modélise pas les données ni n’optimise les offres ou les budgets de campagne. |
| [!UICONTROL Day of Week] | Par défaut | Jour de la semaine signalé : <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> ou <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Par défaut | Date du signalement. |
| [!UICONTROL Device] | Par défaut | (Google Ads, [!DNL LY Ads], Microsoft Advertising, Yahoo ! Campagnes réseau d’affichage et natives Yahoo) Type d’appareil sur lequel les annonces étaient affichées : <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i> ou <i>[!UICONTROL N/A]</i> (aucune valeur). Les lignes des autres réseaux publicitaires ont la valeur <i>[!UICONTROL N/A]</i>.<br><br>Dans les campagnes de recherche, si les modèles de suivi ou les URL de destination pour les mots-clés, les publicités et/ou les extensions publicitaires incluaient des paramètres pour suivre les données par appareil (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) au moment où l’utilisateur a cliqué sur la publicité, les données de conversion sont également incluses dans la ligne pour chaque type d’appareil. Sinon, si les données de conversion ne peuvent pas être attribuées à un type d’appareil, elles sont agrégées dans une ligne distincte avec une valeur « [!UICONTROL Device] » de <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Par défaut | Chiffre d’affaires total. |
| [!UICONTROL Impressions] | Par défaut | Le total des impressions. |
| [!UICONTROL Clicks] | Par défaut | Nombre total de clics. |
| [!UICONTROL Cost] | Par défaut | Coût total. |

>[!MORELIKETHIS]
>
>* [À propos des rapports de précision de modèle](model-accuracy-report-about.md)
>* [Le [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Gérer les rapports planifiés](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Paramètres du rapport de précision du modèle](model-accuracy-report-settings.md)
