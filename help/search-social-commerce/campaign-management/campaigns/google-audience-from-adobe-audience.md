---
title: 'Créer  [!DNL Google Ads]  audiences de correspondance client à partir d’audiences  [!DNL Adobe] '
description: Découvrez comment créer  [!DNL Google Ads]  audiences de correspondance client à partir de vos audiences Adobe Analytics et Audience Manager existantes.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Créer [!DNL Google Ads] audiences de correspondance client à partir d’audiences Adobe Analytics et Audience Manager

*[!DNL Google Ads]les comptes éligibles à la correspondance client uniquement*

*Publicitaires avec une intégration Adobe Advertising-Adobe Audience Manager ou Adobe Advertising-Adobe Analytics uniquement*

Les annonceurs inscrits peuvent créer [!DNL Google Ads] audiences de correspondance client à l’aide des ID utilisateur de a) [!DNL Analytics] segments partagés avec Adobe Experience Cloud et b) segments Audience Manager ayant pour destination Search, Social et Commerce, y compris les segments [!DNL Analytics] publiés sur Adobe Experience Cloud et les segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud. Search, Social et Commerce renvoie automatiquement une URL de suivi [!DNL Google] à chaque segment [!DNL Analytics] ou Audience Manager afin que [!DNL Google] puissiez suivre l’audience.

Chaque audience [!DNL Adobe] ne peut être utilisée que pour une seule audience [!DNL Google].

Chaque nouvelle audience [!DNL Google] porte le même nom que l’audience [!DNL Adobe] d’origine. [!DNL Google] détermine la taille de l’audience à cibler.

>[!TIP]
>
>Pour la segmentation en temps réel, utilisez des audiences créées par Audience Manager. Les segments créés dans [!DNL Analytics] et synchronisés avec Adobe Experience Cloud peuvent avoir des populations plus petites, car ils ne sont synchronisés que quotidiennement ; un internaute qualifié pour un segment peut ne pas être inclus dans le segment avant le lendemain. Les segments provenant de [!DNL Analytics] ont une source de données « suite de rapports - ».

>[!NOTE]
>
>Search, Social et Commerce ne stockent aucune des données client de vos segments de [!DNL Adobe] utilisées pour créer ou modifier une audience [!DNL Google].

1. Renseignez les conditions préalables requises selon vos besoins :

   1. (Pour créer des audiences de liste de remarketing d’ID utilisateur) Un utilisateur administrateur [!DNL Adobe] ou un gestionnaire de compte doit sélectionner le paramètre au niveau de l’annonceur pour activer les audiences de correspondance client.

   1. Implémentez [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) version 2.0 ou ultérieure.

   1. Déployez la balise suivante aussi haut que possible sur les pages web de l’annonceur à partir desquelles l’audience doit être suivie

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      où `Advertising_Cloud_UserID` est l’ID d’utilisateur numérique unique attribué à l’annonceur.

      Exemple : `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Si ce n’est pas déjà fait) Un utilisateur autorisé doit configurer le compte de l’annonceur pour [synchroniser avec le compte d’organisation de l’annonceur dans Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les informations sur l’audience :

   1. Dans le menu **[!UICONTROL Data Source]**, sélectionnez **[!UICONTROL Adobe Audience]**.

   1. Sélectionnez le [!UICONTROL Adobe Audience] sur lequel baser l’audience [!DNL Google].

      >[!NOTE]
      >
      >[!DNL Adobe] audiences déjà utilisées pour une autre audience [!DNL Google] ne sont pas disponibles.

      Vous pouvez éventuellement rechercher des audiences qui contiennent une chaîne de texte spécifique d’au moins trois caractères. Pour toute audience correspondante, cliquez sur **[!UICONTROL Include]** pour la sélectionner.

      Si vous sélectionnez plusieurs audiences [!DNL Adobe], une audience [!DNL Google] distincte est créée pour chacune d’elles.

   1. Sélectionnez le **[!UICONTROL Audience Type]** à créer : **[!UICONTROL Customer List_User ID]**.

      Le compte [!DNL Google Ads] de l’annonceur doit être [éligible à la correspondance personnalisée](https://support.google.com/adspolicy/answer/6299717) et avoir accepté le remarketing sous la forme d’un [ID d’utilisateur](https://support.google.com/google-ads/answer/9199250).

   1. Cochez la case pour indiquer que vous acceptez les conditions des politiques de confidentialité du réseau [!DNL Adobe] et publicitaire.

   1. Spécifiez le nombre de **[!UICONTROL Membership Days]**, qui correspond au nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience.

      Utilisez la durée pendant laquelle vous pensez que votre publicité sera pertinente pour l’utilisateur. La durée maximale des listes de remarketing est de 540 jours. Les listes de clients n’ont pas de durée maximale. Pour indiquer que le cookie n’expire jamais, saisissez 10000.

   1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] traitement du fichier peut prendre jusqu’à 24 heures.
>
>* Consultez la [[!DNL Google Ads] documentation sur le fonctionnement et les limites de la correspondance client](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Création d’une audience  [!DNL Google Ads]  correspondance client à partir d’une liste d’emails Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gérer les audiences de correspondance de clients à l’aide de listes de données client](audience-from-customer-data-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
