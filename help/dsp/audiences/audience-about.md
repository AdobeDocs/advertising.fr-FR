---
title: About audience management in Advertising DSP
description: Learn about audience management features.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
TQID: https://experienceleague.adobe.com/IocF0s67I-vJAUx9Eom-aWEf-Q6H-ZOjczyGr0f9PsA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 1394
ht-degree: 0%

---

# About audience management in Advertising DSP

In DSP, you can create and manage audience segments and audience sets, which you can use as targets for your placements:

* Collect your own first-party audience data by creating and implementing DSP segments. You can later retarget users in the segment with ads or prevent users in the segment from receiving ads. You can create the following types of segments:

   * [Custom segments](/help/dsp/audiences/custom-segment-create.md) to track a) users exposed to ads from desktop and mobile devices and b) users who visit specific webpages. The tracking tag can track either cookie-based users or users associated with ID5 universal IDs.

   * [CCPA opt-out-of-sale segments](/help/dsp/audiences/ccpa-opt-out-segment-create.md) to track the users IDs from consumer opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA). You can retrieve monthly reports of the user IDs from opt-out-of-sale requests.

     For more information about Adobe Advertising support for CCPA opt-out-of-sale requests, see [Adobe Advertising support for the California Consumer Privacy Act: Consumer opt-out of sale support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Beta feature) [Obtain and use universal IDs for cookieless targeting](/help/dsp/audiences/universal-ids.md):

   * Manually send your authenticated [!DNL LiveRamp] [!DNL RampID] segments directly to DSP.

   * Allow DSP to import first-party segments from your customer data platform and translate them to supported universal ID types.

   * Include third-party segments that contain universal IDs in your placement targets without any extra steps.

* Create an audience library of [reusable audiences](/help/dsp/audiences/reusable-audience-create.md). Saved audiences are composed of any of your available audience segments and any of your other saved audiences. Any changes you make to a saved audience are automatically applied to all placements that target or exclude the audience and to all other audiences that include the saved audience.

  Saved audiences allow media planners to group audiences as needed, by including and excluding multiple segments using complex Boolean logic. The  (targetable) size of each individual segment and the overall active audience size are indicated as you build an audience. Campaign executioners can then simply select one or more saved audiences as placement targets rather than manually configure audience targets for each placement.

D’autres types d’audience sont également disponibles pour le ciblage des emplacements.

## Importation de segments de données propriétaires et tiers

Vous disposez de nombreuses options pour importer des segments de données propriétaires et tiers dans DSP, à l’aide de l’interface utilisateur de DSP et/ou par le biais de services d’importation personnalisés.

* DSP peut extraire votre Adobe Audience Manager et d’autres audiences [!DNL Adobe] pour le ciblage. Pour connaître les conditions préalables et les instructions, voir « [Importer des segments Adobe Audience Manager pour le ciblage publicitaire](/help/integrations/audience-manager/import-audiences.md).

* DSP peut traduire des segments de données propriétaires à partir de plateformes de données client prises en charge en segments avec des ID universels à l’aide de la [fonctionnalité Sources](/help/dsp/audiences/sources/source-about.md). Vous pouvez également [envoyer manuellement vos segments authentifiés [!DNL LiveRamp] [!DNL RampID] directement à DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP peut importer vos autres segments de données propriétaires directement à partir de votre plateforme de gestion des données (DMP) et les fournir à n’importe quel ensemble d’annonceurs, si nécessaire.

* DSP peut importer des segments tiers personnalisés, y compris des combinaisons complexes de segments tiers. Vous pouvez fournir les segments à n’importe quel ensemble d’annonceurs, si nécessaire.

Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

## Audiences disponibles en tant que cibles d’emplacement

Vous pouvez cibler vos emplacements sur tous les types d’audiences suivants.

* Toutes les audiences créées par l’utilisateur qui ont été enregistrées dans DSP.

* Tous les segments d’audience créés par l’utilisateur ou l’utilisatrice qui ont été créés dans DSP :

   * Segments personnalisés pour les utilisateurs et utilisatrices qui ont visité des pages web spécifiques et les utilisateurs et utilisatrices exposés aux impressions d’annonces spécifiques.

     Aucun frais n’est encouru pour les impressions diffusées aux identifiants universels.

   * Segments d’audience d’opposition à la vente de la CCPA pour les utilisateurs qui ont soumis des requêtes d’opposition à la vente sur votre site web, conformément à la Loi sur la protection de la vie privée des consommateurs de Californie (CCPA).

* Tous les segments de données propriétaires importés, y compris les segments qui ont été traduits en identifiants universels.

  Des frais supplémentaires sont facturés pour les impressions remises aux cartes d’identité universelles. Consultez « [&#x200B; À propos des sources d’audience propriétaires &#x200B;](/help/dsp/audiences/sources/source-about.md) » pour connaître les taux.

* Tous vos segments de données tiers personnalisés importés.

* (Emplacements ciblant les États-Unis uniquement) [Tous les segments de données tiers disponibles pour les clients DSP de plus de 30 fournisseurs](/help/dsp/audiences/third-party-data-providers.md) dont [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]), [!DNL Lotame], [!DNL Neustar], et bien d’autres.

  Vous pouvez cibler des segments spécifiques, qui ciblent les utilisateurs en fonction des données d’audience (par exemple, les utilisateurs avec des données démographiques spécifiques, des intérêts ou des intentions, et/ou des profils comportementaux). Vous pouvez effectuer une navigation par fournisseur de données et par catégorie, rechercher des segments par nom ou identifiant de segment, ou filtrer les résultats par fournisseur de données, taille du segment actif, nombre de navigateurs web ou nombre d’appareils.

  Third-party segments incur additional fees, which are indicated next to each segment name.

* (Advertisers with Adobe Experience Platform and [!DNL Real-Time CDP], Adobe Audience Manager, or Adobe Analytics who use Adobe Advertising JavaScript conversion tags only) All of your available first-, second-, or third-party audience segments created in [!DNL Real-Time CDP], created in Audience Manager, or published to Adobe CX Enterprise from Audience Manager or [!DNL Analytics].

  Pricing for the use of the segments is pre-negotiated and isn&#39;t visible in DSP.

  Segments from [!DNL Analytics] are available about an hour after you create or publish them as CX Enterprise audiences. Segments coming directly from Audience Manager or [!DNL Real-Time CDP] are available within 24 hours after you share them.

  >[!NOTE]
  >
  >See the documentation for [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html), and [the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) for information about setting up and collecting data for segments in those solutions.

## Audience size data

In Audiences > All Audiences and in the Audience Targeting section of placement settings, you can filter each segment list by size range, including separate ranges for specific device types or universal ID types.

![filter by audience size](/help/dsp/assets/audience-size-filter.png)

You can also see detailed audience size data:

* The active deduplicated audience size across all selected segments and saved audiences is displayed, and you can view details by device type (browser, mobile, or connected TV).

  ![the combined audience size](/help/dsp/assets/audience-size.png)

* For individual segments, the active audience size and CPM (when applicable) are displayed next to the segment name.

  ![the individual segment size](/help/dsp/assets/audience-size-segment.png)

* You can view more details about an individual segment or saved audience, including the size by browser, mobile, connected TV, and universal ID type partner. For saved audiences, the total active audience size is the deduplicated total.

  ![the individual segment or saved audience details](/help/dsp/assets/audience-size-segment-details.png)

## The [!UICONTROL Audiences] views

### The [!UICONTROL All Audiences] view

In the [!UICONTROL All Audiences] view, or Audience Library, you can save and manage reusable audiences, which include groups of audience segments and even other saved audiences. You can use audiences as targets for multiple placements. The number of placements in which each audience is used is indicated next to the placement name.

You can edit, clone, delete, export, or share any audience.

### The [!UICONTROL Segments] view

In the [!UICONTROL Segments] view, all users can create additional custom segments.

The [!UICONTROL Segments] view also lists the following segment types:

* All user-created custom segments available to the user.

  You can view tracking tags for any of the custom segments you created, and share those segments with other users. You can also edit or delete the custom segments you created.

  You can&#39;t edit or share custom segments that other users have shared with you.

* All first-party segments imported as-is that are available to the user.

  You can&#39;t edit or share first-party segments that were shared with you. Contact your Adobe Account Team if you need to share first-party segments with additional users.

* All custom third-party segments available to the user.

  You can&#39;t edit or share third-party segments that were shared with you. Contact your Adobe Account Team if you need to share third-party segments with additional users.

### The [!UICONTROL Sources] view

In the [!UICONTROL Sources] view, you can configure sources for first-party segments in supported customer data platforms that you want to convert to segments containing specified universal ID types. The source settings include an auto-generated source key, which you&#39;ll provide to your customer data platform to establish the connection.

For more information about the supported customer data platforms, supported universal ID types, and the workflows to set up connections to each customer data platform, see &quot;[About first-party audience sources](/help/dsp/audiences/sources/source-about.md).&quot;

The translated segments are available to include in reusable audiences and in placement settings for cookieless targeting.

>[!MORELIKETHIS]
>
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [Create a reusable audience](reusable-audience-create.md)
>* [Créer et implémenter un segment personnalisé](custom-segment-create.md)
>* [Création et implémentation d’un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](/help/dsp/audiences/sources/source-manage.md)
>* [Importer manuellement des segments authentifiés depuis  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
