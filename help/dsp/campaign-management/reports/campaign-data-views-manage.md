---
title: Gestion des vues de données de campagne
description: Découvrez comment personnaliser vos vues de données pour les campagnes, les packages, les emplacements et les publicités.
feature: DSP Campaign Data Views
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Gestion des vues de données de campagne

Vous pouvez personnaliser les données qui apparaissent dans les vues de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], et [!UICONTROL Ads]).

## Gestion des visualisations des données {#data-visualizations-manage}

Vous pouvez modifier les mesures et le mode graphique pour toutes les visualisations de données sur les campagnes ou pour une seule campagne. Les modifications apportées à une seule campagne sont appliquées à toutes les visualisations de données de la campagne, y compris celles du [!UICONTROL Packages], [!UICONTROL Placements], et [!UICONTROL Ads] vues.

### Modification des mesures d’une visualisation de données

1. Dans le coin supérieur droit de la visualisation de données, cliquez sur ![Paramètres](/help/dsp/assets/settings-chart.png).

1. Sélectionnez les mesures.

   Vous ne pouvez pas sélectionner deux fois la même mesure.

1. Cliquez sur **[!UICONTROL Apply]**.

### Modification du mode d’affichage d’une visualisation de données

* Dans le coin supérieur droit de la visualisation des données, cliquez sur le bouton [!UICONTROL Overlay] switch (![Interrupteur de recouvrement](/help/dsp/assets/overlay.png)) pour passer du mode superposition (tous les graphiques superposés ensemble) au mode graphique en courbes (trois graphiques distincts).

## Gestion des tableaux de données {#data-tables-manage}

Dans toutes les vues de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], et [!UICONTROL Ads]), vous pouvez personnaliser les données qui apparaissent dans le tableau de données.

### Gérer les vues de colonne {#column-views-manage}

Chaque niveau de gestion de campagne ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], et [!UICONTROL Ads]) comprend la fonction intégrée [!UICONTROL Pacing] et [!UICONTROL Performance] vues qui incluent des mesures pertinentes pour cette entité. Par défaut, la variable [!UICONTROL Pacing] s’affiche afin que vous puissiez identifier en un coup d’oeil les campagnes et composants de campagne peu performants. Vous pouvez éventuellement créer et modifier des jeux de colonnes personnalisés.

![sélecteur de mode Colonne](/help/dsp/assets/column-view-selector.png)

DSP enregistre votre vue la plus récente comme vue par défaut, de sorte que, chaque fois que vous revenez sur la page, vous affichez toujours les mesures qui vous concernent.

#### Modification du mode Colonnes {#column-view-change}

* Dans le sélecteur d’affichage, cliquez sur ![Flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur le nom du mode Colonne souhaité.

#### Création d’un mode Colonnes personnalisé {#column-view-create}

1. Dans le sélecteur d’affichage, cliquez sur ![Flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur **[!UICONTROL Create View]**.

1. Spécifiez les mesures à inclure dans la vue :

   1. Dans la liste des mesures disponibles, cochez la case en regard de chaque mesure à inclure.

      Toutes les mesures sont alphabétiques par catégorie : [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (mesures standard qui DSP suivies), [!UICONTROL Viewability], et [!UICONTROL Conversions]. Mesures ajoutées avec &quot;([!UICONTROL Lifetime])&quot; renvoie des valeurs à partir du début de la campagne, indépendamment de la période sélectionnée sur la page.

   1. Modifiez l’ordre des colonnes, le cas échéant, en cliquant sur les noms de colonne dans le panneau de droite et en les faisant glisser aux emplacements requis.

   Certaines colonnes ont des positions fixes et ne peuvent pas être déplacées ni supprimées.

1. Appliquez ou enregistrez les paramètres :

   * Pour appliquer temporairement les paramètres sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply].**

   * Pour enregistrer les paramètres dans un nouveau mode de colonne personnalisé, cliquez sur **[!UICONTROL Save As]**. Dans le [!UICONTROL Save View] , saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

#### Modification d’un mode Colonnes {#column-view-edit}

>[!NOTE]
>
>Vous ne pouvez pas enregistrer les modifications dans un mode Colonne standard (prédéfini), mais vous pouvez appliquer temporairement vos modifications ou les enregistrer dans un nouveau mode personnalisé.

1. Dans le sélecteur d’affichage, cliquez sur ![Flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur le nom du mode Colonne existant.

1. Dans le sélecteur d’affichage, cliquez sur ![Flèche vers le bas](/help/dsp/assets/chevron-down.png), puis cliquez sur **[!UICONTROL Edit View]**.

1. Modifiez les mesures à inclure dans la vue :

   1. Dans la liste des mesures disponibles, cochez la case en regard de chaque mesure à inclure et décochez la case en regard de chaque mesure à exclure.

      Toutes les mesures sont alphabétiques par catégorie : [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (mesures standard qui DSP suivies), [!UICONTROL Viewability], et [!UICONTROL Conversions]. Mesures ajoutées avec &quot;([!UICONTROL Lifetime])&quot; renvoie des valeurs à partir du début de la campagne, indépendamment de la période sélectionnée sur la page.

   1. Modifiez l’ordre des colonnes, le cas échéant, en cliquant sur les noms de colonne dans le panneau de droite et en les faisant glisser aux emplacements requis.

   Certaines colonnes ont des positions fixes et ne peuvent pas être déplacées ni supprimées.

1. Appliquez ou enregistrez les paramètres :

   * (Affichages personnalisés uniquement) Pour enregistrer les paramètres, cliquez sur **[!UICONTROL Save]**.

   * Pour appliquer temporairement les paramètres sans les enregistrer dans la vue, cliquez sur **[!UICONTROL Apply].**

   * Pour enregistrer les paramètres dans un nouveau mode de colonne personnalisé, cliquez sur **[!UICONTROL Save As]**. Dans le [!UICONTROL Save View] , saisissez le nom de la nouvelle vue, puis cliquez sur **[!UICONTROL Save]**.

### Filtrage des données de campagne {#filter-data-tables}

Les filtres modifient les données affichées dans l’onglet actif. Les filtres disponibles varient selon le type d’entité, mais peuvent inclure le nom de l’entité, l’état et des colonnes de propriétés supplémentaires.

1. Dans la barre d’outils principale, cliquez sur ![Bouton Filtrer](/help/dsp/assets/filter.png).
1. Pour chaque filtre à appliquer, cliquez sur le nom du filtre dans la colonne de gauche, puis indiquez la ou les valeurs du filtre.
1. Cliquez sur **[!UICONTROL Apply]**.

#### Filtres disponibles

Les filtres suivants sont disponibles pour votre [!UICONTROL Campaigns], [!UICONTROL Packages], et [!UICONTROL Placements] views :

* [!UICONTROL Campaigns] afficher les filtres :
   * [!UICONTROL Campaign status]
   * [!UICONTROL Advertiser]
* [!UICONTROL Packages] afficher les filtres :
   * [!UICONTROL Custom flights] (qu&#39;elles existent ou non)
   * [!UICONTROL Custom goal] (le cas échéant)
   * [!UICONTROL End end date]
   * [!UICONTROL Optimization goal]
   * [!UICONTROL Flight pacing]
   * [!UICONTROL Intraday pacing]
   * [!UICONTROL Package status]
   * [!UICONTROL Start date]
* [!UICONTROL Placements] afficher les filtres :
   * [!UICONTROL Custom ad scheduling]
   * [!UICONTROL Custom goal] (le cas échéant)
   * [!UICONTROL End date]
   * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than], ou [!UICONTROL equal to] une valeur spécifiée)
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
* [!UICONTROL Ads] afficher les filtres :
   * [!UICONTROL Adobe ad approval status]
   * [!UICONTROL Ad ID]
   * [!UICONTROL Ad name]
   * [!UICONTROL Ad type]
   * [!UICONTROL Creation date]


### Modification de la plage de dates

Modifiez la période utilisée dans tous les affichages standard et personnalisés à l’aide du sélecteur de période situé au-dessus d’un tableau de données.

![Sélecteur de période](/help/dsp/assets/date-range-selector.png "Sélecteur de période")

* Pour une période prédéfinie : effectuez une sélection dans la liste des incréments de temps communs. La valeur par défaut est [!UICONTROL Last 30 days]*.

* Pour une plage spécifique, effectuez l’une des opérations suivantes :

   * Cliquez sur ![Calendrier](/help/dsp/assets/calendar.png "Calendrier"), puis cliquez sur la date de début et la date de fin dans le calendrier.

   * Cliquez sur dans la plage de dates, puis entrez une date de début et une date de fin ou sélectionnez-les dans le calendrier.

     Vous pouvez saisir des valeurs numériques (de M-J-AA à MM-JJ-AAAA) et/ou des noms ou abréviations de mois (janvier ou janvier, par exemple).

### Tri d’une colonne de données

Vous pouvez trier n’importe quelle colonne de données par ordre croissant (de A à Z ou de 1 à 10) ou par ordre décroissant (de Z à A ou de 10 à 1).

* Cliquez sur l’en-tête de colonne pour basculer entre l’ordre croissant et l’ordre décroissant.


### Définition du nombre de lignes de données

En bas à droite d’une page, en regard de **[!UICONTROL Items per page]** , sélectionnez *[!UICONTROL 25]*, *[!UICONTROL 50]*, ou *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues Campaign Management](campaign-reports-about.md)
>* [Affichage des sites, publicités et détails de fréquence d’un emplacement](placement-details-view.md)
>* [Afficher le rapport Prévision de positionnement](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Affichage des rapports de diagnostic d’emplacement](placement-diagnostics.md)
>* [Exportation de données à partir d’une vue Campaign Management](campaign-export-data.md)
>* [Vidéo : DSP structure de compte et interface utilisateur](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
