---
title: Suivi des conversions Adobe Analytics
description: Découvrez comment utiliser le suivi des conversions Adobe Analytics pour vos campagnes dans Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: a6dc9edb12484499069a68222a3007ae08d9dfea
workflow-type: tm+mt
source-wordcount: '297'
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

   * L’expiration du [!DNL eVar] de `ef_id` est modifiée pour correspondre à l’intervalle de recherche en amont de clics de l’annonceur pour l’Adobe Advertising.

   * ID d’utilisateur Adobe Advertising.

   * Événements standard et personnalisés à utiliser pour l’optimisation.

1. Dans Search, Social et Commerce, votre équipe d’implémentation :

   1. Synchronise la hiérarchie des comptes de réseau publicitaire existants dans Search, Social et Commerce.

   1. Ajoute des redirections avec passage du jeton « `ef_id` » vers les URL de tracking et les publie sur le réseau publicitaire.

   Cette étape ajoute une redirection au serveur de suivi d’Adobe Advertising (à l’exception des annonces [!DNL Google Ads] et [!DNL Microsoft Advertising] dans les navigateurs qui prennent en charge le suivi parallèle) et ajoute un paramètre « ef_id » renseigné dynamiquement à l’URL au moment du clic sur l’annonce. Lorsque le suivi parallèle s’applique, les utilisateurs finaux sont envoyés directement de votre publicité à votre URL finale et votre URL de modèle de suivi (avec la mesure des clics) est chargée en arrière-plan.

Une fois l’intégration terminée, Search, Social et Commerce reçoit automatiquement toutes les données d’événement sur la page suivies dans [!DNL Analytics] pour les suites de rapports qui ont été configurées.

>[!MORELIKETHIS]
>
>* [Options de suivi des conversions](conversion-tracking-about.md)
