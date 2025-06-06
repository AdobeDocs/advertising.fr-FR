---
title: Présentation de l’implémentation des comptes et campagnes de réseau publicitaire
description: Découvrez les tâches impliquées dans la configuration, la synchronisation et la gestion de vos comptes réseau publicitaires.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Présentation de l’implémentation des comptes et campagnes de réseau publicitaire

Adobe travaille avec chaque annonceur pour configurer ses comptes et campagnes de réseau publicitaire. Cela inclut la configuration de Search, Social et Commerce pour se connecter et se synchroniser avec les comptes de l’annonceur, la création de campagnes et de composants de campagne selon les besoins, la configuration du suivi des publicités des composants, l’ajout facultatif des campagnes aux portefeuilles pour permettre à Search, Social et Commerce d’optimiser l’offre sur les publicités et la validation des données initiales sur le coût, le clic et les recettes.

Une fois qu’une campagne est activée et éventuellement ajoutée à un portfolio, l’équipe de gestion de compte d’Adobe, l’équipe de l’agence ou l’annonceur (selon les conditions du contrat de niveau de service) devra surveiller chaque campagne et modifier les composants et paramètres pertinents nécessaires pour atteindre les objectifs de l’annonceur.

Cette page contient des informations sur tous les types de compte, y compris sur la configuration de la structure de campagne pour les comptes synchronisés. Pour obtenir des instructions supplémentaires sur la configuration des comptes de suivi uniquement pour [!DNL Naver], voir &quot;[Implémentation [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)&quot;.

## Tâches de configuration initiales des comptes et campagnes

[!DNL Adobe] et/ou votre agence travaillera avec vous comme suit :

1. (Nouveaux comptes publicitaires) Configurez les comptes administratifs :

   1. Configurez le compte de l’annonceur.

   1. (Si nécessaire) Créez des comptes utilisateurs pour que l’annonceur puisse afficher et gérer les données de campagne et générer des rapports.

1. (Certains réseaux publicitaires) Accédez à chaque compte via Search, Social et Commerce à l’aide de l’API du réseau publicitaire et de l’interface utilisateur Search, Social et Commerce.

1. Pour chaque compte de réseau publicitaire :

   1. (Si nécessaire) Configurez le compte sur le réseau publicitaire.

   1. Intégrez-le au compte en [créant un enregistrement de compte correspondant](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) dans Search, Social et Commerce contenant les informations d’identification d’accès au compte et les options de suivi, puis définissez l’état du compte sur activé.

      Search, Social et Commerce se synchronise ensuite avec le réseau publicitaire. Si le compte contient déjà des données de campagne, les données sont disponibles dans environ 24 heures.

   1. ([Types d’annonces que vous pouvez créer/modifier](/help/search-social-commerce/introduction/supported-inventory.md) dans Search, Social et Commerce) Si le compte ne contient pas déjà de données de campagne, créez la structure de campagne et les composants de campagne à partir de Search, Social et Commerce en appliquant l’une des méthodes suivantes disponibles pour le type d’annonce :

      * (Publicités Google, Microsoft Advertising, Yahoo! Publicités et comptes Yandex uniquement) Configurez un processus [automatisé pour créer des publicités dynamiques et des mots-clés ciblés sur chaque élément de votre inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) en fonction d’un modèle de publicité spécifique au réseau que vous créez et du contenu des fichiers de données d’inventaire que vous chargez vers un emplacement FTP.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads, et comptes Yandex uniquement) Téléchargez les [fichiers de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) contenant autant de données que vous le souhaitez pour un compte, puis publiez-les sur les réseaux publicitaires.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads et comptes Yandex uniquement) Saisissez les données de composants individuels directement dans l’interface. Pour la plupart des types de campagne et d’annonce, vous pouvez créer des données au niveau de la campagne, du groupe d’annonces, du mot-clé individuel, de l’emplacement et de l’annonce.

      Certains types de campagne et d’annonce nécessitent toutefois des workflows uniques. Reportez-vous aux instructions de configuration des [[!DNL Microsoft Advertising] campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md), des [[!DNL Google Ads] publicités de recherche dynamique](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md), des [[!DNL Google Ads] campagnes de performances max](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md) et des [[!DNL Google Ads] campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md).

   1. ([!DNL Naver] comptes de suivi uniquement) Téléchargez des [fichiers de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) avec des données pour répliquer les campagnes, les groupes publicitaires et les mots-clés existants dans Search, Social et Commerce sans les publier dans [!DNL Naver].

1. Configurez le suivi de toutes les publicités pour lesquelles Adobe Advertising effectuera le suivi des conversions :

   1. (Publicitaires avec service de suivi de conversion d’Adobe Advertising) Si nécessaire, [ configurez le suivi des clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) pour les publicités et, éventuellement, pour les mots-clés, les emplacements et les extensions de publicité en générant et en chargeant les URL de suivi des clics Search, Social et Commerce.

      Pour les campagnes [!DNL Google Ads] de performance maximale, configurez le suivi dans les [paramètres de suivi de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Pour les campagnes de suivi uniquement, vous devez générer des URL de destination à l’aide de feuilles d’envoi groupées, puis ajouter les URL de destination générées aux entités appropriées à l’aide de l’éditeur natif du réseau publicitaire.

   1. Configurez le suivi des conversions. Selon l’implémentation, cela peut impliquer l’ajout de balises de suivi de conversion aux pages web de l’annonceur et/ou la configuration d’une baisse de flux quotidienne pour les données de conversion que l’annonceur a collectées séparément.

      Si vous utilisez le service de suivi de conversion Adobe Advertising, vous pouvez générer des balises de suivi de conversion [ dans Search, Social, &amp; Commerce ](/help/search-social-commerce/tools/conversion-tag-generate.md) ou [ en utilisant Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html?lang=fr).

   1. Validez les données suivies.

   Pour plus d’informations sur la configuration du suivi, reportez-vous au chapitre &quot;Tracking&quot;.

1. (Publicitaires avec Adobe Analytics) [Intégrez Adobe Advertising et Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=fr) afin qu’ils puissent exchange des données.

1. (Pour permettre à Search, Social et Commerce d’optimiser les offres, les budgets de campagne et/ou les cibles de stratégie d’offre de campagne ; [types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) uniquement) [Affectez la campagne à un portefeuille](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Si le portefeuille n’est pas déjà lancé (optimisation des offres et/ou des budgets), laissez la fonctionnalité d’optimisation rassembler suffisamment de données pour créer des modèles de coûts et de recettes afin que vous puissiez établir les performances de base du portefeuille avant de le lancer.

   Si le portfolio est déjà lancé, activez l’apprentissage pour le portfolio. Pour plus d’informations, voir &quot;Ajustement des stratégies de portefeuille&quot;. Une fois de nouvelles campagnes ajoutées, vous devez vous attendre à ce que le portefeuille soit volatile, tandis que la fonctionnalité d’optimisation rassemble les données sur les unités d’offre de la campagne. L’offre s’ajuste automatiquement dans un délai de une à trois semaines.

   Pour plus d’informations sur les portefeuilles, consultez le Guide d’optimisation disponible dans Search, Social et Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (Si de nouvelles conversions sont suivies pour l’annonceur) [Rendez les conversions disponibles](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) pour les rapports, les vues de gestion de campagne et les objectifs de portefeuille.

1. Pour chaque campagne, vérifiez que Search, Social et Commerce reçoit les données de clics et de coûts du réseau publicitaire et validez les données de recettes affichées dans Search, Social et Commerce avec les propres données de recettes de l’annonceur.

1. (Facultatif) Automatisez la création de rapports en configurant des modèles de rapport, des flux de feuille de calcul et la distribution FTP des rapports planifiés.

   Pour obtenir des instructions, reportez-vous au chapitre sur les rapports.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de campagnes dans Search, Social et Commerce](campaign-management-about.md)
>* [ Surveillez et gérez les performances de vos campagnes réseau d’annonces ](monitor-performance-campaigns.md)
>* [Données de conversion Google Ads dans Search, Social et Commerce](google-conversion-data.md)
>* [Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md)
