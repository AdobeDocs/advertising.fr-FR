---
title: A propos de la synchronisation [!DNL Google Analytics] mesures de conversion
description: En savoir plus sur la synchronisation [!DNL Google Analytics] mesures de conversion pour l’optimisation et la création de rapports.
role: User, Admin
exl-id: 0c263ced-3774-4d4b-9d61-65289cd74027
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# A propos de la synchronisation [!DNL Google Analytics] mesures de conversion

Search, Social et Commerce peuvent synchroniser les mesures de conversion pour une [!DNL Google Analytics] combinaison de compte, de propriété et d’affichage pour l’optimisation et la création de rapports. [Pages vues](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sessions](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Taux de rebond](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (calculé en tant que rebonds/sessions) et [Durée de la session](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) sont automatiquement inclus. Vous pouvez inclure jusqu’à 16 mesures supplémentaires par source de données.

>[!NOTE]
>
>Les utilisateurs de la publicité DSP peuvent utiliser les mesures de conversion comme objectifs personnalisés et dans des rapports.

L’ensemble de l’utilisation de l’API pour les transferts de données est évalué dans un projet dans le [!DNL Google Analytics] compte . Vous pouvez afficher vos quotas pour ce projet dans [la valeur [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Voir [!DNL Google Analytics] documentation pour plus d’informations [Quotas et limites d’appels pour les demandes d’API de création de rapports](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

Les étapes suivantes décrivent le processus de synchronisation des données de conversion à partir de [!DNL Google Analytics].

1. [Effectuez les tâches préalables requises](data-source-prerequisites.md)

   * Implémentation d’un jeton publicitaire Adobe (`ef_id` paramètre de chaîne de requête) dans les URL de la page d’entrée pour tous les comptes publicitaires applicables.

   * Capturer le jeton d’Adobe Advertising (`ef_id` paramètre de chaîne de requête) dans un [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Administrateur de compte de l’agence, gestionnaire de compte de l’agence, [!DNL Adobe] gestionnaire de compte et utilisateurs administrateurs uniquement) [Création d’une source de données par [!DNL Google Analytics] combinaison de compte, de propriété et d’affichage](data-source-configure.md).

   Pour intégrer des mesures pour plusieurs propriétés ou pour plusieurs vues pour une seule propriété, configurez une source de données distincte pour chacune d’elles.

   Une fois qu’une source de données est configurée, Search, Social et Commerce extrait les données quotidiennement, à partir de 05h00 dans le fuseau horaire de l’annonceur. Une fois les mesures disponibles, vous pouvez les inclure dans les vues de gestion de campagne et de portefeuille, ainsi que dans les rapports, et les utiliser dans les objectifs d’optimisation, si nécessaire.

>[!MORELIKETHIS]
>
>* [Conditions préalables à la configuration d’un [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [Configurez une [!DNL Google Analytics] vue en tant que source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspension de la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier un [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe : Disponible [!DNL Google Analytics] mesures](data-source-ga-metrics.md)
