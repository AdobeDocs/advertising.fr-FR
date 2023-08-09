---
title: Génération d’une balise de suivi de conversion d’Adobe Advertising
description: Découvrez comment créer une balise de conversion d’Adobe Advertising pour effectuer le suivi de vos événements de conversion.
exl-id: 617cd808-c4ba-4413-89e4-0f52cb44f44b
feature: Search Tools, Search Tracking
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Génération d’une balise de suivi de conversion d’Adobe Advertising

*Publicitaires avec suivi de conversion des Adobes Advertising uniquement*

Créez une balise de conversion distincte pour chaque ensemble de mesures dont vous souhaitez effectuer le suivi et fournissez à l’annonceur ou à l’agence une liste de pages Web sur lesquelles insérer chacune d’elles.

>[!NOTE]
>
>Cette fonctionnalité n’ajoute pas de balises d’image ou [!DNL JavaScript] balises sur les pages web de l’annonceur. Les balises doivent être ajoutées conformément à la procédure normale de mise à jour des pages web de l’annonceur.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Spécifiez la variable [paramètres de balise de conversion](#conversion-tag-settings).

1. Générez la balise :

   * Si le site web utilise HTTP, cliquez sur **[!UICONTROL Generate Conversion Tag]**.

   * Si le site web s’exécute sur un serveur sécurisé (HTTPS), cliquez sur **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copiez la balise de la boîte de dialogue et collez-la dans les pages web appropriées si nécessaire.

>[!NOTE]
>
>Chaque mesure de la nouvelle balise de conversion est automatiquement répertoriée dans [!UICONTROL Admin] > [!UICONTROL Conversions], même si elle n’est pas implémentée ou si les pages web sur lesquelles elle se trouve n’ont reçu aucun clic. Ce comportement diffère du comportement des mesures dans les balises créées manuellement ou ailleurs, qui ne sont pas répertoriées dans [!UICONTROL Admin] > [!UICONTROL Conversions] jusqu’à ce que l’une des pages web sur laquelle elle se trouve ait reçu un clic. Dans tous les cas, toutefois, chaque mesure est initialement exclue des objectifs, des rapports et des vues du portfolio jusqu’à ce que vous les rendiez explicitement disponibles. Toutefois, avant d’ajouter les mesures aux objectifs du portfolio, pensez d’abord à rendre les mesures disponibles et à les ajouter aux rapports pour vérifier quand elles reçoivent des clics.

## Paramètres des balises de conversion Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Type de balise à créer :

* *[!UICONTROL Image]:* Pour créer une balise d’image afin d’afficher une image transparente de 1 pixel x 1 pixel (pixel), invisible pour les utilisateurs finaux, sur la page web. Il est recommandé d’utiliser les balises d’image uniquement lorsque le site a une politique contre l’utilisation de balises JavaScript.

* *[!UICONTROL JavaScript]:* Pour créer une balise JavaScript.

Pour plus d’informations sur les différences entre les types de balises, voir &quot;[Questions fréquentes sur les balises de suivi de conversion d’Adobe Advertising et de pages vues](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Une ou plusieurs mesures de conversion à suivre lorsqu’un utilisateur final consulte une page contenant la balise de conversion. Pour ajouter une mesure à la liste, saisissez son nom dans le champ &quot;[!UICONTROL Add new property]&quot;, puis cliquez sur **[!UICONTROL Add]**.

Lorsque plusieurs mesures sont suivies, elles sont unies par une esperluette (`&`) dans la balise , par exemple `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Les mesures ajoutées à cette liste ne sont enregistrées ni intégrées à la [!UICONTROL Conversions] sur la liste [!UICONTROL Admin] . Cependant, des mesures sont ajoutées au [!UICONTROL Conversions] répertorie automatiquement une fois qu’un Adobe Advertising collecte réellement les données d’une mesure, ce qui se produit lorsque la balise de conversion est implémentée sur une page et qu’un utilisateur final effectue une transaction qui ouvre cette page.

**[!UICONTROL Include unique transaction IDs]:** (Facultatif) Inclut une propriété d’ID de transaction (`ev_transid=<transid>`) dans la balise . L’option est sélectionnée par défaut.

Lorsque vous sélectionnez cette option, l’annonceur doit générer une valeur unique pour `<transid>` (par exemple, un identifiant de commande réel) lorsque la transaction est terminée et que celle-ci est renvoyée à l’Adobe Advertising, par exemple : `ev_transid=0123`. Adobe Advertising utilise l’ID de transaction pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété. L’ID de transaction ne peut pas contenir d’esperluette (`&`), qui sont réservés en tant que séparateurs de paramètres. L’ID de transaction est inclus dans [la valeur [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que vous pouvez utiliser pour valider des données dans Search, Social et Commerce avec les données de l’annonceur.

Si les données ne contiennent pas d’identifiant unique par transaction, l’Adobe Advertising en génère toujours un en fonction de l’heure de la transaction.

>[!NOTE]
>
>Si vous envoyez [flux d’ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id.md) avec des données de conversion pour les conversions hors ligne, vous devez envoyer l’ID de transaction (`ev_transid`) pour la partie en ligne de la transaction dans les données de flux pour les parties hors ligne de la transaction.

**[!UICONTROL Page is inside FB app]:** Obsolète

**[!UICONTROL Segment users]:** Obsolète

**[!UICONTROL JS Version]:** ([!DNL JavaScript] (balises uniquement) Quelle version de [!DNL JavaScript] pour créer la balise : *[!UICONTROL v2]* (valeur par défaut) ou *[!UICONTROL v3]*.

Voir &quot;[Questions fréquentes sur les balises de suivi de conversion d’Adobe Advertising et de pages vues](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; pour plus d’informations sur les différences.

>[!MORELIKETHIS]
>
>* [À propos des balises de suivi de conversion d’Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [A propos des outils de création et de décodage des balises de suivi](tracking-tools-about.md)
>* [Questions fréquentes sur les balises de suivi de conversion et de pages vues](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format des balises de suivi de conversion JavaScript version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format des balises de suivi de conversion JavaScript version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format des balises de suivi de conversion d’image](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Balise de mappage de conversion JavaScript Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [À propos de la gestion des mesures de conversion d’un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
