---
title: '''[!DNL Microsoft Advertising] données de conversion"'
description: En savoir plus sur les types de [!DNL Microsoft Advertising]Données de conversion suivies disponibles dans Search, Social et Commerce.
source-git-commit: 355796d65e5de0dba9111e77fc594a3e50e6ec5e
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] données de conversion dans Search, Social et Commerce

Search, Social et Commerce synchronise automatiquement toutes les conversions suivies par vos [Balises de suivi d’événement universel (UET) de Microsoft Advertising](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) pour les conversions de site web, y compris les conversions d’affichage publicitaire, pour la création de rapports et l’optimisation.

Toutes les mesures sont automatiquement disponibles dans les vues de gestion de campagne et les rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio pour l’optimisation des campagnes Microsoft Advertising.

## Données de conversion disponibles

Search, Social et Commerce synchronise les données pour les conversions pour lesquelles le[!DNL Include in 'Conversions']&quot; est activée, extrayant les données des 35 derniers jours, puis extrayant les modifications apportées aux données quotidiennement d’ici 2009.:00-10:00 dans le fuseau horaire de l&#39;annonceur. Les données historiques peuvent changer d’un jour à l’autre, car de nouvelles conversions sont suivies pour chaque clic.

Deux propriétés de transaction pour chacune [[!DNL Microsoft Advertising]conversion trackée](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (que vous configurez dans [!DNL Microsoft Advertising]) sont automatiquement disponibles dans Search, Social et Commerce, à l’aide des noms de conversion configurés dans [!DNL Microsoft Advertising]. Les propriétés de transaction pour chaque conversion incluent :

* `<conversion-name>` — Valeur de conversion du mot-clé (achat, par exemple).

  >[!TIP]
  >
  >Utilisez ce type de propriété dans l’objectif pour les portefeuilles qui incluent [!DNL Microsoft Advertising] campagnes avec la valeur de conversion maximale et les stratégies d’offre ROAS de la cible.

* `CT_<conversion-name>` — Nombre (décompte) de conversions, commençant par le préfixe &quot;CT_&quot; (tel que CT_Purchase).

  >[!TIP]
  >
  >Utilisez ce type de propriété dans l’objectif pour les portefeuilles qui incluent [!DNL Microsoft Advertising] des campagnes avec les stratégies d’offres max. et Target CPA.

Les données sont disponibles en fonction de l’heure des clics et de l’heure de conversion/transaction à partir de la date d’activation de la fonction pour le compte.

<!-- verify below/ if equivalent

[!DNL Microsoft Advertising] records each conversion by [bid unit](/help/search-social-commerce/glossary.md#a-b), device, and click date (not conversion date). Attribution is based on the default attribution setting for each metric in [!DNL Microsoft Advertising]; Adobe Advertising attribution isn't factored in because click event-level data isn't available.
-->

>[!NOTE]
>
>* Si vous disposez de plusieurs comptes portant le même nom de conversion, il se peut que des noms de conversion en double apparaissent dans Adobe Advertising. Si cela se produit, [modifier le nom d’affichage ;](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) pour l’une des mesures en double dans [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. La création de rapports n’est pas exacte lorsque deux mesures différentes portent le même nom.
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

   1. Ouvrez le [!UICONTROL Columns] et ajoutez le [!DNL Microsoft Advertising] mesures que vous souhaitez comparer.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes et campagnes de réseau publicitaire](campaign-implemention-overview.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaires](monitor-performance-campaigns.md)
>* [Afficher les propriétés de transaction suivies pour un annonceur](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.html?lang=en)