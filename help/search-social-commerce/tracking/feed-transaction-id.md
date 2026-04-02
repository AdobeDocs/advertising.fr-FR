---
title: Suivi des conversions à l’aide d’un flux d’ID de transaction
description: Découvrez comment utiliser un flux d’ID de transaction pour les données de suivi des conversions.
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
TQID: https://experienceleague.adobe.com/wGlR5tUF7ajbnQLUnW0c-U84BskLzr63Wet-e-x823M
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 0%

---

# Suivi des conversions à l’aide d’un flux d’ID de transaction

Lorsqu’un annonceur possède des transactions en ligne et hors ligne, Adobe Advertising peut effectuer le suivi des transactions en ligne au moyen du pixel de suivi des conversions d’Adobe Advertising. L’annonceur peut également effectuer le suivi des transactions hors ligne à l’aide d’un identifiant de transaction et les diffuser via un flux :

* Pour les transactions en ligne, Adobe Advertising effectue le suivi des clics sur vos annonces et des transactions résultantes sur votre site web.

* L’annonceur doit effectuer le suivi des conversions hors ligne et envoyer des fichiers de flux au niveau des transactions à Adobe Advertising.

## Présentation de l’implémentation

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte [!DNL Adobe] et d’utilisateur administrateur uniquement*

1. Utilisez les options de suivi de compte ou de campagne « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] » pour générer automatiquement une URL de destination ou une URL finale pour chaque mot-clé (pour le suivi au niveau du mot-clé) ou publicité (pour le suivi au niveau de l’annonce) dans le compte ou la campagne.

1. Configurez le suivi des conversions Adobe Advertising pour les conversions en ligne. Ce processus est identique à celui des annonceurs avec le suivi de conversion basé sur les pixels d’Adobe Advertising. Il est important de générer des balises de conversion qui incluent un paramètre pour un ID de transaction unique (`ev_transid=<transid>`).

1. Pour la partie hors ligne de chaque transaction, l’annonceur génère le même ID de transaction qui a été utilisé dans la partie en ligne de la transaction à inclure dans le fichier de flux.

1. L’annonceur télécharge un fichier contenant les [données de conversion requises](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) à l’emplacement du serveur désigné.

1. Les services techniques analysent les données de conversion dans les fichiers chargés, puis chargent les données dans Adobe Advertising. Adobe Advertising effectue ensuite le suivi des données par rapport à des mots-clés, des annonces et des emplacements individuels et crée des prévisions de chiffre d’affaires pour chacun.

1. Les services techniques valident les données traitées par rapport aux données de flux et vérifient toute [transaction orpheline](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Exigences relatives aux fichiers de flux de conversion](feed-file-requirements.md)
>* [Exigences de données pour les flux de données utilisant un ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
