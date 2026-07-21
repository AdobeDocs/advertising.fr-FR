---
title: Gérer les groupes de produits d’achat
description: Découvrez, créez, modifiez et supprimez des groupes de produits d’achat et référencez les paramètres de groupe de produits pour Google Ads et Microsoft Advertising.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---


# Gérer les groupes de produits d’achat

*[!DNL Google Ads]et [!DNL Microsoft Advertising] des campagnes d’achat uniquement*

Vous pouvez créer et gérer des groupes de produits dans la vue [!UICONTROL Product Groups] à l’adresse [!UICONTROL Assets] > [!UICONTROL Shopping].

Vous pouvez afficher des données sur les groupes de produits dans [le [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md).

## Que sont les groupes de produits ?

Dans les campagnes d’achats, vos groupes de produits (et non les mots-clés) déterminent les produits de votre compte de centre commercial pour lesquels des annonces d’achats sont affichées. Chaque groupe de produits est basé sur un attribut de produit unique (tel que la catégorie, le type de produit, la marque, la condition, l’ID de produit ou les libellés personnalisés) et utilise la même enchère pour tous les produits correspondants. Vous pouvez inclure ou exclure des offres pour les produits de chaque groupe.

Vous configurez des groupes de produits au niveau du groupe publicitaire afin de déterminer les produits de vos comptes de centre commercial qui apparaissent dans les annonces d’achat pour le groupe publicitaire. Même si le groupe publicitaire ne comprend pas d’entités publicitaires, le réseau publicitaire affiche toujours des annonces pour les produits.

Lorsque le même produit est inclus dans plusieurs campagnes, le réseau publicitaire commence par utiliser la priorité de campagne pour déterminer la campagne (et l’enchère associée) éligible pour les enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, la campagne ayant la meilleure enchère est éligible.

Pour plus d’informations sur les campagnes d’achats et les publicités [!DNL Google], consultez « [Implémenter [!DNL Google Ads] des campagnes d’achats](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md) » et la [documentation sur les publicités Google](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Pour plus d’informations sur les campagnes d’achats [!DNL Microsoft], consultez « [Implémenter [!DNL Microsoft Advertising] des campagnes d’achats](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md) » et la [[!DNL Microsoft Advertising] documentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>La prise en charge n’est pas disponible pour les groupes de listes [!DNL Google Ads] dans les campagnes Performance Max. Pour gérer et afficher des données pour les groupes de listes, utilisez l’éditeur de [!DNL Google Ads].

### Hiérarchie des groupes de produits

Avant de pouvoir créer des groupes de produits avec des attributs spécifiques pour un groupe publicitaire, vous devez d’abord créer un groupe de produits complet appelé « [!UICONTROL All Products] ». À partir de ce groupe de produits parent, vous pouvez créer des groupes de produits enfants pour des sous-ensembles de produits, ainsi que des petits-enfants à partir des groupes de produits enfants. Une fois que vous avez créé le premier groupe de produits enfant pour un groupe publicitaire, un autre groupe de produits appelé « [!UICONTROL Everything Else] » est automatiquement créé à l’aide de l’enchère du groupe publicitaire par défaut. À mesure que vous ajoutez d’autres groupes de produits, le groupe « [!UICONTROL Everything Else] » est ajusté en conséquence afin qu’il constitue tous les produits qui ne font pas partie d’un autre groupe de produits.

Au sein d’un groupe publicitaire, vous pouvez créer jusqu’à sept niveaux de groupes de produits (sans inclure « [!UICONTROL All Products] ») à inclure ou à exclure des offres, avec un ou plusieurs groupes de produits ciblant le même attribut à chaque niveau (par exemple, [!UICONTROL Brand]=Acme pour un groupe de produits et [!UICONTROL Brand]=AcmePlus pour un autre au même niveau). Les groupes de produits parents sont appelés subdivisions et le niveau de subdivision le plus bas est appelé unité. Vous pouvez définir des offres et des modèles de suivi, ou exclure complètement les offres, au niveau de l’unité. L’ensemble complet des groupes de produits actifs pour un groupe publicitaire est appliqué de manière hiérarchique afin de déterminer les produits éligibles. Par exemple, si vous subdivisez [!UICONTROL All Products] en [!UICONTROL Brand]=AcmeBasic et [!UICONTROL Brand]=AcmePlus, puis que vous subdivisez davantage chacun de ces groupes de produits en [!UICONTROL Condition]=Nouveau et définissez des enchères, seuls les nouveaux produits des marques AcmeBasic et AcmePlus peuvent faire l’objet d’une publicité ou être exclus des publicités.

![Exemple d’ensemble de groupes ](/help/search-social-commerce/assets/product-group-list-new.png " produitsExemple d’ensemble de groupes de produits")

![Exemple de hiérarchie de groupe de produits](/help/search-social-commerce/assets/product-group-tree-new.png "Exemple de hiérarchie de groupe de produits")

### Filtres de produit {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

Consultez également les [!DNL Google Ads] d’aide « [ Gérer une campagne d’achat avec des groupes de produits ](https://support.google.com/google-ads/answer/6275317) » et d’aide [!DNL Microsoft Advertising] « [ Comprendre et utiliser des groupes de produits ](https://help.ads.microsoft.com/#apex/bae/en/56782) ».

| Réseau D&#39;Achats | Dimension du produit | Attributs | Remarques |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads] : [!UICONTROL Category=]<br><br>Microsoft : [!UICONTROL Category 1=] à [!UICONTROL Category 5=] | \[L’ID de catégorie\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[La marque\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[ID d’élément\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads] : [!UICONTROL Product Type (1st level)=] à [!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft] : [!UICONTROL Product Type=] | \[Le type de produit\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=] à [!UICONTROL Custom Label 4=] | \[Attribut pour le libellé personnalisé\] | — |
| [!DNL Google Ads] | Canal= | [!UICONTROL Local], [!UICONTROL Online] | Pour afficher uniquement des annonces pour des produits locaux ou des produits en ligne. <br><br><b>Remarque :</b> pour créer des annonces pour des produits locaux, l&#39;option « Annonces d&#39;inventaire local » doit être activée et vous devez participer au programme d&#39;achats locaux avec [!DNL Google Merchant Center]. |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | Permet d’afficher ou non des annonces pour des produits disponibles uniquement pour un seul canal (uniquement en local ou uniquement en ligne) ou pour plusieurs canaux (à la fois en local et en ligne). |

## La vue [!UICONTROL Product Groups]

La vue [!UICONTROL Product Groups] sous [!UICONTROL Assets] > [!UICONTROL Shopping] répertorie tous les groupes de produits dans la vue filtrée pour le compte d’annonceur sélectionné. Vous pouvez également créer et gérer des groupes de produits.

### Actions disponibles <!-- Go through all -->

* [Créer un groupe de produits « [!UICONTROL All Products] »](#product-group-create-all-products)

* [Créer un nœud de groupe de produits enfant dans un groupe de produits existant](#node-add)

* Modifiez les paramètres d’un nœud de groupe de produits :

  * [Modifier les paramètres](#node-edit)

  * [Modifier uniquement le [!UICONTROL Tracking Template]](#node-edit-tracking-template)

  * [Modifier uniquement le [!UICONTROL Max CPC]](#node-edit-maxcpc)

* [Suppression d’un nœud de groupe de produits](#node-delete)

* [Attribuez des contraintes](#constraint-assign) aux groupes de produits et [supprimez des contraintes](#constraint-unassign) aux groupes de produits.

* [Attribuez des classifications d’étiquettes](#classification-values-assign) aux groupes de produits et [supprimez des classifications d’étiquettes](#classification-values-remove) des groupes de produits

>[!NOTE]
>
>Vous pouvez créer et modifier de grandes quantités de données de groupes de produits (y compris des étiquettes et des affectations de contraintes) à la fois en chargeant des [fichiers de feuille d’envoi groupé](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) et en les publiant sur le réseau publicitaire.

## Créer un groupe de produits « [!UICONTROL All Products] » {#product-group-create-all-products}

Avant de pouvoir créer des groupes de produits avec des attributs spécifiques, vous devez d’abord créer un groupe de produits complet appelé « [!UICONTROL All Products] ». Chaque groupe publicitaire ne peut avoir qu’un seul groupe « [!UICONTROL All Products] ».

>[!TIP]
>
>Pour créer plusieurs composants de compte à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Product Group]**.

1. Sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Spécifiez les paramètres du groupe de produits [Google Ads](#google-ads-product-group-settings) ou [Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Si nécessaire, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") et modifiez les paramètres du groupe de produits [Google Ads](#google-ads-product-group-settings) ou [Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Cliquez sur **[!UICONTROL Create]**.

## Créer un nœud de groupe de produits enfant dans un groupe de produits existant {#product-group-create-child}

Une fois que vous avez créé au moins un groupe « [!UICONTROL All Products] » tout compris pour un groupe publicitaire, vous pouvez créer des nœuds de groupe de produits enfants pour des sous-ensembles de produits à inclure ou à exclure des enchères, avec un ou plusieurs groupes de produits ciblant le même attribut à chaque niveau (par exemple, [!UICONTROL Brand]=Acme pour un groupe de produits et [!UICONTROL Brand]=AcmePlus pour un autre au même niveau). Vous pouvez créer jusqu’à sept niveaux de nœuds de groupe de produits enfant, sans inclure « [!UICONTROL All Products] ».

>[!NOTE]
>
>Vous ne pouvez pas créer de groupe de produits enfant pour un groupe de produits « [!UICONTROL Everything Else] ».

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Facultatif) Pour afficher un groupe de produits et ses nœuds enfants dans l’arborescence, placez le curseur sur le nom du groupe de produits, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Placez le curseur sur le nom du groupe de produits, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL + Add Node]**.

1. Spécifiez les paramètres du groupe de produits [Google Ads](#google-ads-product-group-settings) ou [Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Cliquez sur **[!UICONTROL Center]**.

## Modifier les paramètres d’un nœud de groupe de produits {#node-edit}

Vous pouvez modifier le modèle d’offre et de suivi pour les nœuds de groupe de produits unitaires (groupes de produits sans nœuds de groupe de produits enfants) qui sont inclus pour un groupe publicitaire. Vous ne pouvez modifier aucune information pour les groupes de produits unitaires exclus ou pour les nœuds de sous-division inclus ou exclus, qui sont des groupes de produits ayant des nœuds de groupe de produits enfants.

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Facultatif) Pour afficher un groupe de produits et ses nœuds enfants dans l’arborescence, placez le curseur sur le nom du groupe de produits, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Placez le curseur sur le nom du groupe de produits, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL + Edit Node]**.

1. Modifiez les paramètres du groupe de produits [Google Ads](#google-ads-product-group-settings) ou [Microsoft Advertising](#microsoft-advertising-product-group-settings).

1. Cliquez sur **[!UICONTROL Update]**.

## Modifier uniquement les [!UICONTROL Tracking Template] d’un nœud de groupe de produits {#node-edit-tracking-template}

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Placez le curseur sur le nom du groupe de produits, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL Tree View]** pour afficher le groupe de produits et ses nœuds enfants dans l’arborescence.

1. Dans la colonne **[!UICONTROL Tracking Template]**, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier").

1. Modifiez la valeur **[!UICONTROL Tracking Template]**, puis cliquez sur **[!UICONTROL Save]**.

## Modifier uniquement les [!UICONTROL Max CPC] d’un nœud de groupe de produits {#node-edit-maxcpc}

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Placez le curseur sur le nom du groupe de produits, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL Tree View]** pour afficher le groupe de produits et ses nœuds enfants dans l’arborescence.

1. Dans la colonne **[!UICONTROL Max CPC]**, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier").

1. Modifiez la valeur **[!UICONTROL Max CPC]**, puis cliquez sur **[!UICONTROL Save]**.

## Suppression d’un nœud de groupe de produits {#node-delete}

Vous pouvez supprimer n’importe quel groupe de produits, à l’exception d’un groupe « Tout le reste » lorsque d’autres groupes de produits existent au même niveau, utilisé pour déterminer les produits de votre compte de centre commercial qui sont inclus dans les annonces d’achat pour le groupe d’annonces. La suppression d’un groupe de produits supprime tous les groupes de produits enfants.

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Placez le curseur sur le nom du groupe de produits, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL Tree View]** pour afficher le groupe de produits et ses nœuds enfants dans l’arborescence.

1. Cliquez dans la colonne **[!UICONTROL Status]** et sélectionnez **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Affecter une contrainte à des groupes de produits sélectionnés {#constraint-assign}

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Cochez la case en regard de chaque groupe de produits auquel vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

## Supprimer les contraintes des groupes de produits sélectionnés {#constraint-unassign}

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Cochez la case en regard de chaque groupe de produits duquel vous annulerez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

## Attribuer des valeurs de classification à des groupes de produits {#classification-values-assign}

>[!NOTE]
>
>Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Cochez la case en regard de chaque groupe de produits auquel vous affecterez une valeur d’étiquette.

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

## Supprimer les valeurs de classification de libellé des groupes de produits {#classification-values-remove}

La suppression d’une valeur de classification supprime l’association avec le composant de compte et tous ses composants enfants. Les données de rapport pour la valeur de classification ne sont plus disponibles pour ces composants. La suppression d’une valeur de classification ne supprime pas la valeur ni les composants de compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Cochez la case en regard de chaque groupe de produits duquel vous allez supprimer une valeur d’étiquette.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Cochez la case en regard de chaque valeur de classification à supprimer des entités sélectionnées.

   Pour sélectionner toutes les valeurs attribuées, cliquez sur **[!UICONTROL Select All]**. Pour désélectionner toutes les valeurs affectées, cliquez sur **[!UICONTROL Deselect All]**.

1. Cliquez sur **[!UICONTROL Unassign Selected]**.

## [!DNL Google Ads] des paramètres de groupe de produits {#google-ads-product-group-settings}

### Groupes de produits « Tous les produits »

**[!UICONTROL Network]:** (Nouveaux groupes de produits uniquement) Le réseau publicitaire.

**[!UICONTROL Account]:** (Nouveaux groupes de produits uniquement) Nom du compte réseau publicitaire.

**[!UICONTROL Campaign]:** (Nouveaux groupes de produits uniquement) La campagne.

**[!UICONTROL Ad Group]:** (Nouveaux groupes de produits uniquement) Groupe publicitaire .

**[!UICONTROL Condition]** ou **[!UICONTROL Condition Type]:** (lecture seule) Tous les produits

**[!UICONTROL Condition Value]:** (groupes de produits existants uniquement)  

**[!UICONTROL Bid]** ou **[!UICONTROL Max CPC]:** (groupes de produits inclus uniquement) coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants et elle est utilisée à la place de la valeur au niveau du groupe publicitaire.

{{$include /help/_includes/tracking-template-google.md}}

Ce modèle remplace les modèles aux niveaux supérieurs et est utilisé uniquement pour les unités sans groupes de produits enfants. Les paramètres d’ajout spécifiés pour le compte ou la campagne ne sont pas inclus. Les paramètres d’ajout spécifiés pour le compte ou la campagne ne sont pas inclus.

### Tous les autres groupes de produits

**[!UICONTROL Condition Type]** et **[!UICONTROL Condition Value]:** (lecture seule pour les groupes de produits existants). Dimensions de produit à cibler. Pour les nouveaux groupes de produits, saisissez la dimension par laquelle cibler les produits et l’attribut de qualification pour la catégorie d’informations sélectionnée (par exemple, « Acme » lorsque vous ciblez par marque ou « Nouveau » lorsque vous ciblez par condition).

Une fois que vous avez créé un groupe de produits pour des dimensions de produit spécifiques (c’est-à-dire, pas « Tous les produits »), Search, Social et Commerce crée automatiquement un groupe de produits pour « Tout le reste ».

Pour obtenir la liste des dimensions de produit disponibles, voir « [ Filtres de produit ](#product-filters) ». Votre liste de dimensions peut être limitée en fonction du paramètre de [!UICONTROL Inventory Filter] de la campagne.

**[!UICONTROL Excluded]:** (facultatif pour les nouveaux groupes de produits ; en lecture seule pour les groupes de produits existants) Exclut les enchères sur les annonces de produits correspondants.

**[!UICONTROL Max CPC]:** (groupes de produits inclus uniquement) Coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants et elle est utilisée à la place de la valeur au niveau du groupe publicitaire.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Ce modèle remplace les modèles aux niveaux supérieurs et est utilisé uniquement pour les unités sans groupes de produits enfants.

## [!DNL Microsoft Advertising] des paramètres de groupe de produits {#microsoft-advertising-product-group-settings}

### Groupes de produits « Tous les produits »

**[!UICONTROL Network]:** (Nouveaux groupes de produits uniquement) Le réseau publicitaire.

**[!UICONTROL Account]:** (Nouveaux groupes de produits uniquement) Nom du compte réseau publicitaire.

**[!UICONTROL Campaign]:** (Nouveaux groupes de produits uniquement) La campagne.

**[!UICONTROL Ad Group]:** (Nouveaux groupes de produits uniquement) Groupe publicitaire .

**[!UICONTROL Condition]** ou **[!UICONTROL Condition Type]:** (lecture seule) Tous les produits

**[!UICONTROL Condition Value]:** (groupes de produits existants uniquement)  

**[!UICONTROL Bid]** ou **[!UICONTROL Max CPC]:** (groupes de produits inclus uniquement) coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants et elle est utilisée à la place de la valeur au niveau du groupe publicitaire.

**[!UICONTROL Base URL]:** (nouveaux groupes de produits uniquement) Non utilisé<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Ce modèle remplace les modèles aux niveaux supérieurs et est utilisé uniquement pour les unités sans groupes de produits enfants.

### Tous les autres groupes de produits

**[!UICONTROL Condition Type]** et **[!UICONTROL Condition Value]:** (lecture seule pour les groupes de produits existants). Dimensions de produit à cibler. Pour les nouveaux groupes de produits, saisissez la dimension par laquelle cibler les produits et l’attribut de qualification pour la catégorie d’informations sélectionnée (par exemple, « Acme » lorsque vous ciblez par marque ou « Nouveau » lorsque vous ciblez par condition).

Une fois que vous avez créé un groupe de produits pour des dimensions de produit spécifiques (c’est-à-dire, pas « Tous les produits »), Search, Social et Commerce crée automatiquement un groupe de produits pour « Tout le reste ».

Pour obtenir la liste des dimensions de produit disponibles, voir « [ Filtres de produit ](#product-filters) ». Votre liste de dimensions peut être limitée en fonction du paramètre de [!UICONTROL Inventory Filter] de la campagne.

**[!UICONTROL Excluded]:** (facultatif pour les nouveaux groupes de produits ; en lecture seule pour les groupes de produits existants) Exclut les enchères sur les annonces de produits correspondants.

**[!UICONTROL Max CPC]:** (groupes de produits inclus uniquement) Coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire. Cette valeur est utilisée uniquement pour les unités sans groupes de produits enfants et elle est utilisée à la place de la valeur au niveau du groupe publicitaire.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Ce modèle remplace les modèles aux niveaux supérieurs et est utilisé uniquement pour les unités sans groupes de produits enfants.

>[!MORELIKETHIS]
>
>* [Implémenter [!DNL Google Ads] des campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [Implémenter [!DNL Microsoft Advertising] des campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [Le [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
