---
title: '[!UICONTROL Campaign Assist Report]'
description: En savoir plus sur le [!UICONTROL Campaign Assist Report].
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
source-git-commit: 7a87d3c3827125adb97f50986823568c9aef8c24
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 1%

---

# Le [!UICONTROL Campaign Assist Report]

*Publicitaires avec suivi des clics Search, Social et Commerce et avec suivi des conversions à partir d’Adobe Advertising, Adobe Analytics (avec une intégration [!DNL Analytics]) ou fournis dans les flux à l’aide d’un jeton (`ef_id`) uniquement*

La [!UICONTROL Campaign Assist Report] indique les campagnes qui ont contribué au processus de conversion. Le indique comment chaque modèle de campagnes dont les annonces publicitaires ont généré une ou plusieurs conversions a contribué à vos conversions globales. Par exemple, vous pouvez voir le nombre de conversions qui se sont produites lorsque les utilisateurs ont d’abord vu une annonce de la campagne A, puis cliqué sur une annonce de la campagne B, puis passé une commande. De même, vous pouvez voir le nombre de conversions qui se sont produites après que les utilisateurs ont interagi avec des annonces provenant de plus de 10 campagnes.

Les résultats du rapport incluent des données agrégées pour chaque modèle de campagnes dans le chemin de conversion (jusqu’aux N premières campagnes) pour les événements qui se sont produits dans l’[intervalle de recherche en amont de clics](/help/search-social-commerce/glossary.md#c-d) et l’[intervalle de recherche en amont d’impressions](/help/search-social-commerce/glossary.md#i-j) de l’annonceur. Par exemple, si vous sélectionnez une taille de chemin de cinq (5), le rapport inclut les chemins de conversion qui incluaient jusqu’aux cinq premières campagnes, avec une ligne pour chaque modèle de campagnes dont les événements ont été suivis. Chaque ligne affiche un modèle de campagnes, y compris la première campagne du chemin d’accès et la dernière campagne qui a généré des conversions (même si la dernière campagne se trouve en dehors de la taille de chemin spécifiée). Par défaut, les lignes sont classées par ordre croissant en fonction du nombre de campagnes dans le chemin d’accès.

Vous pouvez éventuellement inclure des données de conversion agrégées, y compris vos mesures personnalisées, pour chaque ligne. Lorsque vous incluez des colonnes conversions/chiffre d’affaires dans le rapport, chaque type de conversion est représenté en quatre colonnes, indiquant a) le nombre total de conversions, b) le pourcentage de vos conversions globales qui a été attribué à ce modèle de campagne, c) la latence moyenne en jours entre le premier événement (dans la première campagne) et une conversion, et d) la latence moyenne en jours entre le dernier événement (dans la dernière campagne) et une conversion. Lorsque le chemin de conversion inclut plus de campagnes que la taille de chemin spécifiée, le rapport inclut des lignes supplémentaires agrégeant les données pour les conversions résultant du nombre de campagnes le plus élevé (comme tous les modèles qui incluaient six campagnes).

Vous pouvez également inclure le réseau publicitaire et/ou le type d’événement après le nom de la campagne, tel que `<campaign name> (Google) click`.

Vous pouvez afficher les données des 18 mois précédents.

>[!TIP]
>
>Si les mots-clés de votre marque se trouvent dans une campagne différente de vos mots-clés génériques, le rapport indique si vos mots-clés de marque contribuent aux conversions.

## Colonnes disponibles

Voici les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section Colonnes des paramètres du rapport.

| Colonne | Par défaut ? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] à [!UICONTROL 5th Campaign] | Par défaut | Les cinq premières campagnes du chemin de conversion qui se sont produites dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et [impression de l’annonceur](/help/search-social-commerce/glossary.md#i-j).<br><br>Si vous avez inclus l’une des options de rapport pour indiquer le réseau publicitaire, le nom de compte ou le type d’événement après le nom de l’entité, ces informations sont incluses après le nom de la campagne (`"<"campaign name> [Google] [Account1] [impression]`, par exemple). |
| [!UICONTROL Path Size] | Par défaut | Nombre de campagnes dans le chemin de conversion qui se sont produites dans l’[intervalle de recherche en amont de clic](/help/search-social-commerce/glossary.md#c-d) et l’[intervalle de recherche en amont d’impression](/help/search-social-commerce/glossary.md#i-j) de l’annonceur. |
| [!UICONTROL First Campaign] | Par défaut | Première campagne du chemin de conversion. |
| [!UICONTROL Last Campaign] | Par défaut | Dernière campagne ayant généré des conversions (même si le dernier mot-clé est en dehors de la taille de chemin spécifiée).<br><br>Si vous avez inclus l’une des options de rapport pour indiquer le réseau publicitaire, le nom de compte ou le type d’événement après le nom de l’entité, ces informations sont incluses après le nom de la campagne (`"<"campaign name> [Google] [Account1] [impression]`, par exemple). |
| \[Mesures personnalisées (dérivées) spécifiques à l’annonceur\] | Valeur personnalisée | Valeur d’une mesure personnalisée que vous avez créée, calculée à partir de mesures existantes. |
| \[Mesures de conversion spécifiques à l’annonceur\] | Valeur personnalisée | Nombre de conversions pour une mesure de conversion ou une mesure d’engagement du site spécifiée. |
| [!UICONTROL % of Total] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) Le nombre de conversions pour une mesure de conversion spécifiée qui a résulté du modèle de campagne. |
| [!UICONTROL 6th Campaign] à [!UICONTROL 20th Campaign] | Valeur personnalisée | Les sixième à 20e campagnes du chemin de conversion qui se sont produites dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et [impression](/help/search-social-commerce/glossary.md#i-j) de l’annonceur.<br><br>Si vous avez inclus l’une des options de rapport pour indiquer le réseau publicitaire, le nom de compte ou le type d’événement après le nom de l’entité, ces informations sont incluses après le nom de la campagne (`"<"campaign name> [Baidu] [Account1] [click]`, par exemple). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) Latence moyenne en jours entre le premier événement (dans la première campagne) et une conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport) Latence moyenne en jours entre le dernier événement (dans la dernière campagne) et une conversion. |
| [!UICONTROL EF Campaign ID] | Valeur personnalisée | Identifiant numérique attribué par Search, Social et Commerce à la campagne. |
| [!UICONTROL EF Portfolio Group ID] | Valeur personnalisée | Identifiant numérique du groupe de portefeuilles auquel appartient le portefeuille. |
| [!UICONTROL EF Search Engine ID] | Valeur personnalisée | L’identifiant numérique que Search, Social et Commerce attribue au réseau publicitaire : <i>[!UICONTROL 3]</i> pour [!DNL Google Ads], <i>[!UICONTROL 10]</i> pour [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> pour [!DNL Meta], <i>[!UICONTROL 86]</i> pour [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> pour [!DNL Naver], <i>[!UICONTROL 88]</i> pour [!DNL Baidu], <i>[!UICONTROL 90]</i> pour [!DNL Yandex], <i>[!UICONTROL 94]</i> pour [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> pour [!DNL Yahoo Native], <i>[!UICONTROL 106]</i> pour [!DNL Pinterest] (obsolète) ou pour (obsolète). |
| [!UICONTROL Portfolio ID] | Valeur personnalisée | Identifiant numérique de portfolio. |
| [!UICONTROL User SE Account ID] | Valeur personnalisée | Identifiant numérique attribué par Search, Social et Commerce au réseau publicitaire. |

>[!MORELIKETHIS]
>
>* [À propos des rapports d’assistance](assist-report-about.md)
>* [Le [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Le [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Paramètres des rapports d’assistance](assist-report-settings.md)
>* [Générer un rapport d’assistance](assist-report-generate.md)
