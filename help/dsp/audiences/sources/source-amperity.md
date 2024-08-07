---
title: Convertir les ID utilisateur de [!DNL Amperity]  en ID universels
description: Découvrez comment activer DSP d’ingérer vos segments propriétaires  [!DNL Amperity] .
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL Amperity] en ID universels

*Fonctionnalité Beta*

Utilisez l’intégration DSP à la plateforme de données client [!DNL Amperity] pour convertir les adresses électroniques hachées propriétaires de votre entreprise en identifiants universels pour la publicité ciblée.

1. (Pour convertir les adresses électroniques en [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> ; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [ Configurez le suivi pour activer  [!DNL Analytics] la mesure](#analytics-tracking).

1. [Créez une source d’audience dans DSP](#source-create).

1. [Préparez et partagez des données de mappage de segments](#map-data).

1. [Demandez une transmission de données de [!DNL Amperity] à DSP](#push-data).

1. [Comparez le nombre d&#39;identifiants universels avec le nombre d&#39;adresses électroniques hachées](#compare-id-count).

## Étape 1 : configuration du suivi pour la mesure [!DNL Analytics] {#analytics-tracking}

*Annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Pour convertir les adresses électroniques en [!DNL RampIDs] ou [!DNL ID5] ID, procédez comme suit :

1. (Si vous ne l’avez pas déjà fait) Renseignez toutes les [conditions préalables à l’implémentation  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et assurez-vous que les [AMO ID et EF ID](/help/integrations/analytics/ids.md) sont renseignés dans vos URL de suivi.

1. Inscrivez-vous auprès du partenaire d’ID universel et déployez le code spécifique à l’ID universel sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs de bureau et les navigateurs web mobiles (mais pas les applications mobiles) aux affichages publicitaires :

   * **Pour [!DNL RampIDs] :** vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs web de bureau et mobiles (mais pas sur les applications mobiles) aux affichages publicitaires. Contactez votre équipe de compte d’Adobe, qui vous donnera des instructions pour vous inscrire à une balise [!DNL LiveRamp] [!DNL LaunchPad] des solutions de trafic d’authentification [!DNL LiveRamp]. L&#39;inscription est gratuite, mais vous devez signer un accord. Une fois que vous vous êtes enregistré, votre équipe de compte d’Adobe génère et fournit une balise unique que votre organisation doit implémenter sur vos pages web.

## Étape 2 : création d’une source d’audience dans DSP {#source-create}

1. [Créez une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire. Vous pouvez choisir de convertir vos identifiants d’utilisateur en l’un des [formats d’ID universels disponibles](source-about.md).

   Les paramètres de la source comprennent une clé source générée automatiquement que vous utiliserez pour transmettre les données du segment.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec l’utilisateur [!DNL Amperity].

## Étape 3 : Préparation et partage des données de mappage de segments {#map-data}

L’annonceur doit préparer et partager les données de mappage de segments.

1. Dans [!DNL Amperity], hachez les ID d’email pour l’audience à l’aide de l’algorithme SHA-256.

1. L’annonceur doit fournir des données de mappage de segments à l’équipe du compte d’Adobe pour créer les segments dans DSP. Utilisez les noms et valeurs de colonne suivants dans un fichier de valeurs séparées par des virgules :

   * **Clé de segment externe :** clé de segment [!DNL Amperity] associée au segment.

   * **Nom du segment :** Nom du segment.

   * **Description du segment :** Objectif ou règle du segment, ou les deux.

   * **ID parent :** laissez vide

   * **CPM vidéo :** 0

   * **Afficher CPM :** 0

   * **Fenêtre de segment :** durée de vie du segment.

## Étape 4 : demander une transmission de données de [!DNL Amperity] à DSP {#push-data}

1. Une fois le segment mappé dans DSP, l’annonceur doit travailler avec son représentant [!DNL Amperity] pour distribuer les données de segment à DSP.

1. L’annonceur doit ensuite confirmer auprès de l’équipe du compte d’Adobe que les données de segment ont été reçues.

Les segments doivent être disponibles dans DSP dans les 24 heures. Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est disponible et qu’il est renseigné.

Les segments seront actualisés comme configurés pour l’annonceur dans [!DNL Amperity]. Quelle que soit la fréquence d’actualisation du segment, l’inclusion dans un segment expire par défaut après 30 jours ou après une période d’expiration spécifiée par le client. Actualisez vos segments en les republiant depuis [!DNL Amperity] avant l’expiration. Pour demander une expiration de segment personnalisée, contactez votre équipe de compte d’Adobe.

## Étape 5 : Comparaison du nombre d’identifiants universels avec le nombre d’adresses électroniques hachées {#compare-id-count}

Une fois DSP les données du segment reçues, le nombre d’audiences doit être visible dans les neuf (9) heures.

Dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement), comparez le nombre d’identifiants universels au nombre d’adresses électroniques hachées d’origine. Pour plus d’informations sur les taux de traduction des ID acceptables et sur les raisons pour lesquelles les nombres de segments peuvent varier, voir &quot;[Écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances)&quot;.

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, voir &quot;[Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)&quot;.

Pour résoudre les problèmes liés à la procédure de conversion, contactez votre équipe de compte d’Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universels](source-manage.md)
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)
