---
title: Tâches de configuration initiales des rapports
description: Découvrez comment rendre les mesures disponibles dans les rapports et comment automatiser les rapports.
exl-id: 0f55aae9-6898-4967-a377-190a13dff6fd
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Tâches de configuration initiales des rapports

Les nouveaux utilisateurs doivent effectuer les tâches de configuration initiales suivantes :

* Rendre les propriétés de transaction dont l’Adobe Advertising effectue le suivi pour un annonceur [disponibles pour les rapports et autres vues](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md)et éventuellement [renommer l’un des noms de propriété ;](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) qui s’affichent en en-têtes de colonne pour être lisibles.

  Les propriétés des transactions ne sont pas disponibles pour les rapports, sauf si vous les rendez spécifiquement disponibles.

  Si vous commencez plus tard à suivre une nouvelle propriété de transaction, vous devrez répéter cette tâche.

* (Facultatif) Automatisez la génération des rapports :

   * Si vous souhaitez générer régulièrement des données de rapport pour un incrément de temps spécifique, comme une [!UICONTROL Campaign Report] pour la dernière semaine ou les 30 derniers jours, vous pouvez configurer [modèles de rapport](/help/search-social-commerce/reports/automation/templates/template-about.md) et programmez leur exécution quotidienne ou un jour spécifique de la semaine ou du mois. Chaque fois que l’exécution du rapport est planifiée, un nouveau rapport est généré. Vous avez la possibilité d’informer les adresses électroniques de certains utilisateurs de Search, Social et Commerce une fois le rapport terminé, en fonction de la variable [paramètres de notification configurés dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si vous souhaitez afficher des données de rapport quotidiennes à jour dans une feuille de calcul au format personnalisé, avec ou sans tableaux croisés dynamiques et toutes les colonnes supplémentaires à effectuer, vous pouvez configurer un [flux de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Les flux de feuilles de calcul sont actualisés quotidiennement avec les dernières données de performances et conservent les données des dates précédentes. Pour configurer des flux de feuille de calcul, vous devez d’abord créer un modèle de feuille de calcul personnalisé dans [!DNL Microsoft Excel]. Vous avez la possibilité d’informer les adresses électroniques d’utilisateurs de Search, Social et Commerce spécifiques lorsqu’un fichier de flux est disponible, en fonction de la variable [paramètres de notification configurés dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si vous souhaitez recevoir des rapports de base et avancés à un emplacement FTP, vous pouvez configurer [Accès FTP aux rapports de base et avancés](/help/search-social-commerce/reports/automation/ftp-reports.md) en demandant un compte FTP et en configurant des modèles de rapport à l’aide d’une convention de dénomination spécifique.

>[!MORELIKETHIS]
>
>* [A propos des rapports](report-about.md)
>* [Données utilisées pour les rapports](data-used-for-reports.md)
