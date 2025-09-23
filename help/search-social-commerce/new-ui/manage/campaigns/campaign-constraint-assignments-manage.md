---
title: Gérer les affectations de contraintes pour les campagnes
description: Découvrez comment attribuer des contraintes aux campagnes.
feature: Search Optimization, Search Campaign Management
hide: true
exl-id: d886a228-24d7-4d8e-b68a-76e56b4304ed
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gérer les affectations de contraintes pour les campagnes

*Fonction Beta*

Vous pouvez affecter et supprimer des contraintes d’offres pour les entités de recherche suivantes : campagne, groupe publicitaire, mot-clé, emplacement, groupe de produits au niveau de l’unité et cible de recherche dynamique. Chaque entité ne peut avoir qu&#39;une seule contrainte.

Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire d’affecter des contraintes aux entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

L’annulation de l’affectation d’une contrainte supprime l’association avec les composants de compte et tous leurs composants enfants, et les données de rapport pour la contrainte ne sont plus disponibles pour ces composants. L’annulation de l’affectation d’une contrainte ne supprime pas la contrainte ni les composants de compte eux-mêmes.

>[!NOTE]
>
>* Si vous modifiez par la suite un mot-clé ou la copie d’une publicité, créant ainsi un nouveau mot-clé ou une nouvelle publicité, la contrainte n’est pas affectée à la nouvelle entité.
>* Les contraintes actives limitent les enchères uniquement pour les unités d’offre affectées dans les portefeuilles optimisés au niveau des mots-clés hérités. Elles sont ignorées pour les unités d&#39;enchères qui se trouvent dans des portefeuilles actifs, dans des portefeuilles hybrides ou qui ne se trouvent pas dans des portefeuilles.

## Affecter une contrainte aux campagnes sélectionnées à partir de la nouvelle vue [!UICONTROL Campaigns]

Vous pouvez affecter une seule contrainte à une ou plusieurs campagnes.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à laquelle vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

## Affecter une contrainte à des unités d&#39;enchères de recherche sélectionnées à partir des vues de [!UICONTROL Campaigns] héritées

1. Dans **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, sélectionnez la vue du composant Compte .

1. Cochez la case en regard de chaque ligne pertinente.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte applicable.

1. (Facultatif) Saisissez des détails supplémentaires :

   1. En regard de [!UICONTROL Additional Details], cliquez sur **[!UICONTROL Open]** pour développer les détails.

   1. Saisissez un **[!UICONTROL Project Name]** facultatif et/ou un **[!UICONTROL Description]** facultatif.

1. Cliquez sur **[!UICONTROL Save]**.

## Annuler l’affectation des contraintes des campagnes sélectionnées de la nouvelle vue [!UICONTROL Campaigns]

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Cochez la case en regard de chaque campagne à partir de laquelle vous annulerez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

## Annuler l’affectation des contraintes des unités d’enchères de recherche des vues de [!UICONTROL Campaigns] héritées

>[!NOTE]
>
>Pour supprimer une contrainte, ce qui la rend indisponible pour une utilisation ultérieure, consultez « Supprimer des contraintes pour les unités d’offres de recherche » dans le chapitre du guide d’optimisation sur « Contraintes d’offres », disponible dans Search, Social et Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. Dans **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, sélectionnez la vue du composant Compte .

1. Cochez la case en regard de chaque composant duquel vous souhaitez supprimer la contrainte.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Dans la boîte de dialogue de confirmation, sélectionnez **[!UICONTROL Yes, Unassign]**.

>[!MORELIKETHIS]
>
>* [Gérer les affectations de contraintes pour les groupes publicitaires](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
