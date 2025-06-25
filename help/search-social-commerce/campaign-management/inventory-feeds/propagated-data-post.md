---
title: Publier les données de campagne générées à partir des flux sur les réseaux publicitaires
description: Découvrez comment publier des données générées à partir de flux de données d’inventaire sur les réseaux publicitaires.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Publier les données de campagne générées à partir des flux sur les réseaux publicitaires

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Vous pouvez publier les données de campagne générées à partir d’un flux lorsque vous propagez les données par le biais des modèles associés ou dans le cadre d’un processus distinct. Une fois les données publiées, toutes les données propagées existantes sont supprimées des listes [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

Pour une publication réussie, tous les groupes d’annonces doivent être affectés aux campagnes, tous les mots-clés et toutes les annonces doivent être affectés aux groupes d’annonces, et toutes les informations requises doivent être incluses sans aucune violation de longueur.

* Si vous avez utilisé l’option « [!UICONTROL Propagate and Preview] », [publiez le fichier de feuille d’envoi groupé généré](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (nommé « `<feed file name>_<template name>` ») à partir de la vue [!UICONTROL Bulksheets].

  Si vous n’avez pas validé vos pages de destination [auparavant](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), vous pouvez le faire avant de publier le fichier.

* Si vous avez utilisé l’option « [!UICONTROL Propagate only] », vous pouvez publier les données générées pour les composants avec le statut [[!UICONTROL New] dans une vue de hiérarchie de campagne](propagated-data-status.md) à partir de l’onglet [!UICONTROL Templates] .

  >[!NOTE]
  >
  >Les composants actifs ou supprimés peuvent inclure de nouveaux sous-composants, qui peuvent être publiés si les données sont valides.

  >[!TIP]
  >
  >Si vous n’avez pas validé vos pages de destination précédemment et que vous souhaitez le faire, [propagez les données et prévisualisez-les](feed-data-propagate.md) à partir de la vue [!UICONTROL Bulksheets] au lieu de les publier sur le réseau publicitaire. Vous pouvez ensuite [valider les URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) avant de publier manuellement le fichier sur le réseau publicitaire.

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

   1. Cochez la case en regard du modèle.

   1. Dans la barre d’outils, cliquez sur **[!UICONTROL Post]**.

   1. Dans les paramètres de validation, saisissez ou sélectionnez des informations dans les champs, puis cliquez sur **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** quels composants de compte sont validés.

      * **[!UICONTROL Scheduling]:** Quand publier le fichier :

         * *[!UICONTROL Post to search engine now]* (valeur par défaut) : crée un fichier de feuille en bloc à partir des données de flux propagées et commence immédiatement à le publier.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* crée un fichier de feuille d’envoi groupé et le publie ultérieurement. Spécifiez les éléments suivants :

            * **[!UICONTROL Start Time]:** date et heure futures auxquelles le fichier de feuille d’envoi groupé doit être publié sur le réseau publicitaire. Par défaut, le fichier est envoyé à 00:00 (12:00) le jour suivant. **Remarque :** pour les fichiers volumineux qui nécessitent un traitement plus long, les données publiées ne sont pas disponibles immédiatement dans les vues de gestion de campagne ou dans le gestionnaire de publicités du réseau.

            * **[!UICONTROL End Time]:** date et heure futures auxquelles les publicités publiées peuvent être suspendues ou supprimées en fonction du [paramètre de données de flux](feed-settings-manage.md#feed-data-settings) pour « [!UICONTROL When the Scheduled End Date is reached] ». Par défaut, l’heure de fin est à 00:00 (12:00) dans 30 jours à partir d’aujourd’hui. Sélectionnez **[!UICONTROL None]** pour que les données restent actives indéfiniment (ou jusqu’à ce que vous propagiez de nouvelles données pour le modèle) ou spécifiez une date et une heure.

              Pour spécifier une date, utilisez le format JJ/MM/AAAA ou JJ/MM/AAAA ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar.png "Calendrier") pour ouvrir le calendrier et [sélectionner une date](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Pour modifier une heure, saisissez l’heure au format 24 heures HH/MM ou H/M ou sélectionnez une heure (par intervalles de 30 minutes) dans la liste.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** permet de créer un fichier de feuille en bloc disponible dans la vue [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets]. Vous pouvez éventuellement publier le fichier à partir de là.

           Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, le fichier est au format ZIP. Vous n’avez pas besoin de décompresser le fichier pour le publier.

      * **[!UICONTROL Generate Tracking URLs]:** Inclure ou non des URL de tracking pour les mots-clés et les variations d’annonces dans le fichier de feuille d’envoi groupé : *[!UICONTROL Yes]* (valeur par défaut) ou *[!UICONTROL No]*.

        Si vous sélectionnez *[!UICONTROL Yes]*, les URL sont générées à partir des URL de base des mots-clés et des annonces en fonction des paramètres [!UICONTROL Tracking Methods] dans le [paramètres du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) ou, si vous mappez des données à des campagnes existantes, aux paramètres [!UICONTROL Tracking Methods] dans les [paramètres de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) existants.

        S’il existe des URL de suivi pour les éléments pertinents, elles ne sont pas régénérées, sauf si de nouvelles URL sont nécessaires (par exemple, si le type de correspondance de mot-clé, le texte créatif ou les paramètres de suivi du compte ont changé).

      * **[!UICONTROL Bulksheet Name]:** nom du fichier de feuille d’envoi groupé à créer à partir des données de flux propagées. Par défaut, le fichier est nommé `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Vous pouvez renommer le fichier comme vous le souhaitez, mais il doit se terminer par l’une des extensions de fichier suivantes : `.tsv` (pour les valeurs séparées par des tabulations), `.txt` (pour le texte ASCII), `.csv` (pour les valeurs séparées par des virgules) ou `.zip` (pour un fichier TSV compressé). Pour les données qui incluent des caractères internationaux, utilisez le format TSV ou TXT.

        Le fichier publié est disponible dans la vue [!UICONTROL Bulksheets] pendant 30 jours, que vous le publiiez ou non sur le réseau publicitaire.

La colonne « [!UICONTROL Last Prop. Status] » indique le statut de la tâche pour les modèles applicables.

Lorsque la feuille d&#39;envoi groupé est créée, elle est répertoriée dans la vue [!UICONTROL Bulksheets]. Lorsque le fichier est publié, une notification par e-mail est envoyée avec un lien vers le fichier. Cependant, si la totalité ou une partie des données ne peut pas être publiée, un fichier d’erreur est répertorié dans la vue [!UICONTROL Bulksheets] et une notification par e-mail est envoyée avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>* Quelle que soit l’option de planification sélectionnée, les données spécifiées sont supprimées des listes [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].
>* Le traitement de grandes quantités de données prend plus de temps. Vous pouvez suivre la progression du fichier au cours du processus.
>* Toutes les données publiées sont soumises au processus éditorial du réseau.
>* Avant la validation d&#39;un fichier de feuille d&#39;envoi groupé, vous pouvez [annuler la validation](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Afficher les données générées à partir des flux](propagated-data-view.md)
>* [Modifier les données générées à partir des flux](propagated-data-edit.md)
>* [Arrêter un traitement de validation des données de flux de stock](stop-job.md)
>* [États des données générées à partir des flux](propagated-data-status.md)
