---
title: Paramètres des mots-clés '[!DNL Microsoft Advertising]'
description: Référencez les paramètres de  [!DNL Microsoft Advertising] mots-clés.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] paramètres de mot-clé

Vous pouvez créer des mots-clés pour les campagnes qui utilisent les réseaux de recherche et d’affichage.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Les mots-clés, y compris toute syntaxe de correspondance [!DNL Microsoft Advertising] et les espaces réservés. La longueur maximale par mot-clé est de 100 caractères.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Vous pouvez créer des mots-clés négatifs à partir de la vue [!UICONTROL Keywords] > [!UICONTROL Negatives] et dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d&#39;un mot-clé [!DNL Microsoft Advertising] supprime le mot-clé existant et en crée un nouveau avec un nouvel identifiant de mot-clé. Toutefois, le fait de modifier le type de correspondance ne supprime pas le mot-clé existant.

**[!UICONTROL Status]:** État d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param2]:** Chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de la publicité contient [ la `{Param2}` chaîne de substitution dynamique](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments de publicité dans lesquels vous l’utilisez (par exemple, le titre 1 et le titre 2 combinés peuvent contenir un maximum de 76 caractères).

**[!UICONTROL Param3]:** Chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de la publicité contient [ la `{Param3}` chaîne de substitution dynamique](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments de publicité dans lesquels vous l’utilisez (par exemple, le titre 1 et le titre 2 combinés peuvent contenir un maximum de 76 caractères).

## Options d’URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Ce champ peut éventuellement inclure les variables de substitution dynamique `{Param2}` et `{Param3}`.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
