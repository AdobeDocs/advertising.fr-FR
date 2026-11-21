---
title: À propos de la synchronisation de [!DNL Google Analytics] mesures de conversion
description: Découvrez comment synchroniser [!DNL Google Analytics] mesures de conversion pour l’optimisation et le compte rendu des performances.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
TQID: 'https://experienceleague.adobe.com/dN7AVijGEiKM1o2iu3Fcb2D61pFkTguFOOu0qIe-mZk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 1003789d-7feb-5a2f-a02d-3182fd0ceb8a
    internal-label: Search Admin
  - id: 9bd4e165-792f-5324-bcaa-eee38dc8b8e9
    internal-label: Search Data Sources
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
    internal-label: Data sources
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: Admin
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%
---
# À propos de la synchronisation de [!DNL Google Analytics] mesures de conversion

Search, Social et Commerce peuvent synchroniser les mesures de conversion pour un compte, une propriété et une combinaison d’affichages [!DNL Google Analytics] spécifiques à des fins d’optimisation et de création de rapports. [Les pages vues](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=page_tracking&jump=ga_pageviews), [les sessions](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessions), [le taux de rebond](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_bouncerate) (calculé comme rebonds/sessions) et [la durée de la session](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessionduration) sont automatiquement inclus. Vous pouvez inclure jusqu’à 16 mesures supplémentaires par source de données.

>[!NOTE]
>
>Les utilisateurs d’Advertising DSP peuvent utiliser les mesures de conversion comme objectifs personnalisés et dans les rapports.

Toute utilisation de l’API pour les transferts de données est évaluée sur un projet dans le compte [!DNL Google Analytics] applicable. Vous pouvez afficher vos quotas pour ce projet dans [le [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consultez la documentation [!DNL Google Analytics] pour plus d’informations sur les [quotas et les limites d’appel pour les requêtes d’API de création de rapports](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

Les étapes suivantes décrivent le processus de synchronisation des données de conversion de [!DNL Google Analytics].

1. [Effectuer les tâches préalables](data-source-prerequisites.md)

   * Implémentez un jeton Adobe Advertising (`ef_id` paramètre de chaîne de requête) dans les URL de page de destination pour tous les comptes publicitaires applicables.

   * Capturez le jeton Adobe Advertising (`ef_id` paramètre de chaîne de requête) dans un [!DNL Custom Dimension] dans [!DNL Google Analytics].

1. (Administrateur de compte d’agence, gestionnaire de compte d’agence, [!DNL Adobe] gestionnaire de compte et utilisateurs administrateurs uniquement) [Créez une source de données par [!DNL Google Analytics] combinaison de compte, de propriété et d’affichage](data-source-configure.md).

   Pour intégrer des mesures pour plusieurs propriétés ou pour plusieurs vues pour une seule propriété, configurez une source de données distincte pour chacune.

   Une fois qu’une source de données est configurée, Search, Social et Commerce extrait les données tous les jours, à partir de 5 h dans le fuseau horaire de l’annonceur. Une fois les mesures disponibles, vous pouvez les inclure dans les vues de gestion de campagnes et de portefeuilles ainsi que dans les rapports et les utiliser dans les objectifs d’optimisation, si nécessaire.

>[!MORELIKETHIS]
>
>* [Conditions préalables à la configuration d&#39;une  [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [Configurer une  [!DNL Google Analytics] vue en tant que source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspendre la synchronisation d&#39;une source de données](data-source-pause.md)
>* [Réauthentifier une  [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe -  [!DNL Google Analytics] mesures](data-source-ga-metrics.md) disponibles
