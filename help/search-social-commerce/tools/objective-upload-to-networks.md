---
title: Activer le téléchargement des objectifs vers les réseaux publicitaires
description: Découvrez comment télécharger des objectifs pour vos portefeuilles hybrides vers [!DNL Google Ads] et [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 0fb03410e67be28d24496c948b52399c8465e041
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Activer le téléchargement des objectifs vers les réseaux publicitaires

*Annonceurs avec [!DNL Google Ads] et [!DNL Microsoft® Advertising] comptes uniquement*

*Publicitaires activés uniquement pour l’optimisation hybride*

Si votre compte publicitaire est configuré pour utiliser l’optimisation hybride, Adobe Advertising peut éventuellement télécharger les objectifs des portefeuilles du compte vers [!DNL Google Ads] et [!DNL Microsoft® Advertising] en tant que conversions afin que vous puissiez les utiliser pour l’optimisation hybride.

L’activation de cette option déclenche automatiquement un chargement pour les portfolios qui contiennent des campagnes avec des stratégies d’offres intelligentes. Search, Social et Commerce crée une conversion sur le réseau publicitaire pour chaque combinaison portefeuille-objectif applicable. Chaque conversion porte le nom `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, où `<portfolio_id>` est l’identifiant numérique de portefeuille et `<se_acctid/conversion_manager_se_acctid>` est l’identifiant numérique du compte réseau publicitaire ou du compte de gestionnaire. La conversion représente toutes les mesures de conversion pondérées de l’objectif.

Téléchargements vers [!DNL Google Ads] surviennent tous les jours à 06h00 dans le fuseau horaire de l’annonceur. Téléchargements vers [!DNL Microsoft® Advertising] surviennent tous les jours à 09h00 dans le fuseau horaire de l’annonceur.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Cochez la case en regard de **[!UICONTROL Enable Objective Upload]**.

   Cette option est disponible uniquement si votre compte publicitaire est configuré pour utiliser l’optimisation hybride. Pour activer l’optimisation hybride, contactez votre équipe de compte d’Adobe.

1. (Publicitaires avec [!DNL Google Ads] Comptes qui commercent dans l’Espace économique européen (EEE) ou au Royaume-Uni (Royaume-Uni) ; facultatif) Si vous avez obtenu le consentement des utilisateurs de l’EEE et du Royaume-Uni pour télécharger leurs données à des fins publicitaires, cochez la case en regard de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Cliquez sur **[!UICONTROL Save]**.

1. (Si les conversions sont suivies au niveau du compte de gestionnaire) [Ajout des informations d’identification de votre compte de gestionnaire](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des mesures de conversion d’un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Chargement des mesures de conversion dans [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
