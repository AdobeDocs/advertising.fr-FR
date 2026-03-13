---
title: Création d’une audience réutilisable
description: Découvrez comment créer des audiences réutilisables composées de segments d’audience et d’autres audiences enregistrées.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e2d040409bcf18ca3c7906e8f3d5d3dc6633d2d7
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# Création d’une audience réutilisable

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Vous pouvez enregistrer et gérer des audiences réutilisables, qui sont des groupes de segments d’audience et même d’autres audiences enregistrées, que vous pouvez utiliser comme cibles ou exclusions pour plusieurs emplacements.

>[!NOTE]
>
>(Annonceurs pour lesquels DSP convertit des ID d’e-mail hachés en segments LiveRampID) Les segments d’ID de rampe propriétaires qui ne sont pas joints à un emplacement actif, planifié ou en pause sont suspendus. The segment is noted in the segment list as &quot;Auto paused.&quot;

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Above the data table, click **[!UICONTROL Create]**.

1. Enter a unique **[!UICONTROL Audience Name]**.

1. (Optional) Deselect the option to **[!UICONTROL Share with all advertisers in my account]**.

   When you share an audience, the audience becomes available as a target or exclusion to all advertisers within the account. Cependant, les segments individuels de l’audience ne sont disponibles que pour les utilisateurs et utilisatrices auxquels les segments sont partagés. For example, if you share an audience containing Adobe Analytics segments with an advertiser who isn&#39;t mapped to the same [!DNL Analytics] account, then the segment isn&#39;t previewed in that audience for that advertiser. Seuls les segments disponibles pour cet annonceur sont prévisualisés dans l’audience.

1. Cliquez sur **[!UICONTROL Save]**.

1. Créez l’audience :

   >[!NOTE]
   >
   >À mesure que vous créez l’audience, les [données détaillées sur la taille de l’audience](audience-about.md) sont mises à jour dans le panneau de droite

   * Pour créer manuellement la logique du segment, à l’aide des segments disponibles dans les onglets [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] et [!UICONTROL Saved Audiences]](audience-settings.md) procédez comme suit.

      * (Optional) Search for a segment name, description, or path.

        Search results include segments based on the exact terms you use. When you enter multiple terms, all of the terms must be found for a segment.

      * To add the first segment, locate the segment in the left panel, and select the check box next to the segment name.

      * To add a segment to an existing segment group:

         1. Click the segment group in the right panel.

         1. (Optional) Change the group logic to *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, or *[!UICONTROL Exclude All]*, as needed.

            *[!UICONTROL Exclude All]* n’est pas disponible pour le premier groupe de segments. Pour une audience qui comprend uniquement des exclusions, créez-la sous la forme *[!UICONTROL Include Any]*, puis, au sein d’un emplacement, sélectionnez-la dans le menu Audiences exclues .

         1. Recherchez le nouveau segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

            Le groupe de segments est automatiquement mis à jour avec le nouveau segment.

      * Pour ajouter un nouveau groupe de segments :

         1. Click **[!UICONTROL + New Group]** in the right panel.

         1. (Optional) Change the logic between the previous group and the new group to *[!UICONTROL And]* or *[!UICONTROL Or]*, as needed.

         1. Locate the segments for the new group in the left panel, and select the check boxes next to the segment names.

         1. (Optional) Change the group logic to *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, or *[!UICONTROL Exclude All]*, as needed.

   * To use segment logic from an existing audience:

      1. Copy the segment logic from the existing audience in any of the following ways:

         * Dans la vue Toutes les audiences, placez le curseur sur la ligne d’audience, puis cliquez sur **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Dans les paramètres de l’audience existante, en haut du panneau logique des segments, cliquez sur **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Dans un éditeur de texte, créez manuellement la logique du segment à l’aide des identifiants de segment alphanumériques et de la [syntaxe booléenne](audience-segment-logic-syntax.md), puis copiez-la dans le presse-papiers.

      1. Cliquez sur **[!UICONTROL paste in an audience rule to begin building]**, collez la logique de segment existante dans le champ de saisie, puis cliquez sur **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Si l’audience inclut déjà une logique de segment, coller une nouvelle logique de segment remplace la logique existante.

1. Cliquez sur **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [About Audience Management](audience-about.md)
>* [Audience Settings](audience-settings.md)
>* [Syntax for Audience Segment Logic](audience-segment-logic-syntax.md)
>* [Available Third-party Data Providers](third-party-data-providers.md)
>* [Create and Implement a Custom Segment](custom-segment-create.md)
>* [Création et implémentation d’un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
