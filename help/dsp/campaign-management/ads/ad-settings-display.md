---
title: Afficher les paramètres de publicité
description: Consultez les descriptions des paramètres d’annonce publicitaire disponibles pour l’affichage des annonces.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Afficher les paramètres de publicité

Les paramètres ci-dessous concernent les publicités display standard.

## [!UICONTROL Ad Options]

### De base

**[!UICONTROL Ad Type]:** (Lecture seule) Type d’annonce publicitaire que vous créez, qui correspond au type d’emplacement auquel l’annonce publicitaire peut être associée. La valeur par défaut est *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Nom de l’annonce publicitaire. Le titre de la ressource est utilisé par défaut, mais vous pouvez en modifier le nom.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d&#39;unité et certains attributs clés (tels que Holiday Product Preview: 300x250 Gamer »).

**\[Ad Source\]** : *[!UICONTROL 3rd party]* (lecture seule).

**[!UICONTROL This is an expandable Banner]:** (annonces tierces uniquement) Indique qu’il s’agit d’une bannière publicitaire extensible. Les paramètres d’extension associés déterminent l’inventaire à acheter. Veillez donc à ce qu’ils reflètent le comportement de l’annonce publicitaire.

**[!UICONTROL Expansion Method]:** (bannières publicitaires tierces extensibles uniquement) Si la bannière se développe sous *[!UICONTROL Click]* ou *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (bannières publicitaires tierces extensibles uniquement) Direction dans laquelle la publicité se développe : *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* ou *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (bannières publicitaires tierces extensibles uniquement) Fournisseur certifié pour lequel la publicité est disponible : *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* ou *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (publicités tierces uniquement) URL de la ressource de création tierce. Les paramètres [timestamp] et [[timestamp]] sont remplacés par des valeurs réelles.

**[!UICONTROL Final Display Code]:** (publicités tierces uniquement) URL de la ressource créative tierce, avec les [macros de suivi Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

**[!UICONTROL Ad Size]:** largeur et hauteur de la publicité. Il doit s’agir d’une [taille d’annonce publicitaire standard prise en charge](ad-specs.md). Vous pouvez saisir manuellement la taille de l’annonce avant de la charger ou saisir une [!UICONTROL Display Code]. Si vous n’indiquez pas la taille de la publicité, les dimensions de la publicité ou de la balise de publicité chargée sont automatiquement saisies en lecture seule.

>[!IMPORTANT]
>
> La taille de l’annonce publicitaire déclarée dans les champs de largeur et de hauteur est mise en correspondance avec les demandes d’enchères entrantes. Vous pouvez rencontrer des problèmes de diffusion si les dimensions de l’annonce ne correspondent pas à la taille de l’annonce publicitaire déclarée.

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
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
