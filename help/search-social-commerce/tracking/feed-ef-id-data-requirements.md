---
title: Exigences en matière de données pour les flux de données utilisant des identifiants EF
description: Référencez les exigences en matière de données pour les flux de données à l’aide des identifiants EF.
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
TQID: https://experienceleague.adobe.com/p66X8xVlx-JwKjGgXxonJRRu78Q8F4109VkaIVtUbwU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 0%

---

# Exigences en matière de données pour les flux de données utilisant des identifiants EF

Vous trouverez ci-dessous les champs d’en-tête et les champs de données correspondants requis pour chaque type de fichier de flux.

>[!NOTE]
>* Les en-têtes peuvent être dans n’importe quel ordre tant que les données des lignes suivantes suivent le même ordre. Si vous n’incluez pas d’en-tête, l’ordre des lignes de données doit être cohérent avec chaque fichier de flux.
>* Chaque ligne du fichier de flux doit contenir des données pour une transaction, et la transaction doit être identifiée par un ef_id généré par Adobe Advertising (jeton).

| Nom de champ/colonne d’en-tête | Type | Description |
| ---- | ---- | ---- |
| ID EF | Chaîne sensible à la casse | ef_id (jeton) que vous avez capturé lors du clic pour la transaction, qui se compose de l’identifiant de l’utilisateur, de l’heure de clic et du type de réseau. Ne modifiez pas la valeur. |
| ID de transaction | Chaîne sensible à la casse | (Facultatif mais recommandé) Identifiant de transaction généré par l’annonceur. La bonne pratique consiste à inclure ceci pour chaque transaction, même si ef_id est utilisé pour suivre la transaction au moment de la redirection. |
| Date de transaction | DateTime | Date de la transaction. Le format doit être cohérent pour chaque transaction. |
| Conversion spécifique au client | String | Conversion faisant l’objet d’un suivi (type de transaction ou montant, par exemple). Discutez des conversions à inclure avec l’équipe d’implémentation d’Adobe Advertising avant de démarrer le flux. |

## Exemple

Le fichier d’exemple suivant inclut des données pour deux mesures de conversion (Produit et Chiffre d’affaires).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Exigences relatives aux fichiers de flux de conversion](feed-file-requirements.md)
>* [Suivi des conversions à l’aide d’un flux d’ID EF](/help/search-social-commerce/tracking/feed-efid.md)
