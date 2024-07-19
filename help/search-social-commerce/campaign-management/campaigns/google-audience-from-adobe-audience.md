---
title: Créer [!DNL Google Ads] des audiences de correspondance client à partir d'audiences  [!DNL Adobe]
description: Découvrez comment créer  [!DNL Google Ads] des audiences de correspondance client à partir de vos audiences Adobe Analytics et d’Audience Manager existantes.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Créer [!DNL Google Ads] audiences de correspondance client à partir des audiences Adobe Analytics et Audience Manager

*[!DNL Google Ads]comptes éligibles pour la correspondance client uniquement*

*Annonceurs avec une intégration Adobe Advertising-Adobe Audience Manager ou Adobe Advertising-Adobe Analytics uniquement*

Les publicitaires intégrés peuvent créer [!DNL Google Ads] audiences de correspondance de clients à l’aide d’identifiants d’utilisateur provenant de a) [!DNL Analytics] segments partagés avec Adobe Experience Cloud et b) segments d’Audience Manager ayant pour destination Search, Social et Commerce, y compris [!DNL Analytics] segments publiés sur Adobe Experience Cloud et les segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud. Search, Social et Commerce renvoie automatiquement une URL de suivi [!DNL Google] à chaque segment [!DNL Analytics] ou d’Audience Manager afin que [!DNL Google] puisse suivre l’audience.

Chaque audience [!DNL Adobe] ne peut être utilisée que pour une seule audience [!DNL Google].

Chaque nouvelle audience [!DNL Google] porte le même nom que l&#39;audience [!DNL Adobe] d&#39;origine. [!DNL Google] détermine la taille de l’audience à cibler.

>[!TIP]
>
>Pour la segmentation en temps réel, utilisez les audiences créées par l’Audience Manager. Les segments créés dans [!DNL Analytics] et synchronisés avec Adobe Experience Cloud peuvent avoir des populations plus petites, car ils ne sont synchronisés qu’une fois par jour ; un surfeur admissible à un segment peut ne pas être inclus dans le segment avant le jour suivant. Les segments de [!DNL Analytics] ont une source de données &quot;suite de rapports - .&quot;

>[!NOTE]
>
>Search, Social et Commerce ne stocke aucune des données client de vos segments [!DNL Adobe] utilisés pour créer ou modifier une audience [!DNL Google].

1. Renseignez les conditions préalables si nécessaire :

   1. (Pour créer des audiences de liste de remarketing des identifiants utilisateur) Un utilisateur administrateur ou un gestionnaire de compte [!DNL Adobe] doit sélectionner le paramètre au niveau de l’annonceur pour activer les audiences de correspondance client.

   1. Mettez en oeuvre la version 2.0 ou ultérieure de [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html).

   1. Déployez la balise suivante aussi haut que possible sur les pages web de l’annonceur à partir desquelles l’audience doit être suivie.

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      où `Advertising_Cloud_UserID` est l’identifiant utilisateur numérique unique attribué à l’annonceur.

      Exemple : `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Si ce n’est pas déjà fait) Un utilisateur autorisé doit configurer le compte de l’annonceur pour [synchroniser avec le compte de l’organisation de l’annonceur dans Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Indiquez les informations de l’audience :

   1. Dans le menu **[!UICONTROL Data Source]**, sélectionnez **[!UICONTROL Adobe Audience]**.

   1. Sélectionnez l’ [!UICONTROL Adobe Audience] sur lequel baser l’audience [!DNL Google].

      >[!NOTE]
      >
      >Les audiences [!DNL Adobe] déjà utilisées pour une autre audience [!DNL Google] ne sont pas disponibles.

      Vous pouvez éventuellement rechercher des audiences qui contiennent une chaîne de texte spécifique avec un minimum de trois caractères. Pour toute audience correspondante, cliquez sur **[!UICONTROL Include]** pour la sélectionner.

      Si vous sélectionnez plusieurs audiences [!DNL Adobe], une audience [!DNL Google] distincte est créée pour chacune d’elles.

   1. Sélectionnez le **[!UICONTROL Audience Type]** à créer : **[!UICONTROL Customer List_User ID]**.

      Le compte [!DNL Google Ads] de l’annonceur doit être [ éligible à une correspondance personnalisée ](https://support.google.com/adspolicy/answer/6299717) et a accepté le [remarketing d’ID utilisateur](https://support.google.com/google-ads/answer/9199250).

   1. Cochez la case pour indiquer que vous acceptez les termes des [!DNL Adobe] et des politiques de confidentialité du réseau publicitaire.

   1. Indiquez le nombre de **[!UICONTROL Membership Days]**, qui correspond au nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience.

      Utilisez la durée pendant laquelle votre publicité doit être pertinente pour l’utilisateur. Les listes de remarketing ont une durée maximale de 540 jours. Les listes de clients n’ont pas de durée maximale ; pour indiquer que le cookie n’expire jamais, saisissez 10 000.

   1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] peut mettre jusqu’à 24 heures pour traiter le fichier.
>
>* Consultez la [[!DNL Google Ads] documentation sur le fonctionnement et les limites de la correspondance client](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Créer une  [!DNL Google Ads] audience de correspondance de client à partir d’une liste de messagerie Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gérer les audiences de correspondance de client à l’aide des listes de données de client](audience-from-customer-data-list.md)
>* [Gérer les audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
