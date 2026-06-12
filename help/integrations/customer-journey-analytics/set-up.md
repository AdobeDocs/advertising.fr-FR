---
title: Configurer la collecte de données, le transfert de données et la création de rapports
description: Découvrez comment configurer la collecte de données, le transfert de données et la création de rapports.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: c62a18194544bcbe98117b86eccb1b5e2740999c
workflow-type: tm+mt
source-wordcount: 1804
ht-degree: 0%

---

# Configurer la collecte de données, le transfert de données et la création de rapports

*Annonceurs avec Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

*Annonceurs sans [!DNL Analytics for Advertising] uniquement*

Les tâches suivantes sont requises pour échanger des données de manière native entre Adobe Advertising et Customer Journey Analytics à l’aide de [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr). Le transfert et l’attribution des données commencent après le lancement ; aucune donnée historique n’est incluse.

1. (Analyste web de votre entreprise, facultatif) [Collectez des données historiques pour les ID AMO et les ID EF](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Cette étape s’applique uniquement aux annonceurs qui disposent d’[!DNL Analytics for Advertising].

2. (Administration de sites de votre entreprise pour Adobe Experience Platform) [Configurez la collecte de données dans Experience Platform et implémentez les balises de suivi des conversions](#data-collection).

3. (Administrateur de site de votre organisation pour Customer Journey Analytics) [Créez une connexion à vos jeux de données Experience Platform dans Customer Journey Analytics](#dataset-connection).

4. (Analyste web de votre entreprise) [Configurez des vues de données dans Customer Journey Analytics](#cja-data-views).

5. (Analyste web de votre entreprise) [Configurez des rapports et des visualisations dans Customer Journey Analytics Workspace](#cja-reports).

Les sections suivantes incluent les procédures détaillées, notamment les tâches et les paramètres requis pour l’intégration, mais n’expliquent pas toutes les fonctionnalités disponibles dans les workflows. Consultez les ressources liées pour obtenir des informations complètes.

## Configurer la collecte de données dans Adobe Experience Platform et sur votre site web {#data-collection}

Les tâches suivantes sont nécessaires pour configurer la collecte de données dans Experience Platform et implémenter les balises de suivi des conversions. L’administrateur du site de votre entreprise pour Experience Platform peut effectuer ces tâches, mais le service informatique de votre entreprise peut avoir besoin d’aide pour déployer les balises de suivi.

### Collecter et envoyer des données d’Adobe Advertising vers Experience Platform Edge Network en tant que jeu de données

Cette procédure comprend la création d’un schéma. Vous pouvez éventuellement modifier un schéma existant à la place ; dans ce cas, vous n’avez pas besoin de créer un jeu de données ou un flux de données.

1. Dans Experience Platform, [définissez un schéma manuel](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/ui/resources/schemas) pour les données que vous souhaitez collecter à l’aide du modèle de données d’expérience (XDM).

   * Dans le [!UICONTROL Schema Details], sélectionnez **[!UICONTROL Experience Event]** comme classe de base du schéma pour capturer les événements du site. Nommez votre schéma, puis cliquez sur **[!UICONTROL Finish]**.

   * Dans le panneau de gauche, ajoutez le groupe de champs [Extension complète Adobe Advertising Cloud ExperienceEvent](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) pour ajouter des champs spécifiques à Adobe Advertising. Incluez au minimum l’objet conversionDetails avec les propriétés `trackingCode` et `trackingIdentities`, qui incluent l’ID [AMO ID et l’ID EF](ids.md). Les autres champs sont facultatifs.

   * (Facultatif) Ajoutez d’autres groupes de champs selon les besoins pour connecter des champs de données supplémentaires aux données Adobe Advertising.

   **Remarque :** vous pouvez créer plusieurs schémas, mais vous ne pouvez utiliser qu’un seul schéma par jeu de données et par flux de données, que vous allez créer dans les étapes suivantes.

1. [Créez un jeu de données](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/create) basé sur le schéma pour stocker et gérer la collecte de données d’événement. Il s’agira de votre *jeu de données d’événement*. Si vous modifiez un schéma existant avec un jeu de données, vous pouvez ignorer cette étape.

   * Choisissez l’option pour **[!UICONTROL Create dataset from schema]** et sélectionner votre schéma.

     En fonction de votre jeu de données d’événement, Adobe Advertising crée deux jeux de données supplémentaires : 1\) un *jeu de données de résumé* avec les données de résumé associées (telles que les clics et les impressions) et 2\) un *jeu de données de recherche* (avec des dimensions/métadonnées de classification, telles que le nom de la campagne Adobe Advertising). Les données des jeux de données sont renseignées quotidiennement dans Experience Platform.

   >[!TIP]
   >
   >Créez d’abord un jeu de données d’événement factice pour valider le flux de données avant d’utiliser un jeu de données de production.

1. [Créez un flux de données](https://experienceleague.adobe.com/fr/docs/experience-platform/datastreams/configure) pour spécifier où envoyer des données à partir de votre site web ou de votre application et comment gérer les données entrantes.

   * Pour le paramètre [!UICONTROL Mapping schema] , sélectionnez votre schéma.

   * Ajoutez et activez les services `Adobe Advertising` et `Adobe Experience Platform` au flux de données.

     Le service [!UICONTROL Adobe Advertising] permet d’associer les expositions aux publicités à la payload et le [!UICONTROL Adobe Experience Platform] permet à Edge Network de stocker le jeu de données et de l’acheminer vers Adobe Advertising.

   * Pour le paramètre [!UICONTROL Event dataset] , sélectionnez votre jeu de données d’événement.

     Chaque flux de données ne peut insérer des données que dans un seul jeu de données.

### Envoyez les données du site web de votre organisation au flux de données Experience Platform

Utilisez l’extension Adobe Experience Platform Web SDK dans Adobe Tags pour envoyer les données du site web de votre organisation au flux de données Experience Platform.

>[!NOTE]
>
>Seules les balises Adobe sont prises en charge. La prise en charge n’est pas disponible pour Experience Platform Web SDK (`alloy.js`) autonome ou pour les gestionnaires de balises tiers.

1. Utilisez Experience Platform [balises](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/home) (anciennement appelée [!DNL Launch]) pour générer une balise JavaScript afin d’envoyer les données du site web de votre organisation au flux de données.

   * Créez une propriété de balise, qui est le conteneur de la configuration de balise.

   * Pour votre propriété, [installez l’extension « Adobe Experience Platform Web SDK »](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) à partir du catalogue d’extensions.

     Cette extension envoie des données de vos propriétés web à Adobe CX Enterprise via Experience Platform Edge Network.

     N’utilisez pas l’extension Adobe Advertising.

   * Créez une [version Web SDK personnalisée](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build) :

      * Dans la section [!UICONTROL Custom build components], activez le composant **Advertising**.

        Ce composant inclut tout le code JavaScript nécessaire pour Adobe Advertising dans la balise . Il est requis pour les clients Advertising DSP et Advertising Search, Social et Commerce. Le composant ajoute également un paramètre « Advertising » dans les règles de balise (qui sont facultatives) pour définir la manière dont les données publicitaires sont utilisées pour la mesure d’attribution.

        Vous pouvez éventuellement activer des composants supplémentaires selon vos besoins.

      * Dans la section [!UICONTROL SDK Instances] :

         * Dans les paramètres [!UICONTROL Datastreams], sélectionnez le flux de données à utiliser pour chacun de vos environnements web (production, évaluation, développement).

         * (Organisations avec Adobe Advertising DSP uniquement) Dans les paramètres de [[!UICONTROL Adobe Advertising]](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising) activez **[!UICONTROL Adobe Advertising DSP]** pour autoriser le suivi des vues publicitaires et spécifiez les annonceurs pour lesquels activer le suivi des vues publicitaires. Vous pouvez éventuellement collecter des identifiants à partir d’identifiants universels en ajoutant l’identifiant de partenaire ID5 de votre organisation et/ou le chemin d’accès au code JavaScript [!DNL LiveRamp RampID] de votre organisation (ats.js).

           Si vos annonceurs ne sont pas répertoriés, saisissez l’ID de l’annonceur pour chaque annonceur. Si nécessaire, demandez les identifiants à l’équipe chargée de votre compte Adobe.

         * Enregistrez la version.

   * (Facultatif) [Créez des règles](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/ui/rules) selon les besoins pour déterminer à quel moment Web SDK doit envoyer des données à Edge Network.

      * Pour les actions `[sendEvent](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)`, utilisez le paramètre [[!UICONTROL Advertising] pour définir comment les données publicitaires sont utilisées pour la mesure de l’attribution](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) Ce paramètre s’avère utile lorsque la règle inclut une séquence de plusieurs actions et n’est disponible que lorsque vous avez sélectionné le composant « [!UICONTROL Advertising] » pour le composant de version personnalisé.

   * Créez des [éléments de données](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/ui/data-elements) selon vos besoins pour mapper les variables de votre site web à la structure du schéma XDM que vous avez créé précédemment.

1. [Publiez la balise](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/publish/publishing-flow) dans un environnement de test dans lequel vous pouvez effectuer une itération sur le développement des balises.

1. [Vérifiez l’activité pour chacun de vos trois jeux de données](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/user-guide#view-datasets) afin de valider la diffusion.

1. [Publiez la balise dans votre environnement de production actif](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/publish/publishing-flow).

   Le service informatique de votre entreprise ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé à ce sujet.

## Créer une connexion à vos jeux de données Experience Platform dans Customer Journey Analytics {#dataset-connection}

Pour extraire des données Adobe Advertising de vos jeux de données Experience Platform dans Customer Journey Analytics, procédez comme suit. L’administrateur ou l’administratrice du site de votre entreprise pour Customer Journey Analytics peut effectuer ces tâches.

Vous pouvez également modifier une connexion existante avec les mêmes informations.

1. Dans Customer Journey Analytics, [créez ou modifiez une connexion](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-connections/create-connection) qui inclut vos jeux de données et votre schéma Experience Platform.

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * Vérifiez que le bon sandbox est sélectionné.

   * Calculez le nombre moyen d’événements quotidiens (moins d’un million pour la plupart des organisations).

   * Ajoutez votre jeu de données de mesures d’événement Experience Platform (type : `Event`), votre jeu de données de mesures de résumé d’événement <!-- Adobe Advertising --> (type : `Event`) et votre jeu de données de dimensions <!-- Adobe Advertising --> (classifications/métadonnées) (type : `Lookup`).

     Votre équipe a créé le jeu de données d’événement et Adobe Advertising les jeux de données de résumé et de dimensions en fonction de votre jeu de données d’événement.

     Vous pouvez éventuellement inclure des jeux de données supplémentaires selon vos besoins.

   * Configurez les paramètres du jeu de données :

      * Pour les paramètres [!UICONTROL Event Dataset] :

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Use primary identity namespace]:** Activer le paramètre

         * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->

         * **[!UICONTROL Import all new data]:** Activer le paramètre

      * Pour les paramètres [!UICONTROL Lookup Dataset], mappez le jeu de données des dimensions au jeu de données des événements :

         * **[!UICONTROL Key]** (champ à utiliser comme clé pour le jeu de données dimensions) : `Tracking Code` (qui est identique au champ `trackingCode` dans le schéma).

         * **[!UICONTROL Matching key]** (champ à utiliser comme clé correspondante pour le jeu de données d’événements) : `Tracking Code (Event datasets)`.<!-- verify this Later, you'll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).  -->

         * **[!UICONTROL Import all new data]:** Activer le paramètre

      * Pour les paramètres [!UICONTROL Metrics Dataset] :

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Timestamp]:** Confirmer la valeur

         * **[!UICONTROL Import all new data]:** Activer le paramètre

1. Dans les trois heures, vérifiez que les données sont disponibles dans Customer Journey Analytics.

   1. Dans Customer Journey Analytics, accédez à **[!UICONTROL Connections]** et sélectionnez votre connexion.

   2. Dans la liste des jeux de données affichée, vérifiez que le rapport « [!UICONTROL Number of Records] » indique que des données ont été ajoutées.

## Configurer des vues de données dans Customer Journey Analytics {#cja-data-views}

Dans Customer Journey Analytics, créez une ou plusieurs vues de données pour définir les mesures et dimensions de la création de rapports. Un analyste web peut effectuer ces tâches.

1. Dans Customer Journey Analytics, [créez une vue de données](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Configurez la vue pour inclure les informations suivantes.

   * Si vous disposez d’un compte Adobe Analytics, utilisez le [!UICONTROL Time Zone] correspondant à votre compte [!DNL Analytics] dans la section [!UICONTROL Calendar] de l’onglet [!UICONTROL Configure] .

   * Dans l’onglet [!UICONTROL Components] :

      * Ajoutez votre jeu de données de recherche (avec les dimensions/données de classification), votre jeu de données d’événement (avec vos données au niveau de l’événement) et votre jeu de données de résumé (avec vos autres mesures, telles que les clics).

      * Choisissez des mesures à partir de votre jeu de données d’événement et de votre jeu de données de recherche à inclure dans la vue de données.

      * Recherchez « [!UICONTROL Tracking Code] » (qui fait partie du jeu de données d’événement avec le chemin de schéma `_experience.adcloud.conversionDetails.trackingCode`). <!-- and do what with it? Add it? Or is that what you --> Définissez **[!UICONTROL Persistence]** sur *[!UICONTROL Most Recent]*.

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## Configurer des rapports et des visualisations dans Customer Journey Analytics Workspace {#cja-reports}

Dans Customer Journey Analytics Workspace, procédez comme suit pour configurer des rapports et des visualisations. Un analyste web peut effectuer ces tâches.

1. [Créez un projet](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) dans Workspace pour créer des rapports et des visualisations en fonction des dimensions et des mesures configurées dans la vue de données.

Vous pouvez classer les mesures récapitulatives et les données d’événement à l’aide de la même dimension dans un tableau à structure libre.

1. (Si vous disposez de données provenant de [!DNL Google Ads] ou [!DNL Microsoft Advertising]) Créez un rapport des conversions suivies par l’éditeur à l’aide de champs pour les mesures spécifiques au réseau publicitaire, qui sont regroupées sous la forme `googleConversions` et `microsoftConversions`.

>[!TIP]
>
>Les événements récapitulatifs ajoutent généralement une petite quantité de données supplémentaires aux rapports, telles que quelques événements supplémentaires, une session supplémentaire par jour ou une personne supplémentaire par rapport. Ces ajouts sont négligeables par rapport aux événements web standard. Cependant, vous pouvez filtrer ces données d’événement de résumé supplémentaires en excluant les données du `00000000-0000-0000-0000-000000000000` ID de personne factice.
>![Exemple d’exclusion de données à l’aide d’un ID &#x200B;](/help/integrations/assets/cja-report-with-person-id.png " personneExemple d’exclusion de données à l’aide d’un ID de personne")

![Comment vos jeux de données peuvent-ils apparaître dans Customer Journey Analytics &#x200B;](/help/integrations/assets/cja-report-example.png "Comment vos jeux de données peuvent-ils apparaître dans Customer Journey Analytics ")

>[!MORELIKETHIS]
>
>* [Aperçu](overview.md)
>* [Conditions préalables](prerequisites.md)
>* [Adobe Advertising ID utilisés par  [!DNL Customer Journey Analytics]](ids.md)
>* [Mesures et dimensions Adobe Advertising dans Customer Journey Analytics](advertising-data-in-cja.md)
>* [Collecter des données historiques pour les ID AMO et les ID EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* Guide de [&#128279;](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Guide de l’utilisateur pour les utilisateurs d’Adobe Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
