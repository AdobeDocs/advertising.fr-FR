---
title: '[!DNL Microsoft Advertising] données de conversion'
description: Découvrez les types de données de conversion suivies par [!DNL Microsoft Advertising] disponibles dans Search, Social et Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
TQID: 'https://experienceleague.adobe.com/ZK-uDqw0sThnMzX6bdR-d33gh-AlLTaytJr1fS7pdgs'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
    internal-label: Conversions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%
---
# [!DNL Microsoft Advertising] données de conversion dans Search, Social et Commerce

Search, Social et Commerce synchronise automatiquement toutes les conversions suivies par vos [[!DNL Microsoft Advertising] balises de suivi d’événement universel (UET)](https://help.ads.microsoft.com/#apex/ads/en/53056) pour les conversions de sites web, y compris les conversions d’affichage publicitaire, à des fins de création de rapports et d’optimisation.

Toutes les mesures sont automatiquement disponibles dans vos vues de gestion de campagne et rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio pour l’optimisation des campagnes [!DNL Microsoft Advertising].

## Données de conversion disponibles

Search, Social et Commerce synchronise les données pour les conversions pour lesquelles l’option « [!DNL Include in 'Conversions'] » est activée, en extrayant les données des 35 derniers jours, puis en extrayant les modifications quotidiennes de 09:00-10:00 dans le fuseau horaire de l’annonceur. Les données historiques peuvent changer d’un jour à l’autre à mesure que de nouvelles conversions sont suivies pour chaque clic.

Deux mesures pour chaque conversion [[!DNL Microsoft Advertising] suivie](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (que vous configurez dans [!DNL Microsoft Advertising]) sont automatiquement disponibles dans Search, Social et Commerce, en utilisant les noms de conversion configurés dans [!DNL Microsoft Advertising]. Les mesures de chaque conversion sont les suivantes :

* `<conversion-name>` — Valeur de conversion du mot-clé (par exemple Achat).

  >[!TIP]
  >
  >Utilisez ce type de mesure de conversion dans l’objectif pour les portfolios qui incluent [!DNL Microsoft Advertising] campagnes avec la valeur de conversion maximale et les stratégies d’enchères de retour sur dépenses publicitaires cible.

* `CT_<conversion-name>` - Nombre (count) de conversions commençant par le préfixe « CT_ » (tel que CT_Purchase).

  >[!TIP]
  >
  >Utilisez ce type de mesure de conversion dans l’objectif pour les portfolios qui incluent des campagnes [!DNL Microsoft Advertising] avec les stratégies d’enchères Max Conversions et CPA cible.

Les données sont disponibles en fonction de l’heure de clic et de l’heure de conversion/transaction à partir de la date à laquelle la fonctionnalité est activée pour le compte.

[!DNL Microsoft Advertising] enregistre chaque conversion par [enchère](/help/search-social-commerce/glossary.md#a-b), appareil et date de clic (et non date de conversion). L’attribution est basée sur le paramètre d’attribution par défaut pour chaque mesure dans [!DNL Microsoft Advertising] ; l’attribution Adobe Advertising n’est pas prise en compte, car les données au niveau de l’événement clic ne sont pas disponibles.

>[!NOTE]
>
>* Si plusieurs comptes portent les mêmes noms de conversion, il se peut que des noms de conversion en double s’affichent dans Adobe Advertising. Si cela se produit, [modifiez le nom d’affichage](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#change-the-display-name-for-a-conversion-metric) de l’une des mesures en double dans [!UICONTROL Goals] > [!UICONTROL Conversions]. Le compte rendu des performances n’est pas précis lorsque deux mesures différentes portent le même nom.
>* Les données au niveau de l’unité d’offre correspondent aux données du réseau publicitaire au même niveau. Cependant, les données de conversion du réseau publicitaire pour les niveaux supérieurs peuvent inclure des conversions supplémentaires qui ne sont pas attribuées aux unités d’enchères enfants. Les données dans Search, Social et Commerce sont toujours cumulées à partir du niveau d’unité d’enchère. Par exemple, un rapport au niveau de la campagne peut ne pas avoir les mêmes totaux qu’un rapport au niveau de la campagne dans le réseau publicitaire.
>* La variance des données est généralement inférieure après la synchronisation du matin par rapport à plus tard dans la journée, lorsque des conversions supplémentaires n’ont pas encore été synchronisées. Nous vous recommandons de valider les données le matin.
>* Les données ne sont pas disponibles au niveau de l’audience ou de l’emplacement géographique et ne sont donc pas utilisées pour optimiser automatiquement le RLSA et les ajustements d’enchères d’emplacement.

## Comment comparer les données de conversion dans [!DNL Microsoft Advertising] avec les données dans Search, Social et Commerce

Utilisez les paramètres de rapport suivants pour valider des données comparables.

### Paramètres des rapports à utiliser dans [!DNL Microsoft Advertising]

Générez le rapport pour les actions de conversion sélectionnées par jour et incluez les données pour tous les statuts de publicité.

### Paramètres des rapports à utiliser dans Search, Social et Commerce

Dans Search, Social et Commerce, utilisez l’option d’affichage ou de rapport pour afficher les conversions en fonction de la date de clic (et non de la date de transaction).

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Cliquez sur **[!UICONTROL Create Report]**, cliquez sur **[!UICONTROL Basic Reports]** dans le panneau de gauche, puis sélectionnez **[!UICONTROL Search Engine Account Report]**. Cliquez sur **[!UICONTROL Proceed]**.

1. Dans la fenêtre [!UICONTROL Create Report], ouvrez l’onglet **[!UICONTROL Basic Settings]** et spécifiez les [paramètres de rapport](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md) suivants :

   1. Définir **[!UICONTROL Data Aggregation]** sur **[!UICONTROL Daily]**.

   1. Définir **[!UICONTROL Conversions Based on]** sur **[!UICONTROL Click date]**.

   1. Spécifiez la même période que celle utilisée pour le rapport [!DNL Microsoft Advertising].

   1. Définir **[!UICONTROL Search/Content]** sur **[!UICONTROL Search Only]**.

   1. Si **[!UICONTROL Filter By]** est affiché, sélectionnez **[!UICONTROL Search engine]**.

   1. Dans **[!UICONTROL Search Engine Hierarchy]**, développez [!DNL Microsoft Advertising] et cochez la case en regard du compte que vous souhaitez comparer. Cliquez sur **[!UICONTROL Add selected items]** pour déplacer le compte vers **[!UICONTROL Selected Filters]**.

1. Ouvrez l’onglet **[!UICONTROL Columns]** et ajoutez les mesures [!DNL Microsoft Advertising] que vous souhaitez comparer.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Configurer des comptes et des campagnes de réseau publicitaire](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [À propos de la gestion des campagnes et des portfolios](/help/search-social-commerce/manage/manage-about.md)
>* [Afficher les mesures de conversion suivies pour un annonceur](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#view-the-conversion-metrics-tracked-for-an-advertiser)
