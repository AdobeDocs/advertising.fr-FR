---
title: Conditions préalables et informations clés pour la mise en oeuvre de  [!DNL Analytics for Advertising]
description: Conditions préalables et informations clés pour la mise en oeuvre de  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Conditions préalables et informations clés pour la mise en oeuvre de [!DNL Analytics for Advertising]

*Annonceurs avec Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

Consultez les informations suivantes avant d’intégrer Adobe Advertising à Adobe Analytics.

## Conditions requises pour la création de rapports de données d’Adobe Advertising dans [!DNL Analytics]

* L’une des options suivantes :
   * SDK Web Adobe Experience Platform : `alloy.js`
   * Service Experience Cloud Identity : `visitorAPI.js` version 2.0 ou ultérieure
* Toute version d’Adobe Analytics (y compris [!DNL Prime], [!DNL Premium] ou [!DNL Ultimate])
* Adobe Analytics : `appMeasurement.js` version 2.1 ou ultérieure
* (Clients Advertising DSP) [Fragment de code JavaScript Advertising DSP](javascript.md) déployé dans vos pages web pour suivre les visites d’affichage publicitaire.

>[!TIP]
>
>Pour améliorer la fidélité des données, utilisez la version la plus récente de chaque bibliothèque.

## Conditions requises pour le partage de segments Analytics avec Adobe Advertising

* Service Experience Cloud Identity : `visitorAPI.js` version 2.1 ou ultérieure
* Adobe Analytics : `appMeasurement.js` version 1.8 ou ultérieure

## Conditions requises pour la création de rapports de données [!DNL Analytics] en Adobe Advertising

Fournissez les informations suivantes à l’équipe de mise en oeuvre d’Adobe Advertising :

* L’identifiant de suite de rapports [!DNL Analytics] à utiliser pour la création de rapports sur l’activité de média payant et pour alimenter l’activité du site en vue de l’optimisation et de la création de rapports dans Adobe Advertising
* ID d’organisation Experience Cloud de l’entreprise (ID d’organisation).

Vous trouverez ces deux ID dans l’onglet [Résumé du débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=fr).

![Écran récapitulatif des Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Données en Adobe Advertising {#lookback-a4adc}

Comme les données [!DNL Analytics] sont envoyées à Adobe Advertising pour la création de rapports et l’optimisation, elles sont soumises aux règles d’attribution, y compris les intervalles de recherche en amont des impressions et des clics, qui sont configurés pour l’annonceur dans Adobe Advertising.

![Paramètres de l’intervalle de recherche en amont au niveau de l’annonceur dans Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising de l’intervalle de recherche en amont des clics d’attribution : nombre de jours après le premier clic au cours duquel le clic peut être attribué à une conversion. Par défaut, cette valeur est de 60 jours ; la valeur maximale est de 90 jours.
* Adobe Advertising de la période de recherche en amont des impressions : nombre de jours après une impression publicitaire au cours de laquelle l’impression peut être attribuée à une conversion. Par défaut, cette valeur est de 14 jours ; la valeur maximale est de 30 jours.

  >[!NOTE]
  >
  > L’intervalle de recherche en amont des impressions est spécifique aux rapports d’Adobe Advertising et non [!DNL Analytics for Advertising].

[!DNL Analytics for Advertising] JavaScript utilise ces paramètres pour déterminer le délai depuis lequel une entrée d’affichage publicitaire ou de clic publicitaire sur le site est considérée comme valide. Pour plus d’informations sur la manière dont les affichages publicitaires et les clics publicitaires sont déterminés, voir &quot;[ID d’Adobe Advertising utilisés par Analytics](ids.md)&quot;.

## Adobe Advertising de données dans [!DNL Analytics]

[!DNL Analytics] définit des identifiants d’Adobe Advertising (AMO ID) dans l’accès Analytics, soumis au paramètre de persistance [!DNL eVar] de l’annonceur, qui s’applique à la fois aux clics publicitaires et aux affichages publicitaires. Le paramètre de persistance est configuré sur le serveur principal Adobe Advertising et votre équipe de compte d’Adobe peut le modifier.

* [!DNL Analytics for Advertising] [!DNL eVar] Expiration : 60 jours par défaut pour les AMO ID

>[!NOTE]
>
>Pour segmenter les données pour une autre période, vous pouvez [&#x200B; configurer des segments personnalisés &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=fr) avec différentes intervalles de recherche en amont dans Analysis Workspace.

## Environnements publicitaires pris en charge

* Rechercher
* Affichage
* Vidéo
* Vidéo en ligne
* Télévision connectée
* Native

Contactez votre équipe de compte Adobe pour connaître les derniers environnements publicitaires pris en charge dans chaque canal.

## Informations à connaître avant l’implémentation

* L’équipe de mise en oeuvre de l’Adobe Advertising configure l’intégration.

* Aucun coût supplémentaire n’est facturé pour cette intégration, et les appels au serveur ne génèrent pas non plus de [!DNL Analytics] ou de frais d’Adobe Advertising supplémentaires.

* [!DNL Analytics for Advertising] est indépendant du serveur de publicités : un affichage ou un clic publicitaire peut survenir à partir de n’importe quel serveur de publicités et les identifiants appropriés sont générés lors de l’entrée sur le site.

* L’intégration transmet uniquement [!DNL Analytics] événements standard et personnalisés à Adobe Advertising pour optimiser l’offre des efforts publicitaires et de médias payants ultérieurs. Il ne transmet pas [!DNL Analytics] segments, mesures calculées et [!DNL eVars] à l’Adobe Advertising pour l’optimisation de l’offre.

* Adobe Advertising crée des identifiants persistants dans [!DNL Analytics] en fonction de la dernière publicité sur laquelle l’utilisateur a cliqué ou consultée avant d’entrer sur le site, en fonction des [fenêtres de recherche en amont des clics et des affichages publicitaires](#lookback-a4adc) configurées dans Adobe Advertising. Si le profil d’un visiteur du site comporte les deux types d’interactions d’entrée sur le site et que le clic se trouve pendant la période de recherche arrière, l’identifiant de clic publicitaire du visiteur remplace l’identifiant d’affichage publicitaire pour la création de rapports sur le site.

* Le suivi de conversion [!DNL Analytics for Advertising] dans Adobe Analytics utilise une période de recherche en amont de suivi configurable (60 jours par défaut). Les rapports d’Adobe Advertising reflètent les conversions et l’engagement du site tout au long de cette période de recherche arrière de suivi.

* Tous les types d’annonces sont pris en charge. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] les conversions sont actuellement suivies et attribuées uniquement à un visiteur sur le même appareil.

* [!DNL Analytics for Advertising] ne prend pas en charge les conversions d’affichage publicitaire in-app.

* Le suivi des affichages publicitaires n’est pas pris en charge pour les annonceurs qui utilisent une implémentation de transfert côté serveur de [!DNL Analytics].

### ID supplémentaire

Une fois le service Identity Experience Cloud mis en oeuvre pour un site, les accès qui contiennent des données de [!DNL Analytics] ou un Adobe Advertising contiennent un ID supplémentaire.

Exemple : `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Pour une intégration des données exacte, tous les appels d’Adobe Advertising utilisés par une activité [!DNL Analytics for Advertising] pour diffuser du contenu ou enregistrer la mesure d’objectif doivent avoir un accès [!DNL Analytics] correspondant partageant le même ID supplémentaire.

Lorsque vous effectuez un dépannage dans [!DNL Analytics], veillez à confirmer que l’ID supplémentaire est présent pour les accès [!DNL Analytics]. Dans le [débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=fr), vous pouvez voir cet ID dans l’onglet Adobe Advertising comme paramètre `sdid`.

>[!NOTE]
>
> Cette implémentation fonctionne de la même manière que l’intégration [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Code JavaScript pour Analytics pour Advertising](/help/integrations/analytics/javascript.md)
