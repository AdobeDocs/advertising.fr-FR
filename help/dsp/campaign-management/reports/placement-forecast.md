---
title: Afficher le rapport Prévision de positionnement
description: Afficher le nombre d’impressions, les dépenses et les prévisions maximales optimales pour une stratégie de ciblage spécifique pour un emplacement.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: 2ecf1eacb2a47c20e0c05f9ff62386869b644ba6
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Afficher le rapport Prévision de positionnement

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

L’outil de prévision d’emplacement affiche le nombre d’impressions prévu, les dépenses et l’offre maximale optimale pour une stratégie de ciblage spécifique. Les prévisions sont calculées en fonction de l’inventaire global disponible avec l’emplacement et les utilisateurs uniques disponibles.

>[!NOTE]
>
>* Les codes postaux ne sont pas pris en compte dans les calculs des prévisions de placement.
>* Aucune prévision n’est générée pour les placements dont le ciblage est garanti par un programme uniquement, car la disponibilité et les dépenses sont déterministes.

## Informations dans les prévisions

Les prévisions comprennent les informations suivantes :

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** Coût estimé par millier d’impressions (eCPM) que les paramètres de ciblage peuvent espérer atteindre.

   * **[!UICONTROL Budget]:** Budget estimé pour les paramètres de ciblage.

   * **[!UICONTROL Impression]:** Nombre estimé d’impressions pour les paramètres de ciblage.

* **[!UICONTROL Budget Yield Curve]:** Nombre estimé d’impressions que l’emplacement peut diffuser à différents niveaux de budget si tous les autres paramètres de ciblage sont identiques.

* **[!UICONTROL Max Bid Yield Curve]:** Les dépenses estimées pour l’emplacement à différents niveaux d’offre max, lorsque tous les autres paramètres de ciblage sont identiques.

* **[!UICONTROL Message]:** Fournit des informations sur la production prévue, y compris tous les scénarios dans lesquels la prévision n’a pas pu être générée. Il met également en évidence les paramètres de ciblage examinés, mais non pris en compte dans ce scénario, en raison d’un manque de données.

### Calcul du budget

* Pour les emplacements qui ne sont pas affectés à un package, le budget de placement est utilisé pour les calculs. Dans un vol, le même budget global est calculé.

* Pour les emplacements dans un package, le budget affecté à l’emplacement est utilisé pour les calculs. Pendant le vol, le budget alloué au placement est calculé et inclus dans le message.

* Pour les emplacements ajoutés à un kit en vol, le budget est réparti de manière égale en fonction du nombre d&#39;emplacements. Lorsque l&#39;emplacement est en ligne, le budget affecté par le kit est calculé.

## Conditions

* Dépense minimale : 25 $ par jour ou équivalent en monnaie locale par emplacement.

* Dépense maximale : 15 000 $ par jour ou l’équivalent en monnaie locale par emplacement.

* Offre maximale minimale, Offre maximale maximale : il existe une offre maximale minimale (pour la courbe de rendement du budget) et une offre maximale (pour la courbe de rendement de l’offre maximale) par type d’emplacement. Ces valeurs sont vraies au niveau global et ne prennent pas en compte les variations régionales. Parfois, ces valeurs peuvent être trop élevées ou trop faibles pour la région ciblée.

* Données historiques : la prévision d’emplacement est disponible lorsqu’un nombre suffisant de données historiques est disponible. Vous trouverez ci-dessous des exemples de données historiques insuffisantes :

   * L’emplacement cible une nouvelle région pour la campagne.

   * L’emplacement cible une nouvelle opération de stock pour la campagne.

   * L’emplacement utilise un nouveau type d’annonce pour la campagne.

     Un emplacement est généralement un ensemble de plusieurs modèles d’annonces, tels que définis par des plateformes côté offre. Ainsi, même si l’emplacement existe depuis longtemps, le modèle d’annonce sous-jacent peut être nouveau et l’outil de prévision ne sera pas en mesure de prévoir.

## Ouvrir le rapport Prévision de positionnement

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne, puis sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Recherchez la variable **[!UICONTROL Forecast]** dans le coin supérieur droit. Si nécessaire, cliquez sur ![Prévisions](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* Il arrive que la prévision soit indisponible en raison du cache du navigateur. Si cela se produit, effacez le cache et réessayez.

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues Campaign Management](campaign-reports-about.md)
>* [Affichage des rapports de diagnostic d’emplacement](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
