---
title: Paramètres universels des publicités vidéo
description: Consultez les descriptions des paramètres d’annonces publicitaires disponibles pour les annonces vidéo universelles.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Paramètres universels des publicités vidéo

>[!NOTE]
>
>Les publicités vidéo universelles ne peuvent être associées qu’à des emplacements vidéo universels.

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
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que Aperçu du produit Holiday : vidéo universelle de 30 secondes).

**[!UICONTROL Show Controls]:** Où inclure des commandes vidéo pour la publicité : *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** Conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou étirer la vidéo pour remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (publicités à l’aide de balises VAST uniquement ; lecture seule) Balise VAST tierce que vous avez saisie en tant que source de publicité.

**[!UICONTROL Final VAST Tag]:** (publicités à l’aide de balises VAST uniquement ; lecture seule) Balise VAST tierce entrée en tant que source de publicité avec les [macros de suivi Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

**[!UICONTROL Wmode]:** mode fenêtre : *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*. Si ce paramètre n’est pas applicable, laissez-le vide.

**[!UICONTROL Video Format]:** format du lecteur d’annonces pour l’inventaire potentiel : *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* ou *[!UICONTROL VAST]*. La visibilité est toujours mesurée pour les [!UICONTROL VPAID], mais [!UICONTROL VPAID & VAST] inclut l’inventaire qui ne permet pas de mesurer la visibilité. Tenez compte de cette distinction si les mesures de visibilité sont importantes pour votre campagne.

Utilisez [!UICONTROL VAST], qui ne permet pas de mesurer la visibilité, lorsque vous ciblez une télévision connectée ou un inventaire qui nécessite uniquement un format VAST (généralement à partir de sources d’approvisionnement telles que Google Ad Manager, Appnexus, SpotX et Freewheel). Utilisez également cette option pour les stocks qui étaient auparavant compatibles avec les placements/annonces pré-roll standard (VAST) ou Phone + Tablet Standard (VAST).

**[!UICONTROL Clock Number]** : (utilisé uniquement au Royaume-Uni ; disponible uniquement pour les utilisateurs autorisés) Identifiant unique utilisé pour s’assurer que la bonne publicité est diffusée. Si ce paramètre n’est pas applicable, laissez-le vide.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser les pixels existants et créer de nouveaux pixels si nécessaire, en fonction de vos besoins de suivi pour l’annonce publicitaire individuelle. **Conseil :** pour modifier simultanément les pixels de suivi tiers pour plusieurs annonces d’un emplacement à l’aide de la vue [!UICONTROL Ad Tools], consultez la section « [Joindre des pixels de suivi tiers aux annonces dans un emplacement](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads) ».

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** Événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur le *[!UICONTROL Impression]* ou le *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image de 1x1 pixel), un *[!UICONTROL HTML]* ou un *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour l’[!UICONTROL Pixel Type] spécifié.

**[!UICONTROL Pixel Name]:** nom du pixel. Utilisez un nom qui vous permet d’identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [FAQ sur Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
