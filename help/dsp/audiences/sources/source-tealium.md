---
title: Convertir les ID utilisateur de  [!DNL Tealium]  en ID universels
description: Découvrez comment activer DSP pour ingérer vos segments  [!DNL Tealium] .
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: cff6b5ad2c66699a6e0402bce6685acc536fd0a0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL Tealium] en ID universels

*Fonction Beta*

Utilisez l’intégration de DSP à la plateforme de données clients [!DNL Tealium] pour convertir les adresses e-mail hachées propriétaires de votre organisation en identifiants universels pour la publicité ciblée. Le processus utilise le connecteur de tuyau d’incendie [!DNL Amazon Web Services] (AWS). Pour partager des données de Tealium avec DSP, procédez comme suit :

1. (Pour convertir des adresses e-mail en [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> ; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configurez le suivi pour activer [!DNL Analytics] mesurer](#analytics-tracking).

1. [Créer une source d’audience dans DSP](#source-create).

1. [Préparation et partage des données de mappage de segments](#map-data).

1. [Créez des connecteurs dans  [!DNL Tealium]  pour partager des données de segment](#tealium-connector).

1. [Dupliquez le connecteur existant dans  [!DNL Tealium]  pour continuer à partager des segments](#duplicate-connector).

1. [Comparez le nombre d’identifiants universels avec le nombre d’adresses e-mail hachées](#compare-id-count).

## Étape 1 : configurer le suivi pour la mesure des [!DNL Analytics] {#analytics-tracking}

*Annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Pour convertir des adresses e-mail en identifiants [!DNL RampIDs] ou [!DNL ID5], procédez comme suit :

1. (Si vous ne l’avez pas déjà fait) Renseignez tous les [prérequis pour l’implémentation [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et assurez-vous que les [AMO ID et EF ID](/help/integrations/analytics/ids.md) sont renseignés dans vos URL de tracking.

1. Enregistrez-vous auprès du partenaire d’ID universel et déployez du code spécifique à l’ID universel sur vos pages web pour faire correspondre les conversions des ID sur les navigateurs web de bureau et mobiles (mais pas sur les applications mobiles) aux affichages publicitaires :

   * **Par [!DNL RampIDs] :** vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants des navigateurs web de bureau et mobiles (mais pas des applications mobiles) aux affichages publicitaires. Contactez l’équipe chargée de votre compte Adobe qui vous donnera les instructions nécessaires pour vous inscrire à une balise [!DNL LiveRamp] [!DNL LaunchPad] auprès de [!DNL LiveRamp] solutions de trafic d’authentification. L&#39;inscription est gratuite, mais vous devez signer un contrat. Une fois enregistré, votre équipe de compte Adobe génère et fournit une balise unique que votre organisation peut implémenter sur vos pages web.

## Étape 2 : créer une source d’audience dans DSP {#source-create}

1. [Créez une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte d’annonceur. Vous pouvez choisir de convertir vos identifiants d’utilisateur vers l’un des [formats d’ID universels disponibles](source-about.md).

   Les paramètres source incluent une clé source générée automatiquement, que vous utiliserez pour préparer les données de mappage de segments.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec l’utilisateur [!DNL Tealium].

## Étape 3 : préparation et partage des données de mappage de segments {#map-data}

L’annonceur doit préparer et partager des données de mappage de segments.

1. L&#39;annonceur doit préparer les données dans les [!DNL Tealium] suivants :

   1. Hachez les identifiants d’e-mail pour l’audience de l’annonceur à l’aide de l’algorithme SHA-256.

   1. Mappez la colonne contenant les ID d’e-mail hachés sur l’attribut du type d’ID du visiteur.

   1. Créez l’audience avec l’attribut `Tealium_visitor_id` . Appliquez le bon enrichissement pour déclencher l’audience. Voir la [[!DNL Tealium] documentation sur les attributs d’identifiant visiteur](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. L’annonceur doit fournir des données de mappage de segments à l’équipe du compte Adobe pour créer les segments dans DSP. Utilisez les noms et valeurs de colonne suivants dans un fichier de valeurs séparées par des virgules :

   * **Clé de segment externe :** clé de segment externe, que vous spécifierez ultérieurement dans les paramètres d’action du connecteur dans [!DNL Tealium]. La convention de dénomination recommandée est « `<DSP source key>_<Tealium segment name>` », par exemple « 57bf424dc10_coffee-drinkers ». Pour la clé source DSP, utilisez l’[!UICONTROL Source Key] à partir des paramètres de la source de l’audience DSP.

   * **Nom du segment :** le nom du segment.

   * **Description du segment :** l’objectif ou la règle du segment, ou les deux.

   * **ID parent :** laisser vide

   * **Video CPM :** 0

   * **Afficher CPM:** 0

   * **Fenêtre de segment :** durée de vie du segment.

## Étape 4 : créer des connecteurs dans [!DNL Tealium] pour partager des données de segment {#tealium-connector}

Pour chaque segment que vous souhaitez partager, créez un connecteur distinct pour chaque action qui déclenche des modifications de données. Par exemple, pour partager deux segments qui possèdent chacun deux déclencheurs, créez quatre connecteurs.

1. L’équipe de compte Adobe fournit à l’annonceur les informations d’identification du connecteur du pare-feu AWS.

1. Dans [!DNL Tealium], [ajoutez un connecteur](https://docs.tealium.com/server-side/connectors/add/) à l’aide des options suivantes :

   1. Sélectionnez le connecteur [!DNL AWS Firehose].

   1. Dans les paramètres source :

      1. Sélectionnez le segment d’audience à partager.

      1. Configurez un déclencheur :

         * Pour le premier connecteur du segment, sélectionnez l’`Joined Audience` de déclenchement. Cela permet de s’assurer que les données sont partagées avec DSP chaque fois qu’un utilisateur rejoint un segment.

         * Pour le deuxième connecteur du segment, sélectionnez l’`Left Audience` de déclenchement. Ce connecteur est utilisé pour gérer tous les processus d’opt-out et les utilisateurs qui quittent le segment dans DSP.

   1. Dans les paramètres de configuration, spécifiez le connecteur de tuyau d’incendie AWS. Si vous n’avez pas encore ajouté le connecteur de flexible de feu pour DSP, ajoutez un connecteur de flexible de feu à l’aide des informations suivantes :

      * **Nom :** nom du connecteur.

      * **Clé d’accès :** clé d’accès fournie par l’équipe du compte Adobe.

      * **Clé secrète :** clé secrète fournie par l’équipe du compte Adobe.

      * **Région :** Virginie du Nord-Est des États-Unis (us-east-1)

   1. Dans les paramètres d’action, procédez comme suit :

      1. Créez une action « Envoyer les données client au flux de diffusion (avancé) » pour ajouter des données au segment, à l’aide des informations suivantes :

         * **Nom de l’action :** nom de l’action.

         * **Type d’action :** Envoyer les données client au flux de diffusion (avancé)

         * **Flux de diffusion :** Tealium_CDP_Connector

         * **Données du message :** procédez comme suit :

            1. Choisissez un attribut pour le segment :

               * Pour l’attribut Hashed_Email , attribuez un nom au `hashed_email` de message personnalisé.

               * Pour l’attribut Cookies , attribuez un nom au `cookies` de message personnalisé.

            1. Dans l’option de création d’un champ personnalisé, dans le champ [!DNL Source Key] , saisissez le [!UICONTROL External Segment Key] qui a été inclus dans le [données de mappage de segments](#map-data) dans la procédure précédente.

               DSP utilisera cette clé pour renseigner votre segment.

            1. (Recommandé) Créez une action de mise à jour pour conserver le segment à jour.

## Étape 5 : dupliquer le connecteur existant dans [!DNL Tealium] pour continuer à partager des segments {#duplicate-connector}

Vous ne pouvez avoir qu’un seul connecteur par segment et un seul segment par connecteur.

1. Dans [!DNL Tealium], dupliquez le segment pour lequel vous souhaitez créer un autre segment et renommez le nouveau segment.

1. Dans [!DNL Tealium], dupliquez [le connecteur que vous avez créé](#tealium-connector) dans la procédure précédente, et renommez le nouveau connecteur « `<original name>-copy` » en lui attribuant le nouveau nom de segment.

## Étape 6 : comparaison du nombre d’identifiants universels avec le nombre d’adresses e-mail hachées {#compare-id-count}

Les segments doivent être disponibles dans DSP dans les 24 heures. Une fois que DSP a reçu les données de segment, le nombre de profils des audiences doit être visible dans les neuf (9) heures.

Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est renseigné et comparez le nombre d’identifiants universels avec le nombre d’adresses e-mail hachées d’origine. Pour plus d’informations sur les taux de traduction des identifiants acceptables et sur les raisons pour lesquelles le nombre de segments peut varier, voir « [Variances des données entre les ID d’e-mail et les ID universels](#universal-ids-data-variances) ».

Les segments sont actualisés toutes les 24 heures. Cependant, l’inclusion dans un segment expire après 30 jours par défaut ou après une période d’expiration spécifiée par le client ou la cliente. Actualisez vos segments en les poussant à nouveau depuis [!DNL Tealium] avant l’expiration. Pour demander une expiration de segment personnalisé, contactez l’équipe chargée de votre compte Adobe.

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, consultez « [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md) ».

Pour résoudre les problèmes liés à la procédure de conversion, contactez l’équipe ou l’`adcloud-support@adobe.com` de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](source-manage.md)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
