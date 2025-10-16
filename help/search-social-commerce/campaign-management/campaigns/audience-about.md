---
title: A propos des audiences
description: Découvrez les options permettant de suivre, créer et gérer les audiences  [!DNL Google Ads] et  [!DNL Microsoft Advertising] .
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# À propos de la gestion des audiences [!DNL Google Ads] et [!DNL Microsoft Advertising] dans Search, Social et Commerce

*[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

La bibliothèque d’audiences répertorie toutes vos audiences [!DNL Google Ads] basées sur les données client, sur le marché et similaires, ainsi que vos audiences [!DNL Microsoft Advertising] de remarketing et de remarketing dynamique, personnalisées, de correspondance client, in-market et similaires. Vous pouvez utiliser n’importe quelle audience [!DNL Google Ads] comme cibles et exclusions au niveau de la campagne et du groupe publicitaire, et vous pouvez utiliser n’importe quelle audience [!DNL Microsoft Advertising] comme cibles au niveau de la campagne et du groupe publicitaire et exclusions (audiences de remarketing dynamique uniquement). [!DNL Google Ads]&#x200B;[!DNL Microsoft Advertising] Vous pouvez ajouter ou modifier un ajustement d’offre pour n’importe quelle cible d’audience.

Vous pouvez également créer et gérer des audiences à l’aide de segments ou de listes d’emails provenant de vos audiences Adobe Experience Cloud existantes et de divers types de données client issues de votre système de gestion de la relation client (CRM) :

* **Adobe des segments d’audience :** Les annonceurs disposant de comptes Adobe Audience Manager ou Adobe Analytics ouverts peuvent créer [!DNL Google Ads] audiences de correspondance client à partir de leurs [!DNL Adobe] segments :

   * (Publicitaires disposant de comptes [!DNL Analytics] qui ne disposent pas non plus d’Audience Manager) Vous pouvez créer des audiences de correspondance client [!DNL Google Ads] à l’aide d’identifiants utilisateur provenant de segments [!DNL Analytics] partagés avec Adobe Experience Cloud.

   * (Publicitaires avec comptes d’Audience Manager) Vous pouvez créer [!DNL Google Ads] audiences de correspondance client à l’aide d’identifiants utilisateur provenant de segments d’Audience Manager dont la destination est Search, Social et Commerce. Cela peut inclure les segments Adobe Analytics publiés sur Adobe Experience Cloud et les segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud.

  Pour créer des audiences de correspondance client, le compte [!DNL Google Ads] de l’annonceur doit être [éligible à une correspondance personnalisée](https://support.google.com/adspolicy/answer/6299717) et avoir choisi [&#x200B; segments d’ID utilisateur](https://support.google.com/google-ads/answer/9199250). En outre, le compte de l’annonceur dans Search, Social et Commerce doit être configuré de manière à permettre la création d’audiences avec correspondance client.

  [!DNL Adobe] les données de segment et les fichiers de synchronisation de cookies pour les audiences basées sur les données client sont synchronisés quotidiennement à [!DNL Google Ads].

* **Listes de messagerie Adobe Campaign :** Votre équipe de compte d’Adobe peut vous aider à configurer un workflow pour créer et mettre à jour une audience de correspondance de client [!DNL Google Ads] à partir d’une liste de messagerie dans [!DNL Campaign].

* **Listes de données client :** Les annonceurs disposant de comptes [!DNL Google Ads] ou [!DNL Microsoft Advertising] éligibles à une correspondance client peuvent créer et mettre à jour une audience basée sur les données client spécifique au réseau publicitaire &lt;!— ou audience de remarketing dynamique — incluse dans l’audience basée sur les données client, au moins pour [!DNL Google Ads] ? —> en chargeant un fichier CSV avec les identifiants principaux.

* **Listes de remarketing dynamique :** les annonceurs disposant de comptes [!DNL Microsoft Advertising] peuvent créer et gérer des audiences de remarketing dynamique, que vous pouvez utiliser pour recibler les clients potentiels ayant récemment interagi avec vos produits de l’une des façons suivantes (observateurs de produits ou acheteurs précédents). Les audiences de remarketing dynamique nécessitent que vous utilisiez la balise de conversion JavaScript et de suivi d’audience du réseau publicitaire sur vos pages web. Utilisez des listes de remarketing dynamique avec des campagnes d’achat sur les réseaux de recherche et d’audience pour recibler des audiences avec des publicités de produits, ainsi que des campagnes de recherche pour recibler des audiences avec des publicités textuelles et des annonces de recherche dynamique. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Les modificateurs d’offre pour les cibles d’audience de remarketing dynamique ne sont pas optimisés dans les portefeuilles avec le paramètre &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

>[!NOTE]
>
>Search, Social et Commerce ne stocke aucune des données de client que vous chargez ou des segments [!DNL Adobe] utilisés pour créer ou modifier une audience [!DNL Google Ads] ou [!DNL Microsoft Advertising].

>[!MORELIKETHIS]
>
>* [Créer [!DNL Google Ads]  des audiences de correspondance client à partir des  [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Créer une  [!DNL Google Ads] audience de correspondance de client à partir d’une liste de messagerie Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gérer les audiences de correspondance de client à l’aide des listes de données de client](audience-from-customer-data-list.md)
>* [Gérer les audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
>* [Gérer les cibles d’audience pour les campagnes et les groupes d’annonces](audience-targets-manage.md)
>* [Gérer les exclusions d’audience pour les campagnes et les groupes d’annonces](audience-exclusions-manage.md)
