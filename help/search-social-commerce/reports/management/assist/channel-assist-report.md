---
title: '[!UICONTROL Channel Assist Report]'
description: En savoir plus sur le [!UICONTROL Channel Assist Report].
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
TQID: https://experienceleague.adobe.com/G2KcySAZVdf-J14CxQS2Hk5av6KHlpyFehwfMcZYj78
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 684
ht-degree: 0%

---

# Le [!UICONTROL Channel Assist Report]

*Publicitaires avec suivi des clics Search, Social et Commerce et avec suivi des conversions à partir d’Adobe Advertising, Adobe Analytics (avec une intégration [!DNL Analytics]) ou fournis dans les flux à l’aide d’un jeton (`ef_id`) uniquement*

Les [!UICONTROL Channel Assist Report] indiquent comment divers canaux marketing (recherche ou réseaux sociaux à partir de Search, Social et Commerce ; ou affichage ou vidéo à partir d’Advertising DSP) ont contribué au processus de conversion. Le rapport montre comment chaque modèle de types d’événements qui a conduit à une ou plusieurs conversions a contribué à vos conversions globales. Par exemple, vous pouvez voir le nombre de conversions qui se sont produites lorsque les utilisateurs ont d’abord vu une impression d’annonce publicitaire, puis cliqué sur une annonce de recherche, puis passé une commande ; ou vous pouvez voir le nombre de conversions qui se sont produites après que les utilisateurs ont interagi avec plus de 10 annonces. Les types d’événements incluent les clics de recherche, les impressions et clics d’affichage, les impressions et clics vidéo, ainsi que d’autres impressions et clics. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

Les résultats du rapport incluent des données agrégées pour chaque modèle de types d’événements dans le chemin de conversion (jusqu’aux N premiers types d’événements) qui s’est produit dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et [impression](/help/search-social-commerce/glossary.md#i-j) de l’annonceur. Par exemple, si vous sélectionnez une taille de chemin de cinq (5), le rapport inclut les chemins de conversion qui incluent jusqu’aux cinq événements les plus anciens, avec une ligne pour chaque modèle de types d’événements suivi (comme « clic de recherche », puis « impression d’affichage »). Chaque ligne affiche un modèle d’événements, y compris le premier événement du chemin et le dernier événement qui a entraîné des conversions (même si le dernier événement se trouve en dehors de la taille de chemin spécifiée). Par défaut, les lignes sont dans l’ordre croissant en fonction du nombre d’événements dans le chemin d’accès.

Vous pouvez éventuellement inclure des données de conversion d’agrégat pour chaque ligne. Lorsque vous incluez des colonnes conversions/chiffre d’affaires dans le rapport, chaque type de conversion est représenté en quatre colonnes, indiquant a) le nombre total de conversions, b) le pourcentage de vos conversions globales qui a été attribué à ce modèle d’événement, c) la latence moyenne par jour du premier événement à une conversion et d) la latence moyenne par jour du dernier événement à une conversion. Lorsque le chemin de conversion comprend plus d’événements que la taille de chemin spécifiée, le rapport inclut des lignes supplémentaires agrégeant les données pour les conversions résultant du nombre plus élevé d’événements (comme tous les modèles qui incluaient six types d’événements).

Vous pouvez afficher les données des 18 mois précédents.

## Colonnes disponibles

Voici les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section Colonnes des paramètres du rapport.

| Colonne | Par défaut ? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] à [!UICONTROL 5th Event] | Par défaut | Les cinq premiers types d’événements dans le chemin de conversion qui se sont produits dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et [impression de l’annonceur](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Par défaut | Nombre de types d’événements dans le chemin de conversion qui se sont produits dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et [impression](/help/search-social-commerce/glossary.md#i-j) de l’annonceur. |
| [!UICONTROL First Event Type] | Par défaut | Type d’événement du premier événement (le plus ancien) dans le chemin de conversion. |
| [!UICONTROL Last Event Type] | Par défaut | Type d’événement du dernier événement ayant entraîné des conversions (même si le dernier événement se trouve en dehors de la taille de chemin spécifiée). |
| \[Mesures personnalisées (dérivées) spécifiques à l’annonceur\] | Valeur personnalisée | Valeur d’une mesure personnalisée que vous avez créée, calculée à partir de mesures existantes. |
| \[Mesures de conversion spécifiques à l’annonceur\] | Valeur personnalisée | Nombre de conversions pour une mesure de conversion ou une mesure d’engagement du site spécifiée. |
| [!UICONTROL % of Total] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) Le pourcentage de vos conversions globales dans les portefeuilles qui ont été attribuées au modèle d’événement. |
| [!UICONTROL 6th Event] à [!UICONTROL 30th Event] | Valeur personnalisée | Les sixième à 30e types d’événements dans le chemin de conversion qui se sont produits dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et [impression](/help/search-social-commerce/glossary.md#i-j) de l’annonceur. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) La latence moyenne en jours du premier événement à une conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport) Latence moyenne en jours entre le dernier événement et une conversion. |
| [!UICONTROL Path Frequency] | Valeur personnalisée | Nombre de fois où le chemin d’accès à cette ligne s’est produit avant la conversion. |

>[!MORELIKETHIS]
>
>* [À propos des rapports d’assistance](assist-report-about.md)
>* [Le [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Le [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Paramètres des rapports d’assistance](assist-report-settings.md)
>* [Générer un rapport d’assistance](assist-report-generate.md)
