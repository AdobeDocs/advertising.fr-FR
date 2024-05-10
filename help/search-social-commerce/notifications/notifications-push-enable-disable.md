---
title: Activation et désactivation des notifications push depuis [!UICONTROL Notification Center]
description: Découvrez comment activer et désactiver les notifications push depuis [!UICONTROL Notification Center].
exl-id: f0e91e76-eb1e-4ff0-9a52-e9bc587552a2
feature: Search Notifications
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Activation et désactivation des notifications push depuis [!UICONTROL Notification Center]

*Fonctionnalité bêta*

Vous pouvez activer les notifications dans Search, Social et Commerce, où elles s’affichent conformément aux conventions de notification du navigateur. Sur les périphériques qui utilisent [!DNL Microsoft Windows], les notifications s’affichent dans la partie inférieure droite de l’écran (barre d’état système). Activé [!DNL Apple Mac] appareils, notifications s’affichent dans le menu de droite.

Les notifications push sont disponibles dans les navigateurs suivants :

* [!DNL Google Chrome] 40 et plus

* [!DNL Microsoft Edge] 17 et plus

* [!DNL Mozilla Firefox] 44 et versions ultérieures

Vous pouvez désactiver les notifications push selon la procédure standard du navigateur.

## Activation des notifications push

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** > **[!UICONTROL Insights & Reports]** > **[!UICONTROL Notification Center Beta]**.

2. En bas à droite, cliquez sur ![Activation des notifications push](/help/search-social-commerce/assets/notifications-push.png "Activation des notifications push").

3. Dans le message de confirmation, cliquez sur **[!UICONTROL Enable]**.

4. Configuration du navigateur pour autoriser les notifications de [!UICONTROL Notification Center] at`https://alert-center-ui-na.efrontier.com`.

   Les paramètres de notification par défaut varient selon le navigateur et vous pouvez : a) se voir automatiquement présenter l’option permettant d’autoriser les notifications de [!UICONTROL Notification Center] ou b) doivent gérer manuellement les paramètres de notification. Par exemple, dans [!DNL Microsoft Edge], vous pouvez autoriser les notifications de [!UICONTROL Notification Center] dans la barre d’outils du navigateur. Voir les instructions dans l’aide du navigateur.

   ![Où gérer les paramètres de notification dans Microsoft Edge](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Où gérer les paramètres de notification dans Microsoft Edge")

5. Dans votre [paramètres de notification](notification-edit.md), activez [!UICONTROL Web] notifications pour les types d’alerte à envoyer.

## Désactivation des notifications push

Supprimer des notifications de `https://alert-center-ui-na.efrontier.com` dans le gestionnaire de notifications du navigateur. Par exemple, dans [!DNL Google Chrome], vous pouvez supprimer ou bloquer des notifications de sites spécifiés sur `chrome://settings/content/notifications`.

Voir les instructions dans l’aide du navigateur.

>[!MORELIKETHIS]
>
>* [A propos des notifications](/help/search-social-commerce/notifications/notification-about.md)
>* [Afficher vos notifications](notification-view.md)
>* [Marquer une notification comme lue ou non lue](notification-mark-read-unread.md)
>* [Supprimer une notification](notification-delete.md)
>* [Modification des paramètres de notification](notification-edit.md)
>* [Installez et désinstallez le [!UICONTROL Notification Center] application web](notification-app-install-uninstall.md)
