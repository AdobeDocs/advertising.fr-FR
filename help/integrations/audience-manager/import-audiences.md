---
title: Importation de segments Adobe Audience Manager pour le ciblage des publicités
description: Découvrez comment importer votre [!DNL Adobe] audiences dans Advertising DSP et recherche à l’aide de Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importation de segments Adobe Audience Manager pour le ciblage des publicités

Advertising DSP et [!DNL Advertising Search, Social, & Commerce] peut extraire des métadonnées, des données hiérarchiques et des données d’audience uniques pour l’ensemble du contenu d’un annonceur ou d’une agence ; [!DNL Adobe] audiences<!-- segments or audiences? Standardize terms per AAM's docs -->, notamment :

* Segments Adobe Audience Manager

* Segments Adobe Analytics publiés dans Adobe Experience Cloud

* Segments créés à l’aide de Adobe Experience Cloud [!DNL Audience Library]

* Segments créés dans Adobe Experience Platform et envoyés à l’Adobe Advertising par Audience Manager

Pour accéder [!DNL Adobe] audiences dans DSP ou [!DNL Creative], vous devez importer les audiences dans DSP. Pour accéder [!DNL Adobe] audiences dans [!DNL Search, Social, & Commerce], vous devez importer les audiences dans [!DNL Search, Social, & Commerce].

## Conditions préalables

* L’annonceur doit implémenter [la valeur [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) version 2.0 ou ultérieure. La variable [!DNL Identity Service] fournit un identifiant universel et permanent qui identifie vos visiteurs dans toutes les solutions Experience Cloud.

  La mise en oeuvre comprend l’ajout de la variable [!DNL Identity service] code vers chaque page web des sites de l’annonceur.

* L’organisation doit être [activé pour les services Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) et posséder un Experience Cloud [!DNL Organization ID] (anciennement appelée [!DNL IMS org ID]).

  La variable [!UICONTROL Organization ID] permet aux entreprises disposant de plusieurs produits Adobe Experience Cloud de partager des données entre certains produits.

* (Publicitaires avec [!DNL Analytics]) L’annonceur doit [implémenter [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) version 1.6.4 ou ultérieure.

* Les visiteurs du site web de l’annonceur n’incluent pas un volume élevé de [!DNL Apple Safari] utilisateurs.

* (Recommandé lorsque l’annonceur utilise à la fois l’Audience Manager et [!DNL Analytics]) Pour réduire les appels à chaque page web, supprimez l’Audience Manager existante. [!DNL Data Integration Library] code pour la collecte de données et activation du transfert côté serveur pour chaque [!DNL Analytics] suite de rapports à la place. Pour plus d’informations, voir &quot;[Transfert côté serveur - Aperçu](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Recommandé) Pour des taux de correspondance plus élevés, envoyez uniquement des données de site web propriétaires à Adobe Advertising. Si l’annonceur rassemble des données tierces ou hors ligne d’un système de gestion de la relation client, les fuites de données peuvent réduire les taux de correspondance.

## Importation d’audiences d’Audience Manager dans DSP

### Procédure d’importation d’audiences dans DSP

La variable [!DNL Adobe] les équipes des opérations de compte et de données effectuent les étapes suivantes.

1. L’équipe du compte Adobe doit configurer le paramètre au niveau de l’annonceur &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. L’équipe du compte Adobe doit envoyer une demande à l’équipe des opérations de données pour importer les segments d’Audience Manager de l’entreprise à l’aide de l’intégration de l’API native Advertising DSP.

### Quels changements entraînent l’Audience Manager ?

L’API automatiquement :

* Crée deux destinations DSP en Audience Manager :

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Mappe les deux destinations à tous les segments d’Audience Manager, ce qui permet à l’Audience Manager de partager les segments avec le compte publicitaire DSP associé au même Experience Cloud. [!DNL Organization ID] utilisé pour l’Audience Manager.

  L’organisation peut éventuellement supprimer les segments inutiles des destinations dans l’Audience Manager.

* Ajoute le pixel de synchronisation des cookies d’exchange suivant au conteneur d’Audience Manager de l’entreprise afin d’améliorer la portée des campagnes client :

   * Adobe AdCloud : 411 (Ce pixel est fourni en standard et automatiquement dans le cadre de [!DNL Identity Service] version 2.0. Organisations avec [!DNL Identity Service] Les versions antérieures à la version 2.0 doivent ajouter ce pixel à leur conteneur d’Audience Manager.

## Importation d’audiences d’Audience Manager dans [!DNL Search, Social, & Commerce]

### Procédure d’importation d’audiences dans [!DNL Search, Social, & Commerce]

[!DNL Adobe] Le personnel effectue la plupart ou la totalité des étapes suivantes.

1. L’équipe Compte d’Adobe doit envoyer une demande à l’équipe des opérations de données afin de configurer une intégration entre [!DNL Search, Social, & Commerce] et Audience Manager. Inclure les noms des segments d’Audience Manager que vous souhaitez exporter vers [!DNL Search, Social, & Commerce].

1. Dans Audience Manager, configurez les destinations pour [!DNL Search, Social, & Commerce]:

   1. Créez deux nouvelles destinations : `[!UICONTROL Adobe Media Optimizer (HTTP)]` et `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] est un ancien nom de [!DNL Search, Social, & Commerce].

   1. Spécifiez les segments pour chacune des destinations.

      Avec la variable [!UICONTROL Automatically map all current and future segments] , tous les segments sont mappés et synchronisés quotidiennement.

      La variable [!UICONTROL Manually map segments] vous permet de mapper manuellement les segments à synchroniser avec la destination du lot (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Aucun segment ne doit être mappé manuellement à la destination HTTP.

1. Within [!DNL Search, Social, & Commerce], soit le [!DNL Search, Social, & Commerce] l’équipe de mise en oeuvre ou un utilisateur disposant du rôle de gestionnaire client d’accès direct doit lancer l’importation à partir de [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   L’Experience Cloud de l’organisation [!DNL Organization ID] ([!DNL IMS org ID]) est obligatoire. L’ID doit être identique à celui utilisé pour le compte d’Audience Manager de l’organisation.

### Quels changements entraînent l’Audience Manager ?

Deux [!DNL Search, Social, & Commerce] les destinations deviennent disponibles pour l’organisation en Audience Manager :

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Synchronisation des données

L&#39;import initial prend environ 24 heures. Après l’importation initiale, les données sont synchronisées en temps réel, avec un délai d’une à deux secondes.

Les données d’adhésion au segment ne sont envoyées qu’après l’un des événements suivants :

* (Publicitaires avec DSP) :

   * Le segment est ciblé dans une publicité display Adobe Advertising.

   * Le segment est ajouté au [!DNL Adobe AdCloud Cross-Channel] destinations par lot et en temps réel dans l’interface utilisateur d’Audience Manager.

* (Publicitaires avec [!DNL Search, Social, & Commerce]) :

   * Le segment est ciblé dans une publicité de recherche d’Adobe Advertising.

   * Le segment est ajouté au [!DNL Adobe Media Optimizer] Destinations par lots et HTTP dans l’interface utilisateur de l’Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Synchronisation des données par DSP

DSP synchronise automatiquement les données à l’aide de la fonction [!DNL Adobe Experience Cloud Identity (ECID) Service]. Lors de la synchronisation, la variable [!DNL ECID Service] appelle Adobe Advertising à l’adresse [!DNL cm.everesttech.net]. Comme Adobe Advertising est un domaine de confiance, les synchronisations des identifiants ont lieu à partir des pages parentes plutôt que dans les iframes de publication de destination, comme c’est le cas avec la plupart des partenaires d’activation tiers. Audience Manager identifie les utilisateurs uniques par identifiant d’appareil, à l’aide de la variable [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), également appelé [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Synchronisation des données par Search, Social et Commerce

Search, Social et Commerce synchronise automatiquement les données à l’aide de la variable [!DNL Adobe Experience Cloud Identity (ECID) Service]. Lors de la synchronisation, la variable [!DNL ECID Service] appelle Adobe Advertising à l’adresse [!DNL cm.everesttech.net], qui est un domaine de confiance qui appartient à Adobe Advertising. Audience Manager identifie les utilisateurs uniques par identifiant d’appareil, à l’aide de la variable [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), également appelé [!DNL Device ID].

## Où trouver vos segments synchronisés

### Dans DSP

DSP classe les noms des segments par taxonomie de l’Audience Manager et inclut les décomptes d’adhésion aux segments correspondants dans :

* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): sur le [!UICONTROL Adobe Segments] de la [!UICONTROL Audience Targeting] .

* Dans [paramètres d’audience](/help/dsp/audiences/audience-settings.md): sur le [!UICONTROL Adobe Segments] .

### Dans Advertising Creative

Dans [!DNL Creative], les segments sont disponibles dans les paramètres de l’expérience pour les noeuds cibles.

### Dans [!DNL Advertising Search, Social, & Commerce]

Dans [!DNL Search, Social, & Commerce], les segments sont disponibles lorsque vous créez une [!DNL Google] audience utilisant la variable [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Pour chaque [!DNL Google] audience que vous créez, [!DNL Google] fournit la taille de l’audience.

>[!MORELIKETHIS]
>
>* [Adobe Advertising des intégrations avec Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
