---
title: '''[!DNL Baidu] paramètres de mots-clés'
description: Référencez les paramètres pour [!DNL Baidu] mots-clés.
exl-id: 70ecb5da-1056-4d87-82ba-ac03e0c81761
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] paramètres de mots-clés

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Mots-clés. La longueur maximale par mot-clé est de 30 caractères sur un ou 15 caractères sur deux octets

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes. Utilisez la syntaxe suivante :

* `keyword` pour une correspondance large
* `"keyword"` correspondant à l’expression
* `[keyword]` correspondant exactement à

>[!NOTE]
>
>* [!DNL Baidu] n’autorise qu’un seul type de correspondance par mot-clé par groupe publicitaire. Par exemple, le groupe d’annonces 1 ne peut pas inclure les deux `"keyword"` et `[keyword]`.
>* Vous pouvez créer des mots-clés négatifs à partir de la variable [!UICONTROL Keywords] > [!UICONTROL Negatives] afficher et dans les paramètres du groupe publicitaire et de la campagne.
>* Modification d’un [!DNL Baidu] Le mot-clé supprime le mot-clé existant et en crée un nouveau avec un nouvel identifiant de mot-clé. Toutefois, le fait de modifier le type de correspondance ne supprime pas le mot-clé existant.

**[!UICONTROL Status]:** L’état d’affichage du mot-clé : *Principal* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Principal*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Options d’URL

**[!UICONTROL Base URL]:** (Campagnes avec suivi au niveau des mots-clés uniquement ; facultatif) URL de la page d’entrée vers laquelle les utilisateurs sont redirigés lorsqu’ils cliquent sur votre publicité. Il peut inclure un code de redirection et de suivi tiers. Si vous saisissez une valeur, elle remplace l’URL de base de la publicité.

Une fois l’enregistrement enregistré, l’URL de base inclut tous les paramètres d’ajout configurés pour la campagne ou le compte.

Si vous utilisez le service de suivi de conversion d’Adobe Advertising et que les paramètres de campagne incluent l’utilisation de la variable [!UICONTROL EF Redirect] et en ajoutant le suivi au niveau des mots-clés, puis Search, Social et Commerce ajoute automatiquement son propre code de suivi des clics.

>[!MORELIKETHIS]
>
>* [Gestion des mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
