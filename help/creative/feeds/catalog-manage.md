---
title: Gestion des catalogues de flux
description: Découvrez comment gérer les catalogues de flux.
feature: Creative Dynamic Creatives
exl-id: d3ee20ba-5359-4dbe-bc76-269dc800843c
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Gestion des catalogues de flux

Les catalogues de flux traités sont des ensembles de variations d’annonces potentielles créées à partir d’un fichier de flux spécifié et d’un modèle de flux spécifié. Les publicités dynamiques HTML5 et vidéo, mais pas les publicités HTML5 statiques, nécessitent un catalogue pour créer des publicités dynamiques.

Avant de pouvoir créer des variations d’annonces et [ajouter des annonces dynamiques à une bibliothèque de contenu créatif](/help/creative/creative-libraries/creative-add-dynamic.md), traitez le catalogue. Vous pouvez ensuite mettre à jour le fichier de flux et retraiter le catalogue pour créer un nouvel ensemble de variations d’annonces.<!-- I should list somewhere what happens when you add, update, or remove: I don't think we rewrite existing ads in the creative library, but only add to them. -->

Chaque fichier de flux peut traiter jusqu’à 500 lignes avec des ressources vidéo.

>[!TIP]
>
>Pour tous les comptes disposant de vidéos dynamiques, il est recommandé de [télécharger le modèle de flux universel [!UICONTROL Adobe Creative Template]](feed-template-manage.md), de mapper chaque champ du fichier de ressource à un champ sur le serveur principal d’Advertising Creative, puis de renommer et de charger le modèle de flux. Utilisez le nouveau modèle de flux, ainsi que le fichier de ressource, pour créer un catalogue.

## Création d’un catalogue {#feed-catalog-create}

>[!NOTE]
>
>Vous pouvez également charger directement un catalogue lorsque vous [ajoutez des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-dynamic.md). Tous les catalogues que vous y créez sont disponibles dans la vue [!UICONTROL Catalogs] pour une utilisation ultérieure.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Catalog]** .

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Template]**.

1. Spécifiez les [paramètres du catalogue](#catalog-settings) selon vos besoins.

1. Cliquez sur **[!UICONTROL Next]**.

1. Examinez les variations d’annonces publicitaires potentielles qui peuvent être créées pour le catalogue.

1. Cliquez sur **[!UICONTROL Save]**.

## Modification d’un catalogue

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Catalog]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les [paramètres du catalogue](#catalog-settings) selon vos besoins.

1. Examinez les variations d’annonces publicitaires potentielles qui peuvent être créées pour le catalogue.

1. Cliquez sur **[!UICONTROL Save]**.

## Traitement d’un catalogue {#feed-catalog-process}

Le traitement d’un catalogue rend les variations d’annonces disponibles pour créer des annonces HTML5 dynamiques.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Catalog]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL Run Now]**.

## Mettre en pause un catalogue actif

Mettre en pause un catalogue pour le rendre inactif.<!-- Can you Activate it again? -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL Pause]**.

<!-- Verify if this is available:  1. In the confirmation message, click **[!UICONTROL Pause]**. -->

## Activer un catalogue en pause

<!-- Verify if this is available. -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL Activate]**.

## Archiver un catalogue

Archivez un catalogue pour le supprimer.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de modèle, puis cliquez sur **[!UICONTROL Archive]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Archive]**.

## Paramètres du catalogue {#catalog-settings}

**[!UICONTROL Advertiser]:** annonceur qui peut utiliser le catalogue.

**[!UICONTROL Asset]:** fichier de flux à utiliser comme entrée pour le catalogue.

**[!UICONTROL Catalog Name]:** nom de catalogue unique pour l’annonceur spécifié. Par défaut, le nom du fichier de flux est utilisé, y compris l’extension de fichier, qui est la bonne pratique en matière d’identification.<!-- must it have a file extension? -->

**[!UICONTROL Template]:** modèle de flux à utiliser pour mapper les champs de la ressource/du fichier de flux spécifié aux champs du serveur principal d’Advertising Creative.

>[!MORELIKETHIS]
>
>* [Suivre le statut des tâches de traitement du catalogue](/help/creative/feeds/job-status-track.md)
>* [Workflows pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gérer les fichiers de ressources](/help/creative/feeds/asset-manage.md)
>* [Gérer les modèles de flux](/help/creative/feeds/feed-template-manage.md)
>* [Gestion des modèles de publicité dynamique](/help/creative/ad-templates/ad-template-manage.md)
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-dynamic.md)
