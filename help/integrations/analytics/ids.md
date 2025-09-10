---
title: ID Adobe Advertising utilisés par  [!DNL Analytics]
description: ID Adobe Advertising utilisés par  [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: dede10acca1540a10699be3c14564a6f9360edd2
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 0%

---

# Adobe Advertising IDs Used by [!DNL Analytics]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable à Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising utilise deux identifiants pour le suivi des performances sur site : l’*ID EF* et l’*ID AMO*.

Lorsqu’une impression publicitaire se produit, Adobe Advertising crée les valeurs d’ID AMO et d’ID EF et les stocke. Lorsqu’un visiteur qui a vu une annonce publicitaire accède au site sans cliquer sur une annonce, [!DNL Analytics] appelle ces valeurs depuis Adobe Advertising via le code JavaScript [!DNL Analytics for Advertising]. Pour le trafic d’affichage publicitaire, [!DNL Analytics] génère un ID supplémentaire (`SDID`), qui est utilisé pour regrouper les ID EF et AMO en [!DNL Analytics]. Pour le trafic de clics publicitaires, ces identifiants sont inclus dans l’URL de la page de destination à l’aide des paramètres de chaîne de requête `ef_id` et `s_kwcid` (pour l’AMO ID) .

Adobe Advertising fait la distinction entre une entrée de clic publicitaire ou d’affichage publicitaire sur le site web à l’aide des critères suivants :

* Une entrée d’affichage publicitaire est capturée lorsqu’un utilisateur ou une utilisatrice visite le site après avoir consulté une annonce publicitaire mais sans avoir cliqué dessus. [!DNL Analytics] enregistre une vue d’ensemble si deux conditions sont remplies :

   * Le visiteur ne dispose d’aucune publicité [!DNL DSP] ou [!DNL Search, Social, & Commerce] pendant l’intervalle de recherche en amont [clics publicitaires](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * Le visiteur a vu au moins une publicité [!DNL DSP] pendant l’intervalle de recherche en amont [impression](/help/integrations/analytics/prerequisites.md#lookback-a4adc). La dernière impression est transmise comme affichage.

* Une entrée de clic publicitaire est capturée lorsqu’un visiteur du site clique sur une annonce avant d’accéder au site. [!DNL Analytics] capture un clic publicitaire lorsque l’une des conditions suivantes se produit :

   * L’URL comprend un EF ID et un AMO ID, tels qu’ajoutés par Adobe Advertising à l’URL de la page de destination.

   * L’URL ne contient aucun code de suivi, mais le code Adobe Advertising JavaScript détecte un clic au cours des deux dernières minutes.

![Intégration de [!DNL Analytics] basé sur la vue Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1 : Intégration de [!DNL Analytics] basé sur les vues Adobe Advertising*

![Intégration de [!DNL Analytics] basée sur les URL de clics Adobe Advertising](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2 : intégration de [!DNL Analytics] basées sur les clics Adobe Advertising*

## Identifiants d’éléments d’expérience Adobe Advertising

L’ID d’EF est un jeton unique utilisé par Adobe Advertising pour associer l’activité à une exposition de publicité ou de clic en ligne au niveau du navigateur ou de l’appareil concerné. Les identifiants EF servent principalement de clés pour envoyer des données [!DNL Analytics] et des données Customer Journey Analytics à Adobe Advertising à des fins de création de rapports et d’optimisation des enchères dans Adobe Advertising.

Par [!DNL Analytics], l’identifiant de l’EF est stocké dans [une dimension  [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] ([!DNL eVar] réservé) (identifiant de l’EF Adobe Advertising).

Pour Customer Journey Analytics, l’ID d’élément d’enregistrement est stocké dans la propriété `trackingIdentities` de l’objet `conversionDetails`, qui fait partie du [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] .

### Formats d’ID EF {#ef-id-formats}

>[!NOTE]
>
>Les identifiants d’éléments d’expérience sont sensibles à la casse. Si une implémentation d’[!DNL Analytics] ou de Customer Journey Analytics force le suivi des URL à être écrit en minuscules, alors Adobe Advertising ne reconnaît pas l’ID d’EF. Cela a un impact sur les enchères et les rapports Adobe Advertising, mais n’a aucun impact sur les rapports Adobe Advertising dans [!DNL Analytics] ou Customer Journey Analytics.

#### [!DNL Google Ads] des annonces de recherche

```
{gclid}:G:s
```

où :

* `gclid` est le [!DNL Google Click ID] (GCLID).
* `s` est le type de réseau (« s » pour la recherche).

#### [!DNL Microsoft Advertising] des annonces de recherche

```
{msclkid}:G:s
```

où :

* `msclkid` est le [!DNL Microsoft Click ID] (MSCLKID).
* `s` est le type de réseau (« s » pour la recherche).

#### Affichage des annonces et des annonces de recherche sur d’autres moteurs de recherche

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

où :

* &lt;*Identifiant visiteur Adobe Advertising*> est un identifiant unique par visiteur (par exemple, UhKVaAAABCkJ0mDt). Également appelé *surfer ID*.

* &lt;*timestamp*> correspond à l’heure au format AAAAMMJJHHMMSS (par exemple 20190821192533 pour l’année 2019, le mois 08, le jour 21, l’heure 19:25:33).

* &lt;*channel type*> est le type de canal responsable du clic ou de l’exposition :

   * `d` d’un clic sur une publicité display DSP (affichage clic publicitaire)
   * `i` d’impression d’une publicité display DSP (affichage publicitaire)
   * `s` un clic sur une publicité de recherche (clic publicitaire de recherche).

Exemple de `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### Dimension de l’ID de l’EF dans [!DNL Analytics]

Dans les rapports [!DNL Analytics], vous pouvez trouver des données d’identifiant d’événement en recherchant la dimension [!UICONTROL EF ID] et en utilisant la mesure [!UICONTROL EF ID Instance] .

Les identifiants EF sont soumis à la limite de 500 000 identifiants uniques dans Analysis Workspace. Une fois la valeur de 500 000, tous les nouveaux codes de suivi sont signalés sous le titre « [!UICONTROL Low Traffic] ». En raison de la possibilité de rapport de fidélité manquant, les identifiants EF ne sont pas classés et vous ne devez pas les utiliser pour les segments ou les rapports dans [!DNL Analytics].

<!-- ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

### Méthodes de mise en œuvre de l’AMO ID {#amo-id-implement}

Le paramètre est ajouté à vos URL de tracking de l’une des manières suivantes :

* (Recommandé) Lorsque la fonction d’insertion côté serveur est implémentée.

   * Clients DSP : le serveur de pixels ajoute automatiquement le paramètre s_kwcid aux suffixes de votre page de destination lorsqu’un utilisateur final consulte une publicité display avec le pixel Adobe Advertising.

   * Clients Search, Social et Commerce :

      * Pour les comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] dont le paramètre [!UICONTROL Auto Upload] est activé pour le compte ou la campagne, le serveur de pixels ajoute automatiquement le paramètre s_kwcid aux suffixes de votre page de destination lorsqu’un utilisateur final clique sur une annonce publicitaire contenant le pixel Adobe Advertising.

      * Pour d’autres réseaux publicitaires, ou pour les comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] dont le paramètre [!UICONTROL Auto Upload] est désactivé, ajoutez manuellement le paramètre à vos [paramètres d’ajout au niveau du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, qui l’ajoutent à vos URL de base.

* Lorsque la fonction d&#39;insertion côté serveur n&#39;est pas implémentée :

   * Clients DSP : le code [JavaScript](javascript.md) enregistre automatiquement les clics publicitaires et les affichages publicitaires. Lorsqu’un navigateur ne prend pas en charge les cookies tiers, vous pouvez toujours effectuer le suivi des conversions basées sur les clics pour les types d’annonces suivants :

      * Pour [!DNL Flashtalking] balises d’annonce publicitaire, insérez manuellement des macros supplémentaires par « [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md) ». **Remarque :** cette procédure n’est pas nécessaire si votre entreprise entretient un partenariat direct avec [!DNL Flashtalking] et que vous utilisez des macros de transfert de données pour effectuer le suivi des paramètres de suivi `s_kwcid` et `ef_id` conformément à la documentation d’assistance [!DNL Flashtalking] à l’adresse [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

      * Pour [!DNL Google Campaign Manager 360] balises d’annonce publicitaire, insérez manuellement des macros supplémentaires par « [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md) ».

   * Clients Search, Social et Commerce :

      * Pour les publicités ([!DNL Google Ads] et [!DNL Microsoft Advertising]), ajoutez manuellement le paramètre d’ID AMO à vos suffixes de page de destination, idéalement au niveau du [compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} sauf si un suivi différent est nécessaire pour les composants de compte individuels.

      * Pour les publicités sur tous les autres réseaux publicitaires, ajoutez manuellement le paramètre ID AMO à vos [paramètres d’ajout au niveau du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, qui l’ajoutent à vos URL de base.

Pour implémenter la fonction d’insertion côté serveur ou déterminer la meilleure option pour votre entreprise, contactez l’équipe chargée de votre compte Adobe.

### AMO ID Dimension dans [!DNL Analytics]

Dans les rapports Analytics, vous pouvez trouver des données d’ID AMO en recherchant la dimension [!UICONTROL AMO ID] et en utilisant la mesure [!UICONTROL AMO ID Instances] . La dimension [!UICONTROL AMO ID] héberge toutes les valeurs d’ID AMO capturées, tandis que la mesure [!UICONTROL AMO ID Instances] indique la fréquence à laquelle une valeur d’ID AMO a été capturée par le site. Par exemple, si la même publicité de recherche a fait l’objet de quatre clics mais qu’Analytics a suivi sept entrées de site, [!UICONTROL AMO ID Instances] serait sept (7) et [!UICONTROL Clicks] serait quatre (4).

Pour les rapports ou les audits au sein de [!DNL Analytics], la bonne pratique consiste à utiliser l’AMO ID avec son instance correspondante. Pour plus d’informations, voir « [Validation des données de clic publicitaire pour  [!DNL Analytics for Advertising]](data-variances.md#data-validation) » dans « Variances de données attendues entre [!DNL Analytics] et Adobe Advertising ».

## À Propos Des Classifications Analytics

Dans [!DNL Analytics], une [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) est un élément de métadonnées pour un code de suivi donné, tel qu’un compte, une campagne ou une publicité. Adobe Advertising classe les données Adobe Advertising brutes à l’aide de classifications afin que vous puissiez afficher les données de différentes manières (par exemple par type d’annonce ou campagne) lorsque vous générez des rapports. Les classifications forment la base des rapports Adobe Advertising dans [!DNL Analytics] et peuvent être utilisées avec les mesures AMO telles que [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] et [!UICONTROL AMO Clicks], ainsi qu’avec les événements sur site personnalisés et standard tels que [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] et [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Écarts de données attendus entre  [!DNL Analytics]  et Adobe Advertising](data-variances.md)
