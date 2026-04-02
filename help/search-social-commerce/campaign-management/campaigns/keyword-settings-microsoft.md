---
title: Paramètres des mots-clés [!DNL Microsoft Advertising]
description: Référencez les paramètres des mots [!DNL Microsoft Advertising] clés.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/fA0ZDCw5Ici0wOfpd1kXdjbQA6DtUFxOSBEtrlJl4Oo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# Paramètres des mots-clés [!DNL Microsoft Advertising]

Vous pouvez créer des mots-clés pour les campagnes qui utilisent les réseaux de recherche et d’affichage.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** mots-clés, y compris la syntaxe de correspondance [!DNL Microsoft Advertising] et les espaces réservés. La longueur maximale par mot-clé est de 100 caractères.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Vous pouvez créer des mots-clés négatifs à partir de la vue [!UICONTROL Keywords] > [!UICONTROL Negatives] et dans les paramètres du groupe publicitaire et de la campagne.
>* La modification d’un mot-clé [!DNL Microsoft Advertising] supprime le mot-clé existant et en crée un nouveau avec un nouvel ID de mot-clé. Toutefois, la modification du type de correspondance ne supprime pas le mot-clé existant.

**[!UICONTROL Status]:** statut d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Actif*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param2]:** chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de l’annonce publicitaire contient [la `{Param2}` chaîne de substitution dynamique](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments publicitaires dans lesquels vous l’utilisez (par exemple, les titres 1 et 2 combinés peuvent contenir un maximum de 76 caractères).

**[!UICONTROL Param3]:** chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de l’annonce publicitaire contient [la `{Param3}` chaîne de substitution dynamique](https://help.bingads.microsoft.com/#apex/3/en/53079/0). La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments publicitaires dans lesquels vous l’utilisez (par exemple, les titres 1 et 2 combinés peuvent contenir un maximum de 76 caractères).

## Options d’URL

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

Ce champ peut éventuellement inclure les variables de substitution dynamiques `{Param2}` et `{Param3}`.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
