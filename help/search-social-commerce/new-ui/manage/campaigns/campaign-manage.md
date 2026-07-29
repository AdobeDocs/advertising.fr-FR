---
title: Gestion des campagnes
description: Découvrez comment créer et gérer des campagnes publicitaires.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 7dc3ea3fe1fcb701d9d064b184922ed96626cd4a
workflow-type: tm+mt
source-wordcount: 2285
ht-degree: 0%

---

# Gestion des campagnes

*Fonction*

Une campagne est le composant principal d’un compte réseau publicitaire. Pour la plupart des types de campagne, il se compose d’un ensemble de groupes ou de visionneuses d’annonces. Les paramètres de la campagne comprennent les paramètres de budget de la campagne, les cibles des publicités et les paramètres de suivi facultatifs pour toutes les publicités de la campagne. Les paramètres de tracking au niveau de la campagne remplacent les paramètres au niveau du compte, mais ils peuvent eux-mêmes être remplacés à un niveau inférieur.

Une fois que vous [rendez un compte de réseau publicitaire accessible via une connexion API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) et que Search, Social et Commerce a synchronisé les données du compte avec le réseau publicitaire, vous pouvez créer de nouvelles campagnes avec [types de campagnes pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). Vous pouvez également modifier le statut des campagnes.

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [ Inventaire pris en charge ](/help/search-social-commerce/introduction/supported-inventory.md).

## À propos de la vue [!UICONTROL Campaigns] {#campaign-view-about}

La vue [!UICONTROL Manage] > [!UICONTROL Campaigns] répertorie toutes les campagnes dans la vue filtrée pour le compte d’annonceur sélectionné. Vous pouvez ouvrir une liste de groupes publicitaires dans la campagne en cliquant sur le nom de la campagne.

Lorsque vous ajoutez et modifiez des données de campagne dans les vues [!UICONTROL Campaigns], Search, Social et Commerce envoie immédiatement les modifications de données au réseau publicitaire. Search, Social et Commerce extraient également les données de structure de campagne et cliquent sur les données quotidiennement, ou plus souvent lorsque de nouvelles campagnes sont détectées. Pour tous les réseaux publicitaires synchronisés, vous pouvez également synchroniser les comptes à la demande si nécessaire.

Search, Social et Commerce extraient les données de performances toutes les heures des comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] synchronisés, et tous les jours pour les autres comptes réseau publicitaire synchronisés.

### Actions disponibles

* [Création d’une campagne](#campaign-create)

* [Renommer une campagne à partir de la ligne](#campaign-rename)

* [Modifier les paramètres de la campagne](#campaign-edit)

* [Modifier le statut d’une campagne ou la supprimer à partir de la ligne](#campaign-status)

* [Affectation de campagnes à un portfolio et suppression de campagnes d’un portfolio](#campaign-portfolio)

* [Afficher un graphique des performances dans la vue [!UICONTROL Campaigns]](#campaign-performance-graph)

* [Affectez des contraintes d’enchères aux campagnes et annulez l’affectation des contraintes des campagnes](#campaign-constraints)

* [Affectez des contraintes de cible aux campagnes et annulez l’affectation des contraintes de cible des campagnes](#campaign-target-constraints)

* [Attribuez des classifications de libellé aux campagnes et supprimez des classifications de libellé des campagnes](#campaign-classifications)

* [Gérer les rapports de vue de données à partir de la vue [!UICONTROL Campaigns]](#campaign-reports)

## Création d’une campagne {#campaign-create}

>[!NOTE]
>
>* Avant de créer une campagne, [implémentez les balises de suivi des conversions](/help/search-social-commerce/tracking/conversion-tracking-about.md) dans les pages web de l’annonceur.
>* Pour créer un grand nombre de campagnes à la fois, utilisez <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [feuilles d’envoi groupé campaign](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cliquez sur **[!UICONTROL Create Campaign]**.

1. Spécifiez les paramètres de la campagne [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yahoo-japan.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-microsoft.md) ou [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yandex.md).

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Si nécessaire, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") et modifiez les paramètres de la campagne.

1. Cliquez sur **[!UICONTROL Create]**.

Selon le réseau publicitaire sur lequel la campagne a été créée, vous devrez peut-être créer les groupes publicitaires et les publicités associés avant que la campagne ne soit envoyée au réseau publicitaire.

## Renommer une campagne {#campaign-rename}

Renommez rapidement une campagne sans ouvrir l’ensemble des paramètres de la campagne.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Placez le curseur au-dessus de la ligne de campagne, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Modifiez le nom, puis cliquez sur **[!UICONTROL Apply]**.

## Modifier les paramètres de la campagne {#campaign-edit}

Vous pouvez modifier les paramètres de campagnes individuelles. Vous pouvez également modifier certains champs de plusieurs campagnes à la fois, notamment certains détails de la campagne, les options de budget et les options d’URL communes à toutes les campagnes sélectionnées.

>[!TIP]
>
>Vous pouvez également modifier des données en bloc à l’aide de <!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [feuilles d’envoi groupé campaign](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * Placez le curseur sur le nom de l’entité et cliquez sur **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Cochez la case en regard de la campagne. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yahoo-japan.md), <!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-meta.md), --> Paramètres de la campagne [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-microsoft.md) ou [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yandex.md).

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Si nécessaire, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") et modifiez les paramètres de la campagne.

1. Cliquez sur **[!UICONTROL Update]**.

Selon le réseau publicitaire sur lequel la campagne a été créée, il se peut que la campagne doive inclure des groupes publicitaires et des publicités avant d’être envoyée au réseau publicitaire.

## Modifier le statut d’une campagne {#campaign-status}

Modifier rapidement le statut d’une campagne sans ouvrir l’ensemble des paramètres de la campagne.

Vous pouvez suspendre n’importe quelle campagne active sur un réseau publicitaire pris en charge afin de désactiver les enchères associées. Vous pouvez ensuite reprendre les enchères en redéfinissant leur statut sur Actif.

Vous pouvez également supprimer toute campagne active ou en pause. Les campagnes supprimées sont supprimées du réseau publicitaire. Ils sont toujours visibles lorsque vous les incluez dans le filtre de données, mais vous ne pouvez pas les modifier.

### Activer ou mettre en pause une campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Placez le curseur au-dessus de la ligne de la campagne et cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") en regard de la colonne [!UICONTROL Status].

1. Modifiez le statut :

   * Pour activer une campagne en pause, sélectionnez **[!UICONTROL Active]**.

   * Pour suspendre une campagne active, sélectionnez **[!UICONTROL Paused]**.

### Suppression d’une campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * Placez le curseur au-dessus de la ligne de campagne, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Placez le curseur au-dessus de la ligne de la campagne et cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") en regard de la colonne [!UICONTROL Status]. Sélectionnez **[!UICONTROL Deleted]**.

## Affectation de campagnes à un portfolio {#campaign-portfolio}

L’affectation d’une campagne à un portfolio optimisé permet à Search, Social et Commerce d’optimiser les enchères, les budgets de campagne et les cibles de stratégie d’enchères pour les mots-clés et les annonces de la campagne. Vous pouvez affecter des campagnes à un portfolio à partir de la vue [!UICONTROL Campaigns], lorsque vous créez le portfolio ou en modifiant les paramètres d’un portfolio.

L’optimisation ne s’applique pas à tous les types de campagne et réseaux publicitaires. Consultez la liste des [types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) que vous pouvez inclure dans un portfolio. Vérifiez également la prise en charge de l’optimisation [ pour chaque stratégie d’enchères de campagne](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

>[!NOTE]
>
>Chaque campagne ne peut être affectée qu&#39;à un seul portefeuille. Si vous affectez une campagne déjà associée à un autre portefeuille à un nouveau portefeuille, elle est supprimée du portefeuille d’origine.

### Affectation de campagnes à un portfolio existant à partir de la vue [!UICONTROL Campaigns]

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à affecter à un seul portefeuille.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]** .

1. Sélectionnez le portefeuille.

1. Cliquez sur **[!UICONTROL Assign Now]**.

### Affecter des campagnes à un nouveau portfolio à partir de la vue [!UICONTROL Campaigns]

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne pour laquelle vous souhaitez créer le nouveau portefeuille.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**.

1. Dans l’écran [!UICONTROL Create Portfolio], spécifiez les paramètres du portfolio.

   Les campagnes que vous avez sélectionnées précédemment sont déjà affectées à la campagne. Vous pouvez éventuellement modifier la liste des campagnes pour le portefeuille.

   Pour plus d’informations sur les paramètres du portfolio, consultez le Guide d’optimisation , disponible dans Search, Social et Commerce.

1. Cliquez sur **[!UICONTROL Review and Save]**.

### Modifier les affectations de campagne pour un portefeuille à partir de la vue [!UICONTROL Portfolios]

Lorsque vous supprimez une campagne d’un portefeuille, Search, Social et Commerce ne peuvent pas optimiser les enchères, les budgets de campagne ni les cibles de stratégie d’enchères pour cette campagne.

L’action est consignée dans l’historique des modifications du portefeuille.

Pour plus d’informations sur l’optimisation, consultez le Guide d’optimisation , disponible dans Search, Social et Commerce.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Cochez la case en regard du portefeuille.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Dans les paramètres du portfolio, accédez à la section [!UICONTROL Assign Campaigns] et modifiez les affectations de campagne.

   Pour plus d’informations sur les paramètres du portfolio, consultez le Guide d’optimisation , disponible dans Search, Social et Commerce.

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres et apportez les modifications nécessaires, puis cliquez sur **[!UICONTROL Save]**.

## Gérer les affectations de contrainte d’offre pour les campagnes {#campaign-constraints}

Chaque entité ne peut avoir qu&#39;une seule contrainte. Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire d’affecter des contraintes aux entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

L’annulation de l’affectation d’une contrainte supprime l’association avec les composants de compte et tous leurs composants enfants, et les données de rapport pour la contrainte ne sont plus disponibles pour ces composants. L’annulation de l’affectation d’une contrainte ne supprime pas la contrainte ni les composants de compte eux-mêmes.

>[!NOTE]
>
>Les contraintes actives limitent les enchères uniquement pour les unités d’offre affectées dans les portefeuilles optimisés au niveau des mots-clés hérités. Elles sont ignorées pour les unités d&#39;enchères qui se trouvent dans des portefeuilles actifs, dans des portefeuilles hybrides ou qui ne se trouvent pas dans des portefeuilles.

### Affecter une contrainte d’offre à des campagnes sélectionnées à partir de la nouvelle vue [!UICONTROL Campaigns]

Vous pouvez affecter une seule contrainte à une ou plusieurs campagnes.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à laquelle vous affecterez une seule contrainte.

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

### Supprimer les contraintes d’enchères des campagnes sélectionnées dans la nouvelle vue [!UICONTROL Campaigns]

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à partir de laquelle vous annulerez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

### Supprimer les contraintes d&#39;offre des unités d&#39;offre de recherche des vues de [!UICONTROL Campaigns] héritées

>[!NOTE]
>
>Pour supprimer une contrainte, ce qui la rend indisponible pour une utilisation ultérieure, consultez « Supprimer des contraintes pour les unités d’offres de recherche » dans le chapitre du guide d’optimisation sur « Contraintes d’offres », disponible dans Search, Social et Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. Dans **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, sélectionnez la vue du composant Compte .

1. Cochez la case en regard de chaque composant duquel vous souhaitez supprimer la contrainte.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Dans la boîte de dialogue de confirmation, sélectionnez **[!UICONTROL Yes, Unassign]**.

## Gérer les affectations de contraintes de cible pour les campagnes {#campaign-target-constraints}

### Affecter une contrainte de cible à des campagnes sélectionnées à partir de la nouvelle vue [!UICONTROL Campaigns]

Vous pouvez affecter une seule contrainte de cible à une ou plusieurs campagnes.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à laquelle vous affecterez une seule contrainte cible.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

### Supprimer les contraintes de cible des campagnes sélectionnées à partir de la nouvelle vue [!UICONTROL Campaigns]

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à partir de laquelle vous annulerez l’affectation d’une contrainte cible.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

## Attribuer des classifications de libellés aux campagnes {#campaign-classifications}

>[!NOTE]
>
>Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

### Attribuer des valeurs de classification à des campagnes

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à laquelle vous affecterez une valeur de libellé.

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

### Supprimer les valeurs de classification de libellé des campagnes

La suppression d’une valeur de classification supprime l’association avec le composant de compte et tous ses composants enfants. Les données de rapport pour la valeur de classification ne sont plus disponibles pour ces composants. La suppression d’une valeur de classification ne supprime pas la valeur ni les composants de compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à partir de laquelle vous allez supprimer une valeur de libellé.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Cochez la case en regard de chaque valeur de classification à supprimer des entités sélectionnées.

   Pour sélectionner toutes les valeurs attribuées, cliquez sur **[!UICONTROL Select All]**. Pour désélectionner toutes les valeurs affectées, cliquez sur **[!UICONTROL Deselect All]**.

1. Cliquez sur **[!UICONTROL Unassign Selected]**.

## Afficher un graphique des performances dans la vue [!UICONTROL Campaigns] {#campaign-performance-graph}

Ouvrez et configurez un graphique de performances avec jusqu’à trois mesures totalisées sur toutes les campagnes de la vue pour la période spécifiée.

### Affichage d’un graphique de performances

1. Au-dessus du tableau de données, cliquez sur ![Graphiques](/help/search-social-commerce/assets/charts.png "Graphiques").

1. (Facultatif) Spécifiez la devise et jusqu’à trois mesures à inclure dans le graphique.

### Masquage d’un graphique de performances visible

* Au-dessus du tableau de données, cliquez sur ![Graphiques](/help/search-social-commerce/assets/charts.png "Graphiques").

## Gérer les rapports de vue de données à partir de la vue [!UICONTROL Campaigns] {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

Générez un rapport qui inclut les lignes de données d&#39;une ou plusieurs campagnes dans la vue [!UICONTROL Campaigns], puis téléchargez le rapport sous la forme d&#39;un fichier de feuille de calcul Excel Microsoft (format XLXS). Le rapport inclut toutes les colonnes visibles dans la vue.

Vous pouvez supprimer n’importe quel rapport généré.

Consultez également les sections « >* [ (interface utilisateur héritée) Télécharger des données à partir d’une vue de gestion de campagne »](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md) et « [ (interface utilisateur héritée) Supprimer un rapport de données de performances ou un fichier de feuille d’envoi groupé du menu [!UICONTROL Downloads] »](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).

### Générer un rapport avec les lignes de données filtrées

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Indiquez les campagnes dont vous souhaitez télécharger les données :

   * Pour télécharger des données pour des campagnes spécifiques, cochez les cases en regard des campagnes.

   * Pour télécharger des données pour toutes les campagnes, il n’est pas nécessaire de cocher des cases. Toutes les campagnes sont incluses par défaut.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans les paramètres de [!UICONTROL Grid Reports], saisissez un nom de rapport unique, puis cliquez sur **[!UICONTROL Generate]**.

   Par défaut, le fichier est nommé « campaign_YYYMMDD_NNNN », où « NNNN » est le numéro de tâche séquentielle (par exemple, « campaign_20250402_1326 »).

   Le fichier est ajouté à la liste de [!UICONTROL Recently Generated].

1. (Facultatif) Pour télécharger le fichier une fois l’opération terminée, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Télécharger un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Supprimer un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") en regard du nom du fichier.

>[!MORELIKETHIS]
>
>* [Gérer les contraintes pour les unités d’offres de recherche](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gérer les affectations de contraintes pour les groupes publicitaires](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Gérer les affectations de contraintes pour les mots-clés](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Gérer les affectations de contrainte pour les emplacements](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [ (interface utilisateur héritée) Télécharger des données à partir d’une vue de gestion de campagne](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(interface utilisateur héritée) Supprimez un rapport de données de performances ou un fichier de feuille d’envoi groupé du menu [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] paramètres de campaign](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-baidu.md)
>* [[!DNL Google Ads] paramètres de campaign](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-google.md)
>* [[!DNL LY Ads] paramètres de campaign](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] paramètres de campaign](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-microsoft.md)
>* [[!DNL Yandex] paramètres de campaign](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings/campaign-settings-meta.md) -->

