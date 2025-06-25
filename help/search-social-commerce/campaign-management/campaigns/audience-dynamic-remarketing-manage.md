---
title: Gestion  [!DNL Microsoft Advertising]  audiences de remarketing dynamique
description: Découvrez comment créer et gérer  [!DNL Microsoft Advertising]  audiences de remarketing dynamique.
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Gestion [!DNL Microsoft Advertising] audiences de remarketing dynamique

Comptes *[!DNL Microsoft Advertising]uniquement*

Vous pouvez créer une audience de remarketing dynamique [!DNL Microsoft Advertising] lorsque vous utilisez la balise de conversion et de suivi d’audience JavaScript du moteur de recherche sur vos pages web. Chaque audience est créée à l’aide d’une balise spécifiée incluse dans les pages web dont les utilisateurs composent l’audience. Vous pouvez créer plusieurs audiences avec la même balise de suivi. Vous pouvez également modifier le nom et la source de données des audiences existantes, ou supprimer des audiences existantes.

Les audiences de remarketing dynamique ont le type d’audience « [!UICONTROL Dynamic Remarketing] \&lt;Visitor Type\> » (par exemple, « Remarketing dynamique - acheteurs précédents »).

Pour plus d’informations sur le remarketing dynamique et sur la mise en œuvre de la balise JavaScript requise, consultez la [[!DNL Microsoft Advertising] documentation sur le remarketing dynamique](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Créer une audience de remarketing dynamique

>[!NOTE]
>
>Pour les comptes [!DNL Microsoft Advertising], la balise JavaScript doit inclure les paramètres [ID de produit et type de page](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. Identifiez le nom de la balise de suivi d’événement universel (UET) [!DNL Microsoft Advertising] incluse dans les pages web à partir desquelles l’audience sera créée.

   Vous aurez besoin du nom de la balise à une étape ultérieure.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les informations sur l’audience :

   1. Dans le menu **[!UICONTROL Data Source]**, sélectionnez **[!UICONTROL Dynamic Remarketing List]**.

   1. Saisissez le **[!UICONTROL Audience Name]**.

   1. Dans une liste de toutes les balises disponibles pour le compte de moteur de recherche, sélectionnez le nom de la balise [!DNL Microsoft Advertising] UET incluse dans les pages web dont les utilisateurs composent l’audience.

   1. Sélectionnez le type de visiteur ou de visiteuse pour l’audience, en fonction des actions du visiteur ou de la visiteuse sur les pages web appropriées : *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* ou *[!UICONTROL Shopping Cart Abandoners]*.

   1. Spécifiez le nombre de **[!UICONTROL Membership Days]**, qui correspond au nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience. Les valeurs peuvent être comprises entre 1 et 180.

      Utilisez la durée pendant laquelle vous pensez que votre publicité sera pertinente pour l’utilisateur.

1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>Vos [!DNL Microsoft Advertising] listes de remarketing dynamique sont éligibles au ciblage une fois qu’elles incluent au moins 300 utilisateurs.

## Modifier une audience de remarketing dynamique

Vous pouvez modifier le nom et la source de données d’une audience de remarketing dynamique [!DNL Microsoft Advertising]. Vous ne pouvez pas modifier la valeur du paramètre [!UICONTROL Membership Days].

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Cochez la case en regard de l’audience à modifier.

1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez les informations sur l’audience :

   1. Dans la section **[!UICONTROL Data Source]**, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

   1. (Facultatif) Modifiez le **[!UICONTROL Audience Name]**.

   1. (Facultatif) Dans une liste de toutes les balises disponibles pour le compte de réseau publicitaire, modifiez le nom de la balise [!DNL Microsoft Advertising] UET incluse dans les pages web dont les utilisateurs composent l’audience.

   1. (Facultatif) Modifiez le type de visiteur ou de visiteuse pour l’audience, en fonction des actions des visiteurs ou visiteuses sur les pages web pertinentes : *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]* ou *[!UICONTROL Shopping Cart Abandoners]*.

   1. Cliquez sur **[!UICONTROL Post]**.

## Supprimer une audience de remarketing dynamique

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Facultatif) Filtrez la liste pour inclure des audiences spécifiques.

1. Cochez la case en regard de chaque audience à supprimer.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Créer [!DNL Google Ads] des audiences de correspondance client à partir  [!DNL Adobe]  audiences](google-audience-from-adobe-audience.md)
>* [Création d’une audience  [!DNL Google Ads]  correspondance client à partir d’une liste d’emails Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gérer les audiences de correspondance de clients à l’aide de listes de données client](audience-from-customer-data-list.md)
