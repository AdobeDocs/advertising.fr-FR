---
title: Afficher les paramètres d’annonce publicitaire
description: Consultez les descriptions des paramètres d’annonce publicitaire disponibles pour l’affichage des annonces.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
TQID: https://experienceleague.adobe.com/bcuGR2fzcwjvPcWisdQZBbU8vcaZhgW2qZPAXjV5ndM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 0%

---

# Afficher les paramètres d’annonce publicitaire

Les paramètres ci-dessous concernent les publicités display standard.

## [!UICONTROL Ad Options]

### De base

**[!UICONTROL Ad Type]:** (Lecture seule) Type d’annonce publicitaire que vous créez, qui correspond au type d’emplacement auquel l’annonce publicitaire peut être associée. La valeur par défaut est *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Nom de l’annonce publicitaire. Le titre de la ressource est utilisé par défaut, mais vous pouvez en modifier le nom.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que Aperçu du produit de vacances : 300x250 Gamer »).

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

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités dans Advertising DSP](ad-about.md)
>* [Créer une seule annonce publicitaire](ad-create.md)
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros ](/help/dsp/campaign-management/macros.md)
