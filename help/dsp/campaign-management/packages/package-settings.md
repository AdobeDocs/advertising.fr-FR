---
title: Paramètres du module
description: Reportez-vous à la description des paramètres de package disponibles.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: ab3118901b7cd88776f7c0ce8038b928118a7555
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Paramètres du module

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Nom du package. La longueur maximale est de 60 caractères.

**[!UICONTROL Description]:** (facultatif) description du package.

**[!UICONTROL 3rd Party Billed Fees]:** (Facultatif) Frais tiers statiques à suivre en tant que coût non facturable :

* **[!UICONTROL CPM]:** coût par 1 000 impressions (CPM).

* **[!UICONTROL Description]:** Description des frais CPM.

>[!NOTE]
>
>Les frais facturables sont reflétés dans la mesure [!UICONTROL Net CPM].

Vous pouvez remplacer le paramètre de niveau package au [niveau d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (lecture seule pour les modules existants) À quel niveau pour accélérer et plafonner les emplacements dans le module :

* **[!UICONTROL Package level pacing]:** Cette stratégie de fréquence fonctionne en effectuant un rythme et en plafonnant tous les emplacements inclus en tant que *groupe*. Cette stratégie garantit que tous les emplacements d’un package donné sont optimisés de manière holistique, en répartissant les dépenses en fonction des performances et de l’échelle sur certains indicateurs clés de performance (IPC).

* **[!UICONTROL Placement level pacing]:** Cette stratégie de fréquence fonctionne en effectuant un rythme et en plafonnant tous les emplacements inclus *individuellement*. La bonne pratique consiste à utiliser cette stratégie uniquement pour exécuter des marchés privés garantis.

**[!UICONTROL Flight Dates]:** La date de début et la date de fin globales du package. Les dates de vol doivent être incluses dans les dates de vol de l&#39;opération.

>[!NOTE]
>
>* Les dates de vol de tous les emplacements affectés à ce package doivent être incluses dans ces dates.
> * Vous ne pouvez pas modifier la date de début du module lorsque l’éclairage personnalisé est activé.

**[!UICONTROL Activate Custom Flighting]:** Permet de créer des vols de fréquence variable pour le package dans la section [!UICONTROL Flighting] ci-dessous. Une fois que vous avez activé le vol personnalisé et enregistré le package, vous ne pouvez pas désactiver le vol personnalisé ni modifier la date de début du package.

**[!UICONTROL Budget]:** (Modules avec une fréquence au niveau du package uniquement) Le plafond brut du budget et l’intervalle de budget.

Pour les modules avec un vol personnalisé, l’intervalle de budget est toujours *[!UICONTROL All time]*. Pour les packages sans vol personnalisé, spécifiez l’intervalle de budget : *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Modules avec un rythme au niveau du package et une gestion dynamique des marges uniquement) Le budget maximum brut pour la durée du package.

**[!UICONTROL Optimization Goal]:** (Modules avec un rythme au niveau du module uniquement) Objectif d’optimisation du module. Consultez les descriptions de chaque objectif d’optimisation à l’adresse [Objectifs d’optimisation et Comment les utiliser](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Modules avec les objectifs d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; uniquement) [objectif personnalisé](/help/dsp/optimization/custom-goal.md) qui inclut les recettes ou les événements de conversion utilisés pour calculer la mesure CPA ou ROAS. L’objectif personnalisé peut éventuellement inclure d’autres événements d’entonnoir supérieur pondérés (tels que les visites de pages et les ajouts au panier) à utiliser en plus de la mesure CPA ou ROAS pour l’optimisation du package. Pour plus d’informations sur les objectifs personnalisés, y compris les bonnes pratiques de création pour les objectifs personnalisés et les campagnes qui les utilisent, voir &quot;[Objectifs personnalisés](/help/dsp/optimization/custom-goal.md)&quot; et &quot;[Bonnes pratiques pour configurer des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md)&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->&quot;.

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Facultatif ; modules avec les objectifs d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; uniquement) Indique au modèle d’optimisation de n’apprendre que des conversions basées sur des clics. Dans le cas contraire, le modèle d’optimisation tire les leçons des conversions basées sur les clics et les impressions.

**[!UICONTROL Conversion Metric]:** (Facultatif ; modules avec les objectifs d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; uniquement) L’événement de conversion final (comme les inscriptions) ou le montant d’événement/de vente de recettes (comme les achats et les valeurs d’achat) à utiliser pour calculer le retour sur dépenses publicitaires ou le coût par acquisition. Effectuez une sélection dans une liste de tous les événements principaux (&quot;mesures d’objectif&quot;) mappés à l’objectif personnalisé sélectionné. Si la liste est vide, modifiez l’objectif personnalisé afin d’inclure au moins un des événements sous-jacents en tant que mesure d’objectif.

**[!UICONTROL Package Goal Type]:** (Modules avec objectifs d’optimisation personnalisés uniquement) Objectif du module. Ce paramètre permet de déterminer comment optimiser le module :

* *[!UICONTROL Prospecting]:* Les packages de prospection se concentrent sur l&#39;acquisition de nouveaux clients.

* *[!UICONTROL Retargeting]:* Les modules de reciblage se concentrent sur la réexposition des visiteurs ou clients précédents.

* *[!UICONTROL Other]:* Tous les autres usages.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Modules avec objectifs d’optimisation personnalisés uniquement) Autre module dont les données historiques sont utilisées comme entrée pour optimiser le module.

**[!UICONTROL Target]:** (Modules avec un rythme au niveau du package uniquement) Objectif cible, utilisé pour effectuer le suivi des performances.

>[!NOTE]
>
>Ce champ n’est qu’une référence et n’est pas utilisé pour la prise de décision.

**[!UICONTROL Frequency Cap]:** (Modules avec un rythme au niveau du package uniquement) Le nombre de fois qu’un appareil, un identifiant universel ou une personne unique (en fonction du [!UICONTROL Cross Device Level] spécifié pour la campagne et du paramètre [!UICONTROL Targeting] de l’emplacement) peuvent être diffusées des publicités à partir du package. Les options incluent *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
>* Vous pouvez définir des limites de fréquence aux niveaux de la campagne, du kit et de l’emplacement. DSP respecte la limite de fréquence la plus stricte de la hiérarchie de l&#39;opération.
>* La bonne pratique consiste à définir des limites de fréquence pour la prospection et le reciblage au niveau du package.
> * Des plafonds de fréquence plus élevés se traduisent par des dépenses et des impressions plus élevées, mais une portée moindre. Les limites de fréquence plus basses se traduisent par des dépenses et des impressions plus faibles, mais une portée plus élevée.

**[!UICONTROL Pace on]:** (Modules avec un rythme au niveau du module uniquement) Sur quoi repose le rythme :

* *[!UICONTROL Budget]:* (par défaut) Cette option diffuse autant d’impressions que possible dans le budget alloué du module.

* *[!UICONTROL Impressions]:* Cette option permet de délivrer des impressions jusqu’à ce qu’une quantité spécifiée soit atteinte dans un intervalle spécifié. Lorsque vous sélectionnez cette option, indiquez le nombre d’impressions et l’intervalle : *All time,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Modules avec un rythme au niveau du package uniquement) Comment accélérer le rythme et la diffusion sur l’ensemble du vol :

* *[!UICONTROL Even]:* Effectue un espacement uniforme dans chaque vol, avec une cible de 50 % de la diffusion dans la première moitié du vol.

* *[!UICONTROL Slightly Ahead]:* (valeur par défaut) accélère la diffusion de sorte qu’elle se termine à 55-65 % à mi-chemin de la durée du vol.

* *[!UICONTROL Frontload]:* accélère la diffusion de sorte qu’elle se termine à 65-75 % à mi-chemin du vol.

* *[!UICONTROL Aggressive Frontload]:* accélère la diffusion de sorte qu’elle se termine à 75-85 % à mi-chemin du vol.

**[!UICONTROL Intraday pacing]:** (Modules avec un rythme au niveau du package uniquement) Comment accélérer la diffusion et la diffuser tous les jours dans le vol :

* *[!UICONTROL Even]:* (valeur par défaut) met à l’échelle la diffusion en fonction de la disponibilité de l’inventaire. En règle générale, plus de publicités sont diffusées par heure dans la journée, lorsque le volume des enchères est plus élevé et moins de publicités sont diffusées le matin et le soir.

* *[!UICONTROL ASAP]:* accélère la diffusion à deux fois la vitesse de *Même*.

  >[!CAUTION]
  >
  >Cette option peut avoir une incidence négative sur les performances. Utilisez-le uniquement lorsque vous priorisez entièrement la diffusion et que vous dépensez plus que l’optimisation des performances.

## [!UICONTROL Flighting]

(Packages avec fréquence au niveau du package) Les périodes de vol du package, y compris toutes les périodes de vol personnalisées dans l’ensemble [!UICONTROL Flight Dates] du package. Vous ne pouvez configurer des vols personnalisés que lorsque l’option [!UICONTROL Activate Custom Flighting] est activée dans la section [!UICONTROL Goals & Budget].

**[!DNL Flight N]:** (Disponible uniquement lorsque l’option [!UICONTROL Activate Custom Flighting] est activée) Pour chaque vol, spécifiez la date de début, la date de fin et l’objectif de dépense cible. Pour ajouter un autre vol, cliquez sur **[!UICONTROL Add Flight]**.

Pour les packages existants, vous pouvez éventuellement saisir une valeur dans la colonne [!UICONTROL Rollover] pour n’importe quel vol afin d’ajouter un budget non dépensé potentiel au prochain vol. La valeur projetée dans la colonne [!UICONTROL Adjusted Goal (Goal + Rollover)] est modifiée en conséquence.<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [À propos de la gestion de modules](package-about.md)
>* [Créer un module](package-create.md)
>* [Modifier un module](package-edit.md)
>* [Joindre un emplacement à un package](package-attach-placement.md)
>* [Afficher le journal des modifications d’un package](package-change-log.md)
>* [FAQ sur Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
