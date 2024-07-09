---
title: Paramètres du module
description: Reportez-vous à la description des paramètres de package disponibles.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 1ae55a0c4750e25429c954c406352b2235805016
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# Paramètres du module

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Nom du module. La longueur maximale est de 60 caractères.

**[!UICONTROL Description]:** (Facultatif) Description du module.

**[!UICONTROL 3rd Party Billed Fees]:** (Facultatif) Des frais tiers statiques à suivre en tant que coût non facturable :

>[!NOTE]
>
>Les frais facturables sont reflétés dans la variable [!UICONTROL Net CPM] mesure.
>
* **[!UICONTROL CPM]:** Le coût par 1 000 impressions (CPM).

* **[!UICONTROL CPM Description]:** Description des frais CPM.

Vous pouvez remplacer le paramètre au niveau du module à l’adresse [niveau de placement](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Lecture seule pour les modules existants) À quel niveau placer et limiter les emplacements dans le module :

* **[!UICONTROL Package level pacing]:** Cette stratégie de fréquence fonctionne en plaçant et en plafonnant tous les emplacements inclus sous la forme *group*. Cette stratégie garantit que tous les emplacements d’un package donné sont optimisés de manière holistique, en répartissant les dépenses en fonction des performances et de l’échelle sur certains indicateurs clés de performance (IPC).

* **[!UICONTROL Placement level pacing]:**  Cette stratégie de fréquence fonctionne en effectuant un rythme et un plafonnement de tous les emplacements inclus. *individuellement*. La bonne pratique consiste à utiliser cette stratégie uniquement pour exécuter des marchés privés garantis.

**[!UICONTROL Flight Dates]:** Date de début et date de fin du package.

Si vous le souhaitez, vous pouvez créer des vols de fréquence variable pour le kit, sélectionnez *[!UICONTROL *Activate Custom Flighting]** et configurez les vols personnalisés dans le [!UICONTROL Flighting] ci-dessous. Une fois que vous avez activé le vol personnalisé et enregistré le package, vous ne pouvez pas désactiver le vol personnalisé.

>[!NOTE]
>
>* Les dates de vol doivent être incluses dans les dates de vol de l&#39;opération. De plus, les dates de vols de tous les emplacements affectés à ce package doivent être incluses dans ces dates.
> * Vous ne pouvez pas modifier la date de début du module lorsque l’éclairage personnalisé est activé.

**[!UICONTROL Budget]:** (Packages avec une fréquence au niveau du package uniquement) Le plafond budgétaire brut et l’intervalle de budget.

Pour les modules avec un vol personnalisé, l’intervalle de budget est toujours *[!UICONTROL All time]*. Pour les packages sans vol personnalisé, spécifiez l’intervalle de budget : *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Modules avec un rythme au niveau des packages et gestion dynamique des marges uniquement) Le plafond brut du budget pour la durée du package.

**[!UICONTROL Optimization Goal]:** (Modules avec un rythme au niveau du module uniquement) L’objectif d’optimisation du module. Consultez les descriptions de chaque objectif d’optimisation à l’adresse [Objectifs d’optimisation et utilisation](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Modules avec le[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;objectifs d’optimisation uniquement) A [objectif personnalisé](/help/dsp/optimization/custom-goal.md) qui inclut les recettes ou les événements de conversion utilisés pour calculer la mesure CPA ou ROAS. L’objectif personnalisé peut éventuellement inclure d’autres événements d’entonnoir supérieur pondérés (tels que les visites de pages et les ajouts au panier) à utiliser en plus de la mesure CPA ou ROAS pour l’optimisation du package. Pour plus d’informations sur les bonnes pratiques relatives aux objectifs personnalisés et aux campagnes qui les utilisent, voir [Bonnes pratiques pour la création d’un objectif personnalisé](/help/dsp/optimization/custom-goal.md#custom-goal-best-practices) et [Bonnes pratiques pour configurer des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md).<!-- At some point, all of the objectives will be prefixed with "ADSP " -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Facultatif ; inclut le paramètre[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;objectifs d’optimisation uniquement) Indique au modèle d’optimisation de n’apprendre que des conversions basées sur les clics. Dans le cas contraire, le modèle d’optimisation tire les leçons des conversions basées sur les clics et les impressions.

**[!UICONTROL Conversion Metric]:** (Facultatif ; inclut le paramètre[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;objectifs d’optimisation uniquement) L’événement de conversion final (par exemple, les inscriptions) ou le montant d’événement/vente de recettes (tels que les achats et les valeurs d’achat) à utiliser pour calculer le retour sur dépenses publicitaires ou le coût par acquisition. Effectuez une sélection dans une liste de tous les événements principaux (&quot;mesures d’objectif&quot;) mappés à l’objectif personnalisé sélectionné. Si la liste est vide, modifiez l’objectif personnalisé afin d’inclure au moins un des événements sous-jacents en tant que mesure d’objectif.

**[!UICONTROL Package Goal Type]:** (Modules avec objectifs d’optimisation personnalisés uniquement) L’objectif du module. Ce paramètre permet de déterminer comment optimiser le module :

* *[!UICONTROL Prospecting]:* Les forfaits de prospection se concentrent sur l&#39;acquisition de nouveaux clients.

* *[!UICONTROL Retargeting]:* Les modules de reciblage se concentrent sur la réexposition des visiteurs ou clients précédents.

* *[!UICONTROL Other]:* Tous les autres usages.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Modules avec objectifs d’optimisation personnalisés uniquement) Autre module dont les données historiques sont utilisées comme entrée pour optimiser le module.

**[!UICONTROL Target]:** (Modules avec un rythme au niveau du module uniquement) Objectif cible, utilisé pour effectuer le suivi des performances.

>[!NOTE]
>
>Ce champ n’est qu’une référence et n’est pas utilisé pour la prise de décision.

**[!UICONTROL Frequency Cap]:** (Modules avec une fréquence au niveau du module uniquement) Le nombre de fois où un appareil unique, un identifiant universel ou une personne (selon la variable spécifiée) [!UICONTROL Cross Device Level] pour la campagne et le [!UICONTROL Targeting] ) peuvent être diffusées à partir du module . Les options incluent *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
>* Vous pouvez définir des limites de fréquence aux niveaux de la campagne, du kit et de l’emplacement. DSP respecte la limite de fréquence la plus stricte de la hiérarchie de l&#39;opération.
>* La bonne pratique consiste à définir des limites de fréquence pour la prospection et le reciblage au niveau du package.
> * Des plafonds de fréquence plus élevés se traduisent par des dépenses et des impressions plus élevées, mais une portée moindre. Les limites de fréquence plus basses se traduisent par des dépenses et des impressions plus faibles, mais une portée plus élevée.

**[!UICONTROL Pace on]:** (Modules avec mise en page au niveau du module uniquement) Sur quoi repose l’application :

* *[!UICONTROL Budget]:* (Par défaut) Cette option produit autant d’impressions que possible dans le budget alloué du module.

* *[!UICONTROL Impressions]:* Cette option permet de délivrer des impressions jusqu’à ce qu’une quantité spécifiée soit atteinte au cours d’un intervalle spécifié. Lorsque vous sélectionnez cette option, indiquez le nombre d’impressions et l’intervalle : *Tout le temps* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Modules avec fréquence au niveau du module uniquement) Comment espacer et diffuser sur l’ensemble du vol :

* *[!UICONTROL Even]:* Effectue un espacement uniforme de la diffusion à chaque vol, avec une cible de 50 % de la diffusion dans la première moitié du vol.

* *[!UICONTROL Slightly Ahead]:* (La valeur par défaut) Accélère la diffusion, de sorte qu’elle se termine à 55 à 65 % à mi-chemin de la durée du vol.

* *[!UICONTROL Frontload]:* Accélère la diffusion de sorte qu’elle soit de 65 à 75 % complète à mi-chemin du vol.

* *[!UICONTROL Aggressive Frontload]:* Accélère la diffusion de sorte qu’elle soit complète à 75 à 85 % à mi-chemin du vol.

**[!UICONTROL Intraday pacing]:** (Modules avec une fréquence au niveau du module uniquement) Comment espacer et diffuser chaque jour pendant le vol :

* *[!UICONTROL Even]:* (Par défaut) Lance la diffusion en fonction de la disponibilité du stock. En règle générale, plus de publicités sont diffusées par heure dans la journée, lorsque le volume des enchères est plus élevé et moins de publicités sont diffusées le matin et le soir.

* *[!UICONTROL ASAP]:* Accélère la diffusion à deux fois la vitesse de *Même*.

  >[!CAUTION]
  >
  >Cette option peut avoir une incidence négative sur les performances. Utilisez-le uniquement lorsque vous priorisez entièrement la diffusion et que vous dépensez plus que l’optimisation des performances.

## [!UICONTROL Flighting]

(Modules avec une fréquence au niveau du module et avec &quot;[!UICONTROL Activate Custom Flighting]&quot; activée&quot;) Périodes de vol personnalisées dans l’ensemble [!UICONTROL Flight Dates] spécifié dans la variable [!UICONTROL Goals & Budget] .

Pour chaque vol, indiquez la date de début, la date de fin et l’objectif de dépense cible. Pour ajouter un autre vol, cliquez sur **[!UICONTROL Add Flight]**.

Pour les modules existants, vous pouvez éventuellement saisir une valeur dans la variable [!UICONTROL Rollover] pour tout vol afin d&#39;ajouter un budget potentiel non dépensé au prochain vol. La valeur projetée dans la variable [!UICONTROL Adjusted Goal (Goal + Rollover)] est modifiée en conséquence.<!-- clarify usage -->

>[!MORELIKETHIS]

Pour e
>>
* [À propos de la gestion de modules](package-about.md)
>* [Création d’un module](package-create.md)
* [Modification d’un module](package-edit.md)
* [Joindre un emplacement à un package](package-attach-placement.md)
* [Affichage du journal des modifications d’un module](package-change-log.md)
* [Questions fréquentes à propos de Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
