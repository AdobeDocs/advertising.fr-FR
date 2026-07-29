---
title: '[!DNL LY Ads] des paramètres de la campagne'
description: Référencez les paramètres des campagnes  [!DNL LY Ads] .
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# [!DNL LY Ads] des paramètres de la campagne

## \[Haut de la page]

**[!UICONTROL Campaign Name]:** nom de campagne unique au sein du compte.

**[!UICONTROL Status]:** statut d’affichage de la campagne : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Active*.

## onglet [!UICONTROL Basic Settings]

*Nouvelles campagnes uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte de réseau publicitaire.

**[!UICONTROL Campaign Type]:** Où placer les annonces : la seule option est *[!UICONTROL Search Network Only]* pour afficher des annonces textuelles sur le réseau de recherche.

## onglet [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** Le budget, qui est le montant que vous voulez dépenser chaque jour, en moyenne. Le budget minimum journalier est de 100 JPY.

Si vous affectez cette campagne à un portefeuille pour lequel les limites budgétaires de la campagne sont automatiquement ajustées, en fonction des conditions de recherche, vous pouvez dépenser plus ou moins que le budget spécifié au cours d&#39;une période donnée.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-yahoo-japan.md}}

## onglet [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-yahoo-japan.md}}

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (pour les [!UICONTROL EF Redirect] uniquement) Niveau auquel les clics et le chiffre d’affaires doivent être suivis en ajoutant une redirection (le cas échéant) et en ajoutant des paramètres aux URL pertinentes :

* *[!UICONTROL Keyword]:* pour suivre les données uniquement au niveau du mot-clé.

* *[!UICONTROL Creative]:* pour effectuer le suivi des données uniquement au niveau de l’annonce (contenu publicitaire).

* *[!UICONTROL Creative and Keyword]:* pour effectuer le suivi des données au niveau de l’annonce publicitaire (contenu créatif) et des mots-clés.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** ajoute un paramètre d’URL aux publicités du compte ou de la campagne pour le suivi des conversions.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [Gérer les campagnes](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
