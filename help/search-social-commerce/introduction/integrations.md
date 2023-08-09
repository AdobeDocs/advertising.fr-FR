---
title: Intégration aux solutions et services Adobe Experience Cloud
description: Découvrez les intégrations de Search, Social et Commerce avec les solutions et services Adobe Experience Cloud.
exl-id: e8b521f5-f426-4c50-9df4-361a047c9ff0
feature: Search Introduction
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Intégration aux solutions et services Adobe Experience Cloud

Advertising Search, Social et Commerce est intégré à ce qui suit : [!DNL Adobe] produits.

* [Balises à partir de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — Vous pouvez utiliser la variable [Extension Adobe Advertising Cloud](https://exchange.adobe.com/apps/ec/100155) pour Adobe Experience Platform afin de créer des balises de suivi de conversion d’Adobe Advertising, ainsi que des balises de suivi tierces, pour vos pages d’entrée de publicités. (Vous pouvez également [créer des balises de suivi de conversion directement dans Search, Social et Commerce ;](/help/search-social-commerce/tools/conversion-tag-generate.md).) Contactez votre équipe de compte d’Adobe ou votre équipe de mise en oeuvre pour obtenir des informations à inclure dans vos balises.

* Adobe Analytics — (fonctionnalité d’accord préalable) Adobe Advertising et [!DNL Analytics] sont intégrées de la manière suivante :

   * Adobe Advertising et [!DNL Analytics] partagez facilement des données. [!DNL Analytics] Vous pouvez envoyer quotidiennement des données d’engagement et de conversion du site à Search, Social et Commerce, où elles sont disponibles pour l’optimisation des publicités et la création de rapports. En outre, Adobe Advertising peut envoyer quotidiennement des données sur le trafic des publicités, notamment les impressions, les clics et les coûts, de vos réseaux publicitaires vers [!DNL Analytics], où les données sont disponibles dans tous les outils de reporting.

     Voir &quot;[Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md)&quot; pour plus d’informations sur [!DNL Analytics] prise en charge de chaque réseau publicitaire et type de publicité. Voir aussi &quot;[Présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot; pour plus d’informations sur l’échange de données.

     Pour échanger des données, Adobe Advertising et [!DNL Analytics] doit être configuré initialement. Contactez votre équipe de compte d’Adobe pour plus d’informations sur la configuration initiale.

     >[!NOTE]
     >
     >Par défaut, la variable [!DNL Analytics] Les mesures ne sont pas visibles dans les écrans de recherche, de Social et de Commerce. Vous devez explicitement [rendre les mesures disponibles dans les vues, les portefeuilles et les rapports de gestion de campagne](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) après la balise [!DNL Adobe] l’équipe de mise en oeuvre a configuré des événements standard ou personnalisés sélectionnés à transmettre à Adobe Advertising. Vous pouvez éventuellement modifier les noms des mesures affichées (sans les modifier dans [!DNL Analytics]). Vous pouvez rendre les mesures visibles dans l’interface utilisateur et les renommer à partir de [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Annonceurs avec [!DNL Analytics] mais l’Audience Manager ne peut pas [create [!DNL Google Ads] audiences de correspondance client](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) de [!DNL Analytics] segments partagés avec Adobe Experience Cloud. Pour être éligible, un annonceur doit mettre en oeuvre la variable [Service Adobe Experience Platform Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html) et déployer une balise sur ses sites web. Vous pouvez ensuite utiliser les audiences dans [!DNL Google Ads] campagnes au niveau de la campagne ou au niveau du groupe publicitaire [Cibles](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Segments Adobe Audience Manager — (fonctionnalité d’accord préalable) Vous pouvez [create [!DNL Google Ads] audiences de correspondance client](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) à partir des segments d’Audience Manager dont la destination est Search, Social et Commerce. Cela peut inclure : [!DNL Analytics] segments publiés sur Adobe Experience Cloud et segments créés à l’aide de la bibliothèque d’audiences Adobe Experience Cloud. Vous pouvez ensuite utiliser les audiences dans [!DNL Google Ads] campagnes au niveau de la campagne ou au niveau du groupe publicitaire [Cibles](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) ou [exclusions](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Voir &quot;[Adobe Advertising des intégrations avec Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot; pour plus d’informations.

* Adobe Target : vous pouvez implémenter le partage de signal de clic publicitaire entre Search, Social et Commerce et [!DNL Target], configurez une activité de test A/B dans [!DNL Target] pour vos publicités, puis utilisez [!DNL Analytics] Analysis Workspace pour afficher les données de test.

* Adobe Campaign — Vous pouvez [créer et mettre à jour une [!DNL Google Ads] audience de correspondance client à l’aide d’une liste de courriers électroniques dans [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Notifications Adobe Experience Cloud — (lorsque vous êtes connecté via Adobe Experience Cloud) À partir du lien de notifications ([Notifications d’alertes](/help/search-social-commerce/assets/notifications-panel.png "Notifications d’alertes")) en haut de chaque page, vous pouvez afficher toutes les mises à jour du système Adobe Experience Cloud, publications, mentions et ressources partagées. Contactez votre équipe de compte d’Adobe pour plus d’informations sur l’accès à Adobe Experience Cloud.
