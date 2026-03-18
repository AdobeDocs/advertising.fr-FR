---
title: Convertir les ID utilisateur de  [!DNL Optimizely]  en ID universels
description: Découvrez comment activer DSP pour ingérer vos segments  [!DNL Optimizely] .
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 5110e9b4c966f5d719743d09b5a3aebbb37e0a05
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL Optimizely] en ID universels

*Fonction Beta*

Utilisez l’intégration de DSP à la plateforme de données clients [!DNL Optimizely] pour convertir les adresses e-mail hachées propriétaires de votre organisation en identifiants universels pour la publicité ciblée.

1. (Pour convertir des adresses e-mail en [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> ; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configurez le suivi pour activer [!DNL Analytics] mesurer](#analytics-tracking).

1. [Créer une source d’audience dans DSP](#source-create).

1. [Préparez et envoyez les données de segment](#push-data).

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

1. Après avoir créé la source de l’audience, partagez la clé de code source avec l’utilisateur [!DNL Optimizely].

## Étape 3 : préparation et transmission des données de segment {#push-data}

L’annonceur doit préparer et diffuser les données à l’aide de l’[!DNL Optimizely Data Platform] . Pour toute question sur le processus, contactez votre représentant [!DNL Optimizely].

1. Dans [!DNL Optimizely Data Platform], hachez les ID d’e-mail pour l’audience à l’aide de l’algorithme SHA-256.

1. Suivez les instructions de [[!DNL Optimizely's]  pour pousser le segment vers DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Insérez les informations suivantes pour activer l’intégration :

   * **Clé Source :** il s’agit de la clé source créée à l’[étape 2](#source-create).

   * **Code de compte :** il s’agit du code de compte DSP alphanumérique, que vous pouvez trouver dans DSP à l’adresse [!UICONTROL Settings] > [!UICONTROL Account].

Les segments seront actualisés tels que configurés pour l’annonceur. Quelle que soit la fréquence d’actualisation du segment, l’inclusion dans un segment expire après 30 jours par défaut ou après une période d’expiration spécifiée par le client ou la cliente. Actualisez vos segments en les poussant à nouveau depuis [!DNL Optimizely] avant l’expiration. Pour demander une expiration de segment personnalisé, contactez l’équipe chargée de votre compte Adobe.

## Étape 4 : comparaison du nombre d’identifiants universels avec le nombre d’adresses e-mail hachées {#compare-id-count}

Les segments doivent être disponibles dans DSP dans les 24 heures. Une fois que DSP a reçu les données de segment, le nombre de profils des audiences doit être visible dans les neuf (9) heures.

Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est disponible et qu’il est renseigné, puis comparez le nombre d’identifiants universels avec le nombre d’adresses e-mail hachées d’origine. Pour plus d’informations sur les taux de traduction des identifiants acceptables et sur les raisons pour lesquelles le nombre de segments peut varier, voir « [Variances de données entre les ID d’e-mail et les ID universels](#universal-ids-data-variances) ».

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, consultez « [&#x200B; Prise en charge de l’activation des identifiants universels &#x200B;](/help/dsp/audiences/universal-ids.md) ».

Pour résoudre les problèmes liés à la procédure de conversion, contactez l’équipe ou l’`adcloud-support@adobe.com` de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À Propos Des Sources D’Audience Propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences Universal ID](source-manage.md)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)
