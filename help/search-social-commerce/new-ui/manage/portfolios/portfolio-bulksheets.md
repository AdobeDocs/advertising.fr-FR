---
title: Modifier en masse les paramètres de portfolio à l’aide de fichiers de feuille d’envoi groupé
description: Découvrez comment modifier les paramètres de plusieurs portefeuilles à l’aide d’un fichier de feuille d’envoi groupé.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
TQID: https://experienceleague.adobe.com/tKCeMIgFKnW8hOU-6uavT9x7K9lL2Uqo2bWZ-H-Q5TE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2296997-5d79-4905-b32e-99b5aa892429id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 081453404883619e0a70bba080c857bf7e3136cc
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# Modifier en masse les paramètres de portfolio à l’aide de fichiers de feuille d’envoi groupé

*Fonction*

Une feuille groupée de portfolio est un fichier qui contient les paramètres de portfolio dans un format spécifique et qui peut être utilisé pour vérifier et modifier rapidement les paramètres. Vous pouvez générer (télécharger) des feuilles d’envoi groupé avec des paramètres pour un ou plusieurs portefeuilles. Le fichier est téléchargé sous la forme d’un classeur [!DNL Excel] avec deux feuilles de calcul (format XLSX). Le classeur comprend les éléments suivants :

* Feuille de calcul [!UICONTROL Instructions] en lecture seule contenant des informations sur la modification des champs.

* Un onglet [!UICONTROL Portfolio Settings Edit], avec une ligne par portefeuille inclus. Vous avez la possibilité de modifier les champs selon vos besoins, d’enregistrer le fichier localement, puis de [télécharger le fichier modifié](#portfolio-bulksheet-upload) vers Search, Social et Commerce. Les champs modifiables sont mis en surbrillance en couleur.

## Téléchargement d’un fichier de feuille d’envoi groupé avec les paramètres du portfolio

1. (Facultatif) Cochez la case en regard de chaque portefeuille à inclure dans la feuille d&#39;envoi groupé.

   Si vous ne sélectionnez pas de portefeuilles spécifiques, vous pouvez télécharger les paramètres de tous les portefeuilles.

1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur :

   * (Pour tous les portefeuilles) ![Opérations en bloc](/help/search-social-commerce/assets/chevron-down.png "Opérations en bloc") > **[!UICONTROL Export All Portfolios]**.

   * (Pour les portefeuilles sélectionnés) **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]**.

1. Saisissez le nom du fichier de feuille d&#39;envoi groupé à créer, puis cliquez sur **[!UICONTROL Export Now]**.

   Le fichier est enregistré dans le dossier Téléchargements par défaut de votre navigateur.

## Charger un fichier de feuille d’envoi groupé avec les paramètres de portfolio mis à jour {#portfolio-bulksheet-upload}

Le fichier doit être au format XLSX.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Opérations en bloc](/help/search-social-commerce/assets/chevron-down.png "Opérations en bloc") > **[!UICONTROL Import Portfolio Details]**.

1. Dans la boîte de dialogue [!UICONTROL Import Portfolio Details File] :

   1. Faites glisser et déposez un fichier dans la zone ou cliquez sur **[!UICONTROL Browse File]** pour sélectionner un fichier sur votre appareil ou réseau.

   1. Cliquez sur **[!UICONTROL Import]**.

Vous pouvez vérifier le statut du chargement à partir du bouton [!UICONTROL Global Sync Status] (![Statut de synchronisation global](/help/search-social-commerce/assets/global-sync-status.png "Statut de synchronisation global")) en regard du sélecteur de période. Si l’une des modifications n’a pas réussi, vous pouvez télécharger un fichier d’erreur indiquant ce qui a échoué.

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
