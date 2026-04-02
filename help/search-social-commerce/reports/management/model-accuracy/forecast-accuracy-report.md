---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Découvrez le rapport Précision des prévisions, y compris les colonnes de données.
exl-id: f0c42323-eb0d-461a-ab09-440fd1bfc960
feature: Search Reports, Search Model Accuracy Reports
TQID: https://experienceleague.adobe.com/FHLlU9t-6rhRH9XpgF6pxPviMDucJllzsLX-x7FEuTY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 446
ht-degree: 0%

---

# Le [!UICONTROL Forecast Accuracy Report]

Le rapport affiche la précision des modèles de coût et de chiffre d’affaires par jour pour des portefeuilles spécifiés. Par défaut, il inclut le chiffre d’affaires, le coût et les clics quotidiens prévus et réels, ainsi que l’exactitude des prévisions, pour chaque portefeuille. Il inclut les données des campagnes qui sont actuellement mappées aux portfolios.

Vous pouvez afficher les données des 18 mois précédents.

>[!NOTE]
>
>* Ce rapport fournit les mêmes données que le [!UICONTROL Model Accuracy Report] au niveau du portefeuille, à la différence que vous pouvez l’exécuter sur plusieurs portefeuilles et que vous pouvez modifier la règle d’attribution. Vous pouvez également exécuter et planifier le rapport à l&#39;aide de paramètres personnalisés et l&#39;utiliser pour créer des flux de feuilles de calcul.
>
>* La bonne pratique consiste à afficher les [!UICONTROL Forecast Accuracy Report] pendant au moins les sept derniers jours, car, quelle que soit la stratégie de dépenses du portefeuille, la plupart des portefeuilles affichent une tendance inhérente par jour de la semaine. La fonctionnalité d’optimisation prend cette tendance en compte et alloue les dépenses en conséquence.
>
>* Pour les prévisions de coûts, un écart de 10 % au cours des sept derniers jours est considéré comme acceptable, de sorte que les dépenses réelles qui se situent entre 90 % et 110 % des dépenses prévues sont acceptables. Pour les prévisions de revenus, un écart de 15 % au cours des sept derniers jours est considéré comme acceptable, de sorte que les revenus réels qui se situent entre 85 % et 115 % des dépenses prévues sont acceptables. Les prévisions présentant des écarts plus importants doivent être étudiées.
>
>* Lorsque des mots-clés du portefeuille sont associés à des contraintes de changement d’offre, le portefeuille dépasse ou sous-dépense le montant total causé par le changement d’offre. Par conséquent, les colonnes des coûts prévus s&#39;écartent des dépenses cibles en raison de l&#39;augmentation ou de la diminution des dépenses.

## Colonnes disponibles

Voici les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section [!UICONTROL Columns] des paramètres du rapport.

| Colonne | Par défaut ? | Description |
|----|----|----|
| [!UICONTROL Portfolio] | Par défaut | Le portfolio. |
| [!UICONTROL Day of Week] | Par défaut | Jour de la semaine signalé : <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> ou <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Par défaut | Le premier jour signalé. |
| [!UICONTROL End Date] | Par défaut | Dernier jour signalé. |
| [!UICONTROL Predicted Revenue] | Par défaut | Chiffre d’affaires prévu du portefeuille. |
| [!UICONTROL Revenue] | Par défaut | Chiffre d’affaires réel du portefeuille. |
| [!UICONTROL Revenue Accuracy] | Par défaut | Exactitude des prévisions de revenus, exprimée en pourcentage. |
| [!UICONTROL Predicted Cost] | Par défaut | Coût prévu du portefeuille. |
| [!UICONTROL Cost] | Par défaut | Coût réel du portefeuille. |
| [!UICONTROL Cost Accuracy] | Par défaut | Exactitude de la prévision de coût, exprimée en pourcentage. |
| [!UICONTROL Predicted Clicks] | Par défaut | Nombre de clics prévus sur le portfolio. |
| [!UICONTROL Clicks] | Par défaut | Nombre réel de clics sur le portfolio. |
| [!UICONTROL Click Accuracy] | Par défaut | Précision de la prévision de clic, exprimée en pourcentage. |
| [!UICONTROL EF Portfolio Group ID] | Par défaut | Identifiant numérique du groupe de portefeuilles auquel appartient le portefeuille. |
| [!UICONTROL Portfolio Group Name] | Par défaut | Nom du groupe de portefeuilles auquel le portefeuille appartient. |
| [!UICONTROL Portfolio ID] | Par défaut | Identifiant numérique de portfolio. |

>[!MORELIKETHIS]
>
>* [À propos des rapports de précision de modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [Le [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Générer un rapport de précision de modèle](model-accuracy-report-generate.md)
>* [Paramètres du rapport de précision du modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
