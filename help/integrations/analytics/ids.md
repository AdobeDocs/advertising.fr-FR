---
title: ID d’Adobe Advertising utilisés par [!DNL Analytics]
description: ID d’Adobe Advertising utilisés par [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# ID d’Adobe Advertising utilisés par [!DNL Analytics]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable au DSP de publicité et[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising utilise deux identifiants pour le suivi des performances sur site : *EF ID* et la variable *AMO ID*.

Lorsqu’une impression de publicité se produit, Adobe Advertising crée les valeurs AMO ID et EF ID et les stocke. Lorsqu’un visiteur qui a vu une publicité arrive sur le site sans cliquer sur une publicité, [!DNL Analytics] appelle ces valeurs de l’Adobe Advertising à la variable [!DNL Analytics for Advertising] Code JavaScript. Pour le trafic d’affichage publicitaire, [!DNL Analytics] génère un ID supplémentaire (`SDID`), utilisé pour associer l’EF ID et l’AMO ID à [!DNL Analytics]. Pour le trafic de clics publicitaires, ces identifiants sont inclus dans l’URL de la page d’entrée à l’aide de la variable `s_kwcid` et `ef_id` paramètres de chaîne de requête.

L’Adobe Advertising fait la distinction entre une entrée de clic publicitaire ou d’affichage publicitaire sur le site web selon les critères suivants :

* Une entrée d’affichage publicitaire est capturée lorsqu’un utilisateur se rend sur le site après avoir affiché une publicité, mais sans cliquer dessus. [!DNL Analytics] enregistre un affichage publicitaire si deux conditions sont remplies :
   * Le visiteur ne dispose d’aucun clic publicitaire pour une [!DNL DSP] ou [!DNL Search, Social, & Commerce] pendant la [intervalle de recherche en amont des clics](#lookback-a4adc).
   * Le visiteur en a vu au moins une [!DNL DSP] pendant la [intervalle de recherche en amont des impressions](#lookback-a4adc). La dernière impression est transmise comme affichage publicitaire.
* Une entrée de clic publicitaire est capturée lorsqu’un visiteur du site clique sur une publicité avant d’accéder au site. [!DNL Analytics] capture un clic publicitaire lorsque l’une des conditions suivantes se produit :
   * L’URL comprend un EF ID et un AMO ID, ajoutés par Adobe Advertising à l’URL de la page d’entrée.
   * L’URL ne contient aucun code de suivi, mais le code JavaScript de l’Adobe Advertising détecte un clic au cours des deux dernières minutes.

![Basé sur les vues des Adobes Advertising [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1 : Basé sur la vue des Adobes Advertising [!DNL Analytics] integration*

![Clic Adobe Advertising sur URL [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2 : Adobe Advertising du clic sur une URL [!DNL Analytics] integration*

## Adobe Advertising des ID EF

L’identifiant EF est un jeton unique utilisé par Adobe Advertising pour associer une activité à une exposition aux clics ou publicités en ligne. L’identifiant EF est stocké dans [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] (réservé) [!DNL eVar]) (Adobe Advertising de l’identifiant EF) et effectue le suivi de chaque clic publicitaire ou exposition au niveau du navigateur ou de l’appareil. Les EF ID agissent principalement comme clés d’envoi [!DNL Analytics] données à Adobe Advertising pour la création de rapports et l’optimisation de l’offre dans Adobe Advertising.

### Format d’identifiant EF

>[!NOTE]
>
>Les identifiants EF sont sensibles à la casse. Si [!DNL Analytics] l’implémentation force le suivi des URL en minuscules, puis l’Adobe Advertising ne reconnaît pas l’identifiant EF. Cela aura un impact sur les offres et les rapports d’Adobe Advertising, mais n’aura aucune incidence sur les rapports d’Adobe Advertising dans les [!DNL Analytics].

#### [!DNL Google Ads] annonces de recherche

```
{gclid}:G:s
```

où :

* `gclid` est la valeur [!DNL Google Click ID] (GCLID).
* `s` est le type de réseau (&quot;s&quot; pour la recherche).

#### Publicités de recherche Microsoft Advertising

```
{msclkid}:G:s
```

où :

* `msclkid` est la valeur [!DNL Microsoft Click ID] (MSCLKID).
* `s` est le type de réseau (&quot;s&quot; pour la recherche).

#### Afficher des publicités et des annonces de recherche sur d’autres moteurs de recherche

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

où :

* &lt;*Identifiant visiteur Adobe Advertising*> est un identifiant unique par visiteur (tel que UmKVaABCkJ0mDt). Également appelé *surfer ID*.

* &lt;*timestamp*> correspond à l’heure au format YYYYMMDHHMMSS (par exemple, 20190821192533 pour l’année 2019, le mois 08, le jour 21, l’heure 19):25:3).

* &lt;*type de canal*> est le type de canal responsable du clic ou de l’exposition :

   * `d` pour un clic sur une publicité DSP (clic publicitaire)
   * `i` pour une impression d’une publicité DSP (affichage publicitaire)
   * `s` pour un clic sur une publicité de recherche (clic publicitaire).

Exemple `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### La Dimension d’identifiant EF dans [!DNL Analytics]

Dans [!DNL Analytics] rapports, vous pouvez trouver les données d’identifiant EF en recherchant [!UICONTROL EF ID] et en utilisant la dimension [!UICONTROL EF ID Instance] mesure.

Les identifiants EF sont soumis à la limite d’identifiant unique de 500 000 dans Analysis Workspace. Une fois la valeur de 500 000 atteinte, tous les nouveaux codes de suivi sont signalés sous le titre d’un élément de ligne &quot;[!UICONTROL Low Traffic].&quot; En raison de la possibilité d’une fidélité de création de rapports manquante, les identifiants EF ne sont pas classés et vous ne devez pas les utiliser pour les segments ou la création de rapports dans [!DNL Analytics].

## Adobe Advertising des AMO ID

L’AMO ID effectue le suivi de chaque combinaison d’annonces unique à un niveau moins granulaire et est utilisé pour [!DNL Analytics] classification des données et ingestion de mesures publicitaires (telles que les impressions, les clics et les coûts) à partir d’Adobe Advertising. L’AMO ID est stocké dans une [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou la dimension rVar (AMO ID) et est utilisée exclusivement pour la création de rapports dans [!DNL Analytics].

L’AMO ID est également appelé `s_kwcid`, qui est parfois prononcé en tant que &quot;[!DNL the squid].&quot;

### Format AMO ID pour [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

où :

* &lt;*Identifiant de canal*> peut être :

   * `AC` = DSP de publicité
   * `AL` pour [!DNL Advertising Search, Social, & Commerce]

* &lt;*Identifiant de publicité*> est utilisé comme identifiant unique généré par un Adobe Advertising pour une publicité. Il sert de clé pour traduire les métadonnées des entités d’Adobe Advertising en métadonnées lisibles. [!DNL Analytics] dimensions.

* &lt;*Identifiant de référencement*> est un identifiant unique généré par un Adobe Advertising pour un emplacement. Il sert de clé pour traduire les métadonnées des entités d’Adobe Advertising en métadonnées lisibles. [!DNL Analytics] dimensions.

Exemple d’AMO ID : AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Format AMO ID pour [!DNL Search, Social, & Commerce]

AMO ID pour [!DNL Search, Social, & Commerce] suivent un format distinct pour chaque moteur de recherche. Le format de tous les moteurs de recherche commence par ce qui suit :

```
AL!{userid}!{sid}
```

où :

* `AL` est l’identifiant de canal du réseau publicitaire.
* `{userid}` est l’identifiant utilisateur numérique unique attribué par Adobe Advertising à l’annonceur.
* `{sid}` est l’identifiant numérique utilisé par Adobe Advertising pour le réseau publicitaire spécifié, tel que `3` pour [!DNL Google Ads] ou `10` pour [!DNL Microsoft Advertising].

Vous trouverez ci-dessous les formats AMO ID complets pour quelques réseaux publicitaires. Pour les formats AMO ID pour d’autres réseaux publicitaires, contactez votre équipe de compte Adobe.

Format AMO ID pour [!DNL Google Ads]:

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

où :

* `{creative}` est la valeur [!DNL Google Ads] identifiant numérique unique du créatif.
* `{matchtype}` est le type de correspondance du mot-clé qui a déclenché la publicité : `e` pour exact, `p` pour l’expression, ou `b` pour large.
* `{placement}` est le nom de domaine du site web sur lequel l’utilisateur a cliqué sur la publicité. Une valeur est disponible pour les publicités des campagnes ciblées par emplacement et pour les publicités des campagnes ciblées par mot-clé qui s’affichent sur les sites de contenu.
* `{network}` indique le réseau à partir duquel le clic s’est produit :  `g` pour [!DNL Google] recherche (pour les annonces ciblées par mot-clé uniquement), `s` pour un partenaire de recherche (pour les annonces ciblées par mot-clé uniquement) ou `d` pour le réseau d’affichage (pour les annonces ciblées par mot-clé ou les annonces ciblées par emplacement).
* `{keyword}` est le mot-clé spécifique qui a déclenché votre publicité (sur les sites de recherche) ou le mot-clé correspondant le mieux (sur les sites de contenu).

Format AMO ID pour [!DNL Microsoft Advertising]:

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

où :

* `{AdId}` est la valeur [!DNL Microsoft Advertising] identifiant numérique unique du créatif.
* `{OrderItemId}` est la valeur [!DNL Microsoft Advertising] ID numérique du mot-clé.

### DIMENSION AMO ID dans [!DNL Analytics]

Dans les rapports Analytics, vous pouvez rechercher des données AMO ID en recherchant la variable [!UICONTROL AMO ID] et en utilisant la dimension [!UICONTROL AMO ID Instance] mesure. La variable [!UICONTROL AMO ID] La dimension contient toutes les valeurs AMO ID capturées, tandis que la variable [!UICONTROL AMO ID Instance] mesure indique la fréquence de capture d’une valeur AMO ID par le site. Par exemple, si la même publicité de recherche a fait l’objet de quatre clics mais qu’Analytics a suivi sept entrées de site, [!UICONTROL AMO ID Instance] serait de sept (7) et [!UICONTROL Clicks] serait quatre (4).

Pour tout rapport ou audit dans [!DNL Analytics], la bonne pratique consiste à utiliser l’AMO ID avec son instance correspondante. Pour plus d’informations, voir &quot;[Validation des données pour [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; dans &quot;Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising.&quot;

## À propos des classifications Analytics

Dans [!DNL Analytics], un [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) est un élément de métadonnées d’un code de suivi donné, tel qu’un compte, une campagne ou une publicité. Adobe Advertising classe les données d’Adobe Advertising brutes à l’aide de classifications afin que vous puissiez afficher les données de différentes manières (par type d’annonce ou campagne, par exemple) lors de la génération des rapports. Les classifications constituent la base des rapports d’Adobe Advertising dans [!DNL Analytics] et peut être utilisé avec les mesures AMO, telles que [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], et [!UICONTROL AMO Clicks], ainsi qu’avec les événements personnalisés et standard sur site tels que [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], et [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](data-variances.md)
