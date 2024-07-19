---
title: Gestion de campagne dans Search, Social et Commerce
description: Découvrez les fonctionnalités de gestion de campagne de Search, Social et Commerce.
exl-id: 19e36e73-fcb6-4ff3-980b-fc05042725fd
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Gestion de campagne dans Search, Social et Commerce

Search, Social et Commerce vous permet de suivre et/ou de gérer vos campagnes de recherche, d’affichage/contenu, de réseaux sociaux, d’achats, d’audience et de performances maximales à un seul emplacement. Selon le réseau publicitaire et le type de campagne, les fonctionnalités disponibles peuvent inclure la synchronisation avec vos réseaux publicitaires, la création et la modification de fonctionnalités, l’attribution de suivi et de conversion, la création de rapports, ainsi que l’optimisation de l’offre et du budget. Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, voir &quot;[Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

Lorsque vous ajoutez et modifiez des données de campagne dans les vues [!UICONTROL Campaigns], Search, Social et Commerce envoie immédiatement les modifications de données au réseau publicitaire. Search, Social et Commerce extrait également les données de structure de campagne et les données de clic des comptes réseau publicitaires synchronisés une fois par jour (ou plus souvent lorsque de nouvelles campagnes sont détectées) et sur demande, selon les besoins.

## Configuration de l’accès à vos comptes de réseau publicitaire

Pour effectuer le suivi des performances des publicités dans le compte réseau publicitaire d’un annonceur (et pour placer éventuellement des offres pour les publicités), l’équipe du compte d’Adobe [ crée un enregistrement de compte correspondant](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) dans Search, Social et Commerce. L’enregistrement de compte comprend des options de suivi.

Pour les comptes synchronisés via l’API du réseau publicitaire, l’enregistrement de compte inclut également les informations d’identification d’accès au compte. Une fois le compte activé, les données du compte sont extraites du réseau publicitaire. Vous pouvez ensuite afficher les données de compte existantes ainsi que créer et modifier la structure de campagne et les données de publicité.

## Suivi des clics pour lier les clics aux conversions

Si vous utilisez le service de suivi de conversion Adobe Advertising, vous devez inclure le code de suivi des clics Search, Social et Commerce dans le suffixe de la page d’entrée, les modèles de suivi et les URL finales/de destination pour les annonces, les mots-clés et les emplacements, les liens de site et les listes de produits. Pour les [ réseaux publicitaires et types de campagne pris en charge ](/help/search-social-commerce/introduction/supported-inventory.md) dont les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload]&quot;, Search, Social et Commerce ajoute automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement, de sorte que vous n’ayez pas à l’ajouter manuellement. Sinon, vous devez ajouter manuellement le code à vos modèles de suivi ou URL finales.

Pour plus d’informations sur le tracking, consultez le chapitre &quot;Tracking&quot;.

## Automatisation de la gestion des offres et des budgets

Pour les [ réseaux publicitaires et types de campagne pris en charge ](/help/search-social-commerce/introduction/supported-inventory.md), vous pouvez regrouper vos campagnes dans des portefeuilles, chacun avec un objectif commercial spécifique et un budget ou une cible de performance spécifique. Dans les portfolios standard, Search, Social et Commerce optimise les offres sur les mots-clés CPC et les budgets de campagne. Les portefeuilles hybrides combinent les technologies d’optimisation de Search, Social et Commerce et vos réseaux publicitaires.

Pour plus d’informations sur les options de portefeuille disponibles et sur la configuration des portefeuilles, reportez-vous au chapitre du guide d’optimisation intitulé &quot;Portfolios&quot;, disponible dans Search, Social et Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Les vues de gestion de campagne

Les vues de gestion de campagne vous permettent de surveiller et de gérer vos comptes de recherche. Les vues disponibles sont les suivantes :

* **[!UICONTROL Campaigns]** — Les vues [!UICONTROL Campaigns] affichent les données de chaque compte réseau publicitaire connecté. Vous pouvez afficher les données sur les coûts, les clics, les impressions et les recettes sur tous les comptes de réseau publicitaire et sur les comptes, campagnes, groupes publicitaires, mots-clés, publicités, groupes de produits d’achat, emplacements, cibles automatiques (cibles de recherche dynamique), audiences et bibliothèques d’extension de publicité, ainsi que les entités de compte associées. Pour les [types de campagne pris en charge sur les réseaux publicitaires pris en charge](/help/search-social-commerce/introduction/supported-inventory.md), vous pouvez créer et modifier des données pour des campagnes individuelles et des composants de campagne directement dans l’interface. Vous pouvez éventuellement exporter les données de la plupart des sous-vues vers un fichier de feuille de calcul.

  >[!NOTE]
  >
  >Les données au niveau de la publicité ne sont pas disponibles pour les campagnes [!DNL Google Ads] de recherche dynamique (DSA), de performance maximale, d’achats intelligents et [!DNL YouTube].

* **[!UICONTROL Products]** — Les vues [!UICONTROL Products] affichent des données pour chaque compte [[!DNL Google] ou [!DNL Microsoft] de centre commercial synchronisé](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). La sous-vue par défaut [!UICONTROL Accounts] répertorie tous les comptes synchronisés. Certains types d’utilisateurs peuvent ajouter de nouveaux comptes à partir de cette vue. La sous-vue [!UICONTROL Products] répertorie chaque produit dans le compte.

* **[!UICONTROL Advanced (ACM)]** — Dans la vue [!DNL Advanced] ([!DNL AMC], pour Advanced Campaign Management), vous pouvez configurer des processus automatisés pour créer des [publicités dynamiques et des mots-clés ciblés sur chaque élément de votre inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) en fonction d’un modèle d’annonce spécifique au réseau publicitaire que vous avez créé et du contenu des comptes [!DNL Google Merchant Center] ou des fichiers de données d’inventaire que vous chargez vers un emplacement FTP. Les sous-vues affichent des détails sur chaque modèle de flux pour l’annonceur et sur chaque campagne, groupe publicitaire, mot-clé et publicité inclus dans un flux qui a été propagé par un modèle de flux mais qui n’a pas été publié sur le réseau publicitaire.

* **[!UICONTROL Bulksheets]** — Utilisez la vue [!UICONTROL Bulksheets] pour créer des [fichiers de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contenant autant de données que vous le souhaitez pour un compte sur un [réseau publicitaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md), puis publiez-les sur le réseau publicitaire.

* **[!UICONTROL Audiences]** — [Les [!UICONTROL Audiences] vues](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) répertorient toutes vos audiences [!DNL Google Ads] et [!DNL Microsoft Advertising] générées à partir de différents types de listes d’utilisateurs. Vous pouvez créer [!DNL Google Ads] audiences à partir de vos audiences Adobe Experience Cloud existantes et de vos listes d’adresses électroniques de clients. Vous pouvez également afficher et gérer les cibles et exclusions d’audience pour vos publicités [!DNL Google Ads] et [!DNL Microsoft Advertising].

* **[!UICONTROL Label Classifications]** — Utilisez cette vue pour créer et supprimer des [classifications d’étiquettes](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), qui peuvent vous aider à regrouper vos étiquettes dans des ensembles significatifs.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes de réseau publicitaire et des campagnes](campaign-implemention-overview.md)
>* [ Surveillez et gérez les performances de vos campagnes réseau d’annonces ](monitor-performance-campaigns.md)
>* [Données de conversion Google Ads dans Search, Social et Commerce](google-conversion-data.md)
