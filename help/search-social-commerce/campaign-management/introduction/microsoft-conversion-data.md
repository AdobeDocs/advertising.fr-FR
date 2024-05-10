---
title: '''[!DNL Microsoft Advertising] données de conversion"'
description: En savoir plus sur les types [!DNL Microsoft Advertising]Données de conversion suivies disponibles dans Search, Social et Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] données de conversion dans Search, Social et Commerce

Search, Social et Commerce synchronise automatiquement toutes les conversions suivies par vos [[!DNL Microsoft Advertising] balises de suivi d’événement universel (UET)](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) pour les conversions de site web, y compris les conversions d’affichage publicitaire, pour la création de rapports et l’optimisation.

Toutes les mesures sont automatiquement disponibles dans les vues de gestion de campagne et les rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio pour optimiser les [!DNL Microsoft Advertising] campagnes.

## Données de conversion disponibles

Recherche, Social et Commerce synchronisent les données pour les conversions pour lesquelles le paramètre[!DNL Include in 'Conversions']&quot; est activée, extrayant les données des 35 derniers jours, puis extrayant les modifications apportées aux données quotidiennement d’ici 2009:00-10:00 dans le fuseau horaire de l&#39;annonceur. Les données historiques peuvent changer d’un jour à l’autre, car de nouvelles conversions sont suivies pour chaque clic.

Deux mesures pour chaque [[!DNL Microsoft Advertising]conversion suivie](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (que vous configurez dans [!DNL Microsoft Advertising]) sont automatiquement disponibles dans Search, Social et Commerce, à l’aide des noms de conversion configurés dans [!DNL Microsoft Advertising]. Les mesures pour chaque conversion incluent :

* `<conversion-name>` — Valeur de conversion du mot-clé (achat, par exemple).

  >[!TIP]
  >
  >Utilisez ce type de mesure de conversion dans l’objectif pour les portefeuilles qui incluent [!DNL Microsoft Advertising] campagnes avec la valeur de conversion maximale et les stratégies d’offre ROAS de la cible.

* `CT_<conversion-name>` — Nombre (décompte) de conversions, commençant par le préfixe &quot;CT_&quot; (tel que CT_Purchase).

  >[!TIP]
  >
  >Utilisez ce type de mesure de conversion dans l’objectif pour les portefeuilles qui incluent [!DNL Microsoft Advertising] des campagnes avec les stratégies d’offre max. de conversions et Target CPA.

Les données sont disponibles en fonction de l’heure des clics et de l’heure de conversion/transaction à partir de la date d’activation de la fonction pour le compte.

[!DNL Microsoft Advertising] enregistre chaque conversion par [enchères unit](/help/search-social-commerce/glossary.md#a-b), appareil et date de clic (et non la date de conversion). L’attribution est basée sur le paramètre d’attribution par défaut pour chaque mesure dans [!DNL Microsoft Advertising]; l’attribution de l’Adobe Advertising n’est pas prise en compte, car les données au niveau de l’événement de clic ne sont pas disponibles.

>[!NOTE]
>
>* Si vous disposez de plusieurs comptes portant le même nom de conversion, il se peut que des noms de conversion en double s’affichent dans Adobe Advertising. Si cela se produit, [modifier le nom d’affichage ;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) pour l’une des mesures en double dans [!UICONTROL Admin] > [!UICONTROL Conversions]. La création de rapports n’est pas exacte lorsque deux mesures différentes portent le même nom.
>* Les données au niveau de l’unité d’offre correspondent aux données du réseau publicitaire au même niveau. Cependant, les données de conversion propres au réseau publicitaire pour des niveaux plus élevés peuvent inclure des conversions supplémentaires qui ne sont pas attribuées aux unités d’offre enfant. Les données de Search, Social et Commerce sont toujours cumulées à partir du niveau de l’unité d’offre. Par exemple, un rapport au niveau de la campagne peut ne pas présenter les mêmes totaux qu’un rapport au niveau de la campagne dans le réseau publicitaire.
>* La variance de données est généralement inférieure après la synchronisation matinale par rapport à plus tard dans la journée, lorsque des conversions supplémentaires n’ont pas encore été synchronisées. Nous vous recommandons de valider les données le matin.
>* Les données ne sont pas disponibles au niveau de l’audience ou de l’emplacement géographique et ne sont donc pas utilisées pour optimiser automatiquement les ajustements des offres RLSA et de l’emplacement.

## Comment comparer les données de conversion dans [!DNL Microsoft Advertising] avec des données dans Search, Social et Commerce

Utilisez les paramètres de rapport suivants pour valider des données comparables.

### Paramètres des rapports à utiliser dans [!DNL Microsoft Advertising]

Générez le rapport pour les actions de conversion sélectionnées par jour et incluez les données pour tous les états des publicités.

### Paramètres des rapports à utiliser dans Search, Social et Commerce

Dans Search, Social et Commerce, utilisez l’option d’affichage ou de rapport pour afficher les conversions en fonction de la date de clic (et non de la date de transaction).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur sur **[!UICONTROL Basic Reports]**, puis cliquez sur **[!UICONTROL Search Engine Account Report]**.

1. Dans le [!UICONTROL Report Settings] définissez les paramètres de rapport suivants :

   1. Dans le **[!UICONTROL Conversions Based]** sur la section , sélectionnez **[!UICONTROL Click date]**.

   1. Indiquez la même période que celle utilisée pour la variable [!DNL Microsoft Advertising] rapport.

   1. Dans le **[!UICONTROL Search/Content]** , sélectionnez **[!UICONTROL Search Only]**.

   1. Dans le **[!UICONTROL Search Engine Hierarchy]** , développez la section [!UICONTROL Microsoft Advertising] et sélectionnez le compte.

   1. Ouvrez le [!UICONTROL Columns] et ajoutez le [!DNL Microsoft Advertising] mesures à comparer.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes et campagnes de réseau publicitaire](campaign-implemention-overview.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaires](monitor-performance-campaigns.md)
>* [Afficher les mesures de conversion suivies pour un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
