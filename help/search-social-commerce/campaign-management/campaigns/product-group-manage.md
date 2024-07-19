---
title: Gestion des groupes de produits
description: Découvrez comment créer et gérer des groupes de produits dans les campagnes d’achat.
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Gestion des groupes de produits

*[!DNL Google Ads]et [!DNL Microsoft Advertising] campagnes d’achats uniquement*

Vous pouvez créer et modifier des groupes de produits, et supprimer des groupes de produits et leurs groupes de produits enfants, dans la vue [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups].

## Créer un groupe de produits &quot;[!UICONTROL All Products]&quot;

Avant de pouvoir créer des groupes de produits avec des attributs spécifiques, vous devez d’abord créer un groupe de produits tout compris appelé &quot;[!UICONTROL All Products]&quot;. Chaque groupe d’annonces ne peut avoir qu’un seul groupe &quot;[!UICONTROL All Products]&quot;.

>[!TIP]
>
>Pour créer de nombreux composants de compte en même temps, utilisez les [feuilles d’envoi groupées de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md) ou les [[!DNL Microsoft Advertising]  paramètres du groupe de produits](product-group-settings-microsoft.md).

1. Cliquez sur **[!UICONTROL Post]**.

## Créer un noeud de groupe de produits enfant dans un groupe de produits existant

Une fois que vous avez créé au moins un groupe &quot;[!UICONTROL All Products]&quot; global pour un groupe publicitaire, vous pouvez créer des noeuds de groupe de produits enfants pour des sous-ensembles de produits à inclure ou exclure de l’offre, avec un ou plusieurs groupes de produits ciblant le même attribut dans chaque niveau (par exemple, [!UICONTROL Brand]=Acme pour un groupe de produits et [!UICONTROL Brand]=AcmePlus pour un autre au même niveau. Vous pouvez créer jusqu’à sept niveaux de noeuds de groupe de produits enfants, sans inclure &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>Vous ne pouvez pas créer de groupe de produits enfant pour un groupe de produits &quot;[!UICONTROL Everything Else]&quot;.

>[!TIP]
>
>Pour créer de nombreux composants de compte en même temps, utilisez les [feuilles d’envoi groupées de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facultatif) Pour afficher un groupe de produits et ses noeuds de groupe de produits enfants dans l’arborescence, placez le curseur sur le nom du groupe de produits, cliquez sur ![Icône de menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icône de menu"), puis sélectionnez **[!UICONTROL Tree View]**.

1. Placez le curseur sur le nom du groupe de produits, cliquez sur ![Menu déroulant de la flèche](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu déroulant de la flèche"), puis sélectionnez **[!UICONTROL + Add Node]**.

1. Spécifiez les [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md) ou [[!DNL Microsoft Advertising]  paramètres du groupe de produits](product-group-settings-microsoft.md), y compris la dimension et l’attribut du produit.

1. Cliquez sur **[!UICONTROL Post]**.

## Modification des paramètres du noeud de groupe de produits

Vous pouvez modifier le modèle d’offre et de suivi pour les noeuds de groupe de produits unitaires (groupes de produits sans noeuds de groupe de produits enfant) inclus dans un groupe de publicités. Vous ne pouvez modifier aucune information pour les groupes de produits unitaires exclus ou pour les noeuds de sous-division inclus ou exclus, qui sont des groupes de produits avec des noeuds de groupes de produits enfants.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facultatif) Pour afficher un groupe de produits et ses noeuds de groupe de produits enfants dans l’arborescence, placez le curseur sur le nom du groupe de produits, cliquez sur ![Icône de menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icône de menu"), puis sélectionnez **[!UICONTROL Tree View]**.

1. Effectuez l’une des opérations suivantes :

   1. (Pour modifier les paramètres d’un seul noeud de groupe de produits) Placez le curseur sur le nom du groupe de produits, cliquez sur ![Icône Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icône Menu"), puis sélectionnez **[!UICONTROL + Edit Node]**.

   1. (Pour modifier les paramètres d’un ou de plusieurs groupes d’annonces) Procédez comme suit :

      1. Cochez la case en regard de chaque noeud.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez les [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md) ou les [[!DNL Microsoft Advertising]  paramètres du groupe de produits](product-group-settings-microsoft.md).

   Pour plusieurs noeuds, vos modifications sont appliquées à tous les noeuds sélectionnés. Pour le champ [!UICONTROL Bid], vous avez la possibilité de modifier les valeurs existantes en une valeur spécifiée ou d’augmenter ou de diminuer le montant d’un pourcentage spécifié ou d’un montant monétaire, avec une limite. Pour le champ [!UICONTROL Tracking Template], vous pouvez modifier les valeurs existantes en une valeur spécifiée, remplacer une chaîne existante par une chaîne spécifiée, ajouter un préfixe spécifié au début de chaque valeur ou ajouter un suffixe à la fin de chaque valeur.

1. (Facultatif) Cliquez sur **[!UICONTROL Additional Details]** et saisissez éventuellement un nom et une description du projet.

1. Cliquez sur **[!UICONTROL Post]**.

## Suppression de noeuds de groupe de produits

Vous pouvez supprimer tout groupe de produits (à l’exception d’un groupe &quot;Tout le reste&quot; lorsque d’autres groupes de produits existent au même niveau), qui est utilisé pour déterminer les produits de votre compte de centre commercial qui sont inclus dans les publicités commerciales du groupe. La suppression d’un groupe de produits supprime tous les groupes de produits enfants.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Facultatif) Filtrez la liste pour inclure des groupes de produits spécifiques.

1. Effectuez l’une des opérations suivantes :

   * Pour supprimer un groupe de produits, cliquez dans la colonne **[!UICONTROL Status]** et sélectionnez **[!UICONTROL Delete]**.

   * Pour supprimer un ou plusieurs groupes de produits, procédez comme suit :

      1. Cochez la case en regard de chaque groupe de produits à supprimer.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Dans la barre d’outils, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") et sélectionnez **[!UICONTROL Delete]**.

      1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos des groupes de produits d’achats](product-group-about.md)
>* [[!DNL Google Ads] paramètres du groupe de produits](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] paramètres du groupe de produits](product-group-settings-microsoft.md)
