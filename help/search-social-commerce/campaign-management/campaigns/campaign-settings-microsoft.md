---
title: Paramètres de campagne '[!DNL Microsoft Advertising]'
description: Référencez les paramètres des campagnes  [!DNL Microsoft Advertising] .
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: b8aa2461d261af50e1bf66c4ae29e4e453dfd182
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] paramètres de campagne

## \[Ecran de création de campagne\]

**[!UICONTROL Campaign Type]:** (Disponible uniquement lors de la création de la campagne) Où placer des publicités et quels types de publicités
la campagne peut contenir :

* *[!UICONTROL Search]:* affiche des publicités texte sur le réseau de recherche.

* *[!UICONTROL Shopping Network]:* Affiche des publicités de produits — pour vos produits dans votre catalogue de produits [!DNL Microsoft Merchant Center] — sur le réseau d’achat.

* *[!UICONTROL Audience]:* affiche des publicités natives/display sur [!DNL Microsoft Audience Network]. Vous pouvez : a) générer automatiquement des publicités basées sur des flux en liant la campagne à un magasin de centre commercial dans la section [!UICONTROL Shopping Settings] ou b) créer des publicités réactives avec des ressources de texte et des images téléchargées. Les deux options exigent que vous créiez des groupes d’annonces avec le ciblage des utilisateurs.

* *[!UICONTROL Shopping Campaigns for Brands]:* Promotion de vos produits par le biais de revendeurs liés sur les réseaux de recherche et d’audience. Vous pouvez créer des groupes de publicités enfants et de produits (applications à promouvoir), ainsi que des publicités de produits facultatives pour la campagne ; [!DNL Microsoft Advertising] crée automatiquement des publicités pour les groupes de produits. Pour les campagnes d’achat de marques, utilisez la stratégie d’offre [!UICONTROL Manual CPC] ; pour les promotions d’achat de marques, utilisez la stratégie d’offre [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft Store Ads Campaign]:* promeut vos applications et jeux disponibles dans le [!DNL Microsoft Store]. Vous pouvez créer des groupes d’annonces enfants, des groupes de produits et des publicités de produits facultatives pour la campagne ; [!DNL Microsoft Advertising] crée automatiquement des publicités pour les groupes de produits.

* *[!UICONTROL Audience CTV Video]:* affiche des publicités vidéo de la télévision connectée (CTV) sur le réseau d’audience.

* *[!UICONTROL Audience Video]:* affiche des publicités vidéo standard sur le réseau d’audience.

* *[!UICONTROL Performance Max]:* affiche plusieurs types d’annonces sur tous les réseaux à l’aide de l’offre dynamique [!DNL Microsoft Advertising]. Dans les paramètres de l&#39;opération, vous devez indiquer un ou plusieurs groupes de ressources, notamment des images, des logos, des titres, des descriptions, un appel à l&#39;action facultatif et des signaux d&#39;audience. Le réseau publicitaire combine automatiquement les ressources pour diffuser des publicités en fonction du canal.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** nom de campagne unique dans le compte. La longueur maximale est de 128 caractères.

**[!UICONTROL Status]:** État d’affichage de la campagne : *Active* ou *En pause*. La valeur par défaut des nouvelles campagnes publicitaires est *Active*.

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

* *[!UICONTROL Cost per Sale]:* (campagnes d’achat uniquement) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres en fonction de [!UICONTROL Target CPS] (coût par vente). Vous ne payez que lorsqu’un clic sur votre produit et qu’une vente a lieu dans les 24 heures. **Remarque :** N’incluez pas de campagnes avec cette stratégie d’offre dans les portefeuilles. L’optimisation de la recherche, de Social et de Commerce n’est pas disponible pour les campagnes avec cette stratégie d’offre.

  Une fois que vous avez enregistré une campagne d’achat pour les marques avec cette stratégie d’offre, vous ne pouvez pas modifier la stratégie d’offre. Pour les autres types de campagne d’achat, cette stratégie est disponible uniquement pour les nouvelles campagnes.

* *[!UICONTROL CPV]* (Campagnes vidéo Audience CTV uniquement) Utilise le modèle de coût par vue (CPV). Search, Social et Commerce ne fournit pas d’optimisation pour les campagnes avec cette stratégie d’offre incluse dans les portefeuilles.

* *[!UICONTROL Enhanced CPC]:* (Campagnes sur les réseaux d’audience, de recherche et d’achat) utilise le modèle de coût par clic amélioré du réseau publicitaire, qui permet au réseau publicitaire de modifier automatiquement l’offre par clic (CPC) pour chaque enchère afin d’optimiser les conversions à l’aide des conversions spécifiées dans le réseau publicitaire (et non dans Search, Social et Commerce), tout en essayant de maintenir le CPC moyen en dessous du CPC.

  Lorsque vous ajoutez une campagne avec eCPC à un portefeuille de recherche, de réseaux sociaux et de Commerce optimisé, Search, Social et Commerce optimise les offres de base et, lorsque l’option &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; est activée, le budget de la campagne. Le réseau publicitaire optimise tous les ajustements d’offres et peut modifier les offres générées par Search, Social et Commerce au moment de la requête de l’utilisateur en fonction de données et d’informations propriétaires. **Attention :** Utilisez les campagnes eCPC dans les portefeuilles uniquement lorsque le total des conversions suivies sur le réseau publicitaire correspond à l’objectif du portfolio.

* *[!UICONTROL Manual CPC]* : (campagnes d’achat pour les marques ; [!DNL Microsoft Store Ads] campagnes ; obsolète pour les autres types de campagne) utilise le modèle coût par clic (CPC). Pour certains types d’annonces, vous pouvez éventuellement autoriser le réseau publicitaire à modifier les offres pour la campagne :

   * **[!UICONTROL Enable Enhanced CPC]** (désactivé par défaut) : cette option est identique à l’utilisation de l’option &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campagnes) Utilise le modèle de coût par acquisition (CPA).

* *[!UICONTROL Manual CPM]* (Campagnes d’audience et campagnes vidéo d’audience uniquement) Utilise le modèle de coût par millier d’impressions (CPM), pour lequel vous spécifiez les dépenses à dépenser pour 1 000 impressions vues. Les campagnes avec cette stratégie d’offre ne sont pas optimisées lorsqu’elles sont incluses dans les portefeuilles.

* *[!UICONTROL Maximize Clicks]:* (Campagnes de recherche et d’achat) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour maximiser les clics. Vous pouvez éventuellement saisir un **[!UICONTROL Max CPC]** (coût par clic) pour vous assurer que le réseau publicitaire ne paie pas plus qu’un montant spécifique pour chaque clic. **Attention :** Lorsque vous ajoutez une campagne avec cette stratégie à un portfolio, le poids des clics (et non l’objectif du portfolio) génère des offres.

* *[!UICONTROL Maximize Conversion Value]:* (Recherche et achats/réseaux d’achats intelligents, campagnes de performances max.) Le réseau publicitaire — pas Search, Social et Commerce — optimise les offres pour maximiser la valeur de conversion. Vous pouvez éventuellement saisir un **[!UICONTROL Target Return on Ad Spend]** (RSDP) en pourcentage. **Remarque :** Utilisez cette option pour les campagnes dans des portefeuilles hybrides, mais pas dans des portefeuilles standard. Dans les portfolios hybrides, Search, Social et Commerce optimise le retour sur investissement de Target.

* *[!UICONTROL Maximize Conversions]:* (Performances max. des campagnes et campagnes sur le réseau de recherche ou d’audience (mais pas sur les vidéos d’audience ni sur la télévision connectée) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour maximiser les conversions. Vous pouvez éventuellement saisir un **[!UICONTROL Target CPC]** (coût par clic). Pour les campagnes d’audience, vous pouvez également saisir un **[!UICONTROL Target CPA]** facultatif (coût par acquisition). **Remarque :** Utilisez cette option pour les campagnes dans des portefeuilles hybrides, mais pas dans des portefeuilles standard. Dans les portfolios hybrides, Search, Social et Commerce optimise le CPA Target.

* *[!UICONTROL Target CPA]:* (Campagnes sur le réseau de recherche) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres en fonction d’un **[!UICONTROL Target CPA]** facultatif (coût par acquisition), qui est le montant moyen de 30 jours que vous souhaitez payer pour une acquisition (conversion). **Remarque :** Utilisez cette option pour les campagnes dans des portefeuilles hybrides (mais pas dans des portefeuilles standard) avec une stratégie de dépenses quelconque à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA]. Dans les portfolios hybrides, Search, Social et Commerce optimise le CPA Target.

  La position moyenne et les données sur l&#39;offre du CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;offre.

* *[!UICONTROL Target Impression Share]:* (Campagnes sur le réseau de recherche) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour obtenir un partage d’impression cible et une position publicitaire. Vous pouvez éventuellement saisir un **[!UICONTROL Target Impression Share]** en pourcentage, le **[!UICONTROL Target Ad Position]** et un **[!UICONTROL Max CPC]** (coût par clic). **Remarque :** Cette option n’est pas prise en charge dans les portefeuilles hybrides.

* *[!UICONTROL Target Return on Ad Spend]:* (Campagnes sur les réseaux de recherche et d’achat) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres en fonction de votre **[!UICONTROL Target ROAS]** (retour sur dépenses publicitaires), spécifié en pourcentage. Vous pouvez éventuellement saisir un **[!UICONTROL Max CPC]** (coût par clic) pour vous assurer que le réseau publicitaire ne paie pas plus qu’un montant spécifique pour chaque clic. **Remarque :** Utilisez cette option pour les campagnes dans des portefeuilles hybrides (mais pas dans des portefeuilles standard) avec une stratégie de dépenses quelconque à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS]. Dans les portfolios hybrides, Search, Social et Commerce optimise le retour sur investissement de Target.

  La position moyenne et les données sur l&#39;offre du CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;offre.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (campagnes commerciales uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel
les produits de la campagne sont vendus. Les produits étant associés aux pays cibles, ce paramètre détermine les produits faisant l’objet d’une publicité dans la campagne.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (campagnes d’audience uniquement ; facultatif) associe la campagne à un magasin de centres commerciaux spécifique pour les publicités automatisées basées sur des flux plutôt que les publicités réactives. Lorsque vous sélectionnez cette option, spécifiez les [!UICONTROL Merchant ID] et [!UICONTROL Products]. Vous devez créer des groupes publicitaires pour la campagne, mais vous n’avez pas besoin de créer des publicités.

Une fois que vous avez lié la campagne à un magasin et enregistré les paramètres, vous ne pouvez pas modifier cette option.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (campagnes d’audience liées à un magasin de centre commercial uniquement) Produits à faire de la publicité. Par défaut, *[!UICONTROL All products]* est sélectionné. Pour promouvoir uniquement les produits avec des attributs spécifiques, sélectionnez *[!UICONTROL Filter products]* et spécifiez jusqu’à sept combinaisons de dimension et d’attribut de produit sur lesquelles filtrer vos produits. Toutes les valeurs spécifiées doivent s’appliquer pour que les publicités s’affichent pour le produit. Par exemple, pour afficher des publicités pour des produits pour animaux de compagnie Acme, vous pouvez créer les filtres `Custom Label 1=animals`, `Category=pet supplies` et `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (campagnes de performances maximales uniquement) Langue de la publicité, qui doit correspondre à la langue des sites sur lesquels votre publicité peut apparaître. [!DNL Microsoft Advertising] détermine la langue d’un utilisateur à partir de divers signaux, y compris la requête de l’utilisateur, le pays de l’éditeur et le paramètre de langue de l’utilisateur.

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

Pour plus d’informations sur la disponibilité, voir l’aide d’Microsoft Advertising pour &quot;[Empêcher l’affichage d’annonces sur des sites web spécifiques](https://help.ads.microsoft.com/#apex/bae/en/14061/0)&quot;.

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

## [!UICONTROL Asset Groups] (par groupe de ressources)

**[!UICONTROL Asset Group Name]:** nom du dossier de ressources (groupe de ressources).

**[!UICONTROL Asset Group Status]:** État du groupe de ressources : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** URL finale de toutes les publicités créées à partir du groupe de ressources.

**[!UICONTROL Images]:** jusqu’à 20 images pour la publicité, y compris au moins une image carrée et une image paysage. Voir les [[!DNL Microsoft Advertising] directives d’image](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Vous pouvez télécharger des images ou les sélectionner dans votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour télécharger des images :

   1. Dans l’onglet [!UICONTROL Upload from Device], cliquez sur **[!UICONTROL +]** et sélectionnez des images sur votre appareil ou votre réseau.

   1. Pour chaque image :

      1. Sélectionnez les proportions.

      1. Faites glisser et positionnez la zone de recadrage si nécessaire pour sélectionner la partie visible de l’image, puis redimensionnez la partie visible de l’image si nécessaire.

      1. (Facultatif) Sélectionnez des proportions supplémentaires, puis repositionnez et redimensionnez éventuellement l’image selon les besoins pour chaque rapport d’aspect sélectionné.

         Une ressource est créée pour chaque format sélectionné.

      1. Cliquez sur **[!UICONTROL Proceed]**.

   1. Lorsque vous avez terminé de spécifier les images, cliquez sur **[!UICONTROL Upload]**.

* Pour sélectionner des images de votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les images.

**[!UICONTROL Logos]:** Au moins un logo. Vous pouvez inclure jusqu’à cinq. Voir les [[!DNL Microsoft Advertising] instructions relatives aux ressources](https://help.ads.microsoft.com/#apex/ads/en/60204/0). Vous pouvez télécharger des images ou les sélectionner dans votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour télécharger des images :

   1. Dans l’onglet [!UICONTROL Upload from Device], cliquez sur **[!UICONTROL +]** et sélectionnez des images sur votre appareil ou votre réseau.

   1. Pour chaque image :

      1. Sélectionnez les proportions.

      1. Faites glisser et positionnez la zone de recadrage si nécessaire pour sélectionner la partie visible de l’image, puis redimensionnez la partie visible de l’image si nécessaire.

      1. (Facultatif) Sélectionnez des proportions supplémentaires, puis repositionnez et redimensionnez éventuellement l’image selon les besoins pour chaque rapport d’aspect sélectionné.

         Une ressource est créée pour chaque format sélectionné.

      1. Cliquez sur **[!UICONTROL Proceed]**.

   1. Lorsque vous avez terminé de spécifier les images, cliquez sur **[!UICONTROL Upload]**.

* Pour sélectionner des images de votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les images.

**[!UICONTROL Headlines]:** Au moins trois titres courts, et jusqu’à 15 titres, d’un maximum de 30 caractères chacun. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text], saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources de votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Long Headlines]:** Au moins un titre long de cinq au maximum, avec un maximum de 90 caractères chacun. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text], saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources de votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Descriptions]:** Au moins deux descriptions, et jusqu’à cinq descriptions, contenant un maximum de 90 caractères chacune. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text], saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources de votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Call to Action]:** appel à l’action à inclure dans la publicité. Par défaut, *[!UICONTROL Act Now]* est sélectionné.

**[!UICONTROL Business Name]:** nom de l’entreprise, avec un maximum de 25 caractères. Il ne peut pas contenir de scripts, d’HTML ou d’autres langages de balisage.

**[!UICONTROL Audience Signal]:** (facultatif) [!DNL Microsoft Advertising] audiences à utiliser comme signaux d’audience pour la campagne. [!DNL Microsoft Advertising] Les modèles d’apprentissage automatique utilisent les audiences pour trouver des internautes similaires à cibler et peuvent également afficher des publicités à des audiences qui ne sont pas spécifiées comme signaux pour vous aider à atteindre vos objectifs de performances. Choisissez les audiences les plus susceptibles d’être converties.

>[!NOTE]
>Les signaux d’audience sont différents des [cibles d’audience au niveau du groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Permet de spécifier un autre groupe de ressources.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Indique s’il faut *[!UICONTROL Use account conversion goals for this campaign]* (valeur par défaut) ou *[!UICONTROL Use campaign specific conversion goals]*. Si vous choisissez de spécifier des objectifs de conversion pour la campagne, sélectionnez les objectifs dans la liste de tous les objectifs disponibles. **Remarque :** Les objectifs sont synchronisés quotidiennement, de sorte que les objectifs créés au cours des 24 heures précédentes ne peuvent pas être répertoriés. Pour mettre à jour la liste, [&#x200B; synchronisez manuellement les données du réseau publicitaire &#x200B;](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

>[!TIP]
>
>Si la campagne fait partie d’un portfolio hybride, la bonne pratique consiste à utiliser des objectifs au niveau de la campagne qui correspondent aux objectifs de conversion dans l’objectif du portfolio ; l’inclusion d’objectifs de conversion supplémentaires peut avoir une incidence sur les performances du portfolio.
>
> Toutefois, pour les campagnes dans des portefeuilles hybrides pour lesquelles vous [téléchargez des objectifs sur le réseau publicitaire &#x200B;](/help/search-social-commerce/tools/objective-upload-to-networks.md), effectuez les opérations suivantes dans l’éditeur du réseau publicitaire au lieu de : a) ajouter la mesure d’objectif du portefeuille de recherche, de réseaux sociaux et de Commerce (qui commence par &quot;O_ACS_OBJ&quot;) comme objectif de conversion de la campagne et b) ajouter les objectifs de campagne qui incluent des conversions suivies par l’événement universel [!DNL Microsoft Advertising] (UET) ), car les mesures suivies par le réseau publicitaire ne sont pas transférées vers le réseau publicitaire avec l’objectif .

>[!MORELIKETHIS]
>
>* [Gérer les campagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
