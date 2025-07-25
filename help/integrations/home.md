---
title: Nouveautés
description: Découvrez les mises à jour des intégrations entre Adobe Advertising et d’autres produits et services dans Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: ae93aff0056e58fd4427620d2eab76330a73039c
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Nouveautés

Les fonctionnalités suivantes sont nouvelles ou ont été récemment modifiées.

| Date | Fonctionnalité | Description | Pour Plus D’Informations |
| ---- | ------- | ----------- | -------------------- |
| 26 Mars 2025 | [!DNL Adobe Analytics for Advertising] | (Annonceurs avec Search, Social et Commerce ; comptes [!DNL Microsoft Advertising] ; et [!DNL Adobe Analytics for Advertising]) Pour les comptes avec l’option de suivi [!UICONTROL Auto Upload], le format du paramètre AMO ID dans les suffixes de page de destination pour tous les types de campagne a été mis à jour au dernier format. Auparavant, les campagnes Performance Max pour la plupart des comptes étaient migrées vers le nouveau format.<br><br>Toutefois, pour les comptes sans option de suivi des [!UICONTROL Auto Upload] qui n’ont pas déjà été migrés vers le nouveau format, vous devez mettre à jour manuellement chaque suffixe de page de destination pour inclure le nouveau format d’identifiant AMO.<br><br>Format actuel : `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | Voir « [ Présentation de  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) » et les [ Formats d’ID AMO ](/help/integrations/analytics/ids.md#amo-id-formats). |
| 13 Novembre 2024 | [!DNL Analytics for Advertising] | (Annonceurs avec [!DNL Analytics for Advertising] et Adobe Customer Journey Analytics) Si vous utilisez des variables réservées pour capturer vos AMO ID et EF ID, vous pouvez vous préparer à une intégration future entre Adobe Advertising et Adobe Customer Journey Analytics en copiant dès que possible vos variables réservées pour l’AMO ID et l’EF ID dans des [!DNL eVars] standard. Cela permettra de collecter des données historiques pour les ID AMO et EF dès que vous aurez terminé la tâche, et les données historiques seront disponibles pour une utilisation ultérieure. L’équipe chargée de votre compte Adobe vous indiquera si vous utilisez des variables réservées et si vous devez effectuer cette tâche. | Voir « [Collecter des données historiques pour les ID AMO et les ID EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md) ». |
| Publié Le 29 Octobre 2024 | [!DNL Adobe Analytics for Advertising] | (Annonceurs avec des campagnes Performance Max [!DNL Adobe Analytics for Advertising] et [!DNL Microsoft Advertising]) Les données au niveau du groupe de ressources pour vos campagnes Performance Max sont désormais disponibles dans Adobe Analytics lorsque vous implémentez un nouveau paramètre AMO ID ([!DNL s_kwcid]) dans les URL de tracking pour vos campagnes Performance Max, qui n’incluent pas de publicités ni de mots-clés. Le suivi de la plupart des comptes avec des campagnes Performance Max a déjà été migré au nouveau format. Toutefois, pour les comptes disposant de campagnes Performance Max sans l’option de tracking [!UICONTROL Auto Upload] qui n’ont pas déjà été migrés au nouveau format, vous devez mettre à jour manuellement chaque suffixe de page de destination pour inclure le nouveau format d’identifiant AMO.<br><br>Les données Adobe Analytics pour vos campagnes de performances maximales sont également disponibles dans Search, Social et Commerce. | Découvrez le nouveau [format d’AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) et [ quand et comment ajouter le paramètre à vos URL de tracking](/help/integrations/analytics/ids.md#amo-id-implement). |
| 16 Décembre 2023 | Aide | Un nouveau document explique comment configurer des tests A/B dans [!DNL Target] pour le trafic de clics publicitaires provenant d’annonces dans Search, Social et Commerce. Il fournit également des conseils sur la manière de mesurer et de visualiser vos tests dans [!DNL Analytics]. | Voir « [Configuration des tests A/B dans Adobe Target pour les publicités Search, Social et Commerce](/help/integrations/target/ab-tests-search.md) ». |
| 8 Août 2023 | [!DNL Analytics for Advertising] | Certaines mesures d’événement de succès [!DNL Analytics], notamment les mesures de conversion standard, personnalisées et réservées, ainsi que les mesures de trafic, sont automatiquement disponibles dans DSP et dans Search, Social et Commerce. Désormais, vous pouvez également configurer vos propres mesures de succès en fonction de vos [!DNL Analytics] et [!DNL eVars] de [!DNL props] existants en canalisant les données de niveau [!DNL eVar] et [!DNL prop] vers un événement de succès personnalisé. | Voir « [Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md) ». |
| 13 Juillet 2023 | Création de rapports | (Utilisateurs de DSP avec [!DNL Analytics for Advertising]) Les conversions d’affichage publicitaire pour les emplacements de télévision connectée (CTV) sont désormais incluses dans les données de conversion disponibles dans Adobe Analytics. | Reportez-vous à la section « Exemples d’utilisation de l’intégration » de la section « [ Présentation d’ [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples) ». |
| 1 Novembre 2022 | Aide | Un nouveau document explique comment implémenter le partage de signaux de clics publicitaires et de vues publicitaires entre Advertising DSP et Adobe Target, configurer une activité de test A/B dans [!DNL Target] pour vos publicités DSP et configurer Adobe Analytics Analysis Workspace pour afficher les données de test. | Voir « [ Configuration de tests A/B dans Adobe Target pour Advertising DSP Ads ](/help/integrations/target/ab-tests-dsp.md) ». |
| 17 Août 2022 | Aide | Un nouveau chapitre explique toutes les façons dont Adobe Advertising est intégré à Adobe Audience Manager. | Consultez le chapitre « Intégration à Adobe Audience Manager », y compris une présentation de « [Intégrations Adobe Advertising à Adobe Audience Manager ](/help/integrations/audience-manager/overview.md) ». |
| 27 Avril 2021 | [!DNL Analytics for Advertising] | Découvrez pourquoi et comment ajouter des macros [!DNL Analytics for Advertising] à vos balises d’annonces [!DNL Google Campaign Manager 360] pour envoyer des données de clics à Adobe Analytics. | Voir « [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md) ». |
| 19 Avril 2021 | [!DNL Analytics for Advertising] | Découvrez pourquoi et comment ajouter des macros à vos balises d’annonces [!DNL Flashtalking] pour envoyer des données de clics à Adobe Analytics. | Voir « [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md) ». |
| 27 Octobre 2021 | [!DNL Analytics for Advertising] | Si votre organisation souhaite passer de l’ancienne bibliothèque `visitorAPI.js` Adobe Analytics à la bibliothèque [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr) (`alloy.js`) pour la collecte de données, vous devez apporter quelques modifications pour activer le regroupement des identifiants. | Voir « [ Utilisation de la bibliothèque JavaScript  [!DNL Last Event Service]  avec Adobe Experience Platform  [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md) ». |
| 26 Mai 2021 | Aide | Le chapitre « [!DNL Analytics for Advertising] » comprend désormais un sous-chapitre intitulé « Travailler en [!DNL Analytics Marketing Channels] ». | Voir : « [Principes fondamentaux des canaux marketing](/help/integrations/analytics/marketing-channels/mc-overview.md) », « [Utilisation des identifiants Adobe Advertising pour créer [!DNL Analytics Marketing Channels] traiter des règles](/help/integrations/analytics/marketing-channels/mc-ids.md) », « [Utilisation [!DNL Analytics Marketing Channels] avec des données Adobe Advertising ](/help/integrations/analytics/marketing-channels/mc-ac-data.md) » et « [Pourquoi les données de canal peuvent varier entre Adobe Advertising et  [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md) ». |
| 26 Mai 2021 | Aide | Ajout d’un lien vers tous les tutoriels vidéo sur [!DNL Analytics for Advertising]. | Voir : « [tutoriels vidéo sur les intégrations d’Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=fr) ». |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
