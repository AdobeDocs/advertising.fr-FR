---
title: Paramètres de publicité preroll
description: Consultez les descriptions des paramètres d’annonce publicitaire disponibles pour les annonces publicitaires preroll.
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
TQID: https://experienceleague.adobe.com/vmZ3LDA5Hz0SgYf-tmWgVTdQyM4sikrJGSsSwOQaV-E
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 450
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

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (publicités preroll standard et pouvant être ignorées uniquement) La hauteur de l’ensemble de l’unité publicitaire. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

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
>* [À propos de la gestion des publicités dans Advertising DSP](ad-about.md)
>* [Créer une seule annonce publicitaire](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros &#x200B;](/help/dsp/campaign-management/macros.md)
