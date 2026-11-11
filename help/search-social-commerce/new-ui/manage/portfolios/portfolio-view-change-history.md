---
title: (Nouvelle interface utilisateur) Afficher l’historique des modifications et des modifications d’enchères d’un portefeuille
description: Découvrez comment afficher les modifications de portfolio et l’historique des modifications d’enchères, modifier les périodes, filtrer les modifications de portfolio et générer, télécharger et supprimer des rapports d’historique dans Adobe Advertising Search, Social et Commerce.
feature: Search Portfolios, Search Optimization
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
source-git-commit: e7e0221adbb72127a9e6d2354b6a235b233a4a76
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%
---
# (Nouvelle interface utilisateur) Afficher l’historique des modifications et des modifications d’enchères d’un portefeuille

*Fonctionnalité Beta*

Vous pouvez afficher un journal des modifications apportées au portefeuille au cours d’une période. Les actions consignées incluent la création du portefeuille, toutes les modifications apportées aux paramètres du portefeuille, toutes les campagnes affectées au portefeuille ou non affectées à celui-ci, toutes les contraintes appliquées aux unités d&#39;offre du portefeuille ou supprimées de celles-ci, toutes les contraintes sur les unités d&#39;offre du portefeuille qui ont expiré et d&#39;autres actions affectant le portefeuille.

La boîte de dialogue [!UICONTROL Change History] comprend un onglet [!UICONTROL Portfolio Change History] pour les modifications du portefeuille et un onglet [!UICONTROL Portfolio Bid Change History] pour l’historique des enchères. Par défaut, les deux onglets affichent les 180 derniers jours, se terminant hier.

Vous pouvez filtrer les modifications du portefeuille par catégorie et modifier la période pour l’un ou l’autre des onglets. Vous pouvez également télécharger les données dans un fichier de feuille de calcul.

## Afficher l&#39;historique des modifications d&#39;un portefeuille {#portfolio-change-history}

Les informations de chaque modification comprennent les éléments [!UICONTROL Change Date], [!UICONTROL Changed By], [!UICONTROL Change Type] et [!UICONTROL Description]. Les modifications sont répertoriées du plus récent au plus ancien.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Placez le curseur sur la ligne du portfolio et cliquez sur **[!UICONTROL ...]>[!UICONTROL Change History]**.

1. Dans la boîte de dialogue [!UICONTROL Change History], affichez l’onglet **[!UICONTROL Portfolio Change History]**.

1. (Facultatif) Modifiez les informations affichées :

   * Cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar-new.png "Calendrier") pour modifier la période du rapport.

   * Cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter-new.png "Filtrer") pour filtrer les données par catégorie : [!UICONTROL All], [!UICONTROL Objective], [!UICONTROL Campaign], [!UICONTROL Target], [!UICONTROL Constraints], [!UICONTROL Optimization Levers] ou [!UICONTROL Others].

## Afficher l&#39;historique des modifications d&#39;enchères d&#39;un portefeuille {#portfolio-bid-change-history}

1. [Ouvrez l&#39;historique des modifications du portefeuille](#portfolio-change-history).

1. Cliquez sur l’onglet **[!UICONTROL Portfolio Bid Change History]**.

1. (Facultatif) Cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar-new.png "Calendrier") pour modifier la période.

1. (Facultatif) Cliquez sur l’en-tête de colonne de date pour trier la liste par date dans l’ordre croissant ou décroissant.

Pour afficher l&#39;historique d&#39;une unité d&#39;offre individuelle, [ouvrez les détails de l&#39;unité d&#39;offre à partir des détails des performances du portefeuille](portfolio-details.md#bid-unit-history). Vous pouvez également [ouvrir l&#39;historique des unités d&#39;enchères à partir de la vue [!UICONTROL Keywords]](/help/search-social-commerce/new-ui/manage/keywords/keyword-manage.md#bid-unit-history) lorsque la colonne [!UICONTROL Bid Unit ID] est disponible.

## Gérer les rapports pour les historiques de modification de portefeuille

Vous pouvez télécharger des informations supplémentaires sur l&#39;historique des modifications d&#39;un portfolio vers un fichier au format [!DNL Microsoft Excel] de classeur (fichier XLSX). Le rapport comprend l’identifiant de modification numérique, les anciennes et les nouvelles valeurs, le type de modification (par exemple « ajouté » ou « modifié »), le type d’action (par exemple « Budget » ou « Nom du Portfolio ») et le sous-type, le cas échéant, l’heure et le nom d’utilisateur.

Vous pouvez également générer, télécharger et supprimer des rapports à partir de l&#39;onglet [!UICONTROL Portfolio Bid Change History]. Les paramètres du rapport sont intitulés [!UICONTROL Portfolio History] pour les modifications de portefeuille et [!UICONTROL Portfolio Bid History] pour l’historique des enchères.

### Générer un rapport avec les lignes de données filtrées

1. [Ouvrez l&#39;historique des modifications du portfolio](#portfolio-change-history), puis cliquez sur l&#39;onglet dont vous souhaitez télécharger les données.

1. Dans le coin supérieur droit, cliquez sur ![Télécharger le rapport](/help/search-social-commerce/assets/download.png "Télécharger le rapport").

1. Dans les paramètres [!UICONTROL Portfolio History] ou [!UICONTROL Portfolio Bid History], acceptez le nom de rapport par défaut ou saisissez un nom de rapport unique, puis cliquez sur **[!UICONTROL Generate]**.

   Par défaut, le nom du rapport inclut le type d’historique et la date et l’heure au format `YYYYMMDD_HHmm`, par exemple « portfolioChangeHistory_20260402_1326 ». Si le nom existe déjà, un suffixe numérique est ajouté.

   Le fichier est ajouté à la liste [!UICONTROL Recently Generated].

1. (Facultatif) Pour télécharger le fichier une fois l’opération terminée, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Télécharger un rapport terminé

1. [Ouvrez l&#39;historique des modifications du portefeuille](#portfolio-change-history), puis cliquez sur l&#39;onglet à partir duquel vous avez généré le rapport.

1. Dans le coin supérieur droit, cliquez sur ![Télécharger le rapport](/help/search-social-commerce/assets/download.png "Télécharger le rapport").

1. Dans la liste [!UICONTROL Recently Generated] des paramètres [!UICONTROL Portfolio History] ou [!UICONTROL Portfolio Bid History], cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Supprimer un rapport terminé

1. [Ouvrez l&#39;historique des modifications du portefeuille](#portfolio-change-history), puis cliquez sur l&#39;onglet à partir duquel vous avez généré le rapport.

1. Dans le coin supérieur droit, cliquez sur ![Télécharger le rapport](/help/search-social-commerce/assets/download.png "Télécharger le rapport").

1. Dans la liste [!UICONTROL Recently Generated] des paramètres [!UICONTROL Portfolio History] ou [!UICONTROL Portfolio Bid History], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") en regard du nom du fichier.

>[!MORELIKETHIS]
>
>* [Créer un portfolio](portfolio-create.md)
>* [(Nouvelle interface utilisateur) Modifier un portfolio](portfolio-edit.md)
>* [(Nouvelle interface utilisateur) Afficher les détails sur les performances du portfolio](portfolio-details.md)
>* [(Nouvelle interface utilisateur) Télécharger des données dans la vue [!UICONTROL Portfolios]](portfolio-view-report.md)
>* [À propos des portefeuilles](portfolio-about.md)
