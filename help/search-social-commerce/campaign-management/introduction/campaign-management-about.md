---
title: Gestion de campagnes dans Search, Social et Commerce
description: Découvrez les fonctionnalités de gestion de campagne dans Search, Social et Commerce.
exl-id: e6fca48d-1f6c-4d36-a10d-e1a5db859a37
feature: Search Campaign Management
source-git-commit: d23b5a3c56c35fc5abbeafde681b9f584bf1c905
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Gestion de campagnes dans Search, Social et Commerce

Search, Social et Commerce vous permet de suivre et/ou de gérer vos campagnes de recherche, d’affichage/contenu, de réseaux sociaux, d’achats, d’audience et de performances maximales à un seul emplacement. Selon le réseau publicitaire et le type de campagne, les fonctionnalités disponibles peuvent inclure la synchronisation avec vos réseaux publicitaires, la création et la modification de fonctionnalités, l’attribution de suivi et de conversion, la création de rapports, ainsi que l’optimisation de l’offre et du budget. Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, voir &quot;[Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

À mesure que vous ajoutez et modifiez des données de campagne dans le [!UICONTROL Campaigns] affichages, recherche, Social et commerce transfère immédiatement les modifications de données au réseau publicitaire. Search, Social et Commerce extrait également les données de structure de campagne et clique sur les données des comptes réseau publicitaires synchronisés une fois par jour (ou plus souvent lorsque de nouvelles campagnes sont détectées) et sur demande, selon les besoins.

## Configuration de l’accès à vos comptes de réseau publicitaire

Pour suivre les performances des publicités dans le compte réseau publicitaire d’un annonceur (et pour proposer éventuellement des offres pour les publicités), l’équipe Compte Adobe [crée un enregistrement de compte correspondant.](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) dans Search, Social et Commerce. L’enregistrement de compte comprend des options de suivi.

Pour les comptes synchronisés via l’API du réseau publicitaire, l’enregistrement de compte inclut également les informations d’identification d’accès au compte. Une fois le compte activé, les données du compte sont extraites du réseau publicitaire. Vous pouvez ensuite afficher les données de compte existantes ainsi que créer et modifier la structure de campagne et les données de publicité.

## Suivi des clics pour lier les clics aux conversions

Si vous utilisez le service de suivi des conversions Adobe Advertising, vous devez inclure le code de suivi des clics de Search, Social et Commerce dans le suffixe de la page d’entrée, les modèles de suivi et les URL finales/de destination pour les annonces, les mots-clés et les emplacements, les liens de site et les listes de produits. Pour [réseaux publicitaires et types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) dont les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce ajoute automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement, de sorte que vous n’ayez pas à l’ajouter manuellement. Sinon, vous devez ajouter manuellement le code à vos modèles de suivi ou URL finales.

Pour plus d’informations sur le tracking, consultez le chapitre &quot;Tracking&quot;.

## Automatisation de la gestion des offres et des budgets

Pour [réseaux publicitaires et types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md), vous pouvez regrouper vos campagnes dans des portefeuilles, chacun ayant un objectif commercial spécifique et un objectif de budget ou de performance spécifique. Dans les portfolios standard, Search, Social et Commerce optimise les offres sur les mots-clés CPC et les budgets de campagne. Les portefeuilles hybrides combinent les technologies d’optimisation de Search, Social et Commerce et vos réseaux publicitaires.

Pour plus d’informations sur les options de portefeuille disponibles et sur la configuration des portefeuilles, reportez-vous au chapitre du guide d’optimisation intitulé &quot;Portfolios&quot;, disponible dans Search, Social et Commerce.<!-- verify convention for referencing Optimization Guide here -->

## Les vues de gestion de campagne

Les vues de gestion de campagne vous permettent de surveiller et de gérer vos comptes de recherche. Les vues disponibles sont les suivantes :

* **[!UICONTROL Campaigns]** — Le [!UICONTROL Campaigns] les vues affichent les données de chaque compte réseau publicitaire connecté. Vous pouvez afficher les données sur les coûts, les clics, les impressions et les recettes sur tous les comptes de réseau publicitaire et sur les comptes, campagnes, groupes publicitaires, mots-clés, publicités, groupes de produits d’achat, emplacements, cibles automatiques (cibles de recherche dynamique), audiences et bibliothèques d’extension de publicité, ainsi que les entités de compte associées. Pour [types de campagne pris en charge sur les réseaux publicitaires pris en charge](/help/search-social-commerce/introduction/supported-inventory.md), vous pouvez créer et modifier des données pour des campagnes et des composants de campagne individuels directement dans l’interface. Vous pouvez éventuellement exporter les données de la plupart des sous-vues vers un fichier de feuille de calcul.

  >[!NOTE]
  >
  >Les données au niveau de la publicité ne sont pas disponibles pour [!DNL Google Ads] publicité de recherche dynamique (DSA), niveau de performance maximal, achats intelligents et [!DNL YouTube] campagnes.

* **[!UICONTROL Products]** — Le [!UICONTROL Products] les vues affichent les données pour chaque [[!DNL Google] or [!DNL Microsoft] compte de centre commercial synchronisé](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Par défaut [!UICONTROL Accounts] subview répertorie tous les comptes synchronisés ; certains types d’utilisateurs peuvent ajouter de nouveaux comptes à partir de cette vue. La variable [!UICONTROL Products] subview répertorie chaque produit dans le compte .

* **[!UICONTROL Advanced (ACM)]** — De la [!DNL Advanced] ([!DNL AMC], pour la vue Advanced Campaign Management), vous pouvez configurer des processus automatisés pour créer des [annonces dynamiques et mots-clés ciblés sur chaque élément de votre inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) selon un modèle de publicité spécifique au réseau que vous créez et le contenu de [!DNL Google Merchant Center] comptes ou fichiers de données d’inventaire que vous transférez vers un emplacement FTP. Les sous-vues affichent des détails sur chaque modèle de flux pour l’annonceur et sur chaque campagne, groupe publicitaire, mot-clé et publicité inclus dans un flux qui a été propagé par un modèle de flux mais qui n’a pas été publié sur le réseau publicitaire.

* **[!UICONTROL Bulksheets]** — Utilisez la variable [!UICONTROL Bulksheets] vue à créer [fichiers de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contenant autant de données que vous le souhaitez pour un compte sur une [réseau publicitaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md), puis publiez-les sur le réseau publicitaire.

* **[!UICONTROL Audiences]** — [La variable [!UICONTROL Audiences] views](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) répertorie toutes vos [!DNL Google Ads] et [!DNL Microsoft Advertising] audiences générées à partir de différents types de listes d’utilisateurs. Vous pouvez créer [!DNL Google Ads] audiences de vos audiences Adobe Experience Cloud existantes et listes d’adresses électroniques de vos clients. Vous pouvez également afficher et gérer les cibles et exclusions d’audience pour votre [!DNL Google Ads] et [!DNL Microsoft Advertising] publicités.

* **[!UICONTROL Label Classifications]** — Utilisez cette vue pour créer et supprimer des [classification des étiquettes](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), qui peut vous aider à regrouper vos libellés en ensembles significatifs.

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation des comptes et campagnes de réseau publicitaire](campaign-implemention-overview.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaires](monitor-performance-campaigns.md)
>* [Données de conversion Google Ads dans Search, Social et Commerce](google-conversion-data.md)
