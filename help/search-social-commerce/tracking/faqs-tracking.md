---
title: Questions fréquentes sur le tracking
description: Découvrez les réponses aux questions courantes sur le tracking, y compris les problèmes de dépannage.
exl-id: e5302c09-0b40-47ae-bc88-9299e6bd3044
feature: Search Tracking
TQID: https://experienceleague.adobe.com/KLlUxOpfUEgKdbfbj2ri0o1brljc6spN4AtMRKXrdrQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1190
ht-degree: 0%

---

# Questions fréquentes sur le tracking

## Fonctionnalités de tracking

+++Puis-je effectuer le suivi des campagnes qu’Adobe Advertising ne gère pas ?

Oui. Si Search, Social et Commerce synchronisent l’un de vos comptes de réseau publicitaire, il effectue le suivi des données de clic du réseau publicitaire pour tous les types de campagne [pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) de ce compte. Il effectue également le suivi des données de conversion si vous avez ajouté la redirection Search, Social et Commerce à vos URL de destination d’annonce et/ou de mot-clé ou à vos modèles de suivi et si vous avez implémenté le suivi des conversions dans vos pages de conversion. Indiquez à l’équipe chargée de votre compte Adobe les campagnes que vous souhaitez simplement suivre dans Search, Social et Commerce et celles que vous souhaitez qu’elle gère.
+++

+++Comment puis-je obtenir une attribution multi-événement ?

Pour les annonceurs qui utilisent les balises de suivi des conversions Search, Social et Commerce ou Adobe Analytics, Adobe Advertising propose plusieurs options d’attribution des données de conversion sur une série d’événements qui entraînent une conversion. Un paramètre au niveau de l’annonceur détermine la manière d’attribuer les données de conversion entre les événements, même lorsqu’elles se produisent sur plusieurs canaux publicitaires, tant que les canaux permettent le suivi des impressions au niveau de l’événement. Par défaut, les conversions sont attribuées au dernier événement (le plus récent), mais le paramètre peut être configuré différemment, par exemple pour attribuer des conversions au premier événement ou pour pondérer tous les événements de manière uniforme. La modification de la règle d’attribution affecte le calcul des enchères futures.

Les annonceurs qui fournissent toutes les données de conversion dans un fichier de flux doivent attribuer la conversion aux événements de transaction associés eux-mêmes.

>[!NOTE]
>
>Dans les vues, les rapports et les simulations personnalisées de gestion de campagnes et de gestion de portefeuilles (disponibles pour certains utilisateurs), vous pouvez modifier la règle utilisée pour attribuer les données de conversion dans les vues et les résultats des rapports, sans affecter la manière dont les enchères futures sont calculées.

+++

+++Comment Adobe Advertising identifie-t-il les transactions en double ?

Des transactions en double peuvent se produire lorsqu&#39;un utilisateur actualise la page de confirmation après avoir effectué une transaction. Adobe Advertising utilise l’attribut `ev_transid` pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété.

Voici la logique de déduplication d’Adobe Advertising :

* **Lorsqu’un client envoie une valeur pour l’attribut `ev_transid` :** les requêtes de pixels suivantes sont considérées comme des doublons de la précédente si les éléments suivants sont tous identiques : le `ev_transid` ; l’identifiant de suivi pour le même mot-clé, la même annonce ou le même emplacement ; et la valeur d’une mesure de conversion spécifique.

  Par exemple, si plusieurs demandes de prêt ont le même ID de demande et le même montant de prêt pour le même mot-clé sur un réseau publicitaire spécifique, elles sont considérées comme des doublons et seule la première demande de prêt est comptabilisée.

* **Lorsqu’un client n’envoie pas de valeur pour l’attribut `ev_transid` :** les transactions suivantes sont considérées comme des doublons de la précédente si elles partagent un identifiant de suivi pour le même mot-clé, la même annonce ou le même emplacement, et la même valeur pour une mesure de conversion spécifique.

  Par exemple, si plusieurs demandes de prêt ont le même ID de mot-clé et le même montant de prêt, elles sont considérées comme des doublons et seule la première demande de prêt est comptabilisée.
+++

## Types de mise en œuvre du tracking

+++Je souhaite arrêter d’utiliser le service de suivi des conversions Adobe Advertising pour une ou plusieurs campagnes ou comptes. Comment supprimer rapidement le code de tracking des URL de tracking ?

Tout d’abord, consultez l’équipe chargée de votre compte Adobe pour comprendre les implications de la suppression des URL de tracking.

Dans le compte ou la campagne, remplacez la méthode de suivi par « [!UICONTROL No EF Redirect] ». Créez ensuite une feuille d’envoi groupé à l’aide de l’option « [!UICONTROL Generate Tracking URLs] » et publiez-la sur le réseau publicitaire. Toutes les URL de tracking ou de destination existantes sont remplacées.
+++

## Questions sur les données

+++Comment puis-je savoir quelle mesure de conversion provient d’un flux de données ou est suivie par la balise de suivi des conversions d’Adobe Advertising ?

Dans une [!UICONTROL Transaction Report], vous pouvez déterminer si une mesure de conversion incluse a été suivie par le pixel de suivi des conversions d’Adobe Advertising si vous incluez la colonne personnalisée « [!UICONTROL Tracking URL] ». Les URL de tracking avec le pixel de tracking Adobe Advertising commencent par `http://pixel.everesttech.net`.
+++

+++Que sont les transactions orphelines ?

Les transactions orphelines sont des événements de transaction qui ne peuvent pas être associés à un mot-clé ou à une annonce publicitaire spécifique. Adobe Advertising attribue la transaction/le chiffre d’affaires à un mot-clé ou à une publicité en faisant correspondre les identifiants de suivi reçus avec l’événement de chiffre d’affaires à l’identifiant de suivi unique dans l’URL de suivi du mot-clé ou de la publicité.

Lorsqu’une équipe chargée du compte Adobe soupçonne que les transactions orphelines sont à l’origine d’une baisse de chiffre d’affaires, l’assistance clientèle recherche des transactions orphelines et, si elle en trouve, enquête sur le problème.

Les orphelins se produisent dans les situations suivantes.

**Implémentations en pixels**

Les transactions orphelines ne se produisent presque jamais pour les implémentations en pixels. Cependant, des pixels orphelins se sont produits lorsque :

* Les données de clic ne sont pas disponibles pour la date de clic de la conversion. Dans ce cas, les données sont mappées lorsque Search, Social et Commerce obtient les données de clic du réseau publicitaire.

* Les journaux de clics ne sont pas traités avant les journaux de conversion.

**Implémentations des flux**

* L’identifiant de suivi envoyé dans le flux provient d’un compte que Search, Social et Commerce ne connaissent pas.

* Le compte n’est pas synchronisé ou des erreurs se sont produites pendant le processus de synchronisation.

* L’ID de suivi a été ajouté et supprimé du réseau publicitaire alors que Search, Social et Commerce n’étaient pas synchronisés avec le réseau publicitaire. Search, Social et Commerce ne dispose donc d’aucune information sur l’ID. Ce problème continue de générer des revenus orphelins en cas de retard dans la réception des revenus.

* Le client a envoyé un identifiant de suivi qui n’est pas formaté correctement dans le flux et ne correspond pas à l’identifiant de suivi dans l’URL. Cela se produit généralement en raison d’un problème de mise en forme ou lorsque les identifiants de suivi sont abrégés dans le flux.

* Dans le fichier de configuration, l’expression régulière utilisée pour extraire l’identifiant de tracking des URL est incorrecte ou obsolète. Parfois, l’annonceur modifie l’identifiant de tracking dans l’URL ou adopte un système de tracking entièrement nouveau, ce qui nécessite que l’équipe d’implémentation de Search, Social et Commerce mette à jour l’expression régulière. Dans de tels cas, une grande partie du revenu est orpheline.

**Implémentations de flux à l’aide d’un ID de transaction**

Aucune transaction en ligne n’est disponible avant les dates pour lesquelles les données sont disponibles dans le flux hors ligne.

**Alimenter les implémentations à l’aide d’un jeton (ef_id)**

Les services Search, Social et Commerce ne parviennent pas à trouver un clic correspondant sur leur serveur ou sur le réseau publicitaire. Cela peut être dû au fait que les données de clic ne sont pas disponibles pour la date de clic de la conversion ou (rarement) au fait que les journaux de clic n’ont pas été traités avant les journaux de conversion. Lorsque Search, Social et Commerce reçoit les données de clic du réseau publicitaire ou que les journaux de clic sont traités, les données sont mappées à la conversion.
+++

## Problèmes de tracking des revenus

+++Comment corriger les données anciennes/incorrectes d’un fichier de flux ?

Contactez l’assistance clientèle avec le fichier de données corrigé.
+++

+++Plusieurs mots-clés ont les mêmes URL de tracking.

**Implications**

Pour les implémentations de flux avec plusieurs identifiants de suivi, les données sont signalées par rapport à plusieurs mots-clés. Pour d’autres mises en œuvre, les conversions peuvent être attribuées au mauvais mot-clé, car le système attribue arbitrairement une conversion à l’un des mots-clés.

**Cause possible**

L’URL d’un nouveau mot-clé ou d’une nouvelle publicité a été copiée à partir d’un autre mot-clé ou publicité.

Cela ne devrait pas se produire avec les publicités display ou sociales.

**Solution ou solution possible**

* Si vous gérez vos propres mots-clés et publicités, créez un fichier de feuille d’envoi groupé avec les URL correctes pour les URL en double et publiez-le sur le compte approprié à l’aide de l’option **[!UICONTROL Generate Tracking URLs]** , qui régénère les URL de tous les mots-clés et publicités.

* Si une équipe de compte Adobe gère vos mots-clés, demandez-lui de créer de nouvelles URL pour les URL en double.
+++
