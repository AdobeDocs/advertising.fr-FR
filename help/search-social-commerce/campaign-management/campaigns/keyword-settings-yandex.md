---
title: Paramètres des mots-clés '[!DNL Yandex]'
description: Référencez les paramètres de  [!DNL Yandex] mots-clés.
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# [!DNL Yandex] paramètres de mot-clé

Les mots-clés Yandex sont utilisés pour les réseaux de recherche et d’affichage (contenu).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Les expressions-clés, y compris toute [syntaxe de type correspondance Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) pour les mots-clés. Chaque mot-clé peut contenir, au maximum, sept mots, à l’exception des mots-clés &quot;stop&quot;.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* La modification d’un mot-clé ou d’un type de correspondance [!DNL Yandex] supprime le mot-clé existant et en crée un nouveau.
>* Chaque groupe d’annonces Yandex peut contenir, au maximum, 200 mots-clés.

**[!UICONTROL Status]:** État d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** La valeur des variables de substitution `{param1}` et `{param2}`, qui sont remplacées par toutes les instances de {param1} et {param2} dans l’URL de base pour les publicités et les liens de site lorsque le mot-clé est utilisé pour afficher la publicité. La longueur maximale est de 255 octets.

Les caractères spéciaux sont automatiquement encodés en UTF-8. Par exemple, si la publicité associée a une URL de base de &quot;http://www.example.com/{param1}&quot; et que la valeur de niveau mot-clé {param1} est &quot;shoes/flats.html&quot;, la publicité dirige vers http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
