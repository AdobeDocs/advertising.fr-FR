---
title: Création d [!DNL Excel] un modèle pour un flux de rapports de feuille de calcul
description: Découvrez comment créer des modèles de feuille de calcul spécialement formatés.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Créer un modèle de [!DNL Excel] pour un flux de rapports de feuille de calcul

*Pour les rapports de base et les rapports sur la précision des modèles uniquement*

Pour créer des flux de feuilles de calcul, vous devez d&#39;abord créer des modèles de feuilles de calcul [!DNL Microsoft Excel] spécialement formatés à l&#39;aide de modèles de rapport standard. Vous pouvez éventuellement personnaliser la feuille de calcul [!DNL Excel] pour inclure des colonnes et des graphiques supplémentaires.

1. Dans **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, générez le type de rapport souhaité à l’aide d’une unité de [!UICONTROL Date Aggregation] de « [!UICONTROL Daily] » et de tous les autres paramètres de données souhaités, en enregistrant le rapport en tant que modèle.

   >[!NOTE]
   >
   > * Vous pouvez créer des flux de feuilles de calcul pour les rapports [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] et [!UICONTROL Forecast Accuracy]. Si vous utilisez l’[!UICONTROL Ad Group Report] , limitez le nombre de groupes publicitaires inclus pour obtenir des résultats plus rapides.
   > * L’unité de [!UICONTROL Date Range] définie dans le modèle n’est pas utilisée. Vous définissez les dates auxquelles les données seront actualisées lors de la configuration ultérieure du flux de la feuille de calcul.

1. Une fois le rapport généré, accédez à **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** et exportez une version TSV ou XLS du rapport vers un fichier.

1. Dans [!DNL Excel], créez un modèle personnalisé pour le rapport :

   1. Ouvrez le fichier de rapport dans [!DNL Excel].

   1. Préparez le classeur :

      1. Supprimez les premières lignes qui affichent les paramètres du rapport. Pour les fichiers XLS, supprimez également la ligne « [!UICONTROL Total] ». Vous pouvez éventuellement supprimer certaines lignes de données, mais conservez a) la ligne d’en-tête de données avec toutes les colonnes dans l’ordre d’origine et b) au moins une ligne de données. Ne pas ajouter de données manuellement.

         >[!NOTE]
         >
         > La dernière colonne doit inclure des valeurs non nulles.

      2. Triez les données par date de début par ordre croissant (du plus ancien au plus récent).

      3. Remplacez le nom de l&#39;onglet de feuille de calcul de « [!UICONTROL Sheet1] » par « [!UICONTROL RAW] ».

         Ce nom d’onglet spécifique permet d’actualiser les données.

      4. (Facultatif) Ajoutez des colonnes personnalisées à droite des colonnes du modèle de rapport, si nécessaire.

   1. (Facultatif) Dans une feuille de calcul distincte, créez un tableau croisé dynamique. Une fois que vous avez terminé, cliquez avec le bouton droit de la souris dans n&#39;importe quelle cellule du tableau croisé dynamique et sélectionnez **[!UICONTROL Pivot Table Options]**, cliquez sur l&#39;onglet **[!UICONTROL Data]**, puis sélectionnez **[!UICONTROL Refresh data when opening the file]**.

   1. Enregistrez le fichier en tant que feuille de calcul [!DNL Excel] au format .XLSX.

>[!MORELIKETHIS]
>
>* [À propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [Créer un flux de rapport de feuille de calcul](spreadsheet-feed-create.md)
>* [Modifier les paramètres de flux de rapports des feuilles de calcul](spreadsheet-feed-edit.md)
>* [Paramètres de flux de rapports des feuilles de calcul](spreadsheet-feed-settings.md)
>* [Afficher ou enregistrer un fichier de flux de rapports de feuille de calcul](spreadsheet-feed-view-or-save.md)
>* [Actualiser manuellement les flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
>* [Supprimer des flux de rapports de feuille de calcul](spreadsheet-feed-delete.md)
