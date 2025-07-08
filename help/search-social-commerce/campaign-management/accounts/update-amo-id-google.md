---
title: 'Mettre à jour le code de suivi AMO ID (s_kwcid) pour un compte  [!DNL Google Ads] '
description: Découvrez comment passer au dernier code de suivi AMO ID pour un compte  [!DNL Google Ads] .
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Mettre à jour le code de suivi AMO ID (s_kwcid) pour un compte [!DNL Google Ads]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Comptes *[!DNL Google Ads]uniquement*

Le format hérité (antérieur à octobre 2019) du [code de suivi AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) pour les comptes [!DNL Google Ads] existants ne prend pas en charge certaines fonctionnalités d’Analytics, telles que le compte rendu des performances au niveau de la campagne et du groupe publicitaire pour les campagnes à performances maximales [!DNL Google Ads], les campagnes à brouillons et à expériences, ainsi que d’autres cas d’utilisation dans lesquels la même combinaison de type ad+mot-clé+correspondance existe dans plusieurs campagnes.

Le format actuel inclut les paramètres pour l’identifiant de campagne et l’identifiant de groupe publicitaire :

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Pour un compte existant qui utilise le format hérité, vous pouvez modifier le format actuel. Si vous ne disposez pas de campagnes Performance Max ou de campagnes de brouillons et d’expériences, la migration vers le nouveau format est facultative.

Tous les nouveaux comptes [!DNL Google Ads] utilisent automatiquement le format d’identifiant AMO actuel.

>[!NOTE]
>
>Cette option est disponible uniquement pour les comptes qui n’utilisent pas le format actuel.
>
>Après la migration d’un compte, toutes les données relatives aux clics, aux coûts et aux impressions sont correctement signalées après la modification. Cependant, tous les clics publicitaires survenus avant la migration sont toujours attribués aux données de conversion en fonction de l’ancien format d’identifiant AMO.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, cliquez sur ![icône déroulante de flèche](/help/search-social-commerce/assets/arrow-dropdown-menu.png), puis sélectionnez **[!UICONTROL Edit]**.

1. Cliquez sur **[!UICONTROL Set Account Tracking]**.

1. Commencez la migration :

   1. En regard de **[!UICONTROL S_KWCID FORMAT]** dans les paramètres [!UICONTROL Account Tracking], cliquez sur **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Cliquez sur **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Dans le message de confirmation, activez la case à cocher, puis cliquez sur **[!UICONTROL Continue]**.

   1. Dans les paramètres du compte, cliquez sur **[!UICONTROL Post]**.

   Les métadonnées des campagnes sont mises à jour en [!DNL Analytics] en quelques jours. Le suivi se poursuit sans interruption, de sorte qu’aucune donnée n’est perdue, mais les rapports peuvent ne pas refléter les nouveaux codes de suivi tant que [!DNL Analytics] n’a pas reçu toutes les métadonnées.

   >[!NOTE]
   >
   >Tous les clics publicitaires qui se sont produits avant la migration signalent toujours les données de conversion selon l’ancien format.

1. Après avoir commencé la migration, mettez à jour les paramètres du suffixe de la page de destination (appelé « suffixe d’URL final » dans certains réseaux publicitaires) si nécessaire :

   * Lorsque la fonction [!UICONTROL Auto Upload] » est activée dans les paramètres de tracking, Search, Social et Commerce met automatiquement à jour le code de tracking dans le Suffixe de la page de destination pour ce compte et ses campagnes. Vous n&#39;avez rien à faire.

   * Lorsque la fonction [!UICONTROL Auto Upload] » n’est pas activée et que vous n’utilisez pas la fonction [ID AMO côté serveur](/help/integrations/analytics/ids.md#amo-id-formats), vous devez mettre à jour manuellement le paramètre ID AMO dans les paramètres du suffixe de la page de destination. Vous pouvez modifier manuellement les suffixes au niveau du compte et de la campagne dans les [paramètres du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) et [paramètres de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) ou en [téléchargeant les modifications dans une feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md). Pour configurer un suffixe au niveau du groupe publicitaire ou à un niveau inférieur, utilisez l’éditeur de [!DNL Google Ads].

   * Si vous incluez l’ID AMO dans le paramètre URL de base pour n’importe quel composant de campagne, déplacez-le vers le paramètre Suffixe de page de destination approprié.

1. (Recommandé) Vérifiez les données de ce compte dans [!DNL Analytics] avant de migrer des comptes supplémentaires.

>[!MORELIKETHIS]
>
>* [Gérer les comptes de réseau publicitaire](ad-network-account-manage.md)
>* [ID Adobe Advertising utilisés par  [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Présentation de  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html?lang=fr){target="_blank"}
