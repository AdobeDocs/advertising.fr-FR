---
title: Implémenter  [!DNL Google Ads]  campagnes de performances maximales
description: Découvrez le workflow de configuration  [!DNL Google Ads]  campagnes de performances maximales .
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Implémenter des campagnes de performances maximales [!DNL Google Ads]

Dans les campagnes [!DNL Google Ads] Performance Max, vous ne configurez pas de groupes publicitaires, de publicités ou de mots-clés. Dans les paramètres de la campagne, vous spécifiez plutôt un ou plusieurs groupes de ressources, qui incluent des titres, des descriptions, des images, des logos et des [!DNL YouTube videos] chargés. [!DNL Google Ads] combine automatiquement les ressources pour diffuser des annonces en fonction du canal (par exemple [!DNL YouTube], [!DNL Gmail] ou [!DNL Search]).

Vous pouvez afficher vos campagnes « Performances max » existantes, avec des données de performances au format tableau et graphique de tendances, dans la vue [!DNL Campaigns] ; les données ne sont pas disponibles aux niveaux inférieurs. Les données de performances au niveau des campagnes sont également disponibles dans les rapports ainsi que dans Adobe Analytics (pour les annonceurs qui disposent d’une intégration [&#x200B; Analytics](/help/integrations/analytics/overview.md). Pour afficher les données de performances des campagnes Performance Max dans [!DNL Analytics], la campagne doit utiliser le [code de suivi AMO ID mis à niveau](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items) (qui effectue le suivi de l’identifiant de campagne et de l’identifiant du groupe publicitaire).

>[!NOTE]
>
>* Vous devez charger manuellement tous les fichiers image. Les liens vers les flux de produits [!DNL Google Merchant Center] ne sont pas pris en charge.
>* Seuls les paramètres requis sont disponibles. Pour obtenir des paramètres facultatifs, connectez-vous à l’éditeur de [!DNL Google Ads].
>* La prise en charge des groupes de listes n’est pas disponible. Pour gérer et afficher les données des groupes de listes, connectez-vous à l’éditeur de [!DNL Google Ads].

## Étapes de configuration des campagnes [!DNL Google Ads] Performance Max

Vous pouvez configurer les campagnes de performances maximales individuellement à partir de la vue [!UICONTROL Campaigns] > [!UICONTROL Campaigns] .

1. [Créez une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) avec le type de campagne **[!UICONTROL Performance Max]**.

   Spécifiez les [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting] et [!UICONTROL URL Options]. Le cas échéant, saisissez [!UICONTROL Negative Keywords], saisissez [!UICONTROL Negative Websites] et/ou remplacez les options [!UICONTROL Campaign Tracking].

1. Créez des groupes de ressources et chargez des ressources pour la campagne :

   1. Au bas des paramètres de la campagne, cliquez sur **[!UICONTROL Manage Asset Groups]**.

   1. Spécifiez les paramètres du premier groupe de ressources et chargez les images, les logos et les vidéos facultatives pour le groupe de ressources.

      Consultez [descriptions des paramètres de groupe de ressources](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) pour comprendre les exigences et les spécifications.

   1. Ajoutez d’autres groupes de ressources, le cas échéant.

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Ajoutez la campagne à un portfolio hybride à des fins d’optimisation.
