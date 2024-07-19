---
title: Tâches de configuration initiales des rapports
description: Découvrez comment rendre les mesures disponibles dans les rapports et comment automatiser les rapports.
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Tâches de configuration initiales des rapports

Les nouveaux utilisateurs doivent effectuer les tâches de configuration initiales suivantes :

* Rendez les mesures de conversion qui font l’objet d’un suivi par Adobe Advertising pour un annonceur [ disponibles pour les rapports et autres vues ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md) et, éventuellement, [ renommez l’une des mesures de conversion](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) affichées dans les en-têtes de colonne pour en faciliter la lecture.

  Les propriétés des transactions ne sont pas disponibles pour les rapports, sauf si vous les rendez spécifiquement disponibles.

  Si vous commencez par suivre une nouvelle mesure de conversion, vous devez répéter cette tâche.

* (Facultatif) Automatisez la génération des rapports :

   * Si vous souhaitez générer régulièrement des données de rapport pour un incrément temporel spécifique, comme [!UICONTROL Campaign Report] pour la dernière semaine ou les 30 derniers jours, vous pouvez configurer des [modèles de rapport](/help/search-social-commerce/reports/automation/templates/template-about.md) et programmer leur exécution quotidienne ou un jour spécifique de la semaine ou du mois. Chaque fois que l’exécution du rapport est planifiée, un nouveau rapport est généré. Vous avez la possibilité d’informer les adresses électroniques de certains utilisateurs de Search, Social et Commerce lorsque le rapport est terminé, en fonction des paramètres de notification [ configurés dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si vous souhaitez afficher des données de rapport quotidiennes à jour dans une feuille de calcul au format personnalisé, avec ou sans tableaux croisés dynamiques et toutes les colonnes supplémentaires dont vous avez besoin pour effectuer d’autres calculs, vous pouvez configurer un [flux de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) quotidien. Les flux de feuilles de calcul sont actualisés quotidiennement avec les dernières données de performances et conservent les données des dates précédentes. Pour configurer des flux de feuille de calcul, vous devez d’abord créer un modèle de feuille de calcul personnalisé dans [!DNL Microsoft Excel]. Vous avez la possibilité d’informer les adresses électroniques de certains utilisateurs de Search, Social et Commerce lorsqu’un fichier de flux est disponible, en fonction des paramètres de notification [ configurés dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si vous souhaitez recevoir des rapports de base et avancés sur un emplacement FTP, vous pouvez configurer l’ [accès FTP aux rapports de base et avancés](/help/search-social-commerce/reports/automation/ftp-reports.md) en demandant un compte FTP et en configurant des modèles de rapport à l’aide d’une convention de dénomination spécifique.

>[!MORELIKETHIS]
>
>* [À propos des rapports](report-about.md)
>* [Données utilisées pour les rapports](data-used-for-reports.md)
