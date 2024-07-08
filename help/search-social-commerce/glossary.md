---
title: Glossaire
description: Voir les définitions des termes clés.
exl-id: 87ce61b5-8340-4a6b-bd98-89ef73b2a9d8
feature: Search Introduction
source-git-commit: 3500e22944223997dc56dc94c24639a57e8c54f4
workflow-type: tm+mt
source-wordcount: '2081'
ht-degree: 0%

---

# Glossaire {#glossary}

## A à B {#a-b}

**Groupe publicitaire :** ensemble d’annonces et leurs mots-clés, emplacements et groupes de produits associés pour une campagne.

**Variante publicitaire :** toute publicité au sein d’un groupe publicitaire ou d’une stratégie publicitaire.

**[AMO ID](/help/integrations/analytics/ids.md#amo-id) :** code de suivi qui permet à Adobe Advertising de partager des données sur les campagnes avec Adobe Analytics. Il commence par `s_kwcid=`.

**Unité d’offre :** terme Search, Social et commercial désignant une unité sur laquelle des offres sont placées.

* Pour les campagnes CPC, il s’agit d’un mot-clé et de son type de correspondance pour une campagne de recherche ou de contenu, d’un groupe de produits au niveau de l’unité (le niveau de subdivision le plus bas) pour une campagne d’achat ou d’une cible de recherche dynamique pour une campagne d’annonces de recherche dynamique. Lorsque la même combinaison de mots clés et de types de correspondance, le même groupe de produits ou la même cible de recherche dynamique apparaissent au sein de plusieurs groupes d’annonces au sein d’une même campagne, toutes les instances sont considérées comme la même unité d’offre et ont donc la même enchère.

* Pour les campagnes dotées des stratégies , , , ou [!DNL Target Return on Ad Spend] [!DNL Target Cost Per Acquisition]dépenser, chaque campagne est une unité d’offre[!DNL Maximize Clicks]. [!DNL Maximize Conversions][!DNL Maximize Conversion Value]

* Dans le cas des campagnes sur [!DNL Yahoo! Display Network], qui n’utilisent pas de mots-clés, toutes les publicités d’un groupe d’annonces ont la même enchère et sont considérées comme la même unité d’offre.

**contrainte d’unité d’offre :** Voir « contrainte ».

## C-D {#c-d}

**campagne :** ensemble de groupes publicitaires dans un seul compte publicitaire qui partagent un budget, une période, un ciblage et d’autres paramètres. **Remarque :** [!DNL Baidu] n’a pas le concept de campagnes, mais Search, Social &amp; Commerce crée des pseudo-campagnes pour chaque ensemble de groupes d’annonces connexes dans les comptes existants [!DNL Baidu] qui sont synchronisés dans Search, Social et Commerce.

**Champ sensible à la casse :** un champ ou une requête sensible à la casse traite les lettres majuscules (telles que C) différemment des lettres minuscules (telles que C). Par exemple, Car est traité comme une valeur différente de la voiture.

**click :** un seul utilisateur clique sur ou dans une publicité en ligne.

**Fenêtre de recherche en amont des clics :** paramètre au niveau de l’annonceur qui spécifie le nombre de jours après un clic payant dans une série d’événements au cours desquels le clic peut être attribué à une conversion.

**temps de clic :** heure à laquelle un utilisateur final disposant d’une adresse IP unique clique pour la première fois sur une annonce dans le réseau publicitaire.

**Taux de clics publicitaires :** (CTR) Nombre de clics divisé par le nombre d’impressions sur une annonce. Les annonces les plus pertinentes pour la requête de recherche présentent les taux de clics publicitaires les plus élevés.

**URL de suivi des clics :** Un modèle de tracking ou une URL de destination avec code incorporé pour tracker les clics sur un mot-clé, une variation publicitaire ou un emplacement.

**contrainte :** (Annonceurs avec portefeuilles ; applicable aux unités d’enchères dans les portefeuilles standard uniquement) Règle d’enchères sur un mot-clé ou une annonce publicitaire spécifique. Il remplace toute limite au niveau du portefeuille et la stratégie d’enchères recommandée.

**conversion :** Fin d’une action après qu’un utilisateur final ou une utilisatrice finale a cliqué sur une publicité, généralement capturée sous la forme d’une mesure. Par exemple, les enregistrements et les achats, et ils peuvent représenter des décomptes ou des montants monétaires. Une conversion peut consister en un ou plusieurs événements de transaction, mais les termes « conversion » et « transaction » sont souvent utilisés de manière interchangeable.

**suivi des conversions :** Le suivi des conversions utilise des cookies pour suivre a) les clics sur les annonces publicitaires d’un annonceur sur les réseaux publicitaires et b) les transactions résultantes sur le site web de l’annonceur.

**précision des coûts :** (Annonceurs avec portefeuilles) Dépenses réelles d’un portefeuille divisées par les dépenses prévues.

**modèle de coût :** (Annonceurs disposant de portefeuilles) Technologie Search, Social et Commerce qui prédit le volume des coûts, l’offre requise pour remporter chaque poste ou emplacement et le CPC (recherche) ou le CPM (affichage) pour chaque unité d’offre à l’aide de données historiques et de techniques de prévision mathématique.

**couverture du modèle de coût :** (Annonceurs disposant de portefeuilles) Nombre et/ou pourcentage d’unités d’enchères dans les campagnes CPC ou eCPC qui ont reçu au moins une impression au cours des sept derniers jours afin que la fonctionnalité d’optimisation puisse créer des modèles de coût. Toutes les unités d’offre n’ont pas de modèle de coût ; les unités d’offre avec modèle de coût sont prises en compte dans la couverture du modèle de coût.

**demi-vie du modèle de coût :** (Annonceurs avec portefeuilles) Nombre de jours avant la date actuelle pendant lesquels les données de coût sont considérées comme plus récentes et donc plus pertinentes pour les modèles de coût.

**coût par 1 000 impressions :** (CPM) Coût d’une publicité pour mille impressions. Les annonceurs qui utilisent un modèle de tarification CPM paient par impressions plutôt que par clics.

**Coût par acquisition :** (CPA) Coût d’une publicité divisé par le nombre de conversions. Également appelé coût par transaction (CPT) ou coût par commande (CPO).

**Coût par clic :** (CPC) 1) Coût d’une annonce divisé par le nombre total de clics pour l’annonce. Par exemple, si vous dépensez 100 USD pour une impression publicitaire et que l’annonce génère 10 clics, le coût par clic est de 100 USD/10=10 USD par clic. 2) Un modèle de tarification dans lequel les annonceurs sont facturés pour chaque clic publicitaire.

**Coût par commande :** (CPO) Coût d’une publicité divisé par le nombre de commandes. Également appelé coût par acquisition (CPA) ou coût par transaction (CPT).

**coût par transaction :** (CPT) Coût d’une annonce publicitaire divisé par le nombre de transactions. Également appelé coût par acquisition (CPA).

**CPA :** Voir « coût par acquisition ».

**CPC :** voir « coût par clic ».

**CPM :** voir « coût par 1 000 impressions ».

**CPO :** Voir « coût par commande ».

**CPT :** Voir « coût par transaction ».

**CSV :** format de fichier composé de valeurs séparées par des virgules (CSV).

**CTR :** voir « taux de clics publicitaires ».

## E-F {#e-f}

**eCPM :** CPM effectif, ou coût moyen payé pour 1000 impressions au cours d’une plage de dates spécifiée. Les valeurs eCPM peuvent être calculées pour des campagnes CPM ou CPC.

## G-H {#g-h}

## I-J {#i-j}

**impression :** affichage unique d’une publicité sur une page Web, une application mobile ou un autre support de diffusion. Un utilisateur n’a pas besoin d’afficher ou de cliquer sur l’annonce pour qu’elle soit prise en compte comme une impression.

**Intervalle de recherche en amont des impressions :** (campagnes display et sociales uniquement) paramètre au niveau de l’annonceur qui spécifie le nombre de jours après l’impression d’une publicité pendant lesquels l’impression peut être attribuée à une conversion.

**Poids de remplacement des impressions :** pourcentage spécifié d’une valeur de conversion à attribuer aux impressions qui se produisent dans la fenêtre de recherche en amont des impressions du client lorsque la conversion est précédée de clics et d’impressions payés. Lorsqu’une conversion n’est précédée que d’impressions, le poids de visualisation de l’annonceur, plutôt que le poids de remplacement de l’impression, est appliqué aux impressions.

## K-L {#k-l}

**mot-clé :** Mot ou expression associé à une publicité.

**contrainte de mot-clé :** Voir « contrainte ».

**classification de libellé :** Un moyen de regrouper vos composants de compte en jeux significatifs. Une classification de libellés peut contenir plusieurs valeurs de libellé, qui indiquent des attributs. Par exemple, une classification d’étiquette « Géo » peut inclure des valeurs pour différentes régions géographiques.

**Valeur de l’étiquette :** élément d’une classification d’étiquette. Il peut être attribué en tant que balise aux campagnes publicitaires et aux entités de campagne afin que vous puissiez filtrer les données et les rapports de performances par étiquette ou configurer des contraintes facultatives sur les unités d’offre associées à l’étiquette.

**URL de la page de destination :** URL de la page Web de l’annonceur qui s’ouvre lorsque l’utilisateur final clique sur une annonce.

## M-N {#m-n}

**Coût marginal :** La variation du coût total lorsque la quantité change d’une unité.

**Valeur marginale du coût par rapport à l’objectif :** La variation du coût nécessaire pour augmenter la valeur objective d’un (1). Elle a la même valeur que la colonne héritée « Coût marginal par rapport aux recettes ».

**Type de correspondance :** option qui spécifie la manière dont les termes de recherche sont comparés aux publicités. Les options varient selon le réseau publicitaire.

**Offre minimum :** 1) Le montant minimum à payer par impression ou par 1000 impressions. 2) Pour les mots-clés de recherche, l’offre minimale requise pour un mot-clé donné en fonction de son score de qualité. L’enchère minimale est généralement le montant minimum que vous pouvez payer par clic pour que votre mot-clé affiche des annonces.

## O-P {#o-p}

**objectif :** (Annonceurs avec portefeuilles) Un objectif qu’un client fixe pour atteindre son objectif commercial pour un portefeuille spécifique ou une campagne d’affichage, par exemple pour maximiser les profits ou pour atteindre un objectif de vente spécifique. Un objectif se compose des mesures de conversion à suivre et à optimiser pour le portefeuille, ainsi que des pondérations relatives de ces mesures.

**Valeur objective :** (Annonceurs avec portefeuilles) Le total des conversions pondérées calculées en fonction de l’objectif actuel du portefeuille, y compris :

* toutes les conversions, en tenant compte a) des pondérations attribuées à chaque conversion dans la fonction objectif du portefeuille et, le cas échéant, b) de la pondération d’affichage pour les affichages publicitaires.

* Tous les clics, que la fonctionnalité d’optimisation considère comme une conversion unique et est pondéré en fonction de la valeur de clic pour l’objectif.

Elle a la même valeur que la colonne héritée « Recettes pondérées ».

**Capacité d’optimisation :** (Annonceurs avec portefeuilles) Technologie d’enchères de mots clés Search, Social &amp; Commerce, qui détermine la stratégie optimale d’enchères et de gestion budgétaire pour un portefeuille en fonction de son objectif commercial.

**Transaction orpheline :** événement de transaction qui ne peut pas être associé à un mot-clé ou à une annonce publicitaire spécifique.

**pixel :** image transparente d’un pixel par pixel intégrée à une page Web à des fins de suivi. Adobe Les balises de suivi des conversions publicitaires incluent un pixel d’image HTML ou un JavaScript permettant de suivre les clics et les transactions qui en résultent.

**Emplacement :** emplacement sur un réseau display dans lequel vos publicités peuvent apparaître. Il peut s’agir d’un site Web entier, d’un sous-ensemble d’un site Web ou d’une position publicitaire sur une page spécifique.

**portefeuille :** ensemble de campagnes publicitaires, et leurs unités d’enchères associées, qui sont optimisées pour un objectif commercial unique et un objectif de performance.

**POS :** pourcentage des dépenses

**PPC :** Voir « paiement par clic ».

**property :** Voir « mesure de conversion ».

**heure de la propriété :** Heure à laquelle un événement de conversion individuel se produit. Lorsqu’un événement comprend des événements de suivi associés (par exemple, lorsqu’un client s’inscrit d’abord pour une version d’essai gratuite, puis s’abonne à un service payant), chaque événement dispose de son propre temps de propriété.

## Q-R {#q-r}

**score de qualité :** Score attribué par un réseau publicitaire à l’un de vos mots-clés afin de déterminer son prix d’offre et sa position publicitaire. Il est calculé en fonction de la pertinence du mot-clé par rapport à l’annonce associée et à la requête de recherche de l’utilisateur ou de l’utilisatrice, du taux de clic publicitaire du mot-clé et d’autres facteurs.

**URL de redirection :** Partie d’une URL de destination qui envoie l’utilisateur vers un autre serveur avant ou à la place de la page de destination de l’annonceur.

**retour sur investissement :** (ROI) Revenus moins coûts.

**précision du chiffre d’affaires :** (Annonceurs avec portefeuilles) Chiffre d’affaires réel d’un portefeuille divisé par le chiffre d’affaires prévu.

**modèle de chiffre d’affaires :** (Annonceurs avec portefeuilles) Technologie de recherche, des réseaux sociaux et du commerce qui prédit le taux de conversion et le retour estimé pour chaque unité d’offre, en fonction des données de clic (recherche et réseaux sociaux) ou des données d’impression (affichage) et des données de conversion de l’annonceur.

**Couverture du modèle de recettes :** (Annonceurs avec portefeuilles) Nombre et/ou pourcentage d’unités d’offre dans un portefeuille avec des modèles de revenus. Les unités d’offre peuvent avoir des modèles de recettes même si elles n’ont pas reçu de recettes mais ont reçu des impressions.

**Demi-vie du modèle de revenus :** (Annonceurs avec portefeuilles) Nombre de jours avant la date actuelle pour lesquels les données de revenus sont considérées comme plus récentes et donc plus pertinentes pour les modèles de revenus.

**ROI :** Voir « retour sur investissement ».

## S-T {#s-t}

**simulation :** (annonceurs avec portefeuilles) Portfolio modélisation qui estime le nombre de clics et de conversions auxquels un portefeuille peut s’attendre pour différents niveaux de dépenses et budgets quotidiens correspondants, en utilisant des données historiques.

**stratégie de dépenses :** (Annonceurs avec portefeuilles) Stratégie sélectionnée pour optimiser les enchères de mots-clés/d’annonces publicitaires pour un portefeuille.

**`s_kwcid`:** Voir « ID AMO ».

**URL de tracking :** Un modèle de tracking ou une URL de destination avec des paramètres supplémentaires ajoutés pour tracker les informations sur les clics sur la publicité. Il peut inclure une URL de redirection permettant d’envoyer les utilisateurs à un serveur de tracking avant de les rediriger vers la page de destination de l’annonceur.

**transaction :** Tout événement pouvant faire l’objet d’un suivi, survenant en ligne ou hors ligne. Plusieurs événements de transaction peuvent être suivis ensemble dans le cadre de la même transaction ou conversion ; par exemple, une demande d&#39;information en ligne ainsi qu&#39;une commande par téléphone qui en résulte peuvent être considérés comme des composants d&#39;un achat. Les termes « transaction » et « conversion » sont souvent utilisés de manière interchangeable. Une transaction est représentée par un ID de transaction et est associée à une ou plusieurs propriétés.

**ID de transaction :** Identifiant spécifié par l’annonceur qui identifie une transaction. Lorsqu’une transaction inclut plusieurs événements, ils ont tous le même ID de transaction.

**propriété de transaction :** Voir « conversion ».

**heure de la transaction :** Heure à laquelle un clic ou une impression est converti en transaction. Lorsqu’une transaction se compose de plusieurs événements de transaction (par exemple, lorsqu’un client s’inscrit pour la première fois à une version d’essai gratuite et s’abonne ensuite à un service payant), le temps de transaction provient du premier événement de la chaîne (l’inscription à la version d’essai gratuite).

**TSV :** Format de fichier composé de valeurs séparées par des tabulations (CSV).

## U-V {#u-v}

**Affichage publicitaire :** (publicités affichées et sociales) Impression publicitaire (ou chaîne d’impressions) qui entraîne une conversion sans que l’utilisateur ne clique sur une publicité.

**Poids d’affichage publicitaire :** (campagnes display et sociales uniquement) paramètre au niveau de l’annonceur qui spécifie le poids à attribuer à une conversion d’affichage publicitaire par rapport au poids attribué à une conversion basée sur les clics, en pourcentage.

## W-X {#w-x}

**Chiffre d’affaires pondéré :** Voir « Valeur objective ».

**XLS** ou **XLSX**: un format de fichier binaire pour [!DNL Microsoft Office Excel] classeurs.

## Y-Z {#y-z}
