---
title: Filtrage des données par période
description: Découvrez comment utiliser le filtre de période globale.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Filtrage des données par période

Le même filtre de période globale est appliqué à la plupart des vues de données de campagne, pour tous vos annonceurs, à l’exception des vues par défaut et personnalisées pour lesquelles vous avez enregistré des périodes spécifiques. La période par défaut du système pour les vues de gestion de campagne est &quot;Hier&quot;.

Vos paramètres de période sont enregistrés dans un cookie spécifique au navigateur. Dès lors, toutes les modifications apportées au filtre de période sont utilisées pour tous vos annonceurs chaque fois que vous vous connectez à l’aide de la même application de navigateur, jusqu’à ce que vous modifiiez le filtre ou supprimiez le cookie. Chaque application de navigateur que vous utilisez stocke les paramètres de filtre de période dans un cookie différent.

Lorsque vous enregistrez une plage de dates spécifique pour une vue par défaut ou personnalisée, cette plage est appliquée chaque fois que vous appliquez la vue, quelle que soit l’application du navigateur que vous utilisez.

>[!NOTE]
>
>* Vous pouvez afficher les données des 13 mois précédents, mais les vues personnalisées existantes ne peuvent inclure des données que pour les 180 jours précédents.
>* Pour afficher des données antérieures, accédez à la [[!UICONTROL Reports] view](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) et exécutez un rapport de base.
>* Vous pouvez également enregistrer une période pour une [vue par défaut ou vue personnalisée](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Modifier le filtre de date globale dans les vues de campagne

1. Au-dessus de tout tableau de données dans Rechercher > Campagnes > Campagnes, cliquez sur la période actuelle.

1. Dans le **[!UICONTROL Date Range]** , indiquez la plage :

   * Pour une période prédéfinie : effectuez une sélection dans la liste des incréments de temps communs, allant de *[!UICONTROL Today]* to *[!UICONTROL Last 180 Days]*. La valeur par défaut est *[!UICONTROL Yesterday]*.

   * Pour une plage spécifique : sélectionnez **[!UICONTROL Custom Date Range]** , puis spécifiez la date de début et la date de fin.

     Entrez des dates au format MM/JJ/AAAA ou MM-JJ-AAAA ou cliquez sur ![Icône Calendrier](/help/search-social-commerce/assets/calendar.png "Icône Calendrier") en regard de chaque champ pour ouvrir le calendrier et sélectionner une date.

1. (Facultatif) Comparez les données de la période spécifiée avec celles d’une deuxième période :

   1. Déplacer le **[!UICONTROL Comparison]** curseur vers *[!UICONTROL On]*.

      Lorsque vous sélectionnez cette option, deux colonnes supplémentaires sont ajoutées pour chaque colonne de données ordinaire. Par exemple, au lieu d’inclure une seule colonne pour &quot;[!UICONTROL Impressions],&quot; le tableau comprend des colonnes pour &quot;[!UICONTROL Impressions R1],&quot;[!UICONTROL Impressions R2],&quot; et &quot;[!UICONTROL Impressions Diff].&quot;  Si vous exportez les données, les mêmes colonnes sont indiquées sous la forme &quot;[!UICONTROL Impressions Range 1],&quot;[!UICONTROL Impressions Range 2],&quot; et &quot;[!UICONTROL Impressions Difference].&quot;

   1. Indiquez la deuxième période.

   1. Choisissez comment exprimer la différence entre les données des deux périodes sélectionnées dans le &quot;\[&quot;_Champ de données_\] Différence&quot; :

      * *[!UICONTROL Variance]* (valeur par défaut) : affiche la différence sous la forme d’une valeur numérique.

      * *[!UICONTROL % Change]:*  Affiche la différence en pourcentage.

1. Cliquez sur **[!UICONTROL Apply]**.
