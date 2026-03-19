---
title: Présentation de la gestion des campagnes dans Advertising DSP
description: Découvrez la hiérarchie et les composants de la gestion des campagnes.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: f58e478ea2c1397b15c667c1415a7038b6ea5e5b
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Présentation de la gestion des campagnes dans Advertising DSP

Les campagnes DSP présentent la hiérarchie suivante :

* Campagne
   * Package(s)
      * Emplacement(s)
         * Annonce(s) publicitaire(s)
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campagnes](/help/dsp/campaign-management/campaigns/campaign-about.md) constituent le cadre global des paramètres de vol. Chaque campagne est configurée avec un annonceur, des dates de début et de fin, un budget global, une option de ciblage inter-appareils et une limitation de fréquence par défaut, ainsi que des options de création de rapports pour la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience. Tous les paramètres au niveau de la campagne s’appliquent automatiquement à chaque package et emplacement de la campagne.

## [!UICONTROL Packages]

Chaque campagne peut contenir un ou plusieurs [packages](/help/dsp/campaign-management/packages/package-about.md), chacun d’eux comprenant un ensemble d’emplacements.

Utilisez des packages pour regrouper les emplacements de diffusion selon un budget, un objectif de performances et une stratégie de fréquence personnalisée définis. DSP optimise les packages en transférant les budgets vers les emplacements les plus performants du package. Vous pouvez organiser les packages par format d’emplacement, type d’inventaire, fournisseur de données, persona ou d’autres caractéristiques distinctes.

Les packages sont facultatifs, mais recommandés.

## [!UICONTROL Placements]

Un [emplacement](/help/dsp/campaign-management/placements/placement-about.md) stocke les paramètres de ciblage pour une ou plusieurs annonces du même type d’annonce. Vous pouvez créer un emplacement pour une campagne ou un package unique, puis lui affecter des annonces.

## [!UICONTROL Ads]

Les [publicités](/help/dsp/campaign-management/ads/ad-about.md) incluent des ressources créatives et des URL de suivi. Vous pouvez charger des annonces tierces diffusées individuellement ou en bloc à l’aide de feuilles de balises de partenaire ou du modèle de balise en bloc. Vous pouvez également créer manuellement des publicités display natives pour DSP.

Une fois vos publicités configurées, vous devez joindre chaque publicité à un emplacement pour commencer à exécuter la publicité. Vous pouvez joindre une seule publicité à un ou plusieurs emplacements.

Toutes les annonces actives et approuvées d’un emplacement actif dans une campagne active peuvent être exécutées en fonction des paramètres de ciblage d’emplacement.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des campagnes dans Advertising DSP](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Gestion des packages dans Advertising DSP](/help/dsp/campaign-management/packages/package-about.md)
>* [À propos de la gestion des emplacements dans Advertising DSP](/help/dsp/campaign-management/placements/placement-about.md)
>* [À propos de la gestion des publicités dans Advertising DSP](/help/dsp/campaign-management/ads/ad-about.md)
>* [Liste de contrôle de lancement de Campaign](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Bonnes pratiques pour configurer des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Types de rapports de performances dans les vues de gestion de campagnes](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Gérer les vues de données de votre campagne](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Vidéo : structure du compte DSP et interface utilisateur](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html?lang=fr)
