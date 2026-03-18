---
title: '[!DNL Analytics] de données dans Adobe Advertising'
description: '[!DNL Analytics] de données dans Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# [!DNL Analytics] de données dans Adobe Advertising

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

## Segments Analytics

Tous les segments créés dans [!DNL Analytics] et publiés sur Experience Cloud.

Les nouveaux segments prennent entre 24 et 48 heures pour apparaître dans Adobe Advertising. Les mises à jour des segments existants sont synchronisées dans un délai d’environ huit heures.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Mesures d’engagement du site

>[!NOTE]
>
>* [!DNL Analytics] transmet les événements pour l’ID d’événement [!DNL eVar] dans Adobe Advertising.  L’intégration par défaut ne prend pas en charge l’envoi de mesures calculées ou d’autres dimensions ([!DNL eVars]) dans Adobe Advertising. Toutefois, si la mesure calculée peut être entièrement capturée dans un événement personnalisé, Adobe Advertising peut alors ingérer l’événement personnalisé.
>* [!DNL Analytics] transmet les données à Adobe Advertising toutes les heures.

* [!UICONTROL Timespent_secs_1stvisit] : nombre de secondes passées sur le site lors de la première visite du visiteur ou de la visiteuse.
* [!UICONTROL Timespent_secs_total] : nombre total de secondes passées sur le site au cours de toutes les visites dans l’intervalle de recherche en amont des clics.
* [!UICONTROL Pageviews_1stvisit] : nombre de pages vues sur le site lors de la première visite du visiteur ou de la visiteuse.
* [!UICONTROL Pageviews_total] : nombre total de pages vues sur le site au cours de toutes les visites dans l’intervalle de recherche en amont des clics.
* [[!UICONTROL Bounces] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances] : nombre de fois où [!DNL Analytics] avez collecté une [!UICONTROL EF ID].

## Mesures de conversion

[!DNL Analytics] transmet quotidiennement les mesures de conversion à Adobe Advertising.

### Mesures de conversion standard

* [[!UICONTROL Revenue] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] une mesure](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Mesures de conversion personnalisées

Ces mesures sont spécifiques à la suite de rapports. Par conséquent, les mesures disponibles varient pour chaque client et suite de rapports.

### Mesures de conversion personnalisées créées à partir de [!DNL eVars] et [!DNL Props]

Les mesures disponibles varient pour chaque client. Voir « [Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md) ».

### Mesures de conversion réservées

Ces mesures sont spécifiques à la suite de rapports. Par conséquent, les mesures disponibles varient pour chaque client et suite de rapports.

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Mesures Adobe Advertising dans Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
