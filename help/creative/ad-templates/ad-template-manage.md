---
title: Gestion des modèles de publicité dynamique
description: Découvrez comment gérer les modèles d’annonces dynamiques et créer des annonces à partir de ceux-ci.
feature: Creative Templates
exl-id: 248f1467-ebd3-47f2-a24c-043bbfadcc6e
source-git-commit: 7945887cf34c5ff390a35f1b9a6ede2888254c65
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# Gestion des modèles de publicité dynamique

Créez un modèle de publicité distinct pour chaque combinaison de type de publicité (HTML5 statique ou HTML5 dynamique) et de taille de publicité en chargeant un fichier HTML5 compressé au format de publicité souhaité. Pour les publicités HTML5 dynamiques, vous téléchargez également un fichier contenant les attributs de la publicité<!-- more clarification? -->.

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Création d’un modèle de publicité dynamique

>[!NOTE]
>
>Vous pouvez également charger un modèle de publicité dynamique lorsque vous [ajoutez des contenus publicitaires dynamiques à une bibliothèque de contenus créatifs](/help/creative/creative-libraries/creative-add-dynamic.md). Tous les modèles d’annonce publicitaire que vous y créez sont disponibles dans la vue [!UICONTROL Ad Templates] pour une utilisation ultérieure.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create Ad Template]**

1. Spécifiez les paramètres du modèle [ad](#ad-template-settings)

1. Cliquez sur **[!UICONTROL Create]**.

## Modification d’un modèle de publicité dynamique

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Placez le curseur sur la ligne du modèle d’annonce et cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les paramètres du modèle [ad](#ad-template-settings).

1. Cliquez sur **[!UICONTROL Save]**.

## Téléchargement d’un modèle de publicité dynamique

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Placez le curseur sur la ligne du modèle d’annonce et cliquez sur **[!UICONTROL Download]**.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

## Suppression d’un modèle de publicité dynamique

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Placez le curseur sur la ligne du modèle d’annonce et cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Création d’annonces dynamiques à partir d’un modèle d’annonce

>[!NOTE]
>
>Vous pouvez également [ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-dynamic.md) à partir de cette dernière.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Placez le curseur sur la ligne du modèle d’annonce et cliquez sur **[!UICONTROL Create Dynamic Ad]**.

   Dans l’écran [!UICONTROL New Dynamic Ad], les champs [!UICONTROL Ad Template Size], [!UICONTROL Ad Template Type] et [!UICONTROL Ad Template] sont automatiquement sélectionnés et en lecture seule.

1. Spécifiez les paramètres des annonces dynamiques pour [créer les annonces dynamiques](/help/creative/creative-libraries/creative-add-dynamic.md).

## Paramètres des modèles de publicité {#ad-template-settings}

### Détails du modèle de publicité

**[!UICONTROL Advertiser]** : (lecture seule pour les modèles existants) Annonceur pour lequel les annonces seront générées.

**[!UICONTROL Ad Template Name]** : nom de modèle d’annonce publicitaire unique pour l’annonceur.

**[!UICONTROL Ad Template Type]** : (lecture seule pour les modèles existants). Format du modèle d’annonce : *HTML statique5* ou *HTML dynamique5*.

**[!UICONTROL Ad Template Size]** : (lecture seule pour les modèles existants) dimensions des annonces créées par le modèle.

**[!UICONTROL Description]** : (facultatif) informations utiles à toute personne utilisant le modèle d’annonce.

### (Modèles d’annonces HTML5 statiques) Cliquez sur Balises

**\[Paramètre de balise de clic\]** : paramètres de balise de clic pour autoriser les redirections de suivi des clics à partir d’annonces créées à l’aide du modèle d’annonce. Pour ajouter un paramètre, cliquez sur **[!UICONTROL + Add More]** et saisissez un paramètre supplémentaire. Vous pouvez inclure jusqu’à cinq paramètres.

### HTML5 zip

Fichier HTML5 compressé au format publicitaire souhaité. Si vous avez déjà chargé un fichier, son nom est indiqué.

Voir la spécification de création [HTML5](/help/creative/creative-libraries/html5-creative-specification.md).

Pour charger un fichier :

1. Cliquez sur **[!UICONTROL Upload HTML5 zip]**.

1. Localisez le fichier sur votre appareil ou réseau.

### (Modèles de publicité Dynamic HTML5) Fichier d’attributs

<!-- EXPLAIN and ad specs below for this file type -->Fichier contenant des attributs pour le modèle de publicité. Si vous avez déjà chargé un fichier, son nom est indiqué.

Pour charger un fichier :

1. Cliquez sur **[!UICONTROL Upload Attributes File]**.

1. Localisez le fichier sur votre appareil ou réseau.

>[!MORELIKETHIS]
>
>* [Workflows pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gérer les fichiers de ressources](/help/creative/feeds/asset-manage.md)
>* [Gérer les modèles de flux](/help/creative/feeds/feed-template-manage.md)
>* [Gérer les catalogues](/help/creative/feeds/catalog-manage.md)
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-dynamic.md)
