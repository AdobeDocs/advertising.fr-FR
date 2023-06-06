---
title: Questions fréquentes sur les rapports
description: Découvrez les réponses aux questions courantes sur les rapports de performances, notamment la résolution des problèmes liés aux données.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '3917'
ht-degree: 0%

---

# Questions fréquentes sur les rapports

## Questions générales

+++Que se passe-t-il si la période du rapport commence avant que les données du rapport ne soient disponibles ?
Le rapport est généré, mais il ne comprend que les données des dates pour lesquelles des données sont disponibles. Pour plus d’informations sur le moment où les données sont disponibles pour chaque type de rapport, voir &quot;[Données utilisées pour les rapports](data-used-for-reports.md).&quot;
+++

+++Quelle est la différence entre les rapports Date de clic et Date de transaction ?
Lorsque vous signalez des conversions par date de transaction, les données incluent les transactions dont la date de transaction s’est produite au cours de la période spécifiée. Cette option est le paramètre par défaut des rapports de base et avancés. Elle indique également le montant des recettes générées au cours d’une période donnée.

Lorsque vous signalez des conversions par date de clic, les données incluent les transactions résultant d’un clic qui s’est produit au cours de la période spécifiée. Lorsqu’un portefeuille enregistre des retards significatifs entre les clics et les transactions, ce type de rapport indique les recettes historiques par clic pour le portefeuille, ce qui vous donne une idée des comportements de recettes à attendre au fil du temps.

![Comparaison de la date de clic par rapport à la date de transaction](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Comparaison de la date de clic par rapport à la date de transaction")
+++

+++Que se passe-t-il si je modifie l’intervalle de recherche en amont des clics ou l’intervalle de recherche en amont des impressions ?
(Publicitaires avec service de suivi de conversion Advertising basé sur les pixels uniquement) Les données relatives aux événements résultant du clic initial sont collectées pour une période plus longue ou plus courte.

d’un annonceur ; [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j) déterminer le nombre de jours après un clic payant ou une impression d’affichage (respectivement) au cours de laquelle l’événement peut être attribué à une conversion ; La modification d’une valeur sur une période plus longue ou plus courte peut s’avérer importante pour les annonceurs qui disposent d’un clic sur les recettes particulièrement court ou long ou qui affichent des périodes d’impression sur les recettes.

**Bonne pratique :** Assurez-vous que les intervalles de recherche en amont sont plus longs que les heures de clic vers le chiffre d’affaires et d’affichage d’impression vers le chiffre d’affaires pour la plupart de vos mots-clés ou publicités. Lorsqu’elles sont plus courtes, certaines conversions ne sont pas associées au clic ou à l’impression initial.
+++

+++Comment savoir quelles conversions ont résulté d’une [!DNL Google Ads] extension de publicité ou liste de produits ?
Vous pouvez voir les conversions qui ont résulté d’un clic sur une [!DNL Google Ads] extension de publicité (plutôt que sur la publicité elle-même) ou sur une liste de produits en générant une [!UICONTROL Transaction Report]. Le [!UICONTROL Link Type] La valeur de colonne indique le type et le titre d’un lien sur lequel l’utilisateur a cliqué :

* Les listes de produits sont répertoriées comme `pla:<product ID>`, par exemple `pla:8525822`.

* Les liens de site sont répertoriés comme `sl:<Sitelink text>`, par exemple `sl:See Current Offers`.

   Vous pouvez également identifier un lien de site si vous incluez la variable [!UICONTROL Tracking URL] dans le rapport. Le [!UICONTROL Tracking URL] pour un lien de site comprend l’attribut `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Conversions depuis [!DNL Google Ads] les emplacements et les extensions de téléphone sont inclus dans les données des publicités qu’ils accompagnent. Ils ne sont pas signalés séparément.

+++

+++&quot;[!UICONTROL Keyword]&quot; dans mon rapport, la colonne comprend une valeur &quot;(contenu du groupe) &lt;*nom du groupe publicitaire*>.&quot;
Lorsque la ligne comprend des données pour des campagnes de recherche activées sur le contenu, des campagnes d’affichage ou des campagnes sur les réseaux sociaux (qui n’incluent pas de mots-clés), la variable [!UICONTROL Keyword] affiche le nom du groupe d’annonces concerné à la place.
+++

+++En raison des changements saisonniers ou du marché, mes rapports présentent des données atypiques. Cela aura-t-il une incidence sur les offres une fois les conditions modifiées ?
La fonctionnalité d’optimisation crée quotidiennement ses modèles de recettes pour chaque unité d’offre afin de s’assurer qu’elle identifie les tendances et qu’elle y répond immédiatement, et les modèles intègrent des données historiques à long terme pour aider à prédire les performances saisonnières. Le paramètre de demi-vie du modèle de revenus du portefeuille<!-- add link to glossary? --> détermine également le degré de pondération des données sur les recettes récentes. La bonne pratique consiste à réduire la demi-vie pendant une période de performance atypique, mais à l’augmenter après l’ajustement du modèle de revenu. Si vous avez des questions sur l’ajustement de la demi-vie nécessaire, contactez votre équipe de compte d’Adobe.

Si vous ne souhaitez pas que les données de la période affectent les offres futures, vous pouvez choisir d’exclure ces dates du modèle. Contactez votre équipe de compte d’Adobe pour exclure les dates.
+++

+++Puis-je créer un rapport sur une mesure de propriété spécifique, telle que [!UICONTROL Device] ou [!UICONTROL Objective Name]?
Pour les rapports d’entité de campagne ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], et [!UICONTROL Product Group Report]), les données de mesures sont agrégées dynamiquement par les colonnes de propriétés que vous incluez dans le rapport. Vous pouvez éventuellement supprimer la colonne clé du rapport et inclure uniquement les colonnes de propriétés pour lesquelles vous souhaitez agréger les données.

Par exemple, si vous générez une [!UICONTROL Keyword Report] qui inclut la variable [!UICONTROL Ad Group] et  Colonnes d’appareil, puis, par défaut, le rapport agrège les mesures pour chaque mot-clé par groupe publicitaire et type d’appareil. Toutefois, si vous supprimez la variable [!UICONTROL Keyword] avant de générer le rapport, le rapport génère dynamiquement des mesures pour les groupes d’annonces spécifiés par type d’appareil.

>[!NOTE]
>
>Vous ne pouvez pas utiliser cette fonction pour agréger les données par classification d’étiquettes. Toutes les colonnes de classification des étiquettes du rapport sont omises. Utilisez plutôt la variable [Rapport de classification des étiquettes](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Problèmes généraux liés aux données

+++Les rapports générés à l’aide de différentes règles d’attribution affichent des totaux différents.
Si vous générez un rapport plusieurs fois en utilisant les mêmes paramètres de rapport, mais avec des règles d’attribution différentes, les données peuvent différer pour l’une des raisons suivantes :

* Les données de clic basées sur une date peuvent se trouver en dehors de la période spécifiée.

   Si vous utilisez le paramètre de rapport &quot;[!UICONTROL Conversions based on click date],&quot; la plage de dates spécifiée s’applique à la date du clic au lieu de la date de la transaction. Si le rapport utilise également la règle d’attribution &quot;Premier événement&quot; ou &quot;Dernier événement&quot;, alors le premier ou le dernier événement ayant entraîné la conversion peut se trouver en dehors de la période spécifiée. Supposons, par exemple, qu’un utilisateur ait cliqué sur Mot-clé_1 le 30 avril, sur Mot-clé_2 le 20 mai et ait effectué une conversion le 21 mai. Si le rapport utilise le[!UICONTROL First Event]&quot;règle d’attribution et plage de dates du 1er au 21 mai, puis le premier événement (un clic sur Mot-clé_1 le 30 avril) n’est pas inclus dans le rapport. Si vous exécutez le rapport avec la même période, mais en utilisant le[!UICONTROL Last Event]&quot;règle d’attribution, la conversion est incluse dans le rapport, car le dernier clic s’est produit au cours de la période spécifiée.

* La sélection de filtre de portefeuille exclut certains des événements ayant conduit à la conversion.

   Si vous créez des rapports sur un sous-ensemble de portefeuilles, il se peut que vous n’incluiez pas les campagnes qui incluaient l’événement auquel la conversion a été attribuée sous l’une des règles d’attribution. Supposons, par exemple, qu’un utilisateur clique sur Mot-clé_1 à partir de Portfolio_1, clique sur Mot-clé_2 à partir de Portfolio_2, puis effectue une conversion. Si le rapport utilise le[!UICONTROL First Event]&quot;règle d’attribution, alors Portfolio_1 doit être inclus pour que la conversion soit incluse dans le rapport. Cependant, si le rapport utilise la règle d’attribution &quot;Dernier événement&quot;, alors Portfolio_2 doit être inclus.

>[!TIP]
>
>Si vous souhaitez comparer des totaux de conversion sous différentes règles d’attribution, exécutez des rapports à l’aide du paramètre de rapport &quot;[!UICONTROL Conversions based on transaction date]&quot; et sélectionnez tous les réseaux publicitaires ou tous les portefeuilles. Si vous ne définissez aucun autre filtre, les totaux de conversion doivent correspondre.

+++

+++Les champs de données individuels sont incorrects, bien que les totaux soient corrects.
Cette situation peut se produire lorsque les formats de mesure utilisent des entiers :

* Si vous créez un [mesure personnalisée](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) avec le format *Nombre sans décimales* (qui affiche les données sous forme d’entiers) et les inclut dans un affichage ou un rapport qui utilise une règle d’attribution de conversion pondérée ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]ou [!UICONTROL Even Distribution]), la sortie s’affiche sous forme d’entiers, et non de décimales. Dans ce cas, des champs de données individuels peuvent être incorrects, bien que les totaux soient corrects. Par exemple, si une commande est divisée uniformément entre trois événements, une commande (au lieu de 0,33) est attribuée à chacun des trois événements. Pour résoudre le problème, [modification du format de mesure](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) to *Nombre à 2 points décimaux*.

* De même, si une mesure de recettes est envoyée sous forme d’entier, le même problème se produit. (Le format des recettes est contrôlé par la balise de conversion qui envoie les données.) Pour résoudre le problème, [création d’une mesure personnalisée](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) composé uniquement de la mesure des recettes et du format *Nombre à 2 points décimaux*et l’inclure dans les vues et les rapports plutôt que dans la mesure d’origine.
+++

+++Lorsque des données de clics ou de recettes sont manquantes, comment puis-je les empêcher d’affecter les futures offres ?
Des problèmes de clic sur les données se produisent lorsque Search, Social et Commerce n’est pas synchronisé avec le réseau publicitaire. Contactez votre équipe de compte d’Adobe pour synchroniser manuellement le compte. Si des données de clic sont manquantes pour une journée entière, demandez à votre équipe de compte d’Adobe d’exclure cette journée des modèles de coûts.

Des problèmes de données sur les recettes peuvent se produire en raison d’un problème de suivi ou de fichier de flux. Contactez votre équipe de compte d’Adobe pour enquêter sur le problème. Si des données sur les recettes sont manquantes pour une journée entière, demandez à votre équipe de compte d’Adobe d’exclure cette journée des modèles de recettes.
+++

+++Les données monétaires sont affichées dans un format incorrect.
Par défaut, toutes les données monétaires des rapports sont présentées au format en dollars (1 000,00, par exemple). Pour afficher la valeur dans le bon format de devise (mais sans aucun symbole de devise dans les formats CSV et TSV), ajoutez le &quot;[!UICONTROL Currency]&quot; au rapport. Si le rapport inclut des données pour des comptes avec des devises différentes, alors tout[!UICONTROL Total]&quot;les valeurs monétaires sont simplement la somme de tous les nombres de la colonne, quelle que soit la devise.
+++

+++Pourquoi vois-je des valeurs décimales pour une propriété de transaction qui doit être un nombre naturel (1, 2, etc.) ?
Vous pouvez voir des valeurs décimales dans les cas suivants :

* Si vous avez exécuté le rapport à l’aide d’un paramètre de règle d’attribution de conversion autre que [!UICONTROL Last Event] ou [!UICONTROL First Event], les recettes peuvent alors être fractionnées entre plusieurs événements du chemin de conversion.

* Dans le [!UICONTROL Transaction Report], si plusieurs [enchères](/help/search-social-commerce/glossary.md#a-b) si différents types de correspondance possèdent le même ID de transaction, les recettes de l’ID de suivi sont fractionnées en fonction du nombre de clics effectués à la date de clic spécifiée.
+++

## Mesures de performances standard

+++Les données de clic sont absentes des rapports.
Les raisons suivantes expliquent souvent l’absence de données de clic.

| Cause | Détection/Analyse | Résolution |
|---|---|---|
| Le processus qui récupère les données de clic du compte publicitaire a échoué. | Il n’existe aucun moyen systématique de détecter ce problème, mais vous pouvez remarquer qu’une campagne n’indique aucun coût ou aucune information sur les clics, même si le compte publicitaire a dépensé de l’argent. | Contactez le service clientèle à l’adresse &lt;*votre compte utilisateur Search, Social &amp; Commerce*>@support\.efrontier\.com.<!-- Escaped periods and using HTML code for angle brackets --><br><br>Si les données sont manquantes pendant plus de 24 heures, excluez ces dates des prévisions de coût jusqu&#39;à ce que les données soient récupérées. Votre équipe de compte d’Adobe peut exclure les dates. |
| Un problème de facturation entre l’annonceur et le réseau publicitaire empêche le compte publicitaire de dépenser. | Il n’existe aucun moyen systématique de détecter ce problème, mais vous pouvez remarquer qu’une campagne n’indique aucun coût ou aucune information sur les clics. | Si vous savez qu’un compte publicitaire n’a pas pu être utilisé en raison d’un problème de facturation, excluez ces dates des prévisions de coût. Votre équipe de compte d’Adobe peut exclure les dates. |
+++

+++Les données de performances diffèrent des données de l’éditeur de réseau publicitaire.
Lorsque le réseau publicitaire envoie des mises à jour aux données précédentes (souvent parce qu’il a attribué des clics frauduleux à certains clics), Search, Social et Commerce ne met pas à jour les données, sauf s’il existe une incohérence de plus de 5 % et que l’équipe du compte d’Adobe envoie une demande.

En outre, lorsque vous comparez les données de partage d’impression agrégées sur une période, les données des rapports Search, Social et Commerce peuvent différer des données des rapports du réseau publicitaire. Cette différence est due à la manière dont les données sont signalées par l’API du réseau publicitaire, que Search, Social et Commerce utilise pour extraire des données. Par exemple, pour [!DNL Google Ads] data:

* Pour la plupart des mesures de partage d’impression, [!DNL Google Ads] limite la limite inférieure ou supérieure des valeurs signalées pour les valeurs inférieures à 10 % ou supérieures à 90 %. Les données sont signalées comme étant de 0,0999 pour &lt;10 % et de 0,9001 pour >90 %

* Lorsqu’il existe un mélange de données plafonnées et non plafonnées au cours de la période, Search, Social et Commerce agrège les données de partage d’impression à l’aide des valeurs envoyées en l’état dans l’API, en utilisant 0,0999 pour les lignes comportant &lt;10 % et 0,9001 pour les lignes comportant plus de 90 %. Cette agrégation peut générer une variance de la variable [!DNL Google Ads] données pré-agrégées, car [!DNL Google Ads] peuvent utiliser des valeurs en pourcentage réel, telles que 7 ou 97 %.
+++

+++Les données de performance dans les rapports diffèrent des données de [!DNL Google Analytics].
Les deux systèmes mesurent des données différentes, vous devriez donc vous attendre à voir des données différentes. Par exemple :

* Rechercher, Social et Commerce (et publicités Google) effectuent le suivi des clics, tandis que [!DNL Google Analytics] effectue le suivi des visites par session de navigateur de 30 minutes. Par exemple, si un utilisateur clique une fois sur votre publicité, clique sur le bouton Précédent, puis de nouveau sur la publicité, Search, Social et Commerce enregistre deux clics, mais [!DNL Google Analytics] enregistre une visite.

* [!DNL Google Analytics] affiche toutes les données de trafic, tandis que Search, Social et Commerce (et [!DNL Google Ads]) filtre les clics non valides (tels que les clics excessifs et répétés).

* [!DNL Google Analytics] inclut les données sur les clics et les recettes pour tous les clics. Search, Social et Commerce ne peut pas effectuer le suivi des données de clics et de recettes pour les publicités et les mots-clés dont les URL de suivi sont incorrectes ou manquantes.
+++

## Mesures de conversion

+++Mon rapport ne montre aucune donnée de conversion.
Le rapport peut ne pas inclure de mesures de conversion pour lesquelles des conversions ont eu lieu.
+++

+++Recettes manquantes dans les rapports.

### Annonceurs utilisant des balises de conversion Adobe Advertising

#### Causes possibles

* Des mots-clés ou des publicités ont été ajoutés sans préfixe au préfixe de suivi des clics Search, Social, &amp; Commerce dans les modèles de suivi ou les URL de destination, ou le préfixe de suivi est incorrect.

* La balise de suivi de conversion n’est pas correctement implémentée sur toutes les pages web applicables ou a été modifiée.

* Les propriétés de transaction suivies par Search, Social et Commerce sont exclues des rapports et ne sont donc pas visibles.

* L’analyseur des recettes du client n’a pas été mis en oeuvre.

#### Solution ou solution possible

1. Vérifiez que les colonnes correctes sont incluses dans les rapports ou les vues de données. Si les colonnes correctes ne sont pas disponibles à ajouter, vous ou votre équipe de compte d’Adobe devez [rendre les propriétés de transaction disponibles pour les rapports](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. Vérifiez que les balises de suivi de conversion correctes sont implémentées sur toutes les pages web applicables. Si nécessaire, demandez à votre équipe de compte d’Adobe de créer une transaction de test pour chaque balise de suivi de conversion applicable et de capturer les détails de la transaction, tels que le `transactionid` et les détails du cookie (tels que `trackingid`, `clickid`, etc.).

1. Si la variable [!UICONTROL Auto Upload] est désactivée pour la campagne et vous avez ajouté des mots-clés ou des publicités, puis assurez-vous d’avoir généré un modèle de suivi ou une URL de destination qui inclut le suivi des redirections de clics Search, Social et Commerce pour chacune d’elles. Votre équipe de compte d’Adobe peut exécuter un rapport interne pour déterminer si des URL de suivi des clics (modèles de suivi ou URL de destination) sont manquantes ou incorrectes.

   Si nécessaire, générez le suivi en créant un fichier de feuille d’envoi groupé avec les URL appropriées, puis publiez le fichier sur le compte approprié à l’aide de la fonction **Génération des URL de suivi** .

   L’URL de destination doit commencer par &quot;http://pixel.everesttech.net&quot; ou &quot;https://pixel.everesttech.net&quot;.

1. Si aucune de ces étapes ne résout le problème, alors [Contacter l’assistance clientèle](/help/search-social-commerce/get-help.md).

   Si le client n’a pas été lancé ou est récemment lancé, l’assistance clientèle vérifie si un analyseur des recettes a été configuré. Si l’analyseur est configuré, il vérifie si Search, Social et Commerce reçoit des conversions de pixels et résout le problème.

### Annonceurs envoyant des flux de données de conversion

#### Causes possibles

* Le fichier de flux n’a pas été livré, il n’a pas été complètement analysé ou il contenait des transactions orphelines.

* Les propriétés de transaction appropriées sont exclues des rapports et ne sont donc pas visibles.

>[!NOTE]
>
>Les données n’apparaissent généralement dans l’interface utilisateur que 2 à 4 heures après la réception du flux.

#### Solution ou solution possible

1. Vérifiez que les colonnes correctes sont incluses dans les rapports ou les vues de données. Si les colonnes correctes ne sont pas disponibles à ajouter, vous ou votre équipe de compte d’Adobe devez [rendre les propriétés de transaction disponibles pour les rapports](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. Exécutez la variable [!UICONTROL Portfolio Report]. S’il est vide, exécutez le [!UICONTROL Campaign Report] et [!UICONTROL Search Engine Report] pour voir si les recettes apparaissent dans ces rapports. Si tel est le cas, les campagnes peuvent ne pas être affectées au portfolio approprié.

1. Vérifiez que le fichier a bien été envoyé au serveur de recettes et qu’il respecte le même format et la même convention d’appellation que les fichiers précédents.

   Si le format ou la convention d’affectation des noms de fichier a changé, corrigez le fichier et renvoyez-le.

1. Si le fichier a été envoyé, [Contacter l’assistance clientèle](/help/search-social-commerce/get-help.md).

   L’assistance clientèle vérifie si le fichier a été reçu et analysé. Si le fichier a été traité sans erreur, il vérifie les transactions orphelines.
+++

+++Certains rapports avancés n’incluent pas les données de conversion fournies par un flux publicitaire.
Le [!UICONTROL Geo Distribution Report] et [!UICONTROL Domain Referral Report] utilisez les données capturées par le biais du service de suivi de conversion Adobe Advertising et ne peuvent être générées que pour les annonceurs disposant du service. Les rapports n’incluent pas les données de conversion suivies en dehors du système de suivi de conversion Adobe Advertising.
+++

+++Les données sur les recettes diffèrent des données sur les recettes propres à l’annonceur.

### Annonceurs utilisant des balises de conversion Adobe Advertising

#### Causes possibles

* Search, Social et Commerce ignorent les recettes lorsque le cookie expire ou est supprimé, mais l’annonceur peut considérer qu’il s’agit d’une recette valide.

* Le trafic vers la page de l’annonceur provient d’un signet ou d’une recherche organique plutôt que d’une publicité.

* La balise de suivi de conversion n’est pas correctement implémentée sur toutes les pages web applicables ou a été modifiée.

#### Solution ou solution possible

1. Accédez à **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** et générer un [!UICONTROL Transaction Report]. Comparez les transactions reçues par Search, Social et Commerce aux données de l’annonceur.

1. Si certaines transactions sont incorrectes ou manquantes, assurez-vous que la balise de suivi de conversion appropriée est implémentée sur toutes les pages web applicables et n’a pas été modifiée, sauf si votre équipe de compte d’Adobe vous a conseillé de le faire. Une balise peut être manquante ou modifiée si le site web a été récemment mis à jour.

   Search, Social et Commerce s’attend à des URL bien formées (avec des paramètres dans des paires nom-valeur) au sein de la variable `ef_transaction_properties` et dans la variable `src` de l’élément `img` balise .

1. Si vous ne pouvez pas déterminer et résoudre le problème, alors [Contacter l’assistance clientèle](/help/search-social-commerce/get-help.md).

   L’assistance clientèle tentera d’identifier les transactions manquantes, puis de rechercher les transactions et transactions orphelines qui ne sont pas venues d’une publicité (&quot;conversions sans corrélation&quot;).

### Publicitaires avec des flux de données de conversion utilisant `ef_id` values

Voir les causes possibles et les solutions pour les implémentations de pixels ci-dessus.

### Publicitaires avec des flux de données de conversion utilisant des ID de transaction

#### Causes possibles

* Search, Social et Commerce ignorent les recettes lorsque le cookie expire ou est supprimé, mais l’annonceur peut les considérer comme des recettes valides.

* Le trafic vers la page de l’annonceur provient d’un signet ou d’une recherche organique plutôt que d’une publicité.

* Une conversion hors ligne a été signalée avant qu’une transaction en ligne ne se produise avec le même ID de transaction. La transaction en ligne doit avoir lieu en premier.

#### Solution ou solution possible

1. Accédez à **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** et générer un [!UICONTROL Transaction Report]. Comparez les transactions que Search, Social et Commerce a reçues avec les données de flux de l’annonceur.

1. Si une transaction dans le fichier de flux est manquante dans le rapport, vérifiez si une transaction en ligne avec le même ID de transaction (suivi via le pixel) s’est produite avant la conversion hors ligne.

1. Si vous ne pouvez pas déterminer et résoudre le problème, alors [Contacter l’assistance clientèle](/help/search-social-commerce/get-help.md).

   L’assistance clientèle recherche les erreurs d’analyse des données et [transactions orphelines](/help/search-social-commerce/glossary.md#o-p).

### Annonceurs avec d’autres types de flux de données de conversion

#### Causes possibles

* Search, Social et Commerce ignorent les recettes lorsque le cookie expire ou est supprimé, mais l’annonceur peut considérer qu’il s’agit d’une recette valide.

* Le trafic vers la page de l’annonceur provient d’un signet ou d’une recherche organique plutôt que d’une publicité.

* Il y a [transactions orphelines](/help/search-social-commerce/glossary.md#o-p), ainsi Search, Social et Commerce ne comptabilise pas toutes les recettes qu’il doit générer.

* L’annonceur a validé un rapport de recherche, de réseaux sociaux et de commerce en fonction d’un ensemble de données différent de celui qu’il a envoyé dans le flux.

* Les identifiants de transaction (`ev_transid` n’ont pas été envoyées, ne sont pas uniques ou sont incorrectes.

* Le fichier de flux contient des identifiants de suivi en double.

* Des erreurs se produisaient lors de l’analyse du fichier.

* La logique de déduplication de l’annonceur diffère de la logique de recherche, de réseaux sociaux et de commerce.

#### Solution ou solution possible

1. Accédez à **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** et générer un [!UICONTROL Transaction Report]. Comparez les transactions reçues par Search, Social et Commerce aux données de l’annonceur.

1. Si certaines transactions sont incorrectes ou manquantes, assurez-vous que a) le fichier de flux contient tous les identifiants de transaction requis et qu’aucun ID de suivi en double, et b) les identifiants de transaction sont uniques et corrects.

1. Si vous ne pouvez pas déterminer et résoudre le problème, alors [Contacter l’assistance clientèle](/help/search-social-commerce/get-help.md).

   L’assistance clientèle recherche les erreurs d’analyse des données et les transactions orphelines.
+++

+++Les données sur les recettes diffèrent des données dans Adobe Analytics Voir [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Rapports spécifiques

+++Le paramètre [!UICONTROL Portfolio Report] afficher les mêmes chiffres que la variable [!UICONTROL Portfolios] vue ?
Le [!UICONTROL Portfolio Report] et le [!UICONTROL Portfolios] afficher les mêmes données lorsque tous les filtres pour la vue, les paramètres du rapport et les colonnes de données pour la vue et le rapport sont identiques. Par exemple, si la variable [!UICONTROL Portfolios] La vue affiche les portefeuilles qui sont &quot;[!UICONTROL All but inactive]&quot; pour la période &quot;[!UICONTROL Last 7 days]&quot; et uniquement avec les colonnes de données par défaut affichées, puis une [!UICONTROL Portfolio Report] l’utilisation des paramètres par défaut affiche des données identiques. Si vous modifiez l’un des paramètres du rapport ou utilisez différents filtres dans la variable [!UICONTROL Portfolios] , les valeurs des données peuvent être différentes.
+++

+++Les données de mon [!UICONTROL Portfolio Report] ne correspond pas aux données de mon [!UICONTROL Search Engine Report] ou [!UICONTROL Search Engine Account Report].
Le [!UICONTROL Portfolio Report] affiche les données des seules campagnes affectées aux portefeuilles spécifiés, mais la variable [!UICONTROL Search Engine Report] et [!UICONTROL Search Engine Account Report] peuvent également inclure des données pour les campagnes qui ne sont pas affectées à un portfolio.
+++

+++Comment est la variable [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] différent du niveau du portfolio [!UICONTROL Model Accuracy Report]?
(Uniquement le gestionnaire de compte de l’agence, le gestionnaire de compte d’Adobe et les utilisateurs administrateurs) La variable [!UICONTROL Forecast Accuracy Report] disponible à partir de [!UICONTROL Reports] > [!UICONTROL Model Accuracy] fournit les mêmes données qu’au niveau du portfolio ; [!UICONTROL Model Accuracy Report] mais vous pouvez l’exécuter sur plusieurs portefeuilles et modifier la règle d’attribution. Vous pouvez également exécuter et planifier le rapport à l’aide de paramètres personnalisés. Vous pouvez également l’utiliser pour créer des flux de feuille de calcul. En outre, la variable [!UICONTROL Forecast Accuracy Report] est plus précis que le rapport existant au niveau du portfolio, car il évalue la précision des recettes à l’aide des objectifs historiques du portfolio plutôt que de l’objectif actuel et représente plus précisément les données du fuseau horaire applicable.
+++

+++Les données au niveau de la publicité ne sont pas disponibles pour [!DNL Google Ads] publicité de recherche dynamique (DSA), niveau de performance maximal, achats intelligents et [!DNL YouTube] campagnes.
Les réseaux publicitaires ne fournissent pas l’identifiant nécessaire pour attribuer des recettes à une publicité individuelle pour ces campagnes. Par conséquent, les données de performances au niveau des publicités ne sont pas disponibles pour ces types de campagne dans la variable [!UICONTROL Ads] ou dans le [!UICONTROL Ad Variation Report]. Vous pouvez vous attendre à des incohérences entre le total des données au niveau de la publicité pour une campagne et le total des données de la campagne.
+++

+++Dans le [!UICONTROL Transaction Report], comment savoir quelle propriété de transaction provient d’un flux de données ou est suivie par le pixel de suivi Adobe Advertising ?
Dans un rapport de transaction, vous pouvez déterminer si une propriété de transaction incluse a été suivie par le pixel de suivi Adobe Advertising si vous incluez la colonne personnalisée &quot;[!UICONTROL Tracking URL].&quot; Le suivi des URL avec le pixel de suivi Advertising Adobe commence par &quot;`http://pixel.everesttech.net`.&quot;
+++

+++Les données de mon [!UICONTROL Transaction Report] ne correspond pas aux données de mon [!UICONTROL Keyword Report].
Lorsque vous générez les deux rapports par portefeuille, les données sont différentes si vous générez la variable [!UICONTROL Keyword Report] en utilisant des données historiques (c’est-à-dire en fonction de la configuration du portfolio aux dates spécifiées) plutôt qu’en utilisant des données pour les campagnes actives. Lorsque vous générez la variable [!UICONTROL Transaction Report] par portfolio, il inclut les données des campagnes actuelles du portfolio.
+++

## Flux de feuille de calcul

+++La sortie du rapport comprend un mélange de plages de dates.
Vous pouvez voir différentes périodes si le flux agrège les données à l’aide d’un niveau d’agrégation de données autre que &quot;[!UICONTROL Daily].&quot;

Pour résoudre ce problème, mettez à jour le flux de feuille de calcul afin d’inclure les données agrégées quotidiennement. Cette tâche comprend la mise à jour du modèle de rapport, la génération d’un rapport à l’aide du modèle et la création d’un [!DNL Microsoft® Excel] à l’aide du rapport, puis en mettant à jour les paramètres du flux afin d’inclure le nouveau modèle Excel. Pour plus d’informations, voir[Modifier les paramètres du flux de rapports de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++Un flux de feuille de calcul génère une erreur interne.
Cette erreur peut se produire si vous modifiez les colonnes du modèle de rapport sans mettre à jour le [!DNL Microsoft® Excel] modèle en conséquence.

Pour résoudre ce problème, mettez à jour le flux de feuille de calcul afin d’inclure les nouvelles colonnes. Cette tâche comprend la mise à jour du modèle de rapport, la génération d’un rapport à l’aide du modèle et la création d’un [!DNL Excel] à l’aide du rapport, puis en mettant à jour les paramètres du flux afin d’inclure le nouveau modèle Excel. Pour plus d’informations, voir[Modifier les paramètres du flux de rapports de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++Lorsque j’essaie d’ouvrir un flux de feuille de calcul dans [!DNL Excel], [!DNL Excel] signale une erreur &quot;contenu illisible&quot; et les données sont supprimées du contenu récupéré.
Lorsque la variable [!DNL Microsoft® Excel] ne trie pas les données par date de début dans l’ordre croissant, le flux de feuille de calcul peut contenir des lignes vides. En particulier, [!DNL Excel] signale l’erreur &quot;Excel a trouvé du contenu illisible dans &#39;&lt;*nom du rapport*>.xlsx.&#39; Voulez-vous récupérer le contenu du classeur ? Si vous approuvez la source de ce classeur, cliquez sur oui.&quot; Si vous cliquez sur &quot;Oui&quot;, le message suivant s’affiche : &quot;Supprimés d’enregistrements : Informations sur la cellule de la /xl/worksheets/sheet1.xml partie &quot; et le flux de feuille de calcul comprend des lignes vides.

Pour résoudre le problème, modifiez la variable [!DNL Excel] modèle associé au flux pour trier les données par [!DNL Start date in Ascending (Oldest to Newest) order], puis transférez le modèle mis à jour via les paramètres de flux de feuille de calcul. Pour plus d’informations, voir[Modification des flux de rapports de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++
