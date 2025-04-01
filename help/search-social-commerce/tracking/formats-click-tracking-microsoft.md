---
title: Formats de suivi des clics pour  [!DNL Microsoft Advertising]
description: Découvrez les formats de suivi des clics pour les comptes  [!DNL Microsoft Advertising] .
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Formats de suivi des clics pour les [!DNL Microsoft Advertising]

Vous trouverez ci-dessous les formats de modèle de suivi de base et de suffixe de page de destination (suffixe d’URL final) requis par Search, Social et Commerce pour [!DNL Microsoft Advertising].

## Formats des modèles de tracking

### Réseaux de recherche et d&#39;audience (sauf pour les liens de sites)

Le format suivant s’applique à tous les types d’annonces pouvant faire l’objet d’un suivi sur les réseaux de recherche et d’audience.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable pour l’ID unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission du jeton est activée pour la campagne (valeur par défaut). Si la transmission du jeton est désactivée, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `{TargetId}` représente l’ID de a) le mot-clé ou b) le mot-clé et la liste de remarketing (audience) qui ont déclenché la publicité (par exemple, « kwd-123:aud-456 » pour un mot-clé et une liste de remarketing ou « kwd-123 » pour le mot-clé uniquement).

### Liens du site

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable pour l’ID unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission du jeton est activée pour la campagne (valeur par défaut). Si la transmission du jeton est désactivée, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `{TargetId}` représente l’ID de a) le mot-clé ou b) le mot-clé et la liste de remarketing (audience) qui ont déclenché la publicité (par exemple, « kwd-123:aud-456 » pour un mot-clé et une liste de remarketing ou « kwd-123 » pour le mot-clé uniquement).
>
>* `{adextensionid}` n’est pas utilisé.
>
>* (Liens de site) Vous pouvez voir quelles conversions ont résulté d’un clic sur un lien de site en générant un [!UICONTROL Transaction Report]. La valeur de colonne [!UICONTROL Link Type] pour un lien de site est `sl:<Sitelink text>`, par exemple `sl:See Current Offers`.

### Réseau commercial

Les formats suivants s’appliquent aux annonces d’achats dans les réseaux d’achats. Vous pouvez définir un modèle de tracking au niveau du compte, de la campagne, du groupe publicitaire ou du groupe de produits.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable pour l’ID unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission du jeton est activée pour la campagne (valeur par défaut). Si la transmission du jeton est désactivée, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `{TargetId}` représente l’ID de a) le mot-clé ou b) le mot-clé et la liste de remarketing (audience) qui ont déclenché la publicité (par exemple, « kwd-123:aud-456 » pour un mot-clé et une liste de remarketing ou « kwd-123 » pour le mot-clé uniquement).
>
>* (Facultatif) Au lieu de saisir des modèles de suivi au niveau du compte, de la campagne, du groupe publicitaire ou du groupe de produits, vous pouvez ajouter l’URL de suivi aux données de produit dans le compte [!DNL Microsoft Merchant Center]. Pour ce faire, incluez l’URL de tracking, ainsi que la valeur dans le champ « `link` » ou « `mobile_link` », selon le cas, dans une colonne personnalisée « [bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0) » dans le flux de produits. La valeur du champ « `bingads_redirect` » remplace celle des champs « `link` » et « `mobile_link` ». Les URL générées à l’aide de cette méthode n’incluent aucun paramètre de tracking spécifié dans les paramètres du compte Search, Social et Commerce ou de la campagne.

## Formats des suffixes des landing pages (suffixes des URL finales)

>[!NOTE]
>
>Les suffixes de page de destination de niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent est nécessaire pour les composants de compte individuels. Pour configurer un suffixe au niveau du groupe publicitaire ou à un niveau inférieur, utilisez l’éditeur du réseau publicitaire.

### Réseaux de recherche et d’audience

Les comptes qui utilisent le suivi des conversions Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`msclkid` par [!DNL Microsoft Advertising]) dans le suffixe :

* Lorsque l’annonceur dispose d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}`

* Lorsque l’annonceur ne dispose pas d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `&ev_efid={msclkid}:G:s`

### Réseau commercial

Les comptes qui utilisent le suivi des conversions Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`msclkid` par [!DNL Microsoft Advertising]) dans le suffixe :

* Lorsque l’annonceur dispose d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`

* Lorsque l’annonceur ne dispose pas d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi des conversions Adobe Advertising](formats-click-tracking-about.md)
>* [Formats d’ID AMO](/help/integrations/analytics/ids.md#amo-id-formats)
