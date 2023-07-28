---
title: Exigences de données pour les flux de données à l’aide des ID EF
description: Référencez les exigences de données pour les flux de données à l’aide des identifiants EF.
exl-id: 15e76f3a-c376-4e7b-b3c8-ca76fd427002
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Exigences de données pour les flux de données à l’aide des ID EF

Vous trouverez ci-dessous les champs d’en-tête et les champs de données correspondants requis pour chaque type de fichier de flux.

>[!NOTE]
>* Les en-têtes peuvent être dans n’importe quel ordre tant que les données des lignes suivantes suivent le même ordre. Si vous n’incluez pas d’en-tête, l’ordre des lignes de données doit être cohérent avec celui de chaque fichier de flux.
>* Chaque ligne du fichier de flux doit contenir des données pour une transaction et la transaction doit être identifiée par un ef_id (jeton) généré par l’Adobe Advertising.

| Champ d’en-tête/Nom de colonne | Type | Description |
| ---- | ---- | ---- |
| EF ID | Chaîne sensible à la casse | ef_id (jeton) que vous avez capturé lors du clic pour la transaction, qui comprend l’ID de surfeur, l’heure du clic et le type de réseau. Ne modifiez pas la valeur. |
| ID de transaction | Chaîne sensible à la casse | (Facultatif mais recommandé) Identifiant de transaction généré par l’annonceur. La bonne pratique consiste à inclure cette valeur pour chaque transaction, même si ef_id est utilisé pour effectuer le suivi de la transaction au moment de la redirection. |
| Date de transaction | DateTime | Date de la transaction. Le format doit être cohérent pour chaque transaction. |
| Conversion spécifique au client | Chaîne | Conversion qui fait l’objet d’un suivi (type de transaction ou montant, par exemple). Discutez des conversions à inclure à l’équipe de mise en oeuvre d’Adobe Advertising avant de démarrer le flux. |

## Exemple

L’exemple de fichier suivant inclut des données pour deux propriétés de transaction (Produit et Recettes).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Exigences liées aux fichiers de flux de conversion](feed-file-requirements.md)
>* [Suivi des conversions à l’aide d’un flux d’identifiant EF](/help/search-social-commerce/tracking/feed-efid.md)
