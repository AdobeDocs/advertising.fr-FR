---
title: Paramètres du groupe de produits '[!DNL Microsoft Advertising]'
description: Référencez les paramètres pour les groupes de produits  [!DNL Microsoft Advertising] shopping .
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] paramètres du groupe de produits

## Groupes de produits &quot;Tous produits&quot;

**[!UICONTROL Condition]:** (Lecture seule) Tous les produits

**[!UICONTROL Bid]:** (groupes de produits inclus uniquement) Coût par clic maximum (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants, et elle est utilisée à la place de la valeur au niveau du groupe d’annonces.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Ce modèle remplace les modèles à des niveaux supérieurs et n’est utilisé que pour les unités sans groupes de produits enfants.

## Tous les autres groupes de produits

**[!UICONTROL Condition/Value]:** (Lecture seule pour les groupes de produits existants) Dimensions de produit à cibler. Pour les nouveaux groupes de produits, saisissez la dimension par laquelle cibler les produits et l’attribut qualifiant pour la catégorie d’informations sélectionnée (par exemple &quot;Acme&quot; lorsque vous effectuez un ciblage par marque ou &quot;Nouveau&quot; lorsque vous effectuez un ciblage par condition).

Une fois que vous avez créé un groupe de produits pour des dimensions de produit spécifiques (c’est-à-dire pas &quot;Tous les produits&quot;), Search, Social &amp; Commerce crée automatiquement un groupe de produits pour &quot;Tout le reste&quot;.

Pour obtenir la liste des dimensions de produit disponibles, voir &quot;[Shopping campaign product filters](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;. Votre liste de dimensions peut être limitée en fonction du paramètre [!UICONTROL Inventory Filter] de la campagne.

**[!UICONTROL Excluded]:** (facultatif pour les nouveaux groupes de produits ; en lecture seule pour les groupes de produits existants) Exclut les offres sur les publicités pour les produits correspondants.

**[!UICONTROL Bid]:** (groupes de produits inclus uniquement) Coût par clic maximum (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants, et elle est utilisée à la place de la valeur au niveau du groupe d’annonces.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Ce modèle remplace les modèles à des niveaux supérieurs et n’est utilisé que pour les unités sans groupes de produits enfants.

>[!MORELIKETHIS]
>
>* [À propos des groupes de produits d’achats](product-group-about.md)
>* [Gérer les groupes de produits d&#39;achats](product-group-manage.md)
>* [Filtres de produits de campagne de shopping](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implémentation [!DNL Microsoft Advertising] campagnes d’achat](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
