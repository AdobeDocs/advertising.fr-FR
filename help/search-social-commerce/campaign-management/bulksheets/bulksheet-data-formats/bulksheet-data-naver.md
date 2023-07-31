---
title: Données de feuille d’envoi groupé requises pour [!DNL Naver] comptes
description: Référencez les champs d’en-tête et de données requis dans les feuilles d’envoi groupées pour [!DNL Naver] comptes.
exl-id: bd6e3dab-47b0-428a-825d-bd9c21494fb0
feature: Search Bulksheets
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 1%

---

# Annexe : Données de feuille d’envoi groupé requises pour [!DNL Naver] comptes

Renseignez [!DNL Naver] comptes dans Search, Social et Commerce en générant un fichier de feuille d’envoi groupé dans [!DNL Naver], puis transférez-le vers Search, Social et Commerce.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Champs de données disponibles

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Champ | Campagne | Groupe publicitaire | Mot-clé | Description |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) La plateforme publicitaire. Obligatoire, sauf si chaque ligne comprend un AMO ID pour l’entité. |
| [!UICONTROL Acct Name] | Obligatoire/Facultatif | Obligatoire/Facultatif | Obligatoire/Facultatif | Nom unique qui identifie un compte réseau publicitaire. Obligatoire, sauf si chaque ligne comprend un AMO ID pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire | Obligatoire | Obligatoire | Nom unique qui identifie une campagne pour un compte. |
| [!UICONTROL Ad Group Name] | n/a | Obligatoire | Obligatoire | Nom unique qui identifie un groupe publicitaire. |
| [!UICONTROL Keyword] | n/a | n/a | Obligatoire | Chaîne du mot-clé. |
| [!UICONTROL Base URL] | n/a | n/a | Facultatif | URL de la page d’entrée vers laquelle les utilisateurs finaux sont pris lorsqu’ils cliquent sur votre publicité, y compris les paramètres d’ajout configurés pour la campagne ou le compte.<br><br>Les URL de base/finale au niveau du mot-clé remplacent les URL au niveau de la publicité et au-delà. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information ; non publiés sur le réseau publicitaire) Pour les comptes avec des URL de destination, cette valeur est l’URL qui lie une publicité à une URL/page d’entrée de base sur le site web de l’annonceur (parfois via un autre site qui effectue le suivi des clics, puis redirige l’utilisateur vers la page d’entrée). Il comprend tous les paramètres d’ajout configurés pour la campagne ou le compte Search, Social &amp; Commerce. Si vous avez généré des URL de suivi, cette valeur est basée sur les paramètres de suivi définis dans les paramètres de votre compte et de vos campagnes. Si vous avez ajouté des paramètres spécifiques au réseau, ils peuvent être remplacés par les paramètres équivalents pour Search, Social et Commerce.<br><br>Pour les comptes dont l’URL finale est renseignée, cette colonne affiche la même valeur que la variable [!UICONTROL Base URL/Final URL column]. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif | Facultatif | Facultatif | (Nommé pour une classification d’étiquettes spécifique à l’annonceur, telle que &quot;Couleur&quot; pour une classification d’étiquettes appelée Couleur) Une valeur pour la classification spécifiée qui est associée à l’entité. Vous ne pouvez inclure qu’une seule valeur par classification par entité (par exemple, &quot;rouge&quot; pour la classification d’étiquettes &quot;Couleur&quot; pour la campagne A). La longueur maximale est de 100 caractères et la valeur peut inclure des caractères ASCII et non ASCII.<br><br>Les classifications d’étiquettes et leurs valeurs d’étiquettes sont appliquées à tous les composants enfants ; les nouveaux composants ajoutés ultérieurement sont automatiquement associés au libellé. Les classifications d’étiquettes pour les groupes de produits sont appliquées au niveau de l’unité (la plus granulaire).<br><br>Le nom de la classification et la valeur de la classification ne sont pas sensibles à la casse. |
| [!UICONTROL Constraints] | Facultatif | Facultatif | Facultatif | Contrainte affectée à l’entité. Vous ne pouvez affecter qu’une seule contrainte par entité.<br><br>Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire de saisir des valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées. |
| [!UICONTROL Campaign Status] | Facultatif : créez ou modifiez des<br>Obligatoire : Supprimer | n/a | n/a | Etat d&#39;affichage de la campagne : *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, ou <i>[!UICONTROL Deleted]</i> (campagnes existantes uniquement). La valeur par défaut pour les nouvelles campagnes est <i>[!UICONTROL Active]</i>. Pour supprimer une campagne principale ou suspendue, saisissez la valeur &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | n/a | Facultatif : créez ou modifiez des<br>Obligatoire : Supprimer | n/a | État d’affichage du groupe publicitaire : *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, ou <i>[!UICONTROL Deleted]</i> (groupes publicitaires existants uniquement). La valeur par défaut pour les nouveaux groupes publicitaires est <i>[!UICONTROL Active]</i>. Pour supprimer un groupe publicitaire principal ou en pause, saisissez la valeur &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | n/a | n/a | Facultatif : créez ou modifiez des<br>Obligatoire : Supprimer | Etat d&#39;affichage du mot-clé : *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, ou <i>[!UICONTROL Deleted]</i> (mots-clés existants uniquement). La valeur par défaut des nouveaux mots-clés est <i>[!UICONTROL Active]</i>. Pour supprimer un mot-clé principal ou en pause, saisissez la valeur &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Campaign ID] | n/a : Créer<br>Obligatoire/Facultatif : modification ou suppression | Facultatif | Facultatif | Identifiant unique qui identifie une campagne existante. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le nom de la campagne, à moins que la ligne ne contienne un AMO ID pour la campagne. |
| [!UICONTROL Ad Group ID] | n/a | n/a : Créer<br>Obligatoire/Facultatif : modification ou suppression | Facultatif | Identifiant unique qui identifie un groupe publicitaire existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le nom du groupe publicitaire, sauf si la ligne inclut un AMO ID pour le groupe publicitaire. |
| [!UICONTROL Keyword ID] | n/a | n/a | n/a : Créer<br>Obligatoire/Facultatif : modification<br>Obligatoire : Supprimer | Identifiant unique qui identifie un mot-clé existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le nom du mot-clé, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le mot-clé ou b) un AMO ID. |
| [!UICONTROL AMO ID] | n/a : Créer<br>Facultatif : modification ou suppression | n/a : Créer<br>Facultatif : modification ou suppression | n/a : Créer<br>Facultatif : modification ou suppression | (Dans les feuilles d’envoi groupées générées) Une [!DNL Adobe]Identifiant unique généré pour une entité synchronisée. Pour les annonces de recherche réactive, l’AMO ID est requis pour modifier ou supprimer les annonces, sauf si vous incluez la variable [!UICONTROL Ad ID]. Pour modifier les données de tous les autres types d’entité avec un AMO ID, celui-ci doit les modifier ou les supprimer, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des messages d’erreur de Search, Social et Commerce concernant les données de la ligne ; les messages d’erreur sont inclus dans [!UICONTROL EF Errors] fichiers . Cette valeur n’est pas publiée sur le réseau publicitaire. |
| [!UICONTROL SE Error Message] | n/a | n/a | n/a | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans [!UICONTROL SE Errors] fichiers . Cette valeur n’est pas publiée sur le réseau publicitaire. |

[^1]: Excel convertit les grands nombres en notation scientifique (par exemple, 2.12E+09 pour 2115585666) lorsqu’il ouvre le fichier. Pour afficher les chiffres de la notation standard, sélectionnez n’importe quelle cellule de la colonne et cliquez dans la barre de formule.

>[!MORELIKETHIS]
>
>* [Annexe : Erreurs de feuilles d’envoi groupé](../bulksheet-errors.md)
>* [Opérations que vous pouvez effectuer dans des feuilles d’envoi groupées](bulksheet-operations.md)
>* [Formats de fichiers de feuille d’envoi groupé pris en charge](bulksheet-file-formats.md)
>* [Téléchargement/création d’un fichier de feuille d’envoi groupé](../bulksheet-download.md)
>* [Formats de suivi des clics pour [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Télécharger un fichier de feuille d’envoi groupé ou un fichier d’erreur corrigé](../bulksheet-upload.md)
>* [Mise en oeuvre [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
