---
title: Vérifier et modifier les paramètres des composants de Campaign à l’aide de feuilles d’envoi groupé
description: Découvrez comment examiner et modifier en bloc des packages, des emplacements et des paramètres d’annonces clés à l’aide de feuilles de calcul.
feature: DSP Placements
exl-id: 1ec8362a-d37b-4fd7-becd-3a5b4f0c9504
source-git-commit: 7af6788f2aae3a2fb9e2048676dbe1955c2e56d9
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Vérifier et modifier les paramètres des composants de Campaign à l’aide de feuilles d’envoi groupé

Vous pouvez télécharger les paramètres des packages, des emplacements et des annonces publicitaires dans une seule campagne au format XLSX (feuille de calcul [!DNL Microsoft Excel]) pour consulter et modifier les paramètres. Par défaut, le fichier téléchargé, appelé *feuille d’envoi groupé*, comprend des onglets distincts pour les paramètres de package, les informations de vol du package, les paramètres d’emplacement et les plannings d’annonces d’emplacement. Vous pouvez éventuellement exclure les paramètres de certains types de composants de campagne.

Pour mettre à jour plusieurs paramètres à la fois, chargez un fichier de feuille d’envoi groupé valide avec les modifications. Pour créer la feuille d’envoi groupé, modifiez une feuille d’envoi groupé téléchargée avec les paramètres existants. Les champs modifiables incluent la plupart des paramètres qui sont normalement modifiables. Les champs des paramètres qui ne sont pas utilisés contiennent des valeurs vides.

>[!NOTE]
>
>Vous pouvez également télécharger et modifier les paramètres pour des packages et des emplacements spécifiques uniquement. Voir « [Vérification et modification des paramètres de package à l’aide des feuilles d’envoi groupé](/help/dsp/campaign-management/packages/package-qa.md) » et « [Vérification et modification des paramètres d’emplacement à l’aide des feuilles d’envoi groupé](/help/dsp/campaign-management/placements/placement-qa.md) ».

## Paramètres de téléchargement des packages, des emplacements et des annonces publicitaires dans une campagne {#download-bulksheet-campaign}

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * En regard de la campagne, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   * Cliquez sur le nom de la campagne. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

1. Dans la boîte de dialogue [!UICONTROL Bulksheet Download], désélectionnez les composants de campagne dont vous souhaitez exclure les paramètres du fichier téléchargé, puis cliquez sur **[!UICONTROL Download]**.

Par défaut, les paramètres de tous les composants de campagne sont sélectionnés.

Un message de notification indique quand le fichier peut être téléchargé.

1. Pour télécharger le fichier, effectuez l’une des opérations suivantes :

   * Dans le message de notification, cliquez sur **[!UICONTROL Download].**

   * Dans la partie droite de la barre de menus supérieure, cliquez sur ![ Tâches ](/help/dsp/assets/downloads.png). Cliquez sur **[!UICONTROL Download]** en regard de la tâche.

     Le fichier est enregistré dans le dossier Téléchargements du navigateur.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     Pour modifier l’un des paramètres, modifiez directement le fichier, puis chargez les modifications. Toutes les colonnes modifiables sont surlignées en bleu. Pour utiliser le format correct pour un champ, sélectionnez et copiez la valeur à partir du paramètre de package ou du paramètre d’emplacement approprié. Pour certains paramètres de la cible, tels que le changement de date, les objectifs personnalisés et les mesures de conversion, une option de copie est disponible dans le paramètre .

## Charger une feuille d’envoi groupé avec les paramètres de package, d’emplacement et d’annonce pour une campagne{#upload-bulksheet-campaign-components}

Chargez les paramètres des packages, des emplacements et des annonces publicitaires dans une seule campagne en une seule fois dans une feuille d’envoi groupé remplie.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * En regard de la campagne, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Cliquez sur le nom de la campagne. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Dans la boîte de dialogue [!UICONTROL Upload Bulksheet] :

   1. Faites glisser et déposez un fichier dans la zone ou cliquez à l’intérieur de la zone pour sélectionner un fichier sur votre appareil ou réseau.

   1. Cliquez sur **[!UICONTROL Upload]**.

1. (Facultatif) Pour vérifier que les mises à jour ont été traitées, cliquez sur ![Tâches](/help/dsp/assets/downloads.png) dans la partie droite de la barre de menus supérieure.

Lorsqu’une mise à jour de paramètre échoue, vous pouvez télécharger un fichier d’erreur de feuille d’envoi groupé avec un codage de couleur pour afficher les paramètres (lignes) enregistrés et ceux qui ont échoué, avec une raison pour chaque échec. Vous pouvez ensuite résoudre les problèmes du même fichier et le charger à nouveau pour traiter les informations corrigées.


<!--
## Placement Setting Columns in Downloaded/Uploaded Spreadsheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded spreadsheet, all editable columns are highlighted in blue.

### Campaign-level Spreadsheets

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Any applied labels, for reporting. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | A link to open the placement in Edit mode. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Status] | The placement status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | The placement type. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | The name of the parent package, when applicable. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | The start date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL End Date] | The end date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Whether dayparting is *[!UICONTROL ON]* or *[!UICONTROL OFF]*.<br><b>Note:</b> To check the actual dayparting schedule, open the placement settings in DSP. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Budget] | The placement budget, if there is one. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | The objective of the package. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | The target value of the goal. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Whether the placement is pacing towards the *[!UICONTROL Budget]* or *[!UICONTROL Impressions]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | The maximum bid for the placement. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the placement: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the placement: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Any pre-bid filter criteria to be applied. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Whether bidding rules (deprecated) are *[!UICONTROL ON]* or *[!UICONTROL OFF]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | The primary frequency cap for the placement during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the placement during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | The number of targeted geographical locations, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | The targeted geographical locations, separated by semi-colons,or *[!UICONTROL All Locations]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | The number of excluded geographical locations or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | The excluded geographical locations, separated by semi-colons,  or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | The number of targeted public inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | The number of excluded public inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | The number of targeted private inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | The number of excluded private inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | The number of targeted [!UICONTROL On-Demand Inventory] deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | The number of excluded On-Demand Inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | The targeted type of traffic: *[!UICONTROL Website]* and/or *[!UICONTROL Apps]* | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Whether the Inventory Targeting option to exclude outstream traffic is <i[!UICONTROL >ON]* or *[!UICONTROL OFF]*.<br>Outstream ads usually appear over the content as a pop-up or stuffed into content (in the native experience), rather than as regular video ads in a video player. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | The quality of the sites to target: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, or *[!UICONTROL All Sites]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | The number of targeted site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | The number of excluded site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | The excluded sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Language] | The targeted site languages. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Standard display placements only) Whether or not to allow ad delivery on non-audited sites: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. When the placement targets private inventory, this option may deliver ads on blocked sites. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | The number of targeted sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | The targeted audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | The excluded audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Whether or not [!DNL Comscore] demographic segments are enabled for the placement (and other placements in the campaign): *[!UICONTROL ON]* or *[!UICONTROL OFF]*. This feature may be enabled only for campaigns for which the [!DNL Audience Verification] feature is enabled for [!DNL Nielsen] and/or [!DNL Comscore].  It incurs additional fees.  | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Whether or not to extend the ad targeting across devices: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Included # | The number of targeted topic codes, if any are specified, or *[!UICONTROL All]*.   | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | The number of excluded topic codes, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | The number of targeted device targets, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | The number of excluded device targets, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | The number of targeted ISP providers, if any are specified, or *[!UICONTROL All]/i>. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | The number of excluded ISP providers, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | The number of brand safety filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | The number of pre-bid fraud blocking filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | The number of pre-bid viewability filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |
-->

>[!MORELIKETHIS]
>
>* [Vérification et modification des paramètres de package à l’aide de feuilles d’envoi groupé](/help/dsp/campaign-management/packages/package-qa.md)
>* [Paramètres du package](/help/dsp/campaign-management/packages/package-settings.md)
>* [Vérification et modification des paramètres d’emplacement à l’aide des feuilles d’envoi groupé](/help/dsp/campaign-management/placements/placement-qa.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Paramètres de publicité audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Paramètres TV connectés](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Afficher les paramètres de publicité](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Paramètres des annonces publicitaires mobiles](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Paramètres natifs des publicités display](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Paramètres de publicité preroll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Paramètres universels des publicités vidéo](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
