---
title: Paramètres d’affichage des publicités
description: Consultez la description des paramètres d’annonce disponibles pour les annonces affichées.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 2f137b17deea4cd02ae19494a306ff37c7002423
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Paramètres d’affichage des publicités

Les paramètres suivants concernent les publicités standard.

## [!UICONTROL Ad Options]

### De base

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type d’emplacement auquel la publicité peut être jointe. Par défaut, la valeur *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la variable [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que &quot;Holiday Product Preview: 300x250 Gamer&quot;).

**\[Source de publicité\]**: (lecture seule) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Publicités tierces uniquement) Indique que la publicité est une bannière extensible. Les paramètres d’extension associés déterminent l’inventaire à acheter. Veillez donc à ce qu’ils reflètent le comportement de l’annonce.

**[!UICONTROL Expansion Method]:** (Publicités de bannière extensible tierces uniquement) Indique si la bannière s’étend sur *[!UICONTROL Click]* ou *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Bannières publicitaires extensibles tierces uniquement) La direction dans laquelle la publicité se développe : *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*, ou *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Bannières publicitaires extensibles tierces uniquement) Fournisseur certifié pour lequel la publicité est disponible : *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*, ou *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Publicités tierces uniquement) URL de la ressource créative tierce. Quelconque [timestamp] et [[timestamp]] seront remplacés par des valeurs réelles.

**[!UICONTROL Final Display Code]:** (Publicités tierces uniquement) URL de la ressource créative tierce, avec les [Macros de suivi des DSP publicitaires](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

**[!UICONTROL Ad Size]:** Largeur et hauteur de la publicité. Ce doit être une [taille d’affichage standard prise en charge](ad-specs.md). Vous pouvez saisir manuellement la taille de la publicité avant de la télécharger ou saisir une [!UICONTROL Display Code]. Si vous ne saisissez pas la taille de la publicité, les dimensions de la balise publicitaire ou de publicité chargée sont automatiquement saisies en lecture seule. Notez que la publicité affichée ne sera pas enregistrée si les dimensions ne se trouvent pas dans l’affichage standard sous forme de tailles, par exemple 301x250 au lieu de 300x250.

>[!IMPORTANT]
>
> La taille de l’annonce déclarée dans les champs largeur et hauteur sera mise en correspondance avec les demandes d’offre entrantes. Vous pouvez rencontrer des problèmes de diffusion si les dimensions de l’annonce ne correspondent pas à la taille de l’annonce déclarée.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction des besoins de suivi pour l’annonce individuelle. **Conseil :** Pour modifier les pixels de suivi tiers de plusieurs publicités à la fois dans un emplacement à l’aide de la variable [!UICONTROL Ad Tools] vue, voir[Joindre des pixels de suivi tiers à des publicités dans un emplacement](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** Événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur la variable *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Si le pixel est un *[!UICONTROL IMG URL]* (fichier image 1x1 pixel), *[!UICONTROL HTML]*, ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L’URL de l’image en pixels, au format approprié pour l’objet [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Nom du pixel. Utilisez un nom qui vous aide à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** Fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Création d’une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Spécifications des publicités](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
