---
title: Activer le téléchargement des objectifs vers les réseaux publicitaires
description: Découvrez comment télécharger des objectifs pour vos portefeuilles hybrides vers  [!DNL Google Ads] et [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Activer le téléchargement des objectifs vers les réseaux publicitaires

*Publicitaires avec [!DNL Google Ads] et [!DNL Microsoft Advertising] comptes uniquement*

*Annonceurs activés pour l’optimisation hybride uniquement*

Search, Social et Commerce peuvent transférer les objectifs des portefeuilles d’un compte d’annonceur vers [!DNL Google Ads] et [!DNL Microsoft Advertising] afin que vous puissiez les utiliser pour une optimisation hybride. Vos objectifs téléchargés sont disponibles en tant qu’actions de conversion pour les objectifs de conversion personnalisés au niveau du compte et de la campagne.

L’activation de cette option déclenche automatiquement un chargement pour les objectifs dans les portfolios qui contiennent des campagnes avec des stratégies d’offres intelligentes. Search, Social et Commerce crée une conversion sur le réseau publicitaire pour chaque objectif applicable. La conversion représente toutes les mesures de conversion pondérées de l’objectif au niveau de l’identifiant de clic (EF ID). Pour [!DNL Google Ads] clics, l’identifiant EF est [!DNL Google Ads] `gclid` ; pour [!DNL Microsoft Advertising] clics, l’identifiant EF est [!DNL Microsoft Advertising] `msclkid`. En raison de cet identifiant de clic, les données de conversion peuvent être mappées au mot-clé spécifique et à l’heure des clics.

Chaque conversion téléchargée porte le nom suivant :

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

où `<network_ID>` est l’identifiant numérique utilisé par Search, Social et Commerce pour le réseau publicitaire, `<objective_id>` est l’identifiant de l’objectif numérique et `<network_account_ID>` est l’identifiant numérique du compte du gestionnaire ou du compte du réseau publicitaire.

Les téléchargements vers [!DNL Google Ads] ont lieu tous les jours à 06h00 dans le fuseau horaire de l’annonceur. Les téléchargements vers [!DNL Microsoft Advertising] ont lieu tous les jours à 9h00 dans le fuseau horaire de l’annonceur.

>[!IMPORTANT]
>
>Les conversions suivies par Google Ads et par la balise de suivi universel d’événement (UET) Microsoft Advertising ne sont pas rechargées vers les réseaux publicitaires. Si vous les incluez dans un objectif, vous devez les ajouter aux objectifs de campagne dans l’éditeur du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Cochez la case en regard de **[!UICONTROL Enable Objective Upload]**.

1. (Publicitaires disposant de comptes [!DNL Google Ads] qui exercent des activités dans l’Espace économique européen (EEE) ou au Royaume-Uni (Royaume-Uni) ; facultatif) Si vous avez collecté le consentement des utilisateurs de l’EEE et du Royaume-Uni pour télécharger leurs données à des fins publicitaires, cochez la case en regard de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Cliquez sur **[!UICONTROL Save]**.

1. (Si vos conversions sont suivies au niveau du compte du gestionnaire) [Ajoutez des informations d’identification pour votre compte du gestionnaire](/help/search-social-commerce/admin/manager-accounts.md) à l’adresse **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Vérifiez que chaque objectif — nommé `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — apparaît dans les deux jours sur le réseau publicitaire.

   Dans l’éditeur [!DNL Google Ads], recherchez vos [actions de conversion](https://support.google.com/google-ads/answer/11461796). Dans l’éditeur [!DNL Microsoft Advertising], recherchez vos [objectifs de conversion](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Si nécessaire, mettez à jour la période pour inclure la date de transfert.

## Méthode de calcul de l’objectif pondéré

L’objectif pondéré transmis au réseau publicitaire est la somme de toutes les valeurs de mesure collectées, à l’exception des conversions suivies par [!DNL Google Ads] ou par la balise de suivi d’événement universel (UET) [!DNL Microsoft Advertising]. La valeur est calculée en utilisant la méthode d’attribution configurée pour le compte Search, Social et Commerce de l’annonceur.

Supposons, par exemple, que la mesure d’objectif de l’objectif soit Ajouts au panier avec un poids de 25, et que vos mesures d’assistance incluent GGL_Lead et Recettes avec un poids de 1 et Téléchargements avec un poids de 0,5.

![Exemple d&#39;un objectif pondéré](/help/search-social-commerce/assets/objective-example.png "Exemple d&#39;un objectif pondéré")

Supposons qu’un mot-clé ait entraîné les actions suivantes pour le portefeuille :

* 10 ajouts au panier
* Recettes de 500 $
* 50 téléchargements
* 5 GGL_Lead

GGL_Lead n’est pas inclus dans le calcul/chargement, car il s’agit d’une mesure suivie par Google Ads. La valeur objective pondérée est donc calculée comme suit : ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>Vous pouvez afficher les données relatives aux recettes pondérées par Adobe Advertising dans les rapports du réseau publicitaire. Il est recommandé de comparer les recettes pondérées à la conv [!DNL Google Ads] &quot;All. (par conv. time)&quot; ou la mesure [!DNL Microsoft Advertising] &quot;All conv. revenue,&quot; segmenté à la mesure O_ACS_OBJ*.<!--clarify -->

## Résolution des problèmes liés aux objectifs manquants

Si l’objectif — nommé `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — pour l’un de vos portefeuilles n’apparaît pas sur le réseau publicitaire, vérifiez les points suivants :

* ([!DNL Google Ads]) Vérifiez si les conversions doivent être chargées au niveau du compte ou du gestionnaire. Si elles doivent être chargées au niveau du responsable :

   * Vérifiez si les informations d’identification du compte de gestionnaire [!DNL Google Ads] sont fournies sous **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Si nécessaire, [ajoutez les informations d’identification du compte de gestionnaire](/help/search-social-commerce/admin/manager-accounts.md).

   * Vérifiez si le compte réseau publicitaire inclut déjà le même nom de mesure. Si tel est le cas, renommez la mesure afin de pouvoir créer la propriété correcte au niveau du gestionnaire.

* Vérifiez que l’option &quot;hybride&quot; du portfolio est sélectionnée et que l’objectif dispose de recettes valides.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des mesures de conversion d’un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [ Télécharger les mesures de conversion de recherche, de Social et de suivi Commerce vers  [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
