---
title: '[!DNL Google Ads] des données de conversion'
description: Découvrez les types de données  [!DNL Google Ads] conversion suivies par dans Search, Social et Commerce.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# [!DNL Google Ads] des données de conversion dans Search, Social et Commerce

Search, Social et Commerce synchronise automatiquement les données de conversion suivies par le [!DNL Google Ads] pour toutes vos campagnes sur les réseaux de recherche et d’achat [!DNL Google Ads] dans Search, Social et Commerce à des fins de création de rapports et d’optimisation.

Toutes les mesures sont automatiquement disponibles dans les vues de gestion de campagne et les rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio à des fins d’optimisation.

## Données de conversion disponibles

Search, Social et Commerce synchronise les données pour les conversions pour lesquelles l’option « [!DNL Include in 'Conversions'] » est activée, en extrayant les données des 35 derniers jours, puis en extrayant les modifications quotidiennes jusqu’à 09 :00-10: dans le fuseau horaire de l’annonceur. Les données historiques peuvent changer d’un jour à l’autre à mesure que de nouvelles conversions sont suivies pour chaque clic.

Jusqu’à trois mesures pour chaque conversion [[!DNL Google Ads] (que vous configurez dans [!DNL Google Ads]) sont automatiquement disponibles dans Search, Social et Commerce](https://support.google.com/google-ads/answer/4677036) en utilisant les noms de conversion configurés dans [!DNL Google Ads]. Les mesures de chaque conversion sont les suivantes :

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (Lorsque vous le suivez) Valeur de conversion du mot-clé, commençant par le préfixe « GGL » (tel que GGL Purchase).

* `GGL_CT*` — Nombre (nombre) de conversions commençant par le préfixe « GGL_CT » (tel que GGL_CT_Purchase).

* `GGL_XD_CT*` — (Si disponible pour le type de conversion, lorsque vous les suivez) Nombre (nombre) de conversions entre appareils, telles que mesurées par Google, commençant par le préfixe « GGL_XD_CT_ » (tel que GGL_XD_CT_Purchase).

[!DNL Google Ads] enregistre chaque conversion par [unité d’offre](/help/search-social-commerce/glossary.md#a-b), appareil et date de clic (et non par date de conversion). L’attribution est basée sur le paramètre d’attribution par défaut pour chaque mesure dans [!DNL Google Ads] ; l’attribution Adobe Advertising n’est pas prise en compte, car les données au niveau de l’événement clic ne sont pas disponibles.

>[!NOTE]
>
>* Si plusieurs comptes portent les mêmes noms de conversion, il se peut que des noms de conversion en double s’affichent dans Adobe Advertising. Si cela se produit, [modifiez le nom d’affichage](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) pour l’une des mesures en double dans [!UICONTROL Admin] > [!UICONTROL Conversions]. Le compte rendu des performances n’est pas précis lorsque deux mesures différentes portent le même nom.
>* Les données au niveau de l&#39;unité d&#39;offre correspondent aux données dans [!DNL Google Ads] au même niveau. Toutefois, les données de conversion des [!DNL Google Ads] pour les niveaux supérieurs peuvent inclure des conversions supplémentaires qui ne sont pas attribuées aux unités d’enchères enfants. Les données dans Search, Social et Commerce sont toujours cumulées à partir du niveau d’unité d’enchères. Par exemple, un rapport au niveau de la campagne peut ne pas avoir les mêmes totaux qu’un rapport au niveau de la campagne dans Google Ads.
>* La variance des données est généralement inférieure après la synchronisation du matin par rapport à plus tard dans la journée, lorsque des conversions supplémentaires n’ont pas encore été synchronisées. Nous vous recommandons de valider les données le matin.
>* Les données de conversion ne sont pas disponibles pour les annonces [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App] et [!DNL YouTube]. Filtrez ces types d’annonces lorsque vous comparez les données dans [!DNL Google Ads] aux données dans Search, Social et Commerce.
>* Les données relatives aux conversions [!DNL Google Ads] ne sont pas disponibles au niveau de l’audience ou de l’emplacement géographique et ne sont donc pas utilisées pour optimiser automatiquement le RLSA et les ajustements d’offres d’emplacement.

## Comment comparer les données de conversion dans [!DNL Google Ads] avec les données dans Search, Social et Commerce

Si vous comparez les données de Search, Social et Commerce à celles de [!DNL Google Ads], utilisez l’option d’affichage ou de rapport pour afficher les conversions en fonction de la date de clic (et non de la date de transaction).

Utilisez les paramètres de rapport suivants pour valider des données comparables.

### Paramètres des rapports à utiliser dans [!DNL Google Ads]

Générez le rapport pour les actions de conversion sélectionnées par jour et incluez les données pour tous les statuts de publicité.

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### Paramètres des rapports à utiliser dans Search, Social et Commerce

Dans Search, Social et Commerce, utilisez l’option d’affichage ou de rapport pour afficher les conversions en fonction de la date de clic (et non de la date de transaction).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur sur **[!UICONTROL Basic Reports]**, puis cliquez sur **[!UICONTROL Search Engine Account Report]**.

1. Dans la fenêtre [!UICONTROL Report Settings] , spécifiez les paramètres de rapport suivants :

   1. Dans la section **[!UICONTROL Conversions Based]** sur , sélectionnez **[!UICONTROL Click date]**.

   1. Spécifiez la même période que celle utilisée pour le rapport [!DNL Google Ads].

   1. Dans la section **[!UICONTROL Search/Content]**, sélectionnez **[!UICONTROL Search Only]**.

   1. Dans la section **[!UICONTROL Search Engine Hierarchy]** , développez la section [!UICONTROL Google Adwords] et sélectionnez le compte.

   1. Ouvrez l’onglet [!UICONTROL Columns] et ajoutez les mesures [!DNL Google Ads] (en commençant par « GGL ») que vous souhaitez comparer.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes et des campagnes de réseau publicitaire](campaign-implemention-overview.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaire](monitor-performance-campaigns.md)
>* [Affichage des mesures de conversion suivies pour un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Créer une balise de conversion pour  [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
>* [Chargement des données de conversion hors ligne pour les conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
