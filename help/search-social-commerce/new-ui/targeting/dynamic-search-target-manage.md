---
title: Gestion [!DNL Google Ads] cibles de recherche dynamique
description: Découvrez comment créer et gérer [!DNL Google Ads] cibles de recherche dynamique.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
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
source-git-commit: f907f445c70ce64368dfa7e77d4cd1900ecc7113
workflow-type: tm+mt
source-wordcount: '1504'
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

## La vue [!UICONTROL Auto Targets] {#auto-target-view-about}

La vue [!UICONTROL Targeting] > [!UICONTROL Auto Targets] répertorie toutes les cibles de recherche dynamique dans la vue filtrée pour le compte d’annonceur sélectionné. Vous pouvez également gérer vos cibles de recherche dynamique.

L’affichage des données nécessite l’autorisation [!UICONTROL View Auto Targets] . La création de cibles et la modification de leurs enchères ou de leur statut nécessitent l’autorisation [!UICONTROL Edit Auto Targets].

### Actions disponibles

* [Création d’une cible de recherche dynamique](#auto-target-create)

* [Modification des paramètres des cibles de recherche dynamique](#auto-target-edit)

* [Modification du statut ou suppression de cibles de recherche dynamique](#auto-target-status)

* [Copier toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard)

* [Attribuez des contraintes](#constraint-assign) aux cibles de recherche dynamique et [supprimez des contraintes](#constraint-unassign) aux cibles de recherche dynamique

* [Attribuez des classifications de libellé](#classification-values-assign) aux cibles de recherche dynamique et [supprimez des classifications de libellé](#classification-values-remove) aux cibles de recherche dynamique

>[!NOTE]
>
>Vous pouvez créer et modifier de grandes quantités de données de la cible (y compris des étiquettes et des affectations de contraintes) en une seule fois en chargeant des [fichiers de feuille d’envoi groupé](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) et en les publiant sur le réseau publicitaire.

## Création d’une cible de recherche dynamique [!DNL Google Ads] {#auto-target-create}

Vous pouvez créer des cibles de recherche dynamique pour définir des pages dans vos sites web (c’est-à-dire les domaines utilisés dans les URL d’affichage de vos publicités) dont le contenu est utilisé pour cibler vos publicités de recherche dynamique dans le même groupe de publicités.

Vous pouvez cibler toutes les pages indexées ou spécifier jusqu’à trois critères.

>[!NOTE]
>
>Pour suivre au mieux les performances, créez une cible avec l’option [!UICONTROL All] pour un seul groupe publicitaire par campagne.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Auto Target]**.

1. Dans **[!UICONTROL Basic Settings]**, sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire.

1. Spécifiez les autres [paramètres de la cible de recherche dynamique](#auto-target-create-settings).

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres. Pour modifier des paramètres, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") **[!UICONTROL Edit]** dans la section applicable et modifiez les paramètres.

1. Cliquez sur **[!UICONTROL Create]**.

## Modifier [!DNL Google Ads] paramètres de la cible de recherche dynamique {#auto-target-edit}

Vous pouvez modifier le statut ou l’enchère maximale d’une ou de plusieurs cibles de recherche dynamique. Vous ne pouvez pas modifier les critères ciblés.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque ligne à modifier.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Dans le panneau **[!UICONTROL Edit Auto Targets]**, modifiez le [statut et paramètres d’enchères](#auto-target-edit-settings).

   Vos modifications sont appliquées à toutes les cibles sélectionnées. Les paramètres que vous ne modifiez pas conservent leurs valeurs existantes.

   Lorsque les cibles sélectionnées utilisent plusieurs devises, la modification des enchères est désactivée. Vous pouvez toujours modifier leur statut.

1. Cliquez sur **[!UICONTROL Save]**.

Vous pouvez également modifier l&#39;enchère d&#39;une cible unique directement dans le tableau de données en cliquant sur sa valeur d&#39;enchère.

## Modification du statut ou suppression [!DNL Google Ads] cibles de recherche dynamique {#auto-target-status}

Vous pouvez mettre en pause une cible de recherche dynamique active afin de cesser de l’utiliser pour les annonces de recherche dynamique du même groupe d’annonces. Vous pouvez ensuite reprendre à utiliser la cible en redéfinissant son statut sur Actif. Vous pouvez également supprimer des cibles de recherche dynamique.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. (Facultatif) Filtrez la liste pour inclure des cibles de recherche dynamique spécifiques.

1. Effectuez l’une des opérations suivantes :

   * Pour modifier le statut d&#39;une cible, cliquez sur sa valeur dans la colonne **[!UICONTROL Status]** et sélectionnez **[!UICONTROL Active]** ou **[!UICONTROL Paused]**.

   * Pour modifier le statut de plusieurs cibles, cochez la case en regard de chaque cible, cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse, sélectionnez la **[!UICONTROL Status]** dans le panneau **[!UICONTROL Edit Auto Targets]**, puis cliquez sur **[!UICONTROL Save]**.

   * Pour supprimer une ou plusieurs cibles, cochez la case en regard de chacune d’elles, cliquez sur **[!UICONTROL ...]>[!UICONTROL Delete]** dans la barre d’outils des actions en masse, puis sur **[!UICONTROL Confirm]** dans le message de confirmation.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

## Gestion des affectations de contraintes pour les cibles de recherche dynamique {#constraints}

### Affectation d’une contrainte à des cibles de recherche dynamique {#constraint-assign}

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque cible de recherche dynamique à laquelle vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

### Suppression des contraintes des cibles de recherche dynamique sélectionnées {#constraint-unassign}

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque cible de recherche dynamique à partir de laquelle vous annulerez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

## Gestion des valeurs de classification pour les cibles de recherche dynamique {#classification-values}

### Affectation de valeurs de classification à des cibles de recherche dynamique {#classification-values-assign}

>[!NOTE]
>
>Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les cibles de recherche dynamique, sauf si vous souhaitez remplacer les valeurs héritées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

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

### Supprimer les valeurs de classification de libellé des cibles de recherche dynamique {#classification-values-remove}

La suppression d’une valeur de classification supprime l’association avec le composant de compte et tous ses composants enfants. Les données de rapport pour la valeur de classification ne sont plus disponibles pour ces composants. La suppression d’une valeur de classification ne supprime pas la valeur ni les composants de compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Cochez la case en regard de chaque cible de recherche dynamique à partir de laquelle vous allez supprimer une valeur de libellé.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Cochez la case en regard de chaque valeur de classification à supprimer des entités sélectionnées.

   Pour sélectionner toutes les valeurs attribuées, cliquez sur **[!UICONTROL Select All]**. Pour désélectionner toutes les valeurs attribuées, cliquez sur **[!UICONTROL Deselect All]**.

1. Cliquez sur **[!UICONTROL Unassign Selected]**.

## [!DNL Google Ads] des paramètres de la cible de recherche dynamique {#dynamic-search-target-settings}

### Paramètres disponibles lors de la création {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**Ciblages automatiques :** pages indexées dont le contenu est utilisé pour cibler les annonces de recherche dynamique dans le groupe d’annonces :

* *[!UICONTROL All]* (valeur par défaut) : cible toutes les pages indexées.

* *[!UICONTROL Specific]:* cible les pages qui correspondent à trois critères maximum. Sélectionnez un critère et saisissez sa valeur. Pour ajouter un autre critère, cliquez sur **[!UICONTROL And]**. Les critères sont combinés avec l’opérateur AND ; une page doit donc correspondre à tous les critères spécifiés. Cliquez sur **[!UICONTROL Reset]** pour effacer les critères.

  * *[!UICONTROL Category]:* la catégorie de contenu [!DNL Google Ads] de la page est égale à la valeur spécifiée. Saisissez une valeur.

  * *[!UICONTROL URL]:* l’URL de la page contient la valeur spécifiée, par exemple `shoes.example.com`. Saisissez une URL valide.

  * *[!UICONTROL Page Title]:* Le titre de la page contient le texte spécifié. Saisissez une valeur.

  * *[!UICONTROL Page Content]:* Le contenu de la page contient le texte spécifié. Saisissez une valeur.

Vous ne pouvez pas modifier les critères de la cible après l’avoir créée.

**[!UICONTROL Status]:** Statut de la cible :

* *[!UICONTROL Active]* (valeur par défaut) : permet d’enchérir.

* *[!UICONTROL Paused]:* Désactive les enchères.

**[!UICONTROL Bid]:** coût maximum par clic (CPC) pour la cible. Cette valeur remplace l’enchère au niveau du groupe publicitaire. Le champ est facultatif ; lorsque vous saisissez une enchère, la valeur minimale est 0,01 dans la devise du compte.

>[!NOTE]
>
>Si la cible se trouve dans un portefeuille optimisé, l’enchère CPC spécifiée est appliquée pendant un jour. Ensuite, la fonctionnalité d’optimisation place les offres en fonction de ses propres calculs.

### Paramètres disponibles lors de la modification {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]:** sélectionnez **[!UICONTROL Active]** ou **[!UICONTROL Paused]**.

#### [!UICONTROL Bid details]

La modification des enchères est désactivée lorsque les cibles sélectionnées utilisent plusieurs devises.

**[!UICONTROL Bid adjustment]:** Modification du nombre maximal d&#39;enchères :

* *[!UICONTROL Set to]:* Remplacez chaque enchère par le montant en [!UICONTROL Set value].

* *[!UICONTROL Increase]:* augmenter chaque enchère du montant ou du pourcentage en [!UICONTROL Set value].

* *[!UICONTROL Decrease]:* Diminuer chaque enchère du montant ou du pourcentage en [!UICONTROL Set value].

**[!UICONTROL Modifier type]:** (pour [!UICONTROL Increase] et [!UICONTROL Decrease]) Sélectionnez **[!UICONTROL Currency]** ou **[!UICONTROL Percentage]**.

**[!UICONTROL Set value]:** nouvelle offre, ou montant ou pourcentage en fonction duquel modifier chaque offre. La valeur minimale est 0,01.

**[!UICONTROL Max limit]:** (facultatif ; par [!UICONTROL Increase] et [!UICONTROL Decrease]) Limite dans la devise du compte. Pour une augmentation, il s&#39;agit de l&#39;enchère maximum résultante. Pour une diminution, il s&#39;agit de l&#39;offre minimale résultante. Lorsque vous entrez une limite, la valeur minimale est 0,01.

>[!MORELIKETHIS]
>
>* [(nouvelle interface utilisateur) Gérer les contraintes pour les unités d’enchères de recherche](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nouvelle interface utilisateur) Gérer les classifications de libellés](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
