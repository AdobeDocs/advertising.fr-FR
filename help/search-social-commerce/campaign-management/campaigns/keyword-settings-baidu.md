---
title: Paramètres des mots-clés '[!DNL Baidu]'
description: Référencez les paramètres de  [!DNL Baidu] mots-clés.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# [!DNL Baidu] paramètres de mot-clé

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Mots-clés. La longueur maximale par mot-clé est de 30 caractères sur un ou 15 caractères sur deux octets

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes. Utilisez la syntaxe suivante :

* `keyword` pour une correspondance large
* `"keyword"` pour la correspondance d’expression
* `[keyword]` pour une correspondance exacte

>[!NOTE]
>
>* [!DNL Baidu] n’autorise qu’un seul type de correspondance par mot-clé et par groupe publicitaire. Par exemple, le groupe d’annonces 1 ne peut pas inclure à la fois `"keyword"` et `[keyword]`.
>* Vous pouvez créer des mots-clés négatifs à partir de la vue [!UICONTROL Keywords] > [!UICONTROL Negatives] et dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d&#39;un mot-clé [!DNL Baidu] supprime le mot-clé existant et en crée un nouveau avec un nouvel identifiant de mot-clé. Toutefois, le fait de modifier le type de correspondance ne supprime pas le mot-clé existant.

**[!UICONTROL Status]:** État d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Options d’URL

**[!UICONTROL Base URL]:** (Campagnes avec suivi au niveau des mots-clés uniquement ; facultatif) URL de la page d’entrée vers laquelle les utilisateurs sont dirigés lorsqu’ils cliquent sur votre publicité. Elle peut inclure
code de redirection et de suivi tiers. Si vous saisissez une valeur, elle remplace l’URL de base de la publicité.

Une fois l’enregistrement enregistré, l’URL de base inclut tous les paramètres d’ajout configurés pour la campagne ou le compte.

Si vous utilisez le service de suivi de conversion d’Adobe Advertising et que les paramètres de campagne incluent l’utilisation de [!UICONTROL EF Redirect] et l’ajout du suivi au niveau du mot-clé, Search, Social et Commerce ajoute automatiquement son propre code de suivi des clics.

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
