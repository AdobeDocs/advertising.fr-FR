---
title: Modifier en masse les paramètres de portfolio à l’aide de fichiers de feuille d’envoi groupé
description: Découvrez comment modifier les paramètres de plusieurs portefeuilles à l’aide d’un fichier de feuille d’envoi groupé.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: 14f85e5ff5655be045fa4a2280edc1fe01978029
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Modifier en masse les paramètres de portfolio à l’aide de fichiers de feuille d’envoi groupé

*Fonction Beta*

Une feuille groupée de portfolio est un fichier qui contient les paramètres de portfolio dans un format spécifique et qui peut être utilisé pour vérifier et modifier rapidement les paramètres. Vous pouvez générer (télécharger) des feuilles d’envoi groupé avec des paramètres pour un ou plusieurs portefeuilles. Le fichier est téléchargé sous la forme d’un classeur [!DNL Excel] avec deux feuilles de calcul (format XLSX). Le classeur comprend les éléments suivants :

* Feuille de calcul [!UICONTROL Instructions] en lecture seule contenant des informations sur la modification des champs.

* Un onglet [!UICONTROL Portfolio Settings Edit], avec une ligne par portefeuille inclus. Vous avez la possibilité de modifier les champs selon vos besoins, d’enregistrer le fichier localement, puis de [télécharger le fichier modifié](#portfolio-bulksheet-upload) vers Search, Social et Commerce. Les champs modifiables sont mis en surbrillance en couleur.

## Téléchargement d’un fichier de feuille d’envoi groupé avec les paramètres du portfolio

1. Cochez la case en regard de chaque portefeuille à inclure dans la feuille d&#39;envoi groupé.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**.

1. Saisissez le nom du fichier de feuille d&#39;envoi groupé à créer, puis cliquez sur **[!UICONTROL Export Now]**.

   Le fichier est enregistré dans le dossier Téléchargements par défaut de votre navigateur.

## Charger un fichier de feuille d’envoi groupé avec les paramètres de portfolio mis à jour {#portfolio-bulksheet-upload}

Le fichier doit être au format XLSX.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]**. &lt;!— Doit être « Importer les paramètres Portfolio » — « Détails » peut être trop vague et suggérer d’inclure autre chose. —>

1. Dans la boîte de dialogue [!UICONTROL Import Portfolio Details File] : <!-- reword if we change the name of the operation -->

   1. Faites glisser et déposez un fichier dans la zone ou cliquez sur **[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? -->pour sélectionner un fichier sur votre appareil ou réseau.

   1. Cliquez sur **[!UICONTROL Import]**.

Vous pouvez vérifier le statut du chargement à partir du bouton [!UICONTROL Global Sync Status] (![Statut de synchronisation global](/help/search-social-commerce/assets/global-sync-status.png "Statut de synchronisation global")) en regard du sélecteur de période.<!-- icon similar to Refresh -->. Si l’une des modifications n’a pas réussi, vous pouvez télécharger un fichier d’erreur indiquant ce qui a échoué.

Les notifications sont également ajoutées au Centre de notifications. Vous pouvez ouvrir le volet Notifications à partir de l’icône ![Notifications](/help/search-social-commerce/assets/notifications-new.png "Notifications") située en regard du bouton [!UICONTROL Global Sync Status] (![Statut de synchronisation global](/help/search-social-commerce/assets/global-sync-status.png "Statut de synchronisation global")).

## Exigences de données pour les fichiers de feuilles d’envoi groupé chargés

Tous les fichiers de feuille d’envoi groupé doivent inclure la [!UICONTROL Portfolio ID] de colonne et chaque ligne de données doit inclure une valeur pour que le [!UICONTROL Portfolio ID] soit exploitable. Pour plus d’informations sur les exigences en matière de données, voir l’onglet [!UICONTROL Instructions] du fichier de feuille d’envoi groupé téléchargé.

Pour plus d’informations sur les colonnes de paramétrage du portfolio dans l’onglet [!UICONTROL Portfolio Settings Edit] , consultez le Guide d’optimisation , disponible dans Search, Social et Commerce.

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [ (nouvelle interface utilisateur) Modification d’un portfolio](portfolio-edit.md)
>* [Créer un portfolio](portfolio-create.md)
>* [ (nouvelle interface utilisateur) À propos des portfolios](portfolio-about.md)
