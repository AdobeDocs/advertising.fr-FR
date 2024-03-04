---
title: Données de campagne de publication générées à partir de flux vers les réseaux publicitaires
description: Découvrez comment publier des données générées à partir de flux de données d’inventaire sur des réseaux publicitaires.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: c27665b979ad8e37fd4f92385bb7339af4354d5f
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Données de campagne de publication générées à partir de flux vers les réseaux publicitaires

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Vous pouvez publier des données de campagne générées à partir d’un flux lorsque vous propagez les données par le biais des modèles associés ou dans le cadre d’un processus distinct. Une fois que vous publiez des données, toutes les données propagées existantes sont supprimées de la variable [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] des listes.

Pour une publication réussie, tous les groupes publicitaires doivent être affectés aux campagnes, tous les mots-clés et publicités doivent être affectés aux groupes publicitaires et toutes les informations requises doivent être incluses sans violation de longueur.

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate and Preview],&quot; puis [publier le fichier de feuille d’envoi groupé généré ;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (nommé &quot;`<feed file name>_<template name>`&quot;) de la fonction [!UICONTROL Bulksheets] vue.

  Si vous ne l’aviez pas fait précédemment [valider vos landing pages ;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), vous pouvez le faire avant de publier le fichier.

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate only],&quot; vous pouvez ensuite publier les données générées pour les composants avec la variable [[!UICONTROL New] status](propagated-data-status.md) dans une vue hiérarchique de campagne à partir de la vue [!UICONTROL Templates] .

  >[!NOTE]
  >
  >Les composants actifs ou supprimés peuvent inclure des sous-composants nouveaux et les sous-composants peuvent être publiés si les données sont valides.

  >[!TIP]
  >
  >Si vous n’avez pas validé précédemment vos landing pages et que vous souhaitez le faire, [propagation des données et prévisualisation](feed-data-propagate.md) de la [!UICONTROL Bulksheets] plutôt que de la publier sur le réseau publicitaire. Vous pouvez alors [valider les URL ;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) avant de publier manuellement le fichier sur le réseau publicitaire.

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, qui s’ouvre sur le [!UICONTROL Templates] .

   1. Cochez la case en regard du modèle.

   1. Dans la barre d’outils, cliquez sur **[!UICONTROL Post]**.

   1. Dans les paramètres de publication, saisissez ou sélectionnez des informations dans les champs, puis cliquez sur **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Les composants de compte qui sont publiés.

      * **[!UICONTROL Scheduling]:** Quand publier le fichier :

         * *[!UICONTROL Post to search engine now]* (valeur par défaut) : crée un fichier de feuille en vrac à partir des données de flux propagées et commence à les publier immédiatement.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Crée un fichier de feuille d’envoi groupé et le publie ultérieurement. Indiquez les informations suivantes :

            * **[!UICONTROL Start Time]:** Date et heure futures auxquelles le fichier de feuille d’envoi groupé doit être publié sur le réseau publicitaire. Par défaut, le fichier est envoyé à 00:00 (12:00) le jour suivant. **Remarque :** Pour les fichiers volumineux nécessitant un traitement plus long, les données publiées ne sont pas disponibles immédiatement dans les vues de gestion de campagne ou dans le gestionnaire d’annonces du réseau.

            * **[!UICONTROL End Time]:** Date et heure futures auxquelles les publicités publiées peuvent être suspendues ou supprimées en fonction de la variable [paramètre de données de flux](feed-settings-manage.md#feed-data-settings) pour &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; Par défaut, l’heure de fin est à 00 h (12 h 00) 30 jours à partir d’aujourd’hui. Sélectionner **[!UICONTROL None]** pour que les données restent actives indéfiniment (ou jusqu’à ce que vous propagiez de nouvelles données pour le modèle), ou spécifiez une date et une heure.

              Pour spécifier une date, utilisez le format JJ/MM/AAAA ou JJ/M/AAAA ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar.png "Calendrier") pour ouvrir le calendrier et [sélectionner une date ;](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Pour modifier une heure, saisissez l’heure au format 24 heures HH/MM ou H/M ou sélectionnez une heure (par intervalles de 30 minutes) dans la liste.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Crée un fichier de feuille en vrac disponible à partir du [!UICONTROL Search] > [!UICONTROL Bulksheets] vue. Vous pouvez éventuellement publier le fichier à partir de là.

           Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, il est au format ZIP. Vous n’avez pas besoin de décompresser le fichier pour le publier.

      * **[!UICONTROL Generate Tracking URLs]:** Inclure ou non les URL de suivi des mots-clés et des variations publicitaires dans le fichier de feuille d’envoi groupé : *[!UICONTROL Yes]* (valeur par défaut) ou *[!UICONTROL No]*.

        Si vous sélectionnez *[!UICONTROL Yes]*, les URL sont ensuite générées à partir des URL de base pour les mots-clés et les publicités, en fonction de la variable [!UICONTROL Tracking Methods] dans la variable [paramètres du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) ou, si vous mappez des données avec des campagnes existantes, vers la variable [!UICONTROL Tracking Methods] des paramètres de la [paramètres de campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        S’il existe des URL de suivi pour les éléments pertinents, elles ne sont pas regénérées tant que de nouvelles URL ne sont pas nécessaires (par exemple, si le type de correspondance du mot-clé, le texte créatif ou les paramètres de suivi du compte ont changé).

      * **[!UICONTROL Bulksheet Name]:** Nom du fichier de feuille d’envoi groupé à créer à partir des données de flux propagées. Par défaut, le fichier est nommé `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Vous pouvez renommer le fichier comme vous le souhaitez, mais il doit se terminer par l’une des extensions de fichier suivantes : `.tsv` (pour les valeurs séparées par des tabulations), `.txt` (pour le texte ASCII), `.csv` (pour les valeurs séparées par des virgules) ou `.zip` (pour un fichier TSV compressé). Pour les données contenant des caractères internationaux, utilisez le format TSV ou TXT.

        Le fichier publié est disponible dans la variable [!UICONTROL Bulksheets] affichez pendant 30 jours si vous l’avez publiée ou non sur le réseau publicitaire.

Le &quot;[!UICONTROL Last Prop. Status]&quot; affiche l’état de la tâche pour les modèles applicables.

Lorsque la feuille d’envoi groupé est créée, elle est répertoriée dans la [!UICONTROL Bulksheets] vue. Lorsque le fichier est publié, une notification par courrier électronique est envoyée avec un lien vers le fichier. Cependant, si l’ensemble ou une partie des données ne peuvent pas être publiées, un fichier d’erreur est répertorié dans la variable [!UICONTROL Bulksheets] et une notification électronique est envoyée avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>* Quelle que soit l’option de planification que vous avez sélectionnée, les données spécifiées sont supprimées de la variable [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] des listes.
>* Le traitement de grandes quantités de données prend plus de temps. Vous pouvez suivre la progression du fichier pendant le processus.
>* Toutes les données publiées sont soumises au processus éditorial du réseau.
>* Avant de publier un fichier de feuille d’envoi groupé, vous pouvez : [annuler la publication ;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Affichage des données générées à partir de flux](propagated-data-view.md)
>* [Modification des données générées à partir de flux](propagated-data-edit.md)
>* [Arrêt d’une tâche de publication pour les données de flux d’inventaire](stop-job.md)
>* [Statuts des données générées à partir de flux](propagated-data-status.md)
