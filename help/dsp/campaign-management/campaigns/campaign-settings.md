---
title: Paramètres de la campagne
description: Voir les descriptions des paramètres de campagne disponibles.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9d26e097f007b570c0f0e3b7f02c683a84d5e647
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 0%

---

# Paramètres de la campagne

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Nom de la campagne.

**[!UICONTROL Advertiser]:** (Lecture seule pour les campagnes existantes) L’annonceur applicable (marque). Sélectionnez un annonceur existant ou créez-en un.

**[!UICONTROL Advertiser URL]:** Page officielle de l&#39;annonceur. Ce champ permet d’accélérer le processus d’approbation des publicités avec les partenaires d’inventaire.

**[!UICONTROL Timezone]:** (Lecture seule pour les campagnes existantes) Fuseau horaire pour les rapports et les enchères.

**[!UICONTROL Customer PO]:** (facultatif) Commande fournisseur client pour la commande d’insertion/la commande fournisseur.

**[Dates de la campagne] :** dates de début et de fin de la campagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** (comptes en libre-service gérés par des agences utilisant des marges) Options pour la gestion des marges :

* **[!UICONTROL Would you like to manage margins for this campaign?]:** Permet de spécifier si les marges doivent être gérées pour la campagne : *[!UICONTROL Yes]* ou *[!UICONTROL No]* (valeur par défaut). Lorsque vous choisissez *[!UICONTROL Yes],* spécifiez les paramètres supplémentaires. Une fois que vous avez activé la gestion des marges et enregistré la campagne, vous ne pouvez plus désactiver la gestion des marges.

* **[!UICONTROL How would you like to compute agency fees?]:** (Campagnes avec gestion des marges uniquement) Comment calculer les frais d’agence, qui sont la partie du budget brut de la campagne qui est retenue et non incluse dans les dépenses nettes :

   * *[!UICONTROL Margin % of Total Budget]:* (valeur par défaut) Calculez les frais en pourcentage des dépenses brutes. Spécifiez le [!UICONTROL Agency Fee Type] (fixe ou composite) et le [!UICONTROL Margin %] ou le [!UICONTROL Composite Margin %].

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* Calculez les frais sous la forme d&#39;un pourcentage spécifié du coût des médias, des données et d&#39;autres coûts, et/ou des frais techniques [!DNL Adobe]. Spécifiez le [!UICONTROL Markup %] et sélectionnez les composants sur lesquels appliquer le balisage.

* **[!UICONTROL Agency Fee Type]:** (campagnes qui utilisent [!UICONTROL Margin % of Total Budget]) Type de frais d’agence.

   * *[!UICONTROL Fixed]:* (valeur par défaut) Permet à DSP de retenir un pourcentage fixe des dépenses brutes sous forme de frais d’agence. Spécifiez la [!UICONTROL Margin %].

   * *[!UICONTROL Composite]:* permet à DSP de retenir un pourcentage des dépenses brutes pour tenir compte à la fois des frais d’agence et des frais techniques [!DNL Adobe]. Spécifiez la [!UICONTROL Composite Margin %].

* **[!UICONTROL Margin %]:** (campagnes qui utilisent des [!UICONTROL Margin % of Total Budget] avec des marges fixes) Pourcentage des dépenses brutes à retenir en tant que frais d’agence. Toute modification de la valeur de la marge est appliquée aux dépenses brutes futures uniquement et non aux dépenses brutes historiques pour la campagne. La valeur [!UICONTROL Estimated Tax Withholding] est exclue des dépenses brutes avant l&#39;application de la marge. Consultez les exemples suivants, qui supposent que la campagne ne dépense pas trop ou ne dépense pas trop.

   * Exemple 1 : supposons que le [!UICONTROL Gross Budget] soit `100 USD` et que le [!UICONTROL Margin %] soit `5%` tout au long du vol. À la fin du vol de la campagne, les frais d’agence sont calculés comme `5 USD` (ce qui est `5% of 100 USD`) et les dépenses nettes sont `95 USD` (ce qui est `campaign budget [100 USD] - agency fees [5 USD]`).

   * Exemple 2 avec des modifications de la marge : pour la même campagne, supposons que [!UICONTROL Margin %] ait été modifié de `5%` en `10%` lorsque les dépenses brutes ont été `40 USD`. Pour la période précédant le changement, les frais d&#39;agence sont calculés comme `2 USD` (ce qui est `5% of 40 USD`); pour la période suivant le changement, les frais d&#39;agence sont calculés comme `6 USD` (ce qui est `10% of 60 USD`). Le total des frais d&#39;agence est calculé comme `8 USD` (ce qui est `2 USD + 6 USD`), et les dépenses nettes sont `92 USD` (ce qui est `campaign budget [100 USD] - total agency fees [8 USD]`).

   * Exemple 3 avec retenue d’impôt : supposons que la [!UICONTROL Gross Budget] soit `100 USD`, que la [!UICONTROL Estimated Tax Withholding] à la fin du vol de campagne soit `10 USD` et que la [!UICONTROL Margin %] soit `5%` tout au long du vol. À la fin du vol de la campagne, les frais d’agence sont calculés comme `4.5 USD` (ce qui est `5% of (campaign budget [100 USD] - tax withholding [USD 10])`) et les dépenses nettes sont `85.5 USD` (ce qui est `campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]`).

* **[!UICONTROL Composite Margin %]:** (campagnes qui utilisent des [!UICONTROL Margin % of Total Budget] avec des marges composites) Pourcentage des dépenses brutes qui, combinées aux frais techniques et aux frais d’agence [!DNL Adobe], doivent être retenues. Les frais d’agence sont calculés en soustrayant les frais techniques Adobe du montant de la marge composite. Toute modification de la valeur de la marge composite est appliquée aux dépenses brutes futures uniquement et non aux dépenses brutes historiques pour la campagne. La valeur [!UICONTROL Estimated Tax Withholding] est exclue des dépenses brutes avant l&#39;application de la marge composite.

  Supposons, par exemple, que le [!UICONTROL Gross Budget] soit `100 USD`, que les frais techniques [!DNL Adobe] à la fin du vol de la campagne soient `10 USD` et que le [!UICONTROL Composite Margin %] soit `17%` tout au long du vol. À la fin du vol de la campagne (en supposant que la campagne ne dépense pas trop ou ne dépense pas trop), les frais d’agence sont calculés comme `7 USD` (ce qui est `(17% of 100 USD) - 10`) et les dépenses nettes sont `93 USD` (ce qui est `campaign budget [100 USD] - agency fees [7 USD]`).

* **[!UICONTROL Markup %]:** (campagnes qui utilisent [!UICONTROL Apply Markup % on top of individual cost components]) Pourcentage à appliquer aux composants de coût spécifiés pour calculer les frais d’agence. Toute modification de la valeur de majoration est appliquée aux coûts futurs uniquement et non aux coûts historiques de la campagne.

* **[!UICONTROL Select cost components on which markup will be applied]:** (Campagnes qui utilisent [!UICONTROL Apply Markup % on top of individual cost components]) Composants de coût pour lesquels le [!UICONTROL Markup %] est appliqué. Sélectionnez tous les composants applicables : *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]* et/ou *[!UICONTROL Adobe tech fees]*. Toute modification apportée à la sélection de composant est appliquée aux coûts futurs uniquement et non aux coûts historiques de la campagne.

  Par exemple, la [!UICONTROL Markup %] est `10%` pour « [!UICONTROL Media cost] » et « [!UICONTROL Data and Other costs]. Si, à tout moment pendant le vol de la campagne, le coût des médias est `20 USD`, les données et autres coûts sont `5 USD`, et [!DNL Adobe] les frais techniques sont `2 USD`, alors les frais d&#39;agence sont calculés comme `2.50 USD` (ce qui est `10% of (20 USD + 5 USD)`, et les dépenses brutes sont `29.50 USD` (ce qui est `media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]`).

**[!UICONTROL Gross Budget]:** (Campagnes avec gestion des marges uniquement) Budget brut de la campagne, avant application des ajustements marginaux spécifiés.

**[!UICONTROL Budget]:** (campagnes sans gestion des marges) Budget global de la campagne.

**[!UICONTROL Estimated Tax Withholding]:** Retient un pourcentage des dépenses totales sur les frais de publicité, les frais de diffusion des publicités et/ou les frais de données au niveau du compte pour les taxes nationales ou locales. Les taux sont des estimations à des fins de budgétisation et de fréquence, de sorte que les taux de taxe facturés peuvent varier.

Pour estimer les taxes à retenir :

1. Cliquez sur **[!UICONTROL Update rates here]**.

1. Spécifiez le **[!UICONTROL Estimated tax rate]**, sous la forme d’un pourcentage.

1. Cochez la case en regard de chaque type de frais pour lequel vous souhaitez retenir des taxes. Les types de frais incluent :

   * *[!UICONTROL Include estimated tax - ads fee]:* S’applique à toutes les dépenses liées aux médias Advertising DSP, y compris les taxes sur les frais de gestion de campagne.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* s’applique à toutes les dépenses liées à Advertising DSP, à l’exception des médias et des données. Il exclut les taxes sur les frais de gestion de campagne

   * *[!UICONTROL Include estimated tax - data fee]:* s’applique à toutes les dépenses de données sur Advertising DSP.

1. Cliquez sur **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Aux États-Unis, les États peuvent inclure des frais d&#39;impôt différents selon les publicités, les services publicitaires et les données. Pour les organisations dans d&#39;autres pays, incluez les trois catégories de taxes pour tenir compte de la TVA.
>
>* Vous pouvez également configurer ces valeurs dans les paramètres des frais du compte.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (lecture seule pour les campagnes existantes créées depuis le 22 juin 2020 ; non disponible pour les campagnes créées avant le 22 juin 2020) Niveau auquel DSP cible les publicités et applique des limites de fréquence : *Même appareil* pour cibler un appareil ou *Personnes* pour cibler une personne sur tous ses appareils connus. **Remarque :** la prise en charge inter-appareils n’est pas disponible pour les emplacements qui ciblent les ID universels.

**[!UICONTROL Device Graph]:** (Lecture seule pour les campagnes existantes ; campagnes avec ciblage inter-appareils basé sur les personnes uniquement) Graphique d’appareil à utiliser pour le ciblage inter-appareils et la gestion des fréquences :

* *[!UICONTROL LiveRamp - U.S. only]:* disponible pour tous les annonceurs pour un ciblage inter-appareils à 0,35 $ de CPM pour les impressions diffusées à l’aide du graphique d’appareil [!DNL LiveRamp] (c’est-à-dire pour les appareils introuvables dans les segments d’audience ciblés). Vous pouvez configurer le ciblage inter-appareils au niveau de l’emplacement.

  Cette option est également disponible pour tous les annonceurs, sans frais, pour la gestion des fréquences et la mesure de l’attribution.

  La prise en charge sur l’ensemble des appareils s’applique uniquement aux emplacements qui ciblent les identifiants hérités, mais pas aux emplacements qui ciblent les identifiants universels (y compris les [!DNL LiveRamps]). Le ciblage, la gestion des fréquences et l’attribution pour les identifiants universels sont appliqués uniquement au niveau de l’identifiant.

**[!UICONTROL Frequency Cap]:** (facultatif) Nombre de fois qu’un appareil, un ID universel ou une personne unique (selon le [!UICONTROL Cross Device Level] spécifié et le paramètre de [!UICONTROL Targeting] de l’emplacement) peut recevoir des annonces publicitaires à partir de la campagne. Les options incluent le *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
> Vous pouvez définir des limites de fréquence au niveau de la campagne, du package et de l’emplacement. DSP respecte la limite de fréquence la plus stricte dans la hiérarchie de la campagne.

**[!UICONTROL Packages]:** les [packages](/help/dsp/campaign-management/packages/package-about.md) à inclure dans la campagne. Sélectionnez des packages existants et/ou créez des packages à inclure. Si vous créez des packages, consultez les descriptions des [paramètres du package](/help/dsp/campaign-management/packages/package-settings.md) pour plus d’informations.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Les paramètres suivants activent uniquement les fonctionnalités de mesure et de création de rapports. L’optimisation des performances est exécutée uniquement au niveau du package et de l’emplacement.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (facultatif) Permet de mesurer et de générer des rapports [!DNL IAS] sur la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience, à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Measure On]:** inventaire sur lequel mesurer : *[!UICONTROL Display and VPAID video inventory]* (valeur par défaut) ou *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >La visibilité de la vidéo est mesurable dans l’inventaire PAYANT uniquement.

* **[!UICONTROL IAS Account ID (AnID)]:** (annonceurs avec leurs propres comptes [!DNL IAS] ; facultatif) ID du compte [!DNL IAS] de l’organisation, que [!DNL IAS] facturerez directement pour l’utilisation.

* **[!UICONTROL IAS Team ID]:** (annonceurs avec leurs propres comptes [!DNL IAS] ; facultatif) ID d’équipe du compte [!DNL IAS] de l’organisation, que [!DNL IAS] facturerez directement pour l’utilisation. <!-- verify -->

#### Vérification de l’audience

**[!UICONTROL Comscore Campaign Ratings]:** (facultatif) Permet la mesure et le compte rendu des [!DNL Comscore] validés [!DNL Campaign Ratings] de la vérification de l’audience, à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Target Gender]:** genre à cibler : *[!UICONTROL Both]* (valeur par défaut), *[!UICONTROL Male]* ou *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** la tranche d’âge à cibler. Utilisez les curseurs gauche et droit pour réduire la plage, le cas échéant.

* **[!UICONTROL Target Country]:** (facultatif) Pays à cibler. [!DNL Comscore] mesure les impressions reçues dans les pays bénéficiaires uniquement.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** active le suivi de la mesure [!UICONTROL Attention Score] au niveau de l’emplacement (nombre moyen pondéré de [!DNL Adelaide] « [!DNL Attention Units] » entre les impressions). Les mesures sont disponibles pour tous les types d’emplacement, à l’exception de [!DNL Roku] télévision connectée, du pré-roll VPAID uniquement et de l’audio qui n’est pas un podcast. DSP associe automatiquement une balise JavaScript à tous les contenus publicitaires associés et effectue [!DNL Adelaide] le suivi des données d’exposition et les envoie quotidiennement à DSP. Vous pouvez utiliser la date pour optimiser manuellement vos dépenses en matière de tactiques de placement avec de meilleurs scores d’attention.

Le champ [!UICONTROL Attention Score] est disponible dans la section [!UICONTROL Metrics] des rapports, dans les vues [!UICONTROL Campaigns], [!UICONTROL Packages] et [!UICONTROL Placements], ainsi que dans les onglets [!UICONTROL Sites], [!UICONTROL Ads] et [!UICONTROL Inventory] de la vue [détails de l’emplacement](/help/dsp/campaign-management/reports/placement-details-view.md).

L’utilisation de segments [!DNL Adelaide] pour la mesure entraîne des frais de CPM pour chaque impression diffusée à partir d’annonces avec des balises de mesure [!DNL Adelaide]. Ces frais sont distincts des frais pour le [ciblage de l’attention au niveau du placement](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** permet la mesure et le compte rendu des performances de visibilité propriétaires à l’aide de la technologie [!DNL IAB Open Video Viewability (OpenVV)], en fonction du niveau de sensibilité spécifié :

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [À propos de la gestion de campagnes](campaign-about.md)
>* [Créer une campagne](campaign-create.md)
>* [Modifier une campagne](campaign-edit.md)
>* [Afficher le journal des modifications d&#39;une campagne](campaign-change-log.md)
