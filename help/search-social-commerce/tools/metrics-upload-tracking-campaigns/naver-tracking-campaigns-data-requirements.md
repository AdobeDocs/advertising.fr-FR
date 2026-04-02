---
title: Exigences en matière de données pour les mesures de trafic et de conversion pour les comptes  [!DNL Naver]  suivi uniquement
description: Référencez les exigences de chargement des données pour les comptes  [!DNL Naver]  suivi uniquement.
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
TQID: https://experienceleague.adobe.com/e4n2ab469CRIiEmqq5wd97pXSQZ9Dt-tehqJSp125GU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# Exigences en matière de données de mesure pour les comptes de suivi uniquement [!DNL Naver]

Vous trouverez ci-dessous les exigences en matière de données pour les mesures de trafic et de conversion [!DNL Naver] pour les comptes de suivi uniquement.

Les fichiers de données doivent être au format TSV, CSV ou TXT.

Les champs d’en-tête suivants sont obligatoires et facultatifs. Chaque ligne de données doit inclure une valeur agrégée par jour pour au moins un champ de mesure.

| Nom de champ/colonne d’en-tête | Type | Description |
| ---- | ---- | ---- |
| Période | DateTime | Date à laquelle les données s’appliquent, au format `YYYY.MM.DD.` (par exemple, `2019.11.15.`, avec un point après la journée). |
| Campagne | Chaîne sensible à la casse | Nom de la campagne. |
| Groupe publicitaire (en un mot) | Chaîne sensible à la casse | Nom du groupe publicitaire. |
| Mot-clé | Chaîne sensible à la casse | (Annonces par mot-clé) Mot-clé qui a généré l’annonce. |
| [Mesure] | Entier | (Facultatif) Nombre de [quelle que soit la mesure].</br><br>Les mesures standard incluent les impressions, les coûts et les clics. Vous pouvez inclure toutes les mesures supplémentaires souhaitées dans le réseau publicitaire. Incluez chaque mesure dans une colonne distincte.<br><br><b>Remarques :</b><ul><li>L&#39;en-tête de colonne du coût doit être « Coût (KRW) ».</li><li>Pour inclure le coût (KRW) des publicités de marque, divisez manuellement le coût mensuel fixe par jour au niveau du groupe publicitaire.</li><li>Supprimez toutes les virgules des valeurs de mesure standard. Par exemple, utilisez 1 000 au lieu de 1 000.</li><li>Pour les valeurs nulles, utilisez 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implémentation  [!DNL Naver]  comptes de tracking uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Annexe - Données de feuille d’envoi groupé requises pour  [!DNL Naver]  comptes ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Chargement des mesures de trafic et de conversion pour les comptes  [!DNL Naver]  suivi uniquement](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
