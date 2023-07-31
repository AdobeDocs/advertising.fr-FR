---
title: '''[!DNL Google Ads] données de conversion"'
description: En savoir plus sur les types [!DNL Google Ads]Données de conversion suivies disponibles dans Search, Social et Commerce.
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
feature: Search Campaign Management
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# [!DNL Google Ads] données de conversion dans Search, Social et Commerce

La synchronisation automatique de Search, Social et Commerce [!DNL Google Ads]données de conversion suivies pour toutes vos campagnes sur la variable [!DNL Google Ads] recherchez et accédez aux réseaux d’achat dans Search, Social et Commerce pour optimiser la création de rapports et la création de rapports.

Toutes les mesures sont automatiquement disponibles dans les vues de gestion de campagne et les rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio à des fins d’optimisation.

## Données de conversion disponibles

Search, Social et Commerce synchronise les données pour les conversions pour lesquelles le[!DNL Include in 'Conversions']&quot; est activée, extrayant les données des 35 derniers jours, puis extrayant les modifications apportées aux données quotidiennement d’ici 2009:00-10:00 dans le fuseau horaire de l&#39;annonceur. Les données historiques peuvent changer d’un jour à l’autre, car de nouvelles conversions sont suivies pour chaque clic.

Jusqu’à trois mesures pour chaque [[!DNL Google Ads]conversion suivie](https://support.google.com/google-ads/answer/4677036) (que vous configurez dans [!DNL Google Ads]) sont automatiquement disponibles dans Search, Social et Commerce, à l’aide des noms de conversion configurés dans [!DNL Google Ads]. Les mesures pour chaque conversion incluent :

* `GGL*` — (Lorsque vous en effectuez le suivi) La valeur de conversion du mot-clé, commençant par le préfixe &quot;GGL&quot; (tel que Achat GGL).

* `GGL_CT*` — Nombre (décompte) de conversions, commençant par le préfixe &quot;GGL_CT&quot; (tel que GGL_CT_Purchase).

* `GGL_XD_CT*` — (Lorsqu’il est disponible pour le type de conversion, lorsque vous en effectuez le suivi) Le nombre (nombre) de conversions entre appareils, tel que mesuré par Google, en commençant par le préfixe &quot;GGL_XD_CT_&quot; (tel que GGL_XD_CT_Purchase).

[!DNL Google Ads] enregistre chaque conversion par [enchères unit](/help/search-social-commerce/glossary.md#a-b), appareil et date de clic (et non la date de conversion). L’attribution est basée sur le paramètre d’attribution par défaut pour chaque mesure dans [!DNL Google Ads]; l’attribution de l’Adobe Advertising n’est pas prise en compte, car les données au niveau de l’événement de clic ne sont pas disponibles.

>[!NOTE]
>
>* Si vous disposez de plusieurs comptes portant le même nom de conversion, il se peut que des noms de conversion en double s’affichent dans Adobe Advertising. Si cela se produit, [modifier le nom d’affichage ;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) pour l’une des mesures en double dans [!UICONTROL Admin] > [!UICONTROL Conversions]. La création de rapports n’est pas exacte lorsque deux mesures différentes portent le même nom.
>* Les données au niveau de l’unité d’offre correspondent aux données de [!DNL Google Ads] au même niveau. Cependant, [!DNL Google Ads]Les données de conversion propres aux niveaux supérieurs peuvent inclure des conversions supplémentaires qui ne sont pas attribuées aux unités d’offre enfants. Les données de Search, Social et Commerce sont toujours cumulées à partir du niveau de l’unité d’offre. Par exemple, un rapport au niveau de la campagne peut ne pas présenter les mêmes totaux qu’un rapport au niveau de la campagne dans Google Ads.
>* La variance de données est généralement inférieure après la synchronisation matinale par rapport à plus tard dans la journée, lorsque des conversions supplémentaires n’ont pas encore été synchronisées. Nous vous recommandons de valider les données le matin.
>* Les données de conversion ne sont pas disponibles pour [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], et [!DNL YouTube] publicités. Filtrez ces types d’annonces lorsque vous comparez des données dans [!DNL Google Ads] avec des données dans Search, Social et Commerce.
>* Données pour [!DNL Google Ads] les conversions ne sont pas disponibles au niveau de l’audience ou de l’emplacement géographique et ne sont donc pas utilisées pour optimiser automatiquement les ajustements des offres RLSA et de l’emplacement.

## Comment comparer les données de conversion dans [!DNL Google Ads] avec des données dans Search, Social et Commerce

Si vous comparez les données de Search, Social et Commerce à celles de [!DNL Google Ads], utilisez l’option d’affichage ou de rapport pour afficher les conversions en fonction de la date de clic (et non de la date de transaction).

Utilisez les paramètres de rapport suivants pour valider des données comparables.

### Paramètres des rapports à utiliser dans [!DNL Google Ads]

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

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur sur **[!UICONTROL Basic Reports]**, puis cliquez sur **[!UICONTROL Search Engine Account Report]**.

1. Dans le [!UICONTROL Report Settings] définissez les paramètres de rapport suivants :

   1. Dans le **[!UICONTROL Conversions Based]** sur la section , sélectionnez **[!UICONTROL Click date]**.

   1. Indiquez la même période que celle utilisée pour la variable [!DNL Google Ads] rapport.

   1. Dans le **[!UICONTROL Search/Content]** , sélectionnez **[!UICONTROL Search Only]**.

   1. Dans le **[!UICONTROL Search Engine Hierarchy]** , développez la section [!UICONTROL Google Adwords] et sélectionnez le compte.

   1. Ouvrez le [!UICONTROL Columns] et ajoutez le [!DNL Google Ads] mesures (commençant par &quot;GGL&quot;) que vous souhaitez comparer.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes et campagnes de réseau publicitaire](campaign-implemention-overview.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaires](monitor-performance-campaigns.md)
>* [Afficher les mesures de conversion suivies pour un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
