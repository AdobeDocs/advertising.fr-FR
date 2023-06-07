---
title: Présentation de l’implémentation de Search, Social et Commerce
description: En savoir plus
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# Présentation de l’implémentation de Search, Social et Commerce

[!DNL Adobe] ou l’une de ses agences affiliées travaille avec chaque annonceur pour lancer ses portfolios publicitaires en ligne et suivre toute autre campagne publicitaire. Après le lancement initial, d’autres tâches en cours assurent que les objectifs de l’annonceur continueront à être atteints.

Vous trouverez ci-dessous le processus général d’implémentation et d’utilisation de Search, Social et Commerce.

## Lancement initial

[!DNL Adobe] et/ou votre agence travaille avec vous comme suit :

1. Évaluez vos objectifs généraux et élaborez des stratégies pour les atteindre :

   1. Identifiez votre modèle d’entreprise et vos objectifs marketing.

   1. Identification des exigences de suivi des conversions

   1. Analysez vos structures de compte publicitaire en ligne existantes.

   1. Identifiez les mesures pour l’optimisation du portefeuille et la création de rapports.

1. (Administrateur ou gestionnaire de compte) Configurez les comptes administratifs :

   1. Configurez le compte de l’annonceur. Si une agence gère les données de l’annonceur, le compte de l’annonceur doit être associé au compte de l’agence.

   1. (Si nécessaire) Créez des comptes utilisateurs pour que l’annonceur puisse afficher et gérer les données de campagne et générer des rapports.

   Pour plus d’informations sur la configuration de comptes, reportez-vous au chapitre d’aide &quot;Admin&quot;.

1. Synchronisez avec ou créez des campagnes pour chacun de vos comptes réseau publicitaire :

   * Synchronisez avec le compte en créant a) un enregistrement de compte correspondant dans Search, Social et Commerce qui contient les informations d’identification d’accès au compte et les options de suivi, et b) en définissant l’état du compte sur activé.

   * Si les comptes ne contiennent pas déjà de données de campagne, ajoutez des campagnes, des groupes publicitaires, des mots-clés, des publicités et des emplacements dans Search, Social et Commerce ou depuis le réseau publicitaire.

      Pour plus d’informations sur la configuration des campagnes de recherche, reportez-vous au chapitre d’aide sur &quot;Campaign Management&quot;.

1. Configurez le suivi de toutes les publicités pour lesquelles vous souhaitez qu’Adobe Advertising effectue le suivi des conversions :

   1. (Si nécessaire) Configurez le suivi des clics pour les publicités, et éventuellement pour les mots-clés, [!DNL Google Ads] emplacements et [!DNL Google Ads] en générant et en chargeant des URL de suivi des clics.

      Les URL de suivi des clics pour les annonceurs disposant du service de suivi de conversion basé sur les pixels Adobe Advertising incluent une redirection vers [!DNL Adobe] serveurs.

   1. Configurez le suivi des conversions. Selon l’implémentation, cela peut impliquer l’ajout de balises de suivi de conversion aux pages web appropriées et/ou la configuration d’une baisse quotidienne du flux pour les données de conversion que vous avez collectées à l’aide de votre propre méthode.

      Pour plus d’informations sur la configuration du suivi, reportez-vous au chapitre d’aide &quot;Suivi&quot;.

1. Configurer des intégrations avec des produits supplémentaires :

   1. (Publicitaires avec Adobe Analytics et/ou Adobe Audience Manager) Configurez des intégrations entre les différents comptes afin qu’Adobe Advertising puisse échanger des données avec eux.

      Consultez le guide sur &quot;[Intégrations avec Experience Cloud](/help/integrations/home.md).&quot;

   1. (Publicitaires avec [!DNL Google Analytics]) Synchroniser les mesures de conversion pour un [!DNL Google Analytics] combinaison de compte, de propriété et d’affichage pour l’optimisation et la création de rapports.

      Voir le sous-chapitre d’aide &quot;Admin&quot; > &quot;[Configuration des sources de données](/help/search-social-commerce/admin/data-sources/data-source-about.md).&quot;

1. Configuration et lancement de portfolios :

   1. Configurez des portefeuilles configurés pour atteindre vos objectifs et vos objectifs commerciaux, avec les campagnes appropriées. L’équipe de mise en oeuvre rassemble et valide ensuite les données de clics et de recettes pendant au moins 14 jours, puis valide les paramètres du portfolio.

      >[!NOTE]
      >
      >Search, Social et Commerce effectue toujours le suivi et les rapports des données pour les campagnes qui ne sont pas affectées à des portefeuilles, mais n’optimise pas les offres pour ces derniers.

   1. Une fois que suffisamment de données sont disponibles pour créer une ligne de base, l’équipe peut lancer le portfolio, ce qui permet à Search, Social et Commerce d’optimiser les offres et/ou les budgets du portfolio, en fonction du type d’optimisation.
   Pour plus d’informations sur la configuration et le lancement de portefeuilles, voir l’aide sur &quot;Optimisation&quot;, disponible à partir de la page [!UICONTROL Help] (![Menu Aide](/help/search-social-commerce/assets/help-main-menu.png "Menu Aide")) en haut à droite de n’importe quelle page dans Search, Social et Commerce.

1. Surveillez les performances de vos portefeuilles :

   1. Générez des informations publicitaires, qui sont des données visuelles exploitables sur vos portfolios optimisés et principaux.

   1. Configurez et automatisez éventuellement des rapports personnalisés pour la surveillance des performances.

   Pour plus d’informations sur l’exécution des informations publicitaires et la configuration des rapports, reportez-vous au chapitre d’aide &quot;Statistiques et rapports&quot;.

1. (Facultatif) Configurez votre [vues des données de performances](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) pour afficher les données que vous souhaitez afficher.

## Tâches en cours

Après le lancement initial, les tâches en cours suivantes sont requises. Selon vos conditions d’engagement, soit [!DNL Adobe], une agence affiliée ou l’annonceur effectue les tâches suivantes :

* Continuez à surveiller et à analyser les performances de chaque portefeuille en affichant les alertes, les données de performance pour chaque portefeuille et ses campagnes de composants, les rapports personnalisables et (certains rôles) les simulations.

* Ajustez les différentes stratégies et paramètres que vous utilisez pour gérer l’ensemble du portfolio, si nécessaire, en fonction des performances réelles et prévues du portfolio et des opportunités de croissance :

   * Ajustez les budgets, les objectifs et les autres paramètres du portfolio.

   * Ajustez les structures de compte/de campagne en fonction des modifications apportées à la stratégie marketing.

   * Ajouter/mettre en pause/supprimer des composants de campagne. Cela peut inclure le développement de jeux de mots-clés en fonction de l’analyse des termes de recherche et le test de la copie d’annonces et des landing pages.

   * Mettez à jour les stratégies de ciblage géographique et de site en fonction des rapports de performances avancés.

   * (Facultatif) Ajoutez des contraintes d’offre à des mots-clés de recherche individuels ou à tous les mots-clés d’un groupe publicitaire, d’une campagne ou d’un portefeuille.

   * Ajoutez de nouveaux portefeuilles.

Pour obtenir des instructions sur la surveillance des portefeuilles et l’ajustement des stratégies de portefeuille, reportez-vous au sous-chapitre d’aide &quot;Optimisation&quot; > &quot;Gestion des Portfolios&quot; > &quot;Suivi et gestion des performances&quot;, disponible à partir de la page [!UICONTROL Help] (![Menu Aide](/help/search-social-commerce/assets/help-main-menu.png "Menu Aide")) en haut à droite de n’importe quelle page dans Search, Social et Commerce.