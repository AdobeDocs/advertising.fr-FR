---
title: Paramètres des mots-clés [!DNL Google Ads]
description: Référencez les paramètres des mots [!DNL Google Ads] clés.
exl-id: b2937d18-565a-43f0-ba33-d46d4c77ec07
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/XwutnbHVQrg8mfimzVjv-Px6OeUsOWzT7-347-ff2C0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 0%

---

# Paramètres des mots-clés [!DNL Google Ads]

Vous pouvez créer des mots-clés pour les campagnes qui utilisent les réseaux de recherche et d’affichage.

Consultez l’aide de Google Ads pour connaître les [limites de mots-clés par compte](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** les mots-clés, y compris toute syntaxe de correspondance [!DNL Google Ads] pour les mots-clés et les espaces réservés. Les comptes [!DNL Google Ads] nécessitent des mots-clés avec les attributs suivants :

* La longueur maximale par mot-clé est de 80 caractères et de 10 mots au maximum.
* Le mot-clé ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : espace `# $ & _ - " [] ' + . / :`

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Vous pouvez créer des mots-clés négatifs à partir de la vue [!UICONTROL Keywords] > [!UICONTROL Negatives] et dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d’un [!DNL Google Ads] mot-clé ou d’un type de correspondance supprime le mot-clé existant et en crée un nouveau.

**[!UICONTROL Status]:** statut d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Actif*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param1]:** chaîne à utiliser comme valeur de substitution si l’URL de base ou le modèle de suivi contient [ la chaîne de substitution dynamique `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** chaîne à utiliser comme valeur de substitution si l’URL de base ou le modèle de suivi contient [ la chaîne de substitution dynamique `{param2}`](https://support.google.com/google-ads/answer/6305348).

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
