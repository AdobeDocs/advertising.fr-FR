---
title: '''[!DNL Microsoft® Advertising] paramètres du groupe publicitaire'
description: Référencez les paramètres pour [!DNL Microsoft® Advertising] groupes publicitaires.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 0a858fb9437439d2755f1a9679b0849c614293b7
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] paramètres du groupe publicitaire

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Nom unique du groupe d’annonces dans la campagne. La longueur maximale est de 128 caractères.

**[!UICONTROL Status]:** État d’affichage du groupe publicitaire : *Actif* ou *En pause*. La valeur par défaut pour les nouveaux groupes publicitaires est *Actif*.

**[!UICONTROL Ad Language]:** (Campagnes de recherche) Langue cible des publicités.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Rechercher des publicités) Comment et où placer des publicités dans le groupe publicitaire :

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! websites]* (valeur par défaut) : pour enchérir sur le réseau de recherche.

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! syndicated search partners]:* Pour lancer des offres publicitaires sur des sites partenaires syndiqués.

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

Pour [!DNL Microsoft® Advertising] groupes publicitaires du réseau d’audience, les modificateurs d’offre pour les cibles de localisation ne sont pas optimisés dans les portefeuilles standard avec le paramètre &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

**[!UICONTROL Genre]:** (Groupes publicitaires dans [!UICONTROL Audience CTV Video] ; disponible aux États-Unis, CA, BR, MX, UK, DE, ES, FR, IT, AU, MY et TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) Les genres cibles, qui déterminent les programmes et les canaux sur lesquels vos publicités apparaissent :

* *[!UICONTROL All genres]:* (La valeur par défaut) Cible tous les genres.

* *[!UICONTROL Select From Below List]:* Cible les genres sélectionnés. Choisissez parmi la liste de tous les genres disponibles.

Le placement de la publicité télévisée (CTV) dépend de la qualité vidéo et du montant de l’offre. Voir [exigences techniques pour les publicités CTV](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Groupes publicitaires d’audiences ; facultatif) Des sexes spécifiques à inclure ou à exclure en tant que cibles : *[!UICONTROL Male]*, *[!UICONTROL Female]*, et *[!UICONTROL Unknown]*. Par défaut, tous les sexes sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin d’obtenir une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque sexe ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Age]:** (Groupes publicitaires d’audiences ; facultatif) Catégories d’âge spécifiques à inclure ou à exclure en tant que cibles : *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*, et *[!UICONTROL Unknown]*. Par défaut, toutes les pages sont ciblées. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin d’obtenir une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque âge ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Industry]:** (Groupes d’audiences ; facultatif) industries spécifiques à inclure ou à exclure en tant que cibles. Par défaut, tous les secteurs sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin d’obtenir une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque secteur ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Job Function Targets]:** (Groupes d’audiences ; facultatif) Fonctions de tâche spécifiques à inclure ou à exclure en tant que cibles. Par défaut, toutes les fonctions de tâche sont ciblées. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin d’obtenir une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque fonction de tâche ciblée.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d’obtenir une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Facultatif) Le nombre de fois où des publicités peuvent être diffusées à un client à partir du groupe publicitaire. Saisissez une valeur et sélectionnez l’unité de temps (*[!UICONTROL Hour]*, *[!UICONTROL Day]*, ou *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campagnes sur le réseau d’affichage/natif uniquement ; facultatif) Sites sur le réseau d’affichage sur lequel vous ne souhaitez pas que vos publicités s’affichent. Saisissez une URL valide, telle que www.example.com. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes.

Pour plus d’informations sur la disponibilité, voir [!DNL Microsoft® Advertising] help to &quot;[Empêcher l’affichage des publicités sur des sites web spécifiques](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Gestion des groupes d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
