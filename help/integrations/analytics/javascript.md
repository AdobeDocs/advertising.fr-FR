---
title: Code JavaScript pour  [!DNL Analytics for Advertising]
description: Code JavaScript pour  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# Code JavaScript pour [!DNL Analytics for Advertising]

*Annonceurs avec Advertising DSP uniquement*

Pour Advertising DSP, l’intégration [!DNL Analytics for Advertising] effectue le suivi des interactions entre les affichages publicitaires et les clics publicitaires du site. Les visites de clics publicitaires sont suivies par le code Adobe Analytics standard sur vos pages web ; le code [!DNL Analytics] capture les paramètres AMO ID et EF ID dans l’URL de la page de destination et les suit dans leurs [!DNL eVars] réservés respectifs. Vous pouvez effectuer le suivi des visites d’affichage publicitaire en déployant un fragment de code JavaScript dans vos pages web.

Sur la première page vue d’une visite sur le site, le code Adobe Advertising JavaScript vérifie si le visiteur a déjà vu ou cliqué sur une annonce publicitaire. Si l’utilisateur est déjà entré sur le site par le biais d’un clic publicitaire ou s’il n’a pas vu d’annonce publicitaire, le visiteur est ignoré. Si le visiteur a vu une annonce publicitaire et n’est pas entré sur le site par le biais d’un clic publicitaire au cours de l’intervalle de recherche en amont [clic](/help/integrations/analytics/prerequisites.md#lookback-a4adc) défini dans Adobe Advertising, alors le code Adobe Advertising JavaScript a) utilise le service [Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=fr) pour générer un ID supplémentaire (`SDID`) ou b) utilise la méthode [!DNL Web SDK] de l’`generateRandomID` Adobe Experience Platform pour générer un `[!DNL StitchID]`. Les deux ID sont utilisés pour regrouper les données d’Adobe Advertising vers l’accès Adobe Analytics du visiteur. Adobe Analytics interroge ensuite Adobe Advertising pour obtenir l’AMO ID et l’EF ID associés à l’exposition publicitaire. Les ID AMO et EF sont ensuite renseignés dans leurs [!DNL eVars] respectifs. Ces valeurs persistent pendant une période désignée (par défaut, 60 jours).

[!DNL Analytics] envoie toutes les heures à Adobe Advertising les mesures de trafic sur le site (telles que les pages vues, les visites et le temps passé) et tous les événements [!DNL Analytics] personnalisés ou standard, en utilisant l’identifiant d’événement d’urgence comme clé. Ces mesures de [!DNL Analytics] s’exécutent ensuite dans le système d’attribution d’Adobe Advertising pour connecter les conversions à l’historique des clics et de l’exposition.

>[!NOTE]
>
>La logique de suivi Adobe Advertising JavaScript se produit du côté d’Adobe et n’a donc quasiment aucun impact sur le temps de chargement de la page.
>
>En revanche, la logique du connecteur de données [!DNL DCM] à [!DNL Analytics] (à l’aide de [!DNL Google Campaign Manager 360]) pour Advertising DSP se produit côté client. L’assemblage côté client ralentit le chargement de la page et augmente le risque de perte de données. Cela se produit, car le JavaScript [!DNL Analytics] doit envoyer un ping à [!DNL DoubleClick] et attendre que les [!DNL DoubleClick] retransmettent les données de dernier clic/impression à [!DNL Analytics]. Lorsque votre équipe de [!DNL DSP] configure le connecteur de données [!DNL DCM], vous devez spécifier la durée pendant laquelle vous êtes prêt à retarder la page.

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

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Déploiement du code JavaScript

La bibliothèque JavaScript se compose de deux lignes qui permettent à [!DNL Analytics] et à Adobe Advertising de communiquer entre eux. Si l’intégration [!DNL Analytics for Advertising] a été terminée lors de la mise en œuvre d’Adobe Advertising, vous devez déjà avoir reçu ce code avec des instructions sur la manière de le déployer.

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

1. Comparez les valeurs des identifiants entre les deux accès. Toutes les valeurs doivent être dans des paramètres de chaîne de requête, à l’exception de l’identifiant de suite de rapports dans l’accès Analytics, qui est le chemin d’URL immédiatement après `/b/ss/`.

   | ID | Paramètre Analytics | Edge Network | Paramètre Adobe Advertising |
   | --- | --- | --- | --- |
   | Organisation IMS Experience Cloud | `mcorgid` |  | `_les_imsOrgid` |
   | ID de données supplémentaires | sdid |  | `_les_sdid` |
   | ID d’assemblage | stitchId | `advertisingStitchID` sous la propriété `_adcloud` |  |
   | Suite de rapports Analytics | La valeur après `/b/ss/` | | `_les_rsid` |
   | Identifiant visiteur Experience Cloud | mid |  | `_les_mid` |

   Si les valeurs d’ID correspondent, l’implémentation de JavaScript est confirmée. Adobe Advertising envoie au serveur de [!DNL Analytics] tous les détails de suivi des clics publicitaires ou des affichages publicitaires s’ils existent.

#### Comment confirmer le code avec [!DNL Adobe Experience Cloud Debugger]

1. Ouvrez le [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=fr) sur votre page d’accueil.
1. Accédez à l’onglet [!UICONTROL Network] .
1. Dans la barre d’outils [!UICONTROL Solutions Filter], cliquez sur [!UICONTROL Adobe Advertising] et [!UICONTROL Analytics].
1. Dans la ligne de paramètre [!UICONTROL Request URL - Hostname], recherchez `lasteventf-tm.everesttech.net`.
1. Dans la ligne [!UICONTROL Request - Parameters], vérifiez les signaux générés, comme à l’étape 3 de la rubrique [&#x200B; Confirmer le code avec  [!DNL Chrome Developer Tools]](#validate-js-chrome).
   * (Implémentations qui utilisent le code de `visitorAPI.js` Experience Cloud Identity Service) Assurez-vous que le paramètre `Sdid` correspond au `Supplemental Data ID` dans le filtre Adobe Analytics.
   * (Implémentations qui utilisent Experience Platform [!DNL Web SDK] `alloy.js`code) Assurez-vous que la valeur du paramètre `advertisingStitchID` correspond au `Sdid` envoyé à Experience Platform Edge Network.
   * Si le code n’est pas généré, vérifiez que le cookie Adobe Advertising a été supprimé dans l’onglet [!UICONTROL Application] . Une fois la suppression effectuée, actualisez la page et répétez le processus.

   ![Audit [!DNL Analytics for Advertising] code JavaScript dans [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Conditions préalables et informations clés pour l’implémentation de  [!DNL Analytics for Advertising]](prerequisites.md)
