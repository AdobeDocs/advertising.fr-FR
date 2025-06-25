---
title: Gestion  [!DNL Google Ads]  cibles de recherche dynamiques
description: Découvrez comment créer et gérer  [!DNL Google Ads]  cibles de recherche dynamiques.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Gestion [!DNL Google Ads] cibles de recherche dynamique

Comptes *[!DNL Google Ads]uniquement*

Vous pouvez créer, modifier et modifier le statut des cibles de recherche dynamique pour les campagnes qui utilisent le réseau de recherche.

>[!NOTE]
>
>Vous pouvez créer et modifier simultanément de grandes quantités de données de la cible en chargeant des [fichiers de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) et en les publiant sur le réseau publicitaire.

## Création d’une cible de recherche dynamique [!DNL Google Ads]

Vous pouvez créer des cibles de recherche dynamique pour définir des pages dans vos sites web (c’est-à-dire les domaines utilisés dans les URL d’affichage de vos publicités) dont le contenu est utilisé pour cibler vos publicités de recherche dynamique dans le même groupe de publicités.

Vous pouvez cibler tous les critères ou jusqu’à trois critères individuels.

>[!NOTE]
>
>Pour suivre au mieux les performances, créez une cible « [!UICONTROL All Targets] » pour un seul groupe publicitaire par campagne.

>[!TIP]
>
>Pour créer plusieurs composants de compte à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les paramètres [cible de recherche dynamique](#dynamic-search-target-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Modifier [!DNL Google Ads] paramètres de la cible de recherche dynamique

Vous pouvez modifier le statut ou l’enchère maximale d’une cible de recherche dynamique [!DNL Google Ads]. Vous ne pouvez pas modifier les critères ciblés.

>[!TIP]
>
>Pour modifier de grandes quantités de données à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque ligne à modifier.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Spécifiez les paramètres [cible de recherche dynamique](#dynamic-search-target-settings).

   Si plusieurs cibles sont sélectionnées, vos modifications sont appliquées à toutes les cibles sélectionnées. Pour le [!UICONTROL Bid field], vous avez la possibilité de modifier les valeurs existantes à une valeur spécifiée ou d’augmenter ou de diminuer le montant d’un pourcentage ou d’un montant monétaire spécifié, avec une limite.

1. Enregistrez les données :

   * (Cibles uniques) Cliquez sur **[!UICONTROL Post]**.

   * (Plusieurs groupes publicitaires) Cliquez sur **[!UICONTROL Post Now]**.

## Modification du statut [!DNL Google Ads] cibles de recherche dynamique

Vous pouvez suspendre n’importe quelle cible de recherche dynamique active dans un type de campagne pris en charge afin de cesser de l’utiliser pour les annonces de recherche dynamique du même groupe d’annonces. Vous pouvez ensuite les utiliser comme cibles en redéfinissant le statut de l’annonce sur Actif.

Vous pouvez également supprimer n’importe quelle cible dynamique.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Facultatif) Filtrez la liste pour inclure des cibles dynamiques spécifiques.

1. Effectuez l’une des opérations suivantes :

   * Pour modifier le statut d&#39;une cible dynamique, cliquez dans la colonne **[!UICONTROL Status]** et modifiez le statut.

   * Pour supprimer une ou plusieurs cibles dynamiques, procédez comme suit :

      1. Cochez la case en regard de chaque cible dynamique à supprimer.

     Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

      1. Dans la barre d’outils, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") et sélectionnez **[!UICONTROL Delete]**.

      1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## [!DNL Google Ads] des paramètres de la cible de recherche dynamique {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (obligatoire lorsque vous ne spécifiez pas de domaine ni de langue de site web dans la section [!UICONTROL DSA Options] de la campagne ; en lecture seule pour les cibles existantes) Cibles de recherche dynamique pour le groupe publicitaire :

* *[!UICONTROL All Targets]* (valeur par défaut) : cible toutes les pages indexées.

* *\[Cibles spécifiques\]:* cible jusqu’à trois critères pour les pages indexées. Lorsque vous sélectionnez cette option, vous devez spécifier les critères en spécifiant les catégories d’informations et les valeurs spécifiques pour lesquelles cibler les annonces (par exemple, « L’URL contient des chaussures.exemple.com »). Pour spécifier plusieurs critères, cliquez sur **[!UICONTROL + And]**. Les critères cibles sont les suivants :

   * *[!UICONTROL Category]:* pour afficher des publicités pour des pages indexées avec une catégorie de contenu [!DNL Google Ads] spécifique.

   * *[!UICONTROL URL]:* pour afficher des publicités pour des pages indexées avec une URL spécifique, où la valeur peut être incluse n’importe où dans l’URL.

   * *[!UICONTROL Page Title]:* pour afficher des annonces pour les pages indexées avec un texte spécifique dans le titre de la page.

   * *[!UICONTROL Page Content]:* pour afficher des publicités pour des pages indexées avec un contenu spécifique.

**Statut :** statut des paramètres de la cible :

* *[!UICONTROL Active]* (valeur par défaut) : permet d’enchérir.

* *[!UICONTROL Paused]:* Désactive les enchères.

* *[!UICONTROL Deleted]* (cibles existantes uniquement) : supprime les paramètres de la cible.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** coût maximum par clic (CPC) pour une publicité ou coût par 1 000 impressions (CPM) pour une publicité, selon le modèle de tarification du réseau publicitaire et de la campagne. Cette valeur remplace la valeur au niveau du groupe publicitaire.

>[!NOTE]
>
>Si la cible se trouve dans un portefeuille optimisé, l’enchère CPC spécifiée est appliquée pendant un jour. Ensuite, la fonctionnalité d’optimisation place les offres en fonction de ses propres calculs.

>[!MORELIKETHIS]
>
>* [À propos [!DNL Google Ads] des cibles de recherche dynamique](dynamic-search-target-about.md)
