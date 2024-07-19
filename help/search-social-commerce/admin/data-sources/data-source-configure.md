---
title: Configurer une  [!DNL Google Analytics] vue en tant que source de données
description: Découvrez comment configurer une source de données à partir d’une vue  [!DNL Google Analytics] .
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Configurer une vue [!DNL Google Analytics] en tant que source de données

*Administrateurs de l’agence, Responsables de compte de l’agence, Responsables de compte d’Adobe et Administrateurs uniquement*

Vous pouvez créer une source de données par compte, propriété et combinaison d’affichage [!DNL Google Analytics].

Pour intégrer des mesures pour plusieurs propriétés ou pour plusieurs vues pour une seule propriété, configurez une source de données distincte pour chacune d’elles.

1. [ Exécutez toutes les conditions préalables requises pour intégrer le  [!DNL Google Analytics] compte](data-source-prerequisites.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Dans la boîte de dialogue [!UICONTROL Deployment Prerequisites], cochez la case pour confirmer que la dimension personnalisée requise &quot;ef_id&quot; est implémentée dans le compte [!DNL Google Analytics], puis cliquez sur **[!UICONTROL Continue]**.

   Certaines conditions préalables peuvent avoir été remplies par d’autres rôles de votre organisation. Si vous avez des questions sur les conditions préalables, contactez votre équipe de compte d’Adobe.

1. Saisissez les [paramètres de source de données](data-source-settings.md) :

   1. Dans la section **[!UICONTROL Connect to [!DNL Google Analytics]]**, procédez comme suit.

      1. Saisissez l’identifiant numérique pour le compte [!DNL Google Analytics].

      1. Saisissez l’adresse électronique à utiliser pour accéder aux données de cette source de données. L’adresse électronique doit être enregistrée sur un compte [!DNL Google] et disposer des autorisations de &quot;lecture et analyse&quot; pour le compte [!DNL Google Analytics]. Reportez-vous aux [instructions pour l’attribution des autorisations utilisateur dans [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Pour vous assurer que seules des propriétés et des vues [!DNL Google Analytics] spécifiques sont disponibles dans Adobe Advertising, connectez-vous à l’aide d’une adresse électronique qui n’a accès qu’à ces propriétés et vues.

         >[!NOTE]
         >
         >Si vous modifiez ultérieurement le mot de passe de ce compte de messagerie, toutes les connexions ouvertes au compte de messagerie sont fermées. Pour reprendre la synchronisation des données, revenez à cette page et [réauthentifiez](data-source-reauthenticate.md).

      1. Cochez la case pour autoriser l’Adobe Advertising à accéder aux mesures du compte.

      1. Cliquez sur **[!UICONTROL Authenticate]**.

   1. Dans la section [!UICONTROL Account Details] , spécifiez la propriété et l’affichage des mesures à importer. En outre, spécifiez la dimension personnalisée renseignée avec la valeur du paramètre de chaîne de requête &quot;ef_id&quot;.

   1. Dans la section [!UICONTROL Import Metrics] , spécifiez les mesures à inclure dans le ou les flux.

      Vous ne pouvez pas supprimer [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] ou [!UICONTROL Session Duration], qui sont inclus automatiquement. Vous pouvez ajouter jusqu’à 16 mesures ou mesures valides supplémentaires sans données.

      >[!WARNING]
      >
      >[!DNL Google Analytics] autorise jusqu’à 10 mesures dans un seul flux de données. Search, Social et Commerce peuvent prendre en charge jusqu’à deux flux avec un total de 20 mesures, mais l’utilisation d’un deuxième flux double vos appels API vers [!DNL Google Analytics]. Si vous disposez de plusieurs mesures, sélectionnez uniquement celles que vous souhaitez utiliser dans les objectifs d’optimisation. Pour en savoir plus sur les [quotas et limites d’appels pour les demandes d’API à [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Dans la section [!UICONTROL Metric Tag] , saisissez le nom de la balise à ajouter à chaque mesure pour la source de données.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Post]**.

   La source de données est nommée &quot;NomCompte > NomPropriété > NomVue&quot; et est automatiquement activée. Pour mettre en pause la source de données, voir &quot;[Suspendre un flux d’un Source de données](data-source-pause.md)&quot;.

   Les mesures sont disponibles le lendemain de la fin de la synchronisation quotidienne des données, qui commence à 05h00 dans le fuseau horaire de l’annonceur. Une fois les mesures disponibles, elles sont visibles dans [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Chaque nouvelle mesure de conversion est nommée &quot;`ga:backEndMetricName_propertyID_viewID`&quot;, où &quot;backEndMetricName&quot; est le nom de mesure utilisé par l’API. Le nom d’affichage de chaque nouvelle mesure de conversion est &quot;`friendlyMetricName_ga:MetricTag`&quot;, où &quot;friendlyMetricName&quot; est le nom de la mesure qui apparaît dans [!DNL Google Analytics] et &quot;MetricTag&quot; est le [!UICONTROL Metric Tag] défini dans les paramètres de la source de données.

   Vous pouvez ajouter les mesures directement aux objectifs d’optimisation, de rapports et de vue de gestion de campagne et de portefeuille.

>[!MORELIKETHIS]
>
>* [ À propos de la synchronisation  [!DNL Google Analytics] mesures de conversion](data-source-about.md)
>* [ Conditions préalables à la configuration d’une  [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe - Disponible [!DNL Google Analytics] metrics](data-source-ga-metrics.md)
