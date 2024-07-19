---
title: Format des balises de suivi de conversion d’image
description: Référencez le format des balises de suivi de conversion d’image.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Format des balises de suivi de conversion d’image

>[!NOTE]
>
>Pour plus d’informations sur l’utilisation des balises d’image par rapport aux balises JavaScript, consultez la [FAQ sur les balises de suivi](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Balises non sécurisées pour les sites avec HTTP :

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Balises sécurisées pour les sites avec HTTPS :

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

où :

* `<ef-userid>` est un identifiant utilisateur numérique unique attribué à l’annonceur par Search, Social et Commerce.

* `<propertyname>` est la conversion à suivre. Par exemple, si vous effectuez le suivi d’une conversion appelée &quot;enregistrement&quot;, la balise inclut le paramètre `ev_registration=<registration>` et vous devez transmettre les recettes réelles pour chaque transaction (telles que `ev_registration=1`). Lorsque plusieurs propriétés sont suivies, elles sont unies par une esperluette (`&`), telle que `ev_registration=<registration>&ev_sale=<sale>` (par exemple, `ev_registration=1&ev_sale=12.99`). **Remarque :** Le nom de la propriété ne peut pas contenir de caractères spéciaux.

* `<transid>` est un identifiant de transaction unique (tel qu’un identifiant de commande réel) que l’annonceur génère et transmet pour identifier une transaction. Elle est incluse uniquement lorsque l’option &quot;[!UICONTROL Include unique transaction IDs]&quot; est sélectionnée.

  Search, Social et Commerce utilise l’ID de transaction pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété. L’ID de transaction est inclus dans le [!UICONTROL Transaction Report], que vous pouvez utiliser pour valider les données dans l’Adobe Advertising avec les données de l’annonceur. **Remarque :** Si les données de l’annonceur n’incluent pas d’identifiant unique par transaction, Search, Social et Commerce en génère toujours un en fonction de l’heure de la transaction.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [ À propos des balises de suivi de conversion d’Adobe Advertising ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Générer une balise de conversion d’Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [ Questions fréquentes sur les balises de suivi de conversion et de pages vues ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [ Format des balises de suivi de conversion JavaScript version 2](format-conversion-tag-jsv2.md)
>* [ Format des balises de suivi de conversion JavaScript version 3](format-conversion-tag-jsv3.md)
