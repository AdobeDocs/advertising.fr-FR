---
title: Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et props
description: Configurer des mesures d’événement de succès personnalisées à l’aide d’ [!DNL eVar]- et [!DNL prop]Données au niveau de l’élément.
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: a0d5bc1791f5d05e2cbdeab58e1943f4d494b53f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Création de mesures de conversion à partir d’Adobe Analytics [!DNL eVars] et [!DNL props]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Vous pouvez utiliser les mesures d’événement de succès pour optimiser les packages DSP et les campagnes Search, Social et Commerce en fonction des données de site Adobe Analytics qui correspondent le mieux aux objectifs de votre marque. Vous pouvez configurer des mesures d’événement de succès personnalisées en fonction de vos [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) et [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) par entonnoir [!DNL eVar]- et [!DNL prop]Données au niveau du dossier dans un événement. Autres frais [!DNL Analytics] les mesures , y compris les mesures de conversion et les mesures de trafic standard, personnalisées et réservées, sont automatiquement disponibles dans DSP et dans Search, Social et Commerce.

![Exemple d’utilisation](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Exemple d’utilisation")

La plupart des tâches suivantes doivent être effectuées par un [!DNL Analytics] administrateur ou autre utilisateur. Si vous avez besoin d’aide, contactez (les utilisateurs de DSP) l’équipe d’assistance technique de DSP à l’adresse `adcloud_support@adobe.com` ou (utilisateurs de Search, Social et Commerce) votre équipe de compte d’Adobe.

1. In [!DNL Analytics], [créer un événement de succès d’espace réservé](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Utilisez les paramètres supplémentaires suivants :

   **Type :** `Counter`

   **Polarité :**  soit `Up is Good` ou `Up is Bad`

   **Visibilité :** `Visible Everywhere`

   **Enregistrement unique d’événement :** `Always Record Event`

   **Participation :** `Enabled`

   Vous n’avez pas besoin d’implémenter le nouvel événement sur le site web de votre marque, car il utilise des données existantes déjà capturées.

1. Création et validation d’une règle de traitement dans [!DNL Analytics]:

   >[!NOTE]
   >
   >Uniquement [!DNL Analytics] les administrateurs de compte peuvent créer des règles de traitement, sauf s’ils ont accordé une autorisation à des non-administrateurs.

   1. [Création d’une règle de traitement](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), en utilisant le paramétrage suivant :

      * Pour la condition qui doit être remplie, spécifiez la valeur requise. [!DNL eVars] ou [!DNL props].

        Vous pouvez configurer d’autres niveaux de granularité selon vos besoins pour vous assurer que les événements les plus précis sont créés.

        >[!TIP]
        >
        >La bonne pratique consiste à n’en utiliser qu’un seul [!DNL eVar] ou [!DNL prop].

      * Pour l’action, sélectionnez . **Définir l’événement** et sélectionnez l’événement d’espace réservé.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [créer un projet](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) et extrayez le nouvel événement dans un tableau à structure libre pour vous assurer que les données sont renseignées pour le . [!DNL eVar] ou [!DNL prop] métrique.

1. Contactez l’équipe de votre compte d’Adobe pour synchroniser la nouvelle mesure avec l’Adobe Advertising.

Une fois la mesure disponible, vous pouvez l’utiliser pour créer un objectif, que vous pouvez ensuite affecter à un portfolio Search, Social et Commerce ou utiliser comme [objectif personnalisé](/help/dsp/optimization/custom-goal.md) pour un package DSP.

Pour plus d’informations sur la création d’objectifs, consultez le chapitre du guide d’optimisation intitulé « Objectifs », disponible dans Search, Social et Commerce.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Données en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Affichage des mesures de conversion suivies pour un annonceur](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
