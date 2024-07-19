---
title: Formats de suivi des clics pour [!DNL Microsoft Advertising]
description: Découvrez les formats de suivi des clics pour les comptes  [!DNL Microsoft Advertising] .
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Formats de suivi des clics pour [!DNL Microsoft Advertising]

Vous trouverez ci-dessous les formats de modèle de suivi de base et de suffixe de page d’entrée (suffixe d’URL final) requis par Search, Social et Commerce pour [!DNL Microsoft Advertising].

## Formats des modèles de tracking

### Réseaux de recherche et d’audience (sauf pour les liens de site)

Le format suivant s’applique à tous les types d’annonces pouvant faire l’objet d’un suivi sur les réseaux de recherche et d’audience.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si le transfert de jeton est désactivé, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `{TargetId}` représente l’identifiant de a) le mot-clé ou b) la liste de remarketing et le mot-clé (audience) qui ont déclenché la publicité (par exemple, &quot;kwd-123:aud-456&quot; pour un mot-clé et une liste de remarketing ou &quot;kwd-123&quot; pour le mot-clé uniquement).

### Liens de site

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si le transfert de jeton est désactivé, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `{TargetId}` représente l’identifiant de a) le mot-clé ou b) la liste de remarketing et le mot-clé (audience) qui ont déclenché la publicité (par exemple, &quot;kwd-123:aud-456&quot; pour un mot-clé et une liste de remarketing ou &quot;kwd-123&quot; pour le mot-clé uniquement).
>
>* `{adextensionid}` n’est pas utilisé.
>
>* (Liens de site) Vous pouvez voir les conversions résultant d’un clic sur un lien de site en générant un [!UICONTROL Transaction Report]. La valeur de colonne [!UICONTROL Link Type] pour un lien de site est `sl:<Sitelink text>`, comme `sl:See Current Offers`.

### Réseau commercial

Les formats suivants s’appliquent aux publicités commerciales dans les réseaux commerciaux. Vous pouvez spécifier un modèle de suivi au niveau du compte, de la campagne, du groupe publicitaire ou du groupe de produits.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si le transfert de jeton est désactivé, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `{TargetId}` représente l’identifiant de a) le mot-clé ou b) la liste de remarketing et le mot-clé (audience) qui ont déclenché la publicité (par exemple, &quot;kwd-123:aud-456&quot; pour un mot-clé et une liste de remarketing ou &quot;kwd-123&quot; pour le mot-clé uniquement).
>
>* (Facultatif) Au lieu de saisir des modèles de suivi au niveau du compte, de la campagne, du groupe publicitaire ou du groupe de produits, vous pouvez ajouter l’URL de suivi aux données de produit dans le compte [!DNL Microsoft Merchant Center]. Pour ce faire, incluez l’URL de suivi, ainsi que la valeur dans le champ &quot;`link`&quot; ou &quot;`mobile_link`&quot;, le cas échéant, dans une colonne personnalisée &quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot; dans le flux de produit. La valeur du champ &quot;`bingads_redirect`&quot; remplace les valeurs des champs &quot;`link`&quot; et &quot;`mobile_link`&quot;. Les URL générées à l’aide de cette méthode n’incluent aucun paramètre de suivi spécifié dans les paramètres de compte ou de campagne Search, Social et Commerce.

## Formats des suffixes de landing page (suffixe URL final)

>[!NOTE]
>
>Les suffixes de page d’entrée aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur du réseau publicitaire.

### Réseaux de recherche et d’audience

Les comptes qui utilisent le suivi de conversion d’Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`msclkid` pour [!DNL Microsoft Advertising]) dans le suffixe :

* Lorsque l’annonceur dispose d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Lorsque l’annonceur ne dispose pas d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `&ev_efid={msclkid}:G:s`

### Réseau commercial

Les comptes qui utilisent le suivi de conversion d’Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`msclkid` pour [!DNL Microsoft Advertising]) dans le suffixe :

* Lorsque l’annonceur dispose d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Lorsque l’annonceur ne dispose pas d’une intégration Adobe Analytics, le suffixe doit inclure les éléments suivants :

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion d’Adobe Advertising](formats-click-tracking-about.md)
>* [Formats AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
