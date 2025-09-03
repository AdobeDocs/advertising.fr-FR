---
title: Création d’une audience réutilisable
description: Découvrez comment créer des audiences réutilisables composées de segments d’audience et d’autres audiences enregistrées.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Création d’une audience réutilisable

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Vous pouvez enregistrer et gérer des audiences réutilisables, qui sont des groupes de segments d’audience et même d’autres audiences enregistrées, que vous pouvez utiliser comme cibles ou exclusions pour plusieurs emplacements.

>[!NOTE]
>
>(Annonceurs pour lesquels DSP convertit des ID d’e-mail hachés en segments LiveRampID) Les segments d’ID de rampe propriétaires qui ne sont pas joints à un emplacement actif, planifié ou en pause sont suspendus. Dans la liste des segments, le segment est marqué comme étant « En pause automatique ».

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

1. Saisissez un **[!UICONTROL Audience Name]** unique.

1. (Facultatif) Désélectionnez l’option à **[!UICONTROL Share with all advertisers in my account]**.

   Lorsque vous partagez une audience, celle-ci devient disponible en tant que cible ou exclusion pour tous les annonceurs du compte. Cependant, les segments individuels de l’audience ne sont disponibles que pour les utilisateurs et utilisatrices auxquels les segments sont partagés. Par exemple, si vous partagez une audience contenant des segments Adobe Analytics avec un annonceur qui n’est pas mappé au même compte [!DNL Analytics], le segment n’est pas prévisualisé dans cette audience pour cet annonceur. Seuls les segments disponibles pour cet annonceur sont prévisualisés dans l’audience.

1. Cliquez sur **[!UICONTROL Save]**.

1. Créez l’audience :

   >[!NOTE]
   >
   >À mesure que vous créez l’audience, les [données détaillées sur la taille de l’audience](audience-about.md) sont mises à jour dans le panneau de droite

   * Pour créer manuellement la logique du segment, à l’aide des segments disponibles dans les onglets [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] et [!UICONTROL Saved Audiences]](audience-settings.md) procédez comme suit.

      * Pour ajouter le premier segment, localisez le segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

      * Pour ajouter un segment à un groupe de segments existant :

         1. Cliquez sur le groupe de segments dans le panneau de droite.

         1. (Facultatif) Modifiez la logique de groupe en *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, selon les besoins.

            *[!UICONTROL Exclude All]* n’est pas disponible pour le premier groupe de segments. Pour une audience qui comprend uniquement des exclusions, créez-la sous la forme *[!UICONTROL Include Any]*, puis, au sein d’un emplacement, sélectionnez-la dans le menu Audiences exclues .

         1. Recherchez le nouveau segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

            Le groupe de segments est automatiquement mis à jour avec le nouveau segment.

      * Pour ajouter un nouveau groupe de segments :

         1. Cliquez sur **[!UICONTROL + New Group]** dans le panneau de droite.

         1. (Facultatif) Modifiez la logique entre le groupe précédent et le nouveau groupe en *[!UICONTROL And]* ou *[!UICONTROL Or]*, selon les besoins.

         1. Recherchez les segments du nouveau groupe dans le panneau de gauche, puis cochez les cases en regard des noms de segment.

         1. (Facultatif) Modifiez la logique de groupe en *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, selon les besoins.

   * Pour utiliser la logique de segment à partir d’une audience existante :

      1. Copiez la logique de segment de l’audience existante de l’une des manières suivantes :

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
>* [À propos de la gestion de l’audience](audience-about.md)
>* [Paramètres de l’audience](audience-settings.md)
>* [Syntaxe de la logique de segment d’audience](audience-segment-logic-syntax.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Créer et implémenter un segment personnalisé](custom-segment-create.md)
>* [Création et implémentation d’un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
