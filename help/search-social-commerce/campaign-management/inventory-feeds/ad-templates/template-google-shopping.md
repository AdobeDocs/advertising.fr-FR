---
title: Paramètres de modèle d’annonce d’achat "[!DNL Google Ads]" pour les flux d’inventaire
description: Référencez les paramètres pour  [!DNL Google Ads] acheter des modèles d’annonces pour les flux d’inventaire.
exl-id: 36cbe719-f984-4456-8575-94b9d3e6094e
feature: Search Inventory Feeds
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# [!DNL Google Ads] paramètres de modèle d’annonce d’achat pour les flux d’inventaire

Utilisez les modèles d’annonces d’achat pour configurer des annonces d’achat.

>[!NOTE]
>
>* Les caractères suivants sont réservés à la désignation des noms de colonne et des noms de modificateur dans le modèle et sont donc interdits en tant que texte dans tous les champs d&#39;attribut : `[ ] < > `

## \[Au-dessus de tous les onglets\]

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

**[!UICONTROL Campaign Tracking Template]:** (Facultatif pour les modèles de fichiers de flux client) Le modèle de suivi au niveau de la campagne, qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi et incorpore l’URL finale dans un paramètre. Cette valeur remplace le paramètre au niveau du compte, mais les modèles de suivi à des niveaux plus granulaires (avec le mot-clé comme plus granulaire) remplacent cette valeur.

Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload]&quot;, utilisez le [&#x200B; format de modèle de suivi pour les campagnes commerciales Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md). Si l’intégralité du compte est dédiée aux publicités commerciales, vous pouvez définir un modèle de suivi au niveau du compte.

Pour les redirections et le suivi tiers, saisissez une valeur.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** ID client du compte marchand dont les produits sont utilisés pour la campagne.

**[!UICONTROL Sales Country]:** pays dans lequel les produits de la campagne sont vendus. Les produits étant associés
avec les pays cibles, ce paramètre détermine les produits qui sont annoncés dans la campagne.

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

**[!UICONTROL Networks]:** réseaux sur lesquels placer des publicités. *[!UICONTROL Search]* est déjà sélectionné. Pour inclure des offres sur les listes pour les partenaires de recherche [!DNL Google Ads], cochez la case en regard de **[!UICONTROL Search partners]**.

**[!UICONTROL Campaign Priority]:** Priorité avec laquelle la campagne est utilisée lorsque plusieurs campagnes font de la publicité pour la variable
même produit : *[!UICONTROL Low]* (valeur par défaut pour les nouvelles campagnes), *[!UICONTROL Medium]* ou *[!UICONTROL High]*. Lorsque le même produit est inclus dans plusieurs campagnes, le réseau publicitaire utilise
la priorité de la campagne doit d’abord déterminer la campagne (et l’offre associée) éligible à l’enchère publicitaire. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (facultatif) modèle de suivi au niveau du groupe publicitaire, qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi et incorpore l’URL finale dans un paramètre. Cette valeur remplace les paramètres au niveau du compte et de la campagne, mais les modèles de suivi à des niveaux plus granulaires remplacent cette valeur.

Pour le suivi des conversions par Adobe Advertising, il n’est pas nécessaire de saisir de valeur. La valeur au niveau de la campagne suffit.

Pour les redirections et le suivi tiers, saisissez une valeur.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** groupe de produits par défaut, tout compris, &quot;[!UICONTROL All products]&quot;. Vous ne pouvez pas supprimer ce groupe de produits parent, mais il est automatiquement supprimé lorsque tous les niveaux inférieurs sont absents du flux.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Unités sans groupes de produits enfants ; facultatif) Le modèle de suivi du produit
, qui spécifie tous les paramètres de suivi et redirections de domaine hors d’entrée et incorpore l’URL finale dans un paramètre [!DNL ValueTrack] . Ce modèle remplace les modèles à des niveaux supérieurs.

Pour le suivi des conversions par Adobe Advertising, il n’est pas nécessaire de saisir de valeur. La valeur au niveau de la campagne suffit.

Pour les redirections et le suivi tiers, saisissez une valeur.

**[!UICONTROL Initial Bid]:** Offre initiale pour chaque publicité.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [À propos de l’automatisation de la gestion des publicités à l’aide de flux d’inventaire](../inventory-feeds-about.md)
>* [Gestion des modificateurs](../modifiers-manage.md)
>* [Gestion des fichiers de flux de données d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propager les données de flux par le biais de modèles](../feed-data-propagate.md)
>* [&#x200B; Publier les données de campagne des flux d’inventaire vers les réseaux publicitaires &#x200B;](../propagated-data-post.md)
