---
title: Solutions multi-appareils
description: En savoir plus sur les fonctionnalités multi-appareils.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Solutions multi-appareils

L’intégration d’Advertising DSP avec [!DNL LiveRamp] vous permet d’étendre votre audience à tous les appareils connus d’une personne, et pas seulement aux appareils dont votre marque a fait le suivi. L’intégration fournit également une mesure de limitation et d’attribution des fréquences sur tous les appareils.

Lorsque vous utilisez un graphique d’appareil basé sur les personnes pris en charge, vous pouvez :

* Faire correspondre les audiences sur les canaux et les appareils pour diffuser des publicités aux personnes et aux ménages, plutôt qu’aux appareils.
* Équilibrer l’exposition en comprenant et en plafonnant la fréquence entre les individus.
* Stratégies de test qui exposent ou convertissent des audiences sur plusieurs canaux ou appareils.

## Avantages du graphique de périphérique [!DNL LiveRamp]

* Fournit un pool de données déterministes, y compris les données client hors ligne.

* Offre une couverture égale entre les ID de cookie et les ID d’appareils mobiles

* Inclut principalement des données provenant des États-Unis

* Est gratuit pour le plafonnement des fréquences et la mesure d’attribution

* Prix à 0,35 CPM pour les impressions étendues (impressions diffusées uniquement à l’aide du graphique d’appareil [!DNL LiveRamp] plutôt que sur les appareils trouvés dans les segments d’audience ciblés)

  Le taux est répercuté sur votre carte de taux de compte.

## Gestion des fréquences basée sur les personnes

La gestion des fréquences basée sur les personnes vous permet de spécifier des limites de fréquence au niveau de la personne, plutôt qu’au niveau de l’appareil, pour un véritable contrôle de l’exposition aux médias.

### Activation de la gestion des fréquences basée sur les personnes

* **Campagnes :** Lorsque vous créez une campagne, vous pouvez spécifier un paramètre [!UICONTROL Cross-Device Level]. Activez &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; et sélectionnez une représentation graphique des appareils. Le graphique d’appareil spécifié est utilisé pour le ciblage entre appareils au niveau de l’emplacement et pour la gestion des fréquences basée sur les personnes au niveau de la campagne, du package et de l’emplacement. Les limites de fréquence s’appliquent à tous les périphériques connus d’une personne.

Pour plus d’informations, voir [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Une fois une campagne enregistrée, vous ne pouvez pas modifier son paramètre [!UICONTROL Cross Device Level].

* **Packages :** Vous pouvez éventuellement définir des limites de fréquence supplémentaires au niveau du package. DSP respecte la limite de fréquence la plus stricte de la hiérarchie de l&#39;opération.

* **Emplacements :** Vous pouvez éventuellement définir des limites de fréquence supplémentaires au niveau de l’emplacement. DSP respecte la limite de fréquence la plus stricte de la hiérarchie de l&#39;opération.

## Ciblage basé sur les personnes

Le ciblage basé sur les personnes vous permet de trouver des clients sur les ordinateurs de bureau et les appareils mobiles.

### Activation du ciblage basé sur les personnes

* **Campagnes :** Lorsque vous créez une campagne, vous pouvez spécifier un paramètre [!UICONTROL Cross-Device Level]. Activez &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; et sélectionnez une représentation graphique des appareils. Le graphique d’appareil spécifié est utilisé pour le ciblage entre appareils au niveau de l’emplacement et pour la gestion des fréquences basée sur les personnes.

Pour plus d’informations, voir [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Emplacements :** Lorsque vous sélectionnez des cibles d’audience pour un emplacement dans une campagne avec une représentation graphique des appareils spécifiée, une option [!UICONTROL Cross-Device Targeting] vous permet d’étendre le ciblage sur tous les appareils connus d’une personne (selon la représentation graphique des appareils spécifiée dans les paramètres de campagne), même sur les appareils qui ne figurent pas dans les segments spécifiés.

### Configuration des rapports pour le ciblage basé sur les personnes

Vous pouvez inclure les mesures suivantes dans les rapports personnalisés :

* **Impressions étendues :** (dans la section [!UICONTROL Build Your Report] sous [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) Volume d’impressions incrémentielles diffusées en utilisant une représentation graphique des appareils (et introuvables dans les segments d’audience d’origine). Cette mesure est également utilisée pour calculer les frais applicables associés à l’utilisation d’une représentation graphique des appareils tiers.

  Pour déterminer le coût de vos impressions étendues au cours d’une période, exécutez un rapport personnalisé qui inclut la colonne [!UICONTROL Extended Impressions], puis multipliez le nombre total d’impressions étendues par 0,0035 $ (impressions de 0,35/1000 $).

  Le coût agrégé est également inclus dans la colonne [!UICONTROL Billable Other Net Spend] (sous [!UICONTROL Metrics] > [!UICONTROL Spend]), bien que cette mesure inclut également d’autres frais de campagne que vous avez peut-être ajoutés.

* **Graphique d’appareil :** (dans la section [!UICONTROL Build Your Report] sous [!UICONTROL Dimensions] > [!UICONTROL Campaign]) Graphique d’appareil sélectionné pour une campagne, un package ou un emplacement spécifique.

## Mesure d’attribution basée sur les personnes

*Annonceurs avec suivi des conversions par Adobe Advertising uniquement*

Avec l’attribution basée sur les personnes, vous pouvez attribuer des conversions qui ont eu lieu sur un appareil différent de celui sur lequel l’exposition au média s’est produite. La mesure d’attribution basée sur les personnes est disponible sur DSP, [!DNL Adobe Advertising Creative] et [!DNL Adobe Advertising Search, Social, & Commerce] pour les annonceurs qui ont implémenté des pixels de conversion d’Adobe Advertising sur leurs sites.

### Activation de la mesure d’attribution basée sur les personnes

Si vous souhaitez activer la mesure d’attribution entre appareils, contactez votre équipe de compte d’Adobe.

### Configuration des rapports de conversion pour l’attribution des conversions entre appareils

#### Paramètres du rapport de conversion

Lorsqu’un graphique d’appareil est activé pour la mesure d’attribution, le rapport [!UICONTROL Conversion] comprend un paramètre [!UICONTROL Cross-Device Breakout] qui vous permet d’inclure jusqu’à trois colonnes distinctes pour chaque mesure de conversion, notamment :

* &lt;*Conversion*>[!UICONTROL (tp)] : inclut le nombre total de conversions (nombre total de personnes), qui inclut les conversions sur le même appareil et les conversions sur plusieurs appareils (le cas échéant). Dans le rapport, &quot;[!UICONTROL (tp)]&quot; est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, &quot;Réponses(le)(tl)(tp)).

* &lt;*Conversion*>[!UICONTROL (sd)] : (facultatif) comprend uniquement les conversions pour lesquelles un seul appareil a été suivi dans le chemin de conversion. Dans le rapport, &quot;[!UICONTROL (sd)]&quot; est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, &quot;Réponses(le)(tl)(sd)).

* &lt;*Conversion*>[!UICONTROL (xd)] : (facultatif) comprend uniquement les conversions pour lesquelles plusieurs appareils ont été suivis dans le chemin de conversion. Dans le rapport, &quot;[!UICONTROL (xd)]&quot; est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, &quot;Réponses(le)(tl)(xd)).

#### Interprétation du rapport de conversion

Triez le pourcentage de conversions totales qui sont multi-appareils ([!UICONTROL (xd)]/[!UICONTROL (tl)]) de haut à bas pour comprendre ce qui génère des conversions inter-appareils au-dessus de la moyenne. Vous pouvez l’utiliser pour informer votre stratégie de création ou de ciblage afin de mettre en correspondance la messagerie et l’investissement des canaux avec le comportement des utilisateurs.

* Modules : découvrez les modules qui génèrent le plus de conversions totales et ceux qui présentent un pourcentage élevé de conversions entre appareils. Cela peut vous aider à comprendre où dépenser.

* Emplacements : comparez les performances et l’attribution des emplacements (par exemple, une publicité web mobile peut générer des conversions sur le bureau). Sans graphique d’appareil pour l’attribution, vous pouvez ignorer l’impact d’un emplacement web mobile sur les conversions de bureau, ou il peut être masqué si la majorité de vos utilisateurs se convertissent sur ordinateur et non sur le web mobile.

* Publicités : découvrez les publicités qui génèrent le plus de conversions et quantifiez leur valeur et leur impact sur les navigateurs web et les environnements d’applications mobiles.

* Sites : optimisez les sites d’un site à l’autre plutôt que d’exclure complètement les sites manuellement. Si un site web génère des conversions entre appareils, vous pouvez voir sur quels appareils ce comportement se produit.

* Offres : améliorez l’optimisation manuelle en vérifiant les offres d’inventaire qui génèrent des conversions entre appareils, puis en décidant si vous devez étendre votre ciblage afin d’inclure davantage de périphériques et de canaux dans ces offres.

>[!MORELIKETHIS]
>
>* [Paramètres de rapport](/help/dsp/reports/report-settings.md)
>* [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md)
