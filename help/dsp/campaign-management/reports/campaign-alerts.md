---
title: Affichage des alertes
description: Découvrez comment afficher les alertes et les résolutions recommandées pour vos campagnes et composants de campagne.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 3e227bcd39b3928898e764cace1fea91f61d58d5
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Affichage des alertes

DSP vous aide à identifier les problèmes rencontrés par l’un de vos composants de campagne ou de campagne. Pour chaque problème, DSP crée une alerte avec horodatage et l’action recommandée pour résoudre le problème. Les raisons des alertes incluent les problèmes de configuration (par exemple, lorsqu’aucune publicité n’est jointe à un emplacement ou lorsqu’une offre est mal configurée), le rejet de la publicité et les problèmes d’intégrité de la campagne (comme une diffusion ou des performances médiocres de la publicité). Les alertes sont disponibles aux niveaux de la campagne, du package, de l’emplacement, de l’annonce et de l’opération.

Les alertes sont disponibles aux emplacements suivants :

* Une icône [!UICONTROL Pulse Panel] dans les [!UICONTROL Campaigns], [!UICONTROL Packages] et les détails du package, [!UICONTROL Placements] et les [!UICONTROL Ads] vues indique si des alertes sont disponibles pour les éléments de cette vue. Lorsque l’icône comporte un point bleu (![icône du panneau d’impression lorsque des alertes sont disponibles](/help/dsp/assets/alerts-panel.png "icône du panneau d’impression lorsque des alertes sont disponibles")), des alertes sont disponibles. Lorsqu’aucun point n’est visible (![Icône du panneau d’impression lorsqu’aucune alerte n’est disponible](/help/dsp/assets/alerts-panel-empty.png "Icône du panneau d’impression lorsqu’aucune alerte n’est disponible")), aucune alerte n’est disponible.

* Les tableaux de données dans les mêmes vues incluent une colonne &quot;[!UICONTROL Alerts]&quot; qui indique quand l’élément — ou ses composants — a un problème. Les indicateurs d&#39;alerte sont les suivants : &quot;Critique&quot; (![Critique](/help/dsp/assets/indicator-critical.png "Critique")), &quot;Avertissement&quot; (![Avertissement](/help/dsp/assets/indicator-warning.png "Avertissement")) et &quot;Informations&quot; (![Informations](/help/dsp/assets/indicator-information.png "Informations")).

Vous pouvez ouvrir la vue de gestion de campagne appropriée pour toute alerte afin de pouvoir modifier les paramètres nécessaires pour résoudre le problème.

Vous pouvez également choisir d’ignorer une alerte individuelle, qui la supprime du panneau [!UICONTROL Pulse].

Les alertes et les indicateurs d’alerte disparaissent automatiquement lorsque les problèmes sous-jacents sont résolus.

## Affichage des alertes dans le [!UICONTROL Pulse Panel]

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * (Pour toutes les alertes applicables pour la vue) À droite de la barre d’outils d’une vue de gestion de campagne, cliquez sur l’icône ![&#x200B; Publier le panneau lorsque des alertes sont disponibles](/help/dsp/assets/alerts-panel.png "Icône Panneau à pulser lorsque des alertes sont disponibles").

   * (Pour toutes les alertes d’une campagne spécifique) Cliquez sur l’indicateur d’alerte d’une ligne de campagne, puis cliquez sur **[!UICONTROL View in Pulse panel]**.

   * (Pour toutes les alertes d’un module, d’un emplacement ou d’une publicité spécifique) Effectuez les opérations suivantes :

      1. Cliquez sur le nom de la campagne.

      1. Dans le sous-menu, cliquez sur **[!UICONTROL Packages]**, **[!UICONTROL Placements]** ou **[!UICONTROL Ads]** pour ouvrir la vue du composant de campagne approprié.

      1. Cliquez sur l’indicateur d’alerte d’un package, d’un emplacement ou d’une ligne publicitaire, puis cliquez sur **[!UICONTROL View in Pulse Panel]**.

   Toutes les alertes associées à la campagne et à ses composants, y compris les offres ciblées, sont répertoriées. Par défaut, les alertes critiques sont répertoriées en premier.

1. (Facultatif) Pour regrouper les alertes en fonction de leur première date de détection ou pour les filtrer par état d’alerte, statut du composant, type de composant ou avec un nom de campagne spécifique, cliquez sur ![Bouton de filtrage](/help/dsp/assets/filter.png) dans le coin supérieur droit du panneau, sélectionnez les options de filtre, puis cliquez sur **[!UICONTROL Apply]**.

1. Pour afficher la liste de tous les composants de campagne affectés pour un type d’alerte spécifique, cliquez sur le nom de l’alerte, par exemple &quot;[!UICONTROL Package: No Active Placement (*N*)]&quot;. Pour afficher les détails de chaque composant concerné, y compris l’action recommandée, cliquez sur [!UICONTROL EXPAND ALL] ou sur le nom du composant. Pour ouvrir la vue de gestion de campagne appropriée pour tout composant concerné afin que vous puissiez apporter les modifications recommandées, placez le curseur sur le nom du composant et cliquez sur ![Aller pour afficher](/help/dsp/assets/go-to-view.png "Aller pour afficher").

1. (Facultatif) Pour ignorer (masquer) une alerte, placez le curseur sur le nom du composant et cliquez sur ![Ignorer](/help/dsp/assets/alert-ignore.png "Ignorer"), puis sur **[!UICONTROL Ignore indefinitely]**. <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

Vous avez quelques secondes après avoir ignoré une alerte pour annuler l’action. Une fois le message d’option fermé, vous ne pouvez pas annuler l’action.

1. (Facultatif) Pour récupérer les alertes ignorées, filtrez les alertes afin d’afficher un [!UICONTROL Alert Status] de &quot;[!UICONTROL All]&quot; ou &quot;[!UICONTROL Ignored]&quot;. Pour annuler l’exclusion d’une alerte, placez le curseur sur le nom du composant et cliquez sur ![Ne plus ignorer](/help/dsp/assets/alert-un-ignore.png "Ne plus ignorer").

## Fermez le [!UICONTROL Pulse Panel]

* À droite de la barre d’outils, cliquez sur l’icône ![Panneau d’impression lorsque des alertes sont disponibles](/help/dsp/assets/alerts-panel.png "Icône Panneau d’impression lorsque des alertes sont disponibles") ou ![Icône du panneau d’impression lorsqu’aucune alerte n’est disponible](/help/dsp/assets/alerts-panel-empty.png "Icône du panneau d’impression lorsqu’aucune alerte n’est disponible").

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues Campaign Management](campaign-reports-about.md)
