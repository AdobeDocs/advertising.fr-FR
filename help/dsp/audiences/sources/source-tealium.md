---
title: Convertir les ID utilisateur de [!DNL Tealium]  en ID universels
description: Découvrez comment activer DSP d’ingérer vos segments propriétaires  [!DNL Tealium] .
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL Tealium] en ID universels

*Fonctionnalité Beta*

Utilisez l’intégration DSP à la plateforme de données client [!DNL Tealium] pour convertir les adresses électroniques hachées propriétaires de votre entreprise en identifiants universels pour la publicité ciblée. Le processus utilise le connecteur de prise en charge [!DNL Amazon Web Services] (AWS). Procédez comme suit pour partager des données de Tealium avec DSP :

1. (Pour convertir les adresses électroniques en [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> ; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [&#x200B; Configurez le suivi pour activer  [!DNL Analytics] la mesure](#analytics-tracking).

1. [Créez une source d’audience dans DSP](#source-create).

1. [Préparez et partagez des données de mappage de segments](#map-data).

1. [Créez des connecteurs dans  [!DNL Tealium]  pour partager les données de segment](#tealium-connector).

1. [Dupliquez le connecteur existant dans  [!DNL Tealium]  pour continuer à partager des segments](#duplicate-connector).

1. [Comparez le nombre d&#39;identifiants universels avec le nombre d&#39;adresses électroniques hachées](#compare-id-count).

## Étape 1 : configuration du suivi pour la mesure [!DNL Analytics] {#analytics-tracking}

*Annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Pour convertir les adresses électroniques en [!DNL RampIDs] ou [!DNL ID5] ID, procédez comme suit :

1. (Si vous ne l’avez pas déjà fait) Renseignez toutes les [conditions préalables à l’implémentation  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et assurez-vous que les [AMO ID et EF ID](/help/integrations/analytics/ids.md) sont renseignés dans vos URL de suivi.

1. Inscrivez-vous auprès du partenaire d’ID universel et déployez le code spécifique à l’ID universel sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs de bureau et les navigateurs web mobiles (mais pas les applications mobiles) aux affichages publicitaires :

   * **Pour [!DNL RampIDs] :** vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs web de bureau et mobiles (mais pas sur les applications mobiles) aux affichages publicitaires. Contactez votre équipe de compte d’Adobe, qui vous donnera des instructions pour vous inscrire à une balise [!DNL LiveRamp] [!DNL LaunchPad] des solutions de trafic d’authentification [!DNL LiveRamp]. L&#39;inscription est gratuite, mais vous devez signer un accord. Une fois que vous vous êtes enregistré, votre équipe de compte d’Adobe génère et fournit une balise unique que votre organisation doit implémenter sur vos pages web.

## Étape 2 : création d’une source d’audience dans DSP {#source-create}

1. [Créez une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire. Vous pouvez choisir de convertir vos identifiants d’utilisateur en l’un des [formats d’ID universels disponibles](source-about.md).

   Les paramètres de la source incluent une clé source générée automatiquement, que vous utiliserez pour préparer les données de mappage de segments.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec l’utilisateur [!DNL Tealium].

## Étape 3 : Préparation et partage des données de mappage de segments {#map-data}

L’annonceur doit préparer et partager les données de mappage de segments.

1. L’annonceur doit préparer les données dans [!DNL Tealium] :

   1. Hachez les ID d’email pour l’audience de l’annonceur à l’aide de l’algorithme SHA-256.

   1. Faites correspondre la colonne contenant des ID de courrier électronique haché à l’attribut du type d’identifiant visiteur.

   1. Créez l’audience avec l’attribut `Tealium_visitor_id` . Appliquez l’enrichissement approprié pour déclencher l’audience. Consultez la [[!DNL Tealium] documentation sur les attributs d’identifiant visiteur](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. L’annonceur doit fournir des données de mappage de segments à l’équipe du compte d’Adobe pour créer les segments dans DSP. Utilisez les noms et valeurs de colonne suivants dans un fichier de valeurs séparées par des virgules :

   * **Clé de segment externe :** clé de segment externe que vous préciserez ensuite dans les paramètres d’action du connecteur dans [!DNL Tealium]. La convention d’affectation de nom recommandée est &quot;`<DSP source key>_<Tealium segment name>`&quot;, par exemple &quot;57bf424dc10_coffee-drinkers&quot;. Pour la clé source DSP, utilisez les [!UICONTROL Source Key] des paramètres de source d’audience DSP.

   * **Nom du segment :** Nom du segment.

   * **Description du segment :** Objectif ou règle du segment, ou les deux.

   * **ID parent :** laissez vide

   * **CPM vidéo :** 0

   * **Afficher CPM :** 0

   * **Fenêtre de segment :** durée de vie du segment.

## Étape 4 : Création de connecteurs dans [!DNL Tealium] pour partager les données de segment {#tealium-connector}

Pour chaque segment que vous souhaitez partager, créez un connecteur distinct pour chaque action qui déclenche des modifications de données. Par exemple, pour partager deux segments comportant chacun deux déclencheurs, créez quatre connecteurs.

1. L’équipe du compte Adobe fournit à l’annonceur les informations d’identification du connecteur Firehose AWS.

1. Dans [!DNL Tealium], [ajoutez un connecteur](https://docs.tealium.com/server-side/connectors/add/), à l’aide des options suivantes :

   1. Sélectionnez le connecteur [!DNL AWS Firehose].

   1. Dans les paramètres source :

      1. Sélectionnez le segment d’audience à partager.

      1. Configurez un déclencheur :

         * Pour le premier connecteur du segment, sélectionnez le déclencheur `Joined Audience`. Ainsi, les données sont partagées avec DSP chaque fois qu’un utilisateur rejoint un segment.

         * Pour le deuxième connecteur pour le segment, sélectionnez le déclencheur `Left Audience`. Ce connecteur est utilisé pour gérer tous les utilisateurs et désinscriptions qui quittent le segment dans DSP.

   1. Dans les paramètres de configuration, spécifiez le connecteur AWS firehose. Si vous n’avez pas encore ajouté le connecteur firehose pour DSP, ajoutez un connecteur firehose à l’aide des informations suivantes :

      * **Nom :** Nom du connecteur.

      * **Clé d’accès :** clé d’accès fournie par l’équipe du compte Adobe.

      * **Clé secrète :** clé secrète fournie par l’équipe du compte Adobe.

      * **Région :** États-Unis Est de la Virginie du Nord (us-east-1)

   1. Dans les paramètres de l’action, procédez comme suit :

      1. Créez une action &quot;Envoyer les données client au flux de diffusion (avancé)&quot; pour ajouter des données au segment, à l’aide des informations suivantes :

         * **Nom de l’action :** Nom de l’action.

         * **Type d’action :** envoyer des données client au flux de diffusion (avancé)

         * **Diffusion :** Tealium_CDP_Connector

         * **Données du message :** Effectuez les opérations suivantes :

            1. Sélectionnez un attribut pour le segment :

               * Pour l’attribut Hashed_Email , nommez le message personnalisé `hashed_email`.

               * Pour l’attribut Cookies , nommez le message personnalisé `cookies`.

            1. Dans l’option de création d’un champ personnalisé, dans le champ [!DNL Source Key] , saisissez le [!UICONTROL External Segment Key] qui a été inclus dans les [&#x200B; données de mappage de segments](#map-data) de la procédure précédente.

               DSP utilisera cette clé pour renseigner votre segment.

            1. (Recommandé) Créez une action de mise à jour pour actualiser le segment.

## Étape 5 : dupliquer le connecteur existant dans [!DNL Tealium] pour continuer à partager des segments {#duplicate-connector}

Vous ne pouvez avoir qu’un seul connecteur par segment et un seul segment par connecteur.

1. Dans [!DNL Tealium], dupliquez le segment pour lequel vous souhaitez créer un autre segment, puis renommez le nouveau segment.

1. Dans [!DNL Tealium], dupliquez [&#x200B; le connecteur que vous avez créé](#tealium-connector) lors de la procédure précédente et renommez le nouveau connecteur de &quot;`<original name>-copy`&quot; en un nouveau nom de segment.

## Étape 6 : Comparaison du nombre d’identifiants universels avec le nombre d’adresses électroniques hachées {#compare-id-count}

Les segments doivent être disponibles dans DSP dans les 24 heures. Une fois DSP les données du segment reçues, le nombre d’audiences doit être visible dans les neuf (9) heures.

Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est renseigné et comparez le nombre d’identifiants universels au nombre d’adresses électroniques hachées d’origine. Pour plus d’informations sur les taux de traduction des ID acceptables et sur les raisons pour lesquelles les nombres de segments peuvent varier, voir &quot;[Écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances)&quot;.

Les segments sont actualisés toutes les 24 heures. Cependant, l’inclusion dans un segment expire après 30 jours par défaut ou après une période d’expiration spécifiée par le client. Actualisez vos segments en les republiant depuis [!DNL Tealium] avant l’expiration. Pour demander une expiration de segment personnalisée, contactez votre équipe de compte d’Adobe.

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, voir &quot;[Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)&quot;.

Pour résoudre les problèmes liés à la procédure de conversion, contactez votre équipe de compte d’Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universels](source-manage.md)
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)
