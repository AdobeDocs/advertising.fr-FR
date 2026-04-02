---
title: Paramètres des mots-clés [!DNL Baidu]
description: Référencez les paramètres des mots [!DNL Baidu] clés.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/uMU0oAkL8rmsOIMXYR8qgp9-upe2qWIK-ev1YtPQUb4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 0%

---

# Paramètres des mots-clés [!DNL Baidu]

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Les mots-clés La longueur maximale par mot-clé est de 30 caractères codés sur un octet ou 15 caractères codés sur deux octets

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes. Utilisez la syntaxe suivante :

* `keyword` pour une large correspondance
* `"keyword"` pour la correspondance d’expressions
* `[keyword]` pour une correspondance exacte

>[!NOTE]
>
>* [!DNL Baidu] n’autorise qu’un seul type de correspondance par mot-clé par groupe publicitaire. Par exemple, le groupe publicitaire 1 ne peut pas inclure à la fois `"keyword"` et `[keyword]`.
>* Vous pouvez créer des mots-clés négatifs à partir de la vue [!UICONTROL Keywords] > [!UICONTROL Negatives] et dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d’un mot-clé [!DNL Baidu] supprime le mot-clé existant et en crée un nouveau avec un nouvel ID de mot-clé. Toutefois, la modification du type de correspondance ne supprime pas le mot-clé existant.

**[!UICONTROL Status]:** statut d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Actif*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Options d’URL

**[!UICONTROL Base URL]:** (campagnes avec suivi au niveau des mots-clés uniquement ; facultatif) URL de la page de destination vers laquelle les utilisateurs sont redirigés lorsqu’ils cliquent sur votre annonce. Il peut inclure :
code de redirection et de suivi tiers. Si vous saisissez une valeur, elle remplace l’URL de base de la publicité.

Une fois l’enregistrement enregistré, l’URL de base inclut tous les paramètres d’ajout configurés pour la campagne ou le compte.

Si vous utilisez le service de suivi des conversions Adobe Advertising et que les paramètres de la campagne incluent l’utilisation du [!UICONTROL EF Redirect] et l’ajout du suivi au niveau du mot-clé, Search, Social et Commerce ajoute automatiquement son propre code de suivi des clics.

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
