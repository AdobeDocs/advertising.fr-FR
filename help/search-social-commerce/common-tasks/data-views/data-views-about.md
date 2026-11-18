---
title: À propos de la personnalisation des données dans les vues de gestion de campagne
description: Découvrez les types de données que vous pouvez personnaliser dans les vues de données de Campaign.
exl-id: 89f36865-9275-494e-ac33-d41fa30faa2a
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/PnBql37yqK03DWH2OhLf8hnCBPOwFAVZxD65NNZu0VU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 2f170883b2876ea4a7b39e814df598d337f7ca07
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%
---
# À propos de la personnalisation des données dans les vues de gestion de campagne

Dans la plupart des vues de données de campagne, vous pouvez personnaliser les données qui apparaissent dans le tableau de données. Vous pouvez personnaliser les données des manières suivantes :

* [Modifiez les paramètres de l&#39;ensemble de votre vue par défaut](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md##view-edit) pour une vue d&#39;entité spécifique (telle que [!UICONTROL Campaigns]) afin d&#39;inclure un ordre de colonne spécifique, des filtres, une période, une règle d&#39;attribution, etc., puis appliquez les paramètres temporairement ou enregistrez-les. Vous pouvez également [créer des vues personnalisées supplémentaires](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#create-custom-view), [cloner des vues existantes](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#view-clone) et [appliquer l’une de vos vues](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md#apply-a-default-or-custom-view).

* [Modifiez les colonnes et leur ordre de tri](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md) à l&#39;aide du contrôle [!UICONTROL Custom Columns] de la barre d&#39;outils. Dans la nouvelle interface utilisateur, si la barre d&#39;outils est trop étroite pour afficher le contrôle, cliquez sur **[!UICONTROL Actions]>[!UICONTROL Custom Columns]**. Vous pouvez également [modifier rapidement uniquement les colonnes](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) de n’importe quel en-tête de colonne de l’affichage.

* (Interface utilisateur héritée uniquement) [À partir du panneau de navigation de gauche](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/filter-using-left-panel.md), vous pouvez :

  * Parcourez ou recherchez des entités par réseau publicitaire et filtrez selon le statut de l’entité et le statut du compte, de la campagne et du groupe publicitaire ou de l’ensemble publicitaire. Cliquez sur une entité ou un groupe d’entités dans le panneau pour charger une vue des entités enfants (par exemple, cliquez sur un nom de campagne pour afficher ses groupes d’annonces enfants).

  * Parcourez ou recherchez des campagnes par portefeuille ou groupe de portefeuilles, et filtrez selon le statut de l’entité et le statut du groupe de portefeuilles, du portefeuille et de la campagne. Cliquez sur un groupe de portefeuilles, un portefeuille ou une campagne dans le panneau pour charger les données du groupe de portefeuilles, du portefeuille ou de la campagne dans la vue d&#39;entité actuelle.

  * Accédez à vos vues par défaut, modifiez-les et réinitialisez-les, et accédez à vos vues personnalisées, modifiez-les et supprimez-les. Cliquez sur le nom d’une vue pour charger la vue appropriée.

* Appliquez des filtres sur toutes les colonnes de données disponibles pour modifier les données affichées dans l’onglet actif. Vous pouvez créer des filtres [&#x200B; à partir des en-têtes de colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md) ou [&#x200B; à partir d’un bouton de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md). Pour les vues de gestion de campagne, les filtres sont conservés tels qu&#39;applicables lorsque vous ouvrez des entités enfants. Par exemple, si vous affichez des campagnes avec \> 100 clics, puis ouvrez un groupe publicitaire dans cette campagne, seuls les groupes publicitaires avec \> 100 clics s’affichent.

* [Modifiez la période](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md) utilisée dans toutes les vues personnalisées et par défaut pour lesquelles vous n&#39;avez pas enregistré de périodes spécifiques.

* [Triez à nouveau les données](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-sort.md) en fonction des valeurs d&#39;une colonne spécifique.

* Choisissez d&#39;afficher 25 lignes, 50 lignes, 100 lignes, (interface utilisateur héritée uniquement) 200 lignes ou (interface utilisateur héritée uniquement) [!UICONTROL Continuous Scroll] au bas d&#39;une page.

<!--

## (New UI) Data table tools {#grid-controls-new-ui}

In applicable management views, the toolbar includes the following controls:

* On the left, the [!UICONTROL Filter] control appears before grid search. Where supported, the [!UICONTROL Conversion based on] selector follows search and lets you select [!UICONTROL Click Date] or [!UICONTROL Transaction Date].

* On the right, operational actions, such as [!UICONTROL Reports], appear alongside view and display controls. The available controls depend on the view and your permissions.

* When the available width is reduced, controls move into the [!UICONTROL Actions] menu. This can happen when you narrow the window or open the AI Assistant panel. If a control isn't visible in the toolbar, look for it in [!UICONTROL Actions]. In wider layouts, controls remain inline.

* Within [!UICONTROL Actions], a horizontal divider separates operational actions from view and display controls, such as the current view, [!UICONTROL Custom Columns], [!UICONTROL Compressed Mode], and [!UICONTROL Charts], where available.

* The primary create button remains outside [!UICONTROL Actions].

The [!UICONTROL Refresh] icon is beside the page title in applicable views. The date range control is in the page header. For instructions on comparing two date ranges and changing the comparison format, see "[Filter data by date range](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/date-filter.md#compare-periods-new-ui)."

### Change the grid density

* Where available, click **[!UICONTROL Compressed Mode]** in the toolbar or **[!UICONTROL Actions]** menu to turn compact grid spacing on or off.

  The toolbar button is selected when compressed mode is on. In [!UICONTROL Actions], a switch indicates the current state.

### Show or hide charts

* Where available, click **[!UICONTROL Charts]** in the toolbar or **[!UICONTROL Actions]** menu.

  The toolbar button is selected when charts are shown. In [!UICONTROL Actions], a switch indicates whether charts are shown. Click the control again to hide the charts.

-->
