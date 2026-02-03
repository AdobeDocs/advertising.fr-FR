---
title: Présentation de l’implémentation de Search, Social et Commerce
description: Découvrez le workflow général de lancement et de gestion d’un portfolio.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# Présentation de l’implémentation de Search, Social et Commerce

[!DNL Adobe] ou l&#39;une de ses agences affiliées travaille avec chaque annonceur pour lancer ses portefeuilles de publicité en ligne et pour suivre toutes les campagnes publicitaires supplémentaires. Après le lancement initial, d&#39;autres tâches continues assurent que les objectifs de l&#39;annonceur continueront d&#39;être atteints.

Voici le workflow général d’implémentation et d’utilisation de Search, Social et Commerce.

## Lancement initial

[!DNL Adobe] et/ou votre agence travaillent avec vous pour :

1. Évaluez vos objectifs commerciaux de haut niveau et élaborez des stratégies pour les atteindre :

   1. Identifiez votre modèle d&#39;affaires et vos objectifs de marketing.

   1. Identification des exigences en matière de suivi des conversions

   1. Analysez vos structures de compte publicitaire en ligne existantes.

   1. Identifiez les mesures d’optimisation du portefeuille et de création de rapports.

1. (Utilisateurs administrateurs ou gestionnaires de comptes) Configurez des comptes d’administration :

   1. Configurez le compte de l’annonceur. Si une agence gère les données de l’annonceur, le compte de l’annonceur doit être associé au compte de l’agence.

   1. (Si nécessaire) Créez des comptes utilisateur pour que l’annonceur puisse afficher et gérer ses données de campagne et générer des rapports.

   Pour plus d’informations sur la configuration des comptes, consultez le chapitre d’aide sur « Admin ».

1. Synchronisez avec des campagnes ou créez des campagnes pour chacun de vos comptes de réseau publicitaire :

   * Effectuez une synchronisation avec le compte a) en créant un enregistrement de compte correspondant dans Search, Social et Commerce qui contient les informations d’identification d’accès au compte et les options de suivi, et b) en définissant le statut du compte sur activé.

   * Si les comptes ne contiennent pas déjà de données de campagne, ajoutez des campagnes, des groupes publicitaires, des mots-clés, des annonces et des emplacements dans Search, Social et Commerce ou dans le réseau publicitaire.

     Pour plus d’informations sur la configuration des campagnes de recherche, consultez le chapitre d’aide sur la « Gestion de campagne ».

1. Configurez le suivi de toutes les publicités pour lesquelles vous souhaitez qu’Adobe Advertising suive les conversions :

   1. (Si nécessaire) Configurez le suivi des clics pour les publicités et éventuellement pour les mots-clés, les emplacements de [!DNL Google Ads] et les extensions de [!DNL Google Ads] en générant et en chargeant des URL de suivi des clics.

      Les URL de suivi des clics pour les annonceurs qui utilisent le service de suivi de conversion basé sur les pixels d’Adobe Advertising incluent une redirection vers les serveurs [!DNL Adobe].

   1. Configurez le suivi des conversions. Selon la mise en œuvre, cela peut impliquer l’ajout de balises de suivi des conversions aux pages web appropriées et/ou la configuration d’une goutte de flux quotidienne pour les données de conversion que vous avez collectées à l’aide de votre propre méthode.

      Pour plus d’informations sur la configuration du suivi, consultez le chapitre d’aide sur le « suivi ».

1. Configurez les intégrations à des produits supplémentaires :

   1. (Annonceurs avec Adobe Analytics et/ou Adobe Audience Manager) Configurez des intégrations entre les différents comptes afin qu’Adobe Advertising puisse échanger des données avec eux.

      Consultez le guide sur « [ Intégrations avec Experience Cloud ](/help/integrations/home.md) ».

   1. (Annonceurs avec [!DNL Google Analytics]) Synchronisez les mesures de conversion pour une combinaison de compte, propriété et vue [!DNL Google Analytics] à des fins d’optimisation et de création de rapports.

      Voir le sous-chapitre d’aide « Admin » > « [ Configuration des sources de données ](/help/search-social-commerce/admin/data-sources/data-source-about.md) ».

1. Configurez et lancez les portefeuilles :

   1. Configurez des portfolios configurés pour atteindre vos objectifs et objectifs commerciaux, avec les campagnes appropriées. L’équipe d’implémentation rassemble et valide ensuite les données relatives aux clics et au chiffre d’affaires pendant au moins 14 jours, puis valide les paramètres du portfolio.

      >[!NOTE]
      >
      >Les services Search, Social et Commerce effectuent toujours le suivi et génèrent des rapports sur les données des campagnes qui ne sont pas affectées aux portfolios, mais ils ne les optimisent pas.

   1. Une fois qu’il y a suffisamment de données disponibles pour créer une ligne de base, l’équipe peut lancer le portefeuille, ce qui permet à Search, Social et Commerce d’optimiser les offres et/ou les budgets du portefeuille, en fonction du type d’optimisation.

   Pour plus d’informations sur la configuration et le lancement des portfolios, consultez l’aide sur l’« Optimisation », disponible à partir du menu [!UICONTROL Help] (![menu Aide](/help/search-social-commerce/assets/help-main-menu.png "menu Aide")) dans l’angle supérieur droit de n’importe quelle page dans Search, Social et Commerce.

1. Surveillez les performances de vos portefeuilles :

   1. Générez des informations publicitaires, qui sont des données visuelles et exploitables sur vos portefeuilles optimisés et actifs.

   1. Configurez et automatisez éventuellement des rapports personnalisés pour la surveillance des performances.

   Pour plus d’informations sur l’exécution des informations publicitaires et la configuration des rapports, consultez le chapitre d’aide sur « Informations et rapports ».

1. (Facultatif) Configurez vos [vues de données de performances](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) pour afficher les données souhaitées.

## Tâches en cours

Après le lancement initial, les tâches en cours suivantes sont requises. Selon vos conditions d’engagement, [!DNL Adobe], une agence affiliée ou l’annonceur effectue les tâches suivantes :

* Continuez à surveiller et à analyser les performances de chaque portfolio en affichant les alertes, les données de performances de chaque portfolio et de ses campagnes de composants, les rapports personnalisables et les simulations (de certains rôles).

* Ajustez les différentes stratégies et paramètres que vous utilisez pour gérer l&#39;ensemble de portefeuilles, si nécessaire, en fonction des performances réelles et prévues du portefeuille et des opportunités de croissance :

   * Ajustez les budgets, les objectifs et les autres paramètres du portefeuille.

   * Ajustez les structures de compte/campagne pour tenir compte des modifications apportées à la stratégie marketing.

   * Ajouter/suspendre/supprimer des composants de campagne. Cela peut inclure le développement d’ensembles de mots-clés basés sur l’analyse des termes de recherche, ainsi que le test de copies d’annonces et de pages de destination.

   * Mettez à jour les stratégies de ciblage géographique et de site en fonction de rapports de performances avancés.

   * (Facultatif) Ajoutez des contraintes d’enchères à des mots-clés de recherche individuels ou à tous les mots-clés d’un groupe publicitaire, d’une campagne ou d’un portfolio.

   * Ajoutez de nouveaux portefeuilles.

Pour obtenir des instructions sur la surveillance des portefeuilles et l’ajustement des stratégies de portefeuille, consultez le sous-chapitre d’aide « Optimisation » > « Gestion des portefeuilles » > « Surveillance et gestion des performances », disponible à partir du menu [!UICONTROL Help] (![menu Aide](/help/search-social-commerce/assets/help-main-menu.png "menu Aide")) en haut à droite de n’importe quelle page dans Search, Social et Commerce.
