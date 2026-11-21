---
title: Créer un flux de rapports de feuille de calcul
description: Découvrez comment configurer des flux de feuille de calcul.
exl-id: a6a9ce46-51b4-4b06-b004-89fce06d1da6
feature: Search Reports
TQID: 'https://experienceleague.adobe.com/LM5QfP4QSOBQ4YFLgdARTKb4xNkyXSJxzG79dGdo-HA'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%
---
# Créer un flux de rapports de feuille de calcul

*Pour les rapports de base et les rapports sur la précision des modèles uniquement*

Configurez les flux de feuilles de calcul à l&#39;aide de modèles de feuilles de calcul [!DNL Excel] spécialement formatés que vous créez à partir de modèles de rapport standard.

1. [Créez le  [!DNL Excel] modèle à remplir avec les données du rapport](spreadsheet-feed-create-excel-template.md).

2. Créez le flux de la feuille de calcul :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >.[!UICONTROL Spreadsheet Feeds]**

   1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Dans la boîte de dialogue **[!UICONTROL Add Spreadsheet Feed]**, spécifiez les [paramètres de flux de feuille de calcul](spreadsheet-feed-settings.md).

   1. Cliquez sur **[!UICONTROL Submit]**.

   1. (Facultatif) Une fois que le [!UICONTROL Update Status] du flux est *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur.

      >[!NOTE]
      >
      >Si le modèle de rapport associé au flux est supprimé ultérieurement, le flux est également supprimé.

      Les flux de la feuille de calcul sont automatiquement actualisés chaque jour au [!UICONTROL Schedule Time] configuré. Si le modèle de rapport inclut des adresses pour des destinataires d’e-mails, ces adresses reçoivent des notifications lorsque la feuille de calcul est actualisée.

>[!MORELIKETHIS]
>
>* [À propos des flux de rapports de feuilles de calcul](spreadsheet-feed-about.md)
>* [Créer un [!DNL Excel] modèle pour un flux de rapports de feuille de calcul](spreadsheet-feed-create-excel-template.md)
>* [Modifier les paramètres de flux de rapports de feuille de calcul](spreadsheet-feed-edit.md)
>* [Paramètres de flux de rapports de feuille de calcul](spreadsheet-feed-settings.md)
>* [Afficher ou enregistrer un fichier de flux de rapports de feuille de calcul](spreadsheet-feed-view-or-save.md)
>* [Actualiser manuellement les flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
>* [Supprimer des flux de rapports de feuille de calcul](spreadsheet-feed-delete.md)
