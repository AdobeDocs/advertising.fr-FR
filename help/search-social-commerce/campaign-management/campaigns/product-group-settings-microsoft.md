---
title: '[!DNL Microsoft Advertising] des paramètres de groupe de produits'
description: Référencez les paramètres des groupes  [!DNL Microsoft Advertising]  produits d’achat.
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] des paramètres de groupe de produits

## Groupes de produits « Tous les produits »

**[!UICONTROL Condition]:** (Lecture seule) Tous les produits

**[!UICONTROL Bid]:** (groupes de produits inclus uniquement) Coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants et elle est utilisée à la place de la valeur au niveau du groupe publicitaire.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Ce modèle remplace les modèles aux niveaux supérieurs et est utilisé uniquement pour les unités sans groupes de produits enfants.

## Tous les autres groupes de produits

**[!UICONTROL Condition/Value]:** (Lecture seule pour les groupes de produits existants) Dimensions de produit à cibler. Pour les nouveaux groupes de produits, saisissez la dimension par laquelle cibler les produits et l’attribut de qualification pour la catégorie d’informations sélectionnée (par exemple, « Acme » lorsque vous ciblez par marque ou « Nouveau » lorsque vous ciblez par condition).

Une fois que vous avez créé un groupe de produits pour des dimensions de produit spécifiques (c’est-à-dire, pas « Tous les produits »), Search, Social et Commerce crée automatiquement un groupe de produits pour « Tout le reste ».

Pour obtenir la liste des dimensions de produit disponibles, voir « [ Filtres de produit de campagne d’achat ](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md) ». Votre liste de dimensions peut être limitée en fonction du paramètre de [!UICONTROL Inventory Filter] de la campagne.

**[!UICONTROL Excluded]:** (facultatif pour les nouveaux groupes de produits ; en lecture seule pour les groupes de produits existants) Exclut les enchères sur les annonces de produits correspondants.

**[!UICONTROL Bid]:** (groupes de produits inclus uniquement) Coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants et elle est utilisée à la place de la valeur au niveau du groupe publicitaire.

<!-- **[!UICONTROL Tracking Template]:** -->

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Ce modèle remplace les modèles aux niveaux supérieurs et est utilisé uniquement pour les unités sans groupes de produits enfants.

>[!MORELIKETHIS]
>
>* [À propos des groupes de produits d’achat](product-group-about.md)
>* [Gérer les groupes de produits d’achat](product-group-manage.md)
>* [Filtres de produits de campagne Shopping](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implémenter [!DNL Microsoft Advertising] des campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
