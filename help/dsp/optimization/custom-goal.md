---
title: Bonnes pratiques pour les objectifs personnalisés
description: Découvrez les bonnes pratiques pour définir des objectifs personnalisés pour les packages optimisés pour la CPA la plus faible ou le retour sur investissement le plus élevé.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# Bonnes pratiques pour les objectifs personnalisés

Les objectifs personnalisés définissent les événements de succès dont un annonceur a besoin pour atteindre ses objectifs commerciaux. Chaque package qui utilise l’objectif d’optimisation « [!UICONTROL Highest Return on Ad Spend (ROAS)"] » ou « [!UICONTROL Lowest Cost per Acquisition (CPA)] » doit inclure un objectif personnalisé pour faciliter l’atteinte de l’objectif d’optimisation global. Vous pouvez créer des objectifs personnalisés en tant qu *[objectifs personnalisés](/help/dsp/admin/custom-objectives-manage.md)*.

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Chaque objectif personnalisé se compose d’une ou de plusieurs mesures de conversion à suivre et à optimiser, ainsi que des poids relatifs de ces mesures. Vous pouvez [affecter un objectif personnalisé à un package](/help/dsp/campaign-management/packages/package-settings.md) pour la création de rapports et l’optimisation algorithmique à l’aide de [!DNL Adobe AI].

Pour créer et gérer des objectifs personnalisés, reportez-vous à « [Gérer des objectifs personnalisés](/help/dsp/admin/custom-objectives-manage.md) ».

## Objectifs personnalisés avec une seule mesure

Les exemples suivants montrent comment configurer des objectifs qui ciblent une seule mesure de conversion.

### Exemple pour une campagne avec l&#39;objectif d&#39;optimisation « [!UICONTROL Highest Return on Ad Spend (ROAS)] »

Si l’objectif de votre campagne est le chiffre d’affaires ([!UICONTROL Highest Return on Ad Spend (ROAS)]) et que le chiffre d’affaires de tous les types d’appareils est également important pour vous, incluez la mesure « [!UICONTROL Revenue] » avec un poids de un (1). Sélectionnez le type de mesure *[!UICONTROL Goal]*.

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un poids de un (1) équivaut à une valeur de un (1) pour chaque dollar de chiffre d’affaires qui est suivi pour les publicités display sur n’importe quel appareil. Par exemple, une conversion de 250 $ avec un poids de un (1) est signalée comme 250 $ pour les conversions. Si la mesure de conversion se voit attribuer un poids de 0,5, la conversion de 250 $ est signalée comme 125 $ dans Adobe Advertising (conversion de 250 $ * 0,5 [!UICONTROL weight] = 125 $).

### Exemple pour une campagne avec l&#39;objectif d&#39;optimisation « [!UICONTROL Lowest Cost per Acquisition (CPA)] »

Si l’objectif de votre campagne est le coût par acquisition (CPA) le plus faible et ne nécessite qu’un seul événement de succès (tel que « Envoi de la demande »), incluez cette mesure et indiquez le type de mesure comme *[!UICONTROL Goal]*. La bonne pratique consiste à définir le poids sur un (1).

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un poids de un (1) équivaut à une valeur de un (1) pour chaque conversion qui est suivie pour les publicités display sur n&#39;importe quel appareil. Par exemple, si 10 conversions d’envoi d’application sont suivies, 10 conversions d’envoi d’application sont signalées. Cependant, si la mesure de conversion se voit attribuer un poids de 0,5, les 10 conversions sont signalées comme cinq (5) dans Adobe Advertising (10 conversions * 0,5 [!UICONTROL weight] = 5).

## Objectifs personnalisés avec plusieurs mesures

Il existe deux scénarios dans lesquels vous utiliseriez plusieurs mesures dans un objectif personnalisé :

* L’objectif de votre campagne comporte plusieurs événements de succès. Par exemple, il se peut que vous fassiez de la publicité pour plusieurs actions sur site (téléchargement de PDF, nous contacter et inscription par e-mail) et que toutes ces actions contribuent à l’objectif de votre CPA. Si l’objectif inclut les trois mesures distinctes, chacune ayant un poids d’une (1), l’algorithme optimisé par [!DNL Adobe AI] traite chacune des mesures et chacun des types d’appareils utilisateur avec la même importance. Si les différentes mesures présentent des coûts ou une importance variables, ajustez leur poids relatif en conséquence.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La mesure de conversion unique de votre objectif personnalisé n’atteint pas le minimum de 10 conversions par jour requis pour optimiser les performances. Un nombre inférieur de conversions peut se produire en raison de dépenses quotidiennes minimales du package ou d’un nombre limité de conversions naturelles. L’ajout de mesures de prise en charge supplémentaires à l’objectif personnalisé peut vous aider à atteindre le seuil de 10 conversions par jour. Dix événements annexes peuvent aider un paquet à atteindre le seuil de 10/jour, même lorsque chacun de leurs poids est inférieur à un (1). Mais vous n’aurez peut-être pas besoin d’ajouter autant d’événements.

  Lorsque vous ajoutez des mesures de soutien à un objectif personnalisé, pondérez-les en fonction de leur importance relative par rapport à l’événement de succès principal, et gardez à l’esprit la quantité de points de données. Cela permet à l’algorithme optimisé par [!DNL Adobe AI] d’équilibrer plusieurs mesures et de réaliser une optimisation en vue de votre objectif.

  L’exemple d’objectif suivant inclut trois mesures, chacune ayant un poids différent : Envoi de la demande = 1, Début de la demande = 0,1 et Page de destination de l’annonceur = 0,01. Cela signifie que chaque conversion d’envoi d’application a la même valeur pour votre entreprise qu’une moyenne de 10 conversions de début d’application et de 100 conversions de page de destination d’annonceur.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Si, au contraire, vous pondériez les visites de pages de destination de manière égale dans les envois d’application, alors la quantité naturellement plus élevée de visites de pages de destination pourrait dépasser votre objectif et biaiser l’optimisation en faveur des visites de pages de destination.

>[!MORELIKETHIS]
>
>* [Gérer les objectifs personnalisés](/help/dsp/admin/custom-objectives-manage.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [&#x200B; Paramètres du package &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)
>* [Comment DSP optimise vos campagnes](optimization-how-dsp-optimizes-campaigns.md)
