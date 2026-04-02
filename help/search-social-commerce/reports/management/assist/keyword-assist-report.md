---
title: '[!UICONTROL Keyword Assist Report]'
description: En savoir plus sur le [!UICONTROL Keyword Assist Report].
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
TQID: https://experienceleague.adobe.com/LO6nDisgA7981cjrGw31tJcy4VR6lesl-wvwU7uGlK4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 781
ht-degree: 0%

---

# Le [!UICONTROL Keyword Assist Report]

*Publicitaires avec suivi des clics Search, Social et Commerce et avec suivi des conversions à partir d’Adobe Advertising, Adobe Analytics (avec une intégration [!DNL Analytics]) ou fournis dans les flux à l’aide d’un jeton (`ef_id`) uniquement*

La [!UICONTROL Keyword Assist Report] indique les mots-clés ou emplacements qui génèrent les clics. Le rapport présente chaque modèle de mots-clés de référencement payant ou d’emplacements ayant reçu des clics dans un chemin de conversion et indique comment ce modèle a contribué à vos conversions globales. Par exemple, vous pouvez voir le nombre de conversions qui se sont produites lorsque les utilisateurs ont d’abord cliqué sur une annonce résultant d’une recherche par mot-clé pour « chaussures en cuir », puis ont cliqué sur une annonce après une recherche par mot-clé pour « chaussures en daim », puis ont passé une commande ; ou vous pouvez voir le nombre de conversions qui se sont produites après que les utilisateurs ont cliqué sur des annonces résultant de plus de 10 mots-clés.

Les résultats du rapport incluent des données agrégées pour jusqu’aux N premiers clics de mots-clés de référencement payant ou d’emplacement dans le chemin de conversion qui se sont produits dans le fichier de l’annonceur
cliquez sur intervalles de recherche en amont et de recherche en amont d’impression. Par exemple, si vous sélectionnez une taille de chemin de cinq (5), le rapport se compose de chemins de conversion qui incluent jusqu’aux cinq mots-clés ou emplacements les plus anciens ayant reçu des clics, avec une ligne pour chaque modèle de clics suivi. Chaque ligne inclut le premier mot-clé ou emplacement dans le chemin d’accès et le dernier mot-clé ou emplacement ayant entraîné des conversions (même si le dernier mot-clé est en dehors de la taille de chemin d’accès spécifiée). Par défaut, les lignes sont dans l’ordre croissant en fonction du nombre d’événements dans le chemin d’accès.

>[!NOTE]
>
>Si le rapport inclut des emplacements de campagnes de recherche activées pour le contenu (qui n’incluent pas de mots-clés), la colonne [!UICONTROL Keyword] affiche les noms de groupe publicitaire applicables, tels que « (contenu du groupe publicitaire) Nom de votre groupe publicitaire ».

Vous pouvez éventuellement inclure des données de conversion d’agrégat pour chaque ligne. Lorsque vous incluez des colonnes conversions/chiffre d’affaires dans le rapport, chaque type de conversion est représenté en quatre colonnes, indiquant a) le nombre total de conversions, b) le pourcentage de vos conversions globales qui a été attribué à ce modèle de mot-clé, c) la latence moyenne en jours entre le premier événement (sur le premier mot-clé) et une conversion, et d) la latence moyenne en jours entre le dernier événement (sur le dernier mot-clé) et une conversion. Lorsque le chemin de conversion comprend plus de mots-clés que la taille de chemin spécifiée, le rapport inclut des lignes supplémentaires agrégeant les données pour les conversions résultant du nombre plus élevé de mots-clés (comme tous les modèles qui incluaient des clics sur six mots-clés).

Vous pouvez afficher les données des 18 mois précédents.

## Colonnes disponibles

Voici les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section Colonnes des paramètres du rapport.

| Colonne | Par défaut ? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] à [!UICONTROL 5th Keyword] | Par défaut | Les cinq premiers clics de mot-clé de référencement payant ou d’emplacement dans le chemin de conversion qui se sont produits dans l’[intervalle de recherche en amont de clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont d’impressions](/help/search-social-commerce/glossary.md#i-j) de l’annonceur.<br><br><b>Remarque :</b> si le rapport inclut des emplacements de campagnes de recherche activées pour le contenu (qui n’incluent pas de mots-clés), ces colonnes affichent les noms de groupe publicitaire applicables, tels que « (contenu du groupe publicitaire) Nom de votre groupe publicitaire » à la place. |
| [!UICONTROL Path Size] | Par défaut | Nombre de mots-clés et/ou d’emplacements dans le chemin de conversion qui se sont produits dans l’intervalle de recherche en amont de clic [clics](/help/search-social-commerce/glossary.md#c-d) et l’intervalle de recherche en amont d’impression [ de l’annonceur](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Par défaut | Premier mot-clé ou emplacement dans le chemin de conversion. |
| [!UICONTROL Last Keyword] | Par défaut | Dernier mot-clé ou dernier emplacement ayant entraîné des conversions (même si le dernier mot-clé est en dehors de la taille de chemin spécifiée). |
| \[Mesures personnalisées (dérivées) spécifiques à l’annonceur\] | Valeur personnalisée | Valeur d’une mesure personnalisée que vous avez créée, calculée à partir de mesures existantes. |
| \[Mesures de conversion spécifiques à l’annonceur\] | Valeur personnalisée | Nombre de conversions pour une mesure de conversion ou une mesure d’engagement du site spécifiée. |
| [!UICONTROL % of Total] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie de rapport pour chaque mesure de conversion incluse) Pourcentage de vos conversions globales dans les portefeuilles qui ont été attribuées au mot-clé et/ou au modèle d’emplacement. |
| [!UICONTROL 6th Keyword] à [!UICONTROL 10th Keyword] | Valeur personnalisée | Du sixième au dixième mots-clés de référencement payant ou clics d’emplacement dans le chemin de conversion qui se sont produits dans l’intervalle de recherche en amont de clics [intervalle de recherche en amont de clics](/help/search-social-commerce/glossary.md#c-d) et [ intervalle de recherche en amont d’impressions](/help/search-social-commerce/glossary.md#i-j) de l’annonceur.<br><br><b>Remarque :</b> si le rapport inclut des emplacements de campagnes de recherche activées pour le contenu (qui n’incluent pas de mots-clés), ces colonnes affichent les noms de groupe publicitaire applicables, tels que « (contenu du groupe publicitaire) Nom de votre groupe publicitaire » à la place. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) Latence moyenne en jours entre le premier événement (sur le premier mot-clé ou emplacement) et une conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport) Latence moyenne en jours entre le dernier événement (sur le dernier mot-clé ou le dernier emplacement) et une conversion. |
| [!UICONTROL Path Frequency] | Valeur personnalisée | Nombre de fois où le chemin d’accès à cette ligne s’est produit avant la conversion. |

>[!MORELIKETHIS]
>
>* [À propos des rapports d’assistance](assist-report-about.md)
>* [Le [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [Le [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Paramètres des rapports d’assistance](assist-report-settings.md)
>* [Générer un rapport d’assistance](assist-report-generate.md)
