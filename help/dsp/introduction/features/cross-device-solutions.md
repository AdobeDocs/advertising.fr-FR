---
title: Solutions sur plusieurs appareils
description: En savoir plus sur les fonctionnalités inter-appareils.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: 2c7ba1862b1883b4523d9121d8b0761129ad70fb
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Solutions sur plusieurs appareils

L’intégration d’Advertising DSP à [!DNL LiveRamp] vous permet d’étendre votre audience à tous les appareils connus d’une personne, et pas seulement aux appareils suivis par votre marque. L’intégration fournit également un capping de la fréquence et une mesure d’attribution sur tous les appareils.

Lorsque vous utilisez un graphique d’appareil basé sur les personnes pris en charge, vous pouvez :

* Associez les audiences sur l’ensemble des canaux et des appareils pour diffuser des annonces aux personnes et aux ménages, plutôt qu’aux appareils.
* Équilibrer et exposer en comprenant et en plafonnant la fréquence entre les individus.
* Testez des stratégies qui exposent ou convertissent des audiences sur plusieurs canaux ou appareils.

## Avantages du graphique d’appareil [!DNL LiveRamp]

* Fournit un pool de données déterministe, y compris des données client hors ligne

* Fournit une couverture uniforme entre les ID de cookie et les ID d’appareil mobile

* Comprend des données provenant principalement des États-Unis

* Est libre pour le capping de la fréquence et la mesure d’attribution

* Un prix de 0,35 $ par CPM pour les impressions étendues (impressions diffusées uniquement à l’aide du graphique d’appareil [!DNL LiveRamp] plutôt que sur les appareils trouvés dans les segments ciblés)

  Le taux est reflété sur votre carte tarifaire de compte.

## Gestion des fréquences basée sur les personnes

La gestion des fréquences basée sur les personnes vous permet de spécifier des limites de fréquence au niveau de la personne, plutôt qu’au niveau de l’appareil, pour un véritable contrôle de l’exposition aux médias.

### Activer la gestion des fréquences basée sur les personnes

* **Campagnes :** lorsque vous créez une campagne, vous pouvez spécifier un paramètre de [!UICONTROL Cross-Device Level]. Activez « [!UICONTROL Same Device] » -> « [!UICONTROL People] » et sélectionnez un graphique d’appareil. Le graphique d’appareil spécifié est utilisé pour le ciblage inter-appareils au niveau de l’emplacement et pour la gestion des fréquences basée sur les personnes au niveau de la campagne, du package et de l’emplacement. Les limites de fréquence s’appliquent à tous les appareils connus d’une personne.

Pour plus d’informations, voir [Paramètres de Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Une fois une campagne enregistrée, vous ne pouvez plus modifier son paramètre [!UICONTROL Cross Device Level].

* **Packages :** vous pouvez éventuellement définir des limites de fréquence supplémentaires au niveau du package. DSP respecte la limite de fréquence la plus stricte dans la hiérarchie de la campagne.

* **Emplacements :** vous pouvez éventuellement définir des limites de fréquence supplémentaires au niveau de l’emplacement. DSP respecte la limite de fréquence la plus stricte dans la hiérarchie de la campagne.

## Ciblage basé sur les personnes

Le ciblage basé sur les personnes vous permet de trouver des clients sur les ordinateurs de bureau et les appareils mobiles.

### Activer le ciblage basé sur les personnes

* **Campagnes :** lorsque vous créez une campagne, vous pouvez spécifier un paramètre de [!UICONTROL Cross-Device Level]. Activez « [!UICONTROL Same Device] » -> « [!UICONTROL People] » et sélectionnez un graphique d’appareil. Le graphique d’appareil spécifié est utilisé pour le ciblage inter-appareils au niveau de l’emplacement et pour la gestion des fréquences basée sur les personnes.

Pour plus d’informations, voir [Paramètres de Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Emplacements :** lorsque vous sélectionnez des cibles d’audience pour un emplacement dans une campagne avec un graphique d’appareil spécifié, une option de [!UICONTROL Cross-Device Targeting] vous permet d’étendre votre ciblage sur tous les appareils connus d’une personne (selon le graphique d’appareil spécifié dans les paramètres de la campagne), même les appareils qui ne se trouvent pas dans les segments spécifiés.

### Configurer des rapports pour le ciblage basé sur les personnes

Vous pouvez inclure les mesures suivantes dans les rapports personnalisés :

* **Impressions étendues :** (dans la section [!UICONTROL Build Your Report] sous [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) volume d’impressions incrémentielles diffusées en utilisant un graphique d’appareil (et introuvables dans les segments d’audience d’origine). Cette mesure est également utilisée pour calculer les frais applicables associés à l’utilisation d’un graphique d’appareil tiers.

  Pour déterminer le coût de vos impressions étendues au cours d’une période donnée, exécutez un rapport personnalisé qui inclut la colonne [!UICONTROL Extended Impressions], puis multipliez le nombre total d’impressions étendues par 0,00035 $ (0,35 $/1 000 impressions).

  Le coût agrégé est également inclus dans la colonne [!UICONTROL Billable Other Net Spend] (sous [!UICONTROL Metrics] > [!UICONTROL Spend]), bien que cette mesure inclue également d’autres frais de campagne que vous avez peut-être ajoutés.

* **Graphique d’appareil :** (dans la section [!UICONTROL Build Your Report] sous [!UICONTROL Dimensions] > [!UICONTROL Campaign]) graphique d’appareil sélectionné pour une campagne, un package ou un emplacement particulier.

## Mesure d’attribution basée sur les personnes

*Annonceurs avec suivi des conversions Adobe Advertising uniquement*

Avec l’attribution basée sur les personnes, vous pouvez attribuer les conversions qui ont eu lieu sur un appareil différent de celui sur lequel l’exposition au média a eu lieu. La mesure d’attribution basée sur les personnes est disponible dans DSP, [!DNL Adobe Advertising Creative] et [!DNL Adobe Advertising Search, Social, & Commerce] pour les annonceurs qui ont implémenté des pixels de conversion Adobe Advertising sur leurs sites.

### Activer la mesure d’attribution basée sur les personnes

Si vous souhaitez activer la mesure d’attribution entre appareils, contactez l’équipe chargée de votre compte Adobe.

### Configurer des rapports [!UICONTROL Conversion] pour l’attribution de conversions entre appareils

#### Paramètres des rapports [!UICONTROL Conversion]

Lorsqu’un graphique d’appareil est activé pour la mesure d’attribution, le rapport [!UICONTROL Conversion] comprend un paramètre de [!UICONTROL Cross-Device Breakout] qui vous permet d’inclure jusqu’à trois colonnes distinctes pour chaque mesure de conversion, notamment :

* &lt;*Conversion*>[!UICONTROL (tp)] : inclut le nombre total de conversions (nombre total de personnes), qui inclut les conversions sur le même appareil et les conversions sur plusieurs appareils (le cas échéant). Dans le rapport, « [!UICONTROL (tp)] » est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, « Réponses(le)(tl)(tp) »).

* &lt;*Conversion*>[!UICONTROL (sd)] : (facultatif) inclut uniquement les conversions pour lesquelles un seul appareil a été suivi dans le chemin de conversion. Dans le rapport, « [!UICONTROL (sd)] » est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, « Réponses(le)(tl)(sd) »).

* &lt;*Conversion*>[!UICONTROL (xd)] : (facultatif) inclut uniquement les conversions pour lesquelles plusieurs appareils ont été suivis dans le chemin de conversion. Dans le rapport, « [!UICONTROL (xd)] » est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, « Réponses(le)(tl)(xd) »).

#### Interprétation du rapport [!UICONTROL Conversion]

Triez le pourcentage de conversions totales sur plusieurs appareils ([!UICONTROL (xd)]/[!UICONTROL (tl)]) de élevé à faible pour comprendre ce qui entraîne des conversions sur plusieurs appareils supérieures à la moyenne. Vous pouvez l’utiliser pour éclairer votre stratégie de création ou de ciblage afin de faire correspondre la messagerie et l’investissement dans le canal au comportement des utilisateurs.

* Packages : identifiez les packages qui génèrent le plus grand nombre de conversions totales et ceux qui présentent un pourcentage élevé de conversions entre appareils. Cela peut vous aider à comprendre où concentrer les dépenses.

* Emplacements : comparez les performances et l’attribution des emplacements (par exemple, une publicité web mobile peut générer des conversions sur le bureau). Sans graphique d’appareil pour l’attribution, vous pouvez ignorer l’impact d’un emplacement web mobile sur les conversions sur le bureau, ou il peut être noyé si la majorité de vos utilisateurs effectuent une conversion sur le bureau et non sur le web mobile.

* Publicités : découvrez les publicités qui génèrent des conversions plus élevées, et quantifiez leur valeur et leur impact sur les navigateurs web et les environnements d’applications mobiles.

* Sites : optimisez les sites au lieu d&#39;exclure manuellement complètement les sites. Si un site web génère des conversions entre appareils, vous pouvez voir sur quels appareils ce comportement se produit.

* Offres : améliorez l’optimisation manuelle en vérifiant les offres d’inventaire qui génèrent des conversions entre appareils, puis en décidant si vous devez étendre votre ciblage pour inclure davantage d’appareils et de canaux dans ces offres.

>[!MORELIKETHIS]
>
>* [Paramètres des rapports ](/help/dsp/reports/report-settings.md)
>* [Paramètres de Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [ Paramètres du package ](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
