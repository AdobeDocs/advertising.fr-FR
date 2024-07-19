---
title: A propos des notifications
description: Découvrez les notifications, notamment les différents types et catégories.
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 49dc6a4a18966bbf68402d70aec9574ed11e1886
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# A propos des notifications

*Fonctionnalité Beta*

Vous pouvez configurer vos paramètres de notification pour vous abonner ou vous désabonner à différents types d’alertes. Vous pouvez afficher vos notifications de l’une des manières suivantes :

* Dans le panneau [!UICONTROL Notifications], disponible dans le menu principal à l’adresse ![Notifications](/help/search-social-commerce/assets/notifications-panel.png "Notifications").

* De [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* À partir d’une application web [!UICONTROL Notification Center], qui ouvre [!UICONTROL Notification Center] dans une fenêtre distincte en dehors de Search, Social et Commerce.

  L’application se charge plus rapidement que la version normale du navigateur et est automatiquement mise à jour. Vous pouvez installer l’application et la gérer à l’aide du gestionnaire d’applications du navigateur.

* Des notifications push à votre navigateur.

  Lorsque vous activez des notifications push, elles s’affichent conformément aux conventions de notification du navigateur.

Vous pouvez afficher vos notifications, les marquer comme lues ou non et les supprimer.

## Types de notification

* **[!UICONTROL Notices]** : avis de gestion des versions, des temps d’arrêt et autres modifications.

* **[!UICONTROL Recommendations]** : opportunités identifiées pour améliorer les performances, mettre en oeuvre les bonnes pratiques, etc.

* **[!UICONTROL Warnings]** : problèmes qui nécessitent une attention particulière mais qui ne sont pas essentiels à l’optimisation ou la gestion.

* **[!UICONTROL Issues]** : problèmes critiques nécessitant une attention immédiate. Les notifications d’erreur d’autorisation de compte sont incluses.

## Catégories de notification

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]** : notifications indiquant qu’une [opération bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) a été terminée ou a échoué.

   * **[!UICONTROL Manager Account Missing]** : notifications indiquant que Search, Social et Commerce ne contient pas les informations d’identification pour un [compte de gestionnaire de réseau publicitaire](/help/search-social-commerce/admin/manager-accounts.md), qui sont requises pour la configuration correcte des fonctions critiques.

   * **[!UICONTROL UI Actions]** : notifications indiquant que les tâches effectuées en arrière-plan ont été terminées ou ont échoué. Les types de tâche incluent les [tâches de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), les tâches de modification en masse dans le tableau de données ou à l’aide de la barre d’outils, les tâches d’affectation d’entité ou d’autres actions dans l’interface utilisateur (telles que la synchronisation avec les réseaux publicitaires, le collage de lignes ou le changement de nom des entités). Les affectations d’entité incluent l’attribution ou l’annulation de l’attribution d’une [ valeur de classification d’étiquette ](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) à une entité, l’affectation d’une campagne à un portfolio, ainsi que l’attribution ou l’annulation de l’affectation d’une contrainte à un portfolio.<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]** : utilisé pour une version bêta fermée

      * **[!UICONTROL File Upload to Cloud Storage]** : utilisé pour une version bêta fermée

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]** : notifications indiquant que Search, Social et Commerce n’a pas pu accéder à un [compte réseau publicitaire](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) en raison d’informations d’identification non valides ou d’un jeton d’autorisation non valide ou arrivé à expiration.

      * **[!UICONTROL Account Missing]** : notifications indiquant que Search, Social et Commerce ne contient pas les informations d’identification pour un [compte réseau publicitaire](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md).

      * **[!UICONTROL Manager Account Auth Error]** : notifications que Search, Social et Commerce n’a pas pu se synchroniser avec un [ compte de gestionnaire de réseau publicitaire ](/help/search-social-commerce/admin/manager-accounts.md) en raison d’informations d’identification incorrectes ou d’un jeton d’autorisation non valide ou arrivé à expiration.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]** : notifications indiquant que [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) a été terminé ou a échoué.

   * **[!UICONTROL Custom Alerts]** : notifications que [instances d’alerte](/help/search-social-commerce/alerts/alert-about.md) ont été déclenchées pour un modèle d’alerte.

   * **[!UICONTROL Reports]** : notifications indiquant qu’un [rapport personnalisé ou planifié](/help/search-social-commerce/reports/report-about.md) a été terminé ou a échoué.

   * **[!UICONTROL Spreadsheet Feeds]** : notifications indiquant qu’un [flux de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) a été terminé ou a échoué.

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: 

-->

<!--
* [!UICONTROL Portfolio Management]

  * **[!UICONTROL Simulation Report]**: 

-->

<!--
* [!UICONTROL System]

  * **[!UICONTROL Change Management]**: 

-->

>[!MORELIKETHIS]
>
>* [Afficher vos notifications](notification-view.md)
>* [Marquer une notification comme lue ou non lue](notification-mark-read-unread.md)
>* [Supprimer une notification](notification-delete.md)
>* [Modifier les paramètres de notification](notification-edit.md)
>* [Activer et désactiver les notifications push de [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Installation et désinstallation de l’application web [!UICONTROL Notification Center]](notification-app-install-uninstall.md)
