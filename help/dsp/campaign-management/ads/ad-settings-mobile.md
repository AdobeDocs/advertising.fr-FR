---
title: Paramètres des annonces publicitaires mobiles
description: Consultez les descriptions des paramètres d’annonce publicitaire disponibles pour les annonces publicitaires mobiles.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
TQID: https://experienceleague.adobe.com/1e3HmwtXzDUQ60rGhnJ5n-feky0rYlqwt7ZQZ6YXNCQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 516
ht-degree: 0%

---

# Paramètres des annonces publicitaires mobiles

## [!UICONTROL Insert Ad Tag]

*Nouveaux formats de publicités vidéo pour appareils mobiles uniquement*

**[!UICONTROL URL]** ou **[!UICONTROL Ad Tag]** : balise publicitaire VAST tierce ou balise publicitaire contenant des ressources créatives et des pixels de suivi

**[!UICONTROL Ad Title]** ou **[!UICONTROL Title]** : nom de l’annonce publicitaire utilisée dans la vue [!UICONTROL Ads] et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la touche **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant des `<VAST>` s’affiche en haut de l’écran.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic] : publicités display pour appareils mobiles

**[!UICONTROL Ad Type]:** (Lecture seule) Type d’annonce publicitaire que vous créez, qui correspond au type d’emplacement auquel l’annonce publicitaire peut être associée.

**[!UICONTROL Ad Name]:** Nom de l’annonce publicitaire. Le titre de la ressource est utilisé par défaut, mais vous pouvez en modifier le nom.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue Annonces et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que Aperçu du produit de vacances : 300x250 Gamer »).

**\[Ad Source\]** : *[!UICONTROL 3rd party]* (lecture seule).

**[!UICONTROL Display Code]:** URL de la ressource de création tierce. Les paramètres [timestamp] et [[timestamp]] sont remplacés par des valeurs réelles.

**[!UICONTROL Final Display Code]:** URL de la ressource créative tierce, avec les [macros de suivi Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

### [!UICONTROL Basic] : publicités vidéo

**[!UICONTROL Ad Type]:** (Lecture seule) Type d’annonce publicitaire que vous créez, qui correspond au type d’emplacement auquel l’annonce publicitaire peut être associée.

**[!UICONTROL Ad Name]:** Nom de l’annonce publicitaire. Le titre de la ressource est utilisé par défaut, mais vous pouvez en modifier le nom.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue Annonces et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que Aperçu du produit de vacances : préoll de téléphone de 30 secondes).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** largeur de l’ensemble de l’entité publicitaire. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** hauteur de l’ensemble de l’annonce publicitaire. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

**[!UICONTROL Player X]:** coordonnée X de l’entité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Y]:** coordonnée Y de l’entité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Width]:** largeur de l’ensemble de l’entité publicitaire. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

Il s’agit du même champ que le champ **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** hauteur de l’ensemble de l’unité publicitaire. Cette option peut être verrouillée en fonction du type d’unité publicitaire que vous avez sélectionné.

Il s’agit du même champ que le champ **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Où inclure des commandes vidéo pour la publicité : *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** Conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou étirer la vidéo pour remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Certains types d’annonces) Nombre de secondes pendant lesquelles retarder l’aspect du bouton de fermeture.

**[!UICONTROL VAST Tag]:** (publicités à l’aide de balises VAST uniquement ; lecture seule) Balise VAST tierce que vous avez saisie en tant que ressource créative.

**[!UICONTROL Final VAST Tag]:** (publicités à l’aide de balises VAST uniquement ; lecture seule) Balise VAST tierce entrée en tant que ressource créative avec les [macros de suivi Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

**[!UICONTROL Wmode]:** (certains types d’annonces) Mode fenêtre : *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

### [!UICONTROL Sharing]

Obsolète

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités dans Advertising DSP](ad-about.md)
>* [Créer une seule annonce publicitaire](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros &#x200B;](/help/dsp/campaign-management/macros.md)
