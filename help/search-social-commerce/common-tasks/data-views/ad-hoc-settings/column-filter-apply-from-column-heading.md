---
title: Application de filtres de données à partir d’un menu d’en-tête de colonne
description: Découvrez comment filtrer les données de la page à partir du menu d’en-tête de colonne.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Application d’un filtre de données à partir d’un menu d’en-tête de colonne

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

Vous pouvez appliquer autant de filtres que vous le souhaitez à une colonne, un par un.<!-- True only for entity names, I think: All filters are joined using the AND operator. --> Pour ajouter plusieurs filtres à la fois à l’aide de toutes les mesures disponibles, reportez-vous à « [Appliquer des filtres de données à partir de la barre d’outils](column-filter-apply-from-toolbar.md) ».

1. Sur le côté droit de l’en-tête de colonne, cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flèche vers le bas"), puis sur **[!UICONTROL Add Filter]**.

1. Définissez le filtre sur la colonne :

   * (Filtres sans champs de saisie) Cochez les cases en regard de chaque valeur à inclure, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Ajouter").

   * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, saisissez la valeur applicable, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Ajouter").

     Par exemple, si vous avez sélectionné la colonne « [!UICONTROL Clicks] » et que vous souhaitez renvoyer uniquement des lignes contenant plus de 100 clics, sélectionnez *[!UICONTROL greater than]* » et saisissez `100` dans le champ de saisie. Selon le type de données, les opérateurs disponibles peuvent inclure *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* ou *[!UICONTROL no date]*

     >[!NOTE]
     >
     >* Les valeurs de texte ne respectent pas la casse. Par exemple, si vous filtrez par campagnes avec « loan » dans le nom, les résultats incluent « Consumer Loans » et « loan applications » (demandes de prêt).
     >* Vous ne pouvez appliquer qu&#39;un seul filtre numérique simple (tel que [!UICONTROL Impressions] \> 100) par colonne.

>[!MORELIKETHIS]
>
>* [Appliquer des filtres de données depuis la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [Modifier les filtres de colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-edit.md)
>* [Supprimer un filtre de colonne]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
