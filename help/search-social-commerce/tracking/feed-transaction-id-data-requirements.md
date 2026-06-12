---
title: Exigences de données pour les flux de données utilisant un ID de transaction
description: Référencez les exigences en matière de données pour les flux de données à l’aide d’un identifiant de transaction.
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TONScPVaJyxsORRD-sOrYXwEzO9rsa6ERPUo8oSRono
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# Exigences de données pour les flux de données utilisant un ID de transaction

Vous trouverez ci-dessous les champs d’en-tête et les champs de données correspondants requis pour chaque type de fichier de flux.

>[!NOTE]
>* Les en-têtes peuvent être dans n’importe quel ordre tant que les données des lignes suivantes suivent le même ordre. Si vous n’incluez pas d’en-tête, l’ordre des lignes de données doit être cohérent avec chaque fichier de flux.
>* Chaque ligne du fichier de flux doit contenir des données pour une transaction, et la transaction doit être identifiée par un ID de transaction.

| Nom de champ/colonne d’en-tête | Type | Description |
| ---- | ---- | ---- |
| ID de transaction (ev_transid) | Chaîne sensible à la casse | Identifiant généré par l’annonceur et associé à la transaction. Comme la balise de suivi des conversions Adobe Advertising est utilisée pour les parties en ligne de la transaction, elle doit être identique à l’ID de transaction (ev_transid) fourni par Adobe Advertising pour la partie précédente de la transaction. Cela signifie que la balise de conversion pour la partie en ligne de la transaction doit inclure une mesure de conversion pour un ID de transaction unique.<br><br>**Remarque :** Adobe Advertising utilise l’ID pour localiser les anciennes données de transaction et les mettre à jour selon un mode d’insertion convenu (par exemple, pour remplacer les données existantes ou les compléter par les nouvelles données). |
| Date de transaction | DateTime | Date de la transaction. Le format doit être cohérent pour chaque transaction. |
| Conversion spécifique au client | String | Conversion faisant l’objet d’un suivi (type de transaction ou montant, par exemple). Discutez des conversions à inclure avec l’équipe d’implémentation d’Adobe Advertising avant de démarrer le flux. |

## Exemple

Le fichier d’exemple suivant inclut des données pour deux mesures de conversion (Produit et Chiffre d’affaires).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Exigences relatives aux fichiers de flux de conversion](feed-file-requirements.md)
>* [Suivi des conversions à l’aide d’un flux d’ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id.md)
