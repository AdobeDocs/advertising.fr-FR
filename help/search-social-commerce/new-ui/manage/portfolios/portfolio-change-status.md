---
title: (Nouvelle interface utilisateur) Modifier le statut d’un portfolio
description: Découvrez comment modifier le statut d’un portfolio ou supprimer un portfolio inactif.
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 081453404883619e0a70bba080c857bf7e3136cc
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Modifier le statut d’un portfolio

*Fonction*

Le statut d&#39;un portefeuille peut être l&#39;un des suivants :

* **Inactif :** la fonctionnalité d’optimisation collecte des données de coût/clic/impression pour les campagnes appropriées à des fins de création de rapports, mais elle ne modélise pas les données et n’optimise pas les budgets et les enchères de campagne.

* **Actif :** la fonctionnalité d’optimisation collecte des données sur les coûts/clics/impressions et le chiffre d’affaires pour les campagnes appropriées et modélise les données, mais elle n’optimise pas les budgets de campagne ni les enchères. Activez un portfolio inactif pour commencer à modéliser les données ou rétrogradez un portfolio optimisé vers l’état actif pour arrêter l’optimisation.

* **Optimisé :** la fonctionnalité d’optimisation collecte des données sur les coûts/clics/impressions et le chiffre d’affaires pour les campagnes appropriées, modélise les données et optimise les budgets et les enchères des campagnes (le cas échéant) à la date de début du portefeuille désigné. La modification du statut en optimisé est également appelée lancement du portfolio.

Pour arrêter la collecte des données de coût/clic/impression et des données de chiffre d’affaires pour les campagnes appropriées, supprimez le portfolio . La suppression d’un portfolio le rend indisponible dans Search, Social et Commerce.

Toutes les modifications apportées au statut du portefeuille sont consignées dans l’historique des modifications du portefeuille.

## Optimiser, activer ou désactiver un portefeuille

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Placez le curseur sur la ligne du portfolio et cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier") en regard de la [!UICONTROL Portfolio Status].

1. Modifiez le statut :

   * Pour activer un portfolio optimisé ou inactif, sélectionnez **[!UICONTROL Active]**.

   * Pour désactiver un portefeuille actif, sélectionnez **[!UICONTROL Inactive]**.

   * Pour optimiser (lancer) un portfolio actif, sélectionnez **[!UICONTROL Optimized]**.

     >[!NOTE]
     >
     >* Vous ne pouvez lancer un portfolio que s’il est déjà actif et contient au moins une campagne active avec au moins une annonce publicitaire active et un mot-clé/emplacement.
     >* Avant de lancer un portfolio, vous devez implémenter des balises de suivi des conversions dans les pages web de l’annonceur.
     >* Avant de lancer un portfolio, il est recommandé d’effectuer une analyse de référence.
     >* Si vous lancez un nouveau portefeuille, veillez à ce que la date de début soit aujourd’hui ou plus tard.>* Évitez de modifier le portefeuille au cours de la première semaine suivant le lancement, même si les performances sont instables.
     >* Une fois que Search, Social et Commerce commencent à optimiser un portfolio, vous devez le laisser gérer toutes les modifications futures des enchères (le cas échéant). Search, Social et Commerce remplaceront toutes les modifications que vous apportez depuis le réseau publicitaire.
     >* Après avoir lancé un portefeuille, vous pouvez temporairement définir des enchères manuelles pour n&#39;importe quelle campagne CPC du portefeuille en créant et en publiant des feuilles d&#39;envoi groupé de campagne. Toutes les modifications d’enchères résultant des données validées sont applicables pendant une journée. Ensuite, Search, Social et Commerce reprennent la définition des enchères en fonction de sa propre stratégie d’optimisation.

## Supprimer un portefeuille inactif

Vous ne pouvez supprimer que les portefeuilles inactifs. Si le portfolio est optimisé ou actif, vous devez d’abord changer son statut en inactif avant d’avoir la possibilité de le supprimer.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Effectuez l’une des opérations suivantes :

   * Placez le curseur sur la ligne du portfolio, puis cliquez sur **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Cochez la case en regard du portefeuille. Dans la barre d’outils des actions en bloc, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer").

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Créer un portfolio](portfolio-create.md)
>* [&#x200B; (nouvelle interface utilisateur) Modification d’un portfolio](portfolio-edit.md)
>* [À propos des portefeuilles](portfolio-about.md)
