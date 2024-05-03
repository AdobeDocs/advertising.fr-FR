---
title: Vérification et correction des paramètres de positionnement à l’aide de feuilles de calcul
description: Découvrez comment vérifier et modifier des paramètres d’emplacement clés à l’aide de feuilles de calcul.
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: f352af0ffd5bfeab08f6592b4f3af56a9668feaa
workflow-type: tm+mt
source-wordcount: '1435'
ht-degree: 0%

---

# Vérification et correction des paramètres de positionnement à l’aide de feuilles de calcul

Vous pouvez télécharger les paramètres d’un ou de plusieurs emplacements, ou de tous les emplacements d’une campagne, au format XLSX (feuille de calcul Excel) pour révision. Utilisez cette fonctionnalité pour passer rapidement en revue les détails suivants :

* Les audiences ciblées par la campagne.
* Lorsque les emplacements commencent à être distribués et lorsqu’ils s’arrêteront.
* Les publicités associées aux emplacements.

Vous pouvez ensuite apporter des modifications à la sélection des champs et les charger à nouveau en une seule fois dans DSP. Les champs modifiables incluent les noms des emplacements, les états, les offres, les budgets, les stratégies de fréquence et les limites de fréquence.

>[!TIP]
>
>Pour apporter des modifications plus importantes aux paramètres d’emplacement, utilisez la variable [modification en masse](/help/dsp/campaign-management/placements/placement-edit.md).

## Paramètres de téléchargement pour tous les emplacements d’une campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * En regard du nom de la campagne, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   * Cliquez sur le nom de la campagne pour en afficher les détails. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   Un message de notification indique à quel moment le fichier peut être téléchargé.

1. Effectuez l’une des opérations suivantes :

   * Dans la notification, cliquez sur **[!UICONTROL Download].**

   * Dans la partie droite de la barre de menu supérieure, cliquez sur ![Tâches](/help/dsp/assets/downloads.png). Cliquez sur **[!UICONTROL Download]** à côté de la tâche.

   Le fichier est enregistré dans le dossier Téléchargements du navigateur. Voir &quot;[Colonnes dans les feuilles de calcul téléchargées/téléchargées](#qa-sheet-columns)&quot; pour une liste des colonnes incluses.

## Paramètres de téléchargement pour un ou plusieurs emplacements

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez télécharger les paramètres.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

Le fichier est automatiquement enregistré dans le dossier Téléchargement du navigateur. Voir &quot;[Colonnes dans les feuilles de calcul téléchargées/téléchargées](#qa-sheet-columns)&quot; pour une liste des colonnes incluses.

## Paramètres de téléchargement pour tous les emplacements d’une campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Effectuez l’une des opérations suivantes :

   * En regard du nom de la campagne, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

   * Cliquez sur le nom de la campagne pour en afficher les détails. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

1. Dans le [!UICONTROL Edit in Excel] dialog :

   1. Faites glisser un fichier dans la zone ou cliquez dans la zone pour sélectionner un fichier sur votre périphérique ou votre réseau.

   1. Cliquez sur **[!UICONTROL Upload]**.

1. (Facultatif) Pour vérifier que les mises à jour ont été traitées, cliquez sur ![Tâches](/help/dsp/assets/downloads.png) à droite de la barre de menu supérieure.

## Paramètres de chargement pour un ou plusieurs emplacements

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez charger les paramètres.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. Dans le [!UICONTROL Edit in Excel] dialog :

   1. Faites glisser un fichier dans la zone ou cliquez dans la zone pour sélectionner un fichier sur votre périphérique ou votre réseau.

   1. Cliquez sur **[!UICONTROL Upload]**.

1. (Facultatif) Pour vérifier que les mises à jour ont été traitées, cliquez sur ![Tâches](/help/dsp/assets/downloads.png) à droite de la barre de menu supérieure.

## Colonnes de paramètre d’emplacement dans les feuilles de calcul téléchargées/téléchargées{#qa-sheet-columns}

>[!TIP]
>
> Dans une feuille de calcul téléchargée, toutes les colonnes modifiables sont surlignées en bleu.

### Feuilles de calcul au niveau de la campagne

| Section | Colonne | Description | Modifiable ? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | Identifiant numérique de l’emplacement. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Nom de l’emplacement. | Oui |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Toutes les étiquettes appliquées, pour la création de rapports. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Lien permettant d’ouvrir l’emplacement en mode d’édition. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | État de l’emplacement : *[!UICONTROL active]* ou *[!UICONTROL inactive]*. | Oui |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Type d’emplacement. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Le nom du package parent, le cas échéant. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Date de début de l’emplacement. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Date de fin de l’emplacement. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Si les tranches horaires sont *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<br><b>Remarque :</b> Pour vérifier le planning réel des tranches horaires, ouvrez les paramètres d’emplacement dans DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Le budget de placement, s’il en existe un. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | L’intervalle de budget : &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, ou *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Oui |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | L’objectif du paquet. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | La valeur cible de l’objectif. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Indique si l’emplacement se déplace vers le *[!UICONTROL Budget]* ou *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Offre maximale pour l’emplacement. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | La stratégie de fréquence de vol de l&#39;emplacement : *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, ou *[!UICONTROL aggressive frontload]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | La stratégie de rythme intraday pour l’emplacement : *[!UICONTROL Even]* ou *[!UICONTROL ASAP]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Tout critère de filtrage de pré-enchère à appliquer. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | si les règles d’offre (obsolètes) sont *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Limite de fréquence principale de l’emplacement pendant la [!UICONTROL Frequency Cap Interval]. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervalle de la limite de fréquence principale : *[!UICONTROL Day]*, *[!UICONTROL Week]*, ou *[!UICONTROL Month]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | La limite de fréquence secondaire pour l’emplacement pendant la [!UICONTROL Secondary Frequency Cap Interval] | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Type d’intervalle pour la limite de fréquence secondaire : *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, ou *[!UICONTROL Minute]*. Le nombre applicable de semaines, jours, heures ou minutes est indiqué par la variable [!UICONTROL Secondary Frequency Cap Interval Value]. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Nombre de semaines, jours, heures ou minutes pour lesquelles la variable [!UICONTROL Secondary Frequency Cap] s’applique. Par exemple, si la limite secondaire est de trois impressions par six heures, alors la valeur ici est `6`. | Oui |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | le nombre d&#39;emplacements géographiques ciblés, *[!UICONTROL All]*, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Les emplacements géographiques ciblés, séparés par des points-virgules, ou *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Nombre d’emplacements géographiques exclus ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | les emplacements géographiques exclus, séparés par des points-virgules, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | le nombre d’offres d’inventaire public ciblées, le cas échéant, *[!UICONTROL All]*, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | le nombre d’offres d’inventaire public exclues, le cas échéant ; ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | le nombre d’offres d’inventaire privé ciblées, le cas échéant, *[!UICONTROL All]*, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | le nombre d’offres d’inventaire privé exclues, le cas échéant ; ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Le nombre de ciblages [!UICONTROL On-Demand Inventory] les offres, le cas échéant, *[!UICONTROL All]*, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | le nombre d’offres de stock à la demande exclues, le cas échéant ; ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Le type de trafic ciblé : *[!UICONTROL Website]* et/ou *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Si l’option Ciblage du stock pour exclure le trafic sortant est &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* ou *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Les publicités sortantes apparaissent généralement sur le contenu sous la forme d’une fenêtre contextuelle ou d’un contenu (dans l’expérience native), plutôt que sous la forme de publicités vidéo standard dans un lecteur vidéo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | La qualité des sites à cibler : *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, ou *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | le nombre de catégories de sites ciblées, le cas échéant ; ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | le nombre de catégories de sites exclues, le cas échéant ; ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | les sites exclus, le cas échéant, sont spécifiés, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Les langues du site ciblées. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Emplacements d’affichage standard uniquement) Autoriser ou non la diffusion des publicités sur des sites non contrôlés : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Lorsque l’emplacement cible l’inventaire privé, cette option peut diffuser des publicités sur les sites bloqués. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | le nombre de sites ciblés, le cas échéant, *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | les audiences ciblées, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | les audiences exclues, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Si ou non [!DNL Comscore] les segments démographiques sont activés pour l’emplacement (et d’autres emplacements dans la campagne) : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Cette fonctionnalité peut être activée uniquement pour les campagnes pour lesquelles la fonction [!DNL Audience Verification] La fonction est activée pour [!DNL Nielsen] et/ou [!DNL Comscore].  Il entraîne des frais supplémentaires. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Permet d’étendre ou non le ciblage des publicités sur plusieurs appareils : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Le ciblage sur plusieurs appareils étend le ciblage sur l’ensemble de l’appareil connu d’une personne, selon la représentation graphique des appareils spécifiée dans les paramètres de campagne. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Inclus # | le nombre de codes de rubrique ciblés, le cas échéant, *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | le nombre de codes de rubrique exclus, le cas échéant, *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | le nombre de cibles d’appareil ciblées, le cas échéant, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | le nombre de cibles d’appareils exclues, le cas échéant ; ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Le nombre de fournisseurs de FAI ciblés, le cas échéant, est spécifié, ou *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | le nombre de fournisseurs de FAI exclus, le cas échéant, *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | le nombre de filtres de sécurité de la marque appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | le nombre de filtres de blocage de fraude avant offre appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | le nombre de filtres de visibilité avant offre appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Si le bloc de sécurité du site est activé ou non : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | le nombre de pixels de suivi d’événements tiers associés à l’emplacement, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | le nombre de pixels de suivi de conversion associés à l’emplacement, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Taux de frais tiers statique à suivre en tant que coût non facturable pour 1 000 impressions, le cas échéant. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | le nombre de publicités associées à l’emplacement, le cas échéant ; ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | les noms de toutes les publicités associées à l’emplacement, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | Les identifiants publicitaires uniques générés DSP de toutes les publicités associées à l’emplacement, séparés par des points-virgules. Pour télécharger une liste de noms de publicité et d’identifiants de publicité associés à partir du [!UICONTROL Ads] créer une vue personnalisée qui inclut le [!UICONTROL Ad ID] mesure, puis [exporter les données](/help/dsp/campaign-management/reports/campaign-export-data.md). | Oui |

### Feuilles de calcul de niveau placement

| Colonne | Description | Modifiable ? |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | Identifiant numérique de l’emplacement. | — |
| [!UICONTROL Placement Name] | Nom de l’emplacement. | Oui |
| [!UICONTROL Package Name] | Le nom du package parent, le cas échéant. | — |
| [!UICONTROL Start Date] | Date de début de l’emplacement. | — |
| [!UICONTROL End Date] | Date de fin de l’emplacement. | — |
| [!UICONTROL Status] | État de l’emplacement : *[!UICONTROL active]* ou *[!UICONTROL inactive]*. | — |
| [!UICONTROL Max Bid] | Offre maximale pour l’emplacement. | Oui |
| [!UICONTROL Budget] | Le budget de placement, s’il en existe un. | Oui |
| [!UICONTROL Budget Interval] | L’intervalle de budget : &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, ou *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Oui |
| [!UICONTROL Primary Frequency Cap] | Limite de fréquence principale de l’emplacement pendant la [!UICONTROL Primary Frequency Cap Interval]. | Oui |
| [!UICONTROL Primary Frequency Cap Interval] | Intervalle de la limite de fréquence principale : *[!UICONTROL Day]*, *[!UICONTROL Week]*, ou *[!UICONTROL Month]*. | Oui |
| [!UICONTROL Secondary Frequency Cap] | La limite de fréquence secondaire pour l’emplacement pendant la [!UICONTROL Secondary Frequency Cap Interval] | Oui |
| [!UICONTROL Secondary Frequency Cap Interval] | Type d’intervalle pour la limite de fréquence secondaire : *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, ou *[!UICONTROL Minute]*. Le nombre applicable de semaines, jours, heures ou minutes est indiqué par la variable [!UICONTROL Secondary Frequency Cap Interval Value]. | Oui |
| [!UICONTROL Secondary Frequency Cap Interval Value] | Nombre de semaines, jours, heures ou minutes pour lesquelles la variable [!UICONTROL Secondary Frequency Cap] s’applique. Par exemple, si la limite secondaire est de trois impressions par six heures, alors la valeur ici est `6`. | Oui |
| [!UICONTROL Attached Ad ID] | Les identifiants publicitaires uniques générés DSP de toutes les publicités associées à l’emplacement, séparés par des points-virgules. Pour télécharger une liste de noms de publicité et d’identifiants de publicité associés à partir du [!UICONTROL Ads] créer une vue personnalisée qui inclut le [!UICONTROL Ad ID] mesure, puis [exporter les données](/help/dsp/campaign-management/reports/campaign-export-data.md). | Oui |

>[!MORELIKETHIS]
>
>* [Modifier un emplacement](/help/dsp/campaign-management/placements/placement-edit.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
