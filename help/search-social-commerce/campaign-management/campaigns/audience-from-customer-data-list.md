---
title: Gérer les audiences de correspondance de clients à l’aide de listes de données client
description: Découvrez comment créer et modifier  [!DNL Google Ads]  audiences et  [!DNL Microsoft Advertising]  correspondance client à partir de vos listes de données client.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: 46d736c3e14bf407c513c5cb6a153a578aa65121
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Gérer des audiences de correspondance client [!DNL Google Ads] et [!DNL Microsoft Advertising] à l’aide de listes de données client

Vous pouvez créer des audiences de correspondance client [!DNL Google Ads] et [!DNL Microsoft Advertising] à partir de vos listes de données client. Vous pouvez également mettre à jour n’importe quelle audience de correspondance client [!DNL Google Ads] ou [!DNL Microsoft Advertising], à l’exception des audiences [!DNL Google Ads] créées à partir d’une audience [!DNL Adobe].

## Créer une audience de correspondance de clients à partir d’une liste de données client

*[!DNL Google Ads]et [!DNL Microsoft Advertising] comptes éligibles à la correspondance client uniquement*

Vous pouvez créer une [!DNL Google Ads] ou [!DNL Microsoft Advertising] liste basée sur les données client à partir d’un fichier de données généré à partir de votre système de gestion de la relation client (GRC).

Pour les comptes [!DNL Microsoft Advertising], le fichier peut inclure des adresses e-mail. Pour les comptes [!DNL Google Ads], le fichier peut inclure des adresses e-mail, des adresses postales ou des numéros de téléphone, des identifiants d’utilisateur ou d’appareil mobile provenant de votre système CRM.

>[!NOTE]
>
>Search, Social et Commerce ne stockent aucune des données client que vous chargez ou provenant des segments de [!DNL Adobe] utilisés pour créer ou modifier une audience [!DNL Google Ads] ou [!DNL Microsoft Advertising].

1. Générez un fichier avec les données client au format requis.

   Les prénoms, noms, adresses e-mail et numéros de téléphone doivent être hachés à l’aide de l’algorithme SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Pour les audiences [!DNL Google Ads], consultez la documentation [!DNL Google Ads] sur les « [Instructions de formatage pour le chargement de données hachées](https://support.google.com/google-ads/answer/7476159) » pour obtenir une liste des champs d’informations de contact autorisés et des exigences. Pour [!DNL Microsoft Advertising] d’audiences, consultez la documentation [!DNL Microsoft Advertising] sur [la préparation des listes de correspondance client](https://help.ads.microsoft.com/#apex/ads/en/56921). Vous pouvez éventuellement télécharger un modèle de [!DNL Microsoft Excel] pour obtenir des informations de contact.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les informations sur l’audience :

   1. Dans le menu [!UICONTROL Data Source], sélectionnez **[!UICONTROL Customer List]**.

   1. Saisissez le **[!UICONTROL Audience Name]**.

   1. Chargez le fichier :

      1. Sélectionnez le [!UICONTROL Data Upload Type] : *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]* ou *[!UICONTROL Mobile Device IDs]*.

         L’option ID d’utilisateur est disponible uniquement pour [!DNL Google Ads] annonceurs situés aux États-Unis qui ont choisi les segments [ID d’utilisateur](https://support.google.com/google-ads/answer/9199250)

      1. (Listes des ID d’appareil mobile uniquement) Sélectionnez la **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* ou *[!UICONTROL iOS]*), puis saisissez le **[!UICONTROL App ID]**.

         L’ID d’application est un identifiant unique utilisé par le système d’exploitation mobile pour permettre à votre application de se connecter à Google Play ou Apple App Store :

         * (Applications [!DNL Android™]) Nom du package [!DNL Android™] dans [!DNL Google Play], identifié par « `id=<package_name>` ».

           Par exemple, dans `https://play.google.com/store/apps/details?id=com.example.game`, le nom du package est com.example.game.

         * (Applications [!DNL iOS]) Identifiant d’application dans l’[!DNL iTunes App Store], identifié par « `<idNNNNNNNNN>` » à la fin de l’URL. Il est également disponible dans le [!DNL iOS Developer Console].

           Par exemple, dans `https://itunes.apple.com/us/app/id284882215`, l’ID est id284882215.

         Votre équipe de développement a accès au [!UICONTROL App ID] de la plateforme appropriée.

      1. Dans le champ [!UICONTROL Select File], cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier sur le réseau ou l’appareil.

      1. Cochez la case pour indiquer que vous acceptez les conditions des politiques de confidentialité du réseau [!DNL Adobe] et publicitaire.

      1. (Annonceurs créant des audiences [!DNL Google Ads] qui font des affaires dans l’Espace économique européen (EEE) ou au Royaume-Uni (UK) ; facultatif) Si vous avez obtenu le consentement des utilisateurs de l’EEE et du Royaume-Uni pour charger leurs données à des fins publicitaires, cochez la case en regard de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignore les données des utilisateurs de l’EEE et du Royaume-Uni dont le statut de consentement n’est pas spécifié. Cela peut entraîner des incohérences dans les données et des problèmes de performances.

      1. Cliquez sur **[!UICONTROL Upload File]**.

   1. Spécifiez le nombre de **[!UICONTROL Membership Days]**, qui correspond au nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience.

   Utilisez la durée pendant laquelle vous pensez que votre publicité sera pertinente pour l’utilisateur. Les listes de clients n’expirent que si vous saisissez une valeur.

1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>* Le réseau publicitaire peut prendre jusqu’à 24 heures pour traiter le fichier.
>* Consultez la [[!DNL Google Ads] documentation sur le fonctionnement et les limites de la correspondance client](https://support.google.com/displayvideo/answer/9539301).

## Modification d’une audience de correspondance client à l’aide d’une liste de données client

Vous pouvez mettre à jour n’importe quelle audience de correspondance client [!DNL Google Ads] ou [!DNL Microsoft Advertising], à l’exception des audiences [!DNL Google Ads] créées à partir d’une audience [!DNL Adobe]. Vous pouvez charger des données pour ajouter, supprimer ou remplacer toutes les données existantes pour l’audience.

Les données doivent être du même type que la liste des clients d’origine (adresses e-mail, adresses postales, numéros de téléphone, ID utilisateur ou ID d’appareil mobile pour une application spécifique sur un système d’exploitation mobile spécifique).

1. Générez un fichier avec les données client au format requis pour le type de données existant.

Les prénoms, noms, adresses e-mail et numéros de téléphone doivent être hachés à l’aide de l’algorithme SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Pour les audiences [!DNL Google Ads], consultez la documentation [!DNL Google Ads] sur les « [Instructions de formatage pour le chargement de données hachées](https://support.google.com/google-ads/answer/7476159) » pour obtenir une liste des champs d’informations de contact autorisés et des exigences. Pour [!DNL Microsoft Advertising] d’audiences, consultez la documentation [!DNL Microsoft Advertising] sur [la préparation des listes de correspondance client](https://help.ads.microsoft.com/#apex/ads/en/56921). Vous pouvez éventuellement télécharger un modèle de [!DNL Microsoft Excel] pour obtenir des informations de contact.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Cochez la case en regard de l’audience à modifier.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png).

1. Sélectionnez l’action : *[!UICONTROL Add]* (pour ajouter les données chargées aux données existantes, sauf si elles existent déjà), *[!UICONTROL Delete]* (pour supprimer les données chargées des données existantes, lorsqu’elles existent déjà) ou *[!UICONTROL Replace]* (pour supprimer toutes les données existantes et les remplacer par les données chargées).

1. Chargez le fichier :

   1. Dans le champ [!UICONTROL Select File], cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier sur le réseau ou l’appareil.

   1. Cochez la case pour indiquer que vous acceptez les conditions des politiques de confidentialité du réseau [!DNL Adobe] et publicitaire.

   1. Cliquez sur **[!UICONTROL Upload File]**.

1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>Le réseau publicitaire peut prendre un certain temps pour traiter les mises à jour d’une audience.

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Créer [!DNL Google Ads] des audiences de correspondance client à partir  [!DNL Adobe]  audiences](google-audience-from-adobe-audience.md)
>* [Création d’une audience  [!DNL Google Ads]  correspondance client à partir d’une liste d’emails Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
