---
title: Importation de segments Adobe Audience Manager pour le ciblage publicitaire
description: Découvrez comment importer vos audiences dans Advertising DSP et effectuer  [!DNL Adobe]  recherche à l’aide de Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importation de segments Adobe Audience Manager pour le ciblage publicitaire

Advertising DSP et [!DNL Advertising Search, Social, & Commerce] peuvent chacun extraire des métadonnées, des données hiérarchiques et des données d’audience uniques pour toutes les audiences [!DNL Adobe] d’un annonceur ou d’une agence<!-- segments or audiences? Standardize terms per AAM's docs --> notamment :

* Segments Adobe Audience Manager

* Segments Adobe Analytics publiés sur Adobe Experience Cloud

* Segments créés à l’aide de l’[!DNL Audience Library] Adobe Experience Cloud

* Segments créés dans Adobe Experience Platform et envoyés à Adobe Advertising via Audience Manager

Pour accéder aux audiences [!DNL Adobe] dans DSP ou [!DNL Creative], vous devez importer les audiences dans DSP. Pour accéder aux audiences [!DNL Adobe] dans [!DNL Search, Social, & Commerce], vous devez importer les audiences dans [!DNL Search, Social, & Commerce].

## Conditions préalables

* L’annonceur doit mettre en œuvre [la version 2.0 [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) ou une version ultérieure. Le [!DNL Identity Service] fournit un identifiant universel et persistant qui identifie vos visiteurs dans toutes les solutions d’Experience Cloud.

  La mise en œuvre comprend l’ajout du code [!DNL Identity service] à chaque page web sur les sites de l’annonceur.

* L’organisation doit être [activée pour les services Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) et disposer d’un [!DNL Organization ID] Experience Cloud (anciennement appelé [!DNL IMS org ID]).

  Le [!UICONTROL Organization ID] permet aux entreprises disposant de plusieurs produits Adobe Experience Cloud de partager des données entre certains des produits.

* (Annonceurs avec [!DNL Analytics]) L’annonceur doit [implémenter [!DNL Analytics] utiliser `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) version 1.6.4 ou ultérieure.

* Les visiteurs du site Web de l’annonceur n’incluent pas un grand nombre d’utilisateurs [!DNL Apple Safari].

* (Recommandé lorsque l’annonceur utilise à la fois Audience Manager et [!DNL Analytics]) Pour réduire les appels à chaque page web, supprimez le code de [!DNL Data Integration Library] Audience Manager existant pour la collecte de données et activez le transfert côté serveur pour chaque suite de rapports [!DNL Analytics]. Pour plus d’informations, voir « [Présentation du transfert côté serveur](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Recommandé) Pour des taux de correspondance plus élevés, envoyez uniquement des données de site web propriétaire à Adobe Advertising. Si l’annonceur regroupe des données tierces ou des données hors ligne provenant d’un système de gestion de la relation client, la fuite de données peut réduire les taux de correspondance.

## Importation d’audiences Audience Manager dans DSP

### Étapes d’importation d’audiences dans DSP

Les équipes du compte [!DNL Adobe] et des opérations de données effectuent les étapes suivantes.

1. L’équipe du compte Adobe doit configurer le paramètre au niveau de l’annonceur « [!UICONTROL Adobe Analytics Cloud] ».

1. L’équipe du compte Adobe doit envoyer une demande à l’équipe des opérations de données pour importer les segments Audience Manager de l’organisation à l’aide de l’intégration de l’API native Advertising DSP.

### Quelles modifications génèrent Audience Manager ?

L’API automatiquement :

* Crée deux destinations DSP dans Audience Manager :

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Mappe les deux destinations à tous les segments Audience Manager, ce qui permet à Audience Manager de partager les segments avec le compte de l’annonceur DSP associé au même [!DNL Organization ID] Experience Cloud utilisé pour Audience Manager.

  L’organisation peut éventuellement supprimer les segments inutiles des destinations dans Audience Manager.

* Ajoute le pixel de synchronisation des cookies Exchange suivant au conteneur Audience Manager de l’organisation pour améliorer la portée des campagnes client :

   * Adobe AdCloud : 411 (ce pixel est fourni en standard et automatiquement dans le cadre de la version 2.0 de [!DNL Identity Service]. Les organisations disposant de versions de [!DNL Identity Service] inférieures à la version 2.0 doivent ajouter ce pixel à leur conteneur Audience Manager.

## Importer des audiences Audience Manager dans [!DNL Search, Social, & Commerce]

### Étapes d’importation d’audiences dans [!DNL Search, Social, & Commerce]

[!DNL Adobe] personnel effectue la plupart ou la totalité des étapes suivantes.

1. L’équipe du compte Adobe doit envoyer une demande à l’équipe des opérations de données pour configurer une intégration entre [!DNL Search, Social, & Commerce] et Audience Manager. Incluez les noms des segments Audience Manager que vous souhaitez exporter vers [!DNL Search, Social, & Commerce].

1. Dans Audience Manager, configurez les destinations pour les [!DNL Search, Social, & Commerce] :

   1. Créez deux nouvelles destinations : `[!UICONTROL Adobe Media Optimizer (HTTP)]` et `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] est un ancien nom pour [!DNL Search, Social, & Commerce].

   1. Spécifiez les segments pour chacune des destinations.

      Avec l’option [!UICONTROL Automatically map all current and future segments], tous les segments sont mappés et synchronisés quotidiennement.

      L’option [!UICONTROL Manually map segments] vous permet de mapper manuellement les segments à synchroniser avec la destination par lots (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Aucun segment ne doit être mappé manuellement à la destination HTTP.

1. En [!DNL Search, Social, & Commerce], l’équipe d’implémentation [!DNL Search, Social, & Commerce] ou un utilisateur disposant du rôle de gestionnaire de client d’accès direct doit lancer l’importation à partir de [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Le [!DNL Organization ID] Experience Cloud ([!DNL IMS org ID]) de l’organisation est obligatoire. L’identifiant doit être identique à celui utilisé pour le compte Audience Manager de l’organisation.

### Quelles modifications génèrent Audience Manager ?

Deux destinations [!DNL Search, Social, & Commerce] sont alors disponibles pour l’organisation dans Audience Manager :

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Synchronisation des données

L’importation initiale prend environ 24 heures. Après l’importation initiale, les données sont synchronisées en temps réel, avec un délai d’une à deux secondes.

Les données d’appartenance à un segment ne sont envoyées qu’après l’un des événements suivants :

* (Annonceurs avec DSP) :

   * Le segment est ciblé dans une publicité display Adobe Advertising.

   * Le segment est ajouté aux destinations par lots et en temps réel [!DNL Adobe AdCloud Cross-Channel] dans l’interface utilisateur d’Audience Manager.

* (Annonceurs avec [!DNL Search, Social, & Commerce]) :

   * Le segment est ciblé dans une publicité de recherche Adobe Advertising.

   * Le segment est ajouté aux destinations HTTP et par lots [!DNL Adobe Media Optimizer] dans l’interface utilisateur d’Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Comment DSP synchronise les données

DSP synchronise automatiquement les données à l’aide de l’[!DNL Adobe Experience Cloud Identity (ECID) Service] . Lors de la synchronisation, le [!DNL ECID Service] appelle Adobe Advertising à l’adresse [!DNL cm.everesttech.net]. Adobe Advertising étant un domaine approuvé, les synchronisations des identifiants se produisent à partir des pages parentes plutôt que dans les iFrames de publication de destination, comme c’est le cas avec la plupart des partenaires d’activation tiers. Audience Manager identifie les utilisateurs uniques par ID d’appareil, à l’aide de [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), également appelé [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Comment Search, Social et Commerce synchronisent les données

Search, Social et Commerce synchronise automatiquement les données à l’aide de l’[!DNL Adobe Experience Cloud Identity (ECID) Service]. Lors de la synchronisation, le [!DNL ECID Service] appelle Adobe Advertising à l’adresse [!DNL cm.everesttech.net], qui est un domaine de confiance appartenant à Adobe Advertising. Audience Manager identifie les utilisateurs uniques par ID d’appareil, à l’aide de [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), également appelé [!DNL Device ID].

## Où trouver vos segments synchronisés

### Dans DSP

DSP organise les noms de segment selon la taxonomie Audience Manager et inclut les nombres d’appartenances aux segments correspondants dans :

* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting) : dans l’onglet [!UICONTROL Adobe Segments] de la section [!UICONTROL Audience Targeting] .

* Dans [paramètres d’audience](/help/dsp/audiences/audience-settings.md) : dans l’onglet [!UICONTROL Adobe Segments] .

### Dans Advertising Creative

Dans [!DNL Creative], les segments sont disponibles dans les paramètres d’expérience pour les nœuds cibles.

### En [!DNL Advertising Search, Social, & Commerce]

En [!DNL Search, Social, & Commerce], les segments sont disponibles lorsque vous créez une audience [!DNL Google] à l’aide du [!UICONTROL Data Source] « [!UICONTROL Adobe Audience] » dans [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Pour chaque audience [!DNL Google] que vous créez, [!DNL Google] indique la taille de l’audience.

>[!MORELIKETHIS]
>
>* [Intégrations d’Adobe Advertising à Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
