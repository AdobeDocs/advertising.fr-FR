---
title: (Nouvelle interface utilisateur) Activer le chargement des objectifs sur les réseaux publicitaires
description: Découvrez comment télécharger des objectifs pour vos portfolios hybrides vers Google Ads et Microsoft Advertising.
feature: Search Objectives, Search Optimization
hide: true
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Activer le chargement des objectifs sur les réseaux publicitaires

*Fonction*

*Annonceurs disposant uniquement de comptes [!DNL Google Ads] et [!DNL Microsoft Advertising]*

*Les annonceurs activés pour l’optimisation hybride uniquement*

Search, Social et Commerce peuvent charger les objectifs des portefeuilles d’un compte publicitaire vers [!DNL Google Ads] et [!DNL Microsoft Advertising] afin que vous puissiez les utiliser dans le cadre d’une optimisation hybride. Vos objectifs chargés sont disponibles sous forme d’actions de conversion pour les objectifs de conversion personnalisés au niveau du compte et de la campagne.

L’activation de cette option déclenche automatiquement un chargement pour les objectifs des portefeuilles contenant des campagnes avec des stratégies d’enchères intelligentes. Search, Social et Commerce génèrent une conversion sur le réseau publicitaire pour chaque objectif applicable. La conversion représente toutes les mesures de conversion pondérées de l’objectif au niveau de l’identifiant EF (identifiant de clic). Pour les clics [!DNL Google Ads], l’ID EF est le `gclid` [!DNL Google Ads] ; pour les clics [!DNL Microsoft Advertising], l’ID EF est le `msclkid` [!DNL Microsoft Advertising]. Grâce à cet identifiant de clic, les données de conversion peuvent être mappées au mot-clé spécifique et au temps de clic.

Chaque conversion chargée porte le nom suivant :

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

où `<network_ID>` est l’identifiant numérique utilisé par Search, Social et Commerce pour le réseau publicitaire, `<objective_ID>` est l’identifiant numérique de l’objectif et `<network_account_ID>` est l’identifiant numérique du compte ou du gestionnaire du réseau publicitaire.

Les chargements vers [!DNL Google Ads] et [!DNL Microsoft Advertising] ont lieu toute la journée, généralement toutes les heures. Pour les annonceurs et annonceuses disposant de comptes volumineux ou de configurations personnalisées, les chargements ont lieu au moins trois fois par jour.

>[!IMPORTANT]
>
>Les conversions suivies par [!DNL Google Ads] et par la balise de suivi d’événement universel (UET) [!DNL Microsoft Advertising] ne sont pas rechargées sur les réseaux publicitaires. Si vous les incluez dans un objectif, vous devez les ajouter aux objectifs de la campagne dans l’éditeur du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]** > **[!UICONTROL Objectives]**.

1. Dans la barre d’outils, cliquez sur **[!UICONTROL Upload Objective]**.

1. Dans la boîte de dialogue [!UICONTROL Objective Upload Setup], définissez le bouton **[!UICONTROL Enable Objective Upload]** sur **[!UICONTROL On]**.

1. (Annonceurs disposant de comptes [!DNL Google Ads] qui font des affaires dans l’Espace économique européen (EEE) ou au Royaume-Uni (UK) ; facultatif) Si vous avez obtenu le consentement des utilisateurs de l’EEE et du Royaume-Uni pour télécharger leurs données à des fins publicitaires, cochez la case pour confirmer que les consentements des utilisateurs de l’EEE et du Royaume-Uni ont été collectés. Cela envoie le statut de consentement **[!UICONTROL GRANTED]** à [!DNL Google Ads] et [!DNL Microsoft Advertising]. Si cette option n’est pas cochée, le statut de consentement est envoyé en tant que **[!UICONTROL UNSPECIFIED]**.

1. (Si vos conversions sont suivies au niveau du compte du responsable) [Ajoutez les informations d’identification pour votre compte du responsable](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md) avant d’enregistrer.

1. Cliquez sur **[!UICONTROL Save]**.

1. Vérifiez que chaque objectif — nommé `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — apparaît dans les deux jours sur le réseau publicitaire.

   Dans l’éditeur de [!DNL Google Ads], recherchez vos [ actions de conversion ](https://support.google.com/google-ads/answer/11461796){target="_blank"}. Dans l’éditeur de [!DNL Microsoft Advertising], recherchez vos [ objectifs de conversion ](https://help.ads.microsoft.com/#apex/ads/en/56709){target="_blank"}.

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
>Vous pouvez afficher les données relatives au chiffre d’affaires pondéré d’Adobe Advertising dans les rapports du réseau publicitaire. Il est recommandé de comparer le chiffre d’affaires pondéré à la conv [!DNL Google Ads] « Tous ». (par conv. time) » ou la mesure [!DNL Microsoft Advertising] « All conv. chiffre d’affaires », segmenté en fonction de la mesure O_ACS_OBJ*.

## Résolution des problèmes liés aux objectifs manquants

Si l’objectif (nommé `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`) de l’un de vos portefeuilles n’apparaît pas sur le réseau publicitaire, vérifiez les points suivants :

* ([!DNL Google Ads]) Vérifiez si les conversions doivent être téléchargées au niveau du compte ou du responsable. S’ils doivent être chargés au niveau du responsable :

   * Vérifiez si les informations d’identification du compte [!DNL Google Ads] Manager sont fournies. Si nécessaire, [ajoutez les informations d’identification du compte Manager](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md).

   * Vérifiez si le compte réseau publicitaire inclut déjà le même nom de mesure. Si c’est le cas, renommez la mesure afin de pouvoir créer la propriété de niveau responsable appropriée.

* Vérifiez que l&#39;option « hybride » du portefeuille est sélectionnée et que l&#39;objectif a un chiffre d&#39;affaires valide.

>[!MORELIKETHIS]
>
>* [À propos des objectifs](objective-about.md)
>* [Gérer les mesures de conversion d’un annonceur](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)
>* [Gérer les informations d’identification pour les comptes  [!DNL Google Ads]  responsable](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
