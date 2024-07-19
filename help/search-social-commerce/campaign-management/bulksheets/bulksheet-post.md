---
title: Publier des feuilles d’envoi groupées ou des fichiers d’erreur corrigés
description: Découvrez comment publier des fichiers de feuille d’envoi groupé sur vos réseaux publicitaires.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Publier des feuilles d’envoi groupées ou des fichiers d’erreur corrigés

Vous pouvez publier des fichiers de feuilles d’envoi groupées existants ou des fichiers d’erreur corrigés sur les comptes appropriés pour les [réseaux d’annonces pris en charge](bulksheet-about.md#bulksheet-functionality-by-network). Si le fichier est au format ZIP, il n’est pas nécessaire de le décompresser au préalable.

Les fichiers de feuilles d’envoi groupé et les fichiers d’erreur sont automatiquement supprimés 30 jours après leur téléchargement ou leur génération.

>[!NOTE]
>Vous pouvez également publier un fichier de feuille d’envoi groupé ou un fichier d’erreur lorsque vous chargez le fichier.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Cochez la case en regard de chaque fichier à publier.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Post]**.

1. Dans la boîte de dialogue, saisissez ou sélectionnez des informations dans les [[!UICONTROL Post Bulksheet] settings](#bulksheet-post-settings), puis cliquez sur **[!UICONTROL Post]**.

   Les mêmes paramètres s’appliquent à tous les fichiers que vous publiez.

Lorsque la tâche commence, l’état et la date de publication planifiée de la ligne sont modifiés dans la vue [!UICONTROL Bulksheets]. Lorsque le fichier est publié, une notification par courrier électronique est envoyée avec un lien vers le fichier. Selon la quantité de données compilées, la notification par email peut prendre plusieurs minutes ou plus. Toutefois, si aucune des données ne peut être publiée, un fichier d’erreur est répertorié sur la vue [!UICONTROL Bulksheets] et une notification par e-mail est envoyée avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>* La publication de grandes quantités de données prend plus de temps. Vous pouvez suivre la progression du fichier dans la colonne [!UICONTROL Progress] de la vue [!UICONTROL Bulksheets].
>* Toutes les données publiées sont soumises au processus éditorial du réseau.
* Avant de publier le fichier de feuille d’envoi groupé, vous pouvez annuler la publication.

## Paramètres de publication pour les feuilles d’envoi groupées et les fichiers d’erreur corrigés {#bulksheet-post-settings}

| Paramètre | Description |
|----|----|
| [!UICONTROL Account (Search Engine)] | Compte réseau publicitaire pour lequel les données sont publiées. Si vous publiez plusieurs fichiers simultanément ou un fichier qui s’applique à plusieurs comptes, la valeur est <i>Plusieurs comptes sélectionnés</i>.<br><br>La première lettre du nom du réseau publicitaire est entre parenthèses après le nom du compte (par exemple &quot;Acme Realty (G)&quot; pour un compte [!DNL Google Ads]). |
| [!UICONTROL Scheduling] | Quand publier le fichier sur le réseau publicitaire spécifié :<ul><li><i>[!UICONTROL Post to ad network now]</i> (valeur par défaut) : commence à publier les données immédiatement.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]] :</i> Commence à publier les données à la date et à l’heure spécifiées ; la valeur par défaut est demain à 02h00 (02h00). Pour modifier la date, saisissez une date au format JJ/MM/AAAA ou JJ/M/AAAA ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar.png "Calendrier") pour ouvrir le calendrier et [ sélectionnez une date](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Pour modifier l’heure, saisissez l’heure au format HH/MM ou H/M ou sélectionnez une heure (par intervalles de 15 minutes) dans la liste.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Inclure des modèles de suivi et des suffixes de page d’entrée (pour les réseaux publicitaires applicables) dans les comptes avec modèles de suivi, ou des URL de destination avec des codes de suivi incorporés dans les comptes avec des URL de destination, pour tous les mots-clés, annonces, emplacements, liens de site et [!DNL Google Ads] groupes de produits dans la publication : <i>[!UICONTROL Yes]</i> (valeur par défaut) ou <i>[!UICONTROL No]</i>. Peu importe que les unités d&#39;offre se trouvent dans un portefeuille.<br><br>Si vous sélectionnez <i>[!UICONTROL Yes]</i>, les URL sont générées en fonction des paramètres de la section [!UICONTROL Tracking Methods] des paramètres de compte ou des paramètres de campagne appropriés. Par défaut, s’il existe des URL de suivi, elles ne sont pas regénérées à moins que de nouvelles URL ne soient nécessaires (par exemple, si le type de correspondance du mot-clé, le texte de la publicité ou les paramètres de suivi pour les comptes concernés ont changé).<br><br>Si vous sélectionnez <i>[!UICONTROL No]</i>, vous pouvez toujours générer les URL de suivi ultérieurement en publiant manuellement le fichier chargé.<br><br><b>Remarque : </b> Si l’annonceur utilise le suivi de conversion d’Adobe Advertising et que l’URL de base a changé, vous devez générer de nouvelles URL de suivi, sauf si le compte est configuré pour générer et charger automatiquement les URL de suivi. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Permet de modifier le budget des campagnes dans des portfolios optimisés en fonction des données publiées. Par défaut, cette option n’est pas sélectionnée. Si vous sélectionnez cette option, toute modification du budget de la campagne spécifiée est applicable jusqu’à ce que la fonctionnalité d’optimisation détermine que le budget doit être réalloué (généralement au prochain cycle d’offre).<br><br><b>Remarque : </b> Toute modification budgétaire résultant des données publiées pour les campagnes dans des portefeuilles non optimisés se produit lorsque le fichier est publié. Les modifications s’affichent le lendemain dans les vues de gestion de campagne. |
| [!UICONTROL Enable bidding on ads within portfolios] | Lorsque les composants de campagne inclus se trouvent dans un portefeuille optimisé, cette fonctionnalité remplace la stratégie d’optimisation et permet de modifier les offres en fonction des données de la feuille d’envoi groupé jusqu’à une date de fin spécifiée. Si vous sélectionnez cette option, spécifiez une date de fin comprise entre 1 et 7 jours dans le champ **[!UICONTROL Hold bulksheet bids until]**. |

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](bulksheet-about.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](bulksheet-download.md)
>* [Télécharger des feuilles d’envoi groupées ou des fichiers d’erreur corrigés](bulksheet-upload.md)
>* [Valider les landing pages dans les fichiers de feuille d’envoi groupé](bulksheet-validate-landing-pages.md)
>* [Exporter un fichier de feuille d’envoi groupé généré ou téléchargé](bulksheet-export.md)
