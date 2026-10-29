---
title: Paramètres des mots-clés [!DNL Google Ads]
description: Référencez les paramètres des mots-clés [!DNL Google Ads].
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%
---
# Paramètres des mots-clés [!DNL Google Ads]

Vous pouvez créer des mots-clés pour les campagnes qui utilisent les réseaux de recherche et d’affichage.

Voir l’aide [!DNL Google Ads] pour connaître les [limites de mots-clés par compte](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Basic Settings]

*Nouveaux mots-clés uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte de réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne.

**[!UICONTROL Ad Group]:** groupe publicitaire .

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** les mots-clés, y compris toute syntaxe de correspondance [!DNL Google Ads] pour les mots-clés et les espaces réservés. Les comptes [!DNL Google Ads] nécessitent des mots-clés avec les attributs suivants :

* La longueur maximale par mot-clé est de 80 caractères et de 10 mots au maximum.

* Le mot-clé ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : espace `# $ & _ - " [] ' + . / :`

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Vous pouvez créer des mots-clés négatifs à partir de l’onglet [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] , ainsi que dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d’un [!DNL Google Ads] mot-clé ou d’un type de correspondance supprime le mot-clé existant et en crée un nouveau.

**[!UICONTROL Status]:** statut d’affichage du mot-clé : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. La valeur par défaut des nouveaux mots-clés est *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** chaîne à utiliser comme valeur de substitution si l’URL de base ou le modèle de suivi contient [ la chaîne de substitution dynamique `{param1}`](https://support.google.com/google-ads/answer/6305348).

**[!UICONTROL Param2]:** chaîne à utiliser comme valeur de substitution si l’URL de base ou le modèle de suivi contient [ la chaîne de substitution dynamique `{param2}`](https://support.google.com/google-ads/answer/6305348).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](keyword-manage.md)
