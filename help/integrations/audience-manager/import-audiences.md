---
title: Import Adobe Audience Manager segments for ad targeting
description: Learn how to import your [!DNL Adobe] audiences into Advertising DSP and Search using Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
TQID: https://experienceleague.adobe.com/-OqZLPZ1uWjBqSaCtGnmF5nrrxVIdT0kpE6YznQWttw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 992
ht-degree: 0%

---

# Import Adobe Audience Manager segments for ad targeting

Advertising DSP and [!DNL Advertising Search, Social, & Commerce] can each pull in metadata, hierarchy data, and unique audience data for all of an advertiser&#39;s or agency&#39;s [!DNL Adobe] audiences<!-- segments or audiences? Standardize terms per AAM's docs -->, including:

* Segments Adobe Audience Manager

* Segments Adobe Analytics publiés sur Adobe CX Enterprise

* Segments créés à l’aide de l’[!DNL Audience Library] Adobe CX Enterprise

* Segments that are created in Adobe Experience Platform and sent to Adobe Advertising via Audience Manager

To access [!DNL Adobe] audiences in DSP or [!DNL Creative], you must import the audiences into DSP. To access [!DNL Adobe] audiences in [!DNL Search, Social, & Commerce], you must import the audiences into [!DNL Search, Social, & Commerce].

## Conditions préalables

* The advertiser must implement [the [!DNL Adobe CX Enterprise Identity (ECID) Service]](https://experienceleague.adobe.com/fr/docs/id-service/using/intro/overview) version 2.0 or higher. The [!DNL Identity Service] provides a universal, persistent ID that identifies your visitors across all solutions in CX Enterprise.

  Implementation includes adding the [!DNL Identity service] code to each webpage on the advertiser&#39;s sites.

* The organization must be [enabled for CX Enterprise services](https://experienceleague.adobe.com/fr/docs/core-services/interface/services/overview) and have a CX Enterprise [!DNL Organization ID] (formerly called [!DNL IMS org ID]).

  The [!UICONTROL Organization ID] allows organizations with multiple Adobe CX Enterprise products to share data among some of the products.

* (Advertisers with [!DNL Analytics]) The advertiser must [implement [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/fr/docs/analytics/implementation/js/overview) version 1.6.4 or higher.

* The advertiser&#39;s website visitors don&#39;t include a high volume of [!DNL Apple Safari] users.

* (Recommended when the advertiser uses both Audience Manager and [!DNL Analytics]) To reduce calls to each webpage, remove existing Audience Manager [!DNL Data Integration Library] code for data collection and enable server-side forwarding for each [!DNL Analytics] report suite instead. For more information, see &quot;[Server-side forwarding overview](https://experienceleague.adobe.com/fr/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Recommended) For higher match rates, send only first-party website data to Adobe Advertising. If the advertiser bundles third-party data or offline data from a customer relationship management system, data leakage may reduce match rates.

## Import Audience Manager audiences to DSP

### Steps to import audiences to DSP

The [!DNL Adobe] account and data operations teams perform the following steps.

1. The Adobe Account Team should configure the advertiser-level setting &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. The Adobe Account Team should submit a request to the data operations team to import the organization&#39;s Audience Manager segments using the Advertising DSP native API integration.

### What changes result in Audience Manager?

The API automatically:

* Creates two DSP destinations in Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Maps the two destinations to all Audience Manager segments, allowing Audience Manager to share the segments with the DSP advertiser account that&#39;s associated with the same CX Enterprise [!DNL Organization ID] used for Audience Manager.

  The organization can optionally remove unneeded segments from the destinations within Audience Manager.

* Adds the following exchange cookie-sync pixel to the organization&#39;s Audience Manager container to improve the reach of customer campaigns:

   * Adobe AdCloud: 411 (This pixel comes standard and automatically as part of [!DNL Identity Service] version 2.0. Organizations with [!DNL Identity Service] versions below 2.0 should add this pixel to their Audience Manager container.

## Import Audience Manager audiences to [!DNL Search, Social, & Commerce]

### Steps to import audiences to [!DNL Search, Social, & Commerce]

[!DNL Adobe] personnel perform most or all of the following steps.

1. The Adobe Account Team should submit a request to the data operations team to set up an integration between [!DNL Search, Social, & Commerce] and Audience Manager. Include the names of the Audience Manager segments that you want to export to [!DNL Search, Social, & Commerce].

1. Within Audience Manager, configure destinations for [!DNL Search, Social, & Commerce]:

   1. Create two new destinations: `[!UICONTROL Adobe Media Optimizer (HTTP)]` and `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] is a former name for [!DNL Search, Social, & Commerce].

   1. Specify the segments for each of the destinations.

      With the [!UICONTROL Automatically map all current and future segments] option, all segments are mapped and synced daily.

      L’option [!UICONTROL Manually map segments] vous permet de mapper manuellement les segments à synchroniser avec la destination par lots (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Aucun segment ne doit être mappé manuellement à la destination HTTP.

1. En [!DNL Search, Social, & Commerce], l’équipe d’implémentation [!DNL Search, Social, & Commerce] ou un utilisateur disposant du rôle de gestionnaire de client d’accès direct doit lancer l’importation à partir de [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Le [!DNL Organization ID] Adobe CX Enterprise de l’organisation ([!DNL IMS org ID]) est obligatoire. L’identifiant doit être identique à celui utilisé pour le compte Audience Manager de l’organisation.

### Quels changements génèrent Audience Manager ?

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

DSP synchronise automatiquement les données à l’aide de l’[!DNL Adobe Experience Cloud Identity (ECID) Service] . Lors de la synchronisation, le [!DNL ECID Service] appelle Adobe Advertising à l’adresse [!DNL cm.everesttech.net]. Adobe Advertising étant un domaine approuvé, les synchronisations des identifiants se produisent à partir des pages parentes plutôt que dans les iFrames de publication de destination, comme c’est le cas avec la plupart des partenaires d’activation tiers. Audience Manager identifie les utilisateurs uniques par ID d’appareil, à l’aide de [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/fr/docs/audience-manager/user-guide/reference/ids-in-aam), également appelé [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Comment Search, Social et Commerce synchronisent les données

Search, Social et Commerce synchronise automatiquement les données à l’aide de l’[!DNL Adobe Experience Cloud Identity (ECID) Service]. Lors de la synchronisation, le [!DNL ECID Service] appelle Adobe Advertising à l’adresse [!DNL cm.everesttech.net], qui est un domaine de confiance appartenant à Adobe Advertising. Audience Manager identifie les utilisateurs uniques par ID d’appareil, à l’aide de [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/fr/docs/audience-manager/user-guide/reference/ids-in-aam), également appelé [!DNL Device ID].

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
>* [Intégrations Adobe Advertising avec Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
