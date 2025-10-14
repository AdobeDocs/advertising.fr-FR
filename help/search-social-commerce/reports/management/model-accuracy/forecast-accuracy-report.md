---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Découvrez le rapport Précision des prévisions, y compris les colonnes de données.
exl-id: f0c42323-eb0d-461a-ab09-440fd1bfc960
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# Le [!UICONTROL Forecast Accuracy Report]

Le rapport indique la précision des modèles de coûts et de recettes par jour pour des portefeuilles spécifiques. Par défaut, il inclut les recettes quotidiennes prévues et réelles, le coût et les clics — ainsi que l&#39;exactitude des prévisions — pour chaque portefeuille. Il comprend les données des campagnes qui sont actuellement mappées aux portefeuilles.

Vous pouvez afficher les données des 18 mois précédents.

>[!NOTE]
>
>* Ce rapport fournit les mêmes données que le [!UICONTROL Model Accuracy Report] au niveau du portfolio, sauf que vous pouvez l’exécuter sur plusieurs portefeuilles et que vous pouvez modifier la règle d’attribution. Vous pouvez également exécuter et planifier le rapport à l’aide de paramètres personnalisés. Vous pouvez également l’utiliser pour créer des flux de feuille de calcul.
>
>* La bonne pratique consiste à afficher le [!UICONTROL Forecast Accuracy Report] pendant au moins les sept derniers jours, car, quelle que soit la stratégie de dépenses du portfolio, la plupart des portefeuilles affichent une tendance quotidienne de la semaine. La fonctionnalité d’optimisation prend cette tendance en compte et alloue les dépenses en conséquence.
>
>* Pour les prévisions de coûts, un écart de 10 % au cours des sept derniers jours est considéré comme acceptable, de sorte que les dépenses réelles comprises entre 90 % et 110 % des dépenses prévues sont correctes. Pour les prévisions de recettes, un écart de 15 % au cours des sept derniers jours est considéré comme acceptable, de sorte que les recettes réelles comprises entre 85 % et 115 % des dépenses prévues sont correctes. Les prévisions avec des écarts plus élevés doivent être étudiées.
>
>* Lorsque des mots-clés du portefeuille sont associés à des contraintes de changement d’offre, le portefeuille est surchargé ou sous-dépensé en fonction du montant total dû au changement d’offre. Par conséquent, les colonnes de coûts prédites s’écartent des dépenses cibles par rapport à l’augmentation ou à la diminution des dépenses.

## Colonnes disponibles

Vous trouverez ci-dessous les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section [!UICONTROL Columns] des paramètres du rapport.

| Colonne | Par défaut ? | Description |
|----|----|----|
| [!UICONTROL Portfolio] | Par défaut | Le portefeuille. |
| [!UICONTROL Day of Week] | Par défaut | Le jour de la semaine signalé : <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> ou <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Par défaut | Le premier jour a été rapporté. |
| [!UICONTROL End Date] | Par défaut | Le dernier jour rapporté. |
| [!UICONTROL Predicted Revenue] | Par défaut | Les recettes prévues pour le portefeuille. |
| [!UICONTROL Revenue] | Par défaut | Les recettes réelles du portfolio. |
| [!UICONTROL Revenue Accuracy] | Par défaut | Précision des prévisions de recettes, exprimée en pourcentage. |
| [!UICONTROL Predicted Cost] | Par défaut | Le coût prévu du portefeuille. |
| [!UICONTROL Cost] | Par défaut | Le coût réel du portfolio. |
| [!UICONTROL Cost Accuracy] | Par défaut | Précision de la prévision de coût, exprimée en pourcentage. |
| [!UICONTROL Predicted Clicks] | Par défaut | Nombre de clics prévus pour le portfolio. |
| [!UICONTROL Clicks] | Par défaut | Nombre réel de clics pour le portfolio. |
| [!UICONTROL Click Accuracy] | Par défaut | Précision de la prévision des clics, exprimée en pourcentage. |
| [!UICONTROL EF Portfolio Group ID] | Par défaut | Identifiant numérique pour le groupe de portefeuille auquel appartient le portfolio. |
| [!UICONTROL Portfolio Group Name] | Par défaut | Nom du groupe de portefeuille auquel appartient le portfolio. |
| [!UICONTROL Portfolio ID] | Par défaut | Identifiant numérique de portefeuille. |

>[!MORELIKETHIS]
>
>* [À propos des rapports de précision de modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [&#x200B; [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Générer un rapport de précision de modèle](model-accuracy-report-generate.md)
>* [&#x200B; Paramètres de rapport de précision du modèle &#x200B;](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
