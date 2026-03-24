---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---
# ID AMO ADOBE ADVERTISING

## ID AMO ADOBE ADVERTISING {#amo-id}

L’ID AMO suit chaque combinaison publicitaire unique à un niveau moins granulaire et est utilisé pour la classification des données [!DNL Analytics] et Customer Journey Analytics et l’ingestion des mesures publicitaires (telles que les impressions, les clics et les coûts) à partir d’Adobe Advertising.

Par [!DNL Analytics], l’AMO ID est stocké dans une dimension [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=fr) ou rVar (AMO ID).

Pour Customer Journey Analytics, l’ID AMO est stocké dans la propriété `trackingCode` de l’objet `conversionDetails`, qui fait partie de [la [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

L’ID AMO est également appelé `s_kwcid`, ce qui se prononce parfois comme « [!DNL squid] ».

### Formats d’ID AMO {#amo-id-formats}

Consultez la [Formats des éléments de dimension ID AMO](https://experienceleague.adobe.com/fr/docs/analytics/components/dimensions/amo-id#dimension-items) dans le « Guide des composants d’Adobe Analytics ».

<!-- Legacy content:

Notes for GGL Ads: Verify Creative description. Also, are there more networks now (audience and shopping?) Re "To use the latest AMO ID tracking code, see "[Update the AMO ID tracking code for a [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).: Update terminology there too.

Note: ADD IN Meta:

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

BEGIN LEGACY CONTENT:

#### AMO ID format for [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

where:

* `AC` indicates the display channel.

* `{TM_AD_ID}` is the Adobe Advertising-generated alphanumeric ad key. It's used as an unique identifier for an ad and serves as a key for translating Adobe Advertising entity metadata into readable [!DNL Analytics] and Customer Journey Analytics dimensions.

* `{TM_PLACEMENT_ID}` is the Adobe Advertising-generated alphanumeric placement key. It's used as an unique identifier for a placement and serves as a key for translating Adobe Advertising entity metadata into readable [!DNL Analytics] and Customer Journey Analytics dimensions.

Example AMO ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO ID formats for Search, Social, & Commerce ads {#amo-id-format-search}

The parameters vary by ad network, but the following parameters are common to all:

* `AL` indicates the search channel.

* `{userid}` is a unique user ID assigned to the advertiser.

* `{sid}` is replaced by the numeric ID for the advertiser's ad network account: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (deprecated), or *106* for [!DNL Pinterest] (deprecated).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

where:

* `{creative}` is the ad network's unique numeric ID for the creative.
* `{placement}` is the website on which the ad was clicked.
* `{keywordid}` is the ad network's unique numeric ID for the keyword that triggered the ad.

##### [!DNL Google Ads]

These including shopping campaigns using [!DNL Google Merchant Center].

* Accounts that use the latest AMO ID format, which supports campaign- and ad group-level reporting for performance max campaigns and drafts and experiments campaigns:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* All other accounts:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

where:

* `{creative}` is the [!DNL Google Ads] unique numeric ID for the creative.
* `{matchtype}` is the matchtype of the keyword that triggered the ad: `e` for exact, `p` for phrase, or `b` for broad.
* `{placement}` is the domain name of the website on which the ad was clicked. A value is available for ads in placement-targeted campaigns and for ads in keyword-targeted campaigns that are displayed on content sites.
* `{network}` indicates the network from which the click occurred: `g` for [!DNL Google] search (for keyword-targeted ads only), `s` for a search partner (for keyword-targeted ads only), or `d` for the display network (for either keyword-targeted or placement-targeted ads).
* `{product_partition_id}` is the ad network's unique numeric ID for the product group used with product ads.
* `{keyword}` is either the specific keyword that triggered your ad (on search sites) or the best-matching keyword (on content sites).
* `{campaignid}` is the ad network's unique numeric ID for the campaign.
* `{adgroupid}` is the the ad network's unique numeric ID for the ad group.

>[!NOTE]
>
>* For dynamic search ads, {keyword} is populated with the auto target.
>* When you generate tracking for [!DNL Google] shopping ads, a product ID parameter, `{adwords_producttargetid}`, is inserted before the keyword parameter. The product ID parameter doesn't appear in the [!DNL Google Ads] account-level and campaign-level tracking parameters.
>* To use the latest AMO ID tracking code, see "[Update the AMO ID tracking code for a [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)."

##### [!DNL Microsoft Advertising]

* All campaign types:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

where:

* `{AdId}` is the ad network's unique numeric ID for the creative.
* `{OrderItemId}` is the ad network's numeric ID for the keyword.
* `{CampaignId}` is the ad network's unique numeric ID for the campaign.
* `{AdGroupId}` is the ad network's unique numeric ID for the ad group.

>[!NOTE]
>
> For accounts with campaigns without the [!UICONTROL Auto Upload] tracking option that weren't already migrated to the new format, manually update each landing page suffix to include the above format.
>In the meantime, the legacy formats, as follows, still work: 
>* Search campaigns:
>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Shopping campaigns (using [!DNL Microsoft Merchant Center]):
>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Audience network campaigns:
>  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

where:

* `{creative}` is the ad network's unique numeric ID for the creative.
* `{matchtype}` is the matchtype of the keyword that triggered the ad: `be` for exact, `bp` for phrase, or `bb` for broad.
* `{network}` indicates the network from which the click occurred: `n` for native or `s` for search.
* `{keyword}` is the keyword that triggered your ad.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

where:

* `{ad_id}` is the ad network's unique numeric ID for the creative.
* `{source_type}` is the type of site on which the ad has been displayed: *b* for search, *c* for context (content), or *ct* for category.
* `{phrase_id}` is the ad network's numeric ID for the keyword.

-->
