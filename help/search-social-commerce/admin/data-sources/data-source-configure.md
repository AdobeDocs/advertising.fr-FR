---
title: Configurer une  [!DNL Google Analytics]  en tant que source de données
description: Découvrez comment configurer une source de données à partir d’une  [!DNL Google Analytics] .
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Configurer une vue [!DNL Google Analytics] comme source de données

*Administrateurs d’agence, Gestionnaires de compte d’agence, Gestionnaires de compte Adobe et Administrateurs uniquement*

Vous pouvez créer une source de données par combinaison de compte, propriété et vue [!DNL Google Analytics].

Pour intégrer des mesures pour plusieurs propriétés ou pour plusieurs vues pour une seule propriété, configurez une source de données distincte pour chacune.

1. [Réalisez toutes les conditions préalables à l’intégration du [!DNL Google Analytics] compte](data-source-prerequisites.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Dans la boîte de dialogue [!UICONTROL Deployment Prerequisites], cochez la case pour confirmer que la dimension personnalisée « ef_id » requise est implémentée dans le compte [!DNL Google Analytics], puis cliquez sur **[!UICONTROL Continue]**.

   Certaines conditions préalables peuvent avoir été remplies par d’autres rôles de votre organisation. Si vous avez des questions sur les conditions préalables, contactez l’équipe chargée de votre compte Adobe.

1. Renseignez les [paramètres de la source de données](data-source-settings.md) :

   1. Dans la section **[!UICONTROL Connect to [!DNL Google Analytics]]**, procédez comme suit.

      1. Saisissez l’identifiant numérique du compte [!DNL Google Analytics].

      1. Saisissez l’adresse e-mail à utiliser pour accéder aux données de cette source de données. L’adresse e-mail doit être enregistrée sur un compte [!DNL Google] et disposer des autorisations « Lecture et analyse » pour le compte [!DNL Google Analytics]. Reportez-vous aux [instructions pour l’attribution des autorisations utilisateur dans [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Pour vous assurer que seules des propriétés et des vues de [!DNL Google Analytics] spécifiques sont disponibles dans Adobe Advertising, connectez-vous à l’aide d’une adresse e-mail qui n’a accès qu’à ces propriétés et vues.

         >[!NOTE]
         >
         >Si vous modifiez par la suite le mot de passe de ce compte de messagerie, toutes les connexions ouvertes au compte de messagerie seront fermées. Pour reprendre la synchronisation des données, revenez à cette page et [réauthentifiez](data-source-reauthenticate.md).

      1. Cochez la case pour autoriser Adobe Advertising à accéder aux mesures du compte.

      1. Cliquez sur **[!UICONTROL Authenticate]**.

   1. Dans la section [!UICONTROL Account Details] , spécifiez la propriété et la vue des mesures à importer. En outre, spécifiez la dimension personnalisée qui est renseignée avec la valeur du paramètre de chaîne de requête « ef_id ».

   1. Dans la section [!UICONTROL Import Metrics] , spécifiez les mesures à inclure dans le ou les flux .

      Vous ne pouvez pas supprimer [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] ou [!UICONTROL Session Duration], qui sont automatiquement inclus. Vous pouvez ajouter jusqu’à 16 mesures valides supplémentaires ou mesures sans données.

      >[!WARNING]
      >
      >[!DNL Google Analytics] permet jusqu’à 10 mesures dans un seul flux de données. Search, Social et Commerce peuvent prendre en charge jusqu’à deux flux avec un total de 20 mesures, mais l’utilisation d’un second flux double vos appels API à [!DNL Google Analytics]. Si vous disposez de nombreuses mesures, sélectionnez uniquement celles que vous souhaitez utiliser dans les objectifs pour l’optimisation. En savoir plus sur les [quotas et limites d’appel pour les requêtes API vers [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Dans la section [!UICONTROL Metric Tag] , saisissez le nom de la balise à ajouter à chaque mesure pour la source de données.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Post]**.

   La source de données s’appelle « AccountName > PropertyName > ViewName » et est automatiquement activée. Pour mettre la source de données en pause, reportez-vous à [ Mise en pause d’un flux à partir d’une Source de données ](data-source-pause.md).

   Les mesures sont disponibles le lendemain de la fin de la synchronisation quotidienne des données, qui commence à 5 h dans le fuseau horaire de l’annonceur. Une fois les mesures disponibles, elles sont visibles dans [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Chaque nouvelle mesure de conversion est nommée « `ga:backEndMetricName_propertyID_viewID` », où « backEndMetricName » est le nom de la mesure utilisée par l’API. Le nom d’affichage de chaque nouvelle mesure de conversion est « `friendlyMetricName_ga:MetricTag` », où « friendlyMetricName » est le nom de la mesure qui apparaît dans [!DNL Google Analytics] et « MetricTag » est le [!UICONTROL Metric Tag] défini dans les paramètres de la source de données.

   Vous pouvez ajouter les mesures directement aux vues de gestion de campagnes et de portefeuilles, aux rapports et aux objectifs d’optimisation.

>[!MORELIKETHIS]
>
>* [À propos de la synchronisation [!DNL Google Analytics] des mesures de conversion](data-source-about.md)
>* [Conditions préalables à la configuration d’une source  [!DNL Google Analytics]  données](data-source-prerequisites.md)
>* [Modifier une source  [!DNL Google Analytics]  données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une source  [!DNL Google Analytics]  données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres des sources de données](data-source-settings.md)
>* [Annexe - Mesures  [!DNL Google Analytics]  disponibles](data-source-ga-metrics.md)
