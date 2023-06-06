---
title: "[!DNL Google Ads] données de conversion"
description: En savoir plus sur les types de [!DNL Google Ads]Données de conversion suivies disponibles dans Search, Social et Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] données de conversion dans Search, Social et Commerce

La synchronisation automatique de Search, Social et Commerce [!DNL Google Ads]données de conversion suivies pour toutes vos campagnes sur la variable [!DNL Google Ads] recherchez et accédez aux réseaux d’achat dans Search, Social et Commerce pour optimiser la création de rapports et la création de rapports. Search, Social et Commerce synchronise les données pour les conversions pour lesquelles le[!DNL Include in 'Conversions']&quot; est activée, extrayant les données des 30 derniers jours, puis extrayant les modifications apportées quotidiennement aux données.

## Données de conversion disponibles

Jusqu’à trois propriétés de transaction pour chacune [[!DNL Google Ads]conversion trackée](https://support.google.com/google-ads/answer/4677036) (que vous configurez dans [!DNL Google Ads]) sont automatiquement disponibles dans Search, Social et Commerce, à l’aide des noms de conversion configurés dans [!DNL Google Ads]. Les propriétés de transaction pour chaque conversion incluent :

* `GGL*` — (Lorsque vous en effectuez le suivi) Somme des valeurs de conversion du mot-clé, commençant par le préfixe &quot;GGL&quot; (tel que Achat GGL).

* `GGL_CT*` — Nombre (décompte) de conversions, commençant par le préfixe &quot;GGL_CT&quot; (tel que GGL_CT_Purchase).

* `GGL_XD_CT*` — (Lorsqu’il est disponible pour le type de conversion, lorsque vous en effectuez le suivi) Le nombre (nombre) de conversions entre appareils, tel que mesuré par Google, en commençant par le préfixe &quot;GGL_XD_CT_&quot; (tel que GGL_XD_CT_Purchase).

Les données sont disponibles à partir de la date à laquelle la fonction est activée pour le compte et sont mises à jour quotidiennement à partir du 09.:00-10:00 dans le fuseau horaire de l&#39;annonceur.

[!DNL Google Ads] enregistre chaque conversion par [enchères unit](/help/search-social-commerce/glossary.md#a-b), appareil et date de clic (et non la date de conversion). L’attribution est basée sur le paramètre d’attribution par défaut pour chaque mesure dans [!DNL Google Ads]; L’attribution de publicité Adobe n’est pas prise en compte, car les données au niveau de l’événement de clic ne sont pas disponibles. Chaque jour, Search, Social et Commerce extrait les données de conversion pour les 30 jours précédents, puis calcule les conversions incrémentielles depuis le jour précédent, à l’aide de la date de clic à partir de [!DNL Google Ads] et désignant le jour précédent comme date de transaction. Par conséquent, les données historiques peuvent varier d’un jour à l’autre, à mesure que de nouvelles conversions sont suivies pour chaque clic. Si vous comparez les données de Search, Social et Commerce à celles de [!DNL Google Ads], utilisez l’option d’affichage ou de rapport pour afficher &quot;[!UICONTROL Conversions by: Click date]&quot; (pas par date de transaction).

Toutes les mesures sont automatiquement disponibles dans les vues de gestion de campagne et les rapports de base. Elles peuvent également être utilisées dans les objectifs du portfolio à des fins d’optimisation.

>[!NOTE]
>
>* Si vous disposez de plusieurs comptes portant le même nom de conversion, il se peut que des noms de conversion en double apparaissent dans Adobe Advertising. Si cela se produit, [modifier le nom d’affichage ;](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) pour l’une des mesures en double dans [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. La création de rapports n’est pas exacte lorsque deux mesures différentes portent le même nom.
>* Les données au niveau de l’unité d’offre correspondent aux données de la variable [!DNL Google Ads] au même niveau. Cependant, [!DNL Google Ads]Les données de conversion propres aux niveaux supérieurs peuvent inclure des conversions supplémentaires qui ne sont pas attribuées aux unités d’offre enfants. Les données de Search, Social et Commerce sont toujours cumulées à partir du niveau de l’unité d’offre. Par exemple, un rapport au niveau de la campagne peut ne pas présenter les mêmes totaux qu’un rapport au niveau de la campagne dans Google Ads.
>* La variance de données est généralement inférieure après la synchronisation matinale par rapport à plus tard dans la journée, lorsque des conversions supplémentaires n’ont pas encore été synchronisées. Nous vous recommandons de valider les données le matin.
>* Les données de conversion ne sont pas disponibles pour [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], et [!DNL YouTube] publicités. Filtrez ces types d’annonces lorsque vous comparez des données dans [!DNL Google Ads] avec des données dans Search, Social et Commerce.
>* Données pour [!DNL Google Ads] les conversions ne sont pas disponibles au niveau de l’audience ou de l’emplacement géographique et ne sont donc pas utilisées pour optimiser automatiquement les ajustements des offres RLSA et de l’emplacement.


## Comment comparer les données de conversion dans [!DNL Google Ads] avec des données dans Search, Social et Commerce

Utilisez les paramètres de rapport suivants pour valider des données comparables.

### Paramètres des rapports à utiliser dans [!DNL Google Ads]

1. Dans la barre d’outils principale, sélectionnez **[!DNL Reports]>[!DNL Report]**.

1. Sélectionner **[!DNL + Custom]>[!DNL Table]**.

1. Dans le volet de gauche, spécifiez les lignes et les colonnes du rapport :

   1. Recherchez le **[!DNL Day]** et le faire glisser vers le champ [!DNL Row] .

   1. Recherchez le **[!DNL All conv].** et le faire glisser vers le champ [!DNL Column] .

   1. Recherchez le **[!DNL Conversion action]** et le faire glisser vers le champ [!DNL Column] .

1. Dans la barre d’outils des paramètres de rapport, sélectionnez **[!DNL Filter]>[!DNL Ad status]**, puis sélectionnez toutes les cases.

1. Dans la barre d’outils des paramètres de rapport, sélectionnez **[!DNL Download]>[!DNL Excel .csv]**.

### Paramètres des rapports à utiliser dans Search, Social et Commerce

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
>* [À propos de la gestion des campagnes dans Search, Social et Commerce](campaign-management-about.md)
>* [Présentation de l’implémentation des comptes et campagnes de réseau publicitaire](campaign-implemention-overview.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaires](monitor-performance-campaigns.md)

