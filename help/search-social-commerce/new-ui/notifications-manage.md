---
title: (Nouvelle interface utilisateur) Gérer les notifications
description: Découvrez comment afficher, configurer et gérer les notifications Search, Social et Commerce, y compris les notifications push et l’application web du Centre de notifications.
feature: Search Notifications
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gérer les notifications

*Fonction*

Vous pouvez configurer vos paramètres de notification pour vous abonner ou vous désabonner à différents types d’alertes. Vous pouvez afficher vos notifications de l’une des manières suivantes :

* Dans le panneau [!UICONTROL Notifications], disponible en haut à droite à ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications"). Dans le panneau, vous pouvez filtrer la liste, modifier vos paramètres de notification ou ouvrir des [!UICONTROL Notification Center].

* Depuis [!UICONTROL Notification Center], qui s’ouvre dans une fenêtre distincte en dehors de Search, Social et Commerce. Pour ouvrir [!UICONTROL Notification Center] à partir du panneau [!UICONTROL Notifications], cliquez sur **[!UICONTROL View All]**.

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

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]** : notifications indiquant qu’une opération [feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) a été effectuée ou a échoué.<!-- Update link once file for new UI available-->

   * **[!UICONTROL Manager Account Missing]** : notifications indiquant que Search, Social et Commerce ne disposent pas des informations d’identification d’un compte [ad network manager](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md), lesquelles sont requises pour la configuration correcte des fonctions critiques.<!-- Moving to Campaign Management > Setup Errors at some point -->

   * **[!UICONTROL UI Actions]** : notifications indiquant que les tâches effectuées en arrière-plan ont été menées à bien ou ont échoué. Les types de tâche incluent les tâches [sous forme de feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available-->, les tâches de modification en bloc dans le tableau de données ou à l’aide de la barre d’outils, les tâches d’affectation d’entité ou d’autres actions dans l’interface utilisateur (comme la synchronisation avec les réseaux publicitaires, le collage de lignes ou le changement de nom d’entités). Les affectations d’entité incluent l’affectation ou l’annulation de l’affectation d’une [valeur de classification de libellé](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md) à une entité, l’affectation d’une campagne à un portefeuille et l’[affectation ou annulation de l’affectation d’une contrainte d’offre à une entité](/help/search-social-commerce/new-ui/goals/constraints-manage.md).

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]** : notifications indiquant qu’un fichier de données de compte a été chargé ou qu’un chargement de données de compte a échoué via [chargement manuel de données de compte](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

      * **[!UICONTROL File Upload to Cloud Storage]** : notifications indiquant qu’un fichier de données de compte a été chargé ou qu’un chargement de données de compte a échoué via [chargement de données de compte vers un compartiment  [!DNL Amazon] [!DNL S3]](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]** : notifications indiquant que Search, Social et Commerce n’a pas pu accéder à un compte réseau [ad](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) en raison d’informations d’identification non valides ou d’un jeton d’autorisation non valide ou arrivé à expiration.

      * **[!UICONTROL Account Missing]** : notifications indiquant que Search, Social et Commerce ne disposent pas des informations d’identification d’un compte réseau [publicitaire](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md).

      * **[!UICONTROL Manager Account Auth Error]** : notifications indiquant que Search, Social et Commerce n’ont pas pu être synchronisés avec un compte [ad network manager](/help/search-social-commerce/admin/manager-accounts.md) en raison d’informations d’identification non valides ou d’un jeton d’autorisation non valide ou arrivé à expiration.<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]** : notifications indiquant qu’[an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) est terminé ou a échoué.

   * **[!UICONTROL Custom Alerts]** : notifications [instances d’alerte](/help/search-social-commerce/new-ui/alerts-manage.md) déclenchées pour un modèle d’alerte.

   * **[!UICONTROL Spreadsheet Feeds]** : notifications indiquant qu’un flux [de feuille de calcul](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md) est terminé ou a échoué.

   * [!UICONTROL Reports]

      * **[!UICONTROL Grid Reports]** : notifications indiquant qu’un rapport de vue de données d’une vue spécifique (comme le contenu de la table de données dans la vue [!UICONTROL Camapigns]) a été terminé ou a échoué.

      * **[!UICONTROL Reports]** : notifications indiquant qu’un [rapport personnalisé ou planifié](/help/search-social-commerce/new-ui/reports/management/report-manage.md) a été terminé ou a échoué.

   * [!UICONTROL Portfolio Management]

      * **[!UICONTROL Intraday Optimization]** : notifications lorsque l’optimisation intrajournalière est désactivée.

      * **[!UICONTROL Simulation Report]** : notifications relatives aux tâches de [simulation](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md).

      * [!UICONTROL Objective & Conversion Configuration]

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]** : notifications au niveau de l’annonceur concernant l’affectation automatique réussie et ayant échoué des objectifs de conversion de campagne.

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]** : notifications au niveau du portefeuille concernant l’affectation automatique réussie et ayant échoué des objectifs de conversion de campagne.

      * [!UICONTROL Portfolios]

         * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]** : notifications sur les tâches de modification en bloc de [portfolio) via des feuilles d’envoi groupé](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md).

         * **[!UICONTROL Portfolio Settings]** : notifications sur les [modifications apportées aux paramètres du portfolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md).

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## Actions disponibles

* [Affichage des notifications](#notification-view)

* [Modifier vos paramètres de notification](#notification-edit)

* [Marquer une notification comme lue ou non lue](#notification-mark-read-unread)

* [Supprimer une notification](#notification-delete)

* [Activer et désactiver les notifications push](#notification-push-enable-disable)

* [Installation et désinstallation de l’application web [!UICONTROL Notification Center]](#notification-app-install-uninstall)

## Affichage des notifications {#notification-view}

Lorsque vous êtes [abonné aux notifications](#notification-edit) concernant les erreurs d’authentification du compte, les alertes personnalisées déclenchées et les [!UICONTROL Advertising Insights] générées, vous pouvez afficher vos notifications dans le panneau [!UICONTROL Notifications] ou dans le [!UICONTROL Notification Center].

### Affichage des notifications dans le panneau [!UICONTROL Notifications]

1. Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Pour afficher les détails d’une notification, cliquez sur son nom.

     Dans certaines notifications, la section [!UICONTROL Action Recommended] peut inclure un lien qui ouvre une vue filtrée des entités affectées ou responsables.

   * Pour marquer une notification comme *lue* ou *non lue*, placez le curseur sur le nom de l’alerte et cliquez sur ![Marquer comme lu ou Non lu](/help/search-social-commerce/assets/notifications-read-unread.png "Marquer comme lu ou Non lu").

     Les notifications marquées comme *lues* apparaissent dans un texte plus clair, mais restent disponibles jusqu’à ce que vous les supprimiez.

     ![Notifications lues et non lues](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Notifications lues et non lues")

   * Pour modifier vos préférences d’abonnement pour le type de notification, cliquez sur ![Paramètres](/help/search-social-commerce/assets/settings-nc.png "Paramètres") en regard de la notification, modifiez vos paramètres, puis cliquez sur **[!UICONTROL Save]**.

   * Pour supprimer une notification, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer") en regard de celle-ci.

   * Pour [!UICONTROL Notification Center] ouvrir, cliquez sur **[!UICONTROL View All]**.

### Affichage des notifications dans [!UICONTROL Notification Center]

1. Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Cliquez sur **[!UICONTROL View All]**.

1. (Facultatif) Pour filtrer vos notifications par type, cliquez sur *[!UICONTROL Notices], [!UICONTROL Recommendations], [!UICONTROL Warnings] ou[!UICONTROL Issues]*.

1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Pour afficher les détails d’une notification, cliquez sur son nom.

     Dans certaines notifications, la section [!UICONTROL Action Recommended] peut inclure un lien qui ouvre une vue filtrée des entités affectées ou responsables.

   * Pour marquer une notification comme *lue* ou *non lue*, placez le curseur sur le nom de l’alerte et cliquez sur ![Marquer comme lu ou Non lu](/help/search-social-commerce/assets/notifications-read-unread.png "Marquer comme lu ou Non lu").

     Les notifications marquées comme *lues* apparaissent dans un texte plus clair, mais restent disponibles jusqu’à ce que vous les supprimiez.

   * Pour modifier vos préférences d’abonnement pour le type de notification, cliquez sur ![Paramètres](/help/search-social-commerce/assets/settings-nc.png "Paramètres") en regard de la notification, modifiez vos paramètres, puis cliquez sur **[!UICONTROL Save]**.

   * Pour supprimer une notification, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer") en regard de celle-ci.

## Modifier vos paramètres de notification {#notification-edit}

Vous avez la possibilité de vous abonner ou de vous désabonner des notifications web et par e-mail concernant les erreurs d’authentification du compte, toutes vos alertes personnalisées déclenchées et l’achèvement des [!UICONTROL Advertising Insights] que vous générez.

1. Ouvrez les paramètres de notification de l’une des manières suivantes :

   * Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications") pour ouvrir le panneau [!UICONTROL Notifications]. Dans le coin supérieur droit, cliquez sur ![Paramètres](/help/search-social-commerce/assets/settings-nc.png "Paramètres").

   * Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications"), cliquez sur **[!UICONTROL View All]** pour [!UICONTROL Notification Center] ouvrir, puis dans le menu de gauche, cliquez sur ![Paramètres](/help/search-social-commerce/assets/settings-nc.png "Paramètres").

1. Modifiez vos paramètres pour toute catégorie de notification répertoriée ci-dessus :

   * Pour vous abonner ou vous désabonner des notifications, déplacez le curseur dans la colonne [!UICONTROL Subscribe] :

      * Pour vous désabonner de tous les types de notification, déplacez le curseur vers la gauche (désactivé).

      * Pour vous abonner à un ou plusieurs types de notification, déplacez le curseur vers la droite (activé).

   * (Lorsque l’[!UICONTROL Subscribe] est activée) Pour vous abonner aux notifications par e-mail, cochez la case située dans la colonne **[!UICONTROL Email]** .

   * (Lorsque l’option [!UICONTROL Subscribe] est désactivée) Pour vous abonner aux notifications web dans les notifications Search, Social et Commerce, et aux notifications push si elles sont activées pour le navigateur, cochez la case dans la colonne **[!UICONTROL Web]** .

     Les notifications web sont diffusées uniquement lorsque vous [activez les notifications push](#notification-push-enable-disable) dans votre navigateur.

1. Cliquez sur **[!UICONTROL Save]**.

## Marquer une notification comme lue ou non lue {#notification-mark-read-unread}

Le marquage d’une notification comme *lue* ou *non lue* modifie le nombre de notifications non lues indiquées dans le lien [!UICONTROL Notifications] en haut de chaque page (par exemple, ![Icône Notifications avec compteur de notifications non lues](/help/search-social-commerce/assets/notifications-unread.png "Icône Notifications avec compteur de notifications non lues")).

Les notifications marquées comme *lues* apparaissent dans un texte plus clair, mais restent disponibles jusqu’à ce que vous les supprimiez.

![Notifications lues et non lues](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Notifications lues et non lues")

1. [Ouvrez le panneau Notifications ou le Centre de notifications](#notification-view).

1. Placez le curseur sur le nom de l’alerte et cliquez sur ![Marquer comme lu ou Non lu](/help/search-social-commerce/assets/notifications-read-unread.png "Marquer comme lu ou Non lu").

## Supprimer une notification {#notification-delete}

### Supprimer une notification dans le panneau [!UICONTROL Notifications]

1. Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer") en regard de la notification.

### Supprimer une notification dans [!UICONTROL Notification Center]

1. Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Cliquez sur **[!UICONTROL View All]**.

1. (Facultatif) Pour filtrer vos notifications par type, cliquez sur *[!UICONTROL Notices]*, *[!UICONTROL Recommendations]*, *[!UICONTROL Warnings]* ou *[!UICONTROL Issues]*.

1. Cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer") en regard de la notification.

## Activer et désactiver les notifications push {#notification-push-enable-disable}

Vous pouvez activer les notifications dans Search, Social et Commerce, où elles s’affichent selon les conventions de notification du navigateur. Sur les appareils utilisant [!DNL Microsoft Windows], les notifications s&#39;affichent en bas à droite de l&#39;écran (barre d&#39;état système). Sur les appareils [!DNL Apple Mac], les notifications s’affichent dans le menu de droite.

Les notifications push sont disponibles dans les navigateurs suivants :

* [!DNL Google Chrome] 40 et versions ultérieures

* [!DNL Microsoft Edge] 17 et versions ultérieures

* [!DNL Mozilla Firefox] 44 et versions ultérieures

Vous pouvez désactiver les notifications push en fonction de la procédure standard du navigateur.

### Activer les notifications push

1. Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Cliquez sur **[!UICONTROL View All]**.

1. Dans le coin inférieur droit, cliquez sur ![Activer les notifications push](/help/search-social-commerce/assets/notifications-push.png "Activer les notifications push").

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Enable]**.

1. Configurez le navigateur pour autoriser les notifications de [!UICONTROL Notification Center] à `https://alert-center-ui-na.efrontier.com`.

   Les paramètres de notification par défaut varient selon le navigateur. L’option permettant d’autoriser les notifications provenant de l’adresse [!UICONTROL Notification Center] peut s’afficher automatiquement ou vous devez gérer manuellement les paramètres de notification. Par exemple, dans [!DNL Microsoft Edge], vous pouvez autoriser les notifications de [!UICONTROL Notification Center] depuis la barre d’outils du navigateur. Voir les instructions dans l’aide du navigateur.

   ![Où gérer les paramètres de notification dans Microsoft Edge](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Où gérer les paramètres de notification dans Microsoft Edge")

1. Dans vos [paramètres de notification](#notification-edit), activez les notifications [!UICONTROL Web] pour les types d’alerte que vous souhaitez transmettre.

### Désactiver les notifications push

Supprimez les notifications de `https://alert-center-ui-na.efrontier.com` dans le gestionnaire de notifications du navigateur. Par exemple, dans [!DNL Google Chrome], vous pouvez supprimer ou bloquer des notifications provenant de sites spécifiés à l’adresse `chrome://settings/content/notifications`.

Voir les instructions dans l’aide du navigateur.

## Installation et désinstallation de l’application web [!UICONTROL Notification Center] {#notification-app-install-uninstall}

Vous pouvez recevoir et gérer les notifications en dehors de votre navigateur en installant une application web [!UICONTROL Notification Center]. L’application a le même aspect et les mêmes fonctionnalités que [!UICONTROL Notification Center] dans Search, Social et Commerce. L’application est disponible pour les [!DNL Google Chrome] 40 et ultérieures ou les [!DNL Microsoft Edge] 17 et ultérieures.

Une fois que vous avez installé l’application [!UICONTROL Notification Center], elle est automatiquement activée dans le gestionnaire d’applications du navigateur et elle se charge sous la forme d’une fenêtre distincte dont la disposition est organisée dynamiquement en fonction de la taille de la fenêtre. Vous pouvez ouvrir et fermer l’application à partir du gestionnaire d’applications du navigateur ou l’épingler sur la barre des tâches ou la station d’accueil du système d’exploitation. L’application est automatiquement mise à jour.

![Icône Centre de notifications dans la barre des tâches de Microsoft Windows](/help/search-social-commerce/assets/windows-taskbar.png "Icône Centre de notifications dans la barre des tâches de Microsoft Windows")

Vous pouvez désactiver ou désinstaller l’application à partir du gestionnaire d’applications du navigateur. Pour plus d’informations sur la gestion des applications web, consultez l’aide du navigateur.

### Installation de l’application web [!UICONTROL Notification Center] pour [!DNL Google Chrome]

1. Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

1. Cliquez sur **[!UICONTROL View All]**.

1. Dans le coin inférieur droit, cliquez sur ![Installer l’application web du Centre de notifications](/help/search-social-commerce/assets/notifications-install-app.png "Installer l’application web du Centre de notifications").

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Add]**.

1. Dans l’application d’installation ? , cliquez sur **[!UICONTROL Install]**.

### Installation de l’application web [!UICONTROL Notification Center] pour [!DNL Microsoft Edge]

* Dans Search, Social et Commerce :

   1. Dans l’angle supérieur droit d’une page, cliquez sur ![Notifications](/help/search-social-commerce/assets/notifications.png "Notifications").

   1. Cliquez sur **[!UICONTROL View All]**.

   1. Dans le coin inférieur droit, cliquez sur ![Installer l’application web du Centre de notifications](/help/search-social-commerce/assets/notifications-install-app.png "Installer l’application web du Centre de notifications").

   1. Dans le message de confirmation, cliquez sur **[!UICONTROL Add]**.

   1. Dans le message de l’application [!UICONTROL Install Notification Center], cliquez sur **[!UICONTROL Install]**.

* Dans le menu principal [!DNL Edge] :

   1. Dans la barre d’outils du navigateur, cliquez sur **...** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**.

   1. Dans le message de l’application [!UICONTROL Install Notification Center], cliquez sur **[!UICONTROL Install]**.

### Désinstaller l’application web [!UICONTROL Notification Center] pour [!DNL Google Chrome]

* Dans [!DNL Chrome], accédez à `chrome://apps`, cliquez avec le bouton droit sur **[!UICONTROL notification-center]**, puis cliquez sur **[!UICONTROL Remove from Chrome]**.

### Désinstaller l’application web [!UICONTROL Notification Center] pour [!DNL Microsoft Edge]

1. Dans la barre d’outils du navigateur [!DNL Edge], cliquez sur **...** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**. Sinon, allez à `edge://apps`.

1. Cliquez avec le bouton droit sur **[!UICONTROL Notification Center]** et cliquez sur **[!UICONTROL Uninstall]**.
