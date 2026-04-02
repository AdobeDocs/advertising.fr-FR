---
title: Format des balises de suivi des conversions JavaScript version 2
description: Référencez le format des balises de suivi de conversion JavaScript version 2.
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
TQID: https://experienceleague.adobe.com/WKh16jULfv2I-P7SEm9oP9O933KYNIZNPiIe9FD2xro
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 0%

---

# Format des balises de suivi des conversions JavaScript version 2

Le format suivant s’applique aux sites qui utilisent HTTPS. Pour les sites qui utilisent HTTP, les URL doivent commencer par « http ».

>[!NOTE]
>
>Pour plus d’informations sur l’utilisation de la version 2 ou de la version 3, consultez les [FAQ sur le suivi des balises](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
window.id5PartnerId=<ID5_PartnerID>
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
>* [Format des balises de suivi des conversions JavaScript version 3](format-conversion-tag-jsv3.md)
>* [Format des balises de tracking de conversion d’images](format-conversion-tag-image.md)
