---
title: Création d’un flux de rapport de feuille de calcul
description: Découvrez comment configurer des flux de feuille de calcul.
exl-id: a6a9ce46-51b4-4b06-b004-89fce06d1da6
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Création d’un flux de rapport de feuille de calcul

*Pour les rapports de base et les rapports de précision des modèles uniquement*

Configurez des flux de feuille de calcul à l’aide de modèles de feuille de calcul [!DNL Excel] spécialement formatés que vous créez à partir de modèles de rapport standard.

1. [Créez le modèle [!DNL Excel] à remplir avec les données de rapport](spreadsheet-feed-create-excel-template.md).

2. Créez le flux de feuille de calcul :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

   1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Dans la boîte de dialogue **[!UICONTROL Add Spreadsheet Feed]**, spécifiez les [ paramètres de flux de feuille de calcul ](spreadsheet-feed-settings.md).

   1. Cliquez sur **[!UICONTROL Submit]**.

   1. (Facultatif) Une fois que le [!UICONTROL Update Status] du flux est *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur.

      >[!NOTE]
      >
      >Si le modèle de rapport associé au flux est ensuite supprimé, le flux est également supprimé.

      Les flux de feuille de calcul sont automatiquement actualisés chaque jour au niveau du [!UICONTROL Schedule Time] configuré. Si le modèle de rapport inclut des adresses pour des destinataires de courrier électronique, ces adresses reçoivent des notifications lorsque la feuille de calcul est actualisée.

>[!MORELIKETHIS]
>
>* [À propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [ Créez un  [!DNL Excel] modèle pour un flux de rapport de feuille de calcul](spreadsheet-feed-create-excel-template.md)
>* [Modifier les paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-edit.md)
>* [Paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-settings.md)
>* [ Afficher ou enregistrer un fichier de flux de rapport de feuille de calcul ](spreadsheet-feed-view-or-save.md)
>* [Actualisation manuelle des flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
>* [Supprimer des flux de rapports de feuille de calcul](spreadsheet-feed-delete.md)
