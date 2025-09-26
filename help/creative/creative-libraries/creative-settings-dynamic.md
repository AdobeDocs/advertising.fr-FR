---
title: Paramètres de création dynamique
description: Référencez les paramètres des contenus publicitaires dynamiques.
feature: Creative Dynamic Creatives
source-git-commit: 31651c4e30d22b4d1639ef3fc05d5ff9e02dd040
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Paramètres de création dynamique

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## Paramètres des annonces dynamiques<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Détails de base

**[!UICONTROL Dynamic Ad Name]:** Nom unique du contenu créatif.

**[!UICONTROL Advertiser]:** annonceur pour lequel créer les annonces.

**[!UICONTROL Library]:** bibliothèque créative dans laquelle créer les annonces. Si vous créez les annonces à partir de [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], le nom de la bibliothèque est déjà sélectionné et en lecture seule.

**[!UICONTROL Ad Template Size]:** dimensions [annonce publicitaire](/help/creative/creative-libraries/creative-sizes.md) du modèle d’annonce publicitaire à partir duquel créer l’annonce publicitaire. Si vous sélectionnez d’abord une [!UICONTROL Ad Template] spécifique, cette valeur est automatiquement sélectionnée.

## Modèle de publicité

**[!UICONTROL Ad Template]:** modèle d’annonce publicitaire à partir duquel créer les annonces. Sélectionnez un modèle d’annonce existant ou chargez un nouveau modèle d’annonce et sélectionnez le type de modèle (*Statique* ou *Dynamique*). Un modèle chargé doit être au format ZIP et contenir des fichiers HTML5 et un fichier de définition de modèle (template.TDF). <!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]:** nombre de produits à afficher dans un carrousel.

## Catalogues

**[!UICONTROL Template]:** modèle de flux à utiliser pour créer les annonces.

**\[Catalogs\]** : un ou plusieurs catalogues à partir desquels générer des annonces. Sélectionnez un catalogue existant ou créez un catalogue en téléchargeant un modèle de flux existant, puis en créant et en chargeant le nouveau catalogue.

Les catalogues chargés doivent être au format ZIP et contenir les éléments suivants :

* Un ou plusieurs fichiers de flux au format CSV, TSV ou feuille de calcul Microsoft Excel (XLSX).<!-- Need to add more specs for that -->

* Ressources d’image au format GIF, JPEG, JPG ou PNG

* (Facultatif) Ressources vidéo au format MP4 ou WEBM

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]** : <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->types de colonnes du fichier de flux pour lesquels des valeurs doivent être présentes pour créer des annonces : *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Remarque :** ces paramètres fonctionnent indépendamment des paramètres avancés dans les paramètres d’expérience publicitaire.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mappez chaque attribut (champ d’annonce dynamique) du modèle d’annonce spécifié sur une colonne du catalogue spécifié (libellé du catalogue) ou saisissez une valeur statique.

>[!MORELIKETHIS]
>
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](creative-add-dynamic.md)
>* [Modification de contenus publicitaires dynamiques dans une bibliothèque de contenus publicitaires](creative-edit-dynamic.md)
>* [Workflows pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
