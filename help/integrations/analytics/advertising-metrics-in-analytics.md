---
title: Mesures Adobe Advertising dans Analysis Workspace
description: Mesures Adobe Advertising dans Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Mesures Adobe Advertising dans Analysis Workspace

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

>[!NOTE]
>
>* Adobe Advertising transmet quotidiennement aux [!DNL Analytics] les mesures et dimensions de trafic.
>* [!DNL Analytics] capture les clics publicitaires et les affichages publicitaires d’Adobe Advertising en temps réel.
>* Par [!DNL Search, Social, & Commerce], cette fonctionnalité est prise en charge pour la plupart des réseaux publicitaires et des types de campagne. Pour plus d’informations, reportez-vous à « [Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) » dans le Guide [!DNL Search, Social, & Commerce].

## Mesures de trafic provenant d’Adobe Advertising

Les mesures de trafic Adobe Advertising dans [!DNL Analytics] commencent généralement par « Adobe Advertising », à l’exception de « [!UICONTROL AMO ID Instances] ». Cependant, pour les clients et clientes à long terme qui ont utilisé un événement personnalisé (plutôt qu’un événement réservé) pour créer à l’origine des mesures de clics, de coûts et d’impressions, ces mesures commencent toujours par « AMO ».

| Mesure Trafic | Description |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] ou (certains clients hérités) [!UICONTROL AMO Clicks] | Nombre total de clics Adobe Advertising. |
| [!UICONTROL Adobe Advertising Cost] ou (certains clients hérités) [!UICONTROL AMO Cost] | Dépenses Adobe Advertising dans la devise de la suite de rapports. |
| [!UICONTROL Adobe Advertising Impressions] ou (certains clients hérités) [!UICONTROL AMO Impressions] | Nombre d’impressions Adobe Advertising. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Nombre d’impressions générées pour lesquelles l’instrumentation de visibilité a été initialisée avec succès. Cette valeur est calculée sous la forme (impressions instrumentées - nombre d’impressions non mesurables). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Nombre de minutes pendant lesquelles une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Nombre d’impressions qui ont été déterminées comme non visibles. Cette valeur est calculée comme suit : ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Nombre d’impressions qui ont été mesurées pour être visibles en fonction de la configuration de l’emplacement. |
| [!UICONTROL Adobe Advertising Views] | Nombre de vues sur une publicité. Une vue est comptabilisée lorsque la visionneuse lance la vidéo Adobe Advertising. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Nombre de vues pour lesquelles au moins 25 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Nombre de vues pour lesquelles au moins 50 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Nombre de vues pour lesquelles au moins 75 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Nombre de vues pour lesquelles 100 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL AMO ID Instances] | Nombre de fois où le [!UICONTROL AMO ID] est défini. |

## Dimensions Adobe Advertising

>[!NOTE]
>
>Toutes les dimensions Adobe Advertising dans [!DNL Analytics] sont suivies de « [!DNL (AMO ID)] ».

| Dimension | Données Adobe Advertising applicables | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | Advertising DSP ou le nom du moteur de recherche |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | Nom du compte. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | RTB ([!DNL DSP]) ou le nom du réseau publicitaire ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | Nom de la campagne. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | Nom du package ([!DNL DSP]) ou du portfolio ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] des données | Nom de l’emplacement. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] des données | Nom du groupe publicitaire. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] des données | Le mot-clé . |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] des données | Type de correspondance de recherche. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] des données | Le mot-clé et le type de correspondance. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | Type d’annonce, tel que `text`, `video`, `display` ou `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | Type d’annonce ([!DNL DSP]) ou titre de l’annonce ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | Description de l’annonce ([!DNL DSP]) ou corps de l’annonce ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] des données | URL affichée dans la publicité. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] des données | URL de destination de la publicité. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] et [!DNL Search, Social, & Commerce] des données | Indique si l’entrée de la page de destination était une vue publicitaire ou un clic publicitaire. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] des données | Cible de produit d’une annonce publicitaire dans une liste de produits. |

## Mesures calculées personnalisées utiles pour Adobe Advertising

Envisagez de créer les mesures suivantes pour vos données Adobe Advertising.

* Clics sur l’instance de la page de destination ([!UICONTROL AMO ID Instances]/[!UICONTROL Adobe Advertising Clicks]) : il s’agit du % de personnes qui ont cliqué sur l’annonce et qui ont accédé à la page de destination.
* Taux Mesurable ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Taux d’impression visible ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Coût Par Vue ([!UICONTROL Adobe Advertising Cost]/[!UICONTROL Adobe Advertising Views])
* Coût Par Clic ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Données dans Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
