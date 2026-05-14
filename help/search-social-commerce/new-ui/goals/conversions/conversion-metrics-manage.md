---
title: Gérer les mesures de conversion d’un annonceur
description: Découvrez comment utiliser les mesures de conversion suivies par Adobe Advertising pour un annonceur.
feature: Conversions
source-git-commit: 3272a0d3e5766a22c2ff761b84f1774cafe153bd
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gérer et afficher les données de performances pour les mesures de conversion d’un annonceur

*Fonction*

Les mesures [conversion](/help/search-social-commerce/glossary.md#c-d) d’un annonceur sont utilisées dans Adobe Advertising :

* Dans Search, Social et Commerce, les données des mesures de conversion peuvent être affichées sous forme de colonnes dans les vues de gestion de campagnes, de portefeuilles et d’objectifs, ainsi que dans les rapports. Les utilisateurs disposant de droits d’accès suffisants peuvent également utiliser les mesures de conversion pour créer des objectifs utilisés pour optimiser les portfolios.

* (Annonceurs avec Advertising DSP) Dans DSP, vous pouvez inclure des mesures de conversion dans les vues de gestion de campagne, les objectifs personnalisés et les rapports personnalisés. Vous pouvez également utiliser les mesures de conversion pour créer des [objectifs personnalisés](/help/dsp/admin/custom-objectives-manage.md), qui sont utilisés pour optimiser les packages.

Les mesures disponibles sont les suivantes :

* Mesures de conversion suivies par Adobe Advertising pour un annonceur.

* [Mesures d’engagement du site et de conversion synchronisées à partir d’Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Événements de site synchronisés à partir d’Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Conversions suivies par [!DNL Google Ads] et conversions suivies par [!DNL Microsoft Advertising] balises de suivi des événements universels.

* (Lorsque [vous avez configuré une combinaison de compte [!DNL Google Analytics]  de propriété et d’affichage spécifique en tant que source de données](/help/search-social-commerce/admin/data-sources/data-source-about.md) pour les conversions Search, Social et Commerce) suivies par [!DNL Google Analytics].

* Conversions à partir de flux personnalisés.

Dans la liste des mesures de conversion disponibles, chaque utilisateur ayant accès aux données de l’annonceur peut personnaliser les mesures qui s’affichent pour les vues et les rapports de gestion, y compris des mesures spécifiques, qu’il choisit ou non. Vous pouvez utiliser un nom de mesure tel qu’il est orthographié dans les données récupérées ou modifier le nom affiché dans les en-têtes de colonne pour en faciliter la lecture.

>[!IMPORTANT]
>
>Par défaut, aucune des mesures de conversion d’un annonceur, à l’exception des conversions suivies par les balises de suivi d’événement universel [!DNL Google Ads], [!DNL Google Analytics] et [!DNL Microsoft Advertising], n’est disponible pour inclusion dans les vues, objectifs et rapports de gestion de campagnes et de portefeuilles. Pour rendre une mesure de conversion disponible, vous devez la rendre explicitement disponible.
>
>Les nouvelles conversions suivies par les balises de suivi d’événement universel [!DNL Google Ads], [!DNL Google Analytics] et [!DNL Microsoft Advertising] sont toujours automatiquement disponibles.

>[!TIP]
>
>Une fois que l’annonceur (ou le réseau publicitaire) cesse de collecter une mesure de conversion, [masquez-la dans les vues et les rapports de gestion](#conversion-metrics-change-available) à moins que vous ne souhaitiez l’utiliser pour afficher les données historiques.

## Affichage des mesures de conversion suivies pour un annonceur

* Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

Toutes les mesures de conversion qui ont été collectées pour l’annonceur, ainsi que tous les noms d’affichage différents qui leur ont été attribués, sont répertoriés. Chaque ligne de mesure inclut la source de la mesure.

## Modification du nom d’affichage d’une mesure de conversion

Par exemple, si vous collectez des données d’enregistrement à l’aide d’une mesure de conversion nommée *reg*, vous pouvez éventuellement modifier le nom d’affichage pour qu’il s’affiche sous la forme « Enregistrements ».

Vous ne pouvez pas supprimer un nom d’affichage existant.

>[!NOTE]
>
>Pour les [mesures de [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md), toute modification manuelle apportée au nom d’affichage est remplacée si vous mettez à jour ou authentifiez à nouveau l’intégration. De même, toute modification de nom dans [!DNL Google Analytics] est ignorée, sauf si vous [mettez à jour](/help/search-social-commerce/admin/data-sources/data-source-edit.md) ou [réauthentifiez](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md) l’intégration.

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Filtrez la liste [à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou d’un [en-tête de colonne](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Dans la colonne **[!UICONTROL Conversion Display Name]** de la mesure, placez le curseur sur le nom de la mesure, puis cliquez sur **...** > **[!UICONTROL Rename]**.

1. Saisissez le nom à afficher, puis cliquez sur **[!UICONTROL Apply]**.

   Les noms d&#39;affichage doivent être uniques et ne peuvent pas contenir les caractères spéciaux suivants : `\"<'>&`

## Modifier les mesures de conversion disponibles dans les vues de gestion, les objectifs et les rapports {#conversion-metrics-change-available}

>[!NOTE]
>
>Lorsque vous masquez une mesure de conversion qui était auparavant disponible, elle est supprimée de toute mesure dérivée contenant la mesure de conversion.

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

   Toutes les mesures de conversion qui ont été collectées pour l’annonceur, ainsi que tous les noms différents qui ont été spécifiés pour l’affichage, sont répertoriés.

1. (Facultatif) Filtrez la liste [à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou d’un en-tête de colonne [](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Modifiez les mesures de conversion disponibles pour les vues et les rapports de gestion :

   * Pour afficher ou masquer une seule mesure, cliquez sur le bouton (bascule) de la colonne **[!UICONTROL Visibility]** pour modifier le paramètre.

   * Pour afficher ou masquer plusieurs mesures, procédez comme suit :

      1. Cochez la case en regard de chaque mesure de conversion.

         Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

      1. Dans la barre d’outils des actions en masse, cliquez sur ![Visibilité](/help/search-social-commerce/assets/visible.png "Visibilité") pour afficher les mesures ou sur ![Visibilité désactivée](/help/search-social-commerce/assets/visibility-off.png "Visibilité désactivée") pour masquer les mesures.

      1. (Pour masquer les mesures) Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]** pour masquer les mesures, y compris en les supprimant de toutes les mesures dérivées qui contiennent les mesures.

## Gérer les rapports de données de performance pour les conversions

Vous pouvez télécharger les informations suivantes sur vos conversions suivies : le nom de la mesure synchronisée, le nom d’affichage de la mesure dans les vues et rapports de gestion Search, Social et Commerce, si la mesure est visible dans les vues et rapports de gestion, l’identifiant de conversion et la source de la mesure. Téléchargez les données dans un fichier au format [!DNL Microsoft Excel] classeur (fichier XLSX).

### Générer un rapport avec les lignes de données filtrées

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Indiquez les conversions dont vous souhaitez télécharger les données :

   * Pour télécharger des données pour des lignes spécifiques, cochez les cases en regard des lignes.

   * Pour télécharger des données pour toutes les lignes, il n’est pas nécessaire de cocher des cases. Toutes les lignes sont incluses par défaut.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans les paramètres de [!UICONTROL Grid Reports], saisissez un nom de rapport unique, puis cliquez sur **[!UICONTROL Generate]**.

   Par défaut, le fichier est nommé « conversionsReport_YYYYMMDD_NNNN », où « NNNN » correspond au numéro de tâche séquentiel (par exemple, « conversionsReport_20260402_1326 »).

   Le fichier est ajouté à la liste de [!UICONTROL Recently Generated].

1. (Facultatif) Pour télécharger le fichier une fois l’opération terminée, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Télécharger un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Supprimer un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") **[!UICONTROL Reports]**.

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") en regard du nom du fichier.

<!--
>[!MORELIKETHIS]
>
>* 
-->
