---
title: (Nouvelle interface utilisateur) Afficher les détails sur les performances du portefeuille
description: Découvrez comment afficher les détails sur les performances du portfolio, y compris les mesures réelles et prévues au niveau du portfolio et pour chaque campagne affectée.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
source-git-commit: fee9c6e4649c348cad7561f81a9d45d92eb672ec
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Afficher les détails sur les performances du portefeuille

*Fonction Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

La vue détaillée du portefeuille comprend les informations suivantes sur un portefeuille :

* Les valeurs réelles et prévues pour un maximum de trois mesures de performances. Les rapports incluent les valeurs de mesure totales pour le portefeuille et la répartition des mesures par date.<!-- Not for active portfolios only?  -->

* Données de précision du modèle pour les portefeuilles actifs, qui montrent dans quelle mesure les modèles se sont écartés des prédictions. Le rapport affiche la précision globale des coûts sur une période de sept jours, la précision des clics et la précision de la valeur objective.

  Vous pouvez afficher les données par date de clic (valeur par défaut) ou par date de transaction.   Vous pouvez également afficher les données sous la forme d’un graphique de tendances (valeur par défaut) ou d’un tableau.

* Dépenses cibles par rapport aux dépenses réelles pour les portefeuilles actifs. Vous pouvez également inclure le total des budgets de campagne pour le portefeuille.

* La précision des prédictions de coût, de clic ou [valeur objective](/help/search-social-commerce/glossary.md#o-p) pour les portefeuilles actifs par réseau publicitaire.<!-- Verify -->

* Paramètres du portfolio.

  Vous pouvez éventuellement ouvrir les paramètres du portfolio pour les modifier.

## Ouvrir les détails de performances d’un portfolio

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Cliquez sur le nom du portfolio.

1. (Facultatif) Dans le menu **[!UICONTROL Granularity]** , modifiez la granularité des données entre *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly].*

1. (Facultatif) Pour modifier la période des détails du portefeuille, cliquez sur la période en haut à droite, spécifiez la période, puis cliquez sur **[!UICONTROL Apply]**.

## Personnaliser l’onglet [!UICONTROL Portfolio Overview]

* (Facultatif) Pour personnaliser les rapports [!UICONTROL Portfolio Performance], effectuez l’une des opérations suivantes :

   * Pour modifier les mesures de performances utilisées pour les mesures totales et les mesures détaillées, cliquez sur **[!UICONTROL Metrics]** et sélectionnez jusqu’à trois mesures.

     Les mesures par défaut sont *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* et *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * Pour les mesures détaillées :

      * Déplacez le commutateur en regard de **[!UICONTROL Display predictions]** pour afficher ou masquer les valeurs de mesure prévues.

      * Basculez entre la vue graphique (![Vue graphique](/help/search-social-commerce/assets/chart-view.png "Vue graphique")) et la vue Tableau (![Vue Tableau](/help/search-social-commerce/assets/table-view.png "Vue Tableau")).

      * (Dans la vue graphique) Pour afficher les données d&#39;un point du graphique, placez le curseur sur ce point.

* (Facultatif) Pour personnaliser le graphique de tendance [!UICONTROL Model accuracy], effectuez l’une des opérations suivantes :

   * Basculez entre la vue graphique (![Vue graphique](/help/search-social-commerce/assets/chart-view.png "Vue graphique")) et la vue Tableau (![Vue Tableau](/help/search-social-commerce/assets/table-view.png "Vue Tableau")).

   * Basculez entre l’affichage des données par *[!UICONTROL Click Date]* et *[!UICONTROL Transaction Date]*.

   * Basculez entre l’affichage des données sur le *[!UICONTROL Daily Accuracy]* et l’*[!UICONTROL 7 Day Rolling Accuracy]*.

     [!UICONTROL 7 Day Rolling Accuracy] est l’exactitude moyenne des prévisions pour les sept jours précédents, exprimée en pourcentage. Par exemple, la valeur pour 8 mai 2025 est la précision moyenne pour la période du 1er au 7 mai 2025.

   * (Dans la vue graphique) Pour afficher les données d&#39;un point du graphique, placez le curseur sur ce point.

* (Facultatif) Pour personnaliser le graphique de tendance [!UICONTROL Target vs actual spend], effectuez l’une des opérations suivantes :

   * Déplacez le bouton en regard de **[!UICONTROL Display budget]** pour afficher ou masquer le budget total de la campagne pour chaque date.

   * Pour afficher les données de n’importe quel point du graphique, placez le curseur au-dessus de ce point.

* (Facultatif) Pour personnaliser le graphique de tendance [!UICONTROL Network Accuracy], effectuez l’une des opérations suivantes :

   * Remplacez la mesure signalée par *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* ou *[!UICONTROL Objective Value]*.

   * Pour afficher les données de n’importe quel point du graphique, placez le curseur au-dessus de ce point.

1. Cliquez sur **[!UICONTROL Download report]**.

## Répertorier les campagnes du portfolio

* Cliquez sur l’onglet **[!UICONTROL Campaigns]** .

## Répertorier les groupes publicitaires du portfolio

* Pour afficher tous les groupes publicitaires d’une campagne au sein du portfolio, cliquez sur l’onglet **[!UICONTROL Campaigns]** , puis sur le nom de la campagne.

## Répertorier les mots-clés du portfolio

* Pour afficher tous les mots-clés du portfolio, cliquez sur l’onglet **[!UICONTROL Keywords]** .

* Pour afficher tous les mots-clés d&#39;un groupe publicitaire dans le portfolio, cliquez sur l&#39;onglet **[!UICONTROL Ad Groups]**, puis cliquez sur le nom du groupe publicitaire.

## Afficher et modifier les paramètres du portfolio

* Pour afficher ou masquer les paramètres du portfolio, cliquez sur **[!UICONTROL Portfolio Settings]**.

   * Pour modifier les paramètres de portfolio visibles, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") en regard de la section de paramètre et [modifier les paramètres de portfolio](portfolio-edit.md).

Pour plus d’informations sur les paramètres du portfolio, consultez le Guide d’optimisation , disponible dans Search, Social et Commerce.

## Téléchargez les rapports de performances du portefeuille et les listes des composants du portefeuille

1. Dans la barre d’outils, cliquez sur **[!UICONTROL Download report]**.

1. Cochez la case en regard de chaque rapport de performances et de chaque type de composant de portefeuille à inclure.

   Pour certains rapports de performances, vous pouvez choisir de télécharger les données sous forme de panier ou de tableau.

>[!MORELIKETHIS]
>
>* [&#x200B; (nouvelle interface utilisateur) À propos des portfolios](portfolio-about.md)
>* [&#x200B; (nouvelle interface utilisateur) Modification d’un portfolio](portfolio-edit.md)
>* [&#x200B; (nouvelle interface utilisateur) Télécharger des données dans la vue [!UICONTROL Portfolios]](portfolio-view-report.md)
