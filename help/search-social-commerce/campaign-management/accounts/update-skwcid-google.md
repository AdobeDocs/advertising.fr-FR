---
title: "Mise à jour du code de suivi s\_kwcid pour un [!DNL Google Ads] account"
description: Découvrez comment passer au code de suivi s_kwcid le plus récent pour une [!DNL Google Ads] compte .
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Mettez à jour le code de suivi s\_kwcid pour un événement [!DNL Google Ads] account

*Annonceurs avec une intégration Advertising-Adobe Analytics Adobe uniquement*

*[!DNL Google Ads]comptes uniquement*

Le format hérité du code de suivi s\_kwcid pour existant [!DNL Google Ads] Les comptes ne prennent pas en charge certaines fonctionnalités d’Analytics, telles que la création de rapports aux niveaux de la campagne et du groupe publicitaire pour [!DNL Google Ads] campagnes de performances max, campagnes de brouillons et d’expériences, ainsi que d’autres cas d’utilisation dans lesquels la même combinaison ad+keyword+match type existe dans plusieurs campagnes.

Le dernier format comprend des paramètres pour l’identifiant de campagne et l’identifiant du groupe publicitaire :

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Vous pouvez modifier, individuellement, le nouveau format pour l’un ou l’ensemble de vos comptes existants. Si vous ne disposez pas de campagnes ou de brouillons et de campagnes d’expérience de performances maximales, la migration vers le nouveau format est facultative.

Toutes nouvelles [!DNL Google Ads] Les comptes utilisent automatiquement le nouveau format s\_kwcid .

>[!NOTE]
>
>Une fois que vous avez migré un compte, toutes les données de clic, de coût et d’impression sont correctement consignées après la modification, mais tous les clics publicitaires qui se sont produits avant la migration sont toujours attribués aux données de conversion en fonction de l’ancien format s\_kwcid .

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. Placez le curseur sur le nom du compte, puis cliquez sur ![icône déroulante flèche](/help/search-social-commerce/assets/arrow-dropdown-menu.png), puis sélectionnez **[!UICONTROL Edit]**.
1. Cliquez sur **[!UICONTROL Set Account Tracking]**.
1. Commencer la migration :

   1. En regard de **[!UICONTROL S_KWCID FORMAT]** , cliquez sur **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. Cliquez sur **[!UICONTROL Migrate to new s_kwcid format]**.
   1. Dans le message de confirmation, cochez la case, puis cliquez sur **[!UICONTROL Continue]**.
   1. Dans les paramètres du compte, cliquez sur **[!UICONTROL Post]**.

   Les métadonnées des campagnes sont mises à jour dans Analytics en quelques jours. Le suivi se poursuit sans interruption, de sorte qu’aucune donnée n’est perdue, mais la création de rapports peut ne pas refléter les nouveaux codes de suivi tant qu’Analytics n’a pas reçu toutes les métadonnées.

   >[!NOTE]
   >
   >Tous les clics publicitaires qui se sont produits avant la migration génèrent toujours des rapports sur les données de conversion en fonction de l’ancien format.

1. Une fois la migration commencée, mettez à jour les paramètres du suffixe de la page d’entrée (appelés &quot;suffixe URL final&quot; dans certains réseaux publicitaires) si nécessaire :

   * Lorsque la fonction &quot;Chargement automatique&quot; est activée dans les paramètres de suivi, Search, Social et Commerce met automatiquement à jour le code de suivi dans le suffixe de page d’entrée pour ce compte et ses campagnes. Tu n&#39;es pas obligé de faire quoi que ce soit.
   * Lorsque la fonction &quot;Chargement automatique&quot; n’est pas activée et que vous n’utilisez pas le s-kwcid côté serveur, vous devez mettre à jour manuellement le paramètre s\_kwcid dans les paramètres du suffixe de page d’entrée. Vous pouvez modifier manuellement les suffixes au niveau du compte et de la campagne dans les paramètres du compte et de la campagne ou en chargeant les modifications dans une feuille d’envoi groupé. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez la méthode [!DNL Google Ads] éditeur.
   * Si vous incluez le paramètre s\_kwcid dans le paramètre URL de base de n’importe quel composant de campagne, déplacez-le vers le paramètre Suffixe de page d’entrée approprié.

1. (Recommandé) Vérifiez les données de ce compte dans Analytics avant de migrer des comptes supplémentaires.

>[!MORELIKETHIS]
>
>* [Gestion des comptes de réseau publicitaire](ad-network-account-manage.md)
>* [Le paramètre de suivi s_kwcid](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [Présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html)

