---
title: Paramètres du package
description: Voir les descriptions des paramètres de package disponibles.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: cb57ada624bdc810a0d6921e89deba832a2b16d9
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Paramètres du package

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Nom du package. La longueur maximale est de 60 caractères.

**[!UICONTROL Description]:** (Facultatif) Description du package.

**[!UICONTROL 3rd Party Billed Fees]:** (Facultatif) Frais de tiers statiques à suivre en tant que coûts non facturables :

>[!NOTE]
>
>Les frais facturables sont reflétés dans les [!UICONTROL Net CPM] métrique.
>
* **[!UICONTROL CPM]:** Coût par 1 000 impressions (CPM).

* **[!UICONTROL CPM Description]:** Une description des frais de CPM.

Vous pouvez remplacer le paramètre au niveau du package à l’adresse [niveau de placement](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Lecture seule pour les packages existants) À quel niveau placer et limiter les emplacements dans le package :

* **[!UICONTROL Package level pacing]:** Cette stratégie de fréquence fonctionne en régulant et en plafonnant tous les emplacements inclus en tant que *groupe*. Cette stratégie permet de s’assurer que tous les emplacements au sein d’un package donné sont optimisés de manière holistique, en distribuant les dépenses en fonction des performances et en les mettant à l’échelle vers des indicateurs de performances clés (IPC) sélectionnés.

* **[!UICONTROL Placement level pacing]:**  Cette stratégie de stimulation fonctionne en stimulant et en plafonnant tous les emplacements inclus *individuellement*. La bonne pratique consiste à utiliser cette stratégie uniquement pour exécuter des transactions de marché privé garanties.

**[!UICONTROL Flight Dates]:** La date de début et de fin du package.

Pour créer éventuellement des vols à fréquence inégale pour le package, sélectionnez *[!UICONTROL *Activate Custom Flighting]** et configurer les vols personnalisés dans le [!UICONTROL Flighting] section ci-dessous. Une fois que vous avez activé la mise en surbrillance personnalisée et enregistré le package, vous ne pouvez plus désactiver la mise en surbrillance.

>[!NOTE]
>
>* Les dates des vols doivent être incluses dans les dates des vols de la campagne. En outre, les dates de vol pour tous les emplacements affectés à ce package doivent être incluses dans ces dates.
> * Vous ne pouvez pas modifier la date de début du package lorsque le vol personnalisé est activé.

**[!UICONTROL Budget]:** (Packages avec fréquence au niveau du package uniquement) La limite du budget brut et l’intervalle budgétaire.

Pour les packages avec vols personnalisés, l’intervalle budgétaire est toujours *[!UICONTROL All time]*. Pour les packages sans vol personnalisé, indiquez l&#39;intervalle budgétaire : *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Packages avec régulation au niveau du package et gestion dynamique des marges uniquement) Limite du budget brut pour la durée du package.

**[!UICONTROL Optimization Goal]:** (Packages avec fréquence au niveau du package uniquement) Objectif d’optimisation pour le package. Consultez les descriptions de chaque objectif d’optimisation à l’adresse . [Objectifs d’optimisation et utilisation](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Packages avec le[!UICONTROL Highest Return on Ad Spend]« et »[!UICONTROL Lowest Cost per Acquisition] » objectifs d’optimisation uniquement) A [objectif personnalisé](/help/dsp/optimization/custom-goal-about.md) qui inclut les revenus ou les événements de conversion utilisés pour calculer la mesure CPA ou ROAS. L’objectif personnalisé peut éventuellement inclure des événements supplémentaires pondérés de l’entonnoir supérieur (tels que les visites de page et les ajouts au panier) à utiliser en plus de la mesure CPA ou ROAS pour l’optimisation des packages. Pour plus d’informations sur les bonnes pratiques relatives aux objectifs personnalisés et aux campagnes qui les utilisent, voir  [Bonnes pratiques pour créer un objectif personnalisé](/help/dsp/optimization/custom-goal-best-practices.md) et [Bonnes pratiques relatives à la configuration des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Facultatif ; packages avec «[!UICONTROL Highest Return on Ad Spend]« et »[!UICONTROL Lowest Cost per Acquisition] » objectifs d’optimisation uniquement) Indique au modèle d’optimisation de n’apprendre que des conversions basées sur les clics. Sinon, le modèle d’optimisation tire parti des conversions basées sur les clics et les impressions.

**[!UICONTROL Conversion Metric]:** (Facultatif ; packages avec «[!UICONTROL Highest Return on Ad Spend]« et »[!UICONTROL Lowest Cost per Acquisition]« objectifs d’optimisation uniquement) Événement de conversion final (tel que les inscriptions) ou montant de l’événement/de la vente de chiffre d’affaires (tel que les achats et les valeurs d’achat) à utiliser pour calculer le retour sur dépenses publicitaires ou le coût par acquisition. Effectuez une sélection dans une liste de tous les événements principaux (« mesures d’objectif ») mappés à l’objectif personnalisé sélectionné. Si la liste est vide, modifiez l’objectif personnalisé afin d’inclure au moins l’un des événements sous-jacents en tant que mesure d’objectif.

**[!UICONTROL Package Goal Type]:** (Packages avec des objectifs d’optimisation personnalisés uniquement) Objectif du package. Ce paramètre permet de déterminer comment optimiser le package :

* *[!UICONTROL Prospecting]:* Les forfaits de prospection visent à acquérir de nouveaux clients.

* *[!UICONTROL Retargeting]:* Les packages de reciblage se concentrent sur la réexposition des visiteurs ou des clients précédents.

* *[!UICONTROL Other]:* À toutes autres fins.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Packages avec des objectifs d’optimisation personnalisés uniquement) Autre package dont les données historiques sont utilisées comme entrée pour l’optimisation du package.

**[!UICONTROL Target]:** (Packages avec fréquence au niveau du package uniquement) Objectif cible, utilisé pour effectuer le suivi des performances.

>[!NOTE]
>
>Ce champ n’est qu’une référence et n’est pas utilisé pour la prise de décision.

**[!UICONTROL Frequency Cap]:** (Packages avec fréquence au niveau du package uniquement) Nombre de fois qu’un appareil ou une personne unique (selon le spécifié [!UICONTROL Cross Device Level] pour la campagne) peuvent être diffusés à partir du package. Les options incluent : *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
>* Vous pouvez définir des limites de fréquence au niveau de la campagne, du package et de l’emplacement. DSP respecte la limite de fréquence la plus stricte dans la hiérarchie de la campagne.
>* La bonne pratique consiste à définir des limites de fréquence pour la prospection et le reciblage au niveau du package.
> * Des limitations de fréquence plus élevées entraînent des dépenses et des impressions plus élevées, mais une portée plus faible. Des limitations de fréquence plus faibles entraînent des dépenses et des impressions plus faibles, mais une portée plus élevée.

**[!UICONTROL Pace on]:** (Packages avec fréquence au niveau du package uniquement) Sur quoi la fréquence est basée :

* *[!UICONTROL Budget]:* (Par défaut) Cette option génère autant d’impressions que possible dans le budget alloué au package.

* *[!UICONTROL Impressions]:* Cette option délivre des impressions jusqu’à ce qu’une quantité spécifiée soit atteinte dans un intervalle spécifié. Lorsque vous sélectionnez cette option, indiquez le nombre d’impressions et l’intervalle : *À tout moment,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Packages avec fréquence au niveau du package uniquement) Comment effectuer la fréquence et la diffusion sur l’ensemble du vol :

* *[!UICONTROL Even]:* La livraison se fait de manière uniforme sur chaque vol, avec un objectif de 50% de la livraison dans la première moitié du vol.

* *[!UICONTROL Slightly Ahead]:* (Valeur par défaut) Accélère la diffusion afin qu’elle soit terminée à 55-65 % au milieu de la durée du vol.

* *[!UICONTROL Frontload]:* Accélère la livraison de sorte qu&#39;elle soit terminée à 65-75 % au milieu du vol.

* *[!UICONTROL Aggressive Frontload]:* Accélère la livraison de sorte qu&#39;elle soit terminée à 75-85 % au milieu du vol.

**[!UICONTROL Intraday pacing]:** (Packages avec fréquence au niveau du package uniquement) Comment effectuer la fréquence et la diffusion sur chaque jour du vol :

* *[!UICONTROL Even]:* (Valeur par défaut) Mise à l’échelle de la diffusion en fonction de la disponibilité du stock. Généralement, plus de publicités sont diffusées par heure pendant la journée, lorsque le volume des enchères est plus élevé, et moins de publicités sont diffusées le matin et le soir.

* *[!UICONTROL ASAP]:* Accélère la diffusion à une vitesse deux fois supérieure à *Événement*.

  >[!CAUTION]
  >
  >Cette option peut avoir une incidence négative sur les performances. Utilisez-le uniquement lorsque vous donnez la priorité absolue à la diffusion et aux dépenses plutôt qu’à l’optimisation des performances.

## [!UICONTROL Flighting]

(Packages avec fréquence au niveau du package et avec «[!UICONTROL Activate Custom Flighting] » activé) Périodes de vol personnalisées dans l’ensemble [!UICONTROL Flight Dates] spécifié dans le [!UICONTROL Goals & Budget] section.

Pour chaque vol, saisissez la date de début, la date de fin et le nombre d’impressions cible. Pour ajouter un autre vol, cliquez sur **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des packages](package-about.md)
>* [Création d’un package](package-create.md)
>* [Modification d’un package](package-edit.md)
>* [Joindre un emplacement à un package](package-attach-placement.md)
>* [Affichage du journal des modifications d’un package](package-change-log.md)
>* [Questions fréquentes sur Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
