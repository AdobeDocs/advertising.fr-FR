---
title: Formats de fichiers de feuilles d’envoi groupé pris en charge
description: Référencez les exigences générales en matière de fichiers pour les feuilles d’envoi groupé.
exl-id: f3daf036-8f0c-4c75-9c76-2734abd850ec
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/LaEsBPLbF3nbcIJljn6TvQMmgFU7C-UPEoVjAXu7dp0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 417
ht-degree: 0%

---

# Formats de fichiers de feuilles d’envoi groupé pris en charge

## Formats de fichier

Vous pouvez télécharger, charger et publier des fichiers de feuille d’envoi groupé pour les réseaux publicitaires pris en charge dans l’un des formats suivants :

* CSV (valeurs séparées par des virgules)
* TSV (valeurs séparées par des tabulations)
* TXT (texte Unicode), délimité par des virgules ou des tabulations
* ZIP (compressé) contenant un fichier au format CSV, TSV ou TXT délimité par des virgules ou des tabulations

Lorsque vous créez/téléchargez une feuille d’envoi groupé, elle est créée dans le format de fichier spécifié avec toutes les données pertinentes incluses dans le fichier. Utilisez les informations suivantes pour modifier les données du fichier ou pour créer manuellement votre propre feuille d&#39;envoi groupé.

## Contenu de base d’une feuille de support

Le premier enregistrement (ligne) d’un fichier de feuille d’envoi groupé contient un ensemble de noms de colonnes spécifiques, collectivement appelés <i> en-tête </i>. Les noms des colonnes de l’en-tête sont dans un ordre spécifié et correspondent à chacun des champs des enregistrements de données suivants. Les noms de colonne requis dans l’en-tête varient selon le réseau publicitaire.

Chaque enregistrement suivant (ligne) contient des données, avec des champs contenant des valeurs (ou aucune valeur) pour chaque colonne de l’en-tête.

## Taille de fichier maximale

Les fichiers de feuille d’envoi groupé peuvent contenir jusqu’à 2,5 Go, soit environ 2,5 millions de lignes.

>[!NOTE]
>
>Lorsque vous générez une feuille d’envoi groupé pour plusieurs campagnes et que les données combinées se composent de plus de 500 000 lignes, les données sont fractionnées par campagne en deux fichiers ou plus, nommés `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, etc.

## Exigences de formatage pour différents types de fichiers

Les champs de données délimités par des tabulations et des virgules nécessitent une mise en forme différente.

### Fichiers TSV et TXT délimités par des tabulations

Les champs de données des fichiers TSV et des fichiers TXT délimités par des onglets doivent être formatés comme suit :

* Les champs de chaque enregistrement sont séparés par des tabulations. Pour omettre une valeur pour un champ, utilisez uniquement le caractère de tabulation.

  Exemple : `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Les champs ne peuvent pas contenir de caractères d’onglet incorporés.

### Fichiers CSV et TXT délimités par des virgules

Les champs de données des fichiers CSV et TXT délimités par des virgules doivent être formatés comme suit :

* Les champs d&#39;un enregistrement sont séparés par des virgules. Pour omettre une valeur pour un champ, utilisez uniquement la virgule.

  Exemple : `Cruises,5000,Caribbean,,,`

* Tout champ peut éventuellement être placé entre guillemets doubles (`""`).

  Exemple : `"Cruises","5000","Caribbean",`

* Les champs contenant des virgules incorporées doivent être placés entre guillemets doubles (`""`).

  Exemple : `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Les champs contenant des guillemets doubles incorporés doivent être placés entre guillemets doubles (`""`).

  Exemple : `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Les champs comportant des espaces de début ou de fin doivent être placés entre guillemets doubles (`""`).

  Exemple : `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l&#39;aide de feuilles d&#39;envoi groupé](../bulksheet-about.md)
>* [Opérations que vous pouvez effectuer dans des feuilles d’envoi groupé](bulksheet-operations.md)
>* [Annexe - Erreurs de feuille d’envoi groupé](../bulksheet-errors.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](../bulksheet-download.md)
