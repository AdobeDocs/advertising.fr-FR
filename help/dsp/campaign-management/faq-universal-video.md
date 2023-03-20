---
title: Questions fréquentes à propos des vidéos universelles
description: En savoir plus sur les publicités vidéo universelles.
feature: DSP Placements, DSP Ads
source-git-commit: 8e0237355e834f4ae2b9ef1ed211e047b41cafe7
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# # FAQ sur la vidéo universelle

## Comment créer des publicités et des emplacements de vidéos universels ?

Les emplacements vidéo universels ne peuvent contenir que des publicités vidéo universelles et les publicités vidéo universelles peuvent être associées uniquement à des emplacements vidéo universels.

Créez-les de la même manière que vous créez d’autres types d’emplacements et de vidéos :

1. Dans la campagne souhaitée, [créer un emplacement vidéo universel ;](/help/dsp/campaign-management/placements/placement-create.md), en sélectionnant le [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   Vous devez spécifier au moins un environnement (bureau, mobile, télévision connectée) à cibler.

1. Dans la même campagne que le placement vidéo universel, [créer une publicité vidéo universelle unique ;](/help/dsp/campaign-management/ads/ad-create.md) ou [créer plusieurs publicités vidéo universelles ;](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Si vous créez plusieurs publicités, veillez à spécifier &quot;[!UICONTROL Universal Video]&quot; comme [!UICONTROL Ad Type]. Pour [!DNL Google] ou [!DNL Flashtalking] une fois le fichier téléchargé, cliquez sur le champ Type de publicité dans le champ &quot;[!UICONTROL Review ad types]&quot; et modifiez-la. Pour les autres types de balises d’annonce, indiquez le type d’annonce dans le fichier de feuille de calcul que vous chargez.

1. [Ouvrir les paramètres de publicité](/help/dsp/campaign-management/ads/ad-edit.md) pour chaque nouvelle publicité et sélectionnez le format vidéo approprié :

   * **[!UICONTROL VPAID]:** La visibilité est toujours mesurée.
   * **[!UICONTROL VPAID & VAST (Default)]:** Inclut un inventaire qui n’autorise pas la mesure de la visibilité.
   * **[!UICONTROL VAST]** - Adapté à l’inventaire des télévisions connectées.

   Voir &quot;[Paramètres de publicité vidéo universelle](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; pour plus d’informations.

1. [Ajout de nouvelles publicités vidéo universelles](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) au placement vidéo universel.

## Pourquoi certains objectifs et packages d’optimisation ne sont-ils pas disponibles lorsque l’environnement de télévision connecté est sélectionné pour un emplacement vidéo universel ?

Les objectifs incompatibles avec des emplacements de télévision connectés standard, tels que Coût le plus bas par clic, ne sont pas pris en charge pour l’environnement de télévision connecté dans les emplacements vidéo universels. De même, les modules dont les objectifs d’optimisation sont incompatibles ne sont pas non plus disponibles pour la sélection.

## Lorsque la variable **[!UICONTROL VAST]** format vidéo doit être utilisé pour les publicités vidéo universelles ?

Utilisation **[!UICONTROL VAST]** dans l’un des scénarios suivants :

* L’emplacement cible l’inventaire de la télévision connectée.
* L’emplacement cible l’inventaire des vidéos provenant de Google Ad Manager, d’Appnexus, de SpotX ou de la roue libre. Ces SSP ne prennent pas en charge le format vidéo VPAID &amp; VAST.

## Est-il possible de joindre plusieurs publicités vidéo universelles au même emplacement vidéo universel ?

Oui.
