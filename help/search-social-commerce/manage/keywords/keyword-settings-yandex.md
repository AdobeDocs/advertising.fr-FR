---
title: '[!DNL Yandex] paramètres de mot-clé'
description: Référencez les paramètres pour [!DNL Yandex] mots-clés.
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
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%
---
# [!DNL Yandex] paramètres de mot-clé

[!DNL Yandex] mots-clés sont utilisés pour les réseaux de recherche et d’affichage (de contenu).

## [!UICONTROL Basic Settings]

*Nouveaux mots-clés uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne.

**[!UICONTROL Ad Group]:** Le groupe publicitaire.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** les expressions de mot-clé, y compris toute syntaxe de type [[!DNL Yandex] match](https://yandex.com/support/direct/keywords/symbols-and-operators.html) pour les mots-clés. Chaque mot-clé peut comporter un maximum de sept mots, à l’exclusion des mots vides.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* La modification d&#39;un mot-clé [!DNL Yandex] ou d&#39;un type de correspondance supprime le mot-clé existant et en crée un nouveau.
>* Chaque groupe publicitaire [!DNL Yandex] peut inclure un maximum de 200 mots-clés.

**[!UICONTROL Status]:** Statut d&#39;affichage du mot-clé : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. La valeur par défaut pour les nouveaux mots-clés est *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>Les caractères spéciaux sont automatiquement codés au format UTF-8. Par exemple, si l’annonce publicitaire associée a une URL de base de `http://www.example.com/{param1}` et que la valeur au niveau du mot-clé `{param1}` est `shoes/flats.html`, l’annonce publicitaire mène à `http://www.example.com/shoes%2Fflats.html`.

**[!UICONTROL Param1]:** La chaîne à utiliser comme valeur de substitution si l’URL de base contient la chaîne de substitution dynamique `{param1}` pour les publicités et les liens de site lorsque le mot-clé est utilisé pour afficher la publicité. La longueur maximale est de 255 octets.

**[!UICONTROL Param2]:** La chaîne à utiliser comme valeur de substitution si l’URL de base contient la chaîne de substitution dynamique `{param2}` pour les publicités et les liens de site lorsque le mot-clé est utilisé pour afficher la publicité. La longueur maximale est de 255 octets.

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](keyword-manage.md)
