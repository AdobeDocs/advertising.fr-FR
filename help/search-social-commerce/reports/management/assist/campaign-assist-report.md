---
title: '[!UICONTROL Campaign Assist Report]'
description: En savoir plus sur les [!UICONTROL Campaign Assist Report].
exl-id: 7fbc9c17-c77d-485b-8d51-5e5a153d7a2b
feature: Search Reports, Search Assist Reports
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# La variable [!UICONTROL Campaign Assist Report]

*Annonceurs avec suivi des clics Search, Social et Commerce et suivi des conversions à partir d’Adobe Advertising, Adobe Analytics (avec un [!DNL Analytics] intégration) ou fournie dans les flux à l’aide d’un jeton (`ef_id`) uniquement*

La variable [!UICONTROL Campaign Assist Report] indique les campagnes qui ont contribué au processus de conversion. Le rapport indique comment chaque modèle de campagnes dont les publicités ont entraîné une ou plusieurs conversions a contribué à vos conversions globales. Vous pouvez, par exemple, voir le nombre de conversions survenues lorsque les utilisateurs ont vu une publicité de la campagne A, puis cliqué sur une publicité de la campagne B, puis passé une commande. De même, vous pouvez déterminer le nombre de conversions survenues après l’interaction des utilisateurs avec des publicités issues de plus de 10 campagnes.

Les résultats du rapport incluent des données agrégées pour chaque modèle de campagne dans le chemin de conversion (jusqu’aux N premières campagnes) pour les événements qui se sont produits dans le rapport de l’annonceur. [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). Si, par exemple, vous sélectionnez une taille de chemin de cinq (5), le rapport comprend des chemins de conversion comprenant jusqu’à cinq campagnes au plus tôt, avec une ligne pour chaque modèle de campagne dont les événements ont été suivis. Chaque ligne présente un modèle de campagne, y compris la première campagne dans le chemin et la dernière campagne qui a généré des conversions (même si la dernière campagne est en dehors de la taille de chemin spécifiée). Par défaut, les lignes sont dans l’ordre croissant en fonction du nombre de campagnes dans le chemin.

Vous pouvez éventuellement inclure des données de conversion agrégées, y compris vos mesures personnalisées, pour chaque ligne. Lorsque vous incluez des colonnes de conversions/recettes dans le rapport, chaque type de conversion est représenté en quatre colonnes, ce qui indique a) le nombre total de conversions, b) le pourcentage de vos conversions globales qui ont été attribuées à ce modèle de campagne, c) la latence moyenne en jours entre le premier événement (dans la première campagne) et une conversion, et d) la latence moyenne en jours du dernier événement (dans la dernière campagne) à une conversion. Lorsque le chemin de conversion inclut plus de campagnes que la taille de chemin spécifiée, le rapport inclut des lignes supplémentaires agrègant les données pour les conversions résultant du nombre plus élevé de campagnes (comme tous les modèles qui incluaient six campagnes).

Vous pouvez également inclure le réseau publicitaire et/ou le type d’événement après le nom de la campagne, par exemple `<campaign name> (Google) click`.

Vous pouvez afficher les données des 18 mois précédents.

>[!TIP]
>
>Si vos mots-clés de marque font partie d’une campagne différente de vos mots-clés génériques, le rapport indique si vos mots-clés de marque contribuent aux conversions.

## Colonnes disponibles

Vous trouverez ci-dessous les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section Colonnes des paramètres du rapport.

| Colonne | Par défaut ? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] to [!UICONTROL 5th Campaign] | Par défaut | Les cinq premières campagnes dans le chemin de conversion qui se sont produites dans le [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j).<br><br>Si vous avez inclus l’une des options de rapport pour indiquer le réseau publicitaire, le nom du compte ou le type d’événement après le nom de l’entité, ces informations sont incluses après le nom de la campagne (par exemple `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| [!UICONTROL Path Size] | Par défaut | Le nombre de campagnes dans le chemin de conversion qui se sont produites dans le rapport de l’annonceur [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Par défaut | Première campagne du chemin de conversion. |
| [!UICONTROL Last Campaign] | Par défaut | La dernière campagne qui a généré des conversions (même si le dernier mot-clé est en dehors de la taille de chemin spécifiée).<br><br>Si vous avez inclus l’une des options de rapport pour indiquer le réseau publicitaire, le nom du compte ou le type d’événement après le nom de l’entité, ces informations sont incluses après le nom de la campagne (par exemple `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| \[Mesures personnalisées (dérivées) spécifiques aux annonceurs\] | Personnalisé | La valeur d’une mesure personnalisée que vous avez créée et calculée à partir de mesures existantes. |
| \[Mesures de conversion spécifiques aux annonceurs\] | Personnalisé | Nombre de conversions pour une mesure de conversion spécifiée ou une mesure d’engagement du site. |
| [!UICONTROL % of Total] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) Le nombre de conversions pour une mesure de conversion spécifiée qui a résulté du modèle de campagne. |
| [!UICONTROL 6th Campaign] to [!UICONTROL 20th Campaign] | Personnalisé | Les sixième à 20 campagnes dans le chemin de conversion qui s’est produit dans le rapport de l’annonceur [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j).<br><br>Si vous avez inclus l’une des options de rapport pour indiquer le réseau publicitaire, le nom du compte ou le type d’événement après le nom de l’entité, ces informations sont incluses après le nom de la campagne (par exemple `"<"campaign name> [Baidu] [Account1] [click]`&quot;). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) Latence moyenne en jours entre le premier événement (de la première campagne) et une conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport) Latence moyenne en jours entre le dernier événement (de la dernière campagne) et une conversion. |
| [!UICONTROL EF Campaign ID] | Personnalisé | Identifiant numérique attribué à la campagne par Search, Social et Commerce. |
| [!UICONTROL EF Portfolio Group ID] | Personnalisé | Identifiant numérique pour le groupe de portefeuille auquel appartient le portfolio. |
| [!UICONTROL EF Search Engine ID] | Personnalisé | Identifiant numérique attribué par Search, Social et Commerce au réseau publicitaire : <i>[!UICONTROL 3]</i> pour [!DNL Google Ads], <i>[!UICONTROL 10]</i> pour [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> pour [!DNL Meta], <i>[!UICONTROL 86]</i> pour [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> pour [!DNL Naver], <i>[!UICONTROL 88]</i> pour [!DNL Baidu], <i>[!UICONTROL 90]</i> pour [!DNL Yandex], <i>[!UICONTROL 94]</i> pour [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> pour [!DNL Yahoo Native] (obsolète) ou <i>[!UICONTROL 106]</i> pour [!DNL Pinterest] (obsolète). |
| [!UICONTROL Portfolio ID] | Identifiant numérique de portefeuille. |
| [!UICONTROL User SE Account ID] | Identifiant numérique attribué par Search, Social et Commerce au réseau publicitaire. |

>[!MORELIKETHIS]
>
>* [À propos des rapports d’aide](assist-report-about.md)
>* [La variable [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [La variable [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Aide aux paramètres des rapports](assist-report-settings.md)
>* [Générer un rapport d’assistance](assist-report-generate.md)
