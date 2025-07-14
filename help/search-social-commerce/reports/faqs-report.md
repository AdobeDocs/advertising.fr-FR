---
title: Questions fréquentes sur les rapports personnalisés
description: Découvrez les réponses aux questions courantes sur les rapports de performance, y compris le dépannage des problèmes de données.
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: 01fe9264fee43ed29f6cee022dadeb29fbd26f45
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# Questions fréquentes sur les rapports personnalisés

## Questions générales

+++Que faire si la période du rapport commence avant que les données du rapport ne soient disponibles ?
Le rapport est généré, mais il inclut uniquement les données relatives aux dates pour lesquelles des données sont disponibles. Pour plus d’informations sur la disponibilité des données pour chaque type de rapport, voir « [Les données utilisées pour les rapports](data-used-for-reports.md) ».
+++

+++Quelle est la différence entre les rapports basés sur la date de clic et ceux basés sur la date de transaction ?
Lorsque vous éditez les conversions par date de transaction, les données incluent les transactions dont la date de transaction s&#39;est produite au cours de la période spécifiée. Il s’agit du paramètre par défaut des rapports de base et des rapports avancés. Il indique le montant des revenus générés au cours de la période spécifiée.

Lorsque vous signalez des conversions par date de clic, les données incluent les transactions résultant d’un clic survenu au cours de la période spécifiée. Lorsqu’un portefeuille présente des retards importants entre les clics et les transactions, ce type de rapport affiche le chiffre d’affaires historique par clic pour le portefeuille, ce qui vous donne une idée des comportements de chiffre d’affaires à attendre au fil du temps.

![Date du clic par rapport à la date du mouvement](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Date du clic par rapport à la date du mouvement")
+++

+++Que se passe-t-il si je modifie l’intervalle de recherche en amont des clics ou des impressions ?
(Publicitaires avec service de suivi des conversions basé sur les pixels d’Advertising uniquement) Les données des événements résultant du clic initial sont collectées pour une période plus longue ou plus courte.

L’intervalle de recherche en amont de clic ([click lookback window](/help/search-social-commerce/glossary.md#c-d)) et l’intervalle de recherche en amont d’impression ([impression)](/help/search-social-commerce/glossary.md#i-j) d’un annonceur déterminent le nombre de jours après un clic payé ou une impression d’affichage (respectivement) dans lesquels l’événement peut être attribué à une conversion. Le fait de définir une valeur sur une période plus longue ou plus courte peut s’avérer important pour les annonceurs dont les périodes de clic sur le chiffre d’affaires ou d’impression sur le chiffre d’affaires sont particulièrement courtes ou longues.

**Bonne pratique :** assurez-vous que les intervalles de recherche en amont sont plus longs que les temps de clic sur le chiffre d’affaires et affichez le temps d’impression sur le chiffre d’affaires pour la plupart des mots-clés ou des annonces. Lorsqu’elles sont plus courtes, certaines conversions ne sont pas associées au clic ou à l’impression initiaux.
+++

+++Comment savoir quelles conversions ont résulté d’une extension d’annonce [!DNL Google Ads] ou d’une liste de produits ?
Vous pouvez voir quelles conversions ont résulté d’un clic sur une extension d’annonce [!DNL Google Ads] (plutôt que sur l’annonce elle-même) ou sur une liste de produits en générant une [!UICONTROL Transaction Report]. La valeur de la colonne [!UICONTROL Link Type] affiche le type et le titre d’un lien sur lequel l’utilisateur a cliqué :

* Les listes de produits sont répertoriées comme `pla:<product ID>`, par exemple `pla:8525822`.

* Les liens de site sont répertoriés comme `sl:<Sitelink text>`, par exemple `sl:See Current Offers`.

  Vous pouvez également identifier un lien de site si vous incluez la colonne [!UICONTROL Tracking URL] dans le rapport. La [!UICONTROL Tracking URL] d’un lien de site inclut l’attribut `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Les conversions à partir d’emplacements [!DNL Google Ads] et d’extensions de téléphone sont incluses dans les données pour les publicités qu’elles accompagnent. Ils ne sont pas déclarés séparément.

+++

+++La colonne « [!UICONTROL Keyword] » de mon rapport inclut une valeur « (contenu du groupe publicitaire) &lt;*nom du groupe publicitaire*>. »
Lorsque la ligne inclut des données pour les campagnes de recherche de contenu, les campagnes d’affichage ou les campagnes sur les réseaux sociaux (qui n’incluent pas de mots-clés), la colonne [!UICONTROL Keyword] affiche à la place le nom du groupe publicitaire applicable.
+++

+++En raison des changements saisonniers ou du marché, mes rapports présentent des données atypiques. Cela affecte-t-il les enchères une fois que les conditions changent ?
La fonctionnalité d’optimisation crée quotidiennement ses modèles de chiffre d’affaires pour chaque unité de soumission afin de s’assurer qu’elle identifie les tendances et qu’elle y répond immédiatement. Les modèles incorporent également des données historiques à long terme pour aider à prédire la performance saisonnière. Le paramètre de demi-vie du modèle de revenus du portefeuille détermine également <!-- add link to glossary? --> pondération des données récentes sur les revenus. La bonne pratique consiste à réduire la demi-vie pendant une période de performances atypiques, mais à l’augmenter après ajustement du modèle de chiffre d’affaires. Si vous avez des questions sur la nécessité d’ajuster la demi-vie, contactez l’équipe chargée de votre compte Adobe.

Si vous ne souhaitez pas que les données de la période affectent les enchères futures, vous pouvez choisir d&#39;exclure ces dates du modèle. Contactez l’équipe chargée de votre compte Adobe pour exclure les dates.
+++

+++Puis-je créer un rapport sur une mesure de propriété de compte spécifique, telle que [!UICONTROL Device] ou [!UICONTROL Objective Name] ?
Pour les rapports d’entités de campagne ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] et [!UICONTROL Product Group Report]), les données de mesures sont agrégées dynamiquement par les colonnes de propriétés que vous incluez dans le rapport. Vous avez la possibilité de supprimer la colonne clé du rapport et de n’inclure que les colonnes de propriétés pour lesquelles vous souhaitez agréger les données.

Par exemple, si vous générez un [!UICONTROL Keyword Report] qui inclut les colonnes [!UICONTROL Ad Group] et  Appareil , le rapport agrège par défaut les mesures de chaque mot-clé par groupe publicitaire et type d’appareil. Cependant, si vous supprimez la colonne [!UICONTROL Keyword] avant de générer le rapport, celui-ci génère alors de manière dynamique des mesures pour les groupes publicitaires spécifiés par type d’appareil.

>[!NOTE]
>
>Vous ne pouvez pas utiliser cette fonctionnalité pour agréger les données par classification de libellés. Toutes les colonnes de classification de libellé du rapport sont omises. Utilisez plutôt le rapport [Classification de libellés](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Problèmes généraux liés aux données

+++Les rapports générés à l’aide de différentes règles d’attribution affichent des totaux différents.
Si vous générez un rapport plusieurs fois à l’aide des mêmes paramètres de rapport, mais avec des règles d’attribution différentes, les données peuvent différer pour l’une des raisons suivantes :

* Les données basées sur la date de clic peuvent se trouver en dehors de la période spécifiée.

  Si vous utilisez le paramètre d&#39;état « [!UICONTROL Conversions based on click date] », la période spécifiée s&#39;applique à la date du clic plutôt qu&#39;à la date de la transaction. Si le rapport utilise également la règle d’attribution « Premier événement » ou « Dernier événement », le premier ou le dernier événement qui a entraîné la conversion peut se trouver en dehors de la période spécifiée. Supposons, par exemple, qu’un utilisateur ait cliqué sur Mot-clé_1 le 30 avril, sur Mot-clé_2 le 20 mai et converti le 21 mai. Si le rapport utilise la règle d’attribution « [!UICONTROL First Event] » et une période comprise entre le 1er et le 21 mai, le premier événement (un clic sur Mot-clé_1 le 30 avril) n’est pas inclus dans le rapport. Si vous exécutez le rapport avec la même période, mais en utilisant la règle d’attribution « [!UICONTROL Last Event] », la conversion est incluse dans le rapport, car le dernier clic s’est produit au cours de la période spécifiée.

* La sélection du filtre de portfolio exclut certains des événements menant à la conversion.

  Si vous créez des rapports sur un sous-ensemble de portfolios, il se peut que vous n’incluiez pas les campagnes qui incluaient l’événement auquel la conversion a été attribuée sous l’une des règles d’attribution. Supposons, par exemple, qu’un utilisateur clique sur Mot-clé_1 dans Portfolio_1, sur Mot-clé_2 dans Portfolio_2, puis effectue une conversion. Si le rapport utilise la règle d’attribution « [!UICONTROL First Event] », Portfolio_1 doit être inclus pour que la conversion soit incluse dans le rapport. Cependant, si le rapport utilise la règle d’attribution « Dernier événement », Portfolio_2 doit être inclus.

>[!TIP]
>
>Si vous souhaitez comparer les totaux de conversion sous différentes règles d’attribution, exécutez les rapports à l’aide du paramètre de rapport « [!UICONTROL Conversions based on transaction date] » et sélectionnez tous les réseaux publicitaires ou tous les portfolios. Si vous ne définissez aucun autre filtre, les totaux de conversion doivent correspondre.

+++

+++Les champs de données individuels sont incorrects, bien que les totaux soient corrects.
Cette situation peut se produire lorsque les formats de mesure utilisent des entiers :

* Si vous créez une [mesure personnalisée](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) au format *Nombre sans décimales* (qui affiche les données sous forme d’entiers) et que vous l’incluez dans une vue ou un rapport qui utilise une règle d’attribution de conversion pondérée ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] ou [!UICONTROL Even Distribution]), la sortie s’affiche sous forme d’entiers, et non de décimales. Dans ce cas, les champs de données individuels peuvent être incorrects, bien que les totaux soient corrects. Par exemple, si un ordre est divisé de manière égale entre trois événements, un ordre (plutôt que 0,33 ordre) est attribué à chacun des trois événements. Pour résoudre le problème, [modifiez le format de la mesure](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) en *Nombre à 2 décimales*.

* De même, si vous disposez d’une mesure de chiffre d’affaires envoyé comme dans un entier, le même problème se produit. (Le format des revenus est contrôlé par la balise de conversion qui envoie les données.) Pour résoudre ce problème, [créez une mesure personnalisée](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) composée uniquement de la mesure de chiffre d’affaires et au format *Nombre à 2 décimales*, et incluez-la dans les vues et les rapports plutôt que dans la mesure d’origine.
+++

+++Lorsque des données sur les clics ou le chiffre d’affaires sont manquantes, comment les empêcher d’affecter les enchères futures ?
Les problèmes de données de clic se produisent lorsque Search, Social et Commerce ne sont pas synchronisés avec le réseau publicitaire. Contactez l’équipe chargée de votre compte Adobe pour synchroniser manuellement le compte. Si des données de clics sont manquantes pour une journée entière, demandez à l’équipe chargée de votre compte Adobe d’exclure ce jour des modèles de coûts.

Des problèmes de données de chiffre d’affaires peuvent survenir en raison d’un problème de fichier de tracking ou de flux. Contactez l’équipe chargée de votre compte Adobe pour enquêter sur le problème. Si les données sur le chiffre d’affaires sont manquantes pour une journée entière, demandez à l’équipe chargée de votre compte Adobe d’exclure ce jour des modèles de chiffre d’affaires.
+++

+++Les données monétaires ne sont pas présentées dans le bon format.
Par défaut, toutes les données monétaires des rapports sont présentées en dollars américains (par exemple 1 000,00). Pour afficher la valeur au format de devise approprié (mais sans aucun symbole de devise aux formats CSV et TSV), ajoutez la colonne « [!UICONTROL Currency] » au rapport. Si le rapport inclut des données pour des comptes avec différentes devises, les valeurs monétaires « [!UICONTROL Total] » sont simplement la somme de tous les nombres de la colonne, quelle que soit la devise.
+++

+++Pourquoi les valeurs décimales d’une mesure de conversion qui doit être un nombre naturel (1, 2, etc.) s’affichent-elles ?
Vous pouvez voir des valeurs décimales dans les cas suivants :

* Si vous avez exécuté le rapport à l’aide d’un paramètre de règle d’attribution de conversion autre que [!UICONTROL Last Event] ou [!UICONTROL First Event], le chiffre d’affaires peut être fractionné entre plusieurs événements dans le chemin de conversion.

* Dans le [!UICONTROL Transaction Report], si plusieurs [unités d’enchères](/help/search-social-commerce/glossary.md#a-b) avec différents types de correspondance ont le même ID de transaction, le chiffre d’affaires de l’ID de suivi est fractionné en fonction du nombre de clics effectués à la date de clic spécifiée.
+++

## Mesures de performances standard

+++Les données relatives aux clics sont manquantes dans les rapports.
Vous trouverez ci-dessous les raisons courantes du manque de données de clics.

| Cause | Détection/Analyse | Résolution |
|---|---|---|
| Échec du processus de récupération des données de clic du compte publicitaire. | Il n’existe aucun moyen systématique de détecter ce problème, mais vous remarquerez peut-être qu’une campagne n’affiche aucune information sur les coûts ou les clics, même si le compte publicitaire a dépensé de l’argent. | Contactez votre équipe de compte Adobe.<br><br>Si les données sont manquantes depuis plus de 24 heures, excluez ces dates des prévisions de coûts jusqu’à ce que les données soient récupérées. Votre équipe de compte Adobe peut exclure les dates. |
| Un problème de facturation entre l’annonceur et le réseau publicitaire empêche le compte publicitaire de dépenser. | Il n’existe aucun moyen systématique de détecter ce problème, mais vous remarquerez peut-être qu’une campagne n’affiche aucune information sur les coûts ou les clics. | Si vous savez qu’un compte publicitaire n’a pas pu dépenser en raison d’un problème de facturation, excluez ces dates des prévisions de coûts. Votre équipe de compte Adobe peut exclure les dates. |

+++

+++Les données de performances sont différentes de celles de l’éditeur de réseau publicitaire.
Lorsque le réseau publicitaire envoie des mises à jour aux données précédentes (souvent parce qu’il a attribué la fraude aux clics à certains clics), Search, Social et Commerce ne mettent pas à jour les données à moins qu’il n’y ait plus de 5 % d’incohérence et que l’équipe du compte Adobe ne dépose une demande.

En outre, lorsque vous comparez les données de partage d’impression agrégées sur une période, les données que les rapports Search, Social et Commerce peuvent différer des données rapportées par le réseau publicitaire. Cette différence est due à la manière dont les données sont rapportées par l’API du réseau publicitaire, que Search, Social et Commerce utilisent pour extraire les données. Par exemple, pour les données [!DNL Google Ads] :

* Pour la plupart des mesures de partage d’impression, [!DNL Google Ads] limite l’extrémité inférieure ou supérieure des valeurs signalées pour les valeurs inférieures à 10 % ou supérieures à 90 %. Les données sont de 0,0999 pour &lt; 10 % et de 0,9001 pour > 90 %

* Lorsqu’il existe un mélange de données limitées et non limitées dans la période, Search, Social et Commerce agrège les données de partage d’impression à l’aide des valeurs envoyées dans l’API en l’état, en utilisant 0,0999 pour les lignes avec &lt;10 % et 0,9001 pour les lignes avec >90 %. Cette agrégation peut entraîner un écart par rapport aux données préagrégées [!DNL Google Ads], car [!DNL Google Ads] pouvez utiliser des valeurs de pourcentage réelles, telles que 7 % ou 97 %.
+++

+++Les données de performances des rapports sont différentes de celles des [!DNL Google Analytics].
Les deux systèmes mesurent des données différentes. Vous devez donc vous attendre à voir des données différentes. Par exemple :

* Les publicités Search, Social et Commerce (et Google Ads) effectuent le suivi des clics, tandis que la [!DNL Google Analytics] effectue le suivi des visites par session de navigateur de 30 minutes. Par exemple, si un utilisateur clique sur votre publicité une fois, clique sur le bouton Précédent, puis clique de nouveau sur la publicité, Search, Social et Commerce enregistre deux clics mais enregistre [!DNL Google Analytics] une seule visite.

* [!DNL Google Analytics] affiche toutes les données de trafic, tandis que Search, Social et Commerce (et [!DNL Google Ads]) filtre les clics non valides (comme les clics excessifs et répétés).

* [!DNL Google Analytics] inclut les données sur les clics et le chiffre d’affaires pour tous les clics. Les moteurs de recherche, les réseaux sociaux et Commerce ne peuvent pas suivre les données de clics et de recettes pour les publicités et les mots-clés avec des URL de suivi incorrectes ou manquantes.
+++

## Mesures de conversion

+++Mon rapport n’affiche aucune donnée de conversion.
Le rapport peut ne pas inclure les mesures de conversion pour lesquelles des conversions ont eu lieu.
+++

+++Le chiffre d’affaires est absent des rapports.

**Annonceurs utilisant des balises de conversion Adobe Advertising**

*Causes possibles :*

* Des mots-clés ou des annonces ont été ajoutés sans faire précéder le préfixe de suivi des clics Search, Social et Commerce des modèles de suivi ou des URL de destination, ou le préfixe de suivi est incorrect.

* La balise de suivi des conversions n’est pas correctement implémentée sur toutes les pages web applicables ou a été modifiée.

* Les mesures de conversion suivies par Search, Social et Commerce sont exclues des rapports et ne sont donc pas visibles.

* L&#39;analyseur de revenus pour le client n&#39;a pas été implémenté.

*Solution ou solution de contournement possible :*

1. Vérifiez que les colonnes correctes sont incluses dans les rapports ou les vues de données. Si les colonnes correctes ne sont pas disponibles, vous ou l’équipe chargée de votre compte Adobe devez [mettre les mesures de conversion à la disposition des rapports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Vérifiez que les balises de suivi de conversion correctes sont implémentées sur toutes les pages web applicables. Si nécessaire, demandez à l’équipe chargée de votre compte Adobe de créer une transaction de test pour chaque balise de suivi de conversion applicable et de capturer les détails de la transaction, tels que le `transactionid` et les détails du cookie (tels que le `trackingid`, le `clickid`, etc.).

1. Si l’option [!UICONTROL Auto Upload] est désactivée pour la campagne et que vous avez ajouté des mots-clés ou des annonces, assurez-vous d’avoir généré un modèle de suivi ou une URL de destination qui inclut les options Search, Social et Commerce pour le suivi des clics de redirection. L’équipe chargée de votre compte Adobe peut exécuter un rapport interne pour déterminer si des URL de suivi des clics (modèles de suivi ou URL de destination) sont manquantes ou incorrectes.

   Si nécessaire, générez le tracking en créant un fichier de feuille d’envoi groupé avec les URL correctes, puis publiez le fichier sur le compte approprié à l’aide de l’option **Générer les URL de tracking**.

   L’URL de destination doit commencer par « http://pixel.everesttech.net » ou « https://pixel.everesttech.net ».

1. Si aucune de ces étapes ne résout le problème, [contactez l’assistance clientèle](/help/search-social-commerce/get-help.md).

   Si le client n’a pas été lancé ou vient d’être lancé, l’assistance clientèle vérifie si un analyseur de chiffre d’affaires a été configuré. Si l’analyseur est configuré, il vérifie si Search, Social et Commerce reçoivent des conversions en pixels et résout le problème.

**Annonceurs envoyant des flux de données de conversion**

*Causes possibles :*

* Le fichier de flux n’a pas été livré, il n’a pas été complètement analysé ou le flux contenait des transactions orphelines.

* Les mesures de conversion pertinentes sont exclues des rapports et ne sont donc pas visibles.

>[!NOTE]
>
>Les données n’apparaissent généralement pas dans l’interface utilisateur avant 2 à 4 heures après la réception du flux.

*Solution ou solution de contournement possible :*

1. Vérifiez que les colonnes correctes sont incluses dans les rapports ou les vues de données. Si les colonnes correctes ne sont pas disponibles, vous ou l’équipe chargée de votre compte Adobe devez [mettre les mesures de conversion à la disposition des rapports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Exécutez le [!UICONTROL Portfolio Report]. S’il est vide, exécutez le [!UICONTROL Campaign Report] et [!UICONTROL Search Engine Report] pour voir si le chiffre d’affaires apparaît dans ces rapports. Si c’est le cas, les campagnes peuvent ne pas être affectées au portfolio approprié.

1. Vérifiez que le fichier a été envoyé au serveur de recettes et qu’il a suivi le même format et la même convention de dénomination que les fichiers précédents.

   Si le format ou la convention de dénomination des fichiers a changé, corrigez le fichier et renvoyez-le.

1. Si le fichier a été envoyé, [contactez l’assistance clientèle](/help/search-social-commerce/get-help.md).

   L’assistance clientèle vérifiera si le fichier a été reçu et analysé. Si le fichier a été traité sans erreur, ils recherchent les transactions orphelines.
+++

+++Certains rapports avancés n’incluent pas les données de conversion fournies par un flux d’annonceurs.
Les [!UICONTROL Geo Distribution Report] et [!UICONTROL Domain Referral Report] utilisent des données capturées par le biais du service de suivi des conversions d’Adobe Advertising et ne peuvent être générés que pour les annonceurs qui utilisent le service. Les rapports n’incluent pas les données de conversion qui sont suivies en dehors du système de suivi des conversions d’Adobe Advertising.
+++

+++Les données de chiffre d’affaires sont différentes des données de chiffre d’affaires de l’annonceur.

**Annonceurs utilisant des balises de conversion Adobe Advertising**

*Causes possibles :*

* Search, Social et Commerce ne tiennent pas compte des revenus lorsque le cookie expire ou est supprimé, mais l’annonceur peut le considérer comme un revenu valide.

* Le trafic vers la page de l’annonceur provient d’un signet ou d’une recherche organique plutôt que d’une publicité.

* La balise de suivi des conversions n’est pas correctement implémentée sur toutes les pages web applicables ou a été modifiée.

*Solution ou solution de contournement possible :*

1. Accédez à **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** et générez une [!UICONTROL Transaction Report]. Comparez les transactions que Search, Social et Commerce ont reçues aux données de l’annonceur.

1. Si certaines transactions sont incorrectes ou manquantes, assurez-vous que la balise de suivi de conversion appropriée est implémentée sur toutes les pages web applicables et n’a pas été modifiée, sauf si l’équipe de votre compte Adobe vous a conseillé de le faire. Une balise peut être manquante ou modifiée si le site web a été récemment mis à jour.

   Search, Social et Commerce s’attendent à ce que les URL soient correctement formées (avec des paramètres dans les paires nom-valeur) dans la variable `ef_transaction_properties` et dans l’élément `src` de la balise `img`.

1. Si vous ne parvenez pas à déterminer et à résoudre le problème, [contactez l’assistance clientèle](/help/search-social-commerce/get-help.md).

   L’assistance clientèle tentera d’identifier les transactions manquantes, puis de rechercher les transactions orphelines et les transactions qui ne proviennent pas d’une publicité (« conversions non corrélées »).

**Annonceurs avec des flux de données de conversion utilisant des valeurs `ef_id`**

Consultez les causes possibles et les solutions pour les implémentations de pixels ci-dessus.

**Annonceurs avec des flux de données de conversion utilisant des ID de transaction**

*Causes possibles :*

* Search, Social et Commerce ne tiennent pas compte des revenus lorsque le cookie expire ou est supprimé, mais l’annonceur peut le considérer comme un revenu valide.

* Le trafic vers la page de l’annonceur provient d’un signet ou d’une recherche organique plutôt que d’une publicité.

* Une conversion hors ligne a été signalée avant qu’une transaction en ligne ne se produise avec le même ID de transaction. La transaction en ligne doit avoir lieu en premier.

*Solution ou solution de contournement possible :*

1. Accédez à **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** et générez une [!UICONTROL Transaction Report]. Comparez les transactions reçues par Search, Social et Commerce aux données de flux de l’annonceur.

1. Si une transaction dans le fichier de flux est manquante dans le rapport, vérifiez si une transaction en ligne avec le même ID de transaction (suivi via le pixel) s’est produite avant la conversion hors ligne.

1. Si vous ne parvenez pas à déterminer et à résoudre le problème, [contactez l’assistance clientèle](/help/search-social-commerce/get-help.md).

   L’assistance clientèle vérifiera les erreurs d’analyse des données et les [transactions orphelines](/help/search-social-commerce/glossary.md#o-p).

**Annonceurs avec d’autres types de flux de données de conversion**

*Causes possibles :*

* Search, Social et Commerce ne tiennent pas compte des revenus lorsque le cookie expire ou est supprimé, mais l’annonceur peut le considérer comme un revenu valide.

* Le trafic vers la page de l’annonceur provient d’un signet ou d’une recherche organique plutôt que d’une publicité.

* Il existe des [transactions orphelines](/help/search-social-commerce/glossary.md#o-p), de sorte que Search, Social et Commerce ne comptabilise pas tous les revenus qu’il devrait générer.

* L’annonceur a validé un rapport Search, Social et Commerce par rapport à un ensemble de données différent de celui qu’il a envoyé dans le flux.

* Les ID de transaction (valeurs `ev_transid`) n’ont pas été envoyés, ne sont pas uniques ou sont incorrects.

* Le fichier de flux contient des identifiants de suivi en double.

* Des erreurs se sont produites lors de l&#39;analyse du fichier.

* La logique de déduplication de l’annonceur diffère de la logique Search, Social et Commerce.

*Solution ou solution de contournement possible :*

1. Accédez à **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** et générez une [!UICONTROL Transaction Report]. Comparez les transactions que Search, Social et Commerce ont reçues aux données de l’annonceur.

1. Si certaines transactions sont incorrectes ou manquantes, assurez-vous a) que le fichier de flux contient tous les ID de transaction requis et aucun ID de suivi en double et b) que les ID de transaction sont uniques et corrects.

1. Si vous ne parvenez pas à déterminer et à résoudre le problème, [contactez l’assistance clientèle](/help/search-social-commerce/get-help.md).

   L’assistance clientèle vérifiera les erreurs d’analyse des données et les transactions orphelines.
+++

+++Les données de chiffre d’affaires sont différentes des données d’Adobe Analytics
Voir [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html?lang=fr](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html?lang=fr).<!-- change link URL to relative link -->
+++

## Rapports spécifiques

+++La [!UICONTROL Portfolio Report] doit-elle afficher les mêmes chiffres que la vue [!UICONTROL Portfolios] ?
La vue [!UICONTROL Portfolio Report] et la vue [!UICONTROL Portfolios] affichent les mêmes données lorsque tous les filtres de la vue, les paramètres du rapport et les colonnes de données de la vue et du rapport sont identiques. Par exemple, si la vue [!UICONTROL Portfolios] affiche des portfolios « [!UICONTROL All but inactive] » pour la période « [!UICONTROL Last 7 days] » et que seules les colonnes de données par défaut sont affichées, une [!UICONTROL Portfolio Report] utilisant les paramètres par défaut affiche des données identiques. Si vous modifiez l’un des paramètres de rapport ou utilisez des filtres différents dans la vue [!UICONTROL Portfolios], les valeurs des données peuvent être différentes.
+++

+++Les données de mon [!UICONTROL Portfolio Report] ne correspondent pas à celles de mon [!UICONTROL Search Engine Report] ou de mon [!UICONTROL Search Engine Account Report].
La [!UICONTROL Portfolio Report] affiche les données des campagnes affectées aux portfolios spécifiés uniquement, mais les [!UICONTROL Search Engine Report] et [!UICONTROL Search Engine Account Report] peuvent également inclure des données pour les campagnes qui ne sont pas affectées à un portfolio.
+++

+++En quoi le [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] diffère-t-il du [!UICONTROL Model Accuracy Report] au niveau du portefeuille ?
(Gestionnaire de compte d’Agence, gestionnaire de compte Adobe et utilisateurs administrateurs uniquement) Le [!UICONTROL Forecast Accuracy Report] disponible dans [!UICONTROL Reports] > [!UICONTROL Model Accuracy] fournit les mêmes données que le [!UICONTROL Model Accuracy Report] au niveau du portefeuille, à la différence que vous pouvez l’exécuter sur plusieurs portefeuilles et que vous pouvez modifier la règle d’attribution. Vous pouvez également exécuter et planifier le rapport à l&#39;aide de paramètres personnalisés et l&#39;utiliser pour créer des flux de feuilles de calcul. En outre, le [!UICONTROL Forecast Accuracy Report] est plus précis que le rapport hérité au niveau du portefeuille, car il évalue l’exactitude des revenus à l’aide des objectifs historiques du portefeuille plutôt que de l’objectif actuel, et il représente plus précisément les données pour le fuseau horaire applicable.
+++

+++Les données au niveau des annonces ne sont pas disponibles pour [!DNL Google Ads] annonce de recherche dynamique (DSA), les campagnes Performance max, Achats intelligents et [!DNL YouTube].
Les réseaux publicitaires ne fournissent pas l’identifiant nécessaire pour attribuer le chiffre d’affaires à une publicité individuelle pour ces campagnes. Par conséquent, les données de performances au niveau des annonces ne sont pas disponibles pour ces types de campagnes dans la vue [!UICONTROL Ads] ou dans la [!UICONTROL Ad Variation Report]. Attendez-vous à des incohérences entre le nombre total de données au niveau des annonces pour une campagne et le nombre total de données pour la campagne.
+++

+++Dans la [!UICONTROL Transaction Report], comment savoir quelle mesure de conversion provient d’un flux de données ou est suivie par le pixel de suivi d’Adobe Advertising ?
Dans un rapport de transaction, vous pouvez déterminer si une mesure de conversion incluse a été suivie par le pixel de suivi Adobe Advertising si vous incluez la colonne personnalisée « [!UICONTROL Tracking URL] ». Les URL de tracking avec le pixel de tracking Adobe Advertising commencent par « `http://pixel.everesttech.net` ».
+++

+++Les données de mon [!UICONTROL Transaction Report] ne correspondent pas à celles de mon [!UICONTROL Keyword Report].
Lorsque vous générez les deux rapports par portfolio, les données sont différentes si vous générez le [!UICONTROL Keyword Report] à l’aide de données historiques (c’est-à-dire en fonction de la configuration du portfolio pendant les dates spécifiées) plutôt qu’en utilisant des données pour les campagnes actuelles. Lorsque vous générez le [!UICONTROL Transaction Report] par portfolio, il inclut les données des campagnes actives dans le portfolio.
+++

## Flux de feuilles de calcul

+++La sortie du rapport comprend un mélange de périodes.
Vous pouvez voir différentes périodes si le flux agrège les données à l’aide d’un niveau d’agrégation de données autre que « [!UICONTROL Daily] ».

Pour résoudre ce problème, mettez à jour le flux de la feuille de calcul pour inclure les données agrégées quotidiennement. Cette tâche comprend la mise à jour du modèle de rapport, la génération d’un rapport à l’aide du modèle, la création d’un modèle de [!DNL Microsoft Excel] personnalisé à l’aide du rapport, puis la mise à jour des paramètres de flux pour inclure le nouveau modèle Excel. Pour plus d&#39;informations, voir « [Modifier les paramètres de flux de rapports de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md) ».
+++

+++Un flux de feuille de calcul génère une erreur interne.
Cette erreur peut se produire si vous modifiez les colonnes du modèle de rapport mais que vous ne mettez pas à jour le modèle de [!DNL Microsoft Excel] en conséquence.

Pour résoudre ce problème, mettez à jour le flux de la feuille de calcul pour inclure les nouvelles colonnes. Cette tâche comprend la mise à jour du modèle de rapport, la génération d’un rapport à l’aide du modèle, la création d’un modèle de [!DNL Excel] personnalisé à l’aide du rapport, puis la mise à jour des paramètres de flux pour inclure le nouveau modèle Excel. Pour plus d&#39;informations, voir « [Modifier les paramètres de flux de rapports de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md) ».
+++

+++Lorsque j’essaie d’ouvrir un flux de feuille de calcul dans [!DNL Excel], [!DNL Excel] signale une erreur de « contenu illisible » et les données sont supprimées du contenu récupéré.
Lorsque le modèle de [!DNL Microsoft Excel] ne trie pas les données par date de début dans l’ordre croissant, le flux de la feuille de calcul peut inclure des lignes vides. En particulier, [!DNL Excel] signale l’erreur « Excel a trouvé du contenu illisible dans « &lt;*nom du rapport*>.xlsx ». Voulez-vous récupérer le contenu du classeur ? Si la source de ce classeur est fiable, cliquez sur Oui. » Si vous cliquez sur « Oui », le message suivant s’affiche : « Enregistrements supprimés : informations de cellule de la partie /xl/worksheets/sheet1.xml » et le flux de la feuille de calcul inclut des lignes vides.

Pour résoudre ce problème, modifiez le modèle de [!DNL Excel] associé au flux afin de trier les données par [!DNL Start date in Ascending (Oldest to Newest) order], puis chargez le modèle mis à jour via les paramètres de flux de la feuille de calcul. Pour plus d&#39;informations, voir « [Modifier les flux de rapports de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md) ».
+++
