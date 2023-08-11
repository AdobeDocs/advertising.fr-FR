---
title: Mise en oeuvre [!DNL Google Ads] campagnes de performances max
description: En savoir plus sur le workflow de configuration [!DNL Google Ads] campagnes de performances max.
exl-id: afad96b2-d4a6-41ee-ad84-38aa1306d73e
feature: Search Campaign Management
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Mise en oeuvre [!DNL Google Ads] campagnes de performances max

Dans [!DNL Google Ads] performances max des campagnes, vous ne configurez pas de groupes publicitaires, de publicités ou de mots-clés. Au lieu de cela, dans les paramètres de l’opération, vous définissez un ou plusieurs groupes de ressources, qui comprennent des titres, des descriptions et des images, logos et [!DNL YouTube videos]. [!DNL Google Ads] combine automatiquement les ressources pour diffuser des publicités en fonction du canal (comme [!DNL YouTube], [!DNL Gmail], ou [!DNL Search]).

Vous pouvez afficher vos campagnes de performances max existantes, avec les données de performances au format tableau et graphique de tendances, au format [!DNL Campaigns] vue ; les données ne sont pas disponibles à des niveaux inférieurs. Les données de performances au niveau de la campagne sont également disponibles dans les rapports et dans Adobe Analytics (pour les annonceurs qui disposent d’un [Intégration d’Analytics](/help/integrations/analytics/overview.md). Pour afficher les données de performances pour les campagnes de performances max dans [!DNL Analytics], la campagne doit utiliser la variable [code de suivi AMO ID mis à niveau](/help/integrations/analytics/ids.md#amo-id-formats) (qui effectue le suivi de l’identifiant de campagne et de l’identifiant du groupe publicitaire).

>[!NOTE]
>
>* Vous devez charger manuellement tous les fichiers image. Liens vers [!DNL Google Merchant Center] les flux de produit ne sont pas pris en charge.
>* Seuls les paramètres requis sont disponibles. Pour les paramètres facultatifs, connectez-vous au [!DNL Google Ads] éditeur.
>* La prise en charge des groupes de listes n’est pas disponible. Pour gérer et afficher les données des groupes répertoriés, connectez-vous au [!DNL Google Ads] éditeur.

## Étapes de configuration [!DNL Google Ads] campagnes de performances max

Vous pouvez configurer individuellement le nombre maximal de campagnes de performances à partir du [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vue.

1. [Créer une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) avec type de campagne **[!UICONTROL Performance Max]**.

   Spécifiez la variable [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting], et [!UICONTROL URL Options]. (Facultatif) [!UICONTROL Negative Keywords], saisissez [!UICONTROL Negative Websites], et/ou remplacez la variable [!UICONTROL Campaign Tracking] options.

1. Créez des groupes de ressources et chargez des ressources pour la campagne :

   1. Au bas des paramètres de l’opération, cliquez sur **[!UICONTROL Manage Asset Groups]**.

   1. Spécifiez les paramètres du premier groupe de ressources, puis chargez les images, les logos et les vidéos facultatives du groupe de ressources.

      Voir [description des paramètres du groupe de ressources](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) pour comprendre les exigences et les spécifications.

   1. Ajoutez d’autres groupes de ressources si nécessaire.

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Ajoutez la campagne à un portfolio hybride pour l’optimisation.
