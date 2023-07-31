---
title: Gestion des vues par défaut et personnalisées
description: Découvrez comment personnaliser vos vues par défaut et vos vues personnalisées.
exl-id: b28f58f6-c80a-45f8-8c5f-b821a76dab6d
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '2833'
ht-degree: 0%

---

# Gestion des vues par défaut et personnalisées

Vos vues par défaut et personnalisées vous permettent de personnaliser les données de performances affichées dans les vues de données de campagne de recherche. Les paramètres d’affichage incluent les colonnes à inclure, les filtres, la période, les paramètres d’attribution de conversion et d’autres paramètres avancés. Vous pouvez alors appliquer ces paramètres temporairement ou les enregistrer. (Exception : vous ne pouvez pas enregistrer de filtres pour les vues par défaut.) Chaque vue personnalisée par défaut et ordinaire s’applique à une vue d’entité spécifique (telle que [!UICONTROL Campaigns]) et un compte publicitaire spécifique uniquement. Chaque vue personnalisée universelle est applicable à l’échelle des vues d’entité pour un annonceur spécifique et ne peut donc pas inclure de colonnes de propriétés (telles que le nom ou l’état de l’entité), qui varient selon le type d’entité.

Les vues par défaut s’affichent par défaut chaque fois que vous vous connectez. Vous pouvez créer d’autres vues personnalisées et les appliquer à tout moment. Vous pouvez éventuellement partager avec tous les autres utilisateurs qui peuvent afficher les données de l’annonceur toute vue personnalisée que vous créez. Dans vos listes de vues, chaque vue partagée par une autre personne est mise en italique, par exemple : &quot;*Campagnes les plus performantes*.&quot; Seule la personne qui crée une vue personnalisée peut la supprimer.

Chaque vue est disponible sous forme de raccourci dans la [!UICONTROL Custom Views] dans le panneau de gauche.

## Application d’une vue par défaut ou personnalisée

* (Vues par défaut) Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]** \> **\[type d’entité\]**.

* (Vues personnalisées) Dans le panneau de navigation de gauche :

   1. Dans le panneau de gauche, cliquez sur le **[!UICONTROL Custom Views]** pour l’agrandir.

      Les vues sont triées par entité applicable.

   1. Développez les menus disponibles.

      &quot;[!UICONTROL Universal Views]&quot; inclut des vues personnalisées qui peuvent être utilisées dans toutes les vues d’entité. Toutes les autres vues personnalisées sont regroupées par type d’entité.

   1. Cliquez sur le nom de la vue.

      Si la vue est universelle ou s’applique à l’entité actuelle, le tableau de données est réaffiché selon la configuration de la vue. Si la vue s’applique à une autre entité, les données de l’entité concernée sont affichées en fonction de la configuration de la vue.

## Création d’une vue personnalisée {#create-custom-view}

Les vues personnalisées s’appliquent uniquement aux vues de gestion de campagne.

>[!NOTE]
>
>Outre les paramètres d’affichage que vous spécifiez pour la vue personnalisée, l’ordre de tri des colonnes actuelles est également enregistré.

1. Dans la partie droite de la barre d’outils située au-dessus du tableau de données, cliquez sur le nom de la vue actuelle (qui peut être &quot;[!UICONTROL Default]&quot;).

1. Spécifiez la variable [paramètres d’affichage personnalisés](#view-settings):

   1. (Facultatif) Pour rendre les paramètres de données disponibles pour toutes les vues d’entité (pour [!UICONTROL Campaigns], [!UICONTROL Ads], etc.), sélectionnez **[!UICONTROL Universal View]**.

      Une fois cette option activée ou désactivée, vous ne pouvez pas enregistrer la modification dans la vue existante, mais vous pouvez créer une nouvelle vue avec la modification.

   1. (Facultatif) Pour mettre la vue à la disposition de tous les autres utilisateurs qui peuvent afficher les données de l’annonceur, déplacez le **[!UICONTROL Shared]** curseur vers *[!UICONTROL Yes]*.

   1. (Facultatif) Sur la page **[!UICONTROL Columns]** , modifiez les colonnes disponibles pour l’onglet, leur ordre et la manière de trier les lignes.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Filters]** puis spécifiez les filtres à appliquer.

      L’application de filtres renvoie des lignes uniquement lorsque la valeur d’une mesure répond à des critères spécifiés, que la mesure soit incluse ou non en tant que colonne dans le rapport.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Date]** et modifiez les paramètres de date par défaut.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Additional Settings]** et modifiez les paramètres.

1. Cliquez sur **[!UICONTROL Save as New]**.

1. Saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Utilisez un nom qui vous aidera à identifier l’onglet et les informations auxquelles il s’applique (par exemple, &quot;Campagnes en pause&quot; ou &quot;50 meilleures publicités&quot;).

### Modification d’une vue par défaut ou personnalisée

1. Ouvrez les paramètres d’affichage :

   * (Si vous avez déjà appliqué la vue) Dans la partie droite de la barre d’outils au-dessus du tableau de données, cliquez sur le nom de la vue actuelle (qui peut être &quot;[!UICONTROL Default]&quot;).

   * (Vues personnalisées qui ne sont pas appliquées) Dans le panneau de gauche, cliquez sur ![Vues personnalisées](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vues personnalisées") pour développer la variable [!UICONTROL Custom Views] . Cliquez sur le nom de la vue personnalisée.

1. Modifiez la variable [paramètres d’affichage](#view-settings):

   1. (Facultatif) Pour activer ou désactiver les paramètres de données dans toutes les vues d’entités de recherche (pour [!UICONTROL Campaigns], [!UICONTROL Ad Groups], etc.), sélectionnez ou désélectionnez **[!UICONTROL Universal View]**.

      Vous ne pouvez pas enregistrer la modification dans la vue existante, mais vous pouvez créer une nouvelle vue avec la modification.

   1. (Facultatif ; vues personnalisées que vous avez créées uniquement) Si la vue n’est pas déjà publique, rendez-la disponible pour tous les autres utilisateurs qui peuvent afficher les données de l’annonceur en déplaçant la variable **[!UICONTROL Shared]** curseur vers *[!UICONTROL Yes]*.

   1. (Facultatif) Sur la page **[!UICONTROL Columns]** , modifiez les colonnes disponibles pour l’onglet, leur ordre et la manière de trier les lignes.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Filters]** puis éditez les filtres à appliquer.

      L’application de filtres renvoie des lignes uniquement lorsque la valeur d’une mesure répond à des critères spécifiés, que la mesure soit incluse ou non en tant que colonne dans le rapport.

      >[!NOTE]
      >
      >Vous pouvez appliquer les modifications apportées aux filtres, mais pas les enregistrer, aux paramètres d’affichage par défaut.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Date]** et modifiez les paramètres de date par défaut.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Additional Settings]** et modifiez les paramètres.

1. Appliquez ou enregistrez les paramètres :

   * Pour appliquer temporairement les paramètres sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply]**.

     Les paramètres sont appliqués à l’onglet jusqu’à ce que vous quittiez la vue de gestion de niveau supérieur ou (le cas échéant). [afficher les données d’un autre annonceur ;](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (Pour les vues par défaut et les vues personnalisées que vous avez créées) Pour enregistrer les paramètres dans la vue actuelle, cliquez sur **[!UICONTROL Save]**.

   * Pour enregistrer les paramètres dans une nouvelle vue personnalisée, cliquez sur **[!UICONTROL Save As]**. Dans le [!UICONTROL Enter New Custom View Name] , saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

## Réinitialisation d’une vue par défaut sur les paramètres par défaut du système

La restauration des paramètres d’affichage par défaut supprime tous les paramètres enregistrés et réapplique les paramètres par défaut du système.

Les paramètres par défaut du système varient selon les onglets. Pour la plupart des onglets, la vue par défaut du système affiche les données de la veille pour les éléments des comptes activés et qui sont principaux (par exemple, seuls les groupes publicitaires principaux des principales campagnes), les données étant triées par coût et les données de conversion basées sur la date de transaction.

1. Dans le panneau de gauche, cliquez sur ![Vues personnalisées](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vues personnalisées") pour développer la variable [!UICONTROL Custom Views] .

   Les vues sont triées par entité applicable.

1. En regard du nom de la vue, cliquez sur ![Restaurer les paramètres par défaut](/help/search-social-commerce/assets/revert.png "Restaurer les paramètres par défaut").

## Suppression d’une vue personnalisée

Vous pouvez supprimer toute vue personnalisée que vous avez créée.

Si vous supprimez une vue personnalisée qui est appliquée à l’onglet actif, l’onglet continue à afficher la vue personnalisée jusqu’à ce que vous vous déplaciez en dehors du jeu de vues (par exemple, depuis les vues dans la [!UICONTROL Search] pour [!UICONTROL Reports] ) ou (le cas échéant) lorsque vous [afficher les données d’un autre annonceur ;](/help/search-social-commerce/common-tasks/change-advertiser.md).

1. Dans le panneau de gauche, cliquez sur ![Vues personnalisées](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Vues personnalisées") pour développer la variable [!UICONTROL Custom Views] .

1. Placez le curseur sur le nom de la vue personnalisée, puis cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Continue]**.

## Paramètres d’affichage par défaut et personnalisés {#view-settings}

| **Onglet** | **Champ** | **Description** |
| --- | --- | --- |
| [Par-dessus tous les onglets] | Nom | Nom unique de la vue. Vous ne pouvez pas modifier le nom d’une vue par défaut. <p><b>Conseil :</b> Utilisez un nom qui vous aidera à identifier l’onglet et les informations auxquelles il s’applique (par exemple, &quot;Campagnes en pause&quot; ou &quot;50 meilleures publicités&quot;). |
|   | Vue universelle | Rend les paramètres de données disponibles pour toutes les vues d’entité (pour les campagnes, les publicités, etc.). Les vues universelles peuvent inclure des colonnes de classification de mesures et de libellés, mais pas des colonnes de propriétés (telles que le nom et l’état de l’entité), car elles diffèrent par type d’entité, ainsi que par tous les autres attributs d’affichage. Tous les critères de filtre sont appliqués à la vue d’entité le cas échéant et sont ignorés dans le cas contraire. Tous les filtres de mesure sont évalués localement (par exemple, pour les clics \> 1 000, la vue Campagnes affiche les campagnes avec plus de 1 000 clics, et la vue Groupes publicitaires affiche les groupes publicitaires avec plus de 1 000 clics).<p>Les colonnes de propriétés pour une vue universelle sont extraites de la vue par défaut de l’entité. Vous pouvez modifier les colonnes de propriétés par défaut d’une entité spécifique dans les paramètres d’affichage par défaut.<p>Une fois cette option activée ou désactivée, vous ne pouvez pas enregistrer la modification dans la vue existante, mais vous pouvez créer une nouvelle vue avec la modification. |
|   | Partager | (Affichages personnalisés uniquement ; facultatif) rend la vue disponible pour tous les autres utilisateurs qui peuvent afficher les données de l’annonceur. Les autres utilisateurs ne peuvent ni modifier ni supprimer la vue, mais ils peuvent créer une vue à partir des paramètres. Dans vos listes de vues, chaque vue partagée par une autre personne est mise en italique, par exemple &quot;&quot;._Campagnes les plus performantes_.&quot; |
| Colonnes | Colonnes et ordre sélectionnés | Les colonnes de données affichées et leur ordre :<ul><li> (Pour ajouter une colonne) Dans la liste Colonnes disponibles , cliquez sur le nom d’une colonne, puis faites-la glisser dans la liste Colonnes et commandes sélectionnées ou cliquez sur ![flèche droite](/help/search-social-commerce/assets/chevron-right.png) pour le déplacer.</li><li>(Pour modifier la position horizontale d’une colonne) Dans la liste Colonnes et commandes sélectionnées, cliquez sur le nom de la colonne, puis faites-la glisser jusqu’à l’emplacement souhaité ou cliquez sur ![Flèche vers le haut](/help/search-social-commerce/assets/chevron-up.png) ou ![Flèche vers le bas](/help/search-social-commerce/assets/chevron-down.png) pour le déplacer. Le nom de la colonne supérieure apparaît dans la colonne de gauche.</li><li>(Pour supprimer une colonne) Dans la liste Colonnes et commandes sélectionnées, cliquez sur le nom d’une colonne, puis faites-la glisser dans la liste Colonnes disponibles ou cliquez sur ![flèche gauche](/help/search-social-commerce/assets/chevron-left.png) pour le déplacer.</li></ul><b>Filtrage des données</b><p>Pour ne répertorier qu’un type spécifique de données, cliquez sur l’une des icônes en regard de la liste :<ul><li>![icône de propriétés](/help/search-social-commerce/assets/properties-icon.png) pour les noms de propriété et les identifiants des composants de recherche, tels que État</li><li>![icône de trafic](/help/search-social-commerce/assets/traffic-metrics-icon.png) pour les mesures de trafic standard, telles que les impressions et les clics</li><li>![icône recettes](/help/search-social-commerce/assets/revenue-metrics-icon.png) (pour les mesures de conversion suivies pour l’annonceur, y compris les mesures de conversion et d’engagement du site synchronisées à partir d’Analytics)</li><li>![icône personnalisée](/help/search-social-commerce/assets/custom-metrics-icon.png) (pour les mesures dérivées personnalisées créées par l’annonceur)</li><li>![icône de classification](/help/search-social-commerce/assets/classifications-icon.png) (pour les classifications d’étiquettes).</li></ul> <b>Remarques supplémentaires :</b><ul><li>Pour ajouter, créer ou modifier de nouvelles mesures, voir &quot;Création d’une mesure personnalisée&quot;, &quot;Modification d’une mesure personnalisée&quot; et &quot;Suppression d’une mesure personnalisée&quot;.</li><li>Si le rapport inclut des données pour des comptes avec des devises différentes, les totaux ne sont pas inclus pour les colonnes monétaires (telles que Coût et CPC).</li><li>Vous pouvez [modifier temporairement le jeu de colonnes dans le menu d’en-tête de colonne ;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md), et [modifiez et triez le jeu de colonnes à partir de la fonction [!UICONTROL Columns] icon](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Icône Colonnes](/help/search-social-commerce/assets/custom-columns.png "Icône Colonnes")).</li></ul> |
|   | Trier par | Colonne selon laquelle trier les données. La valeur par défaut est différente pour chaque type de rapport. |
|   | Ordre de tri | Si les données doivent être triées dans **ascendant** ou **Descendant** commande. Déplacez le curseur pour sélectionner une option. |
| Filtres | [Définitions de filtre] | (Facultatif) Filtres à appliquer aux données. L’application de filtres renvoie des lignes uniquement lorsque la valeur d’une colonne répond à des critères spécifiés.<p>Pour chaque filtre à appliquer :<ol><li>Dans le menu Ajouter un filtre , sélectionnez un nom de colonne. La liste comprend toutes les colonnes disponibles et est triée par type de colonne, avec les colonnes de propriétés en premier.</li><li>Définir le filtre sur la colonne</li></ol>(Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, puis saisissez la valeur appropriée. Les valeurs ne respectent pas la casse. Cliquez sur ![icône de vérification](/help/search-social-commerce/assets/select.png) lorsque vous avez fini.<p>Par exemple, si vous avez sélectionné la colonne &quot;Clics&quot; et que vous souhaitez renvoyer uniquement les lignes comportant plus de 100 clics, sélectionnez _\>_ et saisissez `100` dans le champ de saisie.<p>Selon le type de données, les opérateurs disponibles peuvent inclure : <i>supérieur à</i>, <i>inférieur à</i>, <i>est égal à</i>, <i>contains</i>, <i>ne contient pas</i>, <i>commence par</i>, <i>se termine par</i>,<i>pas de valeur</i>, ou <i>has value</i> <i>before</i>, <i>after</i>,ou <i>aucune date</i>.<p>(Filtres sans champs de saisie) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png) en regard du menu Sélectionner les éléments de la liste , puis cochez les cases en regard de chaque valeur à inclure. Cliquez sur ![icône de vérification](/help/search-social-commerce/assets/select.png) lorsque vous avez fini.<p><b>Remarques :</b><ul><li>Vous pouvez appliquer les modifications apportées aux filtres, mais pas les enregistrer, aux paramètres d’affichage par défaut.</li><li>Vous pouvez également [modifier temporairement les filtres applicables ;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) dans la vue.</li></ul> |
|   | Inclure les lignes avec les données de performances uniquement | (vues Groupes publicitaires, Mot-clé, Groupes de produits, Emplacements et Cibles automatiques uniquement) <p>Inclut uniquement les lignes contenant des données de performance aux dates spécifiées. Par défaut, cette option est sélectionnée pour réduire le temps de chargement de la page. <p><b>Avertissement</b>: si vous désélectionnez l’option et que la vue inclut de nombreuses entités sans données de performances, l’affichage des données prendra plus de temps.<p> <b>Remarque</b>: vous pouvez appliquer les modifications apportées aux filtres à vos paramètres d’affichage par défaut, mais pas les enregistrer. Les vues par défaut affichent toujours uniquement les entités avec des données de performances. |
| Date | Période | (Lorsque &quot;Inclure la période&quot; est sélectionné)<p>La période pour laquelle générer les données. Choisissez une option :<ul><li><i>[Période prédéfinie]</i>: liste d’incréments de temps courants, allant de <i>Aujourd&#39;hui</i> to <i>180 derniers jours</i>. Sélectionnez-en une dans la liste ; la valeur par défaut est <i>Hier</i>. Remarque : <i>Mois dernier</i>, <i>3 derniers mois</i>, et <i>6 derniers mois</i> affiche les données des mois calendaires précédents.</li><li><i>Période personnalisée :</i> Indiquez les dates de début et de fin. Entrez des dates au format MM/JJ/AAAA ou M/J/AAAA, ou cliquez sur ![icône de calendrier](/help/search-social-commerce/assets/calendar.png) en regard d’un champ et sélectionnez une date.</li></ul> |
|   | Comparaison | Compare les données de la période spécifiée aux données d’une seconde période. Lorsque vous sélectionnez cette option, deux colonnes supplémentaires sont ajoutées pour chaque colonne de données ordinaire. Par exemple, au lieu d’inclure une seule colonne pour &quot;Impressions&quot;, le rapport inclura des colonnes pour &quot;Plage des impressions 1&quot;, &quot;Plage des impressions 2&quot; et &quot;Différence entre impressions&quot;.<p><b>Remarques :</b><ul><li>La colonne de différence n’est pas affichée pour les mesures dérivées.</li><li>La génération de rapports qui comparent des plages de dates volumineuses peut prendre plus de temps.</li></ul> |
|   | Format de comparaison | Comment exprimer la différence entre les données des deux périodes sélectionnées dans le [_Champ de données_] Différence. Choisissez une option :<ul><li><i>Variance</i> (valeur par défaut) : affiche la différence sous la forme d’une valeur numérique.</li><li><i>% de changement</i>: affiche la différence en pourcentage.</li></ul> |
| Paramètres supplémentaires | Utiliser la valeur par défaut | Applique les paramètres d’attribution spécifiés dans les paramètres d’attribution de conversion au niveau de l’annonceur. |
|   | Règle d’attribution | (Publicitaires avec le service de suivi de conversion basé sur les pixels Adobe Advertising uniquement) Dans l’onglet, comment attribuer des données de conversion (potentiellement sur plusieurs canaux et portfolios publicitaires), dans une série d’événements qui mènent à une conversion. Par défaut, la règle spécifiée dans les paramètres d’attribution de conversion au niveau de l’annonceur est sélectionnée.<ul><li> <i>Premier événement</i>: attribue la conversion au premier clic payant de la série dans l’intervalle de recherche en amont des clics de l’annonceur ou, si aucun clic payant n’a eu lieu, à la dernière impression dans l’intervalle de recherche en amont des impressions de l’annonceur.</li><li><i>Poids - Premier événement Plus</i>: attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont des clics et l’intervalle de recherche en amont des impressions de l’annonceur, mais donne le plus de poids au premier événement et, successivement, moins de poids aux événements suivants. Lorsque la conversion est précédée de clics et d’impressions payants, le poids de remplacement d’impression spécifié est appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids d’affichage publicitaire de l’annonceur plutôt que du poids de remplacement de l’impression.</li><li><i>Même distribution</i>: attribue la conversion de manière égale à chaque événement de la série qui s’est produit dans l’intervalle de recherche en amont des clics et l’intervalle de recherche en amont des impressions de l’annonceur. Lorsque la conversion est précédée de clics et d’impressions payants, le poids de remplacement d’impression spécifié est appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids d’affichage publicitaire de l’annonceur plutôt que du poids de remplacement de l’impression.</li><li><i>Poids du dernier événement plus</i>: attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont des clics et l’intervalle de recherche en amont des impressions de l’annonceur, mais donne le plus de poids au dernier événement et, successivement, moins de poids aux événements précédents. Lorsque la conversion est précédée de clics et d’impressions payants, le poids de remplacement d’impression spécifié est appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids d’affichage publicitaire de l’annonceur plutôt que du poids de remplacement de l’impression.</li><li><i>Dernier événement</i> (valeur par défaut) : attribue la conversion au dernier clic payant de la série dans l’intervalle de recherche en amont des clics de l’annonceur ou, si aucun clic payant n’a eu lieu, à la dernière impression dans l’intervalle de recherche en amont des impressions de l’annonceur.</li><li><i>En forme de U</i>: attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont des clics et l’intervalle de recherche en amont des impressions de l’annonceur, mais donne le plus de poids au premier et aux derniers événements, avec successivement moins de poids aux événements au milieu du chemin de conversion. Lorsque la conversion est précédée de clics et d’impressions payants, le poids de remplacement d’impression spécifié est appliqué aux impressions. Lorsque la conversion est précédée uniquement d’impressions, les impressions sont pondérées en fonction du poids d’affichage publicitaire de l’annonceur plutôt que du poids de remplacement de l’impression.</li></ul><p><b>Remarques :</b><ul><li>Toutes les règles d’attribution en dehors du Dernier événement sont disponibles uniquement pour les annonceurs qui disposent d’un suivi des clics par Adobe Advertising et d’un suivi des conversions depuis Adobe Advertising ou Adobe Analytics (avec une intégration Analytics).</li><li>Les règles d’attribution s’appliquent aux clics sur des publicités payantes dans n’importe quel canal. Elles ne s’appliquent pas aux impressions pour les annonces de référencement payant, qui ne peuvent pas être suivies au niveau de l’événement.</li><li>Lorsque vous signalez des données de conversion à l’aide de n’importe quelle règle d’attribution, à l’exception de l’une des règles &quot;Dernier événement&quot;, les événements menant à la conversion peuvent se produire sur plusieurs portefeuilles. Dans ce cas, la vue inclut des données pour la conversion uniquement lorsque les publicités ou les mots-clés de ces portefeuilles sont inclus dans la vue.</li><li>Pour les vues par défaut, nous vous recommandons de conserver la règle d’attribution par défaut, qui est utilisée pour calculer la variable [valeur de l’objectif](/help/search-social-commerce/glossary.md#o-p) (anciennement appelé &quot;recettes pondérées&quot;) pour chaque unité d’offre lors de l’optimisation de l’offre.</li></ul> |
|   | Conversions basées sur | Comment signaler les données de conversion :<ul><li><i>Date de transaction</i> (valeur par défaut) : pour afficher les transactions dont la date de transaction s’est produite au cours de la période spécifiée. Cela indique le montant des recettes généré au cours d’une période donnée.</li><li><i>Date de clic</i>: pour afficher les transactions résultant d’un clic qui s’est produit au cours de la période spécifiée. Lorsqu’un portfolio présente un délai important entre les clics et les transactions, cette option est utile pour calculer les recettes historiques par clic pour le portfolio, ce qui indique les comportements de recettes à attendre au fil du temps. |
