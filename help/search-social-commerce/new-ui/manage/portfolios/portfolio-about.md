---
title: (Nouvelle interface utilisateur) À propos des portefeuilles
description: En savoir plus sur les portefeuilles.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
source-git-commit: de3c527bd359e0d5285b90e54278983104a2a5b5
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) À propos des portefeuilles

*Fonction Beta*

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

La vue [!UICONTROL Portfolios] répertorie vos portefeuilles existants, avec des données de performances personnalisables. Vous pouvez [personnaliser les colonnes de la vue](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) et filtrer les données pour inclure des portfolios spécifiques [à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou de l’en-tête de colonne [](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

Au-dessus du tableau de données, vous pouvez ouvrir un graphique de performances avec jusqu’à trois mesures totalisées pour tous les portefeuilles dans la vue pour la période spécifiée.

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### Actions disponibles

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [Création d’un portfolio](portfolio-create.md)

* [Dupliquer un portfolio](portfolio-duplicate.md)

* [Modifier les paramètres du portfolio](portfolio-edit.md)

* [Modifier en masse les paramètres de portfolio à l’aide de fichiers de feuille d’envoi groupé](portfolio-bulksheets.md)

* [Afficher un graphique des performances pour tous les portefeuilles dans la vue](portfolio-view-performance-graph.md)

* [Affichage des détails sur les performances du portefeuille](portfolio-details.md)

* [Télécharger les données dans la vue [!UICONTROL Portfolios]](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [Créer un portfolio](portfolio-create.md)
>* [Dupliquer un portfolio](portfolio-duplicate.md)
>* [Modifier un portfolio](portfolio-edit.md)
>* [Gérer les rapports de vue de données à partir de la vue [!UICONTROL Portfolios]](portfolio-view-report.md)
