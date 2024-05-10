---
title: '''[!DNL Microsoft Advertising] paramètres de mots-clés'
description: Référencez les paramètres pour [!DNL Microsoft Advertising] mots-clés.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] paramètres de mots-clés

Vous pouvez créer des mots-clés pour les campagnes qui utilisent les réseaux de recherche et d’affichage.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Les mots-clés, y compris les [!DNL Microsoft Advertising] syntaxe correspondante et espaces réservés. La longueur maximale par mot-clé est de 100 caractères.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Vous pouvez créer des mots-clés négatifs à partir de la variable [!UICONTROL Keywords] > [!UICONTROL Negatives] afficher et dans les paramètres du groupe publicitaire et de la campagne.
>* Modification d’un [!DNL Microsoft Advertising] Le mot-clé supprime le mot-clé existant et en crée un nouveau avec un nouvel identifiant de mot-clé. Toutefois, le fait de modifier le type de correspondance ne supprime pas le mot-clé existant.

**[!UICONTROL Status]:** L’état d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Actif*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param2]:** Chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de la publicité contient [la valeur `{Param2}` chaîne de substitution dynamique](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments de publicité dans lesquels vous l’utilisez (par exemple, le titre 1 et le titre 2 combinés peuvent contenir un maximum de 76 caractères).

**[!UICONTROL Param3]:** Chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de la publicité contient [la valeur `{Param3}` chaîne de substitution dynamique](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments de publicité dans lesquels vous l’utilisez (par exemple, le titre 1 et le titre 2 combinés peuvent contenir un maximum de 76 caractères).

## Options d’URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Ce champ peut éventuellement inclure la variable `{Param2}` et `{Param3}` variables de substitution dynamiques.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gestion des mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
