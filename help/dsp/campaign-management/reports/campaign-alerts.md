---
title: Affichage des alertes
description: Découvrez comment afficher les alertes et les résolutions recommandées pour vos campagnes et composants de campagne.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 39f77087769eda3cc200447aeb0a6d1648e23b42
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%

---

# Affichage des alertes

DSP vous aide à identifier les problèmes éventuels liés à l’une de vos campagnes ou à l’un de vos composants de campagne. Pour chaque problème, DSP crée une alerte avec un horodatage et l’action recommandée pour résoudre le problème. Les causes des alertes incluent les problèmes de configuration (par exemple, lorsqu’aucune publicité n’est jointe à un emplacement ou lorsqu’une offre est configurée incorrectement), le rejet de la publicité et les problèmes d’intégrité de la campagne (comme une diffusion ou des performances publicitaires médiocres). Les alertes sont disponibles aux niveaux de la campagne, du package, de l’emplacement, de l’annonce publicitaire et des affaires.

Les alertes sont disponibles aux emplacements suivants :

* Une icône [!UICONTROL Pulse Panel] dans les vues [!UICONTROL Campaigns], [!UICONTROL Packages] et Détails du package, [!UICONTROL Placements] et [!UICONTROL Ads] indique si des alertes sont disponibles pour les éléments de cette vue. Lorsque l’icône comporte un point bleu (![icône de panneau à impulsions lorsque des alertes sont disponibles](/help/dsp/assets/alerts-panel.png "icône de panneau à impulsions lorsque des alertes sont disponibles")), les alertes sont disponibles. Lorsqu’aucun point n’est visible (![Icône du panneau d’impulsions lorsqu’aucune alerte n’est disponible](/help/dsp/assets/alerts-panel-empty.png "Icône du panneau d’impulsions lorsqu’aucune alerte n’est disponible")), aucune alerte n’est disponible.

* Les tableaux de données dans les mêmes vues incluent une colonne « [!UICONTROL Alerts] » qui indique quand l’élément (ou ses composants) rencontre un problème. Les indicateurs d’alerte comprennent « Critique » (![Critique](/help/dsp/assets/indicator-critical.png "Critique")), « Avertissement » (![Attention](/help/dsp/assets/indicator-warning.png "Attention")) et « Information » (![Information](/help/dsp/assets/indicator-information.png "Information")).

Vous pouvez ouvrir la vue de gestion de campagne appropriée pour n’importe quelle alerte afin de pouvoir modifier les paramètres selon vos besoins pour résoudre le problème.

Vous pouvez également choisir d’ignorer une alerte individuelle, ce qui la supprime du panneau [!UICONTROL Pulse].

Les alertes et indicateurs d’alerte disparaissent automatiquement lorsque les problèmes sous-jacents sont résolus.

## Affichage des alertes dans l’[!UICONTROL Pulse Panel]

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * (Pour toutes les alertes applicables pour la vue) À droite de la barre d’outils dans n’importe quelle vue de gestion de campagne, cliquez sur ![Icône Panneau à impulsion lorsque des alertes sont disponibles](/help/dsp/assets/alerts-panel.png "Icône Panneau à impulsion lorsque des alertes sont disponibles").

   * (Pour toutes les alertes d’une campagne spécifique) Cliquez sur l’indicateur d’alerte d’une ligne de campagne, puis sur **[!UICONTROL View in Pulse panel]**.

   * (Pour toutes les alertes d’un package, d’un emplacement ou d’une annonce publicitaire spécifique) Procédez comme suit :

      1. Cliquez sur le nom de la campagne.

      1. Dans le sous-menu, cliquez sur **[!UICONTROL Packages]**, **[!UICONTROL Placements]** ou **[!UICONTROL Ads]** pour ouvrir la vue du composant de campagne approprié.

      1. Cliquez sur l’indicateur d’alerte d’un package, d’un emplacement ou d’une ligne d’annonce, puis sur **[!UICONTROL View in Pulse Panel]**.

   Toutes les alertes associées à la campagne et à ses composants, y compris les offres ciblées, sont répertoriées. Par défaut, les alertes critiques sont répertoriées en premier.

1. (Facultatif) Pour regrouper les alertes en fonction de leur première date de détection ou les filtrer par statut d’alerte, statut de composant, type de composant ou avec un nom de campagne spécifique, cliquez sur ![Bouton Filtrer](/help/dsp/assets/filter.png) dans le coin supérieur droit du panneau, sélectionnez les options de filtrage, puis cliquez sur **[!UICONTROL Apply]**.

1. Pour afficher la liste de tous les composants de campagne affectés pour un type d’alerte spécifique, cliquez sur le nom de l’alerte, par exemple « [!UICONTROL Package: No Active Placement (*N*)] ». Pour afficher les détails de chaque composant affecté, y compris l’action recommandée, cliquez sur [!UICONTROL EXPAND ALL] ou cliquez sur le nom du composant. Pour ouvrir la vue de gestion de campagne appropriée pour tout composant concerné afin que vous puissiez effectuer les modifications recommandées, maintenez le curseur sur le nom du composant et cliquez sur ![Accéder à la vue](/help/dsp/assets/go-to-view.png "Accéder à la vue").

1. (Facultatif) Pour ignorer (masquer) une alerte, placez le curseur sur le nom du composant et cliquez sur ![Ignorer](/help/dsp/assets/alert-ignore.png "Ignorer"), puis cliquez sur **[!UICONTROL Ignore alert till next check]**, **[!UICONTROL Ignore alert for 3 days]** ou **[!UICONTROL Ignore indefinitely]**.

Vous disposez de quelques secondes après avoir ignoré une alerte pour annuler l’action. Une fois le message d’option fermé, vous ne pouvez pas annuler l’action.

1. (Facultatif) Pour récupérer les alertes ignorées, filtrez les alertes pour afficher une [!UICONTROL Alert Status] de « [!UICONTROL All] » ou « [!UICONTROL Ignored] ». Pour annuler l’ignorance d’une alerte, placez le curseur sur le nom du composant, puis cliquez sur ![Annuler-ignorer](/help/dsp/assets/alert-un-ignore.png "Annuler-ignorer").

## Fermer le [!UICONTROL Pulse Panel]

* À droite de la barre d’outils, cliquez sur ![Icône Panneau à impulsion lorsque des alertes sont disponibles](/help/dsp/assets/alerts-panel.png "Icône Panneau à impulsion lorsque des alertes sont disponibles") ou ![Icône du panneau d’impulsions lorsqu’aucune alerte n’est disponible](/help/dsp/assets/alerts-panel-empty.png "Icône du panneau d’impulsions lorsqu’aucune alerte n’est disponible").

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues de gestion de campagnes](campaign-reports-about.md)
