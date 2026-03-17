---
title: Générer et implémenter une balise de suivi des conversions Adobe Advertising
description: Découvrez comment créer une balise de conversion Adobe Advertising pour suivre vos événements de conversion.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: d92fc3fa1ce218788890c073df22afa336aa9ad1
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 0%

---

# Générer et implémenter une balise de suivi des conversions Adobe Advertising

*Annonceurs avec suivi des conversions Adobe Advertising uniquement*

Créez une balise de conversion distincte pour chaque ensemble de mesures dont vous souhaitez effectuer le suivi.

## Générer et implémenter une balise de suivi des conversions dans Search, Social et Commerce

>[!NOTE]
>
>Cette fonctionnalité n’ajoute pas de balises d’image ni de balises de [!DNL JavaScript] aux pages web de l’annonceur. Fournissez les balises à l’annonceur ou à l’agence avec une liste de pages web sur lesquelles les insérer. Les balises doivent être ajoutées conformément à la procédure normale de l’annonceur pour la mise à jour des pages web.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Spécifiez les [paramètres de balise de conversion](#conversion-tag-settings).

1. Générez la balise :

   * Si le site web utilise le protocole HTTP, cliquez sur **[!UICONTROL Generate Conversion Tag]**.

   * Si le site web s’exécute sur un serveur sécurisé (HTTPS), cliquez sur **[!UICONTROL Generate Secure Conversion Tag]**.

1. Copiez la balise de la boîte de dialogue et collez-la dans les pages web appropriées, si nécessaire.

>[!NOTE]
>
>Chaque mesure de la nouvelle balise de conversion est automatiquement répertoriée dans [!UICONTROL Admin] > [!UICONTROL Conversions], même si elle n’est pas implémentée ou si les pages web sur lesquelles elle se trouve n’ont pas reçu de clics. Ce comportement est différent de celui des mesures contenues dans les balises créées manuellement ou ailleurs, qui ne sont pas répertoriées dans [!UICONTROL Admin] > [!UICONTROL Conversions] tant qu’un clic n’a pas été effectué sur l’une des pages web où elles se trouvent. Cependant, dans tous les cas, chaque mesure est initialement exclue des objectifs, rapports et vues du portfolio jusqu’à ce que vous les rendiez explicitement disponibles. Toutefois, avant d’ajouter des mesures aux objectifs du portefeuille, pensez à les rendre disponibles et à les ajouter aux rapports pour vérifier le moment où ils reçoivent des clics.

### Paramètres des balises de conversion Adobe Advertising {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** type de balise à créer :

* *[!UICONTROL Image]:* pour créer une balise d’image afin d’afficher une image transparente de 1 pixel sur 1 pixel (pixel), invisible pour les utilisateurs finaux, sur la page web. La bonne pratique consiste à utiliser les balises d’image uniquement lorsque le site applique une politique interdisant l’utilisation des balises JavaScript.

* *[!UICONTROL JavaScript]:* Création d’une balise JavaScript.

Pour plus d’informations sur les différences entre les types de balises, voir « [FAQ sur les balises de conversion Adobe Advertising et de suivi des pages vues](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md) ».

**[!UICONTROL Tag Properties]:** une ou plusieurs mesures de conversion à suivre lorsqu’un utilisateur final consulte une page contenant la balise de conversion. Pour ajouter une mesure à la liste, saisissez son nom dans le champ « [!UICONTROL Add new property] » et cliquez sur **[!UICONTROL Add]**.

Lorsque plusieurs mesures sont suivies, elles sont rejointes par une esperluette (`&`) dans la balise , par exemple `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Les mesures ajoutées à cette liste ne sont enregistrées nulle part ou intégrées à la liste [!UICONTROL Conversions] du client dans l’onglet [!UICONTROL Admin] . Cependant, les mesures sont automatiquement ajoutées à la liste de [!UICONTROL Conversions] du client une fois qu’Adobe Advertising collecte réellement les données pour une mesure, ce qui se produit lorsque la balise de conversion est implémentée sur une page et qu’un utilisateur final effectue une transaction qui ouvre cette page.

**[!UICONTROL Include unique transaction IDs]:** (facultatif) Inclut une propriété d’ID de transaction (`ev_transid=<transid>`) dans la balise . L’option est sélectionnée par défaut.

Lorsque vous sélectionnez cette option, l’annonceur doit générer une valeur unique pour `<transid>` (par exemple, un ID de commande réel) une fois la transaction terminée et la transmettre à Adobe Advertising, par exemple `ev_transid=0123`. Adobe Advertising utilise l’ID de transaction pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété. L’ID de transaction ne peut pas contenir d’esperluette (`&`), qui sont réservées comme séparateurs de paramètres. L’ID de transaction est inclus dans [le [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), que vous pouvez utiliser pour valider les données dans Search, Social et Commerce avec les données de l’annonceur.

Si les données n’incluent pas d’ID unique par transaction, Adobe Advertising en génère toujours un en fonction de l’heure de transaction.

>[!NOTE]
>
>Si vous envoyez des [flux d’ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id.md) avec des données de conversion pour des conversions hors ligne, vous devez envoyer l’ID de transaction (`ev_transid`) pour la partie en ligne de la transaction dans les données de flux pour les parties hors ligne de la transaction.

**[!UICONTROL Page is inside FB app]:** Obsolète

**[!UICONTROL Segment users]:** Obsolète

**[!UICONTROL JS Version]:** (balises [!DNL JavaScript] uniquement) Version de la balise [!DNL JavaScript] à créer : *[!UICONTROL v2]* (valeur par défaut) ou *[!UICONTROL v3]*.

Voir « [FAQ sur les balises de conversion et de suivi des pages vues d’Adobe Advertising](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md) ». pour plus d’informations sur les différences.

## Implémentation des balises de suivi des conversions à l’aide des balises Adobe Experience Platform

Vous pouvez configurer le suivi des conversions pour Search, Social et Commerce à l’aide de balises dans Adobe Experience Platform (anciennement appelé Adobe Experience Platform Launch). Les balises sont disponibles pour les clients Adobe Experience Cloud en tant que fonctionnalité à valeur ajoutée incluse.

Les tâches suivantes sont nécessaires pour configurer les balises de suivi des conversions pour Search, Social et Commerce à partir de l’interface utilisateur d’Experience Platform ou de l’interface utilisateur de la collecte de données Experience Platform. Pour obtenir des informations complètes et des instructions sur la configuration des balises, consultez le Guide d’Experience Platform Tags, en commençant par la « [&#x200B; Présentation des balises &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) » et le « [&#x200B; Guide de démarrage rapide &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/get-started/quick-start) ».

>[!PREREQUISITES]
>
>Pour installer l’extension de balise requise, demandez à l’administrateur de votre organisation d’accéder aux fonctionnalités de collecte de données de l’interface utilisateur, y compris l’autorisation `manage_properties`.

1. À partir de l’[interface utilisateur de la collecte de données](https://experience.adobe.com/#/data-collection/), installez l’extension Adobe Advertising [extension](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/extensions/overview) :

   1. Dans la propriété applicable, ouvrez le catalogue d’extensions et sélectionnez **Adobe Advertising**.

   1. Dans le menu déroulant, sélectionnez **SSC** (pour Recherche, Social et Commerce).

   1. Dans le champ **ID d’utilisateur SSC**, saisissez l’ID d’utilisateur numérique pour le compte Search, Social et Commerce de votre entreprise.

      Si vous ne connaissez pas votre identifiant utilisateur, contactez l’équipe chargée de votre compte Adobe.

   1. Cliquez sur **Enregistrer**.

1. Créez une règle (par exemple, « form_completes ») pour déclencher la balise de conversion Search, Social et Commerce :

   1. Dans la section Configuration d’événement :

      1. Sélectionnez les valeurs suivantes :

         **Extension:** `Core`

         **Event Type:** `Library Loaded (Page Top)`

      1. Cliquez sur **Conserver les modifications**.

   1. Dans la section Configuration de la condition :

      1. Spécifiez les valeurs suivantes :

         **Type de logique :** `Regular`

         **Extension:** `Core`

         **Type de condition :** `Path Without Query String`

         **Renvoie true si le chemin est égal à :** le chemin où la conversion doit être suivie (par exemple, `/form_complete`).

      1. Cliquez sur **Conserver les modifications**.

   1. Dans la section Configuration d’action :

      1. Spécifiez les valeurs suivantes :

         **Extension:** `Adobe Advertising`

         **Type d’action :** `AMO Measurement`

         **Nom de la propriété de conversion :** nom de la propriété de conversion (par exemple, `form_completes`).

         **Valeur :** valeur numérique de la propriété de conversion (par exemple, `1` effectuer le suivi de form_completes) ou choisir un [élément de données](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) existant.

      1. Cliquez sur **Conserver les modifications**.

   1. Enregistrez la règle.

1. Publiez les modifications.

>[!MORELIKETHIS]
>
>* [À propos des balises de suivi des conversions Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [À propos des outils de création et de décodage des balises de tracking](tracking-tools-about.md)
>* [FAQ sur les balises de suivi des conversions et des pages vues](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format des balises de suivi des conversions JavaScript version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format des balises de suivi des conversions JavaScript version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format des balises de tracking de conversion d’images](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [Balise de mappage de conversion Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [À propos de la gestion des mesures de conversion d’un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
