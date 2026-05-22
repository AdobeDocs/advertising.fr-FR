---
title: Gestion des rapports planifiés
description: Découvrez comment gérer les rapports planifiés.
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# Gestion des rapports planifiés

Les rapports de performance vous permettent de suivre et de gérer les performances de vos portefeuilles, réseaux publicitaires et entités de compte réseau publicitaire avec le niveau de granularité souhaité. La plupart des rapports offrent une visibilité complète sur la manière dont les annonces publicitaires de chaque canal marketing contribuent au taux de conversion global.

Les données d’un rapport sont compilées dynamiquement à chaque exécution du rapport. Vous avez la possibilité de générer un nouveau rapport à partir d’un rapport existant. Les paramètres de rapport disponibles varient selon le type de rapport. Pour la plupart des rapports, vous avez la possibilité de prévisualiser les 50 premières lignes au lieu de générer le rapport entier. Lorsque vous générez un rapport, vous pouvez envoyer une notification avec des liens de téléchargement à une ou plusieurs adresses e-mail lorsqu’un rapport est terminé. Les destinataires peuvent [gérer les notifications dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Tous les rapports terminés sont disponibles dans la section [!UICONTROL Latest Reports] de la vue [!UICONTROL Reports]. Vous pouvez soit les afficher sous forme de tableau dans la fenêtre du navigateur, soit les ouvrir ou les télécharger sous forme de fichiers.

## Catégories de rapports disponibles

Les catégories de rapports suivantes sont disponibles à partir de la vue [!UICONTROL Reports]. Il se peut que vous n’ayez pas accès à tous ces rapports. Les rapports disponibles et les données qu’ils génèrent sont déterminés par votre rôle et par la configuration de votre compte client.

| Catégorie de rapport | Description |
| ----| ---- |
| [!UICONTROL Basic Reports] | Les [rapports de base](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) disponibles pour tous les utilisateurs, affichent le coût réel et les données relatives aux clics pour les portfolios, les comptes de réseau publicitaire, les comptes de réseau publicitaire spécifiques, les campagnes, les groupes publicitaires, les annonces, les mots-clés, les groupes de produits, les classifications d’étiquettes et les valeurs d’étiquettes, les contraintes d’unité d’offre et les contraintes réseau. Elles sont basées sur les clics facturés par les réseaux publicitaires applicables et peuvent éventuellement inclure des données de conversion ou toute autre mesure que vous créez. |
| [!UICONTROL Advanced Reports] | Les [rapports avancés](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) fournissent des insight supplémentaires dans votre configuration publicitaire, ce qui vous permet d’identifier les endroits où il serait bénéfique de modifier votre ciblage géographique ou vos paramètres réseau. Ils peuvent également vous aider à valider les données de conversion dans les vues et rapports de gestion de campagne et de portefeuille par rapport aux données de suivi de conversion internes de l’annonceur. |
| [!UICONTROL Assist Reports] | [Les rapports d’assistance](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) fournissent des informations sur les chemins de conversion de tous les mots-clés et publicités d’un annonceur. Ils utilisent des données capturées par le biais du service de suivi des conversions d’Adobe Advertising et ne peuvent être générés que pour les annonceurs qui utilisent le service. |
| [!UICONTROL Specialty Reports] | Les [rapports spécialisés](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) sont constitués de données collectées par les réseaux publicitaires (plutôt que par le suivi Adobe Advertising). |
| [!UICONTROL Model Accuracy Reports] | [Rapports sur la précision des modèles](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) indiquez la précision des modèles de coût et de chiffre d’affaires utilisés pour optimiser les offres, les budgets de campagne et les cibles de stratégie d’offre pour un portefeuille. |

## Automatisation des rapports

Planifiez la génération automatique de rapports personnalisés de l’une des façons suivantes, ou des deux :

* Générez automatiquement des rapports chaque jour, ou un jour spécifique de la semaine ou du mois, à l’aide de [&#x200B; modèles de rapport &#x200B;](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Vous pouvez éventuellement paramétrer la diffusion [FTP) de rapports de base et avancés](/help/search-social-commerce/new-ui/reports/ftp-reports.md) qui utilisent un modèle.

* Continuez à actualiser vos modèles de feuilles de calcul personnalisés avec les données de performances quotidiennes à l’aide des [flux de feuilles de calcul](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## Les vues [!UICONTROL Scheduled Reports]

Les vues [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] vous permettent de créer et de gérer des rapports et des modèles de rapport :

* L’onglet **[!UICONTROL Latest Reports]** répertorie tous les rapports disponibles<!-- Doesn't seem to be true: that were requested in the last seven days --> à l’exception de ceux qui ont été supprimés manuellement, le rapport le plus récent étant en haut par défaut. Les informations affichées pour chaque rapport incluent le planning de son exécution (le cas échéant), les dates de début et de fin pour lesquelles des données ont été ou seront générées, l’auteur du rapport et le statut du rapport (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* ou *[!UICONTROL Error]*).

  Les liens en regard de chaque rapport vous permettent d’ouvrir ou d’enregistrer le rapport sous la forme d’un classeur [!DNL Microsoft Excel] (XLS), d’un fichier de valeurs séparées par des tabulations (TSV) ou d’un fichier de valeurs séparées par des virgules (CSV). Certains types de rapports peuvent également être enregistrés en tant que classeurs [!UICONTROL Excel] avec une feuille de calcul distincte pour chaque campagne applicable.

  Dans cet onglet, vous pouvez également créer un nouveau rapport (qui peut éventuellement être utilisé comme modèle), créer un nouveau rapport basé sur les paramètres d&#39;un rapport existant ou à l&#39;aide d&#39;un modèle de rapport, annuler les rapports en cours disponibles en les supprimant et supprimer tout rapport terminé disponible.

* L’onglet **[!UICONTROL Templates]** répertorie tous les modèles de rapport de base et avancés enregistrés disponibles, y compris des informations sur les plannings qui leur sont associés. Par défaut, le modèle le plus récent se trouve en haut de l’écran.

  À partir de cet onglet, vous pouvez créer un modèle, modifier tout modèle que vous avez créé (y compris ajouter, modifier ou supprimer son planning), générer un rapport à partir d’un modèle et supprimer tout modèle disponible.

## Utilisation des rapports

| Objectif | Rapport |
| ---- | ---- |
| Surveillance des performances | <ul><li>[Le [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[Le [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[Le [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[Le [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[Le [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[Le [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Dépannage des performances et analyse des tendances | <ul><li>[Le [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[Le [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[Le [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[Le [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[Le [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) et [Le [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Tout rapport de base qui compare deux fenêtres temporelles à l’aide de la fonction « [!UICONTROL Compare with] »</li></ul> |
| Identifier les opportunités de croissance commerciale | <ul><li>(Annonceurs avec suivi des conversions Adobe Advertising uniquement) [Le [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Annonceurs avec suivi des conversions Adobe Advertising uniquement) [Le [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Annonceurs avec [&#x200B; [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Rapports personnalisés dans Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Annonceurs avec suivi des conversions Adobe Advertising uniquement) [Le [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Annonceurs avec [&#x200B; [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Rapports personnalisés dans Adobe Analytics Analysis Workspace</li></ul> |

## Génération de rapports

### Générer un nouveau rapport

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Cliquez sur **[!UICONTROL Create Report]**, cliquez sur la catégorie de rapport dans le panneau de gauche, puis sélectionnez le type de rapport.<!-- Add link to list of report categories and report types --> Cliquez sur **[!UICONTROL Proceed]**.

1. (Facultatif) Dans la fenêtre [!UICONTROL Create Report], modifiez les paramètres de rapport par défaut pour [rapports de base et avancés](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [rapports d’assistance](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [rapports sur la précision des modèles](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) et [rapports spécialisés](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md) :

   1. (Facultatif) Saisissez un nom personnalisé pour l’état et pour le modèle (si vous enregistrez l’état en tant que modèle).

   1. (Facultatif) Pour enregistrer les paramètres du rapport en tant que modèle, activez le paramètre **[!UICONTROL Save as template]**.

   1. (Facultatif) Sélectionnez un **[!UICONTROL Type]** de rapport différent dans la même catégorie de rapport.

   1. (Facultatif) Dans l’onglet **[!UICONTROL Basic Settings]** , sélectionnez un modèle de rapport existant à utiliser ou modifiez les paramètres de base par défaut pour le rapport.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Columns]** et modifiez les colonnes par défaut du rapport, y compris l’ordre des colonnes.

      Par défaut, toutes les données monétaires des rapports sont présentées en dollars américains (par exemple 1 000,00). Pour afficher la valeur au format de devise approprié (mais sans aucun symbole de devise aux formats CSV et TSV), ajoutez la colonne « [!UICONTROL Currency] » au rapport. Si le rapport inclut des données pour des comptes avec différentes devises, les valeurs monétaires « [!UICONTROL Total] » sont la somme de tous les nombres de la colonne, quelle que soit la devise.

   1. (Certains types de rapports, facultatif) Cliquez sur l’onglet **[!UICONTROL Filters & Attribution]** ou **[!UICONTROL Filters]** et ajoutez des filtres de données. (Certains types de rapports) Limitez les résultats du rapport pour n’inclure que des classifications d’étiquettes spécifiques et modifiez les paramètres d’attribution par défaut de la règle d’attribution et de la conversion.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Scheduling]** et modifiez les options de planification et de diffusion par défaut.

1. Cliquez sur **[!UICONTROL Create]**.

Si vous n&#39;avez pas spécifié de planning de rapport, le rapport est exécuté immédiatement ; dans le cas contraire, il l&#39;est selon le planning spécifié. Le nom du rapport est ajouté à la vue [&#128279;](/help/search-social-commerce/reports/report-about.md). [!UICONTROL Latest Reports]Si vous avez enregistré le rapport en tant que modèle, il est également ajouté à la vue [[!UICONTROL Templates]. &#x200B;](/help/search-social-commerce/reports/report-about.md). Une fois le rapport terminé, vous pouvez ouvrir ou enregistrer le fichier ; les modèles sont disponibles immédiatement.

Si vous avez saisi des adresses e-mail pour la notification, chaque destinataire reçoit une notification lorsque la tâche de rapport est terminée ou échoue, en fonction des [paramètres de notification configurés](/help/search-social-commerce/notifications/notification-edit.md) de l’utilisateur pour les rapports.

### Générer un rapport à partir d&#39;un rapport existant

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]** pour ouvrir l’onglet **[!UICONTROL Latest Reports]** .

1. Effectuez l’une des opérations suivantes :

   * Placez le curseur sur la ligne du rapport, puis cliquez sur **...** > **[!UICONTROL Duplicate]**.

   * Cochez la case en regard du rapport. Dans la barre d’outils des actions en bloc, cliquez sur [Dupliquer](/help/search-social-commerce/assets/duplicate.png "Dupliquer").

1. Modifiez les paramètres du rapport si nécessaire.

1. Cliquez sur **[!UICONTROL Create]**.

### Générer un rapport à partir d&#39;un modèle existant

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Effectuez l’une des opérations suivantes :

   * Placez le curseur sur la ligne de modèle, puis cliquez sur **...** > **[!UICONTROL Duplicate]**.

   * Cochez la case en regard du modèle existant. Dans la barre d’outils des actions en bloc, cliquez sur [Dupliquer](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**.

1. (Facultatif) Renommez le modèle et modifiez les paramètres du rapport si nécessaire.

   Cliquez sur **[!UICONTROL Next]** pour vous déplacer entre les sections de paramètre.

1. Activez le paramètre **[!UICONTROL Save as Template]** .

1. Cliquez sur **[!UICONTROL Create]**.

## Prévisualiser ou enregistrer un rapport

Vous pouvez prévisualiser un rapport dans le navigateur web ou ouvrir ou enregistrer les données du rapport sous la forme d’un classeur [!DNL Microsoft Excel], d’un fichier de valeurs séparées par des tabulations (TSV), d’un fichier de valeurs séparées par des virgules (CSV) ou (pour certains types de rapports) d’un classeur à onglets [!DNL Microsoft Excel].

>[!NOTE]
>
>Les membres de l’équipe du compte Adobe et certains utilisateurs administrateurs peuvent afficher les rapports créés par les utilisateurs de l’annonceur et de l’agence.

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]** pour ouvrir l’onglet **[!UICONTROL Latest Reports]** .

1. Effectuez l’une des opérations suivantes :

   * (Pour afficher un rapport dans le navigateur web) Effectuez l’une des opérations suivantes :

      * Placez le curseur sur la ligne de modèle, puis cliquez sur **...** > **[!UICONTROL Preview]**.

      * Cochez la case en regard du modèle existant. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Preview]**.

   * (Pour ouvrir ou enregistrer les données du rapport dans un fichier) Dans la colonne [!UICONTROL Export] en regard du nom du rapport, cliquez sur le nom d’un format, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur :

      * **[!UICONTROL XLS]:** pour un classeur [!DNL Excel] avec une seule feuille de calcul (format XLSX). Le rapport comprend une feuille de calcul intitulée en haut avec les paramètres, avec une ligne pour chaque composant signalé lorsque des données sont disponibles pour le composant. Les lignes sans données sont omises.

        Les rapports de base incluent un total pour chaque colonne numérique.

      * **[!UICONTROL TSV]:** pour un fichier TSV. Le rapport comprend les paramètres et une ligne pour chaque composant signalé.

      * **[!UICONTROL CSV]:** pour un fichier CSV. Le rapport comprend les paramètres et une ligne pour chaque composant signalé.

## Supprimer des rapports

1. Dans le menu principal, cliquez sur **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]** pour ouvrir l’onglet **[!UICONTROL Latest Reports]** .

1. Effectuez l’une des opérations suivantes :

   * (Pour supprimer un seul rapport) :

      1. Placez le curseur sur la ligne du rapport, puis cliquez sur **...** > **[!UICONTROL Run]**.

      1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

   * (Pour supprimer un ou plusieurs rapports) :

      1. Cochez la case en regard de chaque rapport à supprimer.

      1. Dans la barre d’outils des actions en bloc, cliquez sur [Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") **[!UICONTROL Delete]**.

      1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
