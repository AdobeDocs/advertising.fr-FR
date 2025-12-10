---
title: '[!DNL Microsoft Advertising] des paramètres de la campagne'
description: Référencez les paramètres des campagnes  [!DNL Microsoft Advertising] .
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '2075'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] des paramètres de la campagne

## \[Écran de création de campagne\]

**[!UICONTROL Campaign Type]:** (disponible lors de la création de la campagne uniquement) Où placer des annonces et quels types d’annonces
la campagne peut contenir :

* *[!UICONTROL Search]:* affiche les annonces publicitaires textuelles sur le réseau de recherche.

* *[!UICONTROL Shopping Network]:* affiche les annonces de produits (pour vos produits dans votre catalogue de produits [!DNL Microsoft Merchant Center]) sur le réseau d’achat.

* *[!UICONTROL Audience]:* affiche les publicités natives/display sur le [!DNL Microsoft Audience Network]. Vous pouvez a) générer automatiquement des annonces basées sur des flux en liant la campagne à une boutique de centre commercial dans la section [!UICONTROL Shopping Settings] ou b) créer des annonces réactives avec des ressources textuelles et des images chargées. Les deux options nécessitent de créer des groupes publicitaires avec un ciblage utilisateur.

* *[!UICONTROL Shopping Campaigns for Brands]:* fait la promotion de vos produits auprès de détaillants liés dans les réseaux de recherche et d&#39;audience. Vous pouvez créer des groupes d’annonces enfants et des groupes de produits (applications à promouvoir), ainsi que des annonces de produits facultatives pour la campagne. [!DNL Microsoft Advertising] crée automatiquement des annonces pour les groupes de produits. Pour les campagnes d’achat de marques, utilisez la [!UICONTROL Manual CPC] de stratégie d’enchères. Pour les promotions d’achats de marques, utilisez la [!UICONTROL Cost per Sale] de stratégie d’enchères.

* *[!UICONTROL Microsoft Store Ads Campaign]:* fait la promotion de vos applications et jeux disponibles dans le [!DNL Microsoft Store]. Vous pouvez créer des groupes d’annonces enfants, des groupes de produits et des annonces de produits facultatives pour la campagne ; [!DNL Microsoft Advertising] crée automatiquement des annonces pour les groupes de produits.

* *[!UICONTROL Audience CTV Video]:* Affiche les publicités vidéo de la télévision connectée (CTV) sur le réseau de l&#39;audience.

* *[!UICONTROL Audience Video]:* affiche les publicités vidéo standard sur le réseau de l’audience.

* *[!UICONTROL Performance Max]:* affiche plusieurs types d’annonces sur tous les réseaux à l’aide d’enchères intelligentes [!DNL Microsoft Advertising]. Dans les paramètres de la campagne, vous devez spécifier un ou plusieurs groupes de ressources, qui comprennent des images, des logos, des titres, des descriptions, un call to action facultatif et des signaux d’audience. Le réseau publicitaire combine automatiquement les ressources pour diffuser des annonces en fonction du canal.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Nom de campagne unique au sein du compte. La longueur maximale est de 128 caractères.

**[!UICONTROL Status]:** statut d’affichage de la campagne : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Active*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:**(Applicable aux campagnes qui ciblent des audiences dans l’Union européenne (UE)) Que la campagne contienne ou non de la publicité politique selon les exigences pour les publicités diffusées dans l’Union européenne en vertu du règlement 2024/90 de l’UE : *[!UICONTROL Yes]* ou *[!UICONTROL No]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Stratégie d’enchères pour la campagne :

* *[!UICONTROL Cost per Sale]:* (Campagnes d’achat uniquement) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères en fonction du [!UICONTROL Target CPS] (coût par vente). Vous ne payez que lorsqu’un clic sur votre publicité produit entraîne une vente dans les 24 heures. **Remarque :** n’incluez pas de campagnes avec cette stratégie d’enchères dans les portefeuilles. L’optimisation des moteurs de recherche, des réseaux sociaux et de Commerce n’est pas disponible pour les campagnes avec cette stratégie d’enchères.

  Une fois que vous avez enregistré une campagne d’achat pour les marques avec cette stratégie d’enchères, vous ne pouvez plus modifier la stratégie d’enchères. Pour les autres types de campagnes d’achats, cette stratégie n’est disponible que pour les nouvelles campagnes.

* *[!UICONTROL CPV]* (Campagnes vidéo Audience CTV uniquement) Utilise le modèle de coût par vue (CPV). Search, Social et Commerce ne fournissent pas d’optimisation pour les campagnes avec cette stratégie d’enchères incluses dans les portfolios.

* *[!UICONTROL Enhanced CPC]:* (campagnes sur les réseaux d’audience, de recherche et d’achat) Utilise le modèle de coût par clic (eCPC) amélioré du réseau publicitaire, qui permet au réseau publicitaire de modifier automatiquement le coût par clic (CPC) de l’enchère pour chaque mise aux enchères afin de maximiser les conversions, à l’aide des conversions spécifiées dans le réseau publicitaire (et non dans Search, Social et Commerce), tout en essayant de maintenir votre CPC moyen en dessous de votre CPC maximum.

  Lorsque vous ajoutez une campagne avec eCPC à un portfolio Search, Social et Commerce optimisé, Search, Social et Commerce optimise les enchères de base et, lorsque l’option « [!UICONTROL Auto adjust campaign budget limits] » est activée, le budget de la campagne. Le réseau publicitaire optimise tous les ajustements d’offres et peut modifier les offres générées par Search, Social et Commerce au moment de la requête de l’utilisateur en fonction de données et d’informations propriétaires. **Attention :** utilisez les campagnes eCPC dans les portfolios uniquement lorsque le nombre total de conversions suivies sur le réseau publicitaire correspond à l’objectif du portefeuille.

* *[!UICONTROL Manual CPC]* : (campagnes d’achat pour les marques ; campagnes [!DNL Microsoft Store Ads] ; obsolète pour les autres types de campagne) utilise le modèle de coût par clic (CPC). Pour certains types d’annonces, vous pouvez éventuellement autoriser le réseau publicitaire à modifier les enchères pour la campagne :

   * **[!UICONTROL Enable Enhanced CPC]** (désactivé par défaut) : cette option est identique à l’utilisation de l’option « [!UICONTROL Enhanced CPC] ».

* *[!UICONTROL Manual CPA]:* (campagnes [!DNL Microsoft Store Ads]) utilise le modèle de coût par acquisition (CPA).

* *[!UICONTROL Manual CPM]* (Campagnes d’audience et campagnes vidéo d’audience uniquement) Utilise le modèle de coût par millier d’impressions (CPM), pour lequel vous spécifiez ce que vous souhaitez dépenser par 1 000 impressions consultées. Les campagnes avec cette stratégie d’enchères ne sont pas optimisées lorsqu’elles sont incluses dans les portefeuilles.

* *[!UICONTROL Maximize Clicks]:* (campagnes de recherche et d’achat) Le réseau publicitaire , et non Search, Social et Commerce, optimise les enchères pour maximiser les clics. Vous pouvez éventuellement saisir un **[!UICONTROL Max CPC]** (coût par clic) pour vous assurer que le réseau publicitaire ne paie pas plus d’un montant spécifique pour chaque clic. **Attention :** lorsque vous ajoutez une campagne avec cette stratégie à un portefeuille, le poids du clic (et non l’objectif du portefeuille) génère les enchères.

* *[!UICONTROL Maximize Conversion Value]:* (réseaux de recherche et d’achat/d’achats intelligents, campagnes de performances maximales) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères afin d’optimiser la valeur de la conversion. Entrez éventuellement un **[!UICONTROL Target Return on Ad Spend]** (ROAS) en pourcentage. **Remarque :** utilisez cette option pour les campagnes des portfolios hybrides, mais pas pour les portfolios standard. Dans les portfolios hybrides, Search, Social et Commerce optimise le retour sur dépenses publicitaires cible.

* *[!UICONTROL Maximize Conversions]:* (Performances maximales des campagnes et des campagnes sur le réseau de recherche ou le réseau d’audience (mais pas les vidéos d’audience ni la télévision connectée) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères afin d’optimiser les conversions. Vous pouvez éventuellement saisir un **[!UICONTROL Target CPC]** (coût par clic). Pour les campagnes d’audience, vous pouvez également saisir un **[!UICONTROL Target CPA]** facultatif (coût par acquisition). **Remarque :** utilisez cette option pour les campagnes des portfolios hybrides, mais pas pour les portfolios standard. Dans les portfolios hybrides, Search, Social et Commerce optimise le CPA de Target.

* *[!UICONTROL Target CPA]:* (Campagnes sur le réseau de recherche) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères en fonction d’une **[!UICONTROL Target CPA]** facultative (coût par acquisition), qui correspond au montant moyen sur 30 jours que vous souhaitez payer pour une acquisition (conversion). **Remarque :** utilisez cette option pour les campagnes dans des portfolios hybrides (mais pas dans des portfolios standard) avec n’importe quelle stratégie de dépenses, à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA]. Dans les portfolios hybrides, Search, Social et Commerce optimise le CPA de Target.

  Les données d&#39;enchères Position moyenne et CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;enchères.

* *[!UICONTROL Target Impression Share]:* (Campagnes sur le réseau de recherche) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères pour obtenir un taux d’impressions et une position publicitaire cibles. Vous pouvez éventuellement saisir un **[!UICONTROL Target Impression Share]** sous la forme d’un pourcentage, du **[!UICONTROL Target Ad Position]** et d’un **[!UICONTROL Max CPC]** (coût par clic). **Remarque :** cette option n’est pas prise en charge dans les portfolios hybrides.

* *[!UICONTROL Target Return on Ad Spend]:* (Campagnes sur les réseaux de recherche et d’achat) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères en fonction de vos **[!UICONTROL Target ROAS]** (retour sur dépenses publicitaires), spécifié en tant que pourcentage. Vous pouvez éventuellement saisir un **[!UICONTROL Max CPC]** (coût par clic) pour vous assurer que le réseau publicitaire ne paie pas plus d’un montant spécifique pour chaque clic. **Remarque :** utilisez cette option pour les campagnes dans des portfolios hybrides (mais pas dans des portfolios standard) avec n’importe quelle stratégie de dépenses, à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS]. Dans les portfolios hybrides, Search, Social et Commerce optimise le retour sur dépenses publicitaires cible.

  Les données d&#39;enchères Position moyenne et CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;enchères.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Campagnes d’achat uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel
les produits de la campagne sont vendus. Comme les produits sont associés aux pays cibles, ce paramètre détermine les produits qui sont annoncés dans la campagne.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (Campagnes d’audience uniquement ; facultatif) associe la campagne à un magasin de centre commercial spécifique pour les annonces automatisées basées sur les flux plutôt que sur les annonces réactives. Lorsque vous sélectionnez cette option, spécifiez les [!UICONTROL Merchant ID] et [!UICONTROL Products]. Vous devez créer des groupes publicitaires pour la campagne, mais vous n’avez pas besoin de créer des annonces.

Une fois que vous avez lié la campagne à un magasin et enregistré les paramètres, vous ne pouvez plus modifier cette option.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (Campagnes d’audience liées à une boutique de centre commercial uniquement) Produits à promouvoir. Par défaut, *[!UICONTROL All products]* est sélectionné. Pour ne proposer que des produits dotés d’attributs spécifiques, sélectionnez *[!UICONTROL Filter products]* et spécifiez jusqu’à sept combinaisons dimension-attribut de produit sur lesquelles filtrer vos produits. Toutes les valeurs spécifiées doivent s’appliquer pour que des publicités s’affichent pour le produit. Par exemple, pour afficher des publicités pour des fournitures pour animaux de compagnie Acme, vous pouvez créer les filtres `Custom Label 1=animals`, `Category=pet supplies` et `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Campagnes Performances max uniquement) Langue de l’annonce publicitaire, qui doit correspondre à la langue des sites sur lesquels votre annonce publicitaire peut apparaître. [!DNL Microsoft Advertising] détermine la langue d’un utilisateur à partir de différents signaux, notamment sa requête, le pays de l’éditeur et le paramètre de langue de l’utilisateur.

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

**[!UICONTROL Negative Websites]:** (Campagnes sur le réseau d’affichage/natif uniquement ; facultatif) Sites sur le réseau d’affichage sur lesquels vous ne souhaitez pas que vos annonces s’affichent. Saisissez une URL valide, telle que www.example.com. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes.

Pour plus d’informations sur la disponibilité, consultez l’aide de Microsoft Advertising pour « [Empêcher l’affichage d’annonces sur des sites web spécifiques](https://help.ads.microsoft.com/#apex/bae/en/14061/0) ».

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

**[!UICONTROL Track Product Group]:** (pour les [!UICONTROL EF Redirect] uniquement) Non implémenté

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (par groupe de ressources)

**[!UICONTROL Asset Group Name]:** nom du dossier de ressources (groupe de ressources).

**[!UICONTROL Asset Group Status]:** statut du groupe de ressources : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** URL finale de toutes les publicités créées à partir du groupe de ressources.

**[!UICONTROL Images]:** Jusqu’à 20 images pour la publicité, dont au moins une image carrée et une image de paysage. Voir les [[!DNL Microsoft Advertising] instructions relatives aux images](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Vous pouvez charger des images ou les sélectionner dans votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour charger des images :

   1. Sur l’onglet [!UICONTROL Upload from Device] , cliquez sur **[!UICONTROL +]** et sélectionnez les images sur votre appareil ou réseau.

   1. Pour chaque image :

      1. Sélectionnez les proportions.

      1. Faites glisser et positionnez la zone de recadrage selon vos besoins pour sélectionner la partie visible de l’image, puis redimensionnez la partie visible de l’image selon vos besoins, si possible.

      1. (Facultatif) Sélectionnez d’autres proportions et, éventuellement, repositionnez et redimensionnez l’image selon les besoins pour chaque proportion sélectionnée.

         Une ressource est créée pour chaque format sélectionné.

      1. Cliquez sur **[!UICONTROL Proceed]**.

   1. Lorsque vous avez terminé de spécifier des images, cliquez sur **[!UICONTROL Upload]**.

* Pour sélectionner des images dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les images.

**[!UICONTROL Logos]:** Au moins un logo. Vous pouvez inclure jusqu’à cinq éléments. Voir les [[!DNL Microsoft Advertising] instructions relatives aux ressources](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Vous pouvez charger des images ou les sélectionner dans votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour charger des images :

   1. Sur l’onglet [!UICONTROL Upload from Device] , cliquez sur **[!UICONTROL +]** et sélectionnez les images sur votre appareil ou réseau.

   1. Pour chaque image :

      1. Sélectionnez les proportions.

      1. Faites glisser et positionnez la zone de recadrage selon vos besoins pour sélectionner la partie visible de l’image, puis redimensionnez la partie visible de l’image selon vos besoins, si possible.

      1. (Facultatif) Sélectionnez d’autres proportions et, éventuellement, repositionnez et redimensionnez l’image selon les besoins pour chaque proportion sélectionnée.

         Une ressource est créée pour chaque format sélectionné.

      1. Cliquez sur **[!UICONTROL Proceed]**.

   1. Lorsque vous avez terminé de spécifier des images, cliquez sur **[!UICONTROL Upload]**.

* Pour sélectionner des images dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les images.

**[!UICONTROL Headlines]:** au moins trois titres courts, pouvant aller jusqu&#39;à 15, de 30 caractères chacun. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text] , saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez-les.

**[!UICONTROL Long Headlines]:** au moins un titre long, avec un maximum de 90 caractères chacun, et jusqu’à cinq titres longs. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text] , saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez-les.

**[!UICONTROL Descriptions]:** au moins deux descriptions, et jusqu’à cinq, contenant chacune un maximum de 90 caractères. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text] , saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez-les.

**[!UICONTROL Call to Action]:** call to action à inclure dans la publicité. Par défaut, *[!UICONTROL Act Now]* est sélectionné.

**[!UICONTROL Business Name]:** nom de l’entreprise, avec un maximum de 25 caractères. Il ne peut pas contenir de scripts, d’HTML ou d’autres langages de balisage.

**[!UICONTROL Audience Signal]:** (facultatif) [!DNL Microsoft Advertising] les audiences à utiliser comme signaux d’audience pour la campagne. Les modèles de machine learning [!DNL Microsoft Advertising] utilisent les audiences pour trouver des internautes similaires à cibler et peuvent également afficher des annonces à des audiences qui ne sont pas spécifiées comme signaux pour vous aider à atteindre vos objectifs de performances. Sélectionnez les audiences les plus susceptibles d’être converties.

>[!NOTE]
>Les signaux d’audience sont différents des [cibles d’audience au niveau du groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** permet de spécifier un autre groupe de ressources.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** s’il faut *[!UICONTROL Use account conversion goals for this campaign]* (valeur par défaut) ou *[!UICONTROL Use campaign specific conversion goals]*. Si vous choisissez de spécifier des objectifs de conversion pour la campagne, sélectionnez les objectifs dans la liste de tous les objectifs disponibles. **Remarque :** les objectifs sont synchronisés quotidiennement, de sorte que les objectifs créés au cours des 24 heures précédentes peuvent ne pas être répertoriés. Pour mettre à jour la liste, [synchronisez manuellement les données du réseau publicitaire](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

>[!TIP]
>
>Si la campagne fait partie d’un portfolio hybride, la bonne pratique consiste à utiliser des objectifs au niveau de la campagne qui correspondent aux objectifs de conversion de l’objectif du portfolio. L’inclusion d’objectifs de conversion supplémentaires peut avoir une incidence sur les performances du portfolio.
>
> Toutefois, pour les campagnes dans des portfolios hybrides pour lesquelles vous [chargez les objectifs vers le réseau publicitaire](/help/search-social-commerce/tools/objective-upload-to-networks.md), procédez comme suit dans l’éditeur du réseau publicitaire au lieu de procéder ici : a) ajoutez la mesure d’objectif de portfolio Search, Social et Commerce chargée (qui commence par « O_ACS_OBJ ») comme objectif de conversion pour la campagne, et b) ajoutez tous les objectifs de campagne qui incluent les conversions suivies par la balise de suivi d’événement universel (UET) [!DNL Microsoft Advertising], car les mesures suivies par le réseau publicitaire ne sont pas chargées sur le réseau publicitaire avec l’objectif .

>[!MORELIKETHIS]
>
>* [Gérer les campagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
