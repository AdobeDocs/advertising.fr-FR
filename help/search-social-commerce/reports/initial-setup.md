---
title: Tâches de configuration initiales pour les rapports
description: Découvrez comment rendre les mesures disponibles dans les rapports et comment automatiser les rapports.
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
TQID: https://experienceleague.adobe.com/N50b-O0oFBV6ZMXcFx8gRvLs3M1hN696d43VGlgkg44
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# Tâches de configuration initiales pour les rapports

Les nouveaux utilisateurs doivent effectuer les tâches de configuration initiales suivantes :

* Rendez les mesures de conversion suivies par Adobe Advertising pour un annonceur [disponibles pour les rapports et d’autres vues](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md) et éventuellement [ renommez l’une des mesures de conversion]&#x200B;(/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) affichées dans les en-têtes de colonne pour en faciliter la lecture.

  Les propriétés des transactions ne sont pas disponibles pour les rapports, sauf si vous les rendez spécifiquement disponibles.

  Si vous commencez ultérieurement à effectuer le suivi d’une nouvelle mesure de conversion, vous devez répéter cette tâche.

* (Facultatif) Automatiser la génération de rapports :

   * Si vous souhaitez générer régulièrement des données de rapport pour un incrément de temps spécifique, par exemple un [!UICONTROL Campaign Report] pour la semaine écoulée ou les 30 derniers jours, vous pouvez configurer des modèles de rapport [report](/help/search-social-commerce/reports/automation/templates/template-about.md) et planifier leur exécution quotidienne ou un jour spécifique de la semaine ou du mois. Chaque fois que l’exécution du rapport est planifiée, un nouveau rapport est généré. Vous avez la possibilité d’informer les adresses e-mail d’utilisateurs spécifiques des moteurs de recherche, des réseaux sociaux et de Commerce une fois le rapport terminé, en fonction des paramètres de notification [&#x200B; configurés dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si vous souhaitez afficher des données de rapports quotidiens à jour dans une feuille de calcul au format personnalisé, avec ou sans tableaux croisés dynamiques et toutes les colonnes supplémentaires dont vous avez besoin pour effectuer d&#39;autres calculs, vous pouvez configurer un flux de feuille de calcul quotidien [flux de feuille de calcul](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Les flux de feuilles de calcul sont actualisés quotidiennement avec les dernières données de performances et continuent à conserver les données des dates précédentes. Pour configurer des flux de feuilles de calcul, vous devez d&#39;abord créer un modèle de feuille de calcul personnalisé dans [!DNL Microsoft Excel]. Vous avez la possibilité d’informer les adresses e-mail d’utilisateurs spécifiques des moteurs de recherche, des réseaux sociaux et de Commerce lorsqu’un fichier de flux est disponible, en fonction des paramètres de notification [&#x200B; configurés dans [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

   * Si vous souhaitez recevoir des rapports de base et avancés à un emplacement FTP, vous pouvez configurer l’accès [FTP aux rapports de base et avancés](/help/search-social-commerce/reports/automation/ftp-reports.md) en demandant un compte FTP et en configurant des modèles de rapport selon une convention de nommage spécifique.

>[!MORELIKETHIS]
>
>* [À propos des rapports &#x200B;](report-about.md)
>* [Données utilisées pour les rapports](data-used-for-reports.md)
