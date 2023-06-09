---
title: Créer [!DNL Google Ads] audiences de correspondance client provenant de [!DNL Adobe] audiences
description: Découvrez comment créer [!DNL Google Ads] Les clients correspondent aux audiences de vos audiences Adobe Analytics et d’Audience Manager existantes.
source-git-commit: 7089f7fe75b551953026ac6cca4ac7aafa06ba7b
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Créer [!DNL Google Ads] audiences de correspondance client provenant d’Adobe Analytics et d’Audiences Manager

*[!DNL Google Ads]comptes éligibles pour les correspondances client uniquement*

*Publicitaires avec une intégration Advertising-Adobe Audience Manager Adobe ou Advertising-Adobe Analytics Adobe uniquement*

Les publicitaires intégrés peuvent créer [!DNL Google Ads] correspondance client avec des audiences à l’aide d’identifiants utilisateur provenant d’a) [!DNL Analytics] segments partagés avec Adobe Experience Cloud et b) les segments d’Audience Manager qui ont pour destination Search, Social et Commerce, y compris [!DNL Analytics] segments publiés sur Adobe Experience Cloud et segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud. Search, Social et Commerce envoie automatiquement une [!DNL Google] URL de suivi de chaque [!DNL Analytics] ou d’Audience Manager de sorte que [!DNL Google] peut effectuer le suivi de l’audience.

Chaque [!DNL Adobe] audience ne peut être utilisée que pour une seule [!DNL Google] audience.

Chaque nouvelle [!DNL Google] l’audience porte le même nom que l’audience d’origine [!DNL Adobe] audience. [!DNL Google] détermine la taille de l’audience à cibler.

>[!TIP]
>
>Pour la segmentation en temps réel, utilisez les audiences créées par l’Audience Manager. Segments créés dans [!DNL Analytics] et synchronisées avec Adobe Experience Cloud peuvent avoir des populations plus petites, car elles ne sont synchronisées que tous les jours ; un surfeur admissible pour un segment ne peut pas être inclus dans le segment avant le lendemain. Segments de [!DNL Analytics] possèdent une source de données &quot;suite de rapports - .&quot;

>[!NOTE]
>
>Search, Social et Commerce ne stocke aucune des données client de votre [!DNL Adobe] segments utilisés pour créer ou modifier une [!DNL Google] audience.

1. Renseignez les conditions préalables si nécessaire :

   1. (Pour créer des audiences de liste de remarketing des identifiants utilisateur) Une [!DNL Adobe] l’utilisateur administrateur ou le gestionnaire de compte doit sélectionner le paramètre au niveau de l’annonceur pour activer les audiences de correspondance client. Les paramètres diffèrent selon qu’il s’agit d’un annonceur disposant d’une Audience Manager ou d’un annonceur disposant d’une [!DNL Analytics] uniquement.

   1. Mettez en oeuvre le [Service Adobe Experience Platform Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html) version 2.0 ou ultérieure.

   1. Déployez la balise suivante aussi haut que possible sur les pages web de l’annonceur à partir desquelles l’audience doit être suivie.

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      where `Advertising_Cloud_UserID` est l’identifiant utilisateur unique attribué à l’annonceur. Exemple :  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Si ce n’est pas déjà fait) Un utilisateur autorisé doit configurer le compte de l’annonceur pour [synchronisation avec le compte d’organisation de l’annonceur dans Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Indiquez les informations de l’audience :

   1. Dans le **[!UICONTROL Data Source]** menu, sélectionnez **[!UICONTROL Adobe Audience]**.

   1. Sélectionnez la [!UICONTROL Adobe Audience] sur lequel baser la variable [!DNL Google] audience.

      >[!NOTE]
      >
      >[!DNL Adobe] audiences déjà utilisées pour d’autres [!DNL Google] Les audiences ne sont pas disponibles.

      Vous pouvez éventuellement rechercher des audiences qui contiennent une chaîne de texte spécifique avec un minimum de trois caractères. Pour toute audience correspondante, cliquez sur **[!UICONTROL Include]** pour la sélectionner.

      Si vous sélectionnez plusieurs [!DNL Adobe] audiences, puis une [!DNL Google] l’audience est créée pour chacun d’eux.

   1. Sélectionnez la **[!UICONTROL Audience Type]** pour créer : **[!UICONTROL Customer List_User ID]**.

      L’annonceur [!DNL Google Ads] account doit être [éligible pour une correspondance personnalisée](https://support.google.com/adspolicy/answer/6299717) et ont choisi [remarketing des identifiants utilisateur](https://support.google.com/google-ads/answer/9199250).

   1. Cochez la case pour indiquer que vous acceptez les termes du [!DNL Adobe] et les stratégies de confidentialité du réseau publicitaire.

   1. Indiquez le nombre de **[!UICONTROL Membership Days]**: nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience.

      Utilisez la durée pendant laquelle votre publicité doit être pertinente pour l’utilisateur. Les listes de remarketing ont une durée maximale de 540 jours. Les listes de clients n’ont pas de durée maximale ; pour indiquer que le cookie n’expire jamais, saisissez 10000.

   1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] Le traitement du fichier peut prendre jusqu’à 24 heures.
>
>* Voir [[!DNL Google Ads] documentation sur le fonctionnement et les limitations des correspondances client](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [A propos des audiences](audience-about.md)
>* [Créez un [!DNL Google Ads] audience de correspondance client provenant d’une liste de messagerie Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestion des audiences de correspondance client à l’aide des listes de données client](audience-from-customer-data-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
