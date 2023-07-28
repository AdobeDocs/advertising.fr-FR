---
title: Configurez une [!DNL Google Analytics] vue comme source de données
description: Découvrez comment configurer une source de données à partir d’une [!DNL Google Analytics] vue.
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Configurez une [!DNL Google Analytics] vue comme source de données

*Administrateurs de l’agence, responsables de compte de l’agence, gestionnaires de compte d’Adobe et administrateurs uniquement*

Vous pouvez créer une source de données par [!DNL Google Analytics] combinaison de compte, propriété et vue.

Pour intégrer des mesures pour plusieurs propriétés ou pour plusieurs vues pour une seule propriété, configurez une source de données distincte pour chacune d’elles.

1. [Exécutez toutes les conditions préalables requises pour intégrer la variable [!DNL Google Analytics] account](data-source-prerequisites.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Dans le [!UICONTROL Deployment Prerequisites] , cochez la case pour confirmer que la dimension personnalisée requise &quot;ef_id&quot; est implémentée dans la variable [!DNL Google Analytics] compte, puis cliquez sur **[!UICONTROL Continue]**.

   Certaines conditions préalables peuvent avoir été remplies par d’autres rôles de votre organisation. Si vous avez des questions sur les conditions préalables, contactez votre équipe de compte d’Adobe.

1. Saisissez le [paramètres de source de données](data-source-settings.md):

   1. Dans le **[!UICONTROL Connect to [!DNL Google Analytics]]** , procédez comme suit.

      1. Saisissez l’identifiant numérique pour la variable [!DNL Google Analytics] compte .

      1. Saisissez l’adresse électronique à utiliser pour accéder aux données de cette source de données. L’adresse électronique doit être enregistrée auprès d’un [!DNL Google] et disposer des autorisations de &quot;lecture et analyse&quot; pour la variable [!DNL Google Analytics] compte . Voir [instructions pour attribuer des autorisations d’utilisateur dans [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Pour vous assurer que uniquement [!DNL Google Analytics] les propriétés et les vues sont disponibles dans Adobe Advertising. connectez-vous à l’aide d’une adresse électronique qui n’a accès qu’à ces propriétés et vues.

         >[!NOTE]
         >
         >Si vous modifiez ultérieurement le mot de passe de ce compte de messagerie, toutes les connexions ouvertes au compte de messagerie sont fermées. Pour reprendre la synchronisation des données, revenez à cette page et [réauthentifier](data-source-reauthenticate.md).

      1. Cochez la case pour autoriser l’Adobe Advertising à accéder aux mesures du compte.

      1. Cliquez sur **[!UICONTROL Authenticate]**.

   1. Dans le [!UICONTROL Account Details] , spécifiez la propriété et l’affichage des mesures à importer. En outre, spécifiez la dimension personnalisée renseignée avec la valeur du paramètre de chaîne de requête &quot;ef_id&quot;.

   1. Dans le [!UICONTROL Import Metrics] , spécifiez les mesures à inclure dans le ou les flux.

      Vous ne pouvez pas supprimer [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces], ou [!UICONTROL Session Duration], qui sont inclus automatiquement. Vous pouvez ajouter jusqu’à 16 mesures ou mesures valides supplémentaires sans données.

      >[!WARNING]
      >
      >[!DNL Google Analytics] autorise jusqu’à 10 mesures dans un seul flux de données. Search, Social et Commerce peuvent prendre en charge jusqu’à deux flux avec un total de 20 mesures, mais l’utilisation d’un deuxième flux double vos appels API à [!DNL Google Analytics]. Si vous disposez de plusieurs mesures, sélectionnez uniquement celles que vous souhaitez utiliser dans les objectifs d’optimisation. En savoir plus sur [Quotas et limites d’appel pour les demandes d’API à [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Dans le [!UICONTROL Metric Tag] , saisissez le nom de la balise à ajouter à chaque mesure pour la source de données.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Post]**.

   La source de données est nommée &quot;NomCompte > NomPropriété > NomVue&quot; et est automatiquement activée. Pour mettre en pause la source de données, voir &quot;[Suspension d’un flux à partir d’une source de données](data-source-pause.md).&quot;

   Les mesures sont disponibles le lendemain de la fin de la synchronisation quotidienne des données, qui commence à 05h00 dans le fuseau horaire de l’annonceur. Une fois les mesures disponibles, elles sont visibles dans [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). Chaque nouvelle propriété de transaction est nommée &quot;&quot;`ga:backEndMetricName_propertyID_viewID`,&quot; où &quot;backEndMetricName&quot; est le nom de mesure utilisé par l’API. Le nom d’affichage de chaque nouvelle propriété de transaction est &quot;`friendlyMetricName_ga:MetricTag`,&quot; où &quot;friendlyMetricName&quot; est le nom de la mesure qui apparaît dans [!DNL Google Analytics] et &quot;MetricTag&quot; correspond à [!UICONTROL Metric Tag] définis dans les paramètres de la source de données.

   Vous pouvez ajouter les mesures directement aux objectifs d’optimisation, de rapports et de vue de gestion de campagne et de portefeuille.

>[!MORELIKETHIS]
>
>* [A propos de la synchronisation [!DNL Google Analytics] mesures de conversion](data-source-about.md)
>* [Conditions préalables à la configuration d’un [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspension de la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier un [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe : Disponible [!DNL Google Analytics] mesures](data-source-ga-metrics.md)
