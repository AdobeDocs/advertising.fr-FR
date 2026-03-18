---
title: Écarts de données attendus entre  [!DNL Analytics]  et Adobe Advertising
description: Écarts de données attendus entre  [!DNL Analytics]  et Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '3359'
ht-degree: 0%

---

# Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Les annonceurs avec l’intégration [!DNL Analytics for Advertising] <!-- (A4AdC) --> effectuent le suivi de la publicité payante via Adobe Advertising et Adobe Analytics. Lorsque vous suivez des médias, des campagnes et des canaux via plusieurs systèmes, les mêmes jeux de données provenant de différents systèmes correspondent rarement complètement. Ce document explique comment vous devez vous attendre à ce que les données des médias qui font l’objet d’un trafic via Adobe Advertising soient comparées aux données des différents systèmes dans lesquels le média est suivi au sein de [!DNL Analytics].

>[!NOTE]
>
>Ce document se concentre sur Adobe Advertising et Analytics, mais de nombreux points essentiels sont également transférables à d’autres solutions de suivi.

## Différences d’attribution dans des rapports similaires

### Intervalles de recherche en amont et modèles d’attribution potentiellement différents

L’intégration [!DNL Analytics for Advertising] utilise deux variables ([!DNL eVars] ou [!DNL rVars] \[[!DNL eVars] réservé]\) pour capturer l’ID [EF et l’ID AMO](ids.md). Ces variables sont configurées avec un seul intervalle de recherche en amont (le temps pendant lequel les clics publicitaires et les consultations publicitaires sont attribués) et un modèle d’attribution. Sauf indication contraire, les variables sont configurées pour correspondre à l’intervalle de recherche en amont de clics au niveau de l’annonceur par défaut et au modèle d’attribution dans Adobe Advertising.

Toutefois, les intervalles de recherche en amont et les modèles d’attribution peuvent être configurés dans Analytics (via le [!DNL eVars]) et dans Adobe Advertising. En outre, dans Adobe Advertising, le modèle d’attribution est configurable non seulement au niveau de l’annonceur (pour l’optimisation des enchères), mais également dans les vues de données et les rapports individuels (à des fins de création de rapports uniquement). Par exemple, une organisation peut préférer utiliser le modèle d’attribution de distribution d’événements pour l’optimisation, mais utiliser l’attribution Dernière touche pour les rapports dans Advertising DSP ou [!DNL Advertising Search, Social, & Commerce]. La modification des modèles d’attribution modifie le nombre de conversions attribuées.

Si un intervalle de recherche en amont ou un modèle d’attribution de rapports est modifié dans un produit et non dans l’autre, les mêmes rapports de chaque système affichent des données distinctes :

* **Exemple d’incohérences dues à différents intervalles de recherche en amont :**

  Supposons qu’Adobe Advertising dispose d’un intervalle de recherche en amont des clics de 60 jours et que [!DNL Analytics] dispose d’un intervalle de recherche en amont de 30 jours. Supposons également qu’un utilisateur se rende sur le site par le biais d’une annonce suivie par Adobe Advertising, qu’il quitte le site, puis qu’il y revienne au jour 45 et effectue une conversion. Adobe Advertising attribue la conversion à la visite initiale, car la conversion s’est produite dans l’intervalle de recherche en amont de 60 jours. [!DNL Analytics] ne peut toutefois pas attribuer la conversion à la visite initiale, car la conversion s’est produite après l’expiration de l’intervalle de recherche en amont de 30 jours. Dans cet exemple, Adobe Advertising signale un nombre de conversions supérieur à celui de [!DNL Analytics].

  ![Exemple d’une conversion attribuée dans Adobe Advertising mais non [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Exemple d’incohérences dues à différents modèles d’attribution :**

  Supposons qu’un utilisateur interagisse avec trois annonces Adobe Advertising différentes avant la conversion, avec le chiffre d’affaires comme type de conversion. Si un rapport Adobe Advertising utilise un modèle de distribution égale pour l’attribution, il attribue le chiffre d’affaires de manière égale sur toutes les publicités. Toutefois, si [!DNL Analytics] utilise le modèle d’attribution Dernière touche , il attribue le chiffre d’affaires à la dernière publicité. Dans l’exemple suivant, Adobe Advertising attribue un montant pair de 10 USD sur les 30 USD de chiffre d’affaires capturés à chacune des trois publicités, tandis que [!DNL Analytics] attribue l’ensemble des 30 USD de chiffre d’affaires à la dernière publicité vue par l’utilisateur. Lorsque vous comparez des rapports d’Adobe Advertising et de [!DNL Analytics], vous pouvez vous attendre à voir l’impact de la différence d’attribution.

  ![Différents revenus attribués à Adobe Advertising et [!DNL Analytics] en fonction de différents modèles d’attribution](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La bonne pratique consiste à utiliser les mêmes intervalles de recherche en amont et le même modèle d’attribution dans Adobe Advertising et [!DNL Analytics]. Contactez l’équipe chargée de votre compte Adobe si nécessaire pour identifier les paramètres actuels et conserver la synchronisation des configurations.

Ces mêmes concepts s’appliquent à tous les autres canaux similaires qui utilisent différents intervalles de recherche en amont ou modèles d’attribution.

#### Différents intervalles de recherche en amont pour le suivi des affichages publicitaires {#impression-lookback}

Dans Adobe Advertising, l’attribution repose sur les clics et les impressions. Vous pouvez configurer différents intervalles de recherche en amont pour les clics et les impressions. Toutefois, dans [!DNL Analytics], l’attribution est basée sur les clics publicitaires et les affichages publicitaires, et vous n’avez pas la possibilité de définir des fenêtres d’attribution différentes pour les clics publicitaires et les affichages publicitaires ; le suivi de chaque élément commence lors de la visite initiale du site. Une impression peut se produire le même jour ou plusieurs jours avant une affichage publicitaire et le minutage peut avoir un impact sur l’endroit où la fenêtre d’attribution commence dans chaque système.

En règle générale, la majorité des conversions d’affichage publicitaire se produisent suffisamment rapidement pour que les deux systèmes attribuent du crédit. Cependant, certaines conversions peuvent se produire en dehors de l’intervalle de recherche en amont d’impression Adobe Advertising, mais dans l’intervalle de recherche en amont [!DNL Analytics] ; ces conversions sont attribuées à l’affichage publicitaire dans [!DNL Analytics], mais pas à l’impression dans Adobe Advertising.

Dans l’exemple suivant, supposons qu’un visiteur ait reçu une publicité le jour 1, qu’il ait effectué une visite d’affichage (c’est-à-dire qu’il ait visité la page de destination de la publicité sans cliquer auparavant sur la publicité) le jour 2 et qu’il ait effectué une conversion le jour 45. Dans ce cas, Adobe Advertising effectue le suivi de l’utilisateur des jours 1 à 14 (à l’aide d’une recherche arrière de 14 jours), [!DNL Analytics] effectue le suivi de l’utilisateur des jours 2 à 61 (à l’aide d’une recherche arrière de 60 jours) et la conversion du jour 45 est attribuée à l’annonce dans [!DNL Analytics], mais pas dans Adobe Advertising.

![Exemple de conversion d’affichage publicitaire attribuée dans [!DNL Analytics] mais pas dans Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

Une autre cause des incohérences est que, dans Adobe Advertising, vous pouvez attribuer aux conversions d’affichage publicitaire un *poids d’affichage publicitaire* personnalisé par rapport au poids attribué à une conversion basée sur les clics. Le poids d’affichage publicitaire par défaut est de 40 %, ce qui signifie qu’une conversion d’affichage publicitaire est comptabilisée comme 40 % de la valeur d’une conversion basée sur les clics. [!DNL Analytics] ne fournit pas une telle pondération des conversions en affichage publicitaire. Ainsi, par exemple, une commande de chiffre d’affaires de 100 USD capturée en [!DNL Analytics] est actualisée à 40 USD dans Adobe Advertising si vous utilisez le poids d’affichage publicitaire par défaut, soit une différence de 60 USD.

Tenez compte de ces différences lors de la comparaison des conversions d’affichage publicitaire entre les rapports Adobe Advertising et [!DNL Analytics].

#### Modèles d’attribution disponibles

| Attribution Adobe Advertising | Attribution [!DNL Analytics] | Allocation [!DNL eVar]/[!DNL rVar] |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | s.o. | s.o. |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Ne pas utiliser* |
| [!UICONTROL Weight Last Event More] | s.o. | s.o. |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | s.o. |
| s.o. | [!UICONTROL J-Shaped] | s.o. |
| s.o. | [!UICONTROL Inverse-J] | s.o. |
| s.o. | [!UICONTROL Custom] | s.o. |
| s.o. | [!UICONTROL Participation] | s.o. |
| s.o. | [!UICONTROL Algorithmic] | s.o. |

>[!NOTE]
>
>Pour une affectation linéaire, [!DNL Analytics] attribue les événements de succès de manière égale sur toutes les valeurs de [!DNL eVar] au cours d’une seule visite. Utilisez donc une affectation linéaire avec une expiration [!DNL eVar] de « visite ». Pour la publicité, cependant, l’utilisation de l’attribution linéaire conduit à une attribution qui n’est pas vraiment linéaire et à un compte rendu des performances loin d’être idéal. Par exemple, si un visiteur interagit avec trois annonces avant de les convertir en trois visites distinctes, seule l’annonce vue lors de la dernière visite est attribuée à la conversion, et non aux trois annonces.
>
>En outre, le fait de passer d’une affectation de conversion à ou depuis « Linéaire » empêche l’affichage des données historiques, ce qui peut entraîner des données erronées dans les rapports. Par exemple, une affectation linéaire peut diviser le chiffre d’affaires entre plusieurs valeurs de [!DNL eVar] différentes. Si vous définissez l’affectation sur « Le dernier », 100 % de ce chiffre d’affaires est alors associé à la valeur unique la plus récente. Cette association peut vous conduire à des conclusions incorrectes.
>
>Pour éviter toute confusion, [!DNL Analytics] rend les données historiques indisponibles dans l’interface de création de rapports. Vous pouvez afficher les données historiques si vous redéfinissez le [!DNL eVar] sur le paramètre d’affectation initial, mais vous ne devez pas modifier [!DNL eVar] paramètres d’affectation simplement pour accéder aux données historiques. Adobe recommande d’utiliser une nouvelle [!DNL eVar] lorsque vous souhaitez appliquer un nouveau paramètre d’affectation pour les données déjà enregistrées, plutôt que de modifier les paramètres d’affectation pour une [!DNL eVar] qui dispose déjà d’une quantité importante de données historiques.

Consultez la liste des modèles d’attribution [!DNL Analytics] et de leurs définitions à l’adresse [https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/attribution/models).

Si vous êtes connecté à [!DNL Search, Social, & Commerce], vous pouvez trouver une liste

* (Utilisateurs en Amérique du Nord) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Tous les autres utilisateurs) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Attribution de la date de l’événement dans Adobe Advertising

Dans Adobe Advertising, vous pouvez générer des rapports sur les données de conversion en fonction de la date de clic/de l’événement associé (date de l’événement de clic ou d’impression) ou de la date de transaction (date de conversion). Le concept de rapport de date de clic/événement n’existe pas dans [!DNL Analytics] ; toutes les conversions suivies dans [!DNL Analytics] sont rapportées par date de transaction. Par conséquent, la même conversion peut être signalée avec des dates différentes dans Adobe Advertising et [!DNL Analytics]. Prenons l’exemple d’un utilisateur qui clique sur une annonce le 1er janvier et effectue une conversion le 5 janvier. Si vous affichez les données de conversion par date d’événement dans Adobe Advertising, la conversion est signalée le 1er janvier, lorsque le clic s’est produit. En [!DNL Analytics], la même conversion est signalée le 5 janvier.

![Exemple de conversion attribuée à des dates différentes](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution dans [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] reporting](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) vous permet de configurer des règles pour identifier différents canaux marketing en fonction d’aspects distincts des informations d’accès. Vous pouvez effectuer le suivi des canaux suivis par Adobe Advertising ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] et [!UICONTROL Paid Search]) selon vos [!DNL Marketing Channels] à l’aide du paramètre de chaîne de requête `ef_id` pour identifier le canal. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Cependant, même si les rapports [!DNL Marketing Channels] peuvent suivre les canaux Adobe Advertising, les données peuvent ne pas correspondre aux rapports Adobe Advertising pour plusieurs raisons. Pour plus d’informations, consultez les sections suivantes.

>[!NOTE]
>
> Les concepts de base suivants s’appliquent également à tout suivi multicanal qui implique des campagnes non suivies dans Adobe Advertising, comme la variable [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (également appelée dimension « Code de suivi » ou « [!DNL eVar] 0 ») et le suivi des [!DNL eVar] personnalisées.

### Modèles d’attribution potentiellement différents dans [!DNL Marketing Channels]

La plupart des rapports [!DNL Marketing Channels] sont configurés avec une attribution [!UICONTROL Last Touch], pour laquelle le dernier canal marketing détecté se voit attribuer 100 % de la valeur de conversion. L’utilisation de différents modèles d’attribution pour les rapports [!DNL Marketing Channels] et Adobe Advertising entraîne des incohérences dans les conversions attribuées.

### Intervalle de recherche en amont potentiellement différent dans [!DNL Marketing Channels]

L’intervalle de recherche en amont pour [!DNL Marketing Channels] peut être personnalisé. Dans Adobe Advertising, l’intervalle de recherche en amont des clics est configurable, bien qu’un intervalle fixe de 60 jours soit courant. Si les deux produits utilisent des intervalles de recherche en amont différents, des incohérences de données sont à prévoir.

### Attribution de canaux différents dans [!DNL Marketing Channels]

Les rapports Adobe Advertising capturent uniquement les médias achetés qui font l’objet d’un trafic via Adobe Advertising (recherche payante d’annonces [!DNL Advertising Search, Social, & Commerce] et affichage d’annonces Advertising DSP), tandis que les rapports [!DNL Marketing Channels] peuvent suivre tous les canaux numériques. Cela peut entraîner une incohérence dans le canal pour lequel une conversion est attribuée.

Par exemple, le référencement payant et les canaux de référencement naturel ont souvent une relation symbiotique, dans laquelle chaque canal assiste l’autre. Le rapport [!DNL Marketing Channels] attribue à la recherche naturelle certaines conversions qu’Adobe Advertising ne suit pas, car il ne suit pas la recherche naturelle.

Prenons également le cas d’un client qui consulte une annonce publicitaire, clique sur une annonce de référencement payant, clique dans un e-mail, puis passe une commande de 30 USD. Même si Adobe Advertising et [!DNL Marketing Channels] utilisent tous deux le modèle d’attribution Dernière touche, la conversion serait toujours attribuée différemment à chacun. Adobe Advertising n’a pas accès au canal [!UICONTROL Email], il créditerait donc le référencement payant pour la conversion. [!DNL Marketing Channels], cependant, a accès aux trois canaux, il créditerait donc [!UICONTROL Email] pour la conversion.

![Exemple d’attribution de conversion différente dans Adobe Advertising et dans [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Pour plus d’explications sur les raisons de la variation des mesures, voir « [Pourquoi les données de canal peuvent-elles varier entre Adobe Advertising et  [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md) ? »

## Différences de données dans les [!DNL Paid Search Detection] Adobe Analytics

La fonctionnalité [héritée [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) de [!DNL Analytics] permet aux entreprises de [définir des règles pour effectuer le suivi du trafic de référencement payant et organique](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) pour des moteurs de recherche spécifiés. Les règles [!DNL Paid Search Detection] utilisent à la fois une chaîne de requête et le domaine référent pour identifier le trafic de référencement payant et naturel. Les rapports [!DNL Paid Search Detection] font partie du groupe plus vaste de rapports [Méthodes de recherche](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html), qui expirent lorsqu’un événement spécifié (tel qu’un passage en caisse) se produit ou que la visite se termine.

Voici l’interface de création d’un jeu de règles [!DNL Paid Search Detection] :

![Exemple de règle de détection de référencement payant définie dans [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Les rapports [!DNL Paid Search Detection] qui en résultent incluent les rapports [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] et [!UICONTROL Natural Search Keywords].

Notez les deux restrictions suivantes concernant les données dans les rapports [!DNL Paid Search Detection] :

* Les rapports [!UICONTROL Paid Search Keywords] et [!UICONTROL Natural Search Keywords] affichent les requêtes de recherche identifiées par les URL de référence, et non les mots-clés sur lesquels les utilisateurs ont enchéri. Les rapports Adobe Advertising et [!DNL Analytics] affichent les mots-clés réels. Ne vous attendez donc pas à ce qu’ils s’alignent sur les rapports de mots-clés [!DNL Paid Search Detection].

* Lors de la création initiale de la fonction de [!DNL Paid Search Detection], la requête d’origine (la chaîne de caractères saisie par l’utilisateur dans la barre de recherche du moteur de recherche) était plus facilement accessible aux annonceurs via l’URL de référence. Aujourd’hui, les moteurs de recherche obscurcissent largement la requête de recherche et les rapports de mots-clés [!DNL Paid Search Detection] ont une valeur limitée, car la plupart des données de requête relèvent de la catégorie « non spécifié ».

  Avec [!DNL Analytics for Advertising], les annonceurs peuvent toujours effectuer le suivi des mots-clés payants dans [!DNL Analytics]. Le domaine référent indique aux rapports du moteur quel moteur de recherche a généré le trafic. Comme les informations de compte spécifiques à l’annonceur ne sont pas liées au domaine référent, tout le trafic est répertorié sous le moteur de recherche. Les annonceurs qui disposent de plusieurs comptes dans le même moteur de recherche doivent se reporter aux rapports Adobe Advertising ou [!DNL Analytics] pour obtenir des rapports spécifiques aux comptes.

### Pourquoi configurer [!DNL Paid Search Detection] ?

Les rapports [!DNL Paid Search Detection] vous permettent d’identifier le trafic de recherche naturel dans les [[!DNL Analytics Marketing Channels] rapports](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). La distinction entre le trafic de référencement payant et le trafic de référencement naturel est un excellent moyen de comprendre la valeur que le référencement naturel apporte à l’écosystème marketing complet.

## Validation des données de clic publicitaire pour [!DNL Analytics for Advertising] {#data-validation}

Pour votre intégration, vous devez valider vos données de clics publicitaires afin de vous assurer que toutes les pages de votre site effectuent correctement le suivi des clics publicitaires.

En [!DNL Analytics], l’un des moyens les plus simples de valider [!DNL Analytics for Advertising] suivi consiste à comparer les instances aux clics à l’aide d’une mesure calculée « Instances AMO ID aux clics », qui est calculée comme suit :

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] représente le nombre de fois que les [ AMO ID](ids.md) sont suivis sur le site. Chaque fois que l’utilisateur clique sur une publicité, un paramètre d’ID AMO (`s_kwcid`) est ajouté à l’URL de la page de destination. Le nombre de [!UICONTROL AMO ID Instances] est donc analogue au nombre de clics et peut être validé par rapport aux clics publicitaires réels. Un taux de correspondance de 85 % est généralement affiché pour les [!DNL Search, Social, & Commerce] et de 30 % pour le trafic [!DNL DSP] (lorsqu’il est filtré pour inclure uniquement les [!UICONTROL AMO ID Instances] de clic publicitaire). La différence des attentes entre la recherche et l’affichage peut s’expliquer par le comportement attendu du trafic. La recherche capture l’intention, c’est pourquoi les utilisateurs cliquent généralement sur les résultats de recherche de leur requête. En revanche, les utilisateurs qui voient une publicité display ou vidéo en ligne sont plus susceptibles de cliquer involontairement sur la publicité, puis de rebondir sur le site ou d’abandonner la nouvelle fenêtre qui se charge avant le suivi de l’activité de la page.

Dans les rapports Adobe Advertising, vous pouvez également comparer des instances à des clics à l’aide de la mesure « [!UICONTROL EF ID Instances] » au lieu de [!UICONTROL AMO ID Instances] :

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

Bien que vous devriez vous attendre à un taux de correspondance élevé entre l&#39;AMO ID et l&#39;EF ID, ne vous attendez pas à une parité de 100 %, car l&#39;AMO ID et l&#39;EF ID effectuent fondamentalement le suivi de différentes données, et cette différence peut entraîner de légères différences dans le total des [!UICONTROL AMO ID Instances] et des [!UICONTROL EF ID Instances]. Cependant, si le [!UICONTROL AMO ID Instances] total dans [!DNL Analytics] diffère de [!UICONTROL EF ID Instances] dans Adobe Advertising de plus de 1 %, contactez votre équipe de compte Adobe pour obtenir de l’aide.

Pour plus d’informations sur l’AMO ID et l’EF ID, voir [Adobe Advertising ID utilisés par Analytics](ids.md).

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### Résolution des disparités entre les clics et les instances

Si le rapport [!UICONTROL EF ID Instances]/clics est inférieur à 85 %, vérifiez les points suivants :

* Le suivi des clics vous manque-t-il pour le compte ou à un sous-niveau, ou disposez-vous d’un suivi des clics en double (par exemple, aux niveaux du compte et de la campagne) ?

  Dans Search, Social et Commerce, [téléchargez une feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) pour que le compte vérifie les URL de tracking.

  En outre, dans [!DNL Analytics], vous pouvez voir si l’ID AMO et l’IF EF sont ajoutés de manière cohérente à l’aide d’une mesure calculée « [!DNL AMO ID] à [!DNL EF ID] », qui est calculée comme suit :

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  Une valeur supérieure à 100 % indique qu’il manque plus d’ID EF que d’ID AMO.

* La page de destination présente-t-elle un problème de chargement empêchant la capture des ID AMO et EF ?

* L’URL de la page de destination est-elle redirigée afin que l’AMO ID et l’EF ID soient perdus ?

* Toutes les pages de destination utilisent-elles la suite de rapports configurée ?

>[!NOTE]
>
>En théorie, il est possible qu’une instance ait plusieurs clics. Veillez à rechercher les clics sur différents appareils (tels que les ordinateurs de bureau, les appareils mobiles et les tablettes).

## Comparaison des jeux de données dans [!DNL Analytics for Advertising] et dans Adobe Advertising

Le [ID AMO](ids.md) (paramètre de chaîne de requête s_kwcid) est utilisé pour les rapports dans [!DNL Analytics], et le [ID EF](ids.md) (paramètre de chaîne de requête ef_id) est utilisé pour les rapports dans Adobe Advertising. Comme il s’agit de valeurs distinctes, il est possible qu’une valeur soit endommagée ou ne soit pas ajoutée à la page de destination.

Supposons, par exemple, que nous ayons la page de destination suivante :

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

où l’ID EF est « `test_ef_id` » et l’ID AMO est « `test_amo_id` ».

Si une redirection côté site se produit, l’URL peut se retrouver comme suit :

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

où l’ID EF est « `test_ef_id` » et l’ID AMO est « `test_amo_id#redirectAnchorTag` ».

Dans cet exemple, l’ajout de la balise d’ancrage ajoute des caractères inattendus à l’ID AMO, ce qui entraîne une valeur qu’Analytics ne reconnaît pas. Cet ID AMO n’est pas classé et les conversions qui y sont associées relèvent de la catégorie « [!UICONTROL unspecified] » ou « [!UICONTROL none] » dans les rapports [!DNL Analytics].

Heureusement, bien que les problèmes de ce genre soient courants, ils n&#39;entraînent généralement pas un pourcentage élevé d&#39;incohérence. Cependant, si vous constatez une grande incohérence entre les ID AMO dans [!DNL Analytics] et les ID EF dans Adobe Advertising, contactez l’équipe chargée de votre compte Adobe pour obtenir de l’aide.

## Autres considérations relatives aux mesures

### La différence entre les clics et les visites {#clicks-vs-visits}

Elles semblent analogues, mais les clics et les visites représentent des données différentes :

* **Clic :** le [!DNL DSP] ou le moteur de recherche enregistre un clic lorsqu’un visiteur clique sur une annonce publicitaire sur le site web d’un éditeur.

* **Visite :** [!DNL Analytics] définit une [visite](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) comme une série de pages vues par un utilisateur, se terminant selon l’un des critères, tels que 30 minutes d’inactivité.

Par définition, un clic peut entraîner plusieurs visites.

Prenons l’exemple suivant : l’utilisateur 1 et l’utilisateur 2 accèdent tous deux à un site en cliquant sur une annonce Adobe Advertising. L’utilisateur 1 affiche quatre pages, puis quitte pour la journée. Le clic initial donne donc lieu à une seule visite. L’utilisateur 2 consulte deux pages, part pour un déjeuner de 45 minutes, revient, consulte deux pages supplémentaires, puis quitte ; dans ce cas, le clic initial entraîne deux visites.

![Exemple de la différence entre les clics et les visites](/help/integrations/assets/a4adc-visits-example.png)

### La différence entre les clics et les clics publicitaires

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Les clics et les clics publicitaires sont deux mesures différentes :

* **Clic :** le [!DNL DSP] ou le moteur de recherche enregistre un clic lorsqu’un visiteur clique sur une annonce publicitaire sur le site web d’un éditeur.

* **Clics publicitaires :** [!DNL Analytics] enregistre un clic publicitaire lorsque le visiteur accède au site web de destination, la page de destination se charge et la demande de [!DNL Analytics] au bas de la page envoie les données à [!DNL Analytics].

Les clics et les clics publicitaires peuvent être très différents en raison de clics publicitaires accidentels. Nous avons constaté que la plupart des clics sur les publicités display sont des clics accidentels. Ces visiteurs accidentels appuient sur le bouton Précédent avant le chargement de la page de destination, donc [!DNL Analytics] ne pouvez pas enregistrer de clic publicitaire. C’est particulièrement vrai pour les publicités sur lesquelles un clic accidentel est plus probable, telles que les publicités mobiles, les publicités vidéo et les publicités qui remplissent l’écran et doivent être fermées avant que l’utilisateur ou l’utilisatrice puisse consulter la page.

Les sites chargés sur des appareils mobiles ont également moins de chances d’entraîner des clics publicitaires en raison de la réduction de la bande passante ou de la puissance de traitement disponible, ce qui entraîne un chargement plus long des pages de destination. Il n’est pas rare que 50 à 70 % des clics ne génèrent pas de clics publicitaires. Dans les environnements mobiles, la différence peut atteindre 90 % en raison de la combinaison d’un navigateur plus lent et de la probabilité plus élevée que l’utilisateur clique accidentellement sur la publicité en faisant défiler la page ou en essayant de fermer la publicité.

Les données relatives aux clics peuvent également être enregistrées dans des environnements qui ne peuvent pas enregistrer les clics publicitaires avec les mécanismes de suivi actuels (tels que les clics entrant dans une application mobile ou en provenant) ou pour lesquels l’annonceur n’a déployé qu’une seule approche de suivi (par exemple, avec l’approche JavaScript de visionnage publicitaire, les navigateurs qui bloquent les cookies tiers effectuent le suivi des clics publicitaires, mais pas des clics publicitaires). Adobe recommande de déployer les approches de tracking des URL de clics et de tracking des affichages publicitaires JavaScript afin d’optimiser la couverture des clics publicitaires pouvant faire l’objet d’un suivi.

### Utilisation des mesures de trafic Adobe Advertising pour les dimensions non-Adobe Advertising

Adobe Advertising fournit à Analytics des mesures de trafic [spécifiques à la publicité et les dimensions associées de [!DNL DSP] et [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Les mesures fournies par Adobe Advertising s’appliquent uniquement aux dimensions Adobe Advertising spécifiées et les données ne sont pas disponibles pour les autres dimensions dans [!DNL Analytics].

Par exemple, si vous affichez les mesures [!UICONTROL Adobe Advertising Clicks] et [!UICONTROL Adobe Advertising Cost] par compte, ce qui correspond à une dimension Adobe Advertising, le total des [!UICONTROL Adobe Advertising Clicks] et [!UICONTROL Adobe Advertising Cost] s’affiche par compte.

![Exemple de mesures Adobe Advertising dans un rapport utilisant une dimension Adobe Advertising](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Cependant, si vous affichez les mesures [!UICONTROL Adobe Advertising Clicks] et [!UICONTROL Adobe Advertising Cost] par une dimension sur la page (telle que Page), pour laquelle Adobe Advertising ne fournit pas de données, les [!UICONTROL Adobe Advertising Clicks] et [!UICONTROL Adobe Advertising Cost] de chaque page sont nuls (0).

![Exemple de mesures Adobe Advertising dans un rapport utilisant une dimension non prise en charge](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Utilisation de [!UICONTROL AMO ID Instances] comme substitut des clics avec des dimensions non-Adobe Advertising

Étant donné que vous ne pouvez pas utiliser [!UICONTROL AMO Clicks] avec les dimensions sur site, vous souhaiterez peut-être trouver un équivalent aux clics. Vous pouvez être tenté d’utiliser Visites comme remplacement, mais elles ne sont pas la meilleure option, car chaque visiteur peut avoir plusieurs visites. (Voir « [ La différence entre les clics et les visites ](#clicks-vs-visits). » Nous vous recommandons plutôt d’utiliser [!UICONTROL AMO ID Instances], qui correspond au nombre de fois où l’AMO ID est capturé. Bien que les [!UICONTROL AMO ID Instances] ne correspondent pas exactement aux [!UICONTROL AMO Clicks], ils constituent la meilleure option pour mesurer le trafic des clics sur le site. Pour plus d’informations, voir « [Validation des données de clic publicitaire pour [!DNL Analytics for Advertising]](#data-validation) ».

![Exemple de [!UICONTROL AMO ID Instances] au lieu de [!UICONTROL Adobe Advertising Clicks] pour une dimension non prise en charge](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising ID utilisés par  [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Mesures Adobe Advertising dans Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] données dans Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Pourquoi les données de canal peuvent varier entre Adobe Advertising et  [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
