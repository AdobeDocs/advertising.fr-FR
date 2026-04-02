---
title: À propos du suivi pour Search, Social et Commerce
description: Découvrez les options de suivi pour Search, Social et Commerce.
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
TQID: https://experienceleague.adobe.com/IpPgzsMgRsOCmLv3dyEKBp4EPQwgN90UkVIQy9SaXB8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 0%

---

# À propos du suivi pour Search, Social et Commerce

Pour suivre les performances de vos publicités, Search, Social et Commerce a besoin de données d’impression, de clic, de coût et de conversion (transaction) pour vos publicités. Search, Social et Commerce utilisent ces données pour créer les modèles de prévision de données nécessaires à l’optimisation de vos portfolios publicitaires.

## Données de coût, de clic et d’impression

Les services Search, Social et Commerce récupèrent quotidiennement des données relatives aux impressions, aux clics et aux coûts, directement à partir des [réseaux publicitaires pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). En outre, Search, Social et Commerce peuvent ajouter un code de suivi des clics unique (y compris une redirection vers un serveur de suivi) dans vos modèles de suivi et URL de destination pour effectuer le suivi des impressions d’affichage/de contenu, des clics et des coûts, puis lier les événements aux conversions.

Si vous souhaitez suivre les campagnes sur des réseaux publicitaires avec lesquels Search, Social et Commerce ne synchronisent pas les données, vous devez fournir des données pour ces campagnes en envoyant un fichier de flux quotidien avec les données d’impression, de clic et de coût.

### Balises de suivi des clics

Votre équipe d’implémentation de Search, Social et Commerce configure le suivi des clics en mettant à jour les modèles de suivi et les URL de destination pour les publicités, mots-clés, emplacements, groupes de produits et extensions de lien de site dans vos campagnes publicitaires synchronisées afin d’inclure une chaîne d’identifiant de suivi unique et une redirection Adobe Advertising. Ils ajoutent également un suivi aux suffixes des pages de destination (suffixes d’URL finaux) pour vos comptes et campagnes [!DNL Google Ads] et [!DNL Microsoft Advertising].

Les paramètres de tracking permettent à Adobe Advertising de suivre les clics au niveau d’un mot-clé individuel (campagnes de recherche) ou au niveau d’une variation d’annonce (campagnes de recherche avec ciblage de contenu ou de site, campagnes d’affichage et campagnes sociales). Chaque fois qu’un utilisateur ou une utilisatrice consulte une annonce publicitaire ou clique sur l’une de vos annonces, le réseau publicitaire envoie l’événement aux serveurs de pixels d’Adobe Advertising à l’aide d’une balise de suivi des clics associée au mot-clé ou à l’annonce. Pour les clics :

* Pour les publicités [!DNL Google Ads] et [!DNL Microsoft Advertising] sur les navigateurs qui prennent en charge le suivi parallèle, le réseau publicitaire envoie d’abord le clic sur votre site web, puis sur les serveurs de pixels d’Adobe Advertising, qui placent ensuite un cookie sur l’ordinateur de l’utilisateur, s’il n’existe pas déjà.

* Dans tous les autres cas, le réseau publicitaire envoie directement le clic aux serveurs de pixels d’Adobe Advertising. Le serveur de pixels place un cookie sur l’ordinateur de l’utilisateur (s’il n’en existe pas déjà un), puis redirige l’utilisateur vers l’URL appropriée de votre site web. L’expérience globale de l’utilisateur final est la même que sans redirection.

Le cookie est défini dans le domaine [!DNL Adobe] (`everesttech.net`) en tant que cookie propriétaire. Après une redirection, l’utilisateur se trouve sur le domaine de l’annonceur, et le cookie est alors traité comme un cookie tiers. Pour plus d’informations sur les cookies Adobe Advertising, voir « [Cookies Adobe Advertising &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html?lang=fr) ».

## Données de conversion

Lorsqu’un client clique sur une publicité ou affiche une publicité pour les réseaux sociaux, Search, Social et Commerce doit mapper chaque conversion résultante au clic ou à l’affichage/à l’impression sur les réseaux sociaux d’origine.

L’annonceur joue un rôle dans la fourniture des données de conversion pour tous les clics et affichages/impressions sur les réseaux sociaux. Les données de conversion peuvent inclure des informations sur n’importe quel type d’événement se produisant sur un site web qui peuvent être utilisées pour l’optimisation des enchères. Vous pouvez fournir des données de conversion en implémentant le code de suivi des conversions dans les pages de conversion de l’annonceur (comme la page « succès » affichée une fois qu’un client a terminé une transaction) ou en envoyant un fichier de flux quotidien avec les données de conversion capturées par une autre méthode.

### Balises de suivi des conversions

Vous pouvez utiliser des [balises de conversion de différents fournisseurs](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Lorsque vous utilisez une balise de conversion Adobe Advertising et qu’un utilisateur effectue une transaction réussie et accède à une page « succès », le serveur de pixels d’Adobe Advertising vérifie l’existence du cookie sur l’ordinateur de l’utilisateur, qui a été défini au moment de la redirection par clic. Lorsqu’il trouve un cookie, les informations sur l’événement de transaction sont transmises à l’aide du paramètre ef_transid, et la transaction est reconnue comme une conversion et est créditée à l’impression de clic ou d’affichage publicitaire précédente.

Si l’utilisateur a cliqué sur plusieurs de vos publicités, Adobe Advertising crédite la transaction au clic publicitaire final ou (pour les campagnes d’affichage ou vidéo) à l’impression publicitaire finale, sauf indication contraire. Votre [intervalle de recherche en amont de clic](/help/search-social-commerce/glossary.md#c-d) et votre [intervalle de recherche en amont d’impression](/help/search-social-commerce/glossary.md#i-j) déterminent le nombre de jours après un clic payant ou une impression d’affichage/vidéo (respectivement) dans lesquels l’événement peut être attribué à une conversion.

L’équipe d’implémentation d’Adobe Advertising travaille avec l’annonceur pour déterminer le format des balises de conversion que l’annonceur doit implémenter, identifier les pages web sur lesquelles chaque balise de conversion doit être insérée, puis fournir les balises de conversion à implémenter.
