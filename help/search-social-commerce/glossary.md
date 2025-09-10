---
title: Glossaire
description: Voir les définitions des termes clés.
exl-id: 87ce61b5-8340-4a6b-bd98-89ef73b2a9d8
feature: Search Introduction
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '2308'
ht-degree: 0%

---

# Glossaire {#glossary}

## A-B {#a-b}

**groupe publicitaire :** ensemble d’annonces et leurs mots-clés, emplacements et groupes de produits associés pour une campagne.

**variation publicitaire :** toute publicité au sein d’un groupe publicitaire ou d’une stratégie publicitaire.

**[AMO ID](/help/integrations/analytics/ids.md#amo-id) :** code de suivi qui permet à Adobe Advertising de partager des données sur les campagnes avec Adobe Analytics et Adobe Customer Journey Analytics. Cela commence par la `s_kwcid=`.

**unité d’enchère :** terme Search, Social et Commerce désignant l’unité sur laquelle les enchères sont placées.

* Pour les campagnes CPC, il s’agit d’un mot-clé et de son type de correspondance pour une campagne de recherche ou de contenu, un groupe de produits au niveau de l’unité (niveau de subdivision le plus bas) pour une campagne d’achat ou une cible de recherche dynamique pour une campagne publicitaire de recherche dynamique. Lorsque la même combinaison de mot-clé et de type de correspondance, le même groupe de produits ou la même cible de recherche dynamique se produit au sein de plusieurs groupes publicitaires dans une seule campagne, toutes les instances sont considérées comme la même unité d’enchères et ont donc la même enchère.

* Pour les campagnes avec les stratégies de dépenses [!DNL Maximize Clicks], [!DNL Maximize Conversion Value], [!DNL Maximize Conversions], [!DNL Target Cost Per Acquisition] ou [!DNL Target Return on Ad Spend], chaque campagne est une unité d’enchères.

* Pour les campagnes sur [!DNL Yahoo! Display Network], qui n’utilisent pas de mots-clés, toutes les annonces d’un groupe publicitaire ont la même enchère et sont considérées comme la même unité d’enchère.

**contrainte d’unité d’offre :** voir « contrainte ».

## C-D {#c-d}

**campagne :** ensemble de groupes publicitaires dans un compte publicitaire unique qui partagent un budget, une période, un ciblage et d’autres paramètres. **Remarque :** [!DNL Baidu] n’utilise pas le concept de campagnes, mais Search, Social et Commerce crée des pseudo-campagnes pour chaque ensemble de groupes publicitaires associés dans les comptes [!DNL Baidu] existants synchronisés dans Search, Social et Commerce.

**champ sensible à la casse :** un champ ou une requête sensible à la casse traite les lettres majuscules (C par exemple) différemment des lettres minuscules (C par exemple). Par exemple, la voiture est traitée comme une valeur différente de la voiture.

**click :** un seul utilisateur clique sur ou dans une annonce en ligne.

**intervalle de recherche en amont des clics :** paramètre au niveau de l’annonceur qui spécifie le nombre de jours après un clic payant dans une série d’événements au cours desquels le clic peut être attribué à une conversion.

**heure de clic :** heure à laquelle un utilisateur final disposant d’une adresse IP unique clique pour la première fois sur une publicité dans le réseau publicitaire.

**taux de clic publicitaire :** (CTR) nombre de clics divisé par le nombre d’impressions sur une annonce publicitaire. Les publicités les plus pertinentes pour la requête de recherche présentent les taux de clic publicitaire les plus élevés.

**URL de suivi des clics :** un modèle de suivi ou une URL de destination avec code incorporé pour effectuer le suivi des clics sur un mot-clé, une variation d’annonce publicitaire ou un emplacement.

**contrainte :** (annonceurs avec portefeuilles ; applicable aux unités d’offre dans les portefeuilles standard uniquement) Règle permettant d’enchérir sur un mot-clé ou une annonce publicitaire spécifique. Il remplace toute limite au niveau du portefeuille et la stratégie d’enchères recommandée.

**conversion :** réalisation d’une action après qu’un utilisateur final ou une utilisatrice finale a cliqué sur une annonce, généralement capturée sous la forme d’une mesure. Par exemple, les enregistrements et les achats, et ils peuvent représenter des décomptes ou des montants monétaires. Une conversion peut consister en un ou plusieurs événements de transaction, mais les termes « conversion » et « transaction » sont souvent utilisés de manière interchangeable.

**suivi des conversions :** le suivi des conversions utilise des cookies pour suivre a) les clics sur les publicités d’un annonceur sur les réseaux publicitaires et b) les transactions résultantes sur le site web de l’annonceur.

**exactitude des coûts :** (annonceurs avec portefeuilles) dépenses réelles pour un portefeuille divisées par les dépenses prévues. [Rapports sur la précision des modèles](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indiquez la précision des modèles de coûts utilisés pour l’optimisation. L’[[!UICONTROL Model Accuracy]insight](/help/search-social-commerce/advertising-insights/insight-about.md) inclut des détails supplémentaires, en plus de recommandations pour améliorer la précision des modèles.

**modèle de coût :** (annonceurs avec portefeuilles) technologie Search, Social et Commerce qui prédit le volume des coûts, l’offre requise pour remporter chaque poste ou emplacement et le CPC (recherche) ou le CPM (affichage) pour chaque unité d’offre à l’aide de données historiques et de techniques de prévision mathématique.

**couverture du modèle de coût :** (annonceurs avec portefeuilles) nombre et/ou pourcentage d’unités d’offre dans les campagnes CPC ou eCPC qui ont reçu au moins une impression au cours des sept derniers jours afin que la fonctionnalité d’optimisation puisse créer des modèles de coût. Toutes les unités d’offre n’ont pas de modèle de coût ; les unités d’offre avec modèle de coût sont prises en compte dans la couverture du modèle de coût.

**demi-vie du modèle de coût :** (annonceurs avec portefeuilles) nombre de jours avant la date actuelle pour lequel les données de coût sont considérées comme plus récentes et donc plus pertinentes pour les modèles de coût.

**coût par 1 000 impressions :** (CPM) coût d’une annonce publicitaire pour mille impressions. Les annonceurs qui utilisent un modèle de tarification CPM paient par impressions plutôt que par clics.

**coût par acquisition :** (CPA) coût d’une annonce publicitaire divisé par le nombre de conversions. Également appelé coût par transaction (CPT) ou coût par commande (CPO).

**coût par clic :** (CPC) 1) Coût d’une publicité divisé par le nombre total de clics effectués pour cette publicité. Par exemple, si vous dépensez 100 USD pour une impression d’annonce et que l’annonce génère 10 clics, le coût par clic est de 100 USD/10=10 USD par clic. 2) Un modèle de tarification dans lequel les annonceurs sont facturés pour chaque clic publicitaire.

**coût par commande :** (CPO) coût d’une annonce publicitaire divisé par le nombre de commandes. Également appelé coût par acquisition (CPA) ou coût par transaction (CPT).

**coût par transaction :** (CPT) coût d’une annonce publicitaire divisé par le nombre de transactions. Également appelé coût par acquisition (CPA).

**CPA :** voir « coût par acquisition ».

**CPC :** voir « Coût par clic ».

**CPM :** voir « coût par 1 000 impressions ».

**CPO :** voir « coût par commande ».

**CPT:** Voir « coût par transaction ».

**CSV:** Format de fichier constitué de valeurs séparées par des virgules (CSV).

**CTR :** voir « Taux de clic publicitaire ».

## E-F {#e-f}

**eCPM:** CPM effective ou coût moyen payé pour 1 000 impressions au cours d’une période spécifiée. Les valeurs eCPM peuvent être calculées pour des campagnes CPM ou CPC.

## G-H {#g-h}

**demi-vie :** temps nécessaire pour qu’une grandeur diminue de moitié par rapport à sa valeur initiale. Pour chaque portefeuille, vous pouvez spécifier des demi-vies afin d’indiquer la durée pendant laquelle les données sont pertinentes pour les modèles de coûts et les modèles de chiffre d’affaires.
Voir « demi-vie du modèle de coût » et « demi-vie du modèle de revenu ».

## I-J {#i-j}

**impression :** affichage unique d’une annonce publicitaire sur une page web, une application mobile ou un autre support de diffusion. Il n’est pas nécessaire d’afficher ou de cliquer sur l’annonce publicitaire pour qu’elle soit comptabilisée comme une impression.

**intervalle de recherche en amont d’impression :** (affichage et campagnes sociales uniquement) paramètre au niveau de l’annonceur qui spécifie le nombre de jours après la survenue d’une impression publicitaire que l’impression peut être attribuée à une conversion.

**poids de remplacement d’impression :** pourcentage spécifié d’une valeur de conversion à attribuer aux impressions qui se produisent dans l’intervalle de recherche en amont d’impression du client lorsque la conversion est précédée à la fois de clics payants et d’impressions. Lorsqu’une conversion n’est précédée que d’impressions, le poids de visualisation de l’annonceur, plutôt que le poids de remplacement de l’impression, est appliqué aux impressions.

## K-L {#k-l}

**mot-clé :** mot ou expression associé à une publicité.

**contrainte de mot-clé :** voir « contrainte ».

**classification de libellés :** moyen de regrouper les composants de votre compte en ensembles significatifs. Une classification de libellés peut contenir plusieurs valeurs de libellé, qui indiquent des attributs. Par exemple, une classification de libellé « Géographique » peut inclure des valeurs pour différentes régions géographiques.

**valeur du libellé :** élément d’une classification de libellé. Elle peut être affectée en tant que balise aux campagnes publicitaires et aux entités de campagne afin que vous puissiez filtrer les données et les rapports de performances par libellé ou configurer des contraintes facultatives sur les unités d’enchères associées au libellé.

**URL de la page de destination :** URL de la page web de l’annonceur qui s’ouvre lorsque l’utilisateur final clique sur une publicité.

## M-N {#m-n}

**coût marginal :** variation du coût total lorsque la quantité change d&#39;une unité.

**coût marginal par rapport à l’objectif :** changement de coût nécessaire pour augmenter la valeur de l’objectif de un (1). Celui-ci a la même valeur que la colonne héritée « Coût par rapport au chiffre d’affaires marginal ».

**type de correspondance :** option qui spécifie la manière dont les termes de recherche sont associés aux annonces. Les options varient en fonction du réseau publicitaire.

**enchère minimum :** 1) Montant minimum à payer par impression ou par 1000 impressions. 2) Pour les mots-clés de recherche, enchère minimale requise pour un mot-clé donné en fonction de son score de qualité. L&#39;enchère minimale est généralement le montant minimum que vous pouvez payer par clic pour que votre mot-clé affiche des annonces.

**précision du modèle :** (annonceurs avec des portefeuilles) pourcentage de précision des modèles de coûts et des modèles de chiffre d’affaires utilisés pour optimiser les offres, les budgets de campagne et les cibles de stratégie d’enchères pour un portefeuille. Voir « modèle de coût », « précision des coûts », « modèle de revenu » et « précision du revenu ».

## O-P {#o-p}

**objectif :** (annonceurs avec des portefeuilles). Objectif qu’un client définit pour atteindre son objectif commercial pour un portefeuille spécifique ou une campagne d’affichage, par exemple pour maximiser les bénéfices ou pour atteindre une cible de vente spécifique. Un objectif se compose des mesures de conversion à suivre et à optimiser pour le portefeuille, ainsi que des poids relatifs de ces mesures. Les conversions pondérées totales pour le portefeuille sont calculées et sont appelées la « valeur objective ».

**valeur de l’objectif :** (annonceurs avec portefeuilles) conversions totales pondérées calculées en fonction de l’objectif actuel du portefeuille, y compris :

* toutes les conversions, en tenant compte a) du poids attribué à chaque conversion dans l&#39;objectif du portefeuille et, le cas échéant, b) du poids de visualisation pour les visualisations d&#39;affichage.

* tous les clics, que la fonctionnalité d’optimisation considère comme une seule conversion et est pondérée en fonction de la valeur de clic de l’objectif.

Elle a la même valeur que la colonne héritée « Revenus pondérés ».

**fonctionnalité d’optimisation :** (annonceurs avec portefeuilles) technologie d’enchères par mot-clé Search, Social et Commerce, qui détermine la stratégie d’enchères et de gestion budgétaire optimale pour un portefeuille en fonction de son objectif commercial.

**transaction orpheline :** événement de transaction qui ne peut pas être associé à un mot-clé ou à une annonce publicitaire spécifique.

**pixel :** image transparente, pixel par pixel incorporée sur une page web à des fins de suivi. Les balises de suivi des conversions Adobe Advertising incluent un pixel d’image HTML ou JavaScript pour effectuer le suivi des clics et des transactions résultantes.

**emplacement :** emplacement sur un réseau d’affichage dans lequel vos publicités peuvent apparaître. Il peut s’agir d’un site web entier, d’un sous-ensemble d’un site web ou d’une position d’annonce sur une page spécifique.

**portfolio :** ensemble de campagnes publicitaires, et les unités d’enchères associées, optimisées pour un seul objectif commercial et une cible de performances.

**POS:** pourcentage des dépenses

**PPC :** voir « paiement par clic ».

**property :** voir « mesure de conversion ».

**property time:** Heure à laquelle un événement de conversion individuel se produit. Lorsqu’un événement comprend des événements de suivi associés (par exemple, lorsqu’un client s’inscrit d’abord pour une version d’essai gratuite, puis s’abonne à un service payant), chaque événement dispose de son propre temps de propriété.

## Q-R {#q-r}

**score de qualité :** score qu’un réseau publicitaire attribue à l’un de vos mots-clés pour déterminer son prix d’offre et sa position publicitaire. Il est calculé en fonction de la pertinence du mot-clé par rapport à l’annonce associée et à la requête de recherche de l’utilisateur ou de l’utilisatrice, du taux de clic publicitaire du mot-clé et d’autres facteurs.

**URL de redirection :** partie d’une URL de destination qui envoie l’utilisateur vers un autre serveur avant ou à la place de la page de destination de l’annonceur.

**retour sur investissement :** (ROI) Revenus moins coûts.

**exactitude du chiffre d’affaires :** (annonceurs avec portefeuilles) chiffre d’affaires réel d’un portefeuille divisé par le chiffre d’affaires prévu. [Rapports sur la précision des modèles](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indiquez la précision des modèles de chiffre d’affaires utilisés pour l’optimisation. L’[[!UICONTROL Model Accuracy]insight](/help/search-social-commerce/advertising-insights/insight-about.md) comprend plus de détails, en plus de recommandations pour améliorer la précision des modèles.

**modèle de chiffre d’affaires :** (annonceurs avec portefeuilles) technologie Search, Social et Commerce qui prédit le taux de conversion et le retour estimé pour chaque unité d’enchère, en fonction des données de clic (recherche et réseaux sociaux) ou des données d’impression (affichage) et des données de conversion de l’annonceur.

**couverture du modèle de chiffre d’affaires :** (annonceurs avec portefeuilles) nombre et/ou pourcentage d’unités d’enchères dans un portefeuille avec des modèles de chiffre d’affaires. Les unités d&#39;enchères peuvent avoir des modèles de chiffre d&#39;affaires même si elles n&#39;ont pas reçu de chiffre d&#39;affaires mais ont reçu des impressions.

**demi-vie du modèle de chiffre d’affaires :** (annonceurs avec portefeuilles) nombre de jours avant la date actuelle pour lequel les données de chiffre d’affaires sont considérées comme plus récentes et donc plus pertinentes pour les modèles de chiffre d’affaires.

**ROI :** voir « retour sur investissement ».

## S-T {#s-t}

**simulation:** (annonceurs avec portefeuilles) : modélisation Portfolio qui estime le nombre de clics et de conversions qu’un portefeuille peut attendre pour différents niveaux de dépenses et budgets quotidiens correspondants, à l’aide de données historiques.

**stratégie de dépenses :** (annonceurs avec portefeuilles) stratégie sélectionnée pour optimiser les enchères de mot-clé/publicité pour un portefeuille.

**`s_kwcid`:** voir « AMO ID ».

**modèle de tracking :** (Comptes avec URL finales uniquement) Le modèle de tracking ou l’URL de tracking, qui spécifie toutes les redirections de domaine et tous les paramètres de tracking hors atterrissage et incorpore l’URL finale/avancée dans un paramètre. Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement un préfixe à son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

**URL de tracking :** un modèle de tracking ou une URL de destination avec des paramètres supplémentaires ajoutés pour tracker les informations sur les clics sur l’annonce publicitaire. Il peut inclure une URL de redirection permettant d’envoyer les utilisateurs à un serveur de tracking avant de les rediriger vers la page de destination de l’annonceur.

**transaction :** tout événement pouvant faire l’objet d’un suivi, en ligne ou hors ligne. Plusieurs événements de transaction peuvent être suivis ensemble dans le cadre de la même transaction ou conversion ; par exemple, une demande d&#39;information en ligne ainsi qu&#39;une commande par téléphone qui en résulte peuvent être considérés comme des composants d&#39;un achat. Les termes « transaction » et « conversion » sont souvent utilisés de manière interchangeable. Une transaction est représentée par un ID de transaction et est associée à une ou plusieurs propriétés.

**ID de transaction :** ID spécifié par l’annonceur qui identifie une transaction. Lorsqu’une transaction inclut plusieurs événements, ils ont tous le même ID de transaction.

**propriété transaction :** voir « conversion ».

**heure de transaction :** heure à laquelle un clic ou une impression est converti en transaction. Lorsqu’une transaction se compose de plusieurs événements de transaction (par exemple, lorsqu’un client s’inscrit pour la première fois à une version d’essai gratuite et s’abonne ensuite à un service payant), le temps de transaction provient du premier événement de la chaîne (l’inscription à la version d’essai gratuite).

**TSV:** Format de fichier constitué de valeurs séparées par des tabulations (CSV).

## U-V {#u-v}

**affichage publicitaire :** (affichage et publicités sociales) impression d’annonce (ou chaîne d’impressions) qui entraîne une conversion sans que l’utilisateur clique sur une annonce.

**poids des affichages publicitaires :** (affichage et campagnes sociales uniquement) paramètre au niveau de l’annonceur qui spécifie le poids à attribuer à une conversion d’affichage publicitaire par rapport au poids attribué à une conversion basée sur les clics, en pourcentage.

## W-X {#w-x}

**objectif pondéré :** voir « objectif ».

**revenus pondérés** Voir « valeur objective ».

**XLS** ou **XLSX** : format de fichier binaire pour les classeurs [!DNL Microsoft Office Excel].

## Y-Z {#y-z}
