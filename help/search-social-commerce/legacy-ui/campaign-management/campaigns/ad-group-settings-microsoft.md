---
title: '[!DNL Microsoft Advertising] paramètres du groupe publicitaire'
description: Référencez les paramètres pour [!DNL Microsoft Advertising] groupes publicitaires.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/f-mac9RGzF4qVr7P65-9AuhWKf22tdND5XSJ1YvLWyc'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%
---
# [!DNL Microsoft Advertising] paramètres du groupe publicitaire

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Nom de groupe publicitaire unique dans la campagne. La longueur maximale est de 128 caractères.

**[!UICONTROL Status]:** statut d’affichage du groupe publicitaire : *Actif* ou *En pause*. La valeur par défaut pour les nouveaux groupes publicitaires est *Actif*.

**[!UICONTROL Ad Language]:** (Campagnes de recherche) Langue cible des publicités.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Rechercher des annonces) Comment et où placer des annonces dans le groupe d’annonces :

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (valeur par défaut) : pour placer des enchères pour des annonces sur le réseau de recherche.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* Pour enchérir sur des sites partenaires syndiqués.

* *[!UICONTROL Content network]:* Obsolète

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Obsolète

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (groupes publicitaires d’audience) Si :

* *[!UICONTROL Target and Bid]:* Pour afficher les publicités uniquement aux utilisateurs associés aux audiences cibles qui répondent également à d’autres cibles pour le groupe publicitaire.

* *[!UICONTROL Bid Only]:* Pour afficher des annonces même à des personnes qui ne sont pas associées à des audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire. Vous pouvez toutefois augmenter les chances que les publicités soient présentées à des audiences spécifiques en définissant des enchères plus élevées pour ces audiences.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Pour les groupes publicitaires [!DNL Microsoft Advertising] du réseau d’audiences, les modificateurs d’offres pour les cibles d’emplacement ne sont pas optimisés dans les portfolios standard avec le paramètre « [!UICONTROL Auto-optimize Bid Adjustment Values] ».

**[!UICONTROL Genre]:** (groupes publicitaires dans les campagnes [!UICONTROL Audience CTV Video] ; disponibles aux États-Unis, en Californie, en BR, au MX, au Royaume-Uni, en Allemagne, en Allemagne, en Espagne, en France, en Italie, au Royaume-Uni, en Hongrie et en Thaïlande<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->). Les genres cibles, qui déterminent les programmes et les canaux sur lesquels vos publicités apparaissent :

* *[!UICONTROL All genres]:* (valeur par défaut) cible tous les genres.

* *[!UICONTROL Select From Below List]:* cible les genres sélectionnés. Effectuez un choix dans la liste de tous les genres disponibles.

Le placement des annonces publicitaires de la télévision connectée (CTV) dépend de la qualité de votre vidéo et du montant de votre enchère. Consultez les [exigences techniques pour les annonces CTV](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (groupes publicitaires d’audience ; facultatif) genres spécifiques à inclure ou exclure en tant que cibles : *[!UICONTROL Male]*, *[!UICONTROL Female]* et *[!UICONTROL Unknown]*. Par défaut, tous les genres sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous avez la possibilité d&#39;augmenter ou de diminuer les enchères d&#39;un pourcentage spécifié pour chaque genre ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d&#39;afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

**[!UICONTROL Age]:** (groupes publicitaires d’audience ; facultatif) catégories d’âge spécifiques à inclure ou exclure en tant que cibles : *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* et *[!UICONTROL Unknown]*. Par défaut, tous les âges sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous pouvez augmenter ou diminuer les enchères d&#39;un pourcentage spécifié pour chaque âge ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d&#39;afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

**[!UICONTROL Industry]:** (groupes d’annonces d’audience ; facultatif) secteurs d’activité spécifiques à inclure ou à exclure en tant que cibles. Par défaut, tous les secteurs sont ciblés. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous avez la possibilité d&#39;augmenter ou de diminuer les enchères d&#39;un pourcentage spécifié pour chaque secteur ciblé.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d&#39;afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

**[!UICONTROL Job Function Targets]:** (groupes d’annonces d’audience ; facultatif) Fonctions de tâche spécifiques à inclure ou exclure en tant que cibles. Par défaut, toutes les fonctions sont ciblées. Les exclusions remplacent toujours les inclusions.

* Pour cibler toutes les valeurs, ne sélectionnez aucune valeur.

* Pour inclure une valeur, cliquez une fois sur le cercle adjacent afin qu’une coche bleue (![Inclure](/help/search-social-commerce/assets/include.png "Inclure")) s’affiche. Vous avez la possibilité d&#39;augmenter ou de diminuer les offres d&#39;un pourcentage spécifié pour chaque fonction ciblée.

* Pour exclure une valeur, cliquez deux fois sur le cercle adjacent afin d&#39;afficher une coche rouge (![Exclure](/help/search-social-commerce/assets/exclude.png "Exclure")).

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (facultatif) nombre de fois où des publicités du groupe publicitaire peuvent être diffusées à un client. Saisissez une valeur et sélectionnez l&#39;unité de temps (*[!UICONTROL Hour]*, *[!UICONTROL Day]* ou *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campagnes sur le réseau d’affichage/natif uniquement ; facultatif) Sites sur le réseau d’affichage sur lesquels vous ne souhaitez pas que vos annonces s’affichent. Saisissez une URL valide, telle que www.example.com. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes.

Pour plus d&#39;informations sur la disponibilité, consultez l&#39;aide de [!DNL Microsoft Advertising] pour « [Empêcher l&#39;affichage d&#39;annonces sur des sites Web spécifiques](https://help.ads.microsoft.com/#apex/bae/en/14061/0) ».

>[!MORELIKETHIS]
>
>* [Gérer les groupes publicitaires](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/ad-group-manage.md)
