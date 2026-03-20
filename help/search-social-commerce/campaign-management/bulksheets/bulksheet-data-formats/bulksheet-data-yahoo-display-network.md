---
title: 'Données de feuille d’envoi groupé pour les comptes  [!DNL Yahoo! Display Network] '
description: Référencez les champs d’en-tête et de données dans les feuilles d’envoi groupé téléchargées pour les comptes  [!DNL Yahoo! Display Network] .
exl-id: 8d938009-6edc-4420-8863-21ed241616f8
feature: Search Bulksheets
source-git-commit: 7945887cf34c5ff390a35f1b9a6ede2888254c65
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Annexe - Données de feuille d’envoi groupé pour les comptes [!DNL Yahoo! Display Network]

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

Vous pouvez télécharger en bloc les données des comptes [!DNL Yahoo! Display Network], mais ne pouvez pas charger ni publier de feuilles d’envoi groupé sur le réseau publicitaire.

## Champs de données disponibles

| Champ | Campagne | Groupe publicitaire | Annonce publicitaire | Description |
|----|----|----|----|----|
| [!UICONTROL Platform] | s.o. | s.o. | s.o. | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) La plateforme publicitaire. |
| [!UICONTROL Acct  Name] | Si inclus | Si inclus | Si inclus | Nom unique qui identifie un compte réseau publicitaire. |
| [!UICONTROL Campaign Name] | Si inclus | Si inclus | Si inclus | Nom unique qui identifie une campagne pour un compte. |
| [!UICONTROL Ad Group Name] | s.o. | Si inclus | Si inclus | Nom unique qui identifie un groupe publicitaire. |
| [!UICONTROL Ad Name] | s.o. | s.o. | Si inclus | Nom unique qui identifie l’annonce publicitaire dans un groupe publicitaire. La longueur maximale est de 50 caractères. |
| [!UICONTROL Ad Title] | s.o. | s.o. | Si inclus | Titre d’une publicité. |
| [!UICONTROL Description Line 1] | s.o. | s.o. | Si inclus | Première ligne du corps d’une publicité. |
| [!UICONTROL Description Line 2] | s.o. | s.o. | Si inclus | Deuxième ligne du corps d’une publicité. |
| [!UICONTROL Base URL/Final URL] | s.o. | s.o. | Si inclus | L’URL de la page de destination vers laquelle les utilisateurs finaux sont dirigés lorsqu’ils cliquent sur votre annonce, y compris tout paramètre d’ajout configuré pour la campagne ou le compte. Les URL de base/finales au niveau du mot-clé remplacent les URL au niveau de l’annonce publicitaire et au-delà. |
| [!UICONTROL Destination URL] | s.o. | s.o. | s.o. | (Incluse dans les feuilles d’envoi groupé générées à titre d’information ; non publiée sur le réseau publicitaire) Pour les comptes avec des URL de destination, cette valeur est l’URL qui lie une publicité à une URL de base/une page de destination sur le site web de l’annonceur (parfois via un autre site qui suit le clic et redirige ensuite l’utilisateur vers la page de destination). Elle inclut tous les paramètres d’ajout configurés pour la campagne ou le compte Search, Social et Commerce. Si vous avez généré des URL de tracking, cette valeur est basée sur les paramètres de tracking définis dans les paramètres de votre compte et de votre campagne. Si vous avez ajouté des paramètres spécifiques au réseau, ils peuvent être remplacés par des paramètres équivalents pour Recherche, Réseaux sociaux et Commerce. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Si inclus | Si inclus | Si inclus | (Nom pour une classification d’étiquettes spécifique à l’annonceur, telle que « Couleur » pour une classification d’étiquettes appelée Couleur) Valeur pour la classification spécifiée associée à l’entité. |
| [!UICONTROL Constraints] | Si inclus | Si inclus | s.o. | Contrainte affectée à l&#39;entité. |
| [!UICONTROL Campaign Status] | Si inclus | s.o. | s.o. | Le statut d’affichage de la campagne : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | s.o. | Si inclus | s.o. | Statut d’affichage du groupe publicitaire : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | s.o. | s.o. | Si inclus | Statut d’affichage du mot-clé : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (mots-clés existants uniquement). |
| [!UICONTROL Campaign ID] | Si inclus | Si inclus | Si inclus | Identifiant unique qui identifie une campagne existante. |
| [!UICONTROL Ad Group ID] | s.o. | Si inclus | Si inclus | Identifiant unique qui identifie un groupe publicitaire existant. |
| [!UICONTROL Keyword ID] | s.o. | s.o. | Si inclus | Identifiant unique qui identifie un mot-clé existant. |
| [!UICONTROL AMO ID] | s.o. | s.o. | s.o. | (Dans les feuilles d’envoi groupé générées) Identifiant unique généré par Adobe pour une entité synchronisée. |
| [!UICONTROL EF Error Message] | s.o. | s.o. | s.o. | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage des messages d’erreur de Search, Social et Commerce concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL EF Errors]. |

>[!MORELIKETHIS]
>
>* [Télécharger/créer un fichier de feuille d’envoi groupé](../bulksheet-download.md)
