---
title: "[!DNL Google Ads] paramètres de mots-clés"
description: Référencez les paramètres pour [!DNL Google Ads] mots-clés.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# [!DNL Google Ads] paramètres de mots-clés

Vous pouvez créer des mots-clés pour les campagnes qui utilisent les réseaux de recherche et d’affichage.

Voir l’aide de Google Ads pour [limites de mots-clés par compte](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Les mots-clés, y compris les [!DNL Google Ads] syntaxe correspondante pour les mots-clés et les espaces réservés. [!DNL Google Ads] Les comptes requièrent des mots-clés avec les attributs suivants :

* La longueur maximale par mot-clé est de 80 caractères et ne peut pas dépasser 10 mots.
* Le mot-clé ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : space `# $ & _ - " [] ' + . / :`

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Vous pouvez créer des mots-clés négatifs à partir du [!UICONTROL Keywords] > [!UICONTROL Negatives] afficher et dans les paramètres du groupe publicitaire et de la campagne.
>* Modification d’un [!DNL Google Ads] Le mot-clé ou le type de correspondance supprime le mot-clé existant et en crée un nouveau.


**[!UICONTROL Status]:** L’état d’affichage du mot-clé : *Principal* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Principal*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param1]:** Chaîne à utiliser comme valeur de substitution si l’URL de base ou le modèle de suivi contient [la valeur `{param1}`](https://support.google.com/google-ads/answer/6305348) chaîne de substitution dynamique.

**[!UICONTROL Param2]:** Chaîne à utiliser comme valeur de substitution si l’URL de base ou le modèle de suivi contient [la valeur `{param2}`](https://support.google.com/google-ads/answer/6305348) chaîne de substitution dynamique.

## Options d’URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Gestion des mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)

