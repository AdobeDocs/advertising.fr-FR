---
title: (Nouvelle interface utilisateur) À propos des comptes réseau publicitaires
description: Découvrez les comptes de réseau publicitaire dans la nouvelle interface utilisateur de Search, Social et Commerce.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) À propos des comptes réseau publicitaires

Search, Social et Commerce peuvent suivre n’importe quel compte d’un annonceur sur les réseaux publicitaires pris en charge. Pour activer le suivi d’un compte, vous devez créer un enregistrement de compte correspondant. Vous devez configurer les détails du compte pour tout type de compte, que Search, Social et Commerce se synchronise ou non avec lui ou optimise les enchères et les budgets sur ses annonces.

## Comptes synchronisés via les API

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anciennement [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] et comptes [!DNL Baidu] existants*

Search, Social et Commerce se synchronise (*synchronise*) avec les comptes de réseau publicitaire pris en charge afin que vous puissiez suivre, générer des rapports et visualiser les performances de vos publicités. Pour tous les réseaux publicitaires, à l’exception de [!DNL Yahoo! Display Network], vous pouvez éventuellement gérer les campagnes pour votre compte dans Search, Social et Commerce ; [!DNL Yahoo! Display Network], les campagnes sont en lecture seule. Pour tous les réseaux publicitaires, vous pouvez permettre à la fonctionnalité d’optimisation d’optimiser les enchères, les budgets de campagne et les cibles de stratégie d’enchères de campagne pour les campagnes des comptes gérés, en ajoutant les campagnes aux portefeuilles.

Pour activer la synchronisation d’un compte, l’enregistrement de compte doit contenir les informations d’identification d’accès au compte et être activé (actif).

Pendant la synchronisation, Search, Social et Commerce extrait les structures de campagne de l’annonceur et les entités de campagne prises en charge, y compris la plupart de leurs attributs gérés ou signalés dans Search, Social et Commerce. Elle n’inclut pas les données de clic, ni les offres et les modificateurs d’offres saisis en dehors des moteurs de recherche, des réseaux sociaux et de Commerce, qui sont rassemblés séparément. Search, Social et Commerce se synchronise automatiquement avec vos comptes de réseau publicitaire une fois par jour, ainsi que chaque fois qu’il détecte une nouvelle campagne sur l’un de vos réseaux publicitaires. En outre, il envoie immédiatement au réseau publicitaire toutes les modifications apportées aux données de la campagne à partir de Search, Social et Commerce. Vous pouvez éventuellement demander une synchronisation manuelle si nécessaire.

Pour plus d’informations sur la création et la modification des campagnes synchronisées, consultez le chapitre sur la « Gestion de campagne ».

## Comptes pour lesquels vous téléchargez des données manuellement

Pour les réseaux publicitaires en ligne pour lesquels Search, Social et Commerce ne prennent pas en charge les API, vous pouvez charger du contenu de campagne et des données de coût hors ligne, de clics et de conversion pour un compte à des fins de création de rapports et de simulation de performances. Search, Social et Commerce ne synchronisent pas les données avec le réseau publicitaire, ne proposent pas d’enchères automatisées et ne fournissent aucun type d’optimisation. Cependant, ils vous permettent de rationaliser les informations cross-canal et d’identifier les opportunités d’optimisation manuelle.

## Comptes de tracking basés uniquement sur des modèles

*Disponible uniquement pour les comptes [!DNL Naver] existants*

Les campagnes de tracking vous permettent de suivre, de générer des rapports et de visualiser les performances des publicités que vous achetez directement à partir du réseau publicitaire. Search, Social et Commerce ne synchronisent pas les données avec le réseau publicitaire, ne fournissent pas d’enchères automatisées et ne fournissent aucun type d’optimisation ou de simulation.

Pour permettre à Search, Social et Commerce d’attribuer des conversions aux clics, configurez des options de suivi dans l’enregistrement de compte et activez l’enregistrement de compte. Vous pouvez ensuite utiliser des feuilles d’envoi groupé pour générer des URL de tracking pour vos publicités et mots-clés, et ajouter manuellement les URL de tracking dans le gestionnaire de publicités [!DNL Naver].

Vous ne pouvez pas configurer de nouveaux comptes [!DNL Naver] dans Search, Social et Commerce. Pour plus d’informations sur l’[!DNL Naver] de campagnes de tracking uniquement, voir « [&#x200B; Implémentation  [!DNL Naver]  comptes de tracking uniquement &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md). »

>[!MORELIKETHIS]
>
>* [Gestion des comptes réseau publicitaires via la connexion API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [Gestion des comptes réseau des publicités pour les chargements de données](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [Gérer [!DNL Naver] les comptes pour le suivi uniquement](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [Implémentation  [!DNL Naver]  comptes de tracking uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Gérer les comptes de centre commercial](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
