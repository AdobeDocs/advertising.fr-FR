---
title: Set up data collection, data transfer, and reporting
description: Learn how to set up data collection, data transfer, and reporting.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1792
ht-degree: 0%

---

# Set up data collection, data transfer, and reporting

*Fonction Beta*

The following tasks are required to view Advertising Cloud data in Customer Journey Analytics.

1. (Your organization&#39;s web analyst; optional) [Collect historical data for AMO IDs and EF IDs](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   This step is applicable only for advertisers with [!DNL Analytics for Advertising].

1. (Your organization&#39;s site administrator for Adobe Experience Platform) [Set up data collection in Experience Platform and implement conversion tracking tags](#data-collection).

1. (Your organization&#39;s site administrator for Customer Journey Analytics) [Create a connection to your Experience Platform datasets in Customer Journey Analytics](#dataset-connection).

1. (Your organization&#39;s web analyst) [Set up data views in Customer Journey Analytics](#cja-data-views).

1. (Your organization&#39;s web analyst) [Set up reports and visualizations in Customer Journey Analytics Workspace](#cja-reports).

The following sections include the detailed procedures, which include the tasks and settings required for the integration but do not explain all features available within the workflows. See the linked resources for full information.

## Set up data collection in Adobe Experience Platform and on your website {#data-collection}

The following tasks are required to set up data collection in Experience Platform and implement conversion tracking tags. Your organization&#39;s site administrator for Experience Platform can perform these tasks, but your organization&#39;s IT department may need to help with deploying tracking tags.

### Collect and send data from Adobe Advertising to Experience Platform Edge Network as a dataset

1. In Experience Platform, [define a manual schema](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) for the data you want to collect using the Experience Data Model (XDM).

   * In the [!UICONTROL Schema Details], select **[!UICONTROL Experience Event]** as the base class for the schema to capture site events. Name your schema and click **[!UICONTROL Finish]**.

   * In the left panel, add the field group [Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) to add fields specific to Adobe Advertising. At a minimum, include the conversionDetails object with the `trackingCode` and `trackingIdentities` properties, which include the [AMO ID and EF ID](ids.md). The other fields are optional.

   * (Optional) Add additional field groups as needed to connect additional data fields to Adobe Advertising data.

   **Note:** You can create multiple schemas, but you can use only one schema per dataset and per datastream, which you&#39;ll create in the following steps.

1. [Create a dataset](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) based on the schema to store and manage the collection of event data.

   * Choose the option to **[!UICONTROL Create dataset from schema]** and select your schema.

     Adobe Advertising creates additional datasets for the related summary metrics data (such as conversion values) and lookup data (dimensions/classification metadata, such as Adobe Advertising campaign name) based on your event dataset. Data for the datasets is populated in Experience Platform daily.

1. [Create a datastream](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) for the schema.

   * For the [!UICONTROL Mapping schema] setting, select your schema.

   * Ajoutez et activez les services `Adobe Advertising` et `Adobe Experience Platform` au flux de données.

     Ces services permettent à Edge Network de stocker le jeu de données et de l’acheminer vers Adobe Advertising.

   * Pour le paramètre [!UICONTROL Event dataset] , sélectionnez votre jeu de données.

     Chaque flux de données ne peut insérer des données que dans un seul jeu de données.

### Envoyez les données du site web de votre organisation au flux de données Experience Platform

1. Utilisez Experience Platform [balises](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (anciennement appelée [!DNL Launch]) pour générer une balise JavaScript afin d’envoyer les données du site web de votre organisation au flux de données.

   * Créez une propriété de balise, qui est le conteneur de la configuration de balise.

   * Pour votre propriété, [installez l’extension « Adobe Experience Platform Web SDK »](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) à partir du catalogue d’extensions.

     Cette extension envoie des données de vos propriétés web vers Adobe CX Enterprise via Experience Platform Edge Network.

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

1. [Publish the tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) to a test environment in which you can iterate on the development of tags.

1. Validate delivery of the datasets, and then [publish the tag to your live production environment](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Your organization&#39;s IT department or other group may need to schedule, or be informed about, the tag deployment.

## Create a connection to your Experience Platform datasets in Customer Journey Analytics {#dataset-connection}

Follow these steps to pull Adobe Advertising data from your Experience Platform datasets into Customer Journey Analytics. Your organization&#39;s site administrator for Customer Journey Analytics can perform these tasks.

1. In Customer Journey Analytics, [create a connection](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) that includes your Experience Platform datasets and schema.

   **Note:** Currently, you must send data for all DSP and Search, Social, &amp; Commerce accounts to a single Experience Platform instance and sandbox.

   * Add your Experience Platform event (metrics) dataset, summary (metrics) dataset, and dimensions (classifications/metadata) dataset.

     Your team created the event dataset, and Adobe Advertising created the summary and dimensions datasets based on your event dataset.

     You can optionally include additional datasets as needed.

   * Map the dimensions dataset to the events dataset:

      1. Open the settings for the dimension dataset.

         The heading on the settings page is &quot;[!UICONTROL Lookup Dataset],&quot; which indicates that you can join your dimensions dataset with one of your metric-specific datasets.

      1. In the [!UICONTROL Adobe Advertising Dimensions] section, map the dimensions dataset to the events dataset:

         1. For the [!UICONTROL Key] field, select the field to use as the key for the dimensions dataset: `Adobe Advertising ID` (which is same as the `trackingCode` field in the schema).

         1. For the [!UICONTROL Matching key] field, select the field to use as the matching key for the events dataset. The available field names include the dataset name in parentheses. For example, if you&#39;re mapping your dimensions dataset to your events dataset, select `Tracking Code (Event datasets)`.

         Later, you&#39;ll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).

1. After a couple of hours, verify that the data is available in Customer Journey Analytics.

   1. In Customer Journey Analytics, go to **[!UICONTROL Connections]** and select your connection.

   1. In the list of data sets displayed, verify that the &quot;[!UICONTROL Number of Records]&quot; report shows that data was added.

## Set up data views in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics, create one or more data views to define the metrics and dimensions for reporting. Un analyste web peut effectuer ces tâches.

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
>* [Adobe Advertising ID utilisés par  [!DNL Customer Journey Analytics]](ids.md)
>* [Mesures et dimensions Adobe Advertising dans Customer Journey Analytics](advertising-data-in-cja.md)
>* [Collecter des données historiques pour les ID AMO et les ID EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* Guide de [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Guide de l’utilisateur pour les utilisateurs d’Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
