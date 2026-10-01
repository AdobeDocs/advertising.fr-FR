---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: En savoir plus sur le [!UICONTROL Google AI Max Search Term Combination Report].
feature: Search Reports, Search Specialty Reports
source-git-commit: a595c7d6245fa5d65e704e88230f2eab0a336e72
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*Applicable aux comptes [!DNL Google Ads] avec les campagnes activées pour AI max uniquement*

La [!UICONTROL Google AI Max Search Term Combination Report] montre comment des requêtes de recherche spécifiques sont mappées à des titres générés par l’IA et à des pages de destination dynamiques, ainsi qu’à des actions de conversion pour des annonces dans des campagnes activées par [!DNL Google Ads AI Max] dans des comptes spécifiés. Le rapport comprend deux feuilles :

* [!UICONTROL AI Max Search Term] d’affichage : performances de combinaisons d’annonces et de pages de destination spécifiques en fonction des recherches effectuées dans le réseau de recherche. La feuille comprend des données relatives aux impressions, aux clics et aux coûts, ainsi que toutes les mesures de conversion [!DNL Google Ads] facultatives spécifiées dans les paramètres du rapport. Par défaut, les données incluent une ligne pour chaque combinaison de terme de recherche, d’en-tête et de page de destination qui a reçu au moins une impression dans la plage de données spécifiée. Les lignes sont classées par ordre croissant par campagne par défaut, puis par une autre colonne de votre choix.

  Utilisez cette feuille pour analyser l’intention et les performances des éléments publicitaires résultants par requête afin de pouvoir créer des listes de mots-clés négatifs fiables.

* <!-- [!UICONTROL Search Term x Conversion Action] sheet? -->[!UICONTROL AI Max Search Term #1] : données de conversion suivies par [!DNL Google Ads] par action de conversion pour chaque terme de recherche et type de correspondance. Chaque ligne comprend l’action de conversion, le nombre de conversions et la valeur de conversion, ainsi que toute autre mesure de conversion [!DNL Google Ads] facultative spécifiée dans les paramètres du rapport. Par défaut, les données incluent une ligne pour chaque combinaison de terme de recherche et d’action de conversion dans la plage de données spécifiée. Les lignes sont dans le même ordre que celles de la première feuille.

  <!-- Should it be this?  The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions. -->

  Utilisez cette feuille pour comprendre comment chaque terme de recherche génère des conversions, réparties par action de conversion.

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## Colonnes par défaut

Pour la description de toutes les colonnes par défaut et personnalisées, voir « [Colonnes de rapport pour les rapports spécialisés](specialty-report-columns.md) ».

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Conversion Action] (inclus automatiquement dans la feuille de [!UICONTROL AI Max Search Term #1], même si vous ne l’incluez pas explicitement)
* [!UICONTROL Conversions] (inclus automatiquement dans la feuille de [!UICONTROL AI Max Search Term #1], même si vous ne l’incluez pas explicitement)
* [!UICONTROL Conversions Value] (inclus automatiquement dans la feuille de [!UICONTROL AI Max Search Term #1], même si vous ne l’incluez pas explicitement)

>[!MORELIKETHIS]
>
>* [À propos des rapports spécialisés](specialty-report-about.md)
>* [Gérer les rapports planifiés](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Paramètres des rapports spécialisés](specialty-report-settings.md)
>* [Colonnes de rapport pour les rapports spécialisés](specialty-report-columns.md)
