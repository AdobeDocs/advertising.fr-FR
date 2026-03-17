---
title: Présentation de l’implémentation des comptes et des campagnes de réseau publicitaire
description: Découvrez les tâches liées à la configuration, à la synchronisation et à la gestion de vos comptes de réseau publicitaire.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: 6014f2dc349286d562f219db7e05279deb96e477
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# Présentation de l’implémentation des comptes et des campagnes de réseau publicitaire

Adobe travaille avec chaque annonceur pour configurer ses comptes et campagnes de réseau publicitaire. Cela inclut la configuration de Search, Social et Commerce pour se connecter et se synchroniser avec les comptes de l’annonceur, la création de nouvelles campagnes et de composants de campagne si nécessaire, la configuration du suivi des publicités des composants, l’ajout facultatif des campagnes aux portfolios pour permettre à Search, Social et Commerce d’optimiser les enchères sur les publicités, et la validation des données initiales de coût, de clic et de chiffre d’affaires.

Une fois qu’une campagne est activée et éventuellement ajoutée à un portfolio, l’équipe de gestion de compte d’Adobe, l’équipe de l’agence ou l’annonceur (selon les conditions du service level agreement) doit surveiller chaque campagne et modifier les composants et paramètres pertinents si nécessaire pour atteindre les objectifs de l’annonceur.

Cette page contient des informations sur tous les types de compte, y compris sur la configuration de la structure de campagne pour les comptes synchronisés. Pour obtenir des instructions supplémentaires sur la configuration des comptes de suivi uniquement pour [!DNL Naver], voir « [Implémenter [!DNL Naver] des comptes de suivi uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) ».

## Tâches de configuration initiales pour les comptes et les campagnes

[!DNL Adobe] et/ou votre agence travailleront avec vous pour :

1. (Nouveaux comptes d’annonceurs) Configurez des comptes d’administration :

   1. Configurez le compte de l’annonceur.

   1. (Si nécessaire) Créez des comptes utilisateur pour que l’annonceur puisse afficher et gérer ses données de campagne et générer des rapports.

1. (Certains réseaux publicitaires) Obtenez l’autorisation pour Search, Social et Commerce d’accéder à chaque compte à l’aide de l’API du réseau publicitaire et de l’interface utilisateur Search, Social et Commerce.

1. Pour chaque compte de réseau publicitaire :

   1. (Si nécessaire) Configurez le compte sur le réseau publicitaire.

   1. Effectuez l’intégration au compte en [créant un enregistrement de compte correspondant](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) dans Search, Social et Commerce contenant les informations d’identification et les options de suivi d’accès au compte, puis définissez le statut du compte sur activé.

      Search, Social et Commerce se synchronise ensuite avec le réseau publicitaire. Si le compte contient déjà des données de campagne, les données sont disponibles dans environ 24 heures.

   1. ([Types d’annonces que vous pouvez créer/modifier](/help/search-social-commerce/introduction/supported-inventory.md) dans Search, Social et Commerce) Si le compte ne contient pas déjà de données de campagne, créez la structure de la campagne et les composants de la campagne à partir de Search, Social et Commerce à l’aide de l’une des méthodes suivantes disponibles pour le type d’annonce :

      * (Google Ads, Microsoft Advertising, Yahoo ! Annonces et comptes Yandex uniquement) Configurez un processus [automatisé pour créer des annonces dynamiques et des mots-clés ciblés sur chaque élément de votre inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) en fonction d’un modèle d’annonce spécifique au réseau publicitaire que vous créez et du contenu des fichiers de données d’inventaire que vous téléchargez vers un emplacement FTP.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo ! Japan Ads et comptes Yandex uniquement) Chargez des [fichiers de feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contenant autant de données que vous le souhaitez pour un compte, puis publiez-les sur les réseaux publicitaires.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo ! (Comptes Japan Ads et Yandex uniquement) Saisissez les données des composants individuels directement dans l’interface. Pour la plupart des types de campagnes et d’annonces, vous pouvez créer des données au niveau de la campagne, du groupe d’annonces et des mots-clés individuels, de l’emplacement et des niveaux d’annonces.

      Certains types de campagnes et d’annonces nécessitent toutefois des workflows uniques. Consultez les instructions de configuration [[!DNL Microsoft Advertising] campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md), [[!DNL Google Ads] annonces de recherches dynamiques](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md), [[!DNL Google Ads] campagnes de performances maximales](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md) et [[!DNL Google Ads] campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md).

   1. (Comptes de suivi [!DNL Naver] uniquement) Chargez des [fichiers de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) avec des données pour répliquer les campagnes, groupes publicitaires et mots-clés existants dans Search, Social et Commerce sans les publier sur [!DNL Naver].

1. Configurez le suivi de toutes les publicités pour lesquelles Adobe Advertising suivra les conversions :

   1. (Annonceurs avec le service de suivi des conversions Adobe Advertising) Si nécessaire, [configurez le suivi des clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) pour les publicités et éventuellement pour les mots-clés, les emplacements et les extensions de publicité en générant et en chargeant des URL de suivi des clics Search, Social et Commerce.

      Pour [!DNL Google Ads] campagnes Performance Max, configurez l’ensemble du tracking dans les [paramètres de tracking de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Pour les campagnes de suivi uniquement, vous devez plutôt générer des URL de destination à l’aide de feuilles d’envoi groupé, puis ajouter les URL de destination générées aux entités pertinentes à l’aide de l’éditeur natif du réseau publicitaire.

   1. Configurez le suivi des conversions. Selon la mise en œuvre, cela peut impliquer l’ajout de balises de suivi des conversions aux pages web de l’annonceur et/ou la configuration d’un flux de données quotidien pour les données de conversion que l’annonceur a collectées séparément.

      Si vous utilisez le service de suivi des conversions d’Adobe Advertising, vous pouvez [générer des balises de suivi des conversions](/help/search-social-commerce/tools/conversion-tag-generate.md) dans Search, Social et Commerce ou utiliser des [balises de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html?lang=fr) (anciennement Adobe Experience Platform Launch).

   1. Validez les données qui font l’objet d’un suivi.

   Pour plus d’informations sur la configuration du tracking, consultez le chapitre sur le tracking.

1. (Annonceurs avec Adobe Analytics) [Intégrez Adobe Advertising et Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=fr) afin qu’ils puissent échanger des données.

1. (Pour permettre à Search, Social et Commerce d’optimiser les enchères, les budgets de campagne et/ou les cibles de stratégie d’enchères de campagne ; [types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) uniquement) [Affectez la campagne à un portefeuille](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Si le portefeuille n’est pas déjà lancé (optimisation des offres et/ou des budgets), laissez la fonctionnalité d’optimisation rassembler suffisamment de données pour pouvoir créer des modèles de coût et de chiffre d’affaires afin d’établir les performances de base du portefeuille avant de le lancer.

   Si le portfolio est déjà lancé, alors activez l’apprentissage pour le portfolio. Pour plus d’informations, voir « Ajuster les stratégies de portefeuille ». Vous devez vous attendre à ce que le portefeuille soit volatile après l’ajout de nouvelles campagnes, tandis que la fonctionnalité d’optimisation rassemble des données sur les unités d’enchères de la campagne. Les enchères s’ajustent automatiquement d’une à trois semaines.

   Pour plus d’informations sur les portfolios, consultez le Guide d’optimisation , disponible dans Search, Social et Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (Si de nouvelles conversions font l’objet d’un suivi pour l’annonceur) [Rendez les conversions disponibles](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) pour les rapports, les vues de gestion de campagne et les objectifs du portfolio.

1. Pour chaque campagne, vérifiez que Search, Social et Commerce reçoit les données sur les clics et les coûts du réseau publicitaire, puis validez les données sur les recettes affichées dans Search, Social et Commerce avec les propres données sur les recettes de l’annonceur.

1. (Facultatif) Automatisez la création de rapports en configurant des modèles de rapport, des flux de feuilles de calcul et la diffusion FTP des rapports planifiés.

   Pour obtenir des instructions détaillées, reportez-vous au chapitre « Rapports ».

>[!MORELIKETHIS]
>
>* [À propos de la gestion des campagnes dans Search, Social et Commerce](campaign-management-about.md)
>* [Surveillez et gérez les performances de vos campagnes réseau publicitaire](monitor-performance-campaigns.md)
>* [Données de conversion Google Ads dans Search, Social et Commerce](google-conversion-data.md)
>* [Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md)
