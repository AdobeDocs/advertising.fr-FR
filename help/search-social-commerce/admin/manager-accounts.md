---
title: Gestion des informations d’identification des comptes de gestionnaire de réseau publicitaire
description: Découvrez comment fournir des informations d’identification pour votre [!DNL Google Ads] comptes de gestion.
exl-id: bde22f70-12a7-4eef-a141-dafeed9a7dc5
feature: Search Admin
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# Gestion des informations d’identification des comptes de gestionnaire de réseau publicitaire

*Fonctionnalité bêta*

*[!DNL Google Ads]comptes uniquement*

Indiquez les informations d’identification de votre [!DNL Google Ads] de gérer les comptes vers lesquels vous souhaitez que Search, Social et Commerce charge les conversions entre comptes. Utilisez cette fonctionnalité si vous souhaitez) télécharger [!DNL Adobe]mesures de conversion entre comptes suivis en une [!DNL Google Ads] compte de gestionnaire ou b) transférer des objectifs de portefeuille qui incluent des conversions entre comptes en [!DNL Google Ads] pour l’optimisation hybride.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Vous pouvez ajouter des informations d’identification pour les nouveaux enregistrements de compte de gestionnaire ou réauthentifier un compte de gestionnaire existant.

Une fois que vous avez ajouté les informations d’identification d’un compte de gestionnaire, les paramètres du compte affichent l’identifiant de compte de gestionnaire associé en lecture seule. En outre, un[!UICONTROL Manager Account for Cross-Account Conversions]&quot; dans la colonne [!UICONTROL Campaigns] > [!UICONTROL Accounts] affiche l’identifiant du compte du gestionnaire pour chaque compte enfant et indique une erreur lorsque le compte du gestionnaire n’est pas authentifié. [!UICONTROL Notification Center] inclut des notifications lorsque les informations d’identification d’un compte de gestionnaire sont manquantes ([la valeur [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) ou lorsqu’un jeton d’authentification de compte de gestionnaire expire ([la valeur [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Pour ajouter des informations d’identification pour un nouveau compte de gestionnaire

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Sélectionner **[!UICONTROL Create new manager account]**.

1. Saisissez les informations de connexion pour le compte du gestionnaire.

   La variable **[!UICONTROL Manager Account ID]** et **[!UICONTROL Login Email]** sont obligatoires. Search, Social et Commerce capture et stocke automatiquement le jeton de compte à utiliser pour l’authentification.

   Vous pouvez éventuellement inclure une **[!UICONTROL MCC Account Name]** pour l’identification dans Search, Social et Commerce et le compte. **[!UICONTROL Password]**. Saisissez le mot de passe à chiffrer et enregistrez-le afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

1. Cliquez sur **[!UICONTROL Authenticate]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Pour réauthentifier un compte de gestionnaire existant

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Sélectionner **[!UICONTROL Reauthenticate existing manager account]**.

1. Sélectionnez le compte du gestionnaire.

1. Saisissez les informations de connexion pour le compte du gestionnaire.

   La variable **[!UICONTROL Manager Account ID]** et **Adresse électronique de connexion** sont obligatoires. Search, Social et Commerce capture et stocke automatiquement le jeton de compte à utiliser pour l’authentification.

   Vous pouvez éventuellement inclure une **[!UICONTROL MCC Account Name]** pour l’identification dans Search, Social et Commerce et le compte. **[!UICONTROL Password]**. Saisissez le mot de passe à chiffrer et enregistrez-le afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

1. Cliquez sur **[!UICONTROL Authenticate]**.

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Activer le téléchargement des objectifs vers les réseaux publicitaires](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Chargement des mesures de conversion dans [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Modification des paramètres de notification](/help/search-social-commerce/notifications/notification-edit.md)
