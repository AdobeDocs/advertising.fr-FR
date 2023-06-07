---
title: Suivi des conversions Adobe Analytics
description: Découvrez comment utiliser le suivi de conversion Adobe Analytics pour vos campagnes dans Adobe Advertising.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Suivi des conversions Adobe Analytics

*Annonceurs avec une intégration Advertising-Adobe Analytics Adobe uniquement*

Pour les annonceurs disposant d’une intégration Advertising-Adobe Analytics Adobe, Advertising Cloud peut connecter vos clics publicitaires et vos impressions avec les mesures d’engagement et de conversion du site suivies par [!DNL Analytics] lorsque vous utilisez une redirection avec jeton (`ef_id` ) dans vos URL de suivi des clics pour votre [enchères](/help/search-social-commerce/glossary.md#a-b). Le [!DNL Analytics] les données sont automatiquement envoyées à Advertising Cloud par le biais d’un fichier de flux quotidien.

Voir &quot;[Présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html)&quot; pour plus d’informations sur l’intégration.

>[!PREREQUISITES]
>
> Fuseaux horaires dans le compte publicitaire Search, Social &amp; Commerce, le [!DNL Analytics] les suites de rapports et les comptes de réseau publicitaire doivent correspondre. S’ils ne correspondent pas, les écarts de données existent entre les systèmes.

## Présentation de l’implémentation

1. Dans [!DNL Analytics], votre équipe de mise en oeuvre de Search, Social et Commerce modifie les paramètres de configuration suivants pour chaque suite de rapports :

   * L’expiration de la variable `ef_id` L’eVar a été modifié pour correspondre à l’intervalle de recherche en amont des clics de l’annonceur pour Adobe Advertising.

   * Identifiant utilisateur Adobe Advertising.

   * Événements standard et personnalisés à utiliser pour l’optimisation.

1. Dans Search, Social et Commerce, votre équipe d’implémentation :

   1. Synchronise la hiérarchie des comptes de réseau publicitaire existants dans Search, Social et Commerce.

   1. Ajoute des redirections avec &quot;`ef_id`&quot;jeton transmettant aux URL de suivi et les publiant sur le réseau publicitaire.
   Cette étape préfixe une redirection vers le serveur de suivi Adobe Advertising (sauf pour [!DNL Google Ads] et [!DNL Microsoft Advertising] publicités dans les navigateurs qui prennent en charge le suivi parallèle) et ajoute un paramètre &quot;ef_id&quot; renseigné dynamiquement à l’URL au moment du clic publicitaire. Lorsque le suivi parallèle s’applique, les utilisateurs finaux sont envoyés directement de votre publicité vers votre URL finale, et l’URL de votre modèle de suivi (avec mesure des clics) est chargée en arrière-plan.

Une fois l’intégration terminée, Search, Social et Commerce reçoit automatiquement toutes les données d’événement sur la page qui font l’objet d’un suivi dans [!DNL Analytics] pour les suites de rapports qui ont été configurées.

>[!MORELIKETHIS]
>
>* [Options de suivi des conversions](conversion-tracking-about.md)
