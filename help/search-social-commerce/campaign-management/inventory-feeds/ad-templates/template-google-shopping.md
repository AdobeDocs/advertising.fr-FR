---
title: "[!DNL Google Ads] achats et paramètres de modèle pour les flux de stock"
description: Référencez les paramètres pour [!DNL Google Ads] achat de modèles d’annonces pour les flux d’inventaire.
source-git-commit: f8d17ba787496917f4011f9dcbcb5587fe5c83cb
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# [!DNL Google Ads] achats et paramètres de modèle pour les flux de stock

Utilisez les modèles d’annonces d’achat pour configurer des annonces d’achat.

>[!NOTE]
>
>* Les caractères suivants sont réservés à la désignation des noms de colonne et des noms de modificateur dans le modèle et sont donc interdits en tant que texte dans tous les champs d’attribut :  `[ ] < > `

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

**[!UICONTROL Campaign Tracking Template]:** (Facultatif pour les modèles de fichiers de flux client) Le modèle de suivi au niveau de la campagne, qui spécifie tous les paramètres de suivi et redirections hors domaine d’entrée et incorpore l’URL finale dans un paramètre. Cette valeur remplace le paramètre au niveau du compte, mais les modèles de suivi à des niveaux plus granulaires (avec le mot-clé comme plus granulaire) remplacent cette valeur.

Pour le suivi de conversion Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; utilisez la variable [format de modèle de suivi pour les campagnes commerciales Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md). Si l’intégralité du compte est dédiée aux publicités commerciales, vous pouvez définir un modèle de suivi au niveau du compte.

Pour les redirections et le suivi tiers, saisissez une valeur.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** Identifiant client du compte marchand dont les produits sont utilisés pour la campagne.

**[!UICONTROL Sales Country]:** Pays dans lequel les produits de la campagne sont vendus. Les produits étant associés aux pays cibles, ce paramètre détermine les produits faisant l’objet d’une publicité dans la campagne.

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

**[!UICONTROL Networks]:** Réseaux sur lesquels placer des publicités. *[!UICONTROL Search]* est déjà sélectionnée. Pour inclure des offres sur les listes pour [!DNL Google Ads] partenaires de recherche, cochez la case en regard de **[!UICONTROL Search partners]**.

**[!UICONTROL Campaign Priority]:** La priorité avec laquelle la campagne est utilisée lorsque plusieurs campagnes font la promotion du même produit : *[!UICONTROL Low]* (valeur par défaut pour les nouvelles campagnes), *[!UICONTROL Medium]* ou *[!UICONTROL High]*. Lorsqu’un même produit est inclus dans plusieurs campagnes, le réseau publicitaire utilise d’abord la priorité de la campagne pour déterminer la campagne (et l’offre associée) éligible à l’enchère publicitaire. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Facultatif) Un modèle de suivi au niveau du groupe d’annonces qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi et incorpore l’URL finale dans un paramètre. Cette valeur remplace les paramètres au niveau du compte et de la campagne, mais les modèles de suivi à des niveaux plus granulaires remplacent cette valeur.

Pour le suivi de conversion Adobe Advertising, il n’est pas nécessaire de saisir de valeur. La valeur au niveau de la campagne suffit.

Pour les redirections et le suivi tiers, saisissez une valeur.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** Le groupe de produits par défaut, tout compris, &quot;[!UICONTROL All products].&quot; Vous ne pouvez pas supprimer ce groupe de produits parent, mais il est automatiquement supprimé lorsque tous les niveaux inférieurs sont absents du flux.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Unités sans groupes de produits enfants ; (facultatif) Le modèle de suivi pour le groupe de produits, qui spécifie tous les paramètres de suivi et redirections hors domaine d’entrée et incorpore l’URL finale dans un paramètre ValueTrack. Ce modèle remplace les modèles à des niveaux supérieurs.

Pour le suivi de conversion Adobe Advertising, il n’est pas nécessaire de saisir de valeur. La valeur au niveau de la campagne suffit.

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
>* [A propos de l’automatisation de la gestion des publicités à l’aide des flux d’inventaire](../inventory-feeds-about.md)
>* [Gestion des modificateurs](../modifiers-manage.md)
>* [Gestion des fichiers de flux de données d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propager les données de flux par le biais de modèles](../feed-data-propagate.md)
>* [Publier les données de campagne des flux d’inventaire vers les réseaux publicitaires](../propagated-data-post.md)
