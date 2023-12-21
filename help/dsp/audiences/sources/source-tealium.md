---
title: "Processus d’utilisation de l’intégration DSP avec [!DNL Tealium]"
description: "Découvrez comment activer DSP d’ingérer votre [!DNL Tealium] segments propriétaires."
feature: DSP Audiences
source-git-commit: e7c967d66be9c8ca78a64d644c7e3a691f1e216a
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Processus d’utilisation de l’intégration DSP avec [!DNL Tealium]

Vous pouvez partager les données propriétaires de votre entreprise à partir du [!DNL Tealium] plateforme de données client à l’aide de [!DNL Amazon Web Services] (AWS) connecteur de prise de feu. Il existe quatre étapes pour partager des données de Tealium avec DSP :

1. [Création d’une source d’audience dans DSP](#source-create).

1. [Préparation et partage des données de mappage de segments](#map-data).

1. [Création de connecteurs dans [!DNL Tealium] pour partager des données de segment](#tealium-connector).

1. [Dupliquer le connecteur existant dans [!DNL Tealium] continuer à partager des segments](#duplicate-connector).

## Étape 1 : création d’une source d’audience dans DSP {#source-create}

* [Création d’une source d’audience](source-create.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire, et partager la clé du code source avec le [!DNL Tealium] utilisateur.

## Étape 2 : Préparation et partage des données de mappage de segments {#map-data}

1. L’annonceur doit préparer et partager les données de mappage de segments :

   1. L’annonceur doit préparer les données dans [!DNL Tealium]:

      1. Les ID de courrier électronique de l’audience de l’annonceur doivent être hachés à l’aide de l’algorithme SHA-256.

      1. La colonne contenant des ID de courrier électronique haché doit être mappée à l’attribut du type d’identifiant visiteur.

      1. L’audience doit être créée avec la fonction `Tealium_visitor_id` attribut. L’enrichissement approprié doit être appliqué pour déclencher l’audience. Voir [[!DNL Tealium] documentation sur les attributs d’identifiant visiteur](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. L’annonceur doit fournir des données de mappage de segments à l’équipe du compte d’Adobe pour créer les segments dans DSP. Utilisez les noms et valeurs de colonne suivants dans un fichier de valeurs séparées par des virgules :

      * **Clé de segment externe :** Clé de segment externe que vous allez spécifier ultérieurement dans les paramètres d’action du connecteur dans [!DNL Tealium]. La convention de dénomination recommandée est &quot;`<DSP source key>_<Tealium segment name>`,&quot; par exemple &quot;57bf424dc10_coffee-drinkers&quot;.

      * **Nom du segment :** Nom du segment.

      * **Description du segment :** Objectif ou règle du segment, ou les deux.

      * **ID parent :** Conserver vide

      * **CPM vidéo :** 0

      * **Afficher CPM :** 0

      * **Fenêtre de segment :** Durée de vie du segment.

## Étape 3 : Création de connecteurs dans [!DNL Tealium] pour partager des données de segment {#tealium-connector}

Pour chaque segment que vous souhaitez partager, créez un connecteur distinct pour chaque action qui déclenche des modifications de données. Par exemple, pour partager deux segments comportant chacun deux déclencheurs, créez quatre connecteurs.

1. L’équipe du compte Adobe fournit à l’annonceur les informations d’identification du connecteur Firehose AWS.

1. Dans [!DNL Tealium], [ajouter un connecteur](https://docs.tealium.com/server-side/connectors/add/), à l’aide des options suivantes :

   1. Sélectionnez la variable [!DNL AWS Firehose] connecteur.

   1. Dans les paramètres source :

      1. Sélectionnez le segment d’audience à partager.

      1. Configurez un déclencheur :

         * Pour le premier connecteur du segment, sélectionnez le déclencheur. `Joined Audience`. Ainsi, les données sont partagées avec DSP chaque fois qu’un utilisateur rejoint un segment.

         * Pour le deuxième connecteur pour le segment, sélectionnez le déclencheur. `Left Audience`. Ce connecteur est utilisé pour gérer tous les utilisateurs et désinscriptions qui quittent le segment dans DSP.

   1. Dans les paramètres de configuration, spécifiez le connecteur AWS firehose. Si vous n’avez pas encore ajouté le connecteur firehose pour DSP, ajoutez un connecteur firehose à l’aide des informations suivantes :

      * **Nom :** Nom du connecteur.

      * **Clé d’accès :** Clé d’accès fournie par l’équipe du compte Adobe.

      * **Clé secrète :** Clé secrète fournie par l’équipe du compte d’Adobe.

      * **Région :** Virginie du Nord-Est des États-Unis (us-east-1)

   1. Dans les paramètres de l’action, procédez comme suit :

      1. Créez une action &quot;Envoyer les données client au flux de diffusion (avancé)&quot; pour ajouter des données au segment, à l’aide des informations suivantes :

         * **Nom de l’action :** Nom de l’action.

         * **Type d’action :** Envoi de données client au flux de diffusion (avancé)

         * **Diffusion :** Tealium_CDP_Connector

         * **Données du message :**  Procédez comme suit :

            1. Sélectionnez un attribut pour le segment :

               * Pour l’attribut Hashed_Email , nommez le message personnalisé. `hashed_email`.

               * Pour l’attribut Cookies , nommez le message personnalisé. `cookies`.

            1. Dans l’option de création d’un champ personnalisé, dans la variable [!DNL Source Key] , saisissez la valeur [!UICONTROL External Segment Key] qui a été inclus dans les données de mappage de segments dans [Étape 2](#map-data).

               DSP utilisera cette clé pour renseigner votre segment.

            1. (Recommandé) Créez une action de mise à jour pour actualiser le segment.

## Etape 4 : Dupliquer le connecteur existant dans [!DNL Tealium] continuer à partager des segments {#duplicate-connector}

Vous ne pouvez avoir qu’un seul connecteur par segment et un seul segment par connecteur.

1. Dans [!DNL Tealium], dupliquez le segment pour lequel vous souhaitez créer un autre segment et renommez-le.

1. Dans [!DNL Tealium], dupliquez le connecteur créé dans [Étape 3](#tealium-connector), puis renommez le nouveau connecteur à partir de &quot;`<original name>-copy`&quot; au nouveau nom du segment.

>[!MORELIKETHIS]
>
>* [À propos de l’activation de segments authentifiés à partir des sources d’audience](/help/dsp/audiences/sources/source-about.md)
>* [Création d’une source d’audience pour activer les audiences propriétaires](source-create.md)
>* [Paramètres de la source d’audience](source-settings.md)
>* [Processus d’utilisation de l’intégration DSP avec [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
