---
title: À propos des audiences
description: Découvrez les options de suivi, de création et de gestion  [!DNL Google Ads]  audiences et  [!DNL Microsoft Advertising]  audiences.
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/B77S28vEpSkrgNmhc-Ekn7PXh3W-y2g9et2y3gCQPK8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 528
ht-degree: 0%

---

# À propos de la gestion des audiences [!DNL Google Ads] et [!DNL Microsoft Advertising] dans Search, Social et Commerce

*[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

La bibliothèque d’audiences répertorie toutes vos audiences [!DNL Google Ads] basées sur les données client, sur le marché et similaires, ainsi que vos audiences [!DNL Microsoft Advertising] de remarketing et de remarketing dynamique, personnalisées, de correspondance client, sur le marché et similaires. Vous pouvez utiliser n’importe laquelle des audiences [!DNL Google Ads] comme cibles et exclusions [!DNL Google Ads] niveau de la campagne et du groupe publicitaire, et vous pouvez utiliser n’importe laquelle des audiences [!DNL Microsoft Advertising] comme cibles [!DNL Microsoft Advertising] niveau de la campagne et du groupe publicitaire et exclusions (audiences de remarketing dynamique uniquement). Vous pouvez ajouter ou modifier un ajustement d’enchère pour n’importe quelle cible d’audience.

Vous pouvez également créer et gérer des audiences à l’aide de segments ou de listes d’adresses électroniques issues de vos audiences Adobe Experience Cloud existantes et de différents types de données client provenant de votre système de gestion de la relation client (GRC) :

* **Segments d’audience Adobe :** les annonceurs disposant de comptes Adobe Audience Manager ou Adobe Analytics inscrits peuvent créer [!DNL Google Ads] audiences de correspondance client à partir de leurs segments [!DNL Adobe] :

   * (Annonceurs disposant de comptes [!DNL Analytics] qui ne disposent pas également d’Audience Manager) Vous pouvez créer des audiences de correspondance client [!DNL Google Ads] à l’aide d’identifiants d’utilisateurs provenant de segments [!DNL Analytics] partagés avec Adobe Experience Cloud.

   * (Annonceurs avec comptes Audience Manager) Vous pouvez créer des audiences de correspondance de clients [!DNL Google Ads] à l’aide d’identifiants d’utilisateurs de segments Audience Manager qui ont pour destination Search, Social et Commerce. Il peut s’agir de segments Adobe Analytics publiés sur Adobe Experience Cloud et de segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud.

  Pour créer des audiences de correspondance client, le compte [!DNL Google Ads] de l’annonceur doit être [éligible à la correspondance personnalisée](https://support.google.com/adspolicy/answer/6299717) et avoir accepté les segments [identifiant utilisateur](https://support.google.com/google-ads/answer/9199250). En outre, le compte de l’annonceur dans Search, Social et Commerce doit être configuré pour permettre la création d’audiences de correspondance client.

  [!DNL Adobe] données de segment et les fichiers de synchronisation des cookies pour les audiences basées sur les données client sont synchronisés sur [!DNL Google Ads] quotidiennement.

* **Listes de diffusion par e-mail d’Adobe Campaign :** l’équipe chargée de votre compte Adobe peut vous aider à configurer un workflow pour créer et mettre à jour une audience de correspondance client [!DNL Google Ads] à partir d’une liste de diffusion dans [!DNL Campaign].

* **Listes de données client :** les annonceurs disposant de comptes [!DNL Google Ads] ou [!DNL Microsoft Advertising] éligibles à la correspondance client peuvent créer et mettre à jour une audience basée sur les données client spécifique au réseau publicitaire &lt;!— ou audience de remarketing dynamique — incluse dans l’audience basée sur les données du client, au moins pour [!DNL Google Ads] ? —> en chargeant un fichier CSV avec les identifiants principaux.

* **Listes de remarketing dynamique :** les annonceurs disposant de comptes [!DNL Microsoft Advertising] peuvent créer et gérer des audiences de remarketing dynamique, que vous pouvez utiliser pour recibler les clients potentiels qui ont récemment interagi avec vos produits de l’une des multiples façons (comme les visiteurs de produits ou les acheteurs précédents). Les audiences de remarketing dynamique nécessitent que vous utilisiez la balise de conversion et de suivi d’audience JavaScript du réseau publicitaire sur vos pages web. Utilisez des listes de remarketing dynamique avec des campagnes d’achat sur les réseaux de recherche et d’audience pour recibler les audiences avec des annonces de produit, ainsi qu’avec des campagnes de recherche pour recibler les audiences avec des annonces textuelles et des annonces de recherche dynamique. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Les modificateurs d’offres pour les cibles d’audience de remarketing dynamique ne sont pas optimisés dans les portfolios avec le paramètre « [!UICONTROL Auto-optimize Bid Adjustment Values] ».

>[!NOTE]
>
>Search, Social et Commerce ne stockent aucune des données client que vous chargez ou provenant des segments de [!DNL Adobe] utilisés pour créer ou modifier une audience [!DNL Google Ads] ou [!DNL Microsoft Advertising].

>[!MORELIKETHIS]
>
>* [Créer [!DNL Google Ads] des audiences de correspondance client à partir  [!DNL Adobe]  audiences](google-audience-from-adobe-audience.md)
>* [Création d’une audience  [!DNL Google Ads]  correspondance client à partir d’une liste d’emails Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gérer les audiences de correspondance de clients à l’aide de listes de données client](audience-from-customer-data-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
>* [Gérer les cibles d’audience pour les campagnes et les groupes publicitaires](audience-targets-manage.md)
>* [Gérer les exclusions d’audience pour les campagnes et les groupes publicitaires](audience-exclusions-manage.md)
