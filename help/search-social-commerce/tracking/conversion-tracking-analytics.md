---
title: Suivi des conversions Adobe Analytics
description: Découvrez comment utiliser le suivi de conversion Adobe Analytics pour vos campagnes dans Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Suivi des conversions Adobe Analytics

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Pour les annonceurs disposant d’une intégration Adobe Advertising-Adobe Analytics, Advertising Cloud peut connecter vos clics publicitaires et vos impressions aux mesures d’engagement et de conversion du site suivies par [!DNL Analytics] lorsque vous utilisez un paramètre de redirection avec jeton (`ef_id`) dans vos URL de suivi des clics pour vos [unités d’offre](/help/search-social-commerce/glossary.md#a-b). Les données [!DNL Analytics] sont automatiquement envoyées à Advertising Cloud via un fichier de flux quotidien.

Pour plus d’informations sur l’intégration, voir &quot;[Présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot;.

>[!PREREQUISITES]
>
> Les fuseaux horaires dans le compte publicitaire Search, Social et Commerce, les suites de rapports [!DNL Analytics] et les comptes de réseau publicitaire doivent correspondre. S’ils ne correspondent pas, des écarts de données se produisent sur l’ensemble des systèmes.

## Présentation de l’implémentation

1. Dans [!DNL Analytics], votre équipe de mise en oeuvre de Search, Social et Commerce modifie les paramètres de configuration suivants pour chaque suite de rapports :

   * L’expiration de `ef_id` [!DNL eVar] est modifiée afin de correspondre à l’intervalle de recherche en amont des clics de l’annonceur pour l’Adobe Advertising.

   * Identifiant utilisateur de l’Adobe Advertising.

   * Événements standard et personnalisés à utiliser pour l’optimisation.

1. Dans Search, Social et Commerce, votre équipe de mise en oeuvre :

   1. Synchronise la hiérarchie des comptes de réseau publicitaire existants dans Search, Social et Commerce.

   1. Ajoute des redirections avec jeton &quot;`ef_id`&quot; transmis aux URL de suivi et les publie sur le réseau publicitaire.

   Cette étape ajoute un préfixe à une redirection vers le serveur de suivi d’Adobe Advertising (à l’exception des publicités [!DNL Google Ads] et [!DNL Microsoft Advertising] dans les navigateurs qui prennent en charge le suivi parallèle) et ajoute un paramètre &quot;ef_id&quot; renseigné dynamiquement à l’URL au moment du clic publicitaire. Lorsque le suivi parallèle s’applique, les utilisateurs finaux sont envoyés directement de votre publicité vers votre URL finale, et l’URL de votre modèle de suivi (avec mesure des clics) est chargée en arrière-plan.

Une fois l’intégration terminée, Search, Social et Commerce reçoit automatiquement toutes les données d’événement sur la page suivies dans [!DNL Analytics] pour les suites de rapports qui ont été configurées.

>[!MORELIKETHIS]
>
>* [Options de suivi des conversions](conversion-tracking-about.md)
