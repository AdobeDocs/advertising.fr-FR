---
title: A propos de l’automatisation de la gestion des publicités à l’aide des flux d’inventaire
description: Découvrez la gestion avancée des campagnes, qui vous permet de gérer automatiquement la structure du compte et de diffuser des publicités dynamiques en fonction des données de votre inventaire de produits ou de services.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# A propos de l’automatisation de la gestion des publicités à l’aide des flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

La vue [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] pour la gestion de campagne avancée vous permet de créer et de mettre à jour automatiquement la structure de votre compte réseau publicitaire et de diffuser des publicités dynamiques en fonction des données de votre inventaire de produits ou de services. Vous pouvez charger de nouveaux fichiers avec des données de produit tous les jours ou aussi souvent que vous le souhaitez, ou vous connecter directement à un compte [!DNL Google] ou [!DNL Microsoft] de centre commercial. Utilisez la fonctionnalité pour :

* Créez de nouvelles campagnes à partir de sources de données classées.

* Mettez à jour dynamiquement le texte et les annonces responsives sur le Réseau de Recherche, les [!DNL Google Ads] annonces d’achats ou les [!DNL Microsoft Advertising] annonces d’achats chaque fois que de nouvelles données sont traitées, à l’aide de variables dynamiques pour les éléments de données modifiables (tels que le prix ou la quantité). Chaque fois que vous modifiez les données, les publicités existantes sont supprimées et de nouvelles sont créées.

* Suspendre ou supprimer automatiquement des groupes publicitaires, des mots-clés et des publicités lorsque le stock chute en dessous d’un niveau spécifique, selon une date de fin spécifiée, ou lorsqu’un composant existant est omis des données de flux.

Pour configurer vos publicités, créez des modèles de flux d’inventaire contenant des variables (espaces réservés), puis remplacez les variables par des colonnes de données réelles issues d’un fichier chargé ou d’un compte [Google ou Microsoft Merchant Center synchronisé](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Les variables peuvent également inclure des groupes de modificateurs configurés dans un fichier ou des lignes individuelles du fichier pour créer plusieurs publicités, mots-clés, campagnes ou groupes d’annonces pour chaque ligne applicable du fichier de données. Par exemple, si vous utilisez une variable de groupe de modificateurs dans un titre de publicité, et que le groupe de modificateurs inclut deux modificateurs (&quot;pour économique&quot; et &quot;à remise&quot;), deux publicités distinctes sont créées pour chaque produit — une pour chaque modificateur. Pour les [!DNL Google Ads] et [!DNL Microsoft Advertising] annonces de recherche dynamique, vous pouvez également inclure des valeurs pour les personnalisateurs d’annonces.

| [!UICONTROL Ad Variation] Section du modèle | Modificateurs dans Search, Social et Commerce | Contenu du flux | Publicités résultantes |
|----|----|----|----|
| Titre : Achetez le haut de gamme \{<i>Catégorie de produits</i>\} &lt;<i>CheapList</i>>.<br><br>Description 1 : immense inventaire de \{<i>Nom du produit</i>\}.<br><br>Description 2 : Disponible à l’adresse \{<i>Pourcentage de remise</i>\}% de remise. | Valeurs du groupe de modificateurs &quot;CheapList&quot;:<br><br>&quot;for low&quot;<br><br>&quot;at a discount&quot; | Catégorie de produits, Nom du produit, Pourcentage de remise<br>électronique, iPods,10<br><br>vêtements,Chemises,15<br><br><b>Remarque :</b> Vous pouvez séparer les valeurs par des virgules ou des onglets. | <u>Achetez de l&#39;électronique haut de gamme pour un prix abordable.</u><br>Inventaire énorme de tablettes. Disponible avec remise de 10 %.<br><br><u>Achetez de l&#39;électronique haut de gamme à moindre prix.</u><br>Inventaire énorme de tablettes. Disponible avec remise de 10 %.<br><br><u>Achetez des vêtements haut de gamme pour un prix abordable.</u><br>Un énorme stock de chemises. Disponible avec remise de 15 %.<br><br><u> Achetez des vêtements haut de gamme à prix réduit.</u><br>Un énorme stock de chemises. Disponible avec remise de 15 %. |

Une fois les publicités générées, vous pouvez éventuellement les vérifier, puis les publier sur le réseau publicitaire.

>[!NOTE]
>Pour créer ou modifier des données de campagne en bloc à l’aide de fichiers de feuille de calcul, voir &quot;[À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)&quot;.

## Workflow de gestion des données de campagne à l’aide de flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Testez d’abord au moins un fichier de flux ou un compte, puis automatisez entièrement le processus ou continuez à le contrôler à chaque étape :

1. (Facultatif) Contactez votre équipe de compte d’Adobe pour configurer un répertoire FTP afin de déposer les fichiers de données.

   Si vous utilisez le répertoire FTP, le service de flux recherche les nouveaux fichiers toutes les deux heures.

   Sinon, vous pouvez charger manuellement des fichiers dans la vue [!UICONTROL Advanced (ACM)].

1. Définissez les [&#x200B; paramètres pour le traitement des données de flux](feed-settings-manage.md#feed-data-settings).

   Si vous utilisez le protocole FTP, ne publiez pas automatiquement des données sur les réseaux publicitaires au début. Une fois que vous avez vérifié la sortie de votre premier fichier et que vous êtes satisfait des résultats, vous pouvez modifier les paramètres.

1. Téléchargez un fichier de données dans le répertoire FTP, [&#x200B; téléchargez manuellement un fichier de données &#x200B;](feed-files-manage.md) dans le répertoire [!UICONTROL Advanced (ACM) view] ou [&#x200B; activez l’accès à un compte Google ou Microsoft Merchant Center &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Pour charger manuellement des fichiers, vous pouvez attendre de créer un modèle qui utilise le fichier de données.

1. (Facultatif) Créez des groupes de [modificateurs](modifiers-manage.md) à utiliser comme variables dans divers champs de données dans les modèles de données de flux.

1. [&#x200B; Créez un ou plusieurs modèles](ad-templates/ad-template-manage.md) qui utilisent les colonnes de données pour créer des campagnes, des groupes publicitaires, des mots-clés et/ou des copies de publicité pour un compte réseau publicitaire spécifique.

1. [Propagez les données de flux par le biais des modèles](feed-data-propagate.md), ce qui remplace les noms de colonne dans le modèle par les données dans le fichier ou le compte. Selon les options de modèle, Search, Social et Commerce crée une nouvelle structure de compte (campagnes, groupes publicitaires, mots-clés) pour les annonces à l’aide des paramètres par défaut ou mappe les annonces à la structure de compte existante.

1. (Facultatif) [Prévisualisez la sortie](propagated-data-view.md) dans les vues [!UICONTROL Advanced (ACM)] et visualisez éventuellement un résumé des modifications apportées aux données dans l’onglet [!UICONTROL Propagations].

1. [Publiez les données](propagated-data-post.md) sur les comptes réseau publicitaire appropriés.

1. (Si vous utilisez FTP ou un compte de centre commercial pour charger vos données, facultatif) Après avoir validé la sortie du premier fichier de flux, [&#x200B; modifiez les paramètres](feed-settings-manage.md#feed-data-settings) pour propager automatiquement les données suivantes par le biais des modèles associés et les publier sur les réseaux publicitaires appropriés.

1. (Si vous disposez de nouveaux fichiers de données) Au besoin, téléchargez de nouveaux fichiers, propagez les données par le biais de modèles, puis publiez les données sur le réseau publicitaire approprié. Vous pouvez éventuellement propager et publier les données en une seule étape.

>[!MORELIKETHIS]
>
>* [Quand les composants de compte sont-ils créés ou supprimés par les flux d’inventaire ?](when-are-components-created-deleted.md)
