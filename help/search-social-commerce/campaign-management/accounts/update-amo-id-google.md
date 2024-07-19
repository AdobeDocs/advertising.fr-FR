---
title: Mettez à jour le code de suivi AMO ID (s_kwcid) pour un compte  [!DNL Google Ads] .
description: Découvrez comment passer au code de suivi AMO ID le plus récent pour un compte  [!DNL Google Ads] .
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Mettre à jour le code de suivi AMO ID (s_kwcid) pour un compte [!DNL Google Ads]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*[!DNL Google Ads]comptes uniquement*

Le format hérité (avant octobre 2019) du [code de suivi AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) pour les comptes [!DNL Google Ads] existants ne prend pas en charge certaines fonctionnalités d’Analytics, telles que la création de rapports aux niveaux de la campagne et du groupe publicitaire pour [!DNL Google Ads] campagnes max de performances, campagnes de brouillons et d’expériences, ainsi que d’autres cas d’utilisation dans lesquels la même combinaison ad+mot-clé+type de correspondance existe dans plusieurs campagnes.

Le format actuel comprend des paramètres pour l’identifiant de campagne et l’identifiant du groupe publicitaire :

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Vous pouvez modifier le format actuel de n’importe quel ou de tous vos comptes existants, individuellement. Si vous ne disposez pas de campagnes ou de brouillons et de campagnes d’expérience de performances maximales, la migration vers le nouveau format est facultative.

Tous les nouveaux comptes [!DNL Google Ads] utilisent automatiquement le format AMO ID actuel.

>[!NOTE]
>
>Une fois que vous avez migré un compte, toutes les données de clic, de coût et d’impression sont correctement consignées après la modification, mais tous les clics publicitaires qui se sont produits avant la migration sont toujours attribués aux données de conversion en fonction de l’ancien format AMO ID.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, cliquez sur l’icône ![flèche déroulante](/help/search-social-commerce/assets/arrow-dropdown-menu.png), puis sélectionnez **[!UICONTROL Edit]**.

1. Cliquez sur **[!UICONTROL Set Account Tracking]**.

1. Commencer la migration :

   1. En regard de **[!UICONTROL S_KWCID FORMAT]** , cliquez sur **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Cliquez sur **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Dans le message de confirmation, cochez la case, puis cliquez sur **[!UICONTROL Continue]**.

   1. Dans les paramètres du compte, cliquez sur **[!UICONTROL Post]**.

   Les métadonnées des campagnes sont mises à jour dans [!DNL Analytics] en quelques jours. Le suivi se poursuit sans interruption, de sorte qu’aucune donnée n’est perdue, mais la création de rapports peut ne pas refléter les nouveaux codes de suivi tant que [!DNL Analytics] n’a pas reçu toutes les métadonnées.

   >[!NOTE]
   >
   >Tous les clics publicitaires qui se sont produits avant la migration continuent de reporter les données de conversion en fonction de l’ancien format.

1. Une fois la migration commencée, mettez à jour les paramètres du suffixe de la page d’entrée (appelés &quot;suffixe URL final&quot; dans certains réseaux publicitaires) si nécessaire :

   * Lorsque la fonction [!UICONTROL Auto Upload]&quot; est activée dans les paramètres de suivi, Search, Social et Commerce met automatiquement à jour le code de suivi dans le suffixe de page d’entrée pour ce compte et ses campagnes. Tu n&#39;es pas obligé de faire quoi que ce soit.

   * Lorsque la fonction [!UICONTROL Auto Upload]&quot; n’est pas activée et que vous n’utilisez pas la [ fonction AMO ID côté serveur ](/help/integrations/analytics/ids.md#amo-id-formats), vous devez mettre à jour manuellement le paramètre AMO ID dans les paramètres du suffixe de page d’entrée. Vous pouvez modifier manuellement les suffixes au niveau du compte et de la campagne dans les paramètres du compte et de la campagne ou en chargeant les modifications dans une feuille d’envoi groupé. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur [!DNL Google Ads].

   * Si vous incluez l’AMO ID dans le paramètre d’URL de base d’un composant de campagne, déplacez-le vers le paramètre approprié de suffixe de page d’entrée.

1. (Recommandé) Vérifiez les données de ce compte dans [!DNL Analytics] avant de migrer des comptes supplémentaires.

>[!MORELIKETHIS]
>
>* [Gérer des comptes réseau publicitaires](ad-network-account-manage.md)
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
