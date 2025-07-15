---
title: Télécharger des données à partir d’une vue de gestion de campagne
description: Découvrez comment télécharger des données à partir de la plupart des vues de gestion de campagnes.
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 723d50d11cd76471ac41d3bb007af4f5d1bfa32f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# (interface utilisateur héritée) Télécharger des données à partir d’une vue de gestion de campagne

*Interface utilisateur héritée*

Vous pouvez télécharger des données à partir des vues [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns], à l’exception des vues [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences] et [!UICONTROL Extensions]. Vous pouvez télécharger l’une des options suivantes :

* Rapport au format [!DNL XLSM] (feuille de calcul [!DNL Microsoft Excel] prenant en charge les macros). Si vous sélectionnez des lignes spécifiques dans la vue, le rapport inclut une ligne pour chaque ligne sélectionnée. Si vous ne sélectionnez aucune ligne, une ligne est créée pour chaque ligne de la vue.

* Fichier de feuille d’envoi groupé au format TXT qui comprend toutes les entités enfant pertinentes. Si vous sélectionnez des lignes pour des entités sur plusieurs réseaux publicitaires, un fichier est créé pour chaque réseau publicitaire approprié. Si vous ne sélectionnez aucune ligne, un fichier est créé pour chaque réseau publicitaire représenté dans la vue. Les fichiers de feuilles d’envoi groupé générés pour différents réseaux publicitaires incluent différentes colonnes de données.

  Si vous générez des données pour plusieurs campagnes et que les données combinées se composent de plus de 500 000 lignes, les données sont ensuite fractionnées par campagne en deux fichiers ou plus, selon les besoins, nommés `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`, etc.

  Chaque fichier de feuille d&#39;envoi groupé du panneau [!UICONTROL Downloads] est également répertorié dans la vue [!UICONTROL Bulksheets]. Lorsque le fichier est créé, vous recevez une notification par e-mail avec un lien à partir duquel vous pouvez télécharger le fichier ; selon la quantité de données compilées, la notification peut prendre plusieurs minutes ou plus. En revanche, si la génération du fichier échoue, un fichier d’erreur est répertorié dans la vue Feuilles d’envoi groupé et vous recevez une notification par e-mail avec un lien vers le fichier d’erreur. La suppression d’un fichier de feuille d’envoi groupé du panneau [!UICONTROL Download] ou de l’onglet [!UICONTROL Bulksheets] le supprime des deux emplacements.

>[!NOTE]
>
>Consultez également l’aide sur le téléchargement de données dans la nouvelle interface utilisateur à partir de la « vue [[!UICONTROL Portfolios] »](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md) de la « vue [[!UICONTROL Campaigns] »](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md) et de la « vue [[!UICONTROL Ad Groups] »](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md).

1. (Facultatif) Sélectionnez les lignes individuelles à inclure dans le fichier.

   Sinon, toutes les données de la vue sont incluses.

1. Sur le côté droit de la barre d’outils, cliquez sur ![Téléchargement du rapport](/help/search-social-commerce/assets/download.png "Téléchargement du rapport").

1. Cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer") **[!UICONTROL Create]**, ajoutez éventuellement le nom du fichier, puis cliquez sur **[!UICONTROL Report]** ou **[!UICONTROL Bulksheet]**.

1. (Facultatif) Une fois la tâche de rapport terminée, cliquez sur ![Téléchargement du rapport](/help/search-social-commerce/assets/download.png "Téléchargement du rapport") pour afficher le panneau [!UICONTROL Available Reports], puis téléchargez ou supprimez le rapport :

   * Pour ouvrir ou enregistrer le fichier conformément à la procédure normale de votre navigateur, cliquez sur ![Télécharger la feuille de calcul](/help/search-social-commerce/assets/download-spreadsheet.png "Télécharger la feuille de calcul").

     Pour plus d’informations sur la procédure de votre navigateur, reportez-vous à l’aide en ligne de votre navigateur.

   * Pour supprimer le fichier, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

>[!MORELIKETHIS]
>
>* [(interface utilisateur héritée) Supprimez un rapport de données de performances ou un fichier de feuille d’envoi groupé du menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [(Nouvelle interface utilisateur) Gérer les rapports de vue de données à partir de la vue [!UICONTROL Portfolios]](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-report.md)
>* [(Nouvelle interface utilisateur) Gérer les rapports de vue de données à partir de la vue [!UICONTROL Campaigns]](/help/search-social-commerce/new-ui/manage/campaigns/campaign-view-report.md)
>* [(Nouvelle interface utilisateur) Gérer les rapports de vue de données à partir de la vue [!UICONTROL Ad Groups]](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-view-report.md)
