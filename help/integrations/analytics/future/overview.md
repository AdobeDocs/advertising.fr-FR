---
title: Adobe Advertising des intégrations avec Adobe Analytics
description: Découvrez comment Adobe Advertising peut exchange des données avec Adobe Analytics et comment utiliser les données dans Search, Social et Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Adobe Advertising des intégrations avec Adobe Analytics

Vous pouvez intégrer Adobe Advertising à Analytics de différentes manières.

## Exchange de données entre [!DNL Analytics] et Adobe Advertising

### Extraire les données [!DNL Analytics] dans Adobe Advertising

Avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), [!DNL Search, Social, & Commerce] et DSP pull-in :

* **[!DNL Analytics]segments :** métadonnées, données de hiérarchie et données d’audience uniques pour tous les segments d’annonceurs ou d’agences créés dans [!DNL Analytics] et publiés dans Experience Cloud.

* **[!DNL Analytics]mesures d’engagement du site**

* **[!DNL Analytics]mesures standard, personnalisées et réservées**

### Envoyer des données d&#39;Adobe Advertising à [!DNL Analytics]

* **Mesures de trafic de l’Adobe Advertising**

* **Dimensions de l’Adobe Advertising**

>[!NOTE]
>
>Pour [!DNL Search, Social, & Commerce], cette fonctionnalité est prise en charge pour la plupart des réseaux publicitaires et des types de campagne. Voir &quot;Inventaire pris en charge&quot; dans le guide [!DNL Search, Social, & Commerce] pour plus d’informations.<!-- add link when that's published in ExL -->

### Utilisation de [!DNL Analytics] segments pour créer [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Annonceurs avec abonnement [!DNL Advertising Search, Social, & Commerce] uniquement*

<!-- Verify all -->

Dans [!DNL Search, Social, & Commerce], vous pouvez créer des audiences de correspondance de clients [!DNL Google Ads] Google à partir d’identifiants d’utilisateur à l’aide de vos segments [!DNL Analytics] existants. Cela inclut les segments Adobe Analytics publiés sur Adobe Experience Cloud et les segments créés à l’aide de Adobe Experience Cloud [!DNL Audience Library]. Pour plus d’informations, voir &quot;[Créer [!DNL Google Ads] une audience de correspondance client à partir de [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)&quot;.

[Les audiences de correspondance de client provenant des ID d’utilisateur](https://support.google.com/google-ads/answer/9199250) fonctionnent comme des audiences basées sur des balises de site web, mais un ID non lié aux PII est attribué aux membres d’audience unique pour des avantages distincts par rapport aux audiences basées sur les balises de client standard et de site web.

Pour créer les identifiants utilisateur nécessaires, vous devez utiliser une balise JavaScript Adobe Advertising <!-- with a user ID parameter --> sur vos sites web. Pour plus d’informations, contactez votre équipe de compte d’Adobe.

![processus de création de segment](/help/integrations/assets/ad_search_user_id_pic.png)

Une fois que vous avez créé les audiences, vous pouvez les utiliser dans les campagnes [!DNL Google Ads] en tant que [cibles ou exclusions au niveau de la campagne ou du groupe publicitaire](#audience-manager-targets).

### Utilisation de [!DNL Analytics] segments pour cibler ou exclure des publicités {#analytics-targets}

* (Publicitaires avec abonnement [!DNL Search, Social, & Commerce]) Vous pouvez utiliser toutes les audiences [!DNL Google Ads] [&#x200B; créées à l’aide de  [!DNL Analytics] segments](#audience-manager-google-audiences) comme cibles ou exclusions au niveau de la campagne ou du groupe publicitaire dans vos campagnes [!DNL Google Ads].

* (Publicitaires avec DSP) Vous pouvez utiliser vos segments [!DNL Analytics] existants comme cibles pour vos emplacements publicitaires. Vous pouvez éventuellement inclure les segments dans les audiences réutilisables, que vous pouvez utiliser comme cibles ou exclusions pour plusieurs emplacements.

* (Publicitaires avec Advertising Creative) Vous pouvez utiliser vos segments [!DNL Analytics] existants comme cibles pour des créatifs spécifiques dans vos expériences publicitaires.
