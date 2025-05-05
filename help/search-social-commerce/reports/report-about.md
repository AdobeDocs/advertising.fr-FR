---
title: A propos des rapports
description: Découvrez les rapports de performances, notamment les différents types de rapports disponibles et comment automatiser les rapports.
exl-id: 173d1bad-e3aa-4417-a9b1-4b5d06c304d2
feature: Search Reports
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# A propos des rapports

Les rapports de performances vous permettent de suivre et de gérer les performances de vos portfolios, réseaux publicitaires et entités de compte réseau publicitaire à un niveau aussi granulaire que vous le souhaitez. La plupart des rapports fournissent une visibilité complète sur la manière dont les publicités de chaque canal marketing contribuent au taux de conversion global.

Les données d’un rapport sont compilées dynamiquement chaque fois que vous exécutez le rapport. Vous pouvez éventuellement générer un nouveau rapport à partir d’un rapport existant. Les paramètres de rapport disponibles varient en fonction du type de rapport. Pour la plupart des rapports, vous avez la possibilité de prévisualiser les 50 premières lignes au lieu de générer le rapport entier. Lorsque vous générez un rapport, vous pouvez envoyer une notification avec des liens de téléchargement vers une ou plusieurs adresses électroniques une fois le rapport terminé, et les destinataires peuvent [gérer les notifications dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Tous les rapports terminés sont disponibles dans la section [!UICONTROL Latest Reports] de la vue [!UICONTROL Reports] et vous pouvez les afficher au format tableau dans la fenêtre du navigateur ou les ouvrir ou les télécharger sous forme de fichiers.

## Catégories de rapports disponibles

Les catégories de rapports suivantes sont disponibles à partir de la vue [!UICONTROL Reports]. Vous n’avez peut-être pas accès à tous ces rapports ; les rapports disponibles et les données qu’ils génèrent sont déterminés par votre rôle et la manière dont votre compte client est configuré.

| Catégorie de rapports | Description |
| ----| ---- |
| [!UICONTROL Basic Reports] | Les [ rapports de base ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md), disponibles pour tous les utilisateurs, indiquent le coût réel et les données de clic pour les portefeuilles, les comptes réseau de publicités, les comptes réseau de publicités spécifiques, les campagnes, les groupes publicitaires, les annonces, les mots-clés, les groupes de produits, les classifications d’étiquettes et les valeurs d’étiquettes, les contraintes d’unité d’offre et les contraintes réseau. Elles sont basées sur les clics facturés par les réseaux publicitaires applicables et peuvent éventuellement inclure des données de conversion ou toute autre mesure que vous créez. |
| [!UICONTROL Advanced Reports] | Les [rapports avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) fournissent des informations supplémentaires sur la configuration de vos publicités, afin de vous aider à identifier les avantages potentiels d’une modification du ciblage géographique ou des paramètres réseau. Ils peuvent également vous aider à valider les données de conversion dans les rapports et les vues de gestion de campagne et de portefeuille par rapport aux données de suivi de conversion interne de l’annonceur. |
| [!UICONTROL Assist Reports] | [Les rapports d’assistance](/help/search-social-commerce/reports/management/assist/assist-report-about.md) fournissent des informations sur les chemins de conversion de tous les mots-clés et annonces d’un annonceur. Ils utilisent les données capturées par le biais du service de suivi de conversion d’Adobe Advertising et peuvent uniquement être générées pour les annonceurs disposant du service. |
| [!UICONTROL Specialty Reports] | Les [rapports de spécialité](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) se composent de données collectées par les réseaux publicitaires (plutôt que par le suivi des Adobes Advertising). |
| [!UICONTROL Model Accuracy Reports] | Les [rapports de précision du modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indiquent la précision des modèles de coûts et de recettes utilisés pour optimiser les offres, les budgets de campagne et les cibles de stratégie d’offre pour un portefeuille. |

## Automatisation des rapports

Planifiez la génération automatique de rapports personnalisés de l’une ou l’autre des manières suivantes :

* Générez automatiquement des rapports chaque jour, ou un jour spécifique de la semaine ou du mois, à l’aide des [modèles de rapport](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Vous pouvez éventuellement configurer la [distribution FTP des rapports de base et avancés](/help/search-social-commerce/reports/automation/ftp-reports.md) qui utilisent un modèle.

* Continuez à actualiser vos modèles de feuille de calcul personnalisés avec des données de performances quotidiennes à l’aide des [flux de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## Les vues Rapports

Les [!UICONTROL Reports] vues sur [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] vous permettent de créer et de gérer des rapports, des modèles et des flux de feuille de calcul. La vue comprend deux onglets :

* L’onglet **[!UICONTROL Latest Reports]** répertorie tous les rapports disponibles qui ont été demandés au cours des sept derniers jours, à l’exception de ceux qui ont été supprimés manuellement, le rapport le plus récent se trouvant en haut par défaut. Les informations affichées pour chaque rapport incluent la planification de son exécution (le cas échéant), les dates de début et de fin pour lesquelles des données ont été générées ou le seront, ainsi que l’état du rapport (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* ou *[!UICONTROL Error]*).

  Les liens en regard de chaque rapport vous permettent d’afficher le rapport dans le navigateur web, de l’ouvrir ou de l’enregistrer en tant que fichier de classeur [!DNL Microsoft Excel] (XLS) ou de valeurs séparées par des tabulations (TSV). Certains types de rapports peuvent également être enregistrés en tant que classeurs [!UICONTROL Excel] avec une feuille de calcul distincte pour chaque campagne applicable.

  Depuis cet onglet, vous pouvez également créer un nouveau rapport (qui peut éventuellement être utilisé comme modèle), créer un nouveau rapport en fonction des paramètres d’un rapport existant, annuler les rapports en cours disponibles en les supprimant et supprimer tout rapport terminé qui vous est disponible. Les rapports de plus de sept jours sont automatiquement supprimés.

* L’onglet **[!UICONTROL Templates]** répertorie tous les modèles de rapports de base et avancés enregistrés à votre disposition, y compris des informations sur les plannings qui leur sont associés. Le modèle le plus récent se trouve en haut par défaut.

  Depuis cet onglet, vous pouvez créer un modèle, modifier le modèle que vous avez créé (y compris ajouter, modifier ou supprimer son planning), générer un rapport à partir d’un modèle et supprimer tout modèle mis à votre disposition.

## Utilisation des rapports

| Objectif | Rapport |
| ---- | ---- |
| Surveillance des performances | <ul><li>[ [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[ [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[ [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[ [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[ [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[ [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Dépannage des performances et analyse des tendances | <ul><li>[ [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[ [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[ [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[ [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[ [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) et [Le [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Tout rapport de base qui compare deux fenêtres temporelles à l’aide de la fonction &quot;[!UICONTROL Compare with]&quot;</li></ul> |
| Identifier les opportunités de croissance économique | <ul><li>(Publicitaires avec suivi de conversion par Adobe Advertising uniquement) [The [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Publicitaires avec suivi de conversion par Adobe Advertising uniquement) [The [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Annonceurs avec [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=fr)) Rapports personnalisés dans Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Publicitaires avec suivi de conversion par Adobe Advertising uniquement) [The [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Annonceurs avec [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=fr)) Rapports personnalisés dans Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Données utilisées pour les rapports](data-used-for-reports.md)
>* [ Tâches de configuration initiales pour les rapports ](initial-setup.md)
>* [Générer un rapport de base ou avancé](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Générer un rapport de précision de modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Générer un rapport de spécialité](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Générer un rapport d’assistance](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
