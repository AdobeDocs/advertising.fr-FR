---
title: Affichage du rapport de [!UICONTROL Diagnostics] des emplacements
description: Découvrez comment diagnostiquer les problèmes liés à la configuration et à la fréquence des emplacements.
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: a5be425ee34960cf58642cb850ae817998652f53
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Affichage du rapport de [!UICONTROL Diagnostics] des emplacements

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Les rapports de diagnostic peuvent vous aider à diagnostiquer les problèmes de configuration et de fréquence des emplacements une fois qu’une campagne est active.

## Informations dans le rapport de [!UICONTROL Diagnostics] d’emplacement

* **[!UICONTROL Change Log]:** affiche les modifications apportées aux paramètres d’emplacement clés, tels que le nom, le statut et l’enchère maximale. Chaque entrée inclut la date et le nom d’utilisateur de la personne qui a effectué la modification.

* **[!UICONTROL Ad Approvals]:** indique si les annonces ont été approuvées ou rejetées par les fournisseurs d&#39;inventaire. Vous pouvez éventuellement modifier le statut d’une publicité (par exemple, mettre en pause une publicité rejetée) ou ouvrir les paramètres de la publicité.

* **[!UICONTROL Non Bids]:** indique pourquoi DSP n’a pas enchéri sur l’emplacement.

## Ouvrir le rapport de [!UICONTROL Diagnostics] d’emplacement

1. Ouvrez le rapport [!UICONTROL Diagnostics] :

   1. Ouvrez les paramètres d&#39;emplacement :

      1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

      1. Cliquez sur le nom de la campagne, puis sur **[!UICONTROL Placements]**.

      1. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   1. Dans le coin supérieur droit, cliquez sur ![Diagnostics d’emplacement](/help/dsp/assets/placement-diagnostics.png).

1. Effectuez l’une des opérations suivantes :

   * Pour afficher le journal des modifications :

      1. Cliquez sur **[!UICONTROL Change Log]**.

      1. (Facultatif) Filtrez les résultats du rapport :

         * Dans le menu de date, remplacez la période de rapport des 14 derniers jours par défaut par une autre période (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* ou *[!UICONTROL Last 1 year]*).

         * Dans le menu de gauche, filtrez le rapport par nom d’utilisateur spécifique.

         * Dans le menu de droite, filtrez le rapport selon un paramètre d’emplacement spécifique.

   * Pour afficher le statut des validations d’annonces :

      1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Ad Approvals]**.

      1. (Facultatif) Pour mettre la publicité en pause ou l’activer, cliquez sur le bouton de changement de statut (![Basculement de statut](/help/dsp/assets/status-switch.png)) dans la colonne Publicité .)

      1. (Facultatif) Pour ouvrir les paramètres d’une publicité, cliquez sur **[!UICONTROL View Ad]** en regard de la publicité.

   * Pour savoir pourquoi DSP n’a pas enchéri sur l’emplacement :

      1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Non Bids]**.

      1. (Facultatif) Pour filtrer l’emplacement selon une cible d’opération privée spécifique, sélectionnez l’opération. <!-- Admin users only: Optionally filter the deal by one or more regions ([!UICONTROL US-EAST], [!UICONTROL US-WEST]) [!UICONTROL EU-WEST], [!UICONTROL HKG]) by selecting the regions. -->

      1. (Facultatif) Pour modifier la période, cliquez dans le champ de date et sélectionnez une autre date ou période.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues de gestion de campagnes](campaign-reports-about.md)
>* [Afficher l&#39;état de prévision d&#39;emplacement](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
