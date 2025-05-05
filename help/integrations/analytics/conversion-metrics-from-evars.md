---
title: Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars]  et de props
description: Configurez les mesures d’événement de succès personnalisées à l’aide des données de niveau  [!DNL eVar] et  [!DNL prop].
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: 91e8435ff00feca804dfa2f4c323f88ee31813ab
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et [!DNL props]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Vous pouvez utiliser les mesures d’événement de succès pour optimiser DSP modules et les campagnes Search, Social et Commerce en fonction des données de site Adobe Analytics qui correspondent le mieux aux objectifs de votre marque. Vous pouvez configurer des mesures d’événement de succès personnalisées en fonction de vos [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=fr) et [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html?lang=fr) existants en canalisant les données des niveaux [!DNL eVar] et [!DNL prop] dans un événement. D’autres mesures [!DNL Analytics], notamment des mesures de conversion standard, personnalisées et réservées, ainsi que des mesures de trafic, sont automatiquement disponibles dans DSP et dans Search, Social et Commerce.

![Exemple d’utilisation](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Exemple d’utilisation")

La plupart des tâches suivantes doivent être effectuées par un administrateur [!DNL Analytics] ou un autre utilisateur. Si vous avez besoin d’aide, contactez (DSP utilisateurs) l’équipe d’assistance technique DSP à l’adresse `adcloud_support@adobe.com` ou (utilisateurs de Search, Social et Commerce) votre équipe de compte d’Adobe.

1. Dans [!DNL Analytics], [créez un événement de succès d’espace réservé](https://experienceleague.adobe.com/fr/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event).

   Utilisez les paramètres supplémentaires suivants :

   **Type :** `Counter`

   **Polarité :** soit `Up is Good` soit `Up is Bad`

   **Visibilité :** `Visible Everywhere`

   **Enregistrement d’événement unique :** `Always Record Event`

   **Participation :** `Enabled`

   Vous n’avez pas besoin de mettre en oeuvre le nouvel événement sur le site web de votre marque, car il utilise des données existantes déjà capturées.

1. Créez et validez une règle de traitement dans [!DNL Analytics] :

   >[!NOTE]
   >
   >Seuls les administrateurs de compte [!DNL Analytics] peuvent créer des règles de traitement, sauf s’ils ont accordé des autorisations à des non-administrateurs.

   1. [Créez une règle de traitement](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=fr), à l’aide de la configuration suivante :

      * Pour la condition qui doit être remplie, spécifiez la condition [!DNL eVars] ou [!DNL props] requise.

        Vous pouvez configurer des niveaux de granularité supplémentaires si nécessaire afin de vous assurer que les événements les plus précis sont créés.

        >[!TIP]
        >
        >La bonne pratique consiste à n’utiliser qu’un [!DNL eVar] ou [!DNL prop].

      * Pour l’action, sélectionnez **Définir l’événement** et sélectionnez l’événement d’espace réservé.

   1. Dans [!DNL Analytics] [!DNL Analysis Workspace], [créez un projet](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=fr) et extrayez le nouvel événement dans un tableau à structure libre pour vous assurer que les données sont renseignées pour la mesure [!DNL eVar] ou [!DNL prop].

1. Contactez votre équipe de compte d’Adobe pour synchroniser la nouvelle mesure dans Adobe Advertising.

Une fois la mesure disponible, vous pouvez l’utiliser pour créer un objectif, que vous pouvez ensuite affecter à un portfolio Search, Social et Commerce ou utiliser comme [objectif personnalisé](/help/dsp/optimization/custom-goal.md) pour un module DSP.

Pour plus d’informations sur la création d’objectifs, consultez le chapitre &quot;Objectifs&quot; du Guide d’optimisation, disponible dans Search, Social et Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Données en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Afficher les mesures de conversion suivies pour un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
