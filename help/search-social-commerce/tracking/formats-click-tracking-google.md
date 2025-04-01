---
title: Formats de suivi des clics pour  [!DNL Google Ads]
description: Découvrez les formats de suivi des clics pour les comptes  [!DNL Google Ads] .
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Formats de suivi des clics pour les [!DNL Google Ads]

Vous trouverez ci-dessous les formats de modèle de suivi de base et de suffixe de page de destination (suffixe d’URL final) requis par Search, Social et Commerce pour [!DNL Google Ads].

## Formats des modèles de tracking

### Réseau de recherche/affichage, y compris les liens de sites

Le format suivant s’applique à tous les types d’annonces traçables sur les réseaux de recherche et d’affichage, ainsi qu’aux liens de sites.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemple :

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable pour l’ID unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission du jeton est activée pour la campagne (valeur par défaut). Si la transmission du jeton est désactivée, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* Les paramètres [!DNL ValueTrack] pour indiquer les URL finales dans les modèles de tracking doivent être `{lpurl}` ou `!{unescapedurl}`.
>
>* (Annonces de texte) Lorsque vous enchérissez par mot-clé, le paramètre `ev_pl` (pour les emplacements) n’a aucune valeur. Lorsque vous enchérissez par emplacement, `ev_ln` (pour les mots-clés) n’a aucune valeur. Lorsque vous enchérissez par groupe publicitaire ou par toute autre dimension, `ev_ln` et `ev_pl` n’ont aucune valeur.
>
>* (Annonces de recherche dynamique) `{keyword}` indique l’expression cible de la recherche dynamique, telle que `_cat:[VALUE]` ou `_url:[VALUE]`.
>
>* (Annonces de recherche dynamique) [!DNL Google Ads] détermine l’URL finale de manière dynamique, de sorte que vous n’avez pas besoin d’en saisir une.
>
>* (Liens de site) Vous pouvez voir quelles conversions ont résulté d’un clic sur un lien de site en générant un [!UICONTROL Transaction Report]. La valeur de colonne [!UICONTROL Link Type] pour un lien de site est `sl:<Sitelink text>`, par exemple `sl:See Current Offers`.

### Réseau commercial

Le format suivant s’applique aux annonces d’achats et aux groupes de produits dans les réseaux d’achat. Vous pouvez définir un modèle de tracking au niveau du compte, de la campagne, du groupe publicitaire ou du groupe de produits.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemple :

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable pour l’ID unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission du jeton est activée pour la campagne (valeur par défaut). Si la transmission du jeton est désactivée, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* Les paramètres [!DNL ValueTrack] pour indiquer les URL finales dans les modèles de tracking doivent être `{lpurl}` ou `!{unescapedurl}`.
>
>* [!DNL Google Ads] utilise les URL de produit dans le flux du Centre commercial Google comme URL finales. Vous n’avez donc pas besoin de saisir les URL finales pour vos données de produit ou groupes de produits.
>
>* Vous pouvez voir quelles conversions ont résulté d’un clic sur une annonce d’achat en générant une [!UICONTROL Transaction Report]. La valeur de colonne [!UICONTROL Link Type] pour une annonce publicitaire de produit est pla:`<product ID>`, par exemple `pla:8525822`.

## Formats des suffixes des landing pages (suffixes des URL finales)

Les comptes qui utilisent le suivi des conversions Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`gclid` par [!DNL Google Ads]) dans le suffixe :

* Lorsque l’annonceur dispose d’une intégration Adobe Analytics, le suffixe doit inclure l’un des éléments suivants :

   * [!DNL Google Ads] les comptes qui utilisent le dernier [format d’identifiant AMO](/help/integrations/analytics/ids.md#amo-id-formats) (commençant par `s_kwcid`), qui prend en charge le reporting au niveau de la campagne et du groupe publicitaire pour les campagnes de type Performances max , ainsi que les campagnes sous forme de brouillons et d’expériences :

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Si le compte possède une implémentation AMO ID côté serveur et que le compte ou le paramètre de campagne « [!UICONTROL Auto Upload] » est activé, le paramètre est automatiquement ajouté. Sinon, vous devez l’ajouter manuellement. Voir « [Adobe Advertising IDs utilisés par  [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement). »

   * Tous les autres comptes [!DNL Google Ads] :

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Lorsque l’annonceur ne dispose pas d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Les suffixes de page de destination de niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent est nécessaire pour les composants de compte individuels. Pour configurer un suffixe au niveau du groupe publicitaire ou à un niveau inférieur, utilisez l’éditeur du réseau publicitaire.
>
>* (Annonces de recherche dynamique ; annonceurs avec Adobe Analytics et sans suivi côté serveur) Lorsque vous souhaitez inclure le suivi du flux inverse d’Adobe Advertising vers Analytics, ajoutez le code de suivi de l’ID AMO à la fin du suffixe de page de destination au niveau du compte.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi des conversions Adobe Advertising](formats-click-tracking-about.md)
>* [Formats d’ID AMO](/help/integrations/analytics/ids.md#amo-id-formats)
