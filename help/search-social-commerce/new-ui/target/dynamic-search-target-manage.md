---
title: Gestion  [!DNL Google Ads]  cibles de recherche dynamiques
description: Découvrez comment créer et gérer  [!DNL Google Ads]  cibles de recherche dynamiques.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 702
ht-degree: 0%

---

# Gestion [!DNL Google Ads] cibles de recherche dynamique

Comptes *[!DNL Google Ads]uniquement*

Vous pouvez créer, modifier et modifier le statut des cibles de recherche dynamique pour les campagnes [!DNL Google Ads] qui utilisent le réseau de recherche.

## Que sont les cibles de recherche dynamique ?

Les cibles de recherche dynamique définissent si le réseau publicitaire utilise l’ensemble ou un sous-ensemble des pages de votre site web pour cibler vos publicités de recherche dynamique. Configurez les cibles de recherche dynamique au niveau du groupe publicitaire . Elles s’appliquent à toutes les annonces de recherche dynamique du même groupe publicitaire.

Selon les paramètres de votre campagne, les cibles de recherche dynamique peuvent être requises ou facultatives :

* Vous devez créer des cibles de recherche dynamique lorsque vous ne spécifiez pas de domaine ni de langue de site web dans la section « [!UICONTROL DSA Options] » de la campagne.

* Vous pouvez éventuellement créer des cibles de recherche dynamique lorsque vous spécifiez un domaine et une langue de site web dans la section « [!UICONTROL DSA Options] » de la campagne.

  [!DNL Google Ads] affiche automatiquement vos annonces de recherche dynamique en fonction du contenu d’un site web spécifié avec ces paramètres.

Pour suivre au mieux les performances, configurez votre campagne avec un groupe publicitaire par cible de recherche dynamique et incluez un groupe publicitaire qui cible tous les critères.

Pour plus d’informations sur [!DNL Google Ads] annonces de recherches dynamiques, consultez https://support.google.com/google-ads/answer/2471185.

## La vue [!UICONTROL Auto Targets]

La vue [!UICONTROL Target] > [!UICONTROL Auto Targets] répertorie toutes les cibles de recherche dynamique dans la vue filtrée pour le compte d’annonceur sélectionné. Vous pouvez également gérer vos cibles de recherche dynamique.

### Actions disponibles

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [Attribuez des contraintes](#constraint-assign) aux cibles de recherche dynamique et [supprimez des contraintes](#constraint-unassign) aux cibles de recherche dynamique

* [Attribuez des classifications de libellé](#classification-values-assign) aux cibles de recherche dynamique et [supprimez des classifications de libellé](#classification-values-remove) aux cibles de recherche dynamique

>[!NOTE]
>
>Vous pouvez créer et modifier de grandes quantités de données de la cible (y compris des étiquettes et des affectations de contraintes) en une seule fois en chargeant des [fichiers de feuille d’envoi groupé](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) et en les publiant sur le réseau publicitaire.

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## Affectation d’une contrainte aux cibles de recherche dynamique sélectionnées à partir de la nouvelle vue [!UICONTROL Auto Targets] {#constraint-assign}

1. Dans le menu principal, cliquez sur **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque cible de recherche dynamique à laquelle vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

## Suppression des contraintes des cibles de recherche dynamique sélectionnées dans la nouvelle vue de [!UICONTROL Auto Targets] {#constraint-unassign}

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque cible de recherche dynamique à partir de laquelle vous annulerez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

## Affectation de valeurs de classification à des cibles de recherche dynamique {#classification-values-assign}

>[!NOTE]
>
>Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque cible de recherche dynamique à laquelle vous attribuez une valeur de libellé.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Pour chaque valeur de classification applicable, procédez comme suit :

   1. Dans la colonne **[!UICONTROL Classifications]** , indiquez la classification :

      * Pour utiliser une classification existante, cliquez sur son nom pour la développer.

      * Pour créer une classification, cliquez sur [!UICONTROL +] dans l’en-tête de colonne. Dans le champ de saisie, saisissez le nom de la classification, puis cliquez sur ![Enregistrer](/help/search-social-commerce/assets/save-checkmark.png "Enregistrer") pour enregistrer immédiatement la classification. Pour utiliser la nouvelle classification, cliquez sur son nom pour la développer.

        Le nom doit comporter [caractères ASCII compris entre 32 et 126](https://www.asciitable.com/) et la longueur maximale est de 27 caractères codés sur un seul octet.

   1. Dans la colonne **[!UICONTROL Value Name]** , indiquez la valeur de la classification sélectionnée :

      * Pour utiliser une valeur existante, sélectionnez-la.

      * Pour créer une valeur, cliquez sur [!UICONTROL +] dans l’en-tête de colonne. Dans le champ de saisie, saisissez la valeur, puis cliquez sur ![Enregistrer](/help/search-social-commerce/assets/save-checkmark.png "Enregistrer") pour enregistrer immédiatement la valeur et la sélectionner par défaut.

        La longueur maximale est de 100 caractères et peut inclure des caractères ASCII et non-ASCII.

1. Cliquez sur **+[!UICONTROL Assign Now]**.

## Supprimer les valeurs de classification de libellé des cibles de recherche dynamique {#classification-values-remove}

La suppression d’une valeur de classification supprime l’association avec le composant de compte et tous ses composants enfants. Les données de rapport pour la valeur de classification ne sont plus disponibles pour ces composants. La suppression d’une valeur de classification ne supprime pas la valeur ni les composants de compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque cible de recherche dynamique à partir de laquelle vous allez supprimer une valeur de libellé.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Cochez la case en regard de chaque valeur de classification à supprimer des entités sélectionnées.

   Pour sélectionner toutes les valeurs attribuées, cliquez sur **[!UICONTROL Select All]**. Pour désélectionner toutes les valeurs affectées, cliquez sur **[!UICONTROL Deselect All]**.

1. Cliquez sur **[!UICONTROL Unassign Selected]**.

>[!MORELIKETHIS]
>
>* [(nouvelle interface utilisateur) Gérer les contraintes pour les unités d’enchères de recherche](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nouvelle interface utilisateur) Gérer les classifications de libellés](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
