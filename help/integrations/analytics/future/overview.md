---
title: Adobe Advertising des intégrations avec Adobe Analytics
description: Découvrez comment Adobe Advertising peut échanger des données avec Adobe Analytics et comment utiliser les données dans Search, Social et Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Adobe Advertising des intégrations avec Adobe Analytics

Vous pouvez intégrer Adobe Advertising à Analytics de différentes manières.

## Échanger des données entre [!DNL Analytics] et Adobe Advertising

### Extraire [!DNL Analytics] Données dans Adobe Advertising

Avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] et DSP d’y entrer :

* **[!DNL Analytics]segments :**  Métadonnées, données de hiérarchie et données d’audience uniques pour tous les segments d’un annonceur ou d’une agence créés dans [!DNL Analytics] et publié sur Experience Cloud.

* **[!DNL Analytics]mesures d’engagement du site**

* **[!DNL Analytics]mesures standard, personnalisées et réservées**

### Envoi de données d’Adobe Advertising à [!DNL Analytics]

* **Mesures de trafic depuis l’Adobe Advertising**

* **Dimensions d’Adobe Advertising**

>[!NOTE]
>
>Pour [!DNL Search, Social, & Commerce], cette fonctionnalité est prise en charge pour la plupart des réseaux publicitaires et des types de campagne. Voir &quot;Inventaire pris en charge&quot; dans la [!DNL Search, Social, & Commerce] Guide pour plus d’informations.<!-- add link when that's published in ExL -->

### Utilisation [!DNL Analytics] Segments à créer [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Publicitaires inscrits avec [!DNL Advertising Search, Social, & Commerce] only*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], vous pouvez créer des [!DNL Google Ads] Les clients Google correspondent aux audiences provenant d’identifiants d’utilisateur utilisant votre [!DNL Analytics] segments. Cela inclut les segments Adobe Analytics publiés sur Adobe Experience Cloud et les segments créés à l’aide de Adobe Experience Cloud. [!DNL Audience Library]. Pour plus d’informations, voir &quot;[Créer [!DNL Google Ads] audiences de correspondance client provenant de [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Audiences de ciblage des clients provenant d’ID d’utilisateur](https://support.google.com/google-ads/answer/9199250) fonctionne comme les audiences basées sur des balises de site web, mais un ID non lié aux PII est attribué aux membres d’audience uniques pour des avantages distincts par rapport aux audiences standard basées sur les balises de client et de site web.

Pour créer les ID utilisateur nécessaires, vous devez utiliser une balise JavaScript Adobe Advertising. <!-- with a user ID parameter -->sur vos sites web. Pour plus d’informations, contactez votre équipe de compte d’Adobe.

![processus de création de segments](/help/integrations/assets/ad_search_user_id_pic.png)

Une fois les audiences créées, vous pouvez les utiliser dans [!DNL Google Ads] campagnes comme [cibles ou exclusions au niveau de la campagne ou du groupe publicitaire](#audience-manager-targets).

### Utilisation [!DNL Analytics] Segments pour cibler ou exclure des publicités {#analytics-targets}

* (Publicitaires inscrits avec [!DNL Search, Social, & Commerce]) Vous pouvez utiliser les [!DNL Google Ads] audiences qui étaient [créé à l’aide de [!DNL Analytics] segments](#audience-manager-google-audiences) comme cibles ou exclusions au niveau de la campagne ou du groupe publicitaire dans votre [!DNL Google Ads] campagnes.

* (Publicitaires avec DSP) Vous pouvez utiliser votre [!DNL Analytics] segments comme cibles pour vos emplacements publicitaires. Vous pouvez éventuellement inclure les segments dans les audiences réutilisables, que vous pouvez utiliser comme cibles ou exclusions pour plusieurs emplacements.

* (Publicitaires avec Advertising Creative) Vous pouvez utiliser votre [!DNL Analytics] segments comme cibles pour des créatifs spécifiques dans vos expériences publicitaires.
