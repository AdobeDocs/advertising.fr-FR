---
title: "[!UICONTROL Channel Assist Report]"
description: En savoir plus sur les [!UICONTROL Channel Assist Report].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Le [!UICONTROL Channel Assist Report]

*Annonceurs avec suivi des clics Search, Social et Commerce et suivi des conversions à partir d’Adobe Advertising, Adobe Analytics (avec un [!DNL Analytics] intégration) ou fournie dans les flux à l’aide d’un jeton (`ef_id`) uniquement*

Le [!UICONTROL Channel Assist Report] indiquer comment différents canaux marketing (recherche ou réseaux sociaux à partir de Search, Social et Commerce ; ou display ou video de Advertising DSP) ont contribué au processus de conversion. Le rapport indique comment chaque modèle de types d’événement qui a entraîné une ou plusieurs conversions a contribué à vos conversions globales. Vous pouvez, par exemple, voir le nombre de conversions survenues lorsque les utilisateurs ont vu une impression d’annonce publicitaire, cliqué sur une publicité de recherche, puis passé une commande ; ou vous pouvez voir le nombre de conversions survenues après l’interaction des utilisateurs avec plus de 10 publicités. Les types d’événement incluent les clics de recherche, les impressions et les clics d’affichage, les impressions et les clics vidéo, ainsi que d’autres impressions et autres clics. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

Les résultats du rapport incluent des données agrégées pour chaque modèle de types d’événement dans le chemin de conversion (jusqu’aux N premiers types d’événement) qui s’est produit dans le rapport de l’annonceur. [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). Si, par exemple, vous sélectionnez une taille de chemin de cinq (5), le rapport comprend des chemins de conversion qui incluent jusqu’à cinq événements au plus tôt, avec une ligne pour chaque modèle de types d’événement suivi (par exemple &quot;clic de recherche&quot;, puis &quot;impression d’affichage&quot;). Chaque ligne présente un modèle d’événements, y compris le premier événement du chemin et le dernier événement ayant généré des conversions (même si le dernier événement se trouve en dehors de la taille de chemin spécifiée). Par défaut, les lignes sont dans l’ordre croissant en fonction du nombre d’événements dans le chemin.

Vous pouvez éventuellement inclure des données de conversion agrégées pour chaque ligne. Lorsque vous incluez des colonnes de conversions/recettes dans le rapport, chaque type de conversion est représenté en quatre colonnes, ce qui indique a) le nombre total de conversions, b) le pourcentage de vos conversions globales qui ont été attribuées à ce modèle d’événement, c) la latence moyenne de la journée entre le premier événement et une conversion, et d) la latence moyenne en jours entre le dernier événement et une conversion. Lorsque le chemin de conversion inclut plus d’événements que la taille de chemin spécifiée, le rapport inclut des lignes supplémentaires agrègant les données pour les conversions résultant du nombre plus élevé d’événements (comme tous les modèles qui incluaient six types d’événements).

Vous pouvez afficher les données des 18 mois précédents.

## Colonnes disponibles

Vous trouverez ci-dessous les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section Colonnes des paramètres du rapport.

| Colonne | Par défaut ? | Description |
|----|----|
| [!UICONTROL 1st Event] to [!UICONTROL 5th Event] | Par défaut | Les cinq premiers types d’événement dans le chemin de conversion qui se sont produits dans le [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Par défaut | Nombre de types d’événements dans le chemin de conversion qui se sont produits dans le rapport [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | Par défaut | Type d’événement du premier événement (le plus ancien) dans le chemin de conversion. |
| [!UICONTROL Last Event Type] | Par défaut | Type d’événement du dernier événement qui a généré des conversions (même si le dernier événement se trouve en dehors de la taille de chemin spécifiée). |
| \[Mesures personnalisées (dérivées) spécifiques aux annonceurs\] | Personnalisé | La valeur d’une mesure personnalisée que vous avez créée et calculée à partir de mesures existantes. |
| \[Propriétés de transaction spécifiques aux annonceurs\] | Personnalisé | Nombre de conversions pour une propriété de transaction ou une mesure d’engagement du site spécifiée. |
| [!UICONTROL % of Total] \[propriété de transaction\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport pour chaque propriété de transaction incluse) Le pourcentage de vos conversions globales entre les portefeuilles qui ont été attribués au modèle d’événement. |
| [!UICONTROL 6th Event] to [!UICONTROL 30th Event] | Personnalisé | Les sixième à 30e types d’événements dans le chemin de conversion qui s’est produit dans le rapport de l’annonceur [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[propriété de transaction\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport pour chaque propriété de transaction incluse) Latence moyenne en jours entre le premier événement et une conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[propriété de transaction\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport) Latence moyenne en jours entre le dernier événement et une conversion. |
| [!UICONTROL Path Frequency] | Personnalisé | Nombre de fois où le chemin d’accès de cette ligne s’est produit avant la conversion. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [À propos des rapports d’aide](assist-report-about.md)
>* [Le [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Le [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Aide aux paramètres des rapports](assist-report-settings.md)
>* [Générer un rapport d’assistance](assist-report-generate.md)

