---
title: À propos des rapports personnalisés
description: Découvrez les options de création manuelle de rapports personnalisés ou d’utilisation de modèles de rapports préconfigurés.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 44f7f9b31afbe6b863acd389df641057b1e6dea1
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# À propos des rapports personnalisés

Les rapports personnalisés vous permettent de personnaliser le contenu et la remise des données de votre rapport à l’aide des dimensions de campagne (comme l’annonceur, l’emplacement, les sites ou les zones géographiques) et des mesures qui vous intéressent le plus. Vous pouvez :

* Configurez complètement les rapports de performances de campagne à un niveau granulaire.

* Choisissez parmi des modèles de rapport préconfigurés et personnalisez-les éventuellement davantage.

Vous pouvez générer les rapports une seule fois ou programmer leur génération quotidienne, hebdomadaire ou mensuelle à 03h00 dans le fuseau horaire spécifié selon des critères précis (par exemple tous les 15 jours ou le 1er de chaque mois). Une fois un rapport généré, vous pouvez le télécharger à partir de [!UICONTROL Reports] > [!UICONTROL Custom Reports] ou des [destinations de rapport](/help/dsp/reports/report-destinations/report-destination-about.md) liées des types suivants :

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>Vous pouvez également afficher les données à la demande à tous les niveaux d&#39;une campagne (campagne, package, emplacement ou publicité) [ dans la vue de gestion de campagne appropriée](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Types de rapports disponibles

* **[!UICONTROL Custom]:** Ce rapport est un modèle vierge que vous pouvez utiliser pour créer votre propre rapport personnalisé à l’aide de la plupart des dimensions et mesures. Les rapports [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo] et [!UICONTROL Site] sont des variantes de ce modèle avec des colonnes et des dimensions présélectionnées pour leurs cas d’utilisation respectifs.

* Modèles de rapport préconfigurés

   * **[!UICONTROL Billing]:** Utilisez ce rapport pour comprendre les mesures de facturation clés, telles que les mesures de dépenses pour la facturation des médias par campagne. Les données ne sont pas disponibles pour les emplacements qui ciblent des identifiants universels.

     >[!NOTE]
     >
     >Ce rapport contient des données sur le segment de facturation. Si une impression diffusée par un utilisateur ou un appareil appartient à plusieurs segments, un seul segment facturable est crédité de l’impression.

   * **[!UICONTROL Conversion]:** Utilisez ce rapport pour comprendre les performances de vos campagnes en fonction des mesures de conversion capturées à l’aide du suivi de conversion d’Adobe Advertising. Ce rapport comprend l’attribution multipoint.

   * **[!UICONTROL Device]:** Utilisez ce modèle prérenseigné pour afficher les mesures clés par dimensions liées à l’appareil.

   * **[!UICONTROL Frequency (by Impression)]:** Utilisez ce rapport pour comprendre la distribution des impressions affichées pour les visionneuses uniques (par exemple, le nombre de visionneuses uniques qui ont vu une impression, deux impressions, trois impressions, etc.). Les données sont disponibles par emplacement ou campagne.

     >[!NOTE]
     >
     >* Les données sont disponibles après le 1er mars 2019.
     >* La fréquence est estimée sur la base d&#39;un échantillonnage de données.
     >* Pour certains inventaires, les éditeurs ne transmettent pas d’identifiant d’appareil, ce qui empêche le suivi des fréquences. Ce rapport inclut uniquement les impressions pour lesquelles un identifiant d’appareil était disponible.

   * **[!UICONTROL Frequency (by App/Site)]:** Utilisez ce rapport pour comprendre le nombre d’utilisateurs uniques atteints par l’application ou par site. Vous pouvez également voir le nombre d’utilisateurs uniques auxquels vous avez accédé par le biais d’une application ou d’un site spécifique (&quot;utilisateurs uniques distincts&quot;).

     >[!NOTE]
     >
     >* Les données sont disponibles après le 15 novembre 2018.
     >* Pour certains inventaires privés, les éditeurs ne transmettent pas d’identifiant d’appareil, ce qui empêche le suivi des fréquences.

   * **[!UICONTROL Geo]** : utilisez ce modèle prérenseigné pour afficher les mesures clés par dimensions géographiques.

   * **[!UICONTROL Margin]:** Utilisez ce rapport pour afficher les mesures clés telles que les marges, les bénéfices et les autres mesures de dépenses par campagne ou emplacement. Les données ne sont pas disponibles pour les emplacements qui ciblent des identifiants universels.

   * **[!UICONTROL Segment]:** Utilisez ce modèle prérenseigné pour afficher les mesures clés par segment.

     >[!NOTE]
     >
     >* Ce rapport est destiné à montrer les performances de différents segments ciblés. Elle utilise des données d’adhésion au segment. Lorsqu’une impression est diffusée sur une personne ou un appareil appartenant à deux segments ciblés ou plus, ce rapport comprend une ligne pour chaque segment. Pour cette raison, les totaux de ce rapport peuvent ne pas correspondre à la diffusion réelle.
     >* Les mesures de conversion et les données d’objectif personnalisées pour les segments sont disponibles après le 2 août 2019. Toutes les autres données relatives aux segments sont disponibles à compter du 1er juin 2018.

   * **[!UICONTROL Site]:** Par défaut, inclut les mesures standard, les dépenses nettes totales des médias et les dépenses nettes facturables totales par site.

   * **[!UICONTROL Household Reach & Frequency]:** Utilisez ce rapport pour afficher les impressions, la portée et la fréquence d’une dimension unique dans les formats d’annonce au niveau d’un foyer en fonction de l’adresse IP, plutôt qu’au niveau d’un appareil/d’un cookie. Utilisez les insights pour optimiser votre mix média, améliorer les performances et identifier les opportunités de portée incrémentielle. Pour plus d’informations, voir &quot;[Questions fréquentes sur les rapports des ménages](/help/dsp/reports/faq-household-report.md)&quot;. Les données ne sont pas disponibles pour les emplacements qui ciblent des identifiants universels.

   * **[!UICONTROL Household Conversions]:** Utilisez ce rapport pour afficher les conversions d’affichages publicitaires au niveau du foyer en fonction de l’adresse IP, plutôt qu’au niveau de l’appareil ou du cookie. Utilisez les insights pour mesurer et optimiser les performances de la campagne. Pour plus d’informations, voir &quot;[Questions fréquentes sur les rapports des ménages](/help/dsp/reports/faq-household-report.md)&quot;. Les données ne sont pas disponibles pour les emplacements qui ciblent des identifiants universels.

## Rapports inter-comptes {#cross-account-reporting}

Toute organisation disposant de plusieurs comptes DSP peut éventuellement activer des données inter-comptes dans des rapports personnalisés, en fonction des besoins de l’organisation. Par exemple, vous pouvez donner au compte A l’accès aux données du compte B et au compte B l’accès aux données du compte C (mais pas au compte A). Pour activer et configurer cette fonctionnalité, contactez votre équipe de compte d’Adobe.

Une fois la fonctionnalité activée pour votre organisation, vous pouvez [filtrer](report-settings.md) l’un des types de rapports suivants par compte : [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] et [!UICONTROL Conversion].

Les paramètres de votre compte [!UICONTROL Settings] > [!UICONTROL Account] indiquent a) les autres comptes dont les données sont disponibles pour votre compte et b) les autres comptes qui peuvent accéder aux données de votre compte.

## La vue [!UICONTROL Custom Reports]

[!UICONTROL Reports] > [!UICONTROL Custom Reports] répertorie vos rapports existants, y compris les rapports qui ont été générés, ceux qui sont programmés pour la génération future et ceux qui ont échoué. La colonne &quot;[!UICONTROL Report Run]&quot; indique les dates auxquelles le rapport a été déclenché à partir du 22 août 2024. Par défaut, tous les rapports non archivés créés par l’utilisateur sont répertoriés, les plus récents en haut. Vous pouvez filtrer davantage la liste par statut, que le rapport soit récurrent ou ponctuel, par type de rapport, par type de destination et par créateur de rapport.

Vous pouvez créer de nouveaux rapports personnalisés, modifier des rapports existants ou les dupliquer pour créer de nouveaux rapports, exécuter immédiatement des rapports, télécharger une instance de rapport depuis les quatre derniers mois et supprimer des rapports.

## Statuts des rapports {#custom-report-status}

* **[!UICONTROL Yet to start]:** Le rapport n’a jamais été exécuté.

* **[!UICONTROL Report generating]:** Le rapport est en cours de création.

* **[!UICONTROL Ready to download]:** (Rapports récurrents uniquement) Une ou plusieurs instances du rapport sont disponibles au téléchargement et d’autres instances de rapport sont planifiées.

* **[!UICONTROL Failed]:** La tâche de rapport a échoué. Pour voir pourquoi des instances de rapport individuelles ont échoué pour un suivi de rapport, cliquez sur ![la flèche vers le bas](/help/dsp/assets/chevron-down.png "la flèche vers le bas") en regard de [!UICONTROL Download]. Les tâches de rapport ayant échoué sont indiquées avec une icône d’erreur (![indicateur d&#39;erreur](/help/dsp/assets/indicator-critical.png "indicateur d&#39;erreur")). Placez le curseur sur l’icône d’erreur pour obtenir une description de l’erreur.

* **[!UICONTROL Completed]:** Pour les rapports non récurrents, le rapport est terminé. Pour les rapports récurrents, toutes les instances de rapport sont terminées. Vous pouvez télécharger tous les rapports terminés au cours des quatre derniers mois.

* **[!UICONTROL Archived]:** Le rapport est archivé et ne peut pas être exécuté. Cet état est défini lorsque la génération d’un rapport échoue plusieurs fois pour celui-ci. Actuellement, vous ne pouvez pas définir cet état à partir de l’interface utilisateur.

>[!MORELIKETHIS]
>
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Télécharger un rapport personnalisé](/help/dsp/reports/report-download.md)
>* [Paramètres de rapport personnalisés](/help/dsp/reports/report-settings.md)
>* [ Questions fréquentes sur les rapports des ménages](/help/dsp/reports/faq-household-report.md)
>* [Types de rapports de performances dans les vues Campaign Management](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)
>* [À propos de [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
