---
title: Format des balises de suivi de conversion JavaScript version 2
description: Référencez le format des balises de suivi de conversion JavaScript version 2.
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Format des balises de suivi de conversion JavaScript version 2

Le format suivant est destiné aux sites qui utilisent le protocole HTTPS. Pour les sites qui utilisent HTTP, les URL doivent commencer par &quot;http&quot;.

>[!NOTE]
>
>Pour plus d’informations sur l’utilisation de la version 2 ou de la version 3, voir [Questions fréquentes sur les balises de suivi](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
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

* `<propertyname>` correspond à la conversion à suivre. Par exemple, si vous effectuez le suivi d’une conversion appelée &quot;enregistrement&quot;, la balise inclura le paramètre . `ev_registration=<registration>`, et vous devez transmettre les recettes réelles pour chaque transaction (comme `ev_registration=1`). Lorsque plusieurs propriétés sont suivies, elles sont unies par une esperluette (`&`), par exemple `ev_registration=<registration>&ev_sale=<sale>` (par exemple, `ev_registration=1&ev_sale=12.99`). **Remarque :**  Le nom de la propriété ne peut pas contenir de caractères spéciaux.

* `<transid>` est un identifiant de transaction unique (tel qu’un identifiant de commande réel) que l’annonceur génère et transmet pour identifier une transaction. Elle est incluse uniquement lorsque la variable[!UICONTROL Include unique transaction IDs]&quot; est sélectionnée.

  Search, Social et Commerce utilise l’ID de transaction pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété. L’ID de transaction est inclus dans la variable [!UICONTROL Transaction Report], que vous pouvez utiliser pour valider les données dans Adobe Advertising avec les données de l’annonceur. **Remarque :** Si les données de l’annonceur n’incluent pas d’identifiant unique par transaction, Search, Social et Commerce en génère toujours un en fonction de l’heure de la transaction.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [À propos des balises de suivi de conversion d’Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Génération d’une balise de conversion d’Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Questions fréquentes sur les balises de suivi de conversion et de pages vues](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format des balises de suivi de conversion JavaScript version 2](format-conversion-tag-jsv2.md)
>* [Format des balises de suivi de conversion JavaScript version 3](format-conversion-tag-jsv3.md)
>* [Format des balises de suivi de conversion d’image](format-conversion-tag-image.md)
