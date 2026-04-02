---
title: Format des balises de suivi des conversions JavaScript version 3
description: Référencez le format des balises de suivi de conversion JavaScript version 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
TQID: https://experienceleague.adobe.com/IjPpsTp5GGaG6SM2k1UC0Q0J3QCF-jIR7-ug3yigW3U
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 0%

---

# Format des balises de suivi des conversions JavaScript version 3

Le format suivant s’applique aux sites qui utilisent HTTPS. Pour les sites qui utilisent HTTP, les URL doivent commencer par « http ».

>[!NOTE]
>
>Pour plus d’informations sur l’utilisation de la version 2 ou de la version 3, consultez les [FAQ sur le suivi des balises](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

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
        window.id5PartnerId=<ID5_PartnerID>
        window.EF = window.EF || {};
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

où :

* `<ef-userid>` est un identifiant utilisateur numérique unique attribué par Search, Social et Commerce à l’annonceur.

* `<ID5_PartnerID>` est l’ID de partenaire ID5 de l’organisation, que l’organisation reçoit après avoir signé un accord avec [!DNL ID5]. Incluez cette variable uniquement lorsque l’entreprise utilise DSP et dispose de segments [&#x200B; personnalisés qui effectuent le suivi des utilisateurs associés aux ID5 universels](/help/dsp/audiences/universal-ids.md).

* `<propertyname>` est la conversion à suivre. Par exemple, si vous effectuez le suivi d’une conversion appelée « enregistrement », la balise inclut le paramètre `ev_registration=<registration>` et vous devez transmettre le chiffre d’affaires réel pour chaque transaction (tel que `ev_registration=1`). Lorsque plusieurs propriétés sont suivies, elles sont reliées par une esperluette (`&`), telle que `ev_registration=<registration>&ev_sale=<sale>` (par exemple, `ev_registration=1&ev_sale=12.99`). **Remarque :** le nom de la propriété ne peut pas contenir de caractères spéciaux.

* `<transid>` est un ID de transaction unique (tel qu’un ID de commande réel) que l’annonceur génère et transmet pour identifier une transaction. Il n’est inclus que lorsque l’option « [!UICONTROL Include unique transaction IDs] » est sélectionnée.

  Search, Social et Commerce utilisent l’ID de transaction pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété. L’ID de transaction est inclus dans le [!UICONTROL Transaction Report]. Vous pouvez l’utiliser pour valider les données dans Adobe Advertising avec les données de l’annonceur. **Remarque :** si les données de l’annonceur n’incluent pas d’ID unique par transaction, Search, Social et Commerce en génère toujours un en fonction de l’heure de la transaction.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [À propos des balises de suivi des conversions Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Générer une balise de conversion Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [FAQ sur les balises de suivi des conversions et des pages vues](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format des balises de suivi des conversions JavaScript version 2](format-conversion-tag-jsv2.md)
>* [Format des balises de tracking de conversion d’images](format-conversion-tag-image.md)
