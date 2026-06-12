---
title: (Nouvelle interface utilisateur) Gérer les flux de rapports de feuille de calcul
description: Découvrez comment créer, configurer, actualiser, afficher et supprimer des flux de rapports de feuille de calcul qui fournissent des données de performances quotidiennes dans une feuille de calcul au format personnalisé.
feature: Search Reports
source-git-commit: 38ee8dfbaf82d8f1d212a931956398444e61060f
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gérer les flux de rapports de feuille de calcul

*Pour les rapports de base et les rapports sur la précision des modèles uniquement*

<!-- Update link to notifications once available -->

Les flux de feuilles de calcul fournissent des données de performances quotidiennes pour tous les rapports de base et modélisent les rapports de précision au format de feuille de calcul personnalisé dans [!DNL Microsoft Excel] XLSX. Vous pouvez configurer des flux de feuilles de calcul à l&#39;aide de modèles de feuilles de calcul [!DNL Excel] spécialement formatés que vous créez à partir de modèles de rapport standard. Chaque jour, la feuille de calcul est automatiquement actualisée à une heure spécifiée avec de nouvelles données brutes qui sont agrégées quotidiennement. Les données brutes renseignent toutes les colonnes et tous les graphiques que vous avez inclus dans le modèle de feuille de calcul. Une fois qu’un fichier de flux de feuille de calcul est disponible ou si la génération du fichier échoue, chaque destinataire d’e-mail dans le modèle de rapport reçoit une notification, en fonction des [paramètres de notification pour les rapports](/help/search-social-commerce/notifications/notification-about.md) configurés par l’utilisateur.

Vous pouvez configurer le flux pour actualiser jusqu’aux 90 derniers jours de données et toutes les données existantes précédentes seront conservées, en continuant à s’accumuler.

La vue [!UICONTROL Reports] > [!UICONTROL Spreadsheets Feeds] répertorie tous les flux de feuille de calcul que vous avez créés. Cette vue vous permet de créer des flux de feuille de calcul, d’actualiser manuellement un flux ou de supprimer un flux.

## Actions disponibles

* [Création d [!DNL Excel] un modèle pour un flux de rapports de feuille de calcul](#spreadsheet-feed-create-excel-template)

* [Créer un flux de rapports de feuille de calcul](#spreadsheet-feed-create)

* [Modifier les paramètres du flux de rapports d&#39;une feuille de calcul](#spreadsheet-feed-edit)

* [Afficher ou enregistrer un fichier de flux de rapports de feuille de calcul](#spreadsheet-feed-view-or-save)

* [Actualiser manuellement les flux de rapports de feuille de calcul](#spreadsheet-feed-refresh)

* [Supprimer les flux de rapports de feuille de calcul](#spreadsheet-feed-delete)

## Créer un modèle de [!DNL Excel] pour un flux de rapports de feuille de calcul {#spreadsheet-feed-create-excel-template}

<!-- Add x-refs when available -->

Pour créer des flux de feuilles de calcul, vous devez d&#39;abord créer des modèles de feuilles de calcul [!DNL Microsoft Excel] spécialement formatés à l&#39;aide de modèles de rapport standard. Vous pouvez éventuellement personnaliser la feuille de calcul [!DNL Excel] pour inclure des colonnes et des graphiques supplémentaires.

1. Dans **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**, générez le type de rapport souhaité à l’aide d’une unité de [!UICONTROL Date Aggregation] de « [!UICONTROL Daily] » et de tous les autres paramètres de données souhaités, en enregistrant le rapport en tant que modèle.

   >[!NOTE]
   >
   > * Vous pouvez créer des flux de feuilles de calcul pour les rapports [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] et [!UICONTROL Forecast Accuracy]. Si vous utilisez l’[!UICONTROL Ad Group Report] , limitez le nombre de groupes publicitaires inclus pour obtenir des résultats plus rapides.
   > * L’unité de [!UICONTROL Date Range] définie dans le modèle n’est pas utilisée. Vous définissez les dates auxquelles les données seront actualisées lors de la configuration ultérieure du flux de la feuille de calcul.

1. Une fois le rapport généré, accédez à **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]** et exportez une version TSV ou XLS du rapport vers un fichier.

1. Dans [!DNL Excel], créez un modèle personnalisé pour le rapport :

   1. Ouvrez le fichier de rapport dans [!DNL Excel].

   1. Préparez le classeur :

      1. Supprimez les premières lignes qui affichent les paramètres du rapport. Pour les fichiers XLS, supprimez également la ligne « [!UICONTROL Total] ». Vous pouvez éventuellement supprimer certaines lignes de données, mais conservez a) la ligne d’en-tête de données avec toutes les colonnes dans l’ordre d’origine et b) au moins une ligne de données. Ne pas ajouter de données manuellement.

         >[!NOTE]
         >
         > La dernière colonne doit inclure des valeurs non nulles.

      1. Triez les données par date de début par ordre croissant (du plus ancien au plus récent).

      1. Remplacez le nom de l&#39;onglet de feuille de calcul de « [!UICONTROL Sheet1] » par « [!UICONTROL RAW] ».

         Ce nom d’onglet spécifique permet d’actualiser les données.

      1. (Facultatif) Ajoutez des colonnes personnalisées à droite des colonnes du modèle de rapport, si nécessaire.

   1. (Facultatif) Dans une feuille de calcul distincte, créez un tableau croisé dynamique. Une fois que vous avez terminé, cliquez avec le bouton droit de la souris dans n&#39;importe quelle cellule du tableau croisé dynamique et sélectionnez **[!UICONTROL Pivot Table Options]**, cliquez sur l&#39;onglet **[!UICONTROL Data]**, puis sélectionnez **[!UICONTROL Refresh data when opening the file]**.

   1. Enregistrez le fichier en tant que feuille de calcul [!DNL Excel] au format .XLSX.

## Créer un flux de rapports de feuille de calcul {#spreadsheet-feed-create}

1. [Créez le [!DNL Excel] modèle à remplir avec les données du rapport](#spreadsheet-feed-create-excel-template).

1. Créez le flux de la feuille de calcul :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create Spreadsheet]**.

   1. Dans la boîte de dialogue **[!UICONTROL Create Spreadsheet Feed]**, spécifiez les paramètres [flux de feuille de calcul](#spreadsheet-feed-settings).

   1. Cliquez sur **[!UICONTROL Submit]**.

   1. (Facultatif) Une fois le [!UICONTROL Update Status] du flux *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur.

      >[!NOTE]
      >
      >Si le modèle de rapport associé au flux est supprimé ultérieurement, le flux est également supprimé.

      Les flux de la feuille de calcul sont automatiquement actualisés chaque jour au [!UICONTROL Schedule Time] configuré. Si le modèle de rapport inclut des adresses pour des destinataires d’e-mails, ces adresses reçoivent des notifications lorsque la feuille de calcul est actualisée.

## Modifier les paramètres du flux de rapports d&#39;une feuille de calcul {#spreadsheet-feed-edit}

>[!NOTE]
>
> Si vous modifiez les colonnes du modèle de rapport ou utilisez un modèle de rapport nouveau ou mis à jour, vous devez mettre à jour le modèle de [!DNL Excel] en conséquence et le charger à nouveau.

1. (Facultatif) Pour mettre à jour le modèle de rapport ou le modèle de [!DNL Excel] utilisé pour le flux de feuille de calcul :

   * (Facultatif) Pour utiliser un modèle de rapport différent ou mis à jour pour le flux, [créez un nouveau modèle  [!DNL Excel]  modèle de rapport](#spreadsheet-feed-create-excel-template).

     Dans les étapes suivantes, vous allez charger à la fois le modèle de rapport et le nouveau fichier [!DNL Excel].

   * (Facultatif) Pour ajouter simplement des colonnes personnalisées au modèle de [!DNL Excel], insérez les colonnes à droite des colonnes du modèle de rapport, puis enregistrez le fichier en tant que feuille de calcul [!DNL Excel] au format .XLSX. Vous devrez charger le nouveau fichier [!DNL Excel] à l’étape suivante.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Modifiez les paramètres de flux de la feuille de calcul :

   1. Cochez la case en regard du nom du flux de feuille de calcul.

   1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

   1. Dans la boîte de dialogue [!UICONTROL Create Spreadsheet Feed]<!-- sic -->, modifiez les [paramètres de flux de feuille de calcul](#spreadsheet-feed-settings).

   1. Cliquez sur **[!UICONTROL Submit]**.

   1. (Facultatif) Une fois le [!UICONTROL Update Status] du flux *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur.

   >[!NOTE]
   >
   > Si le modèle de rapport associé au flux est supprimé ultérieurement, le flux est également supprimé.

   Les flux de feuilles de calcul sont automatiquement actualisés à 8 heures :00 chaque jour dans le fuseau horaire de l’annonceur. Si le modèle de rapport inclut des adresses pour des destinataires d’e-mails, ces adresses reçoivent des notifications lorsque la feuille de calcul est actualisée.

## Paramètres de flux de rapports des feuilles de calcul {#spreadsheet-feed-settings}

| Champ | Description |
|---|---|
| [!UICONTROL Feed Name] | Nom du flux de la feuille de calcul. |
| [!UICONTROL Report Template] | Modèle de rapport spécifiant les données de rapport requises. Sélectionnez celui que vous avez utilisé pour créer le modèle de [!DNL Excel]. Tous les modèles de rapport de base sont répertoriés.<br><br><b>Remarque :</b> si vous modifiez le modèle de rapport utilisé pour le rapport ou si vous mettez à jour les colonnes du modèle, vous devez créer et charger un nouveau modèle de [!DNL Excel]. |
| [!UICONTROL Excel Template] | Modèle de [!DNL Excel] spécialement formaté que vous avez créé au format .XLSX et qui est appliqué aux données spécifiées dans le modèle de rapport. Indiquez le fichier à charger en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur <b>[!UICONTROL Browse]</b> pour localiser le fichier sur votre appareil ou réseau. |
| [!UICONTROL Back Fill From] | Date de début pour laquelle les données existantes sur l’onglet [!UICONTROL RAW] sont actualisées, représentée par un nombre de jours dans le passé. Entrez une valeur allant jusqu’à 90 jours ; la valeur par défaut est de sept (7) jours.<br><br>Par exemple, si la valeur est 7 et que la date d’aujourd’hui est le 7 mars, les données existantes dans l’onglet [!UICONTROL RAW] commençant par le 1er mars sont actualisées (jusqu’à la date de fin spécifiée par le paramètre [!UICONTROL Back Fill Until] ). Les lignes de données existantes pour les dates antérieures au 1er mars ne sont pas supprimées, mais elles ne sont pas actualisées. |
| [!UICONTROL Back Fill Until] | Date de fin à laquelle les données existantes sur l’onglet [!UICONTROL RAW] sont actualisées, représentée par un nombre de jours dans le passé. La valeur par défaut est de un (1) jour.<br><br>Par exemple, si cette valeur est définie sur 1 et que la date d’aujourd’hui est le 7 mars, les données existantes dans l’onglet [!UICONTROL RAW] sont actualisées jusqu’au 6 mars (et en commençant par la date de début spécifiée par le paramètre [!UICONTROL Back Fill From] ). Si cette valeur est définie sur 1, le paramètre [!UICONTROL Back Fill Until] est défini sur 7 et que la valeur actuelle est le 7 mars, les données existantes dans l’onglet [!UICONTROL RAW] sont actualisées du 1er au 6 mars. Dans les deux exemples, les lignes de données existantes pour les dates postérieures au 6 mars ne sont pas supprimées, mais elles ne sont pas actualisées. |
| [!UICONTROL Email Recipients] | Adresses e-mail auxquelles envoyer des notifications chaque fois que le rapport est actualisé ou chaque fois que le rapport est exécuté lorsque le modèle inclut un planning. Par défaut, l’adresse de votre compte utilisateur est saisie. Pour spécifier plusieurs adresses, séparez-les par des virgules, des espaces ou de nouvelles lignes. |
| [!UICONTROL Schedule Time] | Heure à laquelle les flux de la feuille de calcul sont actualisés : soit à 08:00 soit à toute heure entre 10 :00 et 23 :00 dans le fuseau horaire de l’annonceur. La valeur par défaut pour les nouveaux flux de feuille de calcul est 10:00.<br><br><b>Remarque :</b> pour des raisons de performances, vous ne pouvez pas actualiser les flux de feuille de calcul à 09:00, lorsque d’autres rapports sont générés. |
| [!UICONTROL Email Notification] | (Lorsque les destinataires d’e-mails sont spécifiés) Éléments à inclure dans les notifications par e-mail aux adresses spécifiées :<ul><li><i>[!UICONTROL Attach feed]</i> — Pour envoyer une copie du rapport complété au format XLSX. Si le fichier dépasse 10 Mo, la notification n’inclut pas de pièce jointe.</li><li><i>[!UICONTROL Notification Only]</i> (valeur par défaut) : pour envoyer uniquement une notification de fin ou d&#39;échec du rapport, avec un lien vers le rapport.</li></ul> |

## Afficher ou enregistrer un fichier de flux de rapports de feuille de calcul {#spreadsheet-feed-view-or-save}

Vous pouvez afficher n’importe quel flux de feuille de calcul généré ou l’enregistrer dans un fichier. Les fichiers de flux des feuilles de calcul sont au format XLSX [!DNL Microsoft Excel].

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur.

## Actualiser manuellement les flux de rapports de feuille de calcul {#spreadsheet-feed-refresh}

>[!NOTE]
>
>Les flux de feuilles de calcul sont automatiquement actualisés à 8 :00 chaque jour dans le fuseau horaire local.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Cochez la case en regard de chaque flux à actualiser.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Run Spreadsheet]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

1. (Facultatif) Une fois la [!UICONTROL Update Status] d’un flux *[!UICONTROL Finished]*, cliquez sur **[!UICONTROL XLSX]** en regard du flux, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur.

## Supprimer les flux de rapports de feuille de calcul {#spreadsheet-feed-delete}

>[!NOTE]
>
>Si le modèle de rapport associé à un flux est supprimé, le flux est automatiquement supprimé.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Cochez la case en regard de chaque flux à supprimer.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.
