---
title: Paramètres de campagne
description: Reportez-vous à la description des paramètres de campagne disponibles.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Paramètres de campagne

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Nom de la campagne.

**[!UICONTROL Advertiser]:** (Lecture seule pour les campagnes existantes) Annonceur (marque) applicable. Sélectionnez un annonceur existant ou créez-en un.

**[!UICONTROL Advertiser URL]:** Page officielle de l’annonceur. Ce champ accélère le processus d’approbation des publicités avec les partenaires d’inventaire.

**[!UICONTROL Timezone]:** (Lecture seule pour les campagnes existantes) Fuseau horaire pour la création de rapports et l’offre.

**[!UICONTROL Customer PO]:** (Facultatif) Commande d’achat d’un client pour la commande d’insertion/la commande d’achat.

**[Dates de campagne]:** Les dates de début et de fin de la campagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Permet de gérer les marges de la campagne : *[!UICONTROL Yes]* ou *[!UICONTROL No]* (valeur par défaut).

Lorsque vous choisissez *[!UICONTROL Yes],* indiquez le type de marge et le montant :

* **[!UICONTROL Margin Type]:** Type de marge. Vous ne pouvez pas modifier le type de marge une fois que vous avez activé la gestion des marges et enregistré l&#39;opération.

   * *[!UICONTROL Fixed]:* (valeur par défaut) Permet DSP calculer et plafonner automatiquement les dépenses en fonction d’un pourcentage de marge fixe de la variable [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Permet de gérer les marges jusqu’au niveau de l’emplacement en spécifiant un [!UICONTROL Budget Reserve %] et [!UICONTROL Gross Budget] pour chaque kit et emplacement de l&#39;opération. DSP optimise en fonction de l&#39;efficacité financière de chaque placement, sans garantir une marge spécifique. Utilisez cette option pour les commandes d’insertion composées de plusieurs éléments de ligne pour lesquels vous avez accepté de fournir un nombre fixe d’unités ou de types d’unités à un rythme fixe.

* **[!UICONTROL Fixed Margin %]:** (Campagnes avec des marges fixes uniquement) Balises par défaut pour chaque ordre d’insertion. <!-- impression? -->, en pourcentage. Ce montant est déduit du montant [!UICONTROL Gross Budget] pour définir le budget net de l&#39;opération.

* **[!UICONTROL Budget Reserve %]:** (Campagnes avec des marges fixes uniquement ; facultatif) réserve un pourcentage spécifié de la variable [!UICONTROL Gross Budget] comme une protection. Ce montant est déduit du montant [!UICONTROL Gross Budget] pour définir le budget net de l&#39;opération.

**[!UICONTROL Gross Budget]:** (Campagnes avec gestion des marges uniquement) Le budget brut de l’opération, avant l’application des ajustements marginaux spécifiés.

Vous pouvez éventuellement ajouter un budget brut quotidien, hebdomadaire ou mensuel supplémentaire :

1. Cliquez sur **[!UICONTROL Add an additional Gross Budget]**.

1. Saisissez le **[!UICONTROL Gross Budget]** et sélectionnez l’intervalle de budget : *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly]*.

Le budget net total, qui correspond au plafond de dépenses de l&#39;opération, est calculé automatiquement sur la base des paramètres de marge et est renseigné sous cette valeur.

**[!UICONTROL Budget]:** (Campagnes sans gestion des marges) Le budget global de l’opération.

**[!UICONTROL Estimated Tax Withholding]:** Retient un pourcentage du total des dépenses par rapport aux frais publicitaires, aux frais de service publicitaire et/ou aux frais de données au niveau du compte pour les impôts locaux ou nationaux. Les taux sont des estimations à des fins de budget et de calendrier, de sorte que les taux d’imposition facturés peuvent varier.

Pour estimer les impôts à retenir :

1. Cliquez sur **[!UICONTROL Update rates here]**.

1. Spécifiez la variable **[!UICONTROL Estimated tax rate]**, en pourcentage.

1. Cochez la case en regard de chaque type de taxe pour lequel vous souhaitez retenir des impôts. Les types de frais incluent :

   * *[!UICONTROL Include estimated tax - ads fee]:* S’applique à toutes les dépenses publicitaires DSP médias, y compris les taxes sur les frais de gestion de campagne.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* S’applique à toutes les dépenses dans les DSP publicitaires, à l’exception des médias et des données. Elle exclut les taxes pour les frais de gestion de campagne

   * *[!UICONTROL Include estimated tax - data fee]:* S’applique à toutes les données dépensées dans les DSP Advertising.

1. Cliquez sur **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Aux États-Unis, les États peuvent varier dans leur inclusion des taxes entre les publicités, les publicités et les données. Pour les organisations d’autres pays, incluez les trois catégories de taxes pour tenir compte de la TVA.
>
>* Vous pouvez également configurer ces valeurs dans les paramètres de frais du compte.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Lecture seule pour les campagnes existantes créées depuis le 22 juin 2020 ; non disponible pour les campagnes créées avant le 22 juin 2020) Niveau auquel DSP cible les publicités et applique des limites de fréquence : *Même appareil* pour cibler un appareil ou *Personnes* pour cibler une personne sur tous ses appareils connus. **Remarque :** La prise en charge inter-appareils n’est pas disponible pour les emplacements qui ciblent les identifiants universels.

**[!UICONTROL Device Graph]:** (Lecture seule pour les campagnes existantes ; campagnes avec ciblage interpériphérique basé sur les personnes uniquement) Graphique d’appareil à utiliser pour le ciblage interpériphérique et la gestion des fréquences :

* *[!UICONTROL LiveRamp - U.S. only]:* Disponible pour tous les annonceurs pour un ciblage multi-appareils à 0,35 CPM pour les impressions diffusées à l’aide de la variable [!DNL LiveRamp] Device Graph (c’est-à-dire, pour les appareils introuvables dans les segments d’audience ciblés). Vous pouvez configurer le ciblage sur plusieurs appareils au niveau de l’emplacement.

  Cette option est également disponible pour tous les annonceurs, sans frais, pour la gestion des fréquences et la mesure d’attribution.

  La prise en charge inter-appareils s’applique uniquement aux emplacements qui ciblent des ID hérités, mais pas aux emplacements qui ciblent des ID universels (y compris [!DNL LiveRamps]). Le ciblage, la gestion des fréquences et l’attribution pour les identifiants universels sont appliqués au niveau des identifiants uniquement.

**[!UICONTROL Frequency Cap]:** (Facultatif) Le nombre de fois où un appareil, un identifiant universel ou une personne unique (en fonction de la variable [!UICONTROL Cross Device Level] et de l’emplacement [!UICONTROL Targeting] ) peuvent être diffusées à partir de la campagne. Les options incluent *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
> Vous pouvez définir des limites de fréquence aux niveaux de la campagne, du kit et de l’emplacement. DSP respecte la limite de fréquence la plus stricte de la hiérarchie de l&#39;opération.

**[!UICONTROL Packages]:** La variable [packages](/help/dsp/campaign-management/packages/package-about.md) à inclure dans la campagne. Sélectionnez les packages existants et/ou créez des packages à inclure. Si vous créez des modules, reportez-vous à la description de la variable [paramètres du package](/help/dsp/campaign-management/packages/package-settings.md) pour plus d’informations.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Les paramètres suivants activent uniquement les fonctionnalités de mesure et de création de rapports. L’optimisation des performances est exécutée uniquement au niveau du package et de l’emplacement.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Facultatif) Active [!DNL IAS] mesure et création de rapports sur la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience, à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Measure On]:** Inventaire sur lequel mesurer : *[!UICONTROL Display and VPAID video inventory]* (valeur par défaut) ou *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >La visibilité des vidéos est mesurable sur l’inventaire VPAID uniquement.

* **[!UICONTROL IAS Account ID (AnID)]:** (Publicitaires avec leurs propres [!DNL IAS] Comptes ; facultatif) L’organisation [!DNL IAS] ID de compte, qui [!DNL IAS] facturera directement pour l’utilisation.

* **[!UICONTROL IAS Team ID]:** (Publicitaires avec leurs propres [!DNL IAS] Comptes ; facultatif) ID d’équipe pour l’organisation [!DNL IAS] , qui [!DNL IAS] facturera directement pour l’utilisation. <!-- verify -->

**[!UICONTROL MOAT]:** (Facultatif) Active [!DNL MOAT] mesure et reporting de la visibilité, de la fraude, de la sécurité de la marque et de la vérification de l’audience. Des frais supplémentaires s’appliquent.

#### Vérification de l’audience

**[!UICONTROL Comscore Campaign Ratings]:** (Facultatif) Active [!DNL Comscore] validé [!DNL Campaign Ratings] mesure et création de rapports sur la vérification des audiences, à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Target Gender]:** Le genre à cibler : *[!UICONTROL Both]* (valeur par défaut), *[!UICONTROL Male]*, ou *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Période à cibler. Utilisez les curseur gauche et droit pour réduire la plage selon vos besoins.

* **[!UICONTROL Target Country]:** (Facultatif) Un pays à cibler. [!DNL Comscore] mesure les impressions diffusées dans les pays pris en charge uniquement.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Active le suivi au niveau de l’emplacement [!UICONTROL Attention Score] mesure (le nombre moyen pondéré [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; sur toutes les impressions). Les mesures sont disponibles pour tous les types d’emplacements, à l’exception de [!DNL Roku] Une télévision connectée, un preroll VPAID et un son qui n&#39;est pas un podcast. DSP associe automatiquement une balise JavaScript à tous les créatifs associés, et [!DNL Adelaide] effectue le suivi des données d’exposition et les envoie DSP tous les jours. Vous pouvez utiliser la date pour optimiser manuellement vos dépenses en faveur des tactiques de placement avec de meilleurs scores d’attention.

La variable [!UICONTROL Attention Score] est disponible dans le champ [!UICONTROL Metrics] de la section [!UICONTROL Campaigns], [!UICONTROL Packages], et [!UICONTROL Placements] et sur la [!UICONTROL Sites], [!UICONTROL Ads], et [!UICONTROL Inventory] des onglets [affichage des détails de placement](/help/dsp/campaign-management/reports/placement-details-view.md).

Utilisation [!DNL Adelaide] les segments pour la mesure engendrent des frais CPM pour chaque impression diffusée à partir de publicités avec [!DNL Adelaide] balises de mesure. Ces frais sont différents des frais pour [ciblage de l’attention au niveau de l’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Permet la mesure propriétaire et la création de rapports sur la visibilité à l’aide de la variable [!DNL IAB Open Video Viewability (OpenVV)] technologie, en fonction du niveau de sensibilité spécifié :

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [À propos de Campaign Management](campaign-about.md)
>* [Création d’une campagne](campaign-create.md)
>* [Modifier une campagne](campaign-edit.md)
>* [Affichage du journal des modifications d’une campagne](campaign-change-log.md)
