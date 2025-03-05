---
title: Rapports de performances au niveau de l’expérience
description: Découvrez comment afficher des rapports de performances au niveau de l’expérience.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# Rapports de performances au niveau de l’expérience

*Version bêta fermée*

Vous pouvez afficher des données de performances détaillées pour n’importe quelle expérience.

## Données dans les rapports de performances au niveau de l’expérience

La vue Rapport inclut les données suivantes :

* Onglet **Aperçu** : aperçu des performances de l’ensemble de l’expérience, notamment :

   * **Performance globale** section :

   * **Performances globales** : nombre total d’impressions, de clics, de taux de clic publicitaire (CTR), de conversions d’affichage publicitaire et de conversions de clics publicitaires pour une seule mesure de conversion. <!-- Just one, or can you select multiple? And I don't see this as of 2/8:  You can optionally combine two metrics at a time into a single chart. -->

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

   * **Taux par défaut** : (expériences avec ciblage d’arborescence de décision uniquement) nombre d’impressions provenant de contenus publicitaires ciblés, de contenus publicitaires génériques sans cible ou ciblés sur « Tout le monde » et du contenu publicitaire par défaut pour l’expérience.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * Section **Répartition des performances** :

      * **Performance régionale :* : mesures individuelles par lieu géographique.

        <!-- You can optionally do the following:
    
      * Click a metric name (such as [!UICONTROL Impressions]) to view that metric.

      * Select the region in the **[!UICONTROL Region]** menu.
      
      -->

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Performances de l’appareil :** mesures individuelles par type d’appareil, système d’exploitation et navigateur. Si vous le souhaitez, cliquez sur la valeur de n’importe quelle catégorie d’appareils pour afficher la liste des <!-- NN --> principaux contenus publicitaires diffusés selon ce critère.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Onglet Performances créatives*** : présentation des performances par élément créatif et lot ou balise publicitaire, notamment :

   * **Contenu créatif** sous-onglet : nombre total d’impressions, de clics et de CTR pour chaque contenu créatif de l’expérience.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

     <!--

     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each creative. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report. [Find out about this:  ..., and total conversions for specified conversion metricsYour conversion metrics are combined into one Conversions column set unless you have made individual metric column sets available within Advertising Cloud Search.]

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each creative. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

   * **Bundles/Balises** sous-onglet : nombre total d’impressions, de clics et de CTR pour des lots individuels (expériences avec ciblage d’arbre de décision) ou des balises d’annonce (expériences sans ciblage d’arbre de décision) dans l’expérience.

     <!--
   
     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each bundle. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions  and click-through conversions (using on the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each ad tag. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

## Affichage des rapports de performances pour une expérience

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facultatif) [Personnaliser la vue](/help/creative/introduction/customize-data-views.md) pour inclure des expériences spécifiques.

1. Sélectionnez l’expérience :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Reports]**.

   * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Reports]**.

   L’onglet [!UICONTROL Overview] s’ouvre.

1. (Facultatif) Dans la barre d’outils supérieure droite, spécifiez la période, la règle d’attribution de conversion et les conversions signalées dans tous les rapports de performances :

   * (Facultatif) Pour modifier la période des données de performances, choisissez une option dans le menu de date :

      * Pour spécifier une période prédéfinie, sélectionnez le rapport : (*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today]ou* *[!UICONTROL Yesterday]*.

      * Pour spécifier une période personnalisée, spécifiez les <!-- in the format MM/DD/YYYY or M/D/YYYY,--> de date de début et de fin ou cliquez sur ![icône de calendrier](/help/search-social-commerce/assets/calendar.png) en regard d’un champ et sélectionnez une date.

   * (Facultatif) Pour modifier la règle utilisée pour attribuer des données de conversion dans une série d’événements qui entraînent une conversion, cliquez sur ![Paramètres](/help/creative/assets/settings.png) et modifiez la **[!UICONTROL Attribution Rule]**.

   * (Facultatif) Pour modifier les conversions signalées, cliquez sur ![Paramètres](/help/creative/assets/settings.png) et sélectionnez les noms de conversion dans le menu **[!UICONTROL Conversions]**.&lt;!— Juste un ou plusieurs ? Vérifiez comment ils apparaissent — Je dois voir un annonceur avec plusieurs conversions déjà configurées —>

     Les colonnes de conversion disponibles incluent les conversions disponibles dans Advertising Search, Social et Commerce, que vous soyez ou non client Search, Social et Commerce. Cela peut inclure les mesures de conversion et d’engagement du site synchronisées à partir d’Adobe Analytics lorsque l’annonceur dispose d’[une [!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md). <!--Analytics calculated metrics and advanced calculated metrics aren't available.--> Pour plus d’informations sur l’inclusion des conversions collectées dans les rapports, consultez la rubrique du guide Search, Social et Commerce intitulée « [À propos de la gestion des mesures de conversion d’un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) ».

1. (Dans l’onglet [!UICONTROL Overview] ) :

   * (Facultatif) Dans la section [!UICONTROL Overall Regional Performance], placez le curseur sur un point du graphique pour afficher les données relatives à ce point.

   * (Facultatif) Dans la section [!UICONTROL Regional Performance], effectuez l’une des opérations suivantes :

      * Cliquez sur le nom d’une mesure (tel que [!UICONTROL Impressions]) pour l’afficher.

      * Sélectionnez la région dans le menu [!UICONTROL Region].

      * Placez le curseur sur un pays ou un état pour afficher les données de cette région.

   * (Facultatif) Dans la section [!UICONTROL Device Performance], effectuez l’une des opérations suivantes :

      * Placez le curseur sur la valeur de n’importe quelle catégorie d’appareils pour afficher les données de ce critère.

      * Cliquez sur la valeur de n’importe quelle catégorie d’appareils pour afficher la liste des <!-- NN--> principaux contenus publicitaires diffusés selon ce critère.

1. (Facultatif) Pour afficher les données par élément créatif et par lot ou balise publicitaire, cliquez sur l’onglet **[!UICONTROL Creative Performance]** .

   * Dans le sous-onglet [!UICONTROL Creatives] , vous pouvez effectuer l’une des opérations suivantes :

      * (Facultatif) Pour basculer entre les vues graphique et grille, cliquez respectivement sur ![Graphique](/help/creative/assets/chart-view-button.png "Graphique") et ![Grille](/help/creative/assets/table-view-button.png "Grille").

      * (Facultatif) Dans la vue graphique, placez le curseur sur un point du graphique pour afficher les données relatives à ce point.

      * (Expériences avec ciblage d’arborescence de décision uniquement ; facultatif) Pour ventiler les performances pour chaque cible publicitaire appliquée, activez **[!UICONTROL Split targeting]**.

1. Pour afficher les données par lot (expériences avec ciblage d’arbre de décision) ou balise publicitaire (expériences sans ciblage d’arbre de décision), cliquez sur le sous-onglet **[!UICONTROL Bundles]** . Vous pouvez effectuer l’une des opérations suivantes :

   * (Facultatif) Pour basculer entre les vues graphique et grille, cliquez respectivement sur ![Graphique](/help/creative/assets/chart-view-button.png "Graphique") et ![Grille](/help/creative/assets/table-view-button.png "Grille").

   * (Facultatif) Dans la vue graphique, placez le curseur sur un point du graphique pour afficher les données relatives à ce point.

   * (Expériences avec ciblage d’arborescence de décision uniquement ; facultatif) Pour ventiler les performances pour chaque cible publicitaire appliquée, activez **[!UICONTROL Split targeting]**.

1. (Facultatif) Pour télécharger les données d’un fichier [!DNL Microsoft Excel] au format feuille de calcul (XLSX), cliquez sur ![Télécharger](/help/creative/assets/download.png "Télécharger") dans la barre d’outils.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

>[!MORELIKETHIS]
>
>* [Rapport créatif personnalisé](/help/creative/report-custom-creative.md)
