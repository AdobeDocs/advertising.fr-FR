---
title: JavaScript code for [!DNL Analytics for Advertising]
description: JavaScript code for [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
TQID: https://experienceleague.adobe.com/g9onwe1IQl1kbyQ82W2KmODPGUAReKiotxy65yCZcNY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 941
ht-degree: 0%

---

# JavaScript code for [!DNL Analytics for Advertising]

*Annonceurs avec Advertising DSP uniquement*

For Advertising DSP, the [!DNL Analytics for Advertising] integration tracks view-through and click-through site interactions. Click-through visits are tracked by the standard Adobe Analytics code on your webpages; the [!DNL Analytics] code captures the AMO ID and EF ID parameters in the landing page URL and tracks them in their respective reserved [!DNL eVars]. You can track view-through visits by deploying a JavaScript snippet in your webpages.

On the first page view of a visit to the site, the Adobe Advertising JavaScript code checks to see if the visitor has previously seen or clicked on an ad. If the user has previously entered the site via a click-through or hasn&#39;t seen an ad, then the visitor is ignored. If the visitor has seen an ad and hasn&#39;t entered the site via a click-through during the [click lookback window](/help/integrations/analytics/prerequisites.md#lookback-a4adc) set within Adobe Advertising, then the Adobe Advertising JavaScript code either a) uses the [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) to generate a supplemental ID (`SDID`) or b) uses the Adobe Experience Platform [!DNL Web SDK] `generateRandomID` method to generate a `[!DNL StitchID]`. Either ID is used to stitch data from Adobe Advertising to the visitor&#39;s Adobe Analytics hit. Adobe Analytics then queries Adobe Advertising for the AMO ID and EF ID associated with the ad exposure. The AMO ID and EF IDs are then populated in their respective [!DNL eVars]. These values persist for a designated period (by default, 60 days).

[!DNL Analytics] sends site traffic metrics (such as page views, visits, and time spent) and any [!DNL Analytics] custom or standard events to Adobe Advertising hourly, using the EF ID as the key. These [!DNL Analytics] metrics then run through the Adobe Advertising attribution system to connect the conversions to the click and exposure history.

>[!NOTE]
>
>The Adobe Advertising JavaScript tracking logic occurs on the Adobe side and thus has virtually no impact to the page load time.
>
>In contrast, the logic for the [!DNL DCM] data connector to [!DNL Analytics] (using [!DNL Google Campaign Manager 360]) for Advertising DSP occurs on the client side. Client-side stitching slows down the page load and increases the risk of data loss. This occurs because the [!DNL Analytics] JavaScript must ping [!DNL DoubleClick] and wait for [!DNL DoubleClick] to pass back the last click/impression data to [!DNL Analytics]. When your [!DNL DSP] team sets up the [!DNL DCM] data connector, you must specify how long you&#39;re willing to delay the page.

<!--
## Deploying the JavaScript code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The standard code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional code to import first-party segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5's technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Deploying the JavaScript code

The JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. Si l’intégration [!DNL Analytics for Advertising] a été terminée lors de la mise en œuvre d’Adobe Advertising, vous devez déjà avoir reçu ce code avec des instructions sur la manière de le déployer.

### Le code

#### Implémentations qui utilisent le code `visitorAPI.js` d’Experience Cloud Identity Service

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implémentations qui utilisent le code [!DNL Web SDK] Experience Platform `alloy.js`

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Où placer le code

La fonction [!DNL Analytics for Advertising] JavaScript doit se placer après le service Experience Cloud ID, mais avant le code Analytics App Measurement. Cela permet de s’assurer que l’ID supplémentaire (`SDID`) ou le `[!DNL StitchID]` est inclus dans votre appel Analytics.

![Code emplacement](/help/integrations/assets/a4adc-code-placement.png)

### Validation du déploiement du code

Vous pouvez effectuer une validation à l’aide de n’importe quel type d’outil de renifleur de paquets (tel que [!DNL Charles], [!DNL Fiddler] ou [!DNL Chrome Developer Tools]) en comparant les valeurs des quatre identifiants entre la requête envoyée à Adobe Advertising et la requête envoyée à [!DNL Analytics], comme indiqué ci-dessous.

#### Comment confirmer le code avec [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Ouvrez [!DNL Chrome Developer Tools] et cliquez sur l’onglet **Réseau**.

1. Chargez une page de site web contenant le JavaScript [!DNL Analytics for Advertising].

1. Filtrez l’onglet [!UICONTROL Network] par `last` et passez en revue deux lignes :

   ![Filtrage le dernier](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La première ligne correspond à l’appel à la bibliothèque JavaScript et est intitulée `last-event-tag-latest.min.js`.
   * La deuxième ligne correspond à l’appel qui envoie la demande à Adobe Advertising. Elle commence comme suit : `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Si vous ne voyez pas l’appel à Adobe Advertising, il se peut que ce ne soit pas la première page vue de votre visite. À des fins de test, vous pouvez supprimer le cookie afin que l’appel suivant soit la première page vue pour la visite correspondante :

   1. Dans l’onglet Application , recherchez le cookie `adcloud` et vérifiez qu’il contient des `_les_v` (dernière visite) avec une valeur de `y` et un horodatage UTC qui expire dans 30 minutes.
      1. Supprimez le cookie `adcloud` et actualisez la page.

1. (Implémentations qui utilisent le code de `visitorAPI.js` Experience Cloud Identity Service) Filtrez les `/b/ss` pour afficher l’accès Analytics.

   ![Filtrage sur `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implémentations qui utilisent Experience Platform [!DNL Web SDK] `alloy.js`code) Filtrez sur les `/interact` pour vérifier que la payload de la requête envoyée à Edge Network contient des `advertisingStitchID`.

   ![Filtrage sur `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Compare the ID values between the two hits. All of the values should be in query string parameters except for the report suite ID in the Analytics hit, which is the URL path immediately after `/b/ss/`.

   | ID | Analytics Parameter | Edge Network | Adobe Advertising Parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS Org | `mcorgid` |  | `_les_imsOrgid` |
   | Supplemental Data ID | sdid |  | `_les_sdid` |
   | Stitch ID | stitchId | `advertisingStitchID` under the `_adcloud` property |  |
   | Analytics Report Suite | The value after `/b/ss/` | | `_les_rsid` |
   | Experience Cloud Visitor ID | mid |  | `_les_mid` |

   If the ID values match, then the JavaScript implementation is confirmed. Adobe Advertising sends the [!DNL Analytics] server any click-through or view-through tracking details if they exist.

#### Comment confirmer le code avec [!DNL Adobe Experience Platform Debugger]

1. Open [the [!DNL Adobe Experience Platform Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) on your homepage.
1. Go to the [!UICONTROL Network] tab.
1. In the [!UICONTROL Solutions Filter] toolbar, click [!UICONTROL Adobe Advertising] and [!UICONTROL Analytics].
1. In the [!UICONTROL Request URL - Hostname] parameter row, locate `lasteventf-tm.everesttech.net`.
1. In the [!UICONTROL Request - Parameters] row, audit the signals generated, similar to Step 3 in &quot;[How to Confirm the Code with [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code) Make sure the `Sdid` parameter matches the `Supplemental Data ID` in the Adobe Analytics filter.
   * (Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code) Make sure the value of the `advertisingStitchID` parameter matches the `Sdid` sent to the Experience Platform Edge Network.
   * If the code isn&#39;t generating, then check to make sure the Adobe Advertising cookie has been removed in the [!UICONTROL Application] tab. Once it&#39;s removed, refresh the page and repeat the process.

   ![Auditing [!DNL Analytics for Advertising] JavaScript code in [!DNL Platform Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Prerequisites and key information for implementing [!DNL Analytics for Advertising]](prerequisites.md)
