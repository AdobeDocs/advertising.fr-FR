---
title: A propos des comptes de réseau publicitaire
description: Découvrez les comptes de réseau publicitaire dans Search, Social et Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# A propos des comptes de réseau publicitaire

*Rôles utilisateur du gestionnaire de compte de l’agence, du gestionnaire de compte d’Adobe et de l’administrateur uniquement*

Search, Social et Commerce peuvent effectuer le suivi de n’importe quel compte d’annonceur sur les réseaux publicitaires pris en charge. Pour activer le suivi d’un compte, vous devez créer un enregistrement de compte correspondant. Vous devez configurer les détails du compte pour n’importe quel type de compte, que Search, Social et Commerce se synchronise ou optimise les offres et les budgets sur ses publicités.

## Comptes synchronisés via les API

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] (anciennement [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], et [!DNL Yandex] comptes*

Synchronisations de Search, Social et Commerce (*syncs*) avec les comptes réseau d’annonces pris en charge afin que vous puissiez suivre, créer des rapports et visualiser les performances de vos annonces. Pour tous les réseaux publicitaires, à l’exception de [!DNL Yahoo! Display Network], vous pouvez éventuellement gérer les campagnes de votre compte dans Search, Social et Commerce. [!DNL Yahoo! Display Network], les campagnes sont en lecture seule. Pour tous les réseaux publicitaires, vous pouvez permettre à la fonctionnalité d’optimisation d’optimiser les offres sur les publicités dans les comptes gérés en les ajoutant aux portefeuilles.

Pour permettre la synchronisation d’un compte, l’enregistrement du compte doit contenir les informations d’identification d’accès au compte et être activé (principal).

Lors de la synchronisation, Search, Social et Commerce extrait les structures de campagne de l’annonceur et les entités de campagne prises en charge, y compris la plupart de leurs attributs gérés ou signalés dans Search, Social et Commerce. Elle n’inclut pas les données de clic, ni les offres et les modificateurs d’offre entrés en dehors de Search, Social et Commerce, qui sont regroupés séparément. Search, Social et Commerce se synchronise automatiquement avec vos comptes de réseau publicitaire une fois par jour, ainsi que chaque fois qu’il détecte une nouvelle campagne sur l’un de vos réseaux publicitaires. En outre, elle envoie immédiatement toutes les modifications apportées aux données de campagne depuis Search, Social et Commerce vers le réseau publicitaire. Vous pouvez éventuellement demander une synchronisation manuelle si nécessaire.

Pour plus d’informations sur la création et la modification des campagnes synchronisées, reportez-vous au chapitre sur &quot;Campaign Management&quot;.

## Comptes de suivi uniquement

*[!DNL Naver]Comptes*

Les campagnes de suivi vous permettent de suivre, de créer des rapports et de visualiser les performances des annonces que vous achetez directement sur le réseau publicitaire. Search, Social et Commerce ne synchronise pas les données avec le réseau publicitaire, n’enchère pas pour le compte ni ne fournit aucun type d’optimisation ou de simulations.

Pour permettre à Search, Social et Commerce d’attribuer des conversions aux clics, configurez les options de suivi dans l’enregistrement de compte et activez l’enregistrement de compte. Vous pouvez ensuite utiliser des feuilles d’envoi groupées pour générer des URL de suivi pour vos publicités et mots-clés, puis ajouter manuellement les URL de suivi dans la variable [!DNL Naver] gestionnaire de publicités.

Voir plus d’informations sur [!DNL Naver] campagnes de suivi uniquement, voir &quot;[Mise en oeuvre [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Gestion des comptes de réseau publicitaire](ad-network-account-manage.md)
>* [Gestion des comptes de centre commercial](merchant-account-manage.md)
>* [Mettez à jour le code de suivi s\_kwcid pour un événement [!DNL Google Ads] account](update-skwcid-google.md)

