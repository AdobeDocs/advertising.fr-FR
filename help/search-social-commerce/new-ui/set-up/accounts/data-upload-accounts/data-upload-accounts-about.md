---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# À propos du chargement de données de compte pour les rapports et simulations

<!-- Move all related files into one page? -->

Si vous utilisez des réseaux publicitaires en ligne pour lesquels Search, Social et Commerce ne prennent pas en charge les API, vous pouvez charger du contenu de campagne et des données de coût hors ligne, de clics et de conversion pour un compte à des fins de création de rapports et de simulation de performances. Les annonceurs avec une [[!DNL Adobe Analytics for Advertising]  intégration &#x200B;](/help/integrations/analytics/overview.md) peuvent également afficher les données de leurs comptes dans Adobe Analytics.

Cette fonctionnalité est disponible pour les réseaux publicitaires qui suivent la structure de campagne standard à trois niveaux (campagne, groupe publicitaire ou ensemble publicitaire, et entité publicitaire (annonce ou mot-clé)). Pour Adobe DSP, la fonctionnalité est disponible pour les packages et les emplacements attribués à un package, mais pas pour les campagnes ni les emplacements avec une fréquence au niveau de l&#39;emplacement.

La prise en charge prête à l’emploi est disponible pour les réseaux suivants :<!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

Le suivi des clics Search, Social et Commerce et le suivi des conversions Adobe Advertising ne sont pas pris en charge avec cette fonctionnalité.

## Fonctionnalité disponible dans Search, Social et Commerce

* Suivi et reporting :

   * Composants de campagne en lecture seule jusqu’au niveau de l’unité d’offre dans les vues de gestion de campagne.

   * Données de performances au niveau du groupe publicitaire <!-- verify the entity level --> dans les vues de gestion de campagnes et les rapports personnalisés. Les annonceurs avec [!DNL Adobe Analytics for Advertising]) obtiennent en outre des données de performances au niveau du groupe publicitaire <!-- verify the entity level --> dans les suites de rapports Adobe Analytics spécifiées pour l’annonceur.&lt;!— Vérifier si les types de données sont limités — coût, clic, impression d&#39;affichage, chiffre d&#39;affaires ? —>

* Simulations de performances lorsque vous ajoutez des campagnes à un portfolio.<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  Search, Social et Commerce n’optimisent rien, et ne placent même pas d’enchères, pour ces types de campagnes au sein d’un portfolio.

## Workflow de configuration des comptes hors ligne

<!-- subtitle wording? -->

1. [Configurer un enregistrement de compte factice](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md).

1. Créez un fichier de données pour un compte unique<!--  in what file format? --> y compris le statut au niveau du jour pour les campagnes, les groupes publicitaires et les publicités.

Les données doivent respecter les exigences en matière de données pour le réseau publicitaire. Les champs de données de chaque entité peuvent donc varier en fonction du réseau publicitaire.

1. &#x200B;<!-- For all ad networks (excluding DSP), -->Chargez les données initiales d’un seul compte de l’une des manières suivantes :

* Chargez un fichier manuellement à partir de votre appareil ou réseau.

* Chargez les données dans un dossier attribué par Search, Social et Commerce dans un compartiment [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]).

  >[!PREREQUISITES]
  >
  >* Contactez l’équipe chargée de votre compte Adobe pour activer le chargement des données de compte pour votre compte d’annonceur Search, Social et Commerce. L’équipe facilitera la création d’un dossier spécifique à l’organisation dans un compartiment [!DNL S3] et vous informera une fois l’opération terminée.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* Récupérez le chemin d’accès de stockage dans le cloud [!DNL S3], l’ID de clé d’accès et la clé d’accès secrète pour votre compte. Le même ID de clé d’accès et la même clé d’accès secrète sont utilisés pour tous les comptes <!-- naming convention?--> de chargement de données de l’organisation.

1. Continuez à charger de nouveaux fichiers de données quotidiennement.

1. Une fois les données chargées pendant 30 jours, vous pouvez éventuellement ajouter les campagnes aux portfolios <!--what type? how should we refer to them? --> et générer des simulations.

Vous pouvez [afficher un journal de chaque chargement de données](upload-log.md) pour consulter son statut. En outre, si vous lancez un chargement mais que celui-ci ne réussit pas complètement, vous recevez une notification d’erreur via [Centre de notifications](/help/search-social-commerce/notifications/notification-about.md), en fonction de vos paramètres de notification.

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [À propos du chargement des données de compte pour les rapports et simulations](data-upload-accounts-about.md)
>* [Charger les données de compte dans un compartiment  [!DNL Amazon] [!DNL S3]](upload-data-from-s3-bucket.md)
>* [Charger les données de compte manuellement](upload-data-manually.md)
>* [Afficher un journal des fichiers de données de compte chargés](upload-log.md)
>* [Gestion des comptes réseau des publicités pour les chargements de données](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
