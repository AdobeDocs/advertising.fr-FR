---
title: Mesures disponibles [!DNL Google Analytics]
description: Référencez les mesures  [!DNL Google Analytics]  disponibles pour les sources de données.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Annexe - Mesures [!DNL Google Analytics] disponibles

Les mesures suivantes, à l’exception des exclusions notées, sont disponibles lorsqu’elles sont activées dans l’implémentation du client dans [!DNL Google Analytics].

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Catégorie | Exclu | Commentaires |
| ---- | ---- | ---- |
| \[Tous\] | Mesures avec un type de données &quot;PERCENT&quot; | Les mesures présentées sous la forme d’un pourcentage sont toujours exclues. |
| Utilisateur | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionsPerUser | — |
| Session | ga:uniqueDimensionCombinations | — |
| Conversions des objectifs | — | — |
| Suivi de page | ga:entrées, ga:timeOnPage, ga:sorties | — |
| Recherche interne | — | Les noms conviviaux de toutes les mesures de la recherche interne sont précédés de la valeur &quot;InternalSearch:&quot; |
| Suivi des événements | — | — |
| eCommerce | — | — |
| Interactions sociales | — | — |
| Exceptions | — | — |
| Variables ou colonnes personnalisées | ga:calcMetric_* | Les mesures calculées sont toujours exclues. |

>[!MORELIKETHIS]
>
>* [&#x200B; À propos de la synchronisation  [!DNL Google Analytics] mesures de conversion](data-source-about.md)
>* [&#x200B; Conditions préalables à la configuration d’une  [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [&#x200B; Configuration d’une  [!DNL Google Analytics] vue en tant que source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
