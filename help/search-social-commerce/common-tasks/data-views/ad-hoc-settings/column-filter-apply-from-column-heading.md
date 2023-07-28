---
title: Application de filtres de données à partir d’un menu d’en-tête de colonne
description: Découvrez comment filtrer les données de page à partir du menu d’en-tête d’une colonne.
exl-id: ad745599-fd98-4f34-b181-085070adb685
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Appliquer un filtre de données à partir d’un menu d’en-tête de colonne

Vous pouvez appliquer autant de filtres que vous le souhaitez à une colonne, une par une. Tous les filtres sont unis à l’aide de l’opérateur AND. Pour ajouter plusieurs filtres à la fois à l’aide de toutes les mesures disponibles, voir &quot;[Application de filtres de données à partir de la barre d’outils](column-filter-apply-from-toolbar.md).&quot;

1. Sur le côté droit de l’en-tête de colonne, cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flèche vers le bas"), puis cliquez sur **[!UICONTROL Add Filter]**.

1. Définissez le filtre sur la colonne :

   * (Filtres sans champs de saisie) Cochez les cases en regard de chaque valeur à inclure, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

   * (Filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, saisissez la valeur appropriée, puis cliquez sur ![Mettre à jour le filtre](/help/search-social-commerce/assets/select.png "Mettre à jour le filtre").

     Par exemple, si vous avez sélectionné le[!UICONTROL Clicks]&quot; et que vous souhaitez renvoyer uniquement les lignes contenant plus de 100 clics, puis sélectionnez *[!UICONTROL greater than]*&quot; et saisissez `100` dans le champ de saisie Selon le type de données, les opérateurs disponibles peuvent inclure : *[!UICONTROL greater than]*, *[!UICONTROL less than]*, *[!UICONTROL equals]*, *[!UICONTROL contains]*, *[!UICONTROL doesn't contain]*, *[!UICONTROL starts with]*, *[!UICONTROL ends with]*, *[!UICONTROL no value]*, *[!UICONTROL has value]*, *[!UICONTROL before]*, *[!UICONTROL after]*, ou *[!UICONTROL no date].*

     >[!NOTE]
     >
     >* Les valeurs de texte ne sont pas sensibles à la casse. Par exemple, si vous filtrez par campagnes dont le nom contient &quot;prêt&quot;, les résultats sont les &quot;prêts aux consommateurs&quot; et les &quot;demandes de prêt&quot;.
     >* Vous ne pouvez appliquer qu’un seul filtre numérique simple (tel que [!UICONTROL Impressions] \> 100) par colonne.
