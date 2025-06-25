---
title: Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés
description: Découvrez comment publier des fichiers de feuilles d’envoi groupé sur vos réseaux publicitaires.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés

Vous pouvez publier des fichiers de feuilles d&#39;envoi groupé existants ou des fichiers d&#39;erreur corrigés sur les comptes appropriés pour [réseaux publicitaires pris en charge](bulksheet-about.md#bulksheet-functionality-by-network). Si le fichier est au format ZIP, il n’est pas nécessaire de le décompresser au préalable.

Les fichiers de feuilles d’envoi groupé et les fichiers d’erreur sont automatiquement supprimés 30 jours après leur chargement ou leur génération.

>[!NOTE]
>Vous pouvez également publier un fichier de feuille d’envoi groupé ou un fichier d’erreur lorsque vous téléchargez le fichier.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Cochez la case en regard de chaque fichier à publier.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Post]**.

1. Dans la boîte de dialogue, saisissez ou sélectionnez des informations dans les paramètres de [[!UICONTROL Post Bulksheet]](#bulksheet-post-settings) puis cliquez sur **[!UICONTROL Post]**.

   Les mêmes paramètres s&#39;appliquent à tous les fichiers que vous publiez.

Lorsque la tâche commence, le statut et la date de publication planifiée de la ligne sont modifiés dans la vue [!UICONTROL Bulksheets]. Lorsque le fichier est publié, une notification par e-mail est envoyée avec un lien vers le fichier. Selon la quantité de données compilées, la notification par e-mail peut prendre plusieurs minutes ou plus. Toutefois, si l’une des données ne peut pas être publiée, un fichier d’erreur est répertorié dans la vue [!UICONTROL Bulksheets] et une notification par e-mail est envoyée avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>* La publication de grandes quantités de données prend plus de temps. Vous pouvez suivre la progression du fichier dans la colonne [!UICONTROL Progress] de la vue [!UICONTROL Bulksheets].
>* Toutes les données publiées sont soumises au processus éditorial du réseau.
* Avant la validation du fichier de feuille d&#39;envoi groupé, vous pouvez annuler la validation.

## Paramètres de publication pour les feuilles d’envoi groupé et les fichiers d’erreur corrigés {#bulksheet-post-settings}

| Paramètre | Description |
|----|----|
| [!UICONTROL Account (Search Engine)] | Compte réseau publicitaire pour lequel les données sont publiées. Si vous publiez plusieurs fichiers simultanément ou un fichier qui s’applique à plusieurs comptes, la valeur est <i>Plusieurs comptes sélectionnés</i>.<br><br>La première lettre du nom du réseau publicitaire est entre parenthèses après le nom du compte (par exemple, « Acme Realty (G) » pour un compte [!DNL Google Ads]). |
| [!UICONTROL Scheduling] | Quand publier le fichier sur le réseau publicitaire spécifié :<ul><li><i>[!UICONTROL Post to ad network now]</i> (valeur par défaut) : commence à publier immédiatement les données.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Commence à publier les données à la date et à l’heure spécifiées ; la valeur par défaut est demain à 02:00 (2 h). Pour modifier la date, saisissez une date au format JJ/MM/AAAA ou JJ/MM/AAAA ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar.png "Calendrier") pour ouvrir le calendrier et [sélectionner une date](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Pour modifier l’heure, saisissez l’heure au format HH/MM ou H/M ou sélectionnez une heure (par intervalles de 15 minutes) dans la liste.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Indique s’il faut inclure des modèles de suivi et des suffixes de page de destination (pour les réseaux publicitaires applicables) dans les comptes avec modèles de suivi, ou des URL de destination avec codes de suivi incorporés dans les comptes avec URL de destination, pour tous les mots-clés, annonces, emplacements, liens de site et groupes de produits [!DNL Google Ads] dans la publication : <i>[!UICONTROL Yes]</i> (par défaut) ou <i>[!UICONTROL No]</i>. Peu importe si les unités de soumission se trouvent dans un portefeuille.<br><br>Si vous sélectionnez <i>[!UICONTROL Yes]</i>, les URL sont générées en fonction des paramètres de la section [!UICONTROL Tracking Methods] des paramètres du compte ou des paramètres de campagne appropriés. Par défaut, si des URL de tracking existent, elles ne sont pas régénérées, sauf si de nouvelles URL sont nécessaires (par exemple, si le type de correspondance de mot-clé, le texte de l’annonce ou les paramètres de tracking pour les comptes concernés ont changé).<br><br>Si vous sélectionnez <i>[!UICONTROL No]</i>, vous pouvez toujours générer des URL de tracking ultérieurement en publiant manuellement le fichier chargé.<br><br><b>Remarque :</b> si l’annonceur utilise le suivi des conversions Adobe Advertising et que l’URL de base a changé, vous devez générer de nouvelles URL de suivi, sauf si le compte est configuré pour générer et charger automatiquement des URL de suivi. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Autorise les modifications de budget apportées aux campagnes dans des portfolios optimisés en fonction des données publiées. Par défaut, cette option n’est pas sélectionnée. Si vous sélectionnez cette option, les modifications du budget de campagne spécifiées sont applicables jusqu&#39;à ce que la fonctionnalité d&#39;optimisation détermine que le budget doit être réaffecté (généralement lors du prochain cycle d&#39;enchères).<br><br><b>Remarque :</b> toute modification de budget résultant des données validées pour des campagnes dans des portefeuilles non optimisés se produit lorsque le fichier est validé. Les modifications apparaissent dans les vues de gestion de campagne le lendemain. |
| [!UICONTROL Enable bidding on ads within portfolios] | Lorsque les composants de campagne inclus se trouvent dans un portfolio optimisé, cette fonctionnalité remplace la stratégie d’optimisation et permet de modifier les enchères en fonction des données de la feuille d’envoi groupé jusqu’à une date de fin spécifiée. Si vous sélectionnez cette option, indiquez une date de fin comprise entre 1 et 7 jours dans le champ **[!UICONTROL Hold bulksheet bids until]** . |

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l&#39;aide de feuilles d&#39;envoi groupé](bulksheet-about.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](bulksheet-download.md)
>* [Charger des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](bulksheet-upload.md)
>* [Valider les pages de destination dans les fichiers de feuille d’envoi groupé](bulksheet-validate-landing-pages.md)
>* [Exporter un fichier de feuille d’envoi groupé généré ou chargé](bulksheet-export.md)
