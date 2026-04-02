---
title: Mesures  [!DNL Google Analytics]  disponibles
description: Référencez les mesures  [!DNL Google Analytics]  pour les sources de données.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/hRYeNcQu4uUTCAHXcF9zaZfQm-mw6kDlqvs2AxZhED8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 0%

---

# Annexe - Mesures de [!DNL Google Analytics] disponibles

Les mesures suivantes, à l’exception des exclusions mentionnées, sont disponibles lorsqu’elles sont activées dans l’implémentation du client dans [!DNL Google Analytics].

<!--
 Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Catégorie | Exclu | Commentaires |
| ---- | ---- | ---- |
| \[Tous\] | Mesures avec un type de données « POURCENTAGE » | Les mesures présentées en tant que pourcentage sont toujours exclues. |
| Utilisateur | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionsPerUser | — |
| Session | ga:uniqueDimensionCombinations | — |
| Conversions d’objectifs | — | — |
| Suivi de page | ga:entrances ga:timeOnPage ga:exits | — |
| Recherche interne | — | Les noms conviviaux de toutes les mesures de la recherche interne sont précédés de la valeur « InternalSearch : » |
| Suivi des événements | — | — |
| Ecommerce | — | — |
| Interactions sociales | — | — |
| Exceptions | — | — |
| Variables ou colonnes personnalisées | ga :calcMetric_* | Les mesures calculées sont toujours exclues. |

>[!MORELIKETHIS]
>
>* [À propos de la synchronisation [!DNL Google Analytics] des mesures de conversion](data-source-about.md)
>* [Conditions préalables à la configuration d’une source  [!DNL Google Analytics]  données](data-source-prerequisites.md)
>* [Configurer une [!DNL Google Analytics] vue comme source de données](data-source-configure.md)
>* [Modifier une source  [!DNL Google Analytics]  données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une source  [!DNL Google Analytics]  données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres des sources de données](data-source-settings.md)
