---
title: Gérez les mesures de conversion d’un annonceur dans DSP.
description: Découvrez comment utiliser les mesures de conversion suivies par Adobe Advertising pour un annonceur DSP.
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Gérer les mesures de conversion d’un annonceur

Les mesures de conversion d’un annonceur sont utilisées dans Adobe Advertising :

* Dans Advertising DSP, vous pouvez inclure des mesures de conversion dans les vues de gestion de campagne, les objectifs personnalisés et les rapports personnalisés. Vous pouvez également utiliser les mesures de conversion d’un annonceur pour créer des [objectifs personnalisés](/help/dsp/admin/custom-objectives-manage.md), qui sont utilisés pour optimiser les packages.

* (Annonceurs avec Advertising Search, Social et Commerce) Dans Search, Social et Commerce, les données des mesures de conversion peuvent être affichées sous forme de colonnes dans les vues de gestion de campagnes, de portfolios et d’objectifs, ainsi que dans les rapports. Les utilisateurs disposant de droits d’accès suffisants peuvent également utiliser les mesures de conversion pour créer des objectifs utilisés pour optimiser les portfolios.

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

Les types de mesures suivis pour les utilisateurs de DSP sont les suivants :

* Mesures de conversion suivies par Adobe Advertising pour un annonceur.

* [Mesures d’engagement du site et de conversion synchronisées à partir d’Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Événements de site synchronisés à partir d’Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Conversions à partir de flux personnalisés.

Dans la liste des mesures de conversion disponibles, chaque utilisateur ayant accès aux données de l’annonceur peut personnaliser les mesures qui s’affichent pour les vues et les rapports de gestion, y compris des mesures spécifiques, qu’il choisit ou non. Vous pouvez utiliser un nom de mesure tel qu’il est orthographié dans les données récupérées ou modifier le nom affiché dans les en-têtes de colonne pour en faciliter la lecture.

>[!IMPORTANT]
>
>Par défaut, aucune mesure de conversion d’un annonceur n’est disponible pour être incluse dans les vues de gestion de campagne, les objectifs personnalisés et les rapports personnalisés. Pour rendre une mesure de conversion disponible, vous devez la rendre explicitement disponible.

>[!TIP]
>
>Une fois que l’annonceur (ou le réseau publicitaire) cesse de collecter une mesure de conversion, [masquez-la dans les vues et les rapports de gestion](#conversion-metrics-change-available) à moins que vous ne souhaitiez l’utiliser pour afficher les données historiques.

## Affichage des mesures de conversion suivies pour un annonceur

* Dans le menu principal, cliquez sur **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

Toutes les mesures de conversion qui ont été collectées pour l’annonceur, ainsi que tous les noms d’affichage différents qui leur ont été attribués, sont répertoriés. Chaque ligne de mesure inclut la source de la mesure.

## Modification du nom d’affichage d’une mesure de conversion

Par exemple, si vous collectez des données d’enregistrement à l’aide d’une mesure de conversion nommée *reg*, vous pouvez éventuellement modifier le nom d’affichage pour qu’il s’affiche sous la forme « Enregistrements ».

Vous ne pouvez pas supprimer un nom d’affichage existant.

1. Dans le menu principal, cliquez sur **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

1. Placez le curseur sur la ligne et cliquez sur **[!UICONTROL Edit Display Name]**.

1. Saisissez le nom à afficher, puis cliquez sur **[!UICONTROL Save]**.

   Les noms d&#39;affichage doivent être uniques et ne peuvent pas contenir les caractères spéciaux suivants : `\"<'>&`

## Modifier les mesures de conversion disponibles dans les vues de gestion de campagne, les objectifs personnalisés et les rapports personnalisés {#change-the-conversion-metrics-available-in-ui}

1. Dans le menu principal, cliquez sur **[!UICONTROL Settings]>[!UICONTROL Conversions]**.

   Toutes les mesures de conversion qui ont été collectées pour l’annonceur, ainsi que tous les noms différents qui ont été spécifiés pour l’affichage, sont répertoriés.

1. (Facultatif) Filtrez la liste :

   1. Au-dessus de la liste, cliquez sur ![Filtrer](/help/dsp/assets/filter.png "Filtrer").

   1. Spécifiez les filtres, puis cliquez sur **[!DNL Apply]**.

      Vous pouvez filtrer les mesures en fonction de l’identifiant du client AMO, selon que les mesures sont visibles ou masquées dans l’interface utilisateur, et selon la source de données.

1. Modifiez les mesures de conversion disponibles pour les vues et les rapports de gestion :

   * Pour afficher une mesure, maintenez le curseur sur la ligne et cliquez sur **[!UICONTROL Show in UI and Reports]**.

   * Pour masquer une mesure, maintenez le curseur sur la ligne et cliquez sur **[!UICONTROL Hide in UI and Reports]**.

>[!MORELIKETHIS]
>
>* [Gérer les vues de données de votre campagne](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Gérer les objectifs personnalisés](/help/dsp/admin/custom-objectives-manage.md)
