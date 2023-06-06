---
title: A propos des audiences
description: En savoir plus sur les options de suivi, de création et de gestion [!DNL Google Ads] et [!DNL Microsoft® Advertising] audiences.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# A propos de la gestion [!DNL Google Ads] et [!DNL Microsoft® Advertising] audiences dans Search, Social et Commerce

*[!DNL Google Ads]et [!DNL Microsoft® Advertising] only*

La bibliothèque d’audiences répertorie toutes vos [!DNL Google Ads] les audiences basées sur les données client, in-marché et similaires et vos [!DNL Microsoft® Advertising] le remarketing et le remarketing dynamique, les audiences personnalisées, les correspondances client, les audiences sur le marché et les audiences similaires. Vous pouvez utiliser l’une des [!DNL Google Ads] audiences en tant que [!DNL Google Ads] cibles et exclusions au niveau de la campagne et du groupe publicitaire, et vous pouvez utiliser n’importe quelle [!DNL Microsoft® Advertising] audiences en tant que [!DNL Microsoft® Advertising] des cibles au niveau de la campagne et au niveau du groupe publicitaire, ainsi que des exclusions (audiences de remarketing dynamique uniquement). Vous pouvez ajouter ou modifier un ajustement d’offre pour n’importe quelle cible d’audience.

Vous pouvez également créer et gérer des audiences à l’aide de segments ou de listes d’emails provenant de vos audiences Adobe Experience Cloud existantes et de divers types de données client issues de votre système de gestion de la relation client (CRM) :

* **Adobe des segments d’audience :** Les annonceurs disposant de comptes Adobe Audience Manager ou Adobe Analytics ouverts peuvent créer [!DNL Google Ads] les clients correspondent aux audiences de leurs [!DNL Adobe] segments :

   * (Publicitaires avec [!DNL Analytics] les comptes qui n’ont pas non plus d’Audience Manager) Vous pouvez créer des [!DNL Google Ads] des audiences de correspondance client à l’aide d’identifiants utilisateur provenant de [!DNL Analytics] segments partagés avec Adobe Experience Cloud.

   * (Publicitaires disposant de comptes d’Audience Manager) Vous pouvez créer des [!DNL Google Ads] les clients correspondent à des audiences à l’aide d’identifiants d’utilisateur provenant de segments d’Audience Manager dont la destination est Search, Social et Commerce. Cela peut inclure les segments Adobe Analytics publiés sur Adobe Experience Cloud et les segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud.
   Pour créer des audiences de correspondance client, le [!DNL Google Ads] account doit être [éligible pour une correspondance personnalisée](https://support.google.com/adspolicy/answer/6299717) et ont choisi [segments d’ID utilisateur](https://support.google.com/google-ads/answer/9199250). En outre, le compte de l’annonceur dans Search, Social et Commerce doit être configuré pour permettre la création d’audiences de correspondance client.<!-- For Analytics audiences: Analytics Only Integration. For Audience Manager, Enable CM/CRM option) -->

   [!DNL Adobe] les données de segment et les fichiers de synchronisation de cookies pour les audiences basées sur les données client sont synchronisés avec [!DNL Google Ads] tous les jours.

* **Les listes de messagerie Adobe Campaign sont les suivantes :** Votre équipe de compte d’Adobe peut vous aider à configurer un workflow pour créer et mettre à jour un [!DNL Google Ads] audience de correspondance de client à partir d’une liste de courriers électroniques dans [!DNL Campaign].

* **Les listes de données du client :** Annonceurs avec [!DNL Google Ads] ou [!DNL Microsoft® Advertising] les comptes éligibles pour une correspondance client peuvent créer et mettre à jour une audience basée sur les données client spécifique au réseau publicitaire. &lt;!>— ou audience de remarketing dynamique — incluse dans l’audience basée sur les données client, au moins pour [!DNL Google Ads]?—> en téléchargeant un fichier CSV avec de Principaux identifiants.

* **Listes de remarketing dynamique :** Annonceurs avec [!DNL Microsoft® Advertising] Les comptes peuvent créer et gérer des audiences de remarketing dynamique, que vous pouvez utiliser pour recibler les clients potentiels qui ont récemment interagi avec vos produits de l’une des manières suivantes (par exemple, les observateurs de produits ou les anciens acheteurs). Les audiences de remarketing dynamique nécessitent que vous utilisiez la balise de conversion JavaScript et de suivi d’audience du réseau publicitaire sur vos pages web. Utilisez des listes de remarketing dynamique avec des campagnes d’achat sur les réseaux de recherche et d’audience pour recibler des audiences avec des publicités de produits, ainsi que des campagnes de recherche pour recibler des audiences avec des publicités textuelles et des annonces de recherche dynamique. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

   >[!NOTE]
   >
   >Les modificateurs d’offre pour les cibles d’audience de remarketing dynamique ne sont pas optimisés dans les portefeuilles avec le paramètre &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

>[!NOTE]
>
>Search, Social et Commerce ne stocke aucune des données client que vous chargez ou provenant de la variable [!DNL Adobe] segments utilisés pour créer ou modifier une [!DNL Google Ads] ou [!DNL Microsoft® Advertising] audience.

>[!MORELIKETHIS]
>
>* [A propos des audiences](audience-about.md)
>* [Créer [!DNL Google Ads] audiences de correspondance client provenant de [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Créez un [!DNL Google Ads] audience de correspondance client provenant d’une liste de messagerie Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestion des audiences de correspondance client à l’aide des listes de données client](audience-from-customer-data-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
>* [Gestion des cibles d’audience pour les campagnes et les groupes publicitaires](audience-targets-manage.md)
>* [Gestion des exclusions d’audience pour les campagnes et les groupes publicitaires](audience-exclusions-manage.md)

