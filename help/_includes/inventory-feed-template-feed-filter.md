---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Modèle de publicité textuelle - Filtre de flux

**\[Filtre de flux\]:** Quelles lignes du fichier de flux propager :

* *[!UICONTROL Propagate all rows found in feed:]* (valeur par défaut) Pour propager les données pour toutes les lignes.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Pour propager les données uniquement pour les lignes qui respectent jusqu’à dix conditions spécifiées. Indiquez les filtres à appliquer :

   1. Sélectionnez l’opération booléenne à utiliser pour tous les filtres : **[!UICONTROL AND]** ou **[!UICONTROL OR]**.

   1. Sélectionnez un nom de colonne dans le premier menu, sélectionnez un opérateur dans le deuxième menu, puis saisissez les valeurs applicables ou laissez le champ de saisie vide pour propager les données des lignes sans conditions.

  La liste des colonnes comprend toutes les colonnes disponibles dans le flux.

  Les opérateurs disponibles sont *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (différent de), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]* et *[!UICONTROL greater than]*. Lorsque vous sélectionnez l’opérateur &quot;[!UICONTROL in]&quot;, vous pouvez entrer une liste de valeurs séparées par des virgules ; si un enregistrement correspond à l’une des valeurs spécifiées, les données sont propagées pour ces lignes. Pour tous les autres opérateurs, ne saisissez qu&#39;une seule valeur. Les valeurs ne respectent pas la casse.

  Par exemple, si vous avez sélectionné la colonne &quot;product_type&quot; et souhaitez renvoyer uniquement des lignes pour les noms de produits contenant &quot;chaussures&quot;, sélectionnez &quot;**[!UICONTROL contains]**&quot; et saisissez `shoes` dans le champ de saisie.

   1. (Pour appliquer jusqu’à neuf filtres supplémentaires) Pour chaque filtre supplémentaire, cliquez sur **[!UICONTROL Add Condition]**, puis spécifiez le filtre supplémentaire par étape 2.
