---
title: Mesures et dimensions Adobe Advertising dans Customer Journey Analytics
description: Référencez les mesures et dimensions Adobe Advertising disponibles dans Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 97c89e03-ab15-4906-96fc-6bb77ea0cd7c
TQID: https://experienceleague.adobe.com/JN42ThofnM6kP8Urd8bTpyQbIWIReb-jgCbOvlnCAQ0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: a93c33ee47bd1a8df137a69598b367e985def4ee
workflow-type: tm+mt
source-wordcount: 456
ht-degree: 0%

---

# Mesures et dimensions Adobe Advertising dans Customer Journey Analytics

*Publicitaires avec une intégration Adobe Advertising-Customer Journey Analytics uniquement*

Adobe Advertising transmet quotidiennement aux [!DNL Customer Journey Analytics] les mesures et dimensions de trafic. [!DNL Web SDK] capture les clics publicitaires et les affichages publicitaires d’Adobe Advertising en temps réel et les transmet à Customer Journey Analytics.

![Exemple de données Adobe Advertising dans Customer Journey Analytics](/help/integrations/assets/cja-report-example.png "Exemple de données Adobe Advertising dans Customer Journey Analytics")

## mesures de trafic Adobe Advertising

<!-- Verify column names -->

Dans le tableau suivant :

* « Nom du champ XDM » est le nom du champ dans Adobe Experience Platform.

* « Nom d’affichage du champ XDM » indique le nom d’affichage dans Customer Journey Analytics.

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

Dans le tableau suivant :

<!-- Need to fill in the "Source" column -->

* « Nom du champ XDM » est le nom du champ dans Adobe Experience Platform.

* « Nom d’affichage du champ XDM » indique le nom d’affichage dans Customer Journey Analytics.

| Nom de champ Adobe Advertising | Nom du champ XDM | Nom d’affichage du champ XDM | Source |
|------------------------------|----------------|------------------------|--------|
| Clé | skwcid | ADOBE ADVERTISING ID |  |
| Plateforme publicitaire | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |  |
| Compte | adobe_advertising_account | Compte Adobe Advertising |  |
| Campagne | adobe_advertising_campaign | Adobe Advertising Campaign |  |
| Groupe publicitaire | adobe_advertising_ad_group | Groupe publicitaire Adobe Advertising |  |
| Mot-clé | adobe_advertising_keyword | Mot-clé Adobe Advertising |  |
| Annonce publicitaire | adobe_advertising_ad | Adobe Advertising Ad |  |
| Placement | adobe_advertising_placement | Emplacement Adobe Advertising |  |
| Type de correspondance | adobe_advertising_match_type | Type de correspondance Adobe Advertising |  |
| Titre de la publicité | adobe_advertising_ad_title | Titre de publicité Adobe Advertising |  |
| Description de l’annonce publicitaire | adobe_advertising_ad_description | Description de l’annonce publicitaire Adobe Advertising |  |
| Ajouter une URL de destination | adobe_advertising_ad_destination_url | URL de destination de la publicité Adobe Advertising |  |
| URL d’affichage de la publicité | adobe_advertising_ad_display_url | URL d’affichage des publicités Adobe Advertising |  |
| Périphérique | adobe_advertising_device | Appareil Adobe Advertising |  |
| Type de correspondance de mot-clé | adobe_advertising_keyword_matchtype | Adobe Advertising Keyword MatchType |  |
| Réseau | adobe_advertising_network | Réseau Adobe Advertising |  |
| Type d’annonce | adobe_advertising_ad_type | Type d’annonce Adobe Advertising |  |
| Cible du produit | adobe_advertising_product_target | Adobe Advertising Product Target |  |
| Type de destination | adobe_advertising_landing_type | Type d’atterrissage Adobe Advertising |  |
| Optimisation | adobe_advertising_optimization | Optimisation d’Adobe Advertising |  |

>[!MORELIKETHIS]
>
>* [Aperçu](overview.md)
>* [Conditions préalables](prerequisites.md)
>* [Adobe Advertising ID utilisés par  [!DNL Customer Journey Analytics]](ids.md)
>* [Configurer la collecte, le transfert et la création de rapports de données](set-up.md)
>* [Dépannage](troubleshooting.md)
