---
title: '[!DNL Google Ads] des paramètres de la campagne'
description: Référencez les paramètres des campagnes  [!DNL Google Ads] .
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 3057
ht-degree: 0%

---

# [!DNL Google Ads] des paramètres de la campagne

## \[Haut de la page]

**[!UICONTROL Campaign Name]:** nom de campagne unique au sein du compte.

**[!UICONTROL Status]:** statut d’affichage de la campagne : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Active*.

## onglet [!UICONTROL Basic Settings]

*Nouvelles campagnes uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte de réseau publicitaire.

**[!UICONTROL Campaign Type]:** Où placer des annonces publicitaires et quels types d’annonces la campagne peut contenir :

* *[!UICONTROL Search Network Only]:* affiche les publicités sur le réseau de recherche, qui comprend [!DNL Google] résultats de recherche et, éventuellement, les sites de partenaires de recherche. Vous devez spécifier des mots-clés pour chaque groupe publicitaire.

* *[!UICONTROL Search with Display Select]:* affiche des annonces sur le réseau de recherche (qui comprend des résultats de recherche [!DNL Google] et, éventuellement, des sites de partenaires de recherche) et affiche potentiellement des annonces sur les sites du réseau d’affichage. Sur le réseau d’affichage, [!DNL Google Ads] affiche vos annonces de manière sélective à l’aide d’enchères automatisées, quelle que soit la stratégie d’enchères de la campagne. Pour les annonces de recherche, spécifiez des mots-clés pour chaque groupe d’annonces ; pour les annonces d’affichage, spécifiez des emplacements et éventuellement des mots-clés pour chaque groupe d’annonces.

* *[!UICONTROL Shopping Network]:* affiche les annonces de produits, que [!DNL Google] génère automatiquement en fonction de vos produits dans [!DNL Google Merchant Center] sur [!DNL Google Shopping], la zone à côté de [!DNL Google] résultats de recherche (séparés des annonces textuelles) et (éventuellement) les sites web des partenaires de recherche. Pour chaque groupe publicitaire de la campagne, vous pouvez spécifier des groupes de produits à annoncer.

* *[!UICONTROL Display Network Only]:* affiche les publicités sur le réseau d’affichage. Pour chaque groupe publicitaire, vous devez spécifier des emplacements et pouvez éventuellement spécifier des mots-clés.

* *[!UICONTROL Performance Max]:* affiche et optimise les conversions de vos publicités sur plusieurs canaux à l’aide d’enchères intelligentes [!DNL Google Ads]. Dans les paramètres de la campagne, vous devez spécifier un ou plusieurs groupes de ressources, qui comprennent des images, des logos, des titres, des descriptions, des vidéos facultatives et des signaux d’audience. [!DNL Google Ads] combine automatiquement les ressources pour diffuser des annonces en fonction du canal (par exemple [!DNL YouTube], [!DNL Gmail] ou [!DNL Search]).

  **Remarques :**

  * Seuls les paramètres requis sont disponibles. Pour obtenir des paramètres facultatifs, connectez-vous à l’éditeur de [!DNL Google Ads].

  * Les liens vers les flux de produits [!DNL Google Merchant Center] ne sont pas pris en charge.

  * La prise en charge des groupes de listes n’est pas disponible. Pour gérer et afficher les données des groupes de listes, connectez-vous à l’éditeur de [!DNL Google Ads].

## onglet [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (campagnes qui ciblent uniquement le réseau de recherche, y compris les campagnes d’achat) Affiche vos annonces sur les réseaux de partenaires de recherche du réseau publicitaire. Par défaut, cette option est *[!UICONTROL Off]*.

**[!UICONTROL Audience Target Method]:**(Campagnes Gmail existantes en lecture seule uniquement) Si :

* *[!UICONTROL Bid Only]:* pour afficher des annonces même à des personnes qui ne sont pas associées à des audiences cibles, à condition qu’elles répondent aux cibles d’autres groupes d’annonces. Vous pouvez toutefois augmenter les chances que les publicités soient présentées à des audiences spécifiques en fixant des enchères plus élevées pour ces audiences.

* *[!UICONTROL Target and Bid]* Pour afficher les annonces uniquement aux utilisateurs associés aux audiences cibles qui répondent également aux autres cibles du groupe publicitaire.

**[!UICONTROL Contains EU Political Ads]:**(Applicable aux campagnes qui ciblent des audiences dans l’Union européenne (UE)) Que la campagne contienne ou non de la publicité politique selon les exigences pour les publicités diffusées dans l’Union européenne en vertu du règlement 2024/90 de l’UE : *[!UICONTROL No]* ou *[!UICONTROL Yes]*.

## onglet [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

**[!UICONTROL Google Recommended Budget]:** (facultatif ; applicable pour les campagnes Performance Max et Search avec tous les paramètres requis et qui incluent uniquement des groupes publicitaires) Cliquez sur **[!UICONTROL Show Recommendation]** pour afficher le budget recommandé par [!DNL Google Ads]. Actuellement, seules les campagnes comportant moins de 40 000 mots-clés sont éligibles.

Pour les campagnes Performance Max et Search, les paramètres suivants sont nécessaires pour les recommandations :

* type de stratégie d’enchères
* URL finale
* groupes de ressources

Pour les campagnes de recherche, les paramètres supplémentaires suivants sont également requis pour les recommandations :

* cible de la stratégie d’enchères
* pays
* langue
* un emplacement inclus ou exclu
* mots-clés

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Stratégie d’enchères pour la campagne :

* *[!UICONTROL Enhanced CPC]:* Obsolète. [!DNL Google Ads] a commencé à modifier automatiquement les [stratégies d’enchères CPC améliorées](https://support.google.com/google-ads/answer/2464964) existantes en une CPC manuelle en 2025.

* *[!UICONTROL Manual CPC]* (valeur par défaut) : (non disponible pour les campagnes de type Performance Max) utilise le modèle de coût par clic (CPC). Vous pouvez éventuellement permettre au réseau publicitaire de modifier les enchères pour la campagne :

  * **[!UICONTROL Enable Enhanced CPC]** (désactivé par défaut) : revient à utiliser l’option « [!UICONTROL Enhanced CPC] », qui est obsolète. [!DNL Google Ads] a commencé à modifier automatiquement les [stratégies d’enchères CPC améliorées](https://support.google.com/google-ads/answer/2464964) existantes en une CPC manuelle en 2025.

* *[!UICONTROL Maximize Clicks]:* (campagnes de recherche, d’affichage et d’achat) Le réseau publicitaire , et non Search, Social et Commerce, optimise les enchères pour maximiser les clics. Vous pouvez éventuellement saisir un **[!UICONTROL Max CPC]** (coût par clic) pour vous assurer que le réseau publicitaire ne paie pas plus d’un montant spécifique pour chaque clic. **Attention :** lorsque vous ajoutez une campagne avec cette stratégie à un portefeuille, les offres sont pilotées par le poids de clic, et non par l’objectif du portefeuille.

* *[!UICONTROL Maximize Conversion Value]:* (campagnes de recherche, de performances maximales et d’achats intelligents) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères afin d’optimiser la valeur de conversion. Entrez éventuellement un **[!UICONTROL Target Return on Ad Spend]** (ROAS) en pourcentage. **Remarque :** utilisez cette option pour les campagnes des portfolios avec optimisation au niveau des campagnes ou des groupes publicitaires, mais pas pour les portfolios avec optimisation au niveau des mots-clés. Dans les portfolios avec optimisation au niveau de la campagne ou du groupe publicitaire, Rechercher, réseaux sociaux et Commerce optimise le retour sur dépenses publicitaires cible au niveau de la campagne ou (le cas échéant) au niveau du groupe publicitaire.

* *[!UICONTROL Maximize Conversions]:* (campagnes Search, display et performance max) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères afin d’optimiser les conversions. Le cas échéant, entrez un **[!UICONTROL Target CPA]** (coût par acquisition) et la stratégie d&#39;enchères **[!UICONTROL Portfolio]** applicable. **Remarque :** utilisez cette option pour les campagnes des portfolios avec optimisation au niveau des campagnes ou des groupes publicitaires, mais pas pour les portfolios avec optimisation au niveau des mots-clés. Dans les portfolios avec optimisation au niveau de la campagne ou du groupe publicitaire, Search, Social et Commerce optimise le CPA cible au niveau de la campagne ou (le cas échéant) au niveau du groupe publicitaire.

* *[!UICONTROL Target CPA]:* (Campagnes en affichage seul) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères en fonction d’une **[!UICONTROL Target CPA]** facultative (coût par acquisition), qui correspond au montant moyen sur 30 jours que vous souhaitez payer pour une acquisition (conversion). **Remarque :** les campagnes dans des portfolios avec optimisation au niveau de la campagne ou du groupe publicitaire (mais pas dans les portfolios avec optimisation au niveau des mots-clés) avec n’importe quelle stratégie de dépenses, à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA]. Dans les portfolios avec optimisation au niveau de la campagne ou du groupe publicitaire, Search, Social et Commerce optimise le CPA cible au niveau de la campagne ou (le cas échéant) au niveau du groupe publicitaire.

  Les données d&#39;enchères Position moyenne et CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;enchères.

* *[!UICONTROL Target Impression Share]:* (Campagnes de recherche) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères pour obtenir un taux d’impressions et une position publicitaire cibles. Vous pouvez éventuellement saisir un **[!UICONTROL Target Impression Share]** sous la forme d’un pourcentage, du **[!UICONTROL Target Ad Position]** et d’un **[!UICONTROL Max CPC]** (coût par clic). **Remarque :** cette option n’est pas prise en charge dans les portefeuilles.

* *[!UICONTROL Target Return on Ad Spend]:* (Campagnes d’achat) Le réseau publicitaire (et non Search, Social et Commerce) optimise les enchères en fonction d’un **[!UICONTROL Target ROAS]** spécifié (retour sur dépenses publicitaires), spécifié sous la forme d’un pourcentage. **Remarque :** utilisez cette option pour les campagnes des portfolios avec optimisation au niveau des campagnes ou des groupes publicitaires (mais pas pour les portfolios avec optimisation au niveau des mots-clés) avec n’importe quelle stratégie de dépenses, à l’exception des [!UICONTROL Weekly] ou des [!UICONTROL Google Target ROAS]. Dans les portfolios avec optimisation au niveau de la campagne ou du groupe publicitaire, Rechercher, réseaux sociaux et Commerce optimise le retour sur dépenses publicitaires cible au niveau de la campagne ou (le cas échéant) au niveau du groupe publicitaire.

  Les données d&#39;enchères Position moyenne et CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;enchères.

* *[!UICONTROL Viewable CPM]:* (Campagnes [!DNL Gmail] existantes, en lecture seule uniquement) Le réseau publicitaire (et non Search, Social et Commerce) enchérit uniquement sur les publicités qui sont mesurées comme visibles. **Remarque :** l&#39;optimisation de cette stratégie n&#39;est prise en charge dans aucun type de portefeuille.

## onglet [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Campagnes d’achat uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel
les produits de la campagne sont vendus. Comme les produits sont associés aux pays cibles, ce paramètre détermine les produits qui sont annoncés dans la campagne.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Campagnes d’achats uniquement ; annonceurs participant déjà au programme d’achats locaux avec des magasins [!DNL Google Merchant Center] aux États-Unis, au Royaume-Uni, en Allemagne, en France, au Japon et au Japon ; facultatif) [!DNL Google Ads] d’ajouter automatiquement vos informations d’inventaire local à vos annonces d’achats sur Google.com.

**Conseil :** si vous utilisez ce paramètre, n’excluez pas les publicités locales du paramètre [!UICONTROL Inventory Filter].

**Remarque** les annonces d’inventaire local nécessitent deux flux supplémentaires à [!DNL Google Merchant Center] : l’un avec vos données de produit local et l’autre avec votre inventaire de produit local. Pour plus d’informations sur les [annonces d’achats locaux](https://www.google.com/retail/local-inventory-ads/), consultez la documentation [!DNL Google Ads] .

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## onglet [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (réseaux de recherche et d’affichage uniquement) Une ou plusieurs langues cibles pour les annonces de la campagne.

[!DNL Google Ads] détermine la langue d’un utilisateur à partir de son paramètre de langue [!DNL Google] ou de la langue de la requête de recherche, de la page active ou des pages récemment consultées sur le [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Emplacements géographiques d’utilisateurs spécifiques à inclure ou à exclure en tant que cibles. Par défaut, tous les emplacements sont ciblés. Vous pouvez inclure et exclure des utilisateurs dans n’importe quelle combinaison d’emplacements. Les exclusions remplacent toujours les inclusions.

* Pour cibler tous les emplacements, ne sélectionnez aucun emplacement.

* Pour cibler ou exclure des emplacements spécifiques :

  * (Pays, États, régions métropolitaines ou villes) Cliquez sur **[!UICONTROL Location Target]** (![Cible de l’emplacement](/help/search-social-commerce/assets/location-target.png "Cible de l’emplacement")) et localisez les emplacements à inclure et à exclure :

    * Pour inclure un emplacement et ses emplacements enfants, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche.

    * Pour exclure un emplacement, cliquez deux fois sur le cercle adjacent afin d’afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

    * Pour développer un emplacement dans ses sous-composants (tels que les États, les régions métropolitaines ou les villes des États-Unis), cliquez sur le nom de l’emplacement.

    * Pour rechercher un emplacement, saisissez ou collez au moins les trois premiers caractères de l’emplacement dans le champ de saisie. Dans les résultats de la recherche, cliquez sur **[!UICONTROL Include]** en regard d’un emplacement à inclure ou **[!UICONTROL Exclude]** en regard d’un emplacement à exclure.

  * (Emplacements proches d’une adresse ; cibles incluses uniquement) Cliquez sur **[!UICONTROL Radius Target]** (![Cible de rayon](/help/search-social-commerce/assets/radius-target.png "Cible de rayon")), puis sur **[!UICONTROL Address]**. Saisissez l’adresse et le rayon en milles ou kilomètres autour de l’adresse à cibler, puis cliquez sur **[!UICONTROL Add]**.

  * (Emplacements proches des coordonnées géographiques ; cibles incluses uniquement) Cliquez sur **[!UICONTROL Radius Target]** (![Cible de rayon](/help/search-social-commerce/assets/radius-target.png "Cible de rayon")), puis cliquez sur **[!UICONTROL Coordinate]**. Saisissez la latitude, la longitude et le rayon en milles ou kilomètres autour de l’emplacement à cibler, puis cliquez sur **[!UICONTROL Add]**.

* (Pour ajouter un ajustement d&#39;offre pour un lieu cible inclus) Saisissez une valeur d&#39;ajustement d&#39;offre :

* 0 % : pour ne pas ajuster les enchères pour les annonces à cet emplacement.

* \[Autres valeurs de -90 % à 300 %\] : pour augmenter ou diminuer l’enchère pour les annonces à cet emplacement.

**Remarque :**

* Search, Social et Commerce ne fournissent pas d’ajustements d’enchères ajustés automatiquement pour les cibles d’emplacement suivantes en raison des limites des données fournies par [!DNL Google Ads] pour mapper les emplacements d’internaute aux cibles d’emplacement :

  * Cibles de rayon.

  * Certains emplacements sous le niveau État/province/région/comté/préfecture pour lesquels [!DNL Google Ads] n’envoie pas d’emplacement parent dans l’URL de l’utilisateur, notamment les aéroports et les districts du Congrès des États-Unis.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## onglet [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Réseau d’affichage uniquement) Opérateurs mobiles spécifiques à cibler ; les opérateurs sont triés
par pays. Si vous ne sélectionnez aucune option, elles sont toutes ciblées.

**[!UICONTROL Mobile Carriers]:** (Réseau d’affichage uniquement) Systèmes d’exploitation spécifiques à cibler. Si vous ne sélectionnez aucune option, elles sont toutes ciblées.

## onglet [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## onglet [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## onglet [!UICONTROL AI Max]

*Campagnes ciblant uniquement le réseau de recherche*

**[!UICONTROL AI Max]:** si [[!UICONTROL AI Max]](https://support.google.com/google-ads/answer/15910366) doit être activé pour la campagne (correspondance de termes de recherche gérée par l’IA, personnalisation du texte et développement final de l’URL). Lorsque vous activez **[!UICONTROL AI Max]**, deux paramètres supplémentaires sont disponibles :

* **[!UICONTROL Text customization]:** permet-[!DNL Google Ads] d’utiliser l’IA générative pour personnaliser la copie de l’annonce, les titres et les descriptions en fonction des annonces existantes et de la copie de la page de destination ?

* **[!UICONTROL Final URL expansion]:** permet-il aux [!DNL Google Ads] d’acheminer le trafic vers la page de destination la plus pertinente de votre site web en fonction de leur intention de recherche ? Ce paramètre est disponible uniquement lorsque **[!UICONTROL Text customization]** est activé.

<!-- Clarify why this is "Unspecified" and read-only for me as of 7/23. Also, shouldn't we reword this? -->

**[!UICONTROL Bundling required]:** (campagnes existantes avec la fonction [!UICONTROL AI Max] activée uniquement ; lecture seule) Si [!UICONTROL AI Max] devez être activé pour respecter ou modifier la personnalisation du texte et les contrôles de liste de marque pour la campagne : *[!UICONTROL Required]*, *[!UICONTROL Not required]* ou *[!UICONTROL Unspecified]*.

<!-- Is this based on the advanced location options set elsewhere in Google Ads editor? -->

**[!UICONTROL Geo Targeting Type]:** (Campagnes existantes avec la fonction [!UICONTROL AI Max] activée uniquement ; lecture seule) Lorsque l’un des groupes publicitaires de la campagne inclut des cibles [!UICONTROL Locations of Interest], les types d’intérêts des utilisateurs et utilisatrices ciblés sont indiqués : *[!UICONTROL Search Interest]* (utilisateurs et utilisatrices intéressés par un emplacement spécifié), *[!UICONTROL Presence]* (utilisateurs et utilisatrices dans un emplacement spécifié ou régulièrement dans un emplacement spécifié) ou *[!UICONTROL Presence or Interest]* (utilisateurs et utilisatrices dans un emplacement spécifié, régulièrement dans un emplacement spécifié ou intéressés par un emplacement spécifié).

## onglet [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

### [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

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

**[!UICONTROL Track Product Group]:** (pour les [!UICONTROL EF Redirect] uniquement) Non implémenté

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

### [!UICONTROL Asset Groups] (par groupe de ressources)

*Performances max des campagnes uniquement*

**[!UICONTROL Asset Group Name]:** nom du groupe de ressources. Les liens vers les flux de produits [!DNL Google Merchant Center] ne sont pas pris en charge.

**[!UICONTROL Asset Group Status]:** statut du groupe de ressources : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** URL finale de toutes les publicités créées à partir du groupe de ressources. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and [!DNL Google Ads] replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Jusqu’à 15 images pour l’annonce, y compris au moins une image de paysage (1,91:1, au moins 600 x 314 pixels) et au moins une image carrée (1:1, au moins 300 x 300 pixels). Vous pouvez éventuellement inclure une image portrait (4:5, au moins 480 x 600 pixels). Voir [[!DNL Google Ads] spécifications de l’image](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Vous pouvez charger des images ou les sélectionner dans votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

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

**[!UICONTROL Logos]:** Au moins un logo carré (1:1, au moins 128 x 128 pixels). Vous pouvez éventuellement inclure un logo en paysage (4:1, au moins 512 x 218 pixels). Vous pouvez inclure jusqu’à cinq logos au total. Voir les [[!DNL Google Ads] spécifications du logo](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Vous pouvez charger des images ou les sélectionner dans votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

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

**[!UICONTROL Videos]:** (facultatif) Au moins une vidéo et jusqu’à cinq vidéos [!DNL YouTube] d’une durée d’au moins 10 secondes. Vous pouvez saisir des URL ou les sélectionner dans votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour saisir des URL :

  1. Dans l’onglet [!UICONTROL Enter Video Url] , saisissez une URL.

  1. (Facultatif) Pour ajouter une autre URL, cliquez sur **[!UICONTROL + Add]** et saisissez l’URL.

* Pour sélectionner des vidéos dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les vidéos.

**[!UICONTROL Headlines]:** Au moins trois titres courts, et jusqu&#39;à cinq titres courts, d&#39;un maximum de 30 caractères chacun. Au moins un titre doit comporter au moins 15 caractères. Si l’option au niveau de la campagne permettant d’activer l’extension finale de l’URL est définie dans [!DNL Google Ads], [!DNL Google Ads] remplace cette valeur par un titre personnalisé en fonction du contenu de la page de destination.

Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour saisir du texte :

  1. Dans l’onglet [!UICONTROL Enter Text] , saisissez le texte.

  1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez-les.

**[!UICONTROL Long Headlines]:** au moins un titre long, avec un maximum de 90 caractères chacun, et jusqu’à cinq titres longs. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour saisir du texte :

  1. Dans l’onglet [!UICONTROL Enter Text] , saisissez le texte.

  1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez-les.

**[!UICONTROL Descriptions]:** au moins deux descriptions, et jusqu’à quatre, contenant chacune un maximum de 90 caractères. Au moins une description doit comporter au moins 30 caractères. Vous pouvez saisir du texte ou sélectionner des ressources à partir de votre [!UICONTROL Asset Library], mais pas les deux dans la même opération.

* Pour saisir du texte :

  1. Dans l’onglet [!UICONTROL Enter Text] , saisissez le texte.

  1. (Facultatif) Pour ajouter une autre chaîne de texte, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez-les.

**[!UICONTROL Call to Action]:** call to action à inclure dans la publicité. Par défaut, *[!UICONTROL Automated]* est sélectionné et [!DNL Google Ads] sélectionne le call to action. Vous pouvez éventuellement choisir une autre action.

**[!UICONTROL Business Name]:** nom de l’entreprise, avec un maximum de 25 caractères.

**[!UICONTROL Audience Signal]:** (facultatif) [!DNL Google Ads] les audiences à utiliser comme signaux d’audience pour la campagne. Les modèles de machine learning [!DNL Google Ads] utilisent les audiences pour trouver des internautes similaires à cibler et peuvent également afficher des annonces à des audiences qui ne sont pas spécifiées comme signaux pour vous aider à atteindre vos objectifs de performances. Sélectionnez les audiences les plus susceptibles d’être converties.

>[!NOTE]
>
>Les signaux d’audience sont différents des [cibles d’audience au niveau de la campagne et du groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Primary Status]:** (champ en lecture seule pour les groupes de ressources existants dans les campagnes Performance Max) Pourquoi le groupe de ressources est-il diffusé ou non à pleine capacité ? Il prend en compte le statut du groupe de ressources ainsi que d’autres signaux, tels que les approbations de politique et de qualité. Les valeurs peuvent inclure *ÉLIGIBLE,* *LIMITÉ,* *NOT_ELIGIBLE,* *EN PAUSE,* *EN ATTENTE,* SUPPRIMÉ,*UNKNOWN,* ou *UNSPECIFIED.* **<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]:** (champ en lecture seule pour les groupes de ressources existants dans les campagnes Performance Max) Informations supplémentaires sur le statut principal du groupe de ressources. Les valeurs peuvent inclure *ASSET_GROUP_DISAPPROVED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,* *ASSET_GROUP_UNDER_REVIEW,* CAMPAIGN_ENDED,*CAMPAIGN_PAUSED,* CAMPAIGN_PENDING,*CAMPAIGN_REMOVED,* UNKNOWN,*ou* UNSPECIFIED.** ** **

### [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** s’il faut *[!UICONTROL Use account conversion goals for this campaign]* (valeur par défaut) ou *[!UICONTROL Use campaign specific conversion goals]*. Si vous choisissez de spécifier des objectifs de conversion pour la campagne, sélectionnez des objectifs standard et/ou créez un objectif personnalisé pour la campagne.

Les objectifs sont synchronisés tous les jours. Il se peut donc que les objectifs existants créés au cours des 24 heures précédentes ne soient pas répertoriés. Pour mettre à jour la liste, [synchronisez manuellement les données du réseau publicitaire](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Pour créer un objectif de conversion personnalisé, cliquez sur **[!UICONTROL + Add custom goal]**, saisissez le nom de l’objectif personnalisé, sélectionnez les [actions de conversion](https://support.google.com/google-ads/answer/6032150) à inclure dans l’objectif personnalisé, puis cliquez sur **[!UICONTROL Save]**. **Remarque :** Chaque campagne ne peut avoir qu’un seul objectif personnalisé.

>[!TIP]
>
>Si la campagne fait partie d’un portfolio hybride, la bonne pratique consiste à utiliser des objectifs au niveau de la campagne qui correspondent aux objectifs de conversion de l’objectif du portfolio. L’inclusion d’objectifs de conversion supplémentaires peut avoir une incidence sur les performances du portfolio.
>
>Toutefois, pour les campagnes dans des portfolios hybrides pour lesquelles vous [chargez les objectifs vers le réseau publicitaire](/help/search-social-commerce/tools/objective-upload-to-networks.md), procédez comme suit dans l’éditeur du réseau publicitaire au lieu de procéder ici : a) ajoutez la mesure d’objectif de portfolio Search, Social et Commerce téléchargée (qui commence par « O_ACS_OBJ ») comme action de conversion pour la campagne, et b) ajoutez tous les objectifs de campagne qui incluent des conversions suivies par le [!DNL Google], car les mesures suivies par le réseau publicitaire ne sont pas téléchargées sur le réseau publicitaire avec l’objectif .

### [!UICONTROL Set Customer Acquisition Goal]

Optimisez votre campagne pour les nouveaux clients, les clients existants ou les deux. Pour utiliser ce paramètre, vous devez d’abord activer l’objectif d’acquisition de nouveaux clients pour le compte [!DNL Google Ads] ou, le cas échéant, pour le compte responsable. L’objectif définit les listes de clients existants éligibles et la valeur de conversion supplémentaire pour les nouveaux clients dans les paramètres de conversion. Voir les étapes 1 à 2 dans l’aide [!DNL Google Ads] « [ Activer l’objectif d’acquisition de nouveaux clients ](https://support.google.com/google-ads/answer/14007601) ».

**[!UICONTROL Customer Goal]:** Type d’objectif d’acquisition de client :

* *[!UICONTROL All Customers]* (valeur par défaut) : effectuez une optimisation égale pour les nouveaux clients et les clients existants.

* *[!UICONTROL New Customers]:* donner la priorité à l’acquisition de nouveaux clients. La sélection de cette option affiche le paramètre **[!UICONTROL New Customer Bid Adjustment]**.

* *[!UICONTROL Existing Customers]:* privilégiez la fidélisation des clients existants.

**[!UICONTROL New Customer Bid Adjustment]:** (**[!UICONTROL Customer Goal]** défini sur **[!UICONTROL New Customers]** uniquement) Multiplicateur appliqué aux offres lors du ciblage de nouveaux clients, de 0,1 à 10,0. La valeur par défaut est 1,0 (aucun ajustement). Par exemple, une augmentation de 1,5x augmente les offres de 50 % pour les nouveaux clients, une augmentation de 2,0x double les offres pour les nouveaux clients et une réduction de 0,5x des offres de 50 % pour les nouveaux clients.

>[!MORELIKETHIS]
>
>* [Gérer les campagnes](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
