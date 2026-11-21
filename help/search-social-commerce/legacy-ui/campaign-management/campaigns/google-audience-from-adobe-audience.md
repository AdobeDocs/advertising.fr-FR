---
title: Créer [!DNL Google Ads] audiences de correspondance client à partir de [!DNL Adobe] audiences
description: Découvrez comment créer [!DNL Google Ads] audiences de correspondance client à partir de vos audiences Adobe Analytics et Audience Manager existantes.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/Ep3X-eo2kcGlW3NsV3CJEKBkEapa-oAv0HLexc1xnhM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%
---
# Créer [!DNL Google Ads] audiences de correspondance client à partir d’audiences Adobe Analytics et Audience Manager

*[!DNL Google Ads]comptes éligibles à la correspondance client uniquement*

*Annonceurs avec une intégration Adobe Advertising-Adobe Audience Manager ou Adobe Advertising-Adobe Analytics uniquement*

Les annonceurs inscrits peuvent créer [!DNL Google Ads] audiences de correspondance client à l’aide des ID utilisateur de a) [!DNL Analytics] segments partagés avec Adobe CX Enterprise et b) segments Audience Manager ayant pour destination Search, Social et Commerce, y compris [!DNL Analytics] segments publiés sur Adobe CX Enterprise et les segments créés à l’aide de la bibliothèque d’audiences Adobe CX Enterprise. Search, Social et Commerce renvoie automatiquement une URL de suivi [!DNL Google] à chaque segment [!DNL Analytics] ou Audience Manager afin que [!DNL Google] puisse suivre l’audience.

Chaque audience [!DNL Adobe] peut être utilisée pour une seule audience [!DNL Google].

Chaque nouvelle audience [!DNL Google] porte le même nom que l’audience [!DNL Adobe] d’origine. [!DNL Google] détermine la taille de l&#39;audience pour pouvoir être ciblée.

>[!TIP]
>
>Pour la segmentation en temps réel, utilisez des audiences créées par Audience Manager. Les segments créés dans [!DNL Analytics] et synchronisés avec Adobe CX Enterprise peuvent avoir des populations plus petites, car ils ne sont synchronisés que quotidiennement ; un internaute qualifié pour un segment peut ne pas être inclus dans le segment avant le lendemain. Les segments de [!DNL Analytics] ont une source de données « suite de rapports - ».

>[!NOTE]
>
>Search, Social et Commerce ne stockent aucune des données client de vos segments [!DNL Adobe] utilisés pour créer ou modifier une audience [!DNL Google].

1. Renseignez les conditions préalables requises selon vos besoins :

   1. (Pour créer des audiences de liste de remarketing d’ID utilisateur) Un utilisateur administrateur [!DNL Adobe] ou un gestionnaire de compte doit sélectionner le paramètre au niveau de l’annonceur pour activer les audiences de correspondance client.

   1. Implémentez [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=fr) version 2.0 ou ultérieure.

   1. Déployez la balise suivante aussi haut que possible sur les pages web de l’annonceur à partir desquelles l’audience doit être suivie

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      où `Advertising_Cloud_UserID` est l’ID d’utilisateur numérique unique attribué à l’annonceur.

      Exemple : `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (S’il n’est pas déjà terminé) Un utilisateur autorisé doit configurer le compte de l’annonceur pour qu’il se synchronise [avec le compte d’organisation de l’annonceur dans Adobe CX Enterprise](/help/search-social-commerce/legacy-ui/admin/sync-adobe-audiences.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >.[!UICONTROL Campaigns]** Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les informations sur l’audience :

   1. Dans le menu **[!UICONTROL Data Source]**, sélectionnez **[!UICONTROL Adobe Audience]**.

   1. Sélectionnez [!UICONTROL Adobe Audience] sur laquelle baser l’audience [!DNL Google].

      >[!NOTE]
      >
      >Les audiences [!DNL Adobe] déjà utilisées pour une autre audience [!DNL Google] ne sont pas disponibles.

      Vous pouvez éventuellement rechercher des audiences qui contiennent une chaîne de texte spécifique d’au moins trois caractères. Pour toute audience correspondante, cliquez sur **[!UICONTROL Include]** pour la sélectionner.

      Si vous sélectionnez plusieurs audiences [!DNL Adobe], une audience [!DNL Google] distincte est créée pour chacune d’elles.

   1. Sélectionnez le **[!UICONTROL Audience Type]** à créer : **[!UICONTROL Customer List_User ID]**.

      Le compte [!DNL Google Ads] de l’annonceur doit être [éligible à la correspondance personnalisée](https://support.google.com/adspolicy/answer/6299717) et avoir accepté le [remarketing de l’ID utilisateur](https://support.google.com/google-ads/answer/9199250).

   1. Cochez la case pour indiquer que vous acceptez les conditions des politiques de confidentialité [!DNL Adobe] et du réseau publicitaire.

   1. Spécifiez le nombre de **[!UICONTROL Membership Days]**, qui correspond au nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience.

      Utilisez la durée pendant laquelle vous pensez que votre publicité sera pertinente pour l’utilisateur. La durée maximale des listes de remarketing est de 540 jours. Les listes de clients n’ont pas de durée maximale. Pour indiquer que le cookie n’expire jamais, saisissez 10000.

   1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] peut prendre jusqu&#39;à 24 heures pour traiter le fichier.
>
>* Consultez la [[!DNL Google Ads] documentation sur le fonctionnement et les limites de la correspondance client](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Création d’une  [!DNL Google Ads] audience de correspondance client à partir d’une liste d’adresses électroniques Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gérer les audiences de correspondance client à l’aide de listes de données client](audience-from-customer-data-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
