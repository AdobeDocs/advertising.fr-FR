---
title: Paramètres de campagne
description: Reportez-vous à la description des paramètres de campagne disponibles.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 0fbdc7e38026d71483c2de1406a4110066690130
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Paramètres de campagne

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Nom de la campagne.

**[!UICONTROL Advertiser]:** (Lecture seule pour les campagnes existantes) L’annonceur (marque) applicable. Sélectionnez un annonceur existant ou créez-en un.

**[!UICONTROL Advertiser URL]:** Page officielle de l’annonceur. Ce champ accélère le processus d’approbation des publicités avec les partenaires d’inventaire.

**[!UICONTROL Timezone]:** (Lecture seule pour les campagnes existantes) Fuseau horaire pour la création de rapports et l’offre.

**[!UICONTROL Customer PO]:** (Facultatif) Commande d’achat d’un client pour la commande d’insertion/la commande d’achat.

**[Dates de campagne] :** Les dates de début et de fin de la campagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Permet de gérer les marges de la campagne : *[!UICONTROL Yes]* ou *[!UICONTROL No]* (valeur par défaut).

Lorsque vous choisissez *[!UICONTROL Yes],* indiquez le type de marge et le montant :

* **[!UICONTROL Margin Type]:** Type de marge. Vous ne pouvez pas modifier le type de marge une fois que vous avez activé la gestion des marges et enregistré l&#39;opération.

   * *[!UICONTROL Fixed]:* (valeur par défaut) Permet DSP calculer et plafonner automatiquement les dépenses en fonction d’un pourcentage de marge fixe de l’ [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* permet de gérer les marges jusqu’au niveau de placement en spécifiant un [!UICONTROL Budget Reserve %] et [!UICONTROL Gross Budget] distincts pour chaque package et emplacement dans la campagne. DSP optimise en fonction de l&#39;efficacité financière de chaque placement, sans garantir une marge spécifique. Utilisez cette option pour les commandes d’insertion composées de plusieurs éléments de ligne pour lesquels vous avez accepté de fournir un nombre fixe d’unités ou de types d’unités à un rythme fixe.

* **[!UICONTROL Fixed Margin %]:** (Campagnes avec des marges fixes uniquement) Balises par défaut pour chaque ordre d’insertion <!-- impression? -->, en pourcentage. Ce montant est déduit du [!UICONTROL Gross Budget] pour définir le budget net de la campagne.

* **[!UICONTROL Budget Reserve %]:** (Campagnes avec des marges fixes uniquement ; facultatif) réserve un pourcentage spécifié de [!UICONTROL Gross Budget] comme protection. Ce montant est déduit du [!UICONTROL Gross Budget] pour définir le budget net de la campagne.

**[!UICONTROL Gross Budget]:** (Campagnes avec gestion des marges uniquement) Le budget brut de l’opération, avant l’application des ajustements marginaux spécifiés.

Vous pouvez éventuellement ajouter un budget brut quotidien, hebdomadaire ou mensuel supplémentaire :

1. Cliquez sur **[!UICONTROL Add an additional Gross Budget]**.

1. Saisissez le **[!UICONTROL Gross Budget]** et sélectionnez l’intervalle de budget : *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly]*.

Le budget net total, qui correspond au plafond de dépenses de l&#39;opération, est calculé automatiquement sur la base des paramètres de marge et est renseigné sous cette valeur.

**[!UICONTROL Budget]:** (Campagnes sans gestion des marges) Budget global de la campagne.

**[!UICONTROL Estimated Tax Withholding]:** retient un pourcentage du total des dépenses par rapport aux frais de publicité, aux frais de service publicitaire et/ou aux frais de données au niveau du compte pour les impôts locaux ou nationaux. Les taux sont des estimations à des fins de budget et de calendrier, de sorte que les taux d’imposition facturés peuvent varier.

Pour estimer les impôts à retenir :

1. Cliquez sur **[!UICONTROL Update rates here]**.

1. Indiquez le **[!UICONTROL Estimated tax rate]**, en pourcentage.

1. Cochez la case en regard de chaque type de taxe pour lequel vous souhaitez retenir des impôts. Les types de frais incluent :

   * *[!UICONTROL Include estimated tax - ads fee]:* s’applique à toutes les dépenses de médias Advertising DSP, y compris les taxes sur les frais de gestion de campagne.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* s’applique à toutes les dépenses dans Advertising DSP, à l’exception des médias et des données. Elle exclut les taxes pour les frais de gestion de campagne

   * *[!UICONTROL Include estimated tax - data fee]:* s’applique à toutes les données dépensées dans Advertising DSP.

1. Cliquez sur **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Aux États-Unis, les États peuvent varier dans leur inclusion des taxes entre les publicités, les publicités et les données. Pour les organisations d’autres pays, incluez les trois catégories de taxes pour tenir compte de la TVA.
>
>* Vous pouvez également configurer ces valeurs dans les paramètres de frais du compte.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Lecture seule pour les campagnes existantes créées depuis le 22 juin 2020 ; non disponible pour les campagnes créées avant le 22 juin 2020) Niveau auquel DSP cible des publicités et applique des limites de fréquence : *Même appareil* pour cibler un appareil ou *Personnes* pour cibler une personne sur tous ses appareils connus. **Remarque :** La prise en charge inter-appareils n’est pas disponible pour les emplacements qui ciblent des identifiants universels.

**[!UICONTROL Device Graph]:** (Lecture seule pour les campagnes existantes ; campagnes avec ciblage inter-appareils basé sur les personnes uniquement) Graphique d’appareil à utiliser pour le ciblage inter-appareils et la gestion des fréquences :

* *[!UICONTROL LiveRamp - U.S. only]:* Disponible pour tous les annonceurs pour un ciblage entre appareils à 0,35 $ CPM pour les impressions diffusées à l’aide du graphique d’appareil [!DNL LiveRamp] (c’est-à-dire pour les appareils non trouvés dans les segments d’audience ciblés). Vous pouvez configurer le ciblage sur plusieurs appareils au niveau de l’emplacement.

  Cette option est également disponible pour tous les annonceurs, sans frais, pour la gestion des fréquences et la mesure d’attribution.

  La prise en charge inter-appareils s’applique uniquement aux emplacements qui ciblent des identifiants hérités, mais pas aux emplacements qui ciblent des identifiants universels (y compris [!DNL LiveRamps]). Le ciblage, la gestion des fréquences et l’attribution pour les identifiants universels sont appliqués au niveau des identifiants uniquement.

**[!UICONTROL Frequency Cap]:** (Facultatif) Le nombre de fois qu’un appareil unique, un identifiant universel ou une personne (en fonction du paramètre [!UICONTROL Cross Device Level] spécifié et du paramètre [!UICONTROL Targeting] de l’emplacement) peuvent être diffusées des publicités à partir de la campagne. Les options incluent *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
> Vous pouvez définir des limites de fréquence aux niveaux de la campagne, du kit et de l’emplacement. DSP respecte la limite de fréquence la plus stricte de la hiérarchie de l&#39;opération.

**[!UICONTROL Packages]:** [packages](/help/dsp/campaign-management/packages/package-about.md) à inclure dans la campagne. Sélectionnez les packages existants et/ou créez des packages à inclure. Si vous créez des packages, reportez-vous à la description des [paramètres de package](/help/dsp/campaign-management/packages/package-settings.md) pour plus d’informations.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Les paramètres suivants activent uniquement les fonctionnalités de mesure et de création de rapports. L’optimisation des performances est exécutée uniquement au niveau du package et de l’emplacement.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Facultatif) Active la mesure [!DNL IAS] et la création de rapports sur la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience, à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Measure On]:** Inventaire sur lequel mesurer : *[!UICONTROL Display and VPAID video inventory]* (valeur par défaut) ou *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >La visibilité des vidéos est mesurable sur l’inventaire VPAID uniquement.

* **[!UICONTROL IAS Account ID (AnID)]:** (Publicitaires disposant de leurs propres comptes [!DNL IAS] ; facultatif) ID de compte [!DNL IAS] de l’organisation, qui [!DNL IAS] facturera directement pour l’utilisation.

* **[!UICONTROL IAS Team ID]:** (Publicitaires disposant de leurs propres comptes [!DNL IAS] ; facultatif) ID d’équipe pour le compte [!DNL IAS] de l’organisation, dont [!DNL IAS] facturera directement l’utilisation. <!-- verify -->

**[!UICONTROL MOAT]:** (Facultatif) Permet la mesure [!DNL MOAT] et la création de rapports sur la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience. Des frais supplémentaires s’appliquent. **Remarque :** [!DNL Oracle] abandonnera son activité publicitaire d’ici le 30 septembre 2024, y compris tous les services de [!DNL MOAT].

#### Vérification de l’audience

**[!UICONTROL Comscore Campaign Ratings]:** (Facultatif) Active la mesure [!DNL Comscore] validée [!DNL Campaign Ratings] et la création de rapports de vérification d’audience à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Target Gender]:** Genre à cibler : *[!UICONTROL Both]* (valeur par défaut), *[!UICONTROL Male]* ou *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** tranche d’âge à cibler. Utilisez les curseur gauche et droit pour réduire la plage selon vos besoins.

* **[!UICONTROL Target Country]:** (facultatif) pays à cibler. [!DNL Comscore] mesure les impressions diffusées dans les pays pris en charge uniquement.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** active le suivi de la mesure [!UICONTROL Attention Score] de niveau emplacement (le nombre moyen pondéré de [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; sur l’ensemble des impressions). Les mesures sont disponibles pour tous les types d’emplacements, à l’exception de [!DNL Roku] la télévision connectée, le preroll VPAID uniquement et le son qui n’est pas un podcast. DSP associe automatiquement une balise JavaScript à tous les créatifs associés, et [!DNL Adelaide] suit les données d’exposition et les envoie DSP tous les jours. Vous pouvez utiliser la date pour optimiser manuellement vos dépenses en faveur des tactiques de placement avec de meilleurs scores d’attention.

Le champ [!UICONTROL Attention Score] est disponible dans la section [!UICONTROL Metrics] des rapports ; dans les [!UICONTROL Campaigns], [!UICONTROL Packages] et [!UICONTROL Placements] vues ; et dans les onglets [!UICONTROL Sites], [!UICONTROL Ads] et [!UICONTROL Inventory] de la [ {vue des détails de l’emplacement](/help/dsp/campaign-management/reports/placement-details-view.md).

L’utilisation de [!DNL Adelaide] segments pour la mesure entraîne des frais CPM pour chaque impression diffusée à partir de publicités avec des balises de mesure [!DNL Adelaide]. Ces frais sont différents des frais pour le [ciblage de niveau emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Active la mesure propriétaire et la création de rapports sur la visibilité à l’aide de la technologie [!DNL IAB Open Video Viewability (OpenVV)], en fonction du niveau de sensibilité spécifié :

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [À propos de Campaign Management](campaign-about.md)
>* [Créer une campagne](campaign-create.md)
>* [Modifier une campagne](campaign-edit.md)
>* [Afficher le journal des modifications d’une campagne](campaign-change-log.md)
