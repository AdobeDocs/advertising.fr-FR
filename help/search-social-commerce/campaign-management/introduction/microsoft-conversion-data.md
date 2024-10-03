---
title: '[!DNL Microsoft Advertising] conversion data'
description: Découvrez les types de données de conversion suivies par  [!DNL Microsoft Advertising] disponibles dans Search, Social et Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: b8a34f3d85947536eb92ee481966f84694250f29
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] données de conversion dans Search, Social et Commerce

Search, Social et Commerce synchronise automatiquement toutes les conversions suivies par vos balises [[!DNL Microsoft Advertising]  de suivi universel des événements (UET)](https://help.ads.microsoft.com/#apex/ads/en/53056) pour les conversions de site web, y compris les conversions d’affichage publicitaire, à des fins de création de rapports et d’optimisation.

Toutes les mesures sont automatiquement disponibles dans les vues de gestion de campagne et les rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio pour l’optimisation des campagnes [!DNL Microsoft Advertising].

## Données de conversion disponibles

Search, Social et Commerce synchronisent les données pour les conversions pour lesquelles l’option &quot;[!DNL Include in 'Conversions']&quot; est activée, extraient les données des 35 derniers jours, puis extraient les modifications apportées aux données quotidiennement par 09:00-10:00 dans le fuseau horaire de l’annonceur. Les données historiques peuvent changer d’un jour à l’autre, car de nouvelles conversions sont suivies pour chaque clic.

Deux mesures pour chaque conversion [[!DNL Microsoft Advertising] suivie ](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (que vous avez configurée dans [!DNL Microsoft Advertising]) sont automatiquement disponibles dans Search, Social et Commerce, à l’aide des noms de conversion configurés dans [!DNL Microsoft Advertising]. Les mesures pour chaque conversion incluent :

* `<conversion-name>` — Valeur de conversion du mot-clé (tel que Achat).

  >[!TIP]
  >
  >Utilisez ce type de mesure de conversion dans l’objectif pour les portefeuilles qui incluent [!DNL Microsoft Advertising] campagnes avec la valeur de conversion maximale et les stratégies d’offre ROAS cible.

* `CT_<conversion-name>` — Nombre (décompte) de conversions, commençant par le préfixe &quot;CT_&quot; (tel que CT_Purchase).

  >[!TIP]
  >
  >Utilisez ce type de mesure de conversion dans l’objectif pour les portfolios qui incluent [!DNL Microsoft Advertising] campagnes avec les stratégies d’offre max. de conversion et Target CPA.

Les données sont disponibles en fonction de l’heure des clics et de l’heure de conversion/transaction à partir de la date d’activation de la fonction pour le compte.

[!DNL Microsoft Advertising] enregistre chaque conversion par [ unité d&#39;offre](/help/search-social-commerce/glossary.md#a-b), appareil et date de clic (et non date de conversion). L’attribution est basée sur le paramètre d’attribution par défaut pour chaque mesure de [!DNL Microsoft Advertising]. L’attribution d’Adobe Advertising n’est pas prise en compte, car les données au niveau de l’événement de clic ne sont pas disponibles.

>[!NOTE]
>
>* Si vous disposez de plusieurs comptes portant le même nom de conversion, il se peut que des noms de conversion en double s’affichent dans Adobe Advertising. Si cela se produit, [modifiez le nom d’affichage](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) pour l’une des mesures en double dans [!UICONTROL Admin] > [!UICONTROL Conversions]. La création de rapports n’est pas exacte lorsque deux mesures différentes portent le même nom.
>* Les données au niveau de l’unité d’offre correspondent aux données du réseau publicitaire au même niveau. Cependant, les données de conversion propres au réseau publicitaire pour des niveaux plus élevés peuvent inclure des conversions supplémentaires qui ne sont pas attribuées aux unités d’offre enfant. Les données de Search, Social et Commerce sont toujours cumulées à partir du niveau de l’unité d’offre. Par exemple, un rapport au niveau de la campagne peut ne pas présenter les mêmes totaux qu’un rapport au niveau de la campagne dans le réseau publicitaire.
>* La variance de données est généralement inférieure après la synchronisation matinale par rapport à plus tard dans la journée, lorsque des conversions supplémentaires n’ont pas encore été synchronisées. Nous vous recommandons de valider les données le matin.
>* Les données ne sont pas disponibles au niveau de l’audience ou de l’emplacement géographique et ne sont donc pas utilisées pour optimiser automatiquement les ajustements des offres RLSA et de l’emplacement.

## Comment comparer les données de conversion dans [!DNL Microsoft Advertising] avec les données dans Search, Social et Commerce

Utilisez les paramètres de rapport suivants pour valider des données comparables.

### Paramètres de rapport à utiliser dans [!DNL Microsoft Advertising]

Générez le rapport pour les actions de conversion sélectionnées par jour et incluez les données pour tous les états des publicités.

### Paramètres des rapports à utiliser dans Search, Social et Commerce

Dans Search, Social et Commerce, utilisez l’option d’affichage ou de rapport pour afficher les conversions en fonction de la date de clic (et non de la date de transaction).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur au-dessus de **[!UICONTROL Basic Reports]**, puis cliquez sur **[!UICONTROL Search Engine Account Report]**.

1. Dans la fenêtre [!UICONTROL Report Settings], spécifiez les paramètres de rapport suivants :

   1. Dans la section **[!UICONTROL Conversions Based]** sur , sélectionnez **[!UICONTROL Click date]**.

   1. Indiquez la même période que celle utilisée pour le rapport [!DNL Microsoft Advertising].

   1. Dans la section **[!UICONTROL Search/Content]**, sélectionnez **[!UICONTROL Search Only]**.

   1. Dans la section **[!UICONTROL Search Engine Hierarchy]** , développez la section [!UICONTROL Microsoft Advertising] et sélectionnez le compte.

   1. Ouvrez l’onglet [!UICONTROL Columns] et ajoutez les mesures [!DNL Microsoft Advertising] à comparer.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes de réseau publicitaire et des campagnes](campaign-implemention-overview.md)
>* [ Surveillez et gérez les performances de vos campagnes réseau d’annonces ](monitor-performance-campaigns.md)
>* [Afficher les mesures de conversion suivies pour un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
