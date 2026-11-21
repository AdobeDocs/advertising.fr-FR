---
title: Présentation de l’implémentation de Search, Social et Commerce
description: Découvrez le workflow général de lancement et de gestion d’un portfolio.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%
---
# Présentation de l’implémentation de Search, Social et Commerce

[!DNL Adobe] ou l&#39;une de ses agences affiliées travaille avec chaque annonceur pour lancer ses portfolios publicitaires en ligne et pour suivre toutes les campagnes publicitaires supplémentaires. Après le lancement initial, d&#39;autres tâches continues assurent que les objectifs de l&#39;annonceur continueront d&#39;être atteints.

Voici le workflow général d’implémentation et d’utilisation de Search, Social et Commerce.

## Lancement initial

[!DNL Adobe] et/ou votre agence travaille avec vous pour effectuer les opérations suivantes :

1. Évaluez vos objectifs commerciaux de haut niveau et élaborez des stratégies pour les atteindre :

   1. Identifiez votre modèle d&#39;affaires et vos objectifs de marketing.

   1. Identification des exigences en matière de suivi des conversions

   1. Analysez vos structures de compte publicitaire en ligne existantes.

   1. Identifiez les mesures d’optimisation du portefeuille et de création de rapports.

1. (Utilisateurs administrateurs ou gestionnaires de comptes) Configurez des comptes d’administration :

   1. Configurez le compte de l’annonceur. Si une agence gère les données de l’annonceur, le compte de l’annonceur doit être associé au compte de l’agence.

   1. (Si nécessaire) Créez des comptes utilisateur pour que l’annonceur puisse afficher et gérer ses données de campagne et générer des rapports.

   Contactez votre administrateur ou administratrice pour configurer l’accès à l’aide de Adobe Admin Console et des profils de produit appropriés. Voir « [Administration des utilisateurs pour Search, Social et Commerce](/help/search-social-commerce/user-administration.md) ».

1. Synchronisez avec des campagnes ou créez des campagnes pour chacun de vos comptes de réseau publicitaire :

   * Pour les comptes connectés à l’API, [créez les détails du compte](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account) dans [!UICONTROL Manage] > [!UICONTROL Accounts], terminez l’authentification spécifique au réseau, configurez les options de suivi et activez le compte.

   * Pour les comptes sans prise en charge de l’API, suivez le workflow [chargement de données](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md) ou [compte de suivi uniquement](/help/search-social-commerce/manage/accounts/template-account-manage.md), selon le cas. Ces comptes ne se synchronisent pas avec le réseau publicitaire et ne prennent pas en charge l’optimisation du portfolio.

   * Si les comptes ne contiennent pas déjà de données de campagne, ajoutez des campagnes, des groupes publicitaires, des mots-clés, des annonces et des emplacements dans Search, Social et Commerce ou dans le réseau publicitaire.

     Pour obtenir la liste de contrôle détaillée de la configuration, voir « [Configuration de comptes et de campagnes de réseau publicitaire](campaign-implementation-overview.md) ». Pour les types de campagne pris en charge, utilisez [!UICONTROL Manage] > [!UICONTROL Campaigns] pour [créer et gérer des campagnes](/help/search-social-commerce/manage/campaigns/campaign-manage.md).

1. Configurez le suivi de toutes les publicités pour lesquelles vous souhaitez qu’Adobe Advertising suive les conversions :

   1. (Si nécessaire) [Configurez le suivi des clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) pour les publicités, et éventuellement pour les mots-clés, [!DNL Google Ads] emplacements et [!DNL Google Ads] extensions en générant et en chargeant des URL de suivi des clics.

      Les URL de suivi des clics pour les annonceurs qui utilisent le service de suivi de conversion basé sur les pixels d’Adobe Advertising incluent une redirection vers les serveurs [!DNL Adobe].

   1. [Configurer le suivi des conversions](/help/search-social-commerce/tracking/conversion-tracking-about.md). Selon la mise en œuvre, cela peut impliquer l’ajout de balises de suivi des conversions aux pages web appropriées et/ou la configuration d’une goutte de flux quotidienne pour les données de conversion que vous avez collectées à l’aide de votre propre méthode. Vous pouvez [générer des balises de suivi des conversions Adobe Advertising](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md) depuis [!UICONTROL Goals] > [!UICONTROL Conversions].

      Pour plus d’informations, voir « [À propos du suivi pour Search, Social et Commerce](/help/search-social-commerce/tracking/tracking-about.md) ».

1. Configurez les intégrations à des produits supplémentaires :

   1. (Annonceurs avec Adobe Analytics et/ou Adobe Audience Manager) Configurez des intégrations entre les différents comptes afin qu’Adobe Advertising puisse échanger des données avec eux.

      Consultez le guide sur les « [Intégrations à CX Enterprise](/help/integrations/home.md) ».

   1. (Annonceurs avec [!DNL Google Analytics]) Synchronisez les mesures de conversion pour une combinaison de compte, propriété et vue [!DNL Google Analytics] à des fins d’optimisation et de création de rapports.

      Cette configuration utilise l’interface utilisateur héritée. Voir « [À propos de la synchronisation [!DNL Google Analytics] des mesures de conversion](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md) » et, si nécessaire, [passer à l’interface héritée](ui-switch.md).

1. (Facultatif) Configurez et lancez des portfolios :

   1. Dans [!UICONTROL Goals] > [!UICONTROL Conversions], [vérifiez les mesures de conversion et rendez les mesures requises visibles](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available). Dans [!UICONTROL Goals] > [!UICONTROL Objectives], [créez ou sélectionnez un objectif](/help/search-social-commerce/goals/objectives/objective-about.md) pour l’optimisation.

   1. Dans [!UICONTROL Manage] > [!UICONTROL Portfolios], [créez des portfolios](/help/search-social-commerce/manage/portfolios/portfolio-create.md) configurés pour atteindre vos objectifs et objectifs commerciaux, avec les [campagnes éligibles appropriées](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). [Activez les portfolios](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) pour collecter et modéliser les données. L’équipe d’implémentation rassemble et valide ensuite les données relatives aux clics et au chiffre d’affaires pendant au moins 14 jours, puis valide les paramètres du portfolio.

      >[!NOTE]
      >
      >Les services Search, Social et Commerce effectuent toujours le suivi et génèrent des rapports sur les données des campagnes qui ne sont pas affectées aux portfolios, mais ils ne les optimisent pas.

   1. Une fois qu’il y a suffisamment de données disponibles pour créer une ligne de base, l’équipe peut [modifier le statut du portefeuille en optimisé](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), ce qui permet à Search, Social et Commerce d’optimiser les enchères, les budgets et/ou les cibles des stratégies d’enchères pour le portefeuille, en fonction du type de portefeuille et des stratégies d’enchères de la campagne.

   Voir « [À propos des portfolios](/help/search-social-commerce/manage/portfolios/portfolio-about.md) » pour la prise en charge de l’optimisation et les statuts de portfolio.

1. Surveillez les performances de vos portefeuilles :

   1. Utilisez [!UICONTROL Dashboard] > [!UICONTROL Overview] pour [examiner les tendances du portfolio](/help/search-social-commerce/dashboard/dashboard-overview.md) et [afficher les détails des performances du portfolio](/help/search-social-commerce/manage/portfolios/portfolio-details.md) afin d’étudier les résultats et la précision du modèle.

   1. [Configurez des alertes personnalisées](/help/search-social-commerce/common-tasks/alerts-manage.md) et [générez des rapports personnalisés](/help/search-social-commerce/reports/management/report-manage.md) pour la surveillance des performances. Si nécessaire, automatisez la création de rapports à l’aide de [modèles de rapports](/help/search-social-commerce/reports/report-templates-manage.md) et de [flux de feuilles de calcul](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Pour plus d’informations, voir « [Surveiller les performances des campagnes et des portefeuilles](/help/search-social-commerce/manage/manage-about.md#monitor-performance) ».

1. (Facultatif) Configurez vos [vues de données de performances](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) pour afficher les données que vous souhaitez afficher.

## Tâches en cours

Après le lancement initial, les tâches en cours suivantes sont requises. Selon vos conditions d&#39;engagement, [!DNL Adobe], une agence affiliée ou l&#39;annonceur effectue ces tâches :

* Continuez à surveiller et à analyser les performances de chaque portfolio en affichant les alertes, les données de performances de chaque portfolio et de ses campagnes de composants, les rapports personnalisables et les simulations (de certains rôles).

* Ajustez les différentes stratégies et paramètres que vous utilisez pour gérer l&#39;ensemble de portefeuilles, si nécessaire, en fonction des performances réelles et prévues du portefeuille et des opportunités de croissance :

  * Ajustez les budgets, les objectifs et les autres paramètres du portefeuille.

  * Ajustez les structures de compte/campagne pour tenir compte des modifications apportées à la stratégie marketing.

  * Ajouter/suspendre/supprimer des composants de campagne. Cela peut inclure le développement d’ensembles de mots-clés basés sur l’analyse des termes de recherche, ainsi que le test de copies d’annonces et de pages de destination.

  * Mettez à jour les stratégies de ciblage géographique et de site en fonction de rapports de performances avancés.

  * (Facultatif) Ajoutez des contraintes d’enchères à des mots-clés de recherche individuels ou à tous les mots-clés d’un groupe publicitaire, d’une campagne ou d’un portfolio.

  * Ajoutez de nouveaux portefeuilles.

Pour obtenir des instructions sur la surveillance des campagnes et des portfolios et l’ajustement de leurs paramètres, voir « [À propos de la gestion des campagnes et des portfolios](/help/search-social-commerce/manage/manage-about.md) » et « [Modifier les détails du portfolio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md) ».
