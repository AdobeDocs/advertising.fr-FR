---
title: (Nouvelle interface utilisateur) Charger une feuille d’envoi groupé ou un fichier d’erreur corrigé
description: Découvrez comment charger manuellement un fichier de feuille d’envoi groupé ou un fichier d’erreur de validation de page de destination corrigé dans la nouvelle interface utilisateur de Search, Social et Commerce.
feature: Search Bulksheets
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e58024d1-d6da-420c-80af-6be211808316
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 38fd7ff63b177f13bdfb19b980fb1d1e14edcf56
workflow-type: tm+mt
source-wordcount: 830
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Charger une feuille d’envoi groupé ou un fichier d’erreur corrigé

Vous pouvez charger des fichiers de feuilles d’envoi groupé, des fichiers d’erreur de validation de page de destination corrigés et d’autres fichiers d’erreur corrigés depuis votre appareil ou réseau pour les [réseaux publicitaires pris en charge](about.md#bulksheet-functionality-by-network). Toutes les colonnes personnalisées du fichier sont supprimées lorsque vous chargez le fichier.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Dans la barre d’outils, cliquez sur **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Upload Bulksheet]**.

1. Saisissez ou sélectionnez des informations dans les paramètres de [&#128279;](#bulksheet-upload-settings).[!UICONTROL Upload Bulksheet]

1. Cliquez sur **[!UICONTROL Upload]**.

Lorsque la tâche commence, le fichier est répertorié dans la vue [!UICONTROL Bulksheets]. Lorsque les notifications par e-mail des feuilles d’envoi groupé sont [&#x200B; activées dans [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications/notification-manage.md), une notification par e-mail est envoyée avec un lien vers le fichier une fois le traitement terminé. Selon la quantité de données compilées, la notification par e-mail peut prendre plusieurs minutes ou plus. Si la génération du fichier échoue, un fichier d’erreur est répertorié dans la vue [!UICONTROL Bulksheets] et une notification est envoyée par e-mail avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>Si vous publiez les données des feuilles d&#39;envoi groupé sur le réseau publicitaire, vous pouvez suivre la progression du fichier dans la colonne [!UICONTROL Progress] de la vue [!UICONTROL Bulksheets]. La publication de grandes quantités de données prend plus de temps.

## Paramètres de chargement des feuilles d’envoi groupé et des fichiers d’erreur corrigés {#bulksheet-upload-settings}

| Paramètre | Description |
|----|----|
| [!UICONTROL File to Upload] | Le fichier à charger. Spécifiez le fichier en cliquant sur **[!UICONTROL Choose File]** pour le localiser sur votre appareil ou réseau.<br><br>Les fichiers de feuilles d’envoi groupé peuvent contenir jusqu’à 2,5 Go (environ 2,5 millions de lignes) et doivent avoir l’une des extensions de fichier suivantes : *[!UICONTROL .tsv]* (pour les valeurs séparées par des tabulations), *[!UICONTROL .txt]* (pour le texte ASCII compatible avec Unicode), *[!UICONTROL .csv]* (pour les valeurs séparées par des virgules) ou *[!UICONTROL .zip]* (pour le format ZIP compressé, qui est décompressé en fichier TSV). Le nom du fichier ne peut pas contenir les caractères suivants : `# % & * \| \ : " < > . ? /`<br><br>**Conseil :** pour les données contenant des caractères internationaux, utilisez des fichiers au format TSV ou TXT. |
| [!UICONTROL Single Account] | Si le fichier s’applique à un compte : *[!UICONTROL Yes]* (pour un compte) ou *[!UICONTROL No]* (pour plusieurs comptes). |
| [!UICONTROL Account (Search Engine)] | (Lorsque le fichier s’applique à un seul compte) Compte sur lequel charger les données. |
| [!UICONTROL Search Engine] | (Lorsque le fichier s’applique à plusieurs comptes) Réseau publicitaire sur lequel télécharger les données.<br><br>**Remarque :** les modifications d’enchères pour les mots-clés des portfolios optimisés ne sont pas prises en charge avec les feuilles d’envoi groupé à comptes multiples. |
| [!UICONTROL Scheduling] | Quand ou si le fichier doit être publié sur le réseau publicitaire spécifié :<ul><li>*[!UICONTROL Post to search engine now]* (valeur par défaut) : commence à publier immédiatement les données.</li><li>*[!UICONTROL Post to search engine on \[specified date\] \[specified time\]]:* Commence à publier les données à la date et à l’heure spécifiées ; la valeur par défaut est demain à 02 :00 (2 heures). Pour modifier la date, saisissez une date au format JJ/MM/AAAA ou cliquez sur l’icône de calendrier pour ouvrir le calendrier et sélectionner une date. Pour modifier l’heure, sélectionnez une heure (par intervalles de 15 minutes) dans la liste.</li><li>*[!UICONTROL Preview only]:* télécharge le fichier dans Search, Social et Commerce sans publier les données sur le réseau publicitaire ; vous pourrez toujours publier le fichier ultérieurement. Lorsque le fichier de feuille d’envoi groupé fait plus de 10 Mo, mais moins de 2 Go, le fichier est au format ZIP ; il n’est pas nécessaire de décompresser le fichier pour le publier.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Indique s’il faut inclure des modèles de suivi et des suffixes de page de destination (pour les réseaux publicitaires applicables) dans les comptes avec modèles de suivi, ou des URL de destination avec codes de suivi incorporés dans les comptes avec URL de destination, pour tous les mots-clés, annonces, emplacements, liens de site et groupes de produits [!DNL Google Ads] dans la publication : *[!UICONTROL Yes]* (par défaut) ou *[!UICONTROL No]*. Peu importe si les unités de soumission se trouvent dans un portefeuille.<br><br>Si vous sélectionnez *[!UICONTROL Yes]*, les URL sont générées en fonction des paramètres de la section [!UICONTROL Tracking Methods] des paramètres du compte ou des paramètres de campagne appropriés. Par défaut, si des URL de tracking existent, elles ne sont pas régénérées, sauf si de nouvelles URL sont nécessaires (par exemple, si le type de correspondance de mot-clé, le texte de l’annonce ou les paramètres de tracking pour les comptes concernés ont changé).<br><br>Si vous sélectionnez *[!UICONTROL No]*, vous pouvez toujours générer des URL de tracking ultérieurement en publiant manuellement le fichier chargé.<br><br>**Remarque :** Si l’annonceur utilise le tracking des conversions Adobe Advertising et que l’URL de base a changé, vous devez générer de nouvelles URL de tracking, sauf si le compte est configuré pour générer et charger automatiquement des URL de tracking. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Disponible si [!UICONTROL Generate Tracking URLs] est *[!UICONTROL Yes]*) Remplace tout suivi Adobe Advertising existant dans les URL du fichier chargé par un suivi nouvellement généré. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Autorise les modifications de budget apportées aux campagnes dans des portfolios optimisés en fonction des données publiées. Par défaut, cette option n’est pas sélectionnée. Si vous sélectionnez cette option, les modifications du budget de la campagne spécifiées sont applicables jusqu&#39;à ce que la fonctionnalité d&#39;optimisation détermine que le budget doit être réaffecté (généralement lors du prochain cycle d&#39;enchères).<br><br>**Remarque :** toute modification du budget résultant des données validées pour les campagnes dans des portefeuilles non optimisés se produit lorsque le fichier est validé. Les modifications apparaissent dans les vues de gestion de campagne le lendemain. |
| [!UICONTROL Enable bidding on ads within portfolios] | Lorsque les composants de campagne inclus se trouvent dans un portfolio optimisé, cette fonctionnalité remplace la stratégie d’optimisation et permet de modifier les enchères en fonction des données de la feuille d’envoi groupé jusqu’à une date de fin spécifiée. Si vous sélectionnez cette option, spécifiez une date de fin comprise entre 1 et 7 jours dans le champ **[!UICONTROL Hold bulksheet bids until]** . |

>[!MORELIKETHIS]
>
>* [&#x200B; (nouvelle interface utilisateur) À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupé](about.md)
>* [(nouvelle interface utilisateur) Télécharger/créer un fichier de feuille d’envoi groupé](download.md)
>* [(Nouvelle interface utilisateur) Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](post.md)
>* [(nouvelle interface utilisateur) Valider les pages de destination dans des fichiers de feuille d’envoi groupé](validate-landing-pages.md)
