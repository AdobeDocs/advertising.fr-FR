---
title: Options de suivi des conversions pour Search, Social et Commerce
description: Découvrez les options de suivi de conversion pour Search, Social et Commerce.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Options de suivi des conversions pour Search, Social et Commerce

Search, Social et Commerce peuvent utiliser les données de conversion qui font l’objet d’un suivi comme suit :

* **Conversions suivies par l’Adobe Advertising :** L’annonceur insère une balise de suivi de conversion par Adobe Advertising sur chaque page de conversion. La balise envoie les données de conversion à un serveur de suivi. Vous pouvez utiliser le pixel tiers hérité ou le pixel propriétaire plus récent. Voir &quot;[Comparaison de chaque méthode de suivi de conversion](#conversion-tracking-comparison)&quot;.

* **Conversions Adobe Analytics :** L’annonceur utilise le suivi Adobe Analytics pour toutes les conversions. Cette option nécessite une intégration Adobe Advertising-Adobe Analytics. Pour plus d’informations, voir &quot;[Suivi de conversion Adobe Analytics](conversion-tracking-analytics.md)&quot;.

* **[!DNL Google Analytics]conversions :** L’annonceur utilise la balise [!DNL Google Analytics] pour effectuer le suivi de toutes les conversions. Voir &quot;[[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; pour plus d’informations sur les conversions qui sont automatiquement synchronisées.

* **Conconversions suivies par les annonceurs :** (clients Search, Social et Commerce uniquement) L’annonceur fournit à Search, Social et Commerce un fichier de flux avec toute combinaison de données de conversion en ligne et hors ligne. Voir &quot;[Suivi des conversions à l’aide d’un flux d’identifiant EF](feed-efid.md)&quot; et &quot;[Suivi des conversions à l’aide d’un flux d’ID de transaction](feed-transaction-id.md)&quot;.

## Comparaison de chaque méthode de suivi de conversion {#conversion-tracking-comparison}

À mesure que les stratégies de cookies de navigateur deviennent plus strictes, il est important de comprendre vos fonctionnalités de suivi actuelles et d’identifier vos meilleures options à plus long terme.

| Méthode de suivi | Description | Limites | Avantages | Recommandé ? |
|----|----|----|----|----|
| Adobe Analytics | Les annonceurs disposant de [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=fr) importent automatiquement leurs [!DNL Analytics] événements standard et personnalisés dans Adobe Advertising pour la création de rapports et l’optimisation. | <ul><li>[!DNL Safari] autorise uniquement une recherche en amont de conversion de sept jours, qui est réinitialisée lors des visites répétées du site pendant l’intervalle de recherche en amont.</li><li> Attendez-vous à des limitations similaires dans [!DNL Chrome] en 2024.</li></ul> | <ul><li>Intégration transparente avec [!DNL Analytics]</li> <li>Voir les données de recherche payante dans [!DNL Analytics] Analysis Workspace</li><li>Avantages au-delà de la recherche payante</li></ul> | Oui |
| Pixel d’Adobe Advertising hérité | Les annonceurs ajoutent une image d’Adobe Advertising héritée ou des pixels JavaScript à leurs pages de conversion. Le pixel se déclenche lorsqu’un utilisateur a cliqué sur une publicité pour atteindre la page. Cette méthode repose sur des cookies tiers. | <ul><li>[!DNL Safari] bloque tout le suivi de conversion à l’aide de cette méthode.</li><li>Attendez-vous à des limitations similaires dans [!DNL Chrome] en 2024.</li></ul> | Le pixel est déjà implémenté. Cependant, vous devez toujours [mettre en oeuvre la balise de mappage ITP supplémentaire](itp-conversion-mapping-tag.md).<br><br>Recommandation : basculez vers le pixel propriétaire. | Non |
| Adobe Advertising de pixel propriétaire | Les annonceurs effectuent les opérations suivantes : <ul><li>Implémentez la bibliothèque JavaScript pour le [service Adobe Experience Cloud ID (ECID) ](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=fr) sur l’ensemble de leur site.</li><li>Ajoutez les [balises JavaScript avec mappage ITP](itp-conversion-mapping-tag.md) Adobe Advertising à n’importe quelle page pouvant être une page d’entrée à partir d’un clic de recherche (idéalement, sur toutes les pages, car les pages d’entrée peuvent changer au fil du temps). La balise permet à l’Adobe Advertising de suivre un événement de conversion qui se produit sur une page qui convertit de grands nombres en notation scientifique sur la page d’entrée.</li><li>Ajoutez la balise de suivi de conversion [JavaScript version 3](format-conversion-tag-jsv3.md) Adobe Advertising aux pages de conversion.</li></ul> | <ul><li>[!DNL Safari] autorise uniquement une recherche en amont de conversion de sept jours, qui est réinitialisée lors des visites répétées du site pendant l’intervalle de recherche en amont.</li><li>Attendez-vous à des limitations similaires dans [!DNL Chrome] en 2022.</li></ul> | [!DNL Safari] effectue le suivi des conversions pendant la recherche en amont de sept jours. La recherche en amont étant réinitialisée lors des visites répétées du site pendant l’intervalle de recherche en amont, la limitation n’affecte pas tous les utilisateurs de [!DNL Safari]. | Non |
| Flux EFID | Les comptes de recherche de l’annonceur sont configurés pour générer des URL de destination/URL finales avec des identifiants uniques d’Adobe Advertising (jetons). Lorsqu’un utilisateur clique sur une publicité, l’Adobe Advertising crée un identifiant unique (`EFID`) et l’affiche à la fin de l’URL finale. Le système client de l’annonceur capture l’EFID en tant qu’identifiant unique des conversions résultant du clic et l’envoie à l’Adobe Advertising dans un flux de recettes qui inclut l’EFID, la date de transaction et la mesure de conversion. Adobe Advertising utilise ensuite l’EFID pour faire correspondre la conversion au clic d’origine. | <ul><li>L’annonceur doit avoir un moyen de capturer l’EFID et d’envoyer quotidiennement des flux automatisés à l’Adobe Advertising.</li><li>Les conversions peuvent être suivies pendant 180 jours au maximum (par Adobe Advertising) ou selon les limites du système de l’annonceur.</li></ul> | <ul><li>Cette méthode utilise des données de conversion propriétaires, de sorte qu’elles ne sont pas affectées par les limites des cookies tiers.</li><li>Les conversions en ligne et hors ligne peuvent être envoyées dans un seul flux.</li><li>Aucune modification de code ou balise n’est requise pour le site.</li></ul> | Oui |
| Flux d’ID de transaction [ flux combiné ] | Les annonceurs ajoutent des pixels d’Adobe Advertising qui incluent un paramètre pour un ID de transaction unique (`ev_transid=&lt;transid&gt;`) à leurs pages web, et l’Adobe Advertising capture l’ID de transaction unique créé lors du déclenchement du pixel. Le système client de l’annonceur capture également le [!UICONTROL Transaction ID] et envoie un flux de recettes pour les conversions hors ligne avec les valeurs [!UICONTROL Transaction ID] correspondantes. | <ul><li>Si l’annonceur utilise le pixel hérité, qui [!DNL Safari] empêche le déclenchement, l’ID n’est pas capturé pour être utilisé pour les données hors ligne.</li><li>Le flux n’est pas automatisé.</li></ul> | <ul><li>Si vous implémentez le pixel propriétaire, alors le [!UICONTROL Transaction ID] est capturé dans [!DNL Safari].</li><li>Permet le suivi des événements de conversion hors ligne/approuvés.</li></ul> | Non |
| [!DNL Google] Conversions | Les conversions suivies avec des balises [!DNL Google Analytics] sont automatiquement importées en Adobe Advertising via une connexion API. Chaque nom de conversion comporte un préfixe `&quot;GGL_&quot;`. | <ul><li>[!DNL Google] ne suit généralement pas les données hors ligne.</li><li>[!DNL Microsoft Advertising] conversions non incluses.</li></ul> | [!DNL Google] utilise l’apprentissage automatique pour extrapoler &quot;[conversions modélisées](https://support.google.com/google-ads/answer/10081327)&quot;. | Non |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [ À propos des balises de suivi de conversion d’Adobe Advertising ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Suivi de conversion Adobe Analytics](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Suivi des conversions à l’aide d’un flux d’identifiant EF](/help/search-social-commerce/tracking/feed-efid.md)
>* [Suivi des conversions à l’aide d’un flux d’ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id.md)
