---
title: Mesures et dimensions Adobe Advertising dans Customer Journey Analytics
description: Référencez les mesures et dimensions Adobe Advertising disponibles dans Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: c3836d8af50061701434790b2bd9214df29e8a01
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Mesures et dimensions Adobe Advertising dans Customer Journey Analytics

*Publicitaires avec une intégration Adobe Advertising-Customer Journey Analytics uniquement*

Adobe Advertising transmet quotidiennement aux [!DNL Customer Journey Analytics] les mesures et dimensions de trafic. [!DNL Web SDK] capture les clics publicitaires et les affichages publicitaires d’Adobe Advertising en temps réel et les transmet à Customer Journey Analytics.

## mesures de trafic Adobe Advertising

<!-- Verify column names -->

>[!NOTE]
>
>* « Nom du champ XDM » est le nom du champ dans Adobe Experience Platform.
>* « Nom d’affichage du champ XDM » indique le nom d’affichage dans Customer Journey Analytics.

| Nom de champ Adobe Advertising | Nom du champ XDM | Nom d’affichage du champ XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Date | Date | Tous | |
| AMO - ID | skwcid | ADOBE ADVERTISING ID | Tous |
| AMO - Impressions | adobe_advertising_impressions | Adobe Advertising Impressions | Tous |
| AMO - Clics | adobe_advertising_clicks | Clics Adobe Advertising | Tous |
| AMO - Coût | adobe_advertising_cost | Coût d’Adobe Advertising | Tous |
| Code de devise | monnaie | Devise monétaire | Tous |
| AMO - Vues | adobe_advertising_views | Vues Adobe Advertising | Ad Cloud DSP |
| AMO - Vues terminées à 25 % | adobe_advertising_views_25_pct | Vues Adobe Advertising terminées à 25 % | Ad Cloud DSP |
| AMO - Vues terminées à 50 % | adobe_advertising_views_50_pct | Vues Adobe Advertising terminées à 50 % | Ad Cloud DSP |
| AMO - Vues terminées à 75 % | adobe_advertising_views_75_pct | Vues Adobe Advertising terminées à 75 % | Ad Cloud DSP |
| AMO - Vues terminées à 100 % | adobe_advertising_views_100_pct | Vues Adobe Advertising terminées à 100 % | Ad Cloud DSP |
| AMO - Minutes vues | adobe_advertising_minutes_viewed | Adobe Advertising Minutes Viewed | Ad Cloud DSP |
| AMO - Impressions visibles | adobe_advertising_viewable_impressions | Adobe Advertising Viewable Impressions | Ad Cloud DSP |
| AMO - Impressions non visibles | adobe_advertising_not_viewable_impressions | Impressions Adobe Advertising non visibles | Ad Cloud DSP |
| AMO - Impressions mesurables | adobe_advertising_measurement_impressions | Adobe Advertising Measurable Impressions | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Dimensions Adobe Advertising

>[!NOTE]
>
>* « Champ XDM » est le nom du champ dans Adobe Experience Platform.
>* « Nom d’affichage du champ XDM » indique le nom d’affichage dans Customer Journey Analytics.

| Nom de champ Adobe Advertising | Nom du champ XDM | Nom d’affichage du champ XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Clé | skwcid | ADOBE ADVERTISING ID |
| Plateforme publicitaire | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |
| Compte | adobe_advertising_account | Compte Adobe Advertising |
| Campagne | adobe_advertising_campaign | Adobe Advertising Campaign |
| Groupe publicitaire | adobe_advertising_ad_group | Groupe publicitaire Adobe Advertising |
| Mot-clé | adobe_advertising_keyword | Mot-clé Adobe Advertising |
| Annonce publicitaire | adobe_advertising_ad | Adobe Advertising Ad |
| Placement | adobe_advertising_placement | Emplacement Adobe Advertising |
| Type de correspondance | adobe_advertising_match_type | Type de correspondance Adobe Advertising |
| Titre de la publicité | adobe_advertising_ad_title | Titre de publicité Adobe Advertising |
| Description de l’annonce publicitaire | adobe_advertising_ad_description | Description de l’annonce publicitaire Adobe Advertising |
| Ajouter une URL de destination | adobe_advertising_ad_destination_url | URL de destination de la publicité Adobe Advertising |
| URL d’affichage de la publicité | adobe_advertising_ad_display_url | URL d’affichage des publicités Adobe Advertising |
| Périphérique | adobe_advertising_device | Appareil Adobe Advertising |
| Type de correspondance de mot-clé | adobe_advertising_keyword_matchtype | Adobe Advertising Keyword MatchType |
| Réseau | adobe_advertising_network | Réseau Adobe Advertising |
| Type d’annonce | adobe_advertising_ad_type | Type d’annonce Adobe Advertising |
| Cible du produit | adobe_advertising_product_target | Adobe Advertising Product Target |
| Type de destination | adobe_advertising_landing_type | Type d’atterrissage Adobe Advertising |
| Optimisation | adobe_advertising_optimization | Optimisation d’Adobe Advertising |

>[!MORELIKETHIS]
>
>* [Aperçu](overview.md)
>* [Conditions préalables](prerequisites.md)
>* [ID Adobe Advertising utilisés par  [!DNL Customer Journey Analytics]](ids.md)
