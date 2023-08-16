---
title: Paramètre de suivi AMO ID (s_kwcid)
description: Découvrez le paramètre de suivi utilisé pour partager des données d’Adobe Advertising avec Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Paramètre de suivi AMO ID (s_kwcid)

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe Advertising partage des données sur vos campagnes avec Adobe Analytics à l’aide du paramètre d’ajout AMO ID, également appelé `s_kwcid` qui se compose d’éléments spécifiques au canal publicitaire et au réseau publicitaire.

Le paramètre est ajouté à vos URL de suivi de l’une des manières suivantes :

* (Recommandé) La fonction d’insertion côté serveur est mise en oeuvre.

   * DSP clients : le serveur de pixels ajoute automatiquement le paramètre s_kwcid aux suffixes de votre page d’entrée lorsqu’un utilisateur final affiche une publicité avec le pixel Adobe Advertising.

   * Clients Search, Social et Commerce :

      * Pour [!DNL Google Ads] et [!DNL Microsoft® Advertising] compte avec la variable [!UICONTROL Auto Upload] activée pour le compte ou la campagne, le serveur de pixels ajoute automatiquement le paramètre s_kwcid aux suffixes de votre page d’entrée lorsqu’un utilisateur clique sur une publicité avec le pixel Adobe Advertising.

      * Pour d’autres réseaux publicitaires, ou [!DNL Google Ads] et [!DNL Microsoft® Advertising] compte avec la variable [!UICONTROL Auto Upload] désactivé, ajoutez manuellement le paramètre aux paramètres d’ajout au niveau du compte, qui l’ajoutent à vos URL de base.

* La fonction d’insertion côté serveur n’est pas mise en oeuvre :

   * DSP clients :

      * Pour [!DNL Flashtalking] balises publicitaires, insérer manuellement des macros supplémentaires par &quot;[Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Flashtalking] Balises publicitaires](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Pour [!DNL Google Campaign Manager 360] balises publicitaires, insérer manuellement des macros supplémentaires par &quot;[Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Google Campaign Manager 360] Balises publicitaires](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Clients Search, Social et Commerce :

      * Pour ([!DNL Google Ads] et [!DNL Microsoft® Advertising]) publicités, ajoutez manuellement le paramètre AMO ID à vos suffixes de page d’entrée.

      * Pour les publicités sur tous les autres réseaux publicitaires, ajoutez manuellement le paramètre AMO ID aux paramètres d’ajout au niveau du compte, qui l’ajoutent à vos URL de base.

Pour mettre en oeuvre la fonction d’insertion côté serveur ou déterminer la meilleure option pour votre entreprise, contactez votre équipe de compte d’Adobe.

Pour connaître les formats AMO ID pour DSP et Search, Social et Commerce, voir &quot;[ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* (Recherche, Social et Commerce) [Gestion des comptes de réseau publicitaire](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* (Recherche, Social et Commerce) [Paramètres de campagne Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* (Recherche, Social et Commerce) [Paramètres de campagne Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* (Recherche, Social et Commerce) [Paramètres de campagne Microsoft® Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* (Recherche, Social et Commerce) [Yahoo ! Paramètres de campagne Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* (Recherche, Social et Commerce) [Paramètres de campagne Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
