---
title: Format des balises de tracking de conversion d’images
description: Référencez le format des balises de suivi de conversion d’images.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TQMACo5-LkbCU2SiMmUE-ZDBRTb8NERQPQ9ISzU0DdU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 0%

---

# Format des balises de tracking de conversion d’images

>[!NOTE]
>
>Pour plus d’informations sur l’utilisation des balises d’image par rapport aux balises JavaScript, consultez la [FAQ sur les balises de suivi](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Balises non sécurisées pour les sites utilisant le protocole HTTP :

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Balises sécurisées pour les sites utilisant HTTPS :

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

où :

* `<ef-userid>` est un identifiant utilisateur numérique unique attribué par Search, Social et Commerce à l’annonceur.

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
