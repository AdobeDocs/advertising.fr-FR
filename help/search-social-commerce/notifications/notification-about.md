---
title: A propos des notifications
description: Découvrez les notifications, notamment les différents types et catégories.
exl-id: a21dae13-b948-48e0-922a-d865f86e72f8
feature: Search Notifications
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# A propos des notifications

*Fonctionnalité bêta*

Vous pouvez configurer vos paramètres de notification pour vous abonner ou vous désabonner à différents types d’alertes. Vous pouvez afficher vos notifications de l’une des manières suivantes :

* Dans la [!UICONTROL Notifications] , disponible dans le menu principal à l’adresse ![Notifications](/help/search-social-commerce/assets/notifications-panel.png "Notifications").

* De [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* Depuis un [!UICONTROL Notification Center] application web qui s’ouvre [!UICONTROL Notification Center] dans une fenêtre distincte en dehors de Search, Social et Commerce.

  L’application se charge plus rapidement que la version normale du navigateur et est automatiquement mise à jour. Vous pouvez installer l’application et la gérer à l’aide du gestionnaire d’applications du navigateur.

* Des notifications push à votre navigateur.

  Lorsque vous activez des notifications push, elles s’affichent conformément aux conventions de notification du navigateur.

Vous pouvez afficher vos notifications, les marquer comme lues ou non et les supprimer.

## Types de notification

* **[!UICONTROL Notices]**: avis de gestion des versions, des temps d’arrêt et autres modifications.

* **[!UICONTROL Recommendations]**: opportunités identifiées pour améliorer les performances, mettre en oeuvre les bonnes pratiques, etc.

* **[!UICONTROL Warnings]**: problèmes qui nécessitent une attention particulière, mais qui ne sont pas essentiels à l’optimisation ou la gestion.

* **[!UICONTROL Issues]**: problèmes critiques nécessitant une attention immédiate. Les notifications d’erreur d’autorisation de compte sont incluses.

## Catégories de notification

* [!UICONTROL Campaign Management]

   * **[!UICONTROL UI Actions]**: notifications indiquant que les tâches effectuées en arrière-plan ont été terminées ou ont échoué. Les types de tâche incluent [Tâches de feuille de support](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), des tâches de modification en masse dans le tableau de données ou à l’aide de la barre d’outils, des tâches d’affectation d’entité ou d’autres actions de l’interface utilisateur (synchronisation avec les réseaux publicitaires, collage de lignes ou changement de nom des entités, par exemple). Les affectations d’entité incluent l’attribution ou l’annulation de l’attribution d’un [valeur de classification de libellé](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) à n’importe quelle entité, en attribuant une campagne à un portefeuille et en attribuant ou en annulant l’affectation d’une contrainte à un portefeuille.<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * **[!UICONTROL Bulksheets]**: avertit qu’une [opération bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) a été terminé ou a échoué.

   * **[!UICONTROL Manager Account Missing]**: notifications indiquant que Search, Social et Commerce n’a pas les informations d’identification pour une [compte de gestionnaire de réseau publicitaire](/help/search-social-commerce/admin/manager-accounts.md), qui servent à la configuration correcte des fonctions critiques.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md); or it's overridden at a lower level by an incorrect value.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are for the correct setup of critical functions.
  -->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Manager Account Auth Error]**: notifications que Search, Social et Commerce n’a pas pu se synchroniser avec une [compte de gestionnaire de réseau publicitaire](/help/search-social-commerce/admin/manager-accounts.md) en raison d’informations d’identification non valides ou d’un jeton d’autorisation non valide ou arrivé à expiration.

      * **[!UICONTROL Account Auth Error]**: notifications indiquant que Search, Social et Commerce n’a pas pu accéder à un [compte réseau publicitaire](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) en raison d’informations d’identification non valides ou d’un jeton d’autorisation non valide ou arrivé à expiration.

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: utilisé pour une version bêta fermée

      * **[!UICONTROL File Upload to Cloud Storage]**: utilisé pour une version bêta fermée

<!--
* [!UICONTROL Optimization]
-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Custom Alerts]**: notifications que [instances d’alerte](/help/search-social-commerce/alerts/alert-about.md) ont été déclenchées pour un modèle d’alerte.

   * **[!UICONTROL Spreadsheet Feeds]**: avertit qu’une [flux de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) a été terminé ou a échoué.

   * **[!UICONTROL Reports]**: avertit qu’une [rapport personnalisé ou planifié](/help/search-social-commerce/reports/report-about.md) a été terminé ou a échoué.

   * **[!UICONTROL Advertising Insights]**: notifications que [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) a été terminé ou a échoué.

<!--
* [!UICONTROL System]
-->

>[!MORELIKETHIS]
>
>* [Afficher vos notifications](notification-view.md)
>* [Marquer une notification comme lue ou non lue](notification-mark-read-unread.md)
>* [Supprimer une notification](notification-delete.md)
>* [Modification des paramètres de notification](notification-edit.md)
>* [Activation et désactivation des notifications push depuis [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Installez et désinstallez le [!UICONTROL Notification Center] application web](notification-app-install-uninstall.md)
