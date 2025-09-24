---
title: Paramètres de création dynamique
description: Référencez les paramètres des contenus publicitaires dynamiques.
feature: Creative Dynamic Creatives
source-git-commit: e08a3c841e733840058f85a7ecc67571631314b3
workflow-type: tm+mt
source-wordcount: '277'
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

**[!UICONTROL Ad Template Size]:** dimensions de l’annonce publicitaire pour le modèle d’annonce publicitaire à partir duquel créer l’annonce publicitaire. Si vous sélectionnez d’abord une [!UICONTROL Ad Template] spécifique, cette valeur est automatiquement sélectionnée.

## Modèle de publicité

**[!UICONTROL Ad Template]:** modèle d’annonce publicitaire à partir duquel créer les annonces.&lt;!— également une option pour charger votre propre modèle de publicité — il faut ajouter les spécifications pour cela —>

**[!UICONTROL Number of offers (Max 50)]:** nombre d’offres pouvant être créées pour chaque publicité.&lt;!— Clarifier ceci — s&#39;agit-il de la limitation de fréquence (nombre maximum de fois qu&#39;une publicité peut être diffusée) ? —>

## Catalogues

**[!UICONTROL Template]:** modèle de flux à utiliser pour créer les annonces.&lt;!— également une option pour charger votre propre modèle de flux — il faut ajouter les spécifications pour cela —>

**\[Catalogues\]** : un ou plusieurs catalogues de l’annonceur spécifié à partir desquels générer des publicités.&lt;!— également une option pour télécharger votre propre catalogue (vous ne trouvez pas le catalogue dont vous avez besoin ? Téléchargez un modèle, créez le vôtre et chargez-le à partir de votre appareil.) — il faut ajouter les spécifications pour cela —>

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]** : types de colonnes dans le fichier de flux pour lesquels des valeurs doivent être présentes pour créer des annonces : *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Remarque :** ces paramètres fonctionnent indépendamment des paramètres avancés dans les paramètres d’expérience publicitaire.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Mappez chaque attribut (champ d’annonce dynamique) du modèle d’annonce spécifié à une colonne du fichier de flux spécifié (libellé de catalogue).

>[!MORELIKETHIS]
>
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](creative-add-dynamic.md)
>* [Modification de contenus publicitaires dynamiques dans une bibliothèque de contenus publicitaires](creative-edit-dynamic.md)
>* [Workflow pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
