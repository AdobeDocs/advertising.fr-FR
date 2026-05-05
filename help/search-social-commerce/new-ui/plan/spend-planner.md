---
title: Utilisation de l’[!UICONTROL Spend Planner]
description: Découvrez comment générer, télécharger et appliquer des recommandations de budget de portefeuille pour vous aider à obtenir une répartition optimale des dépenses dans vos portefeuilles.
feature: Search Optimization, Search Portfolios
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
TQID: https://experienceleague.adobe.com/8BAQij06MRhxYoCoFNjhHsgC4o38lQnj9vpmTzYyqGg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4126848d8192a1d4a23406dfeb5b643788670689
workflow-type: tm+mt
source-wordcount: 801
ht-degree: 0%

---

# Utilisation de l’[!UICONTROL Spend Planner]

Le [!UICONTROL Spend Planner] (appelé « [!UICONTROL Spend Recommendation Tool] » dans l’interface utilisateur héritée) identifie la répartition optimale des dépenses entre les portefeuilles optimisés et actifs avec le même objectif et la même devise, afin que vous puissiez maximiser les recettes ou les objectifs cibles pour le jeu de portefeuilles.

Lorsque vous affichez un rapport de recommandation de dépenses pour les portefeuilles dotés de budgets quotidiens, vous pouvez modifier les budgets de n&#39;importe quel portefeuille en budgets recommandés.

## Données du rapport [!UICONTROL Spend Planner]

Pour les portefeuilles dotés de l’[!UICONTROL Maximize Clicks] d’objectif, le rapport comprend des recommandations de dépenses et des projections de clics. Pour tous les autres objectifs, le rapport comprend des recommandations de dépenses et des projections de recettes.

Les rapports de recommandation de dépenses incluent les données suivantes :

* Un graphique en courbes de dispersion montre le chiffre d’affaires maximum prévu ou les clics qui peuvent être atteints avec un coût total donné pour le portefeuille défini lorsque les objectifs de dépenses individuels sont définis de manière optimale. Le coût prévu pour chaque point de chiffre d’affaires ou de clic est inclus.

* Deux graphiques en anneau indiquant les dépenses et les revenus prévus ou la répartition des clics par portefeuille pour 1\) les objectifs de dépenses actuels et 2\) les objectifs de dépenses proposés.

* Graphique à barres pour chacun des portefeuilles, affichant les dépenses quotidiennes recommandées (coût) et la distribution des revenus prévue ou la distribution des clics lorsque vous maintenez l’objectif actuel de dépenses quotidiennes totales sur tous les portefeuilles sélectionnés, ou pour un objectif de dépenses totales proposées. Vous pouvez éventuellement appliquer les cibles de dépenses recommandées aux portefeuilles sélectionnés, ce qui affecte les enchères dans le prochain cycle d’exécution des offres.

## Actions disponibles

* Générez un rapport [!UICONTROL Spend Planner] à partir de la [nouvelle IU](#spend-recommendations-generate) ou de l’[ancienne IU](#spend-recommendations-generate-legacy).

* [Appliquez les recommandations de dépenses](#spend-recommendations-apply) aux portefeuilles correspondants.

* [Ouvrir ou enregistrer les données du rapport de recommandation de dépenses dans un fichier](#spend-recommendations-download)

## (Nouvelle interface utilisateur) Générer un rapport [!UICONTROL Spend Planner] {#spend-recommendations-generate}

1. Effectuez l’une des opérations suivantes :

   * Dans le menu principal, cliquez sur **[!UICONTROL Plan]>[!UICONTROL Spend Planner]**.

   * Dans le menu principal, cliquez sur **[!UICONTROL Plan]>[!UICONTROL Simulations]**. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Planificateur de dépenses](/help/search-social-commerce/assets/spend-planner-icon.png "Planificateur de dépenses").

   L’outil [!UICONTROL Spend Recommendation] s’ouvre dans l’interface utilisateur héritée.

1. Affichez les données à l&#39;aide des budgets combinés actuels pour les portefeuilles sélectionnés :

   1. Sélectionnez l’objectif du portefeuille.

   1. Sélectionnez la devise.

   1. (Facultatif) Sélectionnez une stratégie de dépenses de portefeuille pour filtrer davantage la liste des portefeuilles.

   1. Cochez la case en regard de chaque portfolio à inclure. Pour sélectionner tous les portefeuilles, cochez la case en regard de [!UICONTROL Portfolios].

      Seuls les portfolios optimisés et actifs avec les paramètres sélectionnés sont répertoriés.

   1. Cliquez sur **[!UICONTROL Update]**.

   1. (Facultatif) Pour afficher le coût et le chiffre d’affaires de n’importe quel point du graphique, placez le curseur au-dessus du point.

1. (Facultatif) Pour afficher l’objectif de dépenses quotidiennes recommandé et le chiffre d’affaires attendu pour chacun des portefeuilles à l’aide d’un objectif de dépenses totales différent, saisissez un objectif de dépenses quotidiennes totales proposé pour tous les portefeuilles dans le champ [!UICONTROL Total Spend Target] . Appuyez ensuite sur la touche **Entrée**.

   L’outil de recommandation des dépenses utilise des données issues de simulations hebdomadaires. Par conséquent, le total des dépenses recommandées est celui qui correspond le mieux à l’objectif de dépenses proposé avec la combinaison de dépenses idéale.

<!--

New UI; validate post-Update steps once I get it to generate a report:

## Generate a spend recommendation report {#spend-recommendations-generate}

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Spend Planner]**.

1. View data using the current, combined budgets for the selected portfolios:

   1. Click **[!UICONTROL Select Objective]**.

   1. Select the portfolio objective.

   1. Select the currency.

   1. (Optional) Select a portfolio spend strategy to further filter the portfolios list.

   1. Select the check box next to each portfolio to include.

      Only optimized and active portfolios with the selected parameters are listed.

   1. Click **[!UICONTROL Update]**.

   1. (Optional) To see the cost and revenue for any point on the chart, hold the cursor over the point.

1. (Optional) To download the proposed allocation and expected revenue per portfolio, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download") next to [!UICONTROL Portfolio Allocation] in the right column.

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

1. (Optional) To view the recommended daily spend and expected revenue for each of the portfolios using a different total spend target, enter a proposed total daily spend target across all portfolios in the [!UICONTROL Total Spend Target] field. Then press the **Enter** key.

   The spend recommendation tool uses data from weekly simulations, so the total recommended spend is the closest match to your proposed spend target with the ideal spend mix.

-->

## (interface utilisateur héritée) Générer un rapport [!UICONTROL Spend Recommendation] à partir de la vue [!UICONTROL Optimization] > [!UICONTROL Spend Recommendation] {#spend-recommendations-generate-legacy}

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Optimization] >[!UICONTROL Spend Recommendation]**.

1. Affichez les données à l&#39;aide des budgets combinés actuels pour les portefeuilles sélectionnés :

   1. Sélectionnez l’objectif du portefeuille.

   1. Sélectionnez la devise.

   1. (Facultatif) Sélectionnez une stratégie de dépenses de portefeuille pour filtrer davantage la liste des portefeuilles.

   1. Cochez la case en regard de chaque portfolio à inclure. Pour sélectionner tous les portefeuilles, cochez la case en regard de [!UICONTROL Portfolios].

      Seuls les portfolios optimisés et actifs avec les paramètres sélectionnés sont répertoriés.

   1. Cliquez sur **[!UICONTROL Update]**.

   1. (Facultatif) Pour afficher le coût et le chiffre d’affaires de n’importe quel point du graphique, placez le curseur au-dessus du point.

1. (Facultatif) Pour afficher les dépenses quotidiennes recommandées et les revenus prévus pour chacun des portefeuilles à l’aide d’une nouvelle cible de dépenses totales, saisissez une cible de dépenses quotidiennes totales proposée pour tous les portefeuilles dans le champ [!UICONTROL Total Spend Target]. Appuyez ensuite sur la touche **Entrée**.

   L’outil de recommandation des dépenses utilise des données issues de simulations hebdomadaires. Par conséquent, le total des dépenses recommandées est celui qui correspond le mieux à l’objectif de dépenses proposé avec la combinaison de dépenses idéale.

<!--
## (New UI) Apply spend recommendations {#spend-recommendations-apply}

*Portfolios with daily budgets only*

>[!NOTE]
>
>* If the applied changes will increase or decrease the spend target of any portfolio by more than 20%, you must approve the change.
>* When the spend target for a portfolio changes by more than 20%, Search, Social, & Commerce takes up to 3-4 days to adjust its models and achieve the new target.

1. [Generate a spend recommendation report](#spend-recommendations-generate) for one or more portfolios with daily budgets.

1. Select the check box next to each portfolio for which you want to apply the recommended spend target. To select all portfolios, select the check box next to **[!UICONTROL Select All Recommendations]**.

1. Click **[!UICONTROL Apply Selected Recommendations]**.

1. (If any of the budgets will change by more than 20%) In the confirmation message, click **[!UICONTROL Confirm]** to approve the changes.

-->

## &#x200B;<!--(Legacy UI) -->Appliquez les recommandations de dépenses {#spend-recommendations-apply-legacy}

*Portefeuilles avec budgets quotidiens uniquement*

>[!NOTE]
>
>* Si les modifications appliquées augmentent ou réduisent l&#39;objectif de dépenses d&#39;un portefeuille de plus de 20 %, vous devez approuver la modification.
>* Lorsque l’objectif de dépenses d’un portefeuille change de plus de 20 %, Search, Social et Commerce met jusqu’à 3 à 4 jours pour ajuster ses modèles et atteindre le nouvel objectif.

1. [Générez un rapport de recommandation de dépenses](#spend-recommendations-generate-legacy) pour un ou plusieurs portefeuilles avec des budgets quotidiens.

1. Cochez la case en regard de chaque portefeuille pour lequel vous souhaitez appliquer la cible de dépenses recommandée. Pour sélectionner tous les portefeuilles, cochez la case en regard de **[!UICONTROL Select All Recommendations]**.

1. Cliquez sur **[!UICONTROL Apply Selected Recommendations]**.

1. (Si l’un des budgets change de plus de 20 %) Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]** pour approuver les modifications.

<!--

## (New UI) Open or save data as a [!DNL Microsoft Excel] workbook file {#spend-recommendations-download}

You can open or save data from either a) the line chart showing cost points and the expected revenue for each cost and b) the donut charts of the current and proposed media mix. [This seems to be identical to the Portfolio Allocation report -- how should these be different?]

1. [Generate a spend recommendation report](#spend-recommendations-generate) for selected portfolios.

1. Above the report, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download").

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

-->

## &#x200B;<!--(Legacy UI) -->Ouvrez ou enregistrez les données en tant que fichier de classeur  {#spend-recommendations-download-legacy}[!DNL Microsoft Excel]

1. Générer un rapport de recommandation de dépenses pour les portefeuilles sélectionnés.

1. Dans l’angle supérieur droit du rapport, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download-spend-recommendation.png "Télécharger").

   Ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur. Pour plus d’informations, consultez l’aide en ligne de votre navigateur.
