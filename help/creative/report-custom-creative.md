---
title: '[!UICONTROL Custom Creative Report]'
description: Découvrez comment générer le [!UICONTROL Custom Creative Report] d’expériences croisées.
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: 3033f26bba5a9e7622d0de51b36035be1005c60f
workflow-type: tm+mt
source-wordcount: '1913'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*Version bêta fermée*

Le [!UICONTROL Custom Creative Report] vous permet de personnaliser le contenu et la diffusion des données de rapport pour toutes vos expériences publicitaires.

Vous pouvez générer des rapports une fois ou les planifier de manière quotidienne, hebdomadaire ou mensuelle à 03h00 dans le fuseau horaire spécifié, selon des critères précis (par exemple, tous les 15 jours ou le 1er de chaque mois). Une fois qu’un rapport est généré, vous pouvez le télécharger à partir de [!UICONTROL Reports] > [!UICONTROL Custom Reports] ou à partir de [destinations de rapport](/help/dsp/reports/report-destinations/report-destination-about.md) liées des types suivants :

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* <!-- (in beta) --> SSL FTP
* SFTP

## Création d’un [!UICONTROL Custom Creative Report]

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]**.

1. Spécifiez les [paramètres du rapport](#report-settings).

1. Cliquez sur **[!UICONTROL Create Custom Report]**.

## Paramètres des rapports {#report-settings}

**[!UICONTROL Name]:** nom du rapport. La longueur maximale est de 180 caractères.

**[!UICONTROL Report Type]:** Type de rapport : *[!UICONTROL Custom Creative Beta]*.

### Section [!UICONTROL Report Range]

Cette section détermine les données incluses dans le rapport. Pour configurer des dates pour le planning du rapport, reportez-vous à la section « [!UICONTROL Report run schedule] ».

**[!UICONTROL Timezone]:** fuseau horaire pour la création de rapports.

**[!UICONTROL Observe Daylight Savings Time]:** prend en compte l’heure d’été dans les heures indiquées.

**Période :** période pour laquelle générer des données. Le nombre de jours disponibles varie en fonction du rapport et des dimensions sélectionnées. Choisir un :

* **[!UICONTROL Previous Calendar Week]:** inclut les données de la semaine civile précédente.

* **[!UICONTROL Previous Calendar Month]:** inclut les données du mois calendaire précédent.

* **[!UICONTROL Custom Range]:** inclut les données comprises entre des dates de début et de fin spécifiques. Pour rapporter les données jusqu’au jour précédent, sélectionnez **[!UICONTROL Present]**.

### Section [!UICONTROL Report Run schedule]

Cette section détermine les dates d&#39;exécution du rapport. Pour configurer les dates auxquelles inclure des données de rapport, reportez-vous à la section « [!UICONTROL Report range] ».

**\[Planification\]:** Quand générer le rapport :

* *[!UICONTROL Immediately]* : ajoute immédiatement le rapport à la file d’attente des rapports.

  >[!NOTE]
  >
  >Vous pouvez également [exécuter un rapport personnalisé à tout moment](/help/dsp/reports/report-run-now.md) à partir de la vue [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\>:* exécute le rapport à une date spécifiée pour s’achever à 9 h dans le fuseau horaire du compte.

* *[!UICONTROL Recurring]:* exécute le rapport selon un planning défini au cours d’une période donnée.

   * **\[Planification\]:** Fréquence d’exécution du rapport :

      * *Quotidien* pour exécuter le rapport tous les N jours. Par exemple, pour exécuter le rapport toutes les deux semaines (14 jours), sélectionnez cette option et saisissez **14**.

      * *Hebdomadaire* pour exécuter le rapport à des jours spécifiés de la semaine. Par exemple, pour exécuter le rapport tous les lundis et vendredis, sélectionnez cette option et cochez les cases en regard de **lundi** et **vendredi**.

      * *Mensuel* pour exécuter le rapport un jour numérique spécifique du mois, compris entre 1 et 30. Par exemple, pour exécuter le rapport le premier jour de chaque mois, sélectionnez cette option et saisissez **1**.

   * **De** : première date à laquelle le rapport peut être exécuté. Selon le planning spécifié, la première instance de rapport peut se produire après cette date.

   * **Jusqu’au** : date d’expiration du rapport, qui peut prendre jusqu’à quatre mois civils. Avant l’expiration d’un rapport, toutes les destinations d’e-mail spécifiées reçoivent une alerte par e-mail sept jours et un jour avant la date d’expiration. Pour conserver le rapport plus longtemps, modifiez cette date.

### Section [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (facultatif) Dimensions supplémentaires selon lesquelles filtrer les données, que les dimensions soient incluses ou non en tant que colonnes dans le rapport. Les filtres disponibles varient selon le type de rapport et peuvent inclure : *[!UICONTROL Advertiser]*, *[!UICONTROL Experience]*, *[!UICONTROL Creative Library]* et *[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->.

Pour appliquer un ou plusieurs filtres, procédez comme suit :

* Sélectionnez une dimension, puis l’opérateur (*égal à* ou *différent de*), puis sélectionnez la valeur applicable. Par exemple, pour renvoyer des données pour les annonces publicitaires de pré-classement uniquement, spécifiez « [!UICONTROL Ad Type equals Preroll] ».
* (Facultatif) Ajoutez des critères supplémentaires au filtre.
* (Facultatif) Ajoutez des filtres supplémentaires, chacun avec un ou plusieurs critères.

### Section [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** les colonnes de données, ou en-têtes, à inclure dans le rapport. Pour ajouter une colonne, développez la catégorie et cochez la case en regard du nom de la colonne. Les colonnes disponibles varient selon le rapport et toutes les mesures indisponibles sont désactivées. Voir « [Colonnes de rapport disponibles](#report-custom-creative-columns) » pour obtenir une description de toutes les options.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** ordre des en-têtes de colonne. Vous pouvez faire glisser et déposer n’importe quelle colonne pour personnaliser l’ordre.

**[!UICONTROL Format]:** Génération d’un rapport au format *[!UICONTROL CSV]* (valeurs séparées par des virgules) ou *[!UICONTROL Tab]* (valeurs séparées par des tabulations).

**[!UICONTROL Headers]:** s’il faut *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]* les en-têtes de colonne.

### Section [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Les paramètres varient selon le type de rapport :

* **\[Type d’attribution\]:** (annonceurs avec suivi des conversions Adobe Advertising uniquement) Dans le rapport, comment attribuer les données de conversion dans une série d’événements qui entraînent une conversion :

   * *[!UICONTROL Unique]:* (valeur par défaut) compte le nombre de fois qu’une valeur de dimension (un appareil ou un emplacement, par exemple) a été sur le chemin d’accès à la conversion.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* distribue le crédit de chaque conversion en fonction de la fréquence d’occurrence de la valeur de dimension (telle qu’un appareil ou un emplacement) sur le chemin d’accès à la conversion. Par exemple, s’il y avait un total de 10 impressions avant la conversion, avec 8 sur CTV et 2 sur Mobile, alors 80 % du crédit (0,8) est attribué aux écrans de CTV et 0,2 à Mobile.

* **\[Type de règle\]:** (annonceurs avec suivi des conversions Adobe Advertising uniquement) Dans le rapport, comment attribuer les données de conversion dans une série d’événements qui conduisent à une conversion. Vous pouvez choisir plusieurs règles pour comparer les différences entre elles.

  >[!NOTE]
  >
  >Les chemins de conversion incluent les impressions et les clics dans les intervalles d’impression ou de recherche en amont des clics de l’annonceur, qui sont configurés dans [!DNL Advertising Search, Social, & Commerce]. Les clics sont prioritaires sur les impressions lors de l’attribution de la conversion. Tous les clics effectués dans un chemin de conversion sont crédités intégralement en fonction de la règle d’attribution. Les impressions reçoivent du crédit uniquement lorsque aucun clic n’est suivi dans le chemin de conversion.

   * *[!UICONTROL Last Event]:* attribue des conversions au dernier clic ou à la dernière impression dans le chemin de conversion.

   * *[!UICONTROL Weight Last More]:* Attribue des conversions à tous les événements du chemin de conversion, mais donne le plus de poids au dernier événement et successivement moins de poids aux événements précédents.

   * *[!UICONTROL Even Distribution]:* Attribue les conversions de manière égale à chaque événement dans le chemin de conversion.

   * *[!UICONTROL Weight First More]:* Attribue des conversions à tous les événements du chemin de conversion, mais donne le plus de poids au premier événement et successivement moins de poids aux événements suivants.

   * *[!UICONTROL First Event]:* attribue des conversions au premier clic ou à la première impression dans le chemin de conversion.

   * *[!UICONTROL U-shaped]:* Attribue la conversion à tous les événements du chemin de conversion, mais donne le plus de poids au premier et au dernier événements, avec successivement moins de poids aux événements au milieu du chemin de conversion.

   * *[!UICONTROL Display Only]:* Attribue les conversions au dernier clic ou à la dernière impression DSP dans le chemin de conversion. Cela inclut les publicités vidéo et TV connectées, et exclut les clics sur les publicités [!DNL Advertising Search, Social, & Commerce].

   * *[!UICONTROL Social Only]:* Obsolète

[ Consultez également la section « Comment les règles d’attribution sont-elles calculées pour Adobe Advertising ](/help/search-social-commerce/reports/attribution-rules.md) ? »

**[!UICONTROL Paths as Columns]:** types de conversions à signaler lorsque des événements précédents se sont produits sur le même appareil. Vous pouvez inclure jusqu’à trois types. Pour chaque type sélectionné, une colonne distincte est incluse pour chaque mesure de conversion et est ajoutée avec le suffixe spécifié ([!UICONTROL (tl)], [!UICONTROL (ct)] ou [!UICONTROL (vt)]) :

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* inclut les conversions attribuées aux clics (CT pour les clics publicitaires) et aux impressions (VT pour les vues publicitaires). Les conversions attribuées aux impressions sont multipliées par le poids de visionnage publicitaire spécifié. Le poids d’affichage publicitaire par défaut est de 100 %, ce qui signifie que les conversions attribuées aux impressions sont comptabilisées comme 100 % de la valeur des conversions attribuées aux clics.

* *[!UICONTROL With Clicks (CT)]:* inclut uniquement les conversions attribuées aux clics.

* *[!UICONTROL Impressions Only (VT)]:* inclut uniquement les conversions attribuées aux impressions, car aucun clic n’a été suivi dans le chemin de conversion.

### Section [!UICONTROL Add Report Destinations]

**[!UICONTROL Destination Type]:** Où diffuser les rapports terminés et les notifications d’erreur. Vous ne pouvez pas modifier le type de destination une fois que vous avez enregistré le rapport.

>[!NOTE]
>
>Vous pouvez toujours télécharger les rapports terminés à partir de la vue [!UICONTROL Reports] > [!UICONTROL Custom Reports] .

* *[!UICONTROL None]:* pour ne pas diffuser de rapports ou de notifications.

* *[!UICONTROL S3]:* pour envoyer le rapport terminé à un ou plusieurs emplacements [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), que vous devez sélectionner dans le champ **[!UICONTROL Destination Name]**.

* *[!UICONTROL sFTP]:* pour envoyer le rapport terminé à un ou plusieurs emplacements SFTP, que vous devez sélectionner dans le champ **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP]:* pour envoyer le rapport terminé à un ou plusieurs emplacements FTP, que vous devez sélectionner dans le champ **[!UICONTROL Destination Name]**.

* *[!UICONTROL FTP SSL](actuellement dans Beta) :* pour envoyer le rapport terminé à un ou plusieurs emplacements FTP SSL, que vous devez sélectionner dans le champ **[!UICONTROL Destination Name]** .

* *[!UICONTROL Email]:* pour spécifier la ou les adresses e-mail auxquelles envoyer les rapports terminés ou les notifications si le rapport est annulé en raison d’erreurs.

**[!UICONTROL Email]:** (type de destination d’e-mail uniquement) Pour chaque adresse, saisissez l’adresse et cliquez sur **+**.

**[!UICONTROL Destination Name]:** (types de destination S3, FTP, sFTP et FTP SSL uniquement) Noms des [destinations de rapport](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} auxquelles le rapport personnalisé est envoyé.

* Pour spécifier une destination existante, sélectionnez un nom de destination dans la liste. Vous pouvez sélectionner plusieurs noms de destination séparément.

* Pour créer une destination :

   1. Cliquez sur **Ajouter une nouvelle destination**.

   1. Saisissez le [paramètres de destination du rapport](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"}, puis cliquez sur **Enregistrer**.

   1. De retour dans les paramètres du rapport, cliquez sur **Actualiser les noms de destination.**

      La nouvelle destination est désormais disponible dans la liste des destinations existantes et vous pouvez éventuellement l’ajouter au rapport.

## Colonnes de rapport disponibles {#report-custom-creative-columns}

<!-- Need to finish these definitions -->

| Type de mesure | Sous-type | Nom de la colonne | Description |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | Dimensions de l’annonce publicitaire publiée. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | Indique si la publicité diffusée était une publicité sous forme d’image par défaut pour l’expérience. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | Indique si les publicités ont fait l’objet d’une rotation en fonction des poids relatifs (*pondérés*) ou algorithmique (*algorithmiques*). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | Identifiant attribué [!UICONTROL Creative] créatif. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | Nom du contenu créatif. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | Type de contenu créatif (par exemple, [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | Identifiant attribué [!UICONTROL Creative] l’élément créatif parent. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | Nom du contenu créatif parent. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | Type de contenu créatif parent (par exemple, [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | . |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | Type de clic. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | Navigateur dans lequel la publicité a été affichée ([!UICONTROL Chrome] ou [!UICONTROL Firefox], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | Système d’exploitation sur lequel la publicité a été affichée ([!UICONTROL Windows], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | Type d’appareil sur lequel la publicité a été affichée ([!UICONTROL Desktop], par exemple). |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Ad ID] | Identifiant de l’annonce publicitaire. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Buy ID] | L’identifiant d’achat pour l’emplacement publicitaire. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Creative ID] | Identifiant du contenu créatif. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP ID] | Identifiant du DSP sur lequel les publicités ont été exécutées. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | Nom du DSP sur lequel les publicités ont été exécutées. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | Identifiant de l’emplacement pour lequel les publicités ont été exécutées. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | Nom de l’emplacement pour lequel les publicités ont été exécutées. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | L’identifiant du site sur lequel les publicités ont été exécutées. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | Nom du site sur lequel les publicités ont été exécutées. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | Identifiant attribué [!UICONTROL Creative] la balise d’expérience publicitaire. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | Nom de l’annonceur. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | Date et heure de l’événement. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | Identifiant attribué [!UICONTROL Creative] l’expérience. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | Nom de l’expérience. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | La cible. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | Ville à laquelle les données déclarées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | Code pays du pays auquel les données déclarées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | Zone de marché désignée (DMA) à laquelle les données déclarées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | Code d’état de l’état auquel les données signalées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | Code postal auquel sont attribuées les données signalées. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | (Annonces dynamiques) Identifiant de la catégorie de produits cible. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | (Annonces dynamiques) Nom de la catégorie de produits cible. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | (Annonces dynamiques) Premier attribut créatif. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | (Annonces dynamiques) Le deuxième attribut créatif. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | (Annonces dynamiques) Troisième attribut créatif. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | (Annonces dynamiques) Quatrième attribut créatif. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | (Annonces dynamiques) Le cinquième attribut créatif. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | (Annonces dynamiques) Identifiant du produit cible. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | (Annonces dynamiques) Nom du produit cible. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | Identifiant du segment d’audience auquel les données rapportées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | Identifiant de segment pour un segment d’audience auquel les données signalées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | Nom d’un segment d’audience auquel les données signalées sont attribuées. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | Attributs d’un segment d’audience auquel les données rapportées sont attribuées. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | Somme de tous les clics sur une annonce publicitaire. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | Taux de clics publicitaires, qui correspond au pourcentage de clics divisé par les impressions de publicité. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | Pourcentage d’impressions diffusées qui ont donné lieu à des interactions avec les utilisateurs. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | Nombre d’interactions sur une publicité diffusée. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | Nombre total d’impressions de publicité. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | Somme de tous les clics sur les annonces publicitaires d’un produit. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | Somme de toutes les conversions sur les annonces publicitaires d’un produit. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | Pourcentage d’annonces pour un produit qui ont entraîné des conversions. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | Taux de clic publicitaire pour des annonces publicitaires pour un produit, qui correspond au pourcentage de clics divisé par les impressions d’annonces publicitaires. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | Nombre total d’impressions pour un produit. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | Chiffre d’affaires total des publicités diffusées pour un produit. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | Chiffre d’affaires total des publicités diffusées. |
| [!UICONTROL Conversion Metrics] | [Regroupé par annonceur dans les paramètres du rapport] | [ Conversion spécifique à l’annonceur ] | Total d’une mesure de conversion spécifique à l’annonceur ou d’un événement Adobe Analytics spécifié. |
| [!UICONTROL Custom Goals] | [Regroupé par annonceur dans les paramètres du rapport] | [Objectif personnalisé spécifique à l’annonceur] | (Annonceurs avec Advertising DSP) Somme pondérée de toutes les conversions incluses dans l’objectif personnalisé [Advertising DSP spécifié](/help/dsp/optimization/custom-goal.md). |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [ Rapports de performances au niveau de l’expérience ](/help/creative/experiences/experience-performance-details.md)
>* [À propos des rapports personnalisés DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [À propos des [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
