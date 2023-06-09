---
title: Questions fréquentes sur le suivi
description: Découvrez les réponses aux questions courantes sur le suivi, notamment les problèmes de dépannage.
source-git-commit: f5e2044af460ebf561e075ed6b1fb057ed47acc3
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Questions fréquentes sur le suivi

## Fonctionnalités de suivi

+++Puis-je suivre les campagnes qu’Adobe Advertising ne gère pas ?

Oui. Si Search, Social et Commerce synchronise l’un de vos comptes de réseau publicitaire, celui-ci effectue le suivi des données de clic du réseau publicitaire pour toutes les [types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) dans ce compte. Il effectue également le suivi des données de conversion si vous avez ajouté la redirection Search, Social &amp; Commerce vers vos URL de destination des publicités et/ou mots-clés ou des modèles de suivi et si vous avez mis en oeuvre le suivi de conversion dans vos pages de conversion. Clarifiez avec votre équipe de compte d’Adobe les campagnes dont vous souhaitez simplement effectuer le suivi dans Search, Social et Commerce et les campagnes que vous souhaitez qu’elles gèrent.
+++

+++Comment obtenir une attribution multi-événement ?

Pour les annonceurs qui utilisent les balises de suivi de conversion Search, Social, &amp; Commerce ou Adobe Analytics, Adobe Advertising propose plusieurs options pour attribuer des données de conversion sur une série d’événements qui mènent à une conversion. Un paramètre au niveau de l’annonceur détermine comment attribuer des données de conversion entre les événements, même lorsqu’ils se produisent sur plusieurs canaux publicitaires, à condition que les canaux permettent le suivi des impressions au niveau de l’événement. Par défaut, les conversions sont attribuées au dernier événement (le plus récent), mais le paramètre peut être configuré différemment, par exemple pour attribuer des conversions au premier événement ou pour pondérer tous les événements de manière égale. La modification de la règle d’attribution affecte le mode de calcul des offres futures.

Les annonceurs qui fournissent toutes les données de conversion dans un fichier de flux doivent attribuer la conversion aux événements de transaction associés eux-mêmes.

>[!NOTE]
>
>Dans les vues, rapports et simulations personnalisées de gestion de campagne et de gestion de portefeuille (disponibles pour certains utilisateurs), vous pouvez modifier la règle utilisée pour attribuer des données de conversion dans les vues et les résultats des rapports, sans affecter la manière dont les offres futures sont calculées.

+++

+++Comment Adobe Advertising identifie-t-il les transactions en double ?

Les transactions en double peuvent se produire lorsqu’un utilisateur actualise la page de confirmation après avoir effectué une transaction. Adobe Advertising utilise la variable `ev_transid` pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété.

Voici la logique de déduplication de l’Adobe Advertising :

* **Lorsqu’un client envoie une valeur pour la variable `ev_transid` attribute:** Les requêtes de pixel suivantes sont considérées comme des doublons de la précédente si les éléments suivants sont identiques : la valeur `ev_transid`; l’identifiant de suivi pour le même mot-clé, la même publicité ou le même emplacement ; et la valeur d’une propriété de transaction spécifique.

  Par exemple, si plusieurs demandes de prêt possèdent le même ID de demande et le même montant de prêt pour le même mot-clé sur un réseau publicitaire spécifique, elles sont considérées comme des doublons et seule la première demande de prêt est comptabilisée.

* **Lorsqu’un client n’envoie pas de valeur pour la variable `ev_transid` attribute:** Les transactions suivantes sont considérées comme des doublons de la précédente si elles partagent un ID de suivi pour le même mot-clé, publicité ou emplacement ; et la même valeur pour une propriété de transaction spécifique.

  Par exemple, si plusieurs demandes de prêt ont le même identifiant de mot-clé et le même montant de prêt, elles sont considérées comme des doublons et seule la première demande de prêt est comptabilisée.
+++

## Types de mise en oeuvre du suivi

+++Je souhaite arrêter d’utiliser le service de suivi de conversion d’Adobe Advertising pour une ou plusieurs campagnes ou comptes. Comment puis-je supprimer rapidement le code de suivi des URL de suivi ?

Tout d’abord, consultez votre équipe de compte d’Adobe pour comprendre les implications de la suppression des URL de suivi.

Dans le compte ou la campagne, remplacez la méthode de suivi par &quot;[!UICONTROL No EF Redirect].&quot; Créez ensuite une feuille d’envoi groupé à l’aide de la commande &quot;[!UICONTROL Generate Tracking URLs]&quot;, puis publiez-la sur le réseau publicitaire. Toutes les URL de tracking ou URL de destination existantes sont remplacées.
+++

## Questions relatives aux données

+++Comment savoir quelle propriété de transaction provient d’un flux de données ou est suivie par la balise de suivi de conversion d’Adobe Advertising ?

Dans un [!UICONTROL Transaction Report], vous pouvez déterminer si une propriété de transaction incluse a été suivie par le pixel de suivi de conversion d’Adobe Advertising si vous avez inclus la colonne personnalisée &quot;[!UICONTROL Tracking URL].&quot; Le suivi des URL avec le pixel de suivi d’Adobe Advertising commence par `http://pixel.everesttech.net`.
+++

+++Que sont les transactions orphelines ?

Les transactions orphelines sont des événements de transaction qui ne peuvent pas être associés à un mot-clé ou à une publicité spécifique. Adobe Advertising attribue la transaction/le chiffre d’affaires à un mot-clé ou à une publicité en faisant correspondre les identifiants de suivi reçus avec l’événement de chiffre d’affaires à l’identifiant de suivi unique dans l’URL de suivi du mot-clé ou de la publicité.

Lorsqu’une équipe de compte d’Adobe soupçonne que les transactions orphelines sont responsables d’une baisse des recettes, l’équipe d’assistance clientèle recherche les orphelins et, le cas échéant, enquête sur le problème.

Les orphelins se produisent dans les situations suivantes.

**Implémentations de pixels**

Les transactions orphelines ne se produisent presque jamais pour les implémentations de pixels. Cependant, des orphelins de pixel se sont produits lorsque :

* Les données de clic ne sont pas disponibles pour la date de clic de la conversion. Dans ce cas, les données sont mises en correspondance lorsque Search, Social et Commerce récupère les données de clic du réseau publicitaire.

* Les journaux de clics ne sont pas traités avant les journaux de conversion.

**Implémentations de flux**

* L’ID de suivi envoyé dans le flux provient d’un compte que Search, Social et Commerce ne connaît pas.

* Le compte n’est pas synchronisé ou des erreurs se sont produites pendant le processus de synchronisation.

* L’ID de suivi a été ajouté et supprimé du réseau publicitaire alors que Search, Social et Commerce n’était pas synchronisé avec le réseau publicitaire. Par conséquent, Search, Social et Commerce ne contient aucune information sur l’ID. Ce problème continue de générer des recettes orphelines en cas de retard dans la réception des recettes.

* Le client a envoyé un ID de suivi mal formaté dans le flux et ne correspond pas à l’ID de suivi dans l’URL. Cela se produit généralement en raison d’un problème de mise en forme ou lorsque les ID de suivi sont abrégés dans le flux.

* Dans le fichier de configuration, l’expression régulière utilisée pour extraire l’ID de suivi des URL est incorrecte ou obsolète. Il arrive que l’annonceur modifie l’ID de suivi dans l’URL ou adopte un système de suivi entièrement nouveau, ce qui nécessite que l’équipe de mise en oeuvre de Search, Social et Commerce mette à jour l’expression régulière. Dans ce cas, une grande partie des recettes est orpheline.

**Implémentations de flux à l’aide d’un ID de transaction**

Aucune transaction en ligne n’est disponible avant les dates auxquelles les données sont disponibles dans le flux hors ligne.

**Implémentations de flux à l’aide d’un jeton (ef_id)**

Search, Social et Commerce ne trouve pas de clic correspondant sur son serveur ou sur le réseau publicitaire. Cela peut être dû au fait que les données de clic ne sont pas disponibles pour la date de clic de la conversion ou (rarement) parce que les journaux de clics n’ont pas été traités avant les journaux de conversion. Lorsque Search, Social et Commerce reçoit les données de clic du réseau publicitaire ou que les journaux de clics sont traités, les données sont mappées à la conversion.
+++

## Problèmes de suivi des recettes

+++Comment corriger des données anciennes ou incorrectes d’un fichier de flux ?

Contactez l’assistance clientèle avec le fichier de données corrigé.
+++

+++Plusieurs mots-clés possèdent les mêmes URL de suivi.

**Implications**

Pour les mises en oeuvre de flux avec plusieurs ID de suivi, les données sont signalées par rapport à plusieurs mots-clés. Pour d’autres mises en oeuvre, les conversions peuvent être attribuées au mot-clé incorrect, car le système attribue arbitrairement une conversion à l’un des mots-clés.

**Cause possible**

L’URL d’un nouveau mot-clé ou d’une nouvelle publicité a été copiée à partir d’un autre mot-clé ou publicité.

Cela ne doit pas se produire avec les publicités display ou sociales.

**Solution possible ou solution de contournement**

* Si vous gérez vos propres mots-clés et annonces, créez un fichier de feuille d’envoi groupé avec les URL correctes pour les URL en double et publiez-le sur le compte approprié à l’aide de la variable **[!UICONTROL Generate Tracking URLs]** qui régénère les URL de tous les mots-clés et annonces.

* Si une équipe de compte d’Adobe gère vos mots-clés, demandez-lui de créer de nouvelles URL pour les URL en double.
+++
