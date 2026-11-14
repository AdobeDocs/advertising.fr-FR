---
title: (Nouvelle interface utilisateur) Modifier le statut d’un portfolio
description: Découvrez comment modifier le statut d'un portefeuille ou supprimer un ou plusieurs portefeuilles inactifs sans ouvrir les paramètres du portefeuille.
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
source-git-commit: 163cbaf9b1a7f22e0205125cfab1ce2558182d8f
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%
---
# (Nouvelle interface utilisateur) Modifier le statut d’un portfolio

*Fonctionnalité Beta*

Vous pouvez modifier rapidement le statut d&#39;un portfolio [1} sans ouvrir les paramètres complets du portfolio.](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status)

Pour arrêter la collecte des données de coût/clic/impression et des données de chiffre d’affaires pour les campagnes appropriées, supprimez le portfolio . La suppression d’un portfolio le rend indisponible dans Search, Social et Commerce.

Toutes les modifications apportées au statut du portefeuille sont consignées dans l’historique des modifications du portefeuille.

>[!NOTE]
>
>Vous pouvez modifier le statut de plusieurs portefeuilles à l’aide des [feuilles d’envoi groupé de portefeuille](portfolio-bulksheets.md).

## Optimiser, activer ou désactiver un portefeuille depuis la vue [!UICONTROL Portfolios]

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Placez le curseur sur la ligne du portfolio et cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") en regard de [!UICONTROL Portfolio Status].

1. Modifiez le statut :

   * Pour activer un portfolio optimisé ou inactif, sélectionnez **[!UICONTROL Active]**.

   * Pour désactiver un portfolio actif ou optimisé, sélectionnez **[!UICONTROL Inactive]**.

   * Pour optimiser (lancer) un portfolio actif :

     1. Sélectionnez **[!UICONTROL Optimized]**.

     1. Dans le message de confirmation, cliquez sur **[!UICONTROL Update]**.

     1. Si d’autres messages de confirmation s’affichent, suivez les invites pour appliquer la modification.

     >[!NOTE]
     >
     >* Vous ne pouvez modifier le statut en optimisé que si le portfolio est déjà actif et contient au moins une campagne active avec au moins une annonce publicitaire active et un mot-clé/emplacement.
     >* Avant de passer au statut optimisé, vous devez implémenter des balises de suivi des conversions dans les pages web de l’annonceur. En outre, la bonne pratique consiste à effectuer une analyse de référence.
     >* Lorsque vous lancez un nouveau portefeuille, veillez à ce que la date de début soit aujourd’hui ou plus tard.
     >* Évitez de modifier le portefeuille au cours de la première semaine suivant l’optimisation, même si les performances sont volatiles.
     >* Une fois que Search, Social et Commerce commencent à optimiser un portfolio, laissez-le gérer tous les budgets futurs de la campagne et (le cas échéant) le changement d’enchères (le cas échéant). Search, Social et Commerce remplaceront toutes les modifications que vous apportez depuis le réseau publicitaire.
     >* Vous pouvez temporairement définir des enchères manuelles pour toute campagne CPC optimisée du portefeuille en créant et en publiant des feuilles d&#39;envoi groupé de campagne. Toutes les modifications d’enchères résultant des données validées sont applicables pendant une journée. Ensuite, Search, Social et Commerce reprennent la définition des enchères en fonction de sa propre stratégie d’optimisation.

## Supprimer un ou plusieurs portefeuilles inactifs de la vue [!UICONTROL Portfolios]

Vous ne pouvez supprimer que les portefeuilles inactifs. Si le portfolio est optimisé ou actif, vous devez d’abord changer son statut en inactif avant d’avoir la possibilité de le supprimer.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Effectuez l’une des opérations suivantes :

   * Pour supprimer un seul portfolio inactif :

     1. Placez le curseur sur la ligne du portfolio et cliquez sur **[!UICONTROL ...]>[!UICONTROL Delete]**.

     1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

   * Pour supprimer un ou plusieurs portefeuilles inactifs :

     1. Cochez la case en regard de chaque portfolio inactif à supprimer.

     1. Dans la barre d’outils des actions en bloc, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer").

     1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Créer un portfolio](portfolio-create.md)
>* [(Nouvelle interface utilisateur) Modifier un portfolio](portfolio-edit.md)
>* [À propos des portefeuilles](portfolio-about.md)
