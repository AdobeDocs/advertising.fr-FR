---
title: '[!UICONTROL Keyword Assist Report]'
description: En savoir plus sur les [!UICONTROL Keyword Assist Report].
exl-id: 07de2880-111b-498f-9f7f-ec15f89230ae
feature: Search Reports, Search Assist Reports
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# La variable [!UICONTROL Keyword Assist Report]

*Annonceurs avec suivi des clics Search, Social et Commerce et suivi des conversions à partir d’Adobe Advertising, Adobe Analytics (avec un [!DNL Analytics] intégration) ou fournie dans les flux à l’aide d’un jeton (`ef_id`) uniquement*

La variable [!UICONTROL Keyword Assist Report] indique les mots-clés ou les emplacements qui génèrent des clics. Le rapport présente chaque modèle de mots-clés de recherche payante ou d’emplacements ayant reçu des clics dans un chemin de conversion et indique comment ce modèle a contribué à vos conversions globales. Vous pouvez, par exemple, déterminer le nombre de conversions survenues lorsque les utilisateurs ont d’abord cliqué sur une publicité résultant d’une recherche par mot-clé de &quot;chaussures en cuir&quot;, puis cliqué sur une publicité après une recherche par mot-clé de &quot;chaussures en daim&quot;, puis passé une commande. Vous pouvez également déterminer le nombre de conversions survenues après que les utilisateurs ont cliqué sur des publicités issues de plus de 10 mots-clés.

Les résultats du rapport incluent des données agrégées pour un maximum de N mots-clés de recherche payante ou de clics d’emplacement les plus anciens dans le chemin de conversion qui se sont produits dans les intervalles de recherche en amont des clics et des impressions de l’annonceur. Si, par exemple, vous sélectionnez une taille de chemin de cinq (5), le rapport se compose de chemins de conversion comprenant jusqu’aux cinq premiers mots-clés ou emplacements ayant reçu des clics, avec une ligne pour chaque modèle de clics suivi. Chaque ligne comprend le premier mot-clé ou l’emplacement dans le chemin et le dernier mot-clé ou emplacement qui a généré des conversions (même si le dernier mot-clé se trouve en dehors de la taille de chemin spécifiée). Par défaut, les lignes sont dans l’ordre croissant en fonction du nombre d’événements dans le chemin.

>[!NOTE]
>
>Si le rapport inclut des emplacements provenant de campagnes de recherche activées sur le contenu (qui n’incluent pas de mots-clés), la variable [!UICONTROL Keyword] affiche les noms des groupes d’annonces applicables, tels que &quot;(contenu du groupe) Nom de votre groupe d’annonces&quot;.

Vous pouvez éventuellement inclure des données de conversion agrégées pour chaque ligne. Lorsque vous incluez des colonnes conversions/recettes dans le rapport, chaque type de conversion est représenté en quatre colonnes, ce qui indique a) le nombre total de conversions, b) le pourcentage de vos conversions globales qui ont été attribuées à ce modèle de mot-clé, c) la latence moyenne en jours entre le premier événement (le premier mot-clé) et d) la latence moyenne en jours entre le dernier événement (le dernier mot-clé) et une conversion. Lorsque le chemin de conversion comprend plus de mots-clés que la taille de chemin spécifiée, le rapport inclut des lignes supplémentaires agrègant les données pour les conversions, en raison du nombre plus élevé de mots-clés (comme tous les modèles qui incluaient des clics sur six mots-clés).

Vous pouvez afficher les données des 18 mois précédents.

## Colonnes disponibles

Vous trouverez ci-dessous les colonnes disponibles pour chaque rapport. Les colonnes par défaut sont automatiquement incluses par défaut. Vous pouvez ajouter les colonnes personnalisées disponibles à partir de la section Colonnes des paramètres du rapport.

| Colonne | Par défaut ? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] to [!UICONTROL 5th Keyword] | Par défaut | Les cinq premiers clics de recherche payante ou d’emplacement dans le chemin de conversion qui s’est produit dans le [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Remarque :</b> Si le rapport inclut des emplacements provenant de campagnes de recherche activées sur le contenu (qui n’incluent pas de mots-clés), ces colonnes indiquent les noms de groupes d’annonces applicables, tels que &quot;(contenu de groupe) Votre nom de groupe d’annonces&quot;, à la place. |
| [!UICONTROL Path Size] | Par défaut | Nombre de mots-clés et/ou d’emplacements dans le chemin de conversion qui se sont produits dans le rapport de l’annonceur [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Par défaut | Premier mot-clé ou emplacement dans le chemin de conversion. |
| [!UICONTROL Last Keyword] | Par défaut | Dernier mot-clé ou emplacement ayant généré des conversions (même si le dernier mot-clé se trouve en dehors de la taille de chemin spécifiée). |
| \[Mesures personnalisées (dérivées) spécifiques aux annonceurs\] | Personnalisé | La valeur d’une mesure personnalisée que vous avez créée et calculée à partir de mesures existantes. |
| \[Propriétés de transaction spécifiques aux annonceurs\] | Personnalisé | Nombre de conversions pour une propriété de transaction ou une mesure d’engagement du site spécifiée. |
| [!UICONTROL % of Total] \[propriété de transaction\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport pour chaque propriété de transaction incluse) Le pourcentage de vos conversions globales entre les portfolios qui ont été attribués au mot-clé et/ou au modèle d’emplacement. |
| [!UICONTROL 6th Keyword] to [!UICONTROL 10th Keyword] | Personnalisé | Le sixième à dixième mot-clé de recherche payante ou clics d’emplacement dans le chemin de conversion qui s’est produit dans le chemin de l’annonceur [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Remarque :</b> Si le rapport inclut des emplacements provenant de campagnes de recherche activées sur le contenu (qui n’incluent pas de mots-clés), ces colonnes indiquent les noms de groupes d’annonces applicables, tels que &quot;(contenu de groupe) Votre nom de groupe d’annonces&quot;, à la place. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[propriété de transaction\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport pour chaque propriété de transaction incluse) Latence moyenne en jours entre le premier événement (sur le premier mot-clé ou emplacement) et une conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[propriété de transaction\] | Automatique | (Non disponible dans les paramètres de rapport, mais automatiquement inclus dans la sortie du rapport) Latence moyenne en jours entre le dernier événement (sur le dernier mot-clé ou emplacement) et une conversion. |
| [!UICONTROL Path Frequency] | Personnalisé | Nombre de fois où le chemin d’accès de cette ligne s’est produit avant la conversion. |

>[!MORELIKETHIS]
>
>* [À propos des rapports d’aide](assist-report-about.md)
>* [La variable [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [La variable [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Aide aux paramètres des rapports](assist-report-settings.md)
>* [Générer un rapport d’assistance](assist-report-generate.md)
