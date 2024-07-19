---
title: Exigences de données pour les flux de données à l’aide d’un ID de transaction
description: Référencez les exigences de données pour les flux de données à l’aide d’un ID de transaction.
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Exigences de données pour les flux de données à l’aide d’un ID de transaction

Vous trouverez ci-dessous les champs d’en-tête et les champs de données correspondants requis pour chaque type de fichier de flux.

>[!NOTE]
>* Les en-têtes peuvent être dans n’importe quel ordre tant que les données des lignes suivantes suivent le même ordre. Si vous n’incluez pas d’en-tête, l’ordre des lignes de données doit être cohérent avec celui de chaque fichier de flux.
>* Chaque ligne du fichier de flux doit contenir des données pour une transaction et la transaction doit être identifiée par un identifiant de transaction.

| Champ d’en-tête/Nom de colonne | Type | Description |
| ---- | ---- | ---- |
| ID de transaction (ev_transid) | Chaîne sensible à la casse | Identifiant généré par l’annonceur associé à la transaction. La balise de suivi de conversion d’Adobe Advertising étant utilisée pour les parties en ligne de la transaction, elle doit être identique à l’ID de transaction (ev_transid) fourni par l’Adobe Advertising pour la partie précédente de la transaction. Cela signifie que la balise de conversion pour la partie en ligne de la transaction doit inclure une mesure de conversion pour un ID de transaction unique.<br><br>**Remarque :** L’Adobe Advertising utilise l’ID pour localiser les anciennes données de transaction et les mettre à jour en fonction d’un mode d’insertion convenu (par exemple, pour remplacer les données existantes ou les agrémenter des nouvelles données). |
| Date de transaction | DateTime | Date de la transaction. Le format doit être cohérent pour chaque transaction. |
| Conversion spécifique au client | Chaîne | Conversion qui fait l’objet d’un suivi (type de transaction ou montant, par exemple). Discutez des conversions à inclure à l’équipe de mise en oeuvre d’Adobe Advertising avant de démarrer le flux. |

## Exemple

L’exemple de fichier suivant inclut des données pour deux mesures de conversion (Produit et Recettes).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Exigences liées aux fichiers pour les fichiers de flux de conversion](feed-file-requirements.md)
>* [Suivi des conversions à l’aide d’un flux d’ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id.md)
