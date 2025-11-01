---
source-git-commit: 73c9cc7134360e073fc466dda3733cfc9bac8786
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Texte et modèle - Filtre de flux

**\[Filtre de flux\] :** les lignes du fichier de flux à propager :

* *[!UICONTROL Propagate all rows found in feed:]* (Valeur par défaut) Pour propager les données de toutes les lignes.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Pour propager les données uniquement pour les lignes qui remplissent un maximum de dix conditions spécifiées. Spécifiez les filtres à appliquer :

   1. Sélectionnez l’opération booléenne à utiliser pour tous les filtres : **[!UICONTROL AND]** ou **[!UICONTROL OR]**.

   1. Sélectionnez un nom de colonne dans le premier menu, sélectionnez un opérateur dans le second menu, puis saisissez les valeurs applicables ou laissez le champ d’entrée vide pour propager les données des lignes sans conditions.

  La liste des colonnes comprend toutes les colonnes disponibles dans le flux.

  Les opérateurs disponibles sont *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (n’est pas égal à), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]* et *[!UICONTROL greater than]*. Lorsque vous sélectionnez l’opérateur « [!UICONTROL in] », vous pouvez saisir une liste de valeurs séparées par des virgules ; si un enregistrement correspond à l’une des valeurs spécifiées, les données sont propagées pour ces lignes. Pour tous les autres opérateurs, saisissez une seule valeur. Les valeurs ne respectent pas la casse.

  Par exemple, si vous sélectionnez la colonne « product_type » et que vous souhaitez renvoyer uniquement des lignes pour les noms de produits contenant « chaussures », sélectionnez « **[!UICONTROL contains]** » et saisissez `shoes` dans le champ de saisie.

   1. (Pour appliquer jusqu’à neuf filtres supplémentaires) Pour chaque filtre supplémentaire, cliquez sur **[!UICONTROL Add Condition]**, puis spécifiez le filtre supplémentaire à l’étape 2.
