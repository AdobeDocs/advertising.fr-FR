---
title: Activer le téléchargement des objectifs vers les réseaux publicitaires
description: Découvrez comment télécharger des objectifs pour vos portefeuilles hybrides vers [!DNL Google Ads] et [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: a61bdd9c68420a16a01057d8a3ac03d659d2ad3f
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Activer le téléchargement des objectifs vers les réseaux publicitaires

*Annonceurs avec [!DNL Google Ads] et [!DNL Microsoft® Advertising] comptes uniquement*

*Publicitaires activés uniquement pour l’optimisation hybride*

Search, Social et Commerce peuvent télécharger les objectifs des portfolios d’un compte publicitaire vers [!DNL Google Ads] et [!DNL Microsoft® Advertising] vous pouvez donc les utiliser pour l’optimisation hybride. Vos objectifs téléchargés sont disponibles en tant qu’actions de conversion pour les objectifs de conversion personnalisés au niveau du compte et de la campagne.

L’activation de cette option déclenche automatiquement un chargement pour les objectifs dans les portfolios qui contiennent des campagnes avec des stratégies d’offres intelligentes. Search, Social et Commerce crée une conversion sur le réseau publicitaire pour chaque objectif applicable. La conversion représente toutes les mesures de conversion pondérées de l’objectif. Chaque conversion porte l’un des noms suivants :

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  where `<network_ID>` est l’identifiant numérique utilisé par Search, Social et Commerce pour le réseau publicitaire, `<objective_id>` est l’identifiant d’objectif numérique, et `<network_account_ID>` est l’identifiant numérique du compte réseau publicitaire ou du compte de gestionnaire.

* (Ancien format qui sera obsolète à l’avenir) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  where `<portfolio_id>` est l’identifiant numérique de portefeuille et `<se_acctid/conversion_manager_se_acctid>` est l’identifiant numérique du compte réseau publicitaire ou du compte de gestionnaire.

  Votre équipe de compte d’Adobe vous aidera à migrer les noms de vos actions de conversion existantes dans le réseau publicitaire avant que l’ancien format ne soit abandonné. Pendant la période de migration, les téléchargements de l’ancien et du nouveau format s’exécuteront en parallèle. La modélisation et l’optimisation ne sont pas affectées, car les nouvelles actions de conversion s’affichent initialement avec l’état &quot;secondaire&quot; (non optimisé) et avec 90 jours de données de renvoi.

Téléchargements vers [!DNL Google Ads] surviennent tous les jours à 06h00 dans le fuseau horaire de l’annonceur. Téléchargements vers [!DNL Microsoft® Advertising] surviennent tous les jours à 09h00 dans le fuseau horaire de l’annonceur.

>[!IMPORTANT]
>
>Les conversions suivies par Google Ads et par la balise de suivi d’événement universel (UET) Microsoft Advertising ne sont pas rechargées vers les réseaux publicitaires. Si vous les incluez dans un objectif, ajoutez-les aux objectifs de la campagne dans l’éditeur du réseau publicitaire.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Cochez la case en regard de **[!UICONTROL Enable Objective Upload]**.

1. (Publicitaires avec [!DNL Google Ads] Comptes qui exercent leurs activités dans l’Espace économique européen (EEE) ou au Royaume-Uni (Royaume-Uni) ; facultatif) Si vous avez recueilli le consentement des utilisateurs de l’EEE et du Royaume-Uni pour télécharger leurs données à des fins publicitaires, cochez la case en regard de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Cliquez sur **[!UICONTROL Save]**.

1. (Si les conversions sont suivies au niveau du compte de gestionnaire) [Ajout des informations d’identification de votre compte de gestionnaire](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

Une fois le chargement quotidien terminé, vous pouvez vérifier que les actions de conversion s’affichent dans le réseau publicitaire.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des mesures de conversion d’un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Chargement des mesures de conversion dans [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
