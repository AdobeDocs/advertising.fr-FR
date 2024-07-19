---
title: '[!DNL Google Ads] conversion data'
description: Découvrez les types de données de conversion suivies par  [!DNL Google Ads] disponibles dans Search, Social et Commerce.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# [!DNL Google Ads] données de conversion dans Search, Social et Commerce

Search, Social et Commerce synchronisent automatiquement les données de conversion suivies par [!DNL Google Ads] pour toutes vos campagnes sur les réseaux de recherche et d’achat [!DNL Google Ads] dans Search, Social et Commerce pour la création de rapports et l’optimisation.

Toutes les mesures sont automatiquement disponibles dans les vues de gestion de campagne et les rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio à des fins d’optimisation.

## Données de conversion disponibles

Search, Social et Commerce synchronisent les données pour les conversions pour lesquelles l’option &quot;[!DNL Include in 'Conversions']&quot; est activée, extraient les données des 35 derniers jours, puis extraient les modifications apportées aux données quotidiennement par 09:00-10:00 dans le fuseau horaire de l’annonceur. Les données historiques peuvent changer d’un jour à l’autre, car de nouvelles conversions sont suivies pour chaque clic.

Jusqu’à trois mesures pour chaque conversion [[!DNL Google Ads] suivie ](https://support.google.com/google-ads/answer/4677036) (que vous configurez dans [!DNL Google Ads]) sont automatiquement disponibles dans Search, Social et Commerce, à l’aide des noms de conversion configurés dans [!DNL Google Ads]. Les mesures pour chaque conversion incluent :

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (Lorsque vous en effectuez le suivi) La valeur de conversion du mot-clé, commençant par le préfixe &quot;GGL&quot; (tel que Achat GGL).

* `GGL_CT*` — Nombre (décompte) de conversions, commençant par le préfixe &quot;GGL_CT&quot; (tel que GGL_CT_Purchase).

* `GGL_XD_CT*` — (Lorsque disponible pour le type de conversion, lorsque vous en effectuez le suivi) Le nombre (nombre) de conversions entre appareils, tel que mesuré par Google, en commençant par le préfixe &quot;GGL_XD_CT_&quot; (tel que GGL_XD_CT_Purchase).

[!DNL Google Ads] enregistre chaque conversion par [ unité d&#39;offre](/help/search-social-commerce/glossary.md#a-b), appareil et date de clic (et non date de conversion). L’attribution est basée sur le paramètre d’attribution par défaut pour chaque mesure de [!DNL Google Ads]. L’attribution d’Adobe Advertising n’est pas prise en compte, car les données au niveau de l’événement de clic ne sont pas disponibles.

>[!NOTE]
>
>* Si vous disposez de plusieurs comptes portant le même nom de conversion, il se peut que des noms de conversion en double s’affichent dans Adobe Advertising. Si cela se produit, [modifiez le nom d’affichage](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) pour l’une des mesures en double dans [!UICONTROL Admin] > [!UICONTROL Conversions]. La création de rapports n’est pas exacte lorsque deux mesures différentes portent le même nom.
>* Les données au niveau de l’unité d’offre correspondent aux données de [!DNL Google Ads] au même niveau. Cependant, les données de conversion propres à [!DNL Google Ads] pour les niveaux supérieurs peuvent inclure des conversions supplémentaires qui ne sont pas attribuées aux unités d’offre enfants. Les données de Search, Social et Commerce sont toujours cumulées à partir du niveau de l’unité d’offre. Par exemple, un rapport au niveau de la campagne peut ne pas présenter les mêmes totaux qu’un rapport au niveau de la campagne dans Google Ads.
>* La variance de données est généralement inférieure après la synchronisation matinale par rapport à plus tard dans la journée, lorsque des conversions supplémentaires n’ont pas encore été synchronisées. Nous vous recommandons de valider les données le matin.
>* Les données de conversion ne sont pas disponibles pour les [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App] et les [!DNL YouTube] publicités. Filtrez ces types d’annonces lorsque vous comparez les données de [!DNL Google Ads] avec celles de Search, Social et Commerce.
>* Les données pour les conversions [!DNL Google Ads] ne sont pas disponibles au niveau de l’audience ou de l’emplacement géographique et ne sont donc pas utilisées pour optimiser automatiquement les ajustements des offres RLSA et de l’emplacement.

## Comment comparer les données de conversion dans [!DNL Google Ads] avec les données dans Search, Social et Commerce

Si vous comparez les données de Search, Social et Commerce à celles de [!DNL Google Ads], utilisez l’option d’affichage ou de rapport pour afficher les conversions en fonction de la date de clic (et non de la date de transaction).

Utilisez les paramètres de rapport suivants pour valider des données comparables.

### Paramètres de rapport à utiliser dans [!DNL Google Ads]

Générez le rapport pour les actions de conversion sélectionnées par jour et incluez les données pour tous les états des publicités.

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

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur au-dessus de **[!UICONTROL Basic Reports]**, puis cliquez sur **[!UICONTROL Search Engine Account Report]**.

1. Dans la fenêtre [!UICONTROL Report Settings], spécifiez les paramètres de rapport suivants :

   1. Dans la section **[!UICONTROL Conversions Based]** sur , sélectionnez **[!UICONTROL Click date]**.

   1. Indiquez la même période que celle utilisée pour le rapport [!DNL Google Ads].

   1. Dans la section **[!UICONTROL Search/Content]**, sélectionnez **[!UICONTROL Search Only]**.

   1. Dans la section **[!UICONTROL Search Engine Hierarchy]** , développez la section [!UICONTROL Google Adwords] et sélectionnez le compte.

   1. Ouvrez l’onglet [!UICONTROL Columns] et ajoutez les mesures [!DNL Google Ads] (commençant par &quot;GGL&quot;) que vous souhaitez comparer.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes de réseau publicitaire et des campagnes](campaign-implemention-overview.md)
>* [ Surveillez et gérez les performances de vos campagnes réseau d’annonces ](monitor-performance-campaigns.md)
>* [Afficher les mesures de conversion suivies pour un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Créer une balise de conversion pour [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
