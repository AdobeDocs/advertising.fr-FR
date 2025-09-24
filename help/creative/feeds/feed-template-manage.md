---
title: Gestion des modèles de flux
description: Découvrez comment gérer les modèles de flux.
feature: Creative Dynamic Creatives
source-git-commit: 5828fada55ba9506589df6088ea58b896084700c
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Gestion des modèles de flux

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

Les modèles de flux mappent les champs de vos fichiers de flux avec les champs du serveur principal d’Advertising Creative. Les annonces dynamiques HTML5, mais pas les annonces statiques HTML5, nécessitent un modèle de flux pour créer des annonces dynamiques.

Vous pouvez utiliser un modèle de flux avec plusieurs modèles d’annonces.

## Création d’un modèle de flux

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Spécifiez les [paramètres du modèle de flux](#feed-template-settings).

1. Cliquez sur **[!UICONTROL Save]**.

## Modification d’un modèle de flux

**Remarque :** vous ne pouvez modifier que les modèles de flux que vous avez créés.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL Duplicate]**.

1. Modifiez les [paramètres du modèle de flux](#feed-template-settings) selon vos besoins.

1. Cliquez sur **[!UICONTROL Save]**.

## Affichage d’un modèle de flux

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL View]**.

## Duplication d’un modèle de flux

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL Duplicate]**.

1. Dans l’écran [!UICONTROL Duplicate Template], saisissez un **[!UICONTROL Template Name]** unique. Si vous dupliquez un modèle créé par une autre personne, sélectionnez la **[!UICONTROL Advertiser]**. Vous pouvez éventuellement modifier d’autres [paramètres de modèle de flux](#feed-template-settings) selon vos besoins.

1. Cliquez sur **[!UICONTROL Save]**.

## Téléchargement d’un modèle de flux

Les modèles de flux téléchargés sont au format de feuille de calcul Excel Microsoft (XLSX) compressée.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL Download]**.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

## Paramètres du modèle de flux {#feed-template-settings}

### Paramètres [!UICONTROL General]

**[!UICONTROL Template Name]:** nom de modèle unique pour l’annonceur spécifié.

**[!UICONTROL Advertiser]:** annonceur qui peut utiliser le modèle.

**[!UICONTROL Description]:** (facultatif) Informations utiles à toute personne utilisant le modèle de flux.

### Paramètres [!UICONTROL Field Mapping]

Mappez chaque champ du fichier de flux à un champ du serveur principal d’Advertising Creative.<!-- Check w/product: What is displayed where in the UI/reports and published ads? --> Vous devez inclure au moins un champ de fichier de flux marqué comme « [!UICONTROL Is Unique] ». Pour ajouter un mappage de champs, cliquez sur **[!UICONTROL +]**. Pour supprimer le dernier mappage de champs, cliquez sur **[!UICONTROL +]**.

**[!UICONTROL Field Name]:** champ du fichier de flux.

**[!UICONTROL Description]:** (facultatif) Informations utiles à toute personne utilisant le modèle de flux.

**[!UICONTROL Is Unique]:** indique que le champ est un ID unique (clé). Au moins un champ par modèle de flux doit être unique. Pour sélectionner cette option, cliquez sur le bouton pour la déplacer vers la droite.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** champ du serveur principal d’Advertising Creative qui correspond au [!UICONTROL Field Name] spécifié dans le fichier de flux.

>[!MORELIKETHIS]
>
>* [Workflow pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gérer les fichiers de ressources](/help/creative/feeds/asset-manage.md)
>* [Gérer les catalogues](/help/creative/feeds/catalog-manage.md)
>* [Suivre le statut des tâches de traitement du catalogue](/help/creative/feeds/job-status-track.md)
>* [Gestion des modèles de publicité dynamique](/help/creative/ad-templates/ad-template-manage.md)
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-dynamic.md)
