---
title: Paramètres universels des publicités vidéo
description: Consultez les descriptions des paramètres d’annonces publicitaires disponibles pour les annonces vidéo universelles.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
TQID: https://experienceleague.adobe.com/el77W69kVO-3vFRPR5pT62NCm35IHlABo-sUvEcVnRI
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 384
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
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que « Aperçu du produit Holiday : vidéo universelle de 30 secondes »).

**[!UICONTROL Show Controls]:** Où inclure des commandes vidéo pour la publicité : *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** Conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou étirer la vidéo pour remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (publicités à l’aide de balises VAST uniquement ; lecture seule) Balise VAST tierce que vous avez saisie en tant que source de publicité.

**[!UICONTROL Final VAST Tag]:** (publicités à l’aide de balises VAST uniquement ; lecture seule) Balise VAST tierce entrée en tant que source de publicité avec les [macros de suivi Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

**[!UICONTROL Wmode]:** mode fenêtre : *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*. Si ce paramètre n’est pas applicable, laissez-le vide.

**[!UICONTROL Video Format]:** format du lecteur d’annonces pour l’inventaire potentiel : *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* ou *[!UICONTROL VAST]*. La visibilité est toujours mesurée pour les [!UICONTROL VPAID], mais [!UICONTROL VPAID & VAST] inclut l’inventaire qui ne permet pas de mesurer la visibilité. Tenez compte de cette distinction si les mesures de visibilité sont importantes pour votre campagne.

Utilisez le format [!UICONTROL VAST], qui ne permet pas de mesurer la visibilité, lorsque vous ciblez une télévision connectée ou un inventaire qui nécessite uniquement un format VAST (généralement à partir de sources d’approvisionnement telles que Google Ad Manager, Appnexus, SpotX et FreeWheel). Utilisez également cette option pour les stocks qui étaient auparavant compatibles avec les placements/annonces pré-roll standard (VAST) ou Phone + Tablet Standard (VAST).

**[!UICONTROL Clock Number]** : (utilisé uniquement au Royaume-Uni ; disponible uniquement pour les utilisateurs autorisés) Identifiant unique utilisé pour s’assurer que la bonne publicité est diffusée. Si ce paramètre n’est pas applicable, laissez-le vide.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [FAQ sur la vidéo universelle](/help/dsp/campaign-management/faq-universal-video.md)
>* [À propos de la gestion des publicités dans Advertising DSP](ad-about.md)
>* [Créer une seule annonce publicitaire](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros ](/help/dsp/campaign-management/macros.md)
