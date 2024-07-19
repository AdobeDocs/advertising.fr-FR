---
title: Gérer les  [!DNL Microsoft Advertising] audiences de remarketing dynamique
description: Découvrez comment créer et gérer des  [!DNL Microsoft Advertising] audiences de remarketing dynamique.
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Gérer les [!DNL Microsoft Advertising] audiences de remarketing dynamique

*[!DNL Microsoft Advertising]comptes uniquement*

Vous pouvez créer une audience de remarketing dynamique [!DNL Microsoft Advertising] lorsque vous utilisez la balise de conversion JavaScript et de suivi d’audience du moteur de recherche sur vos pages web. Chaque audience est créée à l’aide d’une balise spécifique incluse dans les pages web dont les utilisateurs composent l’audience. Vous pouvez créer plusieurs audiences avec la même balise de suivi. Vous pouvez également modifier le nom et la source de données des audiences existantes ou supprimer les audiences existantes.

Les audiences de remarketing dynamique ont le type d’audience &quot;[!UICONTROL Dynamic Remarketing] \&lt;Type de visiteur\>&quot; (par exemple &quot;Acheteurs précédents de remarketing dynamique&quot;).

Pour plus d’informations sur le remarketing dynamique et sur la mise en oeuvre de la balise JavaScript requise, consultez la [[!DNL Microsoft Advertising] documentation sur le remarketing dynamique](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Créer une audience de remarketing dynamique

>[!NOTE]
>
>Pour les comptes [!DNL Microsoft Advertising], la balise JavaScript doit inclure les [paramètres d’ID de produit et de type de page](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifiez le nom de la balise de suivi d’événement universel (UET) [!DNL Microsoft Advertising] incluse dans les pages web à partir desquelles l’audience sera créée.

   Vous aurez besoin du nom de la balise à une étape ultérieure.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Indiquez les informations de l’audience :

   1. Dans le menu **[!UICONTROL Data Source]**, sélectionnez **[!UICONTROL Dynamic Remarketing List]**.

   1. Saisissez le **[!UICONTROL Audience Name]**.

   1. Dans la liste de toutes les balises disponibles pour le compte de moteur de recherche, sélectionnez le nom de la balise UET [!DNL Microsoft Advertising] incluse dans les pages web dont les utilisateurs composent l’audience.

   1. Sélectionnez le type de visiteur pour l’audience, qui est basé sur les actions des visiteurs sur les pages web appropriées : *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* ou *[!UICONTROL Shopping Cart Abandoners]*.

   1. Indiquez le nombre de **[!UICONTROL Membership Days]**, qui correspond au nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience. Les valeurs peuvent être comprises entre une (1) et 180.

      Utilisez la durée pendant laquelle votre publicité doit être pertinente pour l’utilisateur.

1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>Vos [!DNL Microsoft Advertising] listes de remarketing dynamique sont éligibles au ciblage une fois qu’elles incluent au moins 300 utilisateurs.

## Modification d’une audience de remarketing dynamique

Vous pouvez modifier le nom et la source de données d’une audience de remarketing dynamique [!DNL Microsoft Advertising]. Vous ne pouvez pas modifier la valeur du paramètre [!UICONTROL Membership Days] .

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Cochez la case en regard de l’audience à modifier.

1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez les informations de l&#39;audience :

   1. Dans la section **[!UICONTROL Data Source]**, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

   1. (Facultatif) Modifiez le **[!UICONTROL Audience Name]**.

   1. (Facultatif) Dans une liste de toutes les balises disponibles pour le compte réseau publicitaire, modifiez le nom de la balise UET [!DNL Microsoft Advertising] incluse dans les pages web dont les utilisateurs composent l’audience.

   1. (Facultatif) Modifiez le type de visiteur pour l’audience, qui est basé sur les actions des visiteurs sur les pages web appropriées : *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* ou *[!UICONTROL Shopping Cart Abandoners]*.

   1. Cliquez sur **[!UICONTROL Post]**.

## Supprimer une audience de remarketing dynamique

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Facultatif) Filtrez la liste pour inclure des audiences spécifiques.

1. Cochez la case en regard de chaque audience à supprimer.

   Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Créer [!DNL Google Ads]  des audiences de correspondance client à partir des  [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Créer une  [!DNL Google Ads] audience de correspondance de client à partir d’une liste de messagerie Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gérer les audiences de correspondance de client à l’aide des listes de données de client](audience-from-customer-data-list.md)
