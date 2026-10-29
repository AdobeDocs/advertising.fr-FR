---
title: (Nouvelle interface utilisateur) À propos des portefeuilles
description: En savoir plus sur les portefeuilles.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
TQID: 'https://experienceleague.adobe.com/w-NpuD1q3atytkO8AL-ekUWzwhX3NHH-byW9ZIY7WdU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: ebef6e6f-6552-40b6-b842-0c5256698a4e
    internal-label: Predictive modeling
source-git-commit: 700d05fb39b04918ae2662ce24746ed1e84f110e
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%
---
# (Nouvelle interface utilisateur) À propos des portefeuilles

*Fonction*

Vous pouvez gérer vos campagnes publicitaires collectivement à l’aide de portfolios (similaires aux portfolios d’investissement). Un portfolio est un ensemble de campagnes publicitaires ou de jeux de publicités, y compris les mots-clés et les publicités associés, optimisés pour un seul objectif commercial. Un objectif peut inclure plusieurs conversions pondérées et un seul budget ou une seule cible de performance (comme un budget mensuel ou un retour sur investissement cible). Comme les performances des campagnes/ensembles de publicités, mots-clés et publicités peuvent être différentes d’une campagne à l’autre (par exemple, les montants dépensés peuvent varier ou les retour sur investissement peuvent varier), la fonctionnalité d’optimisation utilise des modèles pilotés par l’IA pour orienter l’ensemble du portefeuille afin d’atteindre collectivement la cible. Toutes les campagnes d’un portefeuille utilisent la même devise.

Certains rôles d’utilisateur peuvent créer et configurer des portfolios. Selon le type de portefeuille, les paramètres du portefeuille peuvent inclure l’objectif du portefeuille, les campagnes affectées, la stratégie de dépenses, les contraintes d’offres au niveau du portefeuille, ainsi que les paramètres de modélisation et d’optimisation. Lorsque vous êtes prêt(e) à utiliser Search, Social et Commerce pour commencer l’optimisation d’un portfolio, changez le statut en « optimisé ».

Vous pouvez éventuellement regrouper des portefeuilles en [groupes de portefeuilles](portfolio-group-manage.md) afin de pouvoir afficher des données composites pour l&#39;ensemble du groupe.

En fonction de votre rôle, vous pouvez générer des simulations de performances qui utilisent la modélisation prédictive pour identifier votre point de dépense optimal et des rapports détaillés sur la précision des prévisions.<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## Prise en charge de l’optimisation par stratégie d’enchères {#optimization-by-bid-strategy}

Les campagnes sont éligibles à l’optimisation en fonction de la stratégie d’enchères de la campagne ou du groupe publicitaire.

>[!NOTE]
>
>Les termes « enchère intelligente » et « enchère automatisée » sont souvent utilisés de manière interchangeable, mais ce n&#39;est pas la même chose. Les enchères intelligentes font uniquement référence aux stratégies d’enchères automatisées [!DNL Google Ads] et [!DNL Microsoft Advertising] qui utilisent les enchères au moment des enchères, ce qui signifie que le réseau publicitaire optimise les conversions ou les valeurs de conversion au moment de chaque enchère.

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| Stratégie d’enchères | Enchères intelligentes ? | Enchère Au Niveau Du Mot-Clé/Groupe De Produits ? | Niveau de prise en charge | Type d’objectif | Unité d&#39;enchères | Que définit Adobe ? | Que définit le réseau publicitaire ? |
|---|---|---|---|---|---|---|---|
| CPC manuel (option [!DNL Google Ads] uniquement) | — | Oui | Créer, Modifier, Optimiser | Objectif à propriété unique ou multiple avec n’importe quelle valeur de poids | Mot-clé + Type de correspondance + Campagne | Enchère par mot-clé, budget de campagne, valeurs d’ajustement d’enchère | s.o. |
| ECPC (CPC amélioré) | Oui | Oui | Créer, Modifier, Optimiser | Objectif à propriété unique ou multiple avec n’importe quelle valeur de poids | Mot-clé + Type de correspondance + Campagne | Enchère par mot-clé, budget de la campagne | Ajuste les enchères en temps réel |
| Maximiser les clics [^1] | — | — | Créer, Modifier, Optimiser | Aucune ; optimise vers les clics uniquement | Campagne | Budget de la campagne | Ajuste les enchères en temps réel pour maximiser les clics dans le budget |
| Optimiser les conversions<br>(avec ou sans TCPA) | Oui | — | Créer, Modifier, Optimiser | Objectif à propriété unique avec un poids de 1 | Campagne ou groupe publicitaire ([!DNL Google Ads])<br>Campagne uniquement ([!DNL Microsoft Advertising]) | Budget de la campagne, Coût par acquisition (CPA) cible lorsqu’elle est définie<br>TCPA peut être une stratégie d’enchères autonome en [!DNL Microsoft Advertising]) | Ajuste les enchères en temps réel pour maximiser les commandes/leads dans le budget, atteignant un objectif de CPA lorsque la cible est définie |
| Maximiser la valeur de conversion<br>(avec ou sans TROAS) | Oui | — | Créer, Modifier, Optimiser | Objectif multi-biens avec n’importe quelle valeur de poids, ou objectif mono-bien avec une valeur de poids supérieure à 1 (pour représenter une valeur monétaire) | Campagne ou groupe publicitaire ([!DNL Google Ads])<br>Campagne uniquement ([!DNL Microsoft Advertising]) | Budget de la campagne, retour sur dépenses publicitaires cible lorsqu’il est défini<br>Le retour sur dépenses publicitaires peut être une stratégie d’enchères autonome en [!DNL Microsoft Advertising]) | Ajuste les offres en temps réel pour maximiser les revenus/bénéfices dans le budget, atteignant un objectif de retour sur dépenses publicitaires lorsque la cible est définie |
| Partage d’impression cible | — | — | Créer, Modifier | s.o. | s.o. | s.o. - ne peut pas être affecté à un portefeuille | Ajuste les enchères en temps réel pour atteindre un objectif de partage d’impression |

[^1] : Le paramètre de stratégie d’enchères [!UICONTROL Maximize Clicks] sur le réseau publicitaire n’est pas identique à l’[!UICONTROL Maximize Clicks] d’objectif Rechercher, social et Commerce. Si la stratégie d’enchères est [!UICONTROL Maximize Clicks], vous devez l’affecter uniquement à un portfolio avec optimisation au niveau de la campagne ou du groupe publicitaire, et non à un portfolio avec optimisation au niveau des mots-clés.

## Statuts Portfolio {#portfolio-status}

Un portefeuille peut avoir les statuts suivants :

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## La vue [!UICONTROL Portfolios]

La vue [!UICONTROL Portfolios] répertorie tous les portfolios existants dans la vue filtrée, avec des données de performances personnalisables. Vous pouvez [personnaliser les colonnes de la vue](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) et filtrer les données pour inclure des portfolios spécifiques [à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou de l’en-tête de colonne [&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

### Actions disponibles {#available-actions}

<!-- Update with any new options -->

<!--
 within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

-->

* [Création d’un portfolio](portfolio-create.md)

* [Dupliquer un portfolio](portfolio-duplicate.md)

* Modifier les paramètres :

  * [Renommer un portfolio](portfolio-rename.md)

  * [Modifier les paramètres complets du portfolio](portfolio-edit.md)

  * Modifiez certains paramètres, notamment le statut du portfolio, directement dans la ligne du portfolio.

  * [Modifier en masse les paramètres de portfolio à l’aide de fichiers de feuille d’envoi groupé](portfolio-bulksheets.md)

* Explorez les réseaux publicitaires, les comptes, les campagnes, les groupes publicitaires et les publicités inclus dans le portfolio, et éventuellement explorez les mots-clés d’une campagne incluse. Pour commencer, cliquez sur le nom du portfolio. Les informations sont d’abord répertoriées par réseau publicitaire dans la vue [!UICONTROL Networks] filtrée. Cliquez sur un réseau publicitaire pour afficher les comptes inclus dans la vue [!UICONTROL Accounts] filtrée, cliquez sur un compte pour afficher les campagnes dans la vue [!UICONTROL Campaigns] filtrée, etc.

  Pour ouvrir une liste des mots-clés dans la vue [!UICONTROL Keywords] à partir de la vue [!UICONTROL Campaigns] filtrée, cliquez sur la valeur dans la colonne [!UICONTROL Keywords] .

* Ouvrez une liste de toutes les contraintes du portefeuille, y compris le niveau et le type de contrainte. Pour afficher la liste des contraintes, cliquez sur [!UICONTROL Yes] dans la colonne [!UICONTROL Constraints] . Cette option est disponible lorsqu&#39;un portefeuille ou ses campagnes associées et entités de campagne enfant sont configurés avec des contraintes qui affectent les dépenses (notamment les contraintes de réseau, de budget de campagne, de cible, de CPC ou d&#39;unité d&#39;enchères).

* [Afficher un graphique des performances pour tous les portefeuilles dans la vue](portfolio-view-performance-graph.md)

* [Affichage des détails sur les performances du portefeuille](portfolio-details.md)

* [Afficher l&#39;historique des modifications d&#39;un portefeuille](portfolio-view-change-history.md)

* [Télécharger les données dans la vue [!UICONTROL Portfolios]](portfolio-view-report.md)

* [Ajouter un portefeuille à un groupe de portefeuilles et gérer les groupes de portefeuilles](portfolio-group-manage.md)

>[!MORELIKETHIS]
>
>* [Créer un portfolio](portfolio-create.md)
>* [Dupliquer un portfolio](portfolio-duplicate.md)
>* [Modifier un portfolio](portfolio-edit.md)
>* [Gérer les rapports de vue de données à partir de la vue [!UICONTROL Portfolios]](portfolio-view-report.md)
