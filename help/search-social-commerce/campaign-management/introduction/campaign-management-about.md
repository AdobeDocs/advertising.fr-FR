---
title: À propos de la gestion des campagnes dans Search, Social et Commerce
description: Découvrez les fonctionnalités de gestion des campagnes dans Search, Social et Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tgoMzw4DbEY5evC2s1f6mQHfJYYb7DJzMfFUnc-06Bk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 6a6c9fecfe07a94bf77cfce65bfd7a079755890f
workflow-type: tm+mt
source-wordcount: 834
ht-degree: 0%

---

# À propos de la gestion des campagnes dans Search, Social et Commerce

Search, Social et Commerce vous permet de suivre et de gérer vos campagnes Search, Display/Content, Social, Shopping, Audience et Performance Max à un seul endroit. Selon le réseau publicitaire et le type de campagne, les fonctionnalités disponibles peuvent inclure la synchronisation avec vos réseaux publicitaires, la création et la modification de fonctionnalités, l’attribution du suivi et de la conversion, le reporting et l’optimisation des enchères et du budget. Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [&#x200B; Inventaire pris en charge &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md).

Lorsque vous ajoutez et modifiez des données de campagne dans les vues [!UICONTROL Campaigns], Search, Social et Commerce envoie immédiatement les modifications de données au réseau publicitaire. Search, Social et Commerce extraient également les données de structure de campagne et cliquent quotidiennement sur les données à partir des comptes réseau d’annonces synchronisés, ou plus souvent lorsque de nouvelles campagnes sont détectées. Pour tous les réseaux publicitaires synchronisés, vous pouvez également synchroniser les comptes à la demande si nécessaire.

Search, Social et Commerce extraient les données de performances toutes les heures des comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] synchronisés, et tous les jours pour les autres comptes réseau publicitaire synchronisés.

## Configuration de l’accès à vos comptes de réseau publicitaire

Pour suivre les performances des publicités dans le compte du réseau publicitaire d’un annonceur (et éventuellement placer des enchères pour les publicités), l’équipe du compte Adobe [crée un enregistrement de compte correspondant](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) dans Search, Social et Commerce. L’enregistrement de compte inclut des options de suivi.

Pour les comptes synchronisés via l’API du réseau publicitaire, l’enregistrement de compte inclut également les informations d’identification d’accès au compte. Une fois le compte activé, les données du compte sont extraites avec le réseau publicitaire. Vous pouvez ensuite afficher les données du compte existant, ainsi que créer et modifier la structure de la campagne et les données des annonces.

## Suivi des clics pour lier les clics aux conversions

Si vous utilisez le service de suivi des conversions Adobe Advertising, vous devez inclure le code de suivi des clics Search, Social et Commerce dans le suffixe de la page de destination, les modèles de suivi et les URL finales/de destination pour les annonces, les mots-clés, les emplacements, les liens de site et les listes de produits. Pour les [réseaux publicitaires et types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) dont les paramètres de campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement, de sorte que vous n’ayez pas à l’ajouter manuellement. Sinon, vous devez ajouter manuellement le code à vos modèles de tracking ou URL finales.

Pour plus d’informations sur le tracking, consultez le chapitre « Tracking ».

## Automatisation des enchères et de la gestion des budgets

Pour les [réseaux publicitaires et types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md), vous pouvez regrouper vos campagnes en portfolios, chacun avec un objectif commercial spécifique et un budget ou une cible de performances spécifique. Dans les portfolios standard, Search, Social et Commerce optimise les enchères de mots-clés CPC et les budgets de campagne. Les portfolios hybrides combinent les technologies d’optimisation de Search, Social et Commerce et de vos réseaux publicitaires.

Pour plus d’informations sur les options de portfolio disponibles et sur la configuration des portfolios, consultez le chapitre du Guide d’optimisation sur les « Portfolios », disponible dans Search, Social et Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Les vues de gestion de campagne

Les vues Gestion de campagne vous permettent de surveiller et de gérer vos comptes de recherche. Les vues suivantes sont disponibles :

* **[!UICONTROL Campaigns]** — Les vues [!UICONTROL Campaigns] affichent les données de chaque compte réseau publicitaire connecté. Vous pouvez afficher les données de coût, de clic, d’impression et de chiffre d’affaires sur tous les comptes de réseau publicitaire et sur plusieurs comptes individuels, campagnes, groupes publicitaires, mots-clés, publicités, groupes de produits d’achat, emplacements, cibles automatiques (cibles de recherche dynamique), audiences et bibliothèques d’extensions publicitaires et leurs entités de compte associées. Pour les [types de campagne pris en charge sur les réseaux publicitaires pris en charge](/help/search-social-commerce/introduction/supported-inventory.md), vous pouvez créer et modifier des données pour des campagnes individuelles et des composants de campagne directement dans l’interface. Vous pouvez éventuellement exporter les données de la plupart des sous-vues vers un fichier de feuille de calcul.

  >[!NOTE]
  >
  >Les données au niveau des annonces ne sont pas disponibles pour [!DNL Google Ads] annonce de recherche dynamique (DSA), les campagnes Performance max, Achats intelligents et [!DNL YouTube].

* **[!UICONTROL Products]** — Les vues [!UICONTROL Products] affichent les données de chaque compte [[!DNL Google] ou [!DNL Microsoft] centre commercial synchronisé](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Le sous-affichage [!UICONTROL Accounts] par défaut répertorie tous les comptes synchronisés ; certains types d’utilisateurs peuvent ajouter de nouveaux comptes à partir de cet affichage. La sous-vue [!UICONTROL Products] répertorie chaque produit dans le compte.

* **[!UICONTROL Advanced (ACM)]** : depuis la vue [!DNL Advanced] ([!DNL AMC], pour la gestion avancée des campagnes), vous pouvez configurer des processus automatisés pour créer des [publicités dynamiques et mots-clés ciblés sur chaque élément de votre inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) en fonction d&#39;un modèle de publicité spécifique au réseau publicitaire que vous créez et du contenu de [!DNL Google Merchant Center] comptes ou fichiers de données d&#39;inventaire que vous chargez vers un emplacement FTP. Les sous-vues affichent des détails sur chaque modèle de flux pour l’annonceur et chaque campagne, groupe publicitaire, mot-clé et publicité inclus dans un flux qui a été propagé par le biais d’un modèle de flux mais non publié sur le réseau publicitaire.

* **[!UICONTROL Bulksheets]** — Utilisez la vue [!UICONTROL Bulksheets] pour créer des [fichiers de feuilles d&#39;envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contenant autant de données que vous le souhaitez pour un compte sur un réseau publicitaire [pris en charge](/help/search-social-commerce/introduction/supported-inventory.md), puis pour les publier sur le réseau publicitaire.

* **[!UICONTROL Audiences]** — [vues [!UICONTROL Audiences]](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) répertorie toutes vos audiences [!DNL Google Ads] et [!DNL Microsoft Advertising] générées à partir de différents types de listes d&#39;utilisateurs. Vous pouvez créer des audiences [!DNL Google Ads] à partir de vos audiences Adobe CX Enterprise existantes et de vos listes d’adresses électroniques des clients. Vous pouvez également afficher et gérer les cibles et exclusions d’audience pour vos publicités [!DNL Google Ads] et [!DNL Microsoft Advertising].

* **[!UICONTROL Label Classifications]** — Utilisez cette vue pour créer et supprimer des [classifications de libellés](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) qui peuvent vous aider à regrouper vos libellés en ensembles significatifs.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes et des campagnes de réseau publicitaire](campaign-implemention-overview.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaire](monitor-performance-campaigns.md)
>* [Données de conversion Google Ads dans Search, Social et Commerce](google-conversion-data.md)
