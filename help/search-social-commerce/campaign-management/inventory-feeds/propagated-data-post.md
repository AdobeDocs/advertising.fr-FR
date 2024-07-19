---
title: Données de campagne de publication générées à partir de flux vers les réseaux publicitaires
description: Découvrez comment publier des données générées à partir de flux de données d’inventaire sur des réseaux publicitaires.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: 2cf15dbab3dc00ec88a41e4f7d8b5b3646b843e8
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Données de campagne de publication générées à partir de flux vers les réseaux publicitaires

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Vous pouvez publier des données de campagne générées à partir d’un flux lorsque vous propagez les données par le biais des modèles associés ou dans le cadre d’un processus distinct. Une fois que vous publiez des données, toutes les données propagées existantes sont supprimées des listes [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

Pour une publication réussie, tous les groupes publicitaires doivent être affectés aux campagnes, tous les mots-clés et publicités doivent être affectés aux groupes publicitaires et toutes les informations requises doivent être incluses sans violation de longueur.

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate and Preview]&quot;, [publiez le fichier de feuille d’envoi groupé généré](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (appelé &quot;`<feed file name>_<template name>`&quot;) à partir de la vue [!UICONTROL Bulksheets].

  Si vous n&#39;avez pas précédemment [validé vos landing pages](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), vous pouvez le faire avant de publier le fichier.

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate only]&quot;, vous pouvez publier les données générées pour les composants ayant le statut [[!UICONTROL New]](propagated-data-status.md) dans une vue de hiérarchie de campagne à partir de l’onglet [!UICONTROL Templates].

  >[!NOTE]
  >
  >Les composants actifs ou supprimés peuvent inclure des sous-composants nouveaux et les sous-composants peuvent être publiés si les données sont valides.

  >[!TIP]
  >
  >Si vous n&#39;avez pas validé précédemment vos landing pages et souhaitez le faire, alors [propagez les données et prévisualisez-les](feed-data-propagate.md) depuis la vue [!UICONTROL Bulksheets] au lieu de les publier sur le réseau publicitaire. Vous pouvez ensuite [valider les URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) avant de publier manuellement le fichier sur le réseau publicitaire.

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

   1. Cochez la case en regard du modèle.

   1. Dans la barre d’outils, cliquez sur **[!UICONTROL Post]**.

   1. Dans les paramètres de publication, saisissez ou sélectionnez des informations dans les champs, puis cliquez sur **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Quels composants de compte sont publiés.

      * **[!UICONTROL Scheduling]:** Quand publier le fichier :

         * *[!UICONTROL Post to search engine now]* (valeur par défaut) : crée un fichier de feuille en vrac à partir des données de flux propagées et commence à les publier immédiatement.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* crée un fichier de feuille d’envoi groupé et le publie ultérieurement. Indiquez les informations suivantes :

            * **[!UICONTROL Start Time]:** date et heure futures auxquelles le fichier de feuille d’envoi groupé doit être publié sur le réseau publicitaire. Par défaut, le fichier est envoyé à 00:00 (12:00) le jour suivant. **Remarque :** Pour les fichiers volumineux qui nécessitent un traitement plus long, les données publiées ne sont pas disponibles immédiatement dans les vues de gestion de campagne ou dans le gestionnaire de publicités du réseau.

            * **[!UICONTROL End Time]:** Date et heure futures auxquelles les publicités publiées peuvent être suspendues ou supprimées en fonction du [ paramètre de données de flux ](feed-settings-manage.md#feed-data-settings) pour &quot;[!UICONTROL When the Scheduled End Date is reached]&quot;. Par défaut, l’heure de fin est à 00 h (12 h 00) 30 jours à partir d’aujourd’hui. Sélectionnez **[!UICONTROL None]** pour que les données restent actives indéfiniment (ou jusqu’à ce que vous propagiez de nouvelles données pour le modèle) ou spécifiez une date et une heure.

              Pour spécifier une date, utilisez le format JJ/MM/AAAA ou JJ/M/AAAA ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar.png "Calendrier") pour ouvrir le calendrier et [sélectionnez une date](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Pour modifier une heure, saisissez l’heure au format 24 heures HH/MM ou H/M ou sélectionnez une heure (par intervalles de 30 minutes) dans la liste.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** crée un fichier de feuille en vrac disponible à partir de la vue [!UICONTROL Search] > [!UICONTROL Bulksheets]. Vous pouvez éventuellement publier le fichier à partir de là.

           Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, il est au format ZIP. Vous n’avez pas besoin de décompresser le fichier pour le publier.

      * **[!UICONTROL Generate Tracking URLs]:** Inclure ou non les URL de suivi des mots-clés et des variations de publicités dans le fichier de feuille d’envoi groupé : *[!UICONTROL Yes]* (valeur par défaut) ou *[!UICONTROL No]*.

        Si vous sélectionnez *[!UICONTROL Yes]*, les URL sont générées à partir des URL de base des mots-clés et des publicités en fonction des paramètres [!UICONTROL Tracking Methods] des [ paramètres du compte ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) ou, si vous mappez des données à des campagnes existantes, vers les paramètres [!UICONTROL Tracking Methods] des [ paramètres de campagne ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) existants.

        S’il existe des URL de suivi pour les éléments pertinents, elles ne sont pas regénérées tant que de nouvelles URL ne sont pas nécessaires (par exemple, si le type de correspondance du mot-clé, le texte créatif ou les paramètres de suivi du compte ont changé).

      * **[!UICONTROL Bulksheet Name]:** nom du fichier de feuille d’envoi groupé à créer à partir des données de flux propagées. Par défaut, le fichier est nommé `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Vous pouvez renommer le fichier comme vous le souhaitez, mais il doit se terminer par l’une des extensions de fichier suivantes : `.tsv` (pour les valeurs séparées par des tabulations), `.txt` (pour le texte ASCII), `.csv` (pour les valeurs séparées par des virgules) ou `.zip` (pour un fichier TSV compressé). Pour les données contenant des caractères internationaux, utilisez le format TSV ou TXT.

        Le fichier publié est disponible dans la vue [!UICONTROL Bulksheets] pendant 30 jours, que vous le publiiez ou non sur le réseau publicitaire.

La colonne &quot;[!UICONTROL Last Prop. Status]&quot; indique l’état de la tâche pour les modèles applicables.

Lorsque la feuille d’envoi groupé est créée, elle est répertoriée dans la vue [!UICONTROL Bulksheets]. Lorsque le fichier est publié, une notification par courrier électronique est envoyée avec un lien vers le fichier. Cependant, si l’ensemble ou une partie des données ne peuvent pas être publiées, un fichier d’erreur est répertorié dans la vue [!UICONTROL Bulksheets] et une notification électronique est envoyée avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>* Quelle que soit l’option de planification que vous avez sélectionnée, les données spécifiées sont supprimées des listes [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].
>* Le traitement de grandes quantités de données prend plus de temps. Vous pouvez suivre la progression du fichier pendant le processus.
>* Toutes les données publiées sont soumises au processus éditorial du réseau.
>* Avant la publication d’un fichier de feuille d’envoi groupé, vous pouvez [annuler la publication](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Affichage des données générées à partir de flux](propagated-data-view.md)
>* [Modifier les données générées à partir de flux](propagated-data-edit.md)
>* [Arrêter une tâche de publication pour les données de flux d’inventaire](stop-job.md)
>* [États des données générées à partir de flux](propagated-data-status.md)
