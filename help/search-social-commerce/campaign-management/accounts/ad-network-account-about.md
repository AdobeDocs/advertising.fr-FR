---
title: À propos des comptes de réseau publicitaire
description: Découvrez les comptes de réseau publicitaire dans Search, Social et Commerce.
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/90Dq2tehH-k2aY3Ij30aHF-XQGdvlPY346moWkg3xmk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 429
ht-degree: 0%

---

# À propos des comptes de réseau publicitaire

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Search, Social et Commerce peuvent suivre n’importe quel compte d’un annonceur sur les réseaux publicitaires pris en charge. Pour activer le suivi d’un compte, vous devez créer un enregistrement de compte correspondant. Vous devez configurer les détails du compte pour tout type de compte, que Search, Social et Commerce se synchronise ou non avec lui ou optimise les enchères et les budgets sur ses annonces.

## Comptes synchronisés via les API

*[!DNL Google Ads], [!DNL LY Ads] (anciennement [!DNL Yahoo! Japan Ads]), [!DNL Microsoft Advertising] (anciennement [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yandex] et comptes [!DNL Baidu] existants*

Search, Social et Commerce se synchronise (*synchronise*) avec les comptes de réseau publicitaire pris en charge afin que vous puissiez suivre, générer des rapports et visualiser les performances de vos publicités. Pour tous les réseaux publicitaires, à l’exception de [!DNL Yahoo! Display Network], vous pouvez éventuellement gérer les campagnes pour votre compte dans Search, Social et Commerce ; [!DNL Yahoo! Display Network], les campagnes sont en lecture seule. Pour tous les réseaux publicitaires, vous pouvez permettre à la fonctionnalité d’optimisation d’optimiser les enchères, les budgets de campagne et les cibles de stratégie d’enchères de campagne pour les campagnes des comptes gérés, en ajoutant les campagnes aux portefeuilles.

Pour activer la synchronisation d’un compte, l’enregistrement de compte doit contenir les informations d’identification d’accès au compte et être activé (actif).

Pendant la synchronisation, Search, Social et Commerce extrait les structures de campagne de l’annonceur et les entités de campagne prises en charge, y compris la plupart de leurs attributs gérés ou signalés dans Search, Social et Commerce. Elle n’inclut pas les données de clic, ni les offres et les modificateurs d’offres saisis en dehors des moteurs de recherche, des réseaux sociaux et de Commerce, qui sont rassemblés séparément. Search, Social et Commerce se synchronise automatiquement avec vos comptes de réseau publicitaire une fois par jour, ainsi que chaque fois qu’il détecte une nouvelle campagne sur l’un de vos réseaux publicitaires. En outre, il envoie immédiatement au réseau publicitaire toutes les modifications apportées aux données de la campagne à partir de Search, Social et Commerce. Vous pouvez éventuellement demander une synchronisation manuelle si nécessaire.

Pour plus d’informations sur la création et la modification des campagnes synchronisées, consultez le chapitre sur la « Gestion de campagne ».

## Comptes de tracking uniquement

*[!DNL Naver]comptes*

Les campagnes de tracking vous permettent de suivre, de générer des rapports et de visualiser les performances des publicités que vous achetez directement à partir du réseau publicitaire. Search, Social et Commerce ne synchronise pas les données avec le réseau publicitaire, ne place pas d’enchères pour le compte et ne fournit aucun type d’optimisation ou de simulation.

Pour permettre à Search, Social et Commerce d’attribuer des conversions aux clics, configurez des options de suivi dans l’enregistrement de compte et activez l’enregistrement de compte. Vous pouvez ensuite utiliser des feuilles d’envoi groupé pour générer des URL de tracking pour vos publicités et mots-clés, et ajouter manuellement les URL de tracking dans le gestionnaire de publicités [!DNL Naver].

Pour plus d’informations sur l’[!DNL Naver] de campagnes de tracking uniquement, voir « [ Implémentation  [!DNL Naver]  comptes de tracking uniquement ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md). »

>[!MORELIKETHIS]
>
>* [Gérer les comptes de réseau publicitaire](ad-network-account-manage.md)
>* [Gérer les comptes de centre commercial](merchant-account-manage.md)
>* [Mettre à jour le code de suivi AMO ID pour un  [!DNL Google Ads] compte](update-amo-id-google.md)
