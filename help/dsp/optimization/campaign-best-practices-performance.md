---
title: Bonnes pratiques relatives à la configuration des campagnes de performances
description: Découvrez les bonnes pratiques pour configurer vos campagnes axées sur les performances, qui incluent des emplacements optimisés pour le CPA le plus bas ou le retour sur investissement le plus élevé.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: c2c2ddb18b100dc0592d07af3ed1d9f030178eca
workflow-type: tm+mt
source-wordcount: '1273'
ht-degree: 0%

---

# Bonnes pratiques relatives à la configuration des campagnes de performances

DSP peut optimiser vos campagnes axées sur les performances. Consultez les bonnes pratiques suivantes pour les campagnes de performances :

* Étape 1 - Définir votre objectif
* Étape 2 - Définir votre stratégie
* Étape 3 - Créer des packages
* Étape 4 - Créer Une Structure D&#39;Emplacement
* Étape 5 - Utiliser les ressources créatives appropriées

## Étape 1 - Définir Votre Objectif

Il est important de comprendre l’objectif de la campagne, par exemple obtenir le retour sur dépenses publicitaires le plus élevé possible ou le CPA le plus bas possible. Les campagnes de performances ont le [objectifs d’optimisation](/help/dsp/optimization/optimization-goals.md) «[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou «[!UICONTROL Lowest Cost per Acquisition (CPA)]. » Pour chaque package de la campagne, vous spécifiez l’objectif d’optimisation en conséquence.

![objectif d’optimisation](/help/dsp/assets/optimization-goals.png)

Vous devez également déterminer le ou les événements de succès qui mèneront à l’objectif global et créer des objectifs personnalisés en conséquence. Pour chaque package, vous spécifiez un objectif personnalisé à utiliser avec l’objectif d’optimisation global pour les rapports et l’optimisation algorithmique à l’aide de [!DNL Adobe Sensei]. Pour plus d’informations sur la création d’objectifs personnalisés, voir le [Bonnes pratiques pour créer un objectif personnalisé](custom-goal.md#custom-goal-best-practices).

![objectifs personnalisés](/help/dsp/assets/objective-goals.png)

## Étape 2 - Définir votre stratégie

### Stratégies de prospection

Les packages de l’entonnoir supérieur incluent des emplacements avec un ciblage très large pour atteindre les nouveaux consommateurs nets.

#### Stratégies de placement recommandées pour la prospection

* Trouvez de nouvelles audiences qui sont susceptibles d’être converties à l’aide des tactiques suivantes :

   * Modélisation similaire à partir d’une plateforme de gestion des données (DMP), telle que Adobe Audience Manager.
   * Ciblage comportemental à l’aide de données tierces.
   * Le ciblage contextuel.
   * Ciblage des sites/catégories.

* Utiliser le ciblage RON (Run of Network) : il est important d’inclure une exécution d’emplacement réseau sans ciblage d’audience et avec un ciblage d’inventaire large. Cela permet au [!DNL Adobe Sensei] pour trouver les utilisateurs importants qui peuvent avoir des cookies plus récents qui n’ont pas encore été classés dans une audience.

### Stratégies de reciblage

Les packages d’entonnoir inférieur incluent des emplacements qui ciblent les utilisateurs et utilisatrices qui ont déjà accédé à la page web de l’annonceur ou pour lesquels l’annonceur dispose de données CRM.

#### Stratégies de positionnement recommandées pour le reciblage

* Si l’annonceur est un client d’Adobe Analytics ou de Adobe Audience Manager, vous pouvez créer des segments propriétaires (tels que les visiteurs de la page d’accueil, les pages de produits ou les personnes ayant abandonné leur panier) et les utiliser comme cibles d’emplacement dans DSP.

* Évitez d’affecter trop de budget à un emplacement ciblé sur une audience. En règle générale, budgétez 30 $ par tranche de 1 000 utilisateurs par mois.

## Étape 3 - Créer des packages

La bonne pratique consiste à créer des packages distincts pour la prospection de l’entonnoir supérieur et pour le reciblage de l’entonnoir inférieur. L’optimisation se produit au niveau du package, de sorte que les données de performances de tous les emplacements au sein d’un package sont regroupées. Par conséquent, regroupez les emplacements dans des packages avec des performances attendues similaires.

![exemple de packages distincts pour la prospection et le reciblage](/help/dsp/assets/p-r.png)

Utilisez également les paramètres suivants.

### Objectifs et budget

* **Fréquence et limitation :** Pour sélectionner un objectif d’optimisation de CPA ou de retour sur les dépenses publicitaires, le package doit utiliser la fréquence au niveau du package. Cela permet de s’assurer que tous les emplacements dans le package sont optimisés pour répartir les dépenses en fonction des performances et les mettre à l’échelle vers les objectifs sélectionnés.

* **Dates de vol :** (Packages de prospection) Lorsque votre campagne dure plus de 25 jours, utilisez la variable [!UICONTROL Activate Custom Flighting] fonctionnalité. Tout d’abord, définissez un vol personnalisé pour les 10 premiers jours à environ 75 % du budget quotidien nécessaire pour réduire les dépenses pendant le *phase d&#39;apprentissage*. Définissez ensuite un deuxième vol personnalisé pour le reste du budget.

  Par exemple, si vous avez 100 000 $ à dépenser en 30 jours, définissez le budget du vol 1 (jours 1 à 10) sur 25 000 $ (75 % x 100 000 $/30 jours = 2 500 $ par jour). Utiliser le budget restant de 75 000 $ pour le vol 2 (jours 11 à 30).

* **Budget :** DSP tentera toujours de répartir 100 % du budget du package de manière égale entre tous les emplacements d’un package. Si un emplacement entraîne de faibles dépenses ou aucune dépense, nous vous recommandons de limiter le budget de l’emplacement afin de permettre l’affectation d’une plus grande part du budget aux emplacements à grande échelle. Compter 24 à 48 heures pour étalonner les changements de budget.

* **Objectifs d’optimisation :** Utilisez l’un des deux objectifs d’optimisation des performances : *[!UICONTROL Highest Return on Ad Spend]* ou *[!UICONTROL Lowest Cost per Acquisition]*, en fonction de l’objectif du package. Ces objectifs optimisent automatiquement le package vers les emplacements Retour sur les dépenses publicitaires le plus élevé ou CPA le plus bas, respectivement.

* **Objectifs personnalisés :**
   * Si un nouveau package a le même objectif qu’un package existant, vous pouvez éventuellement lier le package existant afin que l’algorithme puisse utiliser les données de machine learning existantes.
   * Saisir le [!UICONTROL Target CPA] ou [!UICONTROL Target ROAS].

* **Fréquence des vols et Fréquence intrajournalière :** Pour les deux types de fréquence, sélectionnez *[!UICONTROL Even]* pour maximiser vos objectifs de performances en effectuant un rythme uniforme tout au long de la journée et du vol.

  >[!CAUTION]
  >
  >Utilisation *[!UICONTROL FrontLoad]* et *[!UICONTROL Aggressive Front Load]* pour la fréquence des vols et *[!UICONTROL ASAP]* Fréquence des fréquences intrajournalières uniquement lorsque vous donnez entièrement la priorité à la diffusion et aux dépenses sur l’optimisation des performances, car ces stratégies peuvent avoir un impact négatif sur les KPI de performances souhaités.

## Étape 4 - Créer Une Structure D&#39;Emplacement

Moins, c&#39;est plus. Si vous pouvez configurer moins de six emplacements par package, le budget disponible peut être déplacé dynamiquement vers les emplacements les plus performants le plus facilement.

Veillez également à ajouter chaque emplacement à un package avec un type d’objectif de package de *[!UICONTROL Prospecting]* ou *[!UICONTROL Retargeting]*, le cas échéant.

Vous trouverez ci-dessous les paramètres d’emplacement recommandés pour les campagnes de performances.

### Objectifs

Vous allez configurer l’optimisation du CPA ou du ROAS au niveau du package (voir Étape 3 - Créer des packages), mais vous pouvez ajouter des paramètres supplémentaires au niveau de l’emplacement.

* **Enchère max. :**
   * Pour les placements de prospection, utilisez une enchère maximum faible (5 $).
   * Pour recibler les emplacements, utilisez une enchère maximum élevée (12 $).

* **Filtres de pré-enchères :** Minimisez ou, idéalement, évitez de définir des filtres de pré-enchères agressifs, qui empêchent l’échelle de l’emplacement. Les bonnes pratiques sont les suivantes :

   * Utilisez un (1) filtre de pré-enchères par emplacement. Plusieurs filtres de pré-enchères nécessiteront que les deux soient respectés, ce qui réduit l’échelle.

   * Pensez à définir des filtres de pré-enchères moins stricts dans les cas où un ciblage supplémentaire (ciblage d’audience, géographique et de site, par exemple) est appliqué.

Voir les descriptions des moments où utiliser chaque filtre de pré-enchères à l’adresse [Filtres de pré-enchères au niveau des emplacements et utilisation](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventaire

Pour optimiser l’échelle, utilisez [!UICONTROL Public] (Open Exchange) et [!UICONTROL On Demand] inventaire.

### Ciblage du site

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] uniquement
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Ciblage d’audience

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Pour les emplacements de prospection, regroupez des catégories d’audience similaires et des tailles d’audience similaires en un seul emplacement. Ensuite, en fonction des performances, effectuez l’une des opérations suivantes :
      * Supprimez les audiences peu performantes des emplacements existants.
      * Placez les audiences les plus performantes dans un emplacement distinct pour mieux contrôler les budgets.
   * Pour le reciblage des emplacements, vous devez idéalement inclure un segment d’audience par emplacement pour contrôler facilement les offres et le budget.

>[!NOTE]
>
>Vos publicités seront plus performantes si un utilisateur ne peut être atteint que par un seul emplacement. Un chevauchement significatif des utilisateurs entre les emplacements peut provoquer une concurrence, ce qui génère un cycle d’offres en augmentation continue, ce qui augmente le coût par utilisateur. Par conséquent, si vous incluez plusieurs audiences, veillez à ce qu’elles ne soient pas composées d’utilisateurs/membres d’audience qui se chevauchent.
>
> Vous pouvez éviter le chevauchement des audiences en créant vos audiences dans des niveaux afin de pouvoir supprimer les niveaux les plus élevés et les plus inclusifs des emplacements, si nécessaire.

* **[!UICONTROL Frequency Capping]:**
   * Pour les placements de prospection, utilisez des limites de fréquence serrées (une impression par jour).
   * Pour recibler les emplacements, définissez la limite d’emplacement principale sur 6 à 10 impressions par jour et la limite secondaire sur une impression par heure.

* **[!UICONTROL Device Targeting]**:
   * Inclure [!UICONTROL Computer], [!UICONTROL Mobile], et [!UICONTROL Tablet].
   * Ne pas cibler [!UICONTROL Firefox] et [!UICONTROL Safari] en raison des limitations de ciblage et de mesure. Contactez l’équipe chargée de votre compte Adobe pour plus d’informations sur [!DNL Adobe] prise en charge de [!DNL Safari ITP].
   * Si vous ciblez le trafic web mobile, désactivez tous les navigateurs mobiles sauf [!UICONTROL Chrome] et [!UICONTROL Edge].

### Sécurité de la marque et qualité des médias

Utilisation du filtrage contextuel, du blocage des fraudes avant enchères et/ou [!UICONTROL Ads.txt] le filtrage limite l&#39;échelle de vos emplacements, mais utilisez-les si nécessaire.

## Étape 5 - Utiliser les ressources créatives appropriées

* La bonne pratique consiste à inclure autant de tailles d’annonces uniques que possible afin d’optimiser la portée. Le modèle d’affichage universel vous permet de télécharger n’importe quelle taille d’affichage standard.
* Vérifiez que tous les emplacements contiennent *au moins* toutes les tailles d’affichage principal (300 x 250, 728 x 90, 160 x 600, 300 x 600, 320 x 50 et 300 x 50).
* Mettez fréquemment à jour les créatifs pour éviter la fatigue créative.

>[!MORELIKETHIS]
>
>* [Paramètres du package](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Filtres de pré-enchères au niveau des emplacements et utilisation](optimization-pre-bid-filters.md)
>* [Liste de contrôle de Campaign Launch](/help/dsp/campaign-management/campaign-launch-checklist.md)
