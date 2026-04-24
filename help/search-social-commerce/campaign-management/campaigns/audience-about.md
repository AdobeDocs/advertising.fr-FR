---
title: À propos des audiences
description: Découvrez les options de suivi, de création et de gestion  [!DNL Google Ads]  audiences et  [!DNL Microsoft Advertising]  audiences.
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/B77S28vEpSkrgNmhc-Ekn7PXh3W-y2g9et2y3gCQPK8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 0%

---

# À propos de la gestion des audiences [!DNL Google Ads] et [!DNL Microsoft Advertising] dans Search, Social et Commerce

*[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

The Audiences Library lists all of your [!DNL Google Ads] customer data-based, in-market, and similar audiences and your [!DNL Microsoft Advertising] remarketing and dynamic remarketing, custom, customer match, in-market, and similar audiences. Vous pouvez utiliser n’importe laquelle des audiences [!DNL Google Ads] comme cibles et exclusions [!DNL Google Ads] niveau de la campagne et du groupe publicitaire, et vous pouvez utiliser n’importe laquelle des audiences [!DNL Microsoft Advertising] comme cibles [!DNL Microsoft Advertising] niveau de la campagne et du groupe publicitaire et exclusions (audiences de remarketing dynamique uniquement). Vous pouvez ajouter ou modifier un ajustement d’enchère pour n’importe quelle cible d’audience.

Vous pouvez également créer et gérer des audiences à l’aide de segments ou de listes d’adresses électroniques issues de vos audiences Adobe CX Enterprise existantes et de différents types de données client provenant de votre système de gestion de la relation client (GRC) :

* **Adobe audience segments:** Advertisers with opted-in Adobe Audience Manager or Adobe Analytics accounts can create [!DNL Google Ads] customer match audiences from their [!DNL Adobe] segments:

   * (Advertisers with [!DNL Analytics] accounts who don&#39;t also have Audience Manager) You can create [!DNL Google Ads] customer match audiences using user IDs from [!DNL Analytics] segments that are shared with Adobe CX Enterprise.

   * (Advertisers with Audience Manager accounts) You can create [!DNL Google Ads] customer match audiences using user IDs from Audience Manager segments that have Search, Social, &amp; Commerce as a destination. This may include Adobe Analytics segments that are published to Adobe CX Enterprise and segments created using the Adobe CX Enterprise Audience Library.

  To create customer match audiences, the advertiser&#39;s [!DNL Google Ads] account must be [eligible for custom match](https://support.google.com/adspolicy/answer/6299717) and opted in for [user ID segments](https://support.google.com/google-ads/answer/9199250). Also, the advertiser account in Search, Social, &amp; Commerce must be configured to allow the creation of customer match audiences.

  [!DNL Adobe] données de segment et les fichiers de synchronisation des cookies pour les audiences basées sur les données client sont synchronisés sur [!DNL Google Ads] quotidiennement.

* **Adobe Campaign email lists:** Your Adobe Account Team can help you set up a workflow to create and update a [!DNL Google Ads] customer match audience from an email list within [!DNL Campaign].

* **Customer data lists:** Advertisers with [!DNL Google Ads] or [!DNL Microsoft Advertising] accounts that are eligible for customer match can create and update an ad network-specific customer data-based audience &lt;!-- or dynamic remarketing audience -- included in customer data-based audience, at least for [!DNL Google Ads]?--> by uploading a CSV file with primary identifiers.

* **Listes de remarketing dynamique :** les annonceurs disposant de comptes [!DNL Microsoft Advertising] peuvent créer et gérer des audiences de remarketing dynamique, que vous pouvez utiliser pour recibler les clients potentiels qui ont récemment interagi avec vos produits de l’une des multiples façons (comme les visiteurs de produits ou les acheteurs précédents). Dynamic remarketing audiences require you to use the ad network&#39;s JavaScript conversion- and audience-tracking tag on your webpages. Use dynamic remarketing lists with shopping campaigns on the search and audience networks to retarget audiences with product ads, as well as with search campaigns to retarget audiences with text ads and dynamic search ads. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Bid modifiers for dynamic remarketing audience targets aren&#39;t optimized in portfolios with the &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot; setting.

>[!NOTE]
>
>Search, Social, &amp; Commerce doesn&#39;t store any of the customer data you upload or from the [!DNL Adobe] segments used to create or edit a [!DNL Google Ads] or [!DNL Microsoft Advertising] audience.

>[!MORELIKETHIS]
>
>* [Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Création d’une audience  [!DNL Google Ads]  correspondance client à partir d’une liste d’emails Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gérer les audiences de correspondance de clients à l’aide de listes de données client](audience-from-customer-data-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
>* [Gérer les cibles d’audience pour les campagnes et les groupes publicitaires](audience-targets-manage.md)
>* [Gérer les exclusions d’audience pour les campagnes et les groupes publicitaires](audience-exclusions-manage.md)
