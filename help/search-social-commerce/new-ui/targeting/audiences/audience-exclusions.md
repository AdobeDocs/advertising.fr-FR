---
title: Gestion des exclusions d’audience pour les campagnes et les groupes publicitaires
description: Découvrez les exclusions d’audience Google Ads et Microsoft Advertising, y compris comment supprimer les exclusions Google Ads.
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
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%
---
# Gestion des exclusions d’audience pour les campagnes et les groupes publicitaires

Comptes *[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

Une exclusion d’audience empêche les publicités d’une campagne ou d’un groupe publicitaire d’être présentées aux utilisateurs dans une [audience](audience-manage.md) spécifique.

Pour les comptes [!DNL Google Ads], vous pouvez exclure n’importe quel type d’audience. Pour les comptes [!DNL Microsoft Advertising], vous ne pouvez exclure que les audiences de remarketing dynamique.

>[!NOTE]
>
>Les exclusions remplacent toujours [cibles d’audience](audience-targets-manage.md).

## À propos de la vue [!UICONTROL Exclusions] {#audience-exclusions-view-about}

La vue [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions] répertorie les exclusions d’audience dans la vue filtrée pour l’annonceur sélectionné.

L’affichage des données nécessite l’autorisation [!UICONTROL View Audiences] . La sélection de lignes et la suppression des exclusions prises en charge nécessitent l’autorisation [!UICONTROL Edit Audience Exclusions].

### Actions disponibles

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [Supprimer les exclusions d’audience](#audience-exclusions-delete)

* [Copier toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## Supprimer les exclusions d’audience {#audience-exclusions-delete}

*[!DNL Google Ads]exclusions uniquement*

Vous pouvez supprimer une ou plusieurs exclusions d’audience [!DNL Google Ads]. La suppression des exclusions de [!DNL Microsoft Advertising] n’est pas prise en charge dans cet affichage.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Audiences]**, puis sur l&#39;onglet **[!UICONTROL Exclusions]**.

1. (Facultatif) Filtrez la liste pour inclure des exclusions d’audience spécifiques.

1. Cochez la case en regard de chaque exclusion de [!DNL Google Ads] à supprimer. N’incluez pas les exclusions d’un autre réseau publicitaire dans la sélection.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Gérer les audiences](audience-manage.md)
>* [Gérer les cibles d’audience pour les campagnes et les groupes publicitaires](audience-targets-manage.md)
