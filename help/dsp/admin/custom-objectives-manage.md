---
title: Gestion des objectifs personnalisés
description: Découvrez comment définir les événements de succès qui vous aident à atteindre les objectifs d’optimisation au niveau du package.
role: User, Admin
feature: DSP Optimization, DSP Packages
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 0%

---

# Gestion des objectifs personnalisés

*Disponible pour les comptes DSP liés aux comptes Search, Social et Commerce*

Les objectifs définissent les événements de succès qu’un annonceur définit pour atteindre ses objectifs commerciaux. Les objectifs sont disponibles pour les packages DSP sous la forme [objectifs personnalisés](/help/dsp/campaign-management/packages/package-settings.md). Chaque package qui utilise l’objectif d’optimisation « [!UICONTROL Highest Return on Ad Spend (ROAS)"] » ou « [!UICONTROL Lowest Cost per Acquisition (CPA)] » doit inclure un objectif personnalisé pour faciliter l’atteinte de l’objectif d’optimisation global.

Un objectif se compose des mesures (propriétés) qui font l’objet d’un suivi et qui doivent être optimisées, ainsi que des poids relatifs de ces mesures. Chaque objectif peut inclure :

* **[!UICONTROL Goal]des mesures** qui représentent les principales mesures de succès d’un annonceur. Ils incluent généralement les principaux résultats commerciaux d’un package, tels que les revenus, les prospects ou les ventes. Chaque objectif doit avoir au moins une mesure d’objectif.

* Mesures d’**[!UICONTROL Assist]facultatives** qui aident, prédisent, précèdent ou contribuent à la création de mesures d’objectif. Par exemple, les mesures d’engagement, telles que les tests et les essais.

  Vous pouvez [!DNL Adobe AI] laisser affecter et mettre à jour automatiquement les événements d’assistance pondérés afin d’optimiser vos événements d’objectif. Si vous préférez attribuer vos propres mesures d’assistance pondérées, DSP peut éventuellement recommander des mesures d’assistance en fonction des données de performances antérieures d’Adobe Advertising et d’Adobe Analytics. Vous pouvez choisir d’appliquer ou non les recommandations.

Toutes les modifications apportées aux options d’objectif sont suivies au niveau du champ et sont répertoriées dans un journal des modifications.

>[!PREREQUISITES]
>
>Avant de pouvoir créer des objectifs, le compte DSP doit être lié à un compte Search, Social et Commerce avec le même ID d’organisation Adobe Experience Cloud, même si vous n’êtes pas client Search, Social et Commerce. Si votre compte DSP n’est pas lié à un compte [!DNL Search, Social, & Commerce], contactez l’équipe chargée de votre compte Adobe.

>[!NOTE]
>
>* Advertising Search, Social et Commerce utilisent également des objectifs. Chaque portfolio Search, Social et Commerce doit avoir un objectif afin que la fonctionnalité d’optimisation puisse créer des modèles de clic et de chiffre d’affaires pour le portfolio.
>* Vous pouvez utiliser le même objectif pour plusieurs packages DSP et/ou plusieurs portfolios Search, Social et Commerce.

## Mesures disponibles

Vous pouvez inclure l’un des éléments suivants dans vos objectifs :

* Mesures suivies par Adobe Advertising à l’aide du [pixel de suivi de conversion Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* (Annonceurs avec [!DNL Adobe Analytics for Advertising]) [Mesures d’engagement du site et de conversion synchronisées à partir d’Adobe Analytics](/help/integrations/analytics/overview.md).

<!-- Do DSP-only clients have these? * [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).  -->

## Statut de l’objectif

La vue [!UICONTROL Settings] > [!UICONTROL Custom Objectives] indique le statut de chaque objectif. Les valeurs peuvent inclure :

* *[!UICONTROL Waiting]* : l’objectif est à l’état de brouillon jusqu’à ce que des recommandations soient générées.

* *[!UICONTROL Active]* : l’objectif est enregistré et utilisable.

## Statut de la recommandation

* *[!UICONTROL Not Initiated]* : aucune recommandation n&#39;a été demandée.

* *[!UICONTROL Generating]* : des recommandations sont en cours de génération.

* *[!UICONTROL Ready]* : des recommandations peuvent être appliquées.

* *[!UICONTROL Error]* : impossible de générer les recommandations.

## Création d’un objectif

1. Dans le menu principal, cliquez sur **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]**.

1. Saisissez les [&#x200B; paramètres d’objectif &#x200B;](#custom-objective-settings).

   Lorsque vous choisissez l’enchère automatisée, vous pouvez affecter des propriétés (mesures) à l’objectif en tant que mesures « [!UICONTROL Goal] ». Pour les enchères personnalisées, vous pouvez attribuer des propriétés sous la forme de mesures « [!UICONTROL Goal] » ou « [!UICONTROL Assist] » pondérées, mais vous devez inclure au moins une mesure d’objectif.

   Les libellés d’objectif et d’assistance n’affectent pas l’optimisation. Seul le poids des mesures incluses affecte l’optimisation.

1. (Objectifs avec enchères personnalisées ; facultatif) Pour générer les mesures d’assistance recommandées en fonction des données de performances antérieures, cliquez sur **[!UICONTROL Generate]** dans la section inférieure. Dans la **[!UICONTROL Generate Recommendation]**, cliquez sur **[!UICONTROL Generate]**.

   La génération des mesures recommandées prend jusqu’à 20 minutes. Pendant la génération des recommandations, le statut de l’objectif personnalisé est *[!UICONTROL Waiting]*. Une fois les recommandations générées, vous pouvez « [&#x200B; afficher et appliquer les événements d’assistance recommandés &#x200B;](#view-apply-recommendations) ».

1. (Si vous n’avez pas généré de recommandations) Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

Dans les paramètres du package [&#128279;](/help/dsp/campaign-management/packages/package-settings.md) pour les packages qui utilisent l’objectif d’optimisation « [!UICONTROL Highest Return on Ad Spend (ROAS)"] ou « [!UICONTROL Lowest Cost per Acquisition (CPA)] », le nom de l’objectif est désormais inclus dans la liste [!UICONTROL Custom Goals]. Lorsque vous sélectionnez l’objectif en tant qu’objectif personnalisé pour un package, la liste [!UICONTROL Conversion Metric] inclut toutes les mesures d’objectif pour l’objectif.

## Modification d’un objectif

1. Dans le menu principal, cliquez sur **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Dans la ligne, cliquez sur **...*** > **[!UICONTROL Edit]**.

1. Modifiez l’un des [&#x200B; paramètres d’objectif &#x200B;](#custom-objective-settings).

1. (Lorsque des recommandations sont disponibles, facultatif) Affichez et appliquez éventuellement les mesures recommandées :

   1. Dans la section inférieure, cliquez sur **[!UICONTROL View Recommendations]**.

   1. Pour appliquer une recommandation, effectuez l’une des opérations suivantes :

      * Cliquez sur **[!UICONTROL Apply]** en regard de la recommandation.

      * Ajustez manuellement la recommandation, puis cliquez sur **[!UICONTROL Apply]** en regard de la recommandation.

   1. Cliquez sur **[!UICONTROL Close]** pour fermer la liste des [!UICONTROL Recommendations].

   Les modifications prennent effet une fois les paramètres des objectifs synchronisés.

1. (Objectifs avec enchères personnalisées ; facultatif) Pour générer des mesures d’assistance recommandées en fonction des données de performances antérieures, cliquez sur **[!UICONTROL Generate]** dans la section inférieure. Dans la **[!UICONTROL Generate Recommendation]**, cliquez sur **[!UICONTROL Generate]**.

   La génération des mesures recommandées prend jusqu’à 20 minutes. Pendant la génération des recommandations, le statut de l’objectif personnalisé est *[!UICONTROL Waiting]*. Une fois les recommandations générées, vous pouvez « [&#x200B; afficher et appliquer les événements d’assistance recommandés &#x200B;](#view-apply-recommendations) ».

1. (Si vous n’avez pas généré de nouvelles recommandations) Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

## Afficher et appliquer les événements d’assistance recommandés {#view-apply-recommendations}

*Objectifs avec enchères personnalisées*

Vous pouvez afficher les recommandations et, éventuellement, les appliquer lorsque le statut de l’objectif est *[!UICONTROL Active]* et que le [!UICONTROL Recommendation Status] est *[!UICONTROL Ready]*.

1. Dans le menu principal, cliquez sur **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Dans la ligne, cliquez sur **...*** > **[!UICONTROL Edit]**.

1. Dans la section inférieure, cliquez sur **[!UICONTROL View Recommendations]**.

1. (Facultatif) Pour appliquer une recommandation, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Apply]** en regard de la recommandation.

   * Ajustez manuellement la recommandation, puis cliquez sur **[!UICONTROL Apply]** en regard de la recommandation.

1. Cliquez sur **[!UICONTROL Close]** pour fermer la liste des [!UICONTROL Recommendations].

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

   Les modifications prennent effet une fois les paramètres des objectifs synchronisés.

## Afficher le journal des modifications pour un objectif personnalisé

1. Dans le menu principal, cliquez sur **[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**.

1. Dans la ligne, cliquez sur **...*** > **[!UICONTROL Change Log]**.

<!--

Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## Paramètres des objectifs personnalisés {#custom-objective-settings}

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| Section | Paramètre | Description |
|---------|-----------|-------------|
| Détails de base | AMOClient | Identifiant Adobe Advertising unique de l’annonceur. |
| Détails de base | Nom de l’objectif | Nom de l’objectif.<br><br>Tous les noms d’objectifs d’Advertising DSP doivent comporter le préfixe « ADSP_ » (non sensible à la casse) comme « ADSP_Registrations ». Utilisez un nom facile à identifier lorsque vous souhaitez l’affecter à un package. |
|  | Description | (Facultatif) Description de l’objectif. La description s’affiche lorsque vous placez le curseur sur le nom dans la liste des objectifs personnalisés. Si vous n’incluez pas de description, le nom de l’objectif est répété à la place. |
| Stratégie d&#39;enchères |  | La stratégie d’enchères de l’objectif, qui détermine les types d’événements que vous pouvez configurer :<ul><li><b>[!UICONTROL Automated Bidding] :</b> attribuez des propriétés (mesures) à l’objectif en tant que mesures [!DNL goal]. [!DNL Adobe AI] affecte et met automatiquement à jour les événements d’assistance pondérée afin d’optimiser vos événements d’objectif à l’aide d’une approche funnel équilibrée.</li><li><b>[!UICONTROL Custom Bidding]:</b> Configurez votre propre stratégie d’enchères en attribuant aux propriétés des événements « [!DNL goal] » ou « [!DNL assist] » pondérés. Utilisez cette option avancée pour les stratégies prédéfinies.</li></ul>La modification de la stratégie d’enchères efface toutes les mesures sélectionnées précédemment. |
| Propriétés | [!UICONTROL Available Metrics] | Toutes les mesures suivies pour l’annonceur. Pour ajouter une mesure en tant qu’objectif, cliquez sur <b>[!UICONTROL Goal]</b> en regard du nom de la mesure. ([!UICONTROL Custom Bidding] uniquement) Pour ajouter une mesure qui aide les mesures d’objectif affectées, cliquez sur <b>[!UICONTROL Assist]</b> en regard du nom de la mesure.<br><br><b>Remarques :</b> [!DNL Analytics] événements personnalisés suivent cette convention d’affectation des noms : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid.` dimensions [!DNL Analytics] et les segments ne sont pas disponibles pour l’optimisation d’Adobe Advertising.<br><br><b>Conseil :</b> pour des performances optimales, les mesures combinées dans l’objectif personnalisé (objectif) doivent totaliser au moins dix conversions par jour. Dans le cas contraire, il est recommandé d’ajouter à l’objectif des mesures de conversion supplémentaires, telles que les pages de produits ou les démarrages d’application. Consultez [&#x200B; Bonnes pratiques pour créer un objectif personnalisé &#x200B;](#custom-goal-best-practices) pour obtenir des instructions. |
|  | Mesures sélectionnées | Nom de chaque mesure de conversion incluse dans l’objectif. Effectuez l’une des opérations suivantes :<ul><li>Pour ajouter une mesure en tant qu’objectif, cliquez sur <b>[!UICONTROL Goal]</b> en regard du nom de la mesure dans la colonne [!UICONTROL Available Metrics] .</li><li>(Stratégie [!UICONTROL Custom Bidding] uniquement) Pour ajouter une mesure qui aide les mesures d’objectif affectées, cliquez sur <b>[!UICONTROL Assist]</b> en regard du nom de la mesure dans la colonne [!UICONTROL Available Metrics]. Saisissez ensuite le poids numérique de la mesure par rapport aux autres mesures de l’objectif. Le poids doit être compris entre 0,001 et 1 et peut inclure des décimales. Le poids par défaut est 1.</li><li>(Stratégie [!UICONTROL Custom Bidding] uniquement) Pour modifier le poids d’une mesure d’assistance, cliquez dans le champ et saisissez le poids numérique de la mesure par rapport aux autres mesures de l’objectif. Le poids doit être supérieur à zéro (0) et peut inclure des décimales. Le poids par défaut est 1.</li><li>Pour supprimer une mesure de l’objectif, placez le curseur sur le nom de la mesure et cliquez sur **[!UICONTROL X]**./li></ul>**Remarques :**<ul><li>Assurez-vous que les différentes mesures et leur poids sont pertinents par rapport à d’. Par exemple, vous ne pouvez pas comparer directement un décompte à un montant en dollars.</li><li>D’importantes modifications relatives entre les pondérations d’objectif peuvent entraîner une volatilité temporaire des performances. Surveillez donc les performances après la modification.</li></ul>. |

>[!MORELIKETHIS]
>
>* [Objectifs d’optimisation et utilisation](/help/dsp/optimization/optimization-goals.md)
>* [Bonnes pratiques pour les objectifs personnalisés](/help/dsp/optimization/custom-goal.md)
>* [&#x200B; Paramètres du package &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)
>* [Gérer les conversions](/help/dsp/admin/conversion-metrics-manage.md)
