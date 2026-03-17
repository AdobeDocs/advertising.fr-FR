---
title: Intégration aux solutions et services Adobe Experience Cloud
description: Découvrez les intégrations de Search, Social et Commerce aux solutions et services Adobe Experience Cloud.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Intégration aux solutions et services Adobe Experience Cloud

Advertising Search, Social et Commerce est intégré aux produits [!DNL Adobe] suivants.

* [Balises de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — Vous pouvez utiliser l’[extension Adobe Advertising Cloud](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) pour Adobe Experience Platform afin de [créer des balises de suivi de conversion Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md), ainsi que des balises de suivi tierces, pour vos pages de destination publicitaires. Si votre organisation ne dispose pas d’un compte Experience Platform, vous pouvez tout de même installer l’extension directement dans l’[interface utilisateur de la collecte de données Adobe Experience Platform](https://experience.adobe.com/#/data-collection/), disponible gratuitement pour les clients Adobe Experience Cloud.

  Pour installer l’extension requise, contactez l’administrateur de votre organisation pour accéder aux fonctionnalités de collecte de données dans l’interface utilisateur et demandez-lui de vous accorder l’autorisation `manage_properties`.

  **Remarque :** vous pouvez également [créer des balises de suivi des conversions directement dans Search, Social et Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics : (fonctionnalité d’accord préalable) Adobe Advertising et [!DNL Analytics] sont intégrés des manières suivantes :

   * Adobe Advertising et [!DNL Analytics] partagent les données de manière transparente. [!DNL Analytics] pouvez envoyer quotidiennement des données d’engagement et de conversion du site à Search, Social et Commerce, où elles servent à l’optimisation des publicités et à la création de rapports. En outre, Adobe Advertising peut envoyer quotidiennement à [!DNL Analytics] des données sur le trafic publicitaire (notamment les impressions, les clics et les coûts) provenant de vos réseaux publicitaires, où elles sont disponibles dans tous les outils de création de rapports.

     Consultez « [Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md) » pour plus d’informations sur la prise en charge des [!DNL Analytics] pour chaque réseau et type d’annonce publicitaire. Consultez également la section « [Présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"} » pour plus d’informations sur l’échange de données.

     Pour échanger des données, Adobe Advertising et [!DNL Analytics] doivent être initialement configurés. Pour plus d’informations sur la configuration initiale, contactez l’équipe chargée de votre compte Adobe.

     >[!NOTE]
     >
     >Par défaut, les mesures [!DNL Analytics] ne sont pas visibles dans les écrans Search, Social et Commerce. Vous devez explicitement [rendre les mesures disponibles dans les vues de gestion de campagnes, les portfolios et les rapports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) une fois que l’équipe d’implémentation de [!DNL Adobe] a configuré les événements standards ou personnalisés sélectionnés pour les transmettre à Adobe Advertising. Vous pouvez éventuellement modifier les noms des mesures affichés (sans les modifier dans [!DNL Analytics]). Vous pouvez rendre les mesures visibles dans l’interface utilisateur et renommer les mesures à partir de [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Les annonceurs avec [!DNL Analytics] mais pas Audience Manager peuvent [créer [!DNL Google Ads] audiences de correspondance client](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) à partir de segments [!DNL Analytics] partagés avec Adobe Experience Cloud. Pour être éligible, un annonceur doit mettre en œuvre le service d’identités Adobe Experience Platform [&#128279;](https://experienceleague.adobe.com/docs/id-service/using/home.html) et déployer une balise sur ses sites web. Vous pouvez ensuite utiliser les audiences dans [!DNL Google Ads] campagnes comme cibles [cibles](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) au niveau de la campagne ou du groupe publicitaire.

* Segments Adobe Audience Manager — (Fonctionnalité d’opt-in) Vous pouvez [créer [!DNL Google Ads] audiences de correspondance client](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) à partir de segments Audience Manager qui ont comme destination Search, Social et Commerce. Il peut s’agir de segments [!DNL Analytics] publiés sur Adobe Experience Cloud et de segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud. Vous pouvez ensuite utiliser les audiences dans [!DNL Google Ads] campagnes comme cibles [cibles](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) au niveau de la campagne ou du groupe publicitaire.

  Voir « [Intégrations Adobe Advertising avec Adobe Audience Manager »](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html) pour plus d’informations.

* Adobe Target : vous pouvez implémenter le partage de signaux de clics publicitaires entre Search, Social et Commerce et [!DNL Target], configurer une activité de test A/B dans [!DNL Target] pour vos publicités, puis utiliser [!DNL Analytics]’Analysis Workspace pour afficher les données de test.

* Adobe Campaign — Vous pouvez [créer et mettre à jour une audience de correspondance client [!DNL Google Ads] e-mail dans [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notifications Adobe Experience Cloud : (lorsque vous êtes connecté via Adobe Experience Cloud) depuis le lien de notifications ([Notifications d’alerte](/help/search-social-commerce/assets/notifications-panel.png "Notifications d’alerte")) situé en haut de chaque page, vous pouvez afficher toutes les mises à jour du système Adobe Experience Cloud, les publications, les mentions et les ressources partagées. Pour plus d’informations sur l’accès à Adobe Experience Cloud, contactez l’équipe chargée de votre compte Adobe.
