---
title: 'Données de feuille d’envoi groupé requises pour les comptes  [!DNL Naver] '
description: Référencez les champs d’en-tête et de données obligatoires dans les feuilles d’envoi groupé pour les comptes  [!DNL Naver] .
exl-id: 1bfcdbb6-8026-4230-ab6b-b7c79b0d185a
feature: Search Bulksheets
source-git-commit: 7945887cf34c5ff390a35f1b9a6ede2888254c65
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Annexe - Données de feuille d’envoi groupé requises pour les comptes [!DNL Naver]

Renseignez vos comptes [!DNL Naver] dans Search, Social et Commerce en générant un fichier de feuille d’envoi groupé dans [!DNL Naver], puis en le chargeant dans Search, Social et Commerce.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## Champs de données disponibles

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Champ | Campagne | Groupe publicitaire | Mot-clé | Description |
|----|----|----|----|----|
| [!UICONTROL Platform] | s.o. | s.o. | s.o. | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) La plateforme publicitaire. Obligatoire sauf si chaque ligne comprend un ID AMO pour l’entité. |
| [!UICONTROL Acct Name] | Required/Optional | Required/Optional | Required/Optional | Nom unique qui identifie un compte réseau publicitaire. Obligatoire sauf si chaque ligne comprend un ID AMO pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire | Obligatoire | Obligatoire | Nom unique qui identifie une campagne pour un compte. |
| [!UICONTROL Ad Group Name] | s.o. | Obligatoire | Obligatoire | Nom unique qui identifie un groupe publicitaire. |
| [!UICONTROL Keyword] | s.o. | s.o. | Obligatoire | Chaîne du mot-clé. |
| [!UICONTROL Base URL] | s.o. | s.o. | Facultatif | L’URL de la page de destination vers laquelle les utilisateurs finaux sont dirigés lorsqu’ils cliquent sur votre annonce, y compris tout paramètre d’ajout configuré pour la campagne ou le compte.<br><br>Les URL de base/finales au niveau du mot-clé remplacent les URL au niveau de l’annonce publicitaire et au-delà. |
| [!UICONTROL Destination URL] | s.o. | s.o. | s.o. | (Incluse dans les feuilles d’envoi groupé générées à titre d’information ; non publiée sur le réseau publicitaire) Pour les comptes avec des URL de destination, cette valeur est l’URL qui lie une publicité à une URL de base/une page de destination sur le site web de l’annonceur (parfois via un autre site qui suit le clic et redirige ensuite l’utilisateur vers la page de destination). Elle inclut tous les paramètres d’ajout configurés pour la campagne ou le compte Search, Social et Commerce. Si vous avez généré des URL de tracking, cette valeur est basée sur les paramètres de tracking définis dans les paramètres de votre compte et de votre campagne. Si vous avez ajouté des paramètres spécifiques au réseau, ils peuvent être remplacés par des paramètres équivalents pour Recherche, Social et Commerce.<br><br>Pour les comptes avec URL finales, cette colonne affiche la même valeur que la [!UICONTROL Base URL/Final URL column]. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif | Facultatif | Facultatif | (Nom pour une classification d’étiquettes spécifique à l’annonceur, telle que « Couleur » pour une classification d’étiquettes appelée Couleur) Valeur pour la classification spécifiée associée à l’entité. Vous ne pouvez inclure qu’une seule valeur par classification par entité (telle que « rouge » pour la classification de libellé « Couleur » pour la campagne A). La longueur maximale est de 100 caractères et la valeur peut inclure des caractères ASCII et non ASCII.<br><br>Les classifications de libellés et leurs valeurs de libellé sont appliqués à tous les composants enfants ; les nouveaux composants ajoutés ultérieurement sont automatiquement associés au libellé. Les classifications d’étiquettes pour les groupes de produits sont appliquées au niveau de l’unité (le plus granulaire).<br><br>Le nom de la classification et la valeur de classification ne sont pas sensibles à la casse. |
| [!UICONTROL Constraints] | Facultatif | Facultatif | Facultatif | Contrainte affectée à l&#39;entité. Vous ne pouvez affecter qu&#39;une seule contrainte par entité.<br><br>Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire de saisir des valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées. |
| [!UICONTROL Campaign Status] | Facultatif : Créer ou modifier<br>Obligatoire : Supprimer | s.o. | s.o. | Le statut d’affichage de la campagne : *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (campagnes existantes uniquement). La valeur par défaut pour les nouvelles campagnes est <i>[!UICONTROL Active]</i>. Pour supprimer une campagne active ou en pause, saisissez la valeur « [!UICONTROL Deleted] ». |
| [!UICONTROL Ad Group Status] | s.o. | Facultatif : Créer ou modifier<br>Obligatoire : Supprimer | s.o. | Statut d’affichage du groupe publicitaire : *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (groupes publicitaires existants uniquement). La valeur par défaut pour les nouveaux groupes publicitaires est <i>[!UICONTROL Active]</i>. Pour supprimer un groupe publicitaire actif ou en pause, saisissez la valeur « [!UICONTROL Deleted] ». |
| [!UICONTROL Keyword Status] | s.o. | s.o. | Facultatif : Créer ou modifier<br>Obligatoire : Supprimer | Statut d’affichage du mot-clé : *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (mots-clés existants uniquement). La valeur par défaut des nouveaux mots-clés est <i>[!UICONTROL Active]</i>. Pour supprimer un mot-clé actif ou en pause, saisissez la valeur « [!UICONTROL Deleted] ». |
| [!UICONTROL Campaign ID] | n/a : Create<br>Required/Optional : Modifier ou supprimer | Facultatif | Facultatif | Identifiant unique qui identifie une campagne existante. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne comprend un ID AMO pour la campagne. |
| [!UICONTROL Ad Group ID] | s.o. | n/a : Create<br>Required/Optional : Modifier ou supprimer | Facultatif | Identifiant unique qui identifie un groupe publicitaire existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Obligatoire uniquement lorsque vous modifiez le nom du groupe publicitaire, sauf si la ligne comprend un ID AMO pour le groupe publicitaire. |
| [!UICONTROL Keyword ID] | s.o. | s.o. | n/a : Create<br>Required/Optional : Edit<br>Required : Supprimer | Identifiant unique qui identifie un mot-clé existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez le nom du mot-clé, à moins que la ligne ne contienne a) suffisamment de colonnes de propriétés pour identifier le mot-clé ou b) un identifiant AMO. |
| [!UICONTROL AMO ID] | n/a : Créer<br>Facultatif : Modifier ou supprimer | n/a : Créer<br>Facultatif : Modifier ou supprimer | n/a : Créer<br>Facultatif : Modifier ou supprimer | (Dans les feuilles d’envoi groupé générées) Identifiant unique généré par [!DNL Adobe] pour une entité synchronisée. Pour les annonces responsive sur le Réseau de Recherche, l’AMO ID est requis pour modifier ou supprimer des annonces, sauf si vous incluez l’[!UICONTROL Ad ID] . Pour modifier les données de tous les autres types d&#39;entités avec un ID AMO, l&#39;ID AMO est nécessaire pour modifier ou supprimer les données, sauf si vous incluez l&#39;ID d&#39;entité et l&#39;ID d&#39;entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |
| [!UICONTROL EF Error Message] | s.o. | s.o. | s.o. | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage des messages d’erreur de Search, Social et Commerce concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL EF Errors]. Cette valeur n&#39;est pas publiée sur le réseau publicitaire. |
| [!UICONTROL SE Error Message] | s.o. | s.o. | s.o. | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL SE Errors]. Cette valeur n&#39;est pas publiée sur le réseau publicitaire. |

[^1] : Excel convertit les grands nombres en notation scientifique (par exemple 2.12E+09 pour 2115585666) lorsqu’il ouvre le fichier. Pour afficher les chiffres dans la notation standard, sélectionnez une cellule de la colonne et cliquez dans la barre de formule.

>[!MORELIKETHIS]
>
>* [Annexe - Erreurs de feuille d’envoi groupé](../bulksheet-errors.md)
>* [Opérations que vous pouvez effectuer dans des feuilles d’envoi groupé](bulksheet-operations.md)
>* [Formats de fichiers de feuilles d’envoi groupé pris en charge](bulksheet-file-formats.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](../bulksheet-download.md)
>* [Formats de suivi des clics pour  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Charger un fichier de feuille d’envoi groupé ou un fichier d’erreur corrigé](../bulksheet-upload.md)
>* [Implémentation  [!DNL Naver]  comptes de tracking uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
