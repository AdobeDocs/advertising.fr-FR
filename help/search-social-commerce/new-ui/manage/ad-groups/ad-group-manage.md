---
title: Gestion des groupes publicitaires
description: Découvrez comment créer et gérer des groupes publicitaires.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: fc836f17b53a3708bf881dc62a437d391709a050
workflow-type: tm+mt
source-wordcount: 1676
ht-degree: 0%

---

# Gestion des groupes publicitaires

<!-- Go through all -->

*Fonction*

Un groupe publicitaire comprend un ensemble de publicités et leurs mots-clés associés. Un groupe publicitaire dans une campagne qui cible le réseau d’affichage peut également inclure des emplacements, qui sont des emplacements sur le réseau d’affichage dans lesquels vos publicités peuvent apparaître. Les paramètres du groupe publicitaire, qui s’appliquent à tous les composants du groupe publicitaire, varient selon le réseau publicitaire.

Une fois que vous [rendez un compte de réseau publicitaire accessible via une connexion API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) et que Search, Social et Commerce a synchronisé les données du compte avec le réseau publicitaire, vous pouvez créer des groupes publicitaires pour un [type de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). Vous pouvez également modifier le statut des groupes publicitaires.

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [ Inventaire pris en charge ](/help/search-social-commerce/introduction/supported-inventory.md).

## À propos de la vue [!UICONTROL Ad Groups] {#ad-group-view-about}

La vue [!UICONTROL Manage] > [!UICONTROL Ad Groups] répertorie tous les groupes publicitaires dans la vue filtrée pour le compte publicitaire sélectionné.

### Actions disponibles

* [Création d’un groupe publicitaire](#ad-group-create)

* [Renommer un groupe publicitaire à partir de la ligne](#ad-group-rename)

* [Modifier les paramètres d’un groupe publicitaire](#ad-group-edit)

* [Modifier le statut d’un groupe publicitaire ou le supprimer de la ligne](#ad-group-status)

* [Afficher un graphique des performances dans la vue [!UICONTROL Ad Groups]](#ad-group-performance-graph)

* [Affectez des contraintes d’enchères aux groupes publicitaires et annulez l’affectation des contraintes des groupes publicitaires](#ad-group-constraints)

* [Attribuez des classifications d’étiquettes à des groupes publicitaires et supprimez des classifications d’étiquettes des groupes publicitaires](#ad-group-classifications)

* [Gérer les rapports de vue de données à partir de la vue [!UICONTROL Ad Groups]](#ad-group-reports)

## Création d’un groupe publicitaire {#ad-group-create}

>[!TIP]
>
>Pour créer un grand nombre de groupes publicitaires à la fois, utilisez <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [feuilles d’envoi groupé campaign](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Cliquez sur **[!UICONTROL Create Ad Group]**.

1. Spécifiez les paramètres du groupe publicitaire [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md) ou [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md).

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Si nécessaire, cliquez sur le **[!UICONTROL Edit]** ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") et modifiez les paramètres du groupe publicitaire.

1. Cliquez sur **[!UICONTROL Create]**.

Par la suite, vous pouvez éventuellement remplacer les enchères au niveau du groupe publicitaire en définissant les enchères pour des mots-clés ou des emplacements individuels dans le groupe publicitaire.

## Renommer un groupe publicitaire {#ad-group-rename}

Renommez rapidement un groupe publicitaire sans ouvrir les paramètres complets du groupe publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Placez le curseur sur la ligne du groupe publicitaire et cliquez sur **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Modifiez le nom, puis cliquez sur **[!UICONTROL Apply]**.

## Modifier les paramètres d’un groupe publicitaire {#ad-group-edit}

Vous pouvez modifier les paramètres de groupes d’annonces individuels. Vous pouvez également modifier certains champs pour plusieurs groupes publicitaires à la fois, y compris certains détails du groupe publicitaire, les options budgétaires et les options d’URL communes à tous les groupes publicitaires sélectionnés.

>[!TIP]
>
>Vous pouvez également modifier des données en bloc à l’aide de <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [feuilles d’envoi groupé campaign](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Effectuez l’une des opérations suivantes :

   * Placez le curseur sur le nom de l’entité et cliquez sur **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Cochez la case en regard du groupe publicitaire . Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les paramètres du groupe publicitaire [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md) ou [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md).

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Si nécessaire, cliquez sur le **[!UICONTROL Edit]** ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") et modifiez les paramètres du groupe publicitaire.

1. Cliquez sur **[!UICONTROL Update]**.

## Modifier le statut d’un groupe publicitaire {#ad-group-status}

Modifiez rapidement le statut d’un groupe publicitaire sans ouvrir les paramètres complets du groupe publicitaire.

Vous pouvez suspendre n’importe quel groupe publicitaire actif sur un réseau publicitaire pris en charge afin de désactiver les enchères sur ce réseau. Vous pouvez ensuite reprendre les enchères en redéfinissant leur statut sur Actif.

Vous pouvez également supprimer n’importe quel groupe publicitaire actif ou en pause. Les groupes publicitaires supprimés sont supprimés du réseau publicitaire. Ils sont toujours visibles lorsque vous les incluez dans le filtre de données, mais vous ne pouvez pas les modifier.

### Activer ou mettre en pause un groupe publicitaire

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Placez le curseur sur la ligne du groupe publicitaire et cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") en regard de la colonne [!UICONTROL Status].

1. Modifiez le statut :

   * Pour activer un groupe publicitaire en pause, sélectionnez **[!UICONTROL Active]**.

   * Pour mettre en pause un groupe publicitaire actif, sélectionnez **[!UICONTROL Paused]**.

### Suppression d’un groupe publicitaire

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Effectuez l’une des opérations suivantes :

   * Placez le curseur sur la ligne du groupe publicitaire et cliquez sur **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Placez le curseur sur la ligne du groupe publicitaire et cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") en regard de la colonne [!UICONTROL Status]. Sélectionnez **[!UICONTROL Deleted]**.

## Gérer les affectations de contraintes d’offre pour les groupes publicitaires {#ad-group-constraints}

Chaque entité ne peut avoir qu&#39;une seule contrainte. Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire d’affecter des contraintes aux entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

L’annulation de l’affectation d’une contrainte supprime l’association avec les composants de compte et tous leurs composants enfants, et les données de rapport pour la contrainte ne sont plus disponibles pour ces composants. L’annulation de l’affectation d’une contrainte ne supprime pas la contrainte ni les composants de compte eux-mêmes.

### Affecter une contrainte d&#39;offre à des groupes d&#39;annonces sélectionnés à partir de la nouvelle vue [!UICONTROL Ad Groups]

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Cochez la case en regard de chaque groupe d’annonces auquel vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

### Affecter une contrainte d&#39;offre à des unités d&#39;offre de recherche sélectionnées à partir des vues de [!UICONTROL Campaigns] héritées

1. Dans **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, sélectionnez la vue du composant Compte .

1. Cochez la case en regard de chaque ligne pertinente.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte applicable.

1. (Facultatif) Saisissez des détails supplémentaires :

   1. En regard de [!UICONTROL Additional Details], cliquez sur **[!UICONTROL Open]** pour développer les détails.

   1. Saisissez un **[!UICONTROL Project Name]** facultatif et/ou un **[!UICONTROL Description]** facultatif.

1. Cliquez sur **[!UICONTROL Save]**.

### Supprimer les contraintes d&#39;enchères des groupes d&#39;annonces sélectionnés de la nouvelle vue [!UICONTROL Ad Groups]

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Cochez la case en regard de chaque groupe d’annonces duquel vous annulerez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

### Supprimer les contraintes d&#39;offre des unités d&#39;offre de recherche des vues de [!UICONTROL Campaigns] héritées

>[!NOTE]
>
>Pour supprimer une contrainte, ce qui la rend indisponible pour une utilisation ultérieure, consultez « Supprimer des contraintes pour les unités d’offres de recherche » dans le chapitre du guide d’optimisation sur « Contraintes d’offres », disponible dans Search, Social et Commerce.

1. Dans **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, sélectionnez la vue du composant Compte .

1. Cochez la case en regard de chaque composant duquel vous souhaitez supprimer la contrainte.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Dans la boîte de dialogue de confirmation, sélectionnez **[!UICONTROL Yes, Unassign]**.

## Attribuer des classifications d’étiquettes à des groupes d’annonces {#ad-group-classifications}

>[!NOTE]
>
>Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

### Attribuer des valeurs de classification à des groupes d’annonces

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Cochez la case en regard de chaque groupe d’annonces auquel vous affecterez une valeur de libellé.

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

### Supprimer les valeurs de classification de libellé des groupes publicitaires

La suppression d’une valeur de classification supprime l’association avec le composant de compte et tous ses composants enfants. Les données de rapport pour la valeur de classification ne sont plus disponibles pour ces composants. La suppression d’une valeur de classification ne supprime pas la valeur ni les composants de compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Cochez la case en regard de chaque groupe publicitaire duquel vous supprimez une valeur de libellé.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Cochez la case en regard de chaque valeur de classification à supprimer des entités sélectionnées.

   Pour sélectionner toutes les valeurs attribuées, cliquez sur **[!UICONTROL Select All]**. Pour désélectionner toutes les valeurs affectées, cliquez sur **[!UICONTROL Deselect All]**.

1. Cliquez sur **[!UICONTROL Unassign Selected]**.

## Afficher un graphique des performances dans la vue [!UICONTROL Ad Groups] {#ad-group-performance-graph}

Ouvrez et configurez un graphique de performances avec jusqu’à trois mesures totalisées pour tous les groupes publicitaires de la vue pour la période spécifiée.

### Affichage d’un graphique de performances

1. Au-dessus du tableau de données, cliquez sur ![Graphiques](/help/search-social-commerce/assets/charts.png "Graphiques").

1. (Facultatif) Spécifiez la devise et jusqu’à trois mesures à inclure dans le graphique.

### Masquage d’un graphique de performances visible

* Au-dessus du tableau de données, cliquez sur ![Graphiques](/help/search-social-commerce/assets/charts.png "Graphiques").

## Gérer les rapports de vue de données à partir de la vue [!UICONTROL Ad Groups] {#ad-group-reports}

Générez un rapport qui inclut les lignes de données d’un ou de plusieurs groupes publicitaires dans la vue [!UICONTROL Ad Groups], puis téléchargez le rapport sous la forme d’un fichier de feuille de calcul Excel Microsoft (format XLXS). Le rapport inclut toutes les colonnes visibles dans la vue.

Vous pouvez supprimer n’importe quel rapport généré.

Consultez également les sections « >* [ (interface utilisateur héritée) Télécharger des données à partir d’une vue de gestion de campagne »](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md) et « [ (interface utilisateur héritée) Supprimer un rapport de données de performances ou un fichier de feuille d’envoi groupé du menu [!UICONTROL Downloads] »](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).

### Générer un rapport avec les lignes de données filtrées

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Indiquez les groupes publicitaires dont vous souhaitez télécharger les données :

   * Pour télécharger des données relatives à des groupes d’annonces spécifiques, cochez les cases en regard des groupes d’annonces.

   * Pour télécharger des données pour tous les groupes d’annonces, il n’est pas nécessaire de cocher des cases. Tous les groupes publicitaires sont inclus par défaut.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans les paramètres de [!UICONTROL Grid Reports], saisissez un nom de rapport unique, puis cliquez sur **[!UICONTROL Generate]**.

   Par défaut, le fichier est nommé « ad group_YYYYMMDD_NNNN », où « NNNN » correspond au numéro de tâche séquentiel (par exemple, « ad group_20250402_1326 »).

   Le fichier est ajouté à la liste de [!UICONTROL Recently Generated].

1. (Facultatif) Pour télécharger le fichier une fois l’opération terminée, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Télécharger un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Supprimer un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") en regard du nom du fichier.

>[!MORELIKETHIS]
>
>* [Gérer les contraintes pour les unités d’offres de recherche](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gérer les affectations de contrainte pour les campagnes](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Gérer les affectations de contraintes pour les mots-clés](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Gérer les affectations de contrainte pour les emplacements](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [ (interface utilisateur héritée) Télécharger des données à partir d’une vue de gestion de campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(interface utilisateur héritée) Supprimez un rapport de données de performances ou un fichier de feuille d’envoi groupé du menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] paramètres du groupe publicitaire](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] paramètres du groupe publicitaire](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md)
>* [[!DNL LY Ads] paramètres du groupe publicitaire](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md)
>* [[!DNL Microsoft Advertising] paramètres du groupe publicitaire](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] paramètres du groupe publicitaire](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md)
