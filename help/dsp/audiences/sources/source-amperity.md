---
title: Convertir les ID utilisateur à partir de [!DNL Amperity] vers des ID universels
description: Découvrez comment activer DSP d’ingérer votre [!DNL Amperity] segments propriétaires.
feature: DSP Audiences
source-git-commit: dab24efea38951373ec1ada571b10d9843409baf
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Convertir les ID utilisateur à partir de [!DNL Amperity] vers des ID universels

*Fonction bêta*

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

   * **Pour [!DNL RampIDs]:** Vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants des navigateurs de bureau et web mobile (mais pas les applications mobiles) aux affichages publicitaires. Contactez votre équipe de compte d’Adobe, qui vous donnera des instructions pour vous inscrire à une [!DNL LiveRamp] [!DNL LaunchPad] de [!DNL LiveRamp] Solutions de trafic d’authentification. L&#39;inscription est gratuite, mais vous devez signer un accord. Une fois que vous vous êtes enregistré, votre équipe de compte d’Adobe génère et fournit une balise unique que votre organisation doit implémenter sur vos pages web.

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

Les segments doivent être disponibles dans DSP dans les 24 heures et sont actualisés comme configurés pour l’annonceur. Quelle que soit la fréquence d’actualisation du segment, l’inclusion dans un segment expire au bout de 30 jours pour garantir la conformité à la confidentialité. Dès lors, actualisez les audiences en les repoussant de [!DNL Amperity] tous les 30 jours ou moins.

## Étape 5 : Comparaison du nombre d’identifiants universels avec le nombre d’adresses électroniques hachées {#compare-id-count}

Une fois toutes les étapes terminées, vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est disponible et qu’il est renseigné dans les 24 heures. Comparez le nombre d’identifiants universels au nombre d’adresses électroniques hachées d’origine.

Le taux de traduction des adresses électroniques hachées en identifiants universels doit être supérieur à 90 %. Par exemple, si vous envoyez 100 adresses électroniques hachées à partir de votre plateforme de données client, elles doivent être traduites en plus de 90 identifiants universels. Un taux de traduction de 90 % ou moins est un problème. Pour plus d’informations sur la manière dont les décomptes de segments peuvent varier, voir &quot;[Causes des écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances).&quot;

Pour obtenir une assistance en matière de dépannage, contactez votre équipe de compte d’Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gestion des sources d’audience pour activer les audiences d’ID universelles](source-manage.md)
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
