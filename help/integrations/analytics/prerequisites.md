---
title: Conditions préalables et informations clés pour la mise en œuvre [!DNL Analytics for Advertising]
description: Conditions préalables et informations clés pour la mise en œuvre [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Conditions préalables et informations clés pour la mise en œuvre [!DNL Analytics for Advertising]

*Annonceurs avec DSP de publicité et[!DNL Advertising Search, Social, & Commerce]*

Consultez les informations suivantes avant d’intégrer Adobe Advertising à Adobe Analytics.

## Exigences relatives à la création de rapports Adobe données publicitaires dans [!DNL Analytics]

* L’une des options suivantes :
   * SDK Adobe Experience Platform Web : `alloy.js`
   * Experience Cloud Identity Service : `visitorAPI.js` version 2.0 ou ultérieure
* Toute version d’Adobe Analytics (y compris [!DNL Prime], [!DNL Premium]ou [!DNL Ultimate])
* Adobe Analytics : `appMeasurement.js` version 2.1 ou ultérieure
* (Publicité DSP clients) Un [extrait](javascript.md) de code de DSP JavaScript publicitaire déployé sur vos pages Web pour effectuer le suivi des visites affichées.

>[!TIP]
>
>Pour améliorer la fidélité des données, utilisez la version la plus récente de chaque bibliothèque.

## Conditions requises pour le partage de segments Analytics avec des publicités Adobe

* Experience Cloud Identity Service : `visitorAPI.js` version 2.1 ou ultérieure
* Adobe Analytics : `appMeasurement.js` version 1.8 ou supérieure

## Exigences relatives à la création de rapports [!DNL Analytics] de données dans Adobe Advertising

Fournissez à l’équipe de mise en œuvre d’Adobe Advertising les éléments suivants :

* Identifiant [!DNL Analytics] de suite de rapports à utiliser pour la création de rapports sur l’activité des médias payants et pour l’alimentation de l’activité du site afin l’optimisation et la création de rapports dans Adobe Advertising
* ID d’organisation (Org) Experience Cloud de la société.

Ces deux ID sont disponibles dans l’onglet [Résumé de Adobe Experience Cloud débogueur](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud écran récapitulatif du débogueur](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Données dans Adobe Advertising {#lookback-a4adc}

Étant donné que [!DNL Analytics] les données sont envoyées à Adobe Advertising à des fins de création de rapports et d’optimisation, les données sont soumises aux règles d’attribution, y compris les fenêtres d’impression et de recherche en amont des clics, configurées pour l’annonceur dans Adobe Advertising.

![Paramètres de l’intervalle de recherche en amont au niveau de l’annonceur dans Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Fenêtre de recherche en amont des clics d’attribution publicitaire : nombre de jours après le premier clic pendant lesquels le clic peut être attribué à une conversion. Par défaut, cette valeur est de 60 jours ; Le maximum est de 90 jours
* Adobe Intervalle de recherche en amont des impressions d’attribution publicitaire : nombre de jours après l’impression d’une publicité au cours desquels l’impression peut être attribuée à une conversion. Par défaut, cette valeur est de 14 jours ; Le délai maximal est de 30 jours

  >[!NOTE]
  >
  > L’intervalle de recherche en amont des impressions est spécifique à Adobe Publicité, pas [!DNL Analytics for Advertising]aux rapports.

Le [!DNL Analytics for Advertising] JavaScript utilise ces paramètres pour déterminer jusqu’où il faut considérer qu’une entrée d’affichage ou de clic publicitaire sur le site est valide. Pour plus d’informations sur la méthode de détermination des affichages publicitaires et des clics publicitaires, reportez-vous à la section « Adobe[ des identifiants publicitaires utilisés par Analytics](ids.md) ».

## Adobe des données Advertising dans [!DNL Analytics]

[!DNL Analytics] définit Adobe identifiants publicitaires (AMO ID) dans le Analytics accès, sous réserve du paramètre de persistance de [!DNL eVar] l’annonceur, qui s’applique à la fois aux clics publicitaires et aux affichages publicitaires. Le paramètre de persistance est configuré sur le serveur principal Adobe Advertising et votre équipe de compte Adobe peut le modifier.

* [!DNL Analytics for Advertising][!DNL eVar] expiration : 60 jours par défaut pour les identifiants AMO

>[!NOTE]
>
>Pour segmenter des données pour une période différente, vous pouvez [configurer des segments](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) personnalisés avec différentes fenêtres de recherche en amont dans Analysis Workspace.

## Environnements publicitaires pris en charge

* Rechercher
* Montrer
* Vidéo
* Vidéo en ligne
* Connected TV
* Indigène

Contactez votre équipe de compte Adobe pour connaître les derniers environnements publicitaires pris en charge dans chaque canal.

## Informations à connaître avant l’implémentation

* L’équipe de mise en œuvre d’Adobe Advertising configure l’intégration.

* Aucun coût supplémentaire n’est facturé pour cette intégration, et les appels au serveur n’entraînent pas de frais de publicité supplémentaires [!DNL Analytics] ou Adobe.

* [!DNL Analytics for Advertising] est indépendant du serveur publicitaire : un affichage ou un clic publicitaire peut se produire à partir de n’importe quel serveur publicitaire, et les identifiants appropriés sont générés lors de l’entrée sur le site.

* L’intégration transmet uniquement [!DNL Analytics] les événements standard et personnalisés à Adobe Advertising pour optimiser les enchères des médias payants et des efforts publicitaires ultérieurs. Il ne transmet [!DNL Analytics] pas les segments, les mesures calculées et [!DNL eVars] à Adobe Advertising pour l’optimisation des offres.

* Adobe Advertising crée des identifiants persistants en [!DNL Analytics] fonction de la dernière publicité sur laquelle l’utilisateur a cliqué ou qui a été consultée avant que l’utilisateur n’accède au site, en fonction des fenêtres](#lookback-a4adc) de recherche en amont de clic et d’affichage [configuré dans Adobe Advertising. Si un visiteur de site a les deux types d’interactions d’entrée de site dans son profil et que le clic est dans la période de recherche en arrière, l’ID de clic publicitaire du visiteur remplace l’ID d’affichage publicitaire pour les rapports de site.

* [!DNL Analytics for Advertising] Le suivi des conversions dans Adobe Analytics utilise une fenêtre rétroactive de suivi configurable (60 jours par défaut). Adobe Les rapports Advertising reflètent les conversions et l’engagement sur le site jusqu’à la fin de cette fenêtre de recherche en amont de suivi.

* Tous les types d’annonces sont pris en charge. Cependant, tous les environnements publicitaires ne sont pas pris en charge.

* [!DNL Analytics] Les conversions font actuellement l’objet d’un suivi et ne sont attribuées qu’à un visiteur utilisant le même appareil.

* [!DNL Analytics for Advertising] Ne prend pas en charge les conversions d’affichage publicitaire dans l’application.

* Le suivi des affichages publicitaires n’est pas pris en charge pour les annonceurs qui utilisent une implémentation de transfert côté serveur de [!DNL Analytics].

### ID supplémentaire

Une fois que le service Experience Cloud Identity est implémenté pour un site, les accès qui contiennent des données provenant de [!DNL Analytics] ou Adobe Advertising contiennent un ID supplémentaire.

Exemple: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Pour une intégration précise des données, tous les appels Adobe Advertising utilisés par une [!DNL Analytics for Advertising] activité pour fournir du contenu ou enregistrer la mesure d’objectif doivent avoir un accès correspondant [!DNL Analytics] qui partage le même ID supplémentaire.

Lors du dépannage dans [!DNL Analytics], veillez à confirmer que l’ID supplémentaire est présent pour [!DNL Analytics] les accès. Dans le [débogueur](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) Adobe Experience Cloud, vous pouvez voir cet ID dans l’onglet Adobe Publicités comme `sdid` paramètre.

>[!NOTE]
>
> Cette implémentation fonctionne de la même manière que l’intégration [!DNL Analytics for Target] .

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript Code pour Analytics pour la publicité](/help/integrations/analytics/javascript.md)
