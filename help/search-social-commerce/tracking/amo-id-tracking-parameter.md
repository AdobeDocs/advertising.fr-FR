---
title: Paramètre de suivi AMO ID (s_kwcid)
description: Découvrez le paramètre de suivi utilisé pour partager des données d’Adobe Advertising avec Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Paramètre de suivi AMO ID (s_kwcid)

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe Advertising partage des données sur vos campagnes avec Adobe Analytics à l’aide du paramètre d’ajout AMO ID, également appelé `s_kwcid` qui se compose d’éléments spécifiques au canal publicitaire et au réseau publicitaire.

<!-- add everything below to IDs page -->

Le paramètre est ajouté à vos URL de suivi de l’une des manières suivantes :

* (Recommandé) La fonction d’insertion côté serveur est mise en oeuvre.

  Pour [!DNL Google Ads] et [!DNL Microsoft Advertising] compte avec la variable [!UICONTROL Auto Upload] activée pour le compte ou la campagne, le serveur de pixels ajoute automatiquement le paramètre AMO ID aux suffixes de votre landing page lorsqu’un utilisateur clique sur une publicité <!-- click a search ad or views a display ad --> avec le pixel d’Adobe Advertising.

  Pour d’autres réseaux publicitaires, ou [!DNL Google Ads] et [!DNL Microsoft Advertising] compte avec la variable [!UICONTROL Auto Upload] désactivé, ajoutez manuellement le paramètre AMO ID aux paramètres d’ajout au niveau du compte, qui l’ajoutent à vos URL de base.

* <!-- (Search, Social, & Commerce only) -->La fonction d’insertion côté serveur n’est pas mise en oeuvre et vous devez ajouter manuellement le paramètre AMO ID à votre[!DNL Google Ads] et [!DNL Microsoft Advertising]) suffixes de page d’entrée ou paramètres d’ajout au niveau du compte au niveau du compte (autres réseaux publicitaires).

Pour mettre en oeuvre la fonction d’insertion côté serveur ou déterminer la meilleure option pour votre entreprise, contactez votre équipe de compte d’Adobe.

## Format AMO ID pour les annonces publicitaires DSP

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

où :

* `AC` indique le canal d’affichage.

* `{TM_AD_ID}` est la clé publicitaire alphanumérique.

* `{TM_PLACEMENT_ID}` est la clé d’emplacement alphanumérique.

## Formats AMO ID pour les annonces Search, Social &amp; Commerce

Les paramètres varient selon le réseau publicitaire, mais les paramètres suivants sont communs à tous :

* `AL` indique le canal de recherche. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` est un identifiant utilisateur unique attribué à l’annonceur.

* `{sid}` est remplacé par l’identifiant numérique du compte réseau publicitaire de l’annonceur : *3* pour [!DNL Google Ads], *10* pour [!DNL Microsoft Advertising], *45* pour [!DNL Meta], *86* pour [!DNL Yahoo! Display Network], *87* pour [!DNL Naver], *88* pour [!DNL Baidu], *90* pour [!DNL Yandex], *94* pour [!DNL Yahoo! Japan Ads], *105* pour [!DNL Yahoo Native] (obsolète) ou *106* pour [!DNL Pinterest] (obsolète).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Il s’agit notamment des campagnes d’achat utilisant des [!DNL Google Merchant Center].

* Comptes qui utilisent le dernier format AMO ID, qui prend en charge la création de rapports au niveau des campagnes et des groupes d’annonces pour les campagnes de performances maximales et les campagnes de brouillons et d’expériences :

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Tous les autres comptes :

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* Pour les annonces de recherche dynamique, {keyword} est renseignée avec la cible automatique.
>* Lorsque vous générez le suivi pour [!DNL Google] publicités commerciales, un paramètre d’ID de produit, `{adwords_producttargetid}`, est inséré avant le paramètre de mot-clé . Le paramètre d’ID de produit n’apparaît pas dans la variable [!DNL Google Ads] paramètres de suivi au niveau du compte et de la campagne.
>* Pour utiliser le code de suivi AMO ID le plus récent, voir &quot;[Mettre à jour le code de suivi AMO ID pour un [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* Rechercher dans les campagnes :

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Campagnes d’achat (à l’aide de [!DNL Microsoft Merchant Center]) :

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campagnes réseau d’audience :

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Gestion des comptes de réseau publicitaire](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Paramètres de campagne Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Paramètres de campagne Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Paramètres de campagne Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo ! Paramètres de campagne Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Paramètres de campagne Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
