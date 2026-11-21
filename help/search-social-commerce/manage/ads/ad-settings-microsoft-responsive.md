---
title: '[!DNL Microsoft Advertising] paramètres des publicités réactives'
description: Référencez les paramètres de [!DNL Microsoft Advertising] annonces responsive.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%
---
# [!DNL Microsoft Advertising] paramètres d’annonce responsive (audience)

Le format d’annonce responsive est disponible pour les annonces d’audience vidéo basées sur des images, des vidéos et de la télévision connectée sur le [!DNL Microsoft Audience Network]. Le réseau publicitaire assemble dynamiquement des publicités réactives en utilisant les combinaisons les plus efficaces d&#39;éléments publicitaires.

## [!UICONTROL Basic Settings]

*Nouvelles annonces uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne.

**[!UICONTROL Ad Group]:** Le groupe publicitaire.

## [!UICONTROL Audience CTV Video Ad Details]

<!-- I can't find a video ad -- this same header is used for image ads. Need to verify the video ad settings and when you'll get them -->

### Publicités vidéo

**[!UICONTROL Videos]:** URL d’une publicité vidéo.

**[!UICONTROL Status]:** Statut de la publicité : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

### Annonces d’images)

>[!NOTE]
>
>Le réseau publicitaire crée automatiquement des annonces pour les campagnes d’audience liées à une boutique de centre commercial à l’aide des informations sur les produits de la boutique et du ciblage utilisateur au niveau du groupe publicitaire. Vous n’avez pas besoin de créer manuellement des annonces.

**[!UICONTROL Images]:** jusqu’à 15 images JPEG ou PNG pour la publicité. Incluez au moins une image avec un rapport d’aspect de 1,91:1. Affichez les proportions et dimensions autorisées pour [les images publicitaires de l’audience](https://help.ads.microsoft.com/#apex/ads/en/56912/0).

Pour les publicités d’audience, [!DNL Microsoft Advertising] recadre automatiquement cette image pour tous les proportions possibles.

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]:** Nom de l’entreprise, avec un maximum de 25 caractères. Il peut être utilisé dans des formats d’annonce publicitaire accessibles uniquement par appel.

**[!UICONTROL Short Headlines]:** Au moins trois titres courts, pouvant aller jusqu&#39;à 15, contenant au moins un mot et 30 caractères chacun.

**[!UICONTROL Long Headlines]:** Au moins trois grands titres de 90 caractères chacun, et jusqu&#39;à cinq.

**[!UICONTROL Ad Text]:** Au moins deux descriptions, et jusqu&#39;à quatre, comportant au moins un mot et un maximum de 90 caractères chacune.

**[!UICONTROL Status]:** Statut de la publicité : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gérer les publicités](/help/search-social-commerce/manage/ads/ad-manage.md)
