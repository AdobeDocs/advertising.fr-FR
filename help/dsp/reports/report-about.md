---
title: À Propos Des Rapports Personnalisés
description: Découvrez les options permettant de créer des rapports personnalisés manuellement ou d’utiliser des modèles de rapport préconfigurés.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 49e254ca954389b1ea13ac571de55f404ed7ba7c
workflow-type: tm+mt
source-wordcount: '1498'
ht-degree: 0%

---

# À Propos Des Rapports Personnalisés

Les rapports personnalisés vous permettent de personnaliser le contenu et la diffusion de vos données de rapport à l’aide des dimensions de campagne (telles que l’annonceur, l’emplacement, les sites ou les zones géographiques) et des mesures qui vous intéressent le plus. Vous pouvez effectuer l’une des opérations suivantes :

* Configurez complètement les rapports de performances de campagne au niveau granulaire.

* Faites votre choix parmi les modèles de rapport préconfigurés et, éventuellement, personnalisez-les davantage.

Vous pouvez générer des rapports une fois ou les planifier de manière quotidienne, hebdomadaire ou mensuelle à 03h00 dans le fuseau horaire spécifié, selon des critères précis (par exemple, tous les 15 jours ou le 1er de chaque mois). Une fois qu’un rapport est généré, vous pouvez le télécharger à partir de [!UICONTROL Reports] > [!UICONTROL Custom Reports] ou à partir de [destinations de rapport](/help/dsp/reports/report-destinations/report-destination-about.md) liées des types suivants :

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* <!-- (in beta) --> SSL FTP
* SFTP

>[!NOTE]
>
>Vous pouvez également afficher des données à la demande à tous les niveaux d’une campagne (campagne, package, emplacement ou publicité) [dans la vue de gestion de campagne appropriée](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Types de rapports disponibles

* **[!UICONTROL Custom]:** ce rapport est un modèle vierge que vous pouvez utiliser pour créer votre propre rapport personnalisé à l’aide de la plupart des dimensions et des mesures. Les rapports [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo] et [!UICONTROL Site] sont des variantes de ce modèle avec des colonnes et des dimensions présélectionnées pour leurs cas d’utilisation respectifs.

* Modèles de rapport préconfigurés

   * **[!UICONTROL Billing]:** utilisez ce rapport pour comprendre les mesures de facturation clés, telles que les mesures de dépenses pour la facturation des médias par campagne. Les données ne sont pas disponibles pour les emplacements qui ciblent des ID universels.

     >[!NOTE]
     >
     >Ce rapport inclut des données sur le segment de facturation. Si une impression appartenant à plusieurs segments est diffusée à un utilisateur, une seule impression est créditée à un segment facturable.

   * **[!UICONTROL Conversion]:** utilisez ce rapport pour comprendre les performances de vos campagnes en fonction des mesures de conversion capturées à l’aide du suivi des conversions d’Adobe Advertising. Ce rapport comprend l’attribution multipoint.

  <!--
    * **[!UICONTROL Custom Creative Report Beta]:** (Beta feature) Use this report to monitor performance across your Advertising Creative ad experiences.
    -->

   * **[!UICONTROL Device]:** utilisez ce modèle prérempli pour afficher les mesures clés par dimensions liées à l’appareil.

   * **[!UICONTROL Frequency (by Impression)]:** utilisez ce rapport pour comprendre la distribution des impressions affichées pour les visiteurs uniques (par exemple, le nombre de visiteurs uniques qui ont vu une impression, deux impressions, trois impressions, etc.). Les données sont disponibles par emplacement ou campagne.

     >[!NOTE]
     >
     >* Les données sont disponibles après le 1er mars 2019.
     >* La fréquence est estimée sur la base d&#39;un échantillonnage de données.
     >* Pour certains stocks, les éditeurs ne transmettent pas d’identifiant d’appareil, ce qui empêche le suivi de la fréquence. Ce rapport inclut uniquement les impressions pour lesquelles un identifiant d’appareil était disponible.

   * **[!UICONTROL Frequency (by App/Site)]:** utilisez ce rapport pour comprendre le nombre d’utilisateurs uniques auxquels vos publicités ont été associées par application ou par site. Vous pouvez également voir le nombre d’utilisateurs uniques auxquels vos publicités ont été accessibles via une application ou un site spécifique (« utilisateurs uniques distincts »).

     >[!NOTE]
     >
     >* Les données sont disponibles après le 15 novembre 2018.
     >* Pour certains stocks privés, les éditeurs ne transmettent pas d’identifiant d’appareil, ce qui empêche le suivi de la fréquence.

   * **[!UICONTROL Geo]** : utilisez ce modèle prérempli pour afficher les mesures clés par dimensions géographiques.

   * **[!UICONTROL Margin]:** utilisez ce rapport pour afficher les mesures clés telles que la marge, le profit et d’autres mesures de dépenses par campagne ou par emplacement. Les données ne sont pas disponibles pour les emplacements qui ciblent des ID universels.

   * **[!UICONTROL Segment]:** utilisez ce modèle prérempli pour afficher les mesures clés par segment.

     >[!NOTE]
     >
     >* Ce rapport est destiné à montrer les performances des différents segments ciblés. Il utilise les données d’appartenance à un segment. Lorsqu’une impression est transmise à une personne ou à un appareil appartenant à deux segments ciblés ou plus, ce rapport inclut une ligne pour chaque segment. Pour cette raison, les totaux de ce rapport peuvent ne pas correspondre à la diffusion réelle.
     >* Les mesures de conversion et les données d’objectif personnalisées pour les segments sont disponibles après le 2 août 2019. Toutes les autres données pour les segments seront disponibles à partir du 1er juin 2018.

   * **[!UICONTROL Site]:** par défaut, inclut les mesures standard, les dépenses nettes totales des médias et les dépenses nettes totales facturables par site.

   * **[!UICONTROL Household Reach & Frequency]:** utilisez ce rapport pour afficher les impressions, la portée et la fréquence pour une seule dimension dans les formats d’annonce publicitaire au niveau d’un foyer en fonction de l’adresse IP, plutôt qu’au niveau d’un appareil ou d’un cookie. Utilisez les informations pour optimiser votre mix média, améliorer les performances et identifier les opportunités de portée incrémentielle. Voir « [FAQ sur les rapports des ménages](/help/dsp/reports/faq-reports.md) » pour plus d’informations. Les données ne sont pas disponibles pour les emplacements qui ciblent des ID universels.

   * **[!UICONTROL Household Conversions]:** utilisez ce rapport pour afficher les conversions d’affichage publicitaire au niveau du foyer en fonction de l’adresse IP, plutôt qu’au niveau d’un appareil ou d’un cookie. Utilisez les informations pour mesurer et optimiser les performances des campagnes. Voir « [FAQ sur les rapports des ménages](/help/dsp/reports/faq-reports.md) » pour plus d’informations. Les données ne sont pas disponibles pour les emplacements qui ciblent des ID universels.

   * **[!UICONTROL Path to Conversion Beta]:** (fonctionnalité Beta) Utilisez ce rapport pour identifier comment optimiser les budgets et personnaliser les annonces en fonction des séquences d’interaction publicitaire les plus performantes. Le rapport présente la séquence des points d’interaction au sein d’un même foyer qui mènent à chacune des mesures de conversion sélectionnées dans la plage de données spécifiée. Le rapport utilise une période de recherche en amont spécifiée entre la première interaction et une conversion et peut inclure une dimension :

      * [!UICONTROL Channel Assist Type] : indique comment les canaux marketing suivants ont contribué au processus de conversion : [!UICONTROL Audio Impression], [!UICONTROL CTV Impression], [!UICONTROL Display Click], [!UICONTROL Display Impression], [!UICONTROL Native Click], [!UICONTROL Native Impression], [!UICONTROL Search Click], [!UICONTROL Video Click] ou [!UICONTROL Video Impression].

      * [!UICONTROL Campaign ID] ou [!UICONTROL Campaign Name] : indique les campagnes qui ont contribué au processus de conversion.

      * [!UICONTROL Ad ID] ou [!UICONTROL Ad Name] indique quelles publicités DSP ont généré des conversions.

      * [!UICONTROL Ad ID & Paid Keyword (SSC)] ou [!UICONTROL Ad Name & Paid Keyword (SSC)] indique les mots-clés Search, Social et Commerce qui ont généré des conversions.

     Les colonnes du rapport incluent « [!UICONTROL Event #1] » à « [!UICONTROL Event #10] », « [!UICONTROL Path Length] », « % \&lt;Nom de la mesure de conversion 1\> », « % \&lt;Nom de la mesure de conversion 2\> », etc.

     Jusqu’aux 10 points d’interaction les plus récents sont inclus. Les lignes du chemin sont classées en fonction du nombre de conversions.

     Pour une comparaison de ce rapport avec les rapports créés par [!DNL Advanced Measurement Services] et Adobe Analytics, reportez-vous à « [FAQ sur les rapports personnalisés](/help/dsp/reports/faq-reports.md) ».

   * **[!UICONTROL Path Length Beta]:** (fonctionnalité Beta) : utilisez ce rapport pour      suivez le nombre de points d’interaction utilisateur requis pour les conversions au fil du temps afin de choisir la fréquence publicitaire optimale. Le rapport indique le nombre de conversions par longueur de chemin (points d’interaction), par exemple le nombre de conversions qui se sont produites après qu’un utilisateur n’a eu qu’une seule interaction publicitaire, deux interactions publicitaires, etc. Le rapport peut inclure des données pour plusieurs mesures de conversion et utilise une période de recherche en amont spécifiée entre la première interaction et une conversion. Les colonnes du rapport incluent « [!UICONTROL Path Length] », « [!UICONTROL Number of] \&lt;Nom de la mesure de conversion 1\> », « % \&lt;Nom de la mesure de conversion 1\> », « \&lt;Nom de la mesure de conversion 2\> », « % \&lt;Nom de la mesure de conversion 2\> », etc.

     Les données sont affichées pour chaque longueur de chemin allant jusqu’à 10 ; les données pour les longueurs de chemin supérieures à 10 sont regroupées.

   * **[!UICONTROL Time to Conversion Beta]:** (fonctionnalité Beta) : utilisez ce rapport pour déterminer l’intervalle de recherche en amont d’attribution optimal et pour identifier les campagnes dont les temps de conversion sont plus longs, qui peuvent bénéficier du reciblage. Le rapport indique le nombre de conversions par la durée en jours entre la dernière interaction (exposition publicitaire ou clic) et la conversion. Le rapport peut inclure des données pour plusieurs mesures de conversion et utilise une période de recherche en amont spécifiée entre la première interaction et une conversion. Les colonnes du rapport incluent « [!UICONTROL Time Taken (in days)] », « [!UICONTROL Number of] \&lt;Nom de la mesure de conversion 1\> », « % \&lt;Nom de la mesure de conversion 1\> », « \&lt;Nom de la mesure de conversion 2\> », « % \&lt;Nom de la mesure de conversion 2\> », etc. Les conversions dont la durée est supérieure à la période de recherche en amont sont regroupées dans une ligne (par exemple, si le rapport utilise une période de recherche en amont de 30 jours, toutes les conversions dont la durée est supérieure à 30 jours sont regroupées dans une ligne avec une valeur « [!UICONTROL Time Taken (in days)] » de « 30+ »).

## Reporting entre comptes {#cross-account-reporting}

Toute organisation disposant de plusieurs comptes DSP peut éventuellement activer les données entre comptes dans des rapports personnalisés, en fonction des besoins de l’organisation. Par exemple, vous pouvez donner au compte A l’accès aux données du compte B et donner au compte B l’accès aux données du compte C (mais pas au compte A). Pour activer et configurer cette fonctionnalité, contactez l’équipe chargée de votre compte Adobe.

Une fois la fonctionnalité activée pour votre organisation, vous pouvez [filtrer](report-settings.md) l’un des types de rapports suivants par compte : [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] et [!UICONTROL Conversion].

Les paramètres de votre compte à l’adresse [!UICONTROL Settings] > [!UICONTROL Account] indiquent a) les autres comptes dont les données sont disponibles pour votre compte et b) les autres comptes qui peuvent accéder aux données de votre compte.

## La vue [!UICONTROL Custom Reports]

[!UICONTROL Reports] > [!UICONTROL Custom Reports] répertorie les rapports existants, y compris les rapports générés, ceux planifiés pour une génération ultérieure et ceux qui ont échoué. La colonne « [!UICONTROL Report Run] » indique les dates de déclenchement du rapport à compter du 22 août 2024. Par défaut, tous les rapports non archivés créés par l’utilisateur sont répertoriés, le plus récent en haut. Vous pouvez filtrer davantage la liste par statut, que le rapport soit récurrent ou ponctuel, le type de rapport, le type de destination et le créateur du rapport.

Vous pouvez créer des rapports personnalisés, modifier des rapports existants ou les dupliquer pour créer de nouveaux rapports, exécuter des rapports immédiatement, télécharger n’importe quelle instance de rapport des quatre derniers mois et supprimer des rapports.

## Statuts des rapports {#custom-report-status}

* **[!UICONTROL Yet to start]:** Le rapport n&#39;a jamais été exécuté.

* **[!UICONTROL Report generating]:** Le rapport est en cours de création.

* **[!UICONTROL Ready to download]:** (rapports récurrents uniquement) Une ou plusieurs instances du rapport peuvent être téléchargées et d’autres instances de rapport sont planifiées.

* **[!UICONTROL Failed]:** La tâche de rapport a échoué. Pour savoir pourquoi des instances de rapport individuelles ont échoué pour une ligne de rapport, cliquez sur ![la flèche vers le bas](/help/dsp/assets/chevron-down.png "la flèche vers le bas") en regard de [!UICONTROL Download]. Les tâches de rapport ayant échoué sont indiquées par une icône d’erreur (![indicateur d&#39;erreur](/help/dsp/assets/indicator-critical.png "indicateur d&#39;erreur")). Pour obtenir une description de l’erreur, placez le curseur sur l’icône d’erreur.

* **[!UICONTROL Completed]:** Pour les rapports non récurrents, le rapport est terminé. Pour les rapports récurrents, toutes les instances de rapport sont terminées. Vous pouvez télécharger tous les rapports terminés au cours des quatre derniers mois.

* **[!UICONTROL Archived]:** Le rapport est archivé et ne peut pas être exécuté. Ce statut est défini lorsque la génération d’un rapport échoue plusieurs fois. Actuellement, vous ne pouvez pas définir ce statut à partir de l’interface utilisateur.

>[!MORELIKETHIS]
>
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Télécharger un rapport personnalisé](/help/dsp/reports/report-download.md)
>* [Paramètres de rapport personnalisés](/help/dsp/reports/report-settings.md)
>* [FAQ sur les rapports des ménages](/help/dsp/reports/faq-reports.md)
>* [Types de rapports de performances dans les vues de gestion de campagnes](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)
>* [À propos des [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
