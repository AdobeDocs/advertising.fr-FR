---
title: Gestion des modificateurs
description: Découvrez comment configurer et gérer des modificateurs pour vos modèles d’annonces publicitaires pour les flux de données d’inventaire.
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Gestion des modificateurs

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Les modificateurs sont des adjectifs ou des adverbes qui peuvent être ajoutés ou supprimés d’une phrase sans modifier la structure de la phrase de base. Vous pouvez créer des groupes de modificateurs à utiliser comme variables dans divers champs de données de modèles de données de flux. En incluant des modificateurs dans les champs de structure de compte (campagne et groupe publicitaire), les mots-clés, les URL de base et les publicités, vous créez une valeur pour chaque valeur de modificateur associée. Par exemple, si vous utilisez une variable de groupe de conditions commerciales dans un titre d&#39;annonce et que le groupe de conditions commerciales comprend trois conditions commerciales (« bon marché », « réduction » et « abordable »), trois annonces distinctes sont créées pour chaque ligne de données du flux de données, une pour chaque condition commerciale. De même, si vous incluez un groupe de modificateurs avec plusieurs valeurs dans l’URL de base d’un groupe publicitaire, un ensemble de mots-clés est créé pour chacune des URL de base résultantes.

Chaque groupe de modificateurs peut inclure autant de modificateurs que vous le souhaitez. Chaque modèle ne peut utiliser qu&#39;un seul groupe de conditions commerciales.

## Créer un groupe de conditions commerciales

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Modifiers]**.

1. Au-dessus de la liste des groupes de modificateurs, cliquez sur **[!UICONTROL Create]**.

1. Spécifiez les paramètres du groupe de modificateurs :

   **[!UICONTROL Name]:** Nom du groupe de conditions commerciales.

   **[!UICONTROL Modifiers]:** valeurs des conditions commerciales pour le groupe (une par ligne).

1. Cliquez sur **[!UICONTROL Save]**.

## Modifier un groupe de conditions commerciales

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Modifiers]**.

1. Dans la liste des groupes de conditions commerciales, cliquez sur leur nom.

1. Modifiez les paramètres du groupe de modificateurs :

   **[!UICONTROL Name]:** Nom du groupe de conditions commerciales.

   **[!UICONTROL Modifiers]:** valeurs des conditions commerciales pour le groupe (une par ligne).

1. Cliquez sur **[!UICONTROL Save]**.

## Supprimer groupes de conditions commerciales

>[!IMPORTANT]
>
>Lorsque vous supprimez un groupe de conditions commerciales, supprimez toutes les variables de ce groupe de conditions commerciales (désignées sous le nom de `<modifier_group_name>`) dans les champs des modèles existants. Si vous essayez de propager des données par le biais d’un modèle à l’aide de variables pour des modificateurs qui n’existent pas, la tâche échoue1.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Modifiers]**.

1. Cochez la case en regard de chaque groupe de conditions commerciales à supprimer.

1. Au-dessus de la liste des groupes de modificateurs, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]**.

1. (Si nécessaire) [Supprimez les références au modificateur](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) de tous les modèles applicables.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Gérer les modèles publicitaires](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
