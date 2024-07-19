---
title: '[!UICONTROL Keyword Assist Report]'
description: Découvrez [!UICONTROL Keyword Assist Report].
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# Le [!UICONTROL Keyword Assist Report]

*Annonceurs avec suivi des clics Search, Social et Commerce et avec suivi des conversions à partir d’Adobe Advertising, Adobe Analytics (avec une intégration [!DNL Analytics]) ou fournis dans des flux à l’aide d’un jeton (`ef_id`) uniquement*

Le [!UICONTROL Keyword Assist Report] indique les mots-clés ou les emplacements qui génèrent des clics. Le rapport présente chaque modèle de mots-clés de recherche payante ou d’emplacements ayant reçu des clics dans un chemin de conversion et indique comment ce modèle a contribué à vos conversions globales. Vous pouvez, par exemple, déterminer le nombre de conversions survenues lorsque les utilisateurs ont d’abord cliqué sur une publicité résultant d’une recherche par mot-clé de &quot;chaussures en cuir&quot;, puis cliqué sur une publicité après une recherche par mot-clé de &quot;chaussures en daim&quot;, puis passé une commande. Vous pouvez également déterminer le nombre de conversions survenues après que les utilisateurs ont cliqué sur des publicités issues de plus de 10 mots-clés.

Les résultats du rapport incluent des données agrégées pour un maximum de N mots-clés de recherche payante ou de clics d’emplacement les plus anciens dans le chemin de conversion qui s’est produit dans le
cliquez sur intervalles de recherche en amont et d’impression. Si, par exemple, vous sélectionnez une taille de chemin de cinq (5), le rapport se compose de chemins de conversion comprenant jusqu’aux cinq premiers mots-clés ou emplacements ayant reçu des clics, avec une ligne pour chaque modèle de clics suivi. Chaque ligne comprend le premier mot-clé ou l’emplacement dans le chemin et le dernier mot-clé ou emplacement qui a généré des conversions (même si le dernier mot-clé se trouve en dehors de la taille de chemin spécifiée). Par défaut, les lignes sont dans l’ordre croissant en fonction du nombre d’événements dans le chemin.

>[!NOTE]
>
>Si le rapport inclut des emplacements provenant de campagnes de recherche activées sur le contenu (qui n’incluent pas de mots-clés), la colonne [!UICONTROL Keyword] indique les noms de groupes d’annonces applicables, tels que &quot;(contenu du groupe) Votre nom de groupe d’annonces&quot;.

Vous pouvez éventuellement inclure des données de conversion agrégées pour chaque ligne. Lorsque vous incluez des colonnes conversions/recettes dans le rapport, chaque type de conversion est représenté en quatre colonnes, ce qui indique a) le nombre total de conversions, b) le pourcentage de vos conversions globales qui ont été attribuées à ce modèle de mot-clé, c) la latence moyenne en jours entre le premier événement (le premier mot-clé) et d) la latence moyenne en jours entre le dernier événement (le dernier mot-clé) et une conversion. Lorsque le chemin de conversion comprend plus de mots-clés que la taille de chemin spécifiée, le rapport inclut des lignes supplémentaires agrègant les données pour les conversions, en raison du nombre plus élevé de mots-clés (comme tous les modèles qui incluaient des clics sur six mots-clés).

Vous pouvez afficher les données des 18 mois précédents.

## Colonnes disponibles

Vous trouverez ci-dessous les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section Colonnes des paramètres du rapport.

| Colonne | Par défaut ? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] à [!UICONTROL 5th Keyword] | Par défaut | Les cinq mots-clés de recherche payante ou clics d’emplacement les plus anciens dans le chemin de conversion qui s’est produit dans l’ [ intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) de l’annonceur et l’ [ intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Remarque :</b> Si le rapport inclut des emplacements provenant de campagnes de recherche activées pour le contenu (qui n’incluent pas de mots-clés), ces colonnes affichent alors les noms de groupes d’annonces applicables, tels que &quot;(contenu du groupe) Votre nom de groupe d’annonces&quot;, à la place. |
| [!UICONTROL Path Size] | Par défaut | Nombre de mots-clés et/ou d’emplacements dans le chemin de conversion qui se sont produits dans l’ [ intervalle de recherche en amont des clics de l’annonceur](/help/search-social-commerce/glossary.md#c-d) et l’ [ intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Par défaut | Premier mot-clé ou emplacement dans le chemin de conversion. |
| [!UICONTROL Last Keyword] | Par défaut | Dernier mot-clé ou emplacement ayant généré des conversions (même si le dernier mot-clé se trouve en dehors de la taille de chemin spécifiée). |
| \[Mesures personnalisées (dérivées) spécifiques aux annonceurs\] | Personnalisé | La valeur d’une mesure personnalisée que vous avez créée et calculée à partir de mesures existantes. |
| \[Mesures de conversion spécifiques aux annonceurs\] | Personnalisé | Nombre de conversions pour une mesure de conversion spécifiée ou une mesure d’engagement du site. |
| [!UICONTROL % of Total] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) Le pourcentage de vos conversions globales entre les portefeuilles qui ont été attribués au mot-clé et/ou au modèle d’emplacement. |
| [!UICONTROL 6th Keyword] à [!UICONTROL 10th Keyword] | Personnalisé | Le sixième à dixième mot-clé de recherche payante ou clics d’emplacement dans le chemin de conversion qui s’est produit dans l’ [ intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) de l’annonceur et l’ [ intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Remarque :</b> Si le rapport inclut des emplacements provenant de campagnes de recherche activées pour le contenu (qui n’incluent pas de mots-clés), ces colonnes affichent alors les noms de groupes d’annonces applicables, tels que &quot;(contenu du groupe) Votre nom de groupe d’annonces&quot;, à la place. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres du rapport, mais automatiquement inclus dans la sortie du rapport pour chaque mesure de conversion incluse) Latence moyenne en jours entre le premier événement (sur le premier mot-clé ou emplacement) et une conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[mesure de conversion\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport) Latence moyenne en jours entre le dernier événement (sur le dernier mot-clé ou emplacement) et une conversion. |
| [!UICONTROL Path Frequency] | Personnalisé | Nombre de fois où le chemin d’accès de cette ligne s’est produit avant la conversion. |

>[!MORELIKETHIS]
>
>* [À propos des rapports d’assistance](assist-report-about.md)
>* [ [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [ [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [ Paramètres du rapport d’assistance ](assist-report-settings.md)
>* [Générer un rapport d’assistance](assist-report-generate.md)
