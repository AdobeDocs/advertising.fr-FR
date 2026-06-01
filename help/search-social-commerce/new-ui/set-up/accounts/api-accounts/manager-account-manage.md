---
title: (Nouvelle interface utilisateur) Gérer les informations d’identification pour les comptes du gestionnaire Google Ads
description: Découvrez comment configurer et gérer les informations d’identification des comptes du gestionnaire Google Ads dans la nouvelle interface utilisateur.
feature: Search Admin
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gestion des informations d’identification pour les comptes [!DNL Google Ads] Manager

*Fonction*

Comptes *[!DNL Google Ads]uniquement*

Indiquez les informations d’identification des comptes [!DNL Google Ads] Manager sur lesquels vous souhaitez que Search, Social et Commerce chargent les conversions entre comptes. Utilisez cette fonctionnalité dans deux scénarios : si vous souhaitez télécharger des mesures de conversion entre comptes suivies par des [!DNL Adobe] vers un compte [!DNL Google Ads] Manager ou pour télécharger des objectifs de portfolio qui incluent des conversions entre comptes vers [!DNL Google Ads] pour obtenir une optimisation hybride.

Vous pouvez ajouter des informations d’identification pour les nouveaux enregistrements de compte Manager ou réauthentifier un compte Manager existant.

Une fois que vous avez ajouté les informations d’identification d’un compte Manager, les paramètres du compte affichent l’identifiant de compte Manager associé en lecture seule. [!UICONTROL Notification Center] inclut les [notifications](/help/search-social-commerce/new-ui/notifications-manage.md) lorsque les informations d’identification d’un compte Manager sont manquantes (le [!UICONTROL Manager Account Missing Error]) ou lorsqu’un jeton d’authentification du compte Manager expire (le [!UICONTROL Manager Account Auth Error]).

## Ajouter des informations d’identification pour un nouveau compte de responsable {#create-manager-account}

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Cliquez sur **[!UICONTROL +]**.

1. Sélectionnez le réseau publicitaire, puis cliquez sur **[!UICONTROL Next]**.

1. Spécifiez les [paramètres du compte Manager](#manager-account-settings).

1. Cliquez sur **[!UICONTROL Authenticate]** et connectez-vous à l’aide des informations d’identification du compte Manager.

   Search, Social et Commerce capture et stocke automatiquement le jeton d’authentification.

1. Dans Search, Social et Commerce, cliquez sur **[!UICONTROL Save]**.

## Modifier les détails du compte Manager {#edit-manager-account}

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Sélectionnez le compte de l’une des manières suivantes :

   * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

   * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur (/help/search-social-commerce/assets/edit-new.png « Modifier).

1. Modifiez les [paramètres du compte du responsable](#manager-account-settings).

1. Cliquez sur **[!UICONTROL Re-Authenticate]** et connectez-vous à l’aide des informations d’identification du compte Manager.

   Search, Social et Commerce capture et stocke automatiquement le jeton d’authentification.

1. Dans Search, Social et Commerce, cliquez sur **[!UICONTROL Save]**.

## Réauthentifier un compte Manager {#reauthenticate-manager-account}

Réauthentifiez un compte Manager lorsque le jeton OAuth expire ou devient non valide.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Reauthenticate]**.

1. Connectez-vous à l’aide des informations d’identification du compte Manager.

   Search, Social et Commerce capture et stocke automatiquement le nouveau jeton d’authentification.

## Paramètres du compte Manager {#manager-account-settings}

**[!UICONTROL Manager Account ID]:** ID de compte unique pour le compte du responsable sur le réseau publicitaire.

**[!UICONTROL Mnaager Account Name]:** nom à afficher pour le compte du responsable dans Search, Social et Commerce.

**[!UICONTROL Login Email]:** adresse e-mail associée au nom d’utilisateur du compte du responsable. Obligatoire pour l’authentification.

**[!UICONTROL Password]:** (facultatif) Mot de passe du compte. Saisissez le mot de passe lorsque vous souhaitez le chiffrer et enregistrez-le afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

>[!MORELIKETHIS]
>
>* [Activer le chargement des objectifs sur les réseaux publicitaires](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [Gérer les notifications](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
