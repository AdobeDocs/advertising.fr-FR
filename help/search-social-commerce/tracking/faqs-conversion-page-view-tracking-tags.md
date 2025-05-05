---
title: Questions fréquentes sur les balises de suivi de conversion d’Adobe Advertising et de pages vues
description: Comparez les balises de suivi de conversion d’Adobe Advertising et de page vue.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: e9d55ba2f4b3ce8b1ac19c06fe8759a2f862c480
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Questions fréquentes sur les balises de suivi de conversion d’Adobe Advertising et de pages vues

Les éléments suivants s’appliquent aux balises de suivi de conversion d’Adobe Advertising et aux balises de suivi des pages vues.

| | Balises JS avec ECID | Balises JS Version 3 | Balises JS Version 2 | Balises d’image |
| ---- | ---- | ---- | ---- | ---- |
| Peut être utilisé sur la même page web qu’une autre version JS | — | — | — | n/a |
| Permet l’utilisation de plusieurs balises avec les mêmes identifiants d’utilisateur annonceur sur la même page web. | Oui | Oui | Oui | — |
| Permet l’utilisation de plusieurs balises avec différents identifiants utilisateur d’annonceurs sur la même page web. | Oui | Oui | — | — |
| Utilisé par l’extension Adobe Advertising pour Adobe Experience Platform et compatible avec d’autres balises générées à l’aide de Experience Platform | Oui | Oui | — | — |
| Permet le suivi de toutes les conversions provenant de [!DNL Apple Safari] et [!DNL Mozilla Firefox] lorsqu’elles sont utilisées avec la balise de mappage de conversion JavaScript Adobe Advertising | Oui | Oui | Oui | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Toutes les nouvelles mises en oeuvre utilisent JavaScript version 3.
>* La balise JavaScript avec ECID utilise le [service Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=fr) ainsi que l’ef_id et gsurferid hérités pour mesurer les conversions. Cette dernière balise crée des [cookies s_ecid Experience Cloud propriétaires](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html?lang=fr) et offre une intégration plus étroite avec d’autres produits Experience Cloud.
>* Utilisez les balises de la version 2 de JavaScript uniquement lorsqu’elles sont déjà implémentées sur les pages web de l’annonceur.
>* Il est recommandé d’utiliser les balises JavaScript plutôt que les balises d’image, sauf si le site a une politique contre leur utilisation.
>* Les balises JavaScript sont requises pour les annonceurs qui souhaitent cibler les audiences créées dans Adobe Experience Cloud, créées dans Adobe Audience Manager ou publiées sur Adobe Experience Cloud depuis Audience Manager ou Adobe Analytics.

>[!MORELIKETHIS]
>
>* [ À propos des balises de suivi de conversion d’Adobe Advertising ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Générer une balise de conversion d’Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [ Format des balises de suivi de conversion JavaScript version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [ Format des balises de suivi de conversion JavaScript version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format des balises de suivi de conversion d’image](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
