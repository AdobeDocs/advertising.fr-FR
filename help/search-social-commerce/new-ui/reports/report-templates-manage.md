---
title: (Nouvelle interface utilisateur) Gestion des modèles de rapport
description: Découvrez comment créer, afficher, modifier et supprimer des modèles de rapport réutilisables pour les rapports planifiés et à la demande.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: eb12699872b7c89240f5340cd3b0a251c9c08366
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---
# (Nouvelle interface utilisateur) Gestion des modèles de rapport

Les modèles de rapport sont des dispositions de rapport prédéfinies que vous pouvez réutiliser lorsque vous générez la plupart des rapports. L&#39;utilisation de modèles vous permet de gagner du temps si vous souhaitez utiliser des paramètres autres que ceux par défaut, exécuter des variantes du même rapport ou exécuter le même rapport selon un planning régulier. Les modèles enregistrés sont disponibles dans l’onglet **[!UICONTROL Templates]** dans **[!UICONTROL Reports]>[!UICONTROL Reports]**.

Vous pouvez gérer jusqu’à 100 modèles à la fois.

L’affichage des données nécessite l’autorisation [!UICONTROL View Scheduled Reports] . La création, la duplication, la modification, l’exécution et la suppression de modèles, ainsi que la copie de données de ligne, nécessitent l’autorisation [!UICONTROL Edit Scheduled Reports]. Vous ne pouvez modifier que les modèles que vous avez créés.

## Actions disponibles

* [Créez un modèle de rapport](#template-create) en tant que nouveau modèle ou basé sur un modèle existant.

* [Afficher les paramètres d&#39;un modèle de rapport sans modifier l&#39;original](#template-view).

* [Modification d’un modèle de rapport](#template-edit), y compris de sa planification.

* [Exécution de rapports à la demande pour les modèles spécifiés](#template-run).

* [Supprimer des modèles de rapport](#template-delete).

* [Copiez toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard).

## Création d’un modèle de rapport {#template-create}

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Effectuez l’une des opérations suivantes :

   * Pour créer un modèle, cliquez sur **[!UICONTROL Create Template]**. Dans le panneau **[!UICONTROL Create a New Template]**, sélectionnez la catégorie et le type de rapport, puis cliquez sur **[!UICONTROL Proceed]**.

   * Pour créer un modèle basé sur un modèle existant, maintenez le curseur sur la ligne de modèle et cliquez sur ![Paramètres des modèles](/help/search-social-commerce/assets/settings-new.png "Paramètres des modèles") **[!UICONTROL Template Settings]** ou **[!UICONTROL ...]>[!UICONTROL Duplicate]**.

1. Saisissez un **[!UICONTROL Report Name]** unique pour le modèle et assurez-vous que **[!UICONTROL Save as Template]** est activé.

   Le paramètre est activé par défaut lorsque vous commencez par **[!UICONTROL Create Template]**. Si vous la désactivez, l’action finale devient **[!UICONTROL Run Report]**, ce qui génère un rapport au lieu d’enregistrer un modèle.

1. Configurez les paramètres des rapports [rapports de base et avancés](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [rapports d’assistance](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [rapports sur la précision des modèles](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) ou [rapports spécialisés](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md).

   Cliquez sur **[!UICONTROL Next]** pour accéder aux différentes sections de paramètres.

1. (Facultatif) Pour générer automatiquement des rapports, configurez les paramètres de **[!UICONTROL Frequency]** et de diffusion dans **[!UICONTROL Scheduling]**.

1. Cliquez sur **[!UICONTROL Create]**.

Vous pouvez également enregistrer un modèle lors de la [création d’un rapport à partir de l’onglet Derniers rapports](/help/search-social-commerce/new-ui/reports/management/report-manage.md) en **[!UICONTROL Save as Template]** activant avant d’envoyer les paramètres du rapport.

## Affichage des paramètres d’un modèle de rapport {#template-view}

Pour examiner les paramètres sans modifier le modèle d’origine, ouvrez un duplicata. Cette opération nécessite l’autorisation [!UICONTROL Edit Scheduled Reports]. L’ouverture du duplicata n’enregistre pas de nouveau modèle.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de modèle et cliquez sur ![Paramètres des modèles](/help/search-social-commerce/assets/settings-new.png "Paramètres des modèles") **[!UICONTROL Template Settings]**.

1. Vérifiez les paramètres du rapport.

1. Cliquez sur **[!UICONTROL Cancel]** lorsque vous avez terminé. Si vous êtes invité à annuler la configuration, cliquez sur **[!UICONTROL Discard]**.

Pour enregistrer une copie à la place, suivez la procédure [création d’un modèle](#template-create).

## Modification d’un modèle de rapport {#template-edit}

Vous pouvez modifier les paramètres et le planning de n’importe quel modèle que vous avez créé. Les modifications s’appliqueront aux rapports générés à partir du modèle à l’avenir.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Cochez la case en regard d’un modèle que vous avez créé.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

   [!UICONTROL Edit] n’est pas disponible lorsque plusieurs modèles sont sélectionnés ou que le modèle sélectionné a été créé par un autre utilisateur.

1. Modifiez les paramètres du rapport. Pour ajouter, modifier ou supprimer un planning, modifiez le **[!UICONTROL Frequency]** dans **[!UICONTROL Scheduling]**.

   Sélectionnez une fréquence quotidienne, hebdomadaire ou mensuelle pour les rapports planifiés. Pour supprimer une planification récurrente, sélectionnez **[!UICONTROL Now]**.

   **[!UICONTROL Save as Template]** et **[!UICONTROL Type]** sont en lecture seule lors de la modification d’un modèle existant. Vous n’avez pas besoin d’activer à nouveau [!UICONTROL Save as Template].

1. Cliquez sur **[!UICONTROL Save]**.

## Exécuter des rapports à la demande pour les modèles spécifiés {#template-run}

Vous pouvez exécuter des rapports pour un ou plusieurs modèles à tout moment.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Effectuez l’une des opérations suivantes :

   * (Pour exécuter un modèle unique) :

     1. Ouvrez le menu de la ligne de modèle et sélectionnez **[!UICONTROL Run]**.

     1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

   * (Pour exécuter un ou plusieurs modèles) :

     1. Cochez la case en regard de chaque modèle à exécuter.

     1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Run]**.

     1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

Vous pouvez également exécuter un modèle lors de sa modification en cliquant sur **[!UICONTROL Run Report]**, puis sur **[!UICONTROL Confirm]**. Commencez par enregistrer les modifications. Cette action exécute le modèle enregistré.

## Suppression de modèles de rapport {#template-delete}

Vous pouvez supprimer n’importe quel modèle de rapport disponible. Lorsque vous supprimez un modèle qui inclut un planning, ce rapport n’est plus généré.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Effectuez l’une des opérations suivantes :

   * (Pour supprimer un seul modèle) :

     1. Ouvrez le menu de la ligne de modèle et sélectionnez **[!UICONTROL Delete]**.

     1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

   * (Pour supprimer un ou plusieurs modèles) :

     1. Cochez la case en regard de chaque modèle à supprimer.

     1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

     1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.
