---
title: Générer un rapport de base ou un rapport avancé
description: Découvrez comment générer un rapport de base ou avancé personnalisé.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Générer un rapport de base ou un rapport avancé

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur sur **[!UICONTROL Basic Reports]** ou **[!UICONTROL Advanced Reports]**, puis cliquez sur le bouton [type de rapport](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Facultatif) Dans le [!UICONTROL Report Settings] , modifiez la valeur par défaut [paramètres de rapport](basic-advanced-report-settings.md):

   1. (Facultatif) Saisissez un nom personnalisé pour le rapport et le modèle (si vous enregistrez le rapport comme modèle).

   1. (Facultatif) Pour enregistrer les paramètres du rapport en tant que modèle, cochez la case en regard de **[!UICONTROL Save as template]**.

   1. (Facultatif) Sur la page **[!UICONTROL Basic Settings]** sélectionnez un modèle de rapport existant à utiliser ou modifiez les paramètres de base par défaut du rapport.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Columns tab]** et modifiez les colonnes par défaut du rapport.

      Par défaut, toutes les données monétaires des rapports sont présentées au format en dollars (1 000,00, par exemple). Pour afficher la valeur dans le bon format de devise (mais sans aucun symbole de devise dans les formats CSV et TSV), ajoutez le &quot;[!UICONTROL Currency]&quot; au rapport. Si le rapport inclut des données pour des comptes avec des devises différentes, alors tout[!UICONTROL Total]&quot;les valeurs monétaires sont la somme de tous les nombres de la colonne, quelle que soit la devise.

   1. (Facultatif) [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], et [!UICONTROL Label Classification Report] uniquement) Cliquez sur le bouton **[!UICONTROL Classifications]** et limitez les résultats du rapport afin de n’inclure que des classifications d’étiquettes spécifiques.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Advanced Filters]** et modifiez les options avancées par défaut.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Attribution]** et modifiez la règle d’attribution par défaut.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Scheduling and Delivery]** et modifiez les options de planification et de diffusion par défaut.

1. (Facultatif lorsqu’il est disponible) Pour prévisualiser les 50 premières lignes du rapport, cliquez sur **[!UICONTROL Preview]**. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Back]** pour revenir à la page paramètres du rapport.

   >[!NOTE]
   >
   >Le bouton Aperçu est disponible pour tous les rapports de base et avancés, à l’exception du [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report], et [!UICONTROL Transaction Report].

1. Cliquez sur **[!UICONTROL Create]**.

Si vous n’avez pas indiqué de planification de rapport, le rapport est exécuté immédiatement. sinon, il est exécuté selon le planning spécifié. Le nom du rapport est ajouté à la variable [[!UICONTROL Latest Reports] view](/help/search-social-commerce/reports/report-about.md). Si vous avez enregistré le rapport en tant que modèle, il est également ajouté à la variable [[!UICONTROL Templates] view](/help/search-social-commerce/reports/report-about.md). Une fois le rapport terminé, le fichier peut être ouvert ou enregistré ; les modèles sont disponibles immédiatement.

Si vous avez saisi des adresses électroniques de notification, chaque destinataire reçoit une notification une fois la tâche de rapport terminée ou échouée, en fonction des [paramètres de notification configurés](/help/search-social-commerce/notifications/notification-edit.md) pour les rapports.

>[!MORELIKETHIS]
>
>* [À propos des rapports de base et avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Paramètres de base et avancés des rapports](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Colonnes de rapports pour les rapports de base et avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Suppression de rapports](/help/search-social-commerce/reports/management/report-delete.md)
