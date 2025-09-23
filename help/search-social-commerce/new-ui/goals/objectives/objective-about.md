---
title: (Nouvelle interface utilisateur) À propos des objectifs
description: Découvrez les objectifs permettant d’atteindre les objectifs de votre entreprise.
feature: Search Objectives, Search Optimization
hide: true
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) À propos des objectifs

*Fonction Beta*

Les objectifs sont des objectifs qu’un annonceur définit pour atteindre ses objectifs commerciaux, tels que maximiser les bénéfices ou atteindre un objectif de vente spécifique. Advertising Search, Social et Commerce et Advertising DSP utilisent tous deux des objectifs :

* Chaque portfolio Search, Social et Commerce doit avoir un objectif afin que la fonctionnalité d’optimisation puisse créer des modèles de clic et de chiffre d’affaires pour le portfolio.

* Dans DSP, les objectifs s’affichent en tant qu’objectifs personnalisés pour les comptes DSP liés aux comptes Search, Social et Commerce. Chaque package qui utilise les objectifs d’optimisation « Retour sur dépenses publicitaires le plus élevé » ou « Coût par acquisition le plus bas » doit inclure un objectif personnalisé qui permet d’atteindre l’objectif d’optimisation global.

Un objectif se compose des mesures de conversion à suivre et à optimiser, ainsi que des poids relatifs de ces mesures. Supposons, par exemple, qu’un magazine en ligne avec deux niveaux d’abonnement en ligne et un niveau d’abonnement papier et l’objectif « maximiser les bénéfices » ait trois mesures : « abonnements en ligne de base » évalués à 20 USD, « abonnements en ligne premium » évalués à 40 USD et « abonnements sur papier » évalués à 30 USD. Si le magazine souhaite donner un poids en fonction de la valeur monétaire unique de l’abonnement, les poids relatifs des mesures seraient respectivement de 1, 2 et 1,5.

Pour chaque mesure de l’objectif, vous pouvez :

* Configurez des poids distincts pour les conversions à partir des appareils mobiles.

* Étiqueter la mesure comme mesure de [!UICONTROL Goal] ou mesure de [!UICONTROL Assist].

* Appliquez des recommandations de poids aux mesures.

>[!NOTE]
>* (Recherche, réseaux sociaux et Commerce) Vous pouvez associer un objectif à un portfolio lorsque vous [créez le portfolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) ou par la suite [modifiez les paramètres du portfolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md).
>* (Annonceurs avec des comptes DSP liés à des comptes Search, Social et Commerce) Dans Advertising DSP, vous pouvez sélectionner un objectif en tant qu’[objectif d’optimisation personnalisée](/help/dsp/campaign-management/packages/package-settings.md) pour un package avec une fréquence au niveau du package.
>* Vous pouvez utiliser le même objectif pour plusieurs portfolios Search, Social et Commerce et/ou plusieurs packages DSP.
>* Les mesures de chaque objectif de la vue [!UICONTROL Objectives] n’incluent pas les données de DSP.

## Mesures disponibles

Vous pouvez inclure l’un des éléments suivants dans vos objectifs :

* Mesures suivies par Adobe Advertising à l’aide du [pixel de suivi de conversion Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* [Mesures suivies par l’annonceur à partir de fichiers de flux de conversion](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* (Annonceurs avec [!DNL Adobe Analytics for Advertising]) [Mesures d’engagement du site et de conversion synchronisées à partir d’Adobe Analytics](/help/integrations/analytics/overview.md).

  Dans Search, Social et Commerce, les [mesures d’engagement du site](/help/integrations/analytics/analytics-data-in-advertising.md) suivantes sont automatiquement prises en compte dans les algorithmes d’offres du portefeuille : `timespent_secs_1stvisit`, `timespent_secs_total`, `pageviews_1stvisit`, `pageviews_total` et `bounces`.

* Mesures [!DNL Google] : <!-- Search only, or might DSP-only clients also have these? -->

   * [[!DNL Google Ads] des conversions suivies ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) à partir de comptes [!DNL Google Ads] synchronisés.

   * (Annonceurs avec [[!DNL Google Analytics] intégrations](/help/search-social-commerce/admin/data-sources/data-source-about.md)) Pages vues, Sessions, Taux de rebond (calculé comme rebonds/sessions) et Durée de la session.

     Dans Search, Social et Commerce, ces mesures sont automatiquement prises en compte dans les algorithmes d’offres du portefeuille.

## Option de chargement des objectifs sur les réseaux publicitaires

Vous pouvez éventuellement [ [!DNL Google Ads]  charger les objectifs des portefeuilles du compte vers et/ou  [!DNL Microsoft Advertising]  tant que conversions](/help/search-social-commerce/tools/objective-upload-to-networks.md) afin de les utiliser pour une optimisation au niveau de la campagne ou du groupe publicitaire. Lorsque vous activez cette option, Search, Social et Commerce transmettent quotidiennement au réseau publicitaire les données pondérées relatives au chiffre d’affaires au niveau de l’identifiant EF (identifiant de clic). Il omet toutes les mesures suivies par le réseau publicitaire.

>[!MORELIKETHIS]
>
>* [Créer un objectif](objective-create.md)
>* [Modifier un objectif](objective-edit.md)
>* [Supprimer un objectif](objective-delete.md)
>* [Appliquer des recommandations de poids à un objectif](objective-apply-weight-recommendations.md)
>* [Paramètres des objectifs](objective-settings.md)
