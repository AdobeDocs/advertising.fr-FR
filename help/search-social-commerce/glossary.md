---
title: Glossaire
description: Voir les définitions des termes clés.
exl-id: 87ce61b5-8340-4a6b-bd98-89ef73b2a9d8
feature: Search Introduction
source-git-commit: 128446e8fad1e2c973a62042933cc52bb556a71d
workflow-type: tm+mt
source-wordcount: '2242'
ht-degree: 0%

---

# Glossaire {#glossary}

## A-B {#a-b}

**groupe publicitaire :** ensemble de publicités et de leurs mots-clés, emplacements et groupes de produits associés pour une campagne.

**variation publicitaire :** toute publicité dans un groupe publicitaire ou une stratégie publicitaire.

**[AMO ID](/help/integrations/analytics/ids.md#amo-id) :** code de suivi qui permet à l’Adobe Advertising de partager des données sur les campagnes avec Adobe Analytics. Elle commence par `s_kwcid=`.

**Unité d’offre :** Terme de recherche, de Social et de Commerce pour une unité sur laquelle des offres sont placées.

* Pour les campagnes CPC, il s’agit d’un mot-clé et de son type de correspondance pour une campagne de recherche ou de contenu, un groupe de produits au niveau de l’unité (le niveau de subdivisions le plus bas) pour une campagne d’achat ou une cible de recherche dynamique pour une campagne d’annonces de recherche dynamique. Lorsque le même mot-clé et la même combinaison de type de correspondance, le même groupe de produits ou la même cible de recherche dynamique se produisent dans plusieurs groupes publicitaires au sein d’une même campagne, toutes les instances sont considérées comme la même unité d’offre et ont donc la même offre.

* Pour les campagnes avec les stratégies de dépenses [!DNL Maximize Clicks], [!DNL Maximize Conversion Value], [!DNL Maximize Conversions], [!DNL Target Cost Per Acquisition] ou [!DNL Target Return on Ad Spend], chaque campagne est une unité d&#39;offre.

* Pour les campagnes sur [!DNL Yahoo! Display Network], qui n&#39;utilisent pas de mots-clés, toutes les publicités d&#39;un groupe publicitaire ont la même offre et sont considérées comme la même unité d&#39;offre.

**Contrainte d’unité d’offre :** Voir &quot;Contrainte&quot;.

## C-D {#c-d}

**campaign :** ensemble de groupes publicitaires dans un seul compte publicitaire partageant un budget, une période, un ciblage et d’autres paramètres. **Remarque :** [!DNL Baidu] n’a pas le concept de campagne, mais Search, Social et Commerce crée des pseudo-campagnes pour chaque ensemble de groupes d’annonces associés dans les comptes [!DNL Baidu] existants qui sont synchronisés dans Search, Social et Commerce.

**Champ sensible à la casse :** Un champ ou une requête sensible à la casse traite les lettres majuscules (C, par exemple) différemment des lettres minuscules (c, par exemple). Par exemple, Car est traité comme une valeur différente de Car.

**click:** Un utilisateur unique clique sur ou dans une publicité en ligne.

**Intervalle de recherche en amont des clics :** paramètre au niveau de l’annonceur qui spécifie le nombre de jours après un clic payant dans une série d’événements au cours duquel le clic peut être attribué à une conversion.

**heure des clics :** heure à laquelle un utilisateur final disposant d’une adresse IP unique clique pour la première fois sur une publicité dans le réseau publicitaire.

**Taux de clics :** (CTR) nombre de clics divisé par le nombre d’impressions sur une publicité. Les publicités les plus pertinentes pour la requête de recherche ont le taux de clics publicitaires le plus élevé.

**URL de suivi des clics :** modèle de suivi ou URL de destination avec code incorporé pour effectuer le suivi des clics sur un mot-clé, une variation de publicité ou un emplacement.

**Contrainte :** (Publicitaires avec portefeuilles ; applicable aux unités d’offre dans les portefeuilles standard uniquement) Règle pour l’enchère sur un mot-clé ou une publicité spécifique. Il remplace toutes les limites au niveau du portefeuille et la stratégie d’offre recommandée.

**conversion :** aboutissement d’une action après qu’un utilisateur final a cliqué sur une publicité, généralement capturée comme mesure. Par exemple, les inscriptions et les achats et ils peuvent représenter des décomptes ou des montants monétaires. Une conversion peut comporter un ou plusieurs événements de transaction, mais les termes &quot;conversion&quot; et &quot;transaction&quot; sont souvent interchangeables.

**Suivi des conversions :** Le suivi des conversions utilise des cookies pour effectuer le suivi a) des clics sur les publicités d’un annonceur sur les réseaux publicitaires et b) des transactions résultantes sur le site web de l’annonceur.

**Précision des coûts :** (Annonceurs avec portefeuilles) Dépense réelle pour un portefeuille divisée par les dépenses prévues. Les [rapports de précision du modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indiquent la précision des modèles de coûts utilisés pour l’optimisation, et la [[!UICONTROL Model Accuracy]perspicacité](/help/search-social-commerce/advertising-insights/insight-about.md) comprend plus de détails, en plus des recommandations visant à améliorer la précision du modèle.

**Modèle de coût :** (annonceurs avec portefeuilles) Technologie Search, Social, &amp; Commerce qui prédit le volume de coût, l’offre requise pour gagner chaque poste ou emplacement, et le CPC (recherche) ou CPM (affichage) pour chaque unité d’offre à l’aide de données historiques et de techniques de prévision mathématique.

**Couverture du modèle de coût :** (Publicitaires avec portefeuilles) Le nombre et/ou le pourcentage d’unités d’offre dans les campagnes CPC ou eCPC qui ont reçu au moins une impression au cours des sept derniers jours afin que la fonctionnalité d’optimisation puisse créer des modèles de coûts. Toutes les unités d’offre n’ont pas de modèle de coût ; les unités d’offre avec les modèles de coût sont comptabilisées dans la couverture du modèle de coût.

**demi-vie du modèle de coût :** (annonceurs avec portefeuilles) nombre de jours avant la date actuelle pour laquelle les données de coût sont considérées plus récentes et donc plus pertinentes pour les modèles de coûts.

**coût par 1 000 impressions :** (CPM) Le coût d’une publicité pour chaque millier d’impressions. Les annonceurs qui utilisent un modèle de tarification CPM paient par impressions plutôt que par clics.

**coût par acquisition :** (CPA) coût d’une publicité divisé par le nombre de conversions. Également appelé coût par transaction (CPT) ou coût par commande (CPO).

**coût par clic :** (CPC) 1) Coût d’une publicité divisé par le nombre total de clics pour la publicité. Par exemple, si vous dépensez 100 USD pour une impression publicitaire et que la publicité génère 10 clics, le coût par clic est de 100 USD/10=10 USD par clic. 2) Un modèle de tarification dans lequel les annonceurs sont facturés pour chaque clic publicitaire.

**coût par commande :** (CPO) coût d’une publicité divisé par le nombre de commandes. Également appelé coût par acquisition (CPA) ou coût par transaction (CPT).

**coût par transaction :** (CPT) coût d’une publicité divisé par le nombre de transactions. Également appelé coût par acquisition (CPA).

**CPA :** Voir &quot;Coût par acquisition&quot;.

**CPC :** Voir &quot;coût par clic&quot;.

**CPM :** Voir &quot;coût par 1 000 impressions&quot;.

**CPO :** Voir &quot;coût par commande&quot;.

**CPT :** Voir &quot;coût par transaction&quot;.

**CSV :** Format de fichier constitué de valeurs séparées par des virgules (CSV).

**CTR :** Voir &quot;taux de clics publicitaires&quot;.

## E-F {#e-f}

**eCPM :** le CPM effectif, ou le coût moyen payé par 1 000 impressions au cours d’une période spécifiée. Les valeurs eCPM peuvent être calculées pour les campagnes CPM ou CPC.

## G-H {#g-h}

**demi-vie :** temps nécessaire pour qu’une quantité diminue à la moitié de sa valeur initiale. Pour chaque portefeuille, vous pouvez spécifier des demi-vies pour indiquer la durée de validité des données pour les modèles de coûts et de recettes.
Voir &quot;demi-vie du modèle de coût&quot; et &quot;demi-vie du modèle de revenu&quot;.

## I-J {#i-j}

**impression :** affichage unique d’une publicité sur une page web, une application mobile ou tout autre support de diffusion. Un utilisateur n’a pas à afficher ni à cliquer sur la publicité pour qu’elle soit comptée comme impression.

**Intervalle de recherche en amont des impressions :** (Campagnes d’affichage et de réseaux sociaux uniquement) Paramètre au niveau de l’annonceur qui spécifie le nombre de jours après une impression publicitaire que l’impression peut être attribuée à une conversion.

**poids de remplacement des impressions :** pourcentage spécifié d’une valeur de conversion à attribuer aux impressions qui se produisent dans l’intervalle de recherche en amont des impressions du client lorsque la conversion est précédée de clics payants et d’impressions. Lorsqu’une conversion est précédée uniquement par des impressions, le poids d’affichage publicitaire de l’annonceur, plutôt que le poids de remplacement d’impression, est appliqué aux impressions.

## K-L {#k-l}

**mot-clé :** mot ou expression associé à une publicité.

**Contrainte par mot-clé :** Voir &quot;Contrainte&quot;.

**classification d’étiquettes :** Méthode de regroupement des composants de votre compte en ensembles significatifs. Une classification d’étiquettes peut contenir plusieurs valeurs d’étiquettes qui désignent des attributs. Par exemple, une classification d’étiquettes &quot;Géo&quot; peut inclure des valeurs pour différentes régions géographiques.

**valeur d’étiquette :** Élément d’une classification d’étiquettes. Il peut être attribué en tant que balise aux campagnes publicitaires et aux entités de campagne afin que vous puissiez filtrer les données de performances et les rapports par libellé ou configurer des contraintes facultatives sur les unités d’offre associées au libellé.

**URL de la page d’entrée :** URL de la page web de l’annonceur qui s’ouvre lorsque l’utilisateur final clique sur une publicité.

## M-N {#m-n}

**coût marginal :** changement du coût total lorsque la quantité change d’une unité.

**Valeur marginale du coût à l’objectif :** changement de coût nécessaire pour augmenter la valeur objective d’une (1). Celui-ci a la même valeur que la colonne héritée &quot;Coût marginal/Recettes&quot;.

**type de correspondance :** Une option qui spécifie la manière dont les termes de recherche sont associés aux publicités. Les options varient selon le réseau publicitaire.

**offre minimale :** 1) Montant minimum à payer par impression ou par 1 000 impressions. 2) Pour les mots-clés de recherche, offre minimale requise pour un mot-clé donné en fonction de son score de qualité. L&#39;offre minimale est généralement le montant le moins élevé que vous puissiez payer par clic pour que votre mot-clé affiche des publicités.

**Précision du modèle :** (Annonceurs avec portefeuilles) Pourcentage de précision des modèles de coûts et de recettes utilisés pour optimiser les offres, les budgets de campagne et les cibles de stratégie d’offre pour un portefeuille. Voir &quot;Modèle de coût&quot;, &quot;Précision des coûts&quot;, &quot;Modèle des recettes&quot; et &quot;Précision des recettes&quot;.

## O-P {#o-p}

**objectif :** (annonceurs disposant de portefeuilles) objectif qu’un client définit pour atteindre son objectif commercial dans le cadre d’un portefeuille spécifique ou d’une campagne d’affichage, par exemple pour maximiser les bénéfices ou atteindre une cible de vente spécifique. Un objectif consiste à effectuer le suivi et l’optimisation des mesures de conversion pour le portefeuille, ainsi qu’à déterminer leur poids relatif. Les conversions pondérées totales du portfolio sont calculées comme la &quot;valeur objective&quot;.

**Valeur de l’objectif :** (Publicitaires avec portefeuilles) Le total des conversions pondérées tel que calculé en fonction de l’objectif actuel du portfolio, notamment :

* toutes les conversions, en prenant en compte a) les poids affectés à chaque conversion dans l’objectif du portfolio et, le cas échéant, b) le poids d’affichage publicitaire pour les affichages publicitaires.

* tous les clics, que la fonctionnalité d’optimisation prend en compte pour une seule conversion et est pondérée en fonction de la valeur de clic de l’objectif.

Cette valeur est identique à celle de la colonne héritée &quot;Recettes pondérées&quot;.

**fonctionnalité d’optimisation :** (annonceurs avec portefeuilles) Technologie d’offre par mot-clé Search, Social et Commerce, qui détermine la stratégie optimale d’offre et de gestion du budget pour un portefeuille en fonction de son objectif commercial.

**transaction orpheline :** événement de transaction ne pouvant pas être associé à un mot-clé ou à une publicité spécifique.

**pixel :** image transparente, d’un pixel par un pixel incorporée sur une page web à des fins de suivi. Les balises de suivi de conversion d’Adobe Advertising incluent un pixel d’image d’HTML ou JavaScript pour effectuer le suivi des clics et des transactions qui en résultent.

**placement :** Emplacement sur un réseau d’affichage dans lequel vos publicités peuvent apparaître. Il peut s’agir d’un site web entier, d’un sous-ensemble d’un site web ou d’une position publicitaire sur une page spécifique.

**portfolio :** ensemble de campagnes publicitaires et de leurs unités d’offre associées, optimisées pour un seul objectif commercial et une cible de performances.

**POS :** pourcentage de dépenses

**PPC :** Voir &quot;paiement par clic&quot;.

**property:** Voir &quot;mesure de conversion&quot;.

**property time:** Heure à laquelle un événement de conversion individuel se produit. Lorsqu’un événement comprend des événements de relance associés (par exemple, un client qui s’enregistre d’abord pour un essai gratuit et s’abonne ensuite à un service payant), chaque événement a sa propre heure de propriété.

## Q-R {#q-r}

**note de qualité :** un score attribué par un réseau publicitaire à l’un de vos mots-clés pour déterminer le prix de l’offre et la position de l’annonce. Il est calculé en fonction de la pertinence du mot-clé par rapport à la publicité associée et à la requête de recherche de l’utilisateur, du taux de clics publicitaires du mot-clé et d’autres facteurs.

**URL de redirection :** Partie d’une URL de destination qui envoie l’utilisateur vers un autre serveur avant ou à la place de la page d’entrée de l’annonceur.

**retour sur investissement :** (ROI) Recettes moins les coûts.

**Précision des recettes :** (Publicitaires avec portefeuilles) Recettes réelles pour un portefeuille divisé par les recettes prévues. Les [rapports de précision du modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indiquent la précision des modèles de recettes utilisés pour l’optimisation et la [[!UICONTROL Model Accuracy]perspicacité](/help/search-social-commerce/advertising-insights/insight-about.md) comprend plus de détails, en plus des recommandations visant à améliorer la précision du modèle.

**Modèle de recettes :** (Publicitaires avec portefeuilles) technologie de recherche, de réseaux sociaux et de Commerce qui prédit le taux de conversion et le retour estimé pour chaque unité d’offre, en fonction des données de clic (recherche et réseaux sociaux) ou des données d’impression (affichage) et des données de conversion de l’annonceur.

**Couverture du modèle de chiffre d’affaires :** (Publicitaires avec portefeuilles) Nombre et/ou pourcentage d’unités d’offre dans un portefeuille avec des modèles de chiffre d’affaires. Les unités d’offre peuvent avoir des modèles de recettes même si elles n’ont pas reçu de recettes mais ont reçu des impressions.

**demi-vie du modèle de chiffre d’affaires :** (Publicitaires avec portefeuilles) : nombre de jours avant la date actuelle pour laquelle les données sur les recettes sont considérées comme plus récentes et donc plus pertinentes pour les modèles de recettes.

**ROI :** Voir &quot;retour sur investissement&quot;.

## S-T {#s-t}

**simulation :** (Annonceurs avec portefeuilles) modélisation de Portfolio qui estime le nombre de clics et de conversions qu’un portfolio peut attendre pour différents niveaux de dépenses et budgets quotidiens correspondants, à l’aide de données historiques.

**stratégie de dépenses :** (annonceurs avec portefeuilles) Stratégie sélectionnée pour optimiser les enchères sur mots-clés/publicités pour un portefeuille.

**`s_kwcid`:** voir &quot;AMO ID&quot;.

**URL de suivi :** Un modèle de suivi ou une URL de destination avec des paramètres supplémentaires ajoutés pour effectuer le suivi des informations sur les clics sur la publicité. Il peut inclure une URL de redirection permettant d’envoyer d’abord les utilisateurs à un serveur de suivi avant de les rediriger vers la page d’entrée de l’annonceur.

**transaction :** Tout événement pouvant faire l’objet d’un suivi qui se produit en ligne ou hors ligne. Plusieurs événements de transaction peuvent être suivis ensemble dans le cadre d’une même transaction ou conversion ; par exemple, une demande de renseignements en ligne ainsi qu’une commande par téléphone qui en résulte peuvent être considérés comme des composants d’un achat. Les termes &quot;transaction&quot; et &quot;conversion&quot; sont souvent interchangeables. Une transaction est représentée par un identifiant de transaction, auquel sont associées une ou plusieurs propriétés.

**ID de transaction :** identifiant spécifié par l’annonceur qui identifie une transaction. Lorsqu’une transaction comprend plusieurs événements, ils ont tous le même ID de transaction.

**propriété de transaction :** Voir &quot;conversion&quot;.

**temps de transaction :** heure à laquelle un clic ou une impression est converti en transaction. Lorsqu’une transaction se compose de plusieurs événements de transaction (par exemple, lorsqu’un client s’inscrit pour la première fois à un essai gratuit et s’abonne ensuite à un service payant), le temps de transaction provient du premier événement de la chaîne (s’inscrivant pour l’essai gratuit).

**TSV :** Format de fichier constitué de valeurs séparées par des tabulations (CSV).

## U-V {#u-v}

**affichage publicitaire :** (affichage et publicités sociales) Une impression publicitaire (ou chaîne d’impressions) qui entraîne une conversion sans que l’utilisateur ne clique sur une publicité.

**poids d’affichage publicitaire :** (campagnes d’affichage et de réseaux sociaux uniquement) Paramètre au niveau de l’annonceur qui spécifie le poids à attribuer à une conversion d’affichage publicitaire par rapport au poids attribué à une conversion basée sur les clics, en pourcentage.

## W-X {#w-x}

**objectif pondéré :** Voir &quot;objectif&quot;.

**revenu pondéré :** Voir &quot;valeur objective&quot;.

**XLS** ou **XLSX** : format de fichier binaire pour les classeurs [!DNL Microsoft Office Excel].

## Y-Z {#y-z}
