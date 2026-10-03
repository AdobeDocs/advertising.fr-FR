---
title: Implémenter [!DNL Microsoft Advertising] conversions améliorées pour les conversions hors ligne
description: Découvrez le workflow de configuration des conversions améliorées [!DNL Microsoft Advertising] pour les conversions hors ligne.
feature: Search Campaign Management, Conversions
exl-id: 44937db7-9e80-4a5d-85c7-5bd5febc3b96
TQID: 'https://experienceleague.adobe.com/GLFczqDqV8HE5hUZt8ORAlQMNy4OqQTtMdaHoYoN10U'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
    internal-label: Conversions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%
---
# Implémenter [!DNL Microsoft Advertising] conversions améliorées pour les conversions hors ligne

Comptes *[!DNL Microsoft Advertising]uniquement*

[[!DNL Microsoft Advertising] conversions améliorées](https://help.ads.microsoft.com/#apex/ads/en/60178) vous permet de mapper des utilisateurs à des conversions hors ligne à l’aide de vos données de conversion propriétaires. Utilisez des conversions améliorées dans les environnements dans lesquels les ID de clic ne sont pas disponibles, par exemple pour effectuer le suivi des ventes par téléphone ou par e-mail qui résultent de prospects de site web.

Dans Search, Social et Commerce, vous pouvez :

* Affichez vos conversions améliorées existantes pour les conversions hors ligne.

  Search, Social et Commerce synchronise vos conversions améliorées existantes tous les jours à 5 h dans le fuseau horaire de l’annonceur.

* Chargez des données de conversion propriétaires hors ligne pour les mapper à vos objectifs de conversion améliorés existants.

* Incluez vos conversions améliorées en tant que mesures dans les rapports et en tant que mesures pondérées dans les objectifs d’optimisation.

Pour utiliser cette fonctionnalité, procédez comme suit.

1. Suivez toutes les conditions préalables dans l’aide [!DNL Microsoft Advertising] sur « [conversions améliorées](https://help.ads.microsoft.com/#apex/ads/en/60178) ».

1. [Configurez un objectif de conversion amélioré dans [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. Chargez aussi souvent que nécessaire des données propriétaires, y compris des adresses e-mail ou des numéros de téléphone hachés, à attribuer à la conversion pour un compte spécifié. Vous pouvez effectuer cette étape à partir de [Search, Social et Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) ou dans [!DNL Microsoft Advertising].

   * Dans Search, Social et Commerce, vous pouvez télécharger un modèle au format [!DNL Microsoft Excel], saisir vos données de conversion et enregistrer le fichier localement, puis charger le fichier modifié.

     Toutes les données chargées sont synchronisées en temps réel avec [!DNL Microsoft Advertising].

   * Pour plus d’informations sur le chargement de données dans [!DNL Microsoft Advertising], consultez la section « Configuration de conversions améliorées pour les conversions hors ligne » de l’aide [!DNL Microsoft Advertising] sur « [conversions améliorées](https://help.ads.microsoft.com/#apex/ads/en/60178) ».

>[!MORELIKETHIS]
>
>* [Chargement des données de conversion hors ligne pour les conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
