---
title: Gestion des rapports personnalisés
description: Découvrez comment générer et gérer le [!UICONTROL Custom Creative Report] d’expériences croisées.
feature: Creative Reporting
source-git-commit: 455a63be51ca56610cc15ba498e69eeae52ffdba
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]

Vous pouvez créer, dupliquer, modifier, exécuter, télécharger et supprimer des rapports personnalisés.

## Création d’un rapport personnalisé {#report-create}

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]**.

1. Spécifiez les [paramètres du rapport](#report-settings).

1. Cliquez sur **[!UICONTROL Create Custom Report]**.

## Duplication d’un rapport personnalisé

Dupliquez un rapport personnalisé pour créer un rapport avec des paramètres similaires.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. En regard du nom du rapport, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Copy]**.

1. (Facultatif) Modifiez les [paramètres du rapport](#report-settings.md) selon les besoins.

   Par défaut, le nom du rapport est « &lt;*nom du rapport existant*\> \#2 » (ou le numéro suivant dans la séquence).

## Modification d’un rapport personnalisé {#report-edit}

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. En regard du nom du rapport, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Modifiez le [paramètres du rapport](#report-settings.md).

1. Cliquez sur **[!UICONTROL Edit Custom Report]**.

## Exécution d’un rapport personnalisé &lbrace;report-run-now&rbrace;

Vous pouvez exécuter n’importe quel rapport qui n’a pas expiré et qui n’est pas en cours d’exécution.

>[!NOTE]
>
>Vous pouvez également exécuter un rapport personnalisé lorsque vous le [créez](#report-create) ou [modifiez](#report-edit).

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. En regard du nom du rapport, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Run Now]**.

   Une fois le rapport terminé, il est envoyé aux destinations spécifiées dans les paramètres du rapport.

## Téléchargement d’un rapport personnalisé

Vous pouvez télécharger n’importe quelle instance de rapport terminée des quatre derniers mois, dont le statut est « [!UICONTROL Ready to Download] » ou « [!UICONTROL Completed] ».

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Dans la colonne [!UICONTROL Download Report] de la ligne de rapport, procédez comme suit :

   * Pour télécharger la dernière instance du rapport, cliquez sur **[!UICONTROL Download]**.

   * (Rapports comportant plusieurs instances) Cliquez sur ![la flèche vers le bas](/help/dsp/assets/chevron-down.png "la flèche vers le bas") en regard de [!UICONTROL Download], puis cliquez sur la date d’achèvement du rapport à télécharger. Les instances de rapport téléchargeables sont indiquées par une icône de téléchargement (![icône de téléchargement](/help/dsp/assets/indicator-downloadable.png "icône de téléchargement")).

     Lorsque de nombreuses instances sont disponibles, cliquez sur **[!UICONTROL Load More]** au bas de la liste, si nécessaire.

     Lorsqu’un rapport s’exécute plusieurs fois le même jour, les instances de rapport de ce jour sont répertoriées dans l’ordre chronologique, l’instance la plus récente étant en haut.

     Les tâches de rapport ayant échoué sont indiquées par une icône d’erreur (![&#x200B; indicateur d’erreur](/help/dsp/assets/indicator-critical.png "indicateur d’erreur")) et ne peuvent pas être téléchargées. Pour obtenir une description de l’erreur, placez le curseur sur l’icône d’erreur.

## Suppression d’un rapport personnalisé

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. En regard du nom du rapport, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Paramètres des rapports {#report-settings}

**[!UICONTROL Name]:** nom du rapport. La longueur maximale est de 180 caractères.

**[!UICONTROL Report Type]:** type de rapport.

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
  >Vous pouvez également [exécuter un rapport personnalisé à tout moment](#report-run-now) à partir de la vue [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\> :* exécute le rapport à une date spécifiée pour s’achever à 09:00 dans le fuseau horaire du compte.

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

**[!UICONTROL Select To Add As Report Headers]:** les colonnes de données, ou en-têtes, à inclure dans le rapport. Pour ajouter une colonne, développez la catégorie et cochez la case en regard du nom de la colonne. Les colonnes disponibles varient selon le rapport et toutes les mesures indisponibles sont désactivées.<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** ordre des en-têtes de colonne. Vous pouvez faire glisser et déposer n’importe quelle colonne pour personnaliser l’ordre.

**[!UICONTROL Format]:** Génération d’un rapport au format *[!UICONTROL CSV]* (valeurs séparées par des virgules) ou *[!UICONTROL Tab]* (valeurs séparées par des tabulations).

**[!UICONTROL Headers]:** s’il faut *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]* les en-têtes de colonne.

### Section [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Les paramètres varient selon le type de rapport :

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

[&#x200B; Consultez également la section « Comment les règles d’attribution sont-elles calculées pour Adobe Advertising &#x200B;](/help/search-social-commerce/reports/attribution-rules.md) ? »

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

* *[!UICONTROL FTP SSL] (actuellement dans Beta) :* pour envoyer le rapport terminé à un ou plusieurs emplacements FTP SSL, que vous devez sélectionner dans le champ **[!UICONTROL Destination Name]** .

* *[!UICONTROL Email]:* pour spécifier la ou les adresses e-mail auxquelles envoyer les rapports terminés ou les notifications si le rapport est annulé en raison d’erreurs.

**[!UICONTROL Email]:** (type de destination d’e-mail uniquement) Pour chaque adresse, saisissez l’adresse et cliquez sur **+**.

**[!UICONTROL Destination Name]:** (types de destination S3, FTP, sFTP et FTP SSL uniquement) Noms des [destinations de rapport](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} auxquelles le rapport personnalisé est envoyé.

* Pour spécifier une destination existante, sélectionnez un nom de destination dans la liste. Vous pouvez sélectionner plusieurs noms de destination séparément.

* Pour créer une destination :

   1. Cliquez sur **Ajouter une nouvelle destination**.

   1. Saisissez le [paramètres de destination du rapport](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"}, puis cliquez sur **Enregistrer**.

   1. De retour dans les paramètres du rapport, cliquez sur **Actualiser les noms de destination.**

      La nouvelle destination est désormais disponible dans la liste des destinations existantes et vous pouvez éventuellement l’ajouter au rapport.


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [&#x200B; Rapports de performances au niveau de l’expérience &#x200B;](/help/creative/experiences/experience-performance-details.md)
>* [À propos des rapports personnalisés DSP](/help/dsp/reports/report-about.md){target="_blank"}
>* [À propos des [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
