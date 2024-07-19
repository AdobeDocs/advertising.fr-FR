---
title: Paramètres d’affichage des publicités
description: Consultez la description des paramètres d’annonce disponibles pour les annonces affichées.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---

# Paramètres d’affichage des publicités

Les paramètres suivants concernent les publicités standard.

## [!UICONTROL Ad Options]

### De base

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe. Par défaut, il est défini sur *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que &quot;Holiday Product Preview: 300x250 Gamer&quot;).

**\[Ad Source\]** : (lecture seule) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Publicités tierces uniquement) Indique que la publicité est une bannière publicitaire extensible. Les paramètres d’extension associés déterminent l’inventaire à acheter. Veillez donc à ce qu’ils reflètent le comportement de l’annonce.

**[!UICONTROL Expansion Method]:** (bannières extensibles tierces uniquement) Indique si la bannière se développe sur *[!UICONTROL Click]* ou *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (bannières publicitaires extensibles tierces uniquement) La direction dans laquelle la publicité se développe : *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* ou *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (bannières extensibles tierces uniquement) Fournisseur certifié pour lequel la publicité est disponible : *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* ou *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (annonces tierces uniquement) URL de la ressource créative tierce. Tous les paramètres [timestamp] et [[timestamp]] sont remplacés par des valeurs réelles.

**[!UICONTROL Final Display Code]:** (annonces tierces uniquement) URL de la ressource créative tierce, avec les [ macros de suivi Advertising DSP ](/help/dsp/campaign-management/macros.md) nécessaires insérées, le cas échéant.

**[!UICONTROL Ad Size]:** Largeur et hauteur de la publicité. Il doit s’agir d’une [taille d’affichage standard prise en charge](ad-specs.md). Vous pouvez saisir manuellement la taille de la publicité avant de la télécharger ou saisir un [!UICONTROL Display Code]. Si vous ne saisissez pas la taille de la publicité, les dimensions de la balise publicitaire ou de publicité chargée sont automatiquement saisies en lecture seule.

>[!IMPORTANT]
>
> La taille de l’annonce déclarée dans les champs largeur et hauteur correspond aux demandes d’offre entrantes. Vous pouvez rencontrer des problèmes de diffusion si les dimensions de l’annonce ne correspondent pas à la taille de l’annonce déclarée.

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
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Spécifications de la publicité](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
