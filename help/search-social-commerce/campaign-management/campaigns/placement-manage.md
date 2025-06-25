---
title: Gestion  [!DNL Google Ads]  emplacements
description: Découvrez comment créer et gérer des emplacements pouvant faire l’objet d’offres pour des groupes  [!DNL Google Ads] .
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Gestion des emplacements [!DNL Google Ads]

Comptes *[!DNL Google Ads]uniquement*

Vous pouvez créer et modifier des emplacements pour des groupes publicitaires dans [types de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) qui ciblent le réseau d’affichage dans un [compte de réseau publicitaire synchronisé](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Créer des emplacements [!DNL Google Ads]

>[!TIP]
>
>Pour créer plusieurs emplacements à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire, le compte, la campagne et le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Configurez les [paramètres d’emplacement](#placement-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Modifier les emplacements de [!DNL Google Ads]

>[!TIP]
>
>Pour modifier plusieurs emplacements à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Cochez la case en regard de chaque ligne à modifier.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") .

1. Modifiez les [paramètres d’emplacement](#placement-settings).

   Dans le cas de plusieurs emplacements, vos modifications sont appliquées à tous les emplacements sélectionnés. Pour certains champs alphanumériques, vous pouvez modifier les valeurs existantes à une valeur spécifiée, remplacer une chaîne existante par une chaîne spécifiée, ajouter un préfixe spécifié au début de chaque valeur ou ajouter un suffixe à la fin de chaque valeur. Pour certains champs monétaires, vous pouvez modifier les valeurs existantes à une valeur spécifiée ou augmenter ou diminuer le montant d’un pourcentage ou d’un montant monétaire spécifié, avec une limite.

1. Enregistrez les données :

   * (Emplacements uniques) Cliquez sur **[!UICONTROL Post]**.

   * (Plusieurs emplacements) Cliquez sur **[!UICONTROL Post Now]**.

## Paramètres d’emplacement {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites sur le réseau de contenu sur lequel votre publicité peut apparaître. Saisissez une URL valide, telle que www.example.com, example.com ou www.example.com/shoes/kids. Pour spécifier plusieurs chaînes, séparez-les par des virgules ou saisissez-les sur des lignes distinctes. L’URL ne peut pas inclure de point d’interrogation (`?`). **Remarque :** vous pouvez [exclure les emplacements de site web](placement-negative-create.md) de la vue [!UICONTROL Placements] > [!UICONTROL Negatives] et dans les paramètres du groupe publicitaire et de la campagne.

**[!UICONTROL Status]:** statut d’affichage de l’emplacement : *Actif* (pour activer les enchères, valeur par défaut), *En pause* (pour désactiver les enchères) ou *Supprimé* (pour supprimer l’emplacement ; emplacements existants uniquement).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (facultatif) Coût maximum par clic (CPC) ou coût par mille impressions visibles (vCPM) pour l’annonce basée sur l’emplacement, en fonction de la stratégie d’enchères de la campagne. Cette valeur remplace l’enchère au niveau du groupe publicitaire.

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
>* [Modifier le statut des emplacements et des emplacements négatifs](placement-status-edit.md)
