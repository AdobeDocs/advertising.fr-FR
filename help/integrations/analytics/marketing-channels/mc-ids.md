---
title: Utilisation des Adobe Advertising ID pour créer  [!DNL Marketing Channels]  règles
description: Découvrez comment utiliser les Adobe Advertising ID pour créer des règles de traitement pour  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Utilisation des Adobe Advertising ID pour la création de règles de traitement des [!DNL Marketing Channels]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Vous pouvez utiliser les identifiants Adobe Advertising ([AMO ID et EF ID](../ids.md)) pour configurer les règles de traitement des [!DNL Marketing Channels] dans Adobe Analytics. Utilisez les Adobe Advertising ID pour les règles spécifiques à vos campagnes Adobe Advertising. L’ordre dans lequel vous traitez les règles détermine si toutes les données possibles sont capturées correctement.

## ID AMO dans les règles de traitement

L’ID AMO est le code de suivi principal utilisé pour signaler les données Adobe Advertising dans [!DNL Analytics]. L’ID AMO est une concaténation de valeurs dynamiques gérées par Adobe afin de fournir des rapports granulaires dans [!DNL Analytics]. Il est stocké dans une dimension [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (AMO ID). L’AMO ID peut être défini dans [!DNL Analytics] de deux manières :

* Suivi des clics publicitaires : Adobe Advertising définit le paramètre de chaîne de requête `s_kwcid` dans un lien et [!DNL Analytics] sélectionne le paramètre dans l’URL de la page de destination en cas de clic publicitaire.

* Suivi des affichages publicitaires ([!DNL DSP] uniquement) : l’[!DNL Last Event Service] détecte une affichage publicitaire côté serveur et envoie l’AMO ID à [!DNL Analytics]. Dans ce cas, l’URL ne contient pas de paramètre `s_kwcid`.

Les valeurs dynamiques dans les ID AMO indiquent le canal marketing qui a été suivi :

* Le préfixe dans l’AMO ID peut être utilisé pour identifier le canal de niveau supérieur dans [!DNL Marketing Channels].

* Les expressions de caractères dans le corps de l’ID AMO indiquent un type de campagne plus spécifique.

* Le suffixe « vt » est présent pour [!DNL DSP] trafic d’affichage publicitaire et peut être utilisé pour créer des canaux d’[!DNL DSP] d’affichage publicitaire et d’affichage publicitaire distincts.

Le reste de l’AMO ID peut être ignoré.

| [!UICONTROL AMO ID] | Canal | Logique de règle |
|--------|---------|--------------------|
| !ctv (suffixe) | [!UICONTROL DSP Connected TV ViewThrough] | Se Termine Par |
| !d ! (corps) | [!UICONTROL Display Network] | Contient |
| !g ! (corps) | [!UICONTROL Google Search] | Contient |
| !s ! (corps) | [!UICONTROL Search Partner] | Contient |
| !u ! (corps) | [!UICONTROL Smart Shopping Campaign] | Contient |
| !ytv ! (corps) | [!UICONTROL YouTube Video Ad] | Contient |
| !yts ! (corps) | [!UICONTROL YouTube Search Ad] | Contient |
| !vp ! (corps) | [!UICONTROL Google Video Partners] | Contient |
| !vt (suffixe) | [!UICONTROL DSP ViewThrough] | Se Termine Par |
| AL ! (préfixe) | [!UICONTROL Paid Search] | Commence Par |
| AC ! (préfixe) | [!UICONTROL DSP Display] | Commence Par |

## Identifiant de l’élément de formulaire dans les règles de traitement

L’ID EF AMO (ID EF) est le deuxième code de suivi utilisé dans l’intégration [!DNL Analytics for Advertising]. Son principal objectif est de suivre et de transmettre des données d’événement [!DNL Analytics] dans Adobe Advertising. Chaque fois qu’un clic publicitaire ou une affichage publicitaire se produit, un identifiant d’événement publicitaire unique est généré, même s’il s’agit exactement de la même publicité pour le même visiteur. L’ID EF n’est pas utilisé dans l’interface utilisateur de création de rapports [!DNL Analytics], car il dépasse généralement les 500 000 valeurs uniques par limite de variable dans [!DNL Analytics], ce qui le rend inutilisable pour la création de rapports. Les mesures et métadonnées d’Adobe Advertising ne s’appliquent pas à l’ID d’environnement de travail, mais uniquement à l’ID AMO. La granularité ajoutée du tracking est requise pour l’optimisation des campagnes dans Adobe Advertising. Les deux identifiants sont donc requis.

Bien que la dimension Identifiant de l’événement ne soit pas utilisée directement dans les rapports [!DNL Analytics], l’identifiant de l’événement peut s’avérer utile dans la création de canaux marketing. Le suffixe de l’ID de l’EF indique le canal (affichage ou recherche) et si la visite a été effectuée par un clic publicitaire ou une vue publicitaire. Le délimiteur de l’ID EF est un signe deux-points plutôt que le point d’exclamation de l’ID AMO.

| Suffixe de l’ID EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Exemples de règles de traitement pour Adobe Advertising

L’exemple de jeu de règles suivant se concentre sur les règles des canaux publicitaires (référencement payant, affichage ClickThrough et affichage ViewThrough). La règle recommandée pour la détection de référencement payant (y compris la manière dont cette règle interagit avec la logique de canal marketing de recherche naturelle) et une mise à jour facultative de la règle Domaines référents naturels sont également illustrées.

**Remarque :** l’affichage peut être séparé en deux canaux ou fusionné en un seul canal en fonction des préférences de l’annonceur.

D’autres canaux sont inclus dans l’exemple de capture d’écran afin d’illustrer l’ordre recommandé des opérations des canaux publicitaires par rapport à d’autres canaux dans une implémentation standard.

>[!IMPORTANT]
>
>Pour plus d’informations sur l’ordre dans lequel vos règles doivent être traitées, voir « [Ordre des opérations pour  [!DNL Marketing Channels] règles](#rule-order) ».

![Exemple d’ensemble de règles de traitement](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### Règle de référencement payant

La bonne pratique consiste à inclure deux conditions avec l’opérateur « Any » pour une règle [!UICONTROL Paid Search] :

* Les données de coût/clic/impression contiennent l’AMO ID. Incluez donc l’AMO ID. L’ID AMO doit commencer par « AL ». pour attribuer correctement des données de clics/coûts/impressions à [!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* Les URL relatives aux clics [!UICONTROL Paid Search] incluent toujours le paramètre de chaîne de requête `s_kwcid`. Par conséquent, incluez-le pour vous assurer qu’une déduplication correcte se produit si le visiteur revient à la page de destination. Inclure « AL ! » avant l’`s_kwcid` d’affecter correctement les données de clics/coûts/impressions aux [!UICONTROL Paid Search].

Ne définissez pas la valeur du canal sur l’ID AMO. Au lieu de cela, définissez-le sur une valeur telle que le domaine référent, le moteur de recherche + mot-clé ou la page. (Ceci est pertinent pour tous les [!DNL Marketing Channels]).

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![Exemple de règle de recherche payante](/help/integrations/assets/a4adc-mc-rule-paid-search.png "Exemple de règle de recherche payante")

### Règle de recherche naturelle

Par [!UICONTROL Natural Search], assurez-vous que vos règles de détection de [[!UICONTROL Paid Search]](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection) incluent les paramètres de chaîne de requête `ef_id` et `s_kwcid`. (En règle générale, cela est automatiquement configuré lorsque Advertising Search, Social et Commerce est intégré à [!DNL Analytics], mais vérifiez si un administrateur [!DNL Analytics] a modifié la logique une fois l’intégration configurée.)

Définissez la règle sur « Correspond aux règles de détection de recherche naturelle » (qui est généralement le paramètre par défaut pour ce canal).

![Exemple de règle de recherche naturelle](/help/integrations/assets/a4adc-mc-rule-natural-search.png "Exemple de règle de recherche naturelle")

### Afficher les #1 de règles de clic publicitaire

Créez un canal marketing Afficher les clics publicitaires en capturant uniquement les clics publicitaires. Comme l’ID AMO est le même pour les clics publicitaires et les affichages publicitaires, cette règle utilise la variable EF ID et le paramètre de chaîne de requête `ef_id`.

Parfois, les clics publicitaires sont suivis via l’URL (valeur par défaut). Dans d’autres cas, les clics publicitaires sont suivis via le service Last Event du côté serveur. Par conséquent, l’URL ne contient pas le paramètre `ef_id`. La règle vérifie donc les conditions dans lesquelles la variable EF ID ou le paramètre de chaîne de requête `ef_id` se termine par « :d ». Utilisez l’opérateur « `Any` », car vous souhaitez que cette règle soit déclenchée pour l’une ou l’autre des conditions.

![Exemple de première règle Afficher ClickThrough](/help/integrations/assets/a4adc-mc-rule-display-ct.png "Exemple de première règle Afficher ClickThrough")

### Règle des domaines référents naturels

(Facultatif) La bonne pratique consiste à ajouter une condition « Est la première page de la visite » avec l’opérateur « Any » à la règle de [!UICONTROL Natural Referring Domains] standard. Bien que cette règle soit facultative, elle peut empêcher la définition du scénario de référence naturelle lorsque l’utilisateur clique sur le bouton Précédent pour revenir à la page de destination.

![Exemple de règle de domaines référents naturels](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "Exemple de règle de domaines référents naturels")

### Afficher la règle de visualisation CTV

Pour effectuer le suivi des affichages de [!DNL DSP] TV connectée (CTV), créez une règle dans laquelle l’AMO ID se termine par `"!ctv"`. Comme le visiteur n’a pas cliqué sur l’annonce publicitaire, le suivi des affichages publicitaires n’inclut pas le `ef_id` ou le `s_kwcid` dans l’URL et la règle ne nécessite qu’une seule condition.

![Exemple de règle Afficher CTV ViewThrough](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png "Exemple de règle Afficher CTV ViewThrough")

### Afficher la règle d&#39;affichage publicitaire

Pour créer un canal Afficher le parcours, créez une règle dans laquelle l’ID EF se termine par « :i ». Comme le visiteur n’a pas cliqué sur l’annonce publicitaire, le suivi des affichages publicitaires n’inclut pas le `ef_id` ou le `s_kwcid` dans l’URL et la règle ne nécessite qu’une seule condition.

![Exemple de règle Display ViewThrough](/help/integrations/assets/a4adc-mc-rule-display-vt.png "Exemple de règle Display ViewThrough")

### Afficher les #2 de règles de clic publicitaire

Pour la deuxième règle Afficher ClickThrough, définissez **L’identifiant AMO commence par « AC ! ».**. Cette deuxième règle existe pour capturer les données de clic/coût/impression pour le canal d’affichage qui arrivent directement d’Adobe Advertising à [!DNL Analytics]. Ces données sont attribuées à un ID AMO, mais n’incluent pas d’URL avec la chaîne de requête `ef_id`. Ces accès ne sont donc pas connectés à un ID AMO EF, ce qui est ce que capture la première règle Display ClickThrough.

![Exemple de deuxième règle Afficher ClickThrough](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "Exemple de deuxième règle Afficher ClickThrough")

## Ordre des opérations pour les règles de [!DNL Marketing Channels] {#rule-order}

![Ordre idéal des opérations pour les règles liées à Adobe Advertising](/help/integrations/assets/a4adc-mc-rule-order.png "Ordre idéal des opérations pour les règles liées à Adobe Advertising")

* Mettez [!UICONTROL Paid Search] *avant* [!UICONTROL Natural Search]. Dans le cas contraire, les données de référencement payant peuvent être affectées au référencement naturel.

* Mettez le **premier** [!UICONTROL Display ClickThrough] *avant* [!UICONTROL Natural Referring Domains] et [!UICONTROL Natural Social].

* Lorsque vous utilisez [!UICONTROL CTV view-throughs], placez-le *avant* [!UICONTROL Display ViewThroughs]. Sinon, les vues publicitaires CTV seront capturées en tant que vues publicitaires.

* Insérez [!UICONTROL Display ViewThroughs] *après* d’autres canaux, mais avant [!UICONTROL Internal] et [!UICONTROL Direct], car il est possible qu’un affichage publicitaire et un clic publicitaire non [!DNL Advertising] se produisent dans le même événement d’atterrissage. Par exemple, un visiteur peut voir une annonce Adobe Advertising, avoir une impression, puis accéder au site par [!UICONTROL Natural Search].

  La bonne pratique consiste à donner la priorité aux autres canaux (à l’exception de [!UICONTROL Internal] et [!UICONTROL Direct]) sur les vues globales.

* Certains annonceurs peuvent choisir de donner la priorité aux [!UICONTROL Display ViewThroughs] plutôt qu’aux [!UICONTROL Natural Referring Domains]. Pour ce faire, permutez l’ordre de traitement des deux règles.

* La règle de **** second[!UICONTROL Display ClickThrough] permet d’intercepter les données de clic/coût/impression qui entrent directement d’Adobe Advertising vers [!DNL Analytics]. Comme ces données sont uniquement attribuées à un ID AMO, ces accès ne sont pas connectés à un ID AMO EF. Si vous ne définissez pas cette règle, toutes les données de clics/coûts/impressions se trouvent sous le canal [!UICONTROL Direct], qui est le canal par défaut pour toutes les données qui ne correspondent pas à un [!DNL Marketing Channel]. Cette règle doit venir *après* la règle d&#39;affichage publicitaire ou elle récupérera n&#39;importe quel affichage publicitaire.

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [Principes fondamentaux de  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Pourquoi les données de canal peuvent varier entre Adobe Advertising et  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilisation [!DNL Analytics Marketing Channels] avec des données Adobe Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation  [!DNL Marketing Channels]  rapports pour Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising ID utilisés par  [!DNL Analytics]](/help/integrations/analytics/ids.md)