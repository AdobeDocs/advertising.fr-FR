---
title: '[!DNL Yandex] des paramètres de la campagne'
description: Référencez les paramètres des campagnes  [!DNL Yandex] .
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# [!DNL Yandex] des paramètres de la campagne

## \[Haut de la page]

**[!UICONTROL Campaign Name]:** nom de campagne unique au sein du compte.

**[!UICONTROL Status]:** statut d’affichage de la campagne : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Active*.

## onglet [!UICONTROL Basic Settings]

*Nouvelles campagnes uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte de réseau publicitaire.

**[!UICONTROL Campaign Type]:** Où placer des annonces :

* *[!UICONTROL Search Network Only]:* affiche les annonces publicitaires textuelles sur le réseau de recherche. Vous devez spécifier des mots-clés pour chaque groupe publicitaire.

* *[!UICONTROL Search and Display Network]:* affiche des annonces publicitaires textuelles sur le réseau de recherche et le [!DNL Yandex Advertising Network]. Pour les annonces de recherche, vous devez spécifier des mots-clés de recherche pour chaque groupe d’annonces. Pour les publicités display, vous devez spécifier des mots-clés pour les sites web sur lesquels vous souhaitez diffuser des publicités pour chaque groupe publicitaire.

* *[!UICONTROL Display Network Only]:* affiche les annonces publicitaires textuelles sur le [!DNL Yandex Advertising Network]. Pour chaque groupe publicitaire, vous devez spécifier des mots-clés pour les sites web sur lesquels vous souhaitez faire de la publicité.

## onglet [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

## onglet [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** budget, qui correspond au montant que vous souhaitez dépenser quotidiennement (en moyenne) ou pendant la durée de vie de la campagne, en fonction du type de budget du compte. Le budget minimum est de 6 300 €, 10 € ou 10 USD.

**Remarques :**

* Les nouvelles campagnes ont la stratégie de gestion des enchères « Position la plus élevée disponible ».

* Selon les conditions de recherche, si vous affectez cette campagne à un portefeuille configuré pour permettre l’ajustement automatique des limites budgétaires de la campagne, vous pouvez dépenser plus ou moins que le budget spécifié un jour, un mois ou une durée de vie donnés.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## onglet [!UICONTROL Additional Campaign Information]

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (Pour [!UICONTROL EF Redirect] uniquement ; lecture seule) Niveau auquel les clics et le chiffre d’affaires doivent être suivis. Seule la *[!UICONTROL Creative]* est disponible pour les [!DNL Yandex] ; les données sont suivies au niveau de la publicité (contenu publicitaire) uniquement.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [Gérer les campagnes](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
