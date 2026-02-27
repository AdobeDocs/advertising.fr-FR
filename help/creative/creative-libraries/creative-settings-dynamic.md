---
title: Paramètres de création dynamique
description: Référencez les paramètres des contenus publicitaires dynamiques.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 164ee92f85c0e649dc2bd6c0224a531eb72d1962
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Paramètres de création dynamique

<!-- add a description -->

## Paramètres des annonces dynamiques<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Détails de base

**[!UICONTROL Creative Type]:** indique si le contenu publicitaire est une publicité *[!UICONTROL Display]* (HTML5) ou une publicité *[!UICONTROL Video]*.

**[!UICONTROL Dynamic Display Ad Name]** ou **[!UICONTROL Dynamic Video Ad Name]:** nom unique du contenu créatif.

**[!UICONTROL Advertiser]:** annonceur pour lequel créer les annonces. Si vous créez les annonces à partir de [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], l’annonceur est déjà sélectionné et en lecture seule.

**[!UICONTROL Library]:** bibliothèque créative dans laquelle créer les annonces. Si vous créez les annonces à partir de [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], le nom de la bibliothèque est déjà sélectionné et en lecture seule.

## Modèle de publicité

**[!UICONTROL Ad Template]:** modèle d’annonce publicitaire à partir duquel créer les annonces. Sélectionnez un modèle d’annonce existant ou chargez un nouveau modèle d’annonce et sélectionnez le type de modèle (*Statique* ou *Dynamique*). Le modèle doit être au format ZIP et contenir : <!-- Need to add more specs for templates -->

* Afficher les éléments créatifs : fichiers HTML5 au format publicitaire souhaité et (annonces HTML5 dynamiques uniquement) un fichier avec les attributs publicitaires (.tdf)

* Contenus vidéo : un fichier .scene avec le format publicitaire souhaité. Le fichier ZIP ne doit pas dépasser 512 Mo.

Pour continuer, cliquez sur **[!UICONTROL Select Ad Template]**.

**[!UICONTROL Size]:** (Annonces dynamiques uniquement ; lecture seule) [dimensions de l’annonce](/help/creative/creative-libraries/creative-sizes.md) pour le modèle d’annonce sélectionné, qui est utilisé pour créer les annonces.

**[!UICONTROL Card Count (Max 50)]:** (Affichage des annonces uniquement) Nombre de produits à afficher dans un carrousel.

**[!UICONTROL Duration]:** (publicités vidéo uniquement ; lecture seule) Durée de la vidéo dérivée du modèle de publicité sélectionné. La durée de chaque vidéo doit être comprise entre 1 et 90 secondes.

## Catalogues

**\[Catalogs\]** : un ou plusieurs catalogues à partir desquels générer des annonces. Sélectionnez un catalogue existant ou créez un catalogue en téléchargeant un modèle de flux existant, puis en créant et en chargeant le nouveau catalogue. Cliquez sur **[!UICONTROL Select Catalog]**.

Les catalogues chargés doivent être au format ZIP et contenir les éléments suivants :

* (Affichage dynamique et publicités vidéo) Un ou plusieurs fichiers de flux au format CSV, TSV ou feuille de calcul Excel Microsoft (XLSX). La taille de fichier maximale est de 512 Mo.<!-- Need to add more specs for the feed files -->

* (Affichages publicitaires) Ressources d’image au format GIF, JPEG, JPG ou PNG

* (Publicités vidéo) Ressources vidéo au format MP4, MOV ou WEBM. Les modèles d’annonce pris en charge sont les suivants : carte de départ, carte d’extrémité, superposition supérieure, superposition inférieure ou en forme de L. La durée de chaque vidéo doit être comprise entre 1 et 90 secondes.

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]** : <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->types de colonnes du fichier de flux pour lesquels des valeurs doivent être présentes pour créer des annonces : *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Remarque :** ces paramètres fonctionnent indépendamment des paramètres avancés dans les paramètres d’expérience publicitaire.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mappez chaque attribut (champ d’annonce dynamique) du modèle d’annonce spécifié sur une colonne du catalogue spécifié (libellé du catalogue) ou saisissez une valeur statique.

>[!MORELIKETHIS]
>
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](creative-add-dynamic.md)
>* [Modification de contenus publicitaires dynamiques dans une bibliothèque de contenus publicitaires](creative-edit-dynamic.md)
>* [Workflows pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
