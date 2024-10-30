---
title: Vérification et modification des paramètres des composants Campaign à l’aide de feuilles d’envoi groupé
description: Découvrez comment vérifier et modifier des paramètres clés de module, d’emplacement et d’annonce en bloc à l’aide de feuilles de calcul.
feature: DSP Placements
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Vérification et modification des paramètres des composants Campaign à l’aide de feuilles d’envoi groupé

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

Vous pouvez télécharger les paramètres des packages, des emplacements et des publicités dans une seule campagne au format XLSX ([!DNL Microsoft Excel]) pour révision. Par défaut, le fichier téléchargé comprend des onglets distincts pour les paramètres du package, les informations sur le vol du package, les paramètres de placement et les plannings d’annonces d’emplacement. Vous pouvez éventuellement exclure les paramètres de certains types de composants de campagne.

Pour mettre à jour plusieurs paramètres à la fois, téléchargez un fichier de feuille d’envoi groupé valide contenant les modifications. Pour créer la feuille d’envoi groupé, vous pouvez télécharger un modèle de feuille d’envoi groupé vierge qui comprend des onglets pour chaque type de composant de campagne, saisir ou coller des paramètres nouveaux ou mis à jour dans le fichier de modèle, puis enregistrer le fichier pour le télécharger. Les champs modifiables incluent la plupart des paramètres qui sont normalement modifiables.

>[!NOTE]
>
>Vous pouvez également télécharger et modifier les paramètres pour des modules spécifiques et des emplacements spécifiques uniquement. Voir &quot;[Réviser et modifier les paramètres du module à l’aide de feuilles d’envoi groupées](/help/dsp/campaign-management/packages/package-qa.md)&quot; et &quot;[Réviser et modifier les paramètres d’emplacement à l’aide de feuilles d’envoi groupées](/help/dsp/campaign-management/placements/placement-qa.md)&quot;.

## Paramètres de téléchargement des modules, emplacements et publicités dans une campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Dans la boîte de dialogue [!UICONTROL QA Sheet Download], désélectionnez les composants de campagne dont vous souhaitez exclure les paramètres du fichier téléchargé, puis cliquez sur **[!UICONTROL Download]**.

Par défaut, les paramètres de tous les composants de campagne sont sélectionnés.

Un message de notification indique à quel moment le fichier peut être téléchargé.

1. Pour télécharger le fichier, effectuez l’une des opérations suivantes :

   * Dans le message de notification, cliquez sur **[!UICONTROL Download].**

   * À droite de la barre de menu supérieure, cliquez sur ![Tâches](/help/dsp/assets/downloads.png). Cliquez sur **[!UICONTROL Download]** en regard de la tâche.

     Le fichier est enregistré dans le dossier Téléchargements du navigateur. Voir &quot;[Colonnes de placement dans les feuilles de calcul téléchargées/téléchargées](#qa-sheet-columns)&quot; pour obtenir la liste des colonnes incluses.

>[!NOTE]
>
>Vous ne pouvez pas modifier ni recharger des fichiers d’assurance qualité au niveau de la campagne. Pour apporter des modifications aux paramètres du composant de campagne dans ces fichiers, [téléchargez un fichier de modèle de paramètres distinct (fichier de configuration)](#download-template), saisissez ou collez des lignes du fichier d’assurance qualité dans le modèle et enregistrez le fichier, puis [téléchargez le fichier de modèle renseigné](#upload-bulksheet-campaign-components).

## Téléchargement d’un modèle de feuille de support pour une Campaign {#download-template}

Téléchargez un modèle de feuille de support vierge qui comprend des onglets pour chaque type de composant de campagne. Vous pouvez ensuite ajouter des lignes à n’importe quel onglet du modèle et [télécharger le fichier](##upload-bulksheet-campaign-components) modifié pour apporter des modifications aux composants de la campagne.

1. Cliquez sur le nom de la campagne.

1. Dans l’angle supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Dans la boîte de dialogue [!UICONTROL Upload Bulksheet], cliquez sur **[!UICONTROL Bulksheet Template].**

   Le fichier est enregistré dans le dossier Téléchargements du navigateur. Voir &quot;[Colonnes de placement dans les feuilles de calcul téléchargées/téléchargées](#qa-sheet-columns)&quot; pour obtenir la liste des colonnes incluses.

## Chargement d’une feuille d’envoi groupé avec des paramètres de module, d’emplacement et d’annonce pour une campagne{#upload-bulksheet-campaign-components}

Les paramètres de téléchargement des modules, des emplacements et des publicités dans une seule campagne s’affichent tous simultanément dans une feuille d’envoi groupé remplie.

1. [Téléchargez un modèle de feuille d’envoi groupé](#download-template) si nécessaire, saisissez ou collez des paramètres de package, d’emplacement et/ou d’annonce sur les onglets appropriés d’un modèle de feuille d’envoi groupé, puis enregistrez le fichier sur votre périphérique ou réseau.

   Voir les paramètres disponibles ci-dessous.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Dans la boîte de dialogue [!UICONTROL Upload Bulksheet] :

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
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Si les tranches horaires sont *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<br><b>Remarque : </b> Pour vérifier le planning réel des tranches horaires, ouvrez les paramètres de placement dans DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Le budget de placement, s’il en existe un. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Intervalle de budget : &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | L’objectif du paquet. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | La valeur cible de l’objectif. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Indique si l’emplacement se déplace vers *[!UICONTROL Budget]* ou *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Offre maximale pour l’emplacement. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | La stratégie de fréquence des vols pour l&#39;emplacement : *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* ou *[!UICONTROL aggressive frontload]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | La stratégie de rythme intraday pour l’emplacement : *[!UICONTROL Even]* ou *[!UICONTROL ASAP]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Les critères de filtre pré-enchère à appliquer. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Si les règles d’enchère (obsolètes) sont *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Limite de fréquence principale pour le placement au cours de la période spécifiée [!UICONTROL Frequency Cap Interval] | Oui |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervalle de la limite de fréquence principale : *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | La limite de fréquence secondaire pour l’emplacement pendant le [!UICONTROL Secondary Frequency Cap Interval] spécifié | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Type d’intervalle pour la limite de fréquence secondaire : *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. Le nombre applicable de semaines, jours, heures ou minutes est indiqué par le [!UICONTROL Secondary Frequency Cap Interval Value]. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Nombre de semaines, jours, heures ou minutes pour lesquelles s’applique le [!UICONTROL Secondary Frequency Cap]. Par exemple, si la limite secondaire est de trois impressions par six heures, alors la valeur ici est `6`. | Oui |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Nombre d’emplacements géographiques ciblés, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Les emplacements géographiques ciblés, séparés par des points-virgules, ou *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Le nombre de lieux géographiques exclus ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Les emplacements géographiques exclus, séparés par des points-virgules, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Le nombre d’offres d’inventaire public ciblées, le cas échéant, sont spécifiées, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Le nombre d’offres d’inventaire public exclues, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Le nombre d’offres d’inventaire privé ciblées, le cas échéant, sont spécifiées, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Le nombre d’offres d’inventaire privé exclues, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Le nombre d&#39;offres [!UICONTROL On-Demand Inventory] ciblées, le cas échéant, sont spécifiées, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Le nombre d’offres d’inventaire à la demande exclues, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Le type de trafic ciblé : *[!UICONTROL Website]* et/ou *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Si l’option Ciblage de l’inventaire pour exclure le trafic sortant est &lt;i[!UICONTROL >ON]* ou *[!UICONTROL OFF]*.<br> Les publicités sortantes apparaissent généralement sur le contenu sous la forme d’une fenêtre contextuelle ou d’un contenu empilé (dans l’expérience native), plutôt que sous la forme de publicités vidéo standard dans un lecteur vidéo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | Qualité des sites à cibler : *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* ou *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | Le nombre de catégories de site ciblées, le cas échéant, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Le nombre de catégories de site exclues, le cas échéant, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Les sites exclus, le cas échéant, sont spécifiés ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Les langues du site ciblées. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Emplacements d’affichage standard uniquement) Autoriser ou non la diffusion des publicités sur des sites non contrôlés : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Lorsque l’emplacement cible l’inventaire privé, cette option peut diffuser des publicités sur les sites bloqués. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | Le nombre de sites ciblés, le cas échéant, est spécifié ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Les audiences ciblées, le cas échéant, sont spécifiées ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Les audiences exclues, le cas échéant, sont spécifiées ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Si [!DNL Comscore] segments démographiques sont activés ou non pour l’emplacement (et d’autres emplacements dans la campagne) : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Cette fonctionnalité peut être activée uniquement pour les campagnes pour lesquelles la fonction [!DNL Audience Verification] est activée pour [!DNL Nielsen] et/ou [!DNL Comscore].  Il entraîne des frais supplémentaires. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | S’il faut ou non étendre le ciblage publicitaire à tous les périphériques : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Le ciblage entre appareils étend votre ciblage sur l’ensemble du périphérique connu d’une personne, selon le graphique d’appareil spécifié dans les paramètres de campagne. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] -Inclus # | Le nombre de codes de rubrique ciblés, le cas échéant, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Le nombre de codes de rubrique exclus, le cas échéant, est spécifié ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | Le nombre de cibles d’appareil ciblées, le cas échéant, est spécifié ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Le nombre de cibles d’appareils exclues, le cas échéant, est spécifié, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Le nombre de fournisseurs de FAI ciblés, le cas échéant, est spécifié ou *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Le nombre de fournisseurs de FAI exclus, le cas échéant, est spécifié, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | Nombre de filtres de sécurité de marque appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | Le nombre de filtres de blocage des fraudes avant enchère appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | Le nombre de filtres d’affichage avant l’enchère appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Si le bloc de sécurité du site est activé ou non : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Nombre de pixels de suivi d’événement tiers associés à l’emplacement, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Nombre de pixels de suivi de conversion associés à l’emplacement, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Taux de frais tiers statique à suivre en tant que coût non facturable pour 1 000 impressions, le cas échéant. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Nombre de publicités associées à l’emplacement, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Les noms des publicités associées à l’emplacement, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | Les identifiants publicitaires uniques générés DSP de toutes les publicités associées à l’emplacement, séparés par des points-virgules. Pour télécharger une liste de noms de publicité et d’identifiants de publicité associés depuis la vue [!UICONTROL Ads], créez une vue personnalisée qui inclut la mesure [!UICONTROL Ad ID], puis [exportez les données](/help/dsp/campaign-management/reports/campaign-export-data.md). | Oui |

>[!MORELIKETHIS]
>
>* [Vérification et modification des paramètres du module à l’aide de feuilles d’envoi groupées](/help/dsp/campaign-management/packages/package-qa.md)
>* [Vérification et modification des paramètres d’emplacement à l’aide de feuilles d’envoi groupées](/help/dsp/campaign-management/placements/placement-qa.md)
