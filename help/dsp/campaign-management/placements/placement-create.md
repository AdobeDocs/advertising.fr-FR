---
title: Création d’un emplacement
description: Découvrez comment créer un emplacement.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# Création d’un emplacement

>[!TIP]
>
>Créez des emplacements en fonction des objectifs de campagne ou des besoins de création de rapports spécifiques.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne dans laquelle inclure l’emplacement.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**. Dans la section [!UICONTROL Placement Types] du menu, cliquez sur le type d&#39;emplacement.

   Le type d&#39;emplacement détermine le type d&#39;annonce publicitaire que l&#39;emplacement peut inclure.

1. Renseignez les [paramètres d&#39;emplacement](placement-settings.md) :

   1. Spécifiez les paramètres de [!UICONTROL Placement Basics].

   1. Dans la section [!UICONTROL Goals] , spécifiez le [!UICONTROL Gross Budget] et, éventuellement, des objectifs d’emplacement supplémentaires.

      Certains champs comportent des valeurs par défaut que vous pouvez remplacer.

      Si le package auquel l’emplacement est affecté applique une fréquence au niveau du package, vos objectifs et paramètres de fréquence reflètent les paramètres du package.

   1. (Facultatif) Dans la section [!UICONTROL Geo-Targeting], réduisez les emplacements inclus ou exclus.

      Si vous n’identifiez pas d’emplacements spécifiques, tous les emplacements sont ciblés.

      >[!NOTE]
      >
      >Les emplacements de ville et de DMA ne sont pas disponibles pour les emplacements Roku.

   1. Dans la section [!UICONTROL Inventory Targeting], réduisez les sources d’inventaire à inclure ou à exclure.

      Pour la plupart des types d&#39;emplacement, tous les types de stock et toutes les origines pour chaque type sont inclus par défaut. Pour les emplacements [!DNL Roku], vous devez spécifier le type de stock et les origines.

   1. (Facultatif) Dans la section [!UICONTROL Site Targeting], définissez les sites à cibler, puis spécifiez les sites à exclure.

   1. (Facultatif) Dans la section [!UICONTROL Audience Targeting] :

      1. Réduisez l’audience. Cela inclut la sélection des segments d’audience à cibler dans l’emplacement.

         Pour les emplacements [!DNL Roku], vous pouvez tirer parti de la correspondance d’audience unique de [DSP avec [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) en incluant un ou plusieurs segments d’audience qui peuvent être associés au jeu de données déterministe [!DNL Roku] (accepté).

         Les segments propriétaires RampID qui ne sont pas associés à un emplacement actif, planifié ou en pause sont suspendus. Dans la liste des segments, le segment est marqué comme étant « En pause automatique ».

      1. (Pour les campagnes avec ciblage sur plusieurs appareils au niveau des personnes ; facultatif) Lorsque l’emplacement cible une ou plusieurs audiences spécifiques, activez le ciblage sur plusieurs appareils basé sur les personnes pour l’emplacement.

         Le ciblage inter-appareils basé sur les personnes est fourni par [!DNL LiveRamp] à l’aide des données des États-Unis uniquement. Le service est disponible pour tous les annonceurs à 0,35 $ CPM pour les impressions diffusées à l’aide du graphique d’appareil [!DNL LiveRamp] (c’est-à-dire pour les appareils introuvables dans les segments d’audience ciblés).

   1. (Facultatif) Dans la section [!DNL Brand Safety and Media Targeting] , appliquez des restrictions de sécurité de marque à vos emplacements.

   1. (Facultatif) Dans la section [!DNL Tracking] , saisissez des pixels d’événement tiers ou des pixels de conversion pour les annonces de l’emplacement.

      >[!NOTE]
      >
      >(emplacements [!DNL Roku]) Les fournisseurs de pixels tiers approuvés par [!DNL Roku] comprennent [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], [!DNL Research Now],, et.

1. Cliquez sur **[!UICONTROL Create Placement]**.

1. (Facultatif) Joignez des annonces à l’emplacement :

   1. Cliquez sur **[!UICONTROL Attach an ad]**.

   1. Effectuez l’une des opérations suivantes :

      * Pour créer une annonce publicitaire :

         1. Cliquez sur **[!UICONTROL Create a New Ad].**

         1. Spécifiez les paramètres d’annonce publicitaire pour [annonces audio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [télévision connectée](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [affichages publicitaires](/help/dsp/campaign-management/ads/ad-settings-display.md), [annonces mobiles](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [annonces natives](/help/dsp/campaign-management/ads/ad-settings-native.md), [annonces pré-roll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) ou [annonces vidéo universelles](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >Les emplacements vidéo universels ne peuvent contenir que des publicités vidéo universelles.

         1. Cliquez sur **[!UICONTROL Save & Submit for Review]**.

         1. (Facultatif) Pour chaque publicité supplémentaire que vous souhaitez créer pour l’emplacement, cliquez sur **[!UICONTROL Attach Another Ad]**, puis répétez les étapes 1 à 3.

         1. Si vous ne souhaitez pas joindre d’annonces existantes, cliquez sur **[!UICONTROL I'm done for now]**.

      * Pour joindre des annonces existantes dans la campagne :

         1. Cliquez sur **[!UICONTROL Select an Ad]**.

         1. Effectuez l’une des opérations suivantes :

            * Pour ajouter une annonce à la fois :

               1. En regard du nom de l’annonce, cliquez sur **[!UICONTROL Select].**

               1. (Facultatif) Pour chaque annonce publicitaire supplémentaire à joindre, cliquez sur **[!UICONTROL Attach Another Ad]**, puis répétez le processus.

            * Pour ajouter jusqu’à 20 publicités à la fois :

               1. Cochez la case située au-dessus de la liste des publicités.

               1. Cochez la case en regard de chaque publicité à ajouter.

               1. Cliquez sur **[!UICONTROL Attach]**.

               1. En regard du nom de l’annonce publicitaire, cliquez sur **[!UICONTROL Select]**.

         1. (Facultatif) Pour remplacer la période de vol et la rotation d’annonces par défaut pour des annonces spécifiques dans l’emplacement :

            1. Cliquez sur **[!UICONTROL Custom Schedule Ads]**.

            1. Effectuez l’une des opérations suivantes :

               * Pour ajouter un vol, cliquez sur **[!UICONTROL Add Flight]**, puis spécifiez la date de début et la date de fin.

               * Pour ajouter un vol existant à une publicité, cliquez sur **[!UICONTROL +]** dans la ligne de publicité de la colonne de vol.

               * Pour supprimer un vol existant d’une publicité, cliquez sur **[!UICONTROL x]** dans la ligne de publicité de la colonne de vol.

               * (Lorsque plusieurs publicités présentent le même vol) Pour faire pivoter les publicités de manière inégale, cliquez sur **[!UICONTROL Even Rotation]** dans les informations de vol, puis entrez le poids relatif de rotation de chaque publicité, sous la forme d’un pourcentage.

                 Le poids total doit être égal à 100.

            1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Continue]**.

            1. Vérifiez les détails du vol, puis cliquez sur **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Modifier les emplacements](placement-edit.md)
>* [Gérer les multiplicateurs d&#39;offres pour les placements](placement-manage-bid-multipliers.md)
>* [Modifier les plannings de publicités pour les emplacements](placement-edit-ad-schedule.md)
>* [Désactiver ou activer un emplacement](placement-pause-activate.md)
>* [Afficher le journal des modifications pour un emplacement](placement-change-log.md)
>* [Paramètres d’emplacement](placement-settings.md)
>* [Afficher l&#39;état de prévision d&#39;emplacement](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [FAQ sur Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Raccourcis clavier](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Résolution des problèmes liés aux performances](/help/dsp/optimization/troubleshooting-performance.md)
>* [Vidéo : création d’un emplacement d’affichage standard](https://video.tv.adobe.com/v/340454)
