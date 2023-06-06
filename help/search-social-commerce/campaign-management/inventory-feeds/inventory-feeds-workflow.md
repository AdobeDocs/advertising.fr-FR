---
title: A propos de l’automatisation de la gestion des publicités à l’aide des flux d’inventaire
description: Découvrez le workflow permettant de gérer automatiquement la structure du compte et de diffuser des publicités dynamiques basées sur les données de votre inventaire de produits ou de services.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Workflow de gestion des données de campagne à l’aide de flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Testez d’abord au moins un fichier de flux ou un compte, puis automatisez entièrement le processus ou continuez à le contrôler à chaque étape :

1. (Facultatif) Contactez votre équipe de compte d’Adobe pour configurer un répertoire FTP afin de déposer les fichiers de données.

   Si vous utilisez le répertoire FTP, le service de flux recherche les nouveaux fichiers toutes les deux heures.

   Sinon, vous pouvez charger manuellement des fichiers dans le [!UICONTROL Advanced (ACM)] vue.

1. Définir [paramètres de traitement des données de flux](feed-settings-manage.md#feed-data-settings).

   Si vous utilisez le protocole FTP, ne publiez pas automatiquement des données sur les réseaux publicitaires au début. Une fois que vous avez vérifié la sortie de votre premier fichier et que vous êtes satisfait des résultats, vous pouvez modifier les paramètres.

1. Chargez un fichier de données dans le répertoire FTP, [chargement manuel d’un fichier de données](feed-files-manage.md) dans le [!UICONTROL Advanced (ACM) view]ou [activer l’accès à un compte Google ou Microsoft® de centre commercial ;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Pour charger manuellement des fichiers, vous pouvez attendre de créer un modèle qui utilise le fichier de données.

1. (Facultatif) Créez des groupes de [modificateurs](modifiers-manage.md) à utiliser comme variables dans divers champs de données dans les modèles de données de flux.

1. [Créer un ou plusieurs modèles](ad-templates/ad-template-manage.md) qui utilisent les colonnes de données pour créer des campagnes, des groupes publicitaires, des mots-clés et/ou des copies de publicités pour un compte réseau publicitaire spécifique.

1. [Propager les données de flux par le biais des modèles](feed-data-propagate.md), qui remplace les noms des colonnes du modèle par les données du fichier ou du compte. Selon les options de modèle, Search, Social et Commerce crée une nouvelle structure de compte (campagnes, groupes publicitaires, mots-clés) pour les annonces à l’aide des paramètres par défaut ou mappe les annonces à la structure de compte existante.

1. (Facultatif) [Aperçu de la sortie](propagated-data-view.md) dans le [!UICONTROL Advanced (ACM)] et, éventuellement, afficher un résumé des modifications apportées aux données sur la variable [!UICONTROL Propagations] .

1. [Publier les données](propagated-data-post.md) aux comptes réseau publicitaires appropriés.

1. (Si vous utilisez FTP ou un compte de centre commercial pour transférer vos données ; (facultatif) Après avoir validé la sortie du premier fichier de flux, [modification des paramètres](feed-settings-manage.md#feed-data-settings) pour propager automatiquement les données suivantes par le biais des modèles associés et les publier sur les réseaux publicitaires appropriés.

1. (Si vous disposez de nouveaux fichiers de données) Au besoin, téléchargez de nouveaux fichiers, propagez les données par le biais de modèles, puis publiez les données sur le réseau publicitaire approprié. Vous pouvez éventuellement propager et publier les données en une seule étape.

>[!MORELIKETHIS]
>
>* [A propos de l’automatisation de la gestion des publicités à l’aide des flux d’inventaire](inventory-feeds-about.md)
>* [Quand les composants de compte sont-ils créés ou supprimés par les flux de stock ?](when-are-components-created-deleted.md)

