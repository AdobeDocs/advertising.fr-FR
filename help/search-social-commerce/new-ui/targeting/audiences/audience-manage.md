---
title: Gestion des audiences
description: Découvrez la bibliothèque d’audiences et comment gérer les audiences prises en charge pour Google Ads et Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%
---
# Gestion des audiences

Comptes *[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

Une audience est un groupe d’utilisateurs que vous pouvez utiliser comme [cible](audience-targets-manage.md) ou [exclusion](audience-exclusions.md) pour les campagnes et groupes publicitaires pris en charge sur le même réseau publicitaire. Le réseau publicitaire détermine la taille que doit avoir une audience pour pouvoir être ciblée.

## À propos de la vue [!UICONTROL Library] {#audience-view-about}

La vue [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Library] répertorie les audiences de l’annonceur sélectionné. Pour afficher les audiences [!DNL Google Ads] et [!DNL Microsoft Advertising], sélectionnez **[!UICONTROL All Other Network]** dans le menu **[!UICONTROL Network]**.

La bibliothèque comprend [!DNL Google Ads] audiences basées sur les données client, sur le marché et similaires, ainsi que des audiences de remarketing [!DNL Microsoft Advertising], de remarketing dynamique, personnalisées, de correspondance client, sur le marché et similaires.

L’affichage des données nécessite l’autorisation [!UICONTROL View Audiences] . La sélection de lignes et la suppression des audiences prises en charge nécessitent l’autorisation [!UICONTROL Edit Audience Library].

### Actions disponibles

<!--
Restricted to internal beta users:

* [Create a customer match audience from a customer data list](#audience-customer-list-create)

* [Create a Google Ads audience from Adobe audiences](#audience-adobe-create)

* [Create a Microsoft Advertising dynamic remarketing audience](#audience-dynamic-create)

* [Update a customer match audience using a customer data list](#audience-customer-list-edit)

* [Edit a dynamic remarketing audience](#audience-dynamic-edit)
-->

* [Supprimer une audience de remarketing dynamique](#audience-delete)

* [Copier toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard)

## Sources de données d’audience {#audience-data-sources}

Vous pouvez utiliser des audiences basées sur les sources de données suivantes :

* **Segments d’audience Adobe :** les annonceurs disposant de comptes Adobe Audience Manager ou Adobe Analytics inscrits peuvent utiliser [!DNL Google Ads] audiences de correspondance client en fonction de leurs segments d’[!DNL Adobe] existants.

  * Pour les annonceurs disposant de comptes [!DNL Analytics] qui ne disposent pas également d’Audience Manager, les audiences utilisent les ID utilisateur de [!DNL Analytics] segments partagés avec Adobe CX Enterprise.

  * Pour les annonceurs disposant de comptes Audience Manager, les audiences utilisent des identifiants d’utilisateurs provenant de segments Audience Manager qui ont pour destination Search, Social et Commerce. Il peut s’agir de segments [!DNL Analytics] publiés sur Adobe CX Enterprise et de segments créés à l’aide de la bibliothèque d’audiences Adobe CX Enterprise.

  Le compte [!DNL Google Ads] doit être [éligible à la correspondance des clients](https://support.google.com/adspolicy/answer/6299717) et avoir choisi les [segments d’ID utilisateur](https://support.google.com/google-ads/answer/9199250). Le compte de l’annonceur dans Search, Social et Commerce doit également être configuré pour permettre la création d’audiences de correspondance client. Contactez l’équipe chargée de votre compte Adobe pour activer la fonctionnalité.

  [!DNL Adobe] données de segment et les fichiers de synchronisation des cookies pour les audiences basées sur les données client sont synchronisés sur [!DNL Google Ads] quotidiennement.

* **Listes d’adresses électroniques Adobe Campaign** l’équipe de votre compte Adobe peut vous aider à configurer un workflow pour créer et mettre à jour une audience de correspondance client [!DNL Google Ads] à partir d’une liste d’adresses électroniques dans [!DNL Campaign]. Le workflow est configuré dans [!DNL Campaign], et non dans la bibliothèque d’audiences. Voir « [Création d’une audience de correspondance client à partir d’une liste d’emails Adobe Campaign](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md) ».

* **Listes de données client :** les annonceurs disposant de comptes [!DNL Google Ads] ou [!DNL Microsoft Advertising] éligibles peuvent utiliser les audiences de correspondance client en fonction de fichiers CSV contenant les identifiants principaux de leurs systèmes de gestion de la relation client (GRC).

* **Listes de remarketing dynamique :** les annonceurs disposant de comptes [!DNL Microsoft Advertising] peuvent utiliser des audiences en fonction des utilisateurs qui ont récemment interagi avec leurs produits, tels que les visiteurs de produits ou les acheteurs précédents. Ces audiences nécessitent la balise de conversion JavaScript et de suivi d’audience du réseau publicitaire sur les pages web appropriées.

  Les audiences de remarketing dynamique peuvent être utilisées avec des campagnes d’achat sur les réseaux de recherche et d’audience pour recibler les utilisateurs avec des annonces de produit, et avec des campagnes de recherche pour recibler les utilisateurs avec des annonces textuelles et des annonces de recherche dynamique.

  >[!NOTE]
  >
  >Les modificateurs d’offres pour les cibles d’audience de remarketing dynamique ne sont pas optimisés dans les portfolios avec le paramètre [!UICONTROL Auto-optimize Bid Adjustment Values] .

>[!NOTE]
>
>Search, Social et Commerce ne stockent pas les données client que vous chargez ni les données client de [!DNL Adobe] segments utilisés pour créer ou modifier une audience.

<!--
Restricted to internal beta users: audience creation and library editing.

## Create a customer match audience from a customer data list {#audience-customer-list-create}

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts that are eligible for customer match only*

For [!DNL Microsoft Advertising], the file can include email addresses. For [!DNL Google Ads], the file can include email addresses, mailing addresses, telephone numbers, user IDs, or mobile device IDs.

Creating and editing library audiences requires the [!UICONTROL Edit Audience Library] permission in addition to internal beta access.

1. Prepare a CSV file with the customer data in the required format.

   First and last names, email addresses, and telephone numbers must be hashed using SHA-256. Follow the network's formatting requirements for the selected identifier type. See the [Google Ads formatting guidelines](https://support.google.com/google-ads/answer/7476159) or the [Microsoft Advertising instructions for preparing customer match lists](https://help.ads.microsoft.com/#apex/ads/en/56921).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. In **[!UICONTROL Data Source]**, select the customer-list option.

1. Enter the **[!UICONTROL Audience Name]** and select the **[!UICONTROL Data Upload Type]**:

   * ([!DNL Microsoft Advertising]) **[!UICONTROL Emails]**.

   * ([!DNL Google Ads]) **[!UICONTROL Emails, Phones, and/or Mailing Addresses]**, **[!UICONTROL User IDs]**, or **[!UICONTROL Mobile Device IDs]**.

     User ID lists are available only to eligible [!DNL Google Ads] advertisers in the U.S. who are opted in for user ID segments.

1. (Mobile device ID lists only) Select the **[!UICONTROL OS Type]** and enter the **[!UICONTROL App ID]**.

   For an Android app, use its package name in [!DNL Google Play], such as `com.example.game` from `https://play.google.com/store/apps/details?id=com.example.game`. For an iOS app, use its application ID from the [!DNL App Store], such as `id284882215`. Your development team can provide the ID.

1. In **[!UICONTROL Select File]**, select the CSV file from your device or network.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. ([!DNL Google Ads]; optional) If you do business in the European Economic Area (EEA) or United Kingdom (UK) and have collected all required user consents, select the consent check box to send the consent status as **[!UICONTROL GRANTED]** for advertising and ad personalization.

   If you leave the check box unselected, the consent status is sent as **[!UICONTROL UNSPECIFIED]**. [!DNL Google Ads] ignores data for EEA and UK users with an unspecified consent status, which can cause data discrepancies and performance issues.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Membership days specify how long a user's cookie stays in the audience. Use the length of time for which you expect the ad to remain relevant. Customer lists don't expire unless you enter a value.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change a setting, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

The ad network may take up to 24 hours to process the file. See the [Google Ads documentation on customer match and its limitations](https://support.google.com/displayvideo/answer/9539301).

## Create Google Ads customer match audiences from Adobe audiences {#audience-adobe-create}

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

Each [!DNL Adobe] audience can be used for only one [!DNL Google Ads] audience. Each new audience has the same name as the original [!DNL Adobe] audience.

1. Complete the prerequisites:

   1. Ask an [!DNL Adobe] administrator or account manager to enable customer match audiences for the advertiser.

   1. Implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=fr){target="_blank"} version 2.0 or higher.

   1. Deploy the following tag as high as possible on the advertiser's webpages from which the audience should be tracked:

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      Replace `Advertising_Cloud_UserID` with the advertiser's unique numeric user ID.

   1. Have an authorized user [configure synchronization with the advertiser's organization account in Adobe CX Enterprise](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Google Ads] and the account.

1. In **[!UICONTROL Data Source]**, select the Adobe audience option.

1. In **[!UICONTROL Adobe Audience]**, select one or more available segments. You can search the list.

   Segments already used for another [!DNL Google Ads] audience aren't available. If you select multiple segments, a separate audience is created for each segment.

1. Select the available customer list user ID option in **[!UICONTROL Audience Type]**.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Remarketing lists have a maximum duration of 540 days. Customer lists don't have a maximum duration; enter 10000 to indicate that the cookie never expires.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Search, Social, & Commerce automatically pushes a [!DNL Google] tracking URL back to each source segment so that [!DNL Google] can track the audience. [!DNL Google] may take up to 24 hours to process the audience.

>[!TIP]
>
>For real-time segmentation, use Audience Manager-created audiences. [!DNL Analytics] segments synced to Adobe CX Enterprise may have smaller populations because they're synced daily. Users who qualify for a segment may not be included until the next day.

## Create a Microsoft Advertising dynamic remarketing audience {#audience-dynamic-create}

You can create multiple dynamic remarketing audiences using the same tracking tag.

1. Implement the [Microsoft Advertising universal event tracking (UET) tag with the required product ID and page type parameters](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85) on the relevant webpages. Identify the tag's name.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Microsoft Advertising] and the account.

1. In **[!UICONTROL Data Source]**, select the dynamic remarketing list option.

1. Enter the **[!UICONTROL Audience Name]**.

1. In **[!UICONTROL Tag Name]**, select the UET tag on the webpages whose users comprise the audience.

1. In **[!UICONTROL Whom to add to your audience]**, select **[!UICONTROL General Visitors]**, **[!UICONTROL Product Searchers]**, **[!UICONTROL Product Viewers]**, **[!UICONTROL Past Buyers]**, or **[!UICONTROL Shopping Cart Abandoners]**.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available. For dynamic remarketing audiences, membership can range from 1-180 days.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Dynamic remarketing audiences are eligible for targeting once they include at least 300 users.

## Update a customer match audience using a customer data list {#audience-customer-list-edit}

You can update customer match audiences created from data files, but not [!DNL Google Ads] audiences created from [!DNL Adobe] audiences. You can add or delete members, or replace all existing members. You can't edit multiple library audiences at once.

1. Prepare a CSV file in the required format, using the same data type as the original list. For mobile device IDs, use the same app and operating system.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. In **[!UICONTROL Select Action]**, select:

   * **[!UICONTROL Add]:** Add members from the uploaded file who aren't already in the audience.

   * **[!UICONTROL Delete]:** Remove members in the uploaded file from the audience.

   * **[!UICONTROL Replace]:** Replace all existing audience members with the uploaded data.

1. In **[!UICONTROL Select File]**, select the CSV file, accept the privacy policies, and configure the applicable consent setting.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.

The ad network may take a while to process audience updates.

## Edit a dynamic remarketing audience {#audience-dynamic-edit}

You can change a [!DNL Microsoft Advertising] dynamic remarketing audience's name, UET tag, and visitor type. You can't change its membership duration or edit multiple library audiences at once.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one dynamic remarketing audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. Edit the **[!UICONTROL Audience Name]**, **[!UICONTROL Tag Name]**, or **[!UICONTROL Whom to add to your audience]**.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.
-->

## Supprimer une audience de remarketing dynamique {#audience-delete}

Vous pouvez supprimer [!DNL Microsoft Advertising] audiences de remarketing dynamique une par une. Vous ne pouvez pas supprimer d’autres types d’audience [!DNL Google Ads] ou [!DNL Microsoft Advertising] de la bibliothèque.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Audiences]**, puis sur l&#39;onglet **[!UICONTROL Library]**.

1. Sélectionnez **[!UICONTROL All Other Network]** dans le menu **[!UICONTROL Network]**.

1. Cochez la case en regard d’une audience de remarketing dynamique.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Gérer les cibles d’audience pour les campagnes et les groupes publicitaires](audience-targets-manage.md)
>* [Gérer les exclusions d’audience pour les campagnes et les groupes publicitaires](audience-exclusions.md)
