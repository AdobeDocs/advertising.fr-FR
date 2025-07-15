---
title: À propos des simulations
description: En savoir plus sur les simulations de portfolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# À propos des simulations

*Fonction Beta*

Les rapports de simulation indiquent le rapport coût/objectif marginal estimé, le coût, le nombre de clics et la valeur objective que vous pouvez vous attendre à voir pour un portefeuille à différents niveaux de dépenses (coût) et les budgets quotidiens correspondants ou d’autres cibles. Vous pouvez éventuellement personnaliser la vue<!-- add link --> pour afficher des mesures de trafic supplémentaires, les paramètres de simulation et uniquement un type spécifique de simulation ([!UICONTROL Weekly] ou [!UICONTROL Custom]).

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Types de simulations

* **Simulations hebdomadaires automatisées :** les rapports de simulation sont exécutés automatiquement chaque semaine à l’aide des paramètres actuels du portfolio. Les simulations hebdomadaires automatisées ne sont disponibles que pour les périodes où le portefeuille est [optimisé ou actif](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

  Chaque simulation hebdomadaire téléchargée se compose d’un classeur. Chaque classeur comprend la cible pour chacun des 20 niveaux d’étape et les prévisions de coût, de clics, de revenu pondéré (valeur de l’objectif) et de mesures de conversion incluses dans l’objectif, en fonction de la cible correspondante. Pour les 20 premières lignes de données, aucune contrainte n’a été appliquée ; pour les autres lignes de données, des contraintes ont été appliquées.

* **Simulations personnalisées générées par l’utilisateur :** vous pouvez créer un rapport de simulation personnalisé pour un seul portfolio [optimisé ou actif](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) à l’aide des paramètres actuels du portfolio ou des paramètres personnalisés du portfolio pour afficher les résultats que ces paramètres produiraient sans les modifier réellement. Par exemple, vous pouvez créer une simulation personnalisée pour voir l’effet de l’utilisation d’une stratégie de dépenses ou d’un budget d’apprentissage différents<!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->. Vous pouvez afficher les performances estimées au niveau du portefeuille, de la campagne, de l’unité d’enchères et de l’appareil. Les simulations personnalisées héritent du paramètre de dépenses des contraintes du portefeuille.

  >[!NOTE]
  >
  > Le nouveau formulaire de simulation personnalisé utilise les mêmes paramètres que l&#39;ancien formulaire, sauf qu&#39;il hérite des informations sur les contraintes d&#39;unité d&#39;enchères des paramètres du portefeuille. Vous n’avez pas la possibilité d’ignorer les contraintes d’unité d’enchères, comme vous l’avez fait dans l’ancienne page des paramètres personnalisés de simulation.

  Chaque simulation personnalisée téléchargée se compose d’un classeur. Chaque classeur comprend une feuille de calcul pour chaque niveau d&#39;entité spécifié de la simulation (portfolios, campagnes, groupes publicitaires, unités d&#39;enchères) lorsque des données sont disponibles pour ce niveau. Lorsque vous spécifiez des données au niveau de l’appareil, chaque feuille de calcul inclut une colonne [!UICONTROL Device]. Chaque feuille de calcul comprend une ligne avec des données pour chaque entité applicable et (lorsqu’elles sont spécifiées pour le rapport) et un type d’appareil pour chacune des 20 étapes (par exemple, une ligne par campagne). Les données de chaque ligne incluent le rapport coût/chiffre d’affaires marginal prévisionnel, le coût, les clics, le chiffre d’affaires pondéré (valeur de l’objectif), le type d’appareil et les mesures de conversion inclus dans l’objectif, en fonction de la cible correspondante. La feuille de calcul au niveau du portefeuille inclut également la cible pour les niveaux d’étape, et la feuille de calcul au niveau de l’entité inclut le réseau publicitaire, le compte, la campagne et (le cas échéant) le groupe publicitaire.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

## La vue [!UICONTROL Simulations]

La vue [!UICONTROL Simulations] répertorie les simulations hebdomadaires et les simulations personnalisées. L’administrateur et d’autres types d’utilisateurs<!-- Verify which --> peuvent voir les simulations personnalisées créées par d’autres utilisateurs. Tous les autres utilisateurs et utilisatrices ne peuvent voir que les simulations personnalisées qu’ils ou elles créent.

Le tableau de données comprend la progression de chaque simulation ; une colonne [!UICONTROL Target Midpoint] renseignée pour chaque ligne ; et des colonnes pour les prédictions de coût/impression/clic/valeur d’objectif, les valeurs réelles et la précision. Vous pouvez éventuellement ajouter d’autres colonnes personnalisées (y compris les mesures d’effet élévateur, telles que la valeur réelle de l’objectif divisée par le coût).

### Actions disponibles {#simulations-actions}

* [Personnalisez l’affichage](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) afin d’inclure des mesures supplémentaires, y compris les impressions estimées ; le coût réel, les clics, les impressions et la valeur de l’objectif ; la valeur coût par objectif ; la précision des coûts, la précision des clics et la précision de la valeur de l’objectif ; ainsi que la différence (delta) entre la valeur de l’objectif prévu et réel et la valeur coût par objectif. Vous pouvez également inclure des colonnes pour la plupart des paramètres et le type de simulation ([!UICONTROL Custom] ou [!UICONTROL Weekly]).

* [Générer ou réexécuter une simulation personnalisée](simulation-create.md) pour un seul portfolio. Vous pouvez créer une nouvelle simulation ou régénérer une simulation existante dans la liste.

* [Téléchargez des simulations hebdomadaires et personnalisées](simulation-download.md) sous forme de classeurs [!DNL Microsoft Excel] dans des fichiers ZIP.

* À l’aide du bouton [!UICONTROL Spend Planner] , ouvrez l’outil hérité de recommandation des dépenses, qui vous aide à identifier la répartition optimale des dépenses entre les portefeuilles.

## Bonnes pratiques

Surveillez les rapports de simulation dans les situations suivantes :

* Avant de lancer un portfolio, estimez les performances attendues avec les paramètres de portfolio correspondants ; utilisez au moins deux semaines de données. Si les résultats de la simulation indiquent des performances inférieures à celles que vous attendiez sur la base des données historiques pour les campagnes incluses, recherchez et résolvez les problèmes avant de lancer le portfolio.

* Après tout changement majeur apporté à un portefeuille, tel que l’ajout d’une campagne ou la modification de l’objectif. Si vous apportez des modifications à la date de début de modélisation du portefeuille, au poids d’une mesure de conversion ou à la valeur de clic d’un objectif, attendez après 17 h 00 PST le lendemain pour exécuter la simulation, lorsque des modèles de coûts et de revenus mis à jour sont disponibles.

* Surveillez régulièrement les tendances de performances au niveau des mesures de conversion.

>[!MORELIKETHIS]
>
>* [Exécuter ou réexécuter une simulation](simulation-create.md)
>* [Télécharger des simulations](simulation-download.md)
