---
title: Présentation de l’intégration entre Adobe Advertising et Adobe Customer Journey Analytics
description: Découvrez les options d’intégration d’Adobe Advertising à Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: 37c0485189c9bf084d4051fec501a1b2128687ec
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Présentation de l’intégration entre Adobe Advertising et Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Annonceurs avec Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising est intégré à Adobe Customer Journey Analytics pour le partage de données et la création de rapports bidirectionnels. Vous disposez de deux options pour configurer l’intégration :

* Les annonceurs qui utilisent à la fois [!DNL Analytics for Advertising] et Customer Journey Analytics disposent des mêmes fonctionnalités que par le biais de [!DNL Analytics for Advertising], avec l’ajout de visualisations dans Customer Journey Analytics.

  Vous effectuerez toujours le suivi des événements de clic publicitaire à l’aide de Adobe Experience Platform Web SDK (`alloy.js`) ou de Adobe Experience Cloud Identity Service (`visitorAPI.js`). Les annonceurs qui utilisent Advertising DSP utiliseront toujours un fragment de code JavaScript pour effectuer le suivi des événements de visionnage. Les données disponibles dans Customer Journey Analytics incluent :

   * Données de performances des campagnes à partir d’Adobe Advertising dans Customer Journey Analytics

   * Activité et conversions du site suivies par [!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Meta] dans Customer Journey Analytics

   * Données d’attribution provenant de [!DNL Analytics] dans Adobe Advertising, où elles peuvent être utilisées à des fins d’optimisation et de création de rapports

  Dans ce cas d’utilisation, vous n’avez pas besoin d’effectuer d’étapes supplémentaires, à l’exception de la [collecte facultative de données historiques pour les ID AMO et EF à utiliser dans Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).

* (Fonctionnalité bêta à venir) Les annonceurs qui utilisent Customer Journey Analytics, mais pas [!DNL Analytics for Advertising], peuvent échanger nativement les données suivantes entre Adobe Advertising et Customer Journey Analytics en effectuant le suivi des clics publicitaires et des affichages publicitaires à l’aide de Adobe Experience Platform Web SDK (`alloy.js`). Les données sont disponibles aux niveaux de la campagne, du groupe publicitaire, du package, de l’emplacement et des mots-clés.

   * Données de performances des campagnes à partir d’Adobe Advertising dans Customer Journey Analytics

     **Remarque :** les données de [!DNL Apple] et [!DNL Tiktok] ne sont pas disponibles.

   * Activité et conversions du site suivies par [!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Meta] dans Customer Journey Analytics

   * Données d’attribution de Customer Journey Analytics dans Adobe Advertising, où elles peuvent être utilisées à des fins d’optimisation et de création de rapports

  **Remarque :** aucune donnée organique n&#39;est encore disponible.<!-- Does that belong somewhere up above? -->

  Dans ce cas d’utilisation, utilisez Web SDK pour effectuer le suivi des événements de site (à l’aide de cookies, d’adresses IP hachées ou d’identifiants universels) et attribuer les événements de site à l’activité de médias achetés dans [!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Meta], ainsi qu’à Adobe DSP. Vous utiliserez également Adobe Experience Platform pour la collecte de données.

## Comment lancer une intégration native entre Adobe Advertising et Customer Journey Analytics

Contactez l’équipe chargée de votre compte Adobe, qui effectuera la configuration initiale nécessaire pour commencer et qui vous aidera à planifier votre implémentation et l’utilisation des données en fonction des besoins de votre entreprise.

>[!MORELIKETHIS]
>
>* [Conditions préalables](prerequisites.md)
>* (Utilisateurs Adobe Analytics) [Collecter des données historiques pour les ID AMO et les ID EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
