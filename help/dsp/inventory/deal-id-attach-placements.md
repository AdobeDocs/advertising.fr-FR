---
title: Spécifier des emplacements et des annonces pour une offre privée
description: Découvrez comment utiliser une offre privée avec des emplacements et des annonces supplémentaires.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Spécifier des emplacements et des annonces pour une offre privée

Pour les opérations non garanties, vous pouvez spécifier l’opération en tant que cible de stock pour les nouveaux emplacements à partir de la vue [!UICONTROL Placements].

Pour les offres programmatiques garanties (PG), vous pouvez créer des emplacements avec des annonces spécifiées à partir de la vue [!UICONTROL Deals].

Vous pouvez également [joindre des annonces à des emplacements](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associées à des offres PG et non garanties à tout moment.

## Spécifier une offre non garantie comme cible de stock pour un emplacement

* [Créer un emplacement à partir de la vue [!UICONTROL Placements]](/help/dsp/campaign-management/placements/placement-create.md). Dans les paramètres [!UICONTROL Inventory Targeting], sélectionnez l’offre privée.

## Joindre des emplacements et des annonces à une offre PG

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Dans la ligne d&#39;opération, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. Dans les paramètres [!UICONTROL Ad & Campaign Selection], sélectionnez les annonces à utiliser pour l’emplacement :

       1. Sélectionnez l’annonceur, la campagne et le type d’annonce. Vous pouvez éventuellement sélectionner un statut d’annonce publicitaire selon lequel filtrer les annonces.
       
       1. Dans la liste des publicités disponibles, cochez la case en regard de chaque publicité à utiliser pour l’offre.
       
       1. Cliquez sur **[!UICONTROL Apply]**.
   
   1. Dans l’écran des paramètres d’emplacement :

      1. Saisissez le nom de l’emplacement.

      1. (Facultatif) Modifiez les [paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md), y compris en remplaçant l’enchère par défaut, qui est automatiquement renseignée avec la valeur CPM de l’opération ; en modifiant la période ; ou en joignant d’autres annonces.

      L’opération est automatiquement ciblée dans la section Cibles d’inventaire . Toutes les autres options de ciblage ne sont pas applicables.

      1. Cliquez sur **[!UICONTROL Create placement]**.

L’emplacement commence à s’exécuter une fois que l’éditeur a activé votre ID d’offre PG.

>[!NOTE]
>
> Vous n’avez pas besoin d’envoyer la balise d’offre à l’éditeur pour vérification.

>[!MORELIKETHIS]
>
>* [À propos de l&#39;inventaire privé](private-inventory-about.md)
>* [Liste des emplacements et des publicités pour une offre privée](/help/dsp/inventory/private-deal-view-placements.md)
>* [Créer manuellement les détails de l’ID d’offre](deal-id-create.md)
>* [Paramètres manuels d’ID d’offre](deal-id-settings.md)
>* [Configurer une offre programmatique garantie](programmatic-guaranteed-set-up.md)
