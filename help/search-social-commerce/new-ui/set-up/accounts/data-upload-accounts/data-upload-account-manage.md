---
title: Configuration des comptes réseau de publicités pour le chargement de données
description: Découvrez comment configurer et gérer les détails d’un compte réseau publicitaire.
feature: Search Campaign Management
exl-id: 7e8fb475-21f9-446b-a112-e0f27a4c4172
source-git-commit: 00565a6c9e784472fab9c9d223c83b0c7cbb91b1
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Gestion des comptes réseau pour les chargements de données

<!-- Edit all, including title and metadata -->

Vous trouverez ci-dessous des instructions pour la gestion des détails de compte pour les comptes de réseau publicitaire pour lesquels vous allez charger les données de compte.

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [&#x200B; Inventaire pris en charge &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md).

>[!NOTE]
>
>Pour obtenir des instructions sur la gestion des détails d’un compte de réseau publicitaire que Search, Social et Commerce synchronise à l’aide de l’API du réseau publicitaire, voir « [&#x200B; Gérer les comptes du réseau publicitaire via la connexion API »](../api-accounts/api-account-manage.md) à la place.

## Créer des détails de compte {#create-account}

1. Cliquez sur **[!UICONTROL Create Account]**.

1. Cliquez sur le nom du réseau publicitaire, puis sur **[!UICONTROL Next]**.

1. Spécifiez les [paramètres du compte](#account-settings) :

   1. Dans l’onglet **[!UICONTROL Account Details]** , modifiez les détails du compte.

   1. (Annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md)) Cliquez sur l’onglet **[!UICONTROL Set up Adobe Analytics]** et modifiez les suites de rapports [!DNL Analytics] à utiliser pour le suivi et les rapports d’activité de campagne.

   1. (Facultatif) Chargez les fichiers de données du compte dans l’onglet **[!UICONTROL Upload File]** .

1. Cliquez sur **[!UICONTROL Save]**.

## Modifier les détails du compte {#edit-account}

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Sélectionnez le compte de l’une des manières suivantes :

   * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

   * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

1. Modifiez les [paramètres du compte](#account-settings-upload) :

   1. (Facultatif) Dans l’onglet **[!UICONTROL Account Details]** , modifiez les détails du compte.

   1. (Facultatif ; annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md)) Cliquez sur l’onglet **[!UICONTROL Set up Adobe Analytics]** et modifiez les suites de rapports [!DNL Analytics] à utiliser pour le suivi et les rapports d’activité de campagne.

   1. (Facultatif) Chargez les fichiers de données du compte dans l’onglet **[!UICONTROL Upload File]** .

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Cliquez sur **[!UICONTROL Save]**.

## Activer ou désactiver les comptes réseau publicitaires {#enable-disable-account}

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Effectuez l’une des opérations suivantes :

   * (Vue [!UICONTROL Accounts]) :

      * (Pour activer le compte) Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Activate]** dans la barre d’outils des actions en bloc.

      * (Pour désactiver le compte) Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Pause]** dans la barre d’outils des actions en bloc.

   * (Dans les paramètres du compte) :

      1. Sélectionnez le compte de l’une des manières suivantes :

         * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

         * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

      1. Dans l’onglet **[!UICONTROL Account Details]** , désactivez **[!UICONTROL Account enabled]**.

      1. Cliquez sur **[!UICONTROL Save]**.

## Paramètres du compte {#account-settings-upload}

### onglet [!UICONTROL Account Details]

**[!UICONTROL Account Name]:** nom à afficher pour le compte dans Search, Social et Commerce.

>[!NOTE]
>
>Si vous disposez d’une intégration Search, Social et Commerce-Adobe Analytics et que vous modifiez le nom du compte de recherche, contactez l’équipe chargée de votre compte Adobe pour qu’elle mette à jour le mappage.

**[!UICONTROL Network Account ID]:** ID de compte attribué par le réseau publicitaire. Cet identifiant est utilisé uniquement à des fins de création de rapports. Search, Social et Commerce ne se connectent pas directement au compte du réseau publicitaire.

**[!UICONTROL Currency]:** (Lecture seule pour les comptes existants) Abréviation de la devise utilisée pour le compte.

**[!UICONTROL Time Zone]:** (Lecture seule pour les comptes existants) Fuseau horaire de l’annonceur.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled] :** Search, Social et Commerce permet la récupération automatisée des données pour un compartiment S3 spécifié.

## onglet [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md) ; facultatif) Une ou plusieurs suites de rapports Analytics auxquelles Search, Social et Commerce envoient les données que vous chargez pour le réseau publicitaire, y compris les classifications d’entité et les données de clic pour le compte.

Pour que les données apparaissent dans les suites de rapports, (a) la fonction d’identifiant AMO côté serveur doit être configurée pour le compte ou (b) le paramètre au niveau de l’annonceur sur « [!UICONTROL Enable Advertising reporting in Analytics] » doit être activé. En outre, le compte [!DNL Analytics] de l’annonceur doit être configuré pour recevoir des données de Search, Social et Commerce. Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

### onglet [!UICONTROL Upload File]

(Facultatif) Chargez les fichiers de données pour le compte. <!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
