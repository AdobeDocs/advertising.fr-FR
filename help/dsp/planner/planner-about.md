---
title: À propos de l’outil de planification DSP
description: Découvrez l’outil de planification pour prévoir la portée unique des placements de télévision connectée (CTV) en fonction de critères de ciblage et de budget spécifiés.
feature: DSP Planner
source-git-commit: 9799ff5464d48e6258026ec997c5d5091576b9c6
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---


# À propos de l’outil de planification DSP

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Fonction bêta*

L’outil de planification vous permet de prévoir la portée unique au niveau du foyer des placements de télévision connectée (CTV) en fonction de critères de ciblage et de budget spécifiés avant de commencer à dépenser pour l’inventaire. Après avoir évalué plusieurs plans de portée, vous pouvez mettre en oeuvre le plan qui s’aligne le mieux sur les résultats souhaités dans vos modules et emplacements.

L’outil de planification utilise des données historiques d’offre, d’impression et de portée des 90 derniers jours pour estimer la portée unique, le CPM moyen, la fréquence moyenne et les impressions pour une configuration de plan.

## Prévision du planificateur

Chaque prévision se compose d’une courbe de prévision du budget de la portée qui indique le montant d’étendue réalisable avec les paramètres du plan. Déplacez le curseur sur la visualisation pour afficher les opportunités de portée incrémentielle avec des budgets plus élevés.

![Prévision du planificateur](/help/dsp/assets/planner-forecast.png "Prévision du planificateur")

La sortie de la prévision comprend également un [!UICONTROL Inventory Breakdown] qui montre comment les différents éditeurs contribuent à une portée unique, offrant des opportunités de découverte précieuses.

>[!NOTE]
>
>* La variable [!UICONTROL Inventory Breakdown] affiche des données uniquement pour les propriétés privées et [!UICONTROL On Demand] inventaire.
>* La portée unique estimée affichée pour deux éditeurs peut se chevaucher.

## Vue Plan

Dans le [!UICONTROL Planner] Vous pouvez afficher vos plans de portée CTV existants et en créer de nouveaux.

Vous pouvez également modifier, dupliquer, exporter, archiver ou régénérer la prévision pour n’importe quel plan.

## Questions fréquentes

+++Quels types d’inventaire l’outil de planification prend-il en charge ?

L’outil de planification prend en charge tous les types d’inventaire, y compris les stocks garantis par programmation (PG), les marchés privés (PMP), [!UICONTROL On Demand], et public. Pour générer des prévisions précises, incluez des offres d’au moins 50 000 impressions au cours des sept derniers jours.

+++

+++Pourquoi est-ce que je vois &quot;[!UICONTROL Unable to generate forecast]?&quot;

Une des raisons les plus courantes de cette erreur est un budget insuffisant ou une offre maximale. Pour de meilleurs résultats, utilisez un budget minimum de 5000 USD. Si la variable [!UICONTROL Connected TV] le type de support est sélectionné, saisissez une offre maximale d&#39;au moins 10 USD.

Assurez-vous également que les éditeurs ou les offres inclus sont actifs et ont une activité d’impression récente.

+++

+++J’ai créé un emplacement basé sur la prévision, mais il n’a pas atteint la portée unique indiquée par la prévision de portée. Pourquoi ?

La prévision de portée n’est qu’une estimation et les résultats réels devraient varier en raison de facteurs multiples qui changent fréquemment, tels que le caractère saisonnier, la compétitivité des offres et l’offre et la demande. Elle ne devrait pas être entièrement exacte, mais elle est particulièrement utile pour obtenir des informations directionnelles sur les stratégies de campagne qui peuvent potentiellement générer les meilleurs résultats.

+++

+++Le planificateur peut-il générer des résultats de prévision différents avec les mêmes paramètres d’entrée ?

Le planificateur génère des prévisions basées sur les dernières données observées, de sorte que la sortie prévue peut varier à des moments différents, même si les paramètres du plan restent identiques. Envisagez de générer plusieurs prévisions pour le même plan et d’exporter les résultats pour chacune d’elles.

+++

+++Puis-je enregistrer le résultat des prévisions du planificateur ?

Oui, vous pouvez exporter une prévision dans une [!DNL Microsoft® Excel] feuille de calcul en cliquant sur **[!UICONTROL ...]** > **[!UICONTROL Export]** en haut à droite. La feuille de calcul capture les informations affichées dans la courbe de budget de la portée à l’aide de deux colonnes de données : [!UICONTROL Budget] et [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [À propos de l’outil de planification DSP](planner-about.md)
>* [Créer un plan de portée télévisée connectée](planner-create.md)
>* [Duplication d’un plan de portée télévisée connecté](planner-duplicate.md)
>* [Modification d’un plan de portée télévisée connecté](planner-edit.md)
>* [Exportation d’un plan de portée TV connecté](planner-export.md)
>* [Régénération des prévisions pour un plan de portée télévisée connecté](planner-forecast.md)
>* [Archivage d’un plan de portée télévisée connecté](planner-archive.md)
>* [Paramètres des plans de portée TV connectés](planner-settings.md)
