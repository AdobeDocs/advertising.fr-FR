---
title: Générer un rapport de base ou un rapport avancé
description: Découvrez comment générer un rapport de base ou avancé personnalisé.
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Générer un rapport de base ou un rapport avancé

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur sur **[!UICONTROL Basic Reports]** ou **[!UICONTROL Advanced Reports]**, puis cliquez sur le [type de rapport](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Facultatif) Dans la fenêtre [!UICONTROL Report Settings], modifiez les [paramètres de rapport](basic-advanced-report-settings.md) par défaut :

   1. (Facultatif) Saisissez un nom personnalisé pour le rapport et le modèle (si vous enregistrez le rapport comme modèle).

   1. (Facultatif) Pour enregistrer les paramètres du rapport en tant que modèle, cochez la case en regard de **[!UICONTROL Save as template]**.

   1. (Facultatif) Dans l’onglet **[!UICONTROL Basic Settings]**, sélectionnez un modèle de rapport existant pour utiliser ou modifier les paramètres de base par défaut du rapport.

   1. (Facultatif) Cliquez sur **[!UICONTROL Columns tab]**, puis modifiez les colonnes par défaut du rapport.

      Par défaut, toutes les données monétaires des rapports sont présentées au format en dollars (1 000,00, par exemple). Pour afficher la valeur dans le bon format de devise (mais sans symboles de devise dans les formats CSV et TSV), ajoutez la colonne &quot;[!UICONTROL Currency]&quot; au rapport. Si le rapport inclut des données pour des comptes avec des devises différentes, alors toute valeur monétaire &quot;[!UICONTROL Total]&quot; est la somme de tous les nombres de la colonne, quelle que soit la devise.

   1. (Facultatif ; [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] et [!UICONTROL Label Classification Report] uniquement) Cliquez sur l’onglet **[!UICONTROL Classifications]** et limitez les résultats du rapport à inclure uniquement des classifications d’étiquettes spécifiques.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Advanced Filters]** et modifiez les options avancées par défaut.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Attribution]** et modifiez la règle d’attribution par défaut.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Scheduling and Delivery]** et modifiez les options de planification et de diffusion par défaut.

1. (Facultatif lorsqu’il est disponible) Pour prévisualiser les 50 premières lignes du rapport, cliquez sur **[!UICONTROL Preview]**. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Back]** pour revenir à la page des paramètres du rapport.

   >[!NOTE]
   >
   >Le bouton Aperçu est disponible pour tous les rapports de base et avancés, à l’exception de [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report] et [!UICONTROL Transaction Report].

1. Cliquez sur **[!UICONTROL Create]**.

Si vous n’avez pas indiqué de planification de rapport, le rapport est exécuté immédiatement. Dans le cas contraire, il est exécuté selon la planification spécifiée. Le nom du rapport est ajouté à la vue [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Si vous avez enregistré le rapport en tant que modèle, il est également ajouté à la vue [[!UICONTROL Templates]](/help/search-social-commerce/reports/report-about.md). Une fois le rapport terminé, le fichier peut être ouvert ou enregistré ; des modèles sont disponibles immédiatement.

Si vous avez saisi des adresses électroniques de notification, chaque destinataire reçoit une notification une fois la tâche de rapport terminée ou échouée, en fonction des [ paramètres de notification configurés](/help/search-social-commerce/notifications/notification-edit.md) de l’utilisateur pour les rapports.

>[!MORELIKETHIS]
>
>* [À propos des rapports de base et avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [ Paramètres de rapport de base et avancés ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [ Colonnes de rapports pour les rapports de base et avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Supprimer des rapports](/help/search-social-commerce/reports/management/report-delete.md)
