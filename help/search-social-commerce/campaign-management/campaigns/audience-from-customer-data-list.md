---
title: Gestion des audiences de correspondance client à l’aide des listes de données client
description: Découvrez comment créer et modifier [!DNL Google Ads] et [!DNL Microsoft® Advertising] des audiences de correspondance client provenant de vos listes de données client ;
exl-id: 734d8cb1-3915-410f-a0cc-0669d6575eab
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# Gérer [!DNL Google Ads] et [!DNL Microsoft® Advertising] audiences de correspondance client à l’aide de listes de données client

Vous pouvez créer [!DNL Google Ads] et [!DNL Microsoft® Advertising] des audiences de correspondance client provenant de vos listes de données client ; Vous pouvez également mettre à jour les [!DNL Google Ads] ou [!DNL Microsoft® Advertising] audience de correspondance du client, à l’exception de [!DNL Google Ads] audiences créées à partir d’un [!DNL Adobe] audience.

## Création d’une audience de correspondance client à partir d’une liste de données client

*[!DNL Google Ads]et [!DNL Microsoft® Advertising] comptes éligibles pour les correspondances client uniquement*

Vous pouvez créer un [!DNL Google Ads] ou [!DNL Microsoft® Advertising] liste basée sur les données client à partir d’un fichier de données que vous générez à partir de votre système de gestion de la relation client (CRM).

Pour [!DNL Microsoft® Advertising] compte, le fichier peut inclure des adresses électroniques. Pour [!DNL Google Ads] compte, le fichier peut inclure des adresses électroniques, des adresses postales ou des numéros de téléphone, des identifiants d’utilisateur ou des identifiants d’appareil mobile provenant de votre système de gestion de la relation client (CRM).

>[!NOTE]
>
>Search, Social et Commerce ne stocke aucune des données client que vous chargez ou provenant de la variable [!DNL Adobe] segments utilisés pour créer ou modifier une [!DNL Google Ads] ou [!DNL Microsoft® Advertising] audience.

1. Générez un fichier avec les données client au format requis.

   Les prénoms et les noms, adresses électroniques et numéros de téléphone doivent être hachés à l’aide de l’algorithme SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Pour [!DNL Google Ads] audiences, voir [!DNL Google Ads] documentation sur &quot;[Instructions de mise en forme pour le chargement de données hachées](https://support.google.com/google-ads/answer/7476159)&quot; pour une liste des champs d’informations de contact et des exigences autorisées. Pour [!DNL Microsoft® Advertising] audiences, voir [!DNL Microsoft® Advertising] documentation sur [préparation des listes de correspondance client](https://help.ads.microsoft.com/#apex/ads/en/56921). Vous pouvez éventuellement télécharger un [!DNL Microsoft® Excel] modèle pour les coordonnées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Indiquez les informations de l’audience :

   1. Dans le [!UICONTROL Data Source] menu, sélectionnez **[!UICONTROL Customer List]**.

   1. Saisissez le **[!UICONTROL Audience Name]**.

   1. Téléchargez le fichier :

      1. Sélectionnez la variable [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*, ou *[!UICONTROL Mobile Device IDs]*.

         L’option ID utilisateur n’est disponible que pour [!DNL Google Ads] les publicitaires aux États-Unis qui sont inscrits pour [segments d’ID utilisateur](https://support.google.com/google-ads/answer/9199250)

      1. (Les identifiants d’appareil mobile sont répertoriés uniquement) Sélectionnez la variable **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* ou *[!UICONTROL iOS]*), puis saisissez la variable **[!UICONTROL App ID]**.

         L’ID d’application est un identifiant unique utilisé par le système d’exploitation mobile pour permettre à votre application de se connecter à Google Play ou Apple App Store :

         * ([!DNL Android™] apps) La variable [!DNL Android™] nom du module dans [!DNL Google Play], identifié par &quot;`id=<package_name>`.&quot;

           Par exemple, dans https://play.google.com/store/apps/details?id=com.example.game, le nom du module est com.example.game.

         * ([!DNL iOS] apps) ID de l’application dans la variable [!DNL iTunes App Store], identifié par &quot;`<idNNNNNNNNN>`&quot; à la fin de l’URL. Il est également disponible dans la [!DNL iOS Developer Console].

           Par exemple, dans https://itunes.apple.com/us/app/id284882215, l’ID est id284882215.

         Votre équipe de développement a accès au [!UICONTROL App ID] pour la plateforme appropriée.

      1. Dans le [!UICONTROL Select File] champ, cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier sur votre réseau ou périphérique.

      1. Cochez la case pour indiquer que vous acceptez les termes du [!DNL Adobe] et les stratégies de confidentialité du réseau publicitaire.

      1. Cliquez sur **[!UICONTROL Upload File]**.

   1. Indiquez le nombre de **[!UICONTROL Membership Days]**: nombre de jours pendant lesquels le cookie d’un utilisateur reste dans l’audience.

   Utilisez la durée pendant laquelle votre publicité doit être pertinente pour l’utilisateur. Les listes de clients n’expirent pas, sauf si vous saisissez une valeur.

1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>* Le traitement du fichier peut prendre jusqu’à 24 heures au réseau publicitaire.
>* Voir [[!DNL Google Ads] documentation sur le fonctionnement et les limitations des correspondances client](https://support.google.com/displayvideo/answer/9539301).

## Modification d’une audience de correspondance client à l’aide d’une liste de données client

Vous pouvez mettre à jour les [!DNL Google Ads] ou [!DNL Microsoft® Advertising] audience de correspondance du client, à l’exception de [!DNL Google Ads] audiences créées à partir d’un [!DNL Adobe] audience. Vous pouvez charger des données pour ajouter, supprimer ou remplacer toutes les données existantes pour l’audience.

Les données doivent être du même type que la liste des clients d’origine (adresses électroniques, adresses postales, numéros de téléphone, identifiants d’utilisateur ou identifiants d’appareil mobile pour une application spécifique sur un système d’exploitation mobile spécifique).

1. Générez un fichier avec les données client au format requis pour le type de données existant.

Les prénoms et les noms, adresses électroniques et numéros de téléphone doivent être hachés à l’aide de l’algorithme SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Pour [!DNL Google Ads] audiences, voir [!DNL Google Ads] documentation sur &quot;[Instructions de mise en forme pour le chargement de données hachées](https://support.google.com/google-ads/answer/7476159)&quot; pour une liste des champs d’informations de contact et des exigences autorisées. Pour [!DNL Microsoft® Advertising] audiences, voir [!DNL Microsoft® Advertising] documentation sur [préparation des listes de correspondance client](https://help.ads.microsoft.com/#apex/ads/en/56921). Vous pouvez éventuellement télécharger un [!DNL Microsoft® Excel] modèle pour les coordonnées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Cochez la case en regard de l’audience à modifier.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png).

1. Sélectionnez l’action : *[!UICONTROL Add]* (pour ajouter les données chargées aux données existantes, sauf si elles existent déjà), *[!UICONTROL Delete]* (pour supprimer les données chargées des données existantes, lorsqu’elles existent déjà), ou *[!UICONTROL Replace]* (pour supprimer toutes les données existantes et les remplacer par les données chargées).

1. Téléchargez le fichier :

   1. Dans le [!UICONTROL Select File] champ, cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier sur votre réseau ou périphérique.

   1. Cochez la case pour indiquer que vous acceptez les termes du [!DNL Adobe] et les stratégies de confidentialité du réseau publicitaire.

   1. Cliquez sur **[!UICONTROL Upload File]**.

1. Cliquez sur **[!UICONTROL Post]**.

>[!NOTE]
>
>Le réseau publicitaire peut prendre un certain temps pour traiter les mises à jour d’une audience.

>[!MORELIKETHIS]
>
>* [A propos des audiences](audience-about.md)
>* [Créer [!DNL Google Ads] audiences de correspondance client provenant de [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Créez un [!DNL Google Ads] audience de correspondance client provenant d’une liste de messagerie Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
