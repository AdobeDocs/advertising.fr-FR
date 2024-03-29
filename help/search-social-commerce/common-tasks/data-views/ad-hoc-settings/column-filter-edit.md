---
title: Modifier les filtres de colonnes
description: Découvrez comment modifier les filtres de colonnes.
exl-id: 6e42e006-089b-44b9-b9b1-66835b680413
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Modifier les filtres de colonnes

## Modifier un jeu de filtres

1. Cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter.png "Filtrer") dans la barre d’outils.

1. Dans les paramètres de filtre, effectuez l’une des opérations suivantes :

   * Pour ajouter un filtre, cliquez sur ![Ajouter un filtre](/help/search-social-commerce/assets/add.png "Ajouter un filtre") **[!UICONTROL ADD FILTER]** , puis procédez comme suit :

      1. (Facultatif) Pour filtrer les noms de colonne par chaîne de texte, saisissez la chaîne de recherche dans le champ **[!UICONTROL ADD FILTER]** champ de saisie.

      1. Sélectionnez un nom de colonne dans le menu Colonnes.

      1. Définissez le filtre sur la colonne :

         * (Filtres sans champs de saisie) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png "Flèche vers le bas") en regard du deuxième menu, cochez les cases en regard de chaque valeur à inclure, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

         * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, saisissez la valeur appropriée, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

           Par exemple, si vous avez sélectionné le[!UICONTROL Clicks]&quot; et que vous souhaitez renvoyer uniquement les lignes contenant plus de 100 clics, puis sélectionnez *[!UICONTROL greater than]*&quot; et saisissez `100` dans le champ de saisie.

           Selon le type de données, les opérateurs disponibles peuvent inclure : *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, ou *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, ou *[!UICONTROL no date].*

           **Remarque :** Les valeurs de texte ne sont pas sensibles à la casse. Par exemple, si vous recherchez des campagnes dont le nom contient &quot;prêt&quot;, les résultats incluent &quot;Prêts aux consommateurs&quot; et &quot;Demande de prêt&quot;.

   * Pour modifier un filtre existant, cliquez sur le filtre, modifiez la définition du filtre, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

   * Pour supprimer un filtre existant, cliquez sur **[!UICONTROL X]** en regard de la définition de filtre.

1. ([!UICONTROL Keywords] afficher uniquement ; facultatif) Sélectionnez ou désélectionnez le paramètre sur &quot;[!UICONTROL Include rows with no performance data].&quot;

   >[!WARNING]
   >
   >La sélection de cette option augmente le temps de chargement de la page.

1. Cliquez sur **[!UICONTROL Apply]**.

## Modifier un seul filtre

1. (Si nécessaire) Dans l’ensemble de filtres situé au-dessus du tableau de données, cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus") pour développer le jeu de filtres.

1. Au-dessus du tableau de données, cliquez sur la définition de filtre.

1. Editez les filtres à appliquer :

   1. (Facultatif) Modifiez le nom de la colonne dans le menu Colonne.

   1. (Facultatif) Redéfinissez le filtre sur la colonne :

      * (Filtres sans champs de saisie) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png "Flèche vers le bas") en regard du deuxième menu, cochez les cases en regard de chaque valeur à inclure, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

      * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, saisissez la valeur appropriée, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

        Par exemple, si vous avez sélectionné le[!UICONTROL Clicks]&quot; et que vous souhaitez renvoyer uniquement les lignes contenant plus de 100 clics, puis sélectionnez *[!UICONTROL greater than]*&quot; et saisissez `100` dans le champ de saisie

        Selon le type de données, les opérateurs disponibles peuvent inclure : *[!UICONTROL greater than]*, *inférieur à*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *not contains*, ou *commence par .*

        **Remarque :** Les valeurs de texte ne sont pas sensibles à la casse. Par exemple, si vous recherchez des campagnes dont le nom contient &quot;prêt&quot;, les résultats incluent &quot;Prêts aux consommateurs&quot; et &quot;Demande de prêt&quot;.
