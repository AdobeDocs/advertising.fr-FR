---
title: Optimisation des campagnes par DSP
description: Découvrez comment DSP optimise les packages dans vos campagnes.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Optimisation Des Campagnes Par Advertising DSP

Cette page décrit comment le moteur d’optimisation DSP, qui est optimisé par [!DNL Adobe AI], optimise les packages dans vos campagnes. Pour obtenir des conseils et astuces sur la manière d’optimiser manuellement vos campagnes, contactez l’équipe chargée de votre compte Adobe. <!-- add link to trading playbook if we add it to help -->

Les objectifs d’optimisation des packages fonctionnent à deux niveaux :

* Pour chaque package : DSP alloue un budget à chaque emplacement du package en fonction des performances de l’emplacement par rapport aux KPI sélectionnés.

* Pour chaque emplacement/enchère du package : DSP calcule la valeur de KPI économique en temps réel pour chaque enchère par emplacement, puis utilise cette valeur pour déterminer l’offre.

  >[!NOTE]
  >
  >La valeur économique peut être fortement pondérée en fonction de la qualité des dépenses d’un placement. Si un placement se situe derrière son objectif de dépenses, il est alors autorisé à acheter des enchères de moindre qualité. Si un placement atteint facilement son objectif de dépenses, alors l&#39;accent se déplace vers des enchères de meilleure qualité.

## Optimisation des packages

DSP peut optimiser votre diffusion de deux manières fondamentales, avec 20 variations disponibles pour s’aligner sur votre objectif de performances spécifique. Vous pouvez choisir les options suivantes :

* Hiérarchiser le taux de performance

* Privilégiez l’équilibrage coût-efficacité avec le taux de performance

Voir [ Objectifs d’optimisation et méthode d’utilisation ](optimization-goals.md) pour déterminer quel objectif d’optimisation peut vous aider à atteindre vos KPI.

### Packages qui donnent la priorité au taux de performance

Pour les objectifs d’optimisation qui donnent la priorité au taux de performance, DSP prédit la performance de chaque mise aux enchères et enchérit toujours sur l’enchère max. Parmi les exemples d’objectifs d’optimisation applicables, citons notamment [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate], etc.

Ce mode d’optimisation fonctionne bien si :

* Vous connaissez déjà le niveau de CPM effectif/acceptable (par exemple, un niveau de référence historique).

* Vous êtes prêt à ajuster manuellement la [!UICONTROL Max Bid] de chaque emplacement si vous rencontrez des problèmes de mise à l’échelle.

* Vous donnez la priorité à l&#39;échelle plutôt qu&#39;à l&#39;efficacité.

#### Logique de fréquence {#pacing-logic-performance}

* Si les dépenses sont au rendez-vous, les enchères deviennent plus sélectives, de sorte que vous n&#39;enchérissez que sur des enchères dont les taux de performance sont censés être élevés.

* Si les dépenses sont en retard, les enchères deviennent moins sélectives, de sorte que vous enchérissez sur des enchères dont les taux de performance sont censés être plus faibles afin de rattraper l’objectif de rythme.

#### Effacer la nuance des prix/enchères {#clearing-price-performance}

Après avoir exécuté la logique de fréquence, DSP exécute l’offre proposée par le biais d’un modèle de prédiction de prix d’effacement. Si la prédiction indique que l&#39;offre peut être abaissée avec une diminution minimale du taux de gain, alors l&#39;offre est décrémentée selon la prédiction.

### Packages qui privilégient l’équilibre entre rentabilité et taux de performance

Pour atteindre certains objectifs d’optimisation, DSP prédit la performance de chaque mise aux enchères et ajuste automatiquement les prix des enchères, sans jamais dépasser la [!UICONTROL Max Bid] d’un emplacement. Les objectifs d’optimisation applicables incluent notamment [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click], etc.

#### Logique De Fréquence {#pacing-logic-balanced}

* Si les dépenses sont au rythme, alors DSP devient plus sensible aux prix, offrant des montants plus faibles pour échanger le taux de gain avec le plan de rythme.

* Si une mesure de performances est également en cours d’équilibrage (tous les objectifs, à l’exception de [!UICONTROL Lowest CPM]), l’indicateur de performance clé prévu est intégré au montant de l’offre. Vous enchérissez donc plus haut pour les enchères qui devraient être plus performantes sur une base de « coût par ».

* Si les dépenses sont en retard, DSP devient moins sensible aux prix et offre des montants plus élevés, jusqu’à la [!UICONTROL Max Bid], pour échanger le taux de gain avec le plan de stimulation.

#### Effacer la nuance des prix/enchères {#clearing-price-balanced}

Après avoir exécuté la logique de fréquence, DSP exécute l’offre proposée par le biais d’un modèle de prédiction de prix d’effacement. Si la prédiction indique que l&#39;offre peut être abaissée avec une diminution minimale du taux de gain, alors l&#39;offre est décrémentée selon la prédiction.

## Optimisation des emplacements

Les filtres de pré-enchères de positionnement sont le moyen le plus strict d’assurer de bonnes performances. DSP utilise des filtres de pré-enchères de manière stratégique sur différents types d’annonces afin d’atteindre les objectifs de performances à travers les emplacements de chaque package. Vous pouvez utiliser des filtres de pré-enchères simultanément avec l’optimisation au niveau du package ou indépendamment.

>[!NOTE]
>
>Les filtres de pré-enchères disponibles varient selon le type d’annonce. Par exemple, pour un emplacement d’affichage standard, vous pouvez filtrer par taux de clic publicitaire et visibilité, mais pas par taux d’achèvement.

Voir [Filtres de pré-enchères au niveau du positionnement et comment les utiliser](optimization-pre-bid-filters.md) pour déterminer quel filtre de pré-enchères peut vous aider à atteindre vos KPI.

>[!MORELIKETHIS]
>
>* [Paramètres du package](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Filtres de pré-enchères au niveau du placement et utilisation](optimization-pre-bid-filters.md)
>* [Résolution des problèmes liés aux performances](/help/dsp/optimization/troubleshooting-performance.md)
