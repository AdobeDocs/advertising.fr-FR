---
title: '[!DNL Microsoft Advertising] paramètres du groupe publicitaire'
description: Référencez les paramètres pour les groupes publicitaires  [!DNL Microsoft Advertising] .
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] paramètres du groupe publicitaire

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** nom d’un groupe publicitaire unique dans la campagne. La longueur maximale est de 128 caractères.

**[!UICONTROL Status]:** État d’affichage du groupe publicitaire : *Actif* ou *En pause*. La valeur par défaut des nouveaux groupes publicitaires est *Active*.

**[!UICONTROL Ad Language]:** (Campagnes de recherche) Langue cible des publicités.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Rechercher des publicités) Comment et où placer des publicités dans le groupe publicitaire :

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (valeur par défaut) : pour placer des offres pour les publicités sur le réseau de recherche.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* pour placer des offres sur des sites de partenaires syndiqués.

* *[!UICONTROL Content network]:* obsolète

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** obsolète

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (groupes d’audiences) Indique si :

* *[!UICONTROL Target and Bid]:* pour afficher uniquement les publicités aux utilisateurs associés aux audiences cibles qui répondent également à d’autres cibles pour le groupe publicitaire.

* *[!UICONTROL Bid Only]:* pour afficher les publicités même aux personnes qui ne sont pas associées aux audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire. Vous pouvez toutefois augmenter les chances d&#39;affichage des publicités à des audiences spécifiques en définissant des offres plus élevées pour ces audiences.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Pour [!DNL Microsoft Advertising] groupes publicitaires dans le réseau d’audience, les modificateurs d’offre pour les cibles d’emplacement ne sont pas optimisés dans les portefeuilles standard avec le paramètre &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

**[!UICONTROL Genre]:** (Groupes publicitaires dans [!UICONTROL Audience CTV Video] campagnes ; disponibles aux États-Unis, en CA, BR, MX, UK, DE, ES, FR, IT, AU, MY et TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) Les genres cibles, qui déterminent les programmes et les canaux sur lesquels vos publicités apparaissent :

* *[!UICONTROL All genres]:* (valeur par défaut) Cible tous les genres.

* *[!UICONTROL Select From Below List]:* Cible les genres sélectionnés. Choisissez parmi la liste de tous les genres disponibles.

Le placement de la publicité télévisée (CTV) dépend de la qualité vidéo et du montant de l’offre. Voir les [exigences techniques pour les publicités CTV](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (groupes d’audiences ; facultatif) genres spécifiques à inclure ou à exclure en tant que cibles : *[!UICONTROL Male]*, *[!UICONTROL Female]* et *[!UICONTROL Unknown]*. Par défaut, tous les sexes sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Include](/help/search-social-commerce/assets/include.png "Include")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque sexe ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin qu’une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Age]:** (groupes d’audiences ; facultatif) catégories d’âge spécifiques à inclure ou à exclure comme cibles : *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* et *[!UICONTROL Unknown]*. Par défaut, toutes les pages sont ciblées. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Include](/help/search-social-commerce/assets/include.png "Include")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque âge ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin qu’une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Industry]:** (groupes d’audiences ; facultatif) secteurs spécifiques à inclure ou exclure en tant que cibles. Par défaut, tous les secteurs sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Include](/help/search-social-commerce/assets/include.png "Include")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque secteur ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin qu’une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

**[!UICONTROL Job Function Targets]:** (groupes d’annonces d’audience ; facultatif) fonctions de tâche spécifiques à inclure ou exclure en tant que cibles. Par défaut, toutes les fonctions de tâche sont ciblées. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Include](/help/search-social-commerce/assets/include.png "Include")) s’affiche. Vous pouvez éventuellement augmenter ou diminuer les offres d’un pourcentage spécifique pour chaque fonction de tâche ciblée.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin qu’une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")) s’affiche.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Facultatif) Le nombre de fois qu’un client peut recevoir des publicités du groupe publicitaire. Saisissez une valeur et sélectionnez l’unité de temps (*[!UICONTROL Hour]*, *[!UICONTROL Day]* ou *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campagnes sur le réseau d’affichage/natif uniquement ; facultatif) Sites sur le réseau d’affichage sur lequel vous ne souhaitez pas que vos publicités s’affichent. Saisissez une URL valide, telle que www.example.com. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes.

Pour plus d&#39;informations sur la disponibilité, voir l&#39;[!DNL Microsoft Advertising] aide &quot;[Empêcher l&#39;affichage d&#39;annonces sur des sites web spécifiques](https://help.ads.microsoft.com/#apex/bae/en/14061/0)&quot;.

>[!MORELIKETHIS]
>
>* [Gérer les groupes d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
