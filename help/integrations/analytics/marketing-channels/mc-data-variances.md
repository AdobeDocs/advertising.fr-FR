---
title: Pourquoi les données de canal peuvent-elles varier entre Adobe Advertising et  [!DNL Marketing Channels]
description: Découvrez pourquoi les données de canal suivies par l’ID AMO peuvent différer des données de canal suivies par  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Pourquoi les données de canal peuvent varier entre Adobe Advertising et [!DNL Marketing Channels]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Les utilisateurs qui découvrent l’intégration des jeux de données Adobe Advertising et [!DNL Marketing Channels] se posent souvent la question suivante : « Qu’est-ce qui cause la variance des données entre l’AMO ID et l’[!DNL Marketing Channels] ? » Ou, parfois, « Pourquoi les données sont-elles endommagées ? J’ai besoin que toutes les mesures correspondent dans les rapports. » Heureusement, les écarts n’indiquent pas que les données sont « rompues », et des écarts sont attendus et même souhaités. Voyons pourquoi l’intégration a été conçue de cette manière.

Les deux jeux de données ont des cas d’utilisation principaux différents :

* [!DNL Marketing Channels] : le principal cas d’utilisation d’[!DNL Marketing Channels] consiste à comparer des données sur plusieurs canaux avec un modèle d’attribution commun. Les analystes peuvent utiliser la dimension [!UICONTROL Marketing Channel] pour obtenir des informations supplémentaires sur la manière dont les canaux interagissent les uns avec les autres. Cette insight peut aider à alimenter les décisions au niveau macro sur la manière d’investir dans chaque canal et peut conduire à des informations sur la manière dont les visiteurs de chaque canal interagissent avec le site web.

  La dimension [!DNL Analytics] [!UICONTROL Marketing Channel] est donc configurée pour capturer et suivre tous les canaux. [!DNL Marketing Channels] peut également être configuré pour capturer les affichages publicitaires et les clics publicitaires Advertising DSP, et ce par rapport aux autres canaux marketing.

* ID AMO Adobe Advertising : le principal cas d’utilisation des données d’ID AMO Adobe Advertising consiste à alimenter les algorithmes d’offres avancés optimisés par [!DNL Adobe AI]. Les algorithmes prennent automatiquement des milliers de décisions d&#39;enchères au niveau micro prises quotidiennement afin de maximiser les dépenses publicitaires et d&#39;atteindre les objectifs de la campagne [!DNL DSP] ou du portefeuille [!DNL Search, Social, & Commerce]. Plus les algorithmes peuvent connecter les campagnes à des données de conversion, plus ils peuvent prendre ces décisions d’offres.

  Pour collecter ces données, l’intégration [!DNL Analytics for Advertising] transmet des AMO ID bruts qui peuvent être traduits en codes de suivi de clics publicitaires et de vues publicitaires dans la dimension AMO ID d’Adobe Analytics, stockée soit en tant que variable personnalisée (eVar), soit en tant que variable réservée (rVar). Les clics publicitaires pour d’autres canaux ne sont pas définis dans la dimension ID AMO. La dimension ID AMO ne peut donc pas suivre l’entrée à partir de ces autres canaux. Le résultat est que l’AMO ID persiste via les points d’entrée [!DNL Marketing Channels].

Pour plus d’informations sur les écarts de données possibles entre les données suivies par Adobe Advertising et les données suivies par [!DNL Analytics], voir « [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](../data-variances.md) ».

>[!MORELIKETHIS]
>
>* [Écarts de données attendus entre  [!DNL Analytics]  et Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Principes fondamentaux de  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilisation d’Adobe Advertising ID pour créer [!DNL Marketing Channels] traiter des règles](mc-ids.md)
>* [Utilisation  [!DNL Analytics Marketing Channels]  données Adobe Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation  [!DNL Marketing Channels]  rapports Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=fr)
