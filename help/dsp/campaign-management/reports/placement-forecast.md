---
title: Afficher le rapport de prévision d'emplacement
description: Affichez le nombre d’impressions, les dépenses et l’enchère maximale optimale prévue pour une stratégie de ciblage particulière pour un emplacement.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Afficher le rapport de prévision d&#39;emplacement

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

L’outil de prévision d’emplacement affiche le nombre d’impressions prévu, les dépenses et l’enchère maximale optimale pour une stratégie de ciblage particulière. Les prévisions sont calculées en fonction de l&#39;inventaire global disponible avec l&#39;emplacement et des utilisateurs uniques disponibles.

>[!NOTE]
>
>* Les codes postaux ne sont pas pris en compte dans les calculs de prévision d’emplacement.
>* Aucune prévision n’est générée pour les emplacements avec uniquement un ciblage programmatique garanti (PG), car la disponibilité et les dépenses sont déterministes.

## Informations de la prévision

La prévision comprend les informations suivantes :

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** coût estimé pour mille impressions (eCPM) que les paramètres de ciblage peuvent s’attendre à atteindre.

   * **[!UICONTROL Budget]:** Budget estimé pour les paramètres de ciblage.

   * **[!UICONTROL Impression]:** nombre estimé d’impressions pour les paramètres de ciblage.

* **[!UICONTROL Budget Yield Curve]:** nombre estimé d’impressions que l’emplacement peut générer à différents niveaux budgétaires si tous les autres paramètres de ciblage sont identiques.

* **[!UICONTROL Max Bid Yield Curve]:** Estimation des dépenses pour l’emplacement à différents niveaux d’enchères maximales, lorsque tous les autres paramètres de ciblage sont identiques.

* **[!UICONTROL Message]:** fournit des informations sur la sortie prévue, y compris les scénarios dans lesquels la prévision n’a pas pu être générée. Il met également en évidence tous les paramètres de ciblage examinés, mais non pris en compte dans ce scénario en raison d’un manque de données.

### Calcul du budget

* Pour les emplacements qui ne sont pas affectés à un package, le budget d&#39;emplacement est utilisé pour les calculs. Dans un vol, le même budget global est calculé.

* Pour les emplacements au sein d&#39;un package, le budget affecté à l&#39;emplacement est utilisé pour les calculs. Pendant le vol, le budget alloué à l&#39;emplacement est calculé et inclus dans le message.

* Pour les placements ajoutés à un package en cours, le budget est divisé à parts égales en fonction du nombre de placements. Lorsque l&#39;emplacement est activé, le budget affecté par le package est calculé.

## Conditions requises

* Dépenses minimales : 25 $ par jour ou l’équivalent en devise locale par emplacement.

* Dépenses maximales : 15 000 $ par jour ou l’équivalent en devise locale par emplacement.

* Enchère maximum minimum, enchère maximum : il existe une enchère maximum minimum (pour la courbe de rendement budgétaire) et une enchère maximum (pour la courbe de rendement maximum) par type d’emplacement. Ces valeurs sont vraies globalement et ne prennent pas en compte les variations régionales. Parfois, ces valeurs peuvent être trop élevées ou trop basses pour la région ciblée.

* Données historiques : la prévision d’emplacement est disponible lorsque des données historiques suffisantes sont disponibles. Voici des exemples de cas où des données historiques insuffisantes peuvent être disponibles :

   * L’emplacement cible une nouvelle région pour la campagne.

   * L’emplacement cible une nouvelle transaction de stock pour la campagne.

   * L’emplacement utilise un nouveau type d’annonce pour la campagne.

     Un emplacement consiste généralement en un ensemble de plusieurs modèles d’annonces publicitaires définis par des plateformes côté offre. Ainsi, même si l’emplacement existe depuis longtemps, si le modèle d’annonce publicitaire sous-jacent est nouveau, l’outil de prévision ne peut pas créer de prévision.

## Ouvrir le rapport de prévision d&#39;emplacement

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne, puis sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Recherchez la section **[!UICONTROL Forecast]** en haut à droite. Si nécessaire, cliquez sur ![&#x200B; Prévision &#x200B;](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* Parfois, la prévision peut être indisponible en raison de la mise en cache du navigateur. Si cela se produit, effacez le cache et réessayez.

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues de gestion de campagnes](campaign-reports-about.md)
>* [Afficher les rapports de diagnostic d&#39;emplacement](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
