---
title: Questions fréquentes à propos des vidéos universelles
description: En savoir plus sur les publicités vidéo universelles.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Questions fréquentes à propos des vidéos universelles

Les [ publicités vidéo universelles ](/help/dsp/campaign-management/ads/ad-about.md#ad-types) vous permettent de cibler l’inventaire vidéo des environnements de bureau, mobiles et de télévision connectés pour les inventaires VPAID et VAST à l’aide d’un emplacement vidéo unique.

## Comment créer des publicités et des emplacements de vidéos universels ?

Les emplacements vidéo universels ne peuvent contenir que des publicités vidéo universelles, et les publicités vidéo universelles ne peuvent être associées qu’à des emplacements vidéo universels.

Créez des emplacements et des publicités vidéo universels de la même manière que vous créez d’autres types d’emplacements et de vidéos :

1. Dans la campagne de votre choix, [créez un emplacement vidéo universel](/help/dsp/campaign-management/placements/placement-create.md), en sélectionnant [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Vous devez spécifier au moins un environnement (bureau, mobile, télévision connectée) à cibler.

1. Dans la même campagne que l’emplacement vidéo universel, [créez une seule publicité vidéo universelle](/help/dsp/campaign-management/ads/ad-create.md) ou [créez plusieurs publicités vidéo universelles](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Si vous créez plusieurs publicités, veillez à spécifier &quot;[!UICONTROL Universal Video]&quot; comme [!UICONTROL Ad Type] :

   * Pour [!DNL Google] ou [!DNL Flashtalking] annonces : à l’étape &quot;[!UICONTROL Review ad types]&quot; après avoir téléchargé le fichier, cliquez sur le champ **[!UICONTROL Ad Type]** et sélectionnez **[!UICONTROL Universal Video]**.

   * Pour les autres types de balises publicitaires : dans le fichier de feuille de calcul que vous chargez, spécifiez le champ Type de publicité pour chaque publicité comme **[!UICONTROL Universal Video]**.

1. [Ouvrez les paramètres de publicité ](/help/dsp/campaign-management/ads/ad-edit.md) pour chaque nouvelle publicité et sélectionnez le format vidéo approprié :

   * **[!UICONTROL VPAID]:** La visibilité est toujours mesurée.
   * **[!UICONTROL VPAID & VAST (Default)]:** comprend un inventaire qui n’autorise pas la mesure de la visibilité.
   * **[!UICONTROL VAST]** - Adapté à l’inventaire de la télévision connectée.

   Pour plus d’informations, voir &quot;[Paramètres de publicité vidéo universelle](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot;.

1. [Joignez les nouvelles publicités vidéo universelles](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) au placement vidéo universel.

## Pourquoi certains objectifs et packages d’optimisation ne sont-ils pas disponibles lorsque l’environnement de télévision connecté est sélectionné pour un emplacement vidéo universel ?

Les objectifs incompatibles avec des emplacements de télévision connectés standard, tels que Coût le plus bas par clic, ne sont pas pris en charge pour l’environnement de télévision connecté dans les emplacements vidéo universels. De même, les modules dont les objectifs d’optimisation sont incompatibles ne sont pas non plus disponibles pour la sélection.

## Quand le format vidéo **[!UICONTROL VAST]** doit-il être utilisé pour les publicités vidéo universelles ?

Utilisez **[!UICONTROL VAST]** dans l’un des scénarios suivants :

* L’emplacement cible l’inventaire de la télévision connectée.
* L’emplacement cible l’inventaire vidéo à partir de Google Ad Manager, Appnexus, SpotX ou de la roue libre. Ces SSP ne prennent pas en charge le format vidéo VPAID &amp; VAST.

## Est-il possible de joindre plusieurs publicités vidéo universelles au même emplacement vidéo universel ?

Oui.
