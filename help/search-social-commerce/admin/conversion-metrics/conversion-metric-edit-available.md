---
title: Modification des mesures de conversion disponibles dans les vues de gestion et les rapports
description: Découvrez comment rendre les mesures de conversion disponibles dans vos vues et rapports de gestion.
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
source-git-commit: 4f8e378e6808160313c4001f52cfecb291721298
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Modification des mesures de conversion disponibles dans les vues de gestion et les rapports

Lors du suivi d’un Adobe Advertising [conversion](/help/search-social-commerce/glossary.md#c-d) pour un annonceur, elle est initialement exclue des objectifs du portfolio, des rapports et des vues de gestion. Pour rendre une mesure de conversion visible, vous devez la rendre explicitement disponible, puis, éventuellement, modifier le nom d’affichage par défaut, qui est le nom affiché. La seule exception concerne le suivi des conversions par [!DNL Google Ads], [!DNL Google Analytics], et [!DNL Microsoft® Advertising] les balises de suivi d’événement universel sont automatiquement disponibles et visibles.

De même, vous pouvez masquer une mesure de conversion des objectifs du portfolio, des rapports et des vues de gestion. Lorsque vous masquez une mesure de conversion qui était auparavant visible, elle est supprimée des mesures dérivées qui contiennent la mesure de conversion.

Dans la liste des mesures de conversion disponibles, chaque utilisateur ayant accès aux données de l’annonceur peut personnaliser les mesures qui s’affichent pour les vues de gestion et les rapports, y compris ou en omettant des mesures spécifiques de son choix.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Toutes les mesures de conversion collectées pour l’annonceur et tous les noms différents spécifiés pour l’affichage sont répertoriés.

1. (Facultatif) Filtrez la liste :

   * Pour rechercher un nom de mesure ou d’affichage spécifique, cliquez sur ![Rechercher](/help/search-social-commerce/assets/search.png "Rechercher"), saisissez le mot ou la chaîne dans le champ de saisie, puis appuyez sur la touche **[!DNL Enter]** clé.

     Vous pouvez rechercher des chaînes qui apparaissent n’importe où dans l’expression (comme la première lettre ou les trois dernières lettres), et les termes recherchés ne sont pas [sensible à la casse](/help/search-social-commerce/glossary.md#c-d).

   * Pour rechercher des mesures de conversion en fonction de leur disponibilité dans les vues de gestion et les rapports, cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter.png "Filtrer"), puis sélectionnez le filtre **[!UICONTROL Show in UI and Reports]**. Sélectionnez ensuite l’une des options suivantes : **[!UICONTROL Show]** (pour afficher les mesures de conversion disponibles à inclure dans les rapports et les vues de gestion) ou **[!UICONTROL Hide]** (pour afficher les mesures de conversion non disponibles dans les rapports et les vues de gestion).

1. Modifiez les mesures de conversion disponibles pour les vues de gestion et les rapports :

   * Pour afficher ou masquer une seule mesure, cliquez sur le bouton bascule dans la **[!UICONTROL Show in UI and Reports]** pour modifier le paramètre.

   * Pour afficher ou masquer plusieurs mesures, procédez comme suit :

      1. Cochez la case en regard de chaque mesure de conversion.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Afficher](/help/search-social-commerce/assets/show.png "Afficher") pour afficher les mesures ou ![Masquer](/help/search-social-commerce/assets/hide.png "Masquer") pour masquer les mesures.

      1. (Pour masquer les mesures) Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]** pour masquer les mesures, y compris les supprimer des mesures dérivées qui contiennent les mesures.

1. (Facultatif) [Modifier le nom qui apparaît dans les en-têtes de colonne](conversion-metric-edit-display-name.md) pour l’une des mesures de conversion.

   Le nom d’affichage par défaut de chaque mesure de conversion visible est le nom de la mesure tel qu’il est orthographié dans les données récupérées.

>[!NOTE]
>
>Si Adobe Advertising collecte des données pour les nouvelles mesures de conversion, alors les nouvelles mesures — à l’exception des conversions suivies par [!DNL Google Ads], [!DNL Google Analytics], et [!DNL Microsoft® Advertising] balises de suivi d’événement universel : sont automatiquement exclues des vues de gestion et des rapports jusqu’à ce que vous les incluiez. Nouvelles conversions suivies par [!DNL Google Ads], [!DNL Google Analytics], et [!DNL Microsoft® Advertising] les balises de suivi d’événement universel sont toujours disponibles automatiquement.

>[!MORELIKETHIS]
>
* [À propos de la gestion des mesures de conversion d’un annonceur](conversion-metric-about.md)
* [Afficher les mesures de conversion suivies pour un annonceur](conversion-metric-view-tracked.md)
* [Modification du nom d’affichage d’une mesure de conversion](conversion-metric-edit-display-name.md)
