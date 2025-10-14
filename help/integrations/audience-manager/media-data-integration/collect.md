---
title: Collecte de données de clics et d’impressions à partir des campagnes Advertising DSP
description: Découvrez comment capturer des impressions basées sur des cookies et des événements de clic à partir de publicités Advertising DSP à l’aide de pixels d’Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Collecte de données d’exposition multimédia à partir des campagnes Advertising DSP

*Annonceurs avec Advertising DSP uniquement*

*Annonceurs avec une intégration Adobe Advertising-Adobe Audience Manager uniquement*

Ce document explique comment baliser les publicités Advertising DSP pour capturer des événements d’impression et de clic basés sur des cookies à l’aide de pixels d’Audience Manager, ainsi que des tâches supplémentaires nécessaires à l’utilisation des données.

Les pixels d’événement ne capturent pas les événements qui se produisent dans des environnements sans cookie, tels que les applications mobiles et la télévision connectée (CTV).

## Étape 1 : configuration d’une Source de données dans Audience Manager {#set-up-data-source}

Dans Audience Manager, créez une [source de données](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=fr) pour l’impression DSP et cliquez sur les données. Insérez l’ID de source de données [&#x200B; dans chaque balise d’événement &#x200B;](#implement-dsp-pixels) afin que tous les événements suivis soient attribués à la source de données.

>[!NOTE]
> Il est possible de collecter toutes les données d’impression et de clic pour les campagnes publicitaires s’exécutant sur plusieurs DSP au sein d’une seule source de données.

## Étape 2 : implémentation des pixels d’impression et d’événement de clic sur les pages web {#implement-dsp-pixels}

Les annonceurs peuvent créer et implémenter des balises d’événement pour leurs propres marques. Si nécessaire, contactez votre consultant Adobe Audience Manager ou votre équipe de compte d’Adobe pour obtenir de l’aide.

>[!NOTE]
>
>Si votre organisation utilise le suivi [!DNL Analytics], il se peut que vous n’ayez pas besoin du suivi des clics d’Audience Manager. Adobe Analytics capture les signaux de clic et peut les envoyer à l’Audience Manager par le biais du [transfert côté serveur](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=fr).

### Syntaxe des pixels

Les pixels d’événement doivent inclure les paramètres suivants.

**Pixels de suivi d’impression :**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

avec [&#x200B; paramètres supplémentaires facultatifs &#x200B;](#parameters) préfixés avec `&`

**Pixels de suivi des clics :**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

avec [&#x200B; paramètres supplémentaires facultatifs &#x200B;](#parameters) préfixés avec `&`

Où :

* `[Audience Manager customer domain]` est le nom de domaine qui enverra des événements d’impression ou de clic à [!DNL Adobe].

* `[source id]` est l’identifiant de la [source de données](#set-up-data-source) dans laquelle vous effectuez le suivi DSP données d’impression et de clic.

* `[redirect URL]` est l’URL de redirection codée deux fois. Si vous utilisez un outil de codage en ligne, tel que www.urlencoder.org, exécutez la chaîne via l’encodeur et codez à nouveau le résultat.

* `${TM_CAMPAIGN_ID_NUM}` est l’identifiant de campagne numérique dans DSP. Si vous souhaitez coder en dur un identifiant de campagne individuel au lieu d’utiliser la macro DSP, localisez l’identifiant dans les paramètres de la campagne.

* Chaque [paramètre](#key-value-pairs) est précédé du préfixe `&` et est au format `d_parameter=parameter_id`, où `parameter` est remplacé par la paire clé-valeur du nouveau champ. Exemple : `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Paramètres comme paires clé-valeur {#parameters}

**Format :** `d_parameter=parameter_id`

    où :
    
    * le paramètre est précédé du préfixe `&amp;`
    
    * `parameter` est remplacé par la paire clé-valeur du nouveau champ
    
    Exemple : `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`
&rbrace;
Les deux types de pixels peuvent contenir des paramètres supplémentaires, tels que des *paires clé-valeur*, pour collecter les caractéristiques ou fournir des métadonnées de campagne (comme un nom d’emplacement ou un nom de campagne) pour d’autres rapports. Une paire clé-valeur se compose de deux éléments associés : une *clé*, qui est une constante qui définit le jeu de données, et une *valeur*, qui est une variable qui appartient à l’ensemble.

Dans la paire clé-valeur, la variable valeur peut être un identifiant codé en dur ou une *macro*, qui est une petite unité de code autonome remplacée dynamiquement par les valeurs correspondantes lors du chargement de la balise publicitaire pour le suivi des campagnes et des utilisateurs. Pour les paramètres liés à la campagne, vous pouvez utiliser [Macros DSP](/help/dsp/campaign-management/macros.md) au lieu des macros d’Audience Manager pour envoyer les attributs de campagne avec les données d’impression ou de clic correspondantes à l’Audience Manager, à l’aide d’un seul pixel sur toutes les publicités. Les macros DSP que vous insérez dans les pixels de l’événement doivent être des valeurs appropriées pour les paires clé-valeur que vous incluez dans les pixels. Par exemple, pour la clé `d_placement`, vous utiliseriez la macro DSP `${TM_PLACEMENT_ID_NUM}` comme valeur pour capturer les identifiants d’emplacement générés par la macro Adobe Advertising.

Pour obtenir la liste des macros prises en charge par Audience Manager pour les pixels d’événement d’impression, voir &quot;[Capture des données d’impression de campagne via des appels de pixel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=fr#supported-key-value-pairs)&quot;.

Pour obtenir la liste des macros prises en charge par Audience Manager pour les pixels d’événement de clic, voir &quot;[Capture des données de clic de campagne via des appels de pixel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html?lang=fr)&quot;.

>[!TIP]
>
>* La bonne pratique consiste à inclure les identifiants de campagne, d’emplacement, de contenu créatif (publicitaire) et de site afin que vous puissiez utiliser les attributs de campagne pour créer des caractéristiques d’Audience Manager.
>* Pour créer des rapports d’Audience Optimization, des paramètres supplémentaires sont requis.
>* Dans les paires clé-valeur, remplacez les valeurs par les [macros DSP](/help/dsp/campaign-management/macros.md) appropriées afin que vous puissiez utiliser un seul pixel pour toutes les publicités dans toutes les campagnes. Par exemple, remplacez `d_campaign=[%campaignID%]` par `d_campaign=${TM_CAMPAIGN_ID_NUM}` pour capturer les identifiants de campagne générés par la macro Adobe Advertising.
>* Si nécessaire, vous pouvez créer vos propres paramètres avec des valeurs codées en dur. Exemple : `d_DSP=AdCloud`

Exemple de pixel d&#39;événement d&#39;impression :

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Où ajouter les pixels

#### Pixel de suivi d’impression

Joignez un pixel de suivi d&#39;événement d&#39;impression à toutes les publicités de vos campagnes [!DNL DSP]. Vous pouvez le faire à l’un des emplacements suivants :

* Au niveau de l’emplacement, qui applique le pixel par défaut à toutes les publicités de l’emplacement. Dans la section Suivi des paramètres de placement, ajoutez le pixel dans le champ [[!UICONTROL Event pixels]](/help/dsp/campaign-management/placements/placement-settings.md).

* Au niveau de la publicité, qui remplace tous les pixels d’événement de niveau placement. Dans les paramètres de publicité, [créez un pixel d&#39;événement sur l&#39;onglet [!UICONTROL Pixel]](/help/dsp/campaign-management/ads/ad-edit.md).

* (Pour les publicités sur un serveur de publicités tiers) Au niveau de la publicité dans le serveur de publicités.

#### Pixel de suivi des clics

Dans le serveur de publicités, insérez le pixel d’événement de clic (avec l’URL codée ajoutée) partout où vous insérez normalement l’URL de clic publicitaire de la publicité.

## Étape 3 : Tâches après mise en oeuvre

Une fois les balises d’événement implémentées, les données sont transmises aux serveurs de collecte de données d’Audience Manager. Effectuez les tâches suivantes avant de pouvoir utiliser les données dans les rapports.

### Création d’un compartiment [!DNL Amazon S3] et d’un Source de données

Une fois vos données sur les serveurs d’Audience Manager, vous devez créer un compartiment [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), puis une source de données, à laquelle toutes les données de pixel sont envoyées. Contactez votre conseiller en Audience Manager ou l’ [assistance clientèle](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html?lang=fr) si vous avez besoin d’assistance.

### Création de caractéristiques d’Audience Manager et de segments

Vos données d’événement se transforment en Audience Manager en [signaux inutilisés](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html?lang=fr). Créez manuellement des [&#x200B; caractéristiques basées sur des règles &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=fr) à partir des données ingérées, puis créez des [segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html?lang=fr) à l’aide de ces caractéristiques avant de pouvoir utiliser les données dans les rapports.

Exemple de caractéristique qui renseigne les données au niveau de l’utilisateur pour les utilisateurs exposés à un contenu créatif spécifique dans DSP :

1. Identifiez l’événement comme `d_event = imp`.
1. Identifiez l’ID créatif dans la campagne DSP, puis mappez-le à la caractéristique `d_creative=[Creative ID]`.

![Écran de création de caractéristiques](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
>* [Présentation de l’envoi DSP données d’exposition aux médias à Adobe Audience Manager](overview.md)
>* [Cas d’utilisation](use-cases.md)
