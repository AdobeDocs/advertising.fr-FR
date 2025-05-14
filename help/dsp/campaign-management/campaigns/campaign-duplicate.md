---
title: Dupliquer une campagne
description: Découvrez comment dupliquer une campagne.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Dupliquer une campagne

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Dupliquez une campagne pour créer une campagne avec des paramètres similaires. Vous pouvez :

* Dupliquez la campagne pour l’annonceur original ou pour un autre annonceur

* Vous pouvez éventuellement dupliquer les packages et les emplacements d’origine

* Modifier les dates de vol de la nouvelle campagne

Voir « [ Non dupliqué ](#campaign-not-duplicated) » pour obtenir une liste des paramètres d’emplacement qui ne sont pas dupliqués.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. En regard du nom de la campagne, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Définissez les nouveaux paramètres de la campagne :

   1. Saisissez le nouveau nom de la campagne et la date de fin du vol.

   1. (Facultatif) Modifiez les paramètres par défaut.

      Par défaut, la nouvelle campagne est attribuée à l’annonceur initial, dispose d’un planning des vols qui commence le jour en cours et inclut les packages et emplacements d’origine.

1. Cliquez sur **[!UICONTROL Submit]**.

## Éléments non dupliqués {#campaign-not-duplicated}

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

## Bonnes pratiques de configuration de la nouvelle campagne

>[!TIP]
>
>* Utilisez des feuilles d’envoi groupé pour [apporter des modifications à plusieurs composants de campagne à la fois](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Utilisez des feuilles de balises d’annonce publicitaire pour [charger plusieurs annonces publicitaires tierces](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Mettez la nouvelle campagne en pause jusqu’à ce que vous soyez prêt à l’activer.

* Tenez compte des points suivants et modifiez la nouvelle campagne selon vos besoins :

   * Le compte dispose-t-il d’un financement suffisant pour accueillir le nouveau budget de campagne ?

   * La nouvelle campagne a-t-elle besoin d&#39;un budget différent de celui de la campagne précédente ?

   * Des budgets minimaux sont-ils nécessaires pour chacun des placements ?

   * Chargez des contenus publicitaires, y compris la pondération et la planification personnalisées des annonces nécessaires, et joignez-les aux emplacements.

   * Ajoutez des pixels d’événement si nécessaire aux emplacements et aux annonces.

   * Incluez des cibles géographiques et des segments de [!DNL DoubleVerify Authentic Brand Safety] au niveau de l’emplacement selon les besoins des emplacements.

   * Pour les offres programmatiques garanties, utilisez les nouveaux ID d’offres et créez des emplacements par défaut.

   * Créez de nouveaux emplacements pour les offres [!UICONTROL Simple Ad Serving], si nécessaire.

* Pour les campagnes de performances (c’est-à-dire les campagnes avec des packages qui utilisent des objectifs d’optimisation personnalisés), utilisez le paramètre [[!UICONTROL Linked Package for Optimization Learnings Carryover]](/help/dsp/campaign-management/packages/package-settings.md) pour chaque package afin d’utiliser les données historiques de la campagne précédente comme entrée pour optimiser le package.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de campagnes](campaign-about.md)
>* [Créer une campagne](campaign-create.md)
>* [Modifier une campagne](campaign-edit.md)
>* [Afficher le journal des modifications d&#39;une campagne](campaign-change-log.md)
>* [Paramètres de la campagne](campaign-settings.md)
