---
title: Modification des propriétés de transaction disponibles dans les vues de gestion et les rapports
description: Découvrez comment rendre les propriétés de transaction disponibles dans vos rapports et vues de gestion.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Modification des propriétés de transaction disponibles dans les vues de gestion et les rapports

Lorsque Adobe Advertising effectue le suivi d’une [propriété de transaction](/help/search-social-commerce/glossary.md#s-t) pour un annonceur, elle est initialement exclue des objectifs du portfolio, des rapports et des vues de gestion. Pour rendre une propriété visible, vous devez la rendre explicitement disponible, puis éventuellement modifier le nom d’affichage par défaut, qui est le nom affiché. La seule exception concerne le suivi des conversions par [!DNL Google Ads], [!DNL Google Analytics], et [!DNL Microsoft® Advertising] les balises de suivi d’événement universel sont automatiquement disponibles et visibles.

De même, vous pouvez masquer une propriété des objectifs du portfolio, des rapports et des vues de gestion. Lorsque vous masquez une propriété qui était auparavant visible, elle est supprimée des mesures dérivées qui contiennent la propriété.

Dans la liste des propriétés disponibles, chaque utilisateur ayant accès aux données de l’annonceur peut personnaliser les propriétés qu’il voit pour les vues de gestion et les rapports, y compris ou en omettant les propriétés spécifiques de son choix.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   Toutes les propriétés de transaction qui ont été collectées pour l’annonceur et tous les noms différents qui ont été spécifiés pour l’affichage sont répertoriés.

1. (Facultatif) Filtrez la liste :

   * Pour rechercher un nom de propriété ou un nom d’affichage spécifique, cliquez sur ![Rechercher](/help/search-social-commerce/assets/search.png "Rechercher"), saisissez le mot ou la chaîne dans le champ de saisie, puis appuyez sur la touche **[!DNL Enter]** clé.

      Vous pouvez rechercher des chaînes qui apparaissent n’importe où dans l’expression (comme la première lettre ou les trois dernières lettres), et les termes recherchés ne sont pas [sensible à la casse](/help/search-social-commerce/glossary.md#c-d).

   * Pour rechercher des propriétés en fonction de leur disponibilité dans les vues de gestion et les rapports, cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter.png "Filtrer"), puis sélectionnez le filtre **[!UICONTROL Show in UI and Reports]**. Sélectionnez ensuite l’une des options suivantes : **[!UICONTROL Show]** (pour afficher les propriétés disponibles à inclure dans les vues de gestion et de rapports) ou **[!UICONTROL Hide]** (pour afficher les propriétés non disponibles dans les rapports et les vues de gestion).

1. Modifiez les propriétés disponibles pour les vues de gestion et les rapports :

   * Pour afficher ou masquer une seule propriété, cliquez sur le commutateur dans la **[!UICONTROL Show in UI and Reports]** pour modifier le paramètre.

   * Pour afficher ou masquer plusieurs propriétés, procédez comme suit :

      1. Cochez la case en regard de chaque propriété.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Afficher](/help/search-social-commerce/assets/show.png "Afficher") pour afficher les propriétés ou ![Masquer](/help/search-social-commerce/assets/hide.png "Masquer") pour masquer les propriétés.

      1. (Pour masquer les propriétés) Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]** pour masquer les propriétés, notamment les supprimer des mesures dérivées qui contiennent les propriétés.

1. (Facultatif) [Modifier le nom qui apparaît dans les en-têtes de colonne](transaction-property-edit-display-name.md) pour l’une des propriétés.

   Le nom d’affichage par défaut de chaque propriété visible est le nom de la propriété tel qu’il est orthographié dans les données récupérées.

>[!NOTE]
>
>Si Adobe Advertising collecte des données pour les nouvelles propriétés, alors les nouvelles propriétés — à l’exception des conversions suivies par [!DNL Google Ads], [!DNL Google Analytics], et [!DNL Microsoft® Advertising] balises de suivi d’événement universel : sont automatiquement exclues des vues de gestion et des rapports jusqu’à ce que vous les incluiez. Nouvelles conversions suivies par [!DNL Google Ads], [!DNL Google Analytics], et [!DNL Microsoft® Advertising] les balises de suivi d’événement universel sont toujours disponibles automatiquement.

>[!MORELIKETHIS]
* [À propos de la gestion des propriétés de transaction d’un annonceur](transaction-property-about.md)
* [Afficher les propriétés de transaction suivies pour un annonceur](transaction-property-view-tracked.md)
* [Modification du nom d’affichage d’une propriété de transaction](transaction-property-edit-display-name.md)

