---
title: Modification des mesures de conversion disponibles dans les vues de gestion et les rapports
description: Découvrez comment rendre les mesures de conversion disponibles dans vos vues et rapports de gestion.
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Modification des mesures de conversion disponibles dans les vues de gestion et les rapports

Lorsqu’Adobe Advertising effectue le suivi d’une mesure [conversion](/help/search-social-commerce/glossary.md#c-d) pour un annonceur, elle est initialement exclue des objectifs, rapports et vues de gestion du portefeuille. Pour rendre une mesure de conversion visible, vous devez la rendre explicitement disponible, puis éventuellement modifier le nom d’affichage par défaut, qui est le nom affiché. La seule exception est que les conversions suivies par les balises de suivi d’événement universel [!DNL Google Ads], [!DNL Google Analytics] et [!DNL Microsoft Advertising] sont automatiquement disponibles et visibles.

De même, vous pouvez masquer une mesure de conversion dans les objectifs, les rapports et les vues de gestion du portefeuille. Lorsque vous masquez une mesure de conversion qui était visible auparavant, elle est supprimée de toute mesure dérivée contenant la mesure de conversion.

Dans la liste des mesures de conversion disponibles, chaque utilisateur ayant accès aux données de l’annonceur peut personnaliser les mesures qu’il voit pour les vues et les rapports de gestion, y compris des mesures spécifiques, qu’il choisit ou non.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Toutes les mesures de conversion qui ont été collectées pour l’annonceur, ainsi que tous les noms différents qui ont été spécifiés pour l’affichage, sont répertoriés.

1. (Facultatif) Filtrez la liste :

   * Pour rechercher un nom de mesure ou un nom d’affichage spécifique, cliquez sur ![Rechercher](/help/search-social-commerce/assets/search.png "Rechercher"), saisissez le mot ou la chaîne dans le champ de saisie, puis appuyez sur la touche **[!DNL Enter]**.

     Vous pouvez rechercher des chaînes qui apparaissent n’importe où dans l’expression (comme la première lettre ou les trois dernières lettres) et les termes de recherche ne sont pas [ sensibles à la casse](/help/search-social-commerce/glossary.md#c-d).

   * Pour rechercher des mesures de conversion en fonction de leur disponibilité dans les vues de gestion et les rapports, cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter.png "Filtrer"), puis sélectionnez le **[!UICONTROL Show in UI and Reports]** de filtrage. Sélectionnez ensuite **[!UICONTROL Show]** (pour afficher les mesures de conversion disponibles à inclure dans les rapports et les vues de gestion) ou **[!UICONTROL Hide]** (pour afficher les mesures de conversion non disponibles dans les rapports et les vues de gestion).

1. Modifiez les mesures de conversion disponibles pour les vues et les rapports de gestion :

   * Pour afficher ou masquer une seule mesure, cliquez sur le bouton (bascule) de la colonne **[!UICONTROL Show in UI and Reports]** pour modifier le paramètre.

   * Pour afficher ou masquer plusieurs mesures, procédez comme suit :

      1. Cochez la case en regard de chaque mesure de conversion.

         Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Afficher](/help/search-social-commerce/assets/show.png "Afficher") pour afficher les mesures ou sur ![Masquer](/help/search-social-commerce/assets/hide.png "Masquer") pour masquer les mesures.

      1. (Pour masquer les mesures) Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]** pour masquer les mesures, y compris en les supprimant de toutes les mesures dérivées qui contiennent les mesures.

1. (Facultatif) [Modifiez le nom qui apparaît dans les en-têtes de colonne](conversion-metric-edit-display-name.md) pour l’une des mesures de conversion.

   Le nom d’affichage par défaut de chaque mesure de conversion visible est le nom de la mesure tel qu’il est orthographié dans les données récupérées.

>[!NOTE]
>
>Si Adobe Advertising collecte des données pour les nouvelles mesures de conversion, les nouvelles mesures, à l’exception des conversions suivies par [!DNL Google Ads], [!DNL Google Analytics] et [!DNL Microsoft Advertising] balises de suivi d’événement universel, sont automatiquement exclues des vues de gestion et des rapports jusqu’à ce que vous les incluiez. Les nouvelles conversions suivies par les balises de suivi d’événement universel [!DNL Google Ads], [!DNL Google Analytics] et [!DNL Microsoft Advertising] sont toujours automatiquement disponibles.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des mesures de conversion d’un annonceur](conversion-metric-about.md)
>* [Affichage des mesures de conversion suivies pour un annonceur](conversion-metric-view-tracked.md)
>* [Modifier le nom d’affichage d’une mesure de conversion](conversion-metric-edit-display-name.md)
