---
title: Paramètres du package
description: Voir les descriptions des paramètres de package disponibles.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 26c9c553dbd4086aa114b97dabdf4d9be10cdebe
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Paramètres du package

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** nom du package. La longueur maximale est de 60 caractères.

**[!UICONTROL Description]:** (facultatif) Description du package.

**[!UICONTROL 3rd Party Billed Fees]:** (facultatif) Frais de tiers statiques à suivre en tant que coûts non facturables :

* **[!UICONTROL CPM]:** Coût par 1 000 impressions (CPM).

* **[!UICONTROL Description]:** description des frais de CPM.

>[!NOTE]
>
>Les frais facturables sont reflétés dans la mesure [!UICONTROL Net CPM].

Vous pouvez remplacer le paramètre au niveau du package au [niveau de l’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Lecture seule pour les packages existants) À quel niveau placer et limiter les emplacements dans le package :

* **[!UICONTROL Package level pacing]:** cette stratégie de stimulation fonctionne en stimulant et en plafonnant tous les emplacements inclus en tant que *groupe*. Cette stratégie garantit que tous les emplacements au sein d’un package donné sont optimisés de manière holistique, en distribuant les dépenses en fonction des performances et en les mettant à l’échelle selon des indicateurs clés de performance (KPI) sélectionnés.

* **[!UICONTROL Placement level pacing]:** cette stratégie de stimulation fonctionne en stimulant et en plafonnant tous les emplacements inclus *individuellement*. La bonne pratique consiste à n’utiliser cette stratégie que pour exécuter des contrats de marché privé garantis.

**[!UICONTROL Flight Dates]:** date de début et de fin globales du package. Les dates des vols doivent être incluses dans les dates des vols de la campagne.

>[!NOTE]
>
>* Les dates de vol de tous les emplacements affectés à ce package doivent être incluses dans ces dates.
> * Vous ne pouvez pas modifier la date de début du package lorsque le vol personnalisé est activé.

**[!UICONTROL Activate Custom Flighting]:** vous permet de créer des vols à fréquence inégale pour le package dans la section [!UICONTROL Flighting] ci-dessous. Une fois que vous avez activé les vols personnalisés et enregistré le package, vous ne pouvez plus désactiver les vols personnalisés ni modifier la date de début du package.

**[!UICONTROL Budget]:** (Packages avec fréquence au niveau du package uniquement) Limite budgétaire brute et intervalle budgétaire.

Pour les packages avec vols personnalisés, l’intervalle budgétaire est toujours *[!UICONTROL All time]*. Pour les packages sans vol personnalisé, indiquez l&#39;intervalle budgétaire : *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Packages avec régulation au niveau du package et gestion dynamique des marges uniquement) Limite du budget brut pour la durée du package.

**[!UICONTROL Optimization Goal]:** (packages avec fréquence au niveau du package uniquement) Objectif d’optimisation du package. Consultez les descriptions de chaque objectif d’optimisation à l’adresse [&#x200B; Objectifs d’optimisation et comment les utiliser &#x200B;](/help/dsp/optimization/optimization-goals.md).


**[!UICONTROL Link PG Placements for Incremental Reach Optimization]:** (packages avec fréquence au niveau du package et avec les objectifs d’optimisation « [!UICONTROL Always Max Bid & Maximize Reach] » et « [!UICONTROL Lowest Cost per Reach] » uniquement) Utilise les données de portée domestique de tous les emplacements programmatiques garantis dans la campagne pour optimiser la portée incrémentielle.

**[!UICONTROL Custom Goal for Model Learning]:** (packages avec objectifs d’optimisation « [!UICONTROL Highest Return on Ad Spend] » et « [!UICONTROL Lowest Cost per Acquisition] » uniquement) [objectif personnalisé](/help/dsp/optimization/custom-goal.md) qui inclut les événements de chiffre d’affaires ou de conversion utilisés pour calculer la mesure CPA ou ROAS. L’objectif personnalisé doit inclure des événements supplémentaires de l’entonnoir supérieur pondérés (tels que les visites de page et les ajouts au panier) à utiliser en plus de la mesure CPA ou ROAS pour l’optimisation des packages. Pour plus d’informations sur les objectifs personnalisés, y compris les bonnes pratiques pour créer des objectifs personnalisés et les campagnes qui les utilisent, consultez les sections « [Objectifs personnalisés](/help/dsp/optimization/custom-goal.md) » et « [Bonnes pratiques pour configurer des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md) »<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (facultatif ; packages avec les objectifs d’optimisation « [!UICONTROL Highest Return on Ad Spend] » et « [!UICONTROL Lowest Cost per Acquisition] » uniquement) Indique au modèle d’optimisation de n’apprendre que des conversions basées sur les clics. Dans le cas contraire, le modèle d’optimisation tire parti des conversions basées sur les clics et les impressions.

**[!UICONTROL Conversion Metric]:** (packages avec des objectifs d’optimisation « [!UICONTROL Highest Return on Ad Spend] » et « [!UICONTROL Lowest Cost per Acquisition] » uniquement) Événement de conversion final (tel que les inscriptions) ou montant de l’événement/de la vente de chiffre d’affaires (tel que les achats et les valeurs d’achat) à utiliser pour calculer le retour sur dépenses publicitaires ou le coût par acquisition. Effectuez une sélection dans une liste de tous les événements principaux (« mesures d’objectif ») mappés à l’objectif personnalisé sélectionné. Si la liste est vide, modifiez l’objectif personnalisé afin d’inclure au moins l’un des événements sous-jacents en tant que mesure d’objectif.

**[!UICONTROL Package Goal Type]:** (packages avec objectifs d’optimisation personnalisés uniquement) Objectif du package. Ce paramètre permet de déterminer comment optimiser le package :

* *[!UICONTROL Prospecting]:* Les forfaits de prospection visent à acquérir de nouveaux clients.

* *[!UICONTROL Retargeting]:* Les packages de reciblage se concentrent sur la réexposition des visiteurs ou des clients précédents.

* *[!UICONTROL Other]:* à toutes autres fins.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (packages avec objectifs d’optimisation personnalisés uniquement) Autre package dont les données historiques sont utilisées comme entrée pour l’optimisation du package.

**[!UICONTROL Target]:** (packages avec fréquence au niveau du package uniquement) L’objectif cible, qui est utilisé pour effectuer le suivi des performances.

>[!NOTE]
>
>Ce champ n’est qu’un repère et n’est pas utilisé pour la prise de décision.

**[!UICONTROL Frequency Cap]:** (packages avec fréquence au niveau du package uniquement) Nombre de fois qu’un appareil, un ID universel ou une personne unique (selon la [!UICONTROL Cross Device Level] spécifiée pour la campagne et le paramètre de [!UICONTROL Targeting] de l’emplacement) peut recevoir des annonces publicitaires à partir du package. Les options incluent le *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
>* Vous pouvez définir des limites de fréquence au niveau de la campagne, du package et de l’emplacement. DSP respecte la limite de fréquence la plus stricte dans la hiérarchie de la campagne.
>* La bonne pratique consiste à définir des limites de fréquence pour la prospection et le reciblage au niveau du package.
> * Des limitations de fréquence plus élevées entraînent des dépenses et des impressions plus élevées, mais une portée plus faible. Des limitations de fréquence plus faibles entraînent des dépenses et des impressions plus faibles, mais une portée plus élevée.

**[!UICONTROL Pace on]:** (packages avec fréquence au niveau du package uniquement) Sur quoi la fréquence est basée :

* *[!UICONTROL Budget]:* (par défaut) Cette option génère autant d’impressions que possible dans le budget alloué au package.

* *[!UICONTROL Impressions]:* cette option génère des impressions jusqu’à ce qu’une quantité spécifiée soit atteinte dans un intervalle spécifié. Lorsque vous sélectionnez cette option, indiquez le nombre d’impressions et l’intervalle : *À toute heure* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (packages avec fréquence au niveau du package uniquement) Comment effectuer la fréquence de diffusion de l’annonce publicitaire sur l’ensemble du vol :

* *[!UICONTROL Even]:* Accompagne la livraison de manière uniforme tout au long de chaque vol, avec un objectif de 50% de la livraison dans la première moitié du vol.

* *[!UICONTROL Slightly Ahead]:* (valeur par défaut) Accélère la diffusion afin qu’elle soit achevée à 55-65 % au milieu de la durée du vol.

* *[!UICONTROL Frontload]:* Accélère la livraison de sorte qu&#39;elle soit terminée à 65-75% au milieu du vol.

* *[!UICONTROL Aggressive Frontload]:* Accélère la livraison de sorte qu&#39;elle soit terminée à 75-85% au milieu du vol.

**[!UICONTROL Intraday pacing]:** (Packages avec fréquence au niveau du package uniquement) Comment effectuer la fréquence de diffusion des annonces publicitaires sur chaque jour du vol :

* *[!UICONTROL Even]:* (valeur par défaut) met la diffusion à l’échelle en fonction de la disponibilité du stock. Généralement, plus de publicités sont diffusées par heure pendant la journée, lorsque le volume des enchères est plus élevé, et moins de publicités sont diffusées le matin et le soir.

* *[!UICONTROL ASAP]:* accélère la diffusion à une vitesse deux fois supérieure à *pair*.

  >[!CAUTION]
  >
  >Cette option peut avoir une incidence négative sur les performances. Utilisez-le uniquement lorsque vous donnez entièrement la priorité à la diffusion et aux dépenses plutôt qu’à l’optimisation des performances.

## [!UICONTROL Flighting]

(Packages avec fréquence au niveau du package) Périodes de vol du package, y compris les périodes de vol personnalisées dans le [!UICONTROL Flight Dates] global du package. Vous ne pouvez configurer des vols personnalisés que lorsque l’option [!UICONTROL Activate Custom Flighting] est activée dans la section [!UICONTROL Goals & Budget] .

**[!UICONTROL Automatically rollover remaining flight budget to next flight]:** (disponible uniquement lorsque l&#39;option [!UICONTROL Activate Custom Flighting] est activée) Ajoute automatiquement tout budget restant du vol précédent au budget existant du vol suivant.

Dans la vue [!UICONTROL Packages] et dans la vue [!DNL Package Name] > [!UICONTROL Flights], le champ [!UICONTROL Interval Goal], qui affiche l’objectif de vol actuel, inclut tout budget de report.

**[!DNL Flight N]:** (disponible uniquement lorsque l’option [!UICONTROL Activate Custom Flighting] est activée) Pour chaque vol, spécifiez la date de début, la date de fin et l’objectif de dépenses. Pour ajouter un autre vol, cliquez sur **[!UICONTROL Add Flight]**.

Pour les packages existants sans l&#39;option « [!UICONTROL Automatically rollover remaining flight budget to next flight] » activée, vous pouvez éventuellement rouvrir les paramètres pour saisir une valeur dans la colonne **[!UICONTROL Rollover]** pour tout vol afin d&#39;ajouter le budget potentiellement non dépensé au prochain vol.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des packages](package-about.md)
>* [Créer un package](package-create.md)
>* [Modifier un package](package-edit.md)
>* [Joindre un emplacement à un package](package-attach-placement.md)
>* [Afficher le journal des modifications d&#39;un package](package-change-log.md)
>* [FAQ sur Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
