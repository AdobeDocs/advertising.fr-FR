---
title: Activer le chargement des objectifs sur les réseaux publicitaires
description: Découvrez comment charger des objectifs pour vos portfolios hybrides vers [!DNL Google Ads] et [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Activer le chargement des objectifs sur les réseaux publicitaires

*Annonceurs disposant uniquement de comptes [!DNL Google Ads] et [!DNL Microsoft Advertising]*

*Les annonceurs activés pour l’optimisation hybride uniquement*

Search, Social et Commerce peuvent charger les objectifs des portefeuilles d’un compte publicitaire vers [!DNL Google Ads] et [!DNL Microsoft Advertising] afin que vous puissiez les utiliser dans le cadre d’une optimisation hybride. Vos objectifs chargés sont disponibles sous forme d’actions de conversion pour les objectifs de conversion personnalisés au niveau du compte et de la campagne.

L’activation de cette option déclenche automatiquement un chargement pour les objectifs des portefeuilles contenant des campagnes avec des stratégies d’enchères intelligentes. Search, Social et Commerce génèrent une conversion sur le réseau publicitaire pour chaque objectif applicable. La conversion représente toutes les mesures de conversion pondérées de l’objectif au niveau de l’identifiant EF (identifiant de clic). Pour les clics [!DNL Google Ads], l’ID EF est le `gclid` [!DNL Google Ads] ; pour les clics [!DNL Microsoft Advertising], l’ID EF est le `msclkid` [!DNL Microsoft Advertising]. Grâce à cet identifiant de clic, les données de conversion peuvent être mappées au mot-clé spécifique et au temps de clic.

Chaque conversion chargée porte le nom suivant :

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

où `<network_ID>` est l’identifiant numérique utilisé par Search, Social et Commerce pour le réseau publicitaire, `<objective_id>` est l’identifiant numérique de l’objectif et `<network_account_ID>` est l’identifiant numérique du compte ou du gestionnaire du réseau publicitaire.

Les téléchargements vers [!DNL Google Ads] ont lieu tous les jours à 06:00, dans le fuseau horaire de l’annonceur. Les téléchargements vers [!DNL Microsoft Advertising] ont lieu tous les jours à 9 h dans le fuseau horaire de l’annonceur.

>[!IMPORTANT]
>
>Les conversions suivies par les publicités Google et par la balise de suivi des événements universels (UET) d’Advertising Microsoft ne sont pas rechargées sur les réseaux publicitaires. Si vous les incluez dans un objectif, vous devez les ajouter aux objectifs de la campagne dans l’éditeur du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Cochez la case en regard de **[!UICONTROL Enable Objective Upload]**.

1. (Annonceurs disposant de comptes [!DNL Google Ads] qui font des affaires dans l’Espace économique européen (EEE) ou au Royaume-Uni (UK) ; facultatif) Si vous avez obtenu le consentement des utilisateurs de l’EEE et du Royaume-Uni pour télécharger leurs données à des fins publicitaires, cochez la case en regard de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Cliquez sur **[!UICONTROL Save]**.

1. (Si vos conversions font l’objet d’un suivi au niveau du compte du responsable) [Ajoutez les informations d’identification pour votre compte du responsable](/help/search-social-commerce/admin/manager-accounts.md) à l’adresse **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Vérifiez que chaque objectif — nommé `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — apparaît dans les deux jours sur le réseau publicitaire.

   Dans l’éditeur de [!DNL Google Ads], recherchez vos [ actions de conversion ](https://support.google.com/google-ads/answer/11461796). Dans l’éditeur de [!DNL Microsoft Advertising], recherchez vos [ objectifs de conversion ](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Si nécessaire, mettez à jour la période pour inclure la date de chargement.

## Méthode de calcul de l’objectif pondéré

L’objectif pondéré transmis au réseau publicitaire est la somme de toutes les valeurs de mesure collectées, à l’exception des conversions suivies par [!DNL Google Ads] ou par la balise de suivi d’événement universel (UET) [!DNL Microsoft Advertising]. La valeur est calculée à l’aide de la méthode d’attribution configurée pour le compte Search, Social et Commerce de l’annonceur.

Supposons, par exemple, que la mesure d’objectif soit Ajouts au panier avec un poids de 25 et que vos mesures d’assistance incluent GGL_Lead et Revenue avec un poids de 1 et Téléchargements avec un poids de 0,5.

![Exemple d’objectif pondéré](/help/search-social-commerce/assets/objective-example.png "Exemple d’objectif pondéré")

Supposons qu’un mot-clé entraîne les actions suivantes pour le portfolio :

* 10 Ajouts au panier
* Chiffre d’affaires de 500 $
* 50 téléchargements
* 5 GGL_Lead

GGL_Lead n’est pas inclus dans le calcul/chargement car il s’agit d’une mesure suivie par Google Ads. La valeur objective pondérée est donc calculée comme suit : ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>Vous pouvez afficher les données relatives au chiffre d’affaires pondéré d’Adobe Advertising dans les rapports du réseau publicitaire. Il est recommandé de comparer le chiffre d’affaires pondéré à la conv [!DNL Google Ads] « Tous ». (par conv. time) » ou la mesure [!DNL Microsoft Advertising] « All conv. chiffre d’affaires », segmenté à la mesure O_ACS_OBJ*.<!--clarify -->

## Résolution des problèmes liés aux objectifs manquants

Si l’objectif (nommé `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`) de l’un de vos portefeuilles n’apparaît pas sur le réseau publicitaire, vérifiez les points suivants :

* ([!DNL Google Ads]) Vérifiez si les conversions doivent être téléchargées au niveau du compte ou du responsable. S’ils doivent être chargés au niveau du responsable :

   * Vérifiez si les informations d’identification du compte [!DNL Google Ads] Manager sont fournies sous **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Si nécessaire, [ajoutez les informations d’identification du compte Manager](/help/search-social-commerce/admin/manager-accounts.md).

   * Vérifiez si le compte réseau publicitaire inclut déjà le même nom de mesure. Si c’est le cas, renommez la mesure afin de pouvoir créer la propriété de niveau responsable appropriée.

* Vérifiez que l&#39;option « hybride » du portefeuille est sélectionnée et que l&#39;objectif a un chiffre d&#39;affaires valide.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des mesures de conversion d’un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Charger les mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
