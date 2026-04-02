---
title: À propos de la synchronisation [!DNL Google Analytics] des mesures de conversion
description: Découvrez les mesures de synchronisation [!DNL Google Analytics] conversion pour l’optimisation et le reporting.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/dN7AVijGEiKM1o2iu3Fcb2D61pFkTguFOOu0qIe-mZk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# À propos de la synchronisation [!DNL Google Analytics] mesures de conversion

Search, Social et Commerce peuvent synchroniser les mesures de conversion d’un compte [!DNL Google Analytics], d’une propriété et d’une combinaison d’affichages spécifiques à des fins d’optimisation et de création de rapports. [Pages vues](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=page_tracking&jump=ga_pageviews), [Sessions](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessions), [Taux de rebond](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_bouncerate) (calculé comme rebonds/sessions) et [Durée de la session](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessionduration) sont automatiquement inclus. Vous pouvez inclure jusqu’à 16 mesures supplémentaires par source de données.

>[!NOTE]
>
>Les utilisateurs d’Advertising DSP peuvent utiliser les mesures de conversion comme objectifs personnalisés et dans les rapports.

Toute utilisation de l’API pour les transferts de données est évaluée sur un projet dans le compte [!DNL Google Analytics] applicable. Vous pouvez consulter vos quotas pour ce projet dans [le [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Consultez [!DNL Google Analytics] documentation pour plus d’informations sur les [quotas et limites d’appel pour les requêtes d’API de création de rapports](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

Les étapes suivantes décrivent le processus de synchronisation des données de conversion à partir de [!DNL Google Analytics].

1. [Effectuer les tâches préalables](data-source-prerequisites.md)

   * Implémentez un jeton Adobe Advertising (paramètre de chaîne de requête `ef_id`) dans les URL de page de destination pour tous les comptes publicitaires applicables.

   * Capturez le jeton Adobe Advertising (paramètre de chaîne de requête `ef_id`) dans un [!DNL Custom Dimension] dans [!DNL Google Analytics].

1. (Administrateur de compte d’agence, Gestionnaire de compte d’agence, Gestionnaire de compte d’[!DNL Adobe] et utilisateurs administrateurs uniquement) [Créez une source de données par combinaison  [!DNL Google Analytics]  compte, de propriété et d’affichage](data-source-configure.md).

   Pour intégrer des mesures pour plusieurs propriétés ou pour plusieurs vues pour une seule propriété, configurez une source de données distincte pour chacune.

   Une fois qu’une source de données est configurée, Search, Social et Commerce extrait les données tous les jours, à partir de 05:00 dans le fuseau horaire de l’annonceur. Une fois les mesures disponibles, vous pouvez les inclure dans les vues de gestion de campagnes et de portefeuilles ainsi que dans les rapports et les utiliser dans les objectifs d’optimisation, si nécessaire.

>[!MORELIKETHIS]
>
>* [Conditions préalables à la configuration d’une source  [!DNL Google Analytics]  données](data-source-prerequisites.md)
>* [Configurer une [!DNL Google Analytics] vue comme source de données](data-source-configure.md)
>* [Modifier une source  [!DNL Google Analytics]  données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une source  [!DNL Google Analytics]  données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres des sources de données](data-source-settings.md)
>* [Annexe - Mesures  [!DNL Google Analytics]  disponibles](data-source-ga-metrics.md)
