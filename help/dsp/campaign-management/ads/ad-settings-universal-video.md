---
title: Paramètres de publicité vidéo universelle
description: Consultez les descriptions des paramètres d’annonce disponibles pour les publicités vidéo universelles.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Paramètres de publicité vidéo universelle

>[!NOTE]
>
>Les publicités vidéo universelles ne peuvent être associées qu’à des emplacements vidéo universels.

## [!UICONTROL Insert Ad Tag]

*Nouvelles publicités uniquement*

**[!UICONTROL URL]:** URL de balise VAST.

**[!UICONTROL Title]:** Titre du fichier, qui se trouve dans la vue [!UICONTROL Ads] et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la clé **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant `<VAST>` se trouve près de la partie supérieure.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’ aperçu du produit Vacances : vidéo universelle 30 secondes).

**[!UICONTROL Show Controls]:** Où inclure les commandes vidéo pour la publicité : *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** Indique s’il faut conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou étirer la vidéo pour remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Publicités utilisant des balises VAST uniquement ; lecture seule) Balise VAST tierce que vous avez entrée en tant que source de la publicité.

**[!UICONTROL Final VAST Tag]:** (Publicités utilisant des balises VAST uniquement ; lecture seule) La balise VAST tierce que vous avez entrée en tant que source de la publicité avec les [macros de suivi Advertising DSP](/help/dsp/campaign-management/macros.md) nécessaires insérées, le cas échéant.

**[!UICONTROL Wmode]:** Mode de fenêtre : *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*. Si ce paramètre n’est pas applicable, laissez-le vide.

**[!UICONTROL Video Format]:** Format du lecteur de publicités pour l’inventaire potentiel : *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* ou *[!UICONTROL VAST]*. La visibilité est toujours mesurée pour [!UICONTROL VPAID], mais [!UICONTROL VPAID & VAST] comprend un inventaire qui ne permet pas la mesure de la visibilité. Tenez compte de cette distinction si les mesures de visibilité sont importantes pour votre campagne.

Utilisez [!UICONTROL VAST], ce qui n’autorise pas la mesure de la visibilité, lorsque vous ciblez la télévision connectée ou un inventaire qui ne nécessite que strictement le format VAST (provenant généralement de sources d’approvisionnement telles que Google Ad Manager, Appnexus, SpotX et FreeWheeler). Utilisez également cette option pour un inventaire qui était précédemment compatible avec les emplacements/publicités standard preroll (VAST) ou Phone + Tablet Standard Pre-roll (VAST).

**[!UICONTROL Clock Number]** : (utilisé uniquement au Royaume-Uni ; disponible uniquement pour les utilisateurs autorisés). Identifiant unique utilisé pour garantir la diffusion de la bonne publicité. Si ce paramètre n’est pas applicable, laissez-le vide.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction des besoins de suivi pour l’annonce individuelle. **Conseil :** Pour modifier les pixels de suivi tiers pour plusieurs publicités à la fois dans un emplacement à l’aide de la vue [!UICONTROL Ad Tools], voir &quot;[Joindre des pixels de suivi tiers aux publicités dans un emplacement](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour le [!UICONTROL Pixel Type] spécifié.

**[!UICONTROL Pixel Name]:** Nom du pixel. Utilisez un nom qui vous aide à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** Fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [ Questions fréquentes à propos de la vidéo universelle ](/help/dsp/campaign-management/faq-universal-video.md)
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications de la publicité](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
