---
title: Implémentation de campagnes d'achats  [!DNL Google Ads]
description: Découvrez le workflow de configuration des campagnes d'achats  [!DNL Google Ads] .
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Mise en oeuvre de campagnes d’achat [!DNL Google Ads]

Dans les campagnes d’achat, les publicités utilisent des données sur les produits de votre flux de produits [!DNL Google Merchant Center] existant, plutôt que des mots-clés, pour décider comment et où afficher vos publicités.

Les campagnes [!DNL Google Ads] peuvent cibler le [!DNL Google Shopping Network] à l’aide de [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network]&quot;. Les paramètres des campagnes [!DNL Google Shopping] incluent une priorité ([!UICONTROL High], [!UICONTROL Medium] ou [!UICONTROL Low]). Vous pouvez éventuellement afficher les informations de stock local dans vos publicités commerciales à l’aide d’un paramètre au niveau de la campagne.

Vous pouvez contrôler les produits affichés avec vos publicités commerciales en configurant des *[groupes de produits](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* à plusieurs niveaux au niveau des groupes d’annonces. Les groupes de produits sont basés sur n’importe quel attribut de produit (catégorie, type de produit, marque, condition, ID de produit et étiquettes personnalisées). Vous pouvez créer jusqu’à sept niveaux de groupes de produits à inclure ou exclure de l’offre. Vous pouvez définir des offres au plus bas niveau des groupes de produits, en utilisant la même offre pour tous les produits correspondants. Lorsque le même produit est inclus dans plusieurs campagnes, [!DNL Google Ads] utilise d’abord la priorité au niveau de la campagne pour déterminer la campagne (et l’offre associée) éligible à l’enchère publicitaire. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible.

## Étapes de configuration des campagnes d’achat [!DNL Google Ads]

Vous pouvez configurer des campagnes d’achat à l’aide des [ modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) pour [!DNL Google Shopping], à l’aide des [ feuilles d’envoi groupées](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) ou individuellement. Les instructions suivantes comprennent des liens vers la création d’entités individuelles.

1. Configurez votre compte [!DNL Google Merchant Center] et renseignez-le avec les données de produit.

1. [ Autoriser la recherche, Social et Commerce à télécharger les données du  [!DNL Google Merchant Center] compte](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Créez une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sur le réseau d’achat.

1. [Créez un groupe d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dans la campagne et définissez l’offre par défaut pour toutes les publicités.

   Vous pouvez remplacer l’offre par défaut pour des groupes de produits individuels.

1. Créez des groupes de produits pour le groupe publicitaire :

   1. [Créez un groupe de produits &quot;Tous les produits&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facultatif) [Créez des groupes de produits enfants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Vous n’avez pas besoin de créer des publicités commerciales. Même si le groupe publicitaire n’inclut pas d’entités publicitaires, [!DNL Google Ads] affiche toujours des publicités pour les produits.

1. (Facultatif) Pour effectuer le suivi des clics sur la publicité, [générez une URL de suivi à l’aide de l’outil URL de suivi](/help/search-social-commerce/tools/click-tracking-url-generate.md), puis ajoutez-la aux paramètres du compte, de la campagne ou du groupe de produits.

1. Surveillez les performances en [générant les [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) et [ [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Selon les besoins :

   1. [Modifiez les paramètres de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour ajuster le budget de la campagne.

      Si la campagne fait partie d’un portfolio, le paramètre de portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permet à Search, Social et Commerce d’optimiser les budgets pour toutes les campagnes du portfolio.

   1. [Ajustez l&#39;offre maximale pour les groupes de produits existants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [supprimez les groupes de produits](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) pour lesquels vous ne souhaitez plus créer d&#39;annonces, ou ajoutez un [nouveau groupe de produits &quot;tous les produits&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) ou [nouveaux groupes de produits enfants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) pour créer des annonces pour des produits supplémentaires.

>[!NOTE]
>
>* Voir les champs requis pour la gestion des [!DNL Google Shopping] campagnes et groupes de produits à l’aide des [feuilles d’envoi groupées](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) et des [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Pour plus d&#39;informations sur les campagnes [!DNL Google Shopping], consultez la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2454022).
