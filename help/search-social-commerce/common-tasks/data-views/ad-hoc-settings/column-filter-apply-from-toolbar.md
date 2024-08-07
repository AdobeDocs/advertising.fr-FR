---
title: Application de filtres de données à partir de la barre d’outils
description: Découvrez comment filtrer les données de page de la barre d’outils.
exl-id: fc1dca75-b0e5-48fd-90ee-f09c158e3e8b
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Application de filtres de données à partir de la barre d’outils

Vous pouvez appliquer autant de filtres que vous le souhaitez à une vue. Tous les filtres sont unis à l’aide de l’opérateur AND.

1. Dans la barre d’outils, cliquez sur ![Filter](/help/search-social-commerce/assets/filter.png "Filter").

1. Dans les paramètres de filtre, effectuez l’une des opérations suivantes :

   * Pour ajouter un filtre, cliquez sur ![Ajouter un filtre](/help/search-social-commerce/assets/add.png "Ajouter un filtre") **[!UICONTROL ADD FILTER]**, puis procédez comme suit :

      1. (Facultatif) Pour filtrer les noms de colonne par chaîne de texte, saisissez la chaîne de recherche dans le champ d’entrée **[!UICONTROL ADD FILTER]**.

      1. Sélectionnez un nom de colonne dans le menu Colonnes.

      1. Définissez le filtre sur la colonne :

         * (Filtres sans champs de saisie) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png "Flèche vers le bas") en regard du second menu, puis cochez les cases en regard de chaque valeur à inclure.

         * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, puis saisissez la valeur appropriée.

           Par exemple, si vous avez sélectionné la colonne &quot;[!UICONTROL Clicks]&quot; et que vous souhaitez renvoyer uniquement des lignes avec plus de 100 clics, sélectionnez *[!UICONTROL greater than]*&quot; et saisissez `100` dans le champ de saisie.

           Selon le type de données, les opérateurs disponibles peuvent être *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]* ou *[!UICONTROL no date].*

           **Remarque :** Les valeurs de texte ne sont pas sensibles à la casse. Par exemple, si vous filtrez par campagnes dont le nom contient &quot;prêt&quot;, les résultats incluent &quot;Prêts aux consommateurs&quot; et &quot;Demande de prêt&quot;.

         * ([!UICONTROL Ad Groups], [!UICONTROL Keywords], [!UICONTROL Product Groups], [!UICONTROL Placements] et [!UICONTROL Auto Targets] vues uniquement ; facultatif) Remplacez le paramètre par &quot;[!UICONTROL Include rows with performance data only]&quot;.

           **Avertissement :** Si vous désélectionnez l’option et que la vue inclut de nombreuses entités sans données de performances, l’affichage des données prend plus de temps.

   * Pour modifier un filtre existant, cliquez sur le filtre, modifiez la définition du filtre, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

   * Pour supprimer un filtre existant, cliquez sur **[!UICONTROL X]** en regard de la définition de filtre.

1. Cliquez sur **[!UICONTROL Apply]**.
