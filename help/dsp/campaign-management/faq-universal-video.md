---
title: Questions fréquentes sur Universal Video
description: En savoir plus sur les publicités vidéo universelles.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Questions fréquentes sur Universal Video

[Les publicités vidéo universelles](/help/dsp/campaign-management/ads/ad-about.md#ad-types) vous permettent de cibler l’inventaire vidéo à partir d’environnements de bureau, mobiles et de télévision connectée pour un inventaire VPAID et VAST à l’aide d’un seul emplacement vidéo.

## Comment créer des publicités et des emplacements vidéo universels ?

Les emplacements vidéo universels ne peuvent contenir que des annonces vidéo universelles et celles-ci ne peuvent être associées qu’à des emplacements vidéo universels.

Créez des emplacements vidéo et des annonces universels de la même manière que vous créez d’autres types d’emplacements et de vidéos :

1. Dans la campagne souhaitée, [créez un emplacement vidéo universel](/help/dsp/campaign-management/placements/placement-create.md), en sélectionnant le [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Vous devez spécifier au moins un environnement (bureau, mobile, télévision connectée) à cibler.

1. Dans la même campagne que l’emplacement vidéo universel, [créez une seule publicité vidéo universelle](/help/dsp/campaign-management/ads/ad-create.md) ou [créez plusieurs publicités vidéo universelles](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Si vous créez plusieurs publicités, veillez à spécifier « [!UICONTROL Universal Video] » comme [!UICONTROL Ad Type] :

   * Pour les publicités [!DNL Google] ou [!DNL Flashtalking] : à l’étape « [!UICONTROL Review ad types] » après avoir chargé le fichier, cliquez sur le champ **[!UICONTROL Ad Type]** et sélectionnez **[!UICONTROL Universal Video]**.

   * Pour les autres types de balises d’annonce publicitaire : dans le fichier de feuille de calcul que vous chargez, indiquez le champ Type d’annonce publicitaire pour chaque annonce publicitaire comme **[!UICONTROL Universal Video]**.

1. [Ouvrez les paramètres de l’annonce publicitaire](/help/dsp/campaign-management/ads/ad-edit.md) pour chaque nouvelle annonce publicitaire et sélectionnez le format vidéo applicable :

   * **[!UICONTROL VPAID]:** La visibilité est toujours mesurée.
   * **[!UICONTROL VPAID & VAST (Default)]:** inclut l’inventaire qui ne permet pas de mesurer la visibilité.
   * **[!UICONTROL VAST]** - Convient pour l&#39;inventaire de la télévision connectée.

   Pour plus d’informations, consultez « [Paramètres universels de publicité vidéo](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) ».

1. [Joignez les nouvelles publicités vidéo universelles](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) à l’emplacement vidéo universel.

## Pourquoi certains objectifs et packages d’optimisation ne sont-ils pas disponibles lorsque l’environnement TV connectée est sélectionné pour un emplacement vidéo universel ?

Les objectifs incompatibles avec les emplacements de télévision connectée standard, tels que Coût par clic le plus bas, ne sont pas pris en charge pour l’environnement de télévision connectée dans les emplacements vidéo universels. De même, les packages avec des objectifs d’optimisation incompatibles ne peuvent pas être sélectionnés.

## Quand le format vidéo **[!UICONTROL VAST]** doit-il être utilisé pour les publicités vidéo universelles ?

Utilisez **[!UICONTROL VAST]** dans l’un des scénarios suivants :

* L’emplacement cible l’inventaire des télévisions connectées.
* L’emplacement cible l’inventaire vidéo de Google Ad Manager, Appnexus, SpotX ou Freewheel. Ces SSP ne prennent pas en charge le format vidéo VPAID &amp; VAST.

## Est-il possible de joindre plusieurs publicités vidéo universelles au même emplacement vidéo universel ?

Oui.
