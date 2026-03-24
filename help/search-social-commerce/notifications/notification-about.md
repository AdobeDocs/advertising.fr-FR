---
title: À propos des notifications
description: Découvrez les notifications, y compris les différents types et catégories.
exl-id: 79495e1c-72ce-476f-83df-c4d95391f51c
feature: Search Notifications
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# À propos des notifications

*Fonctionnalité*

Vous pouvez configurer vos paramètres de notification pour vous abonner ou vous désabonner à différents types d’alertes. Vous pouvez afficher vos notifications de l’une des manières suivantes :

* Dans le panneau [!UICONTROL Notifications], disponible à partir du menu principal sous ![Notifications](/help/search-social-commerce/assets/notifications-panel.png "Notifications").

* Depuis [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* À partir d’une application web [!UICONTROL Notification Center], qui s’ouvre [!UICONTROL Notification Center] dans une fenêtre distincte en dehors de Search, Social et Commerce.

  L’application se charge plus rapidement que la version standard du navigateur et est automatiquement mise à jour. Vous pouvez installer l’application et la gérer à l’aide du gestionnaire d’applications du navigateur.

* Depuis les notifications push vers votre navigateur.

  Lorsque vous activez les notifications push, elles s’affichent conformément aux conventions de notification du navigateur.

Vous pouvez afficher vos notifications, marquer les notifications comme lues ou non lues et supprimer des notifications.

## Types de notification

* **[!UICONTROL Notices]** : avis de mise à jour, temps d’arrêt et autres avis de gestion des modifications.

* **[!UICONTROL Recommendations]** : opportunités identifiées pour améliorer les performances, mettre en œuvre les bonnes pratiques, etc.

* **[!UICONTROL Warnings]** : problèmes qui nécessitent une attention particulière, mais qui ne sont pas critiques pour l’optimisation ou la gestion.

* **[!UICONTROL Issues]** : problèmes critiques nécessitant une attention immédiate. Les notifications d’erreur d’autorisation de compte sont incluses.

## Catégories de notification

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]** : notifications indiquant qu’une opération [feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) a été effectuée ou a échoué.

   * **[!UICONTROL Manager Account Missing]** : notifications indiquant que Search, Social et Commerce ne disposent pas des informations d’identification d’un compte [ad network manager](/help/search-social-commerce/admin/manager-accounts.md), lesquelles sont requises pour la configuration correcte des fonctions critiques.

   * **[!UICONTROL UI Actions]** : notifications indiquant que les tâches effectuées en arrière-plan ont été menées à bien ou ont échoué. Les types de tâche incluent les tâches [sous forme de feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), les tâches de modification en bloc dans le tableau de données ou à l’aide de la barre d’outils, les tâches d’affectation d’entité ou d’autres actions dans l’interface utilisateur (comme la synchronisation avec les réseaux publicitaires, le collage de lignes ou le changement de nom d’entités). Les affectations d’entité incluent l’affectation ou l’annulation de l’affectation d’une [valeur de classification de libellé](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) à une entité, l’affectation d’une campagne à un portfolio et l’affectation ou l’annulation de l’affectation d’une contrainte à un portfolio<!--Link "constraint" to constraint-about.md if that file is ever public -->.

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]** : utilisé pour une version Beta fermée

      * **[!UICONTROL File Upload to Cloud Storage]** : utilisé pour une version Beta fermée

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]** : notifications indiquant que Search, Social et Commerce n’a pas pu accéder à un compte réseau [ad](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) en raison d’informations d’identification non valides ou d’un jeton d’autorisation non valide ou arrivé à expiration.

      * **[!UICONTROL Account Missing]** : notifications indiquant que Search, Social et Commerce ne disposent pas des informations d’identification d’un compte réseau [publicitaire](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md).

      * **[!UICONTROL Manager Account Auth Error]** : notifications indiquant que Search, Social et Commerce n’ont pas pu être synchronisés avec un compte [ad network manager](/help/search-social-commerce/admin/manager-accounts.md) en raison d’informations d’identification non valides ou d’un jeton d’autorisation non valide ou arrivé à expiration.

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](https://experienceleague.adobe.com/fr/docs/analytics/components/dimensions/amo-id#dimension-items); the [!UICONTROL Tracking Template] is incorrect or missing; or the [!UICONTROL Landing Page Suffix] or [!UICONTROL Tracking Template] is overridden at a lower level by an incorrect value. Separate notifications are sent a) for errors at the account level and b) for errors at the campaign and lower levels.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.
  -->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]** : notifications indiquant qu’[an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) est terminé ou a échoué.

   * **[!UICONTROL Custom Alerts]** : notifications [instances d’alerte](/help/search-social-commerce/alerts/alert-about.md) déclenchées pour un modèle d’alerte.

   * **[!UICONTROL Reports]** : notifications indiquant qu’un [rapport personnalisé ou planifié](/help/search-social-commerce/reports/report-about.md) a été terminé ou a échoué.

   * **[!UICONTROL Spreadsheet Feeds]** : notifications indiquant qu’un flux [de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) est terminé ou a échoué.

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
>* [Modifier vos paramètres de notification](notification-edit.md)
>* [Activer et désactiver les notifications push depuis [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [Installation et désinstallation de l’application web [!UICONTROL Notification Center]](notification-app-install-uninstall.md)
