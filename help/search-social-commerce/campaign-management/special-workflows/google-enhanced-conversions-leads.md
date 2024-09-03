---
title: Mise en oeuvre de [!DNL Google Ads] conversions améliorées pour les pistes
description: Découvrez le processus de configuration de [!DNL Google Ads] conversions améliorées pour les pistes.
feature: Search Campaign Management, Conversions
source-git-commit: 60a67c8668df13afc08e14b0a495a37ded24bc0c
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Mise en oeuvre de [!DNL Google Ads] conversions améliorées pour les pistes

*[!DNL Google Ads]comptes uniquement*

[[!DNL Google Ads] les conversions améliorées pour les pistes](https://support.google.com/google-ads/answer/9888656) vous permettent de mapper les utilisateurs à des conversions hors ligne à l’aide de vos données de conversion propriétaires. Utilisez des conversions améliorées pour les pistes dans les environnements où les ID de clic ne sont pas disponibles, par exemple pour effectuer le suivi des ventes par téléphone ou par e-mail qui résultent des pistes du site web.

Dans Search, Social et Commerce, vous pouvez inclure vos conversions améliorées de pistes sous forme de mesures dans les rapports et de mesures pondérées dans les objectifs d’optimisation. Search, Social et Commerce synchronise vos conversions améliorées existantes pour les prospects tous les jours à 05h00 dans le fuseau horaire de l’annonceur.

Pour utiliser cette fonctionnalité, procédez comme suit. Les étapes de création de balises de suivi de conversion et de création d’actions de conversion peuvent éventuellement être annulées.

1. Dans [!DNL Google Ads], souscrivez à des conversions améliorées pour les pistes :

   1. Ouvrez les paramètres de conversion du compte.

   1. Sélectionnez l’option permettant d’augmenter les conversions des prospects et acceptez les conditions d’utilisation.

   1. Choisissez d’utiliser une balise [!DNL Google] ou [!DNL Google Tag Manager] pour créer la balise de conversion.


1. Configurez et implémentez une balise [!DNL Google] pour l’action de conversion.

   Pour obtenir des instructions, reportez-vous à l’aide [!DNL Google Ads] pour créer des balises pour des conversions améliorées pour les pistes [ à l’aide d’une  [!DNL Google] balise](https://support.google.com/google-ads/answer/11021502) ou [à l’aide de [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Créez une action de conversion pour la conversion améliorée pour les pistes dans [Search, Social, &amp; Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) ou [Google Ads](https://support.google.com/google-ads/answer/12216226).

   Pour le **type de conversion,**, sélectionnez *Importer la conversion* ou *Importer.*

1. Si nécessaire, chargez des données propriétaires, y compris des adresses électroniques hachées ou des numéros de téléphone, afin de les attribuer à la conversion pour un compte spécifié. Vous pouvez effectuer cette étape à partir de [Search, Social, &amp; Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) ou en utilisant [!DNL Google Data Manager].

   * Dans Search, Social et Commerce, vous pouvez télécharger un modèle au format [!DNL Microsoft Excel], saisir vos données de conversion, enregistrer le fichier localement, puis télécharger le fichier modifié. Le modèle comprend des colonnes pour indiquer si le consentement de l’utilisateur a été donné pour télécharger des données vers [!DNL Google] à des fins de publicité et à des fins de personnalisation publicitaire.

     Toutes les données chargées sont synchronisées en temps réel sur [!DNL Google Ads].

   * Pour plus d’informations sur le chargement de données à l’aide de [!DNL Google Data Manager], voir &quot;[À propos du gestionnaire de données](https://support.google.com/google-ads/answer/14639041)&quot;.

>[!MORELIKETHIS]
>
>* [ Créez une action de conversion pour une  [!DNL Google Ads] conversion améliorée pour les pistes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Chargement de données de conversion hors ligne pour des conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
