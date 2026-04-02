---
title: '[!DNL Google Ads] des paramètres de groupe de produits'
description: Référencez les paramètres des groupes  [!DNL Google Ads]  produits d’achat.
exl-id: 2cfef9de-b265-4fa5-b1bd-84e6cba79914
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/TkiKzm1sNZZdcu1ghpySElcQb7OIjnNZVqsVqzrK2uE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 270
ht-degree: 0%

---

# [!DNL Google Ads] des paramètres de groupe de produits

## Groupes de produits « Tous les produits »

**[!UICONTROL Condition]:** (Lecture seule) Tous les produits

**[!UICONTROL Bid]:** (groupes de produits inclus uniquement) Coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants et elle est utilisée à la place de la valeur au niveau du groupe publicitaire.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

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

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Ce modèle remplace les modèles aux niveaux supérieurs et est utilisé uniquement pour les unités sans groupes de produits enfants.

>[!MORELIKETHIS]
>
>* [À propos des groupes de produits d’achat](product-group-about.md)
>* [Gérer les groupes de produits d’achat](product-group-manage.md)
>* [Filtres de produits de campagne Shopping](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implémenter [!DNL Google Ads] des campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
