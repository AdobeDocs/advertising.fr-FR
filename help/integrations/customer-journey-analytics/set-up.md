---
title: Configurer la collecte de données, le transfert de données et la création de rapports
description: Découvrez comment configurer la collecte de données, le transfert de données et la création de rapports.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 2d6cba8d5a3d966b272c5048404ac8fdf0185b74
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# Configurer la collecte de données, le transfert de données et la création de rapports

*Fonction Beta*

Les tâches suivantes sont requises pour afficher les données Advertising Cloud dans Customer Journey Analytics.

1. (Analyste web de votre entreprise, facultatif) [Collectez des données historiques pour les ID AMO et les ID EF](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Cette étape s’applique uniquement aux annonceurs qui disposent d’[!DNL Analytics for Advertising].

1. (Administration de sites de votre entreprise pour Adobe Experience Platform) [Configurez la collecte de données dans Experience Platform et implémentez les balises de suivi des conversions](#data-collection).

1. (Administrateur de site de votre organisation pour Customer Journey Analytics) [Créez une connexion à vos jeux de données Experience Platform dans Customer Journey Analytics](#dataset-connection).

1. (Analyste web de votre entreprise) [Configurez des vues de données dans Customer Journey Analytics](#cja-data-views).

1. (Analyste web de votre entreprise) [Configurez des rapports et des visualisations dans Customer Journey Analytics Workspace](#cja-reports).

Les sections suivantes incluent les procédures détaillées, notamment les tâches et les paramètres requis pour l’intégration, mais n’expliquent pas toutes les fonctionnalités disponibles dans les workflows. Consultez les ressources liées pour obtenir des informations complètes.

## Configurer la collecte de données dans Adobe Experience Platform et sur votre site web {#data-collection}

Les tâches suivantes sont nécessaires pour configurer la collecte de données dans Experience Platform et implémenter les balises de suivi des conversions. L’administrateur du site de votre entreprise pour Experience Platform peut effectuer ces tâches, mais le service informatique de votre entreprise peut avoir besoin d’aide pour déployer les balises de suivi.

1. Collectez et envoyez des données d’Adobe Advertising vers Experience Platform Edge Network en tant que jeu de données :

   1. Dans Experience Platform, [définissez un schéma manuel](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/ui/resources/schemas) pour les données que vous souhaitez collecter à l’aide du modèle de données d’expérience (XDM).

      * Dans le [!UICONTROL Schema Details], sélectionnez **[!UICONTROL Experience Event]** comme classe de base du schéma pour capturer les événements du site. Nommez votre schéma, puis cliquez sur **[!UICONTROL Finish]**.

      * Dans le panneau de gauche, ajoutez le groupe de champs `Adobe Advertising Cloud ExperienceEvent Full Extension` pour ajouter des champs spécifiques à Adobe Advertising.<!-- Add link once published --> Au minimum, incluez l’objet conversionDetails avec les propriétés `trackingCode` et `trackingIdentities`, qui incluent l’[AMO ID et l’EF ID](ids.html). Les autres champs sont facultatifs.

      * (Facultatif) Ajoutez d’autres groupes de champs selon les besoins pour connecter des champs de données supplémentaires aux données Adobe Advertising.

      **Remarque :** vous pouvez créer plusieurs schémas, mais vous ne pouvez utiliser qu’un seul schéma par jeu de données et par flux de données, que vous allez créer dans les étapes suivantes.

   1. [Créez un jeu de données](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/create) basé sur le schéma pour stocker et gérer la collecte de données d’événement.

      * Choisissez l’option pour **[!UICONTROL Create dataset from schema]** et sélectionner votre schéma.

        Adobe Advertising crée des jeux de données supplémentaires pour les données de mesures récapitulatives associées (telles que les valeurs de conversion) et les données de recherche (dimensions/métadonnées de classification, telles que le nom de campagne Adobe Advertising) en fonction de votre jeu de données d’événement. Les données des jeux de données sont renseignées quotidiennement dans Experience Platform.

   1. [Créez un flux de données](https://experienceleague.adobe.com/fr/docs/experience-platform/datastreams/configure) pour le schéma.

      * Pour le paramètre [!UICONTROL Mapping schema] , sélectionnez votre schéma.

      * Ajoutez et activez les services `Adobe Advertising` et `Adobe Experience Platform` au flux de données.

        Ces services permettent à Edge Network de stocker le jeu de données et de l’acheminer vers Adobe Advertising.

      * Pour le paramètre [!UICONTROL Event dataset] , sélectionnez votre jeu de données.

        Chaque flux de données ne peut insérer des données que dans un seul jeu de données.

1. Envoyez les données du site web de votre organisation au flux de données Experience Platform :

   1. Utilisez Experience Platform [balises](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/home) (anciennement appelée [!DNL Launch]) pour générer une balise JavaScript afin d’envoyer les données du site web de votre organisation au flux de données.

      * Créez une propriété de balise, qui est le conteneur de la configuration de balise.

      * Pour votre propriété, [installez l’extension « Adobe Experience Platform Web SDK »](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) à partir du catalogue d’extensions.

        Cette extension envoie des données de vos propriétés web vers Experience Cloud via Experience Platform Edge Network.

        N’utilisez pas l’extension Adobe Advertising.

      * Créez une version de Web SDK personnalisée :

         * Dans la section [!UICONTROL Custom build components], activez le composant **Advertising**.

           Ce composant inclut tout le code JavaScript nécessaire pour Adobe Advertising dans la balise . Elle ajoute également un paramètre « Advertising » dans les règles de balise (qui sont facultatives) pour définir la manière dont les données publicitaires sont utilisées pour la mesure d’attribution.

           Vous pouvez éventuellement activer des composants supplémentaires selon vos besoins.

         * Dans la section [!UICONTROL SDK Instances] :

            * Dans les paramètres [!UICONTROL Datastreams], sélectionnez le flux de données à utiliser pour chacun de vos environnements web (production, évaluation, développement).

            * (Organisations avec Adobe Advertising DSP uniquement) Dans les paramètres [!UICONTROL Adobe Advertising] :

               * Activez le paramètre **[!UICONTROL Adobe Advertising DSP]** pour activer le suivi des affichages publicitaires.

               * Spécifiez les annonceurs pour lesquels activer le suivi des affichages publicitaires.

               * (Facultatif) Saisissez l’ID5 du partenaire de votre organisation pour collecter les ID.

               * (Facultatif) Saisissez le chemin d’accès du code JavaScript [!DNL LiveRamp RampID] de votre organisation (ats.js) pour collecter les identifiants.

            * Enregistrez la version.

      * (Facultatif) [Créez des règles](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/ui/rules) selon les besoins pour déterminer à quel moment Web SDK doit envoyer des données à Edge Network.

         * Pour le paramètre [!UICONTROL Advertising] , définissez la manière dont les données publicitaires sont utilisées pour la mesure d’attribution. Ce paramètre s’avère utile lorsque la règle inclut une séquence de plusieurs actions et n’est disponible que lorsque vous avez sélectionné le composant « [!UICONTROL Advertising] » pour le composant de version personnalisé. Les options incluent :

           *Automatique :* permet d’utiliser les données publicitaires pour mesurer l’attribution des annonces sur l’action `sendEvent` actuelle en fonction des données du cache. Dans ce cas, l’événement d’exposition à la publicité se déclenche lorsqu’il en a l’occasion et il peut ne pas être disponible pour l’événement actuel. Par exemple, si vous déclenchez un événement de passage en caisse pour un achat et qu’aucune donnée d’exposition aux annonces n’est disponible dans le cache, l’événement de passage en caisse n’est pas attribué à l’exposition aux annonces.

           *Attente :* retarde l’exécution de l’appel jusqu’à ce que les données de publicité soient récupérées avec succès du serveur et résolues, ce qui garantit une mesure d’attribution précise. Par exemple, vous pouvez attendre que l’événement d’exposition aux publicités se résolve avant de déclencher un événement de passage en caisse d’achat. **Remarque :** la résolution des identifiants peut prendre quelques secondes selon le navigateur et le type d’identifiant. Utilisez cette option si l’action `sendEvent` en cours peut prendre en charge quelques secondes de retard.

           *Désactivé :* (valeur par défaut) exclut les données publicitaires de la requête que vous déclenchez, ce qui les rend indisponibles pour l’attribution ou le suivi associé.

           *Fournir un élément de données :* utilisez un élément de données pour inclure ou exclure des données publicitaires lors du chargement de la page. Les valeurs résolues pour l’élément de données peuvent inclure `automatic`, `wait` et `disabled`. Pour plus d’informations, reportez-vous à l’étape suivante.

        Si vous n’utilisez pas de règle pour configurer une action de `sendEvent`, les données de publicité sont envoyées sous la forme d’un événement d’enrichissement d’annonce distinct.

      * Créez des [éléments de données](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/ui/data-elements) selon vos besoins pour mapper les variables de votre site web à la structure du schéma XDM que vous avez créé précédemment.

   1. [Publiez la balise](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/publish/publishing-flow) dans un environnement de test dans lequel vous pouvez effectuer une itération sur le développement des balises.

   1. Validez la diffusion des jeux de données, puis [publiez la balise dans votre environnement de production en ligne](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/publish/publishing-flow).

      Le service informatique de votre entreprise ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé à ce sujet.

## Créer une connexion à vos jeux de données Experience Platform dans Customer Journey Analytics {#dataset-connection}

Pour extraire des données Adobe Advertising de vos jeux de données Experience Platform dans Customer Journey Analytics, procédez comme suit. L’administrateur ou l’administratrice du site de votre entreprise pour Customer Journey Analytics peut effectuer ces tâches.

*Bientôt disponible*

## Configurer des vues de données dans Customer Journey Analytics {#cja-data-views}

Dans Customer Journey Analytics, créez une ou plusieurs vues de données pour définir les mesures et dimensions de la création de rapports. Un analyste web peut effectuer ces tâches.

*Bientôt disponible*

## Configurer des rapports et des visualisations dans Customer Journey Analytics Workspace {#cja-reports}

Dans Customer Journey Analytics Workspace, procédez comme suit pour configurer des rapports et des visualisations. Un analyste web peut effectuer ces tâches.

1. [Créez un projet](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) dans Workspace pour créer des rapports et des visualisations en fonction des dimensions et des mesures configurées dans la vue de données.

1. (Si vous disposez de données provenant de [!DNL Google Ads] ou [!DNL Microsoft Advertising]) Créez un rapport des conversions suivies par l’éditeur à l’aide de champs pour les mesures spécifiques au réseau publicitaire, qui sont regroupées sous la forme `googleConversions` et `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Aperçu](overview.md)
>* [Conditions préalables](prerequisites.md)
>* [ID Adobe Advertising utilisés par  [!DNL Customer Journey Analytics]](ids.md)
>* [Mesures et dimensions Adobe Advertising dans Customer Journey Analytics](advertising-data-in-cja.md)
>* [Collecter des données historiques pour les identifiants AMO et EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* Guide de [Customer Journey Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Guide de l’utilisateur pour les utilisateurs d’Adobe Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
