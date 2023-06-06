---
title: Questions fréquentes sur les balises de suivi de conversion d’Adobe Advertising et de pages vues
description: Consultez une comparaison des balises de suivi de conversion d’Adobe Advertising et de page vue.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Questions fréquentes sur les balises de suivi de conversion d’Adobe Advertising et de pages vues

Les éléments suivants s’appliquent aux balises de suivi de conversion d’Adobe Advertising et aux balises de suivi des pages vues.

|  | Balises JS avec ECID | Balises JS Version 3 | Balises JS Version 2 | Balises d’image |
| ---- | ---- | ---- | ---- | ---- |
| Peut être utilisé sur la même page web qu’une autre version JS | — | — | — | n/a |
| Permet l’utilisation de plusieurs balises avec les mêmes identifiants d’utilisateur annonceur sur la même page web. | Oui | Oui | Oui | — |
| Permet l’utilisation de plusieurs balises avec différents identifiants utilisateur d’annonceurs sur la même page web. | Oui | Oui | Non | Non |
| Utilisé par l’extension Adobe Advertising pour Adobe Experience Platform et compatible avec d’autres balises générées à l’aide d’Experience Platform | Oui | Oui | — | — |
| Autorise toutes les conversions issues de [!DNL Apple Safari] et [!DNL Mozilla Firefox] à tracker lors de l’utilisation de la balise de mappage de conversion JavaScript Adobe Advertising | Oui | Oui | Oui | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Toutes les nouvelles mises en oeuvre utilisent JavaScript version 3.
>* La balise JavaScript avec ECID utilise la variable [Service Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) ainsi que l’ef_id et gsurferid hérités pour mesurer les conversions. Cette dernière balise crée [cookies s_ecid Experience Cloud propriétaires](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) et offre une intégration plus étroite avec d’autres produits Experience Cloud.
>* Utilisez les balises JavaScript version 2 uniquement lorsqu’elles sont déjà implémentées sur les pages web de l’annonceur.
>* Il est recommandé d’utiliser des balises JavaScript plutôt que des balises d’image, sauf si le site a une politique contre leur utilisation.
>* Les balises JavaScript sont requises pour les annonceurs qui souhaitent cibler les audiences créées dans Adobe Experience Cloud, créées dans Adobe Audience Manager ou publiées sur Adobe Experience Cloud à partir d’Audience Manager ou d’Adobe Analytics.


>[!MORELIKETHIS]
>
>* [À propos des balises de suivi de conversion Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Génération d’une balise de conversion Advertising Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format des balises de suivi de conversion JavaScript version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format des balises de suivi de conversion JavaScript version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format des balises de suivi de conversion d’image](/help/search-social-commerce/tracking/format-conversion-tag-image.md)


<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
