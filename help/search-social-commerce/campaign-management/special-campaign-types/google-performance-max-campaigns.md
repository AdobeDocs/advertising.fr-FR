---
title: Implémenter [!DNL Google Ads] des campagnes de performances max
description: Découvrez le workflow de configuration des campagnes  [!DNL Google Ads] performances max.
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implémentation de campagnes [!DNL Google Ads] de performances max

Dans les campagnes [!DNL Google Ads] de performances max., vous ne configurez pas de groupes publicitaires, de publicités ni de mots-clés. Au lieu de cela, dans les paramètres de campagne, vous spécifiez un ou plusieurs groupes de ressources, qui incluent des titres, des descriptions et des images, logos et [!DNL YouTube videos] téléchargés. [!DNL Google Ads] combine automatiquement les ressources pour diffuser des publicités en fonction du canal (par exemple [!DNL YouTube], [!DNL Gmail] ou [!DNL Search]).

Vous pouvez afficher vos campagnes de performances max existantes, avec des données de performances au format tableau et diagramme de tendance, dans la vue [!DNL Campaigns] ; les données ne sont pas disponibles à des niveaux inférieurs. Les données de performances au niveau de la campagne sont également disponibles dans les rapports et dans Adobe Analytics (pour les annonceurs avec une [intégration Analytics](/help/integrations/analytics/overview.md). Pour afficher les données de performances pour les campagnes de performances maximales dans [!DNL Analytics], la campagne doit utiliser le [code de suivi AMO ID mis à niveau](/help/integrations/analytics/ids.md#amo-id-formats) (qui suit l’identifiant de campagne et l’identifiant de groupe publicitaire).

>[!NOTE]
>
>* Vous devez charger manuellement tous les fichiers image. Les liens vers les flux de produits [!DNL Google Merchant Center] ne sont pas pris en charge.
>* Seuls les paramètres requis sont disponibles. Pour les paramètres facultatifs, connectez-vous à l’éditeur [!DNL Google Ads].
>* La prise en charge des groupes de listes n’est pas disponible. Pour gérer et afficher les données des groupes de liste, connectez-vous à l’éditeur [!DNL Google Ads].

## Étapes de configuration des campagnes [!DNL Google Ads] de performances max

Vous pouvez configurer individuellement le nombre maximal de campagnes de performances à partir de la vue [!UICONTROL Campaigns] > [!UICONTROL Campaigns].

1. [Créez une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) avec le type de campagne **[!UICONTROL Performance Max]**.

   Spécifiez les [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting] et [!UICONTROL URL Options]. Vous pouvez éventuellement saisir [!UICONTROL Negative Keywords], saisir [!UICONTROL Negative Websites] et/ou remplacer les options [!UICONTROL Campaign Tracking].

1. Créez des groupes de ressources et chargez des ressources pour la campagne :

   1. Au bas des paramètres de la campagne, cliquez sur **[!UICONTROL Manage Asset Groups]**.

   1. Spécifiez les paramètres du premier groupe de ressources, puis chargez les images, les logos et les vidéos facultatives du groupe de ressources.

      Pour connaître les exigences et les spécifications, voir [descriptions des paramètres du groupe de ressources](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) .

   1. Ajoutez d’autres groupes de ressources si nécessaire.

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Ajoutez la campagne à un portfolio hybride pour l’optimisation.
