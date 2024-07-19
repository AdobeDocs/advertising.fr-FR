---
title: Définition des emplacements et publicités pour une transaction privée
description: Découvrez comment utiliser une offre privée avec des emplacements et publicités supplémentaires.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 09119471-429d-413e-8033-e29e1558abb0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Définition des emplacements et publicités pour une transaction privée

Pour les offres non garanties, vous pouvez spécifier l’opération en tant que cible d’inventaire pour les nouveaux emplacements à partir de la vue [!UICONTROL Placements].

Pour les offres PG garanties par la programmation, vous pouvez créer des emplacements avec des publicités spécifiées à partir de la vue [!UICONTROL Deals].

Vous pouvez également [joindre des publicités à des emplacements](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associés à des offres PG et non garanties à tout moment.

## Définition d’une transaction non garantie comme cible d’inventaire pour un emplacement

* [Créez un emplacement à partir de la vue [!UICONTROL Placements]](/help/dsp/campaign-management/placements/placement-create.md). Dans les paramètres [!UICONTROL Inventory Targeting], sélectionnez l’opération privée.

## Joindre des emplacements et des publicités à un contrat PG

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Dans la ligne de la transaction, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Attach New Placement]**.

1. Dans les paramètres [!UICONTROL Ad & Campaign Selection], sélectionnez les publicités à utiliser pour l’emplacement :

       1. Sélectionnez l’annonceur, la campagne et le type d’annonce. Vous pouvez éventuellement sélectionner l’état d’une publicité pour filtrer les publicités.
       
       1. Dans la liste des publicités disponibles, cochez la case en regard de chaque publicité à utiliser pour l’opération.
       
       1. Cliquez sur **[!UICONTROL Apply]**.
   
   1. Dans l’écran des paramètres d’emplacement :

      1. Saisissez le nom de l’emplacement.

      1. (Facultatif) Modifiez les [paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md), y compris le remplacement de l’offre par défaut, qui est automatiquement renseignée avec la valeur CPM de l’opération, la modification de la période ou l’ajout d’annonces en pièce jointe.

      L’opération est automatiquement ciblée dans la section Cibles de l’inventaire . Toutes les autres options de ciblage ne sont pas applicables.

      1. Cliquez sur **[!UICONTROL Create placement]**.

L’emplacement commence à s’exécuter une fois que l’éditeur a activé votre ID d’opération PG.

>[!NOTE]
>
> Vous n’avez pas besoin d’envoyer la balise de transaction à l’éditeur pour vérification.

>[!MORELIKETHIS]
>
>* [À propos de l’inventaire privé](private-inventory-about.md)
>* [Liste des emplacements et des publicités pour une transaction privée](/help/dsp/inventory/private-deal-view-placements.md)
>* [Créer manuellement des détails sur l’identifiant de transaction](deal-id-create.md)
>* [Paramètres d’ID de transaction manuelle](deal-id-settings.md)
>* [Configuration d’une transaction sécurisée par programmation](programmatic-guaranteed-set-up.md)
