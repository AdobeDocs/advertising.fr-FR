---
title: Dépannage des données Adobe Advertising dans Customer Journey Analytics
description: Découvrez comment résoudre les problèmes liés aux données Adobe Advertising dans Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 21280b9826b60e69d9f4829062db1b140aba5c88
workflow-type: tm+mt
source-wordcount: 3204
ht-degree: 0%

---

# Dépannage des données Adobe Advertising dans Customer Journey Analytics

Vous trouverez ci-dessous des problèmes potentiels, leurs causes possibles et des solutions.

## Liste de tous les symptômes potentiels

| Problème | Plus d’informations |
| ------- | ---------------- |
| Aucun appel alloy() n’est visible dans l’onglet de réseau du navigateur | Consultez la section « [Problèmes d’installation et de configuration](#issues-installation-setup) » > « [L’extension WebSDK ne s’initialise pas](#websdk-extension-doesn't-initialize) » |
| Erreur de console : l’alliage n’est pas défini | Voir « [Problèmes d’installation et de configuration](#issues-installation-setup) » > « [L’extension WebSDK ne s’initialise pas](#websdk-extension-doesn't-initialize) » |
| Aucune interaction ou requête de collecte vers edge.adobedc.net | Voir « [Problèmes d’installation et de configuration](#issues-installation-setup) » > « [L’extension WebSDK ne s’initialise pas](#websdk-extension-doesn't-initialize) » |
| Les requêtes atteignent l’edge mais renvoient des erreurs 400 ou 500 | Consultez la section « [&#x200B; Problèmes d’installation et de configuration &#x200B;](#issues-installation-setup) » > « [Flux de données non configuré ou mal configuré](#datastream-not-configured-or-misconfigured) » |
| Aucune donnée n’apparaît dans les rapports Adobe Analytics ou Adobe Advertising | Consultez la section « [&#x200B; Problèmes d’installation et de configuration &#x200B;](#issues-installation-setup) » > « [Flux de données non configuré ou mal configuré](#datastream-not-configured-or-misconfigured) » |
| Erreur dans la réponse réseau : « flux de données introuvable » | Consultez la section « [&#x200B; Problèmes d’installation et de configuration &#x200B;](#issues-installation-setup) » > « [Flux de données non configuré ou mal configuré](#datastream-not-configured-or-misconfigured) » |
| Aucune conversion d’affichage publicitaire ou de clic publicitaire n’est enregistrée pour la page web | Voir la section « [Problèmes de configuration de l’extension Advertising &#x200B;](#advertising-extension-setup-issues) » |
| `_experience.adcloud` est absent de la payload du modèle de données d’expérience (XDM) pour les clics publicitaires | Voir la section « [Problèmes de configuration de l’extension Advertising &#x200B;](#advertising-extension-setup-issues) » |
| Les conversions sont confirmées dans un outil de débogage, mais n’apparaissent pas dans les rapports Adobe Advertising | Voir la section « [Problèmes de configuration de l’extension Advertising &#x200B;](#advertising-extension-setup-issues) » |
| L’identifiant visiteur change entre les pages | Consultez la section « [Problèmes d’identité et d’ECID](#identity-and-ecid-issues) » |
| Les segments d’audience Advertising ne correspondent pas. | Consultez la section « [Problèmes d’identité et d’ECID](#identity-and-ecid-issues) » |
| Le débogueur indique que les conditions de la règle ne sont pas remplies | Consultez la section « [&#x200B; Les règles ou les événements ne se déclenchent pas &#x200B;](#rules-or-events-aren't-firing) » |
| L’action [!UICONTROL Send Event] ne s’exécute jamais | Consultez la section « [&#x200B; Les règles ou les événements ne se déclenchent pas &#x200B;](#rules-or-events-aren't-firing) » |
| Les modifications apportées dans [!DNL Tags] ne sont pas répercutées sur le site actif | Consultez la section « [Problèmes de création et de publication de bibliothèque](#library-build-and-publishing-issues) » |
| Une mise à jour d’extension a été appliquée, mais l’ancien comportement persiste | Consultez la section « [Problèmes de création et de publication de bibliothèque](#library-build-and-publishing-issues) » |
| L’appel de l’événement d’envoi `alloy()` réussit (avec une réponse 200), mais les données de conversion Adobe Advertising sont absentes des rapports | Consultez la section « [Problèmes de validation des schémas pour les champs Advertising](#schema-validation-for-advertising-fields) » |
| La payload XDM du débogueur n’affiche aucun objet `_experience.adcloud` | Consultez la section « [Problèmes de validation des schémas pour les champs Advertising](#schema-validation-for-advertising-fields) » |
| Aucune donnée de rapport de synthèse n’est disponible dans Customer Journey Analytics pour Advertising DSP ou Advertising Search, Social et Commerce. | Voir la section « [Problèmes de reporting](#reporting-issues) » > « [Rapports de synthèse](#summary-reporting) » |
| Les données de rapports récapitulatives sont disponibles dans Customer Journey Analytics pour l’annonceur 1, mais pas pour l’annonceur 2. | Voir la section « [Problèmes de reporting](#reporting-issues) » > « [Rapports de synthèse](#summary-reporting) » |
| (Utilisateurs Search, Social et Commerce) Les données de rapports de synthèse sont disponibles dans Customer Journey Analytics pour un compte [!DNL Google Ads], [!DNL Meta Ads] ou [!DNL Microsoft Advertising], mais pas pour un autre compte. | Voir la section « [Problèmes de reporting](#reporting-issues) » > « [Rapports de synthèse](#summary-reporting) » |
| Les données de rapports de synthèse dans Customer Journey Analytics Workspace sont différentes de celles d’Advertising DSP ou d’Advertising Search, Social et Commerce, ou les données de synthèse sont manquantes pour certaines campagnes et entités de campagne. | Voir la section « [Problèmes de reporting](#reporting-issues) » > « [Rapports de synthèse](#summary-reporting) » |
| Les données de conversion (telles que `Page Views`) ne sont pas disponibles pour une dimension de rapport (telle que `Campaign`) dans CJA Customer Journey Analytics Workspace. | Voir la section « [Problèmes de reporting](#reporting-issues) » > « [Rapports au niveau des événements](#event-level-reporting) » |

## Problèmes d’installation et de configuration {#issues-installation-setup}

### L’extension WebSDK n’initialise pas {#websdk-extension-doesn’t-initialize}

#### Événements :

* Aucun appel alloy() n’est visible dans l’onglet de réseau du navigateur
* Erreur de console : l’alliage n’est pas défini
* Aucune interaction ou requête de collecte vers edge.adobedc.net

#### Causes possibles et vérification/résolution

+++ Bibliothèque non publiée ou à l’état de brouillon

Accédez à [Flux de publication](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) et assurez-vous que la bibliothèque contenant l’extension WebSDK est à l’état approuvé/publié.

+++

+++ Environnement manquant ou incorrect du code incorporé

Vérifiez que le code incorporé [!DNL Tags] sur la page web référence l’environnement approprié (Dev/Stage/Prod). Recherchez l’environnement dans la balise `<head>` pour la balise de script `//assets.adobedtm.com/...`.

+++

+++ Conflit de charge asynchrone et synchrone

Assurez-vous qu’un seul code incorporé [!DNL Tags] est présent par page web. Les codes incorporés en double entraînent des conditions de concurrence.

+++

+++ Blocage de la politique de sécurité du contenu (CSP)

Ajoutez des `edge.adobedc.net` et des `assets.adobedtm.com` à vos `connect-src` CSP et directives `script-src`.

+++

### Flux de données non configuré ou mal configuré {#datastream-not-configured-or-misconfigured}

#### Événements :

* Les requêtes atteignent l’edge mais renvoient des erreurs 400 ou 500
* Aucune donnée n’apparaît dans les rapports Adobe Analytics ou Adobe Advertising<!-- It's not useful to organize this info by cause, not symptom -->
* Erreur dans la réponse réseau : « flux de données introuvable »

#### Causes possibles et vérification/résolution

+++ L’identifiant du flux de données de la propriété de balise est manquant ou incorrect

1. Dans [!DNL Tags], ouvrez les [paramètres de configuration du flux de données](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) de votre propriété de balise.
1. Vérifiez que le champ [!UICONTROL Datastream] pointe vers le flux de données correct pour chaque environnement (développement, évaluation et production), ainsi que vers le schéma et le jeu de données corrects.

   Chaque environnement doit avoir son propre flux de données, sauf si vous partagez explicitement un flux de données entre les trois environnements.

+++

+++ Les services de flux de données ne sont pas activés pour la propriété de balise.

[Ouvrez les paramètres du flux de données](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) et assurez-vous que les services suivants sont activés :

* Adobe Advertising (pour la conversion/synchronisation de l’audience)
* Adobe Experience Platform (pour l’ingestion de profils)

+++

+++ Incompatibilité de sandbox

Assurez-vous que le flux de données appartient au même sandbox Adobe Experience Platform que votre schéma et votre jeu de données. Une erreur courante est de créer un flux de données dans le sandbox de production, mais de pointer les schémas vers le sandbox de développement.

+++

### Problèmes de configuration de l’extension [!UICONTROL Advertising] {#advertising-extension-setup-issues}

#### Événements :

* Aucune conversion d’affichage publicitaire ou de clic publicitaire n’est enregistrée pour la page web.

  Pour vérifier si les conversions sont enregistrées :

  1. Ouvrez la page web avec des `ef_id=test&s_kwcid=test` ajoutées à l’URL.
  1. Ouvrez l’outil d’inspection du code de votre navigateur (souvent appelé [!DNL Inspect]), ouvrez l’onglet [!DNL Network] et recherchez un appel d’interaction pour event_type=« advertising.enrichment_ct » de Adobe Experience Platform.
  1. Dans l’interface de collecte de données, [ouvrez la définition du schéma](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) pour les données du site web que vous souhaitez collecter et confirmez que `xdm->_experience->adcloud->conversionDetails->trackingCode` et `trackingIdentities` contiennent des `ef_id` et des `s_kwcid`.

* `_experience.adcloud` est absent de la payload du modèle de données d’expérience (XDM) pour les clics publicitaires.

* Les conversions sont confirmées dans un outil de débogage, mais n’apparaissent pas dans les rapports Adobe Advertising

#### Causes possibles et vérification/résolution

+++ Le service `Adobe Advertising` n’est pas activé pour le flux de données

1. Dans [!DNL Tags], ouvrez les [paramètres de configuration du flux de données](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) de votre propriété de balise.
1. Activez les services suivants et enregistrez les paramètres :
   * Adobe Advertising (pour la conversion/synchronisation de l’audience)
   * Adobe Experience Platform (pour l’ingestion de profils)

+++

+++ Le composant `Adobe Advertising` n’est pas activé pour l’extension [!UICONTROL WebSDK]

Le composant `Adobe Advertising` de l’extension WebSDK est désactivé par défaut et doit être explicitement activé avant que le suivi des clics publicitaires ou des affichages publicitaires Adobe Advertising ne soit fonctionnel, quelle que soit la configuration du schéma ou des règles XDM.

1. Dans [!DNL Tags], ouvrez les [options de build de la propriété dans les paramètres de configuration de Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components).
1. Activez le composant **&#x200B;**&#x200B;et enregistrez les paramètres.
1. Recréez et republiez la bibliothèque.

+++

+++ Seules les conversions par clic publicitaire sont enregistrées ; les conversions par affichage publicitaire n’apparaissent jamais

Il s’agit du comportement par défaut attendu. Une fois le composant `Adobe Advertising` activé, le suivi des clics publicitaires est automatiquement activé à l’aide des paramètres de requête d’URL `s_kwcid` et `ef_id`. Le suivi des affichages publicitaires est désactivé par défaut et nécessite une configuration supplémentaire (voir l’élément suivant).

+++

+++ Le suivi des affichages publicitaires n’est ni activé ni configuré

1. Activez le service Adobe Advertising pour le flux de données :
   1. Accédez à [!UICONTROL Data Collection] > [!UICONTROL Datastreams] dans Adobe Experience Platform et ouvrez le flux de données utilisé par votre propriété [!DNL Tags].
   1. Sélectionnez **Ajouter un service**, **Adobe Advertising** et **Adobe Experience Platform**, puis sélectionnez **Enregistrer**.
1. Configurez les annonceurs dans Adobe Advertising DSP :
   1. Dans [!DNL Tags], accédez à [!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure].
   1. Dans la section [!UICONTROL Advertiser] , sélectionnez un annonceur dans la liste déroulante et activez-le. Pour configurer plusieurs annonceurs, sélectionnez **Ajouter un annonceur**.
1. Vérifiez que les pixels de conversion de visionneuse se déclenchent :
   1. Dans [!DNL Adobe Experience Platform] Debugger, vérifiez que l’appel d’interaction inclut des `stitchId` sous le champ `xdm.query` .
   1. Vérifiez dans l’onglet de [!UICONTROL Network] du navigateur qu’un événement de type `advertising.enrichment` est déclenché et inclut des `stitchId` sous `xdm.query`.

Les conversions d’affichage publicitaire ne se déclenchent que toutes les 30 minutes, quel que soit le nombre de visites. Si aucun appel d’interaction ne s’affiche, effacez la mémoire cache du navigateur et réessayez.

+++

+++ (Si aucun événement de visionnage publicitaire dans Experience Platform après le déclenchement de l’appel d’interaction Viewthrough) L’annonceur a été saisi manuellement au lieu d’être sélectionné dans la liste déroulante

Sélectionnez à nouveau l’annonceur dans la liste déroulante [!UICONTROL Advertiser] au lieu de le saisir manuellement.

+++

+++ (Si aucun événement d’affichage publicitaire dans Experience Platform après le déclenchement de l’appel d’interaction Viewthrough) Aucun identifiant publicitaire n’est envoyé avec l’appel d’interaction d’affichage publicitaire

Vérifiez qu’un annonceur est configuré et activé dans la section [!UICONTROL Advertiser] de la configuration de l’extension WebSDK, puis recréez et republiez la bibliothèque.

+++

Avant d’ouvrir un ticket d’assistance pour [!UICONTROL Advertising] problèmes de configuration de l’extension, vérifiez les points suivants :

* Les services **&#x200B;**&#x200B;et **Adobe Experience Platform** sont ajoutés au flux de données.
* Le composant **&#x200B;**&#x200B;est activé dans la configuration de l’extension WebSDK.
* La bibliothèque a été reconstruite et republiée après l’activation du composant.
* Pour le suivi des clics publicitaires, l’URL de la page de destination contient les `s_kwcid` et les `ef_id` sur les clics publicitaires.
* Pour le suivi d’affichage publicitaire, un annonceur est configuré dans Adobe Advertising DSP avec l’ID d’annonceur approprié.
* L’extension WebSDK est de la version 2.36.0 ou ultérieure.

## Problèmes d’identité et d’ECID {#identity-and-ecid-issues}

### Événements :

* L’identifiant visiteur change entre les pages
* Les segments d’audience Advertising ne correspondent pas.

### Causes possibles et vérification/résolution

+++ Les cookies tiers sont bloqués

Migrez vers la collecte de données CNAME propriétaire en configurant un domaine propriétaire dans la configuration Edge du flux de données.

+++

+++ `idMigrationEnabled` est défini sur `false` tant qu’un cookie de `s_ecid` hérité est présent

Définissez `idMigrationEnabled: true` dans la configuration de base du SDK Web pour migrer l’ECID existant à partir des cookies `s_ecid` ou `AMCV_`.

+++

### Les règles ou les événements ne se déclenchent pas #rules-or-events-aren’ont pas-déclenché

#### Événements :

* Le débogueur indique que les conditions de la règle ne sont pas remplies
* L’action [!UICONTROL Send Event] ne s’exécute jamais

#### Vérification et résolution

+++ Vérifiez les points suivants :

* La règle est enregistrée et incluse dans la version de bibliothèque principale.
* Le type d’événement correspond au comportement réel de la page (par exemple, [!UICONTROL Library Loaded] ou [!UICONTROL DOM Ready] ou [!UICONTROL Window Loaded]).
* Les conditions de la règle ne sont pas trop restrictives. Testez en supprimant temporairement les conditions pour isoler le problème.
* L’ordre des règles est correct. Si plusieurs règles partagent le même événement, vérifiez l’ordre des règles.
* Aucune erreur JavaScript antérieure sur la page n’interrompt l’exécution. Recherchez des exceptions non interceptées dans la console du navigateur.

+++

### Problèmes de création et de publication de bibliothèque {#library-build-and-publishing-issues}

#### Événements :

* Les modifications apportées dans [!DNL Tags] ne sont pas répercutées sur le site actif
* Une mise à jour d’extension a été appliquée, mais l’ancien comportement persiste

#### Causes possibles et vérification/résolution

+++ Les modifications n’ont pas été ajoutées à une bibliothèque

Dans [!UICONTROL Publishing Flow], vérifiez que vos modifications ont été ajoutées à une bibliothèque dans l’environnement de développement. Accédez à [!UICONTROL Libraries], ouvrez la bibliothèque de travail, sélectionnez **Ajouter toutes les ressources modifiées** puis sélectionnez **Enregistrer et créer**.

+++

+++ Le navigateur met en cache une ancienne bibliothèque

Effectuez une actualisation complète (Ctrl + Maj + R ou Cmd + Maj + R) ou ouvrez la page dans une fenêtre privée ou en mode privé. Effacez entièrement la mémoire cache du navigateur si le problème persiste.

+++

+++ Le code incorporé est destiné à un environnement incorrect

Vérifiez que le code incorporé sur la page est le code incorporé de production si vous testez le comportement en production.

+++

+++ Échec silencieux de la création de la bibliothèque

Accédez à [!UICONTROL Publishing Flow] et vérifiez si la bibliothèque affiche un état [!UICONTROL Build Failed]. Ouvrez la bibliothèque et consultez le journal de génération . Les causes courantes sont les configurations de règle non valides ou les conflits de version d’extension.

+++

### Problèmes de validation des schémas pour les champs Advertising {#schema-validation-for-advertising-fields}

#### Événements :

* L’appel de l’événement d’envoi `alloy()` réussit (avec une réponse 200), mais les données de conversion Adobe Advertising sont absentes des rapports
* La payload XDM du débogueur n’affiche aucun objet `_experience.adcloud`

#### Causes possibles et vérification/résolution

+++ Le groupe de champs [!UICONTROL Advertising] est absent du schéma

Assurez-vous que le groupe de champs [!UICONTROL Advertising] est ajouté au schéma.

1. Accédez à Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas].
1. Ouvrez le schéma utilisé par votre flux de données.
1. Dans le panneau [!UICONTROL Field Groups], confirmez que **Extension complète Adobe Advertising Cloud ExperienceEvent** est répertoriée.
1. S’il est manquant, sélectionnez **Ajouter**, recherchez **Adobe Advertising Cloud**, sélectionnez **Extension complète Adobe Advertising Cloud ExperienceEvent**, puis enregistrez les paramètres.

>[!NOTE]
>La republication de votre bibliothèque [!DNL Tags] n’est pas nécessaire pour les seules modifications de schéma, mais vous devez remapper l’élément de données XDM dans [!DNL Tags] si de nouveaux champs ont été ajoutés.

+++

+++ Les champs Adobe Advertising obligatoires sont absents du schéma.

Assurez-vous que les champs Adobe Advertising requis sont présents dans le schéma sous `_experience.adcloud.conversionDetails`.

| Chemin du champ | Type | Description |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | String | Mappe la conversion sur l’annonce publicitaire d’origine. Renseigné à partir du paramètre de requête `s_kwcid` sur l’URL de la page de destination. |
| `_experience.adcloud.conversionDetails.trackingIdentity` | String | Stocke l’identité unique et d’autres détails pour l’événement de conversion d’affichage publicitaire ou de clic publicitaire suivi. Renseigné à partir du paramètre de requête `ef_id` sur l’URL de la page de destination. |

Si l’un des champs est manquant, vérifiez que le groupe de champs **Extension complète Adobe Advertising Cloud ExperienceEvent** a été enregistré dans le schéma, puis actualisez l’éditeur de schémas.

+++

+++ L’URL de la page de destination n’inclut pas les paramètres de requête requis.

Assurez-vous que l’URL de la page de destination contient les paramètres de requête nécessaires. Lors d’un clic publicitaire, l’URL de la page de destination doit contenir les deux paramètres de requête, par exemple `https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`

| Paramètre manquant | Cause probable |
| ----- | --- |
| `s_kwcid` | Le balisage automatique n’est pas activé dans les paramètres de la campagne Adobe Advertising Search ou DSP. |
| `ef_id` | L’URL de la page de destination n’utilise pas de redirection suivie par Adobe Advertising ou l’ajout d’un ID d’événement n’est pas activé dans les paramètres de la campagne. |

+++

+++ Certains paramètres de la payload XDM sont manquants ou vides.

Pour valider la payload XDM sortante, ouvrez l’onglet [!DNL Adobe Experience Platform] Debugger ou [!UICONTROL Network] du navigateur, recherchez des `edge.adobedc.net` dans le filtre, puis examinez le corps de la requête d’interaction. Une payload de clic publicitaire valide se présente comme suit :

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

Si `trackingCode` ou `trackingIdentity` sont vides ou manquants :

* Le paramètre de requête n’était pas présent sur la page lors du déclenchement de la règle. Vérifiez l’URL et la durée de l’événement de la règle.
* Le groupe de champs est absent du schéma. Reprenez les étapes du schéma ci-dessus.

+++

## Problèmes de reporting {#reporting-issues}

### Rapports de synthèse {#summary-reporting}

#### Problèmes et vérification/résolution

+++ Aucune donnée de rapport de synthèse n’est disponible dans Customer Journey Analytics pour Advertising DSP ou Advertising Search, Social et Commerce.

Vérifiez les points suivants :

* Customer Journey Analytics Workspace référence la vue de données appropriée.

* Le flux d’Adobe Advertising vers Customer Journey Analytics est activé. Vérifiez auprès de l’équipe chargée de votre compte Adobe.

* Votre jeu de données de dimension/classification/recherche Adobe Advertising et votre jeu de données de résumé sont inclus dans votre connexion Customer Journey Analytics.

* Vos dimensions Adobe Advertising et mesures récapitulatives sont incluses dans votre vue de données Customer Journey Analytics.

Si vous vérifiez tous les paramètres ci-dessus mais que vous ne voyez toujours pas de données récapitulatives, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support).

+++

+++ Les données de rapports récapitulatives sont disponibles dans Customer Journey Analytics pour l’annonceur 1, mais pas pour l’annonceur 2.

Vérifiez les points suivants :

* Le flux d’Adobe Advertising vers Customer Journey Analytics est activé pour l’annonceur 2. Vérifiez auprès de l’équipe chargée de votre compte Adobe.

* Le paramètre « [!UICONTROL Backfill all existing data] » est activé pour vos trois jeux de données (dimension/classification/recherche, résumé et mesures d’événement) dans votre connexion Customer Journey Analytics.

Si vous vérifiez toutes les conditions ci-dessus mais que vous ne voyez toujours pas de données récapitulatives, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support).

+++

+++ (Utilisateurs Search, Social et Commerce) Les données de rapports de synthèse sont disponibles dans Customer Journey Analytics pour un compte [!DNL Google Ads], [!DNL Meta Ads] ou [!DNL Microsoft Advertising], mais pas pour un autre compte.

Vérifiez que le flux d’Adobe Advertising vers Customer Journey Analytics est activé pour le compte réseau publicitaire spécifique. Vérifiez auprès de l’équipe chargée de votre compte Adobe.

Si le flux est activé pour un compte, mais que vous ne voyez toujours pas de données récapitulatives, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support). Incluez le [!UICONTROL Account ID] du compte réseau publicitaire.

+++

+++ Les données de rapports de synthèse dans Customer Journey Analytics Workspace sont différentes de celles d’Advertising DSP ou d’Advertising Search, Social et Commerce, ou les données de synthèse sont manquantes pour certaines campagnes et entités de campagne.

Vérifiez les points suivants :

* Vous utilisez les mêmes périodes dans les rapports [!DNL Workspace] et Adobe Advertising.

* Les filtres et les segments appliqués dans [!DNL Workspace] et le rapport Adobe Advertising ne provoquent pas de différences dans les données.

* La [!UICONTROL Time Zone] de la vue de données Customer Journey Analytics correspond à la [[!UICONTROL Default Timezone] de votre compte Advertising DSP](/help/dsp/admin/user-own-profile-edit.md).

* Le paramètre « [!UICONTROL Backfill all existing data] » est activé pour vos trois jeux de données (dimension/classification/recherche, résumé et mesures d’événement) dans votre connexion Customer Journey Analytics.

Si vous êtes sûr d’une incohérence des données, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support). Incluez le [!UICONTROL Account ID] du compte réseau publicitaire. Pour montrer la preuve de l’incohérence, incluez des captures d’écran et des feuilles de calcul. Votre équipe de compte Adobe peut corriger rétroactivement le flux de données pour résoudre l’incohérence, si nécessaire.

+++

### Reporting au niveau des événements {#event-level-reporting}

#### Problèmes et vérification/résolution

+++ Les données de conversion (telles que `Page Views`) ne sont pas disponibles pour une dimension de rapport (telle que `Campaign`) dans CJA Customer Journey Analytics Workspace.

Vérifiez les points suivants, en commençant par les éléments présentant le moins de barrières de vérification :

* Vous utilisez la vue de données correcte.

* Les mesures de conversion applicables sont les événements web/en ligne qu’Adobe Advertising peut attribuer aux dimensions.

* Adobe Advertising effectue le suivi des clics publicitaires et des affichages publicitaires sur le site approprié. <!-- Link to validation instructions in the user guide -->

* Dans la connexion Customer Journey Analytics du jeu de données de classifications, les valeurs des paramètres [!DNL Key] et [!DNL Matching Key] sont correctes : [!DNL Key] : `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key] : `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* Le service [!DNL Adobe Advertising] est ajouté au flux de données Adobe Experience Platform, le schéma mappé du flux de données est `XDM ExperienceEvent Schema` et le groupe de champs `Adobe Advertising Cloud ExperienceEvent Full Extension` est ajouté au schéma `XDM ExperienceEvent`.

* Les paramètres Adobe Advertising sont correctement configurés dans l’extension WebSDK et publiés.

Si vous vérifiez tous les paramètres ci-dessus mais que vous ne voyez toujours pas les données de conversion, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support). Incluez le [!UICONTROL Account ID] du compte réseau publicitaire.

+++

<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

## Outils de validation et de débogage

### Adobe Experience Platform Debugger

Installez l’extension [!DNL Adobe Experience Platform Debugger] pour [!DNL Chrome]. Il fournit les éléments suivants :

* Affichage en temps réel de tous les appels de `alloy()` WebSDK
* Validation de l’environnement et de l’identifiant du flux de données
* Inspection de la payload XDM
* Détails de la requête et de la réponse Edge Network

Vérifications de clés dans le débogueur :

| Tabulation | Éléments à vérifier |
| ----- | --- |
| [!UICONTROL Summary] | Confirme que le SDK Web est détecté et affiche la version installée. |
| [!UICONTROL Adobe Experience Platform WebSDK] | Affiche chaque événement déclenché, la payload XDM complète et la réponse Edge. |
| [!UICONTROL Adobe Advertising] | Confirme la capture de l’ID AMO et l’appel d’interaction XDM avec le type d’événement `advertising.enrichment`. |

### Onglet Réseau du navigateur

Filtrez par `edge.adobedc.net` pour inspecter les requêtes Edge brutes :

* URL de la demande : `https://[org-id].data.adobedc.net/ee/v2/interact`
* Méthode : `POST`
* Statut : `200` (sain), `400` (payload incorrecte) ou `500` (erreur de serveur ou de flux de données)

Vérifiez la payload de la requête pour :

* La bonne `dataStreamId`
* Présence d’un objet `xdm` avec les champs attendus
* Un `identityMap` avec l’ECID renseigné

### Validation de la console

Vérifiez la version du SDK Web installée :

```js
window.alloy.version
```

Déclenchez manuellement un événement de test :

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## Liste de contrôle de référence rapide

Vérifiez les points suivants avant d’ouvrir un ticket d’assistance :

* L’extension WebSDK dispose de la dernière version.
* La bibliothèque est publiée et le code incorporé est correct pour l’environnement.
* L’identifiant du flux de données est défini correctement pour le développement, l’évaluation et la production.
* Tous les services de flux de données requis sont activés.
* Le composant [!UICONTROL Advertising] est activé dans la configuration de l’extension WebSDK et un ID d’annonceur DSP est configuré.
* Le schéma XDM inclut le groupe de champs [!UICONTROL Advertising].
* La règle [!UICONTROL Send Event] inclut un mappage d’identités et se déclenche sur l’événement correct.
* Aucun CSP ou paramètre de confidentialité du navigateur ne bloque les requêtes Edge.
* Le débogueur [!DNL Adobe Experience Platform] confirme que les événements atteignent la limite.
* Aucune erreur JavaScript dans la console du navigateur n’interrompt l’exécution.
* Le groupe de champs **Extension complète Adobe Advertising Cloud ExperienceEvent** est ajouté au schéma.
* `_experience.adcloud.conversionDetails.trackingCode` est présent dans le schéma.
* `_experience.adcloud.conversionDetails.trackingIdentity` est présent dans le schéma.
* L’URL de la page de destination contient à la fois `s_kwcid` et `ef_id` en cas de clic publicitaire.
* Le débogueur [!DNL Adobe Experience Platform] confirme que `conversionDetails` est renseigné dans la payload sortante.

## Quand escalader

Contactez votre équipe de compte Adobe ou votre équipe d’ingénieurs si :

* Les requêtes Edge renvoient des erreurs `500` persistantes après la validation du flux de données.
* Les conversions [!UICONTROL Advertising] sont confirmées dans le débogueur, mais n’apparaissent pas dans les rapports après 24 à 48 heures.
* Une mise à jour de la version du SDK Web introduit une régression qui n’était pas présente dans la version précédente. Incluez les numéros de version spécifiques dans le ticket de support.

>[!MORELIKETHIS]
>
>* [Aperçu](overview.md)
>* [Adobe Advertising ID utilisés par  [!DNL Customer Journey Analytics]](ids.md)
>* [Conditions préalables](prerequisites.md)
>* [Configurer la collecte, le transfert et la création de rapports de données](set-up.md)
>* [Mesures et dimensions Adobe Advertising dans Customer Journey Analytics](advertising-data-in-cja.md)
>* (Utilisateurs Adobe Analytics) [Collectez des données historiques pour les ID AMO et les ID EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
