---
title: Paramètres de la campagne
description: Voir les descriptions des paramètres de campagne disponibles.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: daf995b0c40d77434d2c86c738351a33552dc555
workflow-type: tm+mt
source-wordcount: '1066'
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

* **[!UICONTROL How would you like to compute agency fees?]:** (Campagnes avec gestion des marges uniquement) Comment calculer les frais d’agence :

   * *[!UICONTROL Margin % of Total Budget]:* (par défaut) Calcule les frais en pourcentage du [!UICONTROL Gross Budget]. Spécifiez le [!UICONTROL Agency Fee Type] (fixe ou composite) et le [!UICONTROL Margin %] ou le [!UICONTROL Composite Margin %].

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* Ajoute un pourcentage spécifié de la [!UICONTROL Gross Budget] à vos coûts médias, données et autres coûts, et/ou frais techniques [!DNL Adobe]. Spécifiez le [!UICONTROL Markup %] et sélectionnez les composants sur lesquels appliquer le balisage.

* **[!UICONTROL Agency Fee Type]:** (campagnes qui utilisent [!UICONTROL Margin % of Total Budget]) Type de frais d’agence.

   * *[!UICONTROL Fixed]:* (valeur par défaut) permet à DSP de calculer automatiquement et de limiter les dépenses en fonction d’un pourcentage fixe de la [!UICONTROL Gross Budget]. Spécifiez la [!UICONTROL Margin %].

   * *[!UICONTROL Composite]:* permet à DSP de calculer automatiquement et de limiter les dépenses en fonction d’un pourcentage du [!UICONTROL Gross Budget], à l’aide du pourcentage composite des frais d’agence et des frais techniques [!DNL Adobe]. Spécifiez la [!UICONTROL Composite Margin %].

* **[!UICONTROL Margin %]:** (campagnes qui utilisent des [!UICONTROL Margin % of Total Budget] avec des marges fixes) Le balisage par défaut de chaque ordre d’insertion <!-- impression? -->, sous la forme d’un pourcentage. Ce montant est déduit du [!UICONTROL Gross Budget] pour définir le budget net de la campagne. La marge n&#39;est pas appliquée à la [!UICONTROL Estimated Tax Withholding] sur le [!UICONTROL Gross Budget].

* **[!UICONTROL Composite Margin %]:** (campagnes qui utilisent des [!UICONTROL Margin % of Total Budget] avec des marges composites) Somme des frais d’agence et des frais techniques [!DNL Adobe], en pourcentage. Ce montant est déduit du [!UICONTROL Gross Budget] pour définir le budget net de la campagne. La marge n&#39;est pas appliquée à la [!UICONTROL Estimated Tax Withholding] sur le [!UICONTROL Gross Budget].

* **[!UICONTROL Markup %]:** (Campagnes qui utilisent [!UICONTROL Apply Markup % on top of individual cost components]) Pourcentage de la [!UICONTROL Gross Budget] à ajouter aux composants de coût spécifiés.

* **[!UICONTROL Select cost components on which markup will be applied]:** (Campagnes qui utilisent [!UICONTROL Apply Markup % on top of individual cost components]) Composants de coût pour lesquels le [!UICONTROL Markup %] est appliqué. Sélectionnez tous les composants applicables : *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]* et/ou *[!UICONTROL Adobe tech fees]*.

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
