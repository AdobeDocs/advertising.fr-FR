---
title: Gestion des informations d’identification pour les comptes du gestionnaire de réseau publicitaire
description: Découvrez comment fournir des informations d’identification pour vos comptes  [!DNL Google Ads] .
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Gestion des informations d’identification pour les comptes du gestionnaire de réseau publicitaire

Comptes *[!DNL Google Ads]uniquement*

Indiquez les informations d’identification des comptes [!DNL Google Ads] Manager sur lesquels vous souhaitez que Search, Social et Commerce chargent les conversions entre comptes. Utilisez cette fonctionnalité dans deux scénarios : si vous souhaitez télécharger des mesures de conversion entre comptes suivies par des [!DNL Adobe] vers un compte [!DNL Google Ads] Manager ou pour télécharger des objectifs de portfolio qui incluent des conversions entre comptes vers [!DNL Google Ads] pour obtenir une optimisation hybride.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Vous pouvez ajouter des informations d’identification pour les nouveaux enregistrements de compte Manager ou réauthentifier un compte Manager existant.

Une fois que vous avez ajouté les informations d’identification d’un compte Manager, les paramètres du compte affichent l’identifiant de compte Manager associé en lecture seule. En outre, une colonne « [!UICONTROL Manager Account for Cross-Account Conversions] » facultative dans la vue [!UICONTROL Campaigns] > [!UICONTROL Accounts] affiche l’identifiant du compte responsable pour chaque compte enfant et indique une erreur lorsque le compte responsable n’est pas authentifié. [!UICONTROL Notification Center] inclut des notifications lorsque les informations d’identification d’un compte Manager sont manquantes ([le [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) ou lorsqu’un jeton d’authentification du compte Manager expire ([le [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Pour ajouter des informations d’identification pour un nouveau compte de responsable

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Sélectionnez **[!UICONTROL Create new manager account]**.

1. Saisissez les informations de connexion pour le compte du responsable.

   Les **[!UICONTROL Manager Account ID]** et **[!UICONTROL Login Email]** sont obligatoires. Search, Social et Commerce capture et stocke automatiquement le jeton de compte à utiliser pour l’authentification.

   Vous pouvez éventuellement inclure un **[!UICONTROL MCC Account Name]** d’identification dans Search, Social et Commerce, ainsi que dans le **[!UICONTROL Password]** du compte. Saisissez le mot de passe lorsque vous souhaitez le chiffrer et enregistrez-le afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

1. Cliquez sur **[!UICONTROL Authenticate]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Pour réauthentifier un compte Manager existant

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Sélectionnez **[!UICONTROL Reauthenticate existing manager account]**.

1. Sélectionnez le compte du responsable.

1. Saisissez les informations de connexion pour le compte du responsable.

   Les champs **[!UICONTROL Manager Account ID]** et **E-mail de connexion** sont obligatoires. Search, Social et Commerce capture et stocke automatiquement le jeton de compte à utiliser pour l’authentification.

   Vous pouvez éventuellement inclure un **[!UICONTROL MCC Account Name]** d’identification dans Search, Social et Commerce, ainsi que dans le **[!UICONTROL Password]** du compte. Saisissez le mot de passe lorsque vous souhaitez le chiffrer et enregistrez-le afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

1. Cliquez sur **[!UICONTROL Authenticate]**.

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Activer le chargement des objectifs sur les réseaux publicitaires](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Charger les mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Modifier vos paramètres de notification](/help/search-social-commerce/notifications/notification-edit.md)
