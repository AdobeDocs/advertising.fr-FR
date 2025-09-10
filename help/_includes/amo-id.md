---
source-git-commit: 2b719e00418010b1f8e21b8956ad55b2ffc7dee1
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---
# ID AMO ADOBE ADVERTISING

## ID AMO ADOBE ADVERTISING {#amo-id}

L’ID AMO suit chaque combinaison publicitaire unique à un niveau moins granulaire et est utilisé pour la classification des données [!DNL Analytics] et Customer Journey Analytics et l’ingestion des mesures publicitaires (telles que les impressions, les clics et les coûts) à partir d’Adobe Advertising.

Par [!DNL Analytics], l’AMO ID est stocké dans une dimension [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (AMO ID).

Pour Customer Journey Analytics, l’ID AMO est stocké dans la propriété `trackingCode` de l’objet `conversionDetails`, qui fait partie du [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] .

L’ID AMO est également appelé `s_kwcid`, ce qui se prononce parfois comme « [!DNL squid] ».

### AMO - Formats d&#39;ID {#amo-id-formats}

#### AMO - Format d&#39;ID pour [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

où :

* `AC` indique le canal d’affichage.

* `{TM_AD_ID}` est la clé de publicité alphanumérique générée par Adobe Advertising. Il s’agit d’un identifiant unique pour une publicité et sert de clé pour traduire les métadonnées des entités Adobe Advertising en dimensions [!DNL Analytics] et Customer Journey Analytics lisibles.

* `{TM_PLACEMENT_ID}` est la clé d’emplacement alphanumérique générée par Adobe Advertising. Il s’agit d’un identifiant unique pour un emplacement et sert de clé pour traduire les métadonnées des entités Adobe Advertising en dimensions [!DNL Analytics] et Customer Journey Analytics lisibles.

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
> >En attendant, les formats hérités, comme suit, fonctionnent toujours :
>* Campagnes de recherche :
>  >  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Campagnes d’achat (à l’aide de [!DNL Microsoft Merchant Center]) :
>  >  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campagnes réseau d’audience :
>  >  `s_kwcid=AL!{userid}!10!{AdId}`

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
