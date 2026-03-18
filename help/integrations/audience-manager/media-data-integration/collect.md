---
title: Collecter les données de clics et d’impressions des campagnes Advertising DSP
description: Découvrez comment capturer des événements d’impression et de clic basés sur des cookies à partir d’annonces Advertising DSP à l’aide de pixels Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Collecter des données d’exposition aux médias à partir de campagnes Advertising DSP

*Annonceurs avec Advertising DSP uniquement*

*Publicitaires avec une intégration Adobe Advertising-Adobe Audience Manager uniquement*

Ce document explique comment baliser les publicités Advertising DSP pour capturer des événements d’impression et de clic basés sur des cookies à l’aide de pixels Audience Manager. Il décrit également les tâches supplémentaires nécessaires à l’utilisation des données.

Les pixels d’événement ne capturent pas les événements qui se produisent dans des environnements sans cookies, tels que les applications mobiles et la télévision connectée (CTV).

## Étape 1 : configurer une source de données dans Audience Manager {#set-up-data-source}

Dans Audience Manager, créez une [source de données](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=fr) pour l’impression DSP, puis cliquez sur les données. Incluez l’identifiant de source de données [dans chaque balise d’événement](#implement-dsp-pixels) afin que tous les événements suivis soient attribués à la source de données.

>[!NOTE]
> Il est possible de collecter toutes les données d’impression et de clic pour les campagnes publicitaires s’exécutant sur plusieurs DSP dans une seule source de données.

## Étape 2 : implémenter des pixels d’événement d’impression et de clic sur les pages web {#implement-dsp-pixels}

Les annonceurs peuvent créer et implémenter des balises d’événement pour leurs propres marques. Si nécessaire, contactez votre consultant Adobe Audience Manager ou l’équipe en charge de votre compte Adobe pour obtenir de l’aide.

>[!NOTE]
>
>Si votre entreprise utilise le suivi des clics [!DNL Analytics], vous n’aurez peut-être pas besoin du suivi des clics Audience Manager. Adobe Analytics capture les signaux de clic et peut les envoyer à Audience Manager par le biais du [&#x200B; transfert côté serveur &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=fr).

### Syntaxe des pixels

Les pixels d’événement doivent inclure les paramètres suivants.

**Pixels de suivi d’impression :**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

avec comme [paramètres supplémentaires facultatifs](#parameters) le préfixe `&` ;

**pixels de suivi des clics :**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

avec comme [paramètres supplémentaires facultatifs](#parameters) le préfixe `&` ;

Où :

* `[Audience Manager customer domain]` est le nom de domaine qui enverra les événements d’impression ou de clic à [!DNL Adobe].

* `[source id]` est l’identifiant de la [source de données](#set-up-data-source) dans laquelle vous suivez l’impression DSP et cliquez sur les données.

* `[redirect URL]` est l’URL de redirection codée en double. Si vous utilisez un outil de codage en ligne, tel que www.urlencoder.org, exécutez la chaîne à l’aide de l’encodeur et codez à nouveau le résultat.

* `${TM_CAMPAIGN_ID_NUM}` est l’identifiant numérique de campagne dans DSP. Si vous souhaitez coder en dur un identifiant de campagne individuel au lieu d’utiliser la macro DSP, recherchez l’identifiant dans les paramètres de la campagne.

* Chaque [paramètre](#key-value-pairs) est précédé du préfixe `&` et est au format `d_parameter=parameter_id`, où `parameter` est remplacé par la paire clé-valeur pour le nouveau champ. Exemple : `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Paramètres en tant que paires clé-valeur {#parameters}

**Format:** `d_parameter=parameter_id`

    où:
    
    * le paramètre est précédé du préfixe «&amp; »
    
    * « parameter » est remplacé par la paire clé-valeur pour le nouveau champ
    
    Exemple : `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Les deux types de pixels peuvent contenir des paramètres supplémentaires sous la forme de *paires clé-valeur* pour collecter des caractéristiques ou fournir des métadonnées de campagne (comme un nom d’emplacement ou un nom de campagne) pour d’autres rapports. Une paire clé-valeur se compose de deux éléments associés : une *clé*, qui est une constante définissant le jeu de données, et une *valeur*, qui est une variable appartenant au jeu.

Dans la paire clé-valeur, la variable valeur peut être un identifiant codé en dur ou une *macro*, qui est une petite unité de code autonome remplacée dynamiquement par les valeurs correspondantes lors du chargement de la balise publicitaire pour la campagne et le suivi des utilisateurs. Pour les paramètres liés à la campagne, vous pouvez utiliser [les macros DSP](/help/dsp/campaign-management/macros.md) au lieu des macros Audience Manager, afin d’envoyer les attributs de campagne avec les données d’impression ou de clic correspondantes à Audience Manager, à l’aide d’un seul pixel sur toutes les publicités. Les macros DSP que vous insérez dans les pixels d’événement doivent être des valeurs appropriées pour les paires clé-valeur que vous incluez dans les pixels. Par exemple, pour la clé `d_placement`, vous utiliserez la macro DSP `${TM_PLACEMENT_ID_NUM}` comme valeur pour capturer les identifiants d&#39;emplacement générés par la macro Adobe Advertising.

Pour obtenir une liste des macros prises en charge par Audience Manager pour les pixels d’événement d’impression, voir « [Capture de données d’impression de campagne via des appels de pixels](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=fr#supported-key-value-pairs) ».

Pour obtenir une liste des macros prises en charge par Audience Manager pour les pixels d’événement de clic, voir « [Capture des données de clic de Campaign via des appels de pixels](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html?lang=fr) ».

>[!TIP]
>
>* Il est recommandé d’inclure les identifiants de la campagne, de l’emplacement, des créations (annonces) et du site afin de pouvoir utiliser les attributs de la campagne pour créer des caractéristiques Audience Manager.
>* Pour créer des rapports Audience Optimization, des paramètres supplémentaires sont requis.
>* Dans les paires clé-valeur, remplacez les valeurs par les [macros DSP appropriées](/help/dsp/campaign-management/macros.md) afin de pouvoir utiliser un seul pixel sur toutes les publicités de toutes les campagnes. Par exemple, remplacez `d_campaign=[%campaignID%]` par `d_campaign=${TM_CAMPAIGN_ID_NUM}` pour capturer les identifiants de campagne générés par la macro Adobe Advertising.
>* Si nécessaire, vous pouvez créer vos propres paramètres avec des valeurs codées en dur. Exemple : `d_DSP=AdCloud`

Exemple de pixel d&#39;événement d&#39;impression :

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Où ajouter les pixels

#### Pixel de suivi d’impression

Joignez un pixel de suivi d’événement d’impression à toutes les annonces de vos campagnes [!DNL DSP]. Vous pouvez le faire dans l’un des emplacements suivants :

* Au niveau de l’emplacement : applique le pixel par défaut à toutes les publicités de l’emplacement. Dans la section Suivi des paramètres d’emplacement, ajoutez le pixel dans le champ [[!UICONTROL Event pixels] &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md).

* Au niveau de l’annonce publicitaire, qui remplace tous les pixels d’événement au niveau de l’emplacement. Dans les paramètres de l’annonce publicitaire, [créez un pixel d’événement sur l’onglet [!UICONTROL Pixel]](/help/dsp/campaign-management/ads/ad-edit.md).

* (Pour les publicités sur un serveur de publicités tiers) Au niveau de la publicité dans le serveur de publicités.

#### pixel de suivi des clics

Dans le serveur de publicités, insérez le pixel d’événement de clic (avec l’URL codée en annexe) à l’endroit où vous insérez normalement l’URL de clic publicitaire de la publicité.

## Étape 3 : tâches post-implémentation

Une fois les balises d’événement implémentées, les données sont transmises aux serveurs de collecte de données d’Audience Manager. Effectuez les tâches suivantes avant de pouvoir utiliser les données dans les rapports.

### Créer un compartiment [!DNL Amazon S3] et une source de données

Une fois que vos données se trouvent sur les serveurs Audience Manager, vous devez créer un compartiment [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), puis une source de données, vers laquelle toutes les données de pixels sont envoyées. Contactez votre consultant Audience Manager ou l’[assistance clientèle](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html?lang=fr) si vous avez besoin d’aide.

### Création de caractéristiques et de segments Audience Manager

Les données d’événement sont transmises à Audience Manager sous la forme [signaux inutilisés](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html?lang=fr). Créez manuellement des [caractéristiques basées sur des règles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=fr) à partir des données ingérées, puis créez des [segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html?lang=fr) à l’aide de ces caractéristiques, avant de pouvoir utiliser les données dans les rapports.

Exemple de caractéristique qui renseigne les données au niveau de l’utilisateur pour les utilisateurs exposés à une création spécifique dans DSP :

1. Identifiez l’événement comme `d_event = imp`.
1. Identifiez l’ID de contenu créatif dans la campagne DSP, puis mappez-le à la caractéristique en tant que `d_creative=[Creative ID]`.

![Écran de création des caractéristiques](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
>* [Présentation de l’envoi de données d’exposition aux médias DSP vers Adobe Audience Manager](overview.md)
>* [Cas pratiques](use-cases.md)
