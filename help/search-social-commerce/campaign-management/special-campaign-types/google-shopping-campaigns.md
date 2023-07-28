---
title: Mise en oeuvre [!DNL Google Ads] campagnes d'achat
description: En savoir plus sur le workflow de configuration [!DNL Google Ads] campagnes d’achat.
exl-id: aab61d94-861f-4072-b044-f9ae6759e028
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Mise en oeuvre [!DNL Google Ads] campagnes d&#39;achat

Les publicités dans les campagnes d’achat utilisent des données sur les produits de votre [!DNL Google Merchant Center] flux produit, au lieu de mots-clés, pour décider comment et où afficher vos publicités.

[!DNL Google Ads] les campagnes peuvent cibler la variable [!DNL Google Shopping Network] en utilisant la variable [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; Les paramètres de [!DNL Google Shopping] les campagnes incluent une priorité ([!UICONTROL High], [!UICONTROL Medium], ou [!UICONTROL Low]). Vous pouvez éventuellement afficher les informations de stock local dans vos publicités commerciales à l’aide d’un paramètre au niveau de la campagne.

Vous pouvez contrôler les produits affichés avec vos publicités commerciales en configurant des publicités à plusieurs niveaux. *[groupes de produits](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* au niveau du groupe publicitaire. Les groupes de produits sont basés sur n’importe quel attribut de produit (catégorie, type de produit, marque, condition, ID de produit et étiquettes personnalisées). Vous pouvez créer jusqu’à sept niveaux de groupes de produits à inclure ou exclure de l’offre. Vous pouvez définir des offres au plus bas niveau des groupes de produits, en utilisant la même offre pour tous les produits correspondants. Si le même produit est inclus dans plusieurs campagnes, [!DNL Google Ads] utilise d’abord la priorité au niveau de la campagne pour déterminer la campagne (et l’offre associée) éligible aux enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible.

## Étapes de configuration [!DNL Google Ads] campagnes d&#39;achat

Vous pouvez configurer des campagnes d’achat à l’aide de [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) pour [!DNL Google Shopping], en utilisant [bulles](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)ou individuellement. Les instructions suivantes comprennent des liens vers la création d’entités individuelles.

1. Configurez vos [!DNL Google Merchant Center] et le renseigner avec des données de produit.

1. [Autoriser Search, Social et Commerce à télécharger les données à partir de la variable [!DNL Google Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Créer une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sur le réseau commercial.

1. [Création d’un groupe d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dans la campagne, puis définissez l’offre par défaut pour toutes les publicités.

Vous pouvez remplacer l’offre par défaut pour des groupes de produits individuels.

1. Créez des groupes de produits pour le groupe publicitaire :

   1. [Créer un groupe de produits &quot;Tous les produits&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facultatif) [Création de groupes de produits enfants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Vous n’avez pas besoin de créer des publicités commerciales. Même si le groupe publicitaire n’inclut pas d’entités publicitaires, [!DNL Google Ads] affiche toujours des publicités pour les produits.

1. (Facultatif) Pour effectuer le suivi des clics sur la publicité, [générer une URL de suivi à l’aide de l’outil URL de suivi ;](/help/search-social-commerce/tools/click-tracking-url-generate.md), puis ajoutez-le aux paramètres du compte, de la campagne ou du groupe de produits.

1. Surveillez les performances en [la génération de la [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) et [la valeur [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Selon les besoins :

   1. [Modifier les paramètres de l&#39;opération](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour ajuster le budget de l&#39;opération.

      Si la campagne fait partie d’un portfolio, le paramètre de portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permet à Search, Social et Commerce d’optimiser les budgets pour toutes les campagnes du portefeuille.

   1. [Ajuster l’offre maximale pour les groupes de produits existants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [supprimer des groupes de produits ;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) pour lequel vous ne souhaitez plus créer de publicités ou ajouter une [nouveau groupe de produits &quot;tous produits&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) ou [nouveaux groupes de produits enfants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) pour créer des publicités pour des produits supplémentaires.

>[!NOTE]
>
>* Voir les champs requis pour la gestion [!DNL Google Shopping] campagnes et groupes de produits utilisant [bulles](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) et [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Pour plus d’informations sur [!DNL Google Shopping] campagnes, voir [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2454022).
