---
title: Modifier les paramètres du flux de rapports de feuille de calcul
description: Découvrez comment modifier les paramètres des flux de feuille de calcul.
exl-id: 063b5fb8-905f-480a-817f-f6b339af6028
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# Modifier les paramètres du flux de rapports de feuille de calcul

*Pour les rapports de base et les rapports de précision des modèles uniquement*

Vous pouvez modifier le modèle de rapport, [!DNL Microsoft® Excel] et d’autres paramètres sont utilisés pour un flux de feuille de calcul.

>[!NOTE]
>
> Si vous éditez les colonnes du modèle de rapport ou utilisez un nouveau modèle de rapport ou un modèle mis à jour, vous devez mettre à jour la variable [!DNL Excel] modèle en conséquence et chargez-le à nouveau.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Facultatif) Pour mettre à jour le modèle de rapport ou la variable [!DNL Excel] modèle utilisé pour le flux de feuille de calcul :

   * (Facultatif) Pour utiliser un modèle de rapport différent ou mis à jour pour le flux, [créer [!DNL Excel] modèle de rapport](spreadsheet-feed-create-excel-template.md).

     Vous devrez charger le modèle de rapport et le nouveau [!DNL Excel] à l’étape suivante.

   * (Facultatif) Pour simplement ajouter des colonnes personnalisées au [!DNL Excel] modèle, insérez les colonnes à droite des colonnes du modèle de rapport, puis enregistrez le fichier en tant que [!DNL Excel] feuille de calcul au format .XLSX. Vous devrez charger la nouvelle [!DNL Excel] à l’étape suivante.

1. Modifiez les paramètres du flux de la feuille de calcul :

   * Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * En regard du nom du flux de la feuille de calcul, cliquez sur ![Bouton Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Bouton Afficher/modifier les paramètres").

   * Dans le [!UICONTROL Edit Spreadsheet Feed] de la boîte de dialogue, modifiez la variable [paramètres de flux de feuille de calcul](spreadsheet-feed-settings.md).

   * Cliquez sur **[!UICONTROL Submit]**.

   * (Facultatif) Une fois que la variable [!UICONTROL Update Status] is *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur.

     >[!NOTE]
     >
     > Si le modèle de rapport associé au flux est ensuite supprimé, le flux est également supprimé.

     Les flux de feuille de calcul sont automatiquement actualisés à 8h00 chaque jour dans le fuseau horaire de l’annonceur. Si le modèle de rapport inclut des adresses pour des destinataires de courrier électronique, ces adresses reçoivent des notifications lorsque la feuille de calcul est actualisée.

>[!MORELIKETHIS]
>
>* [A propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [Création d’un flux de rapport de feuille de calcul](spreadsheet-feed-create.md)
>* [Créez un [!DNL Excel] modèle pour un flux de rapport de feuille de calcul](spreadsheet-feed-create-excel-template.md)
>* [Modifier les paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-edit.md)
>* [Paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-settings.md)
>* [Affichage ou enregistrement d’un fichier de flux de rapport de feuille de calcul](spreadsheet-feed-view-or-save.md)
>* [Actualisation manuelle des flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
