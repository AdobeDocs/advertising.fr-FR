---
title: Paramètres des publicités mobiles
description: Consultez la description des paramètres d’annonce disponibles pour les annonces mobiles.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# Paramètres des publicités mobiles

## [!UICONTROL Insert Ad Tag]

*Nouveaux formats de publicités vidéo mobiles uniquement*

**[!UICONTROL URL]** ou **[!UICONTROL Ad Tag]** : balise publicitaire VAST tierce ou balise publicitaire contenant des ressources créatives et des pixels de suivi

**[!UICONTROL Ad Title]** ou **[!UICONTROL Title]** : nom de la publicité utilisée dans la vue [!UICONTROL Ads] et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la clé **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant `<VAST>` se trouve près de la partie supérieure.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic] : Publicités d’affichage mobiles

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue Publicités et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que &quot;Holiday Product Preview: 300x250 Gamer&quot;).

**\[Ad Source\]** : (lecture seule) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** URL de la ressource créative tierce. Tous les paramètres [timestamp] et [[timestamp]] sont remplacés par des valeurs réelles.

**[!UICONTROL Final Display Code]:** URL de la ressource créative tierce, avec les [ macros de suivi Advertising DSP ](/help/dsp/campaign-management/macros.md) nécessaires insérées, le cas échéant.

### [!UICONTROL Basic] : Publicités vidéo

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue Publicités et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’ aperçu du produit Vacances : Preroll 30s Phone&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width] :** largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height] :** Hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Player X]:** Coordonnée X de l’unité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Y]:** Coordonnée Y de l’unité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Width]:** Largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

Identique au champ **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** Hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

Identique au champ **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Où inclure les commandes vidéo pour la publicité : *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** Indique s’il faut conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou étirer la vidéo pour remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Certains types d’annonces) Le nombre de secondes pour retarder l’apparition du bouton de fermeture.

**[!UICONTROL VAST Tag]:** (Publicités utilisant des balises VAST uniquement ; lecture seule) Balise VAST tierce que vous avez entrée en tant que ressource créative.

**[!UICONTROL Final VAST Tag]:** (Publicités utilisant des balises VAST uniquement ; lecture seule) La balise VAST tierce que vous avez entrée en tant que ressource créative avec les [macros de suivi Advertising DSP](/help/dsp/campaign-management/macros.md) nécessaires insérées, le cas échéant.

**[!UICONTROL Wmode]:** (Certains types d’annonces) Mode de fenêtre : *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction des besoins de suivi pour l’annonce individuelle. **Conseil :** Pour modifier les pixels de suivi tiers pour plusieurs publicités à la fois dans un emplacement à l’aide de la vue [!UICONTROL Ad Tools], voir &quot;[Joindre des pixels de suivi tiers aux publicités dans un emplacement](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour le [!UICONTROL Pixel Type] spécifié.

**[!UICONTROL Pixel Name]:** Nom du pixel. Utilisez un nom qui vous aide à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** Fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

### [!UICONTROL Sharing]

Obsolète

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications de la publicité](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
