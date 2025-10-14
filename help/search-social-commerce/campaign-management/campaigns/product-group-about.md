---
title: À propos des groupes de produits d’achat
description: Découvrez les groupes de produits d’achat dans les campagnes d’achat.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# À propos des groupes de produits d’achat

*[!DNL Google Ads]et [!DNL Microsoft Advertising] des campagnes d’achat uniquement*

Dans les campagnes d’achats, vos groupes de produits (et non les mots-clés) déterminent les produits de votre compte de centre commercial pour lesquels des annonces d’achats sont affichées. Chaque groupe de produits est basé sur un attribut de produit unique (tel que la catégorie, le type de produit, la marque, la condition, l’ID de produit ou les libellés personnalisés) et utilise la même enchère pour tous les produits correspondants. Vous pouvez inclure ou exclure des offres pour les produits de chaque groupe.

Vous configurez des groupes de produits au niveau du groupe publicitaire afin de déterminer les produits de vos comptes de centre commercial qui apparaissent dans les annonces d’achat pour le groupe publicitaire. Même si le groupe publicitaire ne comprend pas d’entités publicitaires, le réseau publicitaire affiche toujours des annonces pour les produits.

Lorsque le même produit est inclus dans plusieurs campagnes, le réseau publicitaire commence par utiliser la priorité de campagne pour déterminer la campagne (et l’enchère associée) éligible pour les enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, la campagne ayant la meilleure enchère est éligible.

Pour plus d’informations sur les campagnes d’achats et les publicités [!DNL Google], consultez « [Implémenter [!DNL Google Ads] des campagnes d’achats](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md) » et la [documentation sur les publicités Google](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Pour plus d’informations sur les campagnes d’achats [!DNL Microsoft], consultez « [Implémenter [!DNL Microsoft Advertising] des campagnes d’achats](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md) » et la [[!DNL Microsoft Advertising] documentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>La prise en charge n’est pas disponible pour les groupes de listes [!DNL Google Ads] dans les campagnes Performance Max, qui remplacent les campagnes d’achats intelligents. Pour gérer et afficher des données pour les groupes de listes, utilisez l’éditeur de [!DNL Google Ads].

## Hiérarchie des groupes de produits

Avant de pouvoir créer des groupes de produits avec des attributs spécifiques pour un groupe publicitaire, vous devez d’abord créer un groupe de produits complet appelé « [!UICONTROL All Products] ». À partir de ce groupe de produits parent, vous pouvez créer des groupes de produits enfants pour des sous-ensembles de produits, ainsi que des petits-enfants à partir des groupes de produits enfants. Une fois que vous avez créé le premier groupe de produits enfant pour un groupe publicitaire, un autre groupe de produits appelé « [!UICONTROL Everything Else] » est automatiquement créé à l’aide de l’enchère du groupe publicitaire par défaut. À mesure que vous ajoutez d’autres groupes de produits, le groupe « [!UICONTROL Everything Else] » est ajusté en conséquence afin qu’il constitue tous les produits qui ne font pas partie d’un autre groupe de produits.

Au sein d’un groupe publicitaire, vous pouvez créer jusqu’à sept niveaux de groupes de produits (sans inclure « [!UICONTROL All Products] ») à inclure ou à exclure des offres, avec un ou plusieurs groupes de produits ciblant le même attribut à chaque niveau (par exemple, [!UICONTROL Brand]=Acme pour un groupe de produits et [!UICONTROL Brand]=AcmePlus pour un autre au même niveau). Les groupes de produits parents sont appelés subdivisions et le niveau de subdivision le plus bas est appelé unité. Vous pouvez définir des offres et des modèles de suivi, ou exclure complètement les offres, au niveau de l’unité. L’ensemble complet des groupes de produits actifs pour un groupe publicitaire est appliqué de manière hiérarchique afin de déterminer les produits éligibles. Par exemple, si vous subdivisez [!UICONTROL All Products] en [!UICONTROL Brand]=AcmeBasic et [!UICONTROL Brand]=AcmePlus, puis que vous subdivisez davantage chacun de ces groupes de produits en [!UICONTROL Condition]=Nouveau et définissez des enchères, seuls les nouveaux produits des marques AcmeBasic et AcmePlus peuvent faire l’objet d’une publicité ou être exclus des publicités.

![Exemple d’ensemble de groupes &#x200B;](/help/search-social-commerce/assets/product-group-list.png " produitsExemple d’ensemble de groupes de produits")

![Exemple de hiérarchie de groupe de produits](/help/search-social-commerce/assets/product-group-tree.png "Exemple de hiérarchie de groupe de produits")

## La vue [!UICONTROL Product Groups]

Vous pouvez créer et modifier des groupes de produits et supprimer des groupes de produits et leurs groupes de produits enfants dans la vue [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] .

## Données de suivi et de performance pour les groupes de produits d’achat

(Comptes/campagnes avec l’option de suivi « [!UICONTROL EF Redirect] ») Pour permettre à Search, Social et Commerce de suivre les conversions des groupes de produits, [générez des URL de suivi pour les groupes de produits à l’aide de l’outil URL de suivi](/help/search-social-commerce/tools/click-tracking-url-generate.md), puis effectuez l’une des opérations suivantes :

* (Obligatoire pour les [!DNL Google Ads] ; bonne pratique pour les [!DNL Microsoft Advertising]) Ajoutez l’URL de tracking au champ [!DNL Tracking Template] dans le paramètre du compte, de la campagne ou du groupe de produits. Pour faciliter la maintenance, ajoutez-les au niveau le plus élevé possible. Les paramètres d’ajout spécifiés pour le compte ou la campagne ne sont pas inclus.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Utilisez cette option uniquement lorsque vous n’incluez pas les URL de suivi Search, Social et Commerce dans une colonne personnalisée du flux de produits. Si vous effectuez les deux, les URL incluront deux redirections et provoqueront des liens rompus.

* ([!DNL Microsoft Advertising] uniquement) Ajoutez l’URL de suivi aux données de produit dans le compte [!DNL Microsoft Merchant Center]. Pour ce faire, incluez l’URL de suivi, ainsi que la valeur dans le champ `link` ou `mobile_link`, selon le cas, dans une colonne personnalisée appelée [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) dans le flux de produits. Les URL générées à l’aide de cette méthode n’incluent aucun paramètre de tracking spécifié dans les paramètres du compte ou de la campagne dans Search, Social et Commerce.

Vous pouvez afficher des données sur les groupes de produits dans [le [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Gérer les groupes de produits d’achat](product-group-manage.md)
>* [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md)
>* [Implémenter [!DNL Google Ads] des campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] paramètres du groupe de produits](product-group-settings-microsoft.md)
>* [Implémenter [!DNL Microsoft Advertising] des campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
