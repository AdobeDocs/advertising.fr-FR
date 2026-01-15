---
title: Configurer la collecte de données, le transfert de données et la création de rapports
description: Découvrez comment configurer la collecte de données, le transfert de données et la création de rapports.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
source-git-commit: c31a542d2d49602f5942dddf5f7ae41c9d8dfa72
workflow-type: tm+mt
source-wordcount: '1587'
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

### Collecter et envoyer des données d’Adobe Advertising vers Experience Platform Edge Network en tant que jeu de données

1. Dans Experience Platform, [définissez un schéma manuel](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) pour les données que vous souhaitez collecter à l’aide du modèle de données d’expérience (XDM).

   * Dans le [!UICONTROL Schema Details], sélectionnez **[!UICONTROL Experience Event]** comme classe de base du schéma pour capturer les événements du site. Nommez votre schéma, puis cliquez sur **[!UICONTROL Finish]**.

   * Dans le panneau de gauche, ajoutez le groupe de champs [Extension complète Adobe Advertising Cloud ExperienceEvent](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) pour ajouter des champs spécifiques à Adobe Advertising. Incluez au minimum l’objet conversionDetails avec les propriétés `trackingCode` et `trackingIdentities`, qui incluent l’ID [AMO ID et l’ID EF](ids.md). Les autres champs sont facultatifs.

   * (Facultatif) Ajoutez d’autres groupes de champs selon les besoins pour connecter des champs de données supplémentaires aux données Adobe Advertising.

   **Remarque :** vous pouvez créer plusieurs schémas, mais vous ne pouvez utiliser qu’un seul schéma par jeu de données et par flux de données, que vous allez créer dans les étapes suivantes.

1. [Créez un jeu de données](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) basé sur le schéma pour stocker et gérer la collecte de données d’événement.

   * Choisissez l’option pour **[!UICONTROL Create dataset from schema]** et sélectionner votre schéma.

     Adobe Advertising crée des jeux de données supplémentaires pour les données de mesures récapitulatives associées (telles que les valeurs de conversion) et les données de recherche (dimensions/métadonnées de classification, telles que le nom de campagne Adobe Advertising) en fonction de votre jeu de données d’événement. Les données des jeux de données sont renseignées quotidiennement dans Experience Platform.

1. [Créez un flux de données](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) pour le schéma.

   * Pour le paramètre [!UICONTROL Mapping schema] , sélectionnez votre schéma.

   * Ajoutez et activez les services `Adobe Advertising` et `Adobe Experience Platform` au flux de données.

     Ces services permettent à Edge Network de stocker le jeu de données et de l’acheminer vers Adobe Advertising.

   * Pour le paramètre [!UICONTROL Event dataset] , sélectionnez votre jeu de données.

     Chaque flux de données ne peut insérer des données que dans un seul jeu de données.

### Envoyez les données du site web de votre organisation au flux de données Experience Platform

1. Utilisez Experience Platform [balises](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (anciennement appelée [!DNL Launch]) pour générer une balise JavaScript afin d’envoyer les données du site web de votre organisation au flux de données.

   * Créez une propriété de balise, qui est le conteneur de la configuration de balise.

   * Pour votre propriété, [installez l’extension « Adobe Experience Platform Web SDK »](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) à partir du catalogue d’extensions.

     Cette extension envoie des données de vos propriétés web vers Experience Cloud via Experience Platform Edge Network.

     N’utilisez pas l’extension Adobe Advertising.

   * Créez une [version Web SDK personnalisée](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build) :

      * Dans la section [!UICONTROL Custom build components], activez le composant **Advertising**.

        Ce composant inclut tout le code JavaScript nécessaire pour Adobe Advertising dans la balise . Elle ajoute également un paramètre « Advertising » dans les règles de balise (qui sont facultatives) pour définir la manière dont les données publicitaires sont utilisées pour la mesure d’attribution.

        Vous pouvez éventuellement activer des composants supplémentaires selon vos besoins.

      * Dans la section [!UICONTROL SDK Instances] :

         * Dans les paramètres [!UICONTROL Datastreams], sélectionnez le flux de données à utiliser pour chacun de vos environnements web (production, évaluation, développement).

         * (Organisations avec Adobe Advertising DSP uniquement) Dans les paramètres de [[!UICONTROL Adobe Advertising]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising) activez **[!UICONTROL Adobe Advertising DSP]** pour autoriser le suivi des vues publicitaires et spécifiez les annonceurs pour lesquels activer le suivi des vues publicitaires. Vous pouvez éventuellement collecter des identifiants à partir d’identifiants universels.

           Si vos annonceurs ne sont pas répertoriés, saisissez l’ID de l’annonceur pour chaque annonceur.

         * Enregistrez la version.

   * (Facultatif) [Créez des règles](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) selon les besoins pour déterminer à quel moment Web SDK doit envoyer des données à Edge Network.

      * Pour les actions `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)`, utilisez le paramètre [[!UICONTROL Advertising] pour définir comment les données publicitaires sont utilisées pour la mesure de l’attribution](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) Ce paramètre s’avère utile lorsque la règle inclut une séquence de plusieurs actions et n’est disponible que lorsque vous avez sélectionné le composant « [!UICONTROL Advertising] » pour le composant de version personnalisé.

   * Créez des [éléments de données](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) selon vos besoins pour mapper les variables de votre site web à la structure du schéma XDM que vous avez créé précédemment.

1. [Publiez la balise](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) dans un environnement de test dans lequel vous pouvez effectuer une itération sur le développement des balises.

1. Validez la diffusion des jeux de données, puis [publiez la balise dans votre environnement de production en ligne](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Le service informatique de votre entreprise ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé à ce sujet.

## Créer une connexion à vos jeux de données Experience Platform dans Customer Journey Analytics {#dataset-connection}

Pour extraire des données Adobe Advertising de vos jeux de données Experience Platform dans Customer Journey Analytics, procédez comme suit. L’administrateur ou l’administratrice du site de votre entreprise pour Customer Journey Analytics peut effectuer ces tâches.

1. Dans Customer Journey Analytics, [créez une connexion](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) qui inclut vos jeux de données et votre schéma Experience Platform.

   **Remarque :** actuellement, vous devez envoyer des données pour tous les comptes DSP et Search, Social et Commerce à une seule instance Experience Platform et à un seul sandbox.

   * Ajoutez votre jeu de données d’événement Experience Platform (mesures), de résumé (mesures) et de dimensions (classifications/métadonnées).

     Votre équipe a créé le jeu de données d’événement et Adobe Advertising les jeux de données de résumé et de dimensions en fonction de votre jeu de données d’événement.

     Vous pouvez éventuellement inclure des jeux de données supplémentaires selon vos besoins.

   * Mappez le jeu de données des dimensions au jeu de données des événements :

      1. Ouvrez les paramètres du jeu de données de dimension.

         L’en-tête de la page des paramètres est « [!UICONTROL Lookup Dataset] », ce qui indique que vous pouvez joindre votre jeu de données de dimensions à l’un de vos jeux de données spécifiques aux mesures.

      1. Dans la section [!UICONTROL Adobe Advertising Dimensions] , mappez le jeu de données des dimensions au jeu de données des événements :

         1. Pour le champ [!UICONTROL Key] , sélectionnez le champ à utiliser comme clé pour le jeu de données des dimensions : `Adobe Advertising ID` (qui est identique au champ `trackingCode` dans le schéma).

         1. Pour le champ [!UICONTROL Matching key] , sélectionnez le champ à utiliser comme clé correspondante pour le jeu de données d’événements. Les noms de champ disponibles incluent le nom du jeu de données entre parenthèses. Par exemple, si vous mappez votre jeu de données de dimensions à votre jeu de données d’événements, sélectionnez `Tracking Code (Event datasets)`.

         Plus tard, vous mapperez également le jeu de données d’événements au jeu de données de résumé lorsque vous configurerez votre ou vos vue(#cja-data-views) de données.

1. Au bout de quelques heures, vérifiez que les données sont disponibles dans Customer Journey Analytics.

   1. Dans Customer Journey Analytics, accédez à **[!UICONTROL Connections]** et sélectionnez votre connexion.

   1. Dans la liste des jeux de données affichée, vérifiez que le rapport « [!UICONTROL Number of Records] » indique que des données ont été ajoutées.

## Configurer des vues de données dans Customer Journey Analytics {#cja-data-views}

Dans Customer Journey Analytics, créez une ou plusieurs vues de données pour définir les mesures et dimensions de la création de rapports. Un analyste web peut effectuer ces tâches.

1. Dans Customer Journey Analytics, [créez une vue de données](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configurez la vue pour inclure les informations suivantes.

   * Si vous disposez d’un compte Adobe Analytics, utilisez le [!UICONTROL Time Zone] correspondant à votre compte [!DNL Analytics] dans la section [!UICONTROL Calendar] de l’onglet [!UICONTROL Configure] .

   * Dans l’onglet [!UICONTROL Components] :

      * Ajoutez vos dimensions, événements et jeux de données de résumé.

      * Choisissez des mesures à partir de votre jeu de données d’événements (mesures) et de vos jeux de données de dimensions (classifications/métadonnées) à inclure dans la vue de données.

        Vous avez déjà joint ces deux jeux de données dans la connexion que vous avez créée dans la [dernière procédure](#dataset-connection).

      * Joignez le jeu de données d’événements au jeu de données de résumé, qui n’a encore été joint à rien :

         * Pour chaque dimension contenant des données récapitulatives que vous souhaitez rendre disponibles dans Customer Journey Analytics, [créez un champ dérivé](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

           Par exemple, pour afficher les données récapitulatives des campagnes, créez un champ dérivé pour la dimension `Adobe Advertising Campaign`.

           Vous lierez les deux jeux de données à l’aide de la clé correspondante `trackingCode` (qui est le champ de schéma pour l’Adobe Advertising ID).

            * Dans la section [!UICONTROL Lookup] du créateur de règles dérivées :

               * Pour le champ **[!UICONTROL Value]** , sélectionnez « [!UICONTROL Tracking Code] » dans le jeu de données Résumé des mesures .

               * Pour le champ **[!UICONTROL Lookup dataset]** , sélectionnez le jeu de données des dimensions (par exemple, « Classification Adobe Advertising »).

               * Pour le champ **[!UICONTROL Matching Key]** , sélectionnez « [!UICONTROL Tracking Code] » dans le jeu de données de classification.

               * Pour le champ **[!UICONTROL Values to return]** , sélectionnez la dimension (par exemple « [!UICONTROL Adobe Advertising Campaign] ») dans le jeu de données de classification.

           Le nom du champ dérivé est ajouté avec « (DF) », par exemple `Adobe Advertising Campaign(DF)`.

         * Pour chaque champ dérivé :

            * Dans la section [!UICONTROL Included components] , ajoutez le champ dérivé.

              Deux noms sont désormais répertoriés pour la même dimension (par exemple, « Adobe Advertising Campaign(DF) » (le champ dérivé) et « Adobe Advertising Campaign » (le champ du jeu de données de résumé).

            * Sélectionnez la dimension dans le jeu de données de résumé (par exemple, « Adobe Advertising Campaign ») et modifiez les paramètres du jeu de données.

              Les paramètres s’ouvrent à droite.

               * Dans la section Synthèse du groupe de données , sélectionnez l’option à **[!UICONTROL Create grouping]**.

               * Pour le champ **[!UICONTROL Dimension]** , sélectionnez le champ dérivé (qui est ajouté avec « (DF) », tel que « Adobe Advertising Campaign(DF) »).

               * Sélectionnez l’option à **[!UICONTROL Hide in reporting]**, ce qui masque le nom du champ dérivé dans Workspace.

## Configurer des rapports et des visualisations dans Customer Journey Analytics Workspace {#cja-reports}

Dans Customer Journey Analytics Workspace, procédez comme suit pour configurer des rapports et des visualisations. Un analyste web peut effectuer ces tâches.

1. [Créez un projet](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) dans Workspace pour créer des rapports et des visualisations en fonction des dimensions et des mesures configurées dans la vue de données.

1. (Si vous disposez de données provenant de [!DNL Google Ads] ou [!DNL Microsoft Advertising]) Créez un rapport des conversions suivies par l’éditeur à l’aide de champs pour les mesures spécifiques au réseau publicitaire, qui sont regroupées sous la forme `googleConversions` et `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Aperçu](overview.md)
>* [Conditions préalables](prerequisites.md)
>* [ID Adobe Advertising utilisés par  [!DNL Customer Journey Analytics]](ids.md)
>* [Mesures et dimensions Adobe Advertising dans Customer Journey Analytics](advertising-data-in-cja.md)
>* [Collecter des données historiques pour les identifiants AMO et EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* Guide de [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Guide de l’utilisateur pour les utilisateurs d’Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
