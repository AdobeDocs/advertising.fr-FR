---
title: "Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et props"
description: "Configurer des mesures d’événement de succès personnalisées à l’aide de [!DNL eVar]- et [!DNL prop]données de niveau 1."
feature: Integration with Adobe Analytics, Conversions
source-git-commit: 71ffd021b31154a2ed2a522049f656a13d364d00
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et [!DNL props]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Vous pouvez utiliser les mesures d’événement de succès pour optimiser DSP modules et les campagnes Search, Social et Commerce en fonction des données de site Adobe Analytics qui correspondent le mieux aux objectifs de votre marque. Vous pouvez configurer des mesures d’événement de succès personnalisées en fonction de vos [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) et [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) par l’entonnoir [!DNL eVar]- et [!DNL prop]données de niveau -niveau dans un événement. Autre [!DNL Analytics] les mesures, y compris les mesures de conversion standard, personnalisées et réservées, ainsi que les mesures de trafic, sont automatiquement disponibles dans DSP et dans Search, Social et Commerce.

![Exemple d’utilisation](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Exemple d’utilisation")

La plupart des tâches suivantes doivent être effectuées par une [!DNL Analytics] administrateur ou autre utilisateur. Si vous avez besoin d’aide, contactez (DSP utilisateurs) l’équipe d’assistance technique DSP à l’adresse `adcloud_support@adobe.com` ou (Utilisateurs de Search, Social et Commerce) votre équipe de compte d’Adobe.

1. Dans [!DNL Analytics], [création d’un événement de succès d’espace réservé](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Utilisez les paramètres supplémentaires suivants :

   **Type :** `Counter`

   **Polarité :**  both `Up is Good` ou `Up is Bad`

   **Visibilité :** `Visible Everywhere`

   **Enregistrement d’événement unique :** `Always Record Event`

   **Participation :** `Enabled`

   Vous n’avez pas besoin de mettre en oeuvre le nouvel événement sur le site web de votre marque, car il utilise des données existantes déjà capturées.

1. Création et validation d’une règle de traitement dans [!DNL Analytics]:

   >[!NOTE]
   >
   >Uniquement [!DNL Analytics] les administrateurs de compte peuvent créer des règles de traitement, sauf s’ils ont accordé des autorisations à des non-administrateurs.

   1. [Création d’une règle de traitement](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), à l’aide de la configuration suivante :

      * Pour la condition qui doit être remplie, spécifiez la variable [!DNL eVars] ou [!DNL props].

        Vous pouvez configurer des niveaux de granularité supplémentaires si nécessaire afin de vous assurer que les événements les plus précis sont créés.

        >[!TIP]
        >
        >Il est recommandé d’utiliser un seul [!DNL eVar] ou [!DNL prop].

      * Pour l’action, sélectionnez **Définir un événement** et sélectionnez l’événement d’espace réservé.

   1. Dans [!DNL Analytics] [!DNL Analysis Workspace], [création d’un projet](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) et extrayez le nouvel événement dans un tableau à structure libre pour vous assurer que les données sont renseignées pour la variable [!DNL eVar] ou [!DNL prop] mesure.

1. Contactez votre équipe de compte d’Adobe pour synchroniser la nouvelle mesure dans Adobe Advertising.

Une fois la mesure disponible, vous pouvez l’utiliser pour créer un objectif, que vous pouvez ensuite affecter à un portefeuille de recherche, de réseaux sociaux et de commerce ou utiliser comme [objectif personnalisé](/help/dsp/optimization/custom-goal-about.md) pour un package DSP.

Pour plus d’informations sur la création d’objectifs, consultez le chapitre &quot;Objectifs&quot; du Guide d’optimisation, disponible dans Search, Social et Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Données en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->