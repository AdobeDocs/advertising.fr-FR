---
title: Présentation de  [!DNL Analytics for Advertising]
description: Présentation de  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
TQID: https://experienceleague.adobe.com/OHxJO1mtbzOtt5oGDJF26xSuVLG-HnRDdIGDrUH2pzk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1306
ht-degree: 0%

---

# Présentation de [!DNL Analytics for Advertising]

*Annonceurs avec Advertising Creative, Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] intègre Adobe Analytics et Adobe Advertising pour étendre et améliorer les fonctionnalités de chaque produit.

L’intégration permet aux annonceurs de suivre les interactions de site en cas de clic publicitaire et d’affichage publicitaire dans leurs instances [!DNL Analytics], ce qui permet aux marques de voir comment leurs dépenses publicitaires conduisent à l’engagement du site et aux objectifs commerciaux critiques.

En outre, Adobe Advertising peut accéder aux vastes données propriétaires que [!DNL Analytics] collecte à l’aide de balises [!DNL Analytics] déjà présentes sur le site. Cela permet une gestion de parcours plus robuste, un remarketing propriétaire et des rapports de sites de médias achetés. Adobe Advertising peut utiliser davantage les données [!DNL Analytics] pour l’optimisation des dépenses et des enchères.

Lorsqu’il est correctement utilisé, [!DNL Analytics for Advertising] brouille les lignes entre deux rôles traditionnels : la gestion du parcours publicitaire (le fait d’envoyer des utilisateurs et utilisatrices sur le site par le biais d’annonces publicitaires) et la compréhension de l’engagement du site par le biais d’analyses web.

Avantages du Principal :

* Envoyez [!DNL Analytics] segments directement à Adobe Advertising pour le remarketing de site propriétaire.
* Utilisez [!DNL Analytics] événements personnalisés et standard comme signaux de conversion pour optimiser la publicité sur les médias achetés.
* Tirez parti d’[!DNL Analytics] Analysis Workspace pour mieux comprendre les points d’entrée du site et le comportement des visites.
* resserrer la collaboration entre les analystes web et les équipes de médias achetés.
* Utilisez les identifiants Adobe Advertising persistants d’affichage publicitaire et de clic publicitaire dans [!DNL Analytics] pour comprendre l’engagement du site.
* Améliorez les rapports de médias achetés traditionnels dans Analysis Workspace avec des mesures, des dimensions et une activité de site personnalisées, ce qui n’est pas possible lors de l’exportation de données ou de pixels vers des serveurs de publicités ou d’autres DSP.
* Tirez parti du code [!DNL Analytics] déjà présent sur votre site web pour le tracking et l’optimisation dans Adobe Advertising.

>[!TIP]
>
> Watch a [video introduction to [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Using Analytics for paid media reporting

[!DNL Analytics for Advertising] improves reporting and insight on how your advertising drives site behavior by allowing you to:

* Utilisez les identifiants Adobe Advertising persistants d’affichage publicitaire et de clic publicitaire dans [!DNL Analytics] pour comprendre l’engagement du site.
* Take advantage of Analysis Workspace to better understand site entry points and visit behavior. You can access paid media dimensional and event data, which include Adobe Advertising campaign entity names (down to placements and ads) and their associated metrics, such as clicks, impressions, and cost.

To use [!DNL Analytics] as your paid media reporting tool, your organization needs an Adobe CX Enterprise (formerly Adobe Experience Cloud) login with access to Analysis Workspace. Your Adobe Advertising team will help you to map your Adobe Advertising data to individual report suites in Analysis Workspace. You can send Adobe Advertising data to any report suite, but you should be aware of the report suites that have been mapped to Adobe Advertising and those that haven&#39;t. Depending on the report suite, this may change the data reported.

[Adobe Advertising IDs within [!DNL Analytics]](ids.md) work like other [!DNL eVars], with a custom, persistent expiration. By default, the attribution lookback window is set to 60 days during the Adobe Advertising implementation. To change this setting, work with your Adobe Account Team.

Adobe Advertising dimensions are appended with the suffix &quot;(AMO ID)&quot; (such as &quot;Ad Type (AMO ID)&quot;). See &quot;[Adobe Advertising Metrics in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; for a list of the available dimensions.

>[!NOTE]
>
> When you view Adobe Advertising data (or any data set) within [!DNL Analytics], be aware that metrics and reports are based on the rules that are set within [!DNL Analytics]. The data could be different than what you see within other reporting systems, such as ad server reports, [!DNL DSP] reports, or search engine reports. To understand the data differences in [!DNL Analytics], you need to know when [!DNL eVar] data expires, what defines a visit, what is considered last touch attribution versus total persisting attribution, and other factors. For more information, see [Expected data variances between [!DNL Analytics] and Adobe Advertising](data-variances.md).

## Using Analytics to power Adobe Advertising campaigns and portfolios

Without requiring any additional pixels, [!DNL Analytics for Advertising] enables better optimization and easier audience segmentation by sending two main signals to Adobe Advertising:

* Conversion metrics to be used as bid signals:
   * standard metrics, such as [!UICONTROL Revenue] and [!UICONTROL Cart Views].
   * site engagement metrics, such as page view and visit metrics.
   * custom revenue metrics.
   * reserved revenue metrics.
* Segments created in [!DNL Analytics] and published to CX Enterprise.

  You can use [!DNL Analytics] segments for first-party site retargeting in [!DNL DSP], [!DNL Creative], and paid search advertisements.

  ([!DNL Search, Social, & Commerce] only) Advertisers with [!DNL Analytics] but not Audience Manager can also create Google website tag-based audiences (remarketing lists) and customer match audiences (customer lists) from [!DNL Analytics] segments that are shared with CX Enterprise.

### Site conversion metrics as bid signals

You can use your standard events and custom events from [!DNL Analytics] to build weighted objectives in Adobe Advertising. Objectives inform bidding decisions for your [!DNL DSP] packages and Search, Social, &amp; Commerce portfolios.

For [!DNL Google Ads] and [!DNL Google Microsoft Advertising] campaigns in Search, Social, &amp; Commerce hybrid portfolios, you can optionally upload the objectives — including any [!DNL Analytics] events in the objectives — directly to the ad networks, where they become available as conversion actions for account-level and campaign-level custom conversion goals.

>[!NOTE]
>
> You can&#39;t map calculated metrics from [!DNL Analytics] into Adobe Advertising.

Your Adobe Advertising team will help you to identify and map the events that are applicable to paid media performance into Adobe Advertising.

See &quot;[Analytics Metrics in Adobe Advertising](analytics-data-in-advertising.md)&quot; for a list of available metrics.

### Analytics segments for site retargeting

Adobe Advertising can ingest [!DNL Analytics] segments for remarketing purposes for [!DNL Creative], [!DNL DSP], and [!DNL Search, Social, & Commerce] ads using the native CX Enterprise Audiences integration between [!DNL Analytics] and CX Enterprise.

To access the [!DNL Analytics] segments, an advertiser account must enable the [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). When the ID Service is enabled, all CX Enterprise segments become available within Adobe Advertising as soon as they are processed. CX Enterprise segments include segments created in [!DNL Analytics] and published to CX Enterprise, segments created in Adobe Audience Manager, segments created in CX Enterprise using the [!DNL People core service], and segments created in Adobe Experience Platform and sent to Adobe Advertising via Audience Manager.

[!DNL Analytics] segments are available within 24 hours and are updated daily.

For more information about the CX Enterprise Audiences service, see [CX Enterprise Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Examples of how to use the integration {#integration-examples}

### Using Adobe Advertising data in Analysis Workspace

To learn how you can use your Adobe Advertising data to create visual reports in Analysis Workspace, see the video &quot;[Introduction to Workspace and Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Using connected TV view-through conversions in reports

*Advertising DSP users only*

You can measure the full-funnel effectiveness of your connected TV (CTV) campaigns by linking ad exposure on CTV devices to on-site conversions. The new [!UICONTROL Landing Type] filter &quot;[!UICONTROL View-through (CTV)]&quot; splits conversions into separate rows for [!UICONTROL Click Through], [!UICONTROL View Through], and [!UICONTROL View Through (CTV)] values.

Pour afficher vos mesures de conversion des affichages publicitaires CTV, utilisez la vue Emplacement ou la vue Canal marketing dans Analysis Workspace.

Utilisation de la vue Emplacement :

1. Incluez les emplacements de dépenses CTV dans la vue de rapport.

1. Incluez les mesures souhaitées, telles que « Impressions », « Clics », etc.

1. Appliquez les filtres suivants :

   Plateforme publicitaire : `Advertising Cloud DSP`

   Page de destination : `View-Through (CTV)`

Utilisation de la vue Canal marketing :

1. Incluez la dimension `Marketing Channel`.

1. Incluez les mesures souhaitées, telles que « Impressions », « Clics », etc.

1. Appliquez les filtres suivants :

   Plateforme publicitaire : `Advertising Cloud DSP`

   Page de destination : `View-Through (CTV)`

### Création de tableaux de bord Adobe Advertising

Pour découvrir comment effectuer le suivi de vos données Adobe Advertising par rapport à vos objectifs dans Analysis Workspace, regardez la vidéo « [Création de tableaux de bord Adobe Advertising avec Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html) ».

### Utilisation de l’Adobe Advertising ID pour l’analyse de l’entrée sur le site

Pour découvrir comment créer un rapport d’entrée sur le site Adobe Advertising afin de surveiller les influences géographiques, le navigateur et le jour de la semaine, regardez la vidéo « [ Créer des rapports d’entrée sur le site Adobe Advertising ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html) ».

## Lancement d’une implémentation [!DNL Analytics for Advertising]

Contactez l’équipe chargée de votre compte Adobe, qui effectuera la configuration initiale nécessaire pour commencer et qui vous aidera à planifier votre implémentation et l’utilisation des données en fonction des besoins de votre entreprise.

>[!MORELIKETHIS]
>
>* [Vidéo : présentation de  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Conditions préalables et informations clés pour l’implémentation de  [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe Advertising ID utilisés par Analytics](ids.md)
>* [Code JavaScript pour Analytics for Advertising](/help/integrations/analytics/javascript.md)
>* [Écarts de données attendus entre  [!DNL Analytics]  et Adobe Advertising](data-variances.md)
>* [Mesures Adobe Advertising dans Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
