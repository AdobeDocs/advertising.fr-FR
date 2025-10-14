---
title: Gestion des vues par défaut et personnalisées
description: Découvrez comment personnaliser vos vues par défaut et vos vues personnalisées.
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 399974645b5083e735ff7aa94eba0a1115b4ddeb
workflow-type: tm+mt
source-wordcount: '4453'
ht-degree: 0%

---

# Gestion des vues par défaut et personnalisées

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

Vos vues par défaut et personnalisées vous permettent de personnaliser les données de performances affichées dans les vues de données des campagnes de recherche. Les paramètres d’affichage comprennent les colonnes à inclure, les filtres, la période, les paramètres d’attribution de conversion et d’autres paramètres avancés ; vous pouvez appliquer les paramètres temporairement ou les enregistrer. (Exception : vous ne pouvez pas enregistrer de filtres pour les vues par défaut.) Chaque vue personnalisée par défaut et standard s’applique à une vue spécifique (telle que [!UICONTROL Portfolios] ou [!UICONTROL Campaigns]) et à un compte d’annonceur spécifique uniquement. Dans l’interface utilisateur héritée, chaque vue personnalisée universelle s’applique à toutes les vues d’entité pour un annonceur spécifique et ne peut donc pas inclure de colonnes de propriété (telles que le nom ou le statut de l’entité), qui varient selon le type d’entité.

Les vues par défaut s&#39;affichent par défaut à chaque connexion. Vous pouvez créer des vues personnalisées supplémentaires et les appliquer à tout moment. Vous pouvez éventuellement partager n’importe quelle vue personnalisée que vous créez avec tous les autres utilisateurs qui peuvent afficher les données de l’annonceur. Seule la personne qui crée une vue personnalisée peut la supprimer.

Dans l’interface utilisateur héritée, chaque vue est disponible sous forme de raccourci dans la section [!UICONTROL Custom Views] du panneau de gauche.

## Appliquer une vue par défaut ou personnalisée

### (Nouvelle interface utilisateur) Appliquer une vue par défaut ou personnalisée à une vue de gestion

1. Au-dessus du tableau de données, cliquez sur le nom de la vue actuellement appliquée (![Vue](/help/search-social-commerce/assets/view.png "Vue")).

1. Si nécessaire, cliquez sur l’un des onglets ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] et [!UICONTROL From Others]) pour localiser la vue.

1. Placez le curseur sur le nom de la vue et cliquez sur **[!UICONTROL Apply]**.

### (Interface utilisateur héritée) Appliquer une vue par défaut ou personnalisée à une vue de gestion de campagne

* (Vues par défaut) Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]** \> **\[entity type\]**.

* (Vues personnalisées) À partir du panneau de navigation de gauche :

   1. Dans le panneau de gauche, cliquez sur le menu **[!UICONTROL Custom Views]** pour le développer.

      Les vues sont triées par entité applicable.

   1. Développez les menus disponibles.

      « [!UICONTROL Universal Views] » inclut des vues personnalisées qui peuvent être utilisées dans toutes les vues d’entité. Toutes les autres vues personnalisées sont regroupées par type d&#39;entité.

   1. Cliquez sur le nom de la vue.

      Si la vue est universelle ou s&#39;applique à l&#39;entité actuelle, le tableau de données est réaffiché selon la configuration de la vue. Si la vue s&#39;applique à une autre entité, les données de l&#39;entité applicable sont affichées selon la configuration de la vue.

## Création d’une vue personnalisée {#create-custom-view}

>[!NOTE]
>
>Outre les paramètres d’affichage que vous spécifiez pour l’affichage personnalisé, l’ordre de tri actuel des colonnes est également enregistré.

### (Nouvelle interface utilisateur) Créer une vue personnalisée à partir d’une vue de gestion

*Disponible dans les vues [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] et [!UICONTROL Ad Groups]*

Les vues personnalisées sont spécifiques à une vue unique (telle que la vue [!UICONTROL Portfolios]).

1. Au-dessus du tableau de données, cliquez sur le nom de la vue actuellement appliquée (![Vue](/help/search-social-commerce/assets/view.png "Vue")).

1. Cliquez sur **[!UICONTROL Create View]**.

1. Spécifiez les [paramètres d’affichage personnalisés](#view-settings-new-ui).

1. Enregistrez la vue :

   * Pour enregistrer la vue et l&#39;appliquer, cliquez sur **[!UICONTROL Save & Apply]**.

   * Pour enregistrer la vue sans l&#39;appliquer, cliquez sur **[!UICONTROL Save]**.

### (interface utilisateur héritée) Créer une vue personnalisée à partir d’une vue de gestion de campagne

Les vues personnalisées s&#39;appliquent uniquement aux vues de gestion de campagne.

1. Sur le côté droit de la barre d&#39;outils, au-dessus du tableau de données, cliquez sur le nom de la vue actuelle (qui peut être « [!UICONTROL Default] »).

1. Spécifiez les [paramètres d’affichage personnalisés](#view-settings).

1. Cliquez sur **[!UICONTROL Save as New]**.

1. Saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Utilisez un nom qui vous permet d’identifier l’onglet et les informations auxquelles il s’applique (telles que « Campagnes en pause » ou « Top 50 des publicités »).

## Modifier une vue par défaut ou personnalisée {#view-edit}

### (Nouvelle interface utilisateur) Modifier une vue par défaut ou personnalisée

*Disponible dans les vues [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] et [!UICONTROL Ad Groups]*

1. Au-dessus du tableau de données, cliquez sur le nom de la vue actuellement appliquée (![Vue](/help/search-social-commerce/assets/view.png "Vue")).

1. Si nécessaire, cliquez sur l’un des onglets ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] et [!UICONTROL From Others]) pour localiser la vue.

1. Placez le curseur sur le nom de la vue et cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png).

1. Modifiez le [paramètres d’affichage personnalisés](#view-settings-new-ui).

1. Enregistrez la vue :

   * Pour enregistrer les modifications sans les appliquer, cliquez sur **[!UICONTROL Save]**.

   * Pour enregistrer les modifications et les appliquer, cliquez sur **[!UICONTROL Apply]**.<!-- Should be Save & Apply -->

### (IU héritée) Modifier une vue par défaut ou personnalisée

1. Ouvrez les paramètres d’affichage :

   * (Si vous avez déjà appliqué la vue) Sur le côté droit de la barre d&#39;outils, au-dessus du tableau de données, cliquez sur le nom de la vue actuelle (qui peut être « [!UICONTROL Default] »).

   * (Vues personnalisées non appliquées) Dans le panneau de gauche, cliquez sur ![Vues personnalisées](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vues personnalisées") pour développer le menu [!UICONTROL Custom Views]. Cliquez sur le nom de la vue personnalisée.

1. Modifiez les [paramètres d’affichage](#view-settings).

   >[!NOTE]
   >
   >Vous pouvez appliquer les modifications apportées aux filtres à vos paramètres d’affichage par défaut, mais pas les enregistrer.

1. Appliquez ou enregistrez les paramètres :

   * Pour appliquer les paramètres temporairement sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply]**.

     Les paramètres sont appliqués à l’onglet jusqu’à ce que vous vous éloigniez de la vue de gestion de niveau supérieur ou (le cas échéant) [affichez les données pour un autre annonceur](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (Pour les vues par défaut et les vues personnalisées que vous avez créées) Pour enregistrer les paramètres dans la vue actuelle, cliquez sur **[!UICONTROL Save]**.

   * Pour enregistrer les paramètres dans une nouvelle vue personnalisée, cliquez sur **[!UICONTROL Save As]**. Dans la fenêtre [!UICONTROL Enter New Custom View Name], saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

## (Nouvelle interface utilisateur) Cloner une vue par défaut ou personnalisée {#view-clone}

*Disponible dans les vues [!UICONTROL Simulations], [!UICONTROL Portfolios], [!UICONTROL Campaigns] et [!UICONTROL Ad Groups]*

1. Au-dessus du tableau de données, cliquez sur le nom de la vue actuellement appliquée (![Vue](/help/search-social-commerce/assets/view.png "Vue")).

1. Si nécessaire, cliquez sur l’un des onglets ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] et [!UICONTROL From Others]) pour localiser la vue.

1. Placez le curseur sur le nom de la vue et cliquez sur ![Cloner](/help/search-social-commerce/assets/clone-new.png).

1. Saisissez un nouveau nom d’affichage et modifiez les [paramètres d’affichage personnalisés](#view-settings-new-ui) selon vos besoins.

1. Enregistrez la vue :

   * Pour enregistrer la vue et l&#39;appliquer, cliquez sur **[!UICONTROL Save & Apply]**.

   * Pour enregistrer la vue sans l&#39;appliquer, cliquez sur **[!UICONTROL Save]**.

## Réinitialiser une vue par défaut aux paramètres système par défaut

La restauration des paramètres d&#39;affichage par défaut supprime tous les paramètres que vous avez enregistrés et réapplique les paramètres système par défaut.

Les paramètres système par défaut varient selon la vue de gestion. Pour la plupart des vues de gestion, la vue système par défaut affiche les données du jour précédent pour les éléments des comptes activés et actifs (par exemple, uniquement les groupes d’annonces actifs dans les campagnes actives), avec les données triées par coût et avec les données de conversion basées sur la date de transaction.

* Dans la nouvelle interface utilisateur :

   1. Au-dessus du tableau de données, cliquez sur le nom de la vue actuellement appliquée (![Vue](/help/search-social-commerce/assets/view.png "Vue")).

   1. Si nécessaire, cliquez sur l’un des onglets ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] et [!UICONTROL From Others]) pour localiser la vue.

   1. Placez le curseur sur le nom de la vue et cliquez sur ![Rétablir](/help/search-social-commerce/assets/revert-new.png).

* Depuis les vues de gestion de campagne héritées :

   1. Dans le panneau de gauche, cliquez sur ![Vues personnalisées](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vues personnalisées") pour développer le menu [!UICONTROL Custom Views].

      Les vues sont triées par entité applicable.

   1. En regard du nom de l’affichage, cliquez sur ![Restaurer les paramètres par défaut](/help/search-social-commerce/assets/restore.png "Restaurer les paramètres par défaut").

## Suppression d’une vue personnalisée

Vous pouvez supprimer n’importe quelle vue personnalisée que vous avez créée.

Si vous supprimez une vue personnalisée appliquée à l’onglet actif, l’onglet continue d’afficher la vue personnalisée jusqu’à ce que vous vous déplaciez en dehors du jeu de vues (par exemple, des vues du menu [!UICONTROL Search] au menu [!UICONTROL Reports]) ou (le cas échéant) lorsque vous [affichez les données pour un autre annonceur](/help/search-social-commerce/common-tasks/change-advertiser.md).

* Dans la nouvelle interface utilisateur :

   1. Au-dessus du tableau de données, cliquez sur le nom de la vue actuellement appliquée (![Vue](/help/search-social-commerce/assets/view.png "Vue")).

   1. Si nécessaire, cliquez sur l’un des onglets ([!UICONTROL All Views], [!UICONTROL Private], [!UICONTROL Shared by Me] et [!UICONTROL From Others]) pour localiser la vue.

   1. Placez le curseur sur le nom de la vue et cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png).

   1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

* Depuis les vues de gestion de campagne héritées :

   1. Dans le panneau de gauche, cliquez sur ![Vues personnalisées](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vues personnalisées") pour développer le menu [!UICONTROL Custom Views].

   1. Placez le curseur sur le nom de la vue personnalisée, puis cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

   1. Dans le message de confirmation, cliquez sur **[!UICONTROL Continue]**.

## Paramètres d’affichage par défaut et personnalisés

<!-- Simplify attribution rule definitions here and elsewhere and include links to "How attribution rules are calculated -->

### (Nouvelle interface utilisateur) Paramètres d’affichage par défaut et personnalisés {#view-settings-new-ui}

| **Tabulation** | **Champ** | **Description** |
| --- | --- | --- |
| [Avant tout, onglets] | Nom | Nom unique de la vue. Vous ne pouvez pas modifier le nom d&#39;une vue par défaut.<p><b>Conseil :</b> utilisez un nom qui vous aide à identifier l’onglet et les informations auxquelles il s’applique (telles que « Campagnes en pause » ou « Top 50 des publicités »). |
|   | Partager avec d’autres utilisateurs | (Vues personnalisées uniquement ; facultatif) Rend la vue disponible pour tous les autres utilisateurs qui peuvent afficher les données de l’annonceur. Les autres utilisateurs ne peuvent pas modifier ni supprimer la vue, mais ils peuvent en créer une nouvelle à partir des paramètres. |
| Colonnes | Colonnes et classement sélectionnés | Les colonnes de données affichées et leur ordre :<ul><li> (Pour ajouter une colonne) Dans la liste Colonnes disponibles, cliquez sur le nom d&#39;une colonne, puis faites-la glisser dans la liste Colonnes et classement sélectionnées ou cliquez sur ![flèche de droite](/help/search-social-commerce/assets/chevron-right.png) pour la déplacer.</li><li>(Pour modifier la position horizontale d’une colonne) Dans la liste Colonnes et ordre sélectionnées, cliquez sur le nom de la colonne, puis faites-la glisser à la position souhaitée ou cliquez sur ![flèche vers le haut](/help/search-social-commerce/assets/chevron-up.png) ou ![flèche vers le bas](/help/search-social-commerce/assets/chevron-down.png) pour la déplacer. Le nom de la colonne supérieure s’affiche dans la colonne de gauche.</li><li>(Pour supprimer une colonne) Dans la liste Colonnes et classement sélectionnées, cliquez sur le nom d’une colonne, puis faites-la glisser dans la liste Colonnes disponibles ou cliquez sur ![flèche à gauche](/help/search-social-commerce/assets/chevron-left.png) pour la déplacer.</li></ul><b>Filtrer les données</b><p>Pour répertorier uniquement un type de données spécifique, cliquez sur l’une des icônes en regard de la liste :<ul><li>![icône de propriétés](/help/search-social-commerce/assets/properties-icon-new.png) pour les noms et identifiants de propriété, tels que [!UICONTROL Portfolio Name] ou [!UICONTROL Status]</li><li>![&#x200B; icône de trafic &#x200B;](/help/search-social-commerce/assets/traffic-metrics-icon-new.png) pour les mesures de trafic standard, telles que les impressions et les clics</li><li>![icône de chiffre d’affaires](/help/search-social-commerce/assets/revenue-metrics-icon-new.png) (pour les mesures de conversion suivies pour l’annonceur, y compris les mesures de conversion et d’engagement du site synchronisées à partir d’Analytics)</li><li>![&#x200B; icône personnalisée &#x200B;](/help/search-social-commerce/assets/custom-metrics-icon-new.png) (pour les mesures personnalisées créées par l’annonceur)</li><li>![icône de classification](/help/search-social-commerce/assets/classifications-icon-new.png) (pour les classifications de libellés).</li></ul> <b>Remarques complémentaires :</b><ul><li>Pour ajouter, créer ou modifier des mesures, reportez-vous aux sections « [Créer une mesure personnalisée &#x200B;](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) », « [Modifier une mesure personnalisée &#x200B;](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) » et « [Supprimer une mesure personnalisée](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md) ».</li><li>Si l&#39;état inclut des données pour des comptes avec différentes devises, les totaux ne sont pas inclus pour les colonnes monétaires (telles que Coût et CPC).</li><li>Vous pouvez [modifier temporairement le jeu de colonnes à partir du menu d’en-tête de colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) et [modifier et trier le jeu de colonnes à partir de l’icône [!UICONTROL Columns]](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![icône Colonnes](/help/search-social-commerce/assets/custom-columns.png "icône Colonnes")).</li></ul> |
|   | Trier par | Colonne selon laquelle trier les données. La valeur par défaut est différente pour chaque type de rapport. |
|   | Ordre de tri | Permet de trier les données par ordre **croissant** ou **décroissant**. |
| Filtres | [Définitions de filtre] | (Facultatif) Filtres à appliquer aux données. L’application de filtres renvoie des lignes uniquement lorsque la valeur d’une colonne répond à des critères spécifiés.<p>Pour chaque filtre à appliquer :<ol><li>Dans le menu [!UICONTROL Add Filter], sélectionnez un nom de colonne. La liste comprend toutes les colonnes disponibles et est triée par type de colonne, en commençant par les colonnes de propriété.</li><li>Définir le filtre sur la colonne</li></ol>(Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, puis saisissez la valeur applicable. Les valeurs ne respectent pas la casse.<p>Par exemple, si vous avez sélectionné la colonne « Clics » et que vous souhaitez renvoyer uniquement les lignes contenant plus de 100 clics, sélectionnez _\>_ et saisissez `100` dans le champ de saisie.<p>Selon le type de données, les opérateurs disponibles peuvent inclure <i>supérieur à</i>, <i>inférieur à</i>, <i>égal à</i>, <i>contient</i>, <i>ne contient pas</i>, <i>commence par</i>, <i>se termine par</i>,<i>aucune valeur</i>, ou <i>a une valeur</i> <i>avant</i>, <i>après</i> ou <i>aucune date</i>.<p>(Filtres sans champs de saisie) Cliquez sur ![flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png) en regard du menu Sélectionner des éléments de liste, puis cochez les cases en regard de chaque valeur à inclure.<p><b>Remarques :</b><ul><li>Vous pouvez appliquer les modifications apportées aux filtres à vos paramètres d’affichage par défaut, mais pas les enregistrer.</li><li>Vous pouvez également [modifier temporairement les filtres applicables](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) dans la vue.</li></ul> |
| Configurations supplémentaires | Période | (Lorsque « Inclure la période » est sélectionné)<p>Période pour laquelle générer des données. Choisir une option :<ul><li><i>[Plage prédéfinie]</i> : liste des incréments horaires courants, allant de <i>Aujourd&#39;hui</i> à <i>Les 180 derniers jours</i>. Choisissez-en un dans la liste ; la valeur par défaut est <i>Hier</i>. Remarque : <i>Mois dernier</i>, <i>3 derniers mois</i> et <i>6 derniers mois</i> affichent les données des mois civils précédents.</li><li><i>Période personnalisée :</i> spécifiez la date de début et la date de fin. Saisissez les dates au format MM/JJ/AAAA ou MM/JJ/AAAA, ou cliquez sur ![icône de calendrier](/help/search-social-commerce/assets/calendar.png) en regard d’un champ et sélectionnez une date.</li></ul> |
|   | Comparaison | Compare les données de la période spécifiée aux données d’une seconde période. Lorsque vous sélectionnez cette option, spécifiez la deuxième période. Deux colonnes supplémentaires sont ajoutées pour chaque colonne de données standard. Par exemple, au lieu d’inclure une seule colonne pour « Impressions », le rapport inclut des colonnes pour « Plage d’impressions 1 », « Plage d’impressions 2 » et « Différence d’impressions ».<p><b>Remarques :</b><ul><li>La colonne de différence n’est pas affichée pour les mesures dérivées.</li><li>La génération des rapports qui comparent des périodes volumineuses peut prendre plus de temps.</li></ul> |
|   | Format de comparaison | (Lorsque [!UICONTROL Comparison] est activé) Comment exprimer la différence entre les données des deux périodes sélectionnées dans la colonne « [_Champ de données_] Différence ». Choisir une option :<ul><li><i>Variance</i> (valeur par défaut) : affiche la différence sous forme de valeur numérique.</li><li><i>% Change </i> : affiche la différence en pourcentage.</li></ul> |
|   | Règle d’attribution | (Publicitaires avec le service de suivi des conversions en pixels d’Adobe Advertising uniquement) Dans l’onglet, comment attribuer des données de conversion, potentiellement sur plusieurs canaux et portfolios publicitaires, dans une série d’événements qui conduisent à une conversion. Par défaut, la règle spécifiée dans les paramètres d’attribution de conversion au niveau de l’annonceur est sélectionnée.<ul><li> <i>Premier événement</i> : attribue la conversion au premier clic payant de la série dans l’intervalle de recherche en amont de clic de l’annonceur ou, en l’absence de clics payants, à la dernière impression dans l’intervalle de recherche en amont d’impression de l’annonceur.</li><li><i>Poids du premier événement en plus</i> : attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont de clics et l’intervalle de recherche en amont d’impressions de l’annonceur, mais donne le plus de poids au premier événement et successivement moins de poids aux événements suivants. Lorsque la conversion est précédée à la fois par des clics payés et des impressions, le poids de remplacement d’impression spécifié est ensuite appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids de visionnage de l’annonceur plutôt qu’en fonction du poids de remplacement de l’impression.</li><li><i>Distribution des événements</i> : attribue la conversion de manière égale à chaque événement de la série qui s’est produit dans l’intervalle de recherche en amont de clics et l’intervalle de recherche en amont d’impressions de l’annonceur. Lorsque la conversion est précédée à la fois par des clics payés et des impressions, le poids de remplacement d’impression spécifié est ensuite appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids de visionnage de l’annonceur plutôt qu’en fonction du poids de remplacement de l’impression.</li><li><i>Poids du dernier événement en plus</i> : attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont de clics et l’intervalle de recherche en amont d’impressions de l’annonceur, mais donne le plus de poids au dernier événement et successivement moins de poids aux événements précédents. Lorsque la conversion est précédée à la fois par des clics payés et des impressions, le poids de remplacement d’impression spécifié est ensuite appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids de visionnage de l’annonceur plutôt qu’en fonction du poids de remplacement de l’impression.</li><li><i>Dernier événement</i> (valeur par défaut) : attribue la conversion au dernier clic payant de la série dans l’intervalle de recherche en amont du clic de l’annonceur ou, en l’absence de clics payants, à la dernière impression dans l’intervalle de recherche en amont de l’impression de l’annonceur.</li><li><i>En forme de U</i> : attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont de clics et l’intervalle de recherche en amont d’impressions de l’annonceur, mais donne le plus de poids au premier événement et aux derniers événements, avec successivement moins de poids aux événements au milieu du chemin de conversion. Lorsque la conversion est précédée à la fois par des clics payés et des impressions, le poids de remplacement d’impression spécifié est ensuite appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids de visionnage de l’annonceur plutôt qu’en fonction du poids de remplacement de l’impression.</li></ul><p><b>Remarques :</b><ul><li>Toutes les règles d’attribution, à l’exception du dernier événement, sont disponibles uniquement pour les annonceurs avec le suivi des clics Adobe Advertising et le suivi des conversions à partir d’Adobe Advertising ou d’Adobe Analytics (avec une intégration d’Analytics).</li><li>Les règles d’attribution s’appliquent aux clics sur les annonces publicitaires payantes dans n’importe quel canal. Elles ne s’appliquent pas aux impressions pour les annonces de référencement payant, qui ne peuvent pas être suivies au niveau de l’événement.</li><li>Lorsque vous signalez des données de conversion à l’aide de n’importe quelle règle d’attribution sauf l’une des règles « Dernier événement », les événements menant à la conversion peuvent se produire sur plusieurs portefeuilles. Lorsque c’est le cas, la vue inclut des données pour la conversion uniquement lorsque les publicités ou les mots-clés de ces portefeuilles sont inclus dans la vue.</li><li>Pour les vues par défaut, nous vous recommandons de conserver la règle d’attribution par défaut, qui est utilisée pour calculer la [valeur de l’objectif](/help/search-social-commerce/glossary.md#o-p) (anciennement appelée « revenu pondéré ») pour chaque unité d’offre lors de l’optimisation des offres.</li></ul> |
|   | Conversions basées sur | Comment générer des rapports sur les données de conversion :<ul><li><i>Date du clic</i> : pour afficher les transactions générées par un clic survenu au cours de la période indiquée. Lorsqu’un portefeuille présente un retard important entre les clics et les transactions, cette option est utile pour calculer le chiffre d’affaires historique par clic pour le portefeuille, qui indique les comportements de chiffre d’affaires à attendre au fil du temps.</li><li><i>Date de transaction</i> (valeur par défaut) : pour afficher les transactions dont la date de transaction s&#39;est produite au cours de la période indiquée. Indique le montant des revenus générés au cours de la période spécifiée.</li></ul> |

### (IU héritée) Paramètres d’affichage par défaut et personnalisés {#view-settings}

| **Tabulation** | **Champ** | **Description** |
| --- | --- | --- |
| [Avant tout, onglets] | Nom | Nom unique de la vue. Vous ne pouvez pas modifier le nom d&#39;une vue par défaut.<p><b>Conseil :</b> utilisez un nom qui vous aide à identifier l’onglet et les informations auxquelles il s’applique (telles que « Campagnes en pause » ou « Top 50 des publicités »). |
|   | Vue universelle | (Lecture seule pour les vues existantes) Rend les paramètres de données disponibles dans toutes les vues d’entité (pour les campagnes, les publicités, etc.). Les vues universelles peuvent inclure des colonnes de classification de mesures et d&#39;étiquettes, mais pas des colonnes de propriétés (telles que le nom et le statut de l&#39;entité), car elles diffèrent selon le type d&#39;entité, ni aucun autre attribut de vue. Tous les critères de filtre sont appliqués à la vue d’entité, le cas échéant, et sont ignorés dans les autres cas. Tous les filtres de mesure sont évalués localement (par exemple, pour les clics \> 1 000, les vues Campagnes affichent les campagnes avec plus de 1 000 clics et la vue Groupes publicitaires affiche les groupes publicitaires avec plus de 1 000 clics).<p>Les colonnes de propriétés d&#39;une vue universelle sont extraites de la vue par défaut de l&#39;entité. Vous pouvez modifier les colonnes de propriétés par défaut pour une entité spécifique dans les paramètres d&#39;affichage par défaut.<p>Une fois que vous avez activé ou désactivé cette option, vous ne pouvez pas enregistrer la modification dans l&#39;affichage existant, mais vous pouvez créer un nouvel affichage avec la modification. |
|   | Partager | (Vues personnalisées existantes uniquement ; facultatif) Rend la vue disponible pour tous les autres utilisateurs qui peuvent afficher les données de l’annonceur. Les autres utilisateurs ne peuvent pas modifier ni supprimer la vue, mais ils peuvent en créer une nouvelle à partir des paramètres. Dans vos listes d’affichages, chaque affichage partagé par une autre personne est en italique, par exemple « _Campagnes les plus performantes_ ». |
| Colonnes | Colonnes et classement sélectionnés | Les colonnes de données affichées et leur ordre :<ul><li> (Pour ajouter une colonne) Dans la liste Colonnes disponibles, cliquez sur le nom d&#39;une colonne, puis faites-la glisser dans la liste Colonnes et classement sélectionnées ou cliquez sur ![flèche de droite](/help/search-social-commerce/assets/chevron-right.png) pour la déplacer.</li><li>(Pour modifier la position horizontale d’une colonne) Dans la liste Colonnes et ordre sélectionnées, cliquez sur le nom de la colonne, puis faites-la glisser à la position souhaitée ou cliquez sur ![flèche vers le haut](/help/search-social-commerce/assets/chevron-up.png) ou ![flèche vers le bas](/help/search-social-commerce/assets/chevron-down.png) pour la déplacer. Le nom de la colonne supérieure s’affiche dans la colonne de gauche.</li><li>(Pour supprimer une colonne) Dans la liste Colonnes et classement sélectionnées, cliquez sur le nom d’une colonne, puis faites-la glisser dans la liste Colonnes disponibles ou cliquez sur ![flèche à gauche](/help/search-social-commerce/assets/chevron-left.png) pour la déplacer.</li></ul><b>Filtrer les données</b><p>Pour répertorier uniquement un type de données spécifique, cliquez sur l’une des icônes en regard de la liste :<ul><li>![icône de propriétés](/help/search-social-commerce/assets/properties-icon.png) pour les noms de propriété et les identifiants des composants de recherche, tels que l’état</li><li>![&#x200B; icône de trafic &#x200B;](/help/search-social-commerce/assets/traffic-metrics-icon.png) pour les mesures de trafic standard, telles que les impressions et les clics</li><li>![icône de chiffre d’affaires](/help/search-social-commerce/assets/revenue-metrics-icon.png) (pour les mesures de conversion suivies pour l’annonceur, y compris les mesures de conversion et d’engagement du site synchronisées à partir d’Analytics)</li><li>![&#x200B; icône personnalisée &#x200B;](/help/search-social-commerce/assets/custom-metrics-icon.png) (pour les mesures dérivées personnalisées créées par l’annonceur)</li><li>![icône de classification](/help/search-social-commerce/assets/classifications-icon.png) (pour les classifications de libellés).</li></ul> <b>Remarques complémentaires :</b><ul><li>Pour ajouter, créer ou modifier des mesures, reportez-vous aux sections « [Créer une mesure personnalisée &#x200B;](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) », « [Modifier une mesure personnalisée &#x200B;](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) » et « [Supprimer une mesure personnalisée](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-delete.md) ».</li><li>Si l&#39;état inclut des données pour des comptes avec différentes devises, les totaux ne sont pas inclus pour les colonnes monétaires (telles que Coût et CPC).</li><li>Vous pouvez [modifier temporairement le jeu de colonnes à partir du menu d’en-tête de colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) et [modifier et trier le jeu de colonnes à partir de l’icône [!UICONTROL Columns]](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![icône Colonnes](/help/search-social-commerce/assets/custom-columns.png "icône Colonnes")).</li></ul> |
|   | Trier par | Colonne selon laquelle trier les données. La valeur par défaut est différente pour chaque type de rapport. |
|   | Ordre de tri | Permet de trier les données par ordre **croissant** ou **décroissant**. Déplacez le curseur pour sélectionner une option. |
| Filtres | [Définitions de filtre] | (Facultatif) Filtres à appliquer aux données. L’application de filtres renvoie des lignes uniquement lorsque la valeur d’une colonne répond à des critères spécifiés.<p>Pour chaque filtre à appliquer :<ol><li>Dans le menu [!UICONTROL Add Filter], sélectionnez un nom de colonne. La liste comprend toutes les colonnes disponibles et est triée par type de colonne, en commençant par les colonnes de propriété.</li><li>Définir le filtre sur la colonne</li></ol>(Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, puis saisissez la valeur applicable. Les valeurs ne respectent pas la casse.<p>Par exemple, si vous avez sélectionné la colonne « Clics » et que vous souhaitez renvoyer uniquement les lignes contenant plus de 100 clics, sélectionnez _\>_ et saisissez `100` dans le champ de saisie.<p>Selon le type de données, les opérateurs disponibles peuvent inclure <i>supérieur à</i>, <i>inférieur à</i>, <i>égal à</i>, <i>contient</i>, <i>ne contient pas</i>, <i>commence par</i>, <i>se termine par</i>,<i>aucune valeur</i>, ou <i>a une valeur</i> <i>avant</i>, <i>après</i> ou <i>aucune date</i>.<p>(Filtres sans champs de saisie) Cliquez sur ![flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png) en regard du menu Sélectionner des éléments de liste, puis cochez les cases en regard de chaque valeur à inclure.<p><b>Remarques :</b><ul><li>Vous pouvez appliquer les modifications apportées aux filtres à vos paramètres d’affichage par défaut, mais pas les enregistrer.</li><li>Vous pouvez également [modifier temporairement les filtres applicables](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) dans la vue.</li></ul> |
|   | Inclure les lignes avec les données de performances uniquement | (vues Groupes publicitaires, Mot-clé, Groupes de produits, Emplacements et Cibles automatiques uniquement) <p>Inclut uniquement les lignes contenant des données de performances aux dates spécifiées. Par défaut, cette option est sélectionnée pour réduire le temps de chargement de la page. <p><b>Avertissement </b> : si vous désélectionnez cette option et que la vue contient de nombreuses entités sans données de performances, l&#39;affichage des données prend plus de temps.<p> <b>Remarque </b> : vous pouvez appliquer les modifications apportées aux filtres à vos paramètres d’affichage par défaut, mais pas les enregistrer. Les vues par défaut affichent toujours uniquement les entités avec des données de performances. |
| Date | Période | (Lorsque « Inclure la période » est sélectionné)<p>Période pour laquelle générer des données. Choisir une option :<ul><li><i>[Plage prédéfinie]</i> : liste des incréments horaires courants, allant de <i>Aujourd&#39;hui</i> à <i>Les 180 derniers jours</i>. Choisissez-en un dans la liste ; la valeur par défaut est <i>Hier</i>. Remarque : <i>Mois dernier</i>, <i>3 derniers mois</i> et <i>6 derniers mois</i> affichent les données des mois civils précédents.</li><li><i>Période personnalisée :</i> spécifiez la date de début et la date de fin. Saisissez les dates au format MM/JJ/AAAA ou MM/JJ/AAAA, ou cliquez sur ![icône de calendrier](/help/search-social-commerce/assets/calendar.png) en regard d’un champ et sélectionnez une date.</li></ul> |
|   | Comparaison | Compare les données de la période spécifiée aux données d’une seconde période. Lorsque vous sélectionnez cette option, spécifiez la deuxième période. Deux colonnes supplémentaires sont ajoutées pour chaque colonne de données standard. Par exemple, au lieu d’inclure une seule colonne pour « Impressions », le rapport inclut des colonnes pour « Plage d’impressions 1 », « Plage d’impressions 2 » et « Différence d’impressions ».<p><b>Remarques :</b><ul><li>La colonne de différence n’est pas affichée pour les mesures dérivées.</li><li>La génération des rapports qui comparent des périodes volumineuses peut prendre plus de temps.</li></ul> |
|   | Format de comparaison | (Lorsque [!UICONTROL Comparison] est activé) Comment exprimer la différence entre les données des deux périodes sélectionnées dans la colonne « [_Champ de données_] Différence ». Choisir une option :<ul><li><i>Variance</i> (valeur par défaut) : affiche la différence sous forme de valeur numérique.</li><li><i>% Change </i> : affiche la différence en pourcentage.</li></ul> |
| Configurations supplémentaires | Utiliser la valeur par défaut | Applique les paramètres d’attribution spécifiés dans les paramètres d’attribution de conversion au niveau de l’annonceur. |
|   | Règle d’attribution | (Publicitaires avec le service de suivi des conversions en pixels d’Adobe Advertising uniquement) Dans l’onglet, comment attribuer des données de conversion, potentiellement sur plusieurs canaux et portfolios publicitaires, dans une série d’événements qui conduisent à une conversion. Par défaut, la règle spécifiée dans les paramètres d’attribution de conversion au niveau de l’annonceur est sélectionnée.<ul><li> <i>Premier événement</i> : attribue la conversion au premier clic payant de la série dans l’intervalle de recherche en amont de clic de l’annonceur ou, en l’absence de clics payants, à la dernière impression dans l’intervalle de recherche en amont d’impression de l’annonceur.</li><li><i>Poids du premier événement en plus</i> : attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont de clics et l’intervalle de recherche en amont d’impressions de l’annonceur, mais donne le plus de poids au premier événement et successivement moins de poids aux événements suivants. Lorsque la conversion est précédée à la fois par des clics payés et des impressions, le poids de remplacement d’impression spécifié est ensuite appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids de visionnage de l’annonceur plutôt qu’en fonction du poids de remplacement de l’impression.</li><li><i>Distribution des événements</i> : attribue la conversion de manière égale à chaque événement de la série qui s’est produit dans l’intervalle de recherche en amont de clics et l’intervalle de recherche en amont d’impressions de l’annonceur. Lorsque la conversion est précédée à la fois par des clics payés et des impressions, le poids de remplacement d’impression spécifié est ensuite appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids de visionnage de l’annonceur plutôt qu’en fonction du poids de remplacement de l’impression.</li><li><i>Poids du dernier événement en plus</i> : attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont de clics et l’intervalle de recherche en amont d’impressions de l’annonceur, mais donne le plus de poids au dernier événement et successivement moins de poids aux événements précédents. Lorsque la conversion est précédée à la fois par des clics payés et des impressions, le poids de remplacement d’impression spécifié est ensuite appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids de visionnage de l’annonceur plutôt qu’en fonction du poids de remplacement de l’impression.</li><li><i>Dernier événement</i> (valeur par défaut) : attribue la conversion au dernier clic payant de la série dans l’intervalle de recherche en amont du clic de l’annonceur ou, en l’absence de clics payants, à la dernière impression dans l’intervalle de recherche en amont de l’impression de l’annonceur.</li><li><i>En forme de U</i> : attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont de clics et l’intervalle de recherche en amont d’impressions de l’annonceur, mais donne le plus de poids au premier événement et aux derniers événements, avec successivement moins de poids aux événements au milieu du chemin de conversion. Lorsque la conversion est précédée à la fois par des clics payés et des impressions, le poids de remplacement d’impression spécifié est ensuite appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids de visionnage de l’annonceur plutôt qu’en fonction du poids de remplacement de l’impression.</li></ul><p><b>Remarques :</b><ul><li>Toutes les règles d’attribution, à l’exception du dernier événement, sont disponibles uniquement pour les annonceurs avec le suivi des clics Adobe Advertising et le suivi des conversions à partir d’Adobe Advertising ou d’Adobe Analytics (avec une intégration d’Analytics).</li><li>Les règles d’attribution s’appliquent aux clics sur les annonces publicitaires payantes dans n’importe quel canal. Elles ne s’appliquent pas aux impressions pour les annonces de référencement payant, qui ne peuvent pas être suivies au niveau de l’événement.</li><li>Lorsque vous signalez des données de conversion à l’aide de n’importe quelle règle d’attribution sauf l’une des règles « Dernier événement », les événements menant à la conversion peuvent se produire sur plusieurs portefeuilles. Lorsque c’est le cas, la vue inclut des données pour la conversion uniquement lorsque les publicités ou les mots-clés de ces portefeuilles sont inclus dans la vue.</li><li>Pour les vues par défaut, nous vous recommandons de conserver la règle d’attribution par défaut, qui est utilisée pour calculer la [valeur de l’objectif](/help/search-social-commerce/glossary.md#o-p) (anciennement appelée « revenu pondéré ») pour chaque unité d’offre lors de l’optimisation des offres.</li></ul> |
|   | Conversions basées sur | Comment générer des rapports sur les données de conversion :<ul><li><i>Date du clic</i> : pour afficher les transactions générées par un clic survenu au cours de la période indiquée. Lorsqu’un portefeuille présente un retard important entre les clics et les transactions, cette option est utile pour calculer le chiffre d’affaires historique par clic pour le portefeuille, qui indique les comportements de chiffre d’affaires à attendre au fil du temps.</li><li><i>Date de transaction</i> (valeur par défaut) : pour afficher les transactions dont la date de transaction s&#39;est produite au cours de la période indiquée. Indique le montant des revenus générés au cours de la période spécifiée.</li></ul> |
