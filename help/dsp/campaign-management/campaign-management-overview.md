---
title: Présentation de Campaign Management dans Advertising DSP
description: Découvrez la hiérarchie et les composants de la gestion de campagne.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Présentation de Campaign Management dans Advertising DSP

DSP campagnes présentent la hiérarchie suivante :

* Campagne
   * Package(s)
      * Emplacement(s)
         * Publicités
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campagnes](/help/dsp/campaign-management/campaigns/campaign-about.md) sont le cadre général des paramètres de vol. Chaque campagne est configurée avec un annonceur, des dates de début et de fin, un budget global, une option de ciblage multi-appareils et un plafond de fréquence par défaut, ainsi que des options de reporting pour la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience. Tous les paramètres au niveau de l&#39;opération s&#39;appliquent automatiquement à chaque package et emplacement de l&#39;opération.

## [!UICONTROL Packages]

Chaque campagne peut contenir un ou plusieurs [packages](/help/dsp/campaign-management/packages/package-about.md), dont chacun comprend un ensemble d’emplacements.

Utilisez les packages pour regrouper des emplacements à diffuser selon un budget défini, un objectif de performance et une stratégie de fréquence personnalisée. DSP optimise les packages en transférant les budgets vers les emplacements les plus performants du package. Vous pouvez organiser les packages par format d’emplacement, type de stock, fournisseur de données, persona ou toute autre caractéristique reconnaissable.

Les packages sont facultatifs, mais recommandés.

## [!UICONTROL Placements]

Un [emplacement](/help/dsp/campaign-management/placements/placement-about.md) stocke les paramètres de ciblage pour une ou plusieurs publicités du même type de publicité. Vous pouvez créer un emplacement pour une campagne ou un package unique, puis lui affecter des publicités.

## [!UICONTROL Ads]

[Les publicités](/help/dsp/campaign-management/ads/ad-about.md) incluent des ressources créatives et des URL de suivi. Vous pouvez charger des balises de diffusion de publicités tierces individuellement ou en bloc à l’aide de feuilles de balises partenaires ou du modèle de balise en bloc. Vous pouvez également créer manuellement des publicités d’affichage natives pour DSP à diffuser.

Une fois vos publicités configurées, vous devez joindre chaque publicité à un emplacement pour commencer à exécuter la publicité. Vous pouvez joindre une seule publicité à un ou plusieurs emplacements.

Toutes les publicités actives et approuvées d’un emplacement actif dans une campagne active peuvent être exécutées en fonction des paramètres de ciblage de l’emplacement.

>[!MORELIKETHIS]
>
>* [À propos de Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [À propos de la gestion de modules](/help/dsp/campaign-management/packages/package-about.md)
>* [À propos de la gestion des emplacements](/help/dsp/campaign-management/placements/placement-about.md)
>* [À propos de la gestion des publicités](/help/dsp/campaign-management/ads/ad-about.md)
>* [Liste de contrôle de lancement de campagne](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [ Bonnes pratiques pour configurer des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Types de rapports de performances dans les vues Campaign Management](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Gérer vos vues de données de campagne](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Vidéo : DSP structure de compte et interface utilisateur](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html?lang=fr)
