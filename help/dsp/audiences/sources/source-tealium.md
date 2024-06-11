---
title: Convertir les ID utilisateur à partir de [!DNL Tealium] vers des ID universels
description: Découvrez comment activer DSP d’ingérer votre [!DNL Tealium] segments propriétaires.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 096ca9b5fce101995ca620b78f2ad8abf40355cd
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# Convertir les ID utilisateur à partir de [!DNL Tealium] vers des ID universels

*Fonction bêta*

Utilisez l’intégration DSP avec la [!DNL Tealium] plateforme de données client pour convertir les adresses électroniques hachées propriétaires de votre entreprise en identifiants universels pour la publicité ciblée. Le processus utilise la variable [!DNL Amazon Web Services] (AWS) connecteur de prise de feu. Procédez comme suit pour partager des données de Tealium avec DSP :

1. (Pour convertir des adresses électroniques en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configuration du suivi à activer [!DNL Analytics] mesure](#analytics-tracking).

1. [Création d’une source d’audience dans DSP](#source-create).

1. [Préparation et partage des données de mappage de segments](#map-data).

1. [Création de connecteurs dans [!DNL Tealium] pour partager des données de segment](#tealium-connector).

1. [Dupliquer le connecteur existant dans [!DNL Tealium] continuer à partager des segments](#duplicate-connector).

1. [Comparer le nombre d’identifiants universels au nombre d’adresses électroniques hachées](#compare-id-count).

Les segments doivent être disponibles en DSP dans les 24 heures et être actualisés toutes les 24 heures.

## Étape 1 : configuration du suivi pour [!DNL Analytics] mesure {#analytics-tracking}

*Annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Pour convertir des adresses électroniques en [!DNL RampIDs] ou [!DNL ID5] ID, vous devez effectuer les opérations suivantes :

1. (Si vous ne l’avez pas déjà fait) Complétez tous les [conditions préalables à la mise en oeuvre [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et assurez-vous que la variable [AMO ID et EF ID](/help/integrations/analytics/ids.md) sont renseignées dans vos URL de suivi.

1. Inscrivez-vous auprès du partenaire d’ID universel et déployez le code spécifique à l’ID universel sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs de bureau et les navigateurs web mobiles (mais pas les applications mobiles) aux affichages publicitaires :

   * **Pour [!DNL RampIDs]:** Vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants des navigateurs de bureau et web mobile (mais pas les applications mobiles) aux affichages publicitaires. Contactez votre équipe de compte d’Adobe, qui vous donnera des instructions pour vous inscrire à une [!DNL LiveRamp] [!DNL LaunchPad] de [!DNL LiveRamp] Solutions de trafic d’authentification. L&#39;inscription est gratuite, mais vous devez signer un accord. Une fois que vous vous êtes enregistré, votre équipe de compte d’Adobe génère et fournit une balise unique que votre organisation doit implémenter sur vos pages web.

## Étape 2 : création d’une source d’audience dans DSP {#source-create}

1. [Création d’une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire. Vous pouvez choisir de convertir vos identifiants d’utilisateur en l’un des [formats d’ID universels disponibles](source-about.md).

   Les paramètres de la source incluent une clé source générée automatiquement, que vous utiliserez pour préparer les données de mappage de segments.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec la variable [!DNL Tealium] utilisateur.

## Étape 3 : Préparation et partage des données de mappage de segments {#map-data}

L’annonceur doit préparer et partager les données de mappage de segments.

1. L’annonceur doit préparer les données dans [!DNL Tealium]:

   1. Hachez les ID d’email pour l’audience de l’annonceur à l’aide de l’algorithme SHA-256.

   1. Faites correspondre la colonne contenant des ID de courrier électronique haché à l’attribut du type d’identifiant visiteur.

   1. Créez l’audience avec la fonction `Tealium_visitor_id` attribut. Appliquez l’enrichissement approprié pour déclencher l’audience. Voir [[!DNL Tealium] documentation sur les attributs d’identifiant visiteur](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. L’annonceur doit fournir des données de mappage de segments à l’équipe du compte d’Adobe pour créer les segments dans DSP. Utilisez les noms et valeurs de colonne suivants dans un fichier de valeurs séparées par des virgules :

   * **Clé de segment externe :** Clé de segment externe que vous allez spécifier ultérieurement dans les paramètres d’action du connecteur dans [!DNL Tealium]. La convention de dénomination recommandée est &quot;`<DSP source key>_<Tealium segment name>`,&quot; par exemple &quot;57bf424dc10_coffee-drinkers&quot;. Pour la clé source DSP, utilisez le [!UICONTROL Source Key] dans les paramètres de source d’audience DSP.

   * **Nom du segment :** Nom du segment.

   * **Description du segment :** Objectif ou règle du segment, ou les deux.

   * **ID parent :** Conserver vide

   * **CPM vidéo :** 0

   * **Afficher CPM :** 0

   * **Fenêtre de segment :** Durée de vie du segment.

## Étape 4 : Création de connecteurs dans [!DNL Tealium] pour partager des données de segment {#tealium-connector}

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

            1. Dans l’option de création d’un champ personnalisé, dans la variable [!DNL Source Key] , saisissez la valeur [!UICONTROL External Segment Key] qui était inclus dans la variable [données de mappage de segments](#map-data) lors de la procédure précédente.

               DSP utilisera cette clé pour renseigner votre segment.

            1. (Recommandé) Créez une action de mise à jour pour actualiser le segment.

## Etape 5 : Dupliquer le connecteur existant dans [!DNL Tealium] continuer à partager des segments {#duplicate-connector}

Vous ne pouvez avoir qu’un seul connecteur par segment et un seul segment par connecteur.

1. Dans [!DNL Tealium], dupliquez le segment pour lequel vous souhaitez créer un autre segment et renommez-le.

1. Dans [!DNL Tealium], dupliquer [le connecteur que vous avez créé](#tealium-connector) lors de la procédure précédente, et renommez le nouveau connecteur à partir de &quot;`<original name>-copy`&quot; au nouveau nom du segment.

## Étape 6 : Comparaison du nombre d’identifiants universels avec le nombre d’adresses électroniques hachées {#compare-id-count}

Une fois toutes les étapes terminées, vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est renseigné dans les 24 heures. Comparez le nombre d’identifiants universels au nombre d’adresses électroniques hachées d’origine.

Le taux de traduction des adresses électroniques hachées en identifiants universels doit être supérieur à 90 %. Par exemple, si vous envoyez 100 adresses électroniques hachées à partir de votre plateforme de données client, elles doivent être traduites en plus de 90 identifiants universels. Un taux de traduction de 90 % ou moins est un problème. Pour plus d’informations sur la manière dont les décomptes de segments peuvent varier, voir &quot;[Causes des écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances).&quot;

Les segments sont actualisés toutes les 24 heures. Cependant, l’inclusion dans un segment expire après 30 jours pour garantir la conformité à la confidentialité. Par conséquent, actualisez les audiences en les repoussant de [!DNL Tealium] tous les 30 jours ou moins.

Pour obtenir une assistance en matière de dépannage, contactez votre équipe de compte d’Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gestion des sources d’audience pour activer les audiences d’ID universelles](source-manage.md)
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
