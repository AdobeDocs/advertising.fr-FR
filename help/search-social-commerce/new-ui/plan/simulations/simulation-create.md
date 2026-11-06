---
title: Exécuter ou réexécuter une simulation personnalisée
description: Découvrez comment exécuter ou réexécuter une simulation personnalisée pour un portfolio.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 0ee62d04-fdc4-445c-90fb-71d5a40a9ed0
TQID: 'https://experienceleague.adobe.com/DlSJEcKXOxVz6UXVpAjQqaiwDTakgJ4SS6rsQUxkQIE'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%
---
# Exécuter ou réexécuter une simulation personnalisée

*Fonction*

Vous pouvez générer une simulation personnalisée pour un portfolio [ optimisé ou actif ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#portfolio-status). Vous pouvez également sélectionner une simulation dans la liste pour exécuter une nouvelle simulation pour le même portfolio, ou réexécuter des simulations avec leurs paramètres existants.

La création d’une simulation personnalisée nécessite l’autorisation [!UICONTROL Create Simulation]. La sélection d’un portfolio nécessite l’autorisation [!UICONTROL View Portfolios].

<!-- You can't run sims for portfolios with legacy keyword-level optimization when they include smart bidding campaigns. Clarify all exceptions so users don't find out via error messages. -->

Les utilisateurs de [!UICONTROL Admin] et de [!UICONTROL Account Manager] peuvent voir les simulations créées par d’autres utilisateurs. Tous les autres utilisateurs et utilisatrices ne peuvent voir que les simulations personnalisées qu’ils ou elles créent.

## Création d’une simulation {#simulation-create}

Vous pouvez démarrer à partir de la vue [!UICONTROL Simulations] ou [exécuter une simulation personnalisée à partir de la vue [!UICONTROL Portfolios]](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#run-simulation).

1. Dans le menu principal, cliquez sur **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Effacez les lignes de simulation sélectionnées, puis cliquez sur **[!UICONTROL Run Simulation]**.

1. Sélectionnez le portfolio :

   1. Cliquez sur **[!UICONTROL Select Portfolio]**.

   1. Sélectionnez le portefeuille.

      Pour rechercher des portfolios qui incluent une chaîne de texte spécifique, commencez à saisir la chaîne de texte dans le champ de recherche. Les valeurs ne respectent pas la casse.

   1. Cliquez sur **[!UICONTROL Proceed]**.

1. Définissez les [paramètres personnalisés de la simulation](#custom-simulation-settings) :

   1. (Facultatif) Pour modifier le portfolio utilisé pour la simulation, cliquez sur **[!UICONTROL Change Portfolio]** en regard du nom du portfolio, sélectionnez le portfolio, puis cliquez sur **[!UICONTROL Proceed]**.

   1. Dans l’onglet [!UICONTROL Basic Settings] :

      1. Saisissez un **[!UICONTROL Simulation Name]** unique.

      1. (Facultatif) Modifiez les paramètres de base de la simulation.

   1. (Facultatif) Dans l&#39;onglet [!UICONTROL Advanced Settings], modifiez les paramètres avancés de la simulation.

   Les paramètres existants pour le portefeuille sélectionné sont spécifiés par défaut. La modification des valeurs vous affichera les résultats que différents paramètres produiraient sans modifier les paramètres existants du portefeuille.

1. Cliquez sur **[!UICONTROL Next]**.

1. Passez en revue les paramètres et modifiez-les si nécessaire.

1. Cliquez sur **[!UICONTROL Submit & Run]**.

La demande est envoyée et la vue [!UICONTROL Simulations] s’ouvre. Lorsque le rapport de simulation est disponible, vous et tout autre destinataire d’e-mail spécifié recevez une notification avec un lien de téléchargement. Vous pouvez également [télécharger la simulation depuis la vue [!UICONTROL Simulations]](simulation-download.md).

<!-- Still true:  When the results for any report type include more than 60,000 rows, the workbook includes multiple worksheets. -->

## Réexécuter une simulation avec les paramètres existants {#rerun-a-simulation-with-the-existing-settings}

Vous pouvez réexécuter jusqu’à 10 simulations à la fois avec leurs paramètres existants. Les simulations dont le statut est [!UICONTROL Queued] ou [!UICONTROL In Progress] ne peuvent pas être réexécutées. Si votre sélection inclut ces simulations, elles sont ignorées et les simulations restantes sont envoyées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Cochez les cases en regard des simulations que vous souhaitez réexécuter.

1. Dans la barre d’outils située au-dessus du tableau de données ou dans la barre d’outils d’actions en masse, cliquez sur **[!UICONTROL Re-Run Simulation]**.

La requête est envoyée et la vue s’actualise.

## Exécuter une nouvelle simulation pour un portfolio dans la liste {#edit-the-settings-for-an-existing-simulation-and-rerun-it}

Le fait de sélectionner une simulation avant de cliquer sur [!UICONTROL Run Simulation] sélectionne son portfolio pour une nouvelle simulation. Le formulaire utilise les paramètres actuels du portfolio et non ceux de la simulation sélectionnée. Cette action ne modifie pas la simulation existante.

1. Dans le menu principal, cliquez sur **[!UICONTROL Plan]>[!UICONTROL Simulations]**.

1. Cochez la case en regard d&#39;une simulation pour le portfolio que vous souhaitez utiliser.

   Si vous sélectionnez plusieurs simulations, elles doivent toutes utiliser le même portfolio. Le portefeuille doit être actif ou optimisé.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Run Simulation]**.

1. Spécifiez les [paramètres personnalisés de simulation](#custom-simulation-settings), y compris un **[!UICONTROL Simulation Name]** unique. Modifiez les paramètres sur les onglets **[!UICONTROL Basic Settings]** et **[!UICONTROL Advanced Settings]** selon vos besoins.

1. Cliquez sur **[!UICONTROL Next]**.

1. Passez en revue les paramètres et modifiez-les si nécessaire.

1. Cliquez sur **[!UICONTROL Submit & Run]**.

La demande est envoyée et la vue [!UICONTROL Simulations] s’ouvre. Vous pouvez [télécharger la simulation](simulation-download.md) une fois qu’elle est terminée.

## Paramètres personnalisés de la simulation {#custom-simulation-settings}

Pour plus d’informations sur les paramètres personnalisés de la simulation, consultez le Guide d’optimisation , disponible dans Search, Social et Commerce.

>[!MORELIKETHIS]
>
>* [À propos des simulations](simulation-about.md)
>* [Afficher les détails de la simulation](simulation-view.md)
>* [Télécharger des simulations](simulation-download.md)
