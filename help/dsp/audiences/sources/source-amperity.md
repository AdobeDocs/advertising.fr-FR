---
title: Convertir les ID utilisateur à partir de [!DNL Amperity] vers des ID universels
description: Découvrez comment activer DSP d’ingérer votre [!DNL Amperity] segments propriétaires.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Convertir les ID utilisateur à partir de [!DNL Amperity] vers des ID universels

*Fonctionnalité Beta*

Utilisez l’intégration DSP avec la [!DNL Amperity] plateforme de données client pour convertir les adresses électroniques hachées propriétaires de votre entreprise en identifiants universels pour la publicité ciblée.

1. (Pour convertir des adresses électroniques en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configuration du suivi à activer [!DNL Analytics] mesure](#analytics-tracking).

1. [Création d’une source d’audience dans DSP](#source-create).

1. [Préparation et partage des données de mappage de segments](#map-data).

1. [Demander une transmission de données depuis [!DNL Amperity] à DSP](#push-data).

1. [Comparer le nombre d’identifiants universels au nombre d’adresses électroniques hachées](#compare-id-count).

## Étape 1 : configuration du suivi pour [!DNL Analytics] mesure {#analytics-tracking}

*Annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Pour convertir des adresses électroniques en [!DNL RampIDs] ou [!DNL ID5] ID, vous devez effectuer les opérations suivantes :

1. (Si vous ne l’avez pas déjà fait) Complétez tous les [conditions préalables à la mise en oeuvre [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et assurez-vous que la variable [AMO ID et EF ID](/help/integrations/analytics/ids.md) sont renseignées dans vos URL de suivi.

1. Inscrivez-vous auprès du partenaire d’ID universel et déployez le code spécifique à l’ID universel sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs de bureau et les navigateurs web mobiles (mais pas les applications mobiles) aux affichages publicitaires :

   * **Pour [!DNL RampIDs]:** Vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs de bureau et les navigateurs web mobiles (mais pas les applications mobiles) aux affichages publicitaires. Contactez votre équipe de compte d’Adobe, qui vous donnera des instructions pour vous inscrire à une [!DNL LiveRamp] [!DNL LaunchPad] de [!DNL LiveRamp] Solutions de trafic d’authentification. L&#39;inscription est gratuite, mais vous devez signer un accord. Une fois que vous vous êtes enregistré, votre équipe de compte d’Adobe génère et fournit une balise unique que votre organisation doit implémenter sur vos pages web.

## Étape 2 : création d’une source d’audience dans DSP {#source-create}

1. [Création d’une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire. Vous pouvez choisir de convertir vos identifiants d’utilisateur en l’un des [formats d’ID universels disponibles](source-about.md).

   Les paramètres de la source comprennent une clé source générée automatiquement que vous utiliserez pour transmettre les données du segment.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec la variable [!DNL Amperity] utilisateur.

## Étape 3 : Préparation et partage des données de mappage de segments {#map-data}

L’annonceur doit préparer et partager les données de mappage de segments.

1. Within [!DNL Amperity], hachez les ID d’email pour l’audience à l’aide de l’algorithme SHA-256.

1. L’annonceur doit fournir des données de mappage de segments à l’équipe du compte d’Adobe pour créer les segments dans DSP. Utilisez les noms et valeurs de colonne suivants dans un fichier de valeurs séparées par des virgules :

   * **Clé de segment externe :** La variable [!DNL Amperity] clé de segment associée au segment.

   * **Nom du segment :** Nom du segment.

   * **Description du segment :** Objectif ou règle du segment, ou les deux.

   * **ID parent :** Conserver vide

   * **CPM vidéo :** 0

   * **Afficher CPM :** 0

   * **Fenêtre de segment :** Durée de vie du segment.

## Étape 4 : demander une transmission de données [!DNL Amperity] à DSP {#push-data}

1. Une fois que le segment est mappé dans DSP, l’annonceur doit travailler avec ses [!DNL Amperity] représentant pour distribuer les données de segment à DSP.

1. L’annonceur doit ensuite confirmer auprès de l’équipe du compte d’Adobe que les données de segment ont été reçues.

Les segments doivent être disponibles dans DSP dans les 24 heures. Vérifier dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est disponible et est renseigné.

Les segments seront actualisés comme configurés pour l’annonceur dans [!DNL Amperity]. Quelle que soit la fréquence d’actualisation du segment, l’inclusion dans un segment expire par défaut après 30 jours ou après une période d’expiration spécifiée par le client. Actualisez vos segments en les repoussant depuis [!DNL Amperity] avant l’expiration. Pour demander une expiration de segment personnalisée, contactez votre équipe de compte d’Adobe.

## Étape 5 : Comparaison du nombre d’identifiants universels avec le nombre d’adresses électroniques hachées {#compare-id-count}

Une fois DSP les données du segment reçues, le nombre d’audiences doit être visible dans les neuf (9) heures.

Dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) comparez le nombre d’identifiants universels au nombre d’adresses électroniques hachées d’origine. Pour plus d’informations sur les taux de traduction des identifiants acceptables et sur les raisons pour lesquelles les nombres de segments peuvent varier, voir &quot;[Écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances).&quot;

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, voir &quot;[Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md).&quot;

Pour résoudre les problèmes liés à la procédure de conversion, contactez votre équipe de compte Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gestion des sources d’audience pour activer les audiences d’ID universelles](source-manage.md)
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
