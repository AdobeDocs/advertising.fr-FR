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
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%
---
# Filtrer les données par période

<!-- The same in new UI and legacy CM views -->

Le même filtre de période global est appliqué à la plupart de vos vues de données, sur tous vos annonceurs, à l’exception des vues par défaut et personnalisées pour lesquelles vous avez enregistré des périodes spécifiques. La période système par défaut pour les vues de gestion de campagne est « Hier ».

Vos paramètres de période sont enregistrés dans un cookie spécifique au navigateur. Toute modification du filtre de période est donc utilisée pour tous vos annonceurs chaque fois que vous vous connectez à l’aide de la même application de navigateur jusqu’à ce que vous modifiiez le filtre ou supprimiez le cookie. Chaque application de navigateur que vous utilisez stocke les paramètres de filtrage des périodes dans un cookie différent.

Lorsque vous enregistrez une période spécifique pour une vue par défaut ou personnalisée, cette période est appliquée chaque fois que vous appliquez la vue, quelle que soit l&#39;application du navigateur que vous utilisez.

>[!NOTE]
>
>* Vous pouvez afficher les données des 13 derniers mois, mais toutes les vues personnalisées existantes ne peuvent inclure que les données des 180 derniers jours au maximum.
>* Pour afficher des données antérieures, accédez à la vue [&#128279;](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) puis exécutez un rapport de base.[!UICONTROL Reports]
>* Vous pouvez également enregistrer une période pour une vue [&#x200B; par défaut ou personnalisée](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Modification du filtre de date global dans les vues de campagne

1. Au-dessus de tout tableau de données dans Rechercher \> Campagnes \> Campagnes, cliquez sur la période actuelle.

1. Dans le champ **[!UICONTROL Date Range]** , indiquez la plage :

   * Pour une plage prédéfinie : sélectionnez-en une dans la liste des incréments temporels courants, allant de *[!UICONTROL Today]* à *[!UICONTROL Last 180 Days]*. La valeur par défaut est *[!UICONTROL Yesterday]*.

   * Pour une plage spécifique : sélectionnez **[!UICONTROL Custom Date Range]** , puis spécifiez la date de début et la date de fin.

     Saisissez les dates au format MM/JJ/AAAA ou MM-JJ-AAAA, ou cliquez sur ![icône de calendrier](/help/search-social-commerce/assets/calendar.png "icône de calendrier") en regard de chaque champ pour ouvrir le calendrier et sélectionner une date.

1. (Facultatif) Comparez les données de la période spécifiée aux données d’une deuxième période :

   1. Déplacez le curseur **[!UICONTROL Comparison]** vers la position « activé ».

      Lorsque vous sélectionnez cette option, deux colonnes supplémentaires sont ajoutées pour chaque colonne de données standard. Par exemple, au lieu d’inclure une seule colonne pour « [!UICONTROL Impressions] », le tableau inclut des colonnes pour « [!UICONTROL Impressions R1] », « [!UICONTROL Impressions R2] » et « [!UICONTROL Impressions Diff] ».  Si vous exportez les données, les mêmes colonnes sont orthographiées comme « [!UICONTROL Impressions Range 1] », « [!UICONTROL Impressions Range 2] » et « [!UICONTROL Impressions Difference] ».

   1. Spécifiez la deuxième période.

   1. Choisissez comment exprimer la différence entre les données des deux périodes sélectionnées dans la colonne « \[_Champ de données_\] Différence » :

      * *[!UICONTROL Variance]* (valeur par défaut) : affiche la différence sous la forme d’une valeur numérique.

      * *[!UICONTROL % Change]:* affiche la différence en pourcentage.

1. Cliquez sur **[!UICONTROL Apply]**.
