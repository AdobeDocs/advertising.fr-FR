---
title: (Nouvelle interface utilisateur) Gérer  [!DNL Naver]  comptes pour le suivi uniquement
description: Découvrez comment configurer et gérer les détails du compte dans la nouvelle interface utilisateur d’un  [!DNL Naver] .
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gérer les comptes [!DNL Naver] pour le suivi uniquement

*Fonction Beta*

Vous trouverez ci-dessous des instructions pour gérer les [[!DNL Naver] comptes](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) afin de suivre, de générer des rapports et de visualiser les performances des publicités que vous achetez directement à partir du réseau publicitaire. Search, Social et Commerce ne synchronisent pas les données avec le réseau publicitaire, ne fournissent pas d’enchères automatisées et ne fournissent aucun type d’optimisation ou de simulation.

Pour plus d’informations sur les fonctionnalités disponibles, reportez-vous à « [Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) ».

## Créer un compte réseau publicitaire {#create-account}

Pour activer le suivi d’un compte, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et avec le statut *activé*.

>[!NOTE]
>
>Pour créer un compte sur le réseau publicitaire, accédez au site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Cliquez sur **[!UICONTROL Create Account]**.

1. Cliquez sur le nom du réseau publicitaire, puis sur **[!UICONTROL Next]**.

1. Spécifiez les [paramètres du compte](#account-settings-naver) :

   1. Dans l’onglet **[!UICONTROL Enter Account Details]** , spécifiez les paramètres généraux du compte.

   1. (Annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md)) Cliquez sur l’onglet **[!UICONTROL Set up Adobe Analytics]** et sélectionnez toutes les suites de rapports [!DNL Analytics] à utiliser pour le suivi et les rapports d’activité de campagne.

1. Cliquez sur **[!UICONTROL Save]**.

## Modifier les détails du compte réseau publicitaire {#edit-account}

Pour modifier le nom du compte, son statut ou les suites de rapports [!DNL Analytics] à utiliser pour le suivi et la création de rapports, modifiez les détails du compte.

>[!NOTE]
>
>Pour modifier un compte réel sur le réseau publicitaire, accédez au site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Sélectionnez le compte de l’une des manières suivantes :

   * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

   * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

1. Modifiez les [paramètres du compte](#account-settings-api) :

   1. (Facultatif) Dans l’onglet **[!UICONTROL Account Details]** , modifiez les détails du compte.

   1. (Facultatif ; annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md)) Cliquez sur l’onglet **[!UICONTROL Set up Adobe Analytics]** et modifiez les suites de rapports [!DNL Analytics] à utiliser pour le suivi et les rapports d’activité de campagne.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Cliquez sur **[!UICONTROL Save]**.

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## Paramètres du compte réseau publicitaire {#account-settings-api}

### onglet [!UICONTROL Account Details]

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** nom à afficher pour le compte dans Search, Social et Commerce.

>[!NOTE]
>
>Si vous disposez d’une intégration Search, Social et Commerce-Adobe Analytics et que vous modifiez le nom du compte de recherche, demandez à l’équipe chargée de votre compte Adobe de mettre à jour le mappage.

**[!UICONTROL Network Account ID]:** ID de compte attribué par le réseau publicitaire.

**[!UICONTROL Currency]:** abréviation de la devise utilisée pour le compte.

**[!UICONTROL Time Zone]:** Fuseau horaire de l’annonceur.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled] :** Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’il est pris en charge) et diffuse des enchères automatisées et/ou des budgets de campagne pour les campagnes des portfolios.

## onglet [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md) ; facultatif) Une ou plusieurs suites de rapports Analytics auxquelles Search, Social et Commerce envoient les données que vous chargez pour le réseau publicitaire, y compris les classifications d’entité et les données de clic pour le compte.

Pour que les données apparaissent dans les suites de rapports, (a) la fonction d’identifiant AMO côté serveur doit être configurée pour le compte ou (b) le paramètre au niveau de l’annonceur sur « [!UICONTROL Enable Advertising reporting in Analytics] » doit être activé. En outre, le compte [!DNL Analytics] de l’annonceur doit être configuré pour recevoir des données de Search, Social et Commerce. Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [Implémentation  [!DNL Naver]  comptes de tracking uniquement](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [À propos des comptes de réseau publicitaire](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
