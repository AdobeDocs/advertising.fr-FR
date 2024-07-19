---
title: Importation de segments Adobe Audience Manager pour le ciblage des publicités
description: Découvrez comment importer vos  [!DNL Adobe] audiences dans Advertising DSP et effectuer des recherches à l’aide de Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importation de segments Adobe Audience Manager pour le ciblage des publicités

Advertising DSP et [!DNL Advertising Search, Social, & Commerce] peuvent extraire des métadonnées, des données de hiérarchie et des données d’audience uniques pour toutes les [!DNL Adobe] audiences<!-- segments or audiences? Standardize terms per AAM's docs --> d’un annonceur ou d’une agence, notamment :

* Segments Adobe Audience Manager

* Segments Adobe Analytics publiés dans Adobe Experience Cloud

* Segments créés à l’aide de Adobe Experience Cloud [!DNL Audience Library]

* Segments créés dans Adobe Experience Platform et envoyés à l’Adobe Advertising par Audience Manager

Pour accéder aux audiences [!DNL Adobe] dans DSP ou [!DNL Creative], vous devez importer les audiences dans DSP. Pour accéder aux audiences [!DNL Adobe] dans [!DNL Search, Social, & Commerce], vous devez importer les audiences dans [!DNL Search, Social, & Commerce].

## Conditions préalables

* L’annonceur doit implémenter [la version 2.0 ou ultérieure de  [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview). [!DNL Identity Service] fournit un identifiant universel et permanent qui identifie vos visiteurs dans toutes les solutions Experience Cloud.

  La mise en oeuvre comprend l’ajout du code [!DNL Identity service] à chaque page web sur les sites de l’annonceur.

* L&#39;organisation doit être [activée pour les services Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) et avoir un Experience Cloud [!DNL Organization ID] (anciennement appelé [!DNL IMS org ID]).

  Le [!UICONTROL Organization ID] permet aux entreprises qui disposent de plusieurs produits Adobe Experience Cloud de partager des données entre certains produits.

* (Publicitaires avec [!DNL Analytics]) L’annonceur doit [mettre en oeuvre  [!DNL Analytics] à l’aide de `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) version 1.6.4 ou ultérieure.

* Les visiteurs du site web de l’annonceur n’incluent pas un volume élevé d’utilisateurs [!DNL Apple Safari].

* (Recommandé lorsque l’annonceur utilise à la fois l’Audience Manager et [!DNL Analytics]) Pour réduire les appels vers chaque page web, supprimez le code d’Audience Manager [!DNL Data Integration Library] existant pour la collecte de données et activez le transfert côté serveur pour chaque suite de rapports [!DNL Analytics] à la place. Pour plus d’informations, voir &quot;[Présentation du transfert côté serveur](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf)&quot;.

* (Recommandé) Pour des taux de correspondance plus élevés, envoyez uniquement des données de site web propriétaires à Adobe Advertising. Si l’annonceur rassemble des données tierces ou hors ligne d’un système de gestion de la relation client, les fuites de données peuvent réduire les taux de correspondance.

## Importation d’audiences d’Audience Manager dans DSP

### Procédure d’importation d’audiences dans DSP

Les équipes des opérations de compte et de données [!DNL Adobe] effectuent les étapes suivantes.

1. L’équipe du compte d’Adobe doit configurer le paramètre au niveau de l’annonceur &quot;[!UICONTROL Adobe Analytics Cloud]&quot;.

1. L’équipe Compte d’Adobe doit envoyer une demande à l’équipe des opérations de données pour importer les segments d’Audience Manager de l’organisation à l’aide de l’intégration de l’API native Advertising DSP.

### Quels changements entraînent l’Audience Manager ?

L’API automatiquement :

* Crée deux destinations DSP en Audience Manager :

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Met en correspondance les deux destinations avec tous les segments d’Audience Manager, ce qui permet à l’Audience Manager de partager les segments avec le compte d’annonceur DSP associé au même Experience Cloud [!DNL Organization ID] utilisé pour l’Audience Manager.

  L’organisation peut éventuellement supprimer les segments inutiles des destinations dans l’Audience Manager.

* Ajoute le pixel de synchronisation des cookies d’exchange suivant au conteneur d’Audience Manager de l’entreprise afin d’améliorer la portée des campagnes client :

   * Adobe AdCloud : 411 (Ce pixel est fourni en standard et automatiquement dans le cadre de la version 2.0 de [!DNL Identity Service]. Les organisations disposant de [!DNL Identity Service] versions antérieures à la version 2.0 doivent ajouter ce pixel à leur conteneur d’Audience Manager.

## Importation d’audiences d’Audience Manager vers [!DNL Search, Social, & Commerce]

### Étapes pour importer des audiences vers [!DNL Search, Social, & Commerce]

Le personnel de [!DNL Adobe] effectue la plupart ou la totalité des étapes suivantes.

1. L’équipe Compte d’Adobe doit envoyer une demande à l’équipe des opérations de données pour configurer une intégration entre [!DNL Search, Social, & Commerce] et l’Audience Manager. Incluez les noms des segments d’Audience Manager que vous souhaitez exporter vers [!DNL Search, Social, & Commerce].

1. Dans l’Audience Manager, configurez les destinations pour [!DNL Search, Social, & Commerce] :

   1. Créez deux nouvelles destinations : `[!UICONTROL Adobe Media Optimizer (HTTP)]` et `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] est un ancien nom de [!DNL Search, Social, & Commerce].

   1. Spécifiez les segments pour chacune des destinations.

      Avec l’option [!UICONTROL Automatically map all current and future segments], tous les segments sont mappés et synchronisés quotidiennement.

      L’option [!UICONTROL Manually map segments] vous permet de mapper manuellement les segments à synchroniser avec la destination du lot (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Aucun segment ne doit être mappé manuellement à la destination HTTP.

1. Dans [!DNL Search, Social, & Commerce], l’équipe d’implémentation [!DNL Search, Social, & Commerce] ou un utilisateur avec le rôle de gestionnaire du client d’accès direct doit lancer l’importation depuis [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   L’Experience Cloud de l’organisation [!DNL Organization ID] ([!DNL IMS org ID]) est requis. L’ID doit être identique à celui utilisé pour le compte d’Audience Manager de l’organisation.

### Quels changements entraînent l’Audience Manager ?

Deux destinations [!DNL Search, Social, & Commerce] deviennent disponibles pour l’organisation en Audience Manager :

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Synchronisation des données

L&#39;import initial prend environ 24 heures. Après l’importation initiale, les données sont synchronisées en temps réel, avec un délai d’une à deux secondes.

Les données d’adhésion au segment ne sont envoyées qu’après l’un des événements suivants :

* (Publicitaires avec DSP) :

   * Le segment est ciblé dans une publicité display Adobe Advertising.

   * Le segment est ajouté aux destinations par lot [!DNL Adobe AdCloud Cross-Channel] et en temps réel dans l’interface utilisateur de l’Audience Manager.

* (Annonceurs avec [!DNL Search, Social, & Commerce]) :

   * Le segment est ciblé dans une publicité de recherche d’Adobe Advertising.

   * Le segment est ajouté aux destinations [!DNL Adobe Media Optimizer] par lot et HTTP dans l’interface utilisateur de l’Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Synchronisation des données par DSP

DSP synchronise automatiquement les données à l’aide de [!DNL Adobe Experience Cloud Identity (ECID) Service]. Lors de la synchronisation, le [!DNL ECID Service] appelle l’Adobe Advertising à l’emplacement [!DNL cm.everesttech.net]. Comme Adobe Advertising est un domaine de confiance, les synchronisations des identifiants ont lieu à partir des pages parentes plutôt que dans les iframes de publication de destination, comme c’est le cas avec la plupart des partenaires d’activation tiers. L’Audience Manager identifie les utilisateurs uniques par ID d’appareil, à l’aide de l’ [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), également appelé [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Synchronisation des données par Search, Social et Commerce

Search, Social et Commerce synchronise automatiquement les données à l’aide de [!DNL Adobe Experience Cloud Identity (ECID) Service]. Lors de la synchronisation, le [!DNL ECID Service] appelle l’Adobe Advertising à l’adresse [!DNL cm.everesttech.net], qui est un domaine de confiance qui appartient à l’Adobe Advertising. L’Audience Manager identifie les utilisateurs uniques par ID d’appareil, à l’aide de l’ [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), également appelé [!DNL Device ID].

## Où trouver vos segments synchronisés

### Dans DSP

DSP classe les noms des segments par taxonomie de l’Audience Manager et inclut les décomptes d’adhésion aux segments correspondants dans :

* [Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting) : sur l’onglet [!UICONTROL Adobe Segments] de la section [!UICONTROL Audience Targeting].

* Dans [paramètres d’audience](/help/dsp/audiences/audience-settings.md) : sur l’onglet [!UICONTROL Adobe Segments].

### Dans Advertising Creative

Dans [!DNL Creative], les segments sont disponibles dans les paramètres d’expérience pour les noeuds cibles.

### Dans [!DNL Advertising Search, Social, & Commerce]

Dans [!DNL Search, Social, & Commerce], les segments sont disponibles lorsque vous créez une audience [!DNL Google] à l’aide de [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; à partir de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Pour chaque audience [!DNL Google] que vous créez, [!DNL Google] fournit la taille de l’audience.

>[!MORELIKETHIS]
>
>* [Adobe Advertising des intégrations avec Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
