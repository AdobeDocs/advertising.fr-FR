---
title: Implémenter  [!DNL Google Ads]  campagnes d’achat
description: Découvrez le workflow de configuration  [!DNL Google Ads]  campagnes d’achat.
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/9xk2sCRBNJdRI1az99RyUkAlL-8P9s3OD70Htmnt4r8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# Implémenter des campagnes d’achats [!DNL Google Ads]

Les publicités des campagnes d’achat utilisent les données sur les produits de votre flux de produits [!DNL Google Merchant Center] existant, plutôt que des mots-clés, pour décider comment et où afficher vos publicités.

[!DNL Google Ads] campagnes peuvent cibler les [!DNL Google Shopping Network] à l’aide de la [!UICONTROL Campaign Type] « [!UICONTROL Shopping Network] ». Les paramètres des campagnes [!DNL Google Shopping] incluent une priorité ([!UICONTROL High], [!UICONTROL Medium] ou [!UICONTROL Low]). Vous pouvez éventuellement afficher vos informations d’inventaire local dans vos annonces d’achats à l’aide d’un paramètre au niveau de la campagne.

Vous pouvez contrôler les produits qui s’affichent avec vos annonces d’achats en configurant des *[groupes de produits](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* à plusieurs niveaux au niveau du groupe publicitaire. Les groupes de produits sont basés sur n’importe quel attribut de produit (catégorie, type de produit, marque, condition, ID de produit et libellés personnalisés) et vous pouvez créer jusqu’à sept niveaux de groupes de produits à inclure ou à exclure des enchères. Vous pouvez définir des enchères au niveau le plus bas des groupes de produits, en utilisant la même enchère pour tous les produits correspondants. Lorsque le même produit est inclus dans plusieurs campagnes, [!DNL Google Ads] utilise d’abord la priorité au niveau de la campagne pour déterminer la campagne (et l’enchère associée) éligible pour les enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, celle qui a reçu la meilleure enchère est éligible.

## Étapes de configuration des campagnes d’achats [!DNL Google Ads]

Vous pouvez configurer des campagnes d’achat à l’aide de [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) par [!DNL Google Shopping], à l’aide de [feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) ou individuellement. Les instructions suivantes incluent des liens vers la création d’entités individuelles.

1. Configurez votre compte [!DNL Google Merchant Center] et renseignez-le avec des données de produit.

1. [Autoriser Search, Social et Commerce à télécharger des données à partir du compte  [!DNL Google Merchant Center] ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Créez une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sur le réseau d’achats.

1. [Créez un groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dans la campagne, puis définissez l’enchère par défaut pour toutes les publicités.

   Vous pouvez remplacer l&#39;enchère par défaut pour des groupes de produits individuels.

1. Créez des groupes de produits pour le groupe publicitaire :

   1. [Créez un groupe de produits « Tous les produits »](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facultatif) [Créer des groupes de produits enfants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Vous n’avez pas besoin de créer des annonces d’achats. Même si le groupe publicitaire n’inclut pas les entités publicitaires, [!DNL Google Ads] affiche toujours des annonces pour les produits.

1. (Facultatif) Pour suivre les clics sur l’annonce publicitaire, [générez une URL de tracking à l’aide de l’outil URL de tracking](/help/search-social-commerce/tools/click-tracking-url-generate.md), puis ajoutez-la aux paramètres du compte, de la campagne ou du groupe de produits.

1. Surveillez les performances en [générant le [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) et [le [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Au besoin :

   1. [Modifiez les paramètres de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour ajuster le budget de la campagne.

      Si la campagne fait partie d’un portfolio, le paramètre de portfolio « [!UICONTROL Auto adjust campaign budget limits] » permet à Search, Social et Commerce d’optimiser les budgets de toutes les campagnes du portfolio.

   1. [Ajustez l’enchère maximale pour les groupes de produits existants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [supprimez les groupes de produits](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) pour lesquels vous ne souhaitez plus créer d’annonces, ou ajoutez un [nouveau groupe de produits « tous les produits »](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) ou [nouveau groupe de produits enfant](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) pour créer des annonces pour des produits supplémentaires.

>[!NOTE]
>
>* Consultez les champs requis pour gérer des campagnes [!DNL Google Shopping] et des groupes de produits à l’aide de [feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) et [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Pour plus d’informations sur les campagnes [!DNL Google Shopping], consultez la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2454022).
