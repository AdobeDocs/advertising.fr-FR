---
title: Paramètres natifs des publicités display
description: Consultez les descriptions des paramètres d’annonce publicitaire disponibles pour les annonces publicitaires natives.
feature: DSP Ads
exl-id: 64ce1946-072d-4ca9-b3a8-348987580403
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Paramètres natifs des publicités display

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Lecture seule) Type d’annonce publicitaire que vous créez, qui correspond au type d’emplacement auquel l’annonce publicitaire peut être associée.

**[!UICONTROL Ad Name]:** Nom de l’annonce publicitaire. Le type d’annonce est utilisé par défaut, mais vous pouvez en modifier le nom.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que Aperçu du produit Holiday : 15sec natif).

**[!UICONTROL Native Creative]:** Image de 1 200 x 627 pour optimiser la diffusion sur l’inventaire mobile. Cliquez sur **[!UICONTROL Browse]** et localisez le fichier sur votre appareil ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** Un titre accrocheur pour séduire les spectateurs.

**[!UICONTROL Description]:** Le corps de la publicité. La longueur maximale est de 100 caractères.

**[!UICONTROL Landing Page]:** URL à laquelle la visionneuse accède lorsqu’elle clique sur l’annonce publicitaire.

**[!UICONTROL Final Landing Page]:** URL [!UICONTROL Landing Page] avec les [macros de tracking Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

**[!UICONTROL Sponsored By (Advertiser Name)]:** annonceur de la publicité.

**[!UICONTROL Call to Action]:** (facultatif) Étape que les visiteurs doivent effectuer une fois qu’ils ont vu cette publicité.

**[!UICONTROL Advertiser Logo]:** (facultatif) Logo à 1 :1 à inclure dans la publicité pour une meilleure reconnaissance de la marque. Cliquez sur **[!UICONTROL Browse]** et localisez le fichier sur votre appareil ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser les pixels existants et créer de nouveaux pixels si nécessaire, en fonction de vos besoins de suivi pour l’annonce publicitaire individuelle. **Conseil :** pour modifier simultanément les pixels de suivi tiers pour plusieurs annonces d’un emplacement à l’aide de la vue [!UICONTROL Ad Tools], consultez la section « [Joindre des pixels de suivi tiers aux annonces dans un emplacement](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads) ».

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** Événement qui déclenche le déclenchement du pixel.

**[!UICONTROL Pixel Type]:** indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image de 1x1 pixel), un *[!UICONTROL HTML]* ou un *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour l’[!UICONTROL Pixel Type] spécifié.

**[!UICONTROL Pixel Name]:** nom du pixel. Utilisez un nom qui vous permet d’identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* ou *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
