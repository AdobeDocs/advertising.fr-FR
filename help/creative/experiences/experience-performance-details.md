---
title: Rapports de performances au niveau de l’expérience
description: Découvrez comment afficher des rapports de performances au niveau de l’expérience.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 39e0b8b57fd54e99b09e56ecf9cef753b0c6ea44
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# Rapports de performances au niveau de l’expérience

Vous pouvez afficher des données de performances détaillées pour n’importe quelle expérience.

## Données dans les rapports de performances au niveau de l’expérience

La vue Rapport inclut les données suivantes :

* Onglet **Aperçu** : aperçu des performances de toutes les mesures de conversion pour l’ensemble de l’expérience<!-- Currently, the only metric in the settings list at the top of this main tab is "Select All." --> notamment :

   * **Performance globale** section :

      * **Performances globales** : nombre total d’impressions, de clics, de taux de clics publicitaires (CTR), de conversions d’affichage publicitaire et de conversions de clics publicitaires.

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

      * **Taux par défaut** : (expériences avec ciblage d’arborescence de décision uniquement) nombre d’impressions provenant de contenus publicitaires ciblés, de contenus publicitaires génériques sans cible ou ciblés sur « Tout le monde » et du contenu publicitaire par défaut pour l’expérience.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * Section **Répartition des performances** :

      * **Performance régionale :* : mesures individuelles par lieu géographique.

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Performances de l’appareil :** mesures individuelles par type d’appareil, système d’exploitation et navigateur. Si vous le souhaitez, cliquez sur la valeur de n’importe quelle catégorie d’appareils pour afficher la liste des 10 meilleurs contenus publicitaires diffusés selon ce critère.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Onglet Performances de Creative*** : aperçu des performances par élément créatif et lot ou balise publicitaire, y compris :

   * **Contenu créatif** sous-onglet : nombre total d’impressions, de clics et de CTR pour chaque contenu créatif de l’expérience.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

   * **Bundles/Balises** sous-onglet : nombre total d’impressions, de clics et de CTR pour des lots individuels (expériences avec ciblage d’arbre de décision) ou des balises d’annonce (expériences sans ciblage d’arbre de décision) dans l’expérience.

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

      * Pour spécifier une période personnalisée, saisissez la date de début et la date de fin, ou cliquez sur ![icône de calendrier](/help/search-social-commerce/assets/calendar.png) en regard d’un champ et sélectionnez une date.

   * (Facultatif) Pour modifier la règle utilisée pour attribuer des données de conversion dans une série d’événements qui entraînent une conversion, cliquez sur ![Paramètres](/help/creative/assets/settings.png) et modifiez la **[!UICONTROL Attribution Rule]**.

     Pour plus d’informations sur les règles d’attribution, voir « [Calcul des règles d’attribution](/help/search-social-commerce/reports/attribution-rules.md) ».

   * (Facultatif) Pour modifier les conversions signalées, cliquez sur ![Paramètres](/help/creative/assets/settings.png) et sélectionnez les noms de conversion dans le menu **[!UICONTROL Conversions]**. Actuellement, la seule mesure disponible est « Sélectionner tout » pour inclure toutes les mesures de conversion.

     Les colonnes de conversion disponibles incluent les conversions disponibles dans Advertising Search, Social et Commerce, que vous soyez ou non client Search, Social et Commerce. La liste peut inclure des mesures d’engagement du site et de conversion synchronisées à partir d’Adobe Analytics lorsque l’annonceur dispose d’une [intégration [!DNL Adobe Analytics for Advertising] &#x200B;](/help/integrations/analytics/overview.md). [!DNL Analytics] mesures calculées et les mesures calculées avancées ne sont pas disponibles. Pour plus d’informations sur l’inclusion des conversions collectées dans les rapports, consultez la rubrique du guide Search, Social et Commerce intitulée « [&#x200B; À propos de la gestion des mesures de conversion d’un annonceur &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) ».

1. (Dans l’onglet [!UICONTROL Overview] ) :

   * (Facultatif) Dans la section [!UICONTROL Overall Regional Performance], placez le curseur sur un point du graphique pour afficher les données relatives à ce point.

   * (Facultatif) Dans la section [!UICONTROL Regional Performance], effectuez l’une des opérations suivantes :

      * Cliquez sur le nom d’une mesure (tel que [!UICONTROL Impressions]) pour l’afficher.

      * Sélectionnez la région dans le menu [!UICONTROL Region].

      * Placez le curseur sur un pays ou un état pour afficher les données de cette région.

   * (Facultatif) Dans la section [!UICONTROL Device Performance], effectuez l’une des opérations suivantes :

      * Placez le curseur sur la valeur de n’importe quelle catégorie d’appareils pour afficher les données de ce critère.

      * Cliquez sur la valeur de n’importe quelle catégorie d’appareils pour afficher la liste des principaux talents créatifs diffusés selon ce critère<!-- NN-->

1. (Facultatif) Pour afficher les données par élément créatif et par lot ou balise publicitaire, cliquez sur l’onglet **[!UICONTROL Creative Performance]** .

   * Dans le sous-onglet [!UICONTROL Creatives] , vous pouvez effectuer l’une des opérations suivantes :

      * (Facultatif) Pour basculer entre les vues graphique et grille, cliquez respectivement sur ![Graphique](/help/creative/assets/chart-view-button.png "Graphique") et ![Grille](/help/creative/assets/table-view-button.png "Grille").

      * (Facultatif) Dans la vue graphique, placez le curseur sur un point du graphique pour afficher les données relatives à ce point.

      * (Expériences avec ciblage d’arborescence de décision uniquement ; facultatif) Pour ventiler les performances pour chaque cible publicitaire appliquée, activez **[!UICONTROL Split targeting]**.

1. Pour afficher les données par lot (expériences avec ciblage d’arbre de décision) ou balise publicitaire (expériences sans ciblage d’arbre de décision), cliquez sur le sous-onglet **[!UICONTROL Bundles]** . Vous pouvez effectuer l’une des opérations suivantes :

   * (Facultatif) Pour basculer entre les vues graphique et grille, cliquez respectivement sur ![Graphique](/help/creative/assets/chart-view-button.png "Graphique") et ![Grille](/help/creative/assets/table-view-button.png "Grille").

   * (Facultatif) Dans la vue graphique, placez le curseur sur un point du graphique pour afficher les données relatives à ce point.

   * (Expériences avec ciblage d’arborescence de décision uniquement ; facultatif) Pour ventiler les performances pour chaque cible publicitaire appliquée, activez **[!UICONTROL Split targeting]**.

## Téléchargement de rapports de performances pour une expérience

* Dans la barre d’outils située en haut des rapports de performances, cliquez sur ![Télécharger](/help/creative/assets/download.png "Télécharger").

  Le fichier est téléchargé dans un fichier [!DNL Microsoft Excel] au format tableur (XLSX), conformément à la procédure normale de votre navigateur.

>[!MORELIKETHIS]
>
>* [Rapports personnalisés](/help/creative/reports/reports-about.md)
>* [Gérer les rapports personnalisés](/help/creative/reports/report-manage.md)
>* [Télécharger toutes les expériences de la vue](/help/creative/experiences/experience-download-view.md)
>* [À propos des expériences dans Advertising Creative](/help/creative/experiences/experience-about.md)
>* [Afficher les alertes](/help/creative/reports/alerts-view.md)
