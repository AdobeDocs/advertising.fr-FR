---
title: Données de feuille de support pour [!DNL Yahoo! Display Network] comptes
description: Référencez les champs d’en-tête et de données dans les feuilles d’envoi groupées téléchargées pour [!DNL Yahoo! Display Network] comptes.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Annexe : Données de feuille d’envoi groupé pour [!DNL Yahoo! Display Network] comptes

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

Vous pouvez télécharger des données pour [!DNL Yahoo! Display Network] comptes en bloc, mais ne peuvent pas télécharger ni publier de feuilles d’envoi groupé sur le réseau publicitaire.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Champs de données disponibles

| Champ | Campagne | Groupe publicitaire | Publicité | Description |
|----|----|----|----|----|
| [!UICONTROL Platform] | n/a | n/a | n/a | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) La plateforme publicitaire. |
| [!UICONTROL Acct  Name] | Si inclus | Si inclus | Si inclus | Nom unique qui identifie un compte réseau publicitaire. |
| [!UICONTROL Campaign Name] | Si inclus | Si inclus | Si inclus | Nom unique qui identifie une campagne pour un compte. |
| [!UICONTROL Ad Group Name] | n/a | Si inclus | Si inclus | Nom unique qui identifie un groupe publicitaire. |
| [!UICONTROL Ad Name] | n/a | n/a | Si inclus | Nom unique qui identifie la publicité dans un groupe publicitaire. La longueur maximale est de 50 caractères. |
| [!UICONTROL Ad Title] | n/a | n/a | Si inclus | Titre d’une publicité. |
| [!UICONTROL Description Line 1] | n/a | n/a | Si inclus | Première ligne du corps d’une publicité. |
| [!UICONTROL Description Line 2] | n/a | n/a | Si inclus | La deuxième ligne du corps d’une publicité. |
| [!UICONTROL Base URL/Final URL] | n/a | n/a | Si inclus | URL de la page d’entrée vers laquelle les utilisateurs finaux sont pris lorsqu’ils cliquent sur votre publicité, y compris les paramètres d’ajout configurés pour la campagne ou le compte. Les URL de base/finale au niveau du mot-clé remplacent les URL au niveau de la publicité et au-delà. |
| [!UICONTROL Destination URL] | n/a | n/a | n/a | (Inclus dans les feuilles d’envoi groupé générées à des fins d’information) ; (non publié sur le réseau publicitaire) Pour les comptes avec des URL de destination, cette valeur est l’URL qui lie une publicité à une URL de base/une page d’entrée sur le site web de l’annonceur (parfois via un autre site qui suit le clic, puis redirige l’utilisateur vers la page d’entrée). Il comprend tous les paramètres d’ajout configurés pour la campagne ou le compte Search, Social &amp; Commerce. Si vous avez généré des URL de suivi, cette valeur est basée sur les paramètres de suivi définis dans les paramètres de votre compte et de vos campagnes. Si vous avez ajouté des paramètres spécifiques au réseau publicitaire, ils peuvent être remplacés par les paramètres équivalents pour Search, Social et Commerce. |
| \[Classification d’étiquette spécifique au annonceur\] | Si inclus | Si inclus | Si inclus | (Nommé pour une classification d’étiquettes spécifique à l’annonceur, telle que &quot;Couleur&quot; pour une classification d’étiquettes appelée Couleur) Une valeur pour la classification spécifiée qui est associée à l’entité. |
| [!UICONTROL Constraints] | Si inclus | Si inclus | n/a | Contrainte affectée à l’entité. |
| [!UICONTROL Campaign Status] | Si inclus | n/a | n/a | Etat d&#39;affichage de l&#39;opération : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | n/a | Si inclus | n/a | État d’affichage du groupe publicitaire : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | n/a | n/a | Si inclus | L’état d’affichage du mot-clé : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>ou <i>[!UICONTROL Deleted]</i> (mots-clés existants uniquement). |
| [!UICONTROL Campaign ID] | Si inclus | Si inclus | Si inclus | Identifiant unique qui identifie une campagne existante. |
| [!UICONTROL Ad Group ID] | n/a | Si inclus | Si inclus | Identifiant unique qui identifie un groupe publicitaire existant. |
| [!UICONTROL Keyword ID] | n/a | n/a | Si inclus | Identifiant unique qui identifie un mot-clé existant. |
| [!UICONTROL AMO ID] | n/a | n/a | n/a | (Dans les feuilles d’envoi groupées générées) Identifiant unique généré par l’Adobe pour une entité synchronisée. |
| [!UICONTROL EF Error Message] | n/a | n/a | n/a | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des messages d’erreur de Search, Social et Commerce concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers d’erreurs EF. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Téléchargement/création d’un fichier de feuille d’envoi groupé](../bulksheet-download.md)
