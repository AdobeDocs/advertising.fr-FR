---
title: Application de filtres de données à partir d’un menu d’en-tête de colonne
description: Découvrez comment filtrer les données de page à partir du menu d’en-tête d’une colonne.
exl-id: 508f254a-d859-4155-9bbd-84e0442f01d5
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Appliquer un filtre de données à partir d’un menu d’en-tête de colonne

Vous pouvez appliquer autant de filtres que vous le souhaitez à une colonne, une par une. Tous les filtres sont unis à l’aide de l’opérateur AND. Pour ajouter plusieurs filtres à la fois à l’aide de toutes les mesures disponibles, voir &quot;[Application de filtres de données à partir de la barre d’outils](column-filter-apply-from-toolbar.md)&quot;.

1. Sur le côté droit de l’en-tête de colonne, cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flèche vers le bas"), puis sur **[!UICONTROL Add Filter]**.

1. Définissez le filtre sur la colonne :

   * (Filtres sans champs de saisie) Cochez les cases en regard de chaque valeur à inclure, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

   * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, saisissez la valeur appropriée, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

     Par exemple, si vous avez sélectionné la colonne &quot;[!UICONTROL Clicks]&quot; et que vous souhaitez renvoyer uniquement des lignes avec plus de 100 clics, puis sélectionnez *[!UICONTROL greater than]*&quot; et saisissez `100` dans le champ de saisie En fonction du type de données, les opérateurs disponibles peuvent inclure *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]* 2}, *[!UICONTROL after]* ou *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* Les valeurs de texte ne sont pas sensibles à la casse. Par exemple, si vous filtrez par campagnes dont le nom contient &quot;prêt&quot;, les résultats sont les &quot;prêts aux consommateurs&quot; et les &quot;demandes de prêt&quot;.
     >* Vous ne pouvez appliquer qu’un seul filtre numérique simple (tel que [!UICONTROL Impressions] \> 100) par colonne.
