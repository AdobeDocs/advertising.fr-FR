---
title: Pourquoi les données de canal peuvent varier entre l’Adobe Advertising et  [!DNL Marketing Channels]
description: Découvrez pourquoi les données de canal suivies par l’AMO ID peuvent différer des données de canal suivies par [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Pourquoi les données du canal peuvent varier entre l’Adobe Advertising et [!DNL Marketing Channels]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Une question courante des utilisateurs qui apprennent l’intégration des jeux de données d’Adobe Advertising et [!DNL Marketing Channels] est : &quot;Quelle est la cause de la variance des données entre l’AMO ID et [!DNL Marketing Channels] ?&quot; Ou, parfois, &quot;Pourquoi les données sont-elles rompues ? J’ai besoin que toutes les mesures correspondent dans les rapports.&quot; Heureusement, les incohérences n’indiquent pas que les données sont &quot;cassées&quot; et les incohérences sont attendues et même souhaitées. Examinons pourquoi l’intégration a été conçue de cette manière.

Les deux jeux de données présentent différents cas d’utilisation principaux :

* [!DNL Marketing Channels] : le principal cas d’utilisation de [!DNL Marketing Channels] consiste à comparer les données sur plusieurs canaux avec un modèle d’attribution commun. Les analystes peuvent utiliser la dimension [!UICONTROL Marketing Channel] pour obtenir des informations supplémentaires sur la manière dont les canaux interagissent les uns avec les autres. Ces informations peuvent vous aider à prendre des décisions de macroniveau sur la manière d’investir dans chaque canal et à obtenir des informations sur la manière dont les visiteurs de chaque canal interagissent avec le site web.

  La dimension [!DNL Analytics] [!UICONTROL Marketing Channel] est donc configurée pour capturer et suivre tous les canaux. [!DNL Marketing Channels] peut également être configuré pour capturer les affichages publicitaires et les clics publicitaires Advertising DSP, par rapport aux autres canaux marketing.

* Adobe Advertising AMO ID : le principal cas d’utilisation des données AMO ID de l’Adobe Advertising consiste à alimenter les algorithmes avancés d’enchères optimisés par [!DNL Adobe Sensei]. Les algorithmes prennent automatiquement des milliers de décisions d’offre de microniveau prises quotidiennement afin d’optimiser les dépenses publicitaires et d’atteindre les objectifs de la campagne [!DNL DSP] ou du portefeuille [!DNL Search, Social, & Commerce]. Plus les algorithmes peuvent connecter les campagnes à des données de conversion, mieux ils peuvent prendre ces décisions d’offre.

  Pour collecter ces données, l’intégration [!DNL Analytics for Advertising] transmet des AMO ID bruts qui peuvent être traduits en codes de suivi des clics publicitaires et des affichages publicitaires dans la dimension AMO ID d’Adobe Analytics — qui est stockée sous la forme d’une variable personnalisée (eVar) ou d’une variable réservée (rVar). Les clics publicitaires pour d’autres canaux ne sont pas définis dans la dimension AMO ID. La dimension AMO ID ne peut donc pas effectuer le suivi des entrées à partir de ces autres canaux. Par conséquent, l’AMO ID persiste à travers les points d’entrée [!DNL Marketing Channels].

Pour plus d’informations sur les écarts de données possibles entre les données suivies par l’Adobe Advertising et les données suivies de [!DNL Analytics], voir &quot;[Écarts de données attendus entre [!DNL Analytics] et l’Adobe Advertising](../data-variances.md)&quot;.

>[!MORELIKETHIS]
>
>* [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Principes fondamentaux de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilisation d’identifiants d’Adobe Advertising pour créer [!DNL Marketing Channels] des règles de traitement](mc-ids.md)
>* [Utilisation de  [!DNL Analytics Marketing Channels]  avec des données d’Adobe Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation de [!DNL Marketing Channels] pour la création de rapports d’Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
