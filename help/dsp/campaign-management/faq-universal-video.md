---
title: Questions fréquentes sur la vidéo universelle
description: En savoir plus sur les publicités vidéo universelles.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
TQID: https://experienceleague.adobe.com/LAzSivup-EVuDgtWN1T58lfRjzgrchIiFF9-lMJAVlw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 348
ht-degree: 0%

---

# Questions fréquentes sur la vidéo universelle

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

   Pour plus d’informations, reportez-vous à « [ Paramètres universels de publicité vidéo ](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) ».

1. [Joignez les nouvelles publicités vidéo universelles](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) à l’emplacement vidéo universel.

## Pourquoi certains objectifs et packages d’optimisation ne sont-ils pas disponibles lorsque l’environnement de télévision connectée est sélectionné pour un emplacement vidéo universel ?

Les objectifs incompatibles avec les emplacements de télévision connectée standard, tels que Coût par clic le plus bas, ne sont pas pris en charge pour l’environnement de télévision connectée dans les emplacements vidéo universels. De même, les packages avec des objectifs d’optimisation incompatibles ne peuvent pas être sélectionnés.

## Quand le format vidéo **[!UICONTROL VAST]** doit-il être utilisé pour les publicités vidéo universelles ?

Utilisez **[!UICONTROL VAST]** dans l’un des scénarios suivants :

* L’emplacement cible l’inventaire des télévisions connectées.
* L’emplacement cible l’inventaire vidéo de Google Ad Manager, Appnexus, SpotX ou FreeWheel. Ces SSP ne prennent pas en charge le format vidéo VPAID &amp; VAST.

## Est-il possible de joindre plusieurs publicités vidéo universelles au même emplacement vidéo universel ?

Oui.
