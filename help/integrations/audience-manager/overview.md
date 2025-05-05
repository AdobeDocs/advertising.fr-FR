---
title: Adobe Advertising des intégrations avec Adobe Audience Manager
description: Découvrez les différentes manières dont Adobe Advertising peut exchange des données avec Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Adobe Advertising des intégrations avec Adobe Audience Manager

Vous pouvez intégrer l’Adobe Advertising à l’Audience Manager de la manière suivante.

## Synchroniser l’Audience Manager et d’autres segments [!DNL Adobe] pour le ciblage des publicités

[!DNL Search, Social, & Commerce] et DSP peuvent extraire des métadonnées, des données de hiérarchie et des données d’audience uniques pour l’ensemble de l’Audience Manager d’un annonceur ou d’une agence et d’autres audiences [!DNL Adobe]. Cette connexion unique est disponible uniquement pour les marketeurs utilisant Adobe Advertising. Voir &quot;[Importation de segments Adobe Audience Manager pour le ciblage des publicités](/help/integrations/audience-manager/import-audiences.md)&quot;.

### Utilisation de l’Audience Manager et d’autres segments [!DNL Adobe] pour créer [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Annonceurs avec abonnement [!DNL Advertising Search, Social, & Commerce] uniquement*

Dans [!DNL Search, Social, & Commerce], vous pouvez créer des audiences [!DNL Google Ads] de correspondance client à partir des identifiants d’utilisateur en utilisant vos segments d’Audience Manager existants qui ont [!UICONTROL Adobe Media Optimizer (HTTP)] et [!UICONTROL Adobe Media Optimizer Batch Destination] comme destinations. ([!DNL Media Optimizer] est un ancien nom de [!DNL Search, Social, & Commerce].) Cela inclut les segments Adobe Analytics publiés sur Adobe Experience Cloud et les segments créés à l’aide de Adobe Experience Cloud [!DNL Audience Library]. Pour plus d’informations, voir &quot;[Créer [!DNL Google Ads] une audience de correspondance client à partir de [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

[Les audiences de correspondance de client provenant des ID d’utilisateur](https://support.google.com/google-ads/answer/9199250) fonctionnent comme des audiences basées sur des balises de site web, mais un ID non lié aux PII est attribué aux membres d’audience unique pour des avantages distincts par rapport aux audiences basées sur les balises de client standard et de site web.

Pour créer les identifiants utilisateur nécessaires, vous devez utiliser une balise JavaScript Adobe Advertising <!-- with a user ID parameter --> sur vos sites web. Pour plus d’informations, contactez votre équipe de compte d’Adobe.

![processus de création de segment](/help/integrations/assets/ad_search_user_id_pic.png)

Une fois que vous avez créé les audiences, vous pouvez les utiliser dans les campagnes [!DNL Google Ads] en tant que [cibles ou exclusions au niveau de la campagne ou du groupe publicitaire](#audience-manager-targets).

### Utilisation de l’Audience Manager et d’autres segments [!DNL Adobe] pour cibler ou exclure des publicités {#audience-manager-targets}

* (Publicitaires avec abonnement [!DNL Search, Social, & Commerce]) Vous pouvez utiliser toutes les audiences [!DNL Google Ads] [ créées à l’aide de  [!DNL Adobe] segments](#audience-manager-google-audiences) comme cibles ou exclusions au niveau de la campagne ou du groupe publicitaire dans vos campagnes [!DNL Google Ads].

* (Publicitaires avec DSP) Vous pouvez utiliser vos segments [!DNL Adobe] existants comme cibles pour vos emplacements publicitaires. Vous pouvez éventuellement inclure les segments dans les audiences réutilisables, que vous pouvez utiliser comme cibles ou exclusions pour plusieurs emplacements.

* (Publicitaires avec Advertising Creative) Vous pouvez utiliser vos segments [!DNL Adobe] existants comme cibles pour des créatifs spécifiques dans vos expériences publicitaires.

>[!NOTE]
>
>Pour plus d’informations sur la création d’audiences dans les interfaces d’Audience Manager et d’Experience Cloud [!DNL Audience Library] et les cas d’utilisation courants pour différents types d’audiences, voir &quot;[Options de création d’audience](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=fr)&quot;.

## Envoi DSP données d’exposition multimédia à l’Audience Manager

*Annonceurs avec DSP uniquement*

DSP clients Adobe Audience Manager peuvent capturer des données provenant de campagnes publicitaires à l’aide d’appels de pixel vers Audience Manager. Vous pouvez ensuite utiliser les données de campagne pour créer des caractéristiques basées sur des règles, que vous pouvez utiliser pour définir de nouveaux segments afin d’activer divers cas d’utilisation DSP, tels qu’une segmentation plus avancée, la gestion des fréquences, les analyses marketing et les informations sur les rapports.

Pour plus d’informations, voir &quot;[Présentation de l’envoi DSP données d’exposition aux médias à Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

## Obtenir des informations plus riches sur l’activité du site avec Audience Analytics

Les clients Adobe Advertising disposant de [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=fr) peuvent envoyer à la fois des données suivies par l’Adobe Advertising et des segments d’Audience Manager à [!DNL Analytics] pour obtenir des informations enrichies sur l’activité du site.

Pour plus d’informations, voir &quot;[[!DNL Adobe Audience Analytics] pour les clients Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md)&quot;.
