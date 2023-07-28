---
title: Formats de suivi des clics pour [!DNL Google Ads]
description: Découvrez les formats de suivi des clics pour [!DNL Google Ads] comptes.
exl-id: 68f6da43-3430-4c0a-9369-937fa52c071a
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Formats de suivi des clics pour [!DNL Google Ads]

Vous trouverez ci-dessous les formats de modèle de suivi de base et de suffixe de page d’entrée (suffixe URL final) requis par Search, Social et Commerce pour [!DNL Google Ads].

## Formats des modèles de tracking

### Réseau de recherche/d’affichage, y compris les liens de site

Le format suivant s’applique à tous les types d’annonces pouvant faire l’objet d’un suivi sur les réseaux de recherche et d’affichage, ainsi qu’aux liens de site.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemple :

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si la transmission de jeton est désactivée, remplacez `cq?` after `<advertiser_ID>` avec `c?`.
>
>* La variable [!DNL ValueTrack] Les paramètres pour indiquer les URL finales dans les modèles de suivi doivent être : `{lpurl}` ou `!{unescapedurl}`.
>
>* (Publicités texte) Lorsque vous enchérissez par mot-clé, le paramètre `ev_pl` (pour les emplacements) n’a aucune valeur. Lorsque vous enchérissez par emplacement, `ev_ln` (pour les mots-clés) n’a aucune valeur. Lorsque vous enchérissez par groupe publicitaire ou par une autre dimension, les deux `ev_ln` et `ev_pl` n’ont aucune valeur.
>
>* (Publicités de recherche dynamique) `{keyword}` indique l’expression de la cible de recherche dynamique, telle que `_cat:[VALUE]` ou `_url:[VALUE]`.
>
>* (Publicités de recherche dynamique) [!DNL Google Ads] détermine l’URL finale de manière dynamique, de sorte que vous n’ayez pas à en saisir une.
>
>* (Liens de site) Vous pouvez identifier les conversions résultant d’un clic sur un lien de site en générant une [!UICONTROL Transaction Report]. La variable [!UICONTROL Link Type] la valeur de colonne d’un lien de site est `sl:<Sitelink text>`, par exemple `sl:See Current Offers`.

### Réseau commercial

Le format suivant s’applique aux publicités commerciales et aux groupes de produits des réseaux commerciaux. Vous pouvez spécifier un modèle de suivi au niveau du compte, de la campagne, du groupe publicitaire ou du groupe de produits.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemple :

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si la transmission de jeton est désactivée, remplacez `cq?` after `<advertiser_ID>` avec `c?`.
>
>* La variable [!DNL ValueTrack] Les paramètres pour indiquer les URL finales dans les modèles de suivi doivent être : `{lpurl}` ou `!{unescapedurl}`.
>
>* [!DNL Google Ads] utilise les URL de produit dans le flux Google Merchant Center comme URL finales, de sorte que vous n’ayez pas à saisir d’URL finales pour vos données de produit ou groupes de produits.
>
>* Vous pouvez identifier les conversions résultant d’un clic sur une publicité d’achat en générant une [!UICONTROL Transaction Report]. La variable [!UICONTROL Link Type] valeur de colonne pour une publicité de produit :`<product ID>`, par exemple `pla:8525822`.

## Formats des suffixes de landing page (suffixe URL final)

Les comptes qui utilisent le suivi de conversion d’Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`gclid` pour [!DNL Google Ads]) dans le suffixe :

* Lorsque l’annonceur dispose d’une intégration Adobe Analytics, le suffixe doit inclure l’un des éléments suivants :

   * [!DNL Google Ads] les comptes qui utilisent la dernière `s_kwcid` format , qui prend en charge la création de rapports au niveau des campagnes et des groupes publicitaires pour les performances max des campagnes et les campagnes de brouillons et d’expériences :

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Si le compte comporte une implémentation s_kwcid côté serveur et le paramètre de compte ou de campagne &quot;[!UICONTROL Auto Upload]&quot; est activé, puis le paramètre est ajouté automatiquement. Sinon, vous devez l’ajouter manuellement.

   * Toutes les autres [!DNL Google Ads] comptes :

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Lorsque l’annonceur ne dispose pas d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Les suffixes de page d’entrée aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur du réseau publicitaire.
>
>* (Publicités de recherche dynamique ; annonceurs avec Adobe Analytics et sans suivi côté serveur) Lorsque vous souhaitez inclure le suivi du flux inverse de l’Adobe Advertising à Analytics, ajoutez le `s_kwcid` code de suivi jusqu’à la fin du suffixe de page d’entrée au niveau du compte.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion Adobe Advertising](formats-click-tracking-about.md)
>* [Formats du code de suivi s\_kwcid](skwcid-tracking-parameter.md)
