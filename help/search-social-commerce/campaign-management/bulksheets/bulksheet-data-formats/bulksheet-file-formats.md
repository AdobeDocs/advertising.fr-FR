---
title: Formats de fichiers de feuille d’envoi groupé pris en charge
description: Référencez les exigences générales de fichier pour les feuilles d’envoi groupées.
exl-id: f3daf036-8f0c-4c75-9c76-2734abd850ec
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Formats de fichiers de feuille d’envoi groupé pris en charge

## Formats de fichier

Vous pouvez télécharger, charger et publier des fichiers de feuille d’envoi groupé pour les réseaux publicitaires pris en charge dans l’un des formats suivants :

* CSV (valeurs séparées par des virgules)
* TSV (valeurs séparées par des tabulations)
* TXT (texte Unicode), délimité par des virgules ou des tabulations
* Fichier ZIP (compressé) contenant un fichier au format CSV, TSV ou TXT délimité par des virgules ou des tabulations

Lorsque vous créez/téléchargez une feuille d’envoi groupé, elle est créée dans le format de fichier spécifié avec toutes les données pertinentes incluses dans le fichier. Utilisez les informations suivantes pour modifier les données du fichier ou pour créer manuellement votre propre feuille d’envoi groupé.

## Contenu de base d’une feuille de support

Le premier enregistrement (ligne) d’un fichier de feuille d’envoi groupé contient un ensemble de noms de colonne spécifiques, connus collectivement sous le nom d’<i>en-tête</i>. Les noms des colonnes dans l’en-tête sont dans un ordre spécifié et correspondent à chacun des champs des enregistrements de données suivants. Les noms des colonnes requis dans l’en-tête varient en fonction du réseau publicitaire.

Chaque enregistrement (ligne) suivant contient des données, avec des champs contenant des valeurs (ou aucune valeur) pour chaque colonne de l’en-tête.

## Taille maximale du fichier

Les fichiers de feuilles d’envoi groupé peuvent atteindre 2,5 Go, soit environ 2,5 millions de lignes.

>[!NOTE]
>
>Lorsque vous générez une feuille d’envoi groupé pour plusieurs campagnes et que les données combinées se composent de plus de 500 000 lignes, les données sont fractionnées par campagne en deux fichiers ou plus, nommés `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, etc.

## Exigences de mise en forme pour différents types de fichiers

Les champs de données délimités par des tabulations et par des virgules nécessitent une mise en forme différente.

### Fichiers TSV et fichiers TXT délimités par des onglets

Les champs de données des fichiers TSV et TXT délimités par des onglets doivent être formatés comme suit :

* Les champs de chaque enregistrement sont séparés par des caractères de tabulation. Pour omettre une valeur pour un champ, utilisez uniquement le caractère de tabulation.

  Exemple : `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Les champs ne peuvent pas contenir de caractères de tabulation incorporés.

### Fichiers CSV et fichiers TXT délimités par des virgules

Les champs de données des fichiers CSV et TXT délimités par des virgules doivent être formatés comme suit :

* Les champs d’un enregistrement sont séparés par des virgules. Pour omettre une valeur pour un champ, utilisez uniquement la virgule.

  Exemple : `Cruises,5000,Caribbean,,,`

* Tout champ peut éventuellement être inclus entre guillemets doubles (`""`).

  Exemple : `"Cruises","5000","Caribbean",`

* Les champs avec des virgules incorporées doivent être entourés de guillemets doubles (`""`).

  Exemple : `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Les champs avec des guillemets doubles incorporés doivent être entourés de guillemets doubles (`""`).

  Exemple : `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Les champs avec des espaces au début ou à la fin doivent être entourés de guillemets doubles (`""`).

  Exemple : `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](../bulksheet-about.md)
>* [Opérations que vous pouvez effectuer dans les feuilles d’envoi groupé](bulksheet-operations.md)
>* [Annexe - Erreurs de feuilles d’envoi groupé](../bulksheet-errors.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](../bulksheet-download.md)
