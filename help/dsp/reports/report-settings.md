---
title: Paramètres des rapports personnalisés
description: Voir les descriptions des paramètres des rapports personnalisés.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '1541'
ht-degree: 0%

---

# Paramètres des rapports personnalisés

**[!UICONTROL Name]:** nom du rapport. La longueur maximale est de 180 caractères.

**[!UICONTROL Report Type]:** type de rapport : *[!UICONTROL Custom]* (qui inclut la plupart des options disponibles), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, *[!UICONTROL Household Conversions]*, *[!UICONTROL Path to Conversions Beta]*, *[!UICONTROL Path Length Beta]*, *[!UICONTROL Time to Conversion Beta]*, ou.

## Section [!UICONTROL Report Range]

Cette section détermine les données incluses dans le rapport. Pour configurer des dates pour le planning du rapport, reportez-vous à la section « [!UICONTROL Report run schedule] ».

**[!UICONTROL Timezone]:** fuseau horaire pour la création de rapports.

**[!UICONTROL Observe Daylight Savings Time]:** prend en compte l’heure d’été dans les heures indiquées.

**Période :** période pour laquelle générer des données. Le nombre de jours disponibles varie en fonction du rapport et des dimensions sélectionnées. Choisir un :

* **[!UICONTROL Previous Calendar Week]:** inclut les données de la semaine civile précédente.

* **[!UICONTROL Previous Calendar Month]:** inclut les données du mois calendaire précédent.

* **[!UICONTROL Custom Range]:** inclut les données comprises entre des dates de début et de fin spécifiques. Pour rapporter les données jusqu’au jour précédent, sélectionnez **[!UICONTROL Present]**.

## Section [!UICONTROL Report Run schedule]

Cette section détermine les dates d&#39;exécution du rapport. Pour configurer les dates auxquelles inclure des données de rapport, reportez-vous à la section « [!UICONTROL Report range] ».

**\[Planification\]:** Quand générer le rapport :

* *[!UICONTROL Immediately]* : ajoute immédiatement le rapport à la file d’attente des rapports.

  >[!NOTE]
  >
  >Vous pouvez également [exécuter un rapport personnalisé à tout moment](report-run-now.md) à partir de la vue [!UICONTROL Reports].

* *[!UICONTROL On]\&lt;Date\>:* exécute le rapport à une date spécifiée pour s’achever à 9 h dans le fuseau horaire du compte.

* *[!UICONTROL Recurring]:* exécute le rapport selon un planning défini au cours d’une période donnée.

   * **\[Planification\]:** Fréquence d’exécution du rapport :

      * *Quotidien* pour exécuter le rapport tous les N jours. Par exemple, pour exécuter le rapport toutes les deux semaines (14 jours), sélectionnez cette option et saisissez **14**.

      * *Hebdomadaire* pour exécuter le rapport à des jours spécifiés de la semaine. Par exemple, pour exécuter le rapport tous les lundis et vendredis, sélectionnez cette option et cochez les cases en regard de **lundi** et **vendredi**.

      * *Mensuel* pour exécuter le rapport un jour numérique spécifique du mois, compris entre 1 et 30. Par exemple, pour exécuter le rapport le premier jour de chaque mois, sélectionnez cette option et saisissez **1**.

   * **De** : première date à laquelle le rapport peut être exécuté. Selon le planning spécifié, la première instance de rapport peut se produire après cette date.

   * **Jusqu’au** : date d’expiration du rapport, qui peut prendre jusqu’à quatre mois civils. Avant l’expiration d’un rapport, toutes les destinations d’e-mail spécifiées reçoivent une alerte par e-mail sept jours et un jour avant la date d’expiration. Pour conserver le rapport plus longtemps, modifiez cette date.

## Section [!UICONTROL Apply Filters]

**[!UICONTROL Filter by]:** (facultatif) Dimensions supplémentaires selon lesquelles filtrer les données, que les dimensions soient incluses ou non en tant que colonnes dans le rapport. Les filtres disponibles varient selon le type de rapport et peuvent inclure : *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* et *[!UICONTROL Video Duration]*.

Pour appliquer un ou plusieurs filtres, procédez comme suit :

* Sélectionnez une dimension, puis l’opérateur (*égal à* ou *différent de*), puis sélectionnez la valeur applicable. Par exemple, pour renvoyer des données pour les annonces publicitaires de pré-classement uniquement, spécifiez « [!UICONTROL Ad Type equals Preroll] ».
* (Facultatif) Ajoutez des critères supplémentaires au filtre.
* (Facultatif) Ajoutez des filtres supplémentaires, chacun avec un ou plusieurs critères.

\* *[!UICONTROL Account]* est disponible pour les types de rapports suivants uniquement lorsque votre organisation est configurée pour la création de rapports entre comptes [cross-account](report-about.md#cross-account-reporting) : [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] et [!UICONTROL Conversion]. Pour plus d’informations sur les rapports entre comptes, contactez l’équipe chargée de votre compte Adobe.

**[!UICONTROL Include data from Adobe Advertising SSC]:** (rapports Chemin d’accès à la conversion, Longueur du chemin et Délai d’accès à la conversion uniquement) Inclut des données pour les clics sur les annonces de recherche provenant de campagnes Advertising Search, Social et Commerce spécifiées. Lorsque vous sélectionnez cette option :

1. Sélectionnez le compte Search, Social et Commerce à l’aide du filtre **Filtrer par[!UICONTROL SSC Account]**.

1. Sélectionnez les campagnes à l’aide du filtre **Filtrer par[!UICONTROL SSC Campaign]**.

   Pour sélectionner plusieurs campagnes, cliquez sur **[!UICONTROL Add Criteria]** pour la deuxième campagne et les suivantes.

## Section [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** les colonnes de données, ou en-têtes, à inclure dans le rapport. Pour ajouter une colonne, développez la catégorie et cochez la case en regard du nom de la colonne. Les colonnes disponibles varient selon le rapport et toutes les mesures indisponibles sont désactivées. Les catégories de données disponibles peuvent inclure :

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Les rapports [!UICONTROL Household Reach & Frequency] et [!UICONTROL Path to Conversion] ne peuvent inclure qu’une seule dimension.
  > Les rapports [!UICONTROL Path Length] et [!UICONTROL Time to Conversion] n’incluent pas de dimensions.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Le rapport [!UICONTROL Household Reach & Frequency] peut inclure des mesures avec chevauchement ou des mesures sans chevauchement, mais pas les deux.

* [!UICONTROL Conversion Metrics] (trié par annonceur)

* [!UICONTROL Custom Goals] (trié par annonceur)

Voir « [Colonnes de rapport disponibles](report-columns.md) » pour obtenir une description de toutes les options.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** ordre des en-têtes de colonne. Vous pouvez faire glisser et déposer n’importe quelle colonne pour personnaliser l’ordre.

**[!UICONTROL Format]:** Génération d’un rapport au format *[!UICONTROL CSV]* (valeurs séparées par des virgules) ou *[!UICONTROL Tab]* (valeurs séparées par des tabulations).

**[!UICONTROL Headers]:** s’il faut *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]* les en-têtes de colonne.

## Section [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Les paramètres varient selon le type de rapport :

* **\[Type d’attribution\]:** ([!UICONTROL Household Conversion] des rapports avec des colonnes [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] ; annonceurs avec un suivi des conversions Adobe Advertising uniquement) Dans le rapport, comment attribuer les données de conversion dans une série d’événements qui conduisent à une conversion :

   * *[!UICONTROL Unique]:* (valeur par défaut) compte le nombre de fois qu’une valeur de dimension (un appareil ou un emplacement, par exemple) a été sur le chemin d’accès à la conversion.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* distribue le crédit de chaque conversion en fonction de la fréquence d’occurrence de la valeur de dimension (telle qu’un appareil ou un emplacement) sur le chemin d’accès à la conversion. Par exemple, s’il y avait un total de 10 impressions avant la conversion, avec 8 sur CTV et 2 sur Mobile, alors 80 % du crédit (0,8) est attribué aux écrans de CTV et 0,2 à Mobile.

* **\[Type de règle\]:** (tous les rapports [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] et [!UICONTROL Site] avec des colonnes [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] ; annonceurs avec un suivi de conversion d’Adobe Advertising uniquement) Dans le rapport, comment attribuer les données de conversion dans une série d’événements qui conduisent à une conversion. Vous pouvez choisir plusieurs règles pour comparer les différences entre elles.

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

Consultez également la section « [Comment les règles d’attribution sont calculées pour l’Adobe Advertising ](/help/search-social-commerce/reports/attribution-rules.md) ».

* **Recherche en amont :** ([!UICONTROL Household Conversion] des rapports avec [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colonnes et [!UICONTROL Path to Conversion], [!UICONTROL Path Length] ou [!UICONTROL Time to Conversion] des rapports avec [!UICONTROL Conversion Metrics] colonnes uniquement ; annonceurs avec suivi des conversions d’Adobe Advertising uniquement) dans le rapport, le nombre maximal de jours après un événement d’impression ou un événement de clic (pour les rapports [!UICONTROL Path to Conversion], [!UICONTROL Path Length] ou [!UICONTROL Time to Conversion]) dans lequel un événement de conversion peut lui être attribué. La valeur par défaut est *[!UICONTROL 30 days]* et la valeur maximale est de 92 jours.

  >[!TIP]
  >
  >Si vous utilisez [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), utilisez le même intervalle de recherche en amont que celui utilisé dans [!DNL Analytics].

**[!UICONTROL Paths as Columns]:** (tous les rapports [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] et [!UICONTROL Site] avec des colonnes [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals]) Types de conversions à signaler lorsque des événements précédents se sont produits sur le même appareil. Vous pouvez inclure jusqu’à trois types. Pour chaque type sélectionné, une colonne distincte est incluse pour chaque mesure de conversion et est ajoutée avec le suffixe spécifié ([!UICONTROL (tl)], [!UICONTROL (ct)] ou [!UICONTROL (vt)]) :

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* inclut les conversions attribuées aux clics (CT pour les clics publicitaires) et aux impressions (VT pour les vues publicitaires). Les conversions attribuées aux impressions sont multipliées par le poids de visionnage publicitaire spécifié. Le poids d’affichage publicitaire par défaut est de 100 %, ce qui signifie que les conversions attribuées aux impressions sont comptabilisées comme 100 % de la valeur des conversions attribuées aux clics.

* *[!UICONTROL With Clicks (CT)]:* inclut uniquement les conversions attribuées aux clics.

* *[!UICONTROL Impressions Only (VT)]:* inclut uniquement les conversions attribuées aux impressions, car aucun clic n’a été suivi dans le chemin de conversion.

**[!UICONTROL Conversion Reporting Based On]:** Comment rapporter des données de conversion :

* *[!UICONTROL Conversion Timestamp]:* (valeur par défaut) Les conversions sont associées à la date de conversion.

* *[!UICONTROL Event Timestamp]:* Les conversions sont signalées en fonction de la date de l’impression ou du clic qui a provoqué la conversion, telle que déterminée par le [!UICONTROL Attribution Rule Settings] spécifié.

## Section [!UICONTROL Add Report Destinations]

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

**[!UICONTROL Destination Name]:** (types de destination S3, FTP, sFTP et FTP SSL uniquement) Noms des destinations de rapport vers lesquelles le rapport personnalisé est envoyé.

* Pour spécifier une destination existante, sélectionnez un nom de destination dans la liste. Vous pouvez sélectionner plusieurs noms de destination séparément.

* Pour créer une destination :

   1. Cliquez sur **Ajouter une nouvelle destination**.

   1. Saisissez le [paramètres de destination du rapport](/help/dsp/reports/report-destinations/report-destination-settings.md), puis cliquez sur **Enregistrer**.

   1. De retour dans les paramètres du rapport, cliquez sur **Actualiser les noms de destination.**

      La nouvelle destination est désormais disponible dans la liste des destinations existantes et vous pouvez éventuellement l’ajouter au rapport.

>[!MORELIKETHIS]
>
>* [À propos des rapports personnalisés](/help/dsp/reports/report-about.md)
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Dupliquer un rapport personnalisé](/help/dsp/reports/report-copy.md)
>* [Modifier un rapport personnalisé](/help/dsp/reports/report-edit.md)
>* [Télécharger un rapport personnalisé](/help/dsp/reports/report-download.md)
>* [Exécution d’un rapport personnalisé](/help/dsp/reports/report-run-now.md)
>* [Paramètres de rapport personnalisés](/help/dsp/reports/report-settings.md)
>* [À propos des destinations de rapport](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)
