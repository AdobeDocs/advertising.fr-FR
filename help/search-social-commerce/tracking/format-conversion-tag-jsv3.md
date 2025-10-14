---
title: Format des balises de suivi de conversion JavaScript version 3
description: Référencez le format des balises de suivi de conversion JavaScript version 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
source-git-commit: dda4ff8e7538bc742caa50862575cb4e46a1371d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Format des balises de suivi de conversion JavaScript version 3

Le format suivant est destiné aux sites qui utilisent le protocole HTTPS. Pour les sites qui utilisent HTTP, les URL doivent commencer par &quot;http&quot;.

>[!NOTE]
>
>Pour plus d’informations sur l’utilisation de la version 2 par rapport à la version 3, consultez la [FAQ sur les balises de suivi](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

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

* `<ef-userid>` est un identifiant utilisateur numérique unique attribué à l’annonceur par Search, Social et Commerce.

* `<ID5_PartnerID>` est l’ID de partenaire ID5 de l’organisation, que l’organisation reçoit après la signature d’un accord avec [!DNL ID5]. N’incluez cette variable que lorsque l’organisation utilise DSP et possède des [segments personnalisés qui effectuent le suivi des utilisateurs associés aux ID universels ID5](/help/dsp/audiences/universal-ids.md).

* `<propertyname>` est la conversion à suivre. Par exemple, si vous effectuez le suivi d’une conversion appelée &quot;enregistrement&quot;, la balise inclut le paramètre `ev_registration=<registration>` et vous devez transmettre les recettes réelles pour chaque transaction (telles que `ev_registration=1`). Lorsque plusieurs propriétés sont suivies, elles sont unies par une esperluette (`&`), telle que `ev_registration=<registration>&ev_sale=<sale>` (par exemple, `ev_registration=1&ev_sale=12.99`). **Remarque :** Le nom de la propriété ne peut pas contenir de caractères spéciaux.

* `<transid>` est un identifiant de transaction unique (tel qu’un identifiant de commande réel) que l’annonceur génère et transmet pour identifier une transaction. Elle est incluse uniquement lorsque l’option &quot;[!UICONTROL Include unique transaction IDs]&quot; est sélectionnée.

  Search, Social et Commerce utilise l’ID de transaction pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété. L’ID de transaction est inclus dans le [!UICONTROL Transaction Report], que vous pouvez utiliser pour valider les données dans l’Adobe Advertising avec les données de l’annonceur. **Remarque :** Si les données de l’annonceur n’incluent pas d’identifiant unique par transaction, Search, Social et Commerce en génère toujours un en fonction de l’heure de la transaction.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [&#x200B; À propos des balises de suivi de conversion d’Adobe Advertising &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Générer une balise de conversion d’Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [&#x200B; Questions fréquentes sur les balises de suivi de conversion et de pages vues &#x200B;](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [&#x200B; Format des balises de suivi de conversion JavaScript version 2](format-conversion-tag-jsv2.md)
>* [Format des balises de suivi de conversion d’image](format-conversion-tag-image.md)
