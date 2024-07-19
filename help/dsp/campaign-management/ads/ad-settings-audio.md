---
title: Paramètres de publicité audio
description: Reportez-vous à la description des paramètres de publicité disponibles pour les publicités audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Paramètres de publicité audio

## [!UICONTROL Insert Ad Tag]

*Nouvelles publicités uniquement*

**[!UICONTROL URL]** : URL de la balise VAST.

**[!UICONTROL Title]** : nom du fichier utilisé dans la vue [!UICONTROL Ads] et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la clé **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant `<VAST>` se trouve près de la partie supérieure.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe. Par défaut, il est défini sur *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’ Aperçu du produit de vacances : Audio 30sec).

**[!UICONTROL Ad Duration]:** longueur du fichier audio. Il est automatiquement défini comme [!UICONTROL 15] ou [!UICONTROL 30], selon l’unité publicitaire sélectionnée.

Ce champ peut être affiché ou non, selon les permissions du compte.

**[!UICONTROL VAST Tag]:** (Publicités utilisant des balises VAST uniquement) Une URL pour une source publicitaire tierce. Assurez-vous que la balise VAST comprend uniquement des fichiers de médias audio.

**[!UICONTROL Final VAST Tag]:** (Publicités utilisant uniquement des balises VAST) URL de la source publicitaire tierce avec les [macros de suivi Advertising DSP](/help/dsp/campaign-management/macros.md) nécessaires insérées, le cas échéant.

**[!UICONTROL Select Rate]:** (Utilisateurs avec autorisation uniquement) Taux négocié à l’avance et facturés par l’intermédiaire de l’Adobe, ou l’un des taux que vous avez négociés et facturés par l’intermédiaire du fournisseur. Pour ajouter un taux, contactez votre équipe de compte d’Adobe.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction des besoins de suivi pour l’annonce individuelle. **Conseil :** Pour modifier les pixels de suivi tiers pour plusieurs publicités à la fois dans un emplacement à l’aide de la vue [!UICONTROL Ad Tools], voir &quot;[Joindre des pixels de suivi tiers aux publicités dans un emplacement](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)&quot;.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image de pixel, au format approprié pour le type de pixel spécifié.

**[!UICONTROL Pixel Name]:** Nom du pixel. Utilisez un nom qui vous aide à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** Fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications de la publicité](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
