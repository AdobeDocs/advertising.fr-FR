---
title: (Nouvelle interface utilisateur) Afficher les détails sur les performances du portefeuille
description: Découvrez comment afficher les performances du portefeuille, les détails des unités d’enchères par mot-clé, les prévisions et l’historique des enchères, et exporter l’historique des unités d’enchères dans Adobe Advertising Search, Social et Commerce.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: b5178856-1b0e-45cf-a351-6f31c0b0ec76
TQID: 'https://experienceleague.adobe.com/5hNxKu6YjJTWI4KGEc6aaYnpgXK6k3OsN0-YfetzENw'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 6b779d2f91a140cd69ed4a25ac97d376dd1ed48d
workflow-type: tm+mt
source-wordcount: '1555'
ht-degree: 0%
---
# (Nouvelle interface utilisateur) Afficher les détails sur les performances du portefeuille

*Fonctionnalité Beta*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

La vue détaillée du portefeuille comprend les informations suivantes sur un portefeuille :

* Les valeurs réelles et prévues pour un maximum de trois mesures de performances. Les rapports incluent les valeurs totales des mesures pour le portefeuille et la répartition des mesures par date.<!-- Not for active portfolios only?  -->

* Données de précision du modèle pour les portefeuilles actifs, qui montrent dans quelle mesure les modèles se sont écartés des prédictions. Le rapport affiche la précision globale des coûts sur une période de sept jours, la précision des clics et la précision de la valeur objective.

  Vous pouvez afficher les données sous la forme d’un graphique de tendances (valeur par défaut) ou d’un tableau.

* Dépenses cibles par rapport aux dépenses réelles pour les portefeuilles actifs. Vous pouvez également inclure le total des budgets de campagne pour le portefeuille.

* La précision des prédictions de coût, de clic ou de [valeur d’objectif](/help/search-social-commerce/glossary.md#o-p) pour les portefeuilles actifs par réseau publicitaire.<!-- Verify -->

* Paramètres du portfolio.

  Vous pouvez éventuellement ouvrir les paramètres du portfolio pour les modifier.

* Listes des réseaux publicitaires, des comptes, des campagnes, des groupes publicitaires et des mots-clés du portfolio, avec données de performances.

  Pour des mots-clés individuels, vous pouvez afficher les détails des unités d&#39;enchères, y compris les prévisions, les informations historiques et les informations hiérarchiques. La vue [!UICONTROL Bid Unit Details] comprend les prévisions, les informations historiques et les informations hiérarchiques suivantes pour l&#39;unité d&#39;enchères sélectionnée :

  * Onglet [!UICONTROL Forecast] : clics, coût, coût par clic, position et chiffre d’affaires actuellement prévus pour l’unité d’offre à différents prix d’offre. Les données sont affichées pour tous les appareils et pour chaque type d’appareil ([!UICONTROL Mobile], [!UICONTROL Computer] et [!UICONTROL Tablet]).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. -->

    **Remarque :** Aucune donnée de prévision n&#39;est disponible pour un type d&#39;appareil lorsque les données spécifiques à l&#39;appareil sont insuffisantes pour créer des modèles et définir des ajustements pour ce type d&#39;appareil. **Remarque :** Pour afficher la précision des coûts ou la précision du chiffre d&#39;affaires pour chaque unité d&#39;offre d&#39;un portefeuille qui a reçu un clic au cours d&#39;une période spécifique, consultez respectivement les détails de la précision des coûts ou des chiffres d&#39;affaires du portefeuille.

  * Onglet [!UICONTROL History] : Toutes les offres des 36 derniers jours, y compris les données suivantes pour chacune des offres : date et heure, impressions, clics, coût total, coût par clic moyen, position moyenne et revenu pondéré affichés par date de clic. Les données sont affichées pour tous les appareils et pour chaque type d&#39;appareil (mobile, ordinateur et tablette).<!-- Probably no longer applicable: For portfolios using v6 of the optimization capability, both the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs show the combined totals for computers and tablets. For portfolios using v7, however, all data for the [!UICONTROL Computers] and [!UICONTROL Tablets] tabs is separate. **Note:** Whenever the optimization method changes from v6 to v7 and vice-versa, the history data is reset the same day. -->

  * Onglet [!UICONTROL Details] : mot-clé, type de correspondance (le cas échéant), groupe publicitaire parent, campagne, compte réseau publicitaire et portefeuille auxquels appartient l’entité enchère.

## Ouvrir les détails de performances d’un portfolio

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Placez le curseur sur le nom du portfolio et cliquez sur ![Présentation de Portfolio](/help/search-social-commerce/assets/portfolio-overview.png "Présentation de Portfolio").

1. (Facultatif) Pour modifier la période des détails du portefeuille, cliquez sur la période en haut à droite, spécifiez la période, puis cliquez sur **[!UICONTROL Apply]**.

1. (Facultatif) Dans le menu **[!UICONTROL Data Aggregation]**, modifiez l’unité de temps des données incluses dans chaque ligne : *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly].*

   Les options disponibles dépendent de la période sélectionnée. Si l’agrégation actuelle n’est pas disponible pour une nouvelle période, une autre agrégation disponible est sélectionnée automatiquement.

1. (Facultatif) Dans le menu **[!UICONTROL Conversion Based On]** de l’en-tête de page, sélectionnez **[!UICONTROL Click Date]** ou **[!UICONTROL Transaction Date]**.

   Ce paramètre s’applique aux données de conversion dans les rapports de portfolio et les listes de composants.

Pour afficher les détails d&#39;un autre portefeuille, utilisez le sélecteur de portefeuille en regard du nom du portefeuille.

## Personnaliser l’onglet [!UICONTROL Portfolio Overview]

* (Facultatif) Pour personnaliser les rapports [!UICONTROL Portfolio Performance], effectuez l&#39;une des opérations suivantes :

  * Pour modifier les mesures de performances utilisées pour les mesures totales et les mesures détaillées, cliquez sur **[!UICONTROL Metrics]** et sélectionnez jusqu’à trois mesures.

    Les mesures par défaut sont *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* et *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

  * Pour les mesures détaillées :

    * Déplacez le commutateur en regard de **[!UICONTROL Display predictions]** pour afficher ou masquer les valeurs de mesure prévues.

    * Basculez entre la vue graphique (![Vue graphique](/help/search-social-commerce/assets/chart-view.png "Vue graphique")) et la vue Tableau (![Vue Tableau](/help/search-social-commerce/assets/table-view.png "Vue Tableau")).

    * (Dans la vue graphique) Pour afficher les données d&#39;un point du graphique, placez le curseur sur ce point.

    * (Dans la vue Graphique) Pour effectuer un zoom, sélectionnez une zone du graphique.

    * (Lorsque les marqueurs de modification de paramètre de portfolio sont affichés) Pour afficher l&#39;historique des modifications du portfolio pour une date marquée, cliquez sur le marqueur sur le graphique. Pour plus d&#39;informations sur l&#39;historique, voir « [Afficher l&#39;historique des modifications d&#39;un portefeuille](portfolio-view-change-history.md#portfolio-change-history) ».

* (Facultatif) Pour personnaliser le graphique de tendances [!UICONTROL Model accuracy], effectuez l&#39;une des opérations suivantes :

  * Basculez entre la vue graphique (![Vue graphique](/help/search-social-commerce/assets/chart-view.png "Vue graphique")) et la vue Tableau (![Vue Tableau](/help/search-social-commerce/assets/table-view.png "Vue Tableau")).

  * Basculer entre l’affichage des données sur le *[!UICONTROL Daily Accuracy]* et le *[!UICONTROL 7 Day Rolling Accuracy]*.

    [!UICONTROL 7 Day Rolling Accuracy] est l&#39;exactitude moyenne des prévisions pour les sept jours précédents, exprimée en pourcentage. Par exemple, la valeur pour 8 mai 2025 est la précision moyenne pour la période du 1er au 7 mai 2025.

    [!UICONTROL 7 Day Rolling Accuracy] est disponible uniquement lorsque [!UICONTROL Data Aggregation] est défini sur [!UICONTROL Daily].

  * (Dans la vue graphique) Pour afficher les données d&#39;un point du graphique, placez le curseur sur ce point.

* (Facultatif) Pour personnaliser le graphique de tendances [!UICONTROL Target vs actual spend], effectuez l&#39;une des opérations suivantes :

  * Déplacez le bouton en regard de **[!UICONTROL Display budget]** pour afficher ou masquer le budget total de la campagne pour chaque date.

  * Pour afficher les données de n’importe quel point du graphique, placez le curseur au-dessus de ce point.

* (Facultatif) Pour personnaliser le graphique de tendances [!UICONTROL Network Accuracy], effectuez l&#39;une des opérations suivantes :

  * Remplacez la mesure signalée par *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* ou *[!UICONTROL Objective Value]*.

  * Lorsque des données sont disponibles pour plusieurs réseaux, sélectionnez le réseau dans le menu en regard du menu des mesures.

  * Pour afficher les données de n’importe quel point du graphique, placez le curseur au-dessus de ce point.

  * Pour effectuer un zoom, sélectionnez une zone du graphique.

## Personnaliser les listes des composants de portfolio

Les onglets [!UICONTROL Networks], [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] et [!UICONTROL Keywords] incluent les commandes suivantes :

* Pour effectuer une recherche par nom, saisissez du texte dans le champ de recherche situé au-dessus du tableau, puis soumettez la recherche.

* Pour [filtrer les données](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md), cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter-new.png "Filtrer"). Vous pouvez modifier ou supprimer des filtres appliqués à l’aide des commandes de filtrage situées au-dessus du tableau.

* Pour afficher les composants d’un réseau, d’un compte, d’une campagne ou d’un groupe publicitaire dans l’onglet suivant, cliquez sur son nom. Le parent sélectionné s’affiche dans le chemin de navigation au-dessus du tableau, et les filtres applicables sont reportés au fur et à mesure que vous analysez le tableau. Les sélections de parents peuvent continuer à restreindre la liste lorsque vous changez d’onglet.

  Pour supprimer une sélection d’analyse (un nom de réseau ou de compte, par exemple), cliquez sur **[!UICONTROL X]** en regard du nom du composant dans le chemin de navigation au-dessus du tableau. Les sélections de parents de niveau supérieur peuvent rester en vigueur. Pour revenir à tous les composants du portfolio, supprimez les sélections de parents restantes et tous les autres filtres.

* Pour actualiser les données, cliquez sur ![Actualiser](/help/search-social-commerce/assets/refresh-new.png "Actualiser").

* ([!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] et [!UICONTROL Keywords] onglets uniquement) Pour modifier les colonnes affichées ou l’ordre de tri, cliquez sur ![Colonnes personnalisées](/help/search-social-commerce/assets/custom-columns-new.png "Colonnes personnalisées") et [modifiez le jeu de colonnes et les options de tri](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md).


## Répertorier les réseaux publicitaires du portefeuille

* Cliquez sur l’onglet **[!UICONTROL Networks]**.

## Répertorier les comptes du portefeuille

* Pour afficher tous les comptes du portefeuille, cliquez sur l&#39;onglet **[!UICONTROL Accounts]**.

* Pour afficher les comptes d&#39;un réseau spécifique dans le portefeuille, cliquez sur l&#39;onglet **[!UICONTROL Networks]**, puis sur le nom du réseau.

## Répertorier les campagnes du portfolio

Les détails de chaque campagne comprennent la stratégie d’enchères, le coût réel et prévu, les clics et la valeur de l’objectif, ainsi que la précision du coût, des clics et de la valeur de l’objectif.

* Pour visualiser toutes les campagnes du portfolio, cliquez sur l&#39;onglet **[!UICONTROL Campaigns]**.

* Pour afficher les campagnes d&#39;un compte spécifique du portefeuille, cliquez sur l&#39;onglet **[!UICONTROL Accounts]**, puis sur le nom du compte.

## Répertorier les groupes publicitaires du portfolio

Les détails de chaque groupe publicitaire incluent le réseau, l’enchère par défaut, le coût, les clics, le coût par clic, les impressions, la valeur de l’objectif et les mesures de conversion utilisées dans l’objectif du portefeuille.

* Pour afficher tous les groupes publicitaires du portfolio, cliquez sur l’onglet **[!UICONTROL Ad Groups]**.

* Pour afficher tous les groupes publicitaires d’une campagne au sein du portfolio, cliquez sur l’onglet **[!UICONTROL Campaigns]**, puis sur le nom de la campagne.

## Répertorier et afficher les détails sur les mots-clés du portefeuille {#bid-unit-details}

Les détails de chaque mot-clé incluent l’ID d’unité d’offre, le type de correspondance, le coût réel et prévu, les clics et la valeur d’objectif, ainsi que la différence entre le coût, le clic et la valeur d’objectif. Vous pouvez afficher les détails des unités d&#39;enchères sur un mot-clé individuel.

1. Répertoriez les mots-clés :

   * Pour afficher tous les mots-clés du portfolio, cliquez sur l&#39;onglet **[!UICONTROL Keywords]**.

   * Pour afficher tous les mots-clés d&#39;un groupe publicitaire dans le portfolio, cliquez sur l&#39;onglet **[!UICONTROL Ad Groups]**, puis cliquez sur le nom du groupe publicitaire.

1. (Facultatif) Pour afficher des détails sur une unité d&#39;enchères spécifique, cliquez sur la valeur dans la colonne **[!UICONTROL Bid Unit ID]**. Cliquez sur n’importe quel onglet de [!UICONTROL Bid Unit Details] pour plus d’informations.

### Afficher et télécharger l&#39;historique d&#39;une enchère individuelle {#bid-unit-history}

1. [Ouvrez les détails de l&#39;entité d&#39;enchères](#bid-unit-details).

1. Cliquez sur l’onglet **[!UICONTROL History]**.

1. (Facultatif) Dans le menu d’appareil situé au-dessus du tableau, sélectionnez un type d’appareil pour lequel afficher l’historique. Par défaut, les données de tous les appareils s’affichent.

1. (Facultatif) Lorsque des données d’historique sont disponibles, cliquez sur **[!UICONTROL Export as csv]** pour télécharger l’historique affiché.

Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

Pour afficher l&#39;historique des enchères pour l&#39;ensemble du portefeuille et modifier sa période, consultez « [Afficher l&#39;historique des modifications des enchères d&#39;un portefeuille](portfolio-view-change-history.md#portfolio-bid-change-history) ».

## Afficher et modifier les paramètres du portfolio

* Pour afficher ou masquer les paramètres du portfolio, cliquez sur **[!UICONTROL Portfolio Settings]**.

  * Pour modifier les paramètres visibles du portfolio, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") en regard de la section des paramètres et [modifier les paramètres du portfolio](portfolio-edit.md).

Pour plus d’informations sur les paramètres du portfolio, consultez le Guide d’optimisation , disponible dans Search, Social et Commerce.

## Téléchargez les rapports sur les performances du portfolio et les listes des composants du portfolio

* Pour télécharger les rapports de performances et les listes de composants, procédez comme suit :

  1. Dans la barre d&#39;outils, cliquez sur **[!UICONTROL Download report]**.

  1. Cochez la case en regard de chaque rapport de performances et de chaque type de composant de portefeuille à inclure.

     Les composants de portfolio disponibles sont *[!UICONTROL Campaigns table]*, *[!UICONTROL Ad groups table]* et *[!UICONTROL Keywords table]*. Les tables [!UICONTROL Networks] et [!UICONTROL Accounts] ne sont pas incluses dans ce téléchargement.

     Pour les rapports de performances avec les deux options, sélectionnez **[!UICONTROL As chart]**, **[!UICONTROL As table]** ou les deux. Le rapport [!UICONTROL Network accuracy chart] est disponible uniquement sous la forme d’un graphique.

  1. Cliquez sur **[!UICONTROL Download report]**.

* Pour télécharger un rapport [!UICONTROL Model accuracy] avec des types de données spécifiques :

  1. Dans la barre d&#39;outils de [!UICONTROL Model accuracy], cliquez sur **[!UICONTROL Download report]**.

  1. Sélectionnez **[!UICONTROL Cost Accuracy]**, **[!UICONTROL Objective Value Accuracy]** ou les deux.

  1. Pour chaque type de données sélectionné, sélectionnez **[!UICONTROL By Bid Unit]**, **[!UICONTROL By Click Volume]** ou les deux.

  1. Cliquez sur **[!UICONTROL Download report]**.

>[!MORELIKETHIS]
>
>* [(Nouvelle interface utilisateur) À propos des portefeuilles](portfolio-about.md)
>* [(Nouvelle interface utilisateur) Modifier un portfolio](portfolio-edit.md)
>* [(Nouvelle interface utilisateur) Télécharger des données dans la vue [!UICONTROL Portfolios]](portfolio-view-report.md)
