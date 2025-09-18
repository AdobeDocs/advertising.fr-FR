---
title: Paramètres de publicité audio
description: Consultez les descriptions des paramètres d’annonce publicitaire disponibles pour les annonces publicitaires audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Paramètres de publicité audio

## [!UICONTROL Insert Ad Tag]

*Nouvelles annonces uniquement*

**[!UICONTROL URL]** : l’URL de balise VAST.

**[!UICONTROL Title]** : nom du fichier, qui est utilisé dans la vue [!UICONTROL Ads] et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la touche **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant des `<VAST>` s’affiche en haut de l’écran.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Lecture seule) Type d’annonce publicitaire que vous créez, qui correspond au type d’emplacement auquel l’annonce publicitaire peut être associée. La valeur par défaut est *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Nom de l’annonce publicitaire. Le titre de la ressource est utilisé par défaut, mais vous pouvez en modifier le nom.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que Aperçu du produit Holiday : 30sec Audio »).

**[!UICONTROL Ad Duration]:** longueur du fichier audio. Il est automatiquement défini sur [!UICONTROL 15] ou [!UICONTROL 30], selon l’unité publicitaire sélectionnée.

Ce champ peut s’afficher ou non, selon les autorisations du compte.

**[!UICONTROL VAST Tag]:** (publicités à l’aide de balises VAST uniquement) URL d’une source publicitaire tierce. Assurez-vous que la balise VAST comprend uniquement des fichiers multimédias audio.

**[!UICONTROL Final VAST Tag]:** (publicités à l’aide de balises VAST uniquement) URL de la source publicitaire tierce avec les [macros de suivi Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

**[!UICONTROL Select Rate]:** (Utilisateurs avec autorisation uniquement) Taux prénégocié facturé via Adobe, ou l’un des taux que vous avez négociés et facturé via le fournisseur. Pour ajouter un taux, contactez l’équipe chargée de votre compte Adobe.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser les pixels existants et créer de nouveaux pixels si nécessaire, en fonction de vos besoins de suivi pour l’annonce publicitaire individuelle. **Conseil :** pour modifier simultanément les pixels de suivi tiers pour plusieurs annonces d’un emplacement à l’aide de la vue [!UICONTROL Ad Tools], consultez la section « [Joindre des pixels de suivi tiers aux annonces dans un emplacement](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads) ».

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** Événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur le *[!UICONTROL Impression]* ou le *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image de 1x1 pixel), un *[!UICONTROL HTML]* ou un *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour le type de pixel spécifié.

**[!UICONTROL Pixel Name]:** nom du pixel. Utilisez un nom qui vous permet d’identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** fournisseur de pixels :*[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
