---
title: Modification d’une audience réutilisable
description: Découvrez comment modifier une audience réutilisable.
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Modification d’une audience réutilisable

Lorsque vous modifiez une audience utilisée à des emplacements ou dans d’autres audiences réutilisables, les modifications sont immédiatement appliquées à ces emplacements et audiences.<!-- verify -->

>[!NOTE]
>
>(Annonceurs pour lesquels DSP convertit des ID d’e-mail hachés en segments LiveRampID) Les segments d’ID de rampe propriétaires qui ne sont pas joints à un emplacement actif, planifié ou en pause sont suspendus. Dans la liste des segments, le segment est marqué comme étant « En pause automatique ».

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**.

1. Placez le curseur sur la ligne d’audience et cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les paramètres d’audience de l’une des manières suivantes :

   >[!NOTE]
   >
   >Si vous modifiez la logique du segment d’audience, les [données détaillées sur la taille de l’audience](audience-about.md) sont mises à jour dans le panneau de droite.

   * (Facultatif) Pour modifier le **[!UICONTROL Audience Name]**, cliquez sur ![Modifier](/help/dsp/assets/edit.png) en regard du nom de l’audience, saisissez un nom d’audience unique, puis cliquez sur **[!UICONTROL Apply]**.

   * (Facultatif) Pour modifier manuellement la logique du segment à l’aide des segments disponibles dans les onglets [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] et [!UICONTROL Saved Audiences]](audience-settings.md) procédez comme suit.

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

1. Cliquez sur **[!UICONTROL Save]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de l’audience](audience-about.md)
>* [Créer une audience réutilisable](reusable-audience-create.md)
>* [Dupliquer une audience réutilisable](reusable-audience-duplicate.md)
>* [Afficher les détails sur une audience réutilisable](reusable-audience-view-details.md)
>* [Partage d’une audience réutilisable](reusable-audience-share.md)
>* [Exporter une audience réutilisable](reusable-audience-export.md)
>* [Copiez la clé de segment pour une audience réutilisable dans le presse-papiers](reusable-audience-clipboard.md)
>* [Supprimer une audience réutilisable](reusable-audience-delete.md)
>* [Paramètres de l’audience](audience-settings.md)
>* [Syntaxe de la logique de segment d’audience](audience-segment-logic-syntax.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
