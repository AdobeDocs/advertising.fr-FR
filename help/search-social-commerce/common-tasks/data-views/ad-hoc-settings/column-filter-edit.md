---
title: Modifier les filtres de colonne
description: Découvrez comment modifier les filtres de colonne.
exl-id: 68f816ea-cde2-4df0-b46c-f47fa20a2727
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Modifier les filtres de colonne

<!-- Doesn't include instructions for legacy Portfolios view; not available in Reports views -->

## (Nouvelle interface utilisateur) Modifier un jeu de filtres dans une vue de gestion

1. Dans la barre d’outils, cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter-new.png "Filtrer").

1. Dans les paramètres de filtre, effectuez l’une des opérations suivantes :

   * Pour ajouter un filtre, cliquez sur **[!UICONTROL ADD FILTER]**, puis procédez comme suit :

      1. (Facultatif) Pour filtrer les noms des colonnes par chaîne de texte, saisissez la chaîne de recherche dans le champ de saisie **[!UICONTROL ADD FILTER]**.

      1. Sélectionnez un nom de colonne dans le menu Colonne .

      1. Définissez le filtre sur la colonne :

         * (Filtres sans champs de saisie) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png "Flèche vers le bas") en regard du deuxième menu, puis cochez les cases en regard de chaque valeur à inclure.

         * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, puis saisissez la valeur applicable.

           Par exemple, si vous avez sélectionné la colonne « [!UICONTROL Clicks] » et que vous souhaitez renvoyer uniquement des lignes contenant plus de 100 clics, sélectionnez *[!UICONTROL greater than]* » et saisissez `100` dans le champ de saisie.

           Selon le type de données, les opérateurs disponibles peuvent inclure *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* ou *[!UICONTROL no date].*

           **Remarque :** les valeurs de texte ne respectent pas la casse. Par exemple, si vous filtrez par campagnes avec « loan » dans le nom, les résultats incluent « Consumer Loans » et « loan applications » (demandes de prêt).

   * Pour modifier un filtre existant, cliquez sur le filtre, puis modifiez la définition du filtre.

   * Pour supprimer un filtre existant, cliquez sur **[!UICONTROL -]** en regard de la définition de filtre.

## (IU héritée) Modifier un jeu de filtres dans une vue de gestion de campagne

1. Cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter.png "Filtrer") dans la barre d’outils.

1. Dans les paramètres de filtre, effectuez l’une des opérations suivantes :

   * Pour ajouter un filtre, cliquez sur ![Ajouter un filtre](/help/search-social-commerce/assets/add.png "Ajouter un filtre") **[!UICONTROL ADD FILTER]** , puis procédez comme suit :

      1. (Facultatif) Pour filtrer les noms des colonnes par chaîne de texte, saisissez la chaîne de recherche dans le champ de saisie **[!UICONTROL ADD FILTER]**.

      1. Sélectionnez un nom de colonne dans le menu Colonne .

      1. Définissez le filtre sur la colonne :

         * (Filtres sans champs de saisie) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png "Flèche vers le bas") en regard du deuxième menu, puis cochez les cases en regard de chaque valeur à inclure.

         * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, puis saisissez la valeur applicable.

           Par exemple, si vous avez sélectionné la colonne « [!UICONTROL Clicks] » et que vous souhaitez renvoyer uniquement des lignes contenant plus de 100 clics, sélectionnez *[!UICONTROL greater than]* » et saisissez `100` dans le champ de saisie.

           Selon le type de données, les opérateurs disponibles peuvent être *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]* ou *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* ou *[!UICONTROL no date].*

           **Remarque :** les valeurs de texte ne respectent pas la casse. Par exemple, si vous recherchez des campagnes dont le nom contient « loan », les résultats incluent « Consumer Loans » et « loan applications ».

   * Pour modifier un filtre existant, cliquez sur le filtre, puis modifiez la définition du filtre.

   * Pour supprimer un filtre existant, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer") en regard de la définition du filtre.

1. (Vue [!UICONTROL Keywords] uniquement ; facultatif) Sélectionnez ou désélectionnez le paramètre sur « [!UICONTROL Include rows with no performance data] ».

   >[!WARNING]
   >
   >Cette option augmente le temps de chargement de la page.

1. Cliquez sur **[!UICONTROL Apply]**.

## Modification d’un filtre unique dans une vue de gestion

1. Au-dessus du tableau de données, cliquez sur la définition du filtre.

1. Redéfinissez le filtre sur la colonne :

   * (Filtres sans champs de saisie) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png "Flèche vers le bas") à côté du deuxième menu, puis cochez les cases en regard de chaque valeur à inclure.

   * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, puis saisissez la valeur applicable.

     Par exemple, si vous avez sélectionné la colonne « [!UICONTROL Clicks] » et que vous souhaitez renvoyer uniquement des lignes contenant plus de 100 clics, sélectionnez *[!UICONTROL greater than]* » et saisissez `100` dans le champ de saisie.

     Selon le type de données, les opérateurs disponibles peuvent inclure *[!UICONTROL greater than]*, *inférieur à*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *ne contient pas* ou *commence par.*

     **Remarque :** les valeurs de texte ne respectent pas la casse. Par exemple, si vous recherchez des campagnes dont le nom contient « loan », les résultats incluent « Consumer Loans » et « loan applications ».

>[!MORELIKETHIS]
>
>* [Appliquer un filtre de données à partir du menu d’en-tête de colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)
>* [Appliquer des filtres de données depuis la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)
>* [Supprimer un filtre de colonne]&#x200B;(/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/
