---
title: Colonnes de rapport disponibles
description: Voir les descriptions des colonnes disponibles dans les rapports personnalisés.
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: bd85b4451624e14c95157c84537fdfb53662773f
workflow-type: tm+mt
source-wordcount: '2724'
ht-degree: 0%

---

# Colonnes de rapport disponibles

<!-- Add when added:

|[!UICONTROL Dimension]|[!UICONTROL Feed]|[!UICONTROL Deal List]|The name of a user-created deal list for which an ad was shown.|

-->

| Type de mesure | Sous-type | Nom de la colonne | Description |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | ID de publicité attribué par le serveur de publicités externe. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | Identifiant unique de l’annonce publicitaire dans DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | Nom de l’annonce publicitaire attribué par l’utilisateur. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | Format de la publicité. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | Classification de l’annonce publicitaire telle que modifiée par l’utilisateur ou indiquée par les entrées de date : *[!UICONTROL live]*, *[!UICONTROL scheduled]*, *[!UICONTROL completed]* ou *[!UICONTROL archived]*. |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | Nom de l’annonceur. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | Budget total affecté par l&#39;utilisateur à la campagne. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | Date de fin de la campagne. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | Identifiant unique de la campagne dans DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | Nom de la campagne attribué par l’utilisateur. |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | Première date pour la campagne. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Title] | Contenu/titre du film. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Series] | La série de contenu. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Genre] | Le genre du contenu. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL ProdQ] | La qualité de la production, telle que définie par le laboratoire [IAB Technology Laboratory](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md). Les valeurs peuvent `Unknown`, `Professionally Produced`, `Prosumer` ou `User Generated`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Context] | Type de contenu, tel que défini par le [Laboratoire de technologie de l’IAB](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md). Les valeurs peuvent inclure `Video,` `Game`, `Music`, `Application`, `Text`, `Other` ou `Unknown`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Rating] | Évaluation du contenu, tel que PG ou R. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Livestream] | Indique si l’annonce a été diffusée en direct : `Not Live` ou `Live`. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Length (in seconds)] | Longueur du contenu en secondes. Généralement utilisé pour la vidéo ou l’audio. |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Language (as per ISO 639)] | Langue du contenu à l’aide de la norme ISO-639-1-alpha-2. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | L’année, le mois et le jour. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | Jour [!UICONTROL of Week] | Jour spécifique, tel que [!UICONTROL Monday] ou [!UICONTROL Tuesday]. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | Année, mois, jour et heure. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | Mois et année. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | L’heure à l’heure, de 0 à 23. |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | Période de la semaine concernée, du dimanche au samedi. Exemple : 2021-02-18 à 2021-03-07. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | Fournisseur du navigateur dans lequel l’annonce publicitaire a été affichée (Google ou Mozilla, par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | Version du navigateur dans lequel la publicité a été affichée ([!UICONTROL Safari 4.3] ou [!UICONTROL Chrome 7.0], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | Navigateur dans lequel la publicité a été affichée ([!UICONTROL Chrome] ou [!UICONTROL Firefox], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Environment] | Environnements d’appareil ciblés par l’emplacement : (*[!UICONTROL Desktop]*, *[!UICONTROL Mobile]* et/ou *[!UICONTROL Connected TV])*. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | Type d’appareil sur lequel la publicité a été affichée ([!UICONTROL Set Top Box] ou [!UICONTROL Mobile Phone], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | Fabricant de l’appareil sur lequel la publicité a été affichée (par exemple, [!UICONTROL Samsung], [!UICONTROL Lenovo] ou [!UICONTROL Apple]). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | Modèle de l’appareil sur lequel la publicité a été affichée ([!UICONTROL iPhone XS] ou [!UICONTROL Galaxy Note 7], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | Fournisseur du système d’exploitation sur lequel la publicité a été affichée ([!UICONTROL Microsoft] ou [!UICONTROL Apple], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | Version du système d’exploitation sur lequel la publicité a été affichée ([!UICONTROL Windows 10] ou [!UICONTROL iOS Mojave], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | Système d’exploitation sur lequel la publicité a été affichée ([!UICONTROL Apple iOS] ou [!UICONTROL Android], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Name] | Nom attribué par l’utilisateur à l’opération, tel qu’il a été saisi dans DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Type] | Indique si le contrat est *[!UICONTROL Guaranteed]* ou *[!UICONTROL Non-Guaranteed]*. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | Classification de l’inventaire : *[!UICONTROL Private],* *[!UICONTROL On Demand],* ou *[!UICONTROL Public]*. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Private Deal ID] | Identifiant unique attribué à une transaction privée par l’intermédiaire du partenaire d’approvisionnement externe. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Publisher] | Partenaire côté offre qui fournit l&#39;inventaire. Il s’agit généralement d’un éditeur, mais il peut également s’agir d’un fournisseur de services partagés. |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | Partenaire côté offre (SSP) auquel le média est attribué. |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | Nombre de fois qu’un appareil a reçu une publicité, en fonction du cookie ou de l’ID d’appareil unique. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | Ville à laquelle les données déclarées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | Pays auquel les données déclarées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | Zone de marché désignée (DMA) à laquelle les données déclarées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Pin Code] | Code PIN (Postal Index Number) auquel sont attribuées les données signalées. |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | État auquel les données rapportées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | L’audience. Le rapport prend en charge jusqu’à 10 audiences uniques. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | La campagne. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | La durée de la création. Le rapport prend en charge jusqu’à 10 longueurs de création uniques. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | L’appareil. Le rapport prend en charge jusqu’à 10 appareils uniques. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | Type de flux. Le rapport prend en charge jusqu’à 10 types de flux uniques. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | Type de média. Le rapport prend en charge jusqu’à 10 types de médias uniques. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | L’éditeur. Le rapport prend en charge jusqu’à 10 éditeurs uniques. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | Le package. <!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | L’emplacement.<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | Site ou application sur lequel l’impression publicitaire a été diffusée. Le rapport prend en charge jusqu’à 10 sites ou applications uniques. |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | Balise d’emplacement utilisée comme identifiant personnalisé pour l’emplacement. Le rapport prend en charge jusqu’à 10 balises d’emplacement uniques. <!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Audience] | L’audience. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Campaign] | La campagne. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Creative Length] | La durée de la création. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Device] | L’appareil. (comme CTV, Desktop, etc.) |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Media Type] | Type de média. (Affichage, Audio, etc.) |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Publisher] | L’éditeur. |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Placement] | L’emplacement. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Budget] | Budget du vol à forfait. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight End Date] | Date de fin du vol du package. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Rollover] | Tout budget de reconduction pour le vol de package. |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Start Date] | Date de début du vol du package. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | Date de fin du package. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | Montant de l’objectif de fréquence pour le package. Ce montant est exprimé en dépenses ou en impressions. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | Identifiant unique du package dans DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | Nom du package |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | Date de début du package. |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | Date de fin de l’emplacement. |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | (Obsolète) ID de conversion attribué par DSP aux événements de conversion [!DNL TubeMogul] hérités. |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | (Obsolète) Nom de conversion attribué aux événements de conversion [!DNL TubeMogul] hérités. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | Identifiant unique de l’emplacement dans DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | Nom de l&#39;emplacement tel qu&#39;il est attribué par l&#39;utilisateur. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | Budget d’emplacement. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | Enchère maximale pour l’emplacement. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | Date de fin de l’emplacement. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | Date de début de l’emplacement. |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | Balise d’emplacement utilisée comme identifiant personnalisé pour l’emplacement. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | Description associée à un segment facturable. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | Clé unique associée à un segment facturable. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | Nom d’un segment facturable. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | Description associée à un segment, fournie par le fournisseur de données. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | Clé unique associée à un segment. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | Nom d’un segment. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | Nom du fournisseur de données associé à un segment. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | Identifiant unique du site ou de l’application dans DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | Nom du site. |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Traffic Type] | Indique si la publicité a été affichée sur *[!UICONTROL sites]* ou *[!UICONTROL Apps]*. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | Durée de la vidéo, qui est traitée après le chargement. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | Identifiant unique du contenu vidéo créatif dans DSP. |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | Nom du contenu créatif affecté par l’utilisateur. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | La [!UICONTROL App/Site Distinct Uniques] divisée par [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | Nombre total d’appareils qui ont été atteints sur cette application uniquement. Une visionneuse exposée à une publicité sur plusieurs éditeurs n’est pas incluse dans cette valeur. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | La [!UICONTROL Total Spend] divisée par [!UICONTROL App/Site Distinct Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | La [!UICONTROL Total Spend] divisée par [!UICONTROL App/Site Uniques]. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | Pourcentage estimé de l’univers domestique ciblé ayant reçu une exposition. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | Nombre moyen d’impressions affichées pour des fichiers uniques. Pour certains stocks, les éditeurs ne transmettent pas d’identifiant d’appareil, et ces impressions ne sont pas incluses dans cette valeur. Il existe une mesure similaire dans le rapport [!UICONTROL Frequency (by App/Site)], mais elle n’est pas estimée. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | (Incluse dans le rapport [!UICONTROL Frequency (by Impression)]) Estimation des impressions pour une répartition de fréquence donnée. Les estimations de DSP sont basées sur un échantillon d’impressions. Pour certains stocks, les éditeurs ne transmettent pas d’identifiant d’appareil, et ces impressions ne sont pas incluses dans cette valeur. Il existe une mesure similaire dans le rapport [!UICONTROL Frequency (by App/Site)], mais elle n’est pas estimée. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | (Inclus dans le rapport [!UICONTROL Frequency (by Impression)]) Nombre de navigateurs ou d’appareils uniques enregistrés pour une fréquence donnée. Les estimations de DSP sont basées sur un échantillon d’impressions. Pour certains stocks, ne transmettez pas d’identifiant d’appareil, et ces impressions ne sont pas incluses dans cette valeur. Il existe une mesure similaire dans le rapport [!UICONTROL Frequency (by App/Site)], mais elle n’est pas estimée. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | Somme des ménages uniques que DSP (enchères) a vus au cours de la période. |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | Nombre total d’impressions générées suite à l’utilisation d’un graphique d’appareil pour le ciblage interpériphérique basé sur les personnes. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency] | Fréquence des impressions par foyer. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | Fréquence à laquelle les ménages sont rejoints uniquement par la dimension déclarée, y compris les intersections de trois valeurs maximum pour la dimension. Par exemple, si vous utilisez la dimension [!UICONTROL Placement], vous pouvez voir la fréquence atteinte par des emplacements individuels, les fréquences atteintes par une combinaison de deux emplacements et les fréquences atteintes par des combinaisons de trois emplacements. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | Le nombre de foyers qui ont été atteints uniquement par la dimension signalée, calculé comme <code>[adresses IP qui ont été atteintes uniquement par la dimension signalée] - [adresses IP qui ont été atteintes par toute autre dimension]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | Le pourcentage de foyers qui ont été atteints uniquement par la dimension signalée, calculé comme <code>[le pourcentage d’adresses IP qui ont été atteintes par la dimension] - [le pourcentage d’adresses IP qui ont été atteintes par toute autre dimension]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Impressions] | Nombre total d’impressions de publicité diffusées. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | Nombre total d’impressions diffusées qui ont pu être mesurées en termes de visibilité. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | Nombre total d’impressions mesurables générées uniquement par la dimension générée, y compris les intersections de trois valeurs maximum pour la dimension. Par exemple, si vous utilisez la dimension [!UICONTROL Placement], vous pouvez voir les impressions mesurables obtenues par des emplacements individuels, les impressions mesurables obtenues par une combinaison de deux emplacements et les impressions mesurables obtenues par des combinaisons de trois emplacements. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | Dépenses totales. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | Le nombre total de ménages uniques (adresses IP distinctes) atteint. |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | Nombre total de ménages uniques (adresses IP distinctes) atteints uniquement par la dimension signalée, y compris les intersections de trois valeurs maximum pour la dimension. Par exemple, si vous utilisez la dimension [!UICONTROL Placement], vous pouvez voir les ménages uniques atteints par des emplacements individuels, les ménages communs atteints par une combinaison de deux emplacements, et les ménages communs atteints par des combinaisons de trois emplacements. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Incremental HH] | Dépenses totales divisées par le ménage supplémentaire atteint. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Unique HH] | Dépenses totales divisées par le ménage unique atteint. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Frequency] | Fréquence des impressions par foyer. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Incremental Household Reached] | Le nombre de foyers qui ont été atteints uniquement par la dimension signalée, calculé comme [adresses IP qui ont été atteintes uniquement par la dimension signalée] - [adresses IP qui ont été atteintes par toute autre dimension]. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL % Incremental Household Reached] | Le pourcentage de foyers qui ont été atteints uniquement par la dimension signalée, calculé comme [le pourcentage d’adresses IP atteintes par la dimension] - [le pourcentage d’adresses IP atteintes par toute autre dimension]. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Impressions] | Nombre total d’impressions de publicité diffusées. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Measurable Impressions] | Nombre total d’impressions diffusées qui ont pu être mesurées en termes de visibilité. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Total Media Spend] | Dépenses totales. |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Unique Household Reached] | Le nombre total de ménages uniques (adresses IP distinctes) atteint. |
| [!UICONTROL Metrics] | [!UICONTROL Identifier] | [!UICONTROL Identifier Type] | Type d’identifiant ciblé. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | Pourcentage du nombre total d&#39;enchères ayant été enchéries au CPM Max. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | Coût brut moyen par acquisition, calculé par <code>[!UICONTROL Gross Spend] / [!UICONTROL conversion metric]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | Coût brut moyen par clic publicitaire, calculé par <code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | Coût moyen par vue vidéo terminée, calculé par <code>[!UICONTROL Gross Spend]/[!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPE] | Coût brut moyen par engagement publicitaire, calculé par <code>[!UICONTROL Gross Spend]/[!UICONTROL Total Ad Engagements]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPI] | Coût brut moyen par impression publicitaire, calculé par <code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | Coût moyen par 1 000 impressions, calculé par <code>[!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | Coût moyen par vue vidéo, calculé par <code>[!UICONTROL Gross Spend]/[!UICONTROL Views]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross Custom Goal CPA] | Le <code>[!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>, où [!UICONTROL Custom Goal] correspond au poids de l’objectif pour toutes les conversions associées à l’objectif personnalisé. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | Coût moyen par 1 000 impressions visibles, calculé par <code>[!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | Coût net moyen par clic publicitaire, calculé par <code>[!UICONTROL Net Spend]/[!UICONTROL Total Ad Clicks]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | Coût net moyen par vue vidéo terminée, calculé par <code>[!UICONTROL Net Spend]/[!UICONTROL 100% Completions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPI] | Coût net moyen par impression publicitaire, calculé par <code>[!UICONTROL Net Spend]/[!UICONTROL Total Ad Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | Coût net moyen par 1 000 impressions, calculé par <code>[!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | Coût net moyen par vue vidéo, calculé par <code>[!UICONTROL Net Spend]/[!UICONTROL Views]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net vCPM] | Coût net moyen par 1 000 impressions visibles, calculé par <code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | Nombre d’utilisateurs distincts pour lesquels DSP enchérit pour l’emplacement. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Agency Fee] | Les frais de l&#39;agence. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Creative Spend] | Dépenses totales pour les publicités diffusées à partir d’Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Data Spend] | Coût net total des frais de données de segment d’audience facturés via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Media Spend] | Coût net total des médias facturables, y compris les frais techniques, facturés via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Other Spend] | Coût total des autres frais de service (partenaires de vérification tiers, diffusion de publicités, etc.) facturés via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Creative] | Taxe estimée sur les publicités diffusées à partir d’Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | Taxe estimée sur les segments d’audience et les services de données tiers. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | Taxe estimative sur les médias incluant la taxe appliquée aux services de refacturation des coûts des médias et de frais techniques à DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | Taxe estimée sur les autres frais de service (y compris les partenaires de vérification tiers, le ciblage de rubrique, etc.) facturés via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Gross Spend] | Les dépenses brutes. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Margin %] | (Lorsque la gestion des marges est activée) Le pourcentage de marge, qui est calculé par <code>([!UICONTROL Gross Spend] - [!UICONTROL Net Spend]) / [!UICONTROL Gross Spend]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | La somme des coûts des médias non facturables et facturables sans frais techniques. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | Coût net moyen par 1 000 impressions visibles, calculé par <code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non Billable Creative Spend] | Total des dépenses pour les publicités non facturées via Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Spend] | Coût net total des frais de données de segment d’audience non facturés via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Spend] | Coût net total des médias non facturables, y compris les frais techniques, non facturés via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | Coût total des autres frais de service (partenaires de vérification tiers, diffusion de publicités, etc.) non facturés via DSP. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Billable Spend] | La somme de [!UICONTROL Billable Spend (Media)], [!UICONTROL Billable Spend (Data)] et [!UICONTROL Billable Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative CPM] | Coût moyen net des médias pour 1 000 impressions pour les publicités diffusées à partir d’Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative Spend] | Total des dépenses facturables et non facturables pour les publicités diffusées à partir d’Adobe Creative. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data eCPM] | Coût net moyen des données par 1 000 impressions, calculé par <code>[!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data Spend] | Coût net total des frais de données de segment d’audience. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media CPM] | Coût moyen net du média par 1 000 impressions, calculé par <code>[!UICONTROL Net Spend (Media)] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media Spend] | Coût net total des médias, y compris les frais techniques. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | La somme de [!UICONTROL Net Spend (Media)], [!UICONTROL Net Spend (Data)] et [!UICONTROL Net Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | La somme de [!UICONTROL Non-billable Spend (Media)], [!UICONTROL Non-billable Spend (Data)] et [!UICONTROL Non-billable Spend (Other)]. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other eCPM] | Coût net moyen par 1 000 impressions pour les autres frais, calculé par <code>[!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1 000</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other Spend] | Coût net total des autres frais de service (partenaires de vérification tiers, services publicitaires, etc.). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | Pourcentage de vues ayant visionné l’annonce publicitaire dans son intégralité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | Nombre de vues ayant visionné l’annonce publicitaire dans son intégralité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | Pourcentage d’impressions visibles qui ont visionné l’intégralité de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | Pourcentage de vues ayant regardé au moins un quartile de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | Nombre de vues ayant visionné au moins un quartile de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | Pourcentage de vues ayant regardé au moins deux quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | Nombre de vues ayant visionné au moins deux quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | Pourcentage d’impressions visibles ayant visionné au moins deux quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | Pourcentage de vues ayant regardé au moins trois quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | Nombre de vues ayant visionné au moins trois quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | Pourcentage moyen auquel une publicité a été visionnée jusqu’à la fin, en tenant compte de toutes les vues. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | Nombre de clics sur la superposition et les bannières d’annonces. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | Pourcentage de clics divisé par les impressions de publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | Pourcentage de clics divisé par les vues vidéo. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | Nombre de clics sur les bannières associées. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | Pourcentage de clics divisé par les impressions de bannières associées. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | Nombre d’impressions de bannières associées. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | Type de connexion Internet utilisé pour afficher la publicité (Wifi ou 4g LTE, par exemple). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | Nombre d’interactions sur une publicité diffusée. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | Nombre total d’impressions de publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | Pourcentage d’impressions diffusées qui ont donné lieu à des vues vidéo. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | Durée moyenne d’une vue vidéo, mesurée en secondes. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | Somme de tous les clics sur une annonce publicitaire. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | Nombre total de minutes pendant lesquelles une publicité vidéo a été visionnée. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | Nombre total de vues de publicités vidéo. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 100% Completion Rate] | (Rapport Creative personnalisé) Pourcentage de vues ayant visionné l’intégralité de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 100% Completions] | (Rapport Creative personnalisé) Nombre de vues ayant visionné l’intégralité de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 25% Completion Rate] | (Rapport Creative personnalisé) Pourcentage de vues ayant visionné au moins un quartile de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 25% Completions] | (Rapport Creative personnalisé) Nombre de vues ayant visionné au moins un quartile de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 50% Completion Rate] | (Rapport Creative personnalisé) Pourcentage de vues ayant visionné au moins deux quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 50% Completions] | (Rapport Creative personnalisé) Nombre de vues ayant visionné au moins deux quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 75% Completion Rate] | (Rapport Creative personnalisé) Pourcentage de vues ayant visionné au moins trois quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 75% Completions] | (Rapport Creative personnalisé) Nombre de vues ayant visionné au moins trois quartiles de la publicité. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Avg Percent Viewed] | (Rapport Creative personnalisé) Pourcentage moyen par rapport auquel une annonce a été visionnée jusqu’à la fin, en tenant compte de toutes les vues. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Play Rate] | (Rapport Creative personnalisé) Pourcentage d’impressions diffusées qui ont donné lieu à des vues vidéo. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Playtime per View] | (Rapport Creative personnalisé) Durée moyenne d’une vue vidéo, mesurée en secondes. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Mute] | (Rapport Creative personnalisé) Nombre total de fois où la vidéo a été désactivée. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Pause] | (Rapport Creative personnalisé) Nombre total de fois où la vidéo a été mise en pause. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Resume] | (Rapport Creative personnalisé) Nombre total de fois où la vidéo a été reprise après avoir été suspendue. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Rewind] | (Rapport Creative personnalisé) Nombre total de fois où la vidéo a été rembobinée. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Start] | (Rapport Creative personnalisé) Nombre total de fois où la vidéo a été démarrée. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Unmute] | (Rapport Creative personnalisé) Nombre total d’affichages de la vidéo. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Viewed Minutes] | (Rapport Creative personnalisé) Nombre total de minutes pendant lesquelles une publicité vidéo a été visionnée. |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Views] | (Rapport Creative personnalisé) Nombre total de vues de publicités vidéo. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | Largeur et hauteur moyennes du lecteur. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | Nombre total d’impressions diffusées qui ont pu être mesurées en termes de visibilité. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | Pourcentage d’impressions diffusées qui ont pu être mesurées en termes de visibilité, calculées sous la forme <code>[!UICONTROL Measurable Impressions] x 1 000 / [!UICONTROL Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | Pourcentage d’impressions non mesurables pour la visibilité en raison d’iFrames incompatibles. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | Nombre d’impressions non mesurables pour la visibilité en raison d’un suivi de visibilité non pris en charge sur l’unité publicitaire. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | Pourcentage d’impressions non mesurables pour la visibilité due à d’autres raisons. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | Nombre d’impressions d’annonce publicitaire non mesurables pour la visibilité. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | Pourcentage d’impressions d’annonce publicitaire non mesurables pour la visibilité. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | Pourcentage d’impressions non mesurables pour la visibilité en raison d’un suivi de visibilité non pris en charge sur cette unité publicitaire. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | Pourcentage d’impressions visibles sur toutes les impressions mesurables, calculé comme <code>[!UICONTROL Viewable Impressions]/[!UICONTROL Measurable Impressions]</code>. |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | Nombre d’impressions d’annonce publicitaire considérées comme visibles. |
| [!UICONTROL Conversion Metrics] | [Regroupé par annonceur dans les paramètres du rapport] | [ Conversion spécifique à l’annonceur ] | Total d’une mesure de conversion spécifique à l’annonceur ou d’un événement Adobe Analytics spécifié. |
| [!UICONTROL Custom Goals] | [Regroupé par annonceur dans les paramètres du rapport] | [Objectif personnalisé spécifique à l’annonceur] | Somme pondérée de toutes les conversions incluses dans l’[objectif personnalisé](/help/dsp/optimization/custom-goal.md) spécifié. |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [À propos des rapports personnalisés](/help/dsp/reports/report-about.md)
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Dupliquer un rapport personnalisé](/help/dsp/reports/report-copy.md)
>* [Modifier un rapport personnalisé](/help/dsp/reports/report-edit.md)
>* [Paramètres de rapport personnalisés](/help/dsp/reports/report-settings.md)
