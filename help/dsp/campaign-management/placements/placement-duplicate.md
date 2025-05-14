---
title: Dupliquer les emplacements
description: Découvrez comment dupliquer un ou plusieurs emplacements.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Dupliquer les emplacements

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Dupliquez un ou plusieurs emplacements pour créer des emplacements avec des paramètres similaires. Vous pouvez :

* Créer plusieurs doublons d&#39;emplacements
* Dupliquez des emplacements dans les annonceurs et les campagnes d’origine ou dans différents emplacements
* (Pour les emplacements dupliqués dans les campagnes d’origine) Dupliquez éventuellement les annonces d’origine
* Modifier le statut et les dates de vol des nouveaux emplacements

Voir « [ Non dupliqué ](#placement-not-duplicated) » pour obtenir une liste des paramètres d’emplacement qui ne sont pas dupliqués.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Effectuez l’une des opérations suivantes :

   * Pour dupliquer un emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** en regard du nom du package.

   * Pour dupliquer plusieurs emplacements :

      1. Cochez la case en regard de chaque emplacement à dupliquer.

      1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Duplicate]**.

1. Spécifiez les nouveaux paramètres d&#39;emplacement :

   1. (Emplacements uniques) Saisissez le nouveau nom de l’emplacement.

   1. Dans le menu **[!UICONTROL Choose Package (Required)]**, sélectionnez le package parent ou **[!UICONTROL No package]*.

   1. (Facultatif) Modifiez les paramètres par défaut.

   Les paramètres s’appliquent à tous les emplacements sélectionnés.

   Par défaut, les nouveaux emplacements sont pour le type d’annonce d’origine, sont affectés aux annonceurs et aux campagnes d’origine, ont des plannings de vol qui commencent le jour en cours, sont suspendus et n’incluent pas les annonces d’origine.

   Lorsque vous créez plusieurs emplacements, les nouveaux noms d’emplacement sont ajoutés avec un numéro, dans l’ordre, en utilisant la convention &lt;*original_placement_name #N*>, telle que « Mes #2 d’emplacement ».

1. Cliquez sur **[!UICONTROL Submit]**.

## Éléments non dupliqués {#placement-not-duplicated}

Tous les paramètres des emplacements d’origine sont dupliqués, sauf :

* Paramètres de l’expérience
* (Si vous modifiez les dates de vol) Planification personnalisée des annonces
* (Si vous ne joignez pas d’annonces) Pondération et planification personnalisées des annonces
* Emplacements par défaut pour les offres programmatiques garanties (PG) et emplacements pour les offres [!UICONTROL Simple Ad Serving]
* (Si vous copiez des emplacements dans une autre campagne) :
   * Cibles géographiques
   * Pixels d’événement
   * Publicités
   * Segments [!DNL DoubleVerify Authentic Brand Safety] au niveau de l’emplacement (qui remplacent les segments au niveau de l’annonceur)

## Bonnes pratiques relatives à la configuration des nouveaux emplacements

>[!TIP]
>
>* Utilisez des feuilles d’envoi groupé pour [apporter des modifications à plusieurs composants de campagne à la fois](/help/dsp/campaign-management/campaign-components-review-edit.md).
* Utilisez des feuilles de balises d’annonce publicitaire pour [charger plusieurs annonces publicitaires tierces](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Mettez les nouveaux emplacements en pause jusqu’à ce que vous soyez prêt à les activer.

* Tenez compte des points suivants et modifiez les nouveaux paramètres d’emplacement selon vos besoins :

   * Le compte dispose-t-il de fonds suffisants pour accueillir les nouveaux budgets de placement ?

   * Les nouveaux emplacements ont-ils besoin de budgets différents des emplacements précédents ?

   * Chargez des contenus publicitaires, y compris la pondération et la planification personnalisées des annonces nécessaires, et joignez-les aux emplacements.

   * Ajoutez des pixels d’événement si nécessaire aux emplacements et aux annonces.

   * Incluez des cibles géographiques et des segments de [!DNL DoubleVerify Authentic Brand Safety] au niveau de l’emplacement selon les besoins des emplacements.

   * Pour les offres programmatiques garanties, utilisez les nouveaux ID d’offres et créez des emplacements par défaut.

   * Créez de nouveaux emplacements pour les offres [!UICONTROL Simple Ad Serving], si nécessaire.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Créer un emplacement](placement-create.md)
>* [Modifier les emplacements](placement-edit.md)
>* [Afficher le journal des modifications pour un emplacement](placement-change-log.md)
>* [Paramètres d’emplacement](placement-settings.md)
