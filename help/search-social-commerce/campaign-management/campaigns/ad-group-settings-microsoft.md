---
title: "[!DNL Microsoft Advertising] paramètres du groupe publicitaire"
description: Référencez les paramètres pour [!DNL Microsoft Advertising] groupes publicitaires.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] paramètres du groupe publicitaire

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Nom unique du groupe d’annonces dans la campagne. La longueur maximale est de 128 caractères.

**[!UICONTROL Status]:** État d’affichage du groupe publicitaire : *Principal* ou *En pause*. La valeur par défaut pour les nouveaux groupes d’annonces est *Principal*.

**[!UICONTROL Ad Language]:** Langue cible des publicités.<!-- Which campaign types? Not there for audience image-based ad groups. -->

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** Comment et où placer des publicités dans le groupe publicitaire :

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (valeur par défaut) : Pour lancer des offres pour les publicités sur le réseau de recherche.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* Pour lancer des offres publicitaires sur des sites partenaires syndiqués.

* *[!UICONTROL Content network]:* Obsolète

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Obsolète

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Groupes d’audiences) Si :

* *[!UICONTROL Target and Bid]:* Pour afficher les publicités uniquement aux utilisateurs associés aux audiences cibles qui correspondent également à d’autres cibles du groupe publicitaire.

* *[!UICONTROL Bid Only]:* Afficher les publicités même aux personnes qui ne sont pas associées aux audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire. Vous pouvez toutefois augmenter les chances d&#39;affichage des publicités à des audiences spécifiques en définissant des offres plus élevées pour ces audiences.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Pour [!DNL Microsoft Advertising] groupes publicitaires du réseau d’audience, les modificateurs d’offre pour les cibles de localisation ne sont pas optimisés dans les portefeuilles standard avec le paramètre &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (groupes d’audiences ; (facultatif) Des sexes spécifiques à inclure ou à exclure en tant que cibles : *[!UICONTROL Male]*, *[!UICONTROL Female]*, et *[!UICONTROL Unknown]*. Par défaut, tous les sexes sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle situé à côté de celle-ci afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque sexe ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle en regard de celle-ci afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Age]:** (groupes d’audiences ; (facultatif) Catégories d’âge spécifiques à inclure ou à exclure en tant que cibles : *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*, et *[!UICONTROL Unknown]*. Par défaut, toutes les pages sont ciblées. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle situé à côté de celle-ci afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque âge ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle en regard de celle-ci afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Industry]:** (groupes d’audiences ; (facultatif) industries spécifiques à inclure ou à exclure en tant que cibles. Par défaut, tous les secteurs sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle situé à côté de celle-ci afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque secteur ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle en regard de celle-ci afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Job Function Targets]:** (groupes d’audiences ; (facultatif) Fonctions de tâche spécifiques à inclure ou à exclure en tant que cibles. Par défaut, toutes les fonctions de tâche sont ciblées. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle situé à côté de celle-ci afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque fonction de tâche ciblée.

* Pour exclure une valeur, cliquez deux fois sur le cercle en regard de celle-ci afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campagnes sur le réseau d’affichage/natif uniquement ; (facultatif) Sites sur le réseau d’affichage sur lequel vous ne souhaitez pas que vos publicités s’affichent. Saisissez une URL valide, telle que www.example.com. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes.

Pour plus d’informations sur la disponibilité, voir l’aide de Microsoft Advertising sur &quot;[Empêcher l’affichage des publicités sur des sites web spécifiques](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Gestion des groupes d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)

