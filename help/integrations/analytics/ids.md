---
title: ID Adobe Advertising utilisés par  [!DNL Analytics]
description: ID Adobe Advertising utilisés par  [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: e8c8316418acf4a8c62beabcae2c1b7388dbc297
workflow-type: tm+mt
source-wordcount: '1758'
ht-degree: 0%

---

# Adobe Advertising IDs Used by [!DNL Analytics]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable à Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising utilise deux identifiants pour le suivi des performances sur site : l’*ID EF* et l’*ID AMO*.

Lorsqu’une impression publicitaire se produit, Adobe Advertising crée les valeurs d’ID AMO et d’ID EF et les stocke. Lorsqu’un visiteur qui a vu une annonce publicitaire accède au site sans cliquer sur une annonce, [!DNL Analytics] appelle ces valeurs depuis Adobe Advertising via le code JavaScript [!DNL Analytics for Advertising]. Pour le trafic d’affichage publicitaire, [!DNL Analytics] génère un ID supplémentaire (`SDID`), qui est utilisé pour regrouper les ID EF et AMO en [!DNL Analytics]. Pour le trafic de clics publicitaires, ces identifiants sont inclus dans l’URL de la page de destination à l’aide des paramètres de chaîne de requête `ef_id` et `s_kwcid` (pour l’AMO ID) .

Adobe Advertising fait la distinction entre une entrée de clic publicitaire ou d’affichage publicitaire sur le site web à l’aide des critères suivants :

* Une entrée d’affichage publicitaire est capturée lorsqu’un utilisateur ou une utilisatrice visite le site après avoir consulté une annonce publicitaire mais sans avoir cliqué dessus. [!DNL Analytics] enregistre une vue d’ensemble si deux conditions sont remplies :

   * Le visiteur ne dispose d’aucune publicité [!DNL DSP] ou [!DNL Search, Social, & Commerce] pendant l’intervalle de recherche en amont [clics publicitaires](#lookback-a4adc).

   * Le visiteur a vu au moins une publicité [!DNL DSP] pendant l’intervalle de recherche en amont [impression](#lookback-a4adc). La dernière impression est transmise comme affichage.

* Une entrée de clic publicitaire est capturée lorsqu’un visiteur du site clique sur une annonce avant d’accéder au site. [!DNL Analytics] capture un clic publicitaire lorsque l’une des conditions suivantes se produit :

   * L’URL comprend un EF ID et un AMO ID, tels qu’ajoutés par Adobe Advertising à l’URL de la page de destination.

   * L’URL ne contient aucun code de suivi, mais le code Adobe Advertising JavaScript détecte un clic au cours des deux dernières minutes.

![Intégration de [!DNL Analytics] basé sur la vue Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1 : Intégration de [!DNL Analytics] basé sur les vues Adobe Advertising*

![Intégration de [!DNL Analytics] basée sur les URL de clics Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2 : intégration de [!DNL Analytics] basées sur les clics Adobe Advertising*

## Identifiants d’éléments d’expérience Adobe Advertising

L’identifiant d’événement est un jeton unique utilisé par Adobe Advertising pour associer une activité à une exposition publicitaire ou à un clic en ligne. L’identifiant de l’annonce publicitaire est stocké dans [une dimension  [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] ([!DNL eVar] réservé) (identifiant de l’annonce publicitaire Adobe Advertising) et suit chaque clic publicitaire ou exposition publicitaire au niveau du navigateur ou de l’appareil concerné. Les identifiants EF servent principalement de clés pour envoyer des données [!DNL Analytics] à Adobe Advertising à des fins de création de rapports et d’optimisation des enchères dans Adobe Advertising.

### Format de l’ID de l’EF

>[!NOTE]
>
>Les identifiants d’éléments d’expérience sont sensibles à la casse. Si une implémentation [!DNL Analytics] force le suivi des URL à passer en minuscules, alors Adobe Advertising ne reconnaît pas l’identifiant de l’EF. Cela a un impact sur les enchères et les rapports Adobe Advertising, mais n’a aucun impact sur les rapports Adobe Advertising dans [!DNL Analytics].

#### [!DNL Google Ads] des annonces de recherche

```
{gclid}:G:s
```

où :

* `gclid` est le [!DNL Google Click ID] (GCLID).
* `s` est le type de réseau (« s » pour la recherche).

#### [!DNL Microsoft Advertising] des annonces de recherche

```
{msclkid}:G:s
```

où :

* `msclkid` est le [!DNL Microsoft Click ID] (MSCLKID).
* `s` est le type de réseau (« s » pour la recherche).

#### Affichage des annonces et des annonces de recherche sur d’autres moteurs de recherche

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

où :

* &lt;*Identifiant visiteur Adobe Advertising*> est un identifiant unique par visiteur (par exemple, UhKVaAAABCkJ0mDt). Également appelé *surfer ID*.

* &lt;*timestamp*> correspond à l’heure au format AAAAMMJJHHMMSS (par exemple 20190821192533 pour l’année 2019, le mois 08, le jour 21, l’heure 19:25:33).

* &lt;*channel type*> est le type de canal responsable du clic ou de l’exposition :

   * `d` d’un clic sur une publicité display DSP (affichage clic publicitaire)
   * `i` d’impression d’une publicité display DSP (affichage publicitaire)
   * `s` un clic sur une publicité de recherche (clic publicitaire de recherche).

Exemple de `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### Dimension de l’ID de l’EF dans [!DNL Analytics]

Dans les rapports [!DNL Analytics], vous pouvez trouver des données d’identifiant d’événement en recherchant la dimension [!UICONTROL EF ID] et en utilisant la mesure [!UICONTROL EF ID Instance] .

Les identifiants EF sont soumis à la limite de 500 000 identifiants uniques dans Analysis Workspace. Une fois la valeur de 500 000, tous les nouveaux codes de suivi sont signalés sous le titre « [!UICONTROL Low Traffic] ». En raison de la possibilité de rapport de fidélité manquant, les identifiants EF ne sont pas classés et vous ne devez pas les utiliser pour les segments ou les rapports dans [!DNL Analytics].

## ID AMO ADOBE ADVERTISING {#amo-id}

L’ID AMO suit chaque combinaison publicitaire unique à un niveau moins granulaire et est utilisé pour [!DNL Analytics] classification des données et l’ingestion des mesures publicitaires (telles que les impressions, les clics et les coûts) à partir d’Adobe Advertising. L’ID AMO est stocké dans une dimension [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (ID AMO) et est utilisé exclusivement pour la création de rapports dans [!DNL Analytics].

L’ID AMO est également appelé `s_kwcid`, ce qui se prononce parfois comme « [!DNL squid] ».

### Méthodes de mise en œuvre de l’AMO ID {#amo-id-implement}

Le paramètre est ajouté à vos URL de tracking de l’une des manières suivantes :

* (Recommandé) Lorsque la fonction d’insertion côté serveur est implémentée.

   * Clients DSP : le serveur de pixels ajoute automatiquement le paramètre s_kwcid aux suffixes de votre page de destination lorsqu’un utilisateur final consulte une publicité display avec le pixel Adobe Advertising.

   * Clients Search, Social et Commerce :

      * Pour les comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] dont le paramètre [!UICONTROL Auto Upload] est activé pour le compte ou la campagne, le serveur de pixels ajoute automatiquement le paramètre s_kwcid aux suffixes de votre page de destination lorsqu’un utilisateur final clique sur une annonce publicitaire contenant le pixel Adobe Advertising.

      * Pour d’autres réseaux publicitaires, ou pour les comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] dont le paramètre [!UICONTROL Auto Upload] est désactivé, ajoutez manuellement le paramètre à vos [paramètres d’ajout au niveau du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, qui l’ajoutent à vos URL de base.

* Lorsque la fonction d&#39;insertion côté serveur n&#39;est pas implémentée :

   * Clients DSP : le code [JavaScript](javascript.md) enregistre automatiquement les clics publicitaires et les affichages publicitaires. Lorsqu’un navigateur ne prend pas en charge les cookies tiers, vous pouvez toujours effectuer le suivi des conversions basées sur les clics pour les types d’annonces suivants :

      * Pour [!DNL Flashtalking] balises d’annonce publicitaire, insérez manuellement des macros supplémentaires par « [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md) ». **Remarque :** cette procédure n’est pas nécessaire si votre entreprise entretient un partenariat direct avec [!DNL Flashtalking] et que vous utilisez des macros de transfert de données pour collecter les données de clic conformément à la documentation d’assistance [!DNL Flashtalking] à l’`https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`.

      * Pour [!DNL Google Campaign Manager 360] balises d’annonce publicitaire, insérez manuellement des macros supplémentaires par « [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md) ».

   * Clients Search, Social et Commerce :

      * Pour les publicités ([!DNL Google Ads] et [!DNL Microsoft Advertising]), ajoutez manuellement le paramètre d’ID AMO à vos suffixes de page de destination, idéalement au niveau du [compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} sauf si un suivi différent est nécessaire pour les composants de compte individuels.

      * Pour les publicités sur tous les autres réseaux publicitaires, ajoutez manuellement le paramètre ID AMO à vos [paramètres d’ajout au niveau du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, qui l’ajoutent à vos URL de base.

Pour implémenter la fonction d’insertion côté serveur ou déterminer la meilleure option pour votre entreprise, contactez l’équipe chargée de votre compte Adobe.

### AMO - Formats d&#39;ID {#amo-id-formats}

#### AMO - Format d&#39;ID pour [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

où :

* `AC` indique le canal d’affichage.

* `{TM_AD_ID}` est la clé de publicité alphanumérique générée par Adobe Advertising. Il s’agit d’un identifiant unique pour une publicité et sert de clé pour traduire les métadonnées des entités Adobe Advertising en dimensions [!DNL Analytics] lisibles.

* `{TM_PLACEMENT_ID}` est la clé d’emplacement alphanumérique générée par Adobe Advertising. Il s’agit d’un identifiant unique pour un emplacement et sert de clé pour traduire les métadonnées des entités Adobe Advertising en dimensions [!DNL Analytics] lisibles.

Exemple d’ID AMO : AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### Formats d’ID AMO pour les publicités Search, Social et Commerce {#amo-id-format-search}

Les paramètres varient selon le réseau publicitaire, mais les paramètres suivants sont communs à tous :

* `AL` indique le canal de recherche. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` est un ID d’utilisateur unique attribué à l’annonceur.

* `{sid}` est remplacé par l’ID numérique du compte de réseau publicitaire de l’annonceur : *3* pour [!DNL Google Ads], *10* pour [!DNL Microsoft Advertising], *45* pour [!DNL Meta], *86* pour [!DNL Yahoo! Display Network], *87*, [!DNL Naver]88 *,* 90[!DNL Baidu], *94* pour [!DNL Yandex], *105* pour [!DNL Yahoo! Japan Ads] (obsolète) ou *106* pour [!DNL Yahoo Native] ** [!DNL Pinterest] (obsolète).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

où :

* `{creative}` est l’identifiant numérique unique du réseau publicitaire pour le créatif.
* `{placement}` est le site web sur lequel l’utilisateur ou l’utilisatrice a cliqué sur la publicité.
* `{keywordid}` est l’identifiant numérique unique du réseau publicitaire pour le mot-clé qui a déclenché la publicité.

##### [!DNL Google Ads]

Cela inclut les campagnes d’achat à l’aide de [!DNL Google Merchant Center].

* Comptes qui utilisent le dernier format d’identifiant AMO, qui prend en charge le reporting au niveau des campagnes et des groupes publicitaires pour les campagnes de type Performances max , ainsi que les campagnes de type brouillons et expériences :

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Tous les autres comptes :

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

où :

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` est l’identifiant numérique unique [!DNL Google Ads] pour le contenu créatif.
* `{matchtype}` correspond au type de correspondance du mot-clé qui a déclenché l’annonce : `e` pour exact, `p` pour expression ou `b` pour large.
* `{placement}` est le nom de domaine du site web sur lequel l’utilisateur a cliqué sur la publicité. Une valeur est disponible pour les annonces dans les campagnes ciblées par emplacement et pour les annonces dans les campagnes ciblées par mot-clé qui sont affichées sur les sites de contenu.
* `{network}` indique le réseau à partir duquel le clic a eu lieu : `g` pour [!DNL Google] recherche (pour les annonces ciblées par mot-clé uniquement), `s` pour un partenaire de recherche (pour les annonces ciblées par mot-clé uniquement) ou `d` pour le réseau d’affichage (pour les annonces ciblées par mot-clé ou par positionnement).
* `{product_partition_id}` est l’identifiant numérique unique du réseau publicitaire pour le groupe de produits utilisé avec les publicités de produit.
* `{keyword}` est le mot-clé spécifique qui a déclenché votre annonce (sur les sites de recherche) ou le mot-clé le plus correspondant (sur les sites de contenu).
* `{campaignid}` est l’identifiant numérique unique du réseau publicitaire pour la campagne.
* `{adgroupid}` est l’identifiant numérique unique du réseau publicitaire pour le groupe publicitaire.

>[!NOTE]
>
>* Pour les annonces de recherche dynamique, {keyword} est renseigné avec le ciblage automatique.
>* Lorsque vous générez le suivi de [!DNL Google] publicités d’achat, un paramètre d’ID de produit, `{adwords_producttargetid}`, est inséré avant le paramètre de mot-clé . Le paramètre d’ID de produit n’apparaît pas dans les paramètres de suivi au niveau du compte et de la campagne [!DNL Google Ads].
>* Pour utiliser le code de suivi AMO ID le plus récent, voir « [Mettre à jour le code de suivi AMO ID pour un [!DNL Google Ads] compte](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md) » <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Tous les types de campagne :

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

où :

* `{AdId}` est l’identifiant numérique unique du réseau publicitaire pour le créatif.
* `{OrderItemId}` est l’identifiant numérique du réseau publicitaire pour le mot-clé.
* `{CampaignId}` est l’identifiant numérique unique du réseau publicitaire pour la campagne.
* `{AdGroupId}` est l’identifiant numérique unique du réseau publicitaire pour le groupe publicitaire.

>[!NOTE]
>
> Pour les comptes disposant de campagnes sans l’option de tracking [!UICONTROL Auto Upload] qui n’ont pas déjà été migrés au nouveau format, mettez manuellement à jour chaque suffixe de page de destination pour inclure le format ci-dessus.
>En attendant, les formats hérités, comme suit, fonctionnent toujours :
>* Campagnes de recherche :
>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Campagnes d’achat (à l’aide de [!DNL Microsoft Merchant Center]) :
>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campagnes réseau d’audience :
>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

où :

* `{creative}` est l’identifiant numérique unique du réseau publicitaire pour le créatif.
* `{matchtype}` correspond au type de correspondance du mot-clé qui a déclenché l’annonce : `be` pour exact, `bp` pour expression ou `bb` pour large.
* `{network}` indique le réseau à partir duquel le clic a eu lieu : `n` pour natif ou `s` pour recherche.
* `{keyword}` est le mot-clé qui a déclenché votre publicité.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

où :

* `{ad_id}` est l’identifiant numérique unique du réseau publicitaire pour le créatif.
* `{source_type}` est le type de site sur lequel la publicité a été affichée : *b* pour la recherche, *c* pour le contexte (contenu) ou *ct* pour la catégorie.
* `{phrase_id}` est l’identifiant numérique du réseau publicitaire pour le mot-clé.

### AMO ID Dimension dans [!DNL Analytics]

Dans les rapports Analytics, vous pouvez trouver des données d’ID AMO en recherchant la dimension [!UICONTROL AMO ID] et en utilisant la mesure [!UICONTROL AMO ID Instances] . La dimension [!UICONTROL AMO ID] héberge toutes les valeurs d’ID AMO capturées, tandis que la mesure [!UICONTROL AMO ID Instances] indique la fréquence à laquelle une valeur d’ID AMO a été capturée par le site. Par exemple, si la même publicité de recherche a fait l’objet de quatre clics mais qu’Analytics a suivi sept entrées de site, [!UICONTROL AMO ID Instances] serait sept (7) et [!UICONTROL Clicks] serait quatre (4).

Pour les rapports ou les audits au sein de [!DNL Analytics], la bonne pratique consiste à utiliser l’AMO ID avec son instance correspondante. Pour plus d’informations, voir « [Validation des données de clic publicitaire pour  [!DNL Analytics for Advertising]](data-variances.md#data-validation) » dans « Variances de données attendues entre [!DNL Analytics] et Adobe Advertising ».

## À Propos Des Classifications Analytics

Dans [!DNL Analytics], une [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) est un élément de métadonnées pour un code de suivi donné, tel qu’un compte, une campagne ou une publicité. Adobe Advertising classe les données Adobe Advertising brutes à l’aide de classifications afin que vous puissiez afficher les données de différentes manières (par exemple par type d’annonce ou campagne) lorsque vous générez des rapports. Les classifications forment la base des rapports Adobe Advertising dans [!DNL Analytics] et peuvent être utilisées avec les mesures AMO telles que [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] et [!UICONTROL AMO Clicks], ainsi qu’avec les événements sur site personnalisés et standard tels que [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] et [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Écarts de données attendus entre  [!DNL Analytics]  et Adobe Advertising](data-variances.md)
