---
title: Gérer les  [!DNL Google Ads] cibles de recherche dynamique
description: Découvrez comment créer et gérer des  [!DNL Google Ads] cibles de recherche dynamique.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Gestion des [!DNL Google Ads] cibles de recherche dynamique

*[!DNL Google Ads]comptes uniquement*

Vous pouvez créer, modifier et modifier l’état des cibles de recherche dynamique pour les campagnes qui utilisent le réseau de recherche.

>[!NOTE]
>
>Vous pouvez créer et modifier de grandes quantités de données cibles en même temps en chargeant des [fichiers de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) et en les publiant sur le réseau publicitaire.

## Création d’une cible de recherche dynamique [!DNL Google Ads]

Vous pouvez créer des cibles de recherche dynamique pour définir les pages de vos sites web (c’est-à-dire les domaines utilisés dans les URL d’affichage de vos annonces) dont le contenu est utilisé pour cibler vos annonces de recherche dynamique dans le même groupe d’annonces.

Vous pouvez cibler tous les critères ou trois critères au maximum.

>[!NOTE]
>
>Pour optimiser le suivi des performances, créez une cible &quot;[!UICONTROL All Targets]&quot; pour un seul groupe publicitaire par campagne.

>[!TIP]
>
>Pour créer de nombreux composants de compte en même temps, utilisez les [feuilles d’envoi groupées de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les [paramètres de la cible de recherche dynamique](#dynamic-search-target-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Modification des paramètres de la cible de recherche dynamique [!DNL Google Ads]

Vous pouvez modifier l’état ou l’offre maximale d’une cible de recherche dynamique [!DNL Google Ads]. Vous ne pouvez pas modifier les critères ciblés.

>[!TIP]
>
>Pour modifier de grandes quantités de données à la fois, utilisez les [feuilles d’envoi groupées de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque ligne à modifier.

   Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Spécifiez les [paramètres de la cible de recherche dynamique](#dynamic-search-target-settings).

   Pour plusieurs cibles, vos modifications sont appliquées à toutes les cibles sélectionnées. Pour le [!UICONTROL Bid field], vous avez la possibilité de modifier les valeurs existantes en une valeur spécifiée ou d’augmenter ou de diminuer le montant d’un pourcentage ou d’un montant monétaire spécifié, avec une limite.

1. Enregistrez les données :

   * (Cibles uniques) Cliquez sur **[!UICONTROL Post]**.

   * (Plusieurs groupes publicitaires) Cliquez sur **[!UICONTROL Post Now]**.

## Modification de l’état des cibles de recherche dynamique [!DNL Google Ads]

Vous pouvez suspendre toute cible de recherche dynamique active dans un type de campagne pris en charge afin de ne plus l’utiliser pour les annonces de recherche dynamique du même groupe publicitaire. Vous pouvez ensuite les utiliser comme cibles en redéfinissant l’état de la publicité sur actif.

Vous pouvez également supprimer toute cible dynamique.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Facultatif) Filtrez la liste pour inclure des cibles dynamiques spécifiques.

1. Effectuez l’une des opérations suivantes :

   * Pour modifier l’état d’une cible dynamique, cliquez dans la colonne **[!UICONTROL Status]** et modifiez l’état.

   * Pour supprimer une ou plusieurs cibles dynamiques, procédez comme suit :

      1. Cochez la case en regard de chaque cible dynamique à supprimer.

     Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Dans la barre d’outils, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") et sélectionnez **[!UICONTROL Delete]**.

      1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## [!DNL Google Ads] paramètres de la cible de recherche dynamique {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Obligatoire lorsque vous ne spécifiez pas de domaine et de langue de site web dans la section [!UICONTROL DSA Options] de la campagne ; lecture seule pour les cibles existantes) Cibles de recherche dynamique pour le groupe publicitaire :

* *[!UICONTROL All Targets]* (valeur par défaut) : cible toutes les pages indexées.

* *\[Cibles spécifiques\]:* Cible jusqu’à trois critères pour les pages indexées. Lorsque vous sélectionnez cette option, vous devez spécifier les critères en spécifiant les catégories d’informations et les valeurs spécifiques pour lesquelles cibler les publicités (par exemple, &quot;L’URL contient chaussures.exemple.com&quot;). Pour spécifier plusieurs critères, cliquez sur **[!UICONTROL + And]**. Les critères de ciblage incluent :

   * *[!UICONTROL Category]:* pour afficher des publicités pour des pages indexées avec une catégorie de contenu [!DNL Google Ads] spécifique.

   * *[!UICONTROL URL]:* pour afficher des publicités pour des pages indexées avec une URL spécifique, où la valeur peut être incluse n’importe où dans l’URL.

   * *[!UICONTROL Page Title]:* pour afficher des publicités pour des pages indexées avec du texte spécifique dans le titre de la page.

   * *[!UICONTROL Page Content]:* pour afficher des publicités pour des pages indexées avec du contenu spécifique.

**État :** État des paramètres de la cible :

* *[!UICONTROL Active]* (valeur par défaut) : active l’offre.

* *[!UICONTROL Paused]:* désactive l’offre.

* *[!UICONTROL Deleted]* (cibles existantes uniquement) : supprime les paramètres de la cible.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** coût maximum par clic (CPC) d’une publicité ou coût par 1 000 impressions (CPM) d’une publicité, selon le modèle de tarification du réseau publicitaire et de la campagne. Cette valeur remplace la valeur au niveau du groupe publicitaire.

>[!NOTE]
>
>Si la cible se trouve dans un portefeuille optimisé, l’offre CPC spécifiée est appliquée pendant une journée. Par la suite, la fonctionnalité d’optimisation place les offres en fonction de ses propres calculs.

>[!MORELIKETHIS]
>
>* [À propos de [!DNL Google Ads] cibles de recherche dynamique](dynamic-search-target-about.md)
