---
title: Exigences de données pour les mesures de trafic et de conversion pour les [!DNL Naver] comptes de suivi uniquement
description: Référencez les exigences de transfert de données pour [!DNL Naver] comptes de suivi uniquement.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Exigences de données de mesure pour [!DNL Naver] comptes de suivi uniquement

Voici les exigences en matière de données pour [!DNL Naver] mesures de trafic et de conversion pour les comptes de suivi uniquement.

Les fichiers de données doivent être au format TSV, CSV ou TXT.

Les champs d’en-tête suivants sont obligatoires et facultatifs. Chaque ligne de données doit inclure une valeur agrégée quotidienne pour au moins un champ de mesure.

| Champ d’en-tête/Nom de colonne | Type | Description |
| ---- | ---- | ---- |
| Période | DateTime | Date à laquelle les données s’appliquent, au format `YYYY.MM.DD.` (par exemple, `2019.11.15.`, avec un point après la journée). |
| Campagne | Chaîne sensible à la casse | Nom de la campagne. |
| Adgroup (en tant que mot) | Chaîne sensible à la casse | Nom du groupe publicitaire. |
| Mot-clé | Chaîne sensible à la casse | (Publicités par mots-clés) Mot-clé qui a généré la publicité. |
| [Mesure] | Entier | (Facultatif) Le nombre de [mesure de la mesure].</br><br>Les mesures standard comprennent les impressions, les coûts et les clics. Vous pouvez inclure toutes les mesures supplémentaires du réseau publicitaire. Incluez chaque mesure dans une colonne distincte.<br><br><b>Remarques :</b><ul><li>L’en-tête de colonne pour le coût doit être &quot;Coût (KRW)&quot;.</li><li>Pour inclure le coût (KRW) pour les publicités de marque, divisez manuellement le coût mensuel fixe par jour au niveau du groupe d’annonces.</li><li>Supprimez toutes les virgules des valeurs de mesure standard. Par exemple, utilisez 1 000 au lieu de 1 000.</li><li>Pour les valeurs nulles, utilisez 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Mise en oeuvre [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Annexe : Données de feuille d’envoi groupé requises pour [!DNL Naver] comptes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Chargement des mesures de trafic et de conversion pour [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)

