---
title: Création d’un flux de rapport de feuille de calcul
description: Découvrez comment configurer des flux de feuille de calcul.
exl-id: ed793de5-0df1-4fc3-be59-29adec4959f7
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Création d’un flux de rapport de feuille de calcul

*Pour les rapports de base et les rapports de précision des modèles uniquement*

Configuration de flux de feuille de calcul à l’aide d’un format spécifique [!DNL Excel] modèles de feuille de calcul que vous créez à partir de modèles de rapport standard.

1. [Créez le [!DNL Excel] modèle à renseigner avec les données du rapport](spreadsheet-feed-create-excel-template.md).

2. Créez le flux de feuille de calcul :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

   1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Dans le **[!UICONTROL Add Spreadsheet Feed]** , spécifiez la variable [paramètres de flux de feuille de calcul](spreadsheet-feed-settings.md).

   1. Cliquez sur **[!UICONTROL Submit]**.

   1. (Facultatif) Une fois que la variable [!UICONTROL Update Status] is *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur.

      >[!NOTE]
      >
      >Si le modèle de rapport associé au flux est ensuite supprimé, le flux est également supprimé.

      Les flux de feuille de calcul sont automatiquement actualisés chaque jour au niveau de la [!UICONTROL Schedule Time]. Si le modèle de rapport inclut des adresses pour des destinataires de courrier électronique, ces adresses reçoivent des notifications lorsque la feuille de calcul est actualisée.

>[!MORELIKETHIS]
>
>* [A propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [Créez un [!DNL Excel] modèle pour un flux de rapport de feuille de calcul](spreadsheet-feed-create-excel-template.md)
>* [Modifier les paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-edit.md)
>* [Paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-settings.md)
>* [Affichage ou enregistrement d’un fichier de flux de rapport de feuille de calcul](spreadsheet-feed-view-or-save.md)
>* [Actualisation manuelle des flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
>* [Suppression de flux de rapports de feuille de calcul](spreadsheet-feed-delete.md)
