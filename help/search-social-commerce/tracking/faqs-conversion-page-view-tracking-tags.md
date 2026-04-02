---
title: Questions fréquentes sur la conversion dans Adobe Advertising et les balises de suivi des pages vues
description: Comparez les balises de suivi des conversions et des pages vues d’Adobe Advertising.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
TQID: https://experienceleague.adobe.com/ckLRjqXGTShwM2TTyULRKjPwL5RYVWkiVVSkwMmvxE8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 0%

---

# Questions fréquentes sur la conversion dans Adobe Advertising et les balises de suivi des pages vues

Les éléments suivants s’appliquent aux balises de suivi des conversions et aux balises de suivi des pages vues d’Adobe Advertising.

| | Balises JS avec ECID | Balises JS version 3 | Balises JS version 2 | Balises d’image |
| ---- | ---- | ---- | ---- | ---- |
| Peut être utilisé sur la même page web qu’une autre version de JS. | — | — | — | s.o. |
| Permet l’utilisation de plusieurs balises avec les mêmes ID utilisateur d’annonceur sur la même page web | Oui | Oui | Oui | — |
| Permet l’utilisation de plusieurs balises avec différents ID utilisateur de l’annonceur sur la même page web | Oui | Oui | — | — |
| Utilisé par l’extension Adobe Advertising pour Adobe Experience Platform, et compatible avec d’autres balises générées à l’aide d’Experience Platform | Oui | Oui | — | — |
| Permet le suivi de toutes les conversions provenant de [!DNL Apple Safari] et [!DNL Mozilla Firefox] lorsqu’elles sont utilisées avec la balise de mappage de conversion Adobe Advertising JavaScript | Oui | Oui | Oui | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Toutes les nouvelles mises en œuvre utilisent JavaScript version 3.
>* La balise JavaScript avec ECID utilise le service [Adobe Experience Cloud ID (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=fr) ainsi que les anciens ef_id et gsurferid pour mesurer les conversions. Cette dernière balise crée des [cookies s_ecid Experience Cloud propriétaires](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html?lang=fr) et permet une intégration plus étroite à d’autres produits Experience Cloud.
>* N’utilisez les balises JavaScript version 2 que lorsqu’elles sont déjà implémentées sur les pages web de l’annonceur.
>* La bonne pratique consiste à utiliser les balises JavaScript plutôt que les balises d’image, sauf si le site applique une politique qui interdit leur utilisation.
>* Les balises JavaScript sont requises pour les annonceurs qui souhaitent cibler des audiences créées dans Adobe Experience Cloud, dans Adobe Audience Manager ou publiées sur Adobe Experience Cloud à partir d’Audience Manager ou d’Adobe Analytics.

>[!MORELIKETHIS]
>
>* [À propos des balises de suivi des conversions Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Générer une balise de conversion Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format des balises de suivi des conversions JavaScript version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Format des balises de suivi des conversions JavaScript version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Format des balises de tracking de conversion d’images](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!--
 add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
