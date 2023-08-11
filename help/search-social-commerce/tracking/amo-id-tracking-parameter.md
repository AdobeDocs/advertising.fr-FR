---
title: Paramètre de suivi AMO ID (s_kwcid)
description: Découvrez le paramètre de suivi utilisé pour partager des données d’Adobe Advertising avec Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Paramètre de suivi AMO ID (s_kwcid)

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe Advertising partage des données sur vos campagnes avec Adobe Analytics à l’aide du paramètre d’ajout AMO ID, également appelé `s_kwcid` qui se compose d’éléments spécifiques au canal publicitaire et au réseau publicitaire.

<!-- add everything below to IDs page -->

Le paramètre est ajouté à vos URL de suivi de l’une des manières suivantes :

* (Recommandé) La fonction d’insertion côté serveur est mise en oeuvre.

  Pour [!DNL Google Ads] et [!DNL Microsoft Advertising] compte avec la variable [!UICONTROL Auto Upload] activée pour le compte ou la campagne, le serveur de pixels ajoute automatiquement le paramètre AMO ID aux suffixes de votre landing page lorsqu’un utilisateur clique sur une publicité <!-- click a search ad or views a display ad --> avec le pixel d’Adobe Advertising.

  Pour d’autres réseaux publicitaires, ou [!DNL Google Ads] et [!DNL Microsoft Advertising] compte avec la variable [!UICONTROL Auto Upload] désactivé, ajoutez manuellement le paramètre AMO ID aux paramètres d’ajout au niveau du compte, qui l’ajoutent à vos URL de base.

* <!-- (Search, Social, & Commerce only) -->La fonction d’insertion côté serveur n’est pas mise en oeuvre et vous devez ajouter manuellement le paramètre AMO ID à votre[!DNL Google Ads] et [!DNL Microsoft Advertising]) suffixes de page d’entrée ou paramètres d’ajout au niveau du compte au niveau du compte (autres réseaux publicitaires).

Pour mettre en oeuvre la fonction d’insertion côté serveur ou déterminer la meilleure option pour votre entreprise, contactez votre équipe de compte d’Adobe.

Pour connaître les formats AMO ID pour DSP et Search, Social et Commerce, voir &quot;[ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [Gestion des comptes de réseau publicitaire](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Paramètres de campagne Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Paramètres de campagne Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Paramètres de campagne Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo ! Paramètres de campagne Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Paramètres de campagne Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
