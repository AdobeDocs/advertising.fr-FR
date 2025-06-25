---
title: Gérer les groupes de produits d’achat
description: Découvrez comment créer et gérer des groupes de produits d’achat dans les campagnes d’achat.
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Gérer les groupes de produits d’achat

*[!DNL Google Ads]et [!DNL Microsoft Advertising] des campagnes d’achat uniquement*

Vous pouvez créer et modifier des groupes de produits et supprimer des groupes de produits et leurs groupes de produits enfants dans la vue [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] .

## Créer un groupe de produits « [!UICONTROL All Products] »

Avant de pouvoir créer des groupes de produits avec des attributs spécifiques, vous devez d’abord créer un groupe de produits complet appelé « [!UICONTROL All Products] ». Chaque groupe publicitaire ne peut avoir qu’un seul groupe « [!UICONTROL All Products] ».

>[!TIP]
>
>Pour créer plusieurs composants de compte à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md) ou [[!DNL Microsoft Advertising] paramètres du groupe de produits](product-group-settings-microsoft.md).

1. Cliquez sur **[!UICONTROL Post]**.

## Créer un nœud de groupe de produits enfant dans un groupe de produits existant

Une fois que vous avez créé au moins un groupe « [!UICONTROL All Products] » tout compris pour un groupe publicitaire, vous pouvez créer des nœuds de groupe de produits enfants pour des sous-ensembles de produits à inclure ou à exclure des enchères, avec un ou plusieurs groupes de produits ciblant le même attribut à chaque niveau (par exemple, [!UICONTROL Brand]=Acme pour un groupe de produits et [!UICONTROL Brand]=AcmePlus pour un autre au même niveau). Vous pouvez créer jusqu’à sept niveaux de nœuds de groupe de produits enfant, sans inclure « [!UICONTROL All Products] ».

>[!NOTE]
>
>Vous ne pouvez pas créer de groupe de produits enfant pour un groupe de produits « [!UICONTROL Everything Else] ».

>[!TIP]
>
>Pour créer plusieurs composants de compte à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facultatif) Pour afficher un groupe de produits et ses nœuds enfants dans l’Arborescence, placez le curseur sur le nom du groupe de produits, cliquez sur ![icône de menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "icône de menu"), puis sélectionnez **[!UICONTROL Tree View]**.

1. Placez le curseur sur le nom du groupe de produits, cliquez sur ![Menu déroulant Flèche](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu déroulant Flèche"), puis sélectionnez **[!UICONTROL + Add Node]**.

1. Spécifiez les [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md) ou [[!DNL Microsoft Advertising] paramètres du groupe de produits](product-group-settings-microsoft.md), y compris la dimension et l’attribut du produit.

1. Cliquez sur **[!UICONTROL Post]**.

## Modifier les paramètres du nœud de groupe de produits

Vous pouvez modifier le modèle d’offre et de suivi pour les nœuds de groupe de produits unitaires (groupes de produits sans nœuds de groupe de produits enfants) qui sont inclus pour un groupe publicitaire. Vous ne pouvez modifier aucune information pour les groupes de produits unitaires exclus ou pour les nœuds de sous-division inclus ou exclus, qui sont des groupes de produits ayant des nœuds de groupe de produits enfants.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facultatif) Pour afficher un groupe de produits et ses nœuds enfants dans l’Arborescence, placez le curseur sur le nom du groupe de produits, cliquez sur ![icône de menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "icône de menu"), puis sélectionnez **[!UICONTROL Tree View]**.

1. Effectuez l’une des opérations suivantes :

   1. (Pour modifier les paramètres d’un seul nœud de groupe de produits) Placez le curseur sur le nom du groupe de produits, cliquez sur ![icône de menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "icône de menu"), puis sélectionnez **[!UICONTROL + Edit Node]**.

   1. (Pour modifier les paramètres d’un ou de plusieurs groupes publicitaires) Procédez comme suit :

      1. Cochez la case en regard de chaque nœud.

         Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

      1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez les [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md) ou [[!DNL Microsoft Advertising] paramètres du groupe de produits](product-group-settings-microsoft.md).

   Si plusieurs nœuds sont sélectionnés, vos modifications sont appliquées à tous les nœuds. Pour le champ [!UICONTROL Bid], vous avez la possibilité de modifier les valeurs existantes à une valeur spécifiée ou d’augmenter ou de diminuer le montant d’un pourcentage ou d’un montant monétaire spécifié, avec une limite. Pour le champ [!UICONTROL Tracking Template] , vous pouvez modifier les valeurs existantes à une valeur spécifiée, remplacer une chaîne existante par une chaîne spécifiée, ajouter un préfixe spécifié au début de chaque valeur ou ajouter un suffixe à la fin de chaque valeur.

1. (Facultatif) Cliquez sur **[!UICONTROL Additional Details]** et entrez éventuellement un nom et une description de projet.

1. Cliquez sur **[!UICONTROL Post]**.

## Supprimer les nœuds du groupe de produits

Vous pouvez supprimer n’importe quel groupe de produits, à l’exception d’un groupe « Tout le reste » lorsque d’autres groupes de produits existent au même niveau, utilisé pour déterminer les produits de votre compte de centre commercial qui sont inclus dans les annonces d’achat pour le groupe d’annonces. La suppression d’un groupe de produits supprime tous les groupes de produits enfants.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facultatif) Filtrez la liste pour inclure des groupes de produits spécifiques.

1. Effectuez l’une des opérations suivantes :

   * Pour supprimer un groupe de produits, cliquez dans la colonne **[!UICONTROL Status]** et sélectionnez **[!UICONTROL Delete]**.

   * Pour supprimer un ou plusieurs groupes de produits, procédez comme suit :

      1. Cochez la case en regard de chaque groupe de produits à supprimer.

         Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

      1. Dans la barre d’outils, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") et sélectionnez **[!UICONTROL Delete]**.

      1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos des groupes de produits d’achat](product-group-about.md)
>* [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] paramètres du groupe de produits](product-group-settings-microsoft.md)
