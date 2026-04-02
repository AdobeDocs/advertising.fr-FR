---
title: Paramètres des mots-clés [!DNL Yandex]
description: Référencez les paramètres des mots [!DNL Yandex] clés.
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/-PRiQ9myH0XNYF8pc2OVBuLOK-8BpxzqruOP2hzPW0I
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# Paramètres des mots-clés [!DNL Yandex]

Les mots-clés Yandex sont utilisés pour les réseaux de recherche et d&#39;affichage (de contenu).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** les expressions de mot-clé, y compris toute syntaxe [type de correspondance Yandex](https://yandex.com/support/direct/keywords/symbols-and-operators.html) pour les mots-clés. Chaque mot-clé peut comporter un maximum de sept mots, à l’exclusion des mots vides.

Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

>[!NOTE]
>
>* La modification d’un [!DNL Yandex] mot-clé ou d’un type de correspondance supprime le mot-clé existant et en crée un nouveau.
>* Chaque groupe publicitaire Yandex peut inclure un maximum de 200 mots-clés.

**[!UICONTROL Status]:** statut d’affichage du mot-clé : *Actif* ou *En pause*. La valeur par défaut des nouveaux mots-clés est *Actif*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Espaces réservés

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** valeur des variables de substitution `{param1}` et `{param2}`, qui sont remplacées par toutes les instances de {param1} et {param2} dans l’URL de base pour les publicités et les liens de site lorsque le mot-clé est utilisé pour afficher la publicité. La longueur maximale est de 255 octets.

Les caractères spéciaux sont automatiquement codés au format UTF-8. Par exemple, si l’adresse URL de base de l’annonce publicitaire associée est « http://www.example.com/ {param1} et que la valeur au niveau du mot-clé de {param1} est « shoes/flats.html », l’annonce publicitaire mène à http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Gérer les mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
