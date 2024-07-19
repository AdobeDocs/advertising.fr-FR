---
title: Paramètres de campagne '[!DNL Google Ads]'
description: Référencez les paramètres des campagnes  [!DNL Google Ads] .
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: 977314f07d1299d9b94680861b046161bb444228
workflow-type: tm+mt
source-wordcount: '2450'
ht-degree: 0%

---

# [!DNL Google Ads] paramètres de campagne

## \[Ecran de création de campagne\]

**[!UICONTROL Campaign Type]:** (Disponible uniquement lors de la création de la campagne) Où placer des publicités et quels types de publicités
la campagne peut contenir :

* *[!UICONTROL Search Network Only]:* affiche des publicités sur le réseau de recherche, qui incluent [!DNL Google] résultats de recherche et, éventuellement, des sites de partenaires de recherche. Vous devez spécifier des mots-clés pour chaque groupe publicitaire.

* *[!UICONTROL Search with Display Select]:* affiche des publicités sur le réseau de recherche (qui incluent [!DNL Google] résultats de recherche et, éventuellement, sites de partenaires de recherche) et affiche éventuellement des publicités sur les sites de réseau d’affichage. Sur le réseau d’affichage, [!DNL Google Ads] affiche vos publicités de manière sélective à l’aide d’enchères automatisées, quelle que soit la stratégie d’offre de la campagne. Pour rechercher des publicités, spécifiez des mots-clés pour chaque groupe publicitaire. Pour les publicités affichées, spécifiez des emplacements et éventuellement des mots-clés pour chaque groupe publicitaire.

* *[!UICONTROL Shopping Network]:* Affiche les publicités de produits, que [!DNL Google] génère automatiquement en fonction de vos produits dans [!DNL Google Merchant Center] sur [!DNL Google Shopping], de la zone en regard de [!DNL Google] résultats de recherche (séparés des publicités textuelles) et (éventuellement) des sites web de partenaires de recherche. Pour chaque groupe publicitaire de la campagne, vous pouvez spécifier des groupes de produits à promouvoir.

* *[!UICONTROL Display Network Only]:* affiche des publicités sur le réseau d’affichage. Pour chaque groupe d’annonces, vous devez spécifier des emplacements et pouvez éventuellement spécifier des mots-clés.

* *[!UICONTROL Performance Max]:* affiche et optimise les conversions de vos publicités sur tous les canaux à l’aide de l’offre dynamique [!DNL Google Ads]. Dans les paramètres de l’opération, vous devez indiquer un ou plusieurs groupes de ressources, notamment des images, des logos, des titres, des descriptions, des vidéos facultatives et des signaux d’audience. [!DNL Google Ads] combine automatiquement les ressources pour diffuser des publicités en fonction du canal (par exemple [!DNL YouTube], [!DNL Gmail] ou [!DNL Search]).

  **Notes :**

   * Seuls les paramètres requis sont disponibles. Pour les paramètres facultatifs, connectez-vous à l’éditeur [!DNL Google Ads].

   * Les liens vers les flux de produits [!DNL Google Merchant Center] ne sont pas pris en charge.

   * La prise en charge des groupes de listes n’est pas disponible. Pour gérer et afficher les données des groupes de liste, connectez-vous à l’éditeur [!DNL Google Ads].

   * L’optimisation hybride est prise en charge. Les cibles de la stratégie d&#39;offre et les budgets de campagne sont définis au niveau de l&#39;opération.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** nom de campagne unique dans le compte.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Campagnes Gmail existantes en lecture seule uniquement) Indique si :

* *[!UICONTROL Target and Bid]* Pour afficher les publicités uniquement aux utilisateurs associés aux audiences cibles qui répondent également à toute autre cible du groupe publicitaire.

* *[!UICONTROL Bid Only]:* pour afficher les publicités même aux personnes qui ne sont pas associées aux audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire. Vous pouvez toutefois augmenter les chances d&#39;affichage des publicités à des audiences spécifiques en définissant des offres plus élevées pour ces audiences.

**[!UICONTROL Status]:** État d’affichage de la campagne : *Active* ou *En pause*. La valeur par défaut des nouvelles campagnes publicitaires est *Active*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campagnes qui ciblent uniquement le réseau de recherche, y compris les campagnes d’achat) Affiche
vos publicités sur les réseaux de partenaires de recherche du réseau publicitaire. Par défaut, cette option est *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Stratégie d’offre pour la campagne :

* *[!UICONTROL Enhanced CPC]:* (Non disponible pour les performances maximales ou les campagnes [!DNL Gmail] existantes et en lecture seule) utilise le modèle de coût par clic amélioré du réseau publicitaire, qui permet au réseau publicitaire de modifier automatiquement l’offre coût par clic (CPC) pour chaque enchère afin d’optimiser les conversions à l’aide des conversions spécifiées dans le réseau publicitaire (pas dans Search, Social et Commerce), tout en essayant de conserver le CPC moyen. en dessous du CPC maximum.

Lorsque vous ajoutez une campagne avec eCPC à un portefeuille de recherche, de réseaux sociaux et de Commerce optimisé, Search, Social et Commerce optimise les offres de base et, lorsque l’option &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; est activée, le budget de la campagne. Le réseau publicitaire optimise tous les ajustements d’offres et peut modifier les offres générées par Search, Social et Commerce au moment de la requête de l’utilisateur en fonction de données et d’informations propriétaires. **Attention :** Utilisez les campagnes eCPC dans les portefeuilles uniquement lorsque le total des conversions suivies sur le réseau publicitaire correspond à l’objectif du portfolio. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (valeur par défaut) : (non disponible pour les campagnes de performances max.) utilise le modèle coût par clic (CPC). Vous pouvez éventuellement autoriser le réseau publicitaire à modifier les offres pour la campagne :

   * **[!UICONTROL Enable Enhanced CPC]** (désactivé par défaut) : c’est la même chose que d’utiliser l’option &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Campagnes de recherche, d’affichage et d’achat) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour maximiser les clics. Vous pouvez éventuellement saisir un **[!UICONTROL Max CPC]** (coût par clic) pour vous assurer que le réseau publicitaire ne paie pas plus qu’un montant spécifique pour chaque clic. **Attention :** Lorsque vous ajoutez une campagne avec cette stratégie à un portefeuille, les offres sont pilotées par le poids des clics et non par l’objectif du portefeuille.

* *[!UICONTROL Maximize Conversion Value]:* (campagnes de recherche, de performance maximale et d’achats intelligents) Le réseau publicitaire, et non Search, Social et Commerce, optimise les offres pour maximiser la valeur de conversion. Vous pouvez éventuellement saisir un **[!UICONTROL Target Return on Ad Spend]** (RSDP) en pourcentage. **Remarque :** Utilisez cette option pour les campagnes dans des portefeuilles hybrides, mais pas dans des portefeuilles standard.

* *[!UICONTROL Maximize Conversions]:* (Campagnes max de recherche, d’affichage et de performances) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour maximiser les conversions. Vous pouvez éventuellement saisir un **[!UICONTROL Target CPA]** (coût par acquisition). **Remarque :** Utilisez cette option pour les campagnes dans des portefeuilles hybrides, mais pas dans des portefeuilles standard.

* *[!UICONTROL Target CPA]:* (Campagnes d’affichage ; campagnes de recherche existantes) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres en fonction d’un **[!UICONTROL Target CPA]** facultatif (coût par acquisition), qui est le montant moyen de 30 jours que vous souhaitez payer pour une acquisition (conversion). **Remarque :** Utilisez cette option pour les campagnes dans des portefeuilles hybrides (mais pas dans des portefeuilles standard) avec une stratégie de dépenses quelconque à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA].

  La position moyenne et les données sur l&#39;offre du CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;offre.

  Pour les nouvelles campagnes de recherche, [!DNL Google Ads] a remplacé cette stratégie d’offre par la stratégie [!UICONTROL Maximize Conversions] à l’aide d’une valeur [!UICONTROL Target CPA]. Pour les campagnes de recherche existantes avec cette stratégie, vous pouvez uniquement modifier la valeur cible, ce qui modifie la stratégie en [!UICONTROL Maximize Conversions] à l’aide de la valeur [!UICONTROL Target CPA] spécifiée.

* *[!UICONTROL Target Impression Share]:* (Campagnes de recherche) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour obtenir un partage d’impression cible et une position publicitaire. Vous pouvez éventuellement saisir un **[!UICONTROL Target Impression Share]** en pourcentage, le **[!UICONTROL Target Ad Position]** et un **[!UICONTROL Max CPC]** (coût par clic). **Remarque :** Cette option n’est pas prise en charge dans les portefeuilles.

* *[!UICONTROL Target Return on Ad Spend]:* (campagnes d’affichage et d’achat ; campagnes de recherche existantes) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres en fonction d’un **[!UICONTROL Target ROAS]** spécifié (retour sur dépenses publicitaires), spécifié en pourcentage. **Remarque :** Utilisez cette option pour les campagnes dans des portefeuilles hybrides (mais pas dans des portefeuilles standard) avec une stratégie de dépenses quelconque à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS].

  La position moyenne et les données sur l&#39;offre du CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;offre.

  Pour les nouvelles campagnes de recherche, [!DNL Google Ads] a remplacé cette stratégie d’offre par la stratégie [!UICONTROL Maximize Conversion Value] à l’aide d’un [!UICONTROL Target Return on Ad Spend value]. Pour les campagnes de recherche existantes avec cette stratégie, vous pouvez uniquement modifier la valeur cible, ce qui modifie la stratégie en [!UICONTROL Maximize Conversion Value] à l’aide de la valeur [!UICONTROL Target Return on Ad Spend] spécifiée.

* *[!UICONTROL Viewable CPM]:* (campagnes existantes, en lecture seule [!DNL Gmail] uniquement) Le réseau publicitaire — et non Search, Social et Commerce — offre uniquement sur les publicités qui sont mesurées comme visibles. **Remarque :** L’optimisation de cette stratégie n’est prise en charge dans aucun type de portefeuille.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (campagnes commerciales uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel
les produits de la campagne sont vendus. Les produits étant associés aux pays cibles, ce paramètre détermine les produits faisant l’objet d’une publicité dans la campagne.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (campagnes d’achat uniquement ; annonceurs participant déjà au programme d’achat local avec [!DNL Google Merchant Center] magasins aux États-Unis, au Royaume-Uni, en France, FR, JP et AU ; facultatif) Permet à [!DNL Google Ads] d’ajouter automatiquement vos informations d’inventaire local à vos publicités d’achat sur Google.com.

**Conseil :** Si vous utilisez ce paramètre, n’excluez pas les publicités locales dans le paramètre [!UICONTROL Inventory Filter].

**Remarque :** Les annonces d’inventaire local nécessitent deux flux supplémentaires vers [!DNL Google Merchant Center] : l’un avec vos données de produit locales et l’autre avec votre inventaire de produits locaux. Consultez la documentation [!DNL Google Ads] pour plus d’informations sur les [publicités commerciales locales](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Réseaux de recherche et d’affichage uniquement) Une ou plusieurs langues cibles pour les publicités dans la campagne.

[!DNL Google Ads] détermine la langue d’un utilisateur à partir du paramètre de langue [!DNL Google] de l’utilisateur ou de la langue de la requête de recherche, de la page active ou des pages récemment consultées sur [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** emplacements géographiques d’utilisateurs spécifiques à inclure ou à exclure en tant que cibles. Par défaut, tous les emplacements sont ciblés. Vous pouvez inclure et exclure des utilisateurs dans n’importe quelle combinaison d’emplacements. Les exclusions remplacent toujours les inclusions.

* Pour cibler tous les emplacements, ne sélectionnez aucun emplacement.

* Pour cibler ou exclure des emplacements spécifiques :

   * (Pays, états, régions métropolitaines ou villes) Cliquez sur **[!UICONTROL Location Target]** (![Cible de l’emplacement](/help/search-social-commerce/assets/location-target.png "Cible de l’emplacement")) et localisez les emplacements à inclure et exclure :

      * Pour inclure un emplacement et ses emplacements enfants, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Include](/help/search-social-commerce/assets/include.png "Include")) s’affiche.

      * Pour exclure un emplacement, cliquez deux fois sur le cercle adjacent afin qu’une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

      * Pour développer un emplacement dans ses sous-composants (États, régions métropolitaines ou villes des États-Unis, par exemple), cliquez sur le nom de l’emplacement.

      * Pour rechercher un emplacement, saisissez ou collez au moins les trois premiers caractères de l’emplacement dans le champ de saisie. Dans les résultats de recherche, cliquez sur **[!UICONTROL Include]** en regard d’un emplacement à inclure ou **[!UICONTROL Exclude]** en regard d’un emplacement à exclure.

   * (Emplacements près d’une adresse ; cibles incluses uniquement) Cliquez sur **[!UICONTROL Radius Target]** (![Cible du rayon](/help/search-social-commerce/assets/radius-target.png "Cible du rayon")), puis sur **[!UICONTROL Address]**. Saisissez l&#39;adresse et le rayon en kilomètres autour de l&#39;adresse à cibler, puis cliquez sur **[!UICONTROL Add]**.

   * (Emplacements proches des coordonnées géographiques ; cibles incluses uniquement) Cliquez sur **[!UICONTROL Radius Target]** (![Cible du rayon](/help/search-social-commerce/assets/radius-target.png "Cible du rayon")), puis sur **[!UICONTROL Coordinate]**. Saisissez la latitude et la longitude et le rayon en miles ou kilomètres autour de l’emplacement à cibler, puis cliquez sur **[!UICONTROL Add]**.

* (Pour ajouter un ajustement d’offre pour un emplacement cible inclus) Saisissez une valeur d’ajustement d’offre :

* 0 % : pour ne pas ajuster les offres pour les publicités à cet emplacement.

* \[Autres valeurs de -90 % à 300 %\] : pour augmenter ou diminuer l’offre pour les publicités à cet emplacement.

**Remarque :**

* Search, Social et Commerce ne fournit pas d’ajustements d’enchères auto-ajustés pour les cibles d’emplacement suivantes en raison de limitations des données que [!DNL Google Ads] fournit pour mapper les emplacements de surfeur aux cibles d’emplacement :

   * Cibles de rayon.

   * Certains emplacements au-dessous du niveau État/province/département/préfecture pour lesquels [!DNL Google Ads] n’envoie pas d’emplacement parent dans l’URL du surfeur, y compris les aéroports et les districts du Congrès des États-Unis.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Afficher le réseau uniquement) Opérateurs mobiles spécifiques à cibler ; les opérateurs sont triés
par pays. Si vous n’en sélectionnez aucune, toutes sont ciblées.

**[!UICONTROL Mobile Carriers]:** (Afficher le réseau uniquement) Systèmes d’exploitation spécifiques à cibler. Si vous n’en sélectionnez aucune, toutes sont ciblées.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

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

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

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

**[!UICONTROL Asset Group Name]:** Nom du groupe de ressources. Les liens vers les flux de produits [!DNL Google Merchant Center] ne sont pas pris en charge.

**[!UICONTROL Asset Group Status]:** État du groupe de ressources : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** URL finale de toutes les publicités créées à partir du groupe de ressources. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Jusqu’à 15 images pour la publicité, y compris les tailles suivantes : 1) au moins trois images carrées, 2) au moins trois images paysage et 3) au moins une image portrait. Voir les [[!DNL Google Ads] spécifications d’image](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Vous pouvez télécharger des images ou les sélectionner dans votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

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

**[!UICONTROL Logos]:** Au moins un logo carré (1:1) et un logo paysage (4:1). Vous pouvez inclure jusqu’à cinq de chaque taille. Voir les [[!DNL Google Ads] spécifications du logo](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Vous pouvez télécharger des images ou les sélectionner dans votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

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

**[!UICONTROL Videos]:** (Facultatif) Au moins une vidéo de 10 secondes au moins, et jusqu’à cinq vidéos [!DNL YouTube]. Vous pouvez saisir des URL ou les sélectionner dans votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir des URL :

   1. Dans l’onglet [!UICONTROL Enter Video Url], saisissez une URL.

   1. (Facultatif) Pour ajouter une autre URL, cliquez sur **[!UICONTROL + Add]** et saisissez l’URL.

* Pour sélectionner des vidéos dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les vidéos.

**[!UICONTROL Headlines]:** Au moins trois titres courts, et jusqu’à cinq titres courts de 30 caractères chacun au maximum. Au moins un titre doit comporter 15 caractères ou moins. Si l’option de niveau campagne permettant d’activer l’extension d’URL finale est définie dans [!DNL Google Ads], [!DNL Google Ads] remplace cette valeur par un titre personnalisé basé sur le contenu de la page d’entrée.

Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text], saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources de votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Long Headlines]:** Au moins un titre long de cinq au maximum, avec un maximum de 90 caractères chacun. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text], saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources de votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Descriptions]:** Au moins deux descriptions, et jusqu’à quatre descriptions, contenant un maximum de 90 caractères chacune. Au moins une description doit comporter 30 caractères ou moins. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Dans l’onglet [!UICONTROL Enter Text], saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources de votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Call to Action]:** appel à l’action à inclure dans la publicité. Par défaut, *[!UICONTROL Automated]* est sélectionné et [!DNL Google Ads] sélectionne l’appel à l’action. Vous pouvez éventuellement choisir une autre action.

**[!UICONTROL Business Name]:** nom de l’entreprise, avec un maximum de 25 caractères.

**[!UICONTROL Audience Signal]:** (facultatif) [!DNL Google Ads] audiences à utiliser comme signaux d’audience pour la campagne. [!DNL Google Ads] Les modèles d’apprentissage automatique utilisent les audiences pour trouver des internautes similaires à cibler et peuvent également afficher des publicités à des audiences qui ne sont pas spécifiées comme signaux pour vous aider à atteindre vos objectifs de performances. Choisissez les audiences les plus susceptibles d’être converties.

>[!NOTE]
>Les signaux d’audience sont différents des [cibles d’audience au niveau de la campagne et du groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Permet de spécifier un autre groupe de ressources.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Indique s’il faut *[!UICONTROL Use account conversion goals for this campaign]* (valeur par défaut) ou *[!UICONTROL Use campaign specific conversion goals]*. Si vous choisissez de spécifier des objectifs de conversion pour la campagne, sélectionnez des objectifs standard et/ou créez un objectif personnalisé pour la campagne.

Les objectifs sont synchronisés quotidiennement. Il se peut donc que les objectifs existants créés au cours des 24 heures précédentes ne soient pas répertoriés. Pour mettre à jour la liste, [ synchronisez manuellement les données du réseau publicitaire ](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Pour créer un objectif de conversion personnalisé, cliquez sur **[!UICONTROL + Add custom goal]**, saisissez le nom de l’objectif personnalisé, sélectionnez les [actions de conversion](https://support.google.com/google-ads/answer/6032150) à inclure dans l’objectif personnalisé, puis cliquez sur **[!UICONTROL Save]**. **Remarque :** Chaque campagne ne peut avoir qu’un seul objectif personnalisé.

>[!TIP]
>
>Si la campagne fait partie d’un portfolio hybride, la bonne pratique consiste à utiliser des objectifs au niveau de la campagne qui correspondent aux objectifs de conversion dans l’objectif du portfolio ; l’inclusion d’objectifs de conversion supplémentaires peut avoir une incidence sur les performances du portfolio.
>
>Toutefois, pour les campagnes dans des portefeuilles hybrides pour lesquelles vous [ téléchargez des objectifs sur le réseau publicitaire ](/help/search-social-commerce/tools/objective-upload-to-networks.md), effectuez les opérations suivantes dans l’éditeur du réseau publicitaire au lieu de : a) ajouter la mesure objective du portefeuille de recherche, de réseaux sociaux et de Commerce (qui commence par &quot;O_ACS_OBJ&quot;) comme action de conversion pour la campagne et b) ajouter tous les objectifs de campagne qui incluent des conversions suivies par [!DNL Google], car le réseau publicitaire Les mesures ne sont pas transférées vers le réseau publicitaire avec l’objectif .

>[!MORELIKETHIS]
>
>* [Gérer les campagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

