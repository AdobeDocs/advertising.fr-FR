---
title: Modifier les paramètres du flux de rapports d'une feuille de calcul
description: Découvrez comment modifier les paramètres des flux de feuilles de calcul.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Modifier les paramètres du flux de rapports d&#39;une feuille de calcul

*Pour les rapports de base et les rapports sur la précision des modèles uniquement*

Vous pouvez modifier le modèle de rapport, [!DNL Microsoft Excel] modèle et d&#39;autres paramètres utilisés pour un flux de feuille de calcul.

>[!NOTE]
>
> Si vous modifiez les colonnes du modèle de rapport ou utilisez un modèle de rapport nouveau ou mis à jour, vous devez mettre à jour le modèle de [!DNL Excel] en conséquence et le charger à nouveau.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Facultatif) Pour mettre à jour le modèle de rapport ou le modèle de [!DNL Excel] utilisé pour le flux de feuille de calcul :

   * (Facultatif) Pour utiliser un modèle de rapport différent ou mis à jour pour le flux, [créez un nouveau modèle  [!DNL Excel]  modèle de rapport](spreadsheet-feed-create-excel-template.md).

     À l&#39;étape suivante, vous devrez charger le modèle de rapport et le nouveau fichier [!DNL Excel].

   * (Facultatif) Pour ajouter simplement des colonnes personnalisées au modèle de [!DNL Excel], insérez les colonnes à droite des colonnes du modèle de rapport, puis enregistrez le fichier en tant que feuille de calcul [!DNL Excel] au format .XLSX. Vous devrez charger le nouveau fichier [!DNL Excel] à l’étape suivante.

1. Modifiez les paramètres de flux de la feuille de calcul :

   * Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * En regard du nom du flux de la feuille de calcul, cliquez sur ![bouton Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "bouton Afficher/modifier les paramètres").

   * Dans la boîte de dialogue [!UICONTROL Edit Spreadsheet Feed], modifiez les [paramètres de flux de feuille de calcul](spreadsheet-feed-settings.md).

   * Cliquez sur **[!UICONTROL Submit]**.

   * (Facultatif) Une fois le [!UICONTROL Update Status] du flux *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur.

     >[!NOTE]
     >
     > Si le modèle de rapport associé au flux est supprimé ultérieurement, le flux est également supprimé.

     Les flux des feuilles de calcul sont automatiquement actualisés à 8 h chaque jour dans le fuseau horaire de l’annonceur. Si le modèle de rapport inclut des adresses pour des destinataires d’e-mails, ces adresses reçoivent des notifications lorsque la feuille de calcul est actualisée.

>[!MORELIKETHIS]
>
>* [À propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [Créer un flux de rapport de feuille de calcul](spreadsheet-feed-create.md)
>* [Créer un modèle [!DNL Excel] de flux de rapport de feuille de calcul](spreadsheet-feed-create-excel-template.md)
>* [Modifier les paramètres de flux de rapports des feuilles de calcul](spreadsheet-feed-edit.md)
>* [Paramètres de flux de rapports des feuilles de calcul](spreadsheet-feed-settings.md)
>* [Afficher ou enregistrer un fichier de flux de rapports de feuille de calcul](spreadsheet-feed-view-or-save.md)
>* [Actualiser manuellement les flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
