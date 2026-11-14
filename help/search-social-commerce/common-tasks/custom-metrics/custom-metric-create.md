---
title: Création d’une mesure personnalisée
description: Découvrez comment configurer des mesures personnalisées, qui sont calculées à partir de mesures standard.
exl-id: a9ce503a-67ee-477e-8f79-31b4a9c6e51a
feature: Search Common Tasks, Search Custom Metrics
TQID: 'https://experienceleague.adobe.com/g-J8AlulQ20I-vxQrPkPaP-Ap66bBIng0eKDPqhV9U4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: a1695a4d-41fb-5bb6-a22a-9e7a1b3222d7
    internal-label: Search Custom Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 9837cac1a920b1b3b88b04b150cb604832209eaf
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%
---
# Création d’une mesure personnalisée

## (Nouvelle interface utilisateur) Créer une mesure personnalisée à partir d’une vue de gestion

*Disponible dans la plupart des vues d&#39;entités dans le menu [!UICONTROL Manage],<!-- [!UICONTROL Plan] > [!UICONTROL Simulations],--> [!UICONTROL Setup] > [!UICONTROL Label Classifications], [!UICONTROL Goals] > [!UICONTROL Objectives] et [!UICONTROL Constraints], et [!UICONTROL Targeting] > [!UICONTROL Placements]*

1. Au-dessus du tableau de données, effectuez l’une des opérations suivantes :

   * Cliquez sur le nom de la vue actuellement appliquée (![Vue](/help/search-social-commerce/assets/view.png "Vue")). Placez le curseur sur le nom d’une vue modifiable et cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") pour ouvrir les paramètres de la vue.

     La mesure personnalisée que vous créez sera disponible dans toutes vos vues.

   * Cliquez sur ![Colonnes personnalisées](/help/search-social-commerce/assets/custom-columns-new.png "Colonnes personnalisées") pour ouvrir les paramètres de configuration des colonnes.

1. Sous la liste de colonnes qui s’ouvre, cliquez sur ![Créer une mesure personnalisée](/help/search-social-commerce/assets/add.png "Créer une mesure personnalisée") **[!UICONTROL Create Custom Metric]**.

1. Spécifiez les [paramètres de mesure personnalisés](custom-metric-settings.md).

1. Cliquez sur **[!UICONTROL Create]**.

## (Nouvelle interface utilisateur) Créer une mesure personnalisée à partir des paramètres d’un rapport ou d’un modèle de rapport {#create-from-report-settings}

1. Dans les paramètres du rapport ou du modèle de rapport, passez à l’étape **[!UICONTROL Columns]**.

1. Dans la section **[!UICONTROL Custom Metrics]**, spécifiez les paramètres de mesure :

   * **[!UICONTROL Custom Metric Name]:** Saisissez un nom pour la mesure.

   * **[!UICONTROL Format]:** sélectionnez **[!UICONTROL Currency]**, **[!UICONTROL Number to 2 Decimal Places]**, **[!UICONTROL Number to 3 Decimal Places]**, **[!UICONTROL Number w/out Decimal Places]** ou **[!UICONTROL Percentage]**.

   * **[Champ de saisie de formule] :** Créez la formule en sélectionnant des mesures dans **[!UICONTROL Insert Metric]** et en cliquant sur les boutons de l’opérateur (`+`, `-`, `*`, `/`, `(` et `)`). Vous pouvez également saisir la formule manuellement. Placez le curseur à l’endroit où vous souhaitez insérer chaque mesure ou opérateur.

1. Cliquez sur **[!UICONTROL Add Metric]**.

   Une fois la mesure créée, la liste des colonnes disponibles est filtrée en fonction de son nom. Sa création ne l’inclut pas automatiquement dans le rapport.

1. Pour inclure la mesure dans le rapport, sélectionnez-la dans la liste des colonnes disponibles et cliquez sur ![Flèche à droite](/help/search-social-commerce/assets/arrow-right-customize.png "Flèche à droite") pour la déplacer dans la liste des colonnes sélectionnées.

## (interface utilisateur héritée) Créer une mesure personnalisée à partir d’une vue de gestion de campagne

1. Au-dessus du tableau de données, effectuez l’une des opérations suivantes :

   * Cliquez sur le nom de la vue par défaut ou personnalisée pour ouvrir les paramètres de la vue.

   * Cliquez sur ![Colonnes personnalisées](/help/search-social-commerce/assets/custom-columns.png "Colonnes personnalisées") pour ouvrir les paramètres de configuration des colonnes.

1. Sous la liste de colonnes qui s’ouvre, cliquez sur ![Créer une mesure personnalisée](/help/search-social-commerce/assets/add.png "Créer une mesure personnalisée") **[!UICONTROL Create New Custom Metric]**.

1. Spécifiez les [paramètres de mesure personnalisés](custom-metric-settings.md).

1. Cliquez sur **[!UICONTROL Save]**.

## (interface utilisateur héritée) Créer une mesure personnalisée à partir d’un rapport ou d’un formulaire de modèle de rapport

1. Dans un rapport ou un formulaire de modèle de rapport, accédez à l&#39;onglet **[!UICONTROL Columns]**.

1. Dans la section de droite, cliquez sur **[!UICONTROL Create]**.

1. Spécifiez les [paramètres de mesure personnalisés](custom-metric-settings.md).

1. Cliquez sur **[!UICONTROL Submit]**.

## (interface utilisateur héritée) Créer une mesure personnalisée à partir des vues [!UICONTROL Portfolios]

1. Au-dessus du tableau de données, cliquez sur ![Modifier la vue sélectionnée](/help/search-social-commerce/assets/view-settings.png "Modifier la vue sélectionnée").

1. Cliquez sur l’onglet **[!UICONTROL Columns]**.

1. Dans la section de droite, cliquez sur **[!UICONTROL Create]**.

1. Spécifiez les [paramètres de mesure personnalisés](custom-metric-settings.md).

1. Cliquez sur **[!UICONTROL Submit]**.

>[!MORELIKETHIS]
>
>* [À propos des mesures personnalisées](custom-metric-about.md)
>* [Modifier une mesure personnalisée](custom-metric-edit.md)
>* [Supprimer une mesure personnalisée](custom-metric-delete.md)
>* [Paramètres de mesure personnalisés](custom-metric-settings.md)
