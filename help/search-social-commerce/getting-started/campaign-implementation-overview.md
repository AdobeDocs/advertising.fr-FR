---
title: Configurer des comptes et des campagnes de réseau publicitaire
description: Suivez le workflow de configuration pour les connexions au réseau publicitaire, les campagnes, le suivi, les mesures de conversion et l’optimisation facultative du portfolio.
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%
---
# Configurer des comptes et des campagnes de réseau publicitaire

*Fonctionnalité Beta*

[!DNL Adobe] et votre agence travaillent avec vous pour connecter vos comptes de réseau publicitaire, préparer des campagnes, configurer le suivi et valider les données de performances. Si vous souhaitez que Search, Social et Commerce optimisent les campagnes éligibles, le workflow inclut également la configuration du portfolio.

Cette liste de contrôle fournit les détails du compte et de la campagne pour le workflow d’implémentation [plus large](implemention-overview.md). Les tâches que vous pouvez effectuer dépendent de vos autorisations et de la fonctionnalité [prise en charge pour chaque type de réseau publicitaire et de campagne](/help/search-social-commerce/introduction/supported-inventory.md).

## Configurer le workflow

1. **Confirmez les conditions d&#39;accès et de compte requises.**

   Contactez votre administrateur ou administratrice pour confirmer l’accès à l’annonceur approprié et les autorisations requises pour vos tâches. Voir « [Administration des utilisateurs pour Search, Social et Commerce](/help/search-social-commerce/user-administration.md) ».

   Si nécessaire, créez le compte du réseau publicitaire sur le site web du réseau publicitaire. La création d’un enregistrement de compte dans Search, Social et Commerce n’entraîne pas la création d’un compte sur le réseau publicitaire.

1. **Connectez ou enregistrez chaque compte réseau publicitaire.**

   Dans [!UICONTROL Manage] > [!UICONTROL Accounts], utilisez le workflow pour le [type de compte](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) :

   * **Connexion API :** [Créez les détails du compte](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account), terminez l’authentification spécifique au réseau, configurez les options de suivi et activez le compte. Vérifiez son [authentification et son statut d’accès](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status) ; une authentification réussie ne signifie pas nécessairement que toutes les autorisations requises ont été accordées.

   * **Chargement de données :** [Créez les détails du compte et chargez les données de campagne et de performance](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md). Ces comptes ne se synchronisent pas avec le réseau publicitaire et ne prennent pas en charge l’optimisation du portfolio.

   * **[!DNL Naver]suivi uniquement :** suivez le workflow du compte de suivi uniquement [](/help/search-social-commerce/manage/accounts/template-account-manage.md). Utilisez des feuilles d’envoi groupé pour générer des URL de tracking et les appliquer dans l’éditeur du réseau publicitaire ; le compte ne se synchronise pas et ne prend pas en charge l’optimisation du portfolio.

1. **Examinez ou créez une structure de campagne.**

   Pour les comptes connectés à l’API , passez en revue les campagnes synchronisées et leurs composants. [Demander une synchronisation manuelle](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md) si nécessaire.

   Pour les types de campagne pris en charge, utilisez [!UICONTROL Manage] > [!UICONTROL Campaigns] pour [créer ou modifier des campagnes](/help/search-social-commerce/manage/campaigns/campaign-manage.md). Créez les [groupes publicitaires](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md), [annonces](/help/search-social-commerce/manage/ads/ad-manage.md) et autres composants pris en charge requis. Vous pouvez également utiliser [feuilles d’envoi groupé](/help/search-social-commerce/set-up/bulksheets/about.md) pour les opérations en bloc prises en charge.

   Effectuez toute configuration spécifique au réseau requise avant d’activer les campagnes. Gérez les composants non pris en charge dans la propre interface du réseau publicitaire.

1. **Configurer et valider le suivi avant le lancement.**

   Sélectionnez la [méthode de suivi des conversions](/help/search-social-commerce/tracking/conversion-tracking-about.md) qui correspond à votre implémentation. Si nécessaire, [générez et appliquez des URL de suivi des clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) et [générez des balises de suivi des conversions](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md).

   Configurez les [intégrations](/help/integrations/home.md) ou [flux de conversion](/help/search-social-commerce/tracking/tracking-about.md) requis et vérifiez que les conversions peuvent être attribuées comme prévu. Pour les campagnes de tracking uniquement, appliquez les URL de tracking générées dans l’éditeur du réseau publicitaire.

1. **Vérifier les mesures de conversion.**

   Dans [!UICONTROL Goals] > [!UICONTROL Conversions], [examinez les mesures suivies et rendez les mesures requises visibles](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available) pour les vues de gestion, les rapports et les objectifs. Modifiez les noms d’affichage si nécessaire pour distinguer les mesures.

1. **(Facultatif) Préparer l’optimisation du portfolio.**

   Vérifiez que les campagnes et leurs stratégies d’enchères sont [éligibles à l’optimisation du portefeuille](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

   [Créez ou sélectionnez un objectif](/help/search-social-commerce/goals/objectives/objective-about.md) qui utilise les mesures de conversion appropriées. Dans [!UICONTROL Manage] > [!UICONTROL Portfolios], [créez un portefeuille](/help/search-social-commerce/manage/portfolios/portfolio-create.md) ou [modifiez un portefeuille existant](/help/search-social-commerce/manage/portfolios/portfolio-edit.md) avec l’objectif, la stratégie de dépense et les paramètres d’optimisation requis.

   [Affectez les campagnes au portfolio](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). Chaque campagne ne peut appartenir qu’à un seul portfolio et toutes les campagnes d’un portfolio doivent utiliser la même devise.

1. **Validez les données de la campagne et établissez une ligne de base de performances.**

   Vérifiez que les données relatives au coût, aux clics et à la conversion sont disponibles pour chaque campagne. Comparez les données de conversion avec la source appropriée, y compris [!DNL Google Ads] et [!DNL Microsoft Advertising] le cas échéant. Utilisez des périodes et des paramètres d’attribution cohérents lors de la comparaison des rapports.

   Pour un nouveau portfolio, [activez-le](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) pour collecter et modéliser les données. Validez les données et les paramètres du portfolio avant d’activer l’optimisation.

1. **(Facultatif) Optimisation du portfolio Launch.**

   Lorsque le portfolio est prêt, [modifiez son statut en optimisé](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), en examinant les conditions préalables et les messages de confirmation. Search, Social et Commerce optimise ensuite le portfolio en fonction de ses paramètres et des stratégies d’enchères de campagne prises en charge.

1. **Configurez la surveillance et la création de rapports continues.**

   [Personnalisez vos vues de données](/help/search-social-commerce/common-tasks/data-views/data-views-about.md), [configurez des alertes personnalisées](/help/search-social-commerce/common-tasks/alerts-manage.md) et [générez des rapports planifiés](/help/search-social-commerce/reports/management/report-manage.md). Si nécessaire, automatisez la création de rapports à l’aide de [modèles de rapports](/help/search-social-commerce/reports/report-templates-manage.md) et de [flux de feuilles de calcul](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Continuez à [surveiller et à ajuster les campagnes et les portfolios](/help/search-social-commerce/manage/manage-about.md#monitor-performance) après le lancement.

>[!MORELIKETHIS]
>
>* [Aperçu de l’implémentation de Search, Social et Commerce](implemention-overview.md)
>* [À propos de la gestion des campagnes et des portfolios](/help/search-social-commerce/manage/manage-about.md)
>* [[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
