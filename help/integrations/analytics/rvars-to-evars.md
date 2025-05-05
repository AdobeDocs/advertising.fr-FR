---
title: Collecter des données historiques pour les identifiants AMO et EF à utiliser dans Adobe Customer Journey Analytics
description: Découvrez comment collecter des données historiques pour vos variables réservées dans Adobe Analytics pour une utilisation ultérieure dans Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
source-git-commit: 5b78ec0fc4c5ea4742cbb080b992bdb323fc9af3
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Collecter des données historiques pour les identifiants AMO et EF à utiliser dans Adobe Customer Journey Analytics

*Annonceurs avec [!DNL Analytics for Advertising] et Adobe Customer Journey Analytics uniquement*

Si vous utilisez des variables réservées pour capturer l’[ID AMO et l’ID EF](ids.md) pour votre intégration [!DNL Analytics for Advertising], vous pouvez vous préparer à une intégration future entre Adobe Advertising et [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-overview/cja-overview), qui est la solution [!DNL analytics] nouvelle génération d’Adobe, en copiant dès que possible vos variables réservées pour l’ID AMO et l’ID EF dans [standard [!DNL eVars]](https://experienceleague.adobe.com/fr/docs/analytics/components/dimensions/evar). Cela permet de collecter des données historiques pour les ID AMO et EF dès que vous avez terminé la tâche. L’équipe chargée de votre compte Adobe vous indiquera si vous utilisez des variables réservées et si vous devez effectuer cette tâche.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Pourquoi dois-je collecter des données historiques pour Customer Journey Analytics ?

Customer Journey Analytics vous permet de synchroniser les données de Adobe Experience Platform dans Adobe Analytics Analysis Workspace. Actuellement, le [!DNL Analytics Data Connector] à Experience Platform n’envoie pas de données pour les variables réservées de [!DNL Analytics] à Experience Platform. Par conséquent, les données des ID AMO et EF capturés par des variables réservées ne sont actuellement pas disponibles dans Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->,<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising prévoit une implémentation ultérieure avec Customer Journey Analytics. Une fois l’implémentation publiée, votre intégration [!DNL Analytics for Advertising] nécessite toujours de collecter les données de clics publicitaires<!-- Add back if we implement this:  and (DSP users) view-through data --> à l’aide du suivi des [!DNL Analytics], mais vous pourrez afficher vos données à la fois dans les <!-- (Analysis Workspace using data from Experience Platform)--> 1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> et 2\) Customer Journey Analytics si votre organisation dispose des deux produits. Lorsque la fonctionnalité sera publiée, Experience Platform commencera à collecter les données pour votre AMO ID et votre EF ID à utiliser dans Customer Journey Analytics, mais il n’existera aucune donnée historique antérieure à la date de publication.

Cependant, vous pouvez commencer à collecter des données pour vos AMO ID et EF ID <!-- [!DNL rVars] --> plus tôt en créant une simple [[!DNL Analytics] règle de traitement](https://experienceleague.adobe.com/fr/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) pour copier vos AMO ID et EF ID <!-- [!DNL rVars] --> dans [!DNL eVars] maintenant. Une fois la règle de traitement créée, vous commencerez à accumuler des données pour vos ID AMO et ID EF <!-- [!DNL rVars] --> qu’ils suivent les nouveaux événements. Les données historiques seront alors disponibles dans Customer Journey Analytics une fois l’implémentation disponible.

>[!NOTE]
>
>* Depuis le 28 février 2025, ce processus suit les données de clics publicitaires, mais pas les données de vues publicitaires.
>* Les règles de traitement sont appliquées uniquement aux nouvelles données reçues. Ils ne fonctionnent pas rétroactivement pour recueillir des données antérieures.

## Copiez vos variables réservées pour les ID AMO et EF dans [!DNL eVars]

Cette étape est manuelle et doit être effectuée pour chaque suite de rapports qui effectue le suivi des AMO ID et des EF ID <!-- [!DNL rVars] --> que vous prévoyez d’intégrer à Adobe Advertising à l’avenir.

1. [Créez une règle de traitement](https://experienceleague.adobe.com/fr/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) avec les paramètres suivants :

   * Sélectionnez la suite de rapports pour laquelle vous souhaitez migrer les données de <!-- [!DNL rVar] --> d’ID AMO et d’ID EF vers Experience Platform en vue de leur utilisation par Customer Journey Analytics.

   * Pour l’[!UICONTROL Rule Title], utilisez un nom explicite, tel que « Copier l’ID AMO et l’ID EF dans les eVars ».

   * Dans la section [!UICONTROL Always Execute] , ajoutez deux actions pour créer les eVars :

      * Pour le `AMO ID` :

         1. Sélectionnez **Remplacer la valeur de**.
         1. Sélectionnez *\&lt;l’eVar nouvelle/inutilisée\>*.
         1. Sélectionnez **Paramètre de chaîne de requête**.
         1. Saisissez `s_kwcid`.

        Exemple : ```Overwrite the value of rVar10 with Query String Parameter s_kwcid```

      * Pour le `EF ID` :

         1. Sélectionnez **Remplacer la valeur de**.
         1. Sélectionnez *\&lt;l’eVar nouvelle/inutilisée\>*.
         1. Sélectionnez **Paramètre de chaîne de requête**.
         1. Saisissez `ef_id`.

        Exemple : `Overwrite the value of rVar11 with Query String Parameter ef_id`

   * Pour la [!UICONTROL Reason for rule], utilisez une note descriptive telle que « L’AMO ID et l’EF ID seront transmis à AEP via le connecteur Adobe Analytics ».

1. Validez la règle de traitement enregistrée.

   Une fois la règle de traitement enregistrée, les données des `AMO ID` et des `AMO EF ID` <!-- the existing reserved variables --> doivent être identiques à celles des deux nouvelles eVars vers lesquelles elles sont copiées.

   Par exemple, si la nouvelle `eVar142` eVar est mappée à `amo.s_kwcid(Context Data)`, les données du `eVar142` et de la `AMO ID` doivent être identiques.

Pour plus d’informations sur l’application des règles de traitement, reportez-vous à « [Fonctionnement des règles de traitement](https://experienceleague.adobe.com/fr/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about) ».

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
