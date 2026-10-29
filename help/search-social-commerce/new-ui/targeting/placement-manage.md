---
title: Gestion des emplacements
description: Découvrez comment créer et gérer des emplacements Google Ads et des emplacements négatifs et affecter des contraintes aux emplacements.
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: d3e38179ae119f35c184bee398edaaf456fab563
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 0%
---
# Gestion des emplacements

*Fonction*

Comptes *[!DNL Google Ads]uniquement*

Les emplacements sont des emplacements sur le réseau d’affichage dans lesquels vos annonces publicitaires peuvent apparaître. Les paramètres d’emplacement incluent l’enchère maximale et les paramètres de suivi facultatifs. Les paramètres au niveau de l’emplacement remplacent ceux du groupe publicitaire ou de la campagne. Les emplacements négatifs empêchent l’affichage des publicités sur des sites spécifiés.

Une fois que vous [rendez un compte de réseau publicitaire accessible via une connexion API](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) et que Search, Social et Commerce a synchronisé les données du compte avec le réseau publicitaire, vous pouvez créer des emplacements pour les groupes publicitaires dans [types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) qui ciblent le réseau d’affichage. Vous pouvez également modifier et modifier le statut des emplacements, ainsi que créer et supprimer des emplacements négatifs.

>[!NOTE]
>
>[!DNL Google Ads] ne fournit pas de données de performances au niveau des annonces pour les emplacements.

## À propos de la vue [!UICONTROL Placements] {#placement-view-about}

La vue [!UICONTROL Targeting] > [!UICONTROL Placements] comprend deux onglets pour le compte d’annonceur sélectionné :

* L’onglet [!UICONTROL Placements] répertorie tous les emplacements pouvant faire l’objet d’offres dans la vue filtrée.

* L’onglet [!UICONTROL Negatives] répertorie tous les emplacements négatifs dans la vue filtrée.

L’affichage de la page nécessite l’autorisation [!UICONTROL View Placements] . La création d&#39;emplacements ou d&#39;emplacements négatifs, la modification d&#39;emplacements, la modification du statut d&#39;emplacement et la suppression d&#39;emplacements ou d&#39;emplacements négatifs nécessitent l&#39;autorisation [!UICONTROL Edit Placements].

### Actions disponibles

* [Créer des emplacements](#placement-create)

* [Créer des emplacements négatifs](#placement-negative-create)

* [Modifier les paramètres d’emplacement](#placement-edit)

* [Modifier le statut des emplacements et des emplacements négatifs, ou les supprimer](#placement-status)

* [Copier toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard)

* [Affecter des contraintes aux emplacements et annuler l’affectation de contraintes des emplacements](#placement-constraints)

* [Attribuer des classifications de libellés aux emplacements](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## Créer des emplacements {#placement-create}

>[!TIP]
>
>Pour créer un grand nombre d’emplacements à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Dans l’onglet **[!UICONTROL Placements]** , cliquez sur **[!UICONTROL Create Placement]**.

1. À l’étape **[!UICONTROL Basic Settings]**, sélectionnez le réseau, le compte, la campagne et le groupe publicitaire.

1. Saisissez les [paramètres d’emplacement](#placement-create-settings).

   Pour créer plusieurs emplacements, séparez les URL du site web par des virgules.

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres. Pour modifier des paramètres, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") **[!UICONTROL Edit]** dans la section applicable et modifiez les paramètres.

1. Cliquez sur **[!UICONTROL Create]**.

## Créer des emplacements négatifs {#placement-negative-create}

Vous pouvez créer des emplacements négatifs pour une campagne [!DNL Google Ads] ou un groupe publicitaire qui cible le réseau d’affichage.

>[!NOTE]
>
>Vous pouvez également créer et modifier des emplacements négatifs dans les paramètres [groupe publicitaire](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) et [campagne](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>Pour créer un grand nombre d’emplacements négatifs en même temps, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Dans l’onglet **[!UICONTROL Negatives]** , cliquez sur **[!UICONTROL Create Negative]** , puis sur **[!UICONTROL Campaign Negative]** ou **[!UICONTROL Ad Group Negative]**.

1. À l’étape **[!UICONTROL Basic Settings]**, sélectionnez le réseau, le compte, la campagne et (pour les emplacements négatifs au niveau du groupe publicitaire) le groupe publicitaire.

1. À l’étape **[!UICONTROL Manage Websites]**, saisissez les URL de site web négatives, telles que `www.example.com` ou `example.com/shoes`.

   Séparez plusieurs URL par des virgules. Ce formulaire accepte les URL de site web, et non les chaînes de rubrique ou de catégorie.

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres. Pour modifier des paramètres, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") **[!UICONTROL Edit]** dans la section applicable et modifiez les paramètres.

1. Cliquez sur **[!UICONTROL Create]**.

## Modifier les paramètres d’emplacement {#placement-edit}

Vous pouvez modifier le statut, l’enchère, l’URL de base et le modèle de suivi pour un ou plusieurs emplacements. Vous ne pouvez pas modifier l’URL du site web ciblé ni les emplacements supprimés.

>[!TIP]
>
>Pour modifier simultanément une grande quantité de données d’emplacement, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Dans l’onglet **[!UICONTROL Placements]** , cochez la case en regard de chaque emplacement à modifier.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Dans le panneau **[!UICONTROL Edit Placements]**, modifiez les [paramètres d’emplacement](#placement-edit-settings).

   Dans le cas de plusieurs emplacements, vos modifications sont appliquées à tous les emplacements sélectionnés. Vous pouvez définir des offres à une valeur spécifiée, les augmenter ou les diminuer d&#39;un pourcentage ou d&#39;un montant monétaire spécifié, avec une limite. Pour les URL, vous pouvez remplacer la valeur existante, rechercher et remplacer du texte, ajouter un préfixe ou ajouter un suffixe.

   La modification des enchères est désactivée lorsque les emplacements sélectionnés utilisent plusieurs devises.

1. Cliquez sur **[!UICONTROL Save]**.

## Modifier le statut des emplacements et des emplacements négatifs {#placement-status}

Vous pouvez mettre en pause un emplacement actif pouvant faire l’objet d’une offre afin de désactiver les enchères associées. Vous pouvez ensuite reprendre les enchères en redéfinissant leur statut sur Actif.

Vous pouvez également supprimer des emplacements actifs ou en pause ou des emplacements négatifs. Les emplacements supprimés sont supprimés du réseau publicitaire. Ils sont toujours visibles lorsque vous les incluez dans le filtre de données, mais vous ne pouvez pas les modifier.

### Activer ou mettre en pause des emplacements

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Sur l’onglet **[!UICONTROL Placements]** , vous pouvez éventuellement filtrer la liste, puis cocher la case en regard de chaque emplacement dont vous souhaitez modifier le statut.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Dans la section **[!UICONTROL Placement Details]** , modifiez les **[!UICONTROL Status]** :

   * Pour activer les emplacements en pause, sélectionnez **[!UICONTROL Active]**.

   * Pour suspendre les emplacements actifs, sélectionnez **[!UICONTROL Paused]**.

1. Cliquez sur **[!UICONTROL Save]**.

### Suppression d&#39;emplacements ou d&#39;emplacements négatifs

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Sur l&#39;onglet **[!UICONTROL Placements]** ou **[!UICONTROL Negatives]** , vous pouvez éventuellement filtrer la liste, puis cocher la case en regard de chaque emplacement ou emplacement négatif à supprimer.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

## Gérer les affectations de contraintes pour les emplacements {#placement-constraints}

Vous pouvez affecter et supprimer des contraintes d’offres pour les campagnes, les groupes publicitaires, les mots-clés, les emplacements, les groupes de produits au niveau de l’unité et les cibles de recherche dynamique. Chaque entité ne peut avoir qu&#39;une seule contrainte.

Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire d’affecter des contraintes aux entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

L’annulation de l’affectation d’une contrainte supprime l’association avec les composants de compte et tous leurs composants enfants, et les données de rapport pour la contrainte ne sont plus disponibles pour ces composants. L’annulation de l’affectation d’une contrainte ne supprime pas la contrainte ou les composants de compte eux-mêmes.

>[!NOTE]
>
>* Si vous modifiez par la suite un mot-clé ou la copie d’une publicité non modifiable (créant ainsi un nouveau mot-clé ou une nouvelle publicité), la contrainte n’est pas affectée à la nouvelle entité.
>* Les contraintes actives limitent les enchères uniquement pour les unités d’offre affectées dans les portefeuilles optimisés au niveau des mots-clés hérités. Elles sont ignorées pour les unités d&#39;enchères qui se trouvent dans des portefeuilles actifs, dans des portefeuilles hybrides ou qui ne se trouvent pas dans des portefeuilles.

### Affecter une contrainte aux emplacements {#placement-constraint-assign}

Vous pouvez affecter une seule contrainte à un ou plusieurs emplacements.

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Dans l&#39;onglet **[!UICONTROL Placements]** , cochez la case en regard de chaque emplacement auquel vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Assign]>[!UICONTROL Bid Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

### Annuler l’affectation des contraintes des emplacements {#placement-constraint-unassign}

L’annulation de l’affectation d’une contrainte ne la supprime pas. Pour supprimer une contrainte, ce qui la rend indisponible pour une utilisation ultérieure, reportez-vous à « [&#x200B; Gérer les contraintes pour les unités d’offres de recherche &#x200B;](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status) ».

1. Dans le menu principal, cliquez sur **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Dans l’onglet **[!UICONTROL Placements]** , cochez la case en regard de chaque emplacement duquel vous annulez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Unassign]>[!UICONTROL Bid Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

## Paramètres d’emplacement {#placement-settings}

### Paramètres de la création d&#39;emplacements {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]:** Le réseau publicitaire. Seul [!DNL Google Ads] est pris en charge.

**[!UICONTROL Account]:** Compte de réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne.

**[!UICONTROL Ad Group]:** groupe publicitaire .

#### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites sur le réseau d’affichage sur lequel votre publicité peut apparaître. Saisissez une URL de site web valide, telle que `www.example.com`, `example.com` ou `example.com/shoes`. Séparez plusieurs URL par des virgules. L’URL ne peut pas inclure de point d’interrogation (`?`).

Pour exclure des sites web à la place, [créez des emplacements négatifs](#placement-negative-create) à partir de l’onglet [!UICONTROL Targeting] > [!UICONTROL Placements] > [!UICONTROL Negatives] ou utilisez les paramètres du groupe publicitaire et de la campagne.

**[!UICONTROL Status]:** statut d’affichage de l’emplacement : *[!UICONTROL Active]* (pour activer les enchères) ou *[!UICONTROL Paused]* (pour désactiver les enchères).

#### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (facultatif) Coût maximum par clic (CPC) ou coût par mille impressions visibles (vCPM) pour l’annonce basée sur l’emplacement, en fonction de la stratégie d’enchères de la campagne. Cette valeur remplace l’enchère au niveau du groupe publicitaire.

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>Le formulaire de création d’une nouvelle interface utilisateur nécessite l’URL de base et le modèle de suivi, lorsqu’ils sont spécifiés, pour commencer par `http://` ou `https://`.

### Paramètres de la modification des emplacements {#placement-edit-settings}

Le panneau [!UICONTROL Edit Placements] prend en charge les paramètres suivants pour un ou plusieurs emplacements sélectionnés. Vous ne pouvez pas modifier l’URL du site web ciblé.

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]:** *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]:** Comment modifier l&#39;enchère :

* *[!UICONTROL Set to]:* Remplacer l&#39;enchère existante par une valeur spécifiée.

* *[!UICONTROL Increase]:* augmenter l&#39;enchère existante d&#39;un montant ou d&#39;un pourcentage spécifié.

* *[!UICONTROL Decrease]:* diminuer l&#39;enchère existante d&#39;un montant ou d&#39;un pourcentage spécifié.

**[!UICONTROL Modifier type]:** (pour les augmentations ou les diminutions) Si l’ajustement utilise *[!UICONTROL Currency]* ou *[!UICONTROL Percentage]*.

**[!UICONTROL Set value]:** nouvelle enchère ou montant de l&#39;ajustement. La valeur minimale est 0,01.

**[!UICONTROL Max limit]:** (Pour les augmentations ou les diminutions ; facultatif) Limite de l’enchère ajustée. Dans le cas d&#39;une augmentation, il s&#39;agit de l&#39;offre maximale ; dans le cas d&#39;une diminution, il s&#39;agit de l&#39;offre minimale. La valeur limite minimale est 0,01.

La modification des enchères est désactivée lorsque les emplacements sélectionnés utilisent plusieurs devises.

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**, **[!UICONTROL Tracking Template]:** Pour chaque champ, sélectionnez le mode de modification de la valeur :

* *[!UICONTROL Set To]:* Remplacez la valeur . Saisissez une URL de site web valide commençant par `http://` ou `https://`.

* *[!UICONTROL Find/Replace]:* Remplacez le texte spécifié dans la valeur. Saisissez le texte à rechercher et le texte de remplacement.

* *[!UICONTROL Add Suffix]:* Ajoutez du texte à la valeur. Saisissez le texte du suffixe.

* *[!UICONTROL Add Prefix]:* ajoutez du texte au début de la valeur. Saisissez le texte du préfixe.

>[!NOTE]
>
>Toutes les nouvelles URL de base doivent être des URL valides commençant par `http://` ou `https://`.

>[!MORELIKETHIS]
>
>* [Gérer les contraintes pour les unités d’offres de recherche](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gérer les classifications de libellés](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
