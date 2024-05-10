---
title: À propos du suivi pour Search, Social et Commerce
description: Découvrez les options de suivi pour Search, Social et Commerce.
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# À propos du suivi pour Search, Social et Commerce

Pour effectuer le suivi des performances de vos publicités, Search, Social et Commerce nécessite des données d’impression, de clic, de coût et de conversion (transaction) pour vos publicités. Search, Social et Commerce utilisent ces données pour créer les modèles de prévision de données dont il a besoin pour optimiser vos portefeuilles publicitaires.

## Données de coûts, de clics et d’impressions

Search, Social et Commerce récupère les données d’impression, de clic et de coût directement à partir de [réseaux publicitaires pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) tous les jours. En outre, Search, Social et Commerce peut ajouter un code de suivi des clics unique (y compris une redirection vers un serveur de suivi) dans vos modèles de suivi et URL de destination afin d’effectuer le suivi des impressions d’affichage/de contenu, des clics et des coûts, puis lier les événements aux conversions.

Si vous souhaitez effectuer le suivi de campagnes sur des réseaux publicitaires avec lesquelles Search, Social et Commerce ne synchronise pas les données, vous devez fournir des données pour ces campagnes en envoyant un fichier de flux quotidien contenant les données d’impression, de clic et de coût.

### Balises de suivi des clics

Votre équipe de mise en oeuvre de Search, Social et Commerce configure le suivi des clics en mettant à jour les modèles de suivi et les URL de destination pour les annonces, les mots-clés, les emplacements, les groupes de produits et les extensions de lien de site dans vos campagnes publicitaires synchronisées afin d’inclure une chaîne d’ID de suivi unique et une redirection d’Adobe Advertising. Ils ajoutent également le suivi aux suffixes de page d’entrée (suffixes d’URL finaux) pour votre [!DNL Google Ads] et [!DNL Microsoft Advertising] comptes et campagnes.

Les paramètres de suivi permettent à l’Adobe Advertising de suivre les clics au niveau des mots-clés (campagnes de recherche) ou au niveau des variantes d’annonces (campagnes de recherche avec ciblage de contenu ou de site, campagnes d’affichage et campagnes sur les réseaux sociaux). Chaque fois qu’un utilisateur consulte une publicité d’affichage/de contenu ou clique sur l’une de vos publicités, le réseau publicitaire envoie l’événement aux serveurs de pixels d’Adobe Advertising à l’aide d’une balise de suivi des clics associée au mot-clé ou à la publicité. Pour les clics :

* Pour [!DNL Google Ads] et [!DNL Microsoft Advertising] publicités sur les navigateurs qui prennent en charge le suivi parallèle, le réseau publicitaire envoie d’abord le clic à votre site web, puis aux serveurs de pixels d’Adobe Advertising, qui placent ensuite un cookie sur l’ordinateur de l’utilisateur, le cas échéant.

* Dans tous les autres cas, le réseau publicitaire envoie directement le clic aux serveurs de pixels Adobe Advertising. Le serveur de pixel place un cookie sur l’ordinateur de l’utilisateur (s’il n’existe pas déjà), puis redirige l’utilisateur vers l’URL appropriée de votre site web. L’expérience globale de l’utilisateur final est la même que celle qui se présenterait sans redirection.

Le cookie est défini dans la variable [!DNL Adobe] domain (`everesttech.net`) comme cookie propriétaire. Après une redirection, l’utilisateur se trouve sur le domaine de l’annonceur, puis le cookie est traité comme un cookie tiers. Pour plus d’informations sur les cookies d’Adobe Advertising, voir[Adobe Advertising des cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## Données de conversion

Lorsqu’un client clique sur une publicité ou consulte une publicité ou un affichage sur un réseau social, Search, Social et Commerce doit mettre en correspondance chaque conversion résultante avec le clic ou l’affichage/impression sociale d’origine.

L’annonceur joue un rôle dans la fourniture des données de conversion pour tous les clics et impressions display/social. Les données de conversion peuvent inclure des informations sur tout type d’événement qui se produit sur un site web et qui peut être utilisé pour l’optimisation des offres. Vous pouvez fournir des données de conversion en implémentant du code de suivi de conversion dans les pages de conversion de l’annonceur (par exemple, la page &quot;succès&quot; qui s’affiche une fois qu’un client a effectué une transaction) ou en envoyant un fichier de flux quotidien contenant des données de conversion capturées par une autre méthode.

### Balises de suivi des conversions

Vous pouvez utiliser [balises de conversion de divers fournisseurs](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Lorsque vous utilisez une balise de conversion d’Adobe Advertising et qu’un utilisateur effectue une transaction réussie et accède à une page &quot;succès&quot;, le serveur de pixel d’Adobe Advertising vérifie l’existence du cookie sur l’ordinateur de l’utilisateur, qui a été défini au moment de la redirection des clics. Lorsqu’il trouve un cookie, les informations sur l’événement de transaction sont transmises à l’aide du paramètre ef_transid , et la transaction est reconnue comme une conversion et est créditée à l’impression publicitaire ou d’affichage précédente.

Si l’utilisateur a cliqué sur plusieurs de vos publicités, Adobe Advertising crédite la transaction au dernier clic publicitaire ou à l’impression finale de la publicité (pour les campagnes d’affichage ou vidéo), sauf si vous en spécifiez autrement. Votre [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j) déterminez le nombre de jours après un clic payant ou une impression vidéo (respectivement) au cours de laquelle l’événement peut être attribué à une conversion.

L’équipe chargée de la mise en oeuvre de l’Adobe Advertising travaille avec l’annonceur pour déterminer le format des balises de conversion que l’annonceur doit mettre en oeuvre, identifier les pages web sur lesquelles chaque balise de conversion doit être insérée, puis fournir les balises de conversion à implémenter.
