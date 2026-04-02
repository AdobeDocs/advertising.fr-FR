---
title: Pourquoi les données de canal peuvent-elles varier entre Adobe Advertising et  [!DNL Marketing Channels]
description: Découvrez pourquoi les données de canal suivies par l’ID AMO peuvent différer des données de canal suivies par  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
TQID: https://experienceleague.adobe.com/zzYKrbiwvW9Ysf7baDfKGsETmSvYbXDY7-lIygorXH8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 0%

---

# Pourquoi les données de canal peuvent-elles varier entre Adobe Advertising et [!DNL Marketing Channels] ?

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
>* [Utilisation des Adobe Advertising ID pour la création [!DNL Marketing Channels] le traitement des règles](mc-ids.md)
>* [Utilisation [!DNL Analytics Marketing Channels] avec des données Adobe Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation  [!DNL Marketing Channels]  rapports pour Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
