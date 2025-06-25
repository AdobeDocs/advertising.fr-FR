---
title: '[!DNL Microsoft Advertising] des données de conversion'
description: Découvrez les types de données de conversion suivies par  [!DNL Microsoft Advertising] disponibles dans Search, Social et Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] des données de conversion dans Search, Social et Commerce

Search, Social et Commerce synchronise automatiquement toutes les conversions suivies par vos balises [[!DNL Microsoft Advertising] suivi d’événement universel (UET)](https://help.ads.microsoft.com/#apex/ads/en/53056) pour les conversions de sites web, y compris les conversions d’affichage publicitaire, à des fins de création de rapports et d’optimisation.

Toutes les mesures sont automatiquement disponibles dans les vues de gestion de campagne et les rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio pour l’optimisation des campagnes [!DNL Microsoft Advertising].

## Données de conversion disponibles

Search, Social et Commerce synchronise les données pour les conversions pour lesquelles l’option « [!DNL Include in 'Conversions'] » est activée, en extrayant les données des 35 derniers jours, puis en extrayant les modifications quotidiennes jusqu’à 09 :00-10: dans le fuseau horaire de l’annonceur. Les données historiques peuvent changer d’un jour à l’autre à mesure que de nouvelles conversions sont suivies pour chaque clic.

Deux mesures pour chaque conversion [[!DNL Microsoft Advertising] (que vous configurez dans [!DNL Microsoft Advertising]) sont automatiquement disponibles dans Search, Social et Commerce](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) en utilisant les noms de conversion configurés dans [!DNL Microsoft Advertising]. Les mesures de chaque conversion sont les suivantes :

* `<conversion-name>` : valeur de conversion du mot-clé (par exemple Achat).

  >[!TIP]
  >
  >Utilisez ce type de mesure de conversion dans l’objectif pour les portfolios qui incluent des campagnes [!DNL Microsoft Advertising] avec les stratégies d’enchères Valeur de conversion maximale et Retour sur dépenses publicitaires cible.

* `CT_<conversion-name>` — Nombre (count) de conversions commençant par le préfixe « CT_ » (tel que CT_Purchase).

  >[!TIP]
  >
  >Utilisez ce type de mesure de conversion dans l’objectif pour les portfolios qui incluent des campagnes [!DNL Microsoft Advertising] avec les stratégies d’enchères Max Conversions et CPA cible.

Les données sont disponibles en fonction de l’heure de clic et de l’heure de conversion/transaction à partir de la date à laquelle la fonctionnalité est activée pour le compte.

[!DNL Microsoft Advertising] enregistre chaque conversion par [unité d’offre](/help/search-social-commerce/glossary.md#a-b), appareil et date de clic (et non par date de conversion). L’attribution est basée sur le paramètre d’attribution par défaut pour chaque mesure dans [!DNL Microsoft Advertising] ; l’attribution Adobe Advertising n’est pas prise en compte, car les données au niveau de l’événement clic ne sont pas disponibles.

>[!NOTE]
>
>* Si plusieurs comptes portent les mêmes noms de conversion, il se peut que des noms de conversion en double s’affichent dans Adobe Advertising. Si cela se produit, [modifiez le nom d’affichage](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) pour l’une des mesures en double dans [!UICONTROL Admin] > [!UICONTROL Conversions]. Le compte rendu des performances n’est pas précis lorsque deux mesures différentes portent le même nom.
>* Les données au niveau de l’unité d’offre correspondent aux données du réseau publicitaire au même niveau. Cependant, les données de conversion du réseau publicitaire pour les niveaux supérieurs peuvent inclure des conversions supplémentaires qui ne sont pas attribuées aux unités d’enchères enfants. Les données dans Search, Social et Commerce sont toujours cumulées à partir du niveau d’unité d’enchère. Par exemple, un rapport au niveau de la campagne peut ne pas avoir les mêmes totaux qu’un rapport au niveau de la campagne dans le réseau publicitaire.
>* La variance des données est généralement inférieure après la synchronisation du matin par rapport à plus tard dans la journée, lorsque des conversions supplémentaires n’ont pas encore été synchronisées. Nous vous recommandons de valider les données le matin.
>* Les données ne sont pas disponibles au niveau de l’audience ou de l’emplacement géographique et ne sont donc pas utilisées pour optimiser automatiquement le RLSA et les ajustements d’enchères d’emplacement.

## Comment comparer les données de conversion dans [!DNL Microsoft Advertising] avec les données dans Search, Social et Commerce

Utilisez les paramètres de rapport suivants pour valider des données comparables.

### Paramètres des rapports à utiliser dans [!DNL Microsoft Advertising]

Générez le rapport pour les actions de conversion sélectionnées par jour et incluez les données pour tous les statuts de publicité.

### Paramètres des rapports à utiliser dans Search, Social et Commerce

Dans Search, Social et Commerce, utilisez l’option d’affichage ou de rapport pour afficher les conversions en fonction de la date de clic (et non de la date de transaction).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur sur **[!UICONTROL Basic Reports]**, puis cliquez sur **[!UICONTROL Search Engine Account Report]**.

1. Dans la fenêtre [!UICONTROL Report Settings] , spécifiez les paramètres de rapport suivants :

   1. Dans la section **[!UICONTROL Conversions Based]** sur , sélectionnez **[!UICONTROL Click date]**.

   1. Spécifiez la même période que celle utilisée pour le rapport [!DNL Microsoft Advertising].

   1. Dans la section **[!UICONTROL Search/Content]**, sélectionnez **[!UICONTROL Search Only]**.

   1. Dans la section **[!UICONTROL Search Engine Hierarchy]** , développez la section [!UICONTROL Microsoft Advertising] et sélectionnez le compte.

   1. Ouvrez l’onglet [!UICONTROL Columns] et ajoutez les mesures [!DNL Microsoft Advertising] à comparer.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes et des campagnes de réseau publicitaire](campaign-implemention-overview.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaire](monitor-performance-campaigns.md)
>* [Affichage des mesures de conversion suivies pour un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
