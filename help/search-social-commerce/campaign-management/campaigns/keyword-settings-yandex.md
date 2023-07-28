---
title: '''[!DNL Yandex] paramètres de mots-clés'
description: Référencez les paramètres pour [!DNL Yandex] mots-clés.
exl-id: 276f991b-f604-445c-8dd0-481b6eaee3d2
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] paramètres de mots-clés

Les mots-clés Yandex sont utilisés pour les réseaux de recherche et d’affichage (contenu).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** Les expressions de mots-clés, y compris les [Syntaxe du type de correspondance Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) pour les mots-clés. Chaque mot-clé peut contenir, au maximum, sept mots, à l’exception des mots-clés &quot;stop&quot;.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* Modification d’un [!DNL Yandex] Le mot-clé ou le type de correspondance supprime le mot-clé existant et en crée un nouveau.
>* Chaque groupe d’annonces Yandex peut contenir, au maximum, 200 mots-clés.

**[!UICONTROL Status]:** L’état d’affichage du mot-clé : *Principal* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Principal*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** La valeur de la variable `{param1}` et `{param2}` les variables de substitution qui remplacent toutes les instances de {param1} et {param2} dans l’URL de base des publicités et des liens de site lorsque le mot-clé est utilisé pour afficher la publicité. La longueur maximale est de 255 octets.

Les caractères spéciaux sont automatiquement encodés en UTF-8. Par exemple, si la publicité associée a une URL de base de &quot;http://www.example.com/&quot;{param1} et la valeur au niveau du mot-clé de {param1} est &quot;shoes/flats.html&quot;, puis la publicité mène à http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Gestion des mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
