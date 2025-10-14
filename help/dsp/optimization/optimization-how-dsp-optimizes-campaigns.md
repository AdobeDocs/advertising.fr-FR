---
title: Optimisation des campagnes par DSP
description: Découvrez comment DSP optimise les packages dans vos campagnes.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Optimisation des campagnes par Advertising DSP

Cette page décrit comment le moteur d’optimisation DSP, optimisé par [!DNL Adobe Sensei], optimise les modules de vos campagnes. Pour obtenir des conseils et des astuces sur la façon d’optimiser manuellement vos campagnes, contactez votre équipe de compte d’Adobe. <!-- add link to trading playbook if we add it to help -->

Les objectifs d’optimisation des packages fonctionnent à deux niveaux :

* Pour chaque package : DSP alloue le budget à chaque emplacement dans le package en fonction des performances de l’emplacement par rapport au KPI sélectionné.

* Pour chaque placement/mise aux enchères dans le package : DSP calcule la valeur des IPC économiques en temps réel pour chaque mise aux enchères par emplacement, puis utilise cette valeur pour déterminer l’offre.

  >[!NOTE]
  >
  >La valeur économique peut être fortement pondérée en fonction de la qualité des dépenses d&#39;un placement. Si un placement est derrière son objectif de dépense, alors il est autorisé à acheter des enchères de qualité inférieure. Si un placement atteint facilement son objectif de dépense, alors l&#39;accent est mis sur des enchères de meilleure qualité.

## Optimisation des packages

DSP peut optimiser votre diffusion de deux manières fondamentales, avec 20 variations disponibles pour correspondre à votre objectif de performances spécifique. Vous pouvez choisir entre :

* Définir la priorité du taux de performance

* Donner la priorité à l’équilibrage de l’efficacité des coûts avec le taux de performance

Voir [Objectifs d’optimisation et Comment les utiliser](optimization-goals.md) pour déterminer quel objectif d’optimisation peut vous aider à atteindre vos IPC.

### Packages qui donnent la priorité au taux de performance

Pour les objectifs d’optimisation qui donnent la priorité au taux de performance, DSP prédit les performances de chaque enchère et toujours les offres à l’offre maximale. [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate], etc. sont des exemples d’objectifs d’optimisation applicables.

Ce mode d’optimisation fonctionne bien si :

* Vous connaissez déjà le niveau de CPM effectif/acceptable (par exemple, une référence historique).

* Si vous rencontrez des problèmes de mise à l’échelle, vous êtes prêt à ajuster manuellement le [!UICONTROL Max Bid] pour chaque emplacement.

* Vous privilégiez l&#39;échelle par rapport à l&#39;efficacité.

#### Logique de traitement {#pacing-logic-performance}

* Si les dépenses suivent le rythme, les enchères deviennent plus sélectives, de sorte que vous ne faites que enchérir sur les enchères dont les taux de performance sont élevés.

* Si les dépenses sont en retard, les enchères deviennent moins sélectives, de sorte que vous enchérissez sur les enchères prédites avoir des taux de performance plus bas afin de rattraper l&#39;objectif de rythme.

#### Effacement de l’ombrage du prix/de l’offre {#clearing-price-performance}

Après avoir exécuté la logique de rythme, DSP exécute l’offre proposée par le biais d’un modèle de prévision de prix de compensation. Si la prévision indique que l’offre peut être réduite avec une baisse minimale du taux de victoire, l’offre est décrémentée selon la prévision.

### Packages qui donnent la priorité à l’équilibrage de l’efficacité des coûts avec le taux de performance

Pour certains objectifs d’optimisation, DSP prédit les performances de chaque enchère et ajuste automatiquement les prix de l’offre, sans dépasser les [!UICONTROL Max Bid] d’un emplacement. Parmi les exemples d’objectifs d’optimisation applicables, citons [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click], etc.

#### Logique de traitement {#pacing-logic-balanced}

* Si les dépenses suivent le rythme, DSP deviennent alors plus sensibles aux prix, offrant des montants plus bas pour échanger le taux de victoire avec le plan de rattrapage.

* Si une mesure de performance est également en cours d’équilibrage (tous les objectifs sauf [!UICONTROL Lowest CPM]), l’indicateur de performance clé prédit est fusionné dans le montant de l’offre. Par conséquent, vous proposez une offre plus élevée pour les enchères qui devraient être plus performantes selon le &quot;coût par&quot;.

* Si les dépenses sont en retard, alors DSP devient moins sensible aux prix et propose des montants plus élevés, jusqu&#39;à [!UICONTROL Max Bid], pour échanger le taux de victoire avec le plan d&#39;entraînement.

#### Effacement de l’ombrage du prix/de l’offre {#clearing-price-balanced}

Après avoir exécuté la logique de rythme, DSP exécute l’offre proposée par le biais d’un modèle de prévision de prix de compensation. Si la prévision indique que l’offre peut être réduite avec une baisse minimale du taux de victoire, l’offre est décrémentée selon la prévision.

## Optimisation du placement

Les filtres de pré-enchère de placement constituent la méthode la plus stricte pour garantir des performances élevées. DSP utilise des filtres de pré-enchère de manière stratégique sur différents types d’annonces afin d’atteindre des objectifs de performances à l’échelle des emplacements dans chaque module. Vous pouvez utiliser des filtres avant offre simultanément avec une optimisation au niveau du package ou indépendamment.

>[!NOTE]
>
>Les filtres de pré-enchères disponibles varient en fonction du type de publicité. Par exemple, pour un emplacement d’affichage standard, vous pouvez filtrer par taux de clics publicitaires et visibilité, mais pas par taux d’achèvement.

Voir [&#x200B; Filtres pré-enchères au niveau de l’emplacement et Comment les utiliser &#x200B;](optimization-pre-bid-filters.md) pour déterminer quel filtre pré-enchère peut vous aider à atteindre vos IPC.

>[!MORELIKETHIS]
>
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Objectifs d’optimisation et comment les utiliser](optimization-goals.md)
>* [Filtres de pré-offre de niveau placement et comment les utiliser](optimization-pre-bid-filters.md)
>* [Performance de dépannage](/help/dsp/optimization/troubleshooting-performance.md)
