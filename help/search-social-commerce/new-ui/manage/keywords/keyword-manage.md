---
title: Gestion des mots-clés
description: Découvrez comment créer et gérer des mots-clés pouvant faire l’objet d’une offre et négatifs, et affecter des contraintes aux mots-clés.
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
source-git-commit: d3e38179ae119f35c184bee398edaaf456fab563
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%
---
# Gestion des mots-clés

*Fonction*

Comptes *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] et [!DNL Baidu] existants uniquement*

Un mot-clé est un mot ou une expression associé à une publicité. Les paramètres de mot-clé incluent le type de correspondance de mot-clé, les enchères maximales à utiliser lorsque votre publicité est déclenchée par le mot-clé et (pour certains réseaux publicitaires) des paramètres de suivi facultatifs. Les paramètres au niveau du mot-clé remplacent les paramètres du groupe publicitaire ou de la campagne. Les mots-clés négatifs empêchent l’affichage des publicités pour les recherches correspondantes.

Une fois que vous [rendez un compte de réseau publicitaire accessible via une connexion API](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) et que Search, Social et Commerce a synchronisé les données du compte avec le réseau publicitaire, vous pouvez créer des mots-clés pour les groupes publicitaires de recherche dans [types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). Vous pouvez également modifier et modifier le statut des mots-clés, ainsi que créer et supprimer des mots-clés négatifs.

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [ Inventaire pris en charge ](/help/search-social-commerce/introduction/supported-inventory.md).

## À propos de la vue [!UICONTROL Keywords] {#keyword-view-about}

La vue [!UICONTROL Manage] > [!UICONTROL Keywords] comprend deux onglets pour le compte d’annonceur sélectionné :

* L’onglet [!UICONTROL Keywords] répertorie tous les mots-clés accessibles dans la vue filtrée.

* L’onglet [!UICONTROL Negatives] répertorie tous les mots-clés négatifs dans la vue filtrée.

### Actions disponibles

* [Créer des mots-clés](#keyword-create)

* [Créer des mots-clés négatifs](#keyword-negative-create)

* [Modifier les paramètres de mot-clé](#keyword-edit)

* [Modifier le statut des mots-clés et des mots-clés négatifs, ou les supprimer](#keyword-status)

* [Copier toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard)

* [Attribuez des contraintes aux mots-clés et annulez l’attribution des contraintes aux mots-clés](#keyword-constraints)

* [Attribuer des classifications de libellés](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md) aux mots-clés

## Créer des mots-clés {#keyword-create}

>[!TIP]
>
>Pour créer un grand nombre de mots-clés à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Dans l’onglet **[!UICONTROL Keywords]** , cliquez sur **[!UICONTROL Create Keywords]**.

1. À l’étape **[!UICONTROL Basic Settings]**, sélectionnez le réseau, le compte, la campagne et le groupe publicitaire.

1. Saisissez les [[!DNL Baidu] paramètres de mot-clé](keyword-settings-baidu.md), [[!DNL Google Ads] paramètres de mot-clé](keyword-settings-google.md), [[!DNL LY Ads] paramètres de mot-clé](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] paramètres de mot-clé](keyword-settings-microsoft.md) ou [[!DNL Yandex] paramètres de mot-clé](keyword-settings-yandex.md).

   Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés en une seule opération. Séparez plusieurs mots-clés par des virgules ou saisissez-les sur des lignes distinctes.

   >[!NOTE]
   >
   >Si les paramètres du compte ou de la campagne spécifient le suivi uniquement au niveau des annonces, alors Search, Social et Commerce ne génère pas de suivi des mots-clés.

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres. Pour modifier des paramètres, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") **[!UICONTROL Edit]** dans la section applicable et modifiez les paramètres.

1. Cliquez sur **[!UICONTROL Create]**.

## Modifier les paramètres de mot-clé {#keyword-edit}

La modification du texte du mot-clé ou du type de correspondance peut supprimer le mot-clé existant et en créer un nouveau, selon le réseau publicitaire. Pour plus d’informations, consultez les paramètres de mot-clé de votre réseau publicitaire .

>[!TIP]
>
>Pour modifier une grande quantité de données de mots-clés en même temps, y compris des mots-clés sur différents réseaux publicitaires, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Dans l’onglet **[!UICONTROL Keywords]** , cochez la case en regard de chaque mot-clé à modifier.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les [[!DNL Baidu] paramètres de mot-clé](keyword-settings-baidu.md), [[!DNL Google Ads] paramètres de mot-clé](keyword-settings-google.md), [[!DNL LY Ads] paramètres de mot-clé](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] paramètres de mot-clé](keyword-settings-microsoft.md) ou [[!DNL Yandex] paramètres de mot-clé](keyword-settings-yandex.md).

   Si plusieurs mots-clés sont sélectionnés, vous ne pouvez modifier que les champs communs à tous les mots-clés et vos modifications sont appliquées à tous les mots-clés sélectionnés. Pour certains champs alphanumériques, vous pouvez modifier les valeurs existantes à une valeur spécifiée, remplacer une chaîne existante par une chaîne spécifiée, ajouter un préfixe ou ajouter un suffixe. Pour certains champs monétaires, vous pouvez modifier les valeurs existantes à une valeur spécifiée ou augmenter ou diminuer le montant d’un pourcentage ou d’un montant monétaire spécifié, avec une limite.

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres. Pour modifier des paramètres, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") **[!UICONTROL Edit]** dans la section applicable et modifiez les paramètres.

1. Cliquez sur **[!UICONTROL Update]**.

## Créer des mots-clés négatifs {#keyword-negative-create}

Comptes *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising] et [!DNL Baidu] existants uniquement*

Vous pouvez créer des mots-clés négatifs pour un groupe publicitaire ou une campagne de recherche qui cible la recherche ou le réseau d’affichage/natif.

>[!NOTE]
>
>Vous pouvez également créer et modifier des mots-clés négatifs dans les [paramètres du groupe publicitaire](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) et [paramètres de la campagne](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>Pour créer un grand nombre de mots-clés négatifs en même temps, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Dans l’onglet **[!UICONTROL Negatives]** , cliquez sur **[!UICONTROL Create Negatives]** , puis sur **[!UICONTROL Campaign Negative Keyword]** ou **[!UICONTROL Ad Group Negative Keyword]**.

1. Sélectionnez le réseau, le compte, la campagne et (pour les mots-clés négatifs au niveau du groupe publicitaire) le groupe publicitaire.

1. Saisissez les mots-clés négatifs. Utilisez la syntaxe suivante, sans signe moins (`-`) :

   * Correspondance large négative : `keyword` (non prise en charge par [!DNL Microsoft Advertising])

   * Correspondance de l’expression négative : `"keyword"`

   * Correspondance exacte négative : `[keyword]`

   Séparez plusieurs valeurs par des virgules ou saisissez-les sur des lignes distinctes. Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés négatifs en une seule opération. Les exigences et restrictions suivantes s’appliquent :

   * Longueur maximale des caractères : [!DNL Baidu] : 30 octets simples ou 15 octets doubles ; [!DNL Microsoft Advertising] : 100 octets simples ou 50 octets doubles ; [!DNL Google Ads] et [!DNL LY Ads] : 80 octets simples ou 40 octets doubles.

   * [!DNL Baidu] n’autorise qu’un seul type de correspondance par mot-clé par groupe publicitaire. Par exemple, le groupe publicitaire 1 ne peut pas inclure à la fois `"keyword"` et `[keyword]`.

   * [!DNL Google Ads] : chaque mot-clé ne peut pas comporter plus de 10 mots et ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : espace `# $ & _ - " [ ] ' + . / :`

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres. Pour modifier des paramètres, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") **[!UICONTROL Edit]** dans la section applicable et modifiez les paramètres.

1. Cliquez sur **[!UICONTROL Create]**.

## Modifier le statut des mots-clés et des mots-clés négatifs {#keyword-status}

Vous pouvez mettre en pause un mot-clé de recherche actif pouvant faire l’objet d’une offre pour le désactiver. Vous pouvez ensuite reprendre les enchères en redéfinissant leur statut sur Actif.

Vous pouvez également supprimer des mots-clés de recherche actifs ou en pause ou des mots-clés négatifs. Les mots-clés supprimés sont supprimés du réseau publicitaire. Ils sont toujours visibles lorsque vous les incluez dans le filtre de données, mais vous ne pouvez pas les modifier.

### Activer ou suspendre des mots-clés

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Sur l’onglet **[!UICONTROL Keywords]** , vous pouvez éventuellement filtrer la liste, puis cocher la case en regard de chaque mot-clé dont vous souhaitez modifier le statut.

1. Dans la barre d’outils des actions en bloc, modifiez le statut :

   * Pour activer les mots-clés en pause, cliquez sur **[!UICONTROL Activate]**.

   * Pour suspendre les mots-clés actifs, cliquez sur **[!UICONTROL Pause]**.

### Supprimer les mots-clés ou les mots-clés négatifs

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Sous l’onglet **[!UICONTROL Keywords]** ou **[!UICONTROL Negatives]** , vous pouvez éventuellement filtrer la liste, puis cocher la case en regard de chaque mot-clé ou mot-clé négatif à supprimer.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

## Gérer les affectations de contraintes pour les mots-clés {#keyword-constraints}

Vous pouvez affecter et supprimer des contraintes d’offres pour les campagnes, les groupes publicitaires, les mots-clés, les emplacements, les groupes de produits au niveau de l’unité et les cibles de recherche dynamique. Chaque entité ne peut avoir qu&#39;une seule contrainte.

Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire d’affecter des contraintes aux entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

L’annulation de l’affectation d’une contrainte supprime l’association avec les composants de compte et tous leurs composants enfants, et les données de rapport pour la contrainte ne sont plus disponibles pour ces composants. L’annulation de l’affectation d’une contrainte ne supprime pas la contrainte ou les composants de compte eux-mêmes.

>[!NOTE]
>
>* Si vous modifiez par la suite un mot-clé ou la copie d’une publicité non modifiable (créant ainsi un nouveau mot-clé ou une nouvelle publicité), la contrainte n’est pas affectée à la nouvelle entité.
>* Les contraintes actives limitent les enchères uniquement pour les unités d’offre affectées dans les portefeuilles optimisés au niveau des mots-clés hérités. Elles sont ignorées pour les unités d&#39;enchères qui se trouvent dans des portefeuilles actifs, dans des portefeuilles hybrides ou qui ne se trouvent pas dans des portefeuilles.

### Attribuer une contrainte à des mots-clés {#keyword-constraint-assign}

Vous pouvez affecter une seule contrainte à un ou plusieurs mots-clés.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Dans l’onglet **[!UICONTROL Keywords]** , cochez la case en regard de chaque mot-clé auquel vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

### Annuler l’affectation des contraintes des mots-clés {#keyword-constraint-unassign}

L’annulation de l’affectation d’une contrainte ne la supprime pas. Pour supprimer une contrainte, ce qui la rend indisponible pour une utilisation ultérieure, consultez « Supprimer des contraintes pour les unités d’offres de recherche » dans le chapitre du guide d’optimisation sur « Contraintes d’offres », disponible dans Search, Social et Commerce.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Dans l’onglet **[!UICONTROL Keywords]** , cochez la case en regard de chaque mot-clé duquel vous annulez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] paramètres des mots-clés](keyword-settings-baidu.md)
>* [[!DNL Google Ads] paramètres des mots-clés](keyword-settings-google.md)
>* [[!DNL LY Ads] paramètres des mots-clés](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] paramètres des mots-clés](keyword-settings-microsoft.md)
>* [[!DNL Yandex] paramètres des mots-clés](keyword-settings-yandex.md)
>* [Gérer les contraintes pour les unités d’offres de recherche](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Gérer les classifications de libellés](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
