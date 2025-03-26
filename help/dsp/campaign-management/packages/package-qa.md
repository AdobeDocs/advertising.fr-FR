---
title: Vérifier et modifier les paramètres du package à l’aide des feuilles d’envoi groupé
description: Découvrez comment vérifier et modifier les paramètres clés des packages en bloc à l’aide de feuilles de calcul.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: c482f476de5b79ee9a363791d62ba8c2ada12cbc
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Vérifier et modifier les paramètres du package à l’aide des feuilles d’envoi groupé

Vous pouvez télécharger les paramètres d’un ou plusieurs packages au format XLSX (feuille de calcul [!DNL Microsoft Excel]) pour révision. Le fichier *bulksheet* comprend un onglet distinct contenant des informations sur les vols.

Pour mettre à jour plusieurs paramètres à la fois, vous pouvez effectuer l’une des opérations suivantes :

* Apportez des modifications à certains champs, enregistrez le fichier et chargez à nouveau le fichier de feuille d’envoi groupé modifié dans DSP.

* Pour apporter des modifications à d’autres packages, emplacements ou annonces dans la campagne, téléchargez une feuille d’envoi groupé pour la campagne. Saisissez ou collez les paramètres mis à jour dans le fichier , puis chargez le fichier pour apporter les modifications. Pour obtenir des instructions, voir « [Vérification et modification des paramètres des composants Campaign à l’aide de feuilles d’envoi groupé](/help/dsp/campaign-management/campaign-components-review-edit.md) ».

Les champs modifiables incluent la plupart des paramètres qui sont normalement modifiables.

>[!TIP]
>
>Pour modifier rapidement d’autres champs pour un ou plusieurs packages, consultez « [ Modifier des packages ](/help/dsp/campaign-management/packages/package-edit.md). »

## Paramètres de téléchargement pour tous les packages d’une campagne

Lorsque vous téléchargez les paramètres de tous les packages d’une campagne, la feuille d’envoi groupé comprend des onglets distincts pour les paramètres du package et pour les informations de vol. Vous pouvez éventuellement inclure des paramètres pour les emplacements et les annonces associées aux packages ; des onglets supplémentaires sont inclus pour les paramètres d’emplacement et d’annonce.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * En regard de la campagne, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   * Cliquez sur le nom de la campagne. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

1. Dans la boîte de dialogue [!UICONTROL Bulksheet Download], désélectionnez les composants de campagne dont vous souhaitez exclure les paramètres du fichier téléchargé, puis cliquez sur **[!UICONTROL Download]**.

Par défaut, les paramètres de tous les emplacements et annonces publicitaires associés aux packages sont sélectionnés.

Un message de notification indique quand le fichier peut être téléchargé.

1. Pour télécharger le fichier, effectuez l’une des opérations suivantes :

   * Dans le message de notification, cliquez sur **[!UICONTROL Download].**

   * Dans la partie droite de la barre de menus supérieure, cliquez sur ![ Tâches ](/help/dsp/assets/downloads.png). Cliquez sur **[!UICONTROL Download]** en regard de la tâche.

     Le fichier est enregistré dans le dossier Téléchargements du navigateur.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     Pour modifier l’un des paramètres, modifiez directement le fichier, puis chargez les modifications. Toutes les colonnes modifiables sont surlignées en bleu.

## Paramètres de téléchargement pour des packages spécifiques

Lorsque vous téléchargez des paramètres pour des packages spécifiques, le fichier de feuille d’envoi groupé comprend des onglets distincts pour les paramètres du package et pour les informations de vol, et le fichier est modifiable.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Packages]**.

1. Cochez les cases des packages dont vous souhaitez télécharger les paramètres.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Un message de notification indique quand le fichier de feuille d’envoi groupé peut être téléchargé.

1. Pour télécharger la feuille d’envoi groupé, effectuez l’une des opérations suivantes :

   * Dans le message de notification, cliquez sur **[!UICONTROL Download].**

   * Dans la partie droite de la barre de menus supérieure, cliquez sur ![ Tâches ](/help/dsp/assets/downloads.png). Cliquez sur **[!UICONTROL Download]** en regard de la tâche.

     Le fichier est enregistré dans le dossier Téléchargements du navigateur. Consultez la section « [Colonnes d’emplacement dans les feuilles d’envoi groupé téléchargées/chargées](#qa-sheet-columns) » pour obtenir une liste des colonnes incluses.

     Pour modifier l’un des paramètres, modifiez directement le fichier, puis chargez les modifications. Toutes les colonnes modifiables sont surlignées en bleu. Pour utiliser le format correct pour un champ, sélectionnez et copiez la valeur à partir du paramètre de package ou du paramètre d’emplacement approprié. Pour certains paramètres de la cible, tels que le changement de date, les objectifs personnalisés et les mesures de conversion, une option de copie est disponible dans le paramètre .

## Charger une feuille d’envoi groupé avec les paramètres du package {#upload-bulksheet-package}

Vous pouvez charger les paramètres de vos packages, y compris les emplacements et les publicités associés aux packages, dans un fichier de feuille d’envoi groupé.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * En regard de la campagne parent, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Cliquez sur le nom de la campagne. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

     Cette option est disponible à partir de l’onglet [!UICONTROL Packages], [!UICONTROL Placements] ou [!UICONTROL Ads] .

   * Dans le sous-menu, cliquez sur **[!UICONTROL Packages]**, puis cochez la case d’un package. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Dans la boîte de dialogue [!UICONTROL Upload Bulksheet] :

   1. Faites glisser et déposez un fichier dans la zone ou cliquez à l’intérieur de la zone pour sélectionner un fichier sur votre appareil ou réseau.

   1. Cliquez sur **[!UICONTROL Upload]**.

1. (Facultatif) Pour vérifier que les mises à jour ont été traitées, cliquez sur ![Tâches](/help/dsp/assets/downloads.png) dans la partie droite de la barre de menus supérieure.

Lorsqu’une mise à jour de paramètre échoue, vous pouvez télécharger un fichier d’erreur de feuille d’envoi groupé avec un codage de couleur pour afficher les paramètres (lignes) enregistrés et ceux qui ont échoué, avec une raison pour chaque échec. Vous pouvez ensuite résoudre les problèmes du même fichier et le charger à nouveau pour traiter les informations corrigées.

<!--
## Package Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded bulksheet file, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |
-->

>[!MORELIKETHIS]
>
>* [Vérification et modification des paramètres des composants Campaign à l’aide de feuilles d’envoi groupé](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Modifier les packages](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paramètres du package](/help/dsp/campaign-management/packages/package-settings.md)
