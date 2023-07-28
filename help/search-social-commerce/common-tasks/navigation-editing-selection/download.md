---
title: Téléchargement de données à partir d’une vue de gestion de campagne
description: Découvrez comment télécharger des données à partir de la plupart des vues de gestion de campagne.
exl-id: 0bbb02df-2ee0-4610-b60a-ca2b58daadbb
feature: Search Common Tasks
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Téléchargement de données à partir d’une vue de gestion de campagne

Vous pouvez télécharger des données à partir de la variable [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] sauf pour les [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences], et [!UICONTROL Extensions] vues. Vous pouvez télécharger l’un des éléments suivants :

* Un rapport dans [!DNL XLSM] (prenant en charge les macros [!DNL Microsoft® Excel] format (feuille de calcul). Si vous sélectionnez des lignes spécifiques dans la vue, le rapport inclut alors une ligne pour chaque ligne sélectionnée. Si vous ne sélectionnez aucune ligne, une ligne est créée pour chaque ligne de la vue.

* Fichier de feuille d’envoi groupé au format TXT qui comprend toutes les entités enfants pertinentes. Si vous sélectionnez des lignes pour des entités sur plusieurs réseaux publicitaires, un fichier est créé pour chaque réseau publicitaire approprié. Si vous ne sélectionnez aucune ligne, un fichier est créé pour chaque réseau publicitaire représenté dans la vue. Les fichiers de feuilles d’envoi groupé générés pour différents réseaux publicitaires incluent différentes colonnes de données.

  Si vous générez des données pour plusieurs campagnes et que les données combinées se composent de plus de 500 000 lignes, les données sont ensuite fractionnées par campagne en deux fichiers ou plus, selon les besoins, nommés `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`, etc.

  Chaque fichier de feuille d’envoi groupé dans la [!UICONTROL Downloads] est également répertorié dans la [!UICONTROL Bulksheets] vue. Une fois le fichier créé, vous recevez une notification par email avec un lien à partir duquel vous pouvez télécharger le fichier. Selon la quantité de données à compiler, la notification peut prendre plusieurs minutes ou plus. Toutefois, si la génération du fichier échoue, un fichier d’erreur est répertorié dans la vue Feuilles d’envoi groupées et vous recevez une notification par courrier électronique avec un lien vers le fichier d’erreur. Suppression d’un fichier de feuille d’envoi groupé de l’une des [!UICONTROL Download] ou le panneau [!UICONTROL Bulksheets] l’onglet le supprime des deux emplacements.

1. (Facultatif) Sélectionnez des lignes individuelles à inclure dans le fichier.

   Dans le cas contraire, toutes les données de la vue sont incluses.

1. À droite de la barre d’outils, cliquez sur ![Téléchargement du rapport](/help/search-social-commerce/assets/download.png "Téléchargement du rapport").

1. Cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer") **[!UICONTROL Create]**, ajoutez éventuellement le nom de fichier, puis cliquez sur l’une des options suivantes : **[!UICONTROL Report]** ou **[!UICONTROL Bulksheet]**.

1. (Facultatif) Une fois la tâche de rapport terminée, cliquez sur ![Téléchargement du rapport](/help/search-social-commerce/assets/download.png "Téléchargement du rapport") pour afficher la variable [!UICONTROL Available Reports] puis téléchargez ou supprimez le rapport :

   * Pour ouvrir ou enregistrer le fichier selon la procédure normale du navigateur, cliquez sur ![Télécharger la feuille de calcul](/help/search-social-commerce/assets/download-spreadsheet.png "Télécharger la feuille de calcul").

     Pour plus d’informations sur la procédure de votre navigateur, consultez l’aide en ligne de votre navigateur.

   * Pour supprimer le fichier, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

>[!MORELIKETHIS]
>
>[Supprimez un rapport de données de performances ou un fichier de feuille d’envoi groupé du [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
