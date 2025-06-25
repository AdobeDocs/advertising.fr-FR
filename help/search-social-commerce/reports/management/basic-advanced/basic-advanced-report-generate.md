---
title: Générer un rapport de base ou avancé
description: Découvrez comment générer un rapport de base ou avancé personnalisé.
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Générer un rapport de base ou avancé

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Report]**, placez le curseur sur **[!UICONTROL Basic Reports]** ou **[!UICONTROL Advanced Reports]**, puis cliquez sur le [type de rapport](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Facultatif) Dans la fenêtre [!UICONTROL Report Settings], modifiez les paramètres par défaut [paramètres du rapport](basic-advanced-report-settings.md) :

   1. (Facultatif) Saisissez un nom personnalisé pour l’état et pour le modèle (si vous enregistrez l’état en tant que modèle).

   1. (Facultatif) Pour enregistrer les paramètres du rapport en tant que modèle, cochez la case en regard de **[!UICONTROL Save as template]**.

   1. (Facultatif) Dans l’onglet **[!UICONTROL Basic Settings]** , sélectionnez un modèle de rapport existant à utiliser ou modifiez les paramètres de base par défaut pour le rapport.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Columns tab]** et modifiez les colonnes par défaut du rapport.

      Par défaut, toutes les données monétaires des rapports sont présentées en dollars américains (par exemple 1 000,00). Pour afficher la valeur au format de devise approprié (mais sans aucun symbole de devise aux formats CSV et TSV), ajoutez la colonne « [!UICONTROL Currency] » au rapport. Si le rapport inclut des données pour des comptes avec différentes devises, les valeurs monétaires « [!UICONTROL Total] » sont la somme de tous les nombres de la colonne, quelle que soit la devise.

   1. (Facultatif ; [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report] et [!UICONTROL Label Classification Report] uniquement) Cliquez sur l’onglet **[!UICONTROL Classifications]** et limitez les résultats du rapport à des classifications d’étiquettes spécifiques.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Advanced Filters]** et modifiez les options avancées par défaut.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Attribution]** et modifiez la règle d’attribution par défaut.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Scheduling and Delivery]** et modifiez les options de planification et de diffusion par défaut.

1. (Facultatif si disponible) Pour prévisualiser les 50 premières lignes du rapport, cliquez sur **[!UICONTROL Preview]**. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Back]** pour revenir à la page des paramètres du rapport.

   >[!NOTE]
   >
   >Le bouton Aperçu est disponible pour tous les rapports de base et avancés, à l’exception des rapports [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report] et [!UICONTROL Transaction Report].

1. Cliquez sur **[!UICONTROL Create]**.

Si vous n&#39;avez pas spécifié de planning de rapport, le rapport est exécuté immédiatement ; dans le cas contraire, il l&#39;est selon le planning spécifié. Le nom du rapport est ajouté à la vue [[!UICONTROL Latest Reports]](/help/search-social-commerce/reports/report-about.md). Si vous avez enregistré le rapport en tant que modèle, il est également ajouté à la vue [[!UICONTROL Templates]. ](/help/search-social-commerce/reports/report-about.md). Une fois le rapport terminé, vous pouvez ouvrir ou enregistrer le fichier ; les modèles sont disponibles immédiatement.

Si vous avez saisi des adresses e-mail pour la notification, chaque destinataire reçoit une notification lorsque la tâche de rapport est terminée ou échoue, en fonction des [paramètres de notification configurés](/help/search-social-commerce/notifications/notification-edit.md) de l’utilisateur pour les rapports.

>[!MORELIKETHIS]
>
>* [À propos des rapports de base et avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Paramètres de rapport de base et avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Colonnes de rapport pour les rapports de base et avancés](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Supprimer des rapports](/help/search-social-commerce/reports/management/report-delete.md)
