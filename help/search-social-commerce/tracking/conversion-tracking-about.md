---
title: Options de suivi des conversions pour Search, Social et Commerce
description: Découvrez les options de suivi des conversions pour Search, Social et Commerce.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
TQID: https://experienceleague.adobe.com/Zv-ncIkpwqM24hoF9I2T8Er9Qf8R0j2fJSSk4jI7HSo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 821
ht-degree: 0%

---

# Options de suivi des conversions pour Search, Social et Commerce

Search, Social et Commerce peuvent utiliser les données de conversion qui sont suivies des manières suivantes :

* **Conversions suivies par Adobe Advertising :** l’annonceur insère une balise de suivi des conversions Adobe Advertising sur chaque page de conversion. La balise envoie les données de conversion à un serveur de suivi. Vous pouvez utiliser l’ancien pixel tiers ou le pixel propriétaire plus récent. Voir « [Comparaison de chaque méthode de suivi des conversions](#conversion-tracking-comparison) ».

* **Conversions Adobe Analytics :** l’annonceur utilise le suivi Adobe Analytics pour toutes les conversions. Cette option nécessite une intégration Adobe Advertising-Adobe Analytics. Voir « [Suivi des conversions Adobe Analytics &#x200B;](conversion-tracking-analytics.md) » pour plus d’informations.

* **[!DNL Google Analytics]des conversions :** l’annonceur utilise la balise [!DNL Google Analytics] pour suivre toutes les conversions. Pour plus d’informations sur les conversions automatiquement synchronisées, voir « [[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) ».

* **Conversions suivies par l’annonceur :** (clients Search, Social et Commerce uniquement) L’annonceur fournit à Search, Social et Commerce un fichier de flux avec n’importe quelle combinaison de données de conversion en ligne et hors ligne. Voir « [Suivi des conversions à l’aide d’un flux d’ID de FE](feed-efid.md) » et « [Suivi des conversions à l’aide d’un flux d’ID de transaction](feed-transaction-id.md) ».

## Comparaison de chaque méthode de suivi des conversions {#conversion-tracking-comparison}

Alors que les politiques en matière de cookies de navigateur continuent de devenir plus strictes, il est important de comprendre vos fonctionnalités de tracking actuelles et d’identifier vos meilleures options à long terme.

| Méthode de suivi | Description | Restrictions | Avantages | Recommandé ? |
|----|----|----|----|----|
| Adobe Analytics | Les annonceurs qui utilisent [Adobe Analytics pour Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=fr) importent automatiquement leurs événements [!DNL Analytics] standard et personnalisés dans Adobe Advertising à des fins de création de rapports et d’optimisation. | <ul><li>[!DNL Safari] n’autorise qu’une recherche arrière de conversion de sept jours, qui est réinitialisée lors de visites répétées du site pendant l’intervalle de recherche arrière.</li><li> Attendez-vous à des limitations similaires en [!DNL Chrome] en 2024.</li></ul> | <ul><li>Intégration transparente à [!DNL Analytics]</li> <li>Voir Données de référencement payant dans [!DNL Analytics] Analysis Workspace</li><li>Avantages au-delà du référencement payant</li></ul> | Oui |
| Ancien pixel Adobe Advertising | Les annonceurs ajoutent des pixels Adobe Advertising ou JavaScript hérités à leurs pages de conversion. Le pixel se déclenche lorsqu’un utilisateur ou une utilisatrice qui a cliqué sur une publicité atteint la page. Cette méthode repose sur des cookies tiers. | <ul><li>[!DNL Safari] bloque tout suivi des conversions à l’aide de cette méthode.</li><li>Attendez-vous à des limitations similaires en [!DNL Chrome] en 2024.</li></ul> | Le pixel est déjà implémenté. Cependant, vous devez toujours [implémenter la balise de mappage ITP supplémentaire](itp-conversion-mapping-tag.md).<br><br>Recommandation : passez au pixel propriétaire. | Non |
| Pixel propriétaire Adobe Advertising | Les annonceurs effectuent les opérations suivantes : <ul><li>Implémentez la bibliothèque JavaScript pour le service [Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=fr) sur l’ensemble de leur site.</li><li>Ajoutez les balises Adobe Advertising [JavaScript avec mappage ITP](itp-conversion-mapping-tag.md) à n’importe quelle page qui peut être une page de destination à partir d’un clic de recherche (idéalement, sur toutes les pages, car les pages de destination peuvent changer au fil du temps). La balise permet à Adobe Advertising de suivre un événement de conversion qui se produit sur une page qui convertit de grands nombres en notation scientifique sur la page de destination.</li><li>Ajoutez la balise de suivi des conversions Adobe Advertising [JavaScript v3](format-conversion-tag-jsv3.md) aux pages de conversion.</li></ul> | <ul><li>[!DNL Safari] n’autorise qu’une recherche arrière de conversion de sept jours, qui est réinitialisée lors de visites répétées du site pendant l’intervalle de recherche arrière.</li><li>Attendez-vous à des limitations similaires en [!DNL Chrome] en 2022.</li></ul> | [!DNL Safari] effectue le suivi des conversions pendant la recherche en amont de sept jours. Comme la recherche en amont est réinitialisée lors de visites répétées du site pendant l’intervalle de recherche en amont, la limitation n’affecte pas tous les utilisateurs [!DNL Safari]. | Non |
| Flux EFID | Les comptes de recherche de l’annonceur sont configurés pour générer des URL de destination/URL finales avec des ID uniques Adobe Advertising (jetons). Lorsqu’un utilisateur clique sur une publicité, Adobe Advertising crée un identifiant unique (`EFID`) et l’affiche à la fin de l’URL finale. Le système client de l’annonceur capture l’EFID comme identifiant unique pour les conversions qui résultent du clic et l’envoie à Adobe Advertising dans un flux de recettes qui inclut l’EFID, la date de transaction et la mesure de conversion. Adobe Advertising utilise ensuite l’EFID pour faire correspondre la conversion au clic d’origine. | <ul><li>L’annonceur doit avoir un moyen de capturer l’EFID et d’envoyer quotidiennement des flux automatisés à Adobe Advertising.</li><li>Les conversions peuvent faire l’objet d’un suivi pendant 180 jours au maximum (par Adobe Advertising) ou selon les limites du système de l’annonceur.</li></ul> | <ul><li>Cette méthode utilise des données de conversion propriétaires ; elle n’est donc pas affectée par les limitations des cookies tiers.</li><li>Les conversions en ligne et hors ligne peuvent être envoyées dans un seul flux.</li><li>Aucune modification de code ni balise n’est requise pour le site.</li></ul> | Oui |
| Flux d’ID de transaction [flux combiné] | Les annonceurs ajoutent des pixels Adobe Advertising qui incluent un paramètre pour un ID de transaction unique (`ev_transid=&lt;transid&gt;`) à leurs pages web et Adobe Advertising capture l’ID de transaction unique créé lors du déclenchement du pixel. Le système client de l’annonceur capture également le [!UICONTROL Transaction ID] et envoie à Adobe Advertising un flux de revenus pour les conversions hors ligne avec les valeurs de [!UICONTROL Transaction ID] correspondantes | <ul><li>Si l’annonceur utilise le pixel hérité, ce qui [!DNL Safari] empêche le déclenchement de , l’identifiant n’est pas capturé pour utiliser les données hors ligne.</li><li>Le flux n&#39;est pas automatisé.</li></ul> | <ul><li>Si vous implémentez le pixel propriétaire, le [!UICONTROL Transaction ID] est capturé dans [!DNL Safari].</li><li>Fournit le suivi des événements de conversion hors ligne/approuvés.</li></ul> | Non |
| Conversions [!DNL Google] | Les conversions suivies avec des balises [!DNL Google Analytics] sont automatiquement importées vers Adobe Advertising via une connexion API. Chaque nom de conversion comporte un préfixe `&quot;GGL_&quot;`. | <ul><li>[!DNL Google] ne suit généralement pas les données hors ligne.</li><li>Les conversions [!DNL Microsoft Advertising] ne sont pas incluses.</li></ul> | [!DNL Google] utilise le machine learning pour extrapoler des « conversions [&#x200B; modélisées &#x200B;](https://support.google.com/google-ads/answer/10081327). » | Non |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [À propos des balises de suivi des conversions Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Suivi des conversions &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Suivi des conversions à l’aide d’un flux d’ID EF](/help/search-social-commerce/tracking/feed-efid.md)
>* [Suivi des conversions à l’aide d’un flux d’ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id.md)
