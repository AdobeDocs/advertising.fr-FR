---
title: '[!DNL Baidu] paramètres de la campagne'
description: Référencez les paramètres des campagnes [!DNL Baidu].
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!DNL Baidu] paramètres de la campagne

## \[Haut de la page]

**[!UICONTROL Campaign Name]:** Nom de campagne unique dans le compte.

**[!UICONTROL Status]:** Statut d’affichage de la campagne : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Active*.

## Onglet [!UICONTROL Basic Settings]

*Nouvelles campagnes uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte réseau publicitaire.

**[!UICONTROL Campaign Type]:** Où placer des annonces publicitaires et quels types d’annonces la campagne peut contenir. La seule option est *Rechercher réseau uniquement*.

## Onglet [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:**(Applicable aux campagnes qui ciblent des audiences dans l’Union européenne (UE)) Que la campagne contienne ou non de la publicité politique selon les exigences pour les publicités diffusées dans l’Union européenne en vertu du règlement 2024/90 de l’UE : *[!UICONTROL Yes]* ou *[!UICONTROL No]*.

## Onglet [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]:** Stratégie d’enchères pour la campagne :

* *[!UICONTROL Maximize Conversions]:* Le réseau publicitaire — et non Search, Social et Commerce — optimise les enchères pour maximiser les conversions. Vous pouvez éventuellement saisir un **[!UICONTROL Target CPA]** (coût par acquisition). **Remarque :** utilisez cette option pour les campagnes des portfolios avec optimisation au niveau des campagnes. Dans les portfolios avec optimisation au niveau de la campagne, Search, Social et Commerce optimise le Coût par acquisition (CPA) cible.

* *[!UICONTROL Maximize Conversion Value]:* Le réseau publicitaire — et non Search, Social et Commerce — optimise les enchères afin d’optimiser la valeur de conversion. Entrez éventuellement un **[!UICONTROL Target Return on Ad Spend]** (ROAS) en pourcentage. **Remarque :** utilisez cette option pour les campagnes des portfolios avec optimisation au niveau des campagnes. Dans les portfolios avec optimisation au niveau de la campagne, Search, Social et Commerce optimise le retour sur dépenses publicitaires cible.

## Onglet [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** langue de la publicité, qui doit correspondre à la langue des sites sur lesquels votre publicité peut apparaître. Le réseau publicitaire détermine la langue d&#39;un utilisateur à partir de divers signaux, y compris la requête de l&#39;utilisateur, le pays de l&#39;éditeur et le paramètre de langue de l&#39;utilisateur.

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## Onglet [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### Onglet [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (Pour [!UICONTROL EF Redirect] uniquement) Niveau auquel les clics et le chiffre d’affaires doivent être suivis en ajoutant une redirection (le cas échéant) et en ajoutant des paramètres aux URL pertinentes :

* *[!UICONTROL Keyword]:* Pour suivre les données uniquement au niveau du mot-clé.

* *[!UICONTROL Creative]:* Pour effectuer le suivi des données uniquement au niveau de l’annonce (contenu publicitaire).

* *[!UICONTROL Creative and Keyword]:* Pour effectuer le suivi des données au niveau de la publicité (contenu publicitaire) et des mots-clés.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** ajoute un paramètre d’URL aux publicités dans le compte ou la campagne pour le suivi des conversions.

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
>* [Gérer les campagnes](/help/search-social-commerce/manage/campaigns/campaign-manage.md)
