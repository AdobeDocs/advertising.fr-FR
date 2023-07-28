---
title: Mise en oeuvre [!DNL Microsoft® Advertising] campagnes d'achat
description: En savoir plus sur le workflow de configuration [!DNL Microsoft® Advertising] campagnes d’achat.
exl-id: 3fb19b92-5bc0-414e-9234-68310082d0ed
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Mise en oeuvre [!DNL Microsoft® Advertising] campagnes d&#39;achat

Les publicités dans les campagnes d’achat utilisent des données sur les produits de votre [!DNL Microsoft® Merchant Center] flux produit, au lieu de mots-clés, pour décider comment et où afficher vos publicités.

[!DNL Microsoft®] les campagnes d’achat ciblent [!DNL Microsoft® Advertising Shopping Network]. Les paramètres des campagnes d’achat incluent un pays spécifié dans lequel les produits sont vendus et une priorité ([!DNL High], [!DNL Medium], ou [!DNL Low]). Vous pouvez éventuellement filtrer votre inventaire pour faire la publicité de produits avec des attributs spécifiques, et cibler ou exclure des emplacements et des types d’appareils spécifiques.

Vous pouvez contrôler les produits affichés avec vos publicités commerciales en configurant des publicités à plusieurs niveaux. *[groupes de produits](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* au niveau du groupe publicitaire. Les groupes de produits sont basés sur n’importe quel attribut de produit (catégorie, type de produit, marque, condition, ID de produit et étiquettes personnalisées), et vous pouvez créer jusqu’à sept niveaux de groupes de produits à inclure ou exclure de l’offre, à l’exclusion de &quot;&quot;[!DNL Add Products].&quot; Vous pouvez définir des offres au plus bas niveau des groupes de produits, en utilisant la même offre pour tous les produits correspondants. Si le même produit est inclus dans plusieurs campagnes, [!DNL Microsoft® Advertising] utilise d’abord la priorité au niveau de la campagne pour déterminer la campagne (et l’offre associée) éligible aux enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible.

## Étapes de configuration [!DNL Microsoft® Advertising] campagnes d&#39;achat

Vous pouvez configurer des campagnes d’achat à l’aide de [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) pour [!DNL Microsoft® Advertising], en utilisant [bulles](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)ou individuellement. Les instructions suivantes comprennent des liens vers la création d’entités individuelles.

1. Configurez vos [!DNL Microsoft® Merchant Center] et le renseigner avec des données de produit.

1. [Autoriser Search, Social et Commerce à télécharger les données à partir de la variable [!DNL Microsoft® Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Créer une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sur le réseau commercial.

1. [Création d’un groupe d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dans la campagne, puis définissez l’offre par défaut pour toutes les publicités.

Vous pouvez remplacer l’offre par défaut pour des groupes de produits individuels.

1. Créez des groupes de produits pour le groupe publicitaire :

   1. [Créer un groupe de produits &quot;Tous les produits&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facultatif) [Création de groupes de produits enfants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Créer [publicités de produits](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) avec [lignes de promotion à inclure potentiellement dans chaque publicité d’achat](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) dans le groupe publicitaire.

      Microsoft® Advertising génère dynamiquement la copie de publicité et l’URL de la page d’entrée pour chaque publicité.

      >[!NOTE]
      >
      >Même si le groupe publicitaire n’inclut pas d’entités publicitaires, [!DNL Microsoft® Advertising] affiche toujours des publicités pour les produits.

1. (Facultatif) Pour effectuer le suivi des clics sur la publicité, [générer une URL de suivi à l’aide de l’outil URL de suivi ;](/help/search-social-commerce/tools/click-tracking-url-generate.md). Il est recommandé d’ajouter l’URL de suivi à la variable [!UICONTROL Tracking Template] dans les paramètres du compte, de la campagne ou du groupe de produits. Pour simplifier la maintenance, ajoutez-la au niveau le plus élevé possible.

   Vous pouvez également ajouter l’URL de suivi aux données de produit dans la variable [!DNL Microsoft® Merchant Center] compte . Pour ce faire, incluez l’URL de tracking, ainsi que la valeur du champ &quot;link&quot; ou &quot;mobile_link&quot;, le cas échéant, dans une colonne personnalisée &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; dans le flux de produit. La valeur du champ &quot;bingads_redirect&quot; remplace les valeurs des champs &quot;link&quot; et &quot;mobile_link&quot;. Les URL générées à l’aide de cette méthode n’incluent aucun paramètre de suivi spécifié dans les paramètres de compte ou de campagne de recherche, de Social et de Commerce.

1. Surveillez les performances en [la génération de la [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Selon les besoins :

   1. [Modifier les paramètres de l&#39;opération](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour ajuster le budget de l&#39;opération.

      Si la campagne fait partie d’un portfolio, le paramètre de portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permet à Search, Social et Commerce d’optimiser les budgets pour toutes les campagnes du portefeuille.

   1. Ajustez l’offre maximale pour les groupes de produits existants, supprimez les groupes de produits pour lesquels vous ne souhaitez plus créer d’annonces, ou ajoutez un nouveau groupe de produits &quot;tous les produits&quot; ou de nouveaux groupes de produits enfants afin de créer des annonces pour les produits supplémentaires.

>[!NOTE]
>
>* Voir les champs requis pour la gestion [!DNL Microsoft® Shopping] campagnes et groupes de produits utilisant [bulles](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) et [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Pour plus d’informations sur [!DNL Microsoft® Shopping] campagnes, voir [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/50903).
