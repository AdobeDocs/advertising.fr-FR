---
title: Exigences de données pour les mesures de trafic et de conversion pour les comptes de suivi  [!DNL Naver] uniquement
description: Référencez les exigences de chargement de données pour les comptes  [!DNL Naver] de suivi uniquement.
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Exigences de données de mesure pour les comptes de suivi uniquement [!DNL Naver]

Vous trouverez ci-dessous les exigences de données pour les mesures de trafic et de conversion [!DNL Naver] pour les comptes de suivi uniquement.

Les fichiers de données doivent être au format TSV, CSV ou TXT.

Les champs d’en-tête suivants sont obligatoires et facultatifs. Chaque ligne de données doit inclure une valeur agrégée quotidienne pour au moins un champ de mesure.

| Champ d’en-tête/Nom de colonne | Type | Description |
| ---- | ---- | ---- |
| Période | DateTime | Date pour laquelle les données s’appliquent, au format `YYYY.MM.DD.` (par exemple `2019.11.15.`, avec un point après le jour). |
| Campagne | Chaîne sensible à la casse | Nom de la campagne. |
| Adgroup (en tant que mot) | Chaîne sensible à la casse | Nom du groupe publicitaire. |
| Mot-clé | Chaîne sensible à la casse | (Publicités par mots-clés) Mot-clé qui a généré la publicité. |
| [Mesure] | Entier | (Facultatif) Le nombre de [quelle que soit la mesure ].</br><br> Les mesures standard comprennent les impressions, les coûts et les clics. Vous pouvez inclure toutes les mesures supplémentaires du réseau publicitaire. Incluez chaque mesure dans une colonne distincte.<br><br><b>Notes :</b><ul><li>L’en-tête de colonne pour le coût doit être &quot;Coût (KRW)&quot;.</li><li>Pour inclure le coût (KRW) pour les publicités de marque, divisez manuellement le coût mensuel fixe par jour au niveau du groupe d’annonces.</li><li>Supprimez toutes les virgules des valeurs de mesure standard. Par exemple, utilisez 1 000 au lieu de 1 000.</li><li>Pour les valeurs nulles, utilisez 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implémentation [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Annexe - Données de feuille d’envoi groupé requises pour [!DNL Naver] comptes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [ Chargement des mesures de trafic et de conversion pour les  [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
