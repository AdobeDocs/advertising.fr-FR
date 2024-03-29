---
title: '''[!DNL Microsoft® Advertising] paramètres de campagne'
description: Référencez les paramètres pour [!DNL Microsoft® Advertising] campagnes.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 6b5c37b02191cf7097eb547f9ad58f347824579c
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] paramètres de campagne

## \[Ecran de création de campagne\]

**[!UICONTROL Campaign Type]:** (Disponible uniquement lors de la création de la campagne) Où placer des publicités et quels types de publicités peuvent contenir la campagne :

* *[!UICONTROL Search]:* Affiche des publicités textuelles sur le réseau de recherche.

* *[!UICONTROL Shopping Network]:* Affiche des publicités de produits pour vos produits dans votre [!DNL Microsoft® Merchant Center] catalogue de produits — sur le réseau d’achat.

* *[!UICONTROL Audience]:* Affiche des publicités natives/affichées sur le [!DNL Microsoft® Audience Network]. Vous pouvez : a) générer automatiquement des publicités basées sur le flux en liant la campagne à un magasin de centre commercial dans la variable [!UICONTROL Shopping Settings] ou b) créer des publicités réactives avec des ressources textuelles et des images téléchargées. Les deux options exigent que vous créiez des groupes d’annonces avec le ciblage des utilisateurs.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Fonction bêta) Promotion de vos produits par le biais de revendeurs liés sur les réseaux de recherche et d’audience. Vous pouvez créer des groupes d’annonces enfants et des groupes de produits (applications à promouvoir), ainsi que des publicités de produits facultatives pour la campagne ; [!DNL Microsoft® Advertising] crée automatiquement des publicités pour les groupes de produits.

* *[!UICONTROL Microsoft® Store Ads Campaign]:* (Fonction bêta) Promotion de vos applications et jeux disponibles dans la variable [!DNL Microsoft® Store]. Vous pouvez créer des groupes d’annonces enfants, des groupes de produits et des publicités de produits facultatives pour la campagne ; [!DNL Microsoft® Advertising] crée automatiquement des publicités pour les groupes de produits.

* *[!UICONTROL Audience CTV Video]:* (Fonction bêta) Affiche les publicités vidéo de la télévision connectée (CTV) sur le réseau d’audience.

* *[!UICONTROL Audience Video]:* (Fonction bêta) Affiche des publicités vidéo standard sur le réseau d’audience.

* *[!UICONTROL Performance Max]:* (Fonction bêta) Affiche plusieurs types d’annonces sur tous les réseaux. Attribuer des groupes de ressources séparément dans le [!DNL Microsoft® Advertising] éditeur de publicités.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Nom de campagne unique dans le compte. La longueur maximale est de 128 caractères.

**[!UICONTROL Status]:** Etat d&#39;affichage de l&#39;opération : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Actif*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Stratégie d’offre pour la campagne :

* *[!UICONTROL CPV]* (Campagnes vidéo Audience CTV uniquement) Utilise le modèle de coût par vue (CPV). <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Campagnes sur l’audience, la recherche et les réseaux d’achats) Utilise le modèle de coût par clic amélioré du réseau publicitaire, qui permet au réseau publicitaire de modifier automatiquement l’offre coût par clic (CPC) pour chaque enchère afin d’optimiser les conversions à l’aide des conversions spécifiées dans le réseau publicitaire (et non dans Search, Social et Commerce), tout en essayant de maintenir le CPC moyen en dessous du CPC maximum.

  Lorsque vous ajoutez une campagne avec eCPC à un portefeuille de recherche, de réseaux sociaux et de commerce optimisé, Search, Social et Commerce optimise les offres de base et , lorsque le paramètre[!UICONTROL Auto adjust campaign budget limits]&quot; est activée : le budget de l’opération. Le réseau publicitaire optimise tous les ajustements d’offres et peut modifier les offres générées par Search, Social et Commerce au moment de la requête de l’utilisateur en fonction de données et d’informations propriétaires. **Attention :** Utilisez les campagnes eCPC dans les portfolios uniquement lorsque le total des conversions suivies sur le réseau publicitaire correspond à l’objectif du portfolio.

* *[!UICONTROL Manual CPC]*: (campagnes commerciales pour les marques ; [!DNL Microsoft Store Ads] campagnes ; obsolète de [!DNL Microsoft® Advertising] en 2021 pour les autres types de campagne) Utilise le modèle coût par clic (CPC). Pour certains types d’annonces, vous pouvez éventuellement autoriser le réseau publicitaire à modifier les offres pour la campagne :

   * **[!UICONTROL Enable Enhanced CPC]** (désactivé par défaut) : il s’agit de la même chose que l’utilisation du paramètre[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campagnes) Utilise le modèle de coût par acquisition (CPA).

* *[!UICONTROL Manual CPM]* (Campagnes d’audience et campagnes vidéo d’audience uniquement) Utilise le modèle coût par millier d’impressions (CPM), pour lequel vous spécifiez les dépenses à dépenser pour 1 000 impressions vues. Les campagnes avec cette stratégie d’offre ne sont pas optimisées lorsqu’elles sont incluses dans les portefeuilles.

* *[!UICONTROL Maximize Clicks]:* (Campagnes de recherche et d’achat) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour maximiser les clics. Si vous le souhaitez, vous pouvez saisir une **[!UICONTROL Max CPC]** (coût par clic) pour s’assurer que le réseau publicitaire ne paie pas plus qu’un montant spécifique pour chaque clic. **Attention :** Lorsque vous ajoutez une campagne avec cette stratégie à un portefeuille, les offres sont basées sur le poids des clics et non sur l’objectif du portefeuille.

* *[!UICONTROL Maximize Conversion Value]:* (Recherche et achats/réseaux d’achats intelligents, campagnes de performances max.) Le réseau publicitaire, et non Search, Social et Commerce, optimise les offres pour maximiser la valeur de conversion. Si vous le souhaitez, vous pouvez saisir un **[!UICONTROL Target Return on Ad Spend]** (RSDP) en pourcentage. **Remarque :** Utilisez cette option pour les campagnes dans des portfolios hybrides, mais pas dans des portfolios standard.

* *[!UICONTROL Maximize Conversions]:* (Campagnes et campagnes de performances maximales sur le réseau de recherche ou d’audience (mais pas les vidéos d’audience ni la télévision connectée) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour maximiser les conversions. Si vous le souhaitez, vous pouvez saisir un **[!UICONTROL Target CPC]** (coût par clic). Pour les campagnes d’audience, vous pouvez également saisir une **[!UICONTROL Target CPA]** (coût par acquisition). **Remarque :** Utilisez cette option pour les campagnes dans des portfolios hybrides, mais pas dans des portfolios standard.

* *[!UICONTROL Target CPA]:* (Campagnes sur le réseau de recherche) Le réseau publicitaire (et non Search, Social et Commerce) optimise les offres sur la base d’une option. **[!UICONTROL Target CPA]** (coût par acquisition), qui est le montant moyen de 30 jours que vous souhaitez payer pour une acquisition (conversion). **Remarque :** Utilisez cette option pour les campagnes dans des portfolios hybrides (mais pas dans des portfolios standard) avec une stratégie de dépenses, à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA].

  La position moyenne et les données sur l&#39;offre du CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;offre.

* *[!UICONTROL Target Impression Share]:* (Campagnes sur le réseau de recherche) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour atteindre un partage d’impression cible et une position publicitaire. Si vous le souhaitez, vous pouvez saisir une **[!UICONTROL Target Impression Share]** en pourcentage, la variable **[!UICONTROL Target Ad Position]**, et a **[!UICONTROL Max CPC]** (coût par clic). **Remarque :** Cette option n’est pas prise en charge dans les portefeuilles hybrides.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campagnes sur les réseaux de recherche et d’achat) Le réseau publicitaire, et non Search, Social et Commerce, optimise les offres en fonction de vos **[!UICONTROL Target ROAS]** (retour sur dépenses publicitaires), spécifié en pourcentage. Si vous le souhaitez, vous pouvez saisir une **[!UICONTROL Max CPC]** (coût par clic) pour s’assurer que le réseau publicitaire ne paie pas plus qu’un montant spécifique pour chaque clic. **Remarque :** Utilisez cette option pour les campagnes dans des portfolios hybrides (mais pas dans des portfolios standard) avec une stratégie de dépenses, à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS].

  La position moyenne et les données sur l&#39;offre du CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;offre.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Campagnes d’achat uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel les produits de la campagne sont vendus. Les produits étant associés aux pays cibles, ce paramètre détermine les produits faisant l’objet d’une publicité dans la campagne.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]:** (Campagnes d’audience uniquement ; facultatif) associe la campagne à un magasin de centre commercial spécifique pour les publicités automatisées basées sur les flux plutôt que les publicités réactives. Lorsque vous sélectionnez cette option, indiquez la variable [!UICONTROL Merchant ID] et [!UICONTROL Products]. Vous devez créer des groupes publicitaires pour la campagne, mais vous n’avez pas besoin de créer des publicités.

Une fois que vous avez lié la campagne à un magasin et enregistré les paramètres, vous ne pouvez pas modifier cette option.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]:** (Campagnes d’audience liées uniquement à un magasin du centre commercial) Les produits à faire de la publicité. Par défaut, *[!UICONTROL All products]* est sélectionnée. Pour promouvoir uniquement les produits avec des attributs spécifiques, sélectionnez *[!UICONTROL Filter products]* et indiquez jusqu’à sept combinaisons de dimension et d’attribut de produit sur lesquelles filtrer vos produits. Toutes les valeurs spécifiées doivent s’appliquer pour que les publicités s’affichent pour le produit. Par exemple, pour afficher des publicités pour des produits pour animaux de compagnie Acme, vous pouvez créer des filtres. `Custom Label 1=animals`, `Category=pet supplies`, et `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campagnes sur le réseau d’affichage/natif uniquement ; facultatif) Sites sur le réseau d’affichage sur lequel vous ne souhaitez pas que vos publicités s’affichent. Saisissez une URL valide, telle que www.example.com. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes.

Pour plus d’informations sur la disponibilité, voir l’aide de Microsoft® Advertising à &quot;[Empêcher l’affichage des publicités sur des sites web spécifiques](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (Pour [!UICONTROL EF Redirect] uniquement) Non implémenté

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Si *[!UICONTROL Use account conversion goals for this campaign]* (valeur par défaut) ou *[!UICONTROL Use campaign specific conversion goals]*. Si vous choisissez de spécifier des objectifs de conversion pour la campagne, sélectionnez les objectifs dans la liste de tous les objectifs disponibles. **Remarque :** Les objectifs sont synchronisés quotidiennement. Il se peut donc que les objectifs créés au cours des 24 heures précédentes ne soient pas répertoriés. Pour mettre à jour la liste, [synchroniser manuellement les données du réseau publicitaire ;](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Si la campagne fait partie d’un portfolio, utilisez les mêmes objectifs de conversion que l’objectif du portfolio. L’utilisation d’objectifs de conversion différents peut avoir une incidence sur les performances du portefeuille.

>[!MORELIKETHIS]
>
>* [Gestion des campagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
