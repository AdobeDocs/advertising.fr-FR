---
title: "[!DNL Microsoft® Advertising] paramètres du groupe de produits"
description: Référencez les paramètres pour [!DNL Microsoft® Advertising] des groupes de produits d’achat.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] paramètres du groupe de produits

## Groupes de produits &quot;Tous produits&quot;

**[!UICONTROL Condition]:** (Lecture seule) Tous les produits

**[!UICONTROL Bid]:** (Groupes de produits inclus uniquement) Coût par clic maximum, qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants, et elle est utilisée à la place de la valeur au niveau du groupe d’annonces.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Ce modèle remplace les modèles à des niveaux supérieurs et n’est utilisé que pour les unités sans groupes de produits enfants.

## Tous les autres groupes de produits

**[!UICONTROL Condition/Value]:** (Lecture seule pour les groupes de produits existants) Dimensions de produit à cibler. Pour les nouveaux groupes de produits, saisissez la dimension par laquelle cibler les produits et l’attribut qualifiant pour la catégorie d’informations sélectionnée (par exemple &quot;Acme&quot; lorsque vous effectuez un ciblage par marque ou &quot;Nouveau&quot; lorsque vous effectuez un ciblage par condition).

Une fois que vous avez créé un groupe de produits pour des dimensions de produit spécifiques (c’est-à-dire pas &quot;Tous les produits&quot;), Search, Social &amp; Commerce crée automatiquement un groupe de produits pour &quot;Tout le reste&quot;.

Pour obtenir la liste des dimensions de produit disponibles, voir &quot;[Filtres de produits de campagne d&#39;achat](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; Votre liste de dimensions peut être limitée en fonction de la variable [!UICONTROL Inventory Filter] .

**[!UICONTROL Excluded]:** (Facultatif pour les nouveaux groupes de produits ; lecture seule pour les groupes de produits existants) Exclut les offres sur les publicités pour les produits correspondants.

**[!UICONTROL Bid]:** (Groupes de produits inclus uniquement) Coût par clic maximum, qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants, et elle est utilisée à la place de la valeur au niveau du groupe d’annonces.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Ce modèle remplace les modèles à des niveaux supérieurs et n’est utilisé que pour les unités sans groupes de produits enfants.

>[!MORELIKETHIS]
>
>* [À propos des groupes de produits d’achat](product-group-about.md)
>* [Gestion des groupes de produits](product-group-manage.md)
>* [Filtres de produits de campagne d&#39;achat](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Mise en oeuvre [!DNL Microsoft® Advertising] campagnes d&#39;achat](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)

