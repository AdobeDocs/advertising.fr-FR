---
title: Configuration du suivi de conversion pour vos pages web
description: Découvrez comment activer Adobe Advertising pour effectuer le suivi des conversions résultant des impressions publicitaires et des clics.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Configuration du suivi de conversion pour vos pages web

Avant de pouvoir générer des rapports sur les données de conversion, Adobe Advertising nécessite des données d’impression, de clic, de coût et de conversion (transaction) pour chacun de vos mots-clés et annonces. Adobe Advertising utilise également ces données pour créer les modèles de prévision de données dont il a besoin pour optimiser les budgets de campagne et les offres sur vos mots-clés et publicités.

Pour permettre à Adobe Advertising de suivre les conversions résultant des impressions publicitaires et des clics, vous devez procéder comme suit :

* Insérez un code de suivi des clics unique (et éventuellement un code supplémentaire pour rediriger l’utilisateur vers un serveur de suivi) dans le modèle de suivi ou l’URL de destination pour chaque mot-clé, annonce, emplacement, lien de site et groupe de produits dans chaque campagne publicitaire gérée par Search, Social et Commerce. Cela permet à Adobe Advertising de suivre chaque impression d’annonce (pour les publicités display et sociales uniquement) et chaque clic sur une publicité.

* Effectuez le suivi des données de conversion de l’une des manières suivantes :

   * **Conversions suivies par Adobe Advertising :** L’annonceur insère une balise de suivi de conversion Adobe Advertising sur chaque page de conversion.

   * **Conversions Adobe Analytics :** L’annonceur utilise le suivi Adobe Analytics pour toutes les conversions.

   * **[!DNL Google Analytics]conversions :** L’annonceur utilise la variable [!DNL Google Analytics] pour effectuer le suivi de toutes les conversions.

   * **Conversions suivies par les annonceurs :** L’annonceur fournit un fichier de flux quotidien avec toute combinaison de données de conversion en ligne et hors ligne.

Pour plus d’informations sur l’implémentation du suivi, reportez-vous au chapitre d’aide &quot;Tracking&quot;.

>[!MORELIKETHIS]
>
>* [Génération d’une balise de conversion Advertising Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Générez une URL de suivi des clics Search, Social et Commerce à l’aide de l’outil de suivi des URL.](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [Décodage d’une URL de suivi des clics Search, Social et Commerce](/help/search-social-commerce/tools/click-tracking-url-decode.md)

