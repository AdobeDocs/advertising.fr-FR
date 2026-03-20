---
title: Mesures  [!DNL Google Analytics]  disponibles
description: Référencez les mesures  [!DNL Google Analytics]  pour les sources de données.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '131'
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
