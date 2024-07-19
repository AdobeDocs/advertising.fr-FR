---
title: ID d’Adobe Advertising utilisés par [!DNL Analytics]
description: ID d’Adobe Advertising utilisés par [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 0%

---

# ID d’Adobe Advertising utilisés par [!DNL Analytics]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable à Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising utilise deux ID pour le suivi des performances sur site : l’ *EF ID* et l’ *AMO ID*.

Lorsqu’une impression de publicité se produit, Adobe Advertising crée les valeurs AMO ID et EF ID et les stocke. Lorsqu&#39;un visiteur qui a vu une publicité accède au site sans cliquer sur une publicité, [!DNL Analytics] appelle ces valeurs de l&#39;Adobe Advertising au code JavaScript [!DNL Analytics for Advertising]. Pour le trafic d’affichage publicitaire, [!DNL Analytics] génère un ID supplémentaire (`SDID`), qui est utilisé pour regrouper l’ID EF et l’AMO dans [!DNL Analytics]. Pour le trafic de clics publicitaires, ces identifiants sont inclus dans l’URL de la page d’entrée à l’aide des paramètres de chaîne de requête `ef_id` et `s_kwcid` (pour l’AMO ID).

L’Adobe Advertising fait la distinction entre une entrée de clic publicitaire ou d’affichage publicitaire sur le site web selon les critères suivants :

* Une entrée d’affichage publicitaire est capturée lorsqu’un utilisateur se rend sur le site après avoir affiché une publicité, mais sans cliquer dessus. [!DNL Analytics] enregistre un affichage publicitaire si deux conditions sont remplies :

   * Le visiteur n’a aucun clic publicitaire pour une publicité [!DNL DSP] ou [!DNL Search, Social, & Commerce] au cours de l’ [ intervalle de recherche en amont des clics ](#lookback-a4adc).

   * Le visiteur a vu au moins une publicité [!DNL DSP] au cours de l’ [intervalle de recherche en amont des impressions](#lookback-a4adc). La dernière impression est transmise comme affichage publicitaire.

* Une entrée de clic publicitaire est capturée lorsqu’un visiteur du site clique sur une publicité avant d’accéder au site. [!DNL Analytics] capture un clic publicitaire lorsque l’une des conditions suivantes se produit :

   * L’URL comprend un EF ID et un AMO ID, ajoutés par Adobe Advertising à l’URL de la page d’entrée.

   * L’URL ne contient aucun code de suivi, mais le code JavaScript d’Adobe Advertising détecte un clic au cours des deux dernières minutes.

![Intégration [!DNL Analytics] basée sur des vues d&#39;Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1 : Intégration [!DNL Analytics] basée sur les vues d&#39;Adobe Advertising*

![Intégration [!DNL Analytics] basée sur une URL de clic d’Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2 : Intégration [!DNL Analytics] basée sur une URL de clic d’Adobe Advertising*

## Adobe Advertising des ID EF

L’identifiant EF est un jeton unique utilisé par Adobe Advertising pour associer une activité à une exposition aux clics ou publicités en ligne. L’identifiant EF est stocké dans la dimension [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] (réservé [!DNL eVar]) (Adobe Advertising de l’identifiant EF) et suit chaque clic ou exposition publicitaire au niveau du navigateur ou de l’appareil. Les EF ID agissent principalement comme des clés pour envoyer des données [!DNL Analytics] à l’Adobe Advertising pour la création de rapports et l’optimisation des offres dans Adobe Advertising.

### Format d’identifiant EF

>[!NOTE]
>
>Les identifiants EF sont sensibles à la casse. Si une mise en oeuvre de [!DNL Analytics] force le suivi des URL à être en minuscules, alors Adobe Advertising ne reconnaît pas l’identifiant EF. Cela a un impact sur les offres et les rapports d’Adobe Advertising, mais n’a aucun impact sur les rapports d’Adobe Advertising dans [!DNL Analytics].

#### [!DNL Google Ads] annonces de recherche

```
{gclid}:G:s
```

où :

* `gclid` est le [!DNL Google Click ID] (GCLID).
* `s` est le type de réseau (&quot;s&quot; pour la recherche).

#### [!DNL Microsoft Advertising] annonces de recherche

```
{msclkid}:G:s
```

où :

* `msclkid` est le [!DNL Microsoft Click ID] (MSCLKID).
* `s` est le type de réseau (&quot;s&quot; pour la recherche).

#### Afficher des publicités et des annonces de recherche sur d’autres moteurs de recherche

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

où :

* &lt;*Adobe Advertising visitor ID*> est un identifiant unique par visiteur (par exemple, EuhKVaABCkJ0mDt). Également appelé *surfer ID*.

* &lt;*timestamp*> correspond à l’heure au format YYYYMMDHHMMSS (par exemple, 20190821192533 pour l’année 2019, le mois 08, le jour 21, l’heure 19 :25:33).

* &lt;*channel type*> est le type de canal responsable du clic ou de l’exposition :

   * `d` pour un clic sur une publicité DSP (clic publicitaire)
   * `i` pour une impression d’une publicité DSP (affichage publicitaire)
   * `s` pour un clic sur une publicité de recherche (clic publicitaire).

Exemple `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### La Dimension EF ID dans [!DNL Analytics]

Dans les rapports [!DNL Analytics], vous pouvez rechercher des données d’identifiant EF en recherchant la dimension [!UICONTROL EF ID] et en utilisant la mesure [!UICONTROL EF ID Instance].

Les identifiants EF sont soumis à la limite d’identifiant unique de 500 000 dans Analysis Workspace. Une fois la valeur de 500 000 atteinte, tous les nouveaux codes de suivi sont signalés sous le titre d’élément d’une ligne &quot;[!UICONTROL Low Traffic]&quot;. En raison de la possibilité d’une fidélité des rapports manquante, les identifiants EF ne sont pas classés et vous ne devez pas les utiliser pour les segments ou les rapports dans [!DNL Analytics].

## Adobe Advertising des AMO ID {#amo-id}

L’AMO ID effectue le suivi de chaque combinaison d’annonces unique à un niveau moins granulaire et est utilisé pour la classification des données [!DNL Analytics] et l’ingestion de mesures publicitaires (telles que les impressions, les clics et les coûts) à partir de l’Adobe Advertising. L’AMO ID est stocké dans une dimension [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (AMO ID) et est utilisé exclusivement pour la création de rapports dans [!DNL Analytics].

L’AMO ID est également appelé `s_kwcid`, qui est parfois prononcé en tant que &quot;[!DNL the squid]&quot;.

### Méthodes de mise en oeuvre d’AMO ID {#amo-id-implement}

Le paramètre est ajouté à vos URL de suivi de l’une des manières suivantes :

* (Recommandé) Lorsque la fonction d’insertion côté serveur est mise en oeuvre.

   * DSP clients : le serveur de pixels ajoute automatiquement le paramètre s_kwcid aux suffixes de votre page d’entrée lorsqu’un utilisateur final affiche une publicité avec le pixel Adobe Advertising.

   * Clients Search, Social et Commerce :

      * Pour les comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] dont le paramètre [!UICONTROL Auto Upload] est activé pour le compte ou la campagne, le serveur de pixels ajoute automatiquement le paramètre s_kwcid aux suffixes de votre page d’entrée lorsqu’un utilisateur clique sur une publicité avec le pixel Adobe Advertising.

      * Pour les autres réseaux publicitaires, ou les comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] dont le paramètre [!UICONTROL Auto Upload] est désactivé, ajoutez manuellement le paramètre aux [paramètres d&#39;ajout au niveau du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, qui l&#39;ajoutent à vos URL de base.

* Lorsque la fonction d’insertion côté serveur n’est pas mise en oeuvre :

   * DSP clients : le [code JavaScript](javascript.md) enregistre automatiquement les clics publicitaires et les affichages publicitaires. Lorsqu’un navigateur ne prend pas en charge les cookies tiers, vous pouvez toujours effectuer le suivi des conversions par clic pour les types d’annonces suivants :

      * Pour [!DNL Flashtalking] balises publicitaires, insérez manuellement des macros supplémentaires par &quot;[Ajouter [!DNL Analytics for Advertising] Macros à [!DNL Flashtalking] Balises publicitaires](/help/integrations/analytics/macros-flashtalking.md)&quot;.

      * Pour [!DNL Google Campaign Manager 360] balises publicitaires, insérez manuellement des macros supplémentaires par &quot;[Ajouter [!DNL Analytics for Advertising] Macros à [!DNL Google Campaign Manager 360] Balises publicitaires](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;.

   * Clients Search, Social et Commerce :

      * Pour les annonces ([!DNL Google Ads] et [!DNL Microsoft Advertising]), ajoutez manuellement le paramètre AMO ID aux suffixes de votre page d’entrée, idéalement au [ niveau du compte ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, sauf si un suivi différent pour les composants de compte individuels est nécessaire.

      * Pour les publicités sur tous les autres réseaux publicitaires, ajoutez manuellement le paramètre AMO ID à vos paramètres d’ajout au niveau du compte [, qui l’ajoutent à vos URL de base.](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}

Pour mettre en oeuvre la fonction d’insertion côté serveur ou déterminer la meilleure option pour votre entreprise, contactez votre équipe de compte d’Adobe.

### Formats AMO ID {#amo-id-formats}

#### Format AMO ID pour [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

où :

* `AC` indique le canal d’affichage.

* `{TM_AD_ID}` est la clé publicitaire alphanumérique générée par l’Adobe Advertising. Il utilise un identifiant unique pour une publicité et sert de clé pour traduire les métadonnées d’entité d’Adobe Advertising en dimensions [!DNL Analytics] lisibles.

* `{TM_PLACEMENT_ID}` est la clé de placement alphanumérique générée par l’Adobe Advertising. Il utilise un identifiant unique pour un emplacement et sert de clé pour traduire les métadonnées d’entité d’Adobe Advertising en dimensions [!DNL Analytics] lisibles.

Exemple d’AMO ID : AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### Formats AMO ID pour les annonces Search, Social &amp; Commerce {#amo-id-format-search}

Les paramètres varient selon le réseau publicitaire, mais les paramètres suivants sont communs à tous :

* `AL` indique le canal de recherche. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` est un identifiant utilisateur unique attribué à l’annonceur.

* `{sid}` est remplacé par l’identifiant numérique du compte réseau publicitaire de l’annonceur : *3* pour [!DNL Google Ads], *10* pour [!DNL Microsoft Advertising], *45* pour [!DNL Meta], *86* pour [!DNL Yahoo! Display Network], *87* pour [!DNL Naver], *88* pour [!DNL Baidu], *90* pour [!DNL Yandex], *94* pour [!DNL Yahoo! Japan Ads], *105* pour [!DNL Yahoo Native] (obsolète) ou *106{2 19} pour [!DNL Pinterest] (obsolète).*

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

où :

* `{creative}` est l’identifiant numérique unique du réseau publicitaire pour le créatif.
* `{placement}` est le site web sur lequel a cliqué la publicité.
* `{keywordid}` est l’identifiant numérique unique du réseau publicitaire pour le mot-clé qui a déclenché la publicité.

##### [!DNL Google Ads]

Cela inclut les campagnes d’achat utilisant [!DNL Google Merchant Center].

* Comptes qui utilisent le dernier format AMO ID, qui prend en charge la création de rapports au niveau des campagnes et des groupes d’annonces pour les campagnes de performances maximales et les campagnes de brouillons et d’expériences :

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Tous les autres comptes :

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

où :

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` est l’identifiant numérique unique [!DNL Google Ads] de l’élément créatif.
* `{matchtype}` est le type de correspondance du mot-clé qui a déclenché la publicité : `e` pour exact, `p` pour expression, ou `b` pour large.
* `{placement}` est le nom de domaine du site web sur lequel a cliqué la publicité. Une valeur est disponible pour les publicités des campagnes ciblées par emplacement et pour les publicités des campagnes ciblées par mot-clé qui s’affichent sur les sites de contenu.
* `{network}` indique le réseau à partir duquel le clic a eu lieu : `g` pour la recherche [!DNL Google] (pour les publicités ciblées par mot-clé uniquement), `s` pour un partenaire de recherche (pour les publicités ciblées par mot-clé uniquement) ou `d` pour le réseau d’affichage (pour les publicités ciblées par mot-clé ou par emplacement).
* `{product_partition_id}` est l’identifiant numérique unique du réseau publicitaire pour le groupe de produits utilisé avec les publicités de produits.
* `{keyword}` est le mot-clé spécifique qui a déclenché votre publicité (sur les sites de recherche) ou le mot-clé correspondant le mieux (sur les sites de contenu).
* `{campaignid}` est l’identifiant numérique unique du réseau publicitaire pour la campagne.
* `{adgroupid}` est l’identifiant numérique unique du réseau publicitaire pour le groupe publicitaire.

>[!NOTE]
>
>* Pour les annonces de recherche dynamique, {keyword} est renseigné avec la cible automatique.
>* Lorsque vous générez le suivi des publicités commerciales [!DNL Google], un paramètre d’ID de produit, `{adwords_producttargetid}`, est inséré avant le paramètre de mot-clé . Le paramètre d’ID de produit n’apparaît pas dans les paramètres de suivi au niveau du compte et au niveau de la campagne [!DNL Google Ads].
>* Pour utiliser le code de suivi AMO ID le plus récent, voir &quot;[Mise à jour du code de suivi AMO ID pour un [!DNL Google Ads] compte](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Rechercher dans les campagnes :

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Campagnes d&#39;achat (utilisant [!DNL Microsoft Merchant Center]) :

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campagnes réseau d’audience :

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

où :

* `{AdId}` est l’identifiant numérique unique du réseau publicitaire pour le créatif.
* `{OrderItemId}` est l’identifiant numérique du réseau publicitaire pour le mot-clé.
* `{CriterionId}` est l’identifiant numérique du réseau publicitaire pour le groupe de produits utilisé avec les publicités de produits.

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

où :

* `{creative}` est l’identifiant numérique unique du réseau publicitaire pour le créatif.
* `{matchtype}` est le type de correspondance du mot-clé qui a déclenché la publicité : `be` pour exact, `bp` pour expression, ou `bb` pour large.
* `{network}` indique le réseau à partir duquel le clic a été effectué : `n` pour native ou `s` pour la recherche.
* `{keyword}` est le mot-clé qui a déclenché votre publicité.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

où :

* `{ad_id}` est l’identifiant numérique unique du réseau publicitaire pour le créatif.
* `{source_type}` est le type de site sur lequel la publicité a été affichée : *b* pour la recherche, *c* pour le contexte (contenu) ou *ct* pour la catégorie.
* `{phrase_id}` est l’identifiant numérique du réseau publicitaire pour le mot-clé.

### DIMENSION AMO ID dans [!DNL Analytics]

Dans les rapports Analytics, vous pouvez rechercher des données AMO ID en recherchant la dimension [!UICONTROL AMO ID] et en utilisant la mesure [!UICONTROL AMO ID Instances]. La dimension [!UICONTROL AMO ID] héberge toutes les valeurs AMO ID capturées, tandis que la mesure [!UICONTROL AMO ID Instances] indique la fréquence de capture d’une valeur AMO ID par le site. Par exemple, si la même publicité de recherche a fait l’objet de quatre clics mais qu’Analytics a suivi sept entrées de site, alors [!UICONTROL AMO ID Instances] aurait sept (7) et [!UICONTROL Clicks] aurait quatre (4).

Pour tout rapport ou audit dans [!DNL Analytics], la bonne pratique consiste à utiliser l’AMO ID avec son instance correspondante. Pour plus d’informations, voir &quot;[Validation des données de clic publicitaire pour [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; dans &quot;Écarts de données attendus entre [!DNL Analytics] et l’Adobe Advertising&quot;.

## À propos des classifications Analytics

Dans [!DNL Analytics], une [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) est un élément de métadonnées pour un code de suivi donné, tel que Compte, Campagne ou Publicité. Adobe Advertising classe les données d’Adobe Advertising brutes à l’aide de classifications afin que vous puissiez afficher les données de différentes manières (par type d’annonce ou campagne, par exemple) lors de la génération des rapports. Les classifications constituent la base des rapports d’Adobe Advertising dans [!DNL Analytics] et peuvent être utilisées avec les mesures AMO, telles que [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] et [!UICONTROL AMO Clicks], ainsi qu’avec les événements personnalisés et standard sur site tels que [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] et [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](data-variances.md)
