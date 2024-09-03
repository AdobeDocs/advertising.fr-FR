---
title: Implémentation de campagnes d'achats  [!DNL Microsoft Advertising]
description: Découvrez le workflow de configuration des campagnes d'achats  [!DNL Microsoft Advertising] .
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Mise en oeuvre de campagnes d’achat [!DNL Microsoft Advertising]

Dans les campagnes d’achat, les publicités utilisent des données sur les produits de votre flux de produits [!DNL Microsoft Merchant Center] existant, plutôt que des mots-clés, pour décider comment et où afficher vos publicités.

[!DNL Microsoft] campagnes d’achats ciblant [!DNL Microsoft Advertising Shopping Network]. Les paramètres des campagnes d’achat incluent un pays spécifié dans lequel les produits sont vendus et une priorité ([!DNL High], [!DNL Medium] ou [!DNL Low]). Vous pouvez éventuellement filtrer votre inventaire pour faire la publicité de produits avec des attributs spécifiques, et cibler ou exclure des emplacements et des types d’appareils spécifiques.

Vous pouvez contrôler les produits affichés avec vos publicités commerciales en configurant des *[groupes de produits](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* à plusieurs niveaux au niveau des groupes d’annonces. Les groupes de produits sont basés sur n’importe quel attribut de produit (catégorie, type de produit, marque, condition, ID de produit et étiquettes personnalisées), et vous pouvez créer jusqu’à sept niveaux de groupes de produits à inclure ou exclure de l’offre, sans inclure &quot;[!DNL Add Products]&quot;. Vous pouvez définir des offres au plus bas niveau des groupes de produits, en utilisant la même offre pour tous les produits correspondants. Lorsque le même produit est inclus dans plusieurs campagnes, [!DNL Microsoft Advertising] utilise d’abord la priorité au niveau de la campagne pour déterminer la campagne (et l’offre associée) éligible à l’enchère publicitaire. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible.

## Étapes de configuration des campagnes d’achat [!DNL Microsoft Advertising]

Vous pouvez configurer des campagnes d’achat à l’aide des [ modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) pour [!DNL Microsoft Advertising], à l’aide des [ feuilles d’envoi groupées](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) ou individuellement. Les instructions suivantes comprennent des liens vers la création d’entités individuelles.

1. Configurez votre compte [!DNL Microsoft Merchant Center] et renseignez-le avec les données de produit.

1. [ Autoriser la recherche, Social et Commerce à télécharger les données du  [!DNL Microsoft Merchant Center] compte](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Créez une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) sur le réseau d’achat.

1. [Créez un groupe d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) dans la campagne et définissez l’offre par défaut pour toutes les publicités.

   Vous pouvez remplacer l’offre par défaut pour des groupes de produits individuels.

1. Créez des groupes de produits pour le groupe publicitaire :

   1. [Créez un groupe de produits &quot;Tous les produits&quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facultatif) [Créez des groupes de produits enfants](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Créez des [publicités de produits](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) avec [ lignes de promotion à inclure potentiellement dans chaque publicité d’achat](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) au sein du groupe publicitaire.

      Microsoft Advertising génère dynamiquement la copie de publicité et l’URL de page d’entrée pour chaque publicité.

      >[!NOTE]
      >
      >Même si le groupe publicitaire n’inclut pas d’entités publicitaires, [!DNL Microsoft Advertising] affiche toujours des publicités pour les produits.

1. (Facultatif) Pour effectuer le suivi des clics sur la publicité, [générez une URL de suivi à l’aide de l’outil URL de suivi](/help/search-social-commerce/tools/click-tracking-url-generate.md). La bonne pratique consiste à ajouter l’URL de suivi au champ [!UICONTROL Tracking Template] dans les paramètres du compte, de la campagne ou du groupe de produits. Pour simplifier la maintenance, ajoutez-la au niveau le plus élevé possible.

   Vous pouvez également ajouter l’URL de suivi aux données de produit dans le compte [!DNL Microsoft Merchant Center]. Pour ce faire, incluez l’URL de suivi, ainsi que la valeur du champ &quot;link&quot; ou &quot;mobile_link&quot;, le cas échéant, dans une colonne personnalisée &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; dans le flux de produit. La valeur du champ &quot;bingads_redirect&quot; remplace les valeurs des champs &quot;link&quot; et &quot;mobile_link&quot;. Les URL générées à l’aide de cette méthode n’incluent aucun paramètre de suivi spécifié dans les paramètres de compte ou de campagne Search, Social et Commerce.

1. Surveillez les performances en [générant le [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Selon les besoins :

   1. [Modifiez les paramètres de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour ajuster le budget de la campagne.

      Si la campagne fait partie d’un portfolio, le paramètre de portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; permet à Search, Social et Commerce d’optimiser les budgets pour toutes les campagnes du portfolio.

   1. Ajustez l’offre maximale pour les groupes de produits existants, supprimez les groupes de produits pour lesquels vous ne souhaitez plus créer d’annonces, ou ajoutez un nouveau groupe de produits &quot;tous les produits&quot; ou de nouveaux groupes de produits enfants afin de créer des annonces pour les produits supplémentaires.

>[!NOTE]
>
>* Voir les champs requis pour la gestion des [!DNL Microsoft Shopping] campagnes et groupes de produits à l’aide des [feuilles d’envoi groupées](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) et des [modèles de flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Pour plus d&#39;informations sur les campagnes [!DNL Microsoft Shopping], consultez la [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/50903).
