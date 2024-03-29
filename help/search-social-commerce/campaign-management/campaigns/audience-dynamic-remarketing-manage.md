---
title: Gérer [!DNL Microsoft Advertising] audiences de remarketing dynamique
description: Découvrez comment créer et gérer [!DNL Microsoft Advertising] audiences de remarketing dynamique.
exl-id: 6f0cb6a0-36cc-4a07-82a8-247191b6c4f5
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Gérer [!DNL Microsoft Advertising] audiences de remarketing dynamique

*[!DNL Microsoft Advertising]comptes uniquement*

Vous pouvez créer un [!DNL Microsoft Advertising] audience de remarketing dynamique lorsque vous utilisez la balise de conversion JavaScript et de suivi d’audience du moteur de recherche sur vos pages web. Chaque audience est créée à l’aide d’une balise spécifique incluse dans les pages web dont les utilisateurs constitueront l’audience. Vous pouvez créer plusieurs audiences avec la même balise de suivi. Vous pouvez également modifier le nom et la source de données des audiences existantes ou supprimer les audiences existantes.

Les audiences de remarketing dynamique ont le type d’audience &quot;[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>&quot; (par exemple, &quot;Dynamic Remarketing Antérieurement Buyers&quot;).

Pour plus d’informations sur le remarketing dynamique et sur la mise en oeuvre de la balise JavaScript requise, voir la section [[!DNL Microsoft Advertising] documentation sur le remarketing dynamique](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Créer une audience de remarketing dynamique

>[!NOTE]
>
>Pour [!DNL Microsoft Advertising] comptes, la balise JavaScript doit inclure la variable [ID de produit et paramètres de type de page](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifier le nom de la variable [!DNL Microsoft Advertising] balise de suivi d’événement universel (UET) incluse dans les pages web à partir desquelles l’audience sera créée.

   Vous aurez besoin du nom de la balise à une étape ultérieure.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Indiquez les informations de l’audience :

   1. Dans le **[!UICONTROL Data Source]** menu, sélectionnez **[!UICONTROL Dynamic Remarketing List]**.

   1. Saisissez le **[!UICONTROL Audience Name]**.

   1. Dans la liste de toutes les balises disponibles pour le compte de moteur de recherche, sélectionnez le nom de la variable [!DNL Microsoft Advertising] Balise UET incluse dans les pages web dont les utilisateurs comprendront l’audience.

   1. Sélectionnez le type de visiteur pour l’audience, en fonction des actions du visiteur sur les pages web pertinentes : *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, ou *[!UICONTROL Shopping Cart Abandoners]*.

   1. Indiquez le nombre de **[!UICONTROL Membership Days]**: nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience. Les valeurs peuvent être comprises entre une (1) et 180.

      Utilisez la durée pendant laquelle votre publicité doit être pertinente pour l’utilisateur.

1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>Votre [!DNL Microsoft Advertising] les listes de remarketing dynamique peuvent faire l’objet d’un ciblage une fois qu’elles comprennent au moins 300 utilisateurs.

## Modification d’une audience de remarketing dynamique

Vous pouvez modifier le nom et la source de données d’une [!DNL Microsoft Advertising] audience de remarketing dynamique. Vous ne pouvez pas modifier la valeur de la variable [!UICONTROL Membership Days] .

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Cochez la case en regard de l’audience à modifier.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez les informations de l&#39;audience :

   1. Dans le **[!UICONTROL Data Source]** , cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

   1. (Facultatif) Modifiez la variable **[!UICONTROL Audience Name]**.

   1. (Facultatif) Dans une liste de toutes les balises disponibles pour le compte réseau publicitaire, modifiez le nom de la variable [!DNL Microsoft Advertising] Balise UET incluse dans les pages web dont les utilisateurs comprendront l’audience.

   1. (Facultatif) Modifiez le type de visiteur de l’audience, basé sur les actions du visiteur sur les pages web pertinentes : *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, ou *[!UICONTROL Shopping Cart Abandoners]*.

   1. Cliquez sur **[!UICONTROL Post]**.

## Supprimer une audience de remarketing dynamique

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Facultatif) Filtrez la liste pour inclure des audiences spécifiques.

1. Cochez la case en regard de chaque audience à supprimer.

   Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [A propos des audiences](audience-about.md)
>* [Créer [!DNL Google Ads] audiences de correspondance client provenant de [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Créez un [!DNL Google Ads] audience de correspondance client provenant d’une liste de messagerie Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestion des audiences de correspondance client à l’aide des listes de données client](audience-from-customer-data-list.md)
