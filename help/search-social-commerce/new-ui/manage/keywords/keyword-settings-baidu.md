---
title: Paramètres des mots-clés [!DNL Baidu]
description: Référencez les paramètres des mots-clés [!DNL Baidu].
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%
---
# Paramètres des mots-clés [!DNL Baidu]

## [!UICONTROL Basic Settings]

*Nouveaux mots-clés uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte de réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne.

**[!UICONTROL Ad Group]:** groupe publicitaire .

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Les mots-clés La longueur maximale par mot-clé est de 30 caractères codés sur un octet ou de 15 caractères codés sur deux octets.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes. Utilisez la syntaxe suivante :

* `keyword` pour une large correspondance
* `"keyword"` pour la correspondance d’expressions
* `[keyword]` pour une correspondance exacte

>[!NOTE]
>
>* [!DNL Baidu] n’autorise qu’un seul type de correspondance par mot-clé par groupe publicitaire. Par exemple, le groupe publicitaire 1 ne peut pas inclure à la fois `"keyword"` et `[keyword]`.
>* Vous pouvez créer des mots-clés négatifs à partir de l’onglet [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] , ainsi que dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d’un mot-clé [!DNL Baidu] supprime le mot-clé existant et en crée un nouveau avec un nouvel ID de mot-clé. Toutefois, la modification du type de correspondance ne supprime pas le mot-clé existant.

**[!UICONTROL Status]:** statut d’affichage du mot-clé : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. La valeur par défaut des nouveaux mots-clés est *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL URL Options]

**[!UICONTROL Base URL]:** (campagnes avec suivi au niveau des mots-clés uniquement ; facultatif) URL de la page de destination vers laquelle les utilisateurs sont redirigés lorsqu’ils cliquent sur votre annonce. Il peut inclure du code de redirection et de suivi tiers. Si vous saisissez une valeur, elle remplace l’URL de base de la publicité.

Une fois l’enregistrement enregistré, l’URL de base inclut tous les paramètres d’ajout configurés pour la campagne ou le compte.

Si vous utilisez le service de suivi des conversions Adobe Advertising et que les paramètres de la campagne incluent l’utilisation du [!UICONTROL EF Redirect] et l’ajout du suivi au niveau du mot-clé, Search, Social et Commerce ajoute automatiquement son propre code de suivi des clics.

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](keyword-manage.md)
