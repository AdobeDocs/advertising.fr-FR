---
title: Format des balises de suivi de conversion d’image
description: Référencez le format des balises de suivi de conversion d’image.
source-git-commit: b230c593d93dfa868b8f075939fc9940ea74fa13
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Format des balises de suivi de conversion d’image

>[!NOTE]
>
>Pour plus d’informations sur l’utilisation des balises d’image par rapport aux balises JavaScript, voir [Questions fréquentes sur les balises de suivi](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Balises non sécurisées pour les sites avec HTTP :

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Balises sécurisées pour les sites avec HTTPS :

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

où :

* `<ef-userid>` est un identifiant utilisateur numérique unique attribué par Search, Social et Commerce à l’annonceur.

* `<propertyname>` est la conversion qui sera suivie. Par exemple, si vous effectuez le suivi d’une conversion appelée &quot;enregistrement&quot;, la balise inclura le paramètre . `ev_registration=<registration>`, et vous devez transmettre les recettes réelles pour chaque transaction (comme `ev_registration=1`). Lorsque plusieurs propriétés sont suivies, elles sont unies par une esperluette (`&`), par exemple `ev_registration=<registration>&ev_sale=<sale>` (par exemple, `ev_registration=1&ev_sale=12.99`). **Remarque :**  Le nom de la propriété ne peut pas contenir de caractères spéciaux.

* `<transid>` est un identifiant de transaction unique (tel qu’un identifiant de commande réel) que l’annonceur génère et transmet pour identifier une transaction. Elle est incluse uniquement lorsque la variable[!UICONTROL Include unique transaction IDs]&quot; est sélectionnée.

  Search, Social et Commerce utilise l’ID de transaction pour éliminer les transactions en double avec le même ID de transaction et la même valeur de propriété. L’ID de transaction est inclus dans la variable [!UICONTROL Transaction Report], que vous pouvez utiliser pour valider des données dans Adobe Advertising avec les données de l’annonceur. **Remarque :** Si les données de l’annonceur n’incluent pas d’identifiant unique par transaction, Search, Social et Commerce en génère toujours un en fonction de l’heure de la transaction.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [À propos des balises de suivi de conversion Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Génération d’une balise de conversion Advertising Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Questions fréquentes sur les balises de suivi de conversion et de pages vues](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format des balises de suivi de conversion JavaScript version 2](format-conversion-tag-jsv2.md)
>* [Format des balises de suivi de conversion JavaScript version 3](format-conversion-tag-jsv3.md)
