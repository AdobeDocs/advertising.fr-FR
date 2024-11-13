---
title: Collecte de données historiques pour les AMO ID et les EF ID à utiliser dans Adobe Customer Journey Analytics
description: Découvrez comment collecter des données historiques pour vos variables réservées dans Adobe Analytics pour une utilisation ultérieure dans Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
source-git-commit: 4cd58fd995b3df9fb7837077108207ce910157c1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Collecte de données historiques pour les AMO ID et les EF ID à utiliser dans Adobe Customer Journey Analytics

*Annonceurs avec [!DNL Analytics for Advertising] et Adobe Customer Journey Analytics uniquement*

Si vous utilisez des variables réservées pour capturer l’ [AMO ID et l’ EF ID](ids.md) pour votre intégration [!DNL Analytics for Advertising], vous pouvez vous préparer à une future intégration entre Adobe Advertising et [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), qui est la solution [!DNL analytics] de nouvelle génération d’Adobe, en copiant vos variables réservées pour l’AMO ID et l’EF ID dans [standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) dès que possible. Cela permettra la collecte de données historiques pour les AMO ID et les EF ID dès que vous aurez terminé la tâche. Votre équipe de compte d’Adobe vous informera si vous utilisez des variables réservées et devez effectuer cette tâche.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Pourquoi dois-je collecter des données historiques pour Customer Journey Analytics ?

Customer Journey Analytics vous permet de synchroniser les données de Adobe Experience Platform dans Adobe Analytics Analysis Workspace. Actuellement, [!DNL Analytics Data Connector] à Experience Platform n’envoie pas de données pour les variables réservées de [!DNL Analytics] à Experience Platform. Par conséquent, les données des AMO ID et des EF ID capturés par des variables réservées ne sont actuellement pas disponibles dans Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising prévoit une mise en oeuvre future avec Customer Journey Analytics. Une fois l&#39;implémentation publiée, votre intégration [!DNL Analytics for Advertising] nécessite toujours que vous collectiez les données de clics publicitaires et (DSP utilisateurs) les données d&#39;affichage publicitaire à l&#39;aide du suivi [!DNL Analytics], mais vous pourrez afficher vos données dans les Customer Journey Analytics [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> et 2\) <!-- (Analysis Workspace using data from Experience Platform)--> si votre organisation possède les deux produits. Une fois la fonctionnalité publiée, l’Experience Platform commence à collecter des données pour votre AMO ID et votre EF ID en vue de les utiliser dans Customer Journey Analytics, mais aucune donnée historique n’existe avant la date de publication.

Cependant, vous pouvez commencer à collecter des données pour vos AMO ID et vos EF ID <!-- [!DNL rVars] --> plus tôt en créant une [[!DNL Analytics] règle de traitement](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) simple pour copier vos AMO ID et vos EF ID <!-- [!DNL rVars] --> dans [!DNL eVars] maintenant. Une fois la règle de traitement créée, vous commencerez à accumuler des données pour vos AMO ID et vos EF ID <!-- [!DNL rVars] --> dès qu’ils effectuent le suivi de nouveaux événements. Les données historiques seront alors disponibles dans Customer Journey Analytics une fois l’implémentation disponible.

>[!NOTE]
>
>Les règles de traitement ne s’appliquent qu’aux nouvelles données reçues. Ils ne travaillent pas rétroactivement à la collecte de données antérieures.

## Copiez les variables réservées pour les AMO ID et les EF ID dans [!DNL eVars].

Cette étape est manuelle et doit être effectuée pour chaque suite de rapports qui suit les AMO ID et les EF ID <!-- [!DNL rVars] --> que vous prévoyez d’intégrer à Adobe Advertising à l’avenir.

1. [Créez une règle de traitement](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) avec les paramètres suivants :

   * Sélectionnez la suite de rapports pour laquelle vous souhaitez migrer les données AMO ID et EF ID <!-- [!DNL rVar] --> vers Experience Platform pour une utilisation par Customer Journey Analytics.

   * Pour le [!UICONTROL Rule Title], utilisez un nom descriptif, tel que &quot;Copier l’AMO ID et l’EF ID dans les eVars&quot;.

   * Dans la section [!UICONTROL Always Execute] , ajoutez deux actions pour créer les eVars :

      * Pour le `AMO ID` : ```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

      * Pour le `EF ID` : ```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * Pour [!UICONTROL Reason for rule], utilisez une note descriptive, telle que &quot;AMO ID et EF ID seront transportés vers AEP via Adobe Analytics Connector&quot;.

1. Validez la règle de traitement enregistrée.

   Une fois la règle de traitement enregistrée, les données des variables `AMO ID` et `AMO EF ID` <!-- the existing reserved variables --> doivent être identiques aux données des deux nouvelles eVars auxquelles elles sont copiées.

   Par exemple, si le nouvel eVar `eVar142` est mappé sur `amo.s_kwcid(Context Data)`, les données de `eVar142` et de `AMO ID` doivent être identiques.

Pour plus d’informations sur l’application des règles de traitement, voir &quot;[Fonctionnement des règles de traitement](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)&quot;.

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
