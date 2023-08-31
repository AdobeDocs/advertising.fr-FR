---
title: Adobe Advertising des mesures dans Analysis Workspace
description: Adobe Advertising des mesures dans Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Adobe Advertising des mesures dans Analysis Workspace

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

>[!NOTE]
>
>* Adobe Advertising transmet les mesures et dimensions de trafic à [!DNL Analytics] quotidien.
>* [!DNL Analytics] capture les clics publicitaires et les affichages publicitaires d’Adobe Advertising en temps réel.
>* Pour [!DNL Search, Social, & Commerce], cette fonctionnalité est prise en charge pour la plupart des réseaux publicitaires et des types de campagne. Voir &quot;[Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md)&quot; dans la variable [!DNL Search, Social, & Commerce] Guide pour plus d’informations.

## Mesures de trafic d’un Adobe Advertising

Adobe Advertising des mesures de trafic dans [!DNL Analytics] commence généralement par &quot;Adobe Advertising&quot;, à l’exception de &quot;[!UICONTROL AMO ID Instances].&quot; Toutefois, pour les clients à long terme qui ont utilisé un événement personnalisé (plutôt qu’un événement réservé) pour créer initialement des mesures pour les clics, les coûts et les impressions, ces mesures commencent toujours par &quot;AMO&quot;.

| Mesure de trafic | Description |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] ou (certains clients hérités) [!UICONTROL AMO Clicks] | Nombre total de clics Adobes Advertising. |
| [!UICONTROL Adobe Advertising Cost] ou (certains clients hérités) [!UICONTROL AMO Cost] | L’Adobe Advertising dépensé dans la devise de la suite de rapports. |
| [!UICONTROL Adobe Advertising Impressions] ou (certains clients hérités) [!UICONTROL AMO Impressions] | Nombre d’impressions d’Adobe Advertising. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Nombre d’impressions diffusées pour lesquelles l’instrumentation de visibilité a été initialisée avec succès. Cette valeur est calculée en tant que (impressions instrumentées : nombre d’impressions non mesurables). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Nombre de minutes pendant lesquelles une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Nombre d’impressions qui n’étaient pas visibles. Cette valeur est calculée comme suit : ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Nombre d’impressions qui ont été mesurées pour être visibles en fonction de la configuration de l’emplacement. |
| [!UICONTROL Adobe Advertising Views] | Nombre de vues sur une publicité. Une vue est comptabilisée lorsque la visionneuse lance la vidéo d’Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Nombre d’affichages pour lesquels au moins 25 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Nombre d’affichages pour lesquels au moins 50 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Nombre d’affichages pour lesquels au moins 75 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Nombre de vues pour lesquelles 100 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL AMO ID Instances] | Le nombre de fois où la variable [!UICONTROL AMO ID] est définie. |

## Dimensions d’Adobe Advertising

>[!NOTE]
>
>Toutes les dimensions d’Adobe Advertising dans [!DNL Analytics] sont suivis de &quot;[!DNL (AMO ID)].&quot;

| Dimension | Données d’Adobe Advertising applicables | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | DSP de publicité ou nom du moteur de recherche |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | Nom du compte. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) ou le nom du réseau publicitaire ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | Nom de la campagne. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | Le package ([!DNL DSP]) ou portefeuille ([!DNL Search, Social, & Commerce]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Nom de l’emplacement. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | Nom du groupe publicitaire. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | Mot-clé. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Type de correspondance de recherche. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Mot-clé et type de correspondance. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | Le type d’annonce, tel que `text`, `video`, `display`, ou `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | Type de publicité ([!DNL DSP]) ou titre de la publicité ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | Description de la publicité ([!DNL DSP]) ou du corps de la publicité ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | URL affichée dans la publicité. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | URL de destination de la publicité. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] data | Indique si l’entrée de la page d’entrée était un affichage ou un clic publicitaire. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | Cible du produit d’une publicité avec une liste de produits. |

## Mesures calculées personnalisées utiles pour l’Adobe Advertising

Pensez à créer les mesures suivantes pour vos données d’Adobe Advertising.

* Clics jusqu’à l’instance de page d’entrée ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]) : il s’agit du pourcentage de personnes qui ont cliqué sur la publicité et l’ont affiché sur la page d’entrée.
* Taux mesurable ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Taux d’impression visible ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Coût par affichage ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Coût par clic ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Données en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
