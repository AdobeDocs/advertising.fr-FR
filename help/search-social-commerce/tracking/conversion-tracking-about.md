---
title: Options de suivi des conversions pour Search, Social et Commerce
description: Découvrez les options de suivi de conversion pour Search, Social et Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Options de suivi des conversions pour Search, Social et Commerce

Adobe Advertising peut utiliser des données de conversion qui sont suivies comme suit :

* **Conversions suivies par Adobe Advertising :** L’annonceur insère une balise de suivi de conversion Adobe Advertising sur chaque page de conversion. La balise envoie les données de conversion à un serveur de suivi. Vous pouvez utiliser le pixel tiers hérité ou le pixel propriétaire plus récent. Voir &quot;[Comparaison de chaque méthode de suivi de conversion](#conversion-tracking-comparison).&quot;

* **Conversions Adobe Analytics :** L’annonceur utilise le suivi Adobe Analytics pour toutes les conversions. Cette option nécessite une intégration Advertising-Adobe Analytics Adobe. Voir &quot;[Suivi des conversions Adobe Analytics](conversion-tracking-analytics.md)&quot; pour plus d’informations.

* **[!DNL Google Analytics]conversions :** L’annonceur utilise la variable [!DNL Google Analytics] pour effectuer le suivi de toutes les conversions. Voir &quot;[[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; pour plus d’informations sur les conversions automatiquement synchronisées.

* **Conversions suivies par les annonceurs :** (Clients Search, Social et Commerce uniquement) L’annonceur fournit à Search, Social et Commerce un fichier de flux contenant toute combinaison de données de conversion en ligne et hors ligne. Voir &quot;[Suivi des conversions à l’aide d’un flux d’identifiant EF](feed-efid.md)&quot; et &quot;[Suivi des conversions à l’aide d’un flux d’ID de transaction](feed-transaction-id.md).&quot;

## Comparaison de chaque méthode de suivi de conversion {#conversion-tracking-comparison}

À mesure que les stratégies de cookies de navigateur deviennent plus strictes, il est important de comprendre vos fonctionnalités de suivi actuelles et d’identifier vos meilleures options à plus long terme.

| Méthode de suivi | Description | Limites | Avantages | Recommandé ? |
|----|----|----|----|----|
| Adobe Analytics | Annonceurs avec [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importez automatiquement leurs [!DNL Analytics] événements standard et personnalisés pour Adobe de la publicité à des fins de création de rapports et d’optimisation. | <ul><li>[!DNL Safari] ne permet qu’une recherche en amont de conversion de sept jours, qui est réinitialisée lors des visites répétées du site pendant l’intervalle de recherche en amont.</li><li> Vous pouvez vous attendre à des limitations similaires dans [!DNL Chrome] en 2024.</li></ul> | <ul><li>Intégration transparente avec [!DNL Analytics]</li> <li>Voir Données de recherche payante dans [!DNL Analytics] Analysis Workspace</li><li>Avantages au-delà de la recherche payante</li></ul> | Oui |
| Ancien pixel de publicité d’Adobe | Les annonceurs ajoutent une image Adobe Advertising ou des pixels JavaScript hérités à leurs pages de conversion. Le pixel se déclenche lorsqu’un utilisateur a cliqué sur une publicité pour atteindre la page. Cette méthode repose sur des cookies tiers. | <ul><li>[!DNL Safari] bloque tout suivi de conversion utilisant cette méthode.</li><li>Vous pouvez vous attendre à des limitations similaires dans [!DNL Chrome] en 2024.</li></ul> | Le pixel est déjà implémenté. Cependant, vous devez toujours [implémentation de la balise de mappage ITP supplémentaire](itp-conversion-mapping-tag.md).<br><br>Recommandation : Passez au pixel propriétaire. | Non |
| Pixel propriétaire Adobe Advertising | Les annonceurs effectuent les opérations suivantes : <ul><li>Mise en oeuvre de la bibliothèque JavaScript pour le [Service Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) sur l’ensemble du site.</li><li>Ajout de l’Adobe Advertising [Balises JavaScript avec mappage ITP](itp-conversion-mapping-tag.md) à n’importe quelle page pouvant être une page d’entrée à partir d’un clic de recherche (idéalement, sur toutes les pages, car les pages d’entrée peuvent changer au fil du temps). La balise permet à Adobe Advertising de suivre un événement de conversion qui se produit sur une page qui convertit de grands nombres en notation scientifique sur la page d’entrée.</li><li>Ajout de l’Adobe Advertising [Balise de suivi de conversion JavaScript v3](format-conversion-tag-jsv3.md) aux pages de conversion.</li></ul> | <ul><li>[!DNL Safari] ne permet qu’une recherche en amont de conversion de sept jours, qui est réinitialisée lors des visites répétées du site pendant l’intervalle de recherche en amont.</li><li>Vous pouvez vous attendre à des limitations similaires dans [!DNL Chrome] en 2022.</li></ul> | [!DNL Safari] effectue le suivi des conversions pendant la recherche en amont de sept jours. La recherche en amont étant réinitialisée lors des visites répétées du site pendant l’intervalle de recherche en amont, la limitation n’affecte pas toutes les [!DNL Safari] utilisateurs. | Non |
| Flux EFID | Les comptes de recherche de l’annonceur sont configurés pour générer des URL de destination/URL finales avec des identifiants (jetons) uniques de publicité Adobe. Lorsqu’un utilisateur clique sur une publicité, Adobe Advertising crée un identifiant unique (`EFID`) et l’affiche à la fin de l’URL finale. Le système client de l’annonceur capture l’EFID en tant qu’identifiant unique des conversions résultant du clic et l’envoie à Adobe Advertising dans un flux de recettes qui inclut l’EFID, la date de transaction et la propriété de conversion. Adobe Advertising utilise ensuite l’EFID pour faire correspondre la conversion au clic d’origine. | <ul><li>L’annonceur doit avoir un moyen de capturer l’EFID et d’envoyer quotidiennement des flux automatisés à Adobe Advertising.</li><li>Les conversions peuvent être suivies pendant 180 jours au maximum (par publicité Adobe) ou selon les limites du système de l’annonceur.</li></ul> | <ul><li>Cette méthode utilise des données de conversion propriétaires, de sorte qu’elles ne sont pas affectées par les limites des cookies tiers.</li><li>Les conversions en ligne et hors ligne peuvent être envoyées dans un seul flux.</li><li>Aucune modification de code ou balise n’est requise pour le site.</li></ul> | Oui |
| Flux d’ID de transaction [flux combiné] | Les annonceurs ajoutent des pixels Adobe Advertising qui incluent un paramètre pour un ID de transaction unique (`ev_transid=&lt;transid&gt;`) sur leurs pages web, et Adobe Advertising capture l’identifiant de transaction unique créé lors du déclenchement du pixel. Le système client de l’annonceur capture également la variable [!UICONTROL Transaction ID] et envoie à Adobe Advertising un flux de recettes pour les conversions hors ligne avec une correspondance [!UICONTROL Transaction ID] values | <ul><li>Si l’annonceur utilise le pixel hérité, qui [!DNL Safari] empêche de se déclencher, l’ID n’est pas capturé pour être utilisé pour les données hors ligne.</li><li>Le flux n’est pas automatisé.</li></ul> | <ul><li>Si vous implémentez le pixel propriétaire, la variable [!UICONTROL Transaction ID] est capturé dans [!DNL Safari].</li><li>Permet le suivi des événements de conversion hors ligne/approuvés.</li></ul> | Non |
| Conversions Google | Conversions suivies avec [!DNL Google Analytics] Les balises sont automatiquement importées dans Adobe Advertising via une connexion API. Chaque nom de conversion comporte une `&quot;GGL_&quot;` préfixe. | <ul><li>Google ne suit généralement pas les données hors ligne.</li><li>Les conversions publicitaires Microsoft® ne sont pas incluses.</li></ul> | Google utilise l’apprentissage automatique pour extrapoler &quot;[conversions modélisées](https://support.google.com/google-ads/answer/10081327).&quot; | Non |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [À propos des balises de suivi de conversion Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Suivi des conversions Adobe Analytics](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Suivi des conversions à l’aide d’un flux d’identifiant EF](/help/search-social-commerce/tracking/feed-efid.md)
>* [Suivi des conversions à l’aide d’un flux d’ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id.md)

