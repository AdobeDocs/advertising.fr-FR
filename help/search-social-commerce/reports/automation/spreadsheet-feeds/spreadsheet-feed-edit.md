---
title: Modifier les paramètres du flux de rapports de feuille de calcul
description: Découvrez comment modifier les paramètres des flux de feuille de calcul.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Modifier les paramètres du flux de rapports de feuille de calcul

*Pour les rapports de base et les rapports de précision des modèles uniquement*

Vous pouvez modifier le modèle de rapport, le modèle [!DNL Microsoft Excel] et d’autres paramètres utilisés pour un flux de feuille de calcul.

>[!NOTE]
>
> Si vous éditez les colonnes du modèle de rapport ou utilisez un nouveau modèle de rapport ou un modèle de rapport mis à jour, vous devez mettre à jour le modèle [!DNL Excel] en conséquence et le charger à nouveau.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Facultatif) Pour mettre à jour le modèle de rapport ou le modèle [!DNL Excel] utilisé pour le flux de feuille de calcul :

   * (Facultatif) Pour utiliser un modèle de rapport différent ou mis à jour pour le flux, [ créez un modèle  [!DNL Excel] pour le modèle de rapport](spreadsheet-feed-create-excel-template.md).

     Vous devrez charger le modèle de rapport et le nouveau fichier [!DNL Excel] à l’étape suivante.

   * (Facultatif) Pour simplement ajouter des colonnes personnalisées au modèle [!DNL Excel], insérez les colonnes à droite des colonnes du modèle de rapport, puis enregistrez le fichier sous forme de feuille de calcul [!DNL Excel] au format .XLSX. Vous devrez charger le nouveau fichier [!DNL Excel] à l’étape suivante.

1. Modifiez les paramètres du flux de la feuille de calcul :

   * Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * En regard du nom du flux de la feuille de calcul, cliquez sur le bouton ![Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Bouton Afficher/modifier les paramètres").

   * Dans la boîte de dialogue [!UICONTROL Edit Spreadsheet Feed], modifiez les [ paramètres de flux de feuille de calcul ](spreadsheet-feed-settings.md).

   * Cliquez sur **[!UICONTROL Submit]**.

   * (Facultatif) Une fois que le [!UICONTROL Update Status] du flux est *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur.

     >[!NOTE]
     >
     > Si le modèle de rapport associé au flux est ensuite supprimé, le flux est également supprimé.

     Les flux de feuille de calcul sont automatiquement actualisés à 8h00 chaque jour dans le fuseau horaire de l’annonceur. Si le modèle de rapport inclut des adresses pour des destinataires de courrier électronique, ces adresses reçoivent des notifications lorsque la feuille de calcul est actualisée.

>[!MORELIKETHIS]
>
>* [À propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [Créer un flux de rapport de feuille de calcul](spreadsheet-feed-create.md)
>* [ Créez un  [!DNL Excel] modèle pour un flux de rapport de feuille de calcul](spreadsheet-feed-create-excel-template.md)
>* [Modifier les paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-edit.md)
>* [Paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-settings.md)
>* [ Afficher ou enregistrer un fichier de flux de rapport de feuille de calcul ](spreadsheet-feed-view-or-save.md)
>* [Actualisation manuelle des flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
