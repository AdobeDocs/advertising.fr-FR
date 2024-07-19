---
title: Téléchargement de données à partir d’une vue de gestion de campagne
description: Découvrez comment télécharger des données à partir de la plupart des vues de gestion de campagne.
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Téléchargement de données à partir d’une vue de gestion de campagne

Vous pouvez télécharger des données à partir des vues [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] à l’exception des vues [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences] et [!UICONTROL Extensions]. Vous pouvez télécharger l’un des éléments suivants :

* Rapport au format [!DNL XLSM] (feuille de calcul [!DNL Microsoft Excel] prenant en charge les macros). Si vous sélectionnez des lignes spécifiques dans la vue, le rapport inclut alors une ligne pour chaque ligne sélectionnée. Si vous ne sélectionnez aucune ligne, une ligne est créée pour chaque ligne de la vue.

* Fichier de feuille d’envoi groupé au format TXT qui comprend toutes les entités enfants pertinentes. Si vous sélectionnez des lignes pour des entités sur plusieurs réseaux publicitaires, un fichier est créé pour chaque réseau publicitaire approprié. Si vous ne sélectionnez aucune ligne, un fichier est créé pour chaque réseau publicitaire représenté dans la vue. Les fichiers de feuilles d’envoi groupé générés pour différents réseaux publicitaires incluent différentes colonnes de données.

  Si vous générez des données pour plusieurs campagnes et que les données combinées se composent de plus de 500 000 lignes, les données sont ensuite divisées par campagne en deux fichiers ou plus, selon les besoins, nommés `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`, etc.

  Chaque fichier de feuille d’envoi groupé dans le panneau [!UICONTROL Downloads] est également répertorié dans la vue [!UICONTROL Bulksheets]. Une fois le fichier créé, vous recevez une notification par email avec un lien à partir duquel vous pouvez télécharger le fichier. Selon la quantité de données à compiler, la notification peut prendre plusieurs minutes ou plus. Toutefois, si la génération du fichier échoue, un fichier d’erreur est répertorié dans la vue Feuilles d’envoi groupées et vous recevez une notification par courrier électronique avec un lien vers le fichier d’erreur. La suppression d’un fichier de feuille d’envoi groupé du panneau [!UICONTROL Download] ou de l’onglet [!UICONTROL Bulksheets] le supprime des deux emplacements.

1. (Facultatif) Sélectionnez des lignes individuelles à inclure dans le fichier.

   Dans le cas contraire, toutes les données de la vue sont incluses.

1. À droite de la barre d’outils, cliquez sur ![Téléchargement de rapport](/help/search-social-commerce/assets/download.png "Téléchargement de rapport").

1. Cliquez sur ![Créer](/help/search-social-commerce/assets/add.png " ") **[!UICONTROL Create]**, ajoutez éventuellement le nom du fichier, puis cliquez sur **[!UICONTROL Report]** ou **[!UICONTROL Bulksheet]**.

1. (Facultatif) Une fois la tâche de rapport terminée, cliquez sur ![Téléchargement de rapport](/help/search-social-commerce/assets/download.png " pour afficher le panneau [!UICONTROL Available Reports], puis téléchargez ou supprimez le rapport :")

   * Pour ouvrir ou enregistrer le fichier selon la procédure normale de votre navigateur, cliquez sur ![Télécharger la feuille de calcul](/help/search-social-commerce/assets/download-spreadsheet.png "Télécharger la feuille de calcul").

     Pour plus d’informations sur la procédure de votre navigateur, consultez l’aide en ligne de votre navigateur.

   * Pour supprimer le fichier, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

>[!MORELIKETHIS]
>
>[ Supprimer un rapport de données de performances ou un fichier de feuille d’envoi groupé du menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
