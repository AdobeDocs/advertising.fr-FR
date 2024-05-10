---
title: À propos des groupes de produits d’achat
description: Découvrez les groupes de produits d’achats dans les campagnes d’achat.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# À propos des groupes de produits d’achat

*[!DNL Google Ads]et [!DNL Microsoft Advertising] campagnes d&#39;achat uniquement*

Dans les campagnes d’achat, vos groupes de produits — pas les mots-clés — déterminent les produits de votre compte de centre commercial pour lesquels les publicités commerciales sont affichées. Chaque groupe de produits est basé sur un attribut de produit unique (tel que la catégorie, le type de produit, la marque, la condition, l’ID de produit ou des étiquettes personnalisées) et utilise la même offre pour tous les produits correspondants. Vous pouvez inclure ou exclure des offres pour les produits de chaque groupe.

Vous configurez des groupes de produits au niveau du groupe d’annonces afin de déterminer les produits de vos comptes de centre commercial qui apparaissent dans les publicités du groupe d’annonces. Même si le groupe publicitaire n’inclut pas d’entités publicitaires, le réseau publicitaire affiche toujours des publicités pour les produits.

Lorsqu’un même produit est inclus dans plusieurs campagnes, le réseau publicitaire utilise d’abord la priorité de la campagne pour déterminer la campagne (et l’offre associée) éligible aux enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible.

Pour plus d’informations sur [!DNL Google] campagnes d’achat et publicités, voir[Mise en oeuvre [!DNL Google Ads] campagnes d&#39;achat](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; et la variable [Documentation sur Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Pour plus d’informations sur [!DNL Microsoft] campagnes d’achat, voir[Mise en oeuvre [!DNL Microsoft Advertising] campagnes d&#39;achat](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)&quot; et la variable [[!DNL Microsoft Advertising] documentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>L’assistance n’est pas disponible pour [!DNL Google Ads] répertoriant les groupes dans les campagnes de performances max, qui remplacent les campagnes d’achats intelligentes. Pour gérer et afficher les données des groupes de liste, utilisez le [!DNL Google Ads] éditeur.

## Hiérarchie des groupes de produits

Avant de pouvoir créer des groupes de produits avec des attributs spécifiques pour un groupe publicitaire, vous devez créer un groupe de produits tout compris appelé &quot;[!UICONTROL All Products].&quot; À partir de ce groupe de produits parent, vous pouvez créer des groupes de produits enfants pour des sous-ensembles de produits et vous pouvez créer des petits-enfants à partir des groupes de produits enfants. Une fois que vous avez créé le premier groupe de produits enfant pour un groupe publicitaire, un autre groupe de produits appelé &quot;[!UICONTROL Everything Else]&quot; est automatiquement créé à l’aide de l’offre par défaut du groupe publicitaire. Lorsque vous ajoutez d’autres groupes de produits, le[!UICONTROL Everything Else]&quot; est adapté en conséquence afin qu’il constitue tous les produits qui ne font pas partie d’un autre groupe de produits.

Au sein d’un groupe d’annonces, vous pouvez créer jusqu’à sept niveaux de groupes de produits (sans inclure &quot;[!UICONTROL All Products]&quot;) pour inclure ou exclure des offres, avec un ou plusieurs groupes de produits ciblant le même attribut dans chaque niveau (par exemple : [!UICONTROL Brand]=Acme pour un groupe de produits et [!UICONTROL Brand]=AcmePlus pour un autre au même niveau). Les groupes de produits parents sont appelés subdivisions et le niveau le plus bas de subdivisions est connu sous le nom d’unité. Vous pouvez définir des offres et des modèles de suivi, ou exclure complètement l’offre, au niveau de l’unité. L’ensemble des groupes de produits actifs d’un groupe publicitaire est appliqué de manière hiérarchique afin de déterminer les produits éligibles. Par exemple, si vous subdivisez [!UICONTROL All Products] into [!UICONTROL Brand]=AcmeBasic et [!UICONTROL Brand]=AcmePlus, puis vous subdivisez davantage chacun de ces groupes de produits en [!UICONTROL Condition]= Offres nouvelles et définies, seuls les nouveaux produits des marques AcmeBasic et AcmePlus peuvent être annoncés ou exclus des publicités.

![Exemple d’un ensemble de groupes de produits](/help/search-social-commerce/assets/product-group-list.png "Exemple d’un ensemble de groupes de produits")

![Exemple de hiérarchie de groupes de produits](/help/search-social-commerce/assets/product-group-tree.png "Exemple de hiérarchie de groupes de produits")

## La variable [!UICONTROL Product Groups] view

Vous pouvez créer et modifier des groupes de produits, ainsi que supprimer des groupes de produits et leurs groupes de produits enfants, dans la [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] vue.

## Données de suivi et de performances pour les groupes de produits d’achat

(Comptes/campagnes avec le paramètre[!UICONTROL EF Redirect]&quot;option de suivi&quot;) Pour permettre à Search, Social et Commerce de suivre les conversions des groupes de produits, [générer des URL de suivi pour les groupes de produits à l’aide de l’outil URL de suivi ;](/help/search-social-commerce/tools/click-tracking-url-generate.md), puis effectuez l’une des opérations suivantes :

* (Obligatoire pour [!DNL Google Ads]; bonne pratique pour [!DNL Microsoft Advertising]) Ajoutez l’URL de suivi à la variable [!DNL Tracking Template] dans le paramètre du compte, de la campagne ou du groupe de produits. Pour simplifier la maintenance, ajoutez-les au niveau le plus élevé possible. Les paramètres d’ajout spécifiés pour le compte ou la campagne ne sont pas inclus.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Utilisez cette option uniquement si vous n’incluez pas d’URL de suivi Search, Social et Commerce dans une colonne personnalisée du flux de produit. Si vous effectuez les deux, les URL comprennent deux redirections et provoquent des liens rompus.

* ([!DNL Microsoft Advertising] uniquement) Ajoutez l’URL de suivi aux données du produit dans la variable [!DNL Microsoft Merchant Center] compte . Pour ce faire, incluez l’URL de suivi, ainsi que la valeur de la variable `link` ou `mobile_link` le cas échéant, dans une colonne personnalisée appelée [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) dans le flux de produit. Les URL générées à l’aide de cette méthode n’incluent aucun paramètre de suivi spécifié dans les paramètres du compte ou de la campagne dans Search, Social et Commerce.

Vous pouvez afficher des données sur les groupes de produits dans [la valeur [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Gestion des groupes de produits](product-group-manage.md)
>* [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md)
>* [Mise en oeuvre [!DNL Google Ads] campagnes d&#39;achat](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] paramètres du groupe de produits](product-group-settings-microsoft.md)
>* [Mise en oeuvre [!DNL Microsoft Advertising] campagnes d&#39;achat](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
