---
title: Gestion des cibles d’audience pour les campagnes et les groupes publicitaires
description: Découvrez comment gérer les cibles d’audience et leurs ajustements d’enchères pour Google Ads et Microsoft Advertising.
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
source-wordcount: '562'
ht-degree: 0%
---
# Gestion des cibles d’audience pour les campagnes et les groupes publicitaires

Comptes *[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

[!DNL Google Ads] campagnes et groupes publicitaires, ainsi que les groupes publicitaires [!DNL Microsoft Advertising], peuvent cibler des [audiences](audience-manage.md) spécifiques du même réseau publicitaire. Le réseau publicitaire détermine la taille que doit avoir une audience pour pouvoir être ciblée.

Une audience cible associe une audience existante à une campagne ou à un groupe publicitaire. Vous pouvez modifier l&#39;ajustement des enchères et le statut des cibles existantes.

>[!NOTE]
>
>[Les exclusions d’audience](audience-exclusions.md) remplacent toujours les cibles.

## À propos de la vue [!UICONTROL Targets] {#audience-targets-view-about}

La vue [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets] répertorie les cibles d’audience dans la vue filtrée pour l’annonceur sélectionné.

L’affichage des données nécessite l’autorisation [!UICONTROL View Audiences] . La modification, le changement d’état et la suppression de cibles nécessitent l’autorisation [!UICONTROL Edit Audience Targets].

### Actions disponibles

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [Modifier les ajustements et le statut des enchères de la cible de l’audience](#audience-targets-edit)

* [Modifier le statut des cibles d’audience ou les supprimer](#audience-targets-status)

* [Copier toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## Modifier les ajustements et le statut des enchères de la cible de l’audience {#audience-targets-edit}

Vous pouvez modifier une ou plusieurs cibles d’audience à la fois. Vos modifications s&#39;appliquent à toutes les cibles sélectionnées.

>[!NOTE]
>
>Search, Social et Commerce optimise automatiquement les conditions commerciales d’enchères lorsque la campagne parent utilise la stratégie d’enchères CPC et se trouve dans un portefeuille configuré pour optimiser automatiquement les valeurs d’ajustement d’enchère pour les cibles d’audience. Les modificateurs d’offres pour [!DNL Microsoft Advertising] cibles d’audience de remarketing dynamique ne sont pas optimisés.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Audiences]**, puis sur l&#39;onglet **[!UICONTROL Targets]**.

1. Cochez la case en regard de chaque cible à modifier.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Modifiez le **[!UICONTROL Bid Modifier]** ou le **[!UICONTROL Status]**, ou les deux. Voir [paramètres d’édition](#audience-targets-edit-settings).

   Laissez un champ inchangé pour conserver la valeur existante.

1. (Facultatif) Développez **[!UICONTROL ADDITIONAL DETAILS]** et saisissez un **[!UICONTROL Project Name]** et un **[!UICONTROL Description]**.

1. Cliquez sur **[!UICONTROL Save]**.

Vous pouvez également modifier l&#39;ajustement d&#39;enchères d&#39;une seule cible directement dans le tableau de données en cliquant sur sa valeur dans la colonne **[!UICONTROL Bid Adjustment]**.

## Modifier le statut des cibles d’audience ou les supprimer {#audience-targets-status}

Vous pouvez suspendre une cible d’audience active afin de désactiver les enchères pour cette cible, puis reprendre les enchères en l’activant. Vous pouvez également supprimer des cibles actives ou en pause.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Audiences]**, puis sur l&#39;onglet **[!UICONTROL Targets]**.

1. (Facultatif) Filtrez la liste pour inclure des cibles d’audience spécifiques.

1. Cochez la case en regard de chaque cible dont vous souhaitez modifier le statut.

1. Dans la barre d’outils des actions en bloc, cliquez sur l’un des éléments suivants :

   * **[!UICONTROL Activate]** d’activer les cibles sélectionnées.

   * **[!UICONTROL Pause]** de mettre en pause les cibles sélectionnées.

   * **[!UICONTROL Delete]** de supprimer les cibles sélectionnées.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

## Paramètres de modification de la cible de l’audience {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]:** Modification de l’ajustement d’offre d’audience :

* *[!UICONTROL Set To]:* Remplacer l&#39;ajustement d&#39;offre existant par le pourcentage spécifié.

* *[!UICONTROL Increase]:* augmente la valeur existante selon le pourcentage spécifié.

* *[!UICONTROL Decrease]:* permet de réduire la valeur existante du pourcentage spécifié.

Pour [!UICONTROL Increase] et [!UICONTROL Decrease], saisissez une valeur non négative.

Pour une valeur définie, 0 % n’ajuste pas l’enchère. Les autres valeurs prises en charge sont comprises entre -90 % et 900 %. Par exemple, si l’enchère au niveau du mot-clé est de 1 USD et que l’ajustement de l’enchère de l’audience est de 50 %, l’enchère pour cette audience passe à 1,50 USD.

**[!UICONTROL Status]:** sélectionnez **[!UICONTROL Active]** pour activer les enchères ou **[!UICONTROL Paused]** pour désactiver les enchères pour la cible.

>[!MORELIKETHIS]
>
>* [Gérer les audiences](audience-manage.md)
>* [Gérer les exclusions d’audience pour les campagnes et les groupes publicitaires](audience-exclusions.md)
