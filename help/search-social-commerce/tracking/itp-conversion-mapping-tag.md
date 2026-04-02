---
title: La balise de mappage de conversion Adobe Advertising
description: Découvrez la balise de mappage de conversion basée sur JavaScript pour ITP 2.2, qui permet à Adobe Advertising de suivre un événement de conversion qui se produit sur une page qui n’est pas la page de destination.
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
TQID: https://experienceleague.adobe.com/gG9j9kbctKTam6mhevTy4jTf7f68iy26XQW5dDjd-ZA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 637
ht-degree: 0%

---

# Balise de mappage de conversion Adobe Advertising JavaScript

*Annonceurs avec suivi des conversions Adobe Advertising uniquement*

La balise de mappage de conversion basée sur Adobe Advertising JavaScript, lorsqu’elle est utilisée en plus de la balise de suivi des conversions Adobe Advertising JavaScript v2 ou v3, permet à Adobe Advertising de suivre un événement de conversion qui se produit sur une page qui n’est pas la page de destination. La solution ITP 2.2 stocke le cookie d’un utilisateur dans un enregistrement local dans un iFrame détenu par l’annonceur. Le stockage local peut ensuite conserver la valeur du cookie du clic en aval de la page de conversion.

Utilisez la balise de mappage de conversion pour vous assurer qu’Adobe Advertising peut suivre toutes les conversions qui se produisent dans les navigateurs Apple Safari et Mozilla Firefox, ce qui limite la persistance des cookies propriétaires. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

Pour utiliser la balise de mappage de conversion, procédez comme suit :

1. [Déployez la balise de mappage de conversion](#deploy-conversion-mapping-tag).

1. Si votre organisation utilise plusieurs identifiants d’organisation Adobe Experience Cloud Identity Service (anciennement appelés ID d’organisation IMS), [mettez à jour vos balises de conversion](#update-conversion-tags) pour inclure l’identifiant de l’organisation.

1. [Validez le déploiement de la balise](#validate-conversion-mapping).

## Déployez la balise de mappage de conversion JavaScript pour ITP 2.2. {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Si vous utilisez la balise de mappage de conversion JavaScript pour ITP 2.0, remplacez la balise existante dans toutes les pages de conversion par l’une des balises suivantes <!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Si votre organisation utilise un seul ID d’organisation, qui est utilisé pour votre compte Search, Social et Commerce, utilisez la balise suivante :

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  où vous remplacez `{AMO User ID}` par l’ID d’utilisateur unique de votre compte Search, Social et Commerce.

* Si votre organisation utilise plusieurs ID d’organisation, utilisez la balise suivante :

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  où :

   * vous remplacez la valeur `{xxxxxx@AdobeOrg}` par l’ID d’organisation pour lequel les conversions de la page sont suivies. Utilisez le même ID d’organisation pour toutes les pages de conversion.

   * vous remplacez `{AMO User ID}` par l’ID d’utilisateur unique pour votre compte Search, Social et Commerce.

* Si vous utilisez un système de gestion des balises qui ne prend pas en charge l’ajout de la variable `imsorgid` à la balise du script, utilisez plutôt le code suivant :

  *Si votre organisation utilise un seul ID d’organisation :

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  où vous remplacez `{AMO User ID}` par l’ID d’utilisateur unique de votre compte Search, Social et Commerce.

   * Si votre organisation utilise plusieurs ID d’organisation :

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     où :

      * vous remplacez la valeur `{xxxxxx@AdobeOrg}` par l’ID d’organisation pour lequel les conversions de la page sont suivies. Utilisez le même ID d’organisation pour toutes les pages de conversion.

      * vous remplacez `{AMO User ID}` par l’ID d’utilisateur unique pour votre compte Search, Social et Commerce.

Si vous ne connaissez pas la valeur de votre identifiant d’organisation ou de votre identifiant utilisateur Search, Social et Commerce, demandez à l’équipe chargée de votre compte Adobe.

### Exemples

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### Où ajouter la balise

Ajoutez la balise dans n’importe quelle page qui pourrait être une page de destination à partir d’un clic de recherche (idéalement, sur toutes les pages, car les pages de destination peuvent changer au fil du temps). Il doit être chargé avant la balise de tracking des conversions Adobe Advertising JavaScript v3 .

S’il est placé dans un iframe ou une balise conteneur, alors :

* L’iframe doit être au même niveau que le domaine de niveau supérieur.

* La balise de mappage de conversion ne doit se trouver qu’à un (1) niveau sous le domaine de niveau supérieur.

## Mise à jour des balises de conversion JavaScript {#update-conversion-tags}

Si votre organisation utilise plusieurs identifiants d’organisation, ajoutez l’identifiant d’organisation pour lequel les conversions d’une page sont suivies à vos balises de conversion JavaScript existantes.

Si votre organisation utilise un identifiant d’organisation, cette étape n’est pas nécessaire.

### Balises JavaScript V2

Ajoutez la chaîne suivante au début de la balise du script de conversion :

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

où vous remplacez la valeur `{xxxxxx@AdobeOrg}` par l’ID d’organisation pour lequel les conversions de la page sont suivies.

Exemple :

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

### Balises JavaScript V3

Une fois `window.EF` défini, ajoutez la chaîne suivante :

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

où vous remplacez la valeur `{xxxxxx@AdobeOrg}` par l’ID d’organisation pour lequel les conversions de la page sont suivies.

Exemple :

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        window.EF.imsorgid ="abc12345@AdobeOrg";
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

## Validation du déploiement des balises {#validate-conversion-mapping}

Demandez à l’équipe chargée de votre compte Adobe de vous aider à valider la balise de mappage de conversion et la balise de conversion standard (si vous l’avez mise à jour).
