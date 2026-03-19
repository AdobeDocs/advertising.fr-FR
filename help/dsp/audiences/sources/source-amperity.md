---
title: Convertir les ID utilisateur de  [!DNL Amperity]  en ID universels
description: Découvrez comment activer DSP pour ingérer vos segments  [!DNL Amperity] .
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: cff6b5ad2c66699a6e0402bce6685acc536fd0a0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL Amperity] en ID universels

*Fonction Beta*

Utilisez l’intégration de DSP à la plateforme de données clients [!DNL Amperity] pour convertir les adresses e-mail hachées propriétaires de votre organisation en identifiants universels pour la publicité ciblée.

1. (Pour convertir des adresses e-mail en [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> ; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configurez le suivi pour activer [!DNL Analytics] mesurer](#analytics-tracking).

1. [Créer une source d’audience dans DSP](#source-create).

1. [Préparation et partage des données de mappage de segments](#map-data).

1. [Demander un transfert de données de [!DNL Amperity] vers DSP](#push-data).

1. [Comparez le nombre d’identifiants universels avec le nombre d’adresses e-mail hachées](#compare-id-count).

## Étape 1 : configurer le suivi pour la mesure des [!DNL Analytics] {#analytics-tracking}

*Annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Pour convertir des adresses e-mail en identifiants [!DNL RampIDs] ou [!DNL ID5], procédez comme suit :

1. (Si vous ne l’avez pas déjà fait) Renseignez tous les [prérequis pour l’implémentation [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et assurez-vous que les [AMO ID et EF ID](/help/integrations/analytics/ids.md) sont renseignés dans vos URL de tracking.

1. Enregistrez-vous auprès du partenaire d’ID universel et déployez du code spécifique à l’ID universel sur vos pages web pour faire correspondre les conversions des ID sur les navigateurs web de bureau et mobiles (mais pas sur les applications mobiles) aux affichages publicitaires :

   * **Par [!DNL RampIDs] :** vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants des navigateurs web de bureau et mobiles (mais pas des applications mobiles) aux affichages publicitaires. Contactez l’équipe chargée de votre compte Adobe qui vous donnera les instructions nécessaires pour vous inscrire à une balise [!DNL LiveRamp] [!DNL LaunchPad] auprès de [!DNL LiveRamp] solutions de trafic d’authentification. L&#39;inscription est gratuite, mais vous devez signer un contrat. Une fois enregistré, votre équipe de compte Adobe génère et fournit une balise unique que votre organisation peut implémenter sur vos pages web.

## Étape 2 : créer une source d’audience dans DSP {#source-create}

1. [Créez une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte d’annonceur. Vous pouvez choisir de convertir vos identifiants d’utilisateur vers l’un des [formats d’ID universels disponibles](source-about.md).

   Les paramètres source incluent une clé source générée automatiquement, que vous utiliserez pour transmettre les données du segment.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec l’utilisateur [!DNL Amperity].

## Étape 3 : préparation et partage des données de mappage de segments {#map-data}

L’annonceur doit préparer et partager des données de mappage de segments.

1. Dans [!DNL Amperity], hachez les ID d’e-mail pour l’audience à l’aide de l’algorithme SHA-256.

1. L’annonceur doit fournir des données de mappage de segments à l’équipe du compte Adobe pour créer les segments dans DSP. Utilisez les noms et valeurs de colonne suivants dans un fichier de valeurs séparées par des virgules :

   * **Clé de segment externe :** clé de segment [!DNL Amperity] associée au segment.

   * **Nom du segment :** le nom du segment.

   * **Description du segment :** l’objectif ou la règle du segment, ou les deux.

   * **ID parent :** laisser vide

   * **Video CPM :** 0

   * **Afficher CPM:** 0

   * **Fenêtre de segment :** durée de vie du segment.

## Étape 4 : demander un transfert de données de [!DNL Amperity] vers DSP {#push-data}

1. Une fois le segment mappé dans DSP, l’annonceur doit travailler avec son représentant [!DNL Amperity] pour distribuer les données de segment dans DSP.

1. L’annonceur doit ensuite confirmer auprès de l’équipe du compte Adobe que les données de segment ont été reçues.

Les segments doivent être disponibles dans DSP dans les 24 heures. Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est disponible et est renseigné.

Les segments seront actualisés tels que configurés pour l’annonceur dans [!DNL Amperity]. Quelle que soit la fréquence d’actualisation du segment, l’inclusion dans un segment expire après 30 jours par défaut ou après une période d’expiration spécifiée par le client ou la cliente. Actualisez vos segments en les poussant à nouveau depuis [!DNL Amperity] avant l’expiration. Pour demander une expiration de segment personnalisé, contactez l’équipe chargée de votre compte Adobe.

## Étape 5 : comparaison du nombre d’identifiants universels avec le nombre d’adresses e-mail hachées {#compare-id-count}

Une fois que DSP a reçu les données de segment, le nombre de profils des audiences doit être visible dans les neuf (9) heures.

Dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement), comparez le nombre d’identifiants universels avec le nombre d’adresses e-mail hachées d’origine. Pour plus d’informations sur les taux de traduction des identifiants acceptables et sur les raisons pour lesquelles le nombre de segments peut varier, voir « [Variances des données entre les ID d’e-mail et les ID universels](#universal-ids-data-variances) ».

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, consultez « [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md) ».

Pour résoudre les problèmes liés à la procédure de conversion, contactez l’équipe ou l’`adcloud-support@adobe.com` de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](source-manage.md)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
