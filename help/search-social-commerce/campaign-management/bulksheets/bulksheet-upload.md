---
title: Télécharger une feuille d’envoi groupé ou un fichier d’erreur corrigé
description: Découvrez comment charger manuellement un fichier de feuille d’envoi groupé ou un fichier d’erreur de validation de page d’entrée corrigé.
exl-id: 34843245-6c55-489c-8e04-f8bae4046ae4
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Télécharger une feuille d’envoi groupé ou un fichier d’erreur corrigé

Vous pouvez charger des fichiers de feuille d’envoi groupé, des fichiers d’erreur de validation de page d’entrée corrigés et d’autres fichiers d’erreur corrigés depuis votre périphérique ou réseau pour [réseaux publicitaires pris en charge](bulksheet-about.md#bulksheet-functionality-by-network). Toutes les colonnes personnalisées du fichier sont supprimées lorsque vous chargez le fichier.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Upload Bulksheet]**.

1. Saisissez ou sélectionnez des informations dans le [[!UICONTROL Upload Bulksheet] paramètres](#bulksheet-upload-settings).

1. Cliquez sur **[!UICONTROL Apply]**.

Lorsque la tâche démarre, le fichier est répertorié dans la variable [!UICONTROL Bulksheets] vue. Une fois le fichier terminé, une notification par e-mail est envoyée avec un lien vers le fichier. Selon la quantité de données compilées, la notification par email peut prendre plusieurs minutes ou plus. Toutefois, si la génération du fichier échoue, un fichier d’erreur est répertorié sur la variable [!UICONTROL Bulksheets] et une notification électronique est envoyée avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>Si vous publiez les données de la feuille d’envoi groupé sur le réseau publicitaire, vous pouvez suivre la progression du fichier dans la variable [!UICONTROL Progress] dans la colonne [!UICONTROL Bulksheets] vue. La publication de grandes quantités de données prend plus de temps.

## Chargement des paramètres des feuilles d’envoi groupées et des fichiers d’erreur corrigés {#bulksheet-upload-settings}

| Paramètre | Description |
|----|----|
| [!UICONTROL File to Upload] | Fichier à charger. Spécifiez le fichier en saisissant le chemin d’accès complet et le nom de fichier ou en cliquant sur <b>[!UICONTROL Browse]</b> pour localiser le fichier sur votre périphérique ou réseau.<br><br>Les fichiers de feuille d’envoi groupé peuvent atteindre 2,5 Go (environ 2,5 millions de lignes) et doivent avoir l’une des extensions de fichier suivantes : <i>[!UICONTROL .tsv]</i> (pour les valeurs séparées par des tabulations), <i>[!UICONTROL .txt]</i> (pour le texte ASCII compatible Unicode), <i>[!UICONTROL .csv]</i> (pour les valeurs séparées par des virgules) ou <i>[!UICONTROL .zip]</i> (pour le format ZIP compressé, qui décompresse le fichier vers un fichier TSV). Le nom de fichier ne peut pas contenir les caractères suivants : `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Conseil :</b> Pour les données contenant des caractères internationaux, utilisez des fichiers au format TSV ou TXT. |
| [!UICONTROL Single Account] | Si le fichier s’applique à un compte : <i>[!UICONTROL Yes]</i> (pour un compte) ou <i>[!UICONTROL No]</i>(pour plusieurs comptes). |
| [!UICONTROL Account (Search Engine)] | (Lorsque le fichier s’applique à un seul compte) Le compte auquel charger les données. |
| [!UICONTROL Search Engine] | (Lorsque le fichier s’applique à plusieurs comptes) Le réseau publicitaire auquel charger les données. |
| [!UICONTROL Scheduling] | Quand ou si publier le fichier sur le réseau publicitaire spécifié :<ul><li><i>[!UICONTROL Post to ad network now]</i> (valeur par défaut) : commence à publier les données immédiatement.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Commence à publier les données à la date et à l’heure spécifiées ; la valeur par défaut est demain à 02h00 (02h00). Pour modifier la date, saisissez une date au format JJ/MM/AAAA ou JJ/M/AAAA ou cliquez sur ![Calendrier](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md "Calendrier") pour ouvrir le calendrier et [sélectionner une date ;](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Pour modifier l’heure, saisissez l’heure au format HH/MM ou H/M ou sélectionnez une heure (par intervalles de 15 minutes) dans la liste.</li><li><i>[!UICONTROL Preview only]:</i> Pour charger le fichier dans Search, Social et Commerce sans publier les données sur le réseau publicitaire, vous pouvez tout de même publier le fichier ultérieurement. Si le fichier de feuille d’envoi groupé fait plus de 10 Mo mais moins de 2 Go, il est au format ZIP ; il n’est pas nécessaire de le décompresser pour le publier.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Inclure des modèles de suivi et des suffixes de landing page (pour les réseaux publicitaires applicables) dans les comptes avec des modèles de suivi ou des URL de destination avec des codes de suivi incorporés dans les comptes avec des URL de destination, pour tous les mots-clés, annonces, emplacements, liens de site et [!DNL Google Ads] groupes de produits dans la publication : <i>[!UICONTROL Yes]</i> (valeur par défaut) ou <i>[!UICONTROL No]</i>. Peu importe que les unités d&#39;offre se trouvent dans un portefeuille.<br><br>Si vous sélectionnez <i>[!UICONTROL Yes]</i>, les URL sont alors générées en fonction des paramètres de la variable [!UICONTROL Tracking Methods] de la section paramètres du compte ou paramètres de campagne appropriés. Par défaut, s’il existe des URL de suivi, elles ne sont pas regénérées à moins que de nouvelles URL ne soient nécessaires (par exemple, si le type de correspondance du mot-clé, le texte de la publicité ou les paramètres de suivi pour les comptes concernés ont changé).<br><br>Si vous sélectionnez <i>[!UICONTROL No]</i>, vous pouvez toujours générer les URL de suivi ultérieurement en publiant manuellement le fichier chargé.<br><br><b>Remarque :</b> Si l’annonceur utilise le suivi de conversion d’Adobe Advertising et que l’URL de base a changé, vous devez générer de nouvelles URL de suivi, sauf si le compte est configuré pour générer et charger automatiquement les URL de suivi. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permet de modifier le budget des campagnes dans des portfolios optimisés en fonction des données publiées. Par défaut, cette option n’est pas sélectionnée. Si vous sélectionnez cette option, toute modification du budget de la campagne spécifiée est applicable jusqu’à ce que la fonctionnalité d’optimisation détermine que le budget doit être réalloué (généralement au prochain cycle d’offre).<br><br><b>Remarque :</b> Toute modification du budget résultant des données publiées pour les campagnes dans des portefeuilles non optimisés se produit lorsque le fichier est publié. Les modifications s’affichent le lendemain dans les vues de gestion de campagne. |
| [!UICONTROL Enable bidding on ads within portfolios] | Lorsque les composants de campagne inclus se trouvent dans un portefeuille optimisé, cette fonctionnalité remplace la stratégie d’optimisation et permet de modifier les offres en fonction des données de la feuille d’envoi groupé jusqu’à une date de fin spécifiée. Si vous sélectionnez cette option, indiquez une date de fin comprise entre 1 et 7 jours dans la variable **[!UICONTROL Hold bulksheet bids until]** champ . |

>[!MORELIKETHIS]
>
>* [A propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](bulksheet-about.md)
>* [Téléchargement/création d’un fichier de feuille d’envoi groupé](bulksheet-download.md)
>* [Publier des feuilles d’envoi groupées ou des fichiers d’erreur corrigés](bulksheet-post.md)
>* [Validation des landing pages dans des fichiers de feuille d’envoi groupé](bulksheet-validate-landing-pages.md)
>* [Exportation d’un fichier de feuille d’envoi groupé généré ou transféré](bulksheet-export.md)
