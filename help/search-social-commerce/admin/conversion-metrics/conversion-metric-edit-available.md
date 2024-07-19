---
title: Modification des mesures de conversion disponibles dans les vues de gestion et les rapports
description: Découvrez comment rendre les mesures de conversion disponibles dans vos vues et rapports de gestion.
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Modification des mesures de conversion disponibles dans les vues de gestion et les rapports

Lorsque Adobe Advertising effectue le suivi d’une mesure [conversion](/help/search-social-commerce/glossary.md#c-d) pour un annonceur, elle est initialement exclue des objectifs du portfolio, des rapports et des vues de gestion. Pour rendre une mesure de conversion visible, vous devez la rendre explicitement disponible, puis, éventuellement, modifier le nom d’affichage par défaut, qui est le nom affiché. La seule exception est que les conversions suivies par les balises de suivi universel d’événement [!DNL Google Ads], [!DNL Google Analytics] et [!DNL Microsoft Advertising] sont automatiquement disponibles et visibles.

De même, vous pouvez masquer une mesure de conversion des objectifs du portfolio, des rapports et des vues de gestion. Lorsque vous masquez une mesure de conversion qui était auparavant visible, elle est supprimée des mesures dérivées qui contiennent la mesure de conversion.

Dans la liste des mesures de conversion disponibles, chaque utilisateur ayant accès aux données de l’annonceur peut personnaliser les mesures qui s’affichent pour les vues de gestion et les rapports, y compris ou en omettant des mesures spécifiques de son choix.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Toutes les mesures de conversion collectées pour l’annonceur et tous les noms différents spécifiés pour l’affichage sont répertoriés.

1. (Facultatif) Filtrez la liste :

   * Pour rechercher un nom de mesure ou un nom d’affichage spécifique, cliquez sur ![Rechercher](/help/search-social-commerce/assets/search.png "Rechercher"), entrez le mot ou la chaîne dans le champ de saisie, puis appuyez sur la touche **[!DNL Enter]**.

     Vous pouvez rechercher des chaînes qui apparaissent n’importe où dans l’expression (comme la première lettre ou les trois dernières lettres), et les termes recherchés ne sont pas [sensibles à la casse](/help/search-social-commerce/glossary.md#c-d).

   * Pour rechercher des mesures de conversion en fonction de leur disponibilité dans les vues de gestion et les rapports, cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter.png "Filtre"), puis sélectionnez le filtre **[!UICONTROL Show in UI and Reports]**. Sélectionnez ensuite **[!UICONTROL Show]** (pour afficher les mesures de conversion disponibles à inclure dans les rapports et les vues de gestion) ou **[!UICONTROL Hide]** (pour afficher les mesures de conversion non disponibles dans les rapports et les vues de gestion).

1. Modifiez les mesures de conversion disponibles pour les vues de gestion et les rapports :

   * Pour afficher ou masquer une seule mesure, cliquez sur le commutateur dans la colonne **[!UICONTROL Show in UI and Reports]** pour modifier le paramètre.

   * Pour afficher ou masquer plusieurs mesures, procédez comme suit :

      1. Cochez la case en regard de chaque mesure de conversion.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Afficher](/help/search-social-commerce/assets/show.png "Afficher") pour afficher les mesures ou ![Masquer](/help/search-social-commerce/assets/hide.png "Masquer") pour les masquer.

      1. (Pour masquer les mesures) Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]** pour masquer les mesures, notamment les supprimer des mesures dérivées qui contiennent les mesures.

1. (Facultatif) [Modifiez le nom qui apparaît dans les en-têtes de colonne](conversion-metric-edit-display-name.md) pour l’une des mesures de conversion.

   Le nom d’affichage par défaut de chaque mesure de conversion visible est le nom de la mesure tel qu’il est orthographié dans les données récupérées.

>[!NOTE]
>
>Si Adobe Advertising collecte des données pour les nouvelles mesures de conversion, alors les nouvelles mesures — à l’exception des conversions suivies par les balises de suivi d’événement universel [!DNL Google Ads], [!DNL Google Analytics] et [!DNL Microsoft Advertising] — sont automatiquement exclues des vues de gestion et des rapports jusqu’à ce que vous les incluiez. Les nouvelles conversions suivies par les balises de suivi d’événement universel [!DNL Google Ads], [!DNL Google Analytics] et [!DNL Microsoft Advertising] sont toujours automatiquement disponibles.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des mesures de conversion d’un annonceur](conversion-metric-about.md)
>* [Afficher les mesures de conversion suivies pour un annonceur](conversion-metric-view-tracked.md)
>* [Modification du nom d’affichage d’une mesure de conversion](conversion-metric-edit-display-name.md)
