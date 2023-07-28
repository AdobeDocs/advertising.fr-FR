---
title: Gérer [!DNL Google Ads] cibles de recherche dynamique
description: Découvrez comment créer et gérer [!DNL Google Ads] cibles de recherche dynamique.
exl-id: 85b1455a-dda1-4bb9-b4be-d6e0a837fd9d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# Gérer [!DNL Google Ads] cibles de recherche dynamique

*[!DNL Google Ads]comptes uniquement*

Vous pouvez créer, modifier et modifier l’état des cibles de recherche dynamique pour les campagnes qui utilisent le réseau de recherche.

>[!NOTE]
>
>Vous pouvez créer et modifier de grandes quantités de données de ciblage en même temps en chargeant [fichiers de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) et les publier sur le réseau publicitaire.

## Créez un [!DNL Google Ads] cible de recherche dynamique

Vous pouvez créer des cibles de recherche dynamique pour définir les pages de vos sites web (c’est-à-dire les domaines utilisés dans les URL d’affichage de vos annonces) dont le contenu est utilisé pour cibler vos annonces de recherche dynamique dans le même groupe d’annonces.

Vous pouvez cibler tous les critères ou trois critères au maximum.

>[!NOTE]
>
>Pour optimiser le suivi des performances, créez un[!UICONTROL All Targets]&quot;cible pour un seul groupe publicitaire par campagne.

>[!TIP]
>
>Pour créer plusieurs composants de compte en même temps, utilisez [feuilles d’envoi groupé de campagnes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez la variable [paramètres de cible de recherche dynamique](#dynamic-search-target-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Modifier [!DNL Google Ads] paramètres de cible de recherche dynamique

Vous pouvez modifier l’état ou l’offre maximale d’une [!DNL Google Ads] cible de recherche dynamique. Vous ne pouvez pas modifier les critères ciblés.

>[!TIP]
>
>Pour modifier simultanément de grandes quantités de données, utilisez [feuilles d’envoi groupé de campagnes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque ligne à modifier.

   Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Spécifiez la variable [paramètres de cible de recherche dynamique](#dynamic-search-target-settings).

   Pour plusieurs cibles, vos modifications sont appliquées à toutes les cibles sélectionnées. Pour le [!UICONTROL Bid field], vous avez la possibilité de modifier les valeurs existantes en une valeur spécifique ou d’augmenter ou de diminuer le montant d’un pourcentage spécifié ou d’un montant monétaire, avec une limite.

1. Enregistrez les données :

   * (Cibles uniques) Cliquez sur **[!UICONTROL Post]**.

   * (Plusieurs groupes publicitaires) Cliquez sur **[!UICONTROL Post Now]**.

## Modifier l’état de [!DNL Google Ads] cibles de recherche dynamique

Vous pouvez suspendre toute cible de recherche dynamique principale dans un type de campagne pris en charge afin de ne plus l’utiliser pour les annonces de recherche dynamique du même groupe publicitaire. Vous pouvez ensuite les utiliser comme cibles en redéfinissant l’état de la publicité sur principal.

Vous pouvez également supprimer toute cible dynamique.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Facultatif) Filtrez la liste pour inclure des cibles dynamiques spécifiques.

1. Effectuez l’une des opérations suivantes :

   * Pour modifier l’état d’une cible dynamique, cliquez sur dans la variable **[!UICONTROL Status]** et modifiez l’état.

   * Pour supprimer une ou plusieurs cibles dynamiques, procédez comme suit :

      1. Cochez la case en regard de chaque cible dynamique à supprimer.

     Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Dans la barre d’outils, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") et sélectionnez **[!UICONTROL Delete]**.

      1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## [!DNL Google Ads] paramètres de cible de recherche dynamique {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Obligatoire lorsque vous ne spécifiez pas de domaine et de langue de site web dans le rapport [!UICONTROL DSA Options] section ; lecture seule pour les cibles existantes) Cibles de recherche dynamique pour le groupe publicitaire :

* *[!UICONTROL All Targets]* (valeur par défaut) : cible toutes les pages indexées.

* *\[Cibles spécifiques\] :* Cible jusqu’à trois critères pour les pages indexées. Lorsque vous sélectionnez cette option, vous devez spécifier les critères en spécifiant les catégories d’informations et les valeurs spécifiques pour lesquelles cibler les publicités (par exemple, &quot;L’URL contient chaussures.exemple.com&quot;). Pour spécifier plusieurs critères, cliquez sur **[!UICONTROL + And]**. Les critères de ciblage incluent :

   * *[!UICONTROL Category]:* Pour afficher des publicités pour des pages indexées avec un [!DNL Google Ads] catégorie de contenu.

   * *[!UICONTROL URL]:* Pour afficher des publicités pour des pages indexées avec une URL spécifique, où la valeur peut être incluse n’importe où dans l’URL.

   * *[!UICONTROL Page Title]:* Pour afficher des publicités pour des pages indexées avec du texte spécifique dans le titre de la page.

   * *[!UICONTROL Page Content]:* Pour afficher des publicités pour des pages indexées avec du contenu spécifique.

**État :** État des paramètres de la cible :

* *[!UICONTROL Active]* (valeur par défaut) : active l’offre.

* *[!UICONTROL Paused]:* Désactive l’offre.

* *[!UICONTROL Deleted]* (cibles existantes uniquement) : supprime les paramètres de la cible.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** Coût maximum par clic (CPC) d’une publicité ou coût par 1 000 impressions (CPM) d’une publicité, applicable au réseau publicitaire et au modèle de tarification de campagne. Cette valeur remplace la valeur au niveau du groupe publicitaire.

>[!NOTE]
>
>Si la cible se trouve dans un portefeuille optimisé, l’offre CPC spécifiée est appliquée pendant une journée. Par la suite, la fonctionnalité d’optimisation place les offres en fonction de ses propres calculs.

>[!MORELIKETHIS]
>
>* [A propos [!DNL Google Ads] cibles de recherche dynamique](dynamic-search-target-about.md)
