---
title: Conditions préalables et informations clés pour la mise en œuvre  [!DNL Analytics for Advertising]
description: Conditions préalables et informations clés pour la mise en œuvre  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Conditions préalables et informations clés pour l’implémentation de [!DNL Analytics for Advertising]

*Annonceurs avec Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

Consultez les informations suivantes avant d’intégrer Adobe Advertising à Adobe Analytics.

## Conditions requises pour la création de rapports sur les données Adobe Advertising dans [!DNL Analytics]

* L’une des options suivantes :
   * Adobe Experience Platform Web SDK : `alloy.js`
   * Experience Cloud Identity Service : version `visitorAPI.js` 2.0 ou ultérieure.
* Toute version d’Adobe Analytics (y compris [!DNL Prime], [!DNL Premium] ou [!DNL Ultimate])
* Adobe Analytics : `appMeasurement.js` version 2.1 ou ultérieure
* (Clients Advertising DSP) Un [fragment de code Advertising DSP JavaScript](javascript.md) déployé dans vos pages web pour effectuer le suivi des visites publicitaires.

>[!TIP]
>
>Pour améliorer la fidélité des données, utilisez la version la plus récente de chaque bibliothèque.

## Conditions requises pour le partage de segments Analytics avec Adobe Advertising

* Experience Cloud Identity Service : version `visitorAPI.js` 2.1 ou ultérieure.
* Adobe Analytics : `appMeasurement.js` version 1.8 ou ultérieure

## Conditions requises pour la création de rapports [!DNL Analytics] les données dans Adobe Advertising

Fournissez les éléments suivants à l’équipe d’implémentation d’Adobe Advertising :

* Identifiant de suite de rapports [!DNL Analytics] à utiliser pour le reporting sur l’activité de média payant et pour alimenter l’activité du site à des fins d’optimisation et de création de rapports dans Adobe Advertising
* L’identifiant d’organisation Experience Cloud de l’entreprise (identifiant d’organisation).

Vous trouverez ces deux ID dans l’onglet [&#x200B; Résumé de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Écran Résumé d’Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] de données dans Adobe Advertising {#lookback-a4adc}

Comme [!DNL Analytics] données sont envoyées à Adobe Advertising à des fins de création de rapports et d’optimisation, elles sont soumises aux règles d’attribution, y compris les intervalles de recherche en amont d’impressions et de clics, configurés pour l’annonceur dans Adobe Advertising.

![paramètres de l’intervalle de recherche en amont au niveau de l’annonceur dans Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Intervalle de recherche en amont des clics d’attribution Adobe Advertising : nombre de jours après le premier clic pendant lesquels le clic peut être attribué à une conversion. Par défaut, cette valeur est de 60 jours ; la valeur maximale est de 90 jours
* Intervalle de recherche en amont des impressions d’attribution Adobe Advertising : nombre de jours après la survenue d’une impression publicitaire dans lequel l’impression peut être attribuée à une conversion. Par défaut, cette valeur est de 14 jours ; la valeur maximale est de 30 jours

  >[!NOTE]
  >
  > L’intervalle de recherche en amont d’impression est spécifique aux rapports d’Adobe Advertising et non de [!DNL Analytics for Advertising].

Le JavaScript [!DNL Analytics for Advertising] utilise ces paramètres pour déterminer la durée de validité d’une entrée d’affichage publicitaire ou d’un clic publicitaire sur le site. Pour plus d’informations sur la manière dont les affichages publicitaires et les clics publicitaires sont déterminés, voir « [Adobe Advertising ID utilisés par Analytics](ids.md) ».

## Données Adobe Advertising dans [!DNL Analytics]

[!DNL Analytics] définit les identifiants Adobe Advertising (AMO ID) dans l’accès Analytics, en fonction du paramètre de persistance des [!DNL eVar] de l’annonceur, qui s’applique à la fois aux clics publicitaires et aux affichages publicitaires. Le paramètre de persistance est configuré sur le serveur principal d’Adobe Advertising et votre équipe de compte Adobe peut le modifier.

* Expiration [!DNL Analytics for Advertising] [!DNL eVar] : 60 jours par défaut pour les ID AMO

>[!NOTE]
>
>Pour segmenter les données pour une période différente, vous pouvez [configurer des segments personnalisés](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) avec différents intervalles de recherche en amont dans Analysis Workspace.

## Environnements publicitaires pris en charge

* Rechercher
* Affichage
* Vidéo
* Vidéo en ligne
* TV connectée
* Natif

Contactez l’équipe chargée de votre compte Adobe pour connaître les derniers environnements publicitaires pris en charge dans chaque canal.

## Informations à connaître avant d’implémenter

* L’équipe d’implémentation d’Adobe Advertising configure l’intégration.

* Aucun coût supplémentaire n’est facturé pour cette intégration, de même que les appels au serveur n’entraînent pas de [!DNL Analytics] ou de frais Adobe Advertising supplémentaires.

* [!DNL Analytics for Advertising] est indépendant du serveur de publicités : un affichage publicitaire ou un clic publicitaire peut provenir de n’importe quel serveur de publicités et les identifiants appropriés sont générés lors de l’entrée sur le site.

* L’intégration transmet uniquement [!DNL Analytics] événements standard et personnalisés à Adobe Advertising pour l’optimisation des enchères des efforts publicitaires et des médias achetés suivants. Il ne transmet pas les segments de [!DNL Analytics], les mesures calculées et les [!DNL eVars] à Adobe Advertising pour l’optimisation des enchères.

* Adobe Advertising crée des identifiants persistants dans [!DNL Analytics] en fonction de la dernière publicité ayant fait l’objet d’un clic ou d’une consultation avant l’entrée de l’utilisateur sur le site, en fonction des intervalles de recherche en amont [clics et affichage publicitaire](#lookback-a4adc) configurés dans Adobe Advertising. Si un visiteur du site possède les deux types d’interactions d’entrée sur le site dans son profil et que le clic se situe dans la période de recherche en amont, l’ID de clic publicitaire du visiteur remplace l’ID d’affichage publicitaire pour les rapports sur le site.

* [!DNL Analytics for Advertising] suivi des conversions dans Adobe Analytics utilise un intervalle de recherche en amont configurable (60 jours par défaut). Les rapports Adobe Advertising reflètent les conversions et l’engagement du site jusqu’à la fin de cet intervalle de recherche en amont de suivi.

* Tous les types d’annonces sont pris en charge. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] conversions sont actuellement suivies et attribuées uniquement à un visiteur sur le même appareil.

* [!DNL Analytics for Advertising] ne prend pas en charge les conversions d’affichage publicitaire in-app.

* Le suivi des affichages publicitaires n’est pas pris en charge pour les annonceurs qui utilisent une implémentation du transfert côté serveur de [!DNL Analytics].

### ID supplémentaire

Une fois qu’Experience Cloud Identity Service est implémenté pour un site, les accès contenant des données provenant de [!DNL Analytics] ou d’Adobe Advertising contiennent un ID supplémentaire.

Exemple : `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Pour une intégration de données précise, tous les appels Adobe Advertising utilisés par une activité [!DNL Analytics for Advertising] pour diffuser du contenu ou enregistrer la mesure d’objectif doivent avoir un accès [!DNL Analytics] correspondant qui partage le même identifiant supplémentaire.

Lorsque vous effectuez un dépannage dans [!DNL Analytics], assurez-vous que l’ID supplémentaire est présent pour les accès [!DNL Analytics]. Dans [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), cet identifiant apparaît dans l&#39;onglet Adobe Advertising en tant que paramètre `sdid`.

>[!NOTE]
>
> Cette implémentation fonctionne de la même manière que l’intégration [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Code JavaScript pour Analytics for Advertising](/help/integrations/analytics/javascript.md)
