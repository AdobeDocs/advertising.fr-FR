---
title: Implémenter  [!DNL Google Ads]  conversions améliorées pour les prospects
description: Découvrez le processus de configuration  [!DNL Google Ads]  conversions améliorées pour les prospects.
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
TQID: https://experienceleague.adobe.com/yFJJ662wcsm2KLzCIpxXo6F8nPsklVItHMTBk1h6wHg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 341834cab1e23ddae903ecdeb6946cb004ea777e
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 0%

---

# Implémenter [!DNL Google Ads] conversions améliorées pour les prospects

Comptes *[!DNL Google Ads]uniquement*

[[!DNL Google Ads] conversions améliorées pour les prospects](https://support.google.com/google-ads/answer/9888656) vous permet de mapper des utilisateurs à des conversions hors ligne à l’aide de vos données de conversion propriétaires. Utilisez des conversions améliorées pour les prospects dans les environnements où les ID de clic ne sont pas disponibles, par exemple pour effectuer le suivi des ventes par téléphone ou par e-mail qui résultent des prospects du site web.

Dans Search, Social et Commerce, vous pouvez :

* Affichez vos conversions améliorées existantes pour les prospects.<!-- Where is this? -->

  Search, Social et Commerce synchronise vos conversions améliorées existantes pour les prospects tous les jours à 05:00 dans le fuseau horaire de l’annonceur.

* Créer des conversions améliorées pour les prospects.

* Chargez des données de conversion propriétaires hors ligne pour les mapper à vos conversions améliorées pour les prospects.

* Incluez vos conversions améliorées pour les prospects en tant que mesures dans les rapports et en tant que mesures pondérées dans les objectifs d’optimisation.

Pour utiliser cette fonctionnalité, procédez comme suit. Les étapes de création des balises de suivi de conversion et de création d’actions de conversion peuvent éventuellement être inversées.

1. Dans [!DNL Google Ads], inscrivez-vous aux conversions améliorées pour les prospects :

   1. Ouvrez les paramètres de conversion du compte.

   1. Sélectionnez l’option pour les conversions améliorées de prospects et acceptez les conditions d’utilisation.

   1. Choisissez d’utiliser une balise [!DNL Google] ou [!DNL Google Tag Manager] pour créer la balise de conversion.

1. Configurez et implémentez une balise pour effectuer le suivi de l’action de conversion.

   Pour obtenir des instructions, reportez-vous à l’aide de [!DNL Google Ads] pour créer des balises pour des conversions améliorées de prospects [à l’aide d’une  [!DNL Google]  balise](https://support.google.com/google-ads/answer/11021502) ou [&#x200B; à l’aide de  [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Créez une action de conversion pour la conversion améliorée pour les prospects dans [Search, Social et Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) ou [Google Ads](https://support.google.com/google-ads/answer/12216226).

   Si vous créez l’action de conversion dans Search, Social et Commerce, spécifiez le **type de conversion** tel que *Importer la conversion* ou *Importer*.

1. Chargez aussi souvent que nécessaire des données propriétaires, y compris des adresses e-mail ou des numéros de téléphone hachés, à attribuer à la conversion pour un compte spécifié. Vous pouvez effectuer cette étape à partir de [Search, Social et Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) ou à l’aide de [!DNL Google Data Manager].

   * Dans Search, Social et Commerce, vous pouvez télécharger un modèle au format [!DNL Microsoft Excel], saisir vos données de conversion et enregistrer le fichier localement, puis charger le fichier modifié. Le modèle comprend des colonnes indiquant si l’utilisateur a donné son consentement pour charger des données vers [!DNL Google] à des fins publicitaires et de personnalisation des annonces.

     Toutes les données chargées sont synchronisées en temps réel avec [!DNL Google Ads].

   * Pour plus d’informations sur le chargement de données à l’aide de [!DNL Google Data Manager], voir « [À propos de Data Manager](https://support.google.com/google-ads/answer/14639041) ».

>[!MORELIKETHIS]
>
>* [Création d’une action de conversion pour une conversion  [!DNL Google Ads]  pour les prospects](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Chargement des données de conversion hors ligne pour les conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
