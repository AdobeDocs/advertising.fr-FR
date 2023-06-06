---
title: A propos de l’automatisation de la gestion des publicités à l’aide des flux d’inventaire
description: Découvrez la gestion avancée des campagnes, qui vous permet de gérer automatiquement la structure du compte et de diffuser des publicités dynamiques en fonction des données de votre inventaire de produits ou de services.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# A propos de l’automatisation de la gestion des publicités à l’aide des flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Le [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] vue pour la gestion avancée des campagnes vous permet de créer et de mettre à jour automatiquement la structure de votre compte réseau publicitaire et de diffuser des publicités dynamiques en fonction des données de votre inventaire de produits ou de services. Vous pouvez charger de nouveaux fichiers avec des données de produit tous les jours ou aussi souvent que vous le souhaitez, ou créer directement un lien vers une [!DNL Google] ou [!DNL Microsoft®] compte du centre commercial. Utilisez la fonctionnalité pour :

* Créez de nouvelles campagnes à partir de sources de données classées.

* Mettre à jour dynamiquement le texte et les annonces responsives sur le Réseau de Recherche, [!DNL Google Ads] publicités commerciales, ou [!DNL Microsoft® Advertising] des publicités commerciales chaque fois que de nouvelles données sont traitées, à l’aide de variables dynamiques pour les éléments de données modifiables (tels que le prix ou la quantité). Chaque fois que vous modifiez les données, les publicités existantes sont supprimées et de nouvelles sont créées.

* Suspendre ou supprimer automatiquement des groupes publicitaires, des mots-clés et des publicités lorsque le stock chute en dessous d’un niveau spécifique, selon une date de fin spécifiée, ou lorsqu’un composant existant est omis des données de flux.

Pour configurer vos publicités, créez des modèles de flux d’inventaire contenant des variables (espaces réservés), puis remplacez les variables par les colonnes de données réelles d’un fichier chargé ou d’un [Compte Google ou Microsoft® de centre commercial synchronisé](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Les variables peuvent également inclure des groupes de modificateurs configurés dans un fichier ou des lignes individuelles du fichier pour créer plusieurs publicités, mots-clés, campagnes ou groupes d’annonces pour chaque ligne applicable du fichier de données. Par exemple, si vous utilisez une variable de groupe de modificateurs dans un titre de publicité, et que le groupe de modificateurs inclut deux modificateurs (&quot;pour économique&quot; et &quot;à remise&quot;), deux publicités distinctes sont créées pour chaque produit — une pour chaque modificateur. Pour [!DNL Google Ads] et [!DNL Microsoft® Advertising] annonces de recherche dynamique, vous pouvez également inclure des valeurs pour les personnalisateurs d’annonces.

| [!UICONTROL Ad Variation] Section du modèle | Modificateurs dans Search, Social et Commerce | Contenu du flux | Publicités résultantes |
|----|----|----|----|
| Titre : Acheter le \{ haut de gamme<i>Catégorie de produits</i>\} &lt;<i>CheapList</i>>.<br><br>Description 1 : Énorme inventaire de \{<i>Nom du produit</i>\}.<br><br>Description 2 : Disponible à l’adresse \{<i>Pourcentage de remise</i>\} % de remise. | Valeurs du groupe de modificateurs &quot;CheapList&quot; :<br><br>&quot;pour pas cher&quot;<br><br>&quot;avec remise&quot; | Catégorie de produits, Nom du produit, Pourcentage de remise<br>électronique,iPods,10<br><br>vêtements,chemises,15<br><br><b>Remarque :</b> Vous pouvez séparer les valeurs par des virgules ou des onglets. | <u>Achetez de l&#39;électronique haut de gamme pour un prix abordable.</u><br>Un énorme stock de tablettes. Disponible avec remise de 10 %.<br><br><u>Achetez de l&#39;électronique haut de gamme à moindre prix.</u><br>Un énorme stock de tablettes. Disponible avec remise de 10 %.<br><br><u>Achetez des vêtements haut de gamme pour bon marché.</u><br>Un énorme stock de chemises. Disponible avec remise de 15 %.<br><br><u>Achetez des vêtements haut de gamme à prix réduit.</u><br>Un énorme stock de chemises. Disponible avec remise de 15 %. |

Une fois les publicités générées, vous pouvez éventuellement les vérifier, puis les publier sur le réseau publicitaire.

>[!NOTE]
>Pour créer ou modifier des données de campagne en bloc à l’aide de fichiers de feuille de calcul, reportez-vous à la section &quot;[A propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

>[!MORELIKETHIS]
>
>* [Workflow de gestion des données de campagne à l’aide de flux d’inventaire](inventory-feeds-workflow.md)
>* [Quand les composants de compte sont-ils créés ou supprimés par les flux de stock ?](when-are-components-created-deleted.md)

