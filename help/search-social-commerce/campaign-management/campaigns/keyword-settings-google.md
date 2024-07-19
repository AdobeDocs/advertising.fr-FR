---
title: Paramètres des mots-clés '[!DNL Google Ads]'
description: Référencez les paramètres de  [!DNL Google Ads] mots-clés.
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# [!DNL Google Ads] paramètres de mot-clé

Vous pouvez créer des mots-clés pour les campagnes qui utilisent les réseaux de recherche et d’affichage.

Consultez l’ aide de Google Ads pour obtenir les [limites de mots-clés par compte](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Les mots-clés, y compris toute [!DNL Google Ads] syntaxe de correspondance pour les mots-clés et les espaces réservés. Les comptes [!DNL Google Ads] requièrent des mots-clés avec les attributs suivants :

* La longueur maximale par mot-clé est de 80 caractères et ne peut pas dépasser 10 mots.
* Le mot-clé ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : espace `# $ & _ - " [] ' + . / :`

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Vous pouvez créer des mots-clés négatifs à partir de la vue [!UICONTROL Keywords] > [!UICONTROL Negatives] et dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d’un mot-clé ou d’un type de correspondance [!DNL Google Ads] supprime le mot-clé existant et en crée un nouveau.

**[!UICONTROL Status]:** État d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param1]:** Chaîne à utiliser comme valeur de substitution si l’URL de base ou le modèle de suivi contient [ la chaîne de substitution dynamique `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** Chaîne à utiliser comme valeur de substitution si l’URL de base ou le modèle de suivi contient [ la chaîne de substitution dynamique `{param2}`](https://support.google.com/google-ads/answer/6305348).

## Options d’URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
