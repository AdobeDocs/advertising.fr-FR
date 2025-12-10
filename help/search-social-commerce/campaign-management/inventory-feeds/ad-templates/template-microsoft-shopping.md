---
title: '[!DNL Microsoft Ads] des paramètres de modèle d’annonce publicitaire pour les flux d’inventaire'
description: Référencez les paramètres des modèles d [!DNL Microsoft Ads] annonces d’achat pour les flux d’inventaire.
exl-id: a0dd6542-0516-406a-b8c5-2e102ec7ab3d
feature: Search Inventory Feeds
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---

# [!DNL Microsoft Ads] des paramètres de modèle d’annonce publicitaire pour les flux d’inventaire

Utilisez des modèles d’annonces publicitaires pour configurer les annonces publicitaires.

>[!NOTE]
>
>* Les caractères suivants sont réservés à la désignation des noms de colonne et de modificateur dans le modèle et sont donc interdits en tant que texte dans tous les champs d’attribut : `[ ] < > `

## \[Surtout les onglets\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Panneau de gauche\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** (facultatif pour les modèles de fichiers de flux client) Modèle de suivi au niveau de la campagne, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de l’atterrissage et incorpore l’URL finale dans un paramètre. Cette valeur remplace le paramètre au niveau du compte, mais les modèles de suivi à des niveaux plus granulaires (avec le mot-clé comme le plus granulaire) remplacent cette valeur.

* Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », effectuez l’une des opérations suivantes :

   * (Recommandé) Utilisez le format [modèle de suivi pour les campagnes d’achats Microsoft](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). Si l’ensemble du compte est dédié aux annonces d’achats, vous pouvez plutôt définir un modèle de suivi au niveau du compte.

   * Si, à la place, vous incluez une valeur pour chaque produit dans le flux à l’aide de la colonne « [!DNL bingads_redirect] » (en utilisant le [format correct](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)), saisissez le paramètre `{lpurl}`. Vous pouvez éventuellement ajouter des redirections et un suivi tiers au paramètre `{lpurl}` .

* Pour les redirections et le suivi tiers, saisissez une valeur .

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** ID client du compte marchand dont les produits sont utilisés pour la campagne.

**[!UICONTROL Sales Country]:** Pays dans lequel les produits de la campagne sont vendus. Parce que les produits sont associés
avec les pays cibles, ce paramètre détermine les produits qui font l’objet de publicités dans la campagne.

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Campaign Priority]:** priorité d’utilisation de la campagne lorsque plusieurs campagnes annoncent la campagne
même produit : *[!UICONTROL Low]* (valeur par défaut pour les nouvelles campagnes), *[!UICONTROL Medium]* ou *[!UICONTROL High]*. Lorsque le même produit est inclus dans plusieurs campagnes, le réseau publicitaire utilise
indiquez d’abord la priorité de la campagne pour déterminer quelle campagne (et l’enchère associée) est éligible aux enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, la campagne ayant la meilleure enchère est éligible.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]:**(Campagnes [!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement ; applicable aux campagnes qui ciblent des audiences dans l’Union européenne (UE)) Que la campagne contienne ou non de la publicité politique selon les exigences pour les publicités diffusées dans l’Union européenne en vertu du règlement 2024/90 de l’UE : *[!UICONTROL Yes]* ou *[!UICONTROL No]*.

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (facultatif) Modèle de suivi au niveau du groupe publicitaire, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de l’atterrissage et incorpore l’URL finale dans un paramètre. Cette valeur remplace les paramètres au niveau du compte et de la campagne, mais les modèles de suivi à des niveaux plus granulaires remplacent cette valeur.

Pour le suivi des conversions Adobe Advertising, il n’est pas nécessaire de saisir une valeur. La valeur au niveau de la campagne est suffisante.

Pour les redirections et le suivi tiers, saisissez une valeur .

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** groupe de produits complet par défaut, « [!UICONTROL All products] ». Vous ne pouvez pas supprimer ce groupe de produits parent, mais il est automatiquement supprimé lorsque tous les niveaux inférieurs sont absents du flux.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Unités sans groupes de produits enfants ; facultatif) Modèle de suivi du produit
qui spécifie tous les paramètres de redirection et de tracking des domaines hors atterrissage et incorpore l’URL finale dans un paramètre [!DNL ValueTrack]. Ce modèle remplace les modèles aux niveaux supérieurs.

Pour le suivi des conversions Adobe Advertising, il n’est pas nécessaire de saisir une valeur. La valeur au niveau de la campagne est suffisante.

Pour les redirections et le suivi tiers, saisissez une valeur .

**[!UICONTROL Initial Bid]:** enchère initiale pour chaque publicité.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [À propos de l’automatisation de la gestion des annonces à l’aide des flux d’inventaire](../inventory-feeds-about.md)
>* [Gestion des modificateurs](../modifiers-manage.md)
>* [Gestion des fichiers de flux de données d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propager les données de flux par le biais de modèles](../feed-data-propagate.md)
>* [Publier les données de campagne des flux d’inventaire dans les réseaux publicitaires](../propagated-data-post.md)
