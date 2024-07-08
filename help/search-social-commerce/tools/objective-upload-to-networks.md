---
title: Activer le chargement d’objectifs vers des réseaux publicitaires
description: Découvrez comment transférer les objectifs de vos portefeuilles hybrides vers [!DNL Google Ads] ET [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Activer le chargement d’objectifs vers des réseaux publicitaires

*Annonceurs avec [!DNL Google Ads] et [!DNL Microsoft Advertising] comptes uniquement*

*Annonceurs activés pour l’optimisation hybride uniquement*

Search, Social &amp; Commerce peut télécharger les objectifs des portefeuilles d’un compte publicitaire vers [!DNL Google Ads] et [!DNL Microsoft Advertising] vous pouvez donc les utiliser pour une optimisation hybride. Vos objectifs chargés sont disponibles en tant qu’actions de conversion pour les objectifs de conversion personnalisés au niveau du compte et de la campagne.

L’activation de cette option déclenche automatiquement un chargement pour les objectifs dans les portefeuilles qui contiennent des campagnes avec des stratégies d’enchères intelligentes. Search, Social, &amp; Commerce crée une conversion sur le réseau publicitaire pour chaque objectif applicable. La conversion représente toutes les mesures de conversion pondérées de l’objectif. Chaque conversion porte l’un des noms suivants :

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  où `<network_ID>` est l’ID numérique que Search, Social, &amp; Commerce utilise pour le réseau publicitaire, `<objective_id>` est l’ID d’objectif numérique et `<network_account_ID>` est l’ID numérique du compte du réseau publicitaire ou du compte gestionnaire.

* (Ancien format qui sera abandonné à l’avenir) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  où `<portfolio_id>` est l’ID de portfolio numérique et `<se_acctid/conversion_manager_se_acctid>` est l’ID numérique pour le compte de réseau publicitaire ou le compte de gestion.

  Votre équipe de compte Adobe travaillera avec vous pour migrer vos noms d’action de conversion existants au sein du réseau publicitaire avant que l’ancien format ne soit obsolète. Pendant la période de migration, les transferts de l’ancien et du nouveau format s’exécuteront en parallèle. La modélisation et l’optimisation ne sont pas affectées car les nouvelles actions de conversion apparaissent initialement avec le statut « secondaire » (non optimisé) et avec 90 jours de données de renvoi.

Les téléchargements ont lieu [!DNL Google Ads] tous les jours à 6h00 dans le fuseau horaire de l’annonceur. Les téléchargements ont lieu [!DNL Microsoft Advertising] tous les jours à 9h00 dans le fuseau horaire de l’annonceur.

>[!IMPORTANT]
>
>Les conversions suivies par Google Ads et par la balise de suivi d’événement universel (UET) Microsoft Advertising ne sont pas réimportées sur les réseaux publicitaires. Si vous les incluez dans un objectif, ajoutez-les aux objectifs de la campagne dans l’éditeur du réseau publicitaire.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Cochez la case en regard de **[!UICONTROL Enable Objective Upload]**.

1. (Les annonceurs disposant [!DNL Google Ads] de comptes qui exercent leurs activités dans l’Espace économique européen (EEE) ou au Royaume-Uni (Royaume-Uni) ; facultatif) Si vous avez recueilli le consentement des utilisateurs de l’EEE et du Royaume-Uni pour télécharger leurs données à des fins publicitaires, cochez la case en regard de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Cliquez sur **[!UICONTROL Save]**.

1. (Si vos conversions sont suivies au niveau du compte administrateur) [Ajoutez les informations d’identification pour votre compte](/help/search-social-commerce/admin/manager-accounts.md) administrateur à **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Vérifiez que chaque objectif – nommé `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` – apparaît dans les deux jours sur le réseau publicitaire.

   Dans l’éditeur [!DNL Google Ads] , recherchez vos [actions](https://support.google.com/google-ads/answer/11461796) de conversion. Dans l’éditeur [!DNL Microsoft Advertising] , recherchez vos [objectifs](https://help.ads.microsoft.com/#apex/ads/en/56709) de conversion.

   Si nécessaire, mettez à jour la plage de dates pour inclure la date de transfert.

## Résolution des problèmes liés aux objectifs manquants

Si l’objectif (nommé) `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` de l’un de vos portfolios n’apparaît pas sur le réseau publicitaire, vérifiez les points suivants :

* ([!DNL Google Ads]) Cochez si les conversions doivent être téléchargées au niveau du compte ou du gestionnaire. S’ils doivent être téléchargés au niveau du responsable :

   * Vérifiez si les informations d’identification du [!DNL Google Ads] compte administrateur sont fournies dans **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Si nécessaire, [ajoutez les informations d’identification pour le compte](/help/search-social-commerce/admin/manager-accounts.md) administrateur.

   * Vérifiez si le compte du réseau publicitaire comprend déjà le même nom de mesure. Si tel est le cas, renommez la mesure afin que la propriété de niveau gestionnaire appropriée puisse être créée.

* Vérifiez que l’option « hybride » du portefeuille est sélectionnée et que l’objectif a des revenus valides.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des mesures de conversion d’un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Télécharger des mesures de conversion vers [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
