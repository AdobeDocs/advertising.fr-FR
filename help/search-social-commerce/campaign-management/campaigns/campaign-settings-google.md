---
title: '''[!DNL Google Ads] paramètres de campagne'
description: Référencez les paramètres pour [!DNL Google Ads] campagnes.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: 7b4818260fad61a773fb7261cbcdfd84bee84d42
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---

# [!DNL Google Ads] paramètres de campagne

## \[Ecran de création de campagne\]

**[!UICONTROL Campaign Type]:** (Disponible uniquement lors de la création de la campagne) Où placer des publicités et quels types de publicités peuvent contenir la campagne :

* *[!UICONTROL Search Network Only]:* Affiche les publicités sur le réseau de recherche, qui inclut [!DNL Google] résultats de recherche et, éventuellement, sites de partenaires de recherche. Vous devez spécifier des mots-clés pour chaque groupe publicitaire.

* *[!UICONTROL Search with Display Select]:* Affiche les publicités sur le réseau de recherche (qui inclut [!DNL Google] résultats de recherche et, éventuellement, sites de partenaires de recherche) et affiche éventuellement des publicités sur les sites de réseau d’affichage. Sur le réseau d&#39;affichage, [!DNL Google Ads] affiche vos publicités de manière sélective à l’aide d’enchères automatisées, quelle que soit la stratégie d’offre de la campagne. Pour rechercher des publicités, spécifiez des mots-clés pour chaque groupe publicitaire. Pour les publicités affichées, spécifiez des emplacements et éventuellement des mots-clés pour chaque groupe publicitaire.

* *[!UICONTROL Shopping Network]:* Affiche les publicités de produits, qui [!DNL Google] génère automatiquement en fonction de vos produits dans [!DNL Google Merchant Center] on [!DNL Google Shopping], la zone en regard de [!DNL Google] résultats de recherche (séparés des publicités textuelles) et (éventuellement) sites web de partenaires de recherche. Pour chaque groupe publicitaire de la campagne, vous pouvez spécifier des groupes de produits à promouvoir.

* *[!UICONTROL Display Network Only]:* Affiche les publicités sur le réseau d’affichage. Pour chaque groupe d’annonces, vous devez spécifier des emplacements et pouvez éventuellement spécifier des mots-clés.

* *[!UICONTROL Performance Max]:* (Fonction bêta) Affiche et optimise les conversions de vos publicités sur plusieurs canaux à l’aide de [!DNL Google Ads] enchères intelligentes. Dans les paramètres de l’opération, vous devez indiquer un ou plusieurs groupes de ressources, notamment des images, des logos, des titres, des descriptions, des vidéos facultatives et des signaux d’audience. [!DNL Google Ads] combine automatiquement les ressources pour diffuser des publicités en fonction du canal (comme [!DNL YouTube], [!DNL Gmail], ou [!DNL Search]).

  **Remarques :**

   * Seuls les paramètres requis sont disponibles. Pour les paramètres facultatifs, connectez-vous au [!DNL Google Ads] éditeur.

   * Liens vers [!DNL Google Merchant Center] les flux de produit ne sont pas pris en charge.

   * La prise en charge des groupes de listes n’est pas disponible. Pour gérer et afficher les données des groupes répertoriés, connectez-vous au [!DNL Google Ads] éditeur.

   * L’optimisation hybride est prise en charge. Les cibles de la stratégie d&#39;offre et les budgets de campagne sont définis au niveau de l&#39;opération.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Nom de campagne unique dans le compte.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Campagnes Gmail existantes en lecture seule uniquement) Si :

* *[!UICONTROL Target and Bid]* Pour afficher les publicités uniquement aux utilisateurs associés aux audiences cibles qui correspondent également à d’autres cibles du groupe publicitaire.

* *[!UICONTROL Bid Only]:*  Afficher les publicités même aux personnes qui ne sont pas associées aux audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire. Vous pouvez toutefois augmenter les chances d&#39;affichage des publicités à des audiences spécifiques en définissant des offres plus élevées pour ces audiences.

**[!UICONTROL Status]:** Etat d&#39;affichage de l&#39;opération : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Actif*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campagnes ciblant uniquement le réseau de recherche, y compris les campagnes d’achat) Affiche vos publicités sur les réseaux de partenaires de recherche du réseau publicitaire. Par défaut, cette option est *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** Stratégie d’offre pour la campagne :

* *[!UICONTROL Enhanced CPC]:* (Non disponible pour la performance maximale ou existant, lecture seule) [!DNL Gmail] campagnes) Utilise le modèle de coût par clic amélioré du réseau publicitaire, qui permet au réseau publicitaire de modifier automatiquement l’offre coût par clic (CPC) pour chaque enchère afin d’optimiser les conversions à l’aide des conversions spécifiées dans le réseau publicitaire (et non dans Search, Social et Commerce), tout en essayant de maintenir le CPC moyen en dessous du CPC maximum.

Lorsque vous ajoutez une campagne avec eCPC à un portefeuille de recherche, de réseaux sociaux et de commerce optimisé, Search, Social et Commerce optimise les offres de base et , lorsque le paramètre[!UICONTROL Auto adjust campaign budget limits]&quot; est activée : le budget de l’opération. Le réseau publicitaire optimise tous les ajustements d’offres et peut modifier les offres générées par Search, Social et Commerce au moment de la requête de l’utilisateur en fonction de données et d’informations propriétaires. **Attention :** Utilisez les campagnes eCPC dans les portfolios uniquement lorsque le total des conversions suivies sur le réseau publicitaire correspond à l’objectif du portfolio. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (valeur par défaut) : (non disponible pour les campagnes de performances max.) utilise le modèle coût par clic (CPC). Vous pouvez éventuellement autoriser le réseau publicitaire à modifier les offres pour la campagne :

   * **[!UICONTROL Enable Enhanced CPC]** (désactivé par défaut) : il s’agit de la même chose que l’utilisation du paramètre[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Campagnes de recherche, d’affichage et d’achat) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour maximiser les clics. Si vous le souhaitez, vous pouvez saisir une **[!UICONTROL Max CPC]** (coût par clic) pour s’assurer que le réseau publicitaire ne paie pas plus qu’un montant spécifique pour chaque clic. **Attention :** Lorsque vous ajoutez une campagne avec cette stratégie à un portefeuille, les offres sont basées sur le poids des clics et non sur l’objectif du portefeuille.

* *[!UICONTROL Maximize Conversion Value]:* (Campagnes d’achat intelligentes, de recherche et de performances max.) Le réseau publicitaire, et non Search, Social et Commerce, optimise les offres afin d’optimiser la valeur de conversion. Si vous le souhaitez, vous pouvez saisir un **[!UICONTROL Target Return on Ad Spend]** (RSDP) en pourcentage. **Remarque :** Utilisez cette option pour les campagnes dans des portfolios hybrides, mais pas dans des portfolios standard.

* *[!UICONTROL Maximize Conversions]:* (Campagnes de recherche, d’affichage et de performances max.) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour maximiser les conversions. Si vous le souhaitez, vous pouvez saisir un **[!UICONTROL Target CPA]** (coût par acquisition). **Remarque :** Utilisez cette option pour les campagnes dans des portfolios hybrides, mais pas dans des portfolios standard.

* *[!UICONTROL Target CPA]:* (Campagnes d’affichage ; campagnes de recherche existantes) Le réseau publicitaire, et non Search, Social et Commerce, optimise les offres en fonction d’une **[!UICONTROL Target CPA]** (coût par acquisition), qui est le montant moyen de 30 jours que vous souhaitez payer pour une acquisition (conversion). **Remarque :** Utilisez cette option pour les campagnes dans des portfolios hybrides (mais pas dans des portfolios standard) avec une stratégie de dépenses, à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target CPA].

  La position moyenne et les données sur l&#39;offre du CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;offre.

  Pour les nouvelles campagnes de recherche, [!DNL Google Ads] a remplacé cette stratégie d’offre par la méthode [!UICONTROL Maximize Conversions] stratégie utilisant une [!UICONTROL Target CPA] . Pour les campagnes de recherche existantes avec cette stratégie, vous ne pouvez modifier que la valeur de la cible, ce qui modifie la stratégie en [!UICONTROL Maximize Conversions] stratégie utilisant la variable spécifiée [!UICONTROL Target CPA] .

* *[!UICONTROL Target Impression Share]:* (Campagnes de recherche) Le réseau publicitaire — et non Search, Social et Commerce — optimise les offres pour obtenir un partage d’impression cible et une position publicitaire. Si vous le souhaitez, vous pouvez saisir une **[!UICONTROL Target Impression Share]** en pourcentage, la valeur **[!UICONTROL Target Ad Position]**, et a **[!UICONTROL Max CPC]** (coût par clic). **Remarque :** Cette option n’est pas prise en charge dans les portefeuilles.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campagnes d’affichage et d’achat ; campagnes de recherche existantes) Le réseau publicitaire, et non Search, Social &amp; Commerce, optimise les offres en fonction d’une **[!UICONTROL Target ROAS]** (retour sur dépenses publicitaires), spécifié en pourcentage. **Remarque :** Utilisez cette option pour les campagnes dans des portfolios hybrides (mais pas dans des portfolios standard) avec une stratégie de dépenses, à l’exception de [!UICONTROL Weekly] ou [!UICONTROL Google Target ROAS].

  La position moyenne et les données sur l&#39;offre du CPC ne sont pas disponibles pour les campagnes avec cette stratégie d&#39;offre.

  Pour les nouvelles campagnes de recherche, [!DNL Google Ads] a remplacé cette stratégie d’offre par la méthode [!UICONTROL Maximize Conversion Value] stratégie utilisant une [!UICONTROL Target Return on Ad Spend value]. Pour les campagnes de recherche existantes avec cette stratégie, vous ne pouvez modifier que la valeur de la cible, ce qui modifie la stratégie en [!UICONTROL Maximize Conversion Value] stratégie utilisant la variable spécifiée [!UICONTROL Target Return on Ad Spend] .

* *[!UICONTROL Viewable CPM]:* (Existant, lecture seule) [!DNL Gmail] campagnes uniquement) Le réseau publicitaire — et non Search, Social et Commerce — offre uniquement sur les publicités qui sont mesurées comme visibles. **Remarque :** L’optimisation de cette stratégie n’est prise en charge dans aucun type de portefeuille.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Campagnes d’achat uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel les produits de la campagne sont vendus. Les produits étant associés aux pays cibles, ce paramètre détermine les produits faisant l’objet d’une publicité dans la campagne.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Campagnes d’achat uniquement ; les annonceurs participant déjà au programme d’achat local avec [!DNL Google Merchant Center] magasins aux États-Unis, au Royaume-Uni, en France, en France, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud, en Afrique du Sud ; facultatif). [!DNL Google Ads] pour ajouter automatiquement vos informations d’inventaire locales à vos publicités commerciales sur Google.com.

**Conseil :** Si vous utilisez ce paramètre, n’excluez pas les publicités locales dans la variable [!UICONTROL Inventory Filter] .

**Remarque :** Les annonces d’inventaire locales nécessitent deux flux supplémentaires vers [!DNL Google Merchant Center] — un avec vos données de produit locales et un autre avec votre inventaire de produit local. Voir [!DNL Google Ads] documentation pour plus d’informations [publicités commerciales locales](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Réseaux de recherche et d’affichage uniquement) Une ou plusieurs langues cibles pour les publicités dans la campagne.

[!DNL Google Ads] détermine la langue d’un utilisateur à partir de [!DNL Google] paramètre de langue ou de la langue de la requête de recherche, de la page active ou des pages récemment consultées sur la page [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Emplacements géographiques d’utilisateurs spécifiques à inclure ou à exclure en tant que cibles. Par défaut, tous les emplacements sont ciblés. Vous pouvez inclure et exclure des utilisateurs dans n’importe quelle combinaison d’emplacements. Les exclusions remplacent toujours les inclusions.

* Pour cibler tous les emplacements, ne sélectionnez aucun emplacement.

* Pour cibler ou exclure des emplacements spécifiques :

   * (Pays, états, régions métropolitaines ou villes) Cliquez sur **[!UICONTROL Location Target]** (![Cible de l’emplacement](/help/search-social-commerce/assets/location-target.png "Cible de l’emplacement")) et localisez les emplacements à inclure et exclure :

      * Pour inclure un emplacement et ses emplacements enfants, cliquez une fois sur le cercle en regard de celui-ci pour qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche.

      * Pour exclure un emplacement, cliquez deux fois sur le cercle en regard de celui-ci afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

      * Pour développer un emplacement dans ses sous-composants (États, régions métropolitaines ou villes des États-Unis, par exemple), cliquez sur le nom de l’emplacement.

      * Pour rechercher un emplacement, saisissez ou collez au moins les trois premiers caractères de l’emplacement dans le champ de saisie. Dans les résultats de la recherche, cliquez sur **[!UICONTROL Include]** en regard d’un emplacement à inclure ou **[!UICONTROL Exclude]** en regard d’un emplacement à exclure.

   * (Emplacements près d’une adresse ; cibles incluses uniquement) Cliquez sur **[!UICONTROL Radius Target]** (![Cible du rayon](/help/search-social-commerce/assets/radius-target.png "Cible du rayon")), puis cliquez sur **[!UICONTROL Address]**. Saisissez l’adresse et le rayon en kilomètres autour de l’adresse à cibler, puis cliquez sur **[!UICONTROL Add]**.

   * (Emplacements proches des coordonnées géographiques ; cibles incluses uniquement) Cliquez sur **[!UICONTROL Radius Target]** (![Cible du rayon](/help/search-social-commerce/assets/radius-target.png "Cible du rayon")), puis cliquez sur **[!UICONTROL Coordinate]**. Saisissez la latitude et la longitude et le rayon en kilomètres autour de l’emplacement à cibler, puis cliquez sur **[!UICONTROL Add]**.

* (Pour ajouter un ajustement d’offre pour un emplacement cible inclus) Saisissez une valeur d’ajustement d’offre :

* 0 % : pour ne pas ajuster les offres pour les publicités à cet emplacement.

* \[Autres valeurs de -90 % à 300 %\] : pour augmenter ou diminuer l’offre pour les publicités à cet emplacement.

**Remarque :**

* Search, Social et Commerce ne fournit pas d’ajustements d’enchères auto-ajustés pour les cibles d’emplacement suivantes en raison de limitations dans les données que la variable [!DNL Google Ads] fournit pour mapper les emplacements des surfeurs aux cibles d’emplacement :

   * Cibles de rayon.

   * Certains emplacements situés sous le niveau de l’état/de la province/région/du département/de la préfecture pour lesquels [!DNL Google Ads] n&#39;envoie pas un emplacement parent dans l&#39;URL du surfeur, y compris les aéroports et les circonscriptions du Congrès américain.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Afficher le réseau uniquement) Transporteurs mobiles spécifiques à cibler ; les opérateurs sont triés par pays. Si vous n’en sélectionnez aucune, toutes sont ciblées.

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

**[!UICONTROL Asset Group Name]:** Nom du groupe de ressources. Liens vers [!DNL Google Merchant Center] les flux de produit ne sont pas pris en charge.

**[!UICONTROL Asset Group Status]:** État du groupe de ressources : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** URL finale de toutes les publicités créées à partir du groupe de ressources. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Jusqu’à 15 images pour la publicité, dont les tailles suivantes : 1) au moins trois images carrées, 2) au moins trois images paysage et 3) au moins une image portrait. Voir [[!DNL Google Ads] spécifications d’image](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Vous pouvez soit télécharger des images, soit les sélectionner parmi les [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour télécharger des images :

   1. Sur le [!UICONTROL Upload from Device] , cliquez sur **[!UICONTROL +]** et sélectionnez des images sur votre appareil ou votre réseau.

   1. Pour chaque image :

      1. Sélectionnez les proportions.

      1. Faites glisser et positionnez la zone de recadrage si nécessaire pour sélectionner la partie visible de l’image, puis redimensionnez la partie visible de l’image si nécessaire.

      1. (Facultatif) Sélectionnez des proportions supplémentaires, puis repositionnez et redimensionnez éventuellement l’image selon les besoins pour chaque rapport d’aspect sélectionné.

         Une ressource est créée pour chaque format sélectionné.

      1. Cliquez sur **[!UICONTROL Proceed]**.

   1. Lorsque vous avez terminé de spécifier des images, cliquez sur **[!UICONTROL Upload]**.

* Pour sélectionner des images dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les images.

**[!UICONTROL Logos]:** Au moins un logo carré (1:1) et un logo paysage (4:1). Vous pouvez inclure jusqu’à cinq de chaque taille. Voir [[!DNL Google Ads] spécifications](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). Vous pouvez soit télécharger des images, soit les sélectionner parmi les [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour télécharger des images :

   1. Sur le [!UICONTROL Upload from Device] , cliquez sur **[!UICONTROL +]** et sélectionnez des images sur votre appareil ou votre réseau.

   1. Pour chaque image :

      1. Sélectionnez les proportions.

      1. Faites glisser et positionnez la zone de recadrage si nécessaire pour sélectionner la partie visible de l’image, puis redimensionnez la partie visible de l’image si nécessaire.

      1. (Facultatif) Sélectionnez des proportions supplémentaires, puis repositionnez et redimensionnez éventuellement l’image selon les besoins pour chaque rapport d’aspect sélectionné.

         Une ressource est créée pour chaque format sélectionné.

      1. Cliquez sur **[!UICONTROL Proceed]**.

   1. Lorsque vous avez terminé de spécifier des images, cliquez sur **[!UICONTROL Upload]**.

* Pour sélectionner des images dans votre [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les images.

**[!UICONTROL Videos]:** (Facultatif) Au moins un et jusqu’à cinq, [!DNL YouTube] vidéos d’au moins 10 secondes. Vous pouvez saisir des URL ou les sélectionner parmi les [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir des URL :

   1. Sur le [!UICONTROL Enter Video Url] , saisissez une URL.

   1. (Facultatif) Pour ajouter une autre URL, cliquez sur **[!UICONTROL + Add]** et saisissez l’URL.

* Pour sélectionner des vidéos dans [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les vidéos.

**[!UICONTROL Headlines]:** Au moins trois titres courts d’un maximum de 30 caractères chacun, et cinq d’entre eux. Au moins un titre doit comporter 15 caractères ou moins. Si l’option de niveau campagne permettant d’activer l’extension d’URL finale est définie dans [!DNL Google Ads], puis [!DNL Google Ads] remplace cette valeur par un titre personnalisé basé sur le contenu de la landing page.

Vous pouvez saisir du texte ou sélectionner des ressources dans le [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Sur le [!UICONTROL Enter Text] , saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Long Headlines]:** Au moins un et jusqu’à cinq gros titres de 90 caractères chacun au maximum. Vous pouvez saisir du texte ou sélectionner des ressources dans le [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Sur le [!UICONTROL Enter Text] , saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Descriptions]:** Au moins deux descriptions, et jusqu’à quatre descriptions, avec un maximum de 90 caractères chacune. Au moins une description doit comporter 30 caractères ou moins. Vous pouvez saisir du texte ou sélectionner des ressources dans le [!UICONTROL Asset Library] — mais pas les deux dans la même opération.

* Pour saisir du texte :

   1. Sur le [!UICONTROL Enter Text] , saisissez le texte.

   1. (Facultatif) Pour ajouter une autre chaîne, cliquez sur **[!UICONTROL + Add]** et saisissez la chaîne.

* Pour sélectionner des ressources dans [!UICONTROL Asset Library], cliquez sur **[!UICONTROL Asset Library]** et sélectionnez les ressources.

**[!UICONTROL Call to Action]:** Appel à l’action à inclure dans la publicité. Par défaut, *[!UICONTROL Automated]* est sélectionné, et [!DNL Google Ads] sélectionne l’appel à l’action. Vous pouvez éventuellement choisir une autre action.

**[!UICONTROL Business Name]:** Nom de l’entreprise, avec un maximum de 25 caractères.

**[!UICONTROL Audience Signal]:** (Facultatif) [!DNL Google Ads] audiences à utiliser comme signaux d’audience pour la campagne. [!DNL Google Ads] Les modèles d’apprentissage automatique utilisent les audiences pour trouver des internautes similaires à cibler et peuvent également afficher des publicités à des audiences qui ne sont pas spécifiées comme signaux pour vous aider à atteindre vos objectifs de performances. Choisissez les audiences les plus susceptibles d’être converties.

>[!NOTE]
>Les signaux d’audience sont différents de [cibles d’audience au niveau de la campagne et du groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Permet de spécifier un autre groupe de ressources.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Si *[!UICONTROL Use account conversion goals for this campaign]* (valeur par défaut) ou *[!UICONTROL Use campaign specific conversion goals]*. Si vous choisissez de spécifier des objectifs de conversion pour la campagne, sélectionnez des objectifs standard et/ou créez un objectif personnalisé pour la campagne.

Les objectifs sont synchronisés quotidiennement. Il se peut donc que les objectifs existants créés au cours des 24 heures précédentes ne soient pas répertoriés. Pour mettre à jour la liste, [synchroniser manuellement les données du réseau publicitaire ;](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Pour créer un objectif de conversion personnalisé, cliquez sur **[!UICONTROL + Add custom goal]**, saisissez le nom personnalisé de l’objectif, puis sélectionnez l’option [actions de conversion](https://support.google.com/google-ads/answer/6032150) à inclure dans l’objectif personnalisé, puis cliquez sur **[!UICONTROL Save]**. **Remarque :** Chaque campagne ne peut avoir qu’un seul objectif personnalisé.

>[!TIP]
>
>Si la campagne fait partie d’un portfolio, utilisez les mêmes objectifs de conversion que l’objectif du portfolio. L’utilisation d’objectifs de conversion différents peut avoir une incidence sur les performances du portefeuille.

>[!MORELIKETHIS]
>
>* [Gestion des campagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
