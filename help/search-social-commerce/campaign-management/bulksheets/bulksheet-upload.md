---
title: Charger une feuille d’envoi groupé ou un fichier d’erreur corrigé
description: Découvrez comment charger manuellement un fichier de feuille d’envoi groupé ou un fichier d’erreur de validation de page de destination corrigé.
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Charger une feuille d’envoi groupé ou un fichier d’erreur corrigé

Vous pouvez charger des fichiers de feuilles d’envoi groupé, des fichiers d’erreur de validation de page de destination corrigés et d’autres fichiers d’erreur corrigés depuis votre appareil ou réseau pour les [réseaux publicitaires pris en charge](bulksheet-about.md#bulksheet-functionality-by-network). Toutes les colonnes personnalisées du fichier sont supprimées lorsque vous chargez le fichier.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Upload Bulksheet]**.

1. Saisissez ou sélectionnez des informations dans les paramètres de [[!UICONTROL Upload Bulksheet]](#bulksheet-upload-settings).

1. Cliquez sur **[!UICONTROL Apply]**.

Lorsque la tâche commence, le fichier est répertorié dans la vue [!UICONTROL Bulksheets]. Une fois le fichier terminé, une notification par e-mail est envoyée avec un lien vers le fichier. Selon la quantité de données compilées, la notification par e-mail peut prendre plusieurs minutes ou plus. Cependant, si la génération du fichier échoue, un fichier d’erreur est répertorié dans la vue [!UICONTROL Bulksheets] et une notification est envoyée par e-mail avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>Si vous publiez les données des feuilles d&#39;envoi groupé sur le réseau publicitaire, vous pouvez suivre la progression du fichier dans la colonne [!UICONTROL Progress] de la vue [!UICONTROL Bulksheets]. La publication de grandes quantités de données prend plus de temps.

## Paramètres de chargement des feuilles d’envoi groupé et des fichiers d’erreur corrigés {#bulksheet-upload-settings}

| Paramètre | Description |
|----|----|
| [!UICONTROL File to Upload] | Le fichier à charger. Spécifiez le fichier en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur <b>[!UICONTROL Browse]</b> pour localiser le fichier sur votre appareil ou réseau.<br><br>Les fichiers de feuilles d’envoi groupé peuvent contenir jusqu’à 2,5 Go (environ 2,5 millions de lignes) et doivent avoir l’une des extensions de fichier suivantes : <i>[!UICONTROL .tsv]</i> (pour les valeurs séparées par des tabulations), <i>[!UICONTROL .txt]</i> (pour le texte ASCII compatible avec Unicode), <i>[!UICONTROL .csv]</i> (pour les valeurs séparées par des virgules) ou <i>[!UICONTROL .zip]</i> (pour le format ZIP compressé, qui est décompressé en fichier TSV). Le nom du fichier ne peut pas contenir les caractères suivants : `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Conseil :</b> pour les données contenant des caractères internationaux, utilisez des fichiers au format TSV ou TXT. |
| [!UICONTROL Single Account] | Si le fichier s’applique à un compte : <i>[!UICONTROL Yes]</i> (pour un compte) ou <i>[!UICONTROL No]</i> (pour plusieurs comptes). |
| [!UICONTROL Account (Search Engine)] | (Lorsque le fichier s’applique à un seul compte) Compte sur lequel charger les données. |
| [!UICONTROL Search Engine] | (Lorsque le fichier s’applique à plusieurs comptes) Réseau publicitaire sur lequel les données doivent être chargées. |
| [!UICONTROL Scheduling] | Quand ou si le fichier doit être publié sur le réseau publicitaire spécifié :<ul><li><i>[!UICONTROL Post to ad network now]</i> (valeur par défaut) : commence à publier immédiatement les données.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Commence à publier les données à la date et à l’heure spécifiées ; la valeur par défaut est demain à 02:00 (2 h). Pour modifier la date, saisissez une date au format JJ/MM/AAAA ou JJ/MM/AAAA ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar.png "Calendrier") pour ouvrir le calendrier et [sélectionner une date](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Pour modifier l’heure, saisissez l’heure au format HH/MM ou H/M ou sélectionnez une heure (par intervalles de 15 minutes) dans la liste.</li><li><i>[!UICONTROL Preview only] :</i> pour charger le fichier dans Search, Social et Commerce sans publier les données sur le réseau publicitaire ; vous pourrez toujours publier le fichier ultérieurement. Lorsque le fichier de feuille d’envoi groupé fait plus de 10 Mo, mais moins de 2 Go, le fichier est au format ZIP ; il n’est pas nécessaire de décompresser le fichier pour le publier.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Indique s’il faut inclure des modèles de suivi et des suffixes de page de destination (pour les réseaux publicitaires applicables) dans les comptes avec modèles de suivi, ou des URL de destination avec codes de suivi incorporés dans les comptes avec URL de destination, pour tous les mots-clés, annonces, emplacements, liens de site et groupes de produits [!DNL Google Ads] dans la publication : <i>[!UICONTROL Yes]</i> (par défaut) ou <i>[!UICONTROL No]</i>. Peu importe si les unités de soumission se trouvent dans un portefeuille.<br><br>Si vous sélectionnez <i>[!UICONTROL Yes]</i>, les URL sont générées en fonction des paramètres de la section [!UICONTROL Tracking Methods] des paramètres du compte ou des paramètres de campagne appropriés. Par défaut, si des URL de tracking existent, elles ne sont pas régénérées, sauf si de nouvelles URL sont nécessaires (par exemple, si le type de correspondance de mot-clé, le texte de l’annonce ou les paramètres de tracking pour les comptes concernés ont changé).<br><br>Si vous sélectionnez <i>[!UICONTROL No]</i>, vous pouvez toujours générer des URL de tracking ultérieurement en publiant manuellement le fichier chargé.<br><br><b>Remarque :</b> si l’annonceur utilise le suivi des conversions Adobe Advertising et que l’URL de base a changé, vous devez générer de nouvelles URL de suivi, sauf si le compte est configuré pour générer et charger automatiquement des URL de suivi. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Autorise les modifications de budget apportées aux campagnes dans des portfolios optimisés en fonction des données publiées. Par défaut, cette option n’est pas sélectionnée. Si vous sélectionnez cette option, les modifications du budget de campagne spécifiées sont applicables jusqu&#39;à ce que la fonctionnalité d&#39;optimisation détermine que le budget doit être réaffecté (généralement lors du prochain cycle d&#39;enchères).<br><br><b>Remarque :</b> toute modification de budget résultant des données validées pour des campagnes dans des portefeuilles non optimisés se produit lorsque le fichier est validé. Les modifications apparaissent dans les vues de gestion de campagne le lendemain. |
| [!UICONTROL Enable bidding on ads within portfolios] | Lorsque les composants de campagne inclus se trouvent dans un portfolio optimisé, cette fonctionnalité remplace la stratégie d’optimisation et permet de modifier les enchères en fonction des données de la feuille d’envoi groupé jusqu’à une date de fin spécifiée. Si vous sélectionnez cette option, indiquez une date de fin comprise entre 1 et 7 jours dans le champ **[!UICONTROL Hold bulksheet bids until]** . |

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l&#39;aide de feuilles d&#39;envoi groupé](bulksheet-about.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](bulksheet-download.md)
>* [Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](bulksheet-post.md)
>* [Valider les pages de destination dans les fichiers de feuille d’envoi groupé](bulksheet-validate-landing-pages.md)
>* [Exporter un fichier de feuille d’envoi groupé généré ou chargé](bulksheet-export.md)
