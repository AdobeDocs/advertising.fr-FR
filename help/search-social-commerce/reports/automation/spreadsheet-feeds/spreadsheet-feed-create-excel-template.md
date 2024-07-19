---
title: Créer un modèle  [!DNL Excel]  pour un flux de rapport de feuille de calcul
description: Découvrez comment créer des modèles de feuille de calcul spécialement formatés.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Créer un modèle [!DNL Excel] pour un flux de rapport de feuille de calcul

*Pour les rapports de base et les rapports de précision des modèles uniquement*

Pour créer des flux de feuille de calcul, vous devez d’abord créer des modèles de feuille de calcul [!DNL Microsoft Excel] spécialement formatés à l’aide de modèles de rapport standard. Vous pouvez éventuellement personnaliser la feuille de calcul [!DNL Excel] pour inclure des colonnes et des graphiques supplémentaires.

1. Dans **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, générez le type de rapport souhaité à l’aide d’une unité [!UICONTROL Date Aggregation] de &quot;[!UICONTROL Daily]&quot; et avec tous les autres paramètres de données souhaités, en enregistrant le rapport comme modèle.

   >[!NOTE]
   >
   > * Vous pouvez créer des flux de feuille de calcul pour les rapports [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] et [!UICONTROL Forecast Accuracy]. Si vous utilisez le [!UICONTROL Ad Group Report], limitez le nombre de groupes d’annonces inclus pour des résultats plus rapides.
   > * L&#39;unité [!UICONTROL Date Range] définie dans le modèle n&#39;est pas utilisée. Vous définirez les dates auxquelles actualiser les données lorsque vous configurez le flux de feuille de calcul ultérieurement.

1. Une fois le rapport généré, accédez à **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** et exportez une version TSV ou XLS de la sortie du rapport dans un fichier .

1. Dans [!DNL Excel], créez un modèle personnalisé pour le rapport :

   1. Ouvrez le fichier de rapport dans [!DNL Excel].

   1. Préparez le classeur :

      1. Supprimez les lignes principales qui affichent les paramètres du rapport. Pour les fichiers XLS, supprimez également la ligne &quot;[!UICONTROL Total]&quot;. Vous pouvez éventuellement supprimer certaines lignes de données, mais conserver a) la ligne d’en-tête de données avec toutes les colonnes dans l’ordre d’origine et b) au moins une ligne de données. N’ajoutez pas manuellement de données.

         >[!NOTE]
         >
         > La dernière colonne doit contenir des valeurs non nulles.

      2. Triez les données par date de début par ordre croissant (du plus ancien au plus récent).

      3. Remplacez le nom de l’onglet de la feuille de calcul de &quot;[!UICONTROL Sheet1]&quot; par &quot;[!UICONTROL RAW]&quot;.

         Ce nom d&#39;onglet spécifique permet d&#39;actualiser les données.

      4. (Facultatif) Ajoutez des colonnes personnalisées à droite des colonnes du modèle de rapport, si nécessaire.

   1. (Facultatif) Sur une feuille de calcul distincte, créez un tableau croisé dynamique. Une fois que vous avez terminé, cliquez avec le bouton droit de la souris dans une cellule du tableau croisé dynamique, sélectionnez **[!UICONTROL Pivot Table Options]**, cliquez sur l&#39;onglet **[!UICONTROL Data]**, puis sélectionnez **[!UICONTROL Refresh data when opening the file]**.

   1. Enregistrez le fichier en tant que feuille de calcul [!DNL Excel] au format .XLSX.

>[!MORELIKETHIS]
>
>* [À propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [Créer un flux de rapport de feuille de calcul](spreadsheet-feed-create.md)
>* [Modifier les paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-edit.md)
>* [Paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-settings.md)
>* [ Afficher ou enregistrer un fichier de flux de rapport de feuille de calcul ](spreadsheet-feed-view-or-save.md)
>* [Actualisation manuelle des flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
>* [Supprimer des flux de rapports de feuille de calcul](spreadsheet-feed-delete.md)
