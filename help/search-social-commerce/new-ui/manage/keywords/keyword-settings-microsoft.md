---
title: Paramètres des mots-clés [!DNL Microsoft Advertising]
description: Référencez les paramètres des mots-clés [!DNL Microsoft Advertising].
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
source-wordcount: '281'
ht-degree: 0%
---
# Paramètres des mots-clés [!DNL Microsoft Advertising]

Vous pouvez créer des mots-clés pour les campagnes qui utilisent les réseaux de recherche et d’affichage.

## [!UICONTROL Basic Settings]

*Nouveaux mots-clés uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte de réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne.

**[!UICONTROL Ad Group]:** groupe publicitaire .

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** mots-clés, y compris la syntaxe de correspondance [!DNL Microsoft Advertising] et les espaces réservés. La longueur maximale par mot-clé est de 100 caractères.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Vous pouvez créer des mots-clés négatifs à partir de l’onglet [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] , ainsi que dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d’un mot-clé [!DNL Microsoft Advertising] supprime le mot-clé existant et en crée un nouveau avec un nouvel ID de mot-clé. Toutefois, la modification du type de correspondance ne supprime pas le mot-clé existant.

**[!UICONTROL Status]:** statut d’affichage du mot-clé : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. La valeur par défaut des nouveaux mots-clés est *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de l’annonce publicitaire contient [la `{Param1}` chaîne de substitution dynamique](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments publicitaires dans lesquels vous l’utilisez (par exemple, les titres 1 et 2 combinés peuvent contenir un maximum de 76 caractères).

**[!UICONTROL Param2]:** chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de l’annonce publicitaire contient [la `{Param2}` chaîne de substitution dynamique](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments publicitaires dans lesquels vous l’utilisez (par exemple, les titres 1 et 2 combinés peuvent contenir un maximum de 76 caractères).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Ce champ peut éventuellement inclure les variables de substitution dynamiques `{Param1}` et `{Param2}`.

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](keyword-manage.md)
