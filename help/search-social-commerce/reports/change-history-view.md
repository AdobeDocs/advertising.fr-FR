---
title: Afficher le rapport [!UICONTROL Change History]
description: Découvrez comment afficher les modifications récentes apportées au compte de l’annonceur.
exl-id: f8744da7-cc7a-49c1-aeac-1e601768f992
feature: Search Reports
TQID: https://experienceleague.adobe.com/nRlvKpVQf3wbMd83plf3CQp1pPYpHVJzMVJN54lryYM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 84eb5f060a696e057f706c0066c18c9afc1511e1
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 0%

---

# Afficher le rapport [!UICONTROL Change History]

Le rapport (nouvelle interface utilisateur) [!UICONTROL History Logs] et (ancienne interface utilisateur) [!UICONTROL Change History] comprend un journal des modifications apportées au compte de l’annonceur au cours des 31 derniers jours. Le rapport peut inclure des modifications apportées aux types d’objets suivants : utilisateurs (annonceurs), portfolios, campagnes, groupes publicitaires, publicités, mots-clés, emplacements et cibles de produits. Vous pouvez trier et filtrer les données selon n’importe quelle colonne.

Vous pouvez télécharger des informations supplémentaires sur les journaux d’historique de l’annonceur dans un fichier [!DNL Microsoft Excel] format de classeur (fichier XLSX). Le rapport inclut les anciennes et les nouvelles valeurs ainsi que l’heure à laquelle la modification a eu lieu.

>[!NOTE]
>
>Pour les modifications apportées aux portefeuilles, consultez également l’historique des modifications du [portefeuille](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-view-change-history.md).

## (Nouvelle interface utilisateur) Afficher le rapport [!UICONTROL History Logs] {#history-logs-open}

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL History Logs]**.

1. (Facultatif) [Modifiez les données incluses dans la vue](/help/search-social-commerce/common-tasks/data-views/data-views-about.md).

### Gérer les téléchargements de rapports pour [!UICONTROL History Logs]

#### Générer un rapport avec les lignes de données filtrées

1. [Ouvrez les journaux d’historique](#history-logs-open).

1. Dans le coin supérieur droit, cliquez sur ![Télécharger le rapport](/help/search-social-commerce/assets/download.png "Télécharger le rapport").

1. Dans les paramètres de [!UICONTROL Grid Reports], saisissez un nom de rapport unique, puis cliquez sur **[!UICONTROL Generate]**.

   Par défaut, le fichier est nommé « allChangeHistory_YYYYMMDD_NNNN », où « NNNN » est le numéro de tâche séquentielle (par exemple, « allChangeHistory_20260402_1326 »).

   Le fichier est ajouté à la liste de [!UICONTROL Recently Generated].

1. (Facultatif) Pour télécharger le fichier une fois l’opération terminée, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

#### Télécharger un rapport terminé

1. [Ouvrez les journaux d’historique](#history-logs-open).

1. Dans le coin supérieur droit, cliquez sur ![Télécharger le rapport](/help/search-social-commerce/assets/download.png "Télécharger le rapport").

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

#### Supprimer un rapport terminé

1. [Ouvrez les journaux d’historique](#history-logs-open).

1. Dans le coin supérieur droit, cliquez sur ![Télécharger le rapport](/help/search-social-commerce/assets/download.png "Télécharger le rapport").

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") en regard du nom du fichier.

## (interface utilisateur héritée) Afficher le rapport [!UICONTROL Change History]

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Insights & Reports]** > **[!UICONTROL Change History]**.

1. (Facultatif) Modifiez les données incluses dans le rapport de l’une des manières suivantes :

   * (Pour afficher ou masquer des colonnes) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png "Flèche vers le bas") sur le côté droit de n’importe quel en-tête de colonne, mettez en surbrillance **[!UICONTROL Columns]**, puis activez la case à cocher en regard de chaque colonne à inclure et désactivez la case à cocher en regard de chaque colonne à exclure.

     La configuration des colonnes s’applique à l’affichage de tous les annonceurs.

   * (Pour filtrer les données par valeur de colonne) Effectuez l’une des opérations suivantes :

      * [Appliquer un filtre à partir du lien **[!UICONTROL Add Filter]**](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

      * [Appliquer un filtre à partir du menu d’en-tête de colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

   * (Pour modifier la période du rapport) Procédez comme suit :

      1. Au-dessus du tableau de données, cliquez sur la période en cours.

      1. Spécifiez la plage :

         * (Pour une plage prédéfinie) — Effectuez un choix dans la liste des incréments de temps courants. La valeur par défaut est *[!UICONTROL 2 Days Ago]*.

         * (Pour une plage spécifique) : sélectionnez **[!UICONTROL Custom Date Range]**, puis spécifiez la date de début et la date de fin.

           Saisissez les dates au format MM/JJ/AAAA ou MM-JJ-AAAA, ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar.png "Calendrier") en regard de chaque champ pour ouvrir le calendrier et sélectionner une date. Vous ne pouvez inclure que les données des 31 jours précédents.

      1. Cliquez sur **[!UICONTROL Apply]**.

1. (Facultatif) Téléchargez une copie du rapport :

   1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Download]**.

      Une fois le rapport terminé, il est répertorié dans le menu [!UICONTROL Download].

   1. (Pour ouvrir ou enregistrer les données du rapport dans un fichier) Cliquez sur ![Télécharger le rapport en tant que XLS](/help/search-social-commerce/assets/download-spreadsheet2.png "Télécharger le rapport en tant que XLS") en regard du nom de fichier, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur.

      Pour plus d’informations, consultez l’aide en ligne de votre navigateur.
