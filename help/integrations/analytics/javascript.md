---
title: Code JavaScript pour [!DNL Analytics for Advertising]
description: Code JavaScript pour [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# Code JavaScript pour [!DNL Analytics for Advertising]

*Annonceurs avec Advertising DSP uniquement*

Pour Advertising DSP, l’intégration [!DNL Analytics for Advertising] effectue le suivi des interactions de site affichant et affichant les clics publicitaires. Les visites des clics publicitaires sont suivies par le code Adobe Analytics standard sur vos pages web ; le code [!DNL Analytics] capture les paramètres AMO ID et EF ID dans l’URL de la page d’entrée et les suit dans leurs [!DNL eVars] réservés respectifs. Vous pouvez effectuer le suivi des visites d’affichage publicitaire en déployant un fragment de code JavaScript dans vos pages web.

Sur la première page vue d’une visite sur le site, le code Adobe Advertising JavaScript vérifie si le visiteur a déjà vu ou cliqué sur une publicité. Si l’utilisateur a déjà accédé au site par le biais d’un clic publicitaire ou n’a pas vu de publicité, le visiteur est ignoré. Si le visiteur a vu une publicité et n’est pas entré sur le site par le biais d’un clic publicitaire pendant la [ période de recherche en amont des clics ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) définie dans Adobe Advertising, le code JavaScript d’Adobe Advertising utilise a) le [service d’ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) pour générer un ID supplémentaire (`SDID`) ou b) utilise la méthode Adobe Experience Platform [!DNL Web SDK] `generateRandomID` pour générer un `[!DNL StitchID]`. L’un ou l’autre des identifiants est utilisé pour associer les données de l’Adobe Advertising à l’accès Adobe Analytics du visiteur. Adobe Analytics interroge ensuite l’Adobe Advertising pour l’AMO ID et l’EF ID associés à l’exposition publicitaire. Les AMO ID et EF ID sont ensuite renseignés dans leurs [!DNL eVars] respectifs. Ces valeurs persistent pendant une période donnée (60 jours par défaut).

[!DNL Analytics] envoie les mesures de trafic du site (telles que les pages vues, les visites et la durée de la visite) et tout [!DNL Analytics] événement personnalisé ou standard à Adobe Advertising toutes les heures, à l’aide de l’identifiant EF comme clé. Ces [!DNL Analytics] mesures s’exécutent ensuite par le biais du système d’attribution d’Adobe Advertising pour connecter les conversions à l’historique des clics et des expositions.

>[!NOTE]
>
>La logique de suivi JavaScript de l’Adobe Advertising se produit côté Adobe et n’a donc pratiquement aucun impact sur le temps de chargement de la page.
>
>En revanche, la logique du connecteur de données [!DNL DCM] vers [!DNL Analytics] (utilisant [!DNL Google Campaign Manager 360]) pour Advertising DSP se produit côté client. L’assemblage côté client ralentit le chargement de la page et augmente le risque de perte de données. Cela se produit car [!DNL Analytics] JavaScript doit effectuer un test ping [!DNL DoubleClick] et attendre que [!DNL DoubleClick] retransmet les dernières données de clic/impression à [!DNL Analytics]. Lorsque votre équipe [!DNL DSP] configure le connecteur de données [!DNL DCM], vous devez spécifier la durée pendant laquelle vous souhaitez retarder la page.

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

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

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Déploiement du code JavaScript

La bibliothèque JavaScript se compose de deux lignes qui permettent à [!DNL Analytics] et à l’Adobe Advertising de communiquer entre eux. Si l’intégration [!DNL Analytics for Advertising] a été effectuée pendant la mise en oeuvre de l’Adobe Advertising, vous avez déjà reçu ce code avec des instructions sur la manière de le déployer.

### Le code

#### Mises en oeuvre qui utilisent le code du service Identity Experience Cloud `visitorAPI.js`

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Mises en oeuvre qui utilisent le code [!DNL Web SDK] `alloy.js`Experience Platform

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Emplacement du code

La fonction JavaScript [!DNL Analytics for Advertising] doit se trouver après le service d’identification de l’Experience Cloud, mais avant votre code Analytics App Measurement. Cela garantit que l’ID supplémentaire (`SDID`) ou `[!DNL StitchID]` est inclus dans votre appel Analytics.

![Emplacement du code](/help/integrations/assets/a4adc-code-placement.png)

### Validation du déploiement du code

Vous pouvez effectuer la validation à l’aide de n’importe quel type d’outil de renifleur de paquets (tel que [!DNL Charles], [!DNL Fiddler] ou [!DNL Chrome Developer Tools]) en comparant les valeurs des quatre identifiants entre la requête qui sera Adobe Advertising et la requête qui sera [!DNL Analytics], comme indiqué ci-dessous.

#### Comment confirmer le code avec [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Ouvrez [!DNL Chrome Developer Tools] et cliquez sur l&#39;onglet **Réseau** .

1. Chargez une page de site web qui contient le JavaScript [!DNL Analytics for Advertising].

1. Filtrez l’onglet [!UICONTROL Network] par `last` et passez en revue deux lignes :

   ![Filtrage sur la dernière](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La première ligne correspond à l’appel à la bibliothèque JavaScript et est intitulée `last-event-tag-latest.min.js`.
   * La deuxième ligne correspond à l’appel envoyant la demande à Adobe Advertising. Il commence comme suit : `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Si vous ne voyez pas l’appel à Adobe Advertising, il se peut qu’il ne s’agisse pas de la première page vue de votre visite. À des fins de test, vous pouvez supprimer le cookie afin que l’appel suivant soit la première page vue de la visite correspondante :

   1. Dans l’onglet Application , recherchez le cookie `adcloud` et vérifiez que le cookie contient `_les_v` (dernière visite) avec une valeur `y` et un horodatage d’époque UTC qui expire dans 30 minutes.
      1. Supprimez le cookie `adcloud` et actualisez la page.

1. (Implémentations qui utilisent le code du service Identity Experience Cloud `visitorAPI.js`) Filtrez sur `/b/ss` pour afficher l’accès Analytics.

   ![Filtrage sur `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implémentations qui utilisent le filtre [!DNL Web SDK] `alloy.js`code) Experience Platform sur `/interact` pour vérifier que le payload de requête de l’Edge Network contient `advertisingStitchID`.

   ![Filtrage sur `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Comparez les valeurs d’identifiant entre les deux accès. Toutes les valeurs doivent se trouver dans les paramètres de chaîne de requête, à l’exception de l’identifiant de suite de rapports dans l’accès Analytics, qui est le chemin d’accès à l’URL immédiatement après `/b/ss/`.

   | ID | Paramètre Analytics | Edge Network | Paramètre d’Adobe Advertising |
   | --- | --- | --- | --- |
   | Organisation IMS Experience Cloud | `mcorgid` |  | `_les_imsOrgid` |
   | ID de données supplémentaire | sdid |  | `_les_sdid` |
   | Identifiant d’assemblage | stitchId | `advertisingStitchID` sous la propriété `_adcloud` |  |
   | Suite de rapports Analytics | La valeur après `/b/ss/` | | `_les_rsid` |
   | Identifiant visiteur Experience Cloud | mid |  | `_les_mid` |

   Si les valeurs d’identifiant correspondent, l’implémentation de JavaScript est confirmée. Adobe Advertising envoie au serveur [!DNL Analytics] les détails de suivi des clics ou des affichages publicitaires s’ils existent.

#### Comment confirmer le code avec [!DNL Adobe Experience Cloud Debugger]

1. Ouvrez le [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) sur votre page d’accueil.
1. Accédez à l’onglet [!UICONTROL Network] .
1. Dans la barre d’outils [!UICONTROL Solutions Filter], cliquez sur [!UICONTROL Adobe Advertising] et [!UICONTROL Analytics].
1. Dans la ligne de paramètre [!UICONTROL Request URL - Hostname], recherchez `lasteventf-tm.everesttech.net`.
1. Sur la ligne [!UICONTROL Request - Parameters], effectuez un audit des signaux générés, comme à l’étape 3 de &quot;[ How to Confirm the Code with [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * (Implémentations qui utilisent le code du service Identity Experience Cloud `visitorAPI.js`) Assurez-vous que le paramètre `Sdid` correspond au `Supplemental Data ID` dans le filtre Adobe Analytics.
   * (Implémentations qui utilisent le code [!DNL Web SDK] `alloy.js`Experience Platform) Assurez-vous que la valeur du paramètre `advertisingStitchID` correspond au `Sdid` envoyé à l’Edge Network Experience Platform.
   * Si le code n’est pas généré, vérifiez que le cookie d’Adobe Advertising a été supprimé dans l’onglet [!UICONTROL Application]. Une fois supprimé, actualisez la page et répétez le processus.

   ![Audit [!DNL Analytics for Advertising] du code JavaScript dans [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Conditions préalables et informations clés pour la mise en oeuvre  [!DNL Analytics for Advertising]](prerequisites.md)
