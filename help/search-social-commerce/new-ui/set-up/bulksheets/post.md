---
title: (Nouvelle interface utilisateur) Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés
description: Découvrez comment publier des fichiers de feuilles d’envoi groupé sur vos réseaux publicitaires dans la nouvelle interface utilisateur de Search, Social et Commerce.
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
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: 752
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés

Vous pouvez publier des fichiers de feuilles d&#39;envoi groupé existants ou des fichiers d&#39;erreur corrigés sur les comptes appropriés pour [réseaux publicitaires pris en charge](about.md#bulksheet-functionality-by-network). Si le fichier est au format ZIP, il n’est pas nécessaire de le décompresser au préalable.

Les fichiers de feuilles d’envoi groupé et les fichiers d’erreur sont automatiquement supprimés 30 jours après leur chargement ou leur génération.

>[!NOTE]
>
>Vous pouvez également publier un fichier de feuille d’envoi groupé ou un fichier d’erreur lorsque vous téléchargez le fichier.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Cochez la case en regard de chaque fichier à publier.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Post]**.

1. Saisissez ou sélectionnez des informations dans les paramètres de [&#128279;](#bulksheet-post-settings) puis cliquez sur **[!UICONTROL Post]**.[!UICONTROL Post Bulksheet]

   Les mêmes paramètres s&#39;appliquent à tous les fichiers que vous publiez.

Lorsque la tâche commence, le statut et la date de publication planifiée de la ligne sont mis à jour dans la vue [!UICONTROL Bulksheets]. Lorsque les notifications par e-mail pour les feuilles d’envoi groupé sont [&#x200B; activées dans [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md), une notification par e-mail avec un lien vers le fichier est envoyée lorsque le fichier est publié. Selon la quantité de données compilées, la notification par e-mail peut prendre plusieurs minutes ou plus. Si l’une des données ne peut pas être publiée, un fichier d’erreur est répertorié dans la vue [!UICONTROL Bulksheets] et une notification est envoyée par e-mail avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>* La publication de grandes quantités de données prend plus de temps. Vous pouvez suivre la progression du fichier dans la colonne [!UICONTROL Progress] de la vue [!UICONTROL Bulksheets].
>* Toutes les données publiées sont soumises au processus éditorial du réseau.
>* Avant la validation du fichier de feuille d&#39;envoi groupé, vous pouvez annuler la validation.

## Paramètres de publication pour les feuilles d’envoi groupé et les fichiers d’erreur corrigés {#bulksheet-post-settings}

| Paramètre | Description |
|----|----|
| [!UICONTROL Account (Search Engine)] | Compte réseau publicitaire pour lequel les données sont publiées. Si vous publiez plusieurs fichiers simultanément ou un fichier qui s’applique à plusieurs comptes, la valeur est *Plusieurs comptes sélectionnés*.<br><br>La première lettre du nom du réseau publicitaire est entre parenthèses après le nom du compte (par exemple, « Acme Realty (G) » pour un compte [!DNL Google Ads]). |
| [!UICONTROL Scheduling] | Quand publier le fichier sur le réseau publicitaire spécifié :<ul><li>*[!UICONTROL Post to ad network now]* (valeur par défaut) : commence à publier immédiatement les données.</li><li>*[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:* Commence à publier les données à la date et à l’heure spécifiées ; la valeur par défaut est demain à 02 :00 (2 heures). Pour modifier la date, saisissez une date au format JJ/MM/AAAA ou cliquez sur l’icône de calendrier pour ouvrir le calendrier et sélectionner une date. Pour modifier l’heure, sélectionnez une heure (par intervalles de 15 minutes) dans la liste.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Indique s’il faut inclure des modèles de suivi et des suffixes de page de destination (pour les réseaux publicitaires applicables) dans les comptes avec modèles de suivi, ou des URL de destination avec codes de suivi incorporés dans les comptes avec URL de destination, pour tous les mots-clés, annonces, emplacements, liens de site et groupes de produits [!DNL Google Ads] dans la publication : *[!UICONTROL Yes]* (par défaut) ou *[!UICONTROL No]*. Peu importe si les unités de soumission se trouvent dans un portefeuille.<br><br>Si vous sélectionnez *[!UICONTROL Yes]*, les URL sont générées en fonction des paramètres de la section [!UICONTROL Tracking Methods] des paramètres du compte ou des paramètres de campagne appropriés. Par défaut, si des URL de tracking existent, elles ne sont pas régénérées, sauf si de nouvelles URL sont nécessaires (par exemple, si le type de correspondance de mot-clé, le texte de l’annonce ou les paramètres de tracking pour les comptes concernés ont changé).<br><br>Si vous sélectionnez *[!UICONTROL No]*, vous pouvez toujours générer des URL de tracking ultérieurement en publiant manuellement le fichier chargé.<br><br>**Remarque :** Si l’annonceur utilise le tracking des conversions Adobe Advertising et que l’URL de base a changé, vous devez générer de nouvelles URL de tracking, sauf si le compte est configuré pour générer et charger automatiquement des URL de tracking. |
| [!UICONTROL Replace Media Optimizer Tracking] | (Disponible si [!UICONTROL Generate Tracking URLs] est *[!UICONTROL Yes]*) Remplace tout suivi Adobe Advertising existant dans les URL du fichier chargé par un suivi nouvellement généré. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Autorise les modifications de budget apportées aux campagnes dans des portfolios optimisés en fonction des données publiées. Par défaut, cette option n’est pas sélectionnée. Si vous sélectionnez cette option, les modifications du budget de la campagne spécifiées sont applicables jusqu&#39;à ce que la fonctionnalité d&#39;optimisation détermine que le budget doit être réaffecté (généralement lors du prochain cycle d&#39;enchères).<br><br>**Remarque :** toute modification du budget résultant des données validées pour les campagnes dans des portefeuilles non optimisés se produit lorsque le fichier est validé. Les modifications apparaissent dans les vues de gestion de campagne le lendemain. |
| [!UICONTROL Enable bidding on ads within portfolios] | Lorsque les composants de campagne inclus se trouvent dans un portfolio optimisé, cette fonctionnalité remplace la stratégie d’optimisation et permet de modifier les enchères en fonction des données de la feuille d’envoi groupé jusqu’à une date de fin spécifiée. Si vous sélectionnez cette option, indiquez une date de fin comprise entre 1 et 7 jours dans le champ **[!UICONTROL Hold bulksheet bids until]** . |

>[!MORELIKETHIS]
>
>* [&#x200B; (nouvelle interface utilisateur) À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupé](about.md)
>* [(nouvelle interface utilisateur) Télécharger/créer un fichier de feuille d’envoi groupé](download.md)
>* [(Nouvelle interface utilisateur) Chargez une feuille d’envoi groupé ou un fichier d’erreur corrigé](upload.md)
>* [(nouvelle interface utilisateur) Valider les pages de destination dans des fichiers de feuille d’envoi groupé](validate-landing-pages.md)
>* [(Nouvelle interface utilisateur) Supprimer les feuilles d’envoi groupé et les fichiers d’erreur chargés](delete.md)
