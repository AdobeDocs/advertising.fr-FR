---
title: Gestion des comptes marchands
description: Découvrez comment configurer et gérer les détails d’un compte de centre commercial.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Gestion des comptes marchands

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Search, Social et Commerce peuvent télécharger et afficher des données de produit chaque jour pour n’importe quel compte du Centre commercial Google ou du Centre commercial Microsoft d’un annonceur. En outre, Search, Social et Commerce peuvent automatiser la création d’annonces en fonction du contenu du compte marchand. Pour travailler directement avec les données de produit dans Search, Social et Commerce, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et avec l’accès *activé*.

>[!NOTE]
>
>Vous ne pouvez pas supprimer un enregistrement de compte marchand. Vous pouvez désactiver l’accès à un compte en définissant le type de compte sur *désactivé*.

## Créer des détails de compte marchand {#create-merchant-account}

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Pour afficher les données de produit, générer des modèles de suivi pour un compte de commerçant et créer des annonces basées sur les données, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et avec un accès au compte *activé*.

>[!NOTE]
>
>Pour créer un compte réel sur le réseau marchand, rendez-vous sur le site web du réseau.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, qui ouvre l’onglet [!UICONTROL Accounts] .

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Account]**.

1. Spécifiez les [paramètres du compte marchand](#merchant-account-settings) :

   1. Dans le menu [!UICONTROL Product Source], sélectionnez le centre marchand.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Obligatoire pour les comptes [!DNL Google Ads] ; facultatif pour les comptes [!DNL Microsoft Advertising]) Autorisez Search, Social et Commerce à accéder au compte à l’aide du [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/) :

      1. (Comptes [!DNL Microsoft Advertising] uniquement) Sélectionnez **[!UICONTROL oAuth]**.

      1. Cliquez sur **[!UICONTROL Enable Connection]**.

      1. (Si vous n’êtes pas connecté au compte de l’annonceur) Connectez-vous au compte de l’annonceur. La bonne pratique consiste à utiliser les informations d’identification pour l’accès de l’API de contenu au compte du centre commercial.

      1. Dans l’écran de demande d’accès/d’autorisation, cliquez sur le bouton pour confirmer l’autorisation.

      1. Copiez la chaîne d’authentification dans la fenêtre pop-up qui s’ouvre et collez la chaîne dans le champ **[!UICONTROL oAuth Token]** .

      1. Spécifiez les autres paramètres du compte.

1. Cliquez sur **[!UICONTROL Save]**.

   Les données d’attribut pour tous les produits du compte sont disponibles dans Search, Social et Commerce après le prochain processus de synchronisation quotidien (vers 6 h dans le fuseau horaire local de l’utilisateur). Vous pouvez ensuite utiliser les données de produit pour automatiser la création d’annonces publicitaires à l’aide de flux d’inventaire.

## Modifier les détails du compte marchand {#edit-merchant-account}

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Si les informations d’identification du compte changent ou si vous souhaitez arrêter de récupérer et d’utiliser les données d’un compte marchand, modifiez les détails du compte.

>[!NOTE]
>
>Pour modifier un compte réel sur le réseau marchand, accédez au site Web du réseau.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, qui ouvre l’onglet [!UICONTROL Accounts] .

1. En regard du nom du compte, cliquez sur ![Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Afficher/modifier les paramètres").

1. Modifiez les [paramètres du compte marchand](#merchant-account-settings).

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social et Commerce doivent synchroniser les nouvelles données de compte avec celles du réseau marchand. Cela se produit automatiquement une fois par jour vers 6h00 dans le fuseau horaire local de l’utilisateur.

## Désactiver l&#39;accès à un compte marchand {#disable-merchant-account}

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Lorsque vous désactivez un compte commercial, Search, Social et Commerce ne se connecte pas au compte et ne récupère donc pas les données de produit mises à jour. Les données collectées lors de l’activation du compte sont toujours stockées, et les annonces existantes créées à l’aide des données de produit ne sont pas mises à jour, mises en pause ou supprimées conformément au modèle de flux et aux paramètres des données de flux.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , qui ouvre l’onglet [!UICONTROL Accounts] .

1. En regard du nom du compte, cliquez sur ![Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Afficher/modifier les paramètres").

1. Remplacez le [!UICONTROL EF Account Type] par **[!UICONTROL Disabled]**.

1. Cliquez sur **[!UICONTROL Save]**.

## Paramètres du compte marchand {#merchant-account-settings}

>[!NOTE]
>
>Seuls les rôles de gestionnaire de compte d’agence, de gestionnaire de compte [!DNL Adobe] et d’administrateur peuvent configurer les paramètres du compte marchand.

**[!UICONTROL Product Source]:** Le réseau marchand. Vous ne pouvez pas modifier la valeur d’un compte existant.

**[!UICONTROL OAuth Token]:** (comptes [!DNL Google Merchant Center] uniquement) Jeton du compte pour autoriser les connexions à l’aide du [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] uniquement) Autoriser ou non les connexions au compte à l’aide de :

* *[!UICONTROL Client login]:* pour utiliser le nom d’utilisateur du client.

* *[!UICONTROL oAuth]* (valeur par défaut) : pour utiliser le [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] uniquement) Clé d’accès que le compte de développeur doit utiliser.

**[!UICONTROL Account Name]:** nom affiché pour le compte dans Search, Social et Commerce.

**[!UICONTROL Login]:** nom ou ID de connexion du compte.

**[!UICONTROL Password]:** mot de passe du compte.

**[!UICONTROL Confirm Password]:** mot de passe du compte.

**[!UICONTROL EF Account Type]:** si Search, Social et Commerce accèdent au compte :

* *[!UICONTROL Enabled]* (valeur par défaut) : Search, Social et Commerce peuvent se connecter au compte pour récupérer des données de produit.

* *[!UICONTROL Disabled]:* Search, Social et Commerce ne se connecte pas au compte et ne récupère donc pas les données de produit mises à jour. Les données collectées lors de l’activation du compte sont toujours stockées, et les annonces existantes créées à l’aide des données de produit ne sont pas mises à jour, mises en pause ou supprimées conformément au modèle de flux et aux paramètres des données de flux.

**[!UICONTROL Account ID]:** ID du compte marchand. Si vous ne disposez que d’un seul compte avec les informations de connexion spécifiées, cette valeur est facultative.

**[!UICONTROL Time Zone]:** Fuseau horaire de l’annonceur. Utilisez le même fuseau horaire configuré pour les informations du compte Search, Social et Commerce de l’annonceur (qui est défini lors de la création du compte). Vous ne pouvez pas modifier la valeur d’un compte existant.

>[!MORELIKETHIS]
>
>* [À propos des comptes de réseau publicitaire](ad-network-account-about.md)
>* [Gérer les comptes de réseau publicitaire](ad-network-account-manage.md)
