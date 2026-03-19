---
title: À propos de l’outil DSP [!UICONTROL Planner]
description: Découvrez l’outil de planification pour prévoir la portée unique des emplacements de télévision connectée (CTV) en fonction du budget et des critères de ciblage spécifiés.
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
source-git-commit: dad30b0bd24c0286c1de6520471cb90707046ff3
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# À propos de l’outil DSP [!UICONTROL Planner]

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Fonction Beta*

L&#39;outil de planification vous aide à prévoir la portée unique au niveau du ménage des emplacements de télévision connectée (CTV) en fonction du budget et des critères de ciblage spécifiés avant de commencer à dépenser pour les stocks. Après avoir évalué plusieurs plans de portée, vous pouvez mettre en œuvre le plan qui correspond le mieux aux résultats souhaités dans vos packages et emplacements.

L’outil de planification utilise les données historiques d’enchères, d’impressions et d’impressions des 90 derniers jours pour estimer la portée unique, le CPM moyen, la fréquence moyenne et les impressions d’une configuration de plan.

## Prévisions du planificateur

Chaque prévision se compose d’une courbe de prévision du budget de portée qui indique la quantité de portée réalisable avec les paramètres du plan. Déplacez le curseur sur la visualisation pour afficher les opportunités de portée incrémentielle avec des budgets plus élevés.

![Prévision du planificateur](/help/dsp/assets/planner-forecast.png "Prévision du planificateur")

La sortie prévisionnelle comprend également une section [!UICONTROL Inventory Breakdown] qui montre comment différents éditeurs contribuent à une portée unique, offrant de précieuses opportunités de découverte.

>[!NOTE]
>
>* La section [!UICONTROL Inventory Breakdown] affiche des données pour les inventaires privé et [!UICONTROL On Demand] uniquement.
>* La portée unique estimée affichée pour deux éditeurs peut se chevaucher.

## Vue du planificateur

Dans la vue [!UICONTROL Planner], vous pouvez afficher vos plans de portée CTV existants et en créer de nouveaux.

Vous pouvez également modifier, dupliquer, exporter, archiver ou régénérer la prévision pour n&#39;importe quel plan.

## Questions fréquentes

+++Quels types d’inventaire l’outil de planification prend-il en charge ?

L’outil de planification prend en charge tous les types d’inventaire, y compris les inventaires programmatiques garantis (PG), de marché privé (PMP), [!UICONTROL On Demand] et publics. Pour générer des prévisions précises, incluez des offres avec au moins 50 000 impressions au cours des sept derniers jours.

+++

+++Pourquoi est-ce que je vois « [!UICONTROL Unable to generate forecast] ? »

L&#39;une des raisons les plus courantes de cette erreur est un budget insuffisant ou une soumission maximale. Pour de meilleurs résultats, utilisez un budget minimum de 5000 USD. Si le type de média [!UICONTROL Connected TV] est sélectionné, saisissez une enchère maximale d&#39;au moins 10 USD.

Assurez-vous également que les éditeurs ou les offres inclus sont actifs et ont une activité d’impression récente.

+++

+++J&#39;ai créé un emplacement basé sur la prévision, mais il n&#39;a pas atteint la portée unique indiquée par la prévision de portée. Pourquoi ? 

La prévision de portée n’est qu’une estimation, et les résultats réels devraient varier en raison de multiples facteurs qui changent fréquemment, comme la saisonnalité, la compétitivité des soumissions et l’offre et la demande. Il ne devrait pas être entièrement précis, mais il est surtout utile pour obtenir des informations directionnelles sur les stratégies de campagne qui peuvent potentiellement générer les meilleurs résultats.

+++

+++Le planificateur peut-il générer différents résultats de prévision avec les mêmes paramètres d&#39;entrée ?

Le planificateur génère des prévisions basées sur les dernières données observées, de sorte que la sortie prévue peut varier à différents moments même si les paramètres du plan restent les mêmes. Pensez à générer plusieurs prévisions pour le même plan et à exporter les résultats de chacun d’eux.

+++

+++Puis-je enregistrer la sortie de la prévision du planificateur ?

Oui, vous pouvez exporter une prévision dans une feuille de calcul [!DNL Microsoft Excel] en cliquant sur **[!UICONTROL ...]** > **[!UICONTROL Export]** dans le coin supérieur droit. La feuille de calcul capture les informations affichées dans la courbe du budget de portée à l’aide de deux colonnes de données : [!UICONTROL Budget] et [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [À propos de l’outil de [!UICONTROL Planner] DSP](planner-about.md)
>* [Créer un plan de portée TV connectée](planner-create.md)
>* [Dupliquer un plan de portée TV connectée](planner-duplicate.md)
>* [Modification d’un plan de portée de télévision connectée](planner-edit.md)
>* [Exporter un plan de portée TV connectée](planner-export.md)
>* [Régénérer la prévision pour un plan de portée TV connectée](planner-forecast.md)
>* [Archiver un plan de portée TV connectée](planner-archive.md)
>* [Paramètres des plans de portée TV connectée](planner-settings.md)
