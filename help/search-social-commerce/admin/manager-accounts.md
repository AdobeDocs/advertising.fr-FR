---
title: Gestion des informations d’identification des comptes de gestionnaire de réseau publicitaire
description: Découvrez comment fournir des informations d’identification pour vos comptes  [!DNL Google Ads] manager.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 4cf04fc7ea22e50b5f56cd278ad9a1aac724edf7
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# Gestion des informations d’identification des comptes de gestionnaire de réseau publicitaire

*[!DNL Google Ads]comptes uniquement*

Indiquez les informations d’identification de vos comptes de gestionnaire [!DNL Google Ads] vers lesquels vous souhaitez que Search, Social et Commerce charge les conversions entre comptes. Utilisez cette fonction si vous souhaitez a) télécharger des mesures de conversion inter-comptes suivies de [!DNL Adobe] vers un compte de gestionnaire [!DNL Google Ads] ou b) charger des objectifs de portefeuille qui incluent des conversions entre comptes vers [!DNL Google Ads] pour une optimisation hybride.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Vous pouvez ajouter des informations d’identification pour les nouveaux enregistrements de compte de gestionnaire ou réauthentifier un compte de gestionnaire existant.

Une fois que vous avez ajouté les informations d’identification d’un compte de gestionnaire, les paramètres du compte affichent l’identifiant de compte de gestionnaire associé en lecture seule. En outre, une colonne &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; facultative dans la vue [!UICONTROL Campaigns] > [!UICONTROL Accounts] affiche l’identifiant du compte de gestionnaire pour chaque compte enfant et indique une erreur lorsque le compte de gestionnaire n’est pas authentifié. [!UICONTROL Notification Center] comprend des notifications lorsque les informations d’identification d’un compte de gestionnaire sont manquantes ([le [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) ou lorsqu’un jeton d’authentification de compte de gestionnaire expire ([le [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Pour ajouter des informations d’identification pour un nouveau compte de gestionnaire

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Sélectionnez **[!UICONTROL Create new manager account]**.

1. Saisissez les informations de connexion pour le compte du gestionnaire.

   Les **[!UICONTROL Manager Account ID]** et **[!UICONTROL Login Email]** sont obligatoires. Search, Social et Commerce capture et stocke automatiquement le jeton de compte à utiliser pour l’authentification.

   Vous pouvez éventuellement inclure un **[!UICONTROL MCC Account Name]** pour l’identification dans Search, Social, &amp; Commerce et le compte **[!UICONTROL Password]**. Saisissez le mot de passe à chiffrer et enregistrez-le afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

1. Cliquez sur **[!UICONTROL Authenticate]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Pour réauthentifier un compte de gestionnaire existant

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Sélectionnez **[!UICONTROL Reauthenticate existing manager account]**.

1. Sélectionnez le compte du gestionnaire.

1. Saisissez les informations de connexion pour le compte du gestionnaire.

   **[!UICONTROL Manager Account ID]** et **Login Email** sont requis. Search, Social et Commerce capture et stocke automatiquement le jeton de compte à utiliser pour l’authentification.

   Vous pouvez éventuellement inclure un **[!UICONTROL MCC Account Name]** pour l’identification dans Search, Social, &amp; Commerce et le compte **[!UICONTROL Password]**. Saisissez le mot de passe à chiffrer et enregistrez-le afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

1. Cliquez sur **[!UICONTROL Authenticate]**.

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Activer le téléchargement des objectifs vers les réseaux publicitaires](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [ Télécharger des mesures de conversion vers  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Modifier les paramètres de notification](/help/search-social-commerce/notifications/notification-edit.md)
