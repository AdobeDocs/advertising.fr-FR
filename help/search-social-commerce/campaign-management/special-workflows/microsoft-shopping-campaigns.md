---
title: Implémenter  [!DNL Microsoft Advertising]  campagnes d’achat
description: Découvrez le workflow de configuration  [!DNL Microsoft Advertising]  campagnes d’achat.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/2SXWaNmPPcXmljB2DUKq9DNWgPv9Qb-0t3SJcdO6aR8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 587
ht-degree: 0%

---

# Implémenter des campagnes d’achats [!DNL Microsoft Advertising]

Les publicités des campagnes d’achat utilisent les données sur les produits de votre flux de produits [!DNL Microsoft Merchant Center] existant, plutôt que des mots-clés, pour décider comment et où afficher vos publicités.

[!DNL Microsoft] campagnes d’achat ciblent le [!DNL Microsoft Advertising Shopping Network]. Les paramètres des campagnes d’achat incluent un pays spécifié dans lequel les produits sont vendus et une priorité ([!DNL High], [!DNL Medium] ou [!DNL Low]). Vous pouvez éventuellement filtrer votre inventaire pour faire la publicité de produits avec des attributs spécifiques et cibler ou exclure des emplacements et des types d’appareils spécifiques.

Vous pouvez contrôler les produits qui s’affichent avec vos annonces d’achats en configurant des *[groupes de produits](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* à plusieurs niveaux au niveau du groupe publicitaire. Les groupes de produits sont basés sur n’importe quel attribut de produit (catégorie, type de produit, marque, condition, ID de produit et libellés personnalisés). Vous pouvez créer jusqu’à sept niveaux de groupes de produits à inclure ou à exclure des enchères, y compris « [!DNL Add Products] ». Vous pouvez définir des enchères au niveau le plus bas des groupes de produits, en utilisant la même enchère pour tous les produits correspondants. Lorsque le même produit est inclus dans plusieurs campagnes, [!DNL Microsoft Advertising] utilise d’abord la priorité au niveau de la campagne pour déterminer la campagne (et l’enchère associée) éligible pour les enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, celle qui a reçu la meilleure enchère est éligible.

## Étapes de configuration des campagnes d’achats [!DNL Microsoft Advertising]

Vous pouvez configurer des campagnes d’achat à l’aide de [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) par [!DNL Microsoft Advertising], à l’aide de [feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) ou individuellement. Les instructions suivantes incluent des liens vers la création d’entités individuelles.

1. Configurez votre compte [!DNL Microsoft Merchant Center] et renseignez-le avec des données de produit.

1. [Autoriser Search, Social et Commerce à télécharger des données à partir du compte  [!DNL Microsoft Merchant Center] &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Créez une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sur le réseau d’achats.

1. [Créez un groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dans la campagne, puis définissez l’enchère par défaut pour toutes les publicités.

   Vous pouvez remplacer l&#39;enchère par défaut pour des groupes de produits individuels.

1. Créez des groupes de produits pour le groupe publicitaire :

   1. [Créez un groupe de produits « Tous les produits »](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facultatif) [Créer des groupes de produits enfants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Créez des [annonces de produits](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) avec des [lignes de promotion à inclure éventuellement dans chaque annonce publicitaire](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) au sein du groupe publicitaire.

      Microsoft Advertising génère dynamiquement la copie de la publicité et l’URL de la page de destination pour chaque publicité.

      >[!NOTE]
      >
      >Même si le groupe publicitaire n’inclut pas les entités publicitaires, [!DNL Microsoft Advertising] affiche toujours des annonces pour les produits.

1. (Facultatif) Pour suivre les clics sur l’annonce publicitaire, [générez une URL de tracking à l’aide de l’outil URL de tracking](/help/search-social-commerce/tools/click-tracking-url-generate.md). La bonne pratique consiste à ajouter l’URL de tracking au champ [!UICONTROL Tracking Template] dans les paramètres du compte, de la campagne ou du groupe de produits. Pour faciliter la maintenance, ajoutez-la au niveau le plus élevé possible.

   Vous pouvez également ajouter l’URL de suivi aux données de produit dans le compte [!DNL Microsoft Merchant Center]. Pour ce faire, incluez l’URL de tracking, ainsi que la valeur dans le champ « link » ou « mobile_link », selon le cas, dans une colonne personnalisée « [bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084) » dans le flux de produits. La valeur du champ « bingads_redirect » remplace les valeurs des champs « link » et « mobile_link ». Les URL générées à l’aide de cette méthode n’incluent aucun paramètre de tracking spécifié dans les paramètres du compte Search, Social et Commerce ou de la campagne.

1. Surveillez les performances en [générant le [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)).

1. Au besoin :

   1. [Modifiez les paramètres de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour ajuster le budget de la campagne.

      Si la campagne fait partie d’un portfolio, le paramètre de portfolio « [!UICONTROL Auto adjust campaign budget limits] » permet à Search, Social et Commerce d’optimiser les budgets de toutes les campagnes du portfolio.

   1. Ajustez l’enchère maximale pour les groupes de produits existants, supprimez les groupes de produits pour lesquels vous ne souhaitez plus créer d’annonces ou ajoutez un nouveau groupe de produits « tous les produits » ou de nouveaux groupes de produits enfants pour créer des annonces pour des produits supplémentaires.

>[!NOTE]
>
>* Consultez les champs requis pour gérer des campagnes [!DNL Microsoft Shopping] et des groupes de produits à l’aide de [feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) et [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Pour plus d’informations sur les campagnes [!DNL Microsoft Shopping], consultez la [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/50903).
