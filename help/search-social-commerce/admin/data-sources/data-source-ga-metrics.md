---
title: Disponible [!DNL Google Analytics] mesures
description: Référencez la variable [!DNL Google Analytics] mesures disponibles pour les sources de données.
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Annexe : Disponible [!DNL Google Analytics] mesures

Les mesures suivantes, à l’exception des exclusions indiquées, sont disponibles lorsqu’elles sont activées dans l’implémentation du client dans [!DNL Google Analytics].

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
>* [A propos de la synchronisation [!DNL Google Analytics] mesures de conversion](data-source-about.md)
>* [Conditions préalables à la configuration d’un [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [Configurez une [!DNL Google Analytics] vue comme source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspension de la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier un [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
