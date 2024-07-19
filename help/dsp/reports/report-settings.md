---
title: Paramètres des rapports personnalisés
description: Reportez-vous à la description des paramètres de rapport personnalisés.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# Paramètres des rapports personnalisés

**[!UICONTROL Name]** Nom du rapport. La longueur maximale est de 180 caractères.

**[!UICONTROL Report Type]** Type de rapport : *[!UICONTROL Custom]* (qui comprend la plupart des options disponibles), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]* ou *[!UICONTROL Household Conversions]*.

## Section [!UICONTROL Apply Filters]

**[!UICONTROL Timezone]:** Fuseau horaire pour la création de rapports.

**[!UICONTROL Observe Daylight Savings Time]:** considère l’heure d’été comme l’heure d’été aux heures signalées.

**\[Période\]:** La période pour laquelle générer des données. Le nombre de jours disponibles varie selon le rapport et selon les dimensions sélectionnées. Choisissez-en une :

* **[!UICONTROL Previous N days]:** inclut des données pour un nombre spécifique de jours avant aujourd’hui.

* **[!UICONTROL Custom]:** inclut des données entre des dates de début et de fin spécifiques. Pour générer des rapports sur les données du jour précédent, sélectionnez **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** inclut des données pour le mois civil précédent.

**[!UICONTROL Add Filters]:** (Facultatif) Dimensions supplémentaires par lesquelles filtrer les données, que les dimensions soient incluses ou non sous forme de colonnes dans le rapport. Les filtres disponibles varient selon le type de rapport et peuvent inclure : *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* et *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* est disponible pour les types de rapports suivants uniquement lorsque votre organisation est configurée pour la [création de rapports entre comptes](report-about.md#cross-account-reporting) : [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] et [!UICONTROL Conversion]. Contactez votre équipe de compte Adobe pour plus d’informations sur la création de rapports entre comptes.

Pour appliquer un ou plusieurs filtres, procédez comme suit :

* Sélectionnez une dimension, sélectionnez l’opérateur (*equals* ou *not equals*), puis sélectionnez la valeur applicable. Par exemple, pour renvoyer des données uniquement pour les publicités preroll, spécifiez &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Facultatif) Ajoutez des critères supplémentaires au filtre.
* (Facultatif) Ajoutez des filtres supplémentaires, chacun avec un ou plusieurs critères.

## Section [!UICONTROL Build Your Report]

**[!UICONTROL Select To Add As Report Headers]:** Colonnes de données, ou en-têtes, à inclure dans le rapport. Pour ajouter une colonne, développez la catégorie et cochez la case en regard de son nom. Les colonnes disponibles varient selon le rapport et toutes les mesures non disponibles sont désactivées. Les catégories de données disponibles sont les suivantes :

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Le rapport [!UICONTROL Household Reach & Frequency] ne peut inclure qu’une seule dimension.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Le rapport [!UICONTROL Household Reach & Frequency] peut inclure des mesures de chevauchement ou d’autres mesures, mais pas les deux.

* [!UICONTROL Conversion Metrics] (triés par annonceur)

* [!UICONTROL Custom Goals] (triés par annonceur)

Voir &quot;[Colonnes de rapport disponibles](report-columns.md)&quot; pour obtenir une description de toutes les options.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Ordre des en-têtes de colonne. Vous pouvez faire glisser et déposer n’importe quelle colonne pour personnaliser l’ordre.

**[!UICONTROL Format]:** Générer un rapport au format *[!UICONTROL CSV]* (valeurs séparées par des virgules) ou *[!UICONTROL Tab]* (valeurs séparées par des tabulations).

**[!UICONTROL Headers]:** Indique s’il faut se reporter aux en-têtes de colonne *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]*.

## Section [!UICONTROL Multi-Touch Conversion Options]

**[!UICONTROL Attribution Rule Settings]:** Les paramètres varient selon le type de rapport :

* **\[Type d’attribution\]:** ([!UICONTROL Household Conversion] rapports avec [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colonnes ; annonceurs avec suivi de conversion par Adobe Advertising uniquement) Dans le rapport, comment attribuer des données de conversion dans une série d’événements qui mènent à une conversion :

   * *[!UICONTROL Unique]:* (valeur par défaut) compte le nombre de fois où une valeur de dimension (un appareil ou un emplacement, par exemple) a été placée sur le chemin de la conversion.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* distribue le crédit de chaque conversion en fonction de la fréquence d’occurrence de la valeur de dimension (un appareil ou un emplacement, par exemple) sur le chemin d’accès à la conversion. Par exemple, s’il y avait un total de 10 impressions avant conversion, dont 8 sur CTV et 2 sur Mobile, alors 80 % du crédit (0,8) est attribué aux écrans CTV et 0,2 à Mobile.

* **\[Type de règle\]:** (Tous les rapports [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] et [!UICONTROL Site] avec des colonnes [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] ; annonceurs avec suivi de conversion par Adobe Advertising uniquement) Dans le rapport, comment attribuer des données de conversion dans une série d’événements qui mènent à une conversion. Vous pouvez choisir plusieurs règles si vous souhaitez comparer les différences entre les règles.

  >[!NOTE]
  >
  >Les chemins de conversion incluent toutes les impressions et tous les clics dans les fenêtres d’impression ou de recherche en amont des clics de l’annonceur, qui sont configurés dans [!DNL Advertising Search, Social, & Commerce]. Les clics sont préférés aux impressions lors de l’attribution de conversion. Tous les clics dans un chemin de conversion reçoivent un crédit complet en fonction de la règle d’attribution. Les impressions ne reçoivent du crédit que lorsqu’aucun clic n’est suivi dans le chemin de conversion.

   * *[!UICONTROL Last Event]:* Attribue des conversions au dernier clic ou impression dans le chemin de conversion.

   * *[!UICONTROL Weight Last More]:* Attribue des conversions à tous les événements du chemin de conversion, mais donne le plus de poids au dernier événement et, successivement, le moins de poids aux événements précédents.

   * *[!UICONTROL Even Distribution]:* Attribue les conversions de manière égale à chaque événement dans le chemin de conversion.

   * *[!UICONTROL Weight First More]:* Attribue des conversions à tous les événements du chemin de conversion, mais donne le plus de poids au premier événement et, successivement, le moins de poids aux événements suivants.

   * *[!UICONTROL First Event]:* Attribue des conversions au premier clic ou impression dans le chemin de conversion.

   * *[!UICONTROL U-shaped]:* Attribue la conversion à tous les événements du chemin de conversion, mais donne le plus de poids aux premier et dernier événements, avec tour de rôle moins d’importance aux événements au milieu du chemin de conversion.

   * *[!UICONTROL Display Only]:* Attribue des conversions au dernier clic ou impression DSP dans le chemin de conversion. Cela inclut les publicités vidéo et TV connectées et exclut les clics sur [!DNL Advertising Search, Social, & Commerce] publicités.

   * *[!UICONTROL Social Only]:* obsolète

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **Recherche en amont :** ([!UICONTROL Household Conversion] rapports avec des colonnes [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] ; annonceurs avec suivi de conversion par Adobe Advertising uniquement) Dans le rapport, nombre maximal de jours après un événement d’impression auquel un événement de conversion peut être attribué. La valeur par défaut est *[!UICONTROL 30 days]* et la valeur maximale est de 92 jours.

**[!UICONTROL Paths as Columns]:** (Tous les rapports [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] et [!UICONTROL Site] avec [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colonnes) Quels types de conversions signaler lorsque des événements précédents se sont produits sur le même appareil. Vous pouvez inclure jusqu’à trois types. Pour chaque type sélectionné, une colonne distincte est incluse pour chaque mesure de conversion et est ajoutée avec le suffixe spécifié ([!UICONTROL (tl)], [!UICONTROL (ct)] ou [!UICONTROL (vt)]) :

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* comprend des conversions attribuées aux clics (CT pour les clics publicitaires) et aux impressions (VT pour les affichages publicitaires). Les conversions attribuées aux impressions sont multipliées par le poids d’affichage publicitaire spécifié. Le poids par défaut de l’affichage publicitaire est de 100 %, ce qui signifie que les conversions attribuées aux impressions sont comptabilisées à 100 % de la valeur des conversions attribuées aux clics.

* *[!UICONTROL With Clicks (CT)]:* comprend uniquement des conversions attribuées aux clics.

* *[!UICONTROL Impressions Only (VT)]:* inclut uniquement les conversions qui ont été attribuées aux impressions, car aucun clic n’a été suivi dans le chemin de conversion.

**[!UICONTROL Conversion Reporting Based On]:** Comment signaler les données de conversion :

* *[!UICONTROL Conversion Timestamp]:* (valeur par défaut) Les conversions sont associées à la date de conversion.

* *[!UICONTROL Event Timestamp]:* Les conversions sont signalées en fonction de la date de l’impression ou du clic qui a provoqué la conversion, comme déterminé par le [!UICONTROL Attribution Rule Settings] spécifié.

## Section [!UICONTROL Add Report Destinations]

**[!UICONTROL Destination Type]:** Choisissez l’un des types de destinations suivants :

* *[!UICONTROL S3]:* Pour envoyer le rapport terminé à un ou plusieurs emplacements [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), que vous devez spécifier dans le champ **[!UICONTROL Destination Name]**.
* *[!UICONTROL sFTP]:* Pour envoyer le rapport terminé à un ou plusieurs emplacements SFTP, que vous devez spécifier dans le champ **[!UICONTROL Destination Name]**.
* *[!UICONTROL FTP]:* Pour envoyer le rapport terminé à un ou plusieurs emplacements FTP, que vous devez spécifier dans le champ **[!UICONTROL Destination Name]**.
* *[!UICONTROL FTP SSL](actuellement dans Beta) :* pour envoyer le rapport terminé à un ou plusieurs emplacements FTP SSL, que vous devez spécifier dans le champ **[!UICONTROL Destination Name]**.
* *[!UICONTROL Email]:* Pour spécifier la ou les adresses électroniques auxquelles envoyer les rapports ou notifications terminés si le rapport est annulé en raison d’erreurs.

>[!NOTE]
>
> Vous ne pouvez pas modifier le type de destination une fois le rapport enregistré.

**[!UICONTROL Email]:** (Type de destination d’email uniquement) Pour chaque adresse, saisissez l’adresse et cliquez sur **+**.

**[!UICONTROL Destination Name]:** (types de destination S3, FTP, sFTP et FTP SSL uniquement) Les noms des destinations de rapport vers lesquelles le rapport personnalisé est envoyé.

* Pour spécifier une destination existante, sélectionnez un nom de destination dans la liste. Vous pouvez sélectionner plusieurs noms de destination séparément.

* Pour créer une destination :

   1. Cliquez sur **Ajouter une nouvelle destination**.

   1. Saisissez les [ paramètres de destination du rapport ](/help/dsp/reports/report-destinations/report-destination-settings.md), puis cliquez sur **Enregistrer**.

   1. De retour dans les paramètres du rapport, cliquez sur **Actualiser les noms des destinations.**

      La nouvelle destination est désormais disponible dans la liste des destinations existantes et vous pouvez éventuellement l’ajouter au rapport.

**[!UICONTROL Frequency]:** (Pour chaque [!UICONTROL Destination Name]) À quelle fréquence envoyer le rapport vers la destination : *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]* ou *[!UICONTROL Monthly]*.

**[!UICONTROL Start Day]:** (Pour chaque [!UICONTROL Destination Name] avec [!UICONTROL Frequency] de *[!UICONTROL Weekly]* ou *[!UICONTROL Monthly]*) Jour de génération du rapport. Pour les rapports hebdomadaires, sélectionnez le jour de la semaine. Pour les rapports mensuels, sélectionnez le jour numérique du mois.

## Section [!UICONTROL Save Report]

**[!UICONTROL When to Generate]:** quand générer le rapport : *[!UICONTROL On Schedule]* ou *[!UICONTROL Run Now]*. Les rapports planifiés sont remis avant 9h00 dans le fuseau horaire du compte.

**[!UICONTROL End Date]:** date d’expiration du rapport, qui peut aller jusqu’à quatre mois. Avant l’expiration d’un rapport, tous les destinataires de messagerie spécifiés reçoivent une alerte sept jours et un jour avant la date d’expiration. Pour prolonger le rapport, modifiez la date d’expiration dans les paramètres du rapport.

>[!NOTE]
>
>Vous pouvez [exécuter un rapport personnalisé à tout moment](report-run-now.md) à partir de la vue [!UICONTROL Reports].

>[!MORELIKETHIS]
>
>* [À propos des rapports personnalisés](/help/dsp/reports/report-about.md)
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Dupliquer un rapport personnalisé](/help/dsp/reports/report-copy.md)
>* [Modifier un rapport personnalisé](/help/dsp/reports/report-edit.md)
>* [Exécuter un rapport personnalisé](/help/dsp/reports/report-run-now.md)
>* [Paramètres de rapport personnalisés](/help/dsp/reports/report-settings.md)
>* [À propos des destinations de rapport](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)
