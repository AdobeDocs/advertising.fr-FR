---
title: Intégrations d’Adobe Advertising à Adobe Audience Manager
description: Découvrez les différentes manières dont Adobe Advertising peut échanger des données avec Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
TQID: https://experienceleague.adobe.com/4O4O-DmHhClvSiOSxM9blAEvVslzYzRobEyU6RGeMEQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# Intégrations d’Adobe Advertising à Adobe Audience Manager

Vous pouvez intégrer Adobe Advertising à Audience Manager comme suit.

## Synchroniser Audience Manager et d’autres segments [!DNL Adobe] pour le ciblage publicitaire

[!DNL Search, Social, & Commerce] et DSP peuvent extraire des métadonnées, des données hiérarchiques et des données d’audience uniques pour toutes les audiences Audience Manager d’un annonceur ou d’une agence et d’autres audiences [!DNL Adobe]. Cette connexion unique n’est disponible que pour les marketeurs qui utilisent Adobe Advertising. Voir « [Importation de segments Adobe Audience Manager pour le ciblage publicitaire](/help/integrations/audience-manager/import-audiences.md) ».

### Utiliser Audience Manager et d’autres segments [!DNL Adobe] pour créer des audiences [!DNL Google Ads] {#audience-manager-google-audiences}

*Publicitaires inscrits avec [!DNL Advertising Search, Social, & Commerce] uniquement*

Dans [!DNL Search, Social, & Commerce], vous pouvez créer [!DNL Google Ads] audiences de correspondance client à partir d’identifiants d’utilisateur à l’aide de vos segments Audience Manager existants qui ont [!UICONTROL Adobe Media Optimizer (HTTP)] et [!UICONTROL Adobe Media Optimizer Batch Destination] comme destinations. ([!DNL Media Optimizer] est un ancien nom pour [!DNL Search, Social, & Commerce].) Cela inclut les segments Adobe Analytics publiés sur Adobe Experience Cloud et les segments créés à l’aide de l’[!DNL Audience Library] Adobe Experience Cloud. Pour plus d’informations, voir « [Créer [!DNL Google Ads] des audiences de correspondance client à partir d’ [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) ».

[Les audiences de correspondance client à partir d’ID utilisateur](https://support.google.com/google-ads/answer/9199250) fonctionnent comme des audiences basées sur des balises de site web, mais un ID autre que des informations d’identification personnelle est affecté aux membres d’audience uniques pour des avantages distincts par rapport aux audiences de correspondance client standard et basées sur des balises de site web.

Pour créer les identifiants d’utilisateur nécessaires, vous devez utiliser une balise Adobe Advertising JavaScript <!-- with a user ID parameter -->sur vos sites web. Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

![processus de création de segment](/help/integrations/assets/ad_search_user_id_pic.png)

Une fois les audiences créées, vous pouvez les utiliser dans des campagnes [!DNL Google Ads] en tant que [&#x200B; cibles ou exclusions au niveau de la campagne ou du groupe publicitaire &#x200B;](#audience-manager-targets).

### Utiliser Audience Manager et d’autres segments de [!DNL Adobe] pour cibler ou exclure les publicités {#audience-manager-targets}

* (Publicitaires inscrits avec [!DNL Search, Social, & Commerce]) Vous pouvez utiliser toutes les audiences [!DNL Google Ads] qui ont été [créées à l’aide  [!DNL Adobe]  segments](#audience-manager-google-audiences) comme cibles ou exclusions au niveau de la campagne ou du groupe publicitaire dans vos campagnes [!DNL Google Ads].

* (Annonceurs avec DSP) Vous pouvez utiliser vos segments [!DNL Adobe] existants en tant que cibles pour vos emplacements publicitaires. Vous pouvez éventuellement inclure les segments dans des audiences réutilisables, que vous pouvez utiliser comme cibles ou exclusions pour plusieurs emplacements.

* (Annonceurs avec Advertising Creative) Vous pouvez utiliser vos segments [!DNL Adobe] existants comme cibles pour des contenus publicitaires spécifiques dans vos expériences publicitaires.

>[!NOTE]
>
>Pour plus d’informations sur la création d’audiences dans les interfaces de [!DNL Audience Library] d’Audience Manager et d’Experience Cloud, ainsi que pour des cas d’utilisation courants pour différents types d’audiences, voir « [Options de création d’audience](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html) ».

## Envoi de données d’exposition aux médias DSP vers Audience Manager

*Annonceurs avec DSP uniquement*

Les clients DSP avec Adobe Audience Manager peuvent capturer des données de campagnes publicitaires à l’aide d’appels de pixels vers Audience Manager. Vous pouvez ensuite utiliser les données de la campagne pour créer des caractéristiques basées sur des règles, que vous pouvez utiliser pour définir de nouveaux segments afin d’activer divers cas d’utilisation de DSP, tels qu’une segmentation plus avancée, la gestion des fréquences, les analyses marketing et les informations sur les rapports.

Pour plus d’informations, consultez « [Présentation de l’envoi de données d’exposition aux médias DSP vers Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md) ».

## Obtenez des informations plus riches sur l’activité du site avec Audience Analytics

Les clients Adobe Advertising disposant de [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) peuvent envoyer à la fois des données suivies par Adobe Advertising et des segments Audience Manager à [!DNL Analytics] pour obtenir des informations enrichies sur l’activité du site.

Pour plus d’informations, voir « [[!DNL Adobe Audience Analytics]  pour les clients Adobe Advertising &#x200B;](/help/integrations/audience-manager/audience-analytics.md). »
