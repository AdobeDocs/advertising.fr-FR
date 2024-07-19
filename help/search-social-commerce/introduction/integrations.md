---
title: Intégration aux solutions et services Adobe Experience Cloud
description: Découvrez les intégrations de Search, Social et Commerce aux solutions et services Adobe Experience Cloud.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Intégration aux solutions et services Adobe Experience Cloud

Advertising Search, Social et Commerce est intégré aux produits [!DNL Adobe] suivants.

* [Balises de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — Vous pouvez utiliser l’ [extension Adobe Advertising Cloud](https://exchange.adobe.com/apps/ec/100155) pour Adobe Experience Platform pour créer des balises de suivi de conversion d’Adobe Advertising, ainsi que des balises de suivi tierces, pour vos pages d’entrée de publicités. (Vous pouvez également [créer des balises de suivi de conversion directement dans Search, Social et Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md).) Contactez votre équipe de compte d’Adobe ou votre équipe de mise en oeuvre pour obtenir des informations à inclure dans vos balises.

* Adobe Analytics — (fonctionnalité d’opt-in) Adobe Advertising et [!DNL Analytics] sont intégrés de différentes manières :

   * Adobe Advertising et [!DNL Analytics] partagent facilement des données. [!DNL Analytics] peut envoyer quotidiennement des données d’engagement et de conversion du site à Search, Social et Commerce, où elles sont disponibles pour l’optimisation des publicités et pour la création de rapports. En outre, Adobe Advertising peut envoyer des données de trafic de publicités — y compris les impressions, les clics et les coûts — de vos réseaux publicitaires tous les jours à [!DNL Analytics], où les données sont disponibles dans tous les outils de création de rapports.

     Voir &quot;[Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md)&quot; pour plus d’informations sur la prise en charge de [!DNL Analytics] pour chaque réseau publicitaire et type de publicité. Voir aussi &quot;[Présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; pour plus d’informations sur l’exchange de données.

     Pour exchange des données, Adobe Advertising et [!DNL Analytics] doivent être configurés initialement. Contactez votre équipe de compte d’Adobe pour plus d’informations sur la configuration initiale.

     >[!NOTE]
     >
     >Par défaut, les mesures [!DNL Analytics] ne sont pas visibles dans les écrans Rechercher, Social et Commerce. Vous devez [ rendre explicitement disponibles les mesures dans les vues de gestion de campagne, les portefeuilles et les rapports ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) une fois que l’équipe de mise en oeuvre de [!DNL Adobe] a configuré les événements standard ou personnalisés à transmettre à Adobe Advertising. Vous pouvez éventuellement modifier les noms des mesures affichées (sans les modifier dans [!DNL Analytics]). Vous pouvez rendre les mesures visibles dans l’interface utilisateur et renommer les mesures de [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Les annonceurs disposant de [!DNL Analytics] mais pas d’Audience Manager peuvent [créer [!DNL Google Ads] une correspondance client avec des audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) à partir de [!DNL Analytics] segments partagés avec Adobe Experience Cloud. Pour être éligible, un annonceur doit mettre en oeuvre le [service Adobe Experience Platform Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html) et déployer une balise sur ses sites web. Vous pouvez ensuite utiliser les audiences dans les campagnes [!DNL Google Ads] comme des [cibles](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) au niveau de la campagne ou du groupe publicitaire.

* Segments Adobe Audience Manager — (fonctionnalité d’opt-in) Vous pouvez [créer [!DNL Google Ads] des audiences de correspondance client](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) à partir des segments d’Audience Manager qui ont pour destination Search, Social et Commerce. Il peut s’agir de [!DNL Analytics] segments publiés sur Adobe Experience Cloud et de segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud. Vous pouvez ensuite utiliser les audiences dans les campagnes [!DNL Google Ads] comme des [cibles](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) au niveau de la campagne ou du groupe publicitaire.

  Pour plus d’informations, voir &quot;[Adobe Advertising des intégrations avec Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot;.

* Adobe Target : vous pouvez mettre en oeuvre le partage de signal de clic publicitaire entre Search, Social et Commerce et [!DNL Target], configurer une activité de test A/B dans [!DNL Target] pour vos publicités, puis utiliser [!DNL Analytics] Analysis Workspace pour afficher les données de test.

* Adobe Campaign : vous pouvez [ créer et mettre à jour une audience de  [!DNL Google Ads] correspondance de client à l’aide d’une liste d’emails dans  [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notifications Adobe Experience Cloud : (lorsque vous êtes connecté via Adobe Experience Cloud) à partir du lien de notifications ([Notifications d’alerte](/help/search-social-commerce/assets/notifications-panel.png "Notifications d’alertes")) situé en haut de chaque page, vous pouvez afficher toutes les mises à jour du système Adobe Experience Cloud, publications, mentions et ressources partagées. Contactez votre équipe de compte d’Adobe pour plus d’informations sur l’accès à Adobe Experience Cloud.
