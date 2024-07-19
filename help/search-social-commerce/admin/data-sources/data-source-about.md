---
title: À propos de la synchronisation des mesures de conversion  [!DNL Google Analytics]
description: Découvrez la synchronisation des mesures de conversion  [!DNL Google Analytics] pour l’optimisation et la création de rapports.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# A propos de la synchronisation des mesures de conversion [!DNL Google Analytics]

Search, Social et Commerce peuvent synchroniser les mesures de conversion pour un compte, une propriété et une combinaison d’affichage spécifiques [!DNL Google Analytics] à des fins d’optimisation et de création de rapports. [Pages vues](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sessions](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Taux de rebond](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (calculé en tant que bounces/sessions) et [Durée de session](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) sont automatiquement inclus. Vous pouvez inclure jusqu’à 16 mesures supplémentaires par source de données.

>[!NOTE]
>
>Les utilisateurs d’Advertising DSP peuvent utiliser les mesures de conversion comme objectifs personnalisés et dans des rapports.

L’utilisation de l’API pour les transferts de données est évaluée sur un projet dans le compte [!DNL Google Analytics] applicable. Vous pouvez afficher vos quotas pour ce projet dans [le [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Voir la documentation [!DNL Google Analytics] pour plus d’informations sur les [quotas et limites d’appels pour les demandes d’API de création de rapports](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

Les étapes suivantes décrivent le processus de synchronisation des données de conversion de [!DNL Google Analytics].

1. [Effectuez les tâches préalables requises](data-source-prerequisites.md)

   * Implémentez un jeton d’Adobe Advertising (`ef_id` paramètre de chaîne de requête) dans les URL de page d’entrée pour tous les comptes publicitaires applicables.

   * Capturez le jeton d’Adobe Advertising (`ef_id` paramètre de chaîne de requête) dans un [!DNL Custom Dimension] dans [!DNL Google Analytics].

1. (Administrateur de compte de l&#39;agence, gestionnaire de compte de l&#39;agence, gestionnaire de compte [!DNL Adobe] et utilisateurs administrateurs uniquement) [Créez une source de données par [!DNL Google Analytics] combinaison de compte, de propriété et d&#39;affichage](data-source-configure.md).

   Pour intégrer des mesures pour plusieurs propriétés ou pour plusieurs vues pour une seule propriété, configurez une source de données distincte pour chacune d’elles.

   Une fois qu’une source de données est configurée, Search, Social et Commerce extrait les données quotidiennement, à partir de 05h00 dans le fuseau horaire de l’annonceur. Une fois les mesures disponibles, vous pouvez les inclure dans les vues de gestion de campagne et de portefeuille, ainsi que dans les rapports, et les utiliser dans les objectifs d’optimisation, si nécessaire.

>[!MORELIKETHIS]
>
>* [ Conditions préalables à la configuration d’une  [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [ Configuration d’une  [!DNL Google Analytics] vue en tant que source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe - Disponible [!DNL Google Analytics] metrics](data-source-ga-metrics.md)
