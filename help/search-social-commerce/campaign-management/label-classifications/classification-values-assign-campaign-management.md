---
title: Attribuer des valeurs de classification aux composants de compte à partir des vues de gestion de campagne
description: Découvrez comment attribuer des valeurs de classification aux composants de compte.
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Attribuer des valeurs de classification aux composants de compte à partir des vues de gestion de campagne

Vous pouvez affecter et supprimer des valeurs de classification pour les entités de recherche suivantes des vues de gestion de campagne : campagne, groupe publicitaire, mot-clé, publicité, emplacement, groupe de produits au niveau de l&#39;unité et cible de recherche dynamique. Si nécessaire, vous pouvez créer des classifications et des valeurs de classification au cours du processus d’affectation. Chaque classification de libellé peut contenir jusqu’à 2 000 valeurs.

Chaque entité peut avoir une valeur de libellé par classification. Par exemple, Shoes_Campaign peut avoir une valeur Color de « red » et une valeur Geo de « Los Angeles », mais pas plusieurs valeurs pour Color ou Geo.

Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

>[!NOTE]
>
>Vos mots-clés et votre texte publicitaire pour certains réseaux publicitaires et types de campagne sont [non modifiables](/help/search-social-commerce/campaign-management/faqs-campaigns.md), ce qui signifie que leur modification supprime l’entité existante et en crée une nouvelle. Lorsqu&#39;une entité existante est supprimée de cette manière, la classification des libellés n&#39;est pas affectée à la nouvelle entité.

1. Cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, puis sélectionnez la vue du composant de compte.

1. Effectuez l’une des opérations suivantes :

   * (Pour attribuer des valeurs à une seule entité) Placez le curseur sur le nom de l’entité, cliquez sur ![Bouton de menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Bouton de menu"), puis sélectionnez **[!UICONTROL Classification]**.

   * (Pour attribuer des valeurs à une ou plusieurs entités) Procédez comme suit :

      * Cochez la case en regard de chaque ligne pertinente.

        Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

      * Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus"), puis sur **[!UICONTROL Classification]**.

1. Dans le [!UICONTROL Assignment Details], effectuez l’une des opérations suivantes :

   * Pour remplacer des valeurs de classification existantes par de nouvelles valeurs, sélectionnez **[!UICONTROL Set To]**.

     La longueur maximale de chaque valeur est de 100 caractères et peut inclure des caractères ASCII et non ASCII.

   * Pour attribuer des valeurs de classification spécifiées sans supprimer les valeurs existantes, sélectionnez **[!UICONTROL Assign]**.

   * Pour supprimer des valeurs de classification spécifiques actuellement attribuées, sélectionnez **[!UICONTROL Remove]**.

     Lorsque vous supprimez une valeur de classification, les données de rapport correspondant à cette valeur ne sont plus disponibles pour les composants de compte spécifiés.

   * Pour supprimer des valeurs de classification spécifiées, sélectionnez **[!UICONTROL Delete]**.

     La suppression d’une valeur de classification la rend indisponible pour une utilisation ultérieure et les données de rapport ne sont plus disponibles pour cette valeur. Toutes les affectations entre les valeurs et les composants de compte spécifiques sont supprimées, mais les composants de compte ne sont pas supprimés.

1. Pour chaque valeur de classification applicable, procédez comme suit :

   1. Dans la colonne **[!UICONTROL Classification]** , indiquez le nom de la classification :

      * Pour utiliser une classification existante, cliquez sur son nom pour la développer.

      * Pour créer une classification, cliquez sur [!UICONTROL +]. Dans le champ de saisie, saisissez le nom de la classification, puis cliquez sur ![Enregistrer](/help/search-social-commerce/assets/select.png "Enregistrer") pour enregistrer immédiatement la classification.

        Le nom doit comporter [caractères ASCII compris entre 32 et 126](https://www.asciitable.com/) et la longueur maximale est de 27 caractères codés sur un seul octet.

   1. Dans la colonne **[!UICONTROL Value Name]** , indiquez le nom de la valeur :

      * Pour utiliser une valeur existante, cliquez sur le nom de la valeur pour la sélectionner.

      * Pour créer une valeur, cliquez sur [!UICONTROL +]. Dans le champ de saisie, saisissez la valeur, puis cliquez sur ![Enregistrer](/help/search-social-commerce/assets/select.png "Enregistrer") pour enregistrer immédiatement la valeur.

        La longueur maximale est de 100 caractères et peut inclure des caractères ASCII et non-ASCII.

1. (Facultatif) Saisissez des détails supplémentaires :

   1. À côté de **[!UICONTROL Additional Details]**, cliquez sur ![Ouvrir](/help/search-social-commerce/assets/chevron-up.png "Ouvrir") pour développer les détails.

   1. Saisissez un **[!UICONTROL Project Name]** facultatif et/ou un **[!UICONTROL Description]** facultatif.

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [À propos des classifications de libellés](classification-about.md)
>* [Créer une classification de libellé](classification-create.md)
>* [Attribuez des valeurs de classification aux composants de compte à l’aide de feuilles d’envoi groupé](classification-values-assign-bulksheets.md)
>* [Supprimer les valeurs de classification de libellé des composants de compte](classification-values-remove.md)
>* [Supprimer les valeurs de classification de libellé](classification-values-delete.md)
>* [Supprimer les classifications de libellés](classification-delete.md)
