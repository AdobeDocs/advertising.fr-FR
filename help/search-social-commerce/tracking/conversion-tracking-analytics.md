---
title: Suivi des conversions Adobe Analytics
description: Découvrez comment utiliser le suivi des conversions Adobe Analytics pour vos campagnes dans Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
TQID: https://experienceleague.adobe.com/CM0S4RvR4RJ5Ylta5EJTdZh-VDDHYIfa7Qsd1Dm4D78
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 0%

---

# Suivi des conversions Adobe Analytics

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Pour les annonceurs disposant d’une intégration Adobe Advertising-Adobe Analytics, Advertising Cloud peut connecter vos clics et impressions publicitaires aux mesures d’engagement et de conversion du site suivies par [!DNL Analytics] lorsque vous utilisez une redirection avec jeton (paramètre de `ef_id`) dans vos URL de suivi des clics pour vos [unités d’enchères](/help/search-social-commerce/glossary.md#a-b). Les données [!DNL Analytics] sont automatiquement envoyées à Advertising Cloud via un fichier de flux quotidien.

Consultez « [Présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/fr/docs/advertising/integrations/analytics/overview){target="_blank"} » pour plus d’informations sur l’intégration.

>[!PREREQUISITES]
>
> Les fuseaux horaires du compte publicitaire Search, Social et Commerce, des suites de rapports [!DNL Analytics] et des comptes de réseau publicitaire doivent correspondre. S’ils ne correspondent pas, des variations de données se produisent entre les systèmes.

## Présentation de l’implémentation

1. Dans [!DNL Analytics], votre équipe d’implémentation Search, Social et Commerce modifie les paramètres de configuration suivants pour chaque suite de rapports :

   * L’expiration du `ef_id` [!DNL eVar] est modifiée pour correspondre à l’intervalle de recherche en amont de clic de l’annonceur pour Adobe Advertising.

   * L’identifiant utilisateur Adobe Advertising.

   * Événements standard et personnalisés à utiliser pour l’optimisation.

1. Dans Search, Social et Commerce, votre équipe d’implémentation :

   1. Synchronise la hiérarchie des comptes de réseau publicitaire existants dans Search, Social et Commerce.

   1. Ajoute des redirections avec passage du jeton « `ef_id` » vers les URL de tracking et les publie sur le réseau publicitaire.

   Cette étape ajoute une redirection au serveur de tracking Adobe Advertising (à l’exception des annonces [!DNL Google Ads] et [!DNL Microsoft Advertising] dans les navigateurs qui prennent en charge le tracking parallèle) et ajoute un paramètre « ef_id » renseigné dynamiquement à l’URL au moment du clic sur l’annonce. Lorsque le suivi parallèle s’applique, les utilisateurs finaux sont envoyés directement de votre publicité à votre URL finale et votre URL de modèle de suivi (avec la mesure des clics) est chargée en arrière-plan.

Une fois l’intégration terminée, Search, Social et Commerce reçoit automatiquement toutes les données d’événement sur la page suivies dans [!DNL Analytics] pour les suites de rapports qui ont été configurées.

>[!MORELIKETHIS]
>
>* [Options de suivi des conversions](conversion-tracking-about.md)
