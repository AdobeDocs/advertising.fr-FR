---
title: Rapports
description: Découvrez les rapports de performance, y compris les différents types de rapports disponibles et comment automatiser les rapports.
exl-id: 173d1bad-e3aa-4417-a9b1-4b5d06c304d2
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# Rapports

Les rapports de performance vous permettent de suivre et de gérer les performances de vos portefeuilles, réseaux publicitaires et entités de compte réseau publicitaire avec le niveau de granularité souhaité. La plupart des rapports offrent une visibilité complète sur la manière dont les annonces publicitaires de chaque canal marketing contribuent au taux de conversion global.

Les données d’un rapport sont compilées dynamiquement à chaque exécution du rapport. Vous avez la possibilité de générer un nouveau rapport à partir d’un rapport existant. Les paramètres de rapport disponibles varient selon le type de rapport. Pour la plupart des rapports, vous avez la possibilité de prévisualiser les 50 premières lignes au lieu de générer le rapport entier. Lorsque vous générez un rapport, vous pouvez envoyer une notification avec des liens de téléchargement à une ou plusieurs adresses e-mail lorsqu’un rapport est terminé. Les destinataires peuvent [gérer les notifications dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Tous les rapports terminés sont disponibles dans la section [!UICONTROL Latest Reports] de la vue [!UICONTROL Reports]. Vous pouvez soit les afficher sous forme de tableau dans la fenêtre du navigateur, soit les ouvrir ou les télécharger sous forme de fichiers.

## Catégories de rapports disponibles

Les catégories de rapports suivantes sont disponibles à partir de la vue [!UICONTROL Reports]. Il se peut que vous n’ayez pas accès à tous ces rapports. Les rapports disponibles et les données qu’ils génèrent sont déterminés par votre rôle et par la configuration de votre compte client.

| Catégorie de rapport | Description |
| ----| ---- |
| [!UICONTROL Basic Reports] | Les [rapports de base](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) disponibles pour tous les utilisateurs, affichent le coût réel et les données relatives aux clics pour les portfolios, les comptes de réseau publicitaire, les comptes de réseau publicitaire spécifiques, les campagnes, les groupes publicitaires, les annonces, les mots-clés, les groupes de produits, les classifications d’étiquettes et les valeurs d’étiquettes, les contraintes d’unité d’offre et les contraintes réseau. Elles sont basées sur les clics facturés par les réseaux publicitaires applicables et peuvent éventuellement inclure des données de conversion ou toute autre mesure que vous créez. |
| [!UICONTROL Advanced Reports] | Les [rapports avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) fournissent des insight supplémentaires dans votre configuration publicitaire, ce qui vous permet d’identifier les endroits où il serait bénéfique de modifier votre ciblage géographique ou vos paramètres réseau. Ils peuvent également vous aider à valider les données de conversion dans les vues et rapports de gestion de campagne et de portefeuille par rapport aux données de suivi de conversion internes de l’annonceur. |
| [!UICONTROL Assist Reports] | [Les rapports d’assistance](/help/search-social-commerce/reports/management/assist/assist-report-about.md) fournissent des informations sur les chemins de conversion de tous les mots-clés et publicités d’un annonceur. Ils utilisent des données capturées par le biais du service de suivi des conversions d’Adobe Advertising et ne peuvent être générés que pour les annonceurs qui utilisent le service. |
| [!UICONTROL Specialty Reports] | Les [rapports spécialisés](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) sont constitués de données collectées par les réseaux publicitaires (plutôt que par le suivi Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Rapports sur la précision des modèles](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indiquez la précision des modèles de coût et de chiffre d’affaires utilisés pour optimiser les offres, les budgets de campagne et les cibles de stratégie d’offre pour un portefeuille. |

## Automatisation des rapports

Planifiez la génération automatique de rapports personnalisés de l’une des façons suivantes, ou des deux :

* Générez automatiquement des rapports chaque jour, ou un jour spécifique de la semaine ou du mois, à l’aide de [ modèles de rapport ](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Vous pouvez éventuellement paramétrer la diffusion [FTP) de rapports de base et avancés](/help/search-social-commerce/reports/automation/ftp-reports.md) qui utilisent un modèle.

* Continuez à actualiser vos modèles de feuilles de calcul personnalisés avec les données de performances quotidiennes à l’aide des [flux de feuilles de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## Les vues Rapports

Les vues [!UICONTROL Reports] dans [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] vous permettent de créer et de gérer des rapports, des modèles et des flux de feuilles de calcul. La vue comprend deux onglets :

* L’onglet **[!UICONTROL Latest Reports]** répertorie tous les rapports disponibles qui ont été demandés au cours des sept derniers jours, à l’exception de ceux qui ont été supprimés manuellement, le rapport le plus récent étant en haut par défaut. Les informations affichées pour chaque rapport incluent le planning de son exécution (le cas échéant), les dates de début et de fin pour lesquelles des données ont été ou seront générées, ainsi que le statut du rapport (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* ou *[!UICONTROL Error]*).

  Les liens en regard de chaque rapport vous permettent d’afficher le rapport dans le navigateur web ou de l’ouvrir ou de l’enregistrer en tant que fichier de classeurs [!DNL Microsoft Excel] (XLS) ou de valeurs séparées par des tabulations (TSV) ; certains types de rapports peuvent également être enregistrés en tant que classeurs [!UICONTROL Excel] avec une feuille de calcul distincte pour chaque campagne applicable.

  Dans cet onglet, vous pouvez également créer un nouveau rapport (qui peut éventuellement être utilisé comme modèle), créer un nouveau rapport basé sur les paramètres d&#39;un rapport existant, annuler les rapports en cours disponibles en les supprimant et supprimer tout rapport terminé disponible. Les rapports datant de plus de sept jours sont automatiquement supprimés.

* L’onglet **[!UICONTROL Templates]** répertorie tous les modèles de rapport de base et avancés enregistrés disponibles, y compris des informations sur les plannings qui leur sont associés. Par défaut, le modèle le plus récent se trouve en haut de l’écran.

  À partir de cet onglet, vous pouvez créer un modèle, modifier tout modèle que vous avez créé (y compris ajouter, modifier ou supprimer son planning), générer un rapport à partir d’un modèle et supprimer tout modèle disponible.

## Utilisation des rapports

| Objectif | Rapport |
| ---- | ---- |
| Surveillance des performances | <ul><li>[Le [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[Le [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[Le [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[Le [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[Le [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[Le [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Dépannage des performances et analyse des tendances | <ul><li>[Le [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[Le [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[Le [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[Le [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[Le [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) et [Le [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Tout rapport de base qui compare deux fenêtres temporelles à l’aide de la fonction « [!UICONTROL Compare with] »</li></ul> |
| Identifier les opportunités de croissance commerciale | <ul><li>(Annonceurs avec suivi des conversions Adobe Advertising uniquement) [Le [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Annonceurs avec suivi des conversions Adobe Advertising uniquement) [Le [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Annonceurs avec [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Rapports personnalisés dans Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Annonceurs avec suivi des conversions Adobe Advertising uniquement) [Le [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Annonceurs avec [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Rapports personnalisés dans Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Données utilisées pour les rapports](data-used-for-reports.md)
>* [Tâches de configuration initiales pour les rapports](initial-setup.md)
>* [Générer un rapport de base ou avancé](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Générer un rapport de précision de modèle](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Générer un rapport spécialisé](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Générer un rapport d’assistance](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
