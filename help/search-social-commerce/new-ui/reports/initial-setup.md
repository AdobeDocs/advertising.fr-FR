---
title: (Nouvelle interface utilisateur) Tâches de configuration initiales pour les rapports
description: Découvrez comment rendre les mesures disponibles dans les rapports et comment automatiser les rapports.
feature: Search Reports
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Tâches de configuration initiales pour les rapports

Les nouveaux utilisateurs doivent effectuer les tâches de configuration initiales suivantes :

* Rendez les mesures de conversion qu’Adobe Advertising suit pour un annonceur disponibles pour les rapports et d’autres vues. Vous pouvez également renommer les mesures de conversion affichées dans les en-têtes de colonne pour en faciliter la lecture. Voir « [ Gérer les mesures de conversion d’un annonceur ](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md) ».

  Les propriétés des transactions ne sont pas disponibles pour les rapports, sauf si vous les rendez spécifiquement disponibles.

  Si vous commencez ultérieurement à effectuer le suivi d’une nouvelle mesure de conversion, vous devez répéter cette tâche.

* (Facultatif) Automatiser la génération de rapports :

   * Si vous souhaitez générer régulièrement des données de rapport pour un incrément de temps spécifique, par exemple un [!UICONTROL Campaign Report] pour la semaine écoulée ou les 30 derniers jours, vous pouvez configurer des modèles de rapport [report](report-templates-manage.md) et planifier leur exécution quotidienne ou un jour spécifique de la semaine ou du mois. Chaque fois que l’exécution du rapport est planifiée, un nouveau rapport est généré. Vous avez la possibilité d’informer les adresses e-mail d’utilisateurs spécifiques des moteurs de recherche, des réseaux sociaux et de Commerce une fois le rapport terminé, en fonction des paramètres de notification [ configurés dans [!UICONTROL Notification Center]][Manage custom alerts]&#x200B;(/help/search-social-commerce/new-ui/notifications-manage.md).

   * Si vous souhaitez afficher des données de rapports quotidiens à jour dans une feuille de calcul au format personnalisé, avec ou sans tableaux croisés dynamiques et toutes les colonnes supplémentaires dont vous avez besoin pour effectuer d&#39;autres calculs, vous pouvez configurer un flux de feuille de calcul quotidien [flux de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Les flux de feuilles de calcul sont actualisés quotidiennement avec les dernières données de performances et continuent à conserver les données des dates précédentes. Pour configurer des flux de feuilles de calcul, vous devez d&#39;abord créer un modèle de feuille de calcul personnalisé dans [!DNL Microsoft Excel]. Vous avez la possibilité d’informer les adresses e-mail d’utilisateurs spécifiques des moteurs de recherche, des réseaux sociaux et de Commerce lorsqu’un fichier de flux est disponible, en fonction des paramètres de notification [ configurés dans [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md).

   * Si vous souhaitez recevoir des rapports de base et avancés à un emplacement FTP, vous pouvez configurer l’accès [FTP aux rapports de base et avancés](/help/search-social-commerce/new-ui/reports/ftp-reports.md) en demandant un compte FTP et en configurant des modèles de rapport selon une convention de nommage spécifique.

>[!MORELIKETHIS]
>
>* [À propos des rapports ](report-about.md)
>* [Données utilisées pour les rapports](data-used-for-reports.md)
