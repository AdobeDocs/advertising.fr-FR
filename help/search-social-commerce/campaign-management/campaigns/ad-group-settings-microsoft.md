---
title: '[!DNL Microsoft Advertising] paramètres de groupe publicitaire'
description: Référencez les paramètres des groupes  [!DNL Microsoft Advertising] ’annonces.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/f-mac9RGzF4qVr7P65-9AuhWKf22tdND5XSJ1YvLWyc
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 651
ht-degree: 0%

---

# [!DNL Microsoft Advertising] paramètres de groupe publicitaire

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** nom de groupe publicitaire unique dans la campagne. La longueur maximale est de 128 caractères.

**[!UICONTROL Status]:** statut d’affichage du groupe publicitaire : *Actif* ou *En pause*. La valeur par défaut pour les nouveaux groupes publicitaires est *Actif*.

**[!UICONTROL Ad Language]:** (Campagnes de recherche) Langue cible des annonces.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Rechercher des annonces) Comment et où placer des annonces dans le groupe d’annonces :

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (valeur par défaut) : pour placer des offres pour des annonces sur le réseau de recherche.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* pour placer des offres pour des annonces sur des sites partenaires syndiqués.

* *[!UICONTROL Content network]:* Obsolète

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Obsolète

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Groupes d’annonces d’audience) Si :

* *[!UICONTROL Target and Bid]:* pour afficher les annonces uniquement aux utilisateurs et utilisatrices associés aux audiences cibles qui répondent également à d’autres cibles du groupe publicitaire.

* *[!UICONTROL Bid Only]:* pour afficher des annonces même à des personnes qui ne sont pas associées à des audiences cibles, à condition qu’elles répondent aux cibles d’autres groupes d’annonces. Vous pouvez toutefois augmenter les chances que les publicités soient présentées à des audiences spécifiques en définissant des enchères plus élevées pour ces audiences.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Pour les groupes publicitaires [!DNL Microsoft Advertising] dans le réseau d’audiences, les modificateurs d’offres pour les cibles d’emplacement ne sont pas optimisés dans les portfolios standard avec le paramètre « [!UICONTROL Auto-optimize Bid Adjustment Values] ».

**[!UICONTROL Genre]:** (groupes publicitaires dans les campagnes [!UICONTROL Audience CTV Video] ; disponibles aux États-Unis, en Californie, en Belgique, au Royaume-Uni, au Royaume-Uni, en Allemagne, en Espagne, en France, en Italie, au Royaume-Uni, en Italie, au Royaume-Uni et en Italie<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->). Les genres cibles, qui déterminent les programmes et les canaux sur lesquels vos publicités apparaissent :

* *[!UICONTROL All genres]:* (valeur par défaut) cible tous les genres.

* *[!UICONTROL Select From Below List]:* cible les genres sélectionnés. Effectuez un choix dans la liste de tous les genres disponibles.

Le placement des annonces publicitaires de la télévision connectée (CTV) dépend de la qualité de votre vidéo et du montant de votre enchère. Consultez les [exigences techniques pour les publicités CTV](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (groupes d’annonces d’audience, facultatif) Genres spécifiques à inclure ou à exclure en tant que cibles : *[!UICONTROL Male]*, *[!UICONTROL Female]* et *[!UICONTROL Unknown]*. Par défaut, tous les genres sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous avez la possibilité d&#39;augmenter ou de diminuer les enchères d&#39;un pourcentage spécifié pour chaque genre ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d’afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

**[!UICONTROL Age]:** (groupes publicitaires d’audience, facultatif) Catégories d’âge spécifiques à inclure ou à exclure en tant que cibles : *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* et *[!UICONTROL Unknown]*. Par défaut, tous les âges sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez augmenter ou diminuer les enchères d&#39;un pourcentage spécifié pour chaque âge ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d’afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

**[!UICONTROL Industry]:** (groupes d’annonces d’audience ; facultatif) Industries spécifiques à inclure ou à exclure en tant que cibles. Par défaut, tous les secteurs sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous avez la possibilité d&#39;augmenter ou de diminuer les enchères d&#39;un pourcentage spécifié pour chaque secteur ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d’afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

**[!UICONTROL Job Function Targets]:** (Audience et groupes d’annonces ; facultatif) Fonctions de tâche spécifiques à inclure ou exclure en tant que cibles. Par défaut, toutes les fonctions sont ciblées. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous avez la possibilité d&#39;augmenter ou de diminuer les offres d&#39;un pourcentage spécifié pour chaque fonction ciblée.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d’afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (facultatif) Nombre de fois où un client ou une cliente peut recevoir des annonces du groupe publicitaire. Saisissez une valeur et sélectionnez l’unité de temps (*[!UICONTROL Hour]*, *[!UICONTROL Day]* ou *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campagnes sur le réseau d’affichage/natif uniquement ; facultatif) Sites sur le réseau d’affichage sur lesquels vous ne souhaitez pas que vos annonces s’affichent. Saisissez une URL valide, telle que www.example.com. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes.

Pour plus d’informations sur la disponibilité, consultez [!DNL Microsoft Advertising]’aide de la section « [Empêcher l’affichage d’annonces sur des sites web spécifiques](https://help.ads.microsoft.com/#apex/bae/en/14061/0) ».

>[!MORELIKETHIS]
>
>* [Gérer les groupes publicitaires](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
