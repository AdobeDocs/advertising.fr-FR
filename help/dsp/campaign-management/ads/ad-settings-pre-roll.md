---
title: Paramètres de publicité preroll
description: Consultez les descriptions des paramètres d’annonce publicitaire disponibles pour les annonces publicitaires preroll.
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# Paramètres de publicité preroll

## [!UICONTROL Insert Ad Tag]

*Nouvelles annonces uniquement*

**[!UICONTROL URL]:** l’URL de balise VAST.

**[!UICONTROL Title]:** Titre du fichier, qui se trouve dans la vue [!UICONTROL Ads] et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la touche **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant des `<VAST>` s’affiche en haut de l’écran.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Lecture seule) Type d’annonce publicitaire que vous créez, qui correspond au type d’emplacement auquel l’annonce publicitaire peut être associée.

**[!UICONTROL Ad Name]:** Nom de l’annonce publicitaire. Le titre de la ressource est utilisé par défaut, mais vous pouvez en modifier le nom.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que Prévisualisation du produit Holiday : preroll de 30 secondes).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (publicités preroll standard et pouvant être ignorées uniquement) La largeur de l’unité publicitaire entière. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (publicités preroll standard et pouvant être ignorées uniquement) Hauteur de l’ensemble de l’unité publicitaire. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

**[!UICONTROL Player X]:** coordonnée X de l’entité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Y]:** coordonnée Y de l’entité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Width]:** largeur de l’ensemble de l’entité publicitaire. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

Ce champ est identique au champ **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** hauteur de l’ensemble de l’unité publicitaire. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

Il s’agit du même champ que le champ **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Où inclure des commandes vidéo pour la publicité : *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** Conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou étirer la vidéo pour remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (publicités à l’aide de balises VAST uniquement ; lecture seule) Balise VAST tierce que vous avez saisie en tant que source de publicité.

**[!UICONTROL Final VAST Tag]:** (publicités à l’aide de balises VAST uniquement ; lecture seule) Balise VAST tierce entrée en tant que source de publicité avec les [macros de suivi Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

**[!UICONTROL Wmode]:** (Pré-roll interactif uniquement) Mode fenêtre : *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Pré-roll interactif uniquement) Format du lecteur d’annonces pour l’inventaire potentiel : *[!UICONTROL VPAID]* ou *[!UICONTROL VPAID & VAST]*. La visibilité est toujours mesurée pour VPAID, mais VPAID &amp; VAST inclut un inventaire qui ne permet pas de mesurer la visibilité. Tenez compte de cette distinction si les mesures de visibilité sont importantes pour votre campagne.

**[!UICONTROL Clock Number]** : (pré-roll interactif uniquement ; utilisé uniquement au Royaume-Uni ; disponible uniquement pour les utilisateurs avec autorisation) Identifiant unique utilisé pour s’assurer que la bonne publicité est diffusée. Si ce paramètre n’est pas applicable, laissez-le vide.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
