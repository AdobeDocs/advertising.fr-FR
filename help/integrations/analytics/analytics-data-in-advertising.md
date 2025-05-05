---
title: '[!DNL Analytics] Data in Adobe Advertising'
description: '[!DNL Analytics] Data in Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# [!DNL Analytics] Données en Adobe Advertising

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

## Segments Analytics

Tous les segments créés dans [!DNL Analytics] et publiés dans Experience Cloud.

L’affichage des nouveaux segments dans Adobe Advertising prend entre 24 et 48 heures. Les mises à jour des segments existants sont synchronisées dans un délai d’environ huit heures.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Mesures d’engagement du site

>[!NOTE]
>
>* [!DNL Analytics] transmet les événements de l’EF ID [!DNL eVar] dans Adobe Advertising.  L’intégration par défaut ne prend pas en charge l’envoi de mesures calculées ou d’autres dimensions ([!DNL eVars]) dans Adobe Advertising. Toutefois, si la mesure calculée peut être entièrement capturée dans un événement personnalisé, l’Adobe Advertising peut ingérer l’événement personnalisé.
>* [!DNL Analytics] transmet les données à l’Adobe Advertising toutes les heures.

* [!UICONTROL Timespent_secs_1stvisit] : nombre de secondes passées sur le site lors de la première visite du visiteur.
* [!UICONTROL Timespent_secs_total] : nombre total de secondes passées sur le site pour toutes les visites dans l’intervalle de recherche en amont des clics.
* [!UICONTROL Pageviews_1stvisit] : nombre de pages vues sur le site pendant la première visite du visiteur.
* [!UICONTROL Pageviews_total] : nombre total de pages vues sur le site pour toutes les visites dans l’intervalle de recherche en amont des clics.
* [[!UICONTROL Bounces] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=fr)
* [[!UICONTROL Visits] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=fr)
* [!UICONTROL ef_id_instances] : nombre de fois où [!DNL Analytics] a collecté un [!UICONTROL EF ID].

## Mesures de conversion

[!DNL Analytics] transmet quotidiennement les mesures de conversion à l’Adobe Advertising.

### Mesures de conversion standard

* [[!UICONTROL Revenue] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=fr)
* [[!UICONTROL Orders] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=fr)
* [[!UICONTROL Units] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=fr)
* [[!UICONTROL Carts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=fr)
* [[!UICONTROL Cart Views] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=fr)
* [[!UICONTROL Checkouts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=fr)
* [[!UICONTROL Cart Additions] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html?lang=fr)
* [[!UICONTROL Cart Removals] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=fr)

### Mesures de conversion personnalisées

Ces mesures sont spécifiques à la suite de rapports. Par conséquent, les mesures disponibles varient pour chaque client et suite de rapports.

### Mesures de conversion personnalisées créées à partir de [!DNL eVars] et [!DNL Props]

Les mesures disponibles varient pour chaque client. Voir &quot;[Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;.

### Mesures de conversion réservées

Ces mesures sont spécifiques à la suite de rapports. Par conséquent, les mesures disponibles varient pour chaque client et suite de rapports.

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising des mesures dans Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
