---
title: Gestion des comptes de commerce
description: Découvrez comment configurer et gérer les détails d’un compte de centre commercial.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Gestion des comptes de commerce

*Gestionnaire de compte de l’agence, gestionnaire de compte d’Adobe et rôles utilisateur administrateur uniquement*

Search, Social et Commerce peut télécharger et afficher des données de produit chaque jour pour l’un des comptes Google Merchant Center ou Microsoft Merchant Center d’un annonceur. En outre, Search, Social et Commerce peut automatiser la création des publicités en fonction du contenu du compte marchand. Pour travailler directement avec les données de produit dans Search, Social et Commerce, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et avec l’accès *enabled*.

>[!NOTE]
>
>Vous ne pouvez pas supprimer un enregistrement de compte marchand. Vous pouvez désactiver l&#39;accès à un compte en définissant le type de compte sur *disabled*.

## Création de détails de compte commercial {#create-merchant-account}

*Gestionnaire de compte de l’agence, gestionnaire de compte d’Adobe et rôles utilisateur administrateur uniquement*

Pour afficher les données de produit et générer des modèles de suivi pour un compte marchand, ainsi que pour créer des publicités basées sur les données, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et ayant accès au compte *enabled*.

>[!NOTE]
>
>Pour créer un compte réel sur le réseau marchand, rendez-vous sur le site web du réseau.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, ce qui ouvre l’onglet [!UICONTROL Accounts] .

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Account]**.

1. Spécifiez les [paramètres du compte marchand](#merchant-account-settings) :

   1. Dans le menu [!UICONTROL Product Source], sélectionnez le centre commercial.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Requis pour les comptes [!DNL Google Ads] ; facultatif pour les comptes [!DNL Microsoft Advertising]) Autoriser Search, Social et Commerce à accéder au compte à l’aide du [[!DNL OAuth]  protocole d’autorisation](https://oauth.net/2/) :

      1. ([!DNL Microsoft Advertising] comptes uniquement) Sélectionnez **[!UICONTROL oAuth]**.

      1. Cliquez sur **[!UICONTROL Enable Connection]**.

      1. (Si vous n’êtes pas connecté au compte de l’annonceur) Connectez-vous au compte de l’annonceur. La bonne pratique consiste à utiliser les informations d’identification pour l’accès de l’API de contenu au compte de centre commercial.

      1. Dans l’écran de demande d’accès/d’autorisation, cliquez sur le bouton pour confirmer l’autorisation.

      1. Copiez la chaîne d’authentification dans la fenêtre contextuelle qui s’ouvre, puis collez-la dans le champ **[!UICONTROL oAuth Token]**.

      1. Spécifiez les autres paramètres du compte.

1. Cliquez sur **[!UICONTROL Save]**.

   Les données d’attribut pour tous les produits du compte sont disponibles dans Search, Social et Commerce après le prochain processus de synchronisation quotidien (vers 6 h dans le fuseau horaire local de l’utilisateur). Vous pouvez ensuite utiliser les données de produit pour automatiser la création d’annonces à l’aide de flux d’inventaire.

## Modification des détails du compte commercial {#edit-merchant-account}

*Gestionnaire de compte de l’agence, gestionnaire de compte d’Adobe et rôles utilisateur administrateur uniquement*

Si les informations d’identification du compte changent ou si vous souhaitez arrêter de récupérer et d’utiliser des données pour un compte marchand, modifiez les détails du compte.

>[!NOTE]
>
>Pour modifier un compte réel sur le réseau marchand, rendez-vous sur le site web du réseau.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, ce qui ouvre l’onglet [!UICONTROL Accounts] .

1. En regard du nom du compte, cliquez sur ![Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Afficher/modifier les paramètres").

1. Modifiez les [paramètres du compte marchand](#merchant-account-settings).

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social et Commerce doivent synchroniser les nouvelles données de compte avec celles du réseau commercial. Cela se produit automatiquement une fois par jour à 06h00 environ dans le fuseau horaire local de l’utilisateur.

## Désactiver l’accès à un compte marchand {#disable-merchant-account}

*Gestionnaire de compte de l’agence, gestionnaire de compte d’Adobe et rôles utilisateur administrateur uniquement*

Lorsque vous désactivez un compte marchand, Search, Social et Commerce ne se connecte pas au compte et ne récupère donc pas les données de produit mises à jour. Les données collectées lors de l’activation du compte sont toujours stockées et les publicités existantes créées à l’aide des données de produit ne sont pas mises à jour, mises en pause ou supprimées selon le modèle de flux et les paramètres des données de flux.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , ce qui ouvre l’onglet [!UICONTROL Accounts] .

1. En regard du nom du compte, cliquez sur ![Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Afficher/modifier les paramètres").

1. Remplacez [!UICONTROL EF Account Type] par **[!UICONTROL Disabled]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Paramètres du compte marchand {#merchant-account-settings}

>[!NOTE]
>
>Seuls le gestionnaire de compte d’agence, le gestionnaire de compte [!DNL Adobe] et les rôles d’utilisateur administrateur peuvent configurer les paramètres du compte commercial.

**[!UICONTROL Product Source]:** Réseau du commerce. Vous ne pouvez pas modifier la valeur d’un compte existant.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] comptes uniquement) Jeton du compte pour autoriser les connexions à l’aide du [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] uniquement) Indique s’il faut autoriser des connexions au compte à l’aide de :

* *[!UICONTROL Client login]:* pour utiliser la connexion du client.

* *[!UICONTROL oAuth]* (valeur par défaut) : pour utiliser le [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] uniquement) Clé d’accès du compte de développeur à utiliser.

**[!UICONTROL Account Name]:** nom affiché pour le compte dans Search, Social et Commerce.

**[!UICONTROL Login]:** nom ou identifiant de connexion du compte.

**[!UICONTROL Password]:** mot de passe du compte.

**[!UICONTROL Confirm Password]:** mot de passe du compte.

**[!UICONTROL EF Account Type]:** Indique si Search, Social et Commerce accède au compte :

* *[!UICONTROL Enabled]* (valeur par défaut) : Search, Social et Commerce peut se connecter au compte pour récupérer les données de produit.

* *[!UICONTROL Disabled]:* La recherche, Social et Commerce ne se connecte pas au compte et ne récupère donc pas les données de produit mises à jour. Les données collectées lors de l’activation du compte sont toujours stockées et les publicités existantes créées à l’aide des données de produit ne sont pas mises à jour, mises en pause ou supprimées selon le modèle de flux et les paramètres des données de flux.

**[!UICONTROL Account ID]:** ID du compte marchand. Si vous ne disposez que d’un seul compte avec les informations de connexion spécifiées, cette valeur est facultative.

**[!UICONTROL Time Zone]:** Fuseau horaire de l’annonceur. Utilisez le même fuseau horaire configuré pour les informations de compte Search, Social et Commerce de l’annonceur (qui sont définies lors de la création du compte). Vous ne pouvez pas modifier la valeur d’un compte existant.

>[!MORELIKETHIS]
>
>* [À propos des comptes réseau d’annonces](ad-network-account-about.md)
>* [Gérer des comptes réseau publicitaires](ad-network-account-manage.md)
