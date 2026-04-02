---
title: À propos de l’automatisation de la gestion des publicités à l’aide de flux d’inventaire
description: Découvrez la gestion avancée des campagnes, qui vous permet de gérer automatiquement la structure du compte et de diffuser des annonces dynamiques basées sur les données relatives à votre inventaire de produits ou services.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/UqICY8g8nUAo4JSdAJ8h09P65nbe36aUYDEfOnBT9Jg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 838
ht-degree: 0%

---

# À propos de l’automatisation de la gestion des publicités à l’aide de flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

La vue [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] de la gestion de campagnes avancée vous permet de créer et de mettre à jour automatiquement la structure du compte du réseau publicitaire et de diffuser des annonces dynamiques en fonction des données relatives à votre inventaire de produits ou services. Vous pouvez charger de nouveaux fichiers avec des données de produit tous les jours ou aussi souvent que vous le souhaitez, ou créer un lien direct vers un compte [!DNL Google] ou [!DNL Microsoft] centre commercial. Utilisez la fonction pour :

* Créez de nouvelles campagnes à partir de sources de données ordonnées.

* Mettez à jour de manière dynamique du texte et des annonces de recherches réactives, des annonces d’achats [!DNL Google Ads] ou des annonces d’achats [!DNL Microsoft Advertising] chaque fois que de nouvelles données sont traitées, à l’aide de variables dynamiques pour les éléments de données modifiables (tels que le prix ou la quantité). Chaque fois que vous modifiez les données, les annonces existantes sont supprimées et de nouvelles sont créées.

* Suspendre ou supprimer automatiquement les groupes d’annonces, les mots-clés et les annonces lorsque les stocks chutent en dessous d’un niveau spécifique, selon une date de fin spécifiée, ou lorsqu’un composant existant est omis des données de flux.

Pour configurer vos publicités, créez des modèles de flux d’inventaire contenant des variables (espaces réservés), puis remplacez les variables par des colonnes de données réelles à partir d’un fichier chargé ou d’un compte de centre commercial [Google ou Microsoft synchronisé](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Les variables peuvent également inclure des groupes de modificateurs que vous configurez dans un fichier ou des lignes individuelles du fichier pour créer plusieurs annonces, mots-clés, campagnes ou groupes d’annonces pour chaque ligne applicable dans le fichier de données. Par exemple, si vous utilisez une variable de groupe de conditions commerciales dans un titre d&#39;annonce et que le groupe de conditions commerciales comprend deux conditions commerciales (« pour un prix abordable » et « avec une remise »), deux annonces distinctes sont créées pour chaque produit, une pour chaque condition commerciale. Pour les annonces de recherche dynamique [!DNL Google Ads] et [!DNL Microsoft Advertising], vous pouvez également inclure des valeurs pour les personnalisateurs d’annonces.

| Section [!UICONTROL Ad Variation] du modèle | Modificateurs dans Search, Social et Commerce | Contenu du flux | Publicités résultantes |
|----|----|----|----|
| Titre : achetez des produits haut de gamme \{<i>Product Category</i>\} &lt;<i>CheapList</i>>.<br><br>Description 1 : vaste inventaire de \{<i>Product Name</i>\}.<br><br>Description 2 : disponible au \{<i>Pourcentage de remise</i>\} % de remise. | Valeurs pour le groupe de conditions commerciales « CheapList »:<br><br>« for cost »<br><br>« at a discount » | Catégorie de produits,Nom du produit,Pourcentage de remise<br>électronique,iPods,10<br><br>vêtements,Chemises,15<br><br><b>Remarque :</b> vous pouvez séparer les valeurs par des virgules ou des tabulations. | <u>Achetez de l&#39;électronique haut de gamme pour pas cher.</u><br>Gros stock de tablettes. Disponible à 10% de réduction.<br><br><u>Achetez de l&#39;électronique haut de gamme à rabais.</u><br>Gros stock de tablettes. Disponible à 10% de réduction.<br><br><u>Achetez des vêtements haut de gamme pour pas cher.</u><br>Gros stock de chemises. Disponible à 15% de réduction.<br><br><u>Achetez des vêtements haut de gamme à prix réduit.</u><br>Gros stock de chemises. Disponible à 15% de réduction. |

Une fois les publicités générées, vous pouvez éventuellement les passer en revue, puis les publier sur le réseau publicitaire.

>[!NOTE]
>Pour créer ou modifier des données de campagne en bloc à l’aide de fichiers de feuille de calcul, reportez-vous à « [À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) ».

## Workflow de gestion des données de campagne à l’aide des flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Testez d’abord au moins un fichier ou compte de flux, puis vous pouvez entièrement automatiser le processus ou continuer à le contrôler à chaque étape :

1. (Facultatif) Contactez l’équipe chargée de votre compte Adobe pour configurer un répertoire FTP afin de déposer les fichiers de données.

   Si vous utilisez le répertoire FTP, le service de flux recherche les nouveaux fichiers toutes les deux heures.

   Sinon, vous pouvez charger manuellement les fichiers dans la vue [!UICONTROL Advanced (ACM)].

1. Définissez [&#x200B; paramètres de traitement des données de flux &#x200B;](feed-settings-manage.md#feed-data-settings).

   Si vous utilisez le protocole FTP, ne publiez pas automatiquement les données sur les réseaux publicitaires au départ. Une fois que vous avez vérifié la sortie de votre premier fichier et que vous êtes satisfait des résultats, vous pouvez modifier les paramètres.

1. Chargez un fichier de données dans le répertoire FTP, [chargez manuellement un fichier de données](feed-files-manage.md) dans le [!UICONTROL Advanced (ACM) view] ou [activez l’accès à un compte Google ou Microsoft Merchant Center](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Pour charger manuellement des fichiers, vous pouvez attendre de créer un modèle qui utilise le fichier de données.

1. (Facultatif) Créez des groupes de [modificateurs](modifiers-manage.md) à utiliser comme variables dans divers champs de données des modèles de données de flux.

1. [Créez un ou plusieurs modèles](ad-templates/ad-template-manage.md) qui utilisent les colonnes de données pour créer des campagnes, des groupes publicitaires, des mots-clés et/ou des copies publicitaires pour un compte de réseau publicitaire spécifique.

1. [Propage les données de flux à travers les modèles](feed-data-propagate.md), ce qui remplace les noms de colonne dans le modèle par les données du fichier ou du compte. Selon les options du modèle, Search, Social et Commerce crée une structure de compte (campagnes, groupes publicitaires, mots-clés) pour les annonces à l’aide des paramètres par défaut ou mappe les annonces à la structure de compte existante.

1. (Facultatif) [Prévisualisez la sortie](propagated-data-view.md) dans les vues [!UICONTROL Advanced (ACM)] et visualisez éventuellement un résumé des modifications de données dans l’onglet [!UICONTROL Propagations].

1. [Publiez les données](propagated-data-post.md) sur les comptes de réseau publicitaire appropriés.

1. (Si vous utilisez un FTP ou un compte de centre commercial pour charger vos données ; facultatif) Après avoir validé la sortie du premier fichier de flux, [modifiez les paramètres](feed-settings-manage.md#feed-data-settings) pour propager automatiquement les données suivantes par le biais des modèles associés et les publier sur les réseaux publicitaires appropriés.

1. (Lorsque vous disposez de nouveaux fichiers de données) Si nécessaire, chargez de nouveaux fichiers, propagez les données par le biais de modèles et publiez les données sur le réseau publicitaire approprié. Vous pouvez éventuellement propager et publier les données en une seule étape.

>[!MORELIKETHIS]
>
>* [Quand les composants de compte sont-ils créés ou supprimés par les flux d’inventaire ?](when-are-components-created-deleted.md)
