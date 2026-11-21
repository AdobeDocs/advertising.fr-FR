---
title: (Nouvelle interface utilisateur) Informations sur Advertising
description: Découvrez comment configurer et afficher les tableaux de bord Advertising insight pour la précision des modèles, les performances, les simulations, les limites de budget et les conversions.
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%
---
# (Nouvelle interface utilisateur) Informations sur Advertising

Les informations d’Advertising présentent des données visuelles exploitables pour vous aider à évaluer les performances du portfolio, à identifier les problèmes d’optimisation et à comparer les données de conversion. Chaque insight est généré à la demande et affiché sous la forme d’un tableau de bord à l’écran.

La vue **[!UICONTROL Reports]>[!UICONTROL Insights]** affiche les informations disponibles sous **[!UICONTROL Dashboards]**. L&#39;en-tête de la page est **[!UICONTROL Advertising Insights]**.

>[!NOTE]
>
>Cette page décrit les tableaux de bord insight dans la nouvelle interface utilisateur de la version bêta. La disponibilité dépend de votre accès et des informations disponibles pour l’annonceur sélectionné. Les [insights Advertising hérités](/help/search-social-commerce/legacy-ui/advertising-insights/insight-about.md) incluent un ensemble différent d’analyses et de procédures pour les fichiers générés.

## Types d’informations {#insight-types}

| Insight | Description |
| --- | --- |
| [!UICONTROL Model Accuracy] | Détermine dans quelle mesure Search, Social et Commerce prévoient le coût et le chiffre d’affaires d’un portefeuille. Vous pouvez vérifier la précision du modèle au niveau du portefeuille, du réseau publicitaire et de la campagne. |
| [!UICONTROL Performance Insights] | Compare les performances du portefeuille avant et après un changement de statut d&#39;optimisation, un changement d&#39;objectif ou une date spécifiée. Le tableau de bord comprend des résumés des performances, un audit des modifications affectant l’optimisation, des comparaisons de campagnes, des tendances et une analyse des valeurs objectives. |
| [!UICONTROL Portfolio Simulation Analysis] | Compare une simulation personnalisée existante aux performances réelles. Vous pouvez examiner les données de portfolio et de campagne, analyser la précision de la simulation et explorer les performances estimées à différents niveaux de dépenses cibles. |
| [!UICONTROL Campaign Budget Cap Analysis] | Indique si les dépenses d&#39;un portefeuille ont été limitées par les plafonds budgétaires de la campagne. Le tableau de bord comprend les dépenses plafonnées, les campagnes affectées, les impressions perdues estimées, les tendances quotidiennes et quotidiennes, ainsi que des recommandations pour les paramètres du portfolio. |
| [!UICONTROL Modeled Conversions] | Compare les valeurs de conversion d’Adobe aux valeurs signalées par le réseau publicitaire, y compris les données modélisées. Vous pouvez analyser les comptes, les portfolios ou les campagnes et comparer les valeurs mesurées et modélisées par Adobe et celles mesurées et modélisées par Adobe aux valeurs rapportées par l’éditeur. |
| [!UICONTROL Delayed Revenue Analysis] | Mesure le délai de conversion (temps écoulé entre un clic publicitaire ou une visualisation et une conversion ultérieure) et indique son impact sur la valeur objective, le retour sur investissement (ROI) et la précision du modèle. L’analyse est disponible uniquement pour les portefeuilles avec attribution de chiffre d’affaires basée sur les clics ou sur les vues. |

## Générer une insight {#insight-generate}

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Insights]**.

1. Cliquez sur l’insight à générer.

1. Dans le panneau **[!UICONTROL Configure]**, spécifiez les [paramètres insight](#insight-settings).

1. Cliquez sur **[!UICONTROL Generate Insight]**.

   Le panneau de configuration se ferme et le tableau de bord affiche l’analyse.

1. Examinez les [résultats insight](#insight-results).

Pour modifier les paramètres, cliquez sur **[!UICONTROL Configure]**, modifiez les valeurs, puis cliquez de nouveau sur **[!UICONTROL Generate Insight]**. Pour revenir à la liste insight, cliquez sur **[!UICONTROL Analysis List]** dans le chemin de navigation.

## Paramètres d’Insight {#insight-settings}

### Précision du modèle {#model-accuracy-settings}

* **[!UICONTROL Portfolios]:** sélectionnez un portefeuille.

* **[!UICONTROL Choose Revenue Type]:** sélectionnez **[!UICONTROL Actual Revenue]** (valeur par défaut) ou **[!UICONTROL Delayed Revenue]**.

* **[!UICONTROL Date Range]:** Sélectionnez les dates à analyser. Voir [Paramètres des périodes](#date-range-settings).

### Informations sur les performances {#performance-insights-settings}

* **[!UICONTROL Portfolios]:** sélectionnez un portefeuille.

* **[!UICONTROL Revenue Type]:** sélectionnez **[!UICONTROL Actual Revenue]** (valeur par défaut) ou **[!UICONTROL Delayed Revenue]**.

* **Date de l’événement :** Sélectionnez le type de date autour de laquelle comparer les performances :

  * **[!UICONTROL Optimization Status Change (last 90 days)]** (valeur par défaut) : sélectionnez une date de modification de l’état d’optimisation disponible pour le portfolio.

  * **[!UICONTROL Objective Change Date (last 90 days)]:** Sélectionnez une date de modification d’objectif disponible pour le portefeuille.

  * **[!UICONTROL Specific Date]:** Spécifiez une date à l’aide du sélecteur de date.

  Sélectionnez la date de l’événement avant de configurer les périodes de comparaison. Si aucune date d’événement n’est disponible pour le portfolio sélectionné, vous pouvez utiliser **[!UICONTROL Specific Date]**.

* **[!UICONTROL Pre Days]:** Spécifiez la période précédant la date de l’événement :

  * Sélectionnez **[!UICONTROL 7]** (valeur par défaut), **[!UICONTROL 14]** ou **[!UICONTROL 30]**.

  * Sélectionnez **[!UICONTROL Pre Start Date]** et spécifiez **[!UICONTROL Custom Pre Date]**.

  * Sélectionnez **[!UICONTROL Custom Pre Days]** et saisissez un nombre de jours positif.

* **[!UICONTROL Post Days]:** Spécifiez la période postérieure à la date de l’événement :

  * Sélectionnez **[!UICONTROL 7]** (valeur par défaut), **[!UICONTROL 14]** ou **[!UICONTROL 30]**.

  * Sélectionnez **[!UICONTROL Post End Date]** et spécifiez **[!UICONTROL Custom Post Date]**.

  * Sélectionnez **[!UICONTROL Custom Post Days]** et saisissez un nombre de jours positif.

  La date de l’événement elle-même n’est incluse dans aucune des périodes de comparaison.

* **[!UICONTROL Date Exclusion]:** (facultatif) Excluez les dates de l’analyse :

  1. Cliquez sur **[!UICONTROL Select Dates]**.

  1. Sélectionnez les dates à exclure :

     * Cliquez sur des dates individuelles pour les sélectionner ou les désélectionner.

     * Maintenez la touche **[!UICONTROL Shift]** enfoncée tout en cliquant pour sélectionner une plage.

     * Pour supprimer toutes les exclusions, cliquez sur **[!UICONTROL Clear All]**.

  1. Cliquez sur **[!UICONTROL Done]** lorsque vous avez terminé.

### Analyse de la simulation Portfolio {#simulation-settings}

* **[!UICONTROL Portfolios]:** Sélectionnez un portfolio avec une simulation personnalisée existante.

* **[!UICONTROL Simulation Date]:** Sélectionnez la date de la simulation à analyser. Si plusieurs simulations sont disponibles pour cette date, sélectionnez également la simulation par nom.

  Si aucune simulation personnalisée n’est disponible, [générez une simulation personnalisée](/help/search-social-commerce/manage/portfolios/portfolio-create-simulation.md) avant d’utiliser cette insight.

* **[!UICONTROL Actual Days]:** sélectionnez **[!UICONTROL 7]** (valeur par défaut), **[!UICONTROL 14]** ou **[!UICONTROL 30]** jours de données de performances réelles. Pour spécifier un autre nombre, sélectionnez **[!UICONTROL Enter Actual Days]** et saisissez une valeur comprise entre 1 et 90.

* **[!UICONTROL Type]:** sélectionnez **[!UICONTROL Transaction Date]** (valeur par défaut) ou **[!UICONTROL Click Date]** pour l’attribution de conversion.

### Analyse des limites budgétaires de la campagne {#budget-cap-settings}

* **[!UICONTROL Portfolio]:** sélectionnez un portefeuille.

* **[!UICONTROL Date Range]:** Sélectionnez les dates à analyser. Voir [Paramètres des périodes](#date-range-settings).

### Conversions Modélisées {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]:** sélectionnez **[!UICONTROL Account]**, **[!UICONTROL Portfolio]** (valeur par défaut) ou **[!UICONTROL Campaign]**.

* **[!UICONTROL Accounts]**, **[!UICONTROL Portfolios]** ou **[!UICONTROL Campaigns]:** sélectionnez les entités applicables pour le niveau d’analyse. Vous pouvez sélectionner plusieurs entités.

* **[!UICONTROL Date Range]:** Sélectionnez les dates à analyser. Voir [Paramètres des périodes](#date-range-settings).

* **[!UICONTROL Adobe Conversion]:** Sélectionnez la propriété de conversion Adobe à comparer.

* **[!UICONTROL Publisher Conversion]:** Sélectionnez la propriété de conversion de l’éditeur à comparer.

  Les propriétés de conversion disponibles dépendent du niveau d’analyse, des entités sélectionnées et de la période. Les deux propriétés de conversion sont requises pour la comparaison.

### Analyse des revenus différés {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]:** sélectionnez un portefeuille avec attribution de chiffre d’affaires basée sur les clics ou l’affichage publicitaire.

* **[!UICONTROL Date Range]:** Sélectionnez les dates à analyser. Voir [Paramètres des périodes](#date-range-settings).

### Paramètres des périodes {#date-range-settings}

Pour obtenir des informations avec un paramètre **[!UICONTROL Date Range]**, sélectionnez **[!UICONTROL Last 7 days]** (valeur par défaut), **[!UICONTROL Last 14 days]** ou **[!UICONTROL Last 30 days]**.

Pour spécifier une autre période, sélectionnez **[!UICONTROL Custom Date]** et saisissez **[!UICONTROL Start Date]** et **[!UICONTROL End Date]**. Vous pouvez sélectionner des dates comprises dans les 90 derniers jours, jusqu’à la date actuelle.

## Affichage des résultats d’insight {#insight-results}

### Précision du modèle {#model-accuracy-results}

Passez en revue les détails du portefeuille et utilisez les onglets suivants :

* **[!UICONTROL Portfolio]:** Examinez la précision du modèle au niveau du portefeuille et les comparaisons de budgets.

* **[!UICONTROL Ad Network]:** Examinez la précision du modèle et les comparaisons de budgets par réseau publicitaire.

* **[!UICONTROL Campaigns]:** vérifiez la précision du modèle au niveau de la campagne et la cible par rapport aux performances réelles.

* **[!UICONTROL Playground Beta]:** comparez la précision du modèle pour plusieurs campagnes.

Pour les graphiques de précision de campagne, sélectionnez les valeurs **[!UICONTROL Comparison Options]** et **[!UICONTROL Campaign]**. Dans **[!UICONTROL Playground Beta]**, vous pouvez sélectionner plusieurs campagnes. Cliquez sur **[!UICONTROL Table View]** pour basculer entre un graphique et ses données sous-jacentes.

### Informations sur les performances {#performance-insights-results}

Le tableau de bord affiche les **[!UICONTROL Pre Period]** et **[!UICONTROL Post Period]**, les mesures de performances agrégées pour les deux périodes, ainsi que les détails du portefeuille.

Le **[!UICONTROL Audit Trail]** résume les modifications apportées aux facteurs affectant l’optimisation, notamment le budget du portefeuille, la stratégie de dépenses, les dépenses de campagne minimales et les limites de dépenses multiples. Lorsque des détails sont disponibles pour les modifications, cliquez sur **[!UICONTROL View Details]** pour les examiner.

Utilisez les onglets **[!UICONTROL Comparative Overview]**, **[!UICONTROL Campaigns Comparison]**, **[!UICONTROL Trends & Patterns]**, **[!UICONTROL Deep Analysis]** et **[!UICONTROL Objective Value And Analysis]** pour explorer la comparaison.

### Analyse de la simulation Portfolio {#simulation-results}

Passez en revue les détails de la simulation et utilisez les onglets suivants :

* **[!UICONTROL Portfolio]:** examinez les données de simulation au niveau du portfolio. Dans cet onglet :

  * **[!UICONTROL Simulation Data]** affiche les mesures de simulation et les performances des dépenses cibles.

  * **[!UICONTROL Simulation Vs Actual]** compare les performances simulées et réelles.

  * **[!UICONTROL Try New Target]** vous permet de saisir une dépense cible dans **[!UICONTROL Explore Target Spend]** pour afficher une estimation des clics, des coûts et du chiffre d’affaires. Il s&#39;agit d&#39;une analyse du rendement estimatif ; cela ne modifie pas l&#39;objectif de dépenses du portefeuille.

* **[!UICONTROL Campaigns]:** passez en revue les comparaisons de simulation au niveau de la campagne.

* **[!UICONTROL Accuracy Analysis]:** Vérifier la précision de la simulation.

### Analyse des limites budgétaires de la campagne {#budget-cap-results}

Examinez les détails du portefeuille et les mesures récapitulatives :

* **[!UICONTROL Total Capped Spend]:** Pourcentage des dépenses sur les jours où les budgets de campagne ont été atteints.

* **[!UICONTROL Capped Campaigns]:** Nombre de campagnes qui ont atteint leur budget au moins une fois.

* **[!UICONTROL Est. Lost Impressions]:** impressions estimées manquantes en raison des limites de budget.

* **[!UICONTROL Peak Capping Day]:** jour de la semaine où les dépenses sont les plus plafonnées.

Les graphiques **[!UICONTROL Spend on Capped Campaigns by Day]** et **[!UICONTROL Capped Spend by Weekday]** affichent des tendances de limitation. Vérifiez **[!UICONTROL Capped Campaign Performance]** pour les détails de la campagne et **[!UICONTROL Portfolio Settings Recommendations]** pour les modifications de paramètres suggérées.

### Conversions Modélisées {#modeled-conversions-results}

Consultez les tableaux suivants pour les entités et la période sélectionnées :

* **[!UICONTROL Adobe Measured vs Publisher Conversions]:** compare les valeurs de conversion mesurées directement par Adobe avec les valeurs rapportées par l’éditeur, qui incluent les données mesurées et modélisées.

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]:** compare les valeurs de conversion mesurées et modélisées par Adobe aux valeurs signalées par l’éditeur.

Les deux tableaux incluent le nom et l’ID de l’entité, la valeur d’Adobe, la valeur signalée par l’éditeur, la différence absolue et la différence en pourcentage.

Si aucune donnée n’est disponible, vérifiez que vous avez sélectionné les deux propriétés de conversion et que les données existent pour les entités et la période sélectionnées.

### Analyse des revenus différés {#delayed-revenue-results}

Le **[!UICONTROL Key Insights Summary]** affiche le chiffre d’affaires pondéré attendu (désormais appelé « [valeur d’objectif](/help/search-social-commerce/glossary.md#o-p) »), le retour sur investissement et les informations sur la précision du modèle.

La section **[!UICONTROL Conversion Lag Breakdown by Revenue Property]** indique le pourcentage de conversions réalisées au jour 0 et aux jours 3, 7, 14 et 28 pour chaque propriété de chiffre d’affaires.

Dans **[!UICONTROL Performance Over Time]**, sélectionnez **[!UICONTROL Objective Value]**, **[!UICONTROL ROI]** ou **[!UICONTROL Model Accuracy]** pour comparer la date de clic, la date de transaction et les performances attendues. Cliquez sur **[!UICONTROL Table View]** pour basculer entre le graphique et ses données sous-jacentes.

Dans **[!UICONTROL Metrics Definitions]**, cliquez sur **[!UICONTROL Show]** pour obtenir des explications sur les dates et les mesures utilisées dans l’analyse, ou sur **[!UICONTROL Hide]** pour les réduire.

Si l’analyse n’est pas applicable, sélectionnez un portefeuille avec une attribution de chiffre d’affaires basée sur les clics ou sur les vues. Si aucune donnée n’est disponible, vérifiez qu’il existe des données pour le portefeuille et la période sélectionnés.
