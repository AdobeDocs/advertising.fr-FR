---
title: Nouveautés
description: Découvrez les mises à jour apportées aux intégrations entre Adobe Advertising et d’autres produits et services dans Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: 11bc1f3f5d38c204a512cbffa9a5c5faa6ae0ab4
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Nouveautés

Les fonctionnalités suivantes sont nouvelles ou récemment modifiées.

| Date | Fonctionnalité | Description | Pour plus d’informations |
| ---- | ------- | ----------- | -------------------- |
| Publié le 29 octobre 2024 | [!DNL Adobe Analytics for Advertising] | (Publicitaires avec des campagnes de performances [!DNL Adobe Analytics for Advertising] et [!DNL Microsoft Advertising] max.) Les données au niveau du groupe de ressources pour vos campagnes de performances max. sont désormais disponibles dans Adobe Analytics lorsque vous implémentez un nouveau paramètre AMO ID ([!DNL s_kwcid]) dans les URL de suivi pour vos campagnes de performances max. qui n’incluent pas de publicités et de mots-clés. Le suivi de la plupart des campagnes de performances maximales a déjà été migré vers le nouveau format. Pour les campagnes de performances maximales sans l’option de suivi [!UICONTROL Auto Upload] qui n’ont pas déjà été migrées vers le nouveau format, cependant, vous devez mettre à jour manuellement chaque suffixe de page d’entrée afin d’inclure le format AMO ID suivant :<br><br>`AL!%(userid)d!%(sid)d!%(creativeref)s!!!%(termid/orderid)d!!!%(campaignid)!%(adref)`<br><br>Les données Adobe Analytics de vos campagnes de performances maximales sont également disponibles dans Search, Social et Commerce. | Voir le nouveau [format AMO ID]((/help/integrations/analytics/ids.md #amo-id-format-search) et [quand et comment ajouter le paramètre à vos URL de suivi](/help/integrations/analytics/ids.md#amo-id-implement). |
| 13 novembre 2024 | [!DNL Analytics for Advertising] | (Publicitaires avec [!DNL Analytics for Advertising] et Adobe Customer Journey Analytics) Si vous utilisez des variables réservées pour capturer vos AMO ID et vos EF ID, vous pouvez vous préparer à une future intégration entre Adobe Advertising et Adobe Customer Journey Analytics en copiant vos variables réservées pour l’AMO ID et l’EF ID dans la [!DNL eVars] standard dès que possible. Cela permet la collecte de données historiques pour les AMO ID et les EF ID dès que vous terminez la tâche, et les données historiques seront disponibles pour une utilisation ultérieure. Votre équipe de compte d’Adobe vous informera si vous utilisez des variables réservées et devez effectuer cette tâche. | Voir &quot;[Collecter des données historiques pour les AMO ID et les EF ID à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)&quot;. |
| 16 décembre 2023 | Aide | Un nouveau document explique comment configurer des tests A/B dans [!DNL Target] pour le trafic de clics publicitaires provenant des publicités dans Search, Social et Commerce, ainsi que des conseils sur la mesure et la visualisation de vos tests dans [!DNL Analytics]. | Voir &quot;[Configuration de tests A/B dans Adobe Target pour les annonces Search, Social et Commerce](/help/integrations/target/ab-tests-search.md)&quot;. |
| 8 août 2023 | [!DNL Analytics for Advertising] | Certaines mesures d’événement de succès [!DNL Analytics], y compris les mesures de conversion standard, personnalisées et réservées, ainsi que les mesures de trafic, sont automatiquement disponibles dans DSP et dans Search, Social et Commerce. Désormais, vous pouvez également configurer vos propres mesures de succès en fonction de vos [!DNL Analytics] [!DNL eVars] et [!DNL props] existants en orientant les données des niveaux [!DNL eVar] et [!DNL prop] vers un événement de succès personnalisé. | Voir &quot;[Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;. |
| 13 juillet 2023 | Reporting | (DSP utilisateurs disposant de [!DNL Analytics for Advertising]) Les conversions d’affichages publicitaires pour les emplacements de télévision connectée (CTV) sont désormais incluses dans les données de conversion disponibles dans Adobe Analytics. | Voir la section &quot;Exemples d’utilisation de l’intégration&quot; dans &quot;[Présentation de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)&quot;. |
| 1er novembre 2022 | Aide | Un nouveau document explique comment mettre en oeuvre le partage de signal de clics et d’affichages publicitaires entre Advertising DSP et Adobe Target, configurer une activité de test A/B dans [!DNL Target] pour vos annonces DSP et configurer Adobe Analytics Analysis Workspace pour afficher les données de test. | Voir &quot;[Configuration de tests A/B dans Adobe Target pour Advertising DSP Ads](/help/integrations/target/ab-tests-dsp.md)&quot;. |
| 17 août 2022 | Aide | Un nouveau chapitre explique toutes les façons dont Adobe Advertising est intégré à Adobe Audience Manager. | Consultez le chapitre sur &quot;Intégration avec Adobe Audience Manager&quot;, y compris une présentation de &quot;[Adobe Advertising des intégrations avec Adobe Audience Manager](/help/integrations/audience-manager/overview.md)&quot;. |
| 27 avril 2021 | [!DNL Analytics for Advertising] | Découvrez pourquoi et comment ajouter des macros [!DNL Analytics for Advertising] à vos balises publicitaires [!DNL Google Campaign Manager 360] pour envoyer des données de clic à Adobe Analytics. | Voir &quot;[Ajouter [!DNL Analytics for Advertising] des macros à [!DNL Google Campaign Manager 360] Ajouter des balises](/help/integrations/analytics/macros-google-campaign-manager.md)&quot;. |
| 19 avril 2021 | [!DNL Analytics for Advertising] | Découvrez pourquoi et comment ajouter des macros à vos balises publicitaires [!DNL Flashtalking] pour envoyer des données de clic à Adobe Analytics. | Voir &quot;[Ajouter [!DNL Analytics for Advertising] des macros à [!DNL Flashtalking] Ajouter des balises](/help/integrations/analytics/macros-flashtalking.md)&quot;. |
| 27 octobre 2021 | [!DNL Analytics for Advertising] | Si votre entreprise souhaite passer de l’utilisation de la bibliothèque Adobe Analytics `visitorAPI.js` héritée à la bibliothèque [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) (`alloy.js`) pour la collecte de données, vous devez apporter quelques modifications pour activer le regroupement d’identifiants. | Voir &quot;[Utilisation de la  [!DNL Last Event Service] bibliothèque JavaScript avec Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md)&quot;. |
| 26 mai 2021 | Aide | Le chapitre &quot;[!DNL Analytics for Advertising]&quot; comprend désormais un sous-chapitre sur &quot;Utilisation de [!DNL Analytics Marketing Channels]&quot;. | Voir : &quot;[Principes de base des canaux marketing](/help/integrations/analytics/marketing-channels/mc-overview.md)&quot;, &quot;[Utilisation d’identifiants d’Adobe Advertising pour créer [!DNL Analytics Marketing Channels] Règles de traitement](/help/integrations/analytics/marketing-channels/mc-ids.md)&quot;, &quot;[Utilisation [!DNL Analytics Marketing Channels] de données d’Adobe Advertising](/help/integrations/analytics/marketing-channels/mc-ac-data.md)&quot; et &quot;[Pourquoi les données de canal peuvent varier entre l’Adobe Advertising et  [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)&quot;. |
| 26 mai 2021 | Aide | Ajout d’un lien vers tous les tutoriels vidéo sur [!DNL Analytics for Advertising] - | Voir : &quot;[Tutoriels vidéo sur les intégrations Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html)&quot;. |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
