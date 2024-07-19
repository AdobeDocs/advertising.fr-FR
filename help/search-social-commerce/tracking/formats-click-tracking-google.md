---
title: Formats de suivi des clics pour [!DNL Google Ads]
description: Découvrez les formats de suivi des clics pour les comptes  [!DNL Google Ads] .
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Formats de suivi des clics pour [!DNL Google Ads]

Vous trouverez ci-dessous les formats de modèle de suivi de base et de suffixe de page d’entrée (suffixe d’URL final) requis par Search, Social et Commerce pour [!DNL Google Ads].

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
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si le transfert de jeton est désactivé, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* Les paramètres [!DNL ValueTrack] pour indiquer les URL finales dans les modèles de suivi doivent être `{lpurl}` ou `!{unescapedurl}`.
>
>* (Publicités texte) Lorsque vous enchérissez par mot-clé, le paramètre `ev_pl` (pour les emplacements) n’a aucune valeur. Lorsque vous enchérissez par emplacement, `ev_ln` (pour les mots-clés) n’a aucune valeur. Lorsque vous enchérissez par groupe publicitaire ou par toute autre dimension, `ev_ln` et `ev_pl` n’ont aucune valeur.
>
>* (Publicités de recherche dynamique) `{keyword}` indique l’expression cible de recherche dynamique, telle que `_cat:[VALUE]` ou `_url:[VALUE]`.
>
>* (Publicités de recherche dynamique) [!DNL Google Ads] détermine dynamiquement l’URL finale, de sorte que vous n’ayez pas à en saisir une.
>
>* (Liens de site) Vous pouvez voir les conversions résultant d’un clic sur un lien de site en générant un [!UICONTROL Transaction Report]. La valeur de colonne [!UICONTROL Link Type] pour un lien de site est `sl:<Sitelink text>`, comme `sl:See Current Offers`.

### Réseau commercial

Le format suivant s’applique aux publicités commerciales et aux groupes de produits des réseaux commerciaux. Vous pouvez spécifier un modèle de suivi au niveau du compte, de la campagne, du groupe publicitaire ou du groupe de produits.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Exemple :

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si le transfert de jeton est désactivé, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* Les paramètres [!DNL ValueTrack] pour indiquer les URL finales dans les modèles de suivi doivent être `{lpurl}` ou `!{unescapedurl}`.
>
>* [!DNL Google Ads] utilise les URL de produit dans le flux Google Merchant Center comme URL finales, de sorte que vous n’avez pas besoin de saisir les URL finales pour vos données de produit ou groupes de produits.
>
>* Vous pouvez voir les conversions qui ont résulté d’un clic sur une publicité d’achat en générant un [!UICONTROL Transaction Report]. La valeur de colonne [!UICONTROL Link Type] pour une publicité de produit est pla:`<product ID>`, par exemple `pla:8525822`.

## Formats des suffixes de landing page (suffixe URL final)

Les comptes qui utilisent le suivi de conversion d’Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`gclid` pour [!DNL Google Ads]) dans le suffixe :

* Lorsque l’annonceur dispose d’une intégration Adobe Analytics, le suffixe doit inclure l’un des éléments suivants :

   * [!DNL Google Ads] comptes qui utilisent le dernier [format AMO ID](/help/integrations/analytics/ids.md#amo-id-formats) (commençant par `s_kwcid`), qui prend en charge la création de rapports au niveau des campagnes et des groupes publicitaires pour les performances maximales des campagnes et des brouillons et campagnes d’expériences :

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Si le compte a une implémentation AMO ID côté serveur et que le paramètre de compte ou de campagne &quot;[!UICONTROL Auto Upload]&quot; est activé, le paramètre est ajouté automatiquement. Sinon, vous devez l’ajouter manuellement. Voir &quot;[ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement)&quot;.

   * Tous les autres comptes [!DNL Google Ads] :

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Lorsque l’annonceur ne dispose pas d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Les suffixes de page d’entrée aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur du réseau publicitaire.
>
>* (Publicités de recherche dynamique ; annonceurs avec Adobe Analytics et sans suivi côté serveur) Lorsque vous souhaitez inclure le suivi du flux inverse d’Adobe Advertising à Analytics, ajoutez le code de suivi AMO ID à la fin du suffixe de la page d’entrée au niveau du compte.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion d’Adobe Advertising](formats-click-tracking-about.md)
>* [Formats AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
