---
title: Affectation de valeurs de classification à des composants de compte à partir des vues de gestion de campagne
description: Découvrez comment affecter des valeurs de classification aux composants de compte.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Affectation de valeurs de classification à des composants de compte à partir des vues de gestion de campagne

Vous pouvez attribuer et supprimer des valeurs de classification pour les entités de recherche suivantes dans les vues de gestion de campagne : campagne, groupe publicitaire, mot-clé, publicité, emplacement, groupe de produits au niveau de l’unité et cible de recherche dynamique. Si nécessaire, vous pouvez créer des classifications et des valeurs de classification au cours du processus d’affectation. Chaque classification d’étiquettes peut comporter jusqu’à 2 000 valeurs.

Chaque entité peut avoir une valeur d’étiquette par classification. Par exemple, Shoes_Campaign peut avoir une valeur Color de &quot;red&quot; et une valeur Geo de &quot;Los Angeles&quot;, mais il ne peut pas avoir plusieurs valeurs pour Color ou Geo.

Les valeurs d’étiquette sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

>[!NOTE]
>
>Les mots-clés et la copie de publicité pour certains réseaux publicitaires et types de campagne sont les suivants : [non modifiable](/help/search-social-commerce/campaign-management/faqs-campaigns.md), ce qui signifie que les modifier supprime l’entité existante et en crée une nouvelle. Lorsqu’une entité existante est ainsi supprimée, la classification de libellés n’est pas affectée à la nouvelle entité.

1. Cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**, puis sélectionnez la vue du composant de compte.

1. Effectuez l’une des opérations suivantes :

   * (Pour attribuer des valeurs à une seule entité) Placez le curseur sur le nom de l’entité, cliquez sur ![Bouton Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Bouton Menu"), puis sélectionnez **[!UICONTROL Classification]**.

   * (Pour attribuer des valeurs à une ou plusieurs entités) Procédez comme suit :

      * Cochez la case en regard de chaque ligne correspondante.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus"), puis cliquez sur **[!UICONTROL Classification]**.

1. Dans le [!UICONTROL Assignment Details], effectuez l’une des opérations suivantes :

   * Pour remplacer des valeurs de classification existantes par de nouvelles valeurs, sélectionnez **[!UICONTROL Set To]**.

      La longueur maximale de chaque valeur est de 100 caractères. Elle peut contenir des caractères ASCII et non ASCII.

   * Pour attribuer des valeurs de classification spécifiées sans supprimer des valeurs existantes, sélectionnez **[!UICONTROL Assign]**.

   * Pour supprimer des valeurs de classification spécifiques actuellement attribuées, sélectionnez **[!UICONTROL Remove]**.

      Lorsque vous supprimez une valeur de classification, les données de rapport correspondant à la valeur ne sont plus disponibles pour les composants de compte spécifiés.

   * Pour supprimer des valeurs de classification spécifiées, sélectionnez **[!UICONTROL Delete]**.

      La suppression d’une valeur de classification la rend indisponible pour une utilisation ultérieure et les données de rapport ne sont plus disponibles pour la valeur. Toutes les affectations entre les valeurs et des composants de compte spécifiques sont supprimées, mais les composants de compte ne sont pas supprimés.

1. Pour chaque valeur de classification applicable, procédez comme suit :

   1. Dans le **[!UICONTROL Classification]** , indiquez le nom de la classification :

      * Pour utiliser une classification existante, cliquez sur son nom pour la développer.

      * Pour créer une classification, cliquez sur [!UICONTROL +]. Dans le champ de saisie, saisissez le nom de la classification, puis cliquez sur ![Enregistrer](/help/search-social-commerce/assets/select.png "Enregistrer") pour enregistrer immédiatement la classification.

         Le nom doit être composé de [Caractères ASCII 32 à 126](https://www.asciitable.com/), et la longueur maximale est de 27 caractères sur un octet.
   1. Dans le **[!UICONTROL Value Name]** , indiquez le nom de la valeur :

      * Pour utiliser une valeur existante, cliquez sur le nom de la valeur pour la sélectionner.

      * Pour créer une valeur, cliquez sur [!UICONTROL +]. Dans le champ de saisie, saisissez la valeur, puis cliquez sur ![Enregistrer](/help/search-social-commerce/assets/select.png "Enregistrer") pour enregistrer immédiatement la valeur.

         La longueur maximale est de 100 caractères. Elle peut contenir des caractères ASCII et non ASCII.


1. (Facultatif) Saisissez des détails supplémentaires :

   1. En regard de **[!UICONTROL Additional Details]**, cliquez sur ![Ouvrir](/help/search-social-commerce/assets/chevron-up.png "Ouvrir") pour développer les détails.

   1. Saisissez un **[!UICONTROL Project Name]** et/ou facultatif **[!UICONTROL Description]**.

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [À propos des classifications d’étiquettes](classification-about.md)
>* [Création d’une classification d’étiquettes](classification-create.md)
>* [Affectation de valeurs de classification à des composants de compte à l’aide de feuilles d’envoi groupées](classification-values-assign-bulksheets.md)
>* [Suppression des valeurs de classification d’étiquette des composants de compte](classification-values-remove.md)
>* [Supprimer des valeurs de classification d’étiquettes](classification-values-delete.md)
>* [Supprimer des classifications d’étiquettes](classification-delete.md)

