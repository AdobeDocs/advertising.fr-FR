---
title: Résolution des problèmes de performances
description: Référencez les problèmes de performances courants et découvrez comment les résoudre.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
TQID: https://experienceleague.adobe.com/CLEAjCOYzIKDaAbH4-mZxna7MK5jmpvaCjdhGScwzQs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Résolution des problèmes de performances

| Problème | Cause possible | Mesures à prendre |
| --- | --- | --- |
| Aucune dépense sur l’emplacement | L’emplacement n’inclut pas de publicités, et/ou les publicités ne sont pas actives. | Vérifiez que toutes les publicités attendues sont jointes à l’emplacement et sont approuvées et actives.<br><br>Vérifiez également si l’emplacement inclut un planning d’annonces personnalisé, ce qui peut limiter la période de vol de chaque annonce. Pour afficher le planning publicitaire d’un emplacement dans la vue Emplacements , cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** en regard du nom de l’emplacement. |
| | Les dates affectées ne sont pas comprises dans les dates de vol configurées. | Vérifiez que les dates des vols sont valides au niveau de la campagne, du package et de l&#x200B;emplacement. |
| | L’objectif budgétaire a été atteint et/ou n’est pas assez élevé. | Vérifiez les paramètres de budget au niveau de la campagne, du package et de l’emplacement. |
| | Le compte n&#39;a pas assez de financement. | Pour voir si votre compte est suffisamment financé, accédez à **[!UICONTROL Settings]** > **[!UICONTROL Account]** et vérifiez le montant de la [!UICONTROL Usable Funds]. Si vous avez besoin d’ajouter des fonds, contactez l’équipe chargée de votre compte Adobe. |
| | Aucun inventaire n&#39;est disponible. | Vérifiez si les sources d&#39;inventaire spécifiées ([!UICONTROL Public], [!UICONTROL Private] ou [!UICONTROL On Demand]) sont :<ul><li>Configurez correctement.</li><li>Actif et envoi par enchères.</li><li>Compatible avec l’annonce publicitaire et le type d’emplacement applicables.</li></ul><br>Si toutes les sources de stock sont valides et actives, ciblez des sources de stock supplémentaires ou toutes lorsque cela est possible. |
| | Aucun utilisateur n’est disponible. | Vérifiez que les cibles d’audience spécifiées incluent suffisamment d’utilisateurs actifs. Si ce n’est pas le cas, développez les cibles en ajoutant d’autres audiences. |
| Faible dépense en placement | La section [!UICONTROL Non Bids] du rapport de diagnostics d&#39;emplacement indique les raisons possibles pour lesquelles l&#39;emplacement n&#39;a pas enchéri. | [Consultez le rapport de [!UICONTROL Non Bids]](/help/dsp/campaign-management/reports/placement-diagnostics.md) pour comprendre pourquoi l’emplacement n’a pas fait d’enchères.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | L’emplacement utilise des [filtres de pré-enchères](/help/dsp/campaign-management/placements/placement-settings.md) qui limitent les enchères. | Abaissez de 5 % les seuils des filtres de pré-enchères pour évaluer le solde des dépenses et de la performance. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Gardez à l’esprit que l’utilisation de plusieurs cibles d’emplacement, telles que les filtres de pré-enchères, les zones géographiques, les stocks et les audiences, peut limiter de manière cumulative les enchères et les dépenses. |
| | Le taux de gain de l’emplacement est faible. | Augmentez le [!UICONTROL Max Bid] pour améliorer le taux de gain.<br><br><b>REMARQUE :</b> les prix des stocks peuvent varier en fonction du ciblage de l’emplacement.<br><br>Un taux de gain de 10 % est considéré comme sain. |
| | Un faible nombre de stocks est disponible. | Dans la mesure du possible, ciblez toutes les sources de stock ou d’autres sources.<br><br>Gardez à l’esprit que l’utilisation de plusieurs cibles d’emplacement, telles que les filtres de pré-enchères, les zones géographiques, les stocks et les audiences, peut limiter de manière cumulative les enchères et les dépenses. |
| | Un faible nombre d’utilisateurs est disponible. | Vérifiez que les cibles d’audience spécifiées incluent suffisamment d’utilisateurs actifs. Si ce n’est pas le cas, développez les cibles en ajoutant d’autres audiences.<br><br>Gardez à l’esprit que l’utilisation de plusieurs cibles d’emplacement, telles que les filtres de pré-enchères, les zones géographiques, les stocks et les audiences, peut limiter de manière cumulative les enchères et les dépenses. |
| | Le package comprend un grand nombre d’emplacements actifs. | Réduisez le nombre d’emplacements actifs dans le package ou augmentez le budget global du package.<br><br>Si le package comporte de nombreux emplacements, mais pas suffisamment de budget, DSP peut ne pas être en mesure d’allouer suffisamment de budget à chaque emplacement. Chaque placement doit avoir la possibilité de dépenser au moins 2 USD/jour. Par exemple, si votre forfait dispose d&#39;un budget de 10 USD/jour, il est préférable d&#39;inclure cinq emplacements ou moins. &#x200B; |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [&#x200B; Paramètres du package &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres de Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md)
