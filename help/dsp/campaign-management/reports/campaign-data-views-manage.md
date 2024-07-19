---
title: Gestion des vues de données de campagne
description: Découvrez comment personnaliser vos vues de données pour les campagnes, les packages, les emplacements et les publicités.
feature: DSP Campaign Data Views
exl-id: a22da10b-104d-4860-a23f-f2a6e59b637c
source-git-commit: 5b07096e5f07c60a3efcbf4213b3bc2f061f36a4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Gestion des vues de données de campagne

Vous pouvez personnaliser les données qui apparaissent dans vos vues de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]).

## Gestion des visualisations des données {#data-visualizations-manage}

Vous pouvez modifier les mesures et le mode graphique pour toutes les visualisations de données sur les campagnes ou pour une seule campagne. Les modifications apportées à une seule campagne sont appliquées à toutes les visualisations de données de la campagne, y compris celles des vues [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads].

### Modification des mesures d’une visualisation de données

1. Dans le coin supérieur droit de la visualisation des données, cliquez sur ![Paramètres](/help/dsp/assets/settings-chart.png).

1. Sélectionnez les mesures.

   Vous ne pouvez pas sélectionner deux fois la même mesure.

1. Cliquez sur **[!UICONTROL Apply]**.

### Modification du mode d’affichage d’une visualisation de données

* Dans le coin supérieur droit de la visualisation des données, cliquez sur le commutateur [!UICONTROL Overlay] (![Interrupteur de recouvrement](/help/dsp/assets/overlay.png)) pour passer du mode superposition (tous les graphiques superposés ensemble) au mode graphique à contours (trois graphiques distincts).

## Gestion des tableaux de données {#data-tables-manage}

Dans toutes les vues de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]), vous pouvez personnaliser les données qui apparaissent dans le tableau de données.

### Gérer les vues de colonne {#column-views-manage}

Chaque niveau de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]) comprend des vues [!UICONTROL Pacing] et [!UICONTROL Performance] intégrées qui incluent les mesures pertinentes pour cette entité. Par défaut, la vue [!UICONTROL Pacing] s’affiche afin que vous puissiez identifier en un coup d’oeil les campagnes et composants de campagne peu performants. Vous pouvez éventuellement créer et modifier des jeux de colonnes personnalisés.

![sélecteur de vue de colonne](/help/dsp/assets/column-view-selector.png)

DSP enregistre votre vue la plus récente comme vue par défaut, de sorte que, chaque fois que vous revenez sur la page, vous affichez toujours les mesures qui vous concernent.

#### Modification du mode Colonnes {#column-view-change}

* Dans le sélecteur d’affichage, cliquez sur ![flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur le nom de la colonne de votre choix.

#### Création d’un mode Colonnes personnalisé {#column-view-create}

1. Dans le sélecteur d’affichage, cliquez sur ![flèche vers le bas](/help/dsp/assets/chevron-down.png), puis sur **[!UICONTROL Create View]**.

1. Spécifiez les mesures à inclure dans la vue :

   1. Dans la liste des mesures disponibles, cochez la case en regard de chaque mesure à inclure.

      Toutes les mesures sont alphabétiques par catégorie : [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (mesures standard qui DSP le suivi), [!UICONTROL Viewability] et [!UICONTROL Conversions]. Les mesures ajoutées avec &quot;([!UICONTROL Lifetime])&quot; renvoient des valeurs depuis le début de la campagne, indépendamment de la période sélectionnée sur la page.

   1. Modifiez l’ordre des colonnes, le cas échéant, en cliquant sur les noms de colonne dans le panneau de droite et en les faisant glisser aux emplacements requis.

   Certaines colonnes ont des positions fixes et ne peuvent pas être déplacées ni supprimées.

1. Appliquez ou enregistrez les paramètres :

   * Pour appliquer temporairement les paramètres sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply].**

   * Pour enregistrer les paramètres dans une nouvelle vue de colonne personnalisée, cliquez sur **[!UICONTROL Save As]**. Dans la fenêtre [!UICONTROL Save View], saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

#### Modification d’un mode Colonnes {#column-view-edit}

>[!NOTE]
>
>Vous ne pouvez pas enregistrer les modifications dans un mode Colonne standard (prédéfini), mais vous pouvez appliquer temporairement vos modifications ou les enregistrer dans un nouveau mode personnalisé.

1. Dans le sélecteur d’affichage, cliquez sur ![flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur le nom du mode Colonne existant.

1. Dans le sélecteur d’affichage, cliquez sur ![flèche vers le bas](/help/dsp/assets/chevron-down.png), puis sur **[!UICONTROL Edit View]**.

1. Modifiez les mesures à inclure dans la vue :

   1. Dans la liste des mesures disponibles, cochez la case en regard de chaque mesure à inclure et décochez la case en regard de chaque mesure à exclure.

      Toutes les mesures sont alphabétiques par catégorie : [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (mesures standard qui DSP le suivi), [!UICONTROL Viewability] et [!UICONTROL Conversions]. Les mesures ajoutées avec &quot;([!UICONTROL Lifetime])&quot; renvoient des valeurs depuis le début de la campagne, indépendamment de la période sélectionnée sur la page.

   1. Modifiez l’ordre des colonnes, le cas échéant, en cliquant sur les noms de colonne dans le panneau de droite et en les faisant glisser aux emplacements requis.

   Certaines colonnes ont des positions fixes et ne peuvent pas être déplacées ni supprimées.

1. Appliquez ou enregistrez les paramètres :

   * (Affichages personnalisés uniquement) Pour enregistrer les paramètres, cliquez sur **[!UICONTROL Save]**.

   * Pour appliquer temporairement les paramètres sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply].**

   * Pour enregistrer les paramètres dans une nouvelle vue de colonne personnalisée, cliquez sur **[!UICONTROL Save As]**. Dans la fenêtre [!UICONTROL Save View], saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

### Filtrage des données de campagne {#filter-data-tables}

Les filtres modifient les données affichées dans l’onglet actif. Les filtres disponibles varient selon le type d’entité, mais peuvent inclure le nom de l’entité, l’état et des colonnes de propriétés supplémentaires.

1. Dans la barre d’outils principale, cliquez sur ![Bouton de filtrage](/help/dsp/assets/filter.png).
1. Pour chaque filtre à appliquer, cliquez sur le nom du filtre dans la colonne de gauche, puis indiquez la ou les valeurs du filtre.
1. Cliquez sur **[!UICONTROL Apply]**.

#### Filtres disponibles

Les filtres suivants sont disponibles pour vos vues [!UICONTROL Campaigns], [!UICONTROL Packages] et [!UICONTROL Placements] :

* [!UICONTROL Campaigns] filtres de vue :
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] filtres de vue :
   * [!UICONTROL Custom flights] (s’ils existent ou non)
   * [!UICONTROL Custom goal] (le cas échéant)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] filtres de vue :
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (le cas échéant)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than] ou [!UICONTROL equal to] une valeur spécifiée)
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Pacing on] ([!UICONTROL impressions] ou [!UICONTROL spend])
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package]
   * [!UICONTROL Placement status]
   * [!UICONTROL Placement type]
   * [!UICONTROL Placement sub-type]
   * [!UICONTROL Start date]
   * [!UICONTROL Creation date]
* [!UICONTROL Ads] filtres de vue :
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]


### Modification de la plage de dates

Modifiez la période utilisée dans tous les affichages standard et personnalisés à l’aide du sélecteur de période situé au-dessus d’un tableau de données.

![Sélecteur de plage de dates](/help/dsp/assets/date-range-selector.png "Sélecteur de plage de dates")

* Pour une période prédéfinie : effectuez une sélection dans la liste des incréments de temps communs. La valeur par défaut est [!UICONTROL Last 30 days]*.

* Pour une plage spécifique, effectuez l’une des opérations suivantes :

   * Cliquez sur ![Calendrier](/help/dsp/assets/calendar.png "2}, puis sur la date de début et la date de fin dans le calendrier.")

   * Cliquez sur dans la plage de dates, puis entrez une date de début et une date de fin ou sélectionnez-les dans le calendrier.

     Vous pouvez saisir des valeurs numériques (de M-J-AA à MM-JJ-AAAA) et/ou des noms ou abréviations de mois (janvier ou janvier, par exemple).

### Tri d’une colonne de données

Vous pouvez trier n’importe quelle colonne de données par ordre croissant (de A à Z ou de 1 à 10) ou par ordre décroissant (de Z à A ou de 10 à 1).

* Cliquez sur l’en-tête de colonne pour basculer entre l’ordre croissant et l’ordre décroissant.


### Définition du nombre de lignes de données

En bas à droite d’une page, en regard de **[!UICONTROL Items per page]** , sélectionnez *[!UICONTROL 25]*, *[!UICONTROL 50]* ou *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues Campaign Management](campaign-reports-about.md)
>* [Affichage des sites, publicités et détails de fréquence pour un emplacement](placement-details-view.md)
>* [Afficher le rapport Prévision de positionnement](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Affichage des rapports de diagnostic d’emplacement](placement-diagnostics.md)
>* [Exporter des données d’une vue Campaign Management](campaign-export-data.md)
>* [Vidéo : DSP structure de compte et interface utilisateur](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
