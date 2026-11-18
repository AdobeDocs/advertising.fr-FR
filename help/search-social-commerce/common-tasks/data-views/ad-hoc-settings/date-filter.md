---
title: Filtrer les données par période
description: Découvrez comment utiliser le filtre de période globale.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: b5d2d666af6062eb3bf07ae041992819a4cc6780
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 0%
---
# Filtrer les données par période

Utilisez le filtre de période pour spécifier la période pendant laquelle afficher les données de performances. Dans les vues qui prennent en charge la comparaison de dates, vous pouvez également comparer les performances pour deux périodes.

## (Nouvelle interface utilisateur) Modifier la période {#date-filter-new-ui}

1. Dans l’en-tête de la page, cliquez sur le contrôle de période avec l’icône de calendrier.

1. Spécifiez la période :

   * Pour utiliser une plage prédéfinie, sélectionnez une option dans le menu au-dessus du premier calendrier, par exemple **[!UICONTROL Yesterday]** ou **[!UICONTROL Last 7 Days]**.

   * Pour utiliser une plage personnalisée, sélectionnez **[!UICONTROL Custom Date Range]** et sélectionnez les dates de début et de fin dans le calendrier. Utilisez les flèches du calendrier pour naviguer entre les mois.

1. Cliquez sur **[!UICONTROL Apply]**.

## (Nouvelle interface utilisateur) Comparer des données pour deux périodes {#compare-periods-new-ui}

*Vues prenant uniquement en charge la comparaison de dates*

1. Dans l’en-tête de la page, cliquez sur le contrôle de période avec l’icône de calendrier.

1. Activer **[!UICONTROL Compare Periods]**.

   Deux panneaux de calendrier sont affichés côte à côte. La première période a un marqueur bleu sarcelle, et la période de comparaison a un marqueur violet.

1. Dans le premier panneau, spécifiez la période :

   * Pour utiliser une plage prédéfinie, sélectionnez une option dans le menu au-dessus du premier calendrier, par exemple **[!UICONTROL Yesterday]** ou **[!UICONTROL Last 7 Days]**.

   * Pour utiliser une plage personnalisée, sélectionnez **[!UICONTROL Custom Date Range]** et sélectionnez les dates de début et de fin dans le calendrier. Utilisez les flèches du calendrier pour naviguer entre les mois.

1. Dans le deuxième panneau, sélectionnez un paramètre prédéfini de comparaison ou cliquez sur une date de début dans le calendrier.

   La période de comparaison comporte le même nombre de jours que la première période. Consultez les périodes complètes au-dessus des deux calendriers.

1. Dans **[!UICONTROL Comparison Format]**, sélectionnez comment afficher la différence :

   * **[!UICONTROL As percentage]:** Afficher la différence en pourcentage.

   * **[!UICONTROL As variance]:** afficher la différence sous forme de valeur numérique.

1. Cliquez sur **[!UICONTROL Apply]**.

   Le contrôle de période affiche les deux périodes complètes avec leurs libellés de période et leurs marqueurs de couleur. Chaque mesure comparable est regroupée en deux colonnes de période et une colonne **[!UICONTROL Change]**. Les champs qui ne sont pas comparables restent des colonnes uniques. Les marqueurs de période dans les en-têtes de colonne identifient les périodes correspondantes.

Pour arrêter la comparaison des périodes, ouvrez la commande de période, désactivez **[!UICONTROL Compare Periods]**, puis cliquez sur **[!UICONTROL Apply]**. La désactivation de la comparaison efface les filtres en fonction des données de comparaison.

### Modification du format de comparaison à partir d’un menu de colonne

1. Lorsque la comparaison de dates est activée, ouvrez le menu d’en-tête de colonne pour une colonne **[!UICONTROL Change]** ou une colonne de période pour une mesure comparable.

1. Sélectionnez **[!UICONTROL As percentage]** ou **[!UICONTROL As variance]**.

   La sélection s’applique à toutes les mesures de comparaison de la grille et pas seulement à la colonne sélectionnée. Le contrôle de période est synchronisé avec la sélection et le format est partagé sur toutes les pages applicables pour l’annonceur actuel, y compris les vues avec des périodes enregistrées.

   Un message de confirmation s’affiche une fois la grille actualisée. Si la grille ne peut pas être actualisée avec le format sélectionné, un message d’erreur s’affiche à la place de cette action. Essayez de sélectionner à nouveau le format.

Les options de tri et de filtrage restent disponibles dans les menus de colonne, lorsqu’elles sont prises en charge.

## (interface utilisateur héritée) Paramètres de période

Le même filtre de période global est appliqué à la plupart de vos vues de données, sur tous vos annonceurs, à l’exception des vues par défaut et personnalisées pour lesquelles vous avez enregistré des périodes spécifiques. La période système par défaut pour les vues de gestion de campagne est « Hier ».

Vos paramètres de période sont enregistrés dans un cookie spécifique au navigateur. Toute modification du filtre de période est donc utilisée pour tous vos annonceurs chaque fois que vous vous connectez à l’aide de la même application de navigateur jusqu’à ce que vous modifiiez le filtre ou supprimiez le cookie. Chaque application de navigateur que vous utilisez stocke les paramètres de filtrage des périodes dans un cookie différent.

Lorsque vous enregistrez une période spécifique pour une vue par défaut ou personnalisée, cette période est appliquée chaque fois que vous appliquez la vue, quelle que soit l&#39;application du navigateur que vous utilisez.

>[!NOTE]
>
>* Vous pouvez afficher les données des 13 derniers mois, mais toutes les vues personnalisées existantes ne peuvent inclure que les données des 180 derniers jours au maximum.
>* Pour afficher des données antérieures, accédez à la vue [[!UICONTROL Reports]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) et exécutez un rapport de base.
>* Vous pouvez également enregistrer une période pour une vue [par défaut ou personnalisée](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## (interface utilisateur héritée) Modifier le filtre de date global dans les vues de campagne

1. Au-dessus de tout tableau de données dans Rechercher \> Campagnes \> Campagnes, cliquez sur la période actuelle.

1. Dans le champ **[!UICONTROL Date Range]**, spécifiez la plage :

   * Pour une plage prédéfinie : sélectionnez-en une dans la liste des incréments temporels courants, compris entre *[!UICONTROL Today]* et *[!UICONTROL Last 180 Days]*. La valeur par défaut est *[!UICONTROL Yesterday]*.

   * Pour une plage spécifique : sélectionnez **[!UICONTROL Custom Date Range]** , puis spécifiez la date de début et la date de fin.

     Saisissez les dates au format MM/JJ/AAAA ou MM-JJ-AAAA, ou cliquez sur ![Icône du calendrier](/help/search-social-commerce/assets/calendar.png "Icône du calendrier") à côté de chaque champ pour ouvrir le calendrier et sélectionner une date.

1. (Facultatif) Comparez les données de la période spécifiée aux données d’une deuxième période :

   1. Déplacez le curseur **[!UICONTROL Comparison]** vers la position « activé ».

      Lorsque vous sélectionnez cette option, deux colonnes supplémentaires sont ajoutées pour chaque colonne de données standard. Par exemple, au lieu d’inclure une seule colonne pour « [!UICONTROL Impressions] », le tableau inclut des colonnes pour « [!UICONTROL Impressions R1] », « [!UICONTROL Impressions R2] » et « [!UICONTROL Impressions Diff] ».  Si vous exportez les données, les mêmes colonnes sont orthographiées comme « [!UICONTROL Impressions Range 1] », « [!UICONTROL Impressions Range 2] » et « [!UICONTROL Impressions Difference] ».

   1. Spécifiez la deuxième période.

   1. Choisissez comment exprimer la différence entre les données des deux périodes sélectionnées dans la colonne « \[_Champ de données_\] Différence » :

      * *[!UICONTROL Variance]* (valeur par défaut) : affiche la différence sous forme de valeur numérique.

      * *[!UICONTROL % Change]:* affiche la différence en pourcentage.

1. Cliquez sur **[!UICONTROL Apply]**.
