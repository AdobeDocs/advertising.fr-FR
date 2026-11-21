---
title: À propos de la gestion des campagnes et des portfolios
description: Découvrez comment les comptes de réseau publicitaire, les campagnes, le tracking et l’optimisation des portefeuilles fonctionnent ensemble, et comment surveiller et améliorer les performances.
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%
---
# À propos de la gestion des campagnes et des portfolios

*Fonctionnalité Beta*

Search, Social et Commerce rassemblent dans une seule interface la gestion des campagnes, le reporting des performances et l&#39;optimisation des portefeuilles. Selon le réseau publicitaire et le type de campagne, vous pouvez synchroniser les données de la campagne, créer et modifier les composants de la campagne, effectuer le suivi des conversions et optimiser les enchères, les budgets ou les cibles de la stratégie d’enchères. Consultez [inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) pour connaître les fonctionnalités disponibles pour chaque réseau publicitaire.

Le menu [!UICONTROL Manage] permet d’accéder à vos comptes, campagnes, groupes publicitaires, annonces, mots-clés, groupes de produits et portfolios. Vos autorisations déterminent les vues et actions disponibles. Pour l’organisation complète du menu, consultez « [Organisation de l’interface utilisateur](/help/search-social-commerce/getting-started/user-interface.md) ».

## Comment les comptes, les campagnes et les portfolios s’intègrent

* **Les comptes de réseau publicitaire** connectent les données de votre annonceur à Search, Social et Commerce. [Les types de comptes](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) incluent les comptes synchronisés par le biais d’une connexion API, les comptes pour lesquels vous chargez des données et les comptes de suivi basés uniquement sur des modèles. Le type de compte détermine si vous pouvez synchroniser les données, gérer des campagnes ou utiliser l’optimisation du portfolio.

* **Les campagnes** contiennent les annonces et autres composants utilisés pour diffuser vos annonces. Pour les types de campagne pris en charge, vous pouvez [créer et gérer des campagnes](/help/search-social-commerce/manage/campaigns/campaign-manage.md) et leurs composants à partir des vues [!UICONTROL Manage]. Vous pouvez également utiliser [feuilles d’envoi groupé](/help/search-social-commerce/set-up/bulksheets/about.md) pour les opérations en bloc prises en charge.

* **Les portfolios** regroupent les campagnes éligibles afin de les optimiser en fonction d’un objectif commercial commun et d’un budget ou d’une cible de performances. Une campagne ne peut appartenir qu’à un seul portfolio et toutes les campagnes d’un portfolio doivent utiliser la même devise. Voir « [À propos des portefeuilles](/help/search-social-commerce/manage/portfolios/portfolio-about.md) ».

L’affectation de Portfolio est facultative. Vous pouvez effectuer le suivi et générer des rapports sur les campagnes sans les affecter à un portfolio. Tous les réseaux publicitaires, types de campagne ou stratégies d’enchères ne prennent pas en charge l’optimisation des portefeuilles.

## Synchroniser les données de campagne

Pour les comptes connectés par le biais d’une API, Search, Social et Commerce récupère la structure de campagne et les données de performances prises en charge à partir du réseau publicitaire. Les modifications que vous apportez aux composants de campagne pris en charge dans Search, Social et Commerce sont envoyées au réseau publicitaire.

Si nécessaire, vous pouvez [demander une synchronisation manuelle](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md). Si un compte cesse la synchronisation, vérifiez son [authentification et son statut d&#39;accès](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status).

Les comptes de chargement de données et les comptes de suivi uniquement ne se synchronisent pas avec le réseau publicitaire. Suivez le workflow pour le [type de compte](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) afin de fournir des données de campagne et de performances.

## Configurer le suivi et l’optimisation

[Le tracking](/help/search-social-commerce/tracking/tracking-about.md) relie l’activité de campagne aux conversions qui comptent pour votre entreprise. Selon votre implémentation, les données de conversion peuvent provenir de balises Adobe Advertising, d’une intégration d’Adobe Analytics, d’un suivi réseau ou de flux de données. Configurez le suivi des clics et des conversions selon les besoins de votre implémentation et validez les données avant de les utiliser pour l’optimisation.

Dans [!UICONTROL Goals] > [!UICONTROL Conversions], vous pouvez [vérifier les mesures de conversion suivies pour l’annonceur et contrôler leur visibilité](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md). Utilisez les mesures appropriées dans vos [objectifs](/help/search-social-commerce/goals/objectives/objective-about.md).

Pour activer l’optimisation du portfolio, [créez un portfolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md), attribuez un objectif et des campagnes éligibles, puis configurez ses paramètres de dépenses et d’optimisation. Un portefeuille actif rassemble et modélise des données de performances. Lorsque les données et les paramètres sont prêts, [modifiez le statut du portfolio en optimisé](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) pour commencer l&#39;optimisation. Les actions effectuées dépendent du type de portefeuille et des [stratégies d’enchères de la campagne](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

Pour la séquence de configuration détaillée, voir « [Configurer des comptes et des campagnes de réseau publicitaire](/help/search-social-commerce/getting-started/campaign-implementation-overview.md) ».

## Surveiller les performances des campagnes et des portefeuilles {#monitor-performance}

L’équipe du compte, l’agence ou l’annonceur est chargé de surveiller les performances et d’effectuer des ajustements, conformément aux termes du contrat de service. Régulièrement :

* Examinez les performances de la campagne et du compte dans les vues [!UICONTROL Manage]. [Personnalisez les colonnes, les filtres et les périodes](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) pour vous concentrer sur les mesures et les entités importantes.

* Utilisez [!UICONTROL Dashboard] > [!UICONTROL Overview] pour [surveiller les tendances et les changements de performances du portfolio](/help/search-social-commerce/dashboard/dashboard-overview.md).

* Consultez [alertes personnalisées](/help/search-social-commerce/common-tasks/alerts-manage.md) pour connaître les conditions qui nécessitent une enquête.

* [Générez des rapports](/help/search-social-commerce/reports/management/report-manage.md) pour les performances des campagnes, des mots-clés, des annonces et des portefeuilles. Pour les portefeuilles, [consultez les détails des performances](/help/search-social-commerce/manage/portfolios/portfolio-details.md), y compris les performances réelles et la précision du modèle.

* Le cas échéant, utilisez des [simulations](/help/search-social-commerce/plan/simulations/simulation-about.md) pour évaluer les effets prévus de différents niveaux de dépenses.

* Examinez les différences entre vos conversions signalées et les données source. Consultez les conseils relatifs aux données de conversion [!DNL Google Ads] et [!DNL Microsoft Advertising] dans les liens connexes.

## Ajuster des campagnes et des portfolios

En fonction des performances et des changements de vos objectifs commerciaux, vous devrez peut-être :

* Modifiez les paramètres de la campagne, créez ou mettez en pause des composants de campagne, affinez les ensembles de mots-clés ou testez différentes publicités. Les actions disponibles dépendent du réseau publicitaire et du type de campagne.

* Examinez le ciblage géographique, d’audience et d’emplacement à l’aide des vues et des rapports de gestion pertinents.

* [Modifier les affectations de campagne](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) lorsqu’une campagne doit être optimisée avec un portfolio différent. L’affectation d’une campagne à un autre portfolio la supprime de son portfolio précédent.

* [Modifiez les paramètres du portfolio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md), y compris l’objectif, la stratégie de dépense, les contraintes ou les contrôles d’optimisation, comme le permet votre profil de produit.

* Consultez [l&#39;historique des modifications](/help/search-social-commerce/reports/history-logs.md) lorsque vous recherchez des modifications de performances.

>[!MORELIKETHIS]
>
>* [Configurer des comptes et des campagnes de réseau publicitaire](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md)
>* [[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
