---
title: '''[!DNL Analytics] Données en Adobe Advertising"'
description: '''[!DNL Analytics] Données en Adobe Advertising"'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: b382184072af88273570fc045d0bcebe24ed81fb
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# [!DNL Analytics] Données en Adobe Advertising

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

## Segments Analytics

Tous les segments créés dans [!DNL Analytics] et publié sur Experience Cloud.

L’affichage des nouveaux segments dans Adobe Advertising prend entre 24 et 48 heures. Les mises à jour des segments existants sont synchronisées dans un délai d’environ huit heures.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Mesures d’engagement du site

>[!NOTE]
>
>* [!DNL Analytics] transmet les événements de l’eVar EF ID en Adobe Advertising.  L’intégration par défaut ne prend pas en charge l’envoi de mesures calculées ou d’autres dimensions (eVars) dans Adobe Advertising. Toutefois, si la mesure calculée peut être entièrement capturée dans un événement personnalisé, l’Adobe Advertising peut ingérer l’événement personnalisé.
>* [!DNL Analytics] transmet les données à Adobe Advertising toutes les heures.

* [!UICONTROL Timespent_secs_1stvisit]: nombre de secondes écoulées sur le site au cours de la première visite du visiteur.
* [!UICONTROL Timespent_secs_total]: nombre total de secondes passées sur le site lors de toutes les visites dans l’intervalle de recherche en amont des clics.
* [!UICONTROL Pageviews_1stvisit]: nombre de pages vues sur le site au cours de la première visite du visiteur.
* [!UICONTROL Pageviews_total]: nombre total de pages vues sur le site pour toutes les visites dans l’intervalle de recherche en amont des clics.
* [[!UICONTROL Bounces] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: nombre de fois où [!DNL Analytics] collecté [!UICONTROL EF ID].

## Mesures de conversion

[!DNL Analytics] transmet quotidiennement les mesures de conversion à Adobe Advertising.

### Mesures de conversion standard

* [[!UICONTROL Revenue] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Mesures de conversion personnalisées

Ces mesures sont spécifiques à la suite de rapports. Par conséquent, les mesures disponibles varient pour chaque client et suite de rapports.

### Mesures de conversion personnalisées créées à partir d’eVars et de props

Les mesures disponibles varient pour chaque client. Voir &quot;[Création de mesures de conversion à partir d’eVars et de props Adobe Analytics](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Mesures de conversion réservées

Ces mesures sont spécifiques à la suite de rapports. Par conséquent, les mesures disponibles varient pour chaque client et suite de rapports.

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising des mesures dans Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
