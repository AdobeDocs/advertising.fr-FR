---
title: Dupliquer un package
description: Découvrez comment dupliquer un package.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Dupliquer un package

Dupliquez un package pour créer un package avec des paramètres similaires. Vous pouvez :

* Dupliquez le package dans l’annonceur et la campagne d’origine ou dans différents packages

* Vous pouvez éventuellement dupliquer les emplacements dans le package

* (Pour les packages dupliqués dans les campagnes d’origine) Dupliquez éventuellement les annonces d’origine et les pixels d’événement au niveau de l’emplacement

* Modifier les dates de vol du nouveau forfait

Voir « [&#x200B; Non dupliqué &#x200B;](#package-not-duplicated) » pour obtenir une liste des paramètres d’emplacement qui ne sont pas dupliqués.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne pour ouvrir la vue [!UICONTROL Packages].

1. En regard du nom du package, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Spécifiez les nouveaux paramètres du package :

   1. Saisissez le nouveau nom du package.

   1. (Facultatif) Modifiez les paramètres par défaut.

      Par défaut :

      * Le nouveau package est affecté à l’annonceur et à la campagne d’origine.

      * Le nouveau package devient actif le jour en cours.<!-- and the flight continues for NN  days. -->

      * Les emplacements dans le package d’origine sont copiés dans le nouveau package.

      * Les annonces publicitaires et les pixels d’événement au niveau de l’emplacement ne sont pas copiés dans le nouveau package.

1. Cliquez sur **[!UICONTROL Submit]**.

## Éléments non dupliqués {#package-not-duplicated}

Tous les paramètres des emplacements d’origine sont dupliqués, sauf :

* Paramètres de l’expérience
* Budgets minimaux au niveau des emplacements
* (Si vous modifiez les dates de vol) Planification personnalisée des annonces
* (Si vous ne joignez pas d’annonces) Pondération et planification personnalisées des annonces
* Emplacements par défaut pour les offres programmatiques garanties (PG) et emplacements pour les offres [!UICONTROL Simple Ad Serving]
* (Si vous copiez des emplacements dans une autre campagne) :
   * Cibles géographiques
   * Pixels d’événement
   * Publicités
   * Segments [!DNL DoubleVerify Authentic Brand Safety] au niveau de l’emplacement (qui remplacent les segments au niveau de l’annonceur)

## Bonnes pratiques relatives à la configuration du nouveau package

>[!TIP]
>
>* Utilisez des feuilles d’envoi groupé pour [apporter des modifications à plusieurs composants de campagne à la fois](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Utilisez des feuilles de balises d’annonce publicitaire pour [charger plusieurs annonces publicitaires tierces](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Mettez le nouveau package en pause jusqu’à ce que vous soyez prêt à l’activer.

* Tenez compte des points suivants et modifiez le nouveau package si nécessaire :

   * Le compte dispose-t-il d&#39;un financement suffisant pour accueillir le nouveau budget du paquet ?

   * Le nouveau paquet a-t-il besoin d&#39;un budget différent du précédent ?

   * Des budgets minimaux sont-ils nécessaires pour chacun des placements ?

   * Chargez des contenus publicitaires, y compris la pondération et la planification personnalisées des annonces nécessaires, et joignez-les aux emplacements.

   * Ajoutez des pixels d’événement si nécessaire aux emplacements et aux annonces.

   * Incluez des cibles géographiques et des segments de [!DNL DoubleVerify Authentic Brand Safety] au niveau de l’emplacement selon les besoins des emplacements.

   * Pour les offres programmatiques garanties, utilisez les nouveaux ID d’offres et créez des emplacements par défaut.

   * Créez de nouveaux emplacements pour les offres [!UICONTROL Simple Ad Serving], si nécessaire.

* Pour les packages qui utilisent des objectifs d’optimisation personnalisés, utilisez le paramètre [[!UICONTROL Linked Package for Optimization Learnings Carryover] &#x200B;](/help/dsp/campaign-management/packages/package-settings.md) pour chaque package afin d’utiliser les données historiques de la campagne précédente comme entrée pour optimiser le package.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des packages](package-about.md)
>* [Créer un package](package-create.md)
>* [Modifier un package](package-edit.md)
>* [Afficher le journal des modifications d&#39;un package](package-change-log.md)
>* [Paramètres du package](package-settings.md)
