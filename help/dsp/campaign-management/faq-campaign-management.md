---
title: Questions fréquentes sur la gestion de campagnes
description: Découvrez la gestion des campagnes, notamment la période de latence des modifications et ce qui se passe lorsque vous apportez des modifications au budget au cours d’un vol.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
TQID: https://experienceleague.adobe.com/PgO4aktP20KQzNe6SG6Vw7ahvYqHTSISQ10FCum-vQg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# Questions fréquentes sur la gestion de campagnes

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latence des modifications de paramètre

* Lorsque vous modifiez un emplacement ou un paramètre de package, à quel moment la modification prend-elle effet ?

  Les modifications des paramètres prennent généralement effet immédiatement, mais peuvent prendre jusqu’à 12 heures.

  Si c’est le dernier jour de la diffusion, apportez les modifications tôt dans la journée afin que DSP ait tout le temps nécessaire pour recalibrer le package en fonction des modifications. Par exemple, si vous passez de la fréquence régulière à la fréquence de préalimentation, DSP doit réévaluer la répartition des dépenses pendant le reste du vol. Ne faites pas ce genre de changement s&#39;il ne vous reste qu&#39;une heure pour livrer le dernier jour du vol.

## Mises à jour budgétaires en cours de route

* Lorsque vous apportez une modification à un emplacement, combien de temps DSP prend-il pour réaffecter le budget du package ?

  L’allocation budgétaire est basée sur les performances des emplacements, évaluées à l’aide d’une moyenne sur 14 jours. Les modifications apportées à un emplacement n&#39;entraînent des modifications de la répartition budgétaire que lorsqu&#39;elles entraînent des modifications des performances au cours de la moyenne sur 14 jours.

  Lorsque des modifications de performances se produisent, DSP réaffecte le budget du package entre les emplacements en conséquence au cours du cycle d’optimisation du budget suivant, qui se produit vers minuit (00:00) dans le fuseau horaire de la campagne.

* Comment le budget est-il réaffecté lorsqu’un emplacement est supprimé d’un package et ajouté à un autre package ?

  L’historique complet des dépenses d’un emplacement est joint à l’emplacement et passe d’un package à l’autre.

  Lorsque vous supprimez un emplacement d’un package, le package n’a plus d’historique des dépenses de l’emplacement. Le budget du package devient (budget du package - budget d’emplacement supprimé) / intervalle de temps restant en cours. Le budget du package est ensuite alloué aux emplacements restants dans le package.

  De même, si vous ajoutez le même emplacement à un package différent, DSP prend en compte l&#39;historique des dépenses de l&#39;emplacement lorsqu&#39;il alloue un budget pour tous les emplacements dans le nouveau package.

* Comment la fréquence des colis change-t-elle le dernier jour d&#39;un vol ?

  Le dernier jour d&#39;un vol, la journée est raccourcie de 24 heures à 23 heures afin que le budget du forfait ne soit pas dépassé. En outre, la stratégie de régulation du remplissage du package passe automatiquement à « [!UICONTROL Frontload] », même si elle est définie sur « [!UICONTROL even] ». Cela signifie que 65 % du budget quotidien devrait être versé avant 11 :30 (heure de Paris).

>[!MORELIKETHIS]
>
>* [ Paramètres du package ](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Bonnes pratiques pour configurer des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md)
