---
title: Gérer [!DNL Google Ads] emplacements
description: Découvrez comment créer et gérer des emplacements abordables pour [!DNL Google Ads] groupes publicitaires.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Gérer [!DNL Google Ads] emplacements

*[!DNL Google Ads]comptes uniquement*

Vous pouvez créer et modifier des emplacements pour des groupes publicitaires dans [types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) qui ciblent le réseau d’affichage dans un [compte réseau publicitaire synchronisé](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Créer [!DNL Google Ads] emplacements

>[!TIP]
>
>Pour créer plusieurs emplacements simultanément, utilisez [feuilles d’envoi groupé de campagnes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Configurez la variable [paramètres de placement](#placement-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Modifier [!DNL Google Ads] emplacements

>[!TIP]
>
>Pour modifier plusieurs emplacements simultanément, utilisez [feuilles d’envoi groupé de campagnes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Cochez la case en regard de chaque ligne à modifier.

   Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") .

1. Modifiez la variable [paramètres de placement](#placement-settings).

   Pour plusieurs emplacements, les modifications sont appliquées à tous les emplacements sélectionnés. Pour certains champs alphanumériques, vous pouvez remplacer des valeurs existantes par une valeur spécifique, remplacer une chaîne existante par une chaîne spécifiée, ajouter un préfixe spécifique au début de chaque valeur ou ajouter un suffixe à la fin de chaque valeur. Pour certains champs monétaires, vous pouvez modifier les valeurs existantes en une valeur spécifique ou augmenter ou diminuer le montant d’un pourcentage ou d’un montant monétaire spécifié, avec une limite.

1. Enregistrez les données :

   * (Emplacements uniques) Cliquez sur **[!UICONTROL Post]**.

   * (Plusieurs emplacements) Cliquez sur **[!UICONTROL Post Now]**.

## Paramètres d’emplacement {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites sur le réseau de contenu sur lequel votre publicité peut apparaître. Saisissez une URL valide, telle que www.example.com, example.com ou www.example.com/shoes/kids. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes. L’URL ne peut pas inclure de point d’interrogation (`?`). **Remarque :** Vous pouvez [exclure des emplacements de site web](placement-negative-create.md) de la [!UICONTROL Placements] > [!UICONTROL Negatives] afficher et dans les paramètres du groupe publicitaire et de la campagne.

**[!UICONTROL Status]:** État d’affichage de l’emplacement : *Principal* (pour permettre l’enchère) la valeur par défaut), *En pause* (pour désactiver l’offre) ou *Supprimé* (pour supprimer l’emplacement ; emplacements existants uniquement).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Facultatif) Le coût par clic (CPC) ou le coût par millier d’impressions visualisables (vCPM) pour la publicité basée sur l’emplacement, selon la stratégie d’offre de la campagne. Cette valeur remplace l’offre au niveau du groupe publicitaire.

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [À propos des emplacements](placement-about.md)
>* [Créer des emplacements négatifs](placement-negative-create.md)
>* [Modifier l’état des emplacements et des emplacements négatifs](placement-status-edit.md)

