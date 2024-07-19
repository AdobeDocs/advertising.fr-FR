---
title: Suivi des conversions à l’aide d’un flux d’ID de transaction
description: Découvrez comment utiliser un flux d’ID de transaction pour les données de suivi de conversion.
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Suivi des conversions à l’aide d’un flux d’ID de transaction

Lorsqu’un annonceur effectue des transactions en ligne et hors ligne, il peut suivre les transactions en ligne par le biais du pixel de suivi de conversion de l’Adobe Advertising, et il peut suivre les transactions hors ligne à l’aide d’un ID de transaction et les diffuser par le biais d’un flux :

* Pour les transactions en ligne, Adobe Advertising effectue le suivi des clics sur vos publicités et des transactions qui en résultent sur votre site web.

* L’annonceur doit effectuer le suivi des conversions hors ligne et envoyer des fichiers de flux au niveau de la transaction à Adobe Advertising.

## Présentation de l’implémentation

*Gestionnaire de compte de l’agence, [!DNL Adobe] gestionnaire de compte et rôles utilisateur administrateur uniquement*

1. Utilisez les options de suivi de compte ou de campagne &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload]&quot; pour générer automatiquement une URL de destination ou une URL finale pour chaque mot-clé (pour le suivi au niveau du mot-clé) ou publicité (pour le suivi au niveau de la publicité) dans le compte ou la campagne.

1. Configurez le suivi de conversion d’Adobe Advertising pour les conversions en ligne. Ce processus est identique à celui des annonceurs qui effectuent un suivi de conversion basé sur les pixels Adobe Advertising. Il est important de générer des balises de conversion qui incluent un paramètre pour un ID de transaction unique (`ev_transid=<transid>`).

1. Pour la partie hors ligne de chaque transaction, l’annonceur génère le même ID de transaction qui a été utilisé dans la partie en ligne de la transaction à inclure dans le fichier de flux.

1. L’annonceur charge un fichier avec les [ données de conversion requises](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) vers l’emplacement de serveur désigné.

1. Les services techniques analysent les données de conversion dans les fichiers chargés, puis chargent les données dans Adobe Advertising. Adobe Advertising effectue ensuite le suivi des données par rapport à des mots-clés, publicités et emplacements individuels, puis crée une prévision de recettes pour chacun d’eux.

1. Les services techniques valident les données traitées par rapport aux données de flux et recherchent toutes les [transactions orphelines](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Exigences liées aux fichiers pour les fichiers de flux de conversion](feed-file-requirements.md)
>* [ Exigences de données pour les flux de données à l’aide d’un ID de transaction ](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
