---
title: Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising
description: Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 6470ed471c60477bf19cf9b125f0250136f31511
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# Écarts de données attendus entre [!DNL Analytics] et l’Adobe Advertising

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Les annonceurs disposant de l’intégration [!DNL Analytics for Advertising] <!-- (A4AdC) --> effectuent le suivi de la publicité payante par le biais d’Adobe Advertising et d’Adobe Analytics. Lorsque vous effectuez le suivi de médias, de campagnes et de canaux via plusieurs systèmes, les mêmes jeux de données de différents systèmes correspondent rarement entièrement. Ce document explique comment vous devriez vous attendre à ce que les données du trafic sur les médias passant par l’Adobe Advertising soient comparées aux données des différents systèmes dans lesquels le suivi des médias se fait dans [!DNL Analytics].

>[!NOTE]
>
>Ce document est axé sur Adobe Advertising et Analytics, mais de nombreux points clés peuvent également être transférés à d’autres solutions de suivi.

## Différences d’attribution dans des rapports similaires

### Fenêtres de recherche en amont et modèles d’attribution potentiellement différents

L’intégration [!DNL Analytics for Advertising] utilise deux variables ([!DNL eVars] ou [!DNL rVars] \[réservé [!DNL eVars]]\) pour capturer l’ [identifiant EF et l’&#39;AMO ID](ids.md). Ces variables sont configurées avec un seul intervalle de recherche en amont (l’heure à laquelle les clics publicitaires et les affichages publicitaires sont attribués) et un modèle d’attribution. Sauf indication contraire, les variables sont configurées pour correspondre à l’intervalle de recherche en amont des clics par défaut au niveau de l’annonceur et au modèle d’attribution dans Adobe Advertising.

Cependant, les intervalles de recherche en amont et les modèles d’attribution peuvent être configurés dans Analytics (via l’ [!DNL eVars]) et dans Adobe Advertising. En outre, dans l’Adobe Advertising, le modèle d’attribution est configurable non seulement au niveau de l’annonceur (pour l’optimisation des offres), mais également dans les vues de données et les rapports individuels (à des fins de création de rapports uniquement). Par exemple, une organisation peut préférer utiliser le modèle d’attribution distribution paire pour l’optimisation, mais utiliser l’attribution Dernière touche pour les rapports dans Advertising DSP ou [!DNL Advertising Search, Social, & Commerce]. La modification des modèles d’attribution modifie le nombre de conversions attribuées.

Si un intervalle de recherche en amont des rapports ou un modèle d’attribution est modifié dans un produit et non dans l’autre, les mêmes rapports de chaque système affichent des données distinctes :

* **Exemple d&#39;incohérences dues à différents intervalles de recherche en amont :**

  Supposons que l’Adobe Advertising ait une période de recherche en amont des clics de 60 jours et que [!DNL Analytics] ait une période de recherche en amont de 30 jours. Supposons également qu’un utilisateur se rende sur le site par le biais d’une publicité qui fait l’objet d’un suivi par Adobe Advertising, quitte le site, puis revient le 45e jour et effectue une conversion. Adobe Advertising attribue la conversion à la visite initiale, car la conversion s’est produite dans l’intervalle de recherche en amont de 60 jours. [!DNL Analytics], cependant, ne peut pas attribuer la conversion à la visite initiale, car la conversion s’est produite après l’expiration de l’intervalle de recherche en amont de 30 jours. Dans cet exemple, Adobe Advertising signale un nombre de conversions plus élevé que [!DNL Analytics].

  ![Exemple de conversion attribuée en Adobe Advertising mais pas [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Exemple d’incohérences causées par différents modèles d’attribution :**

  Supposons qu’un utilisateur interagisse avec trois publicités Adobe Advertising différentes avant la conversion, avec les recettes comme type de conversion. Si un rapport d’Adobe Advertising utilise un modèle de distribution uniforme pour l’attribution, il attribue les recettes de manière uniforme sur toutes les publicités. Cependant, si [!DNL Analytics] utilise le modèle d’attribution Dernière touche, il attribue les recettes à la dernière publicité. Dans l’exemple suivant, Adobe Advertising attribue 10 USD sur les 30 USD des recettes capturées à chacune des trois publicités, tandis que [!DNL Analytics] attribue les 30 USD des recettes à la dernière publicité vue par l’utilisateur. Lorsque vous comparez des rapports d’Adobe Advertising et de [!DNL Analytics], vous pouvez vous attendre à voir l’impact de la différence d’attribution.

  ![Recettes différentes attribuées à l’Adobe Advertising et [!DNL Analytics] en fonction de différents modèles d’attribution](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La bonne pratique consiste à utiliser les mêmes intervalles de recherche en amont et modèle d’attribution dans Adobe Advertising et [!DNL Analytics]. Contactez votre équipe de compte d’Adobe si nécessaire pour identifier les paramètres actuels et conserver la synchronisation des configurations.

Ces mêmes concepts s’appliquent à tout autre canal, tel que les canaux qui utilisent des intervalles de recherche en amont différents ou des modèles d’attribution.

#### Différentes fenêtres de recherche en amont pour le suivi des affichages publicitaires {#impression-lookback}

Dans Adobe Advertising, l’attribution est basée sur les clics et les impressions, et vous pouvez configurer différents intervalles de recherche en amont pour les clics et les impressions. Cependant, dans [!DNL Analytics], l’attribution est basée sur les clics publicitaires et les affichages publicitaires et vous n’avez pas la possibilité de définir différentes fenêtres d’attribution pour les clics publicitaires et les affichages publicitaires ; le suivi pour chaque début de visite initiale du site. Une impression peut se produire le même jour ou plusieurs jours avant qu’un affichage publicitaire ne se produise, et le timing peut avoir une incidence sur le début de la fenêtre d’attribution dans chaque système.

En règle générale, la majorité des conversions d’affichages publicitaires se produisent assez rapidement pour que les deux systèmes attribuent du crédit. Cependant, certaines conversions peuvent se produire en dehors de l’intervalle de recherche en amont des impressions de l’Adobe Advertising, mais dans l’intervalle de recherche en amont [!DNL Analytics] ; de telles conversions sont attribuées à l’affichage publicitaire dans [!DNL Analytics] mais pas à l’impression dans l’Adobe Advertising.

Dans l’exemple suivant, supposons qu’un visiteur ait reçu une publicité le jour 1, qu’il ait effectué une visite d’affichage publicitaire (c’est-à-dire qu’il a visité la page d’entrée de la publicité sans avoir cliqué auparavant sur la publicité) le jour 2 et qu’il ait été converti le jour 45. Dans ce cas, Adobe Advertising suivrait l’utilisateur des jours 1 à 14 (à l’aide d’une recherche en amont de 14 jours), [!DNL Analytics] suivrait l’utilisateur des jours 2 à 61 (à l’aide d’une recherche en amont de 60 jours), et la conversion du jour 45 serait attribuée à la publicité dans les [!DNL Analytics] mais pas dans l’Adobe Advertising.

![Exemple de conversion d&#39;affichage publicitaire attribuée dans [!DNL Analytics] mais pas d&#39;Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

Une autre cause d’incohérences est que, dans l’Adobe Advertising, vous pouvez attribuer aux conversions d’affichage publicitaire un *poids d’affichage publicitaire* personnalisé relatif au poids attribué à une conversion basée sur les clics. La pondération d’affichage publicitaire par défaut est de 40 %, ce qui signifie qu’une conversion d’affichage publicitaire est comptabilisée comme 40 % de la valeur d’une conversion basée sur les clics. [!DNL Analytics] ne fournit aucune pondération des conversions d’affichage publicitaire de ce type. Par exemple, une commande de recettes de 100 USD capturée dans [!DNL Analytics] est réduite à 40 USD en Adobe Advertising si vous utilisez le poids d’affichage publicitaire par défaut — une différence de 60 USD.

Tenez compte de ces différences lors de la comparaison des conversions d’affichage publicitaire entre les rapports d’Adobe Advertising et [!DNL Analytics].

#### Modèles d’attribution disponibles

| Attribution des Adobes Advertising | [!DNL Analytics] Attribution | [!DNL eVar]/[!DNL rVar] Affectation |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Ne pas utiliser* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>Pour l’affectation linéaire, [!DNL Analytics] attribue uniformément les événements de succès sur toutes les valeurs [!DNL eVar] au cours d’une seule visite. Par conséquent, utilisez l’affectation linéaire avec une expiration [!DNL eVar] de &quot;Visite&quot;. Toutefois, pour la publicité, l’utilisation de l’attribution linéaire conduit à une attribution qui n’est pas vraiment linéaire et à des rapports moins que idéaux. Par exemple, si un visiteur interagit avec trois publicités avant de procéder à la conversion au cours de trois visites distinctes, seule la publicité vue lors de la dernière visite est attribuée à la conversion, et non aux trois publicités.
>
>En outre, le fait de basculer l’attribution de conversion vers ou depuis &quot;Linéaire&quot; empêche l’affichage des données historiques, ce qui peut entraîner des données erronées dans les rapports. Par exemple, l’affectation linéaire peut diviser les recettes entre plusieurs valeurs [!DNL eVar] différentes. Si vous définissez l’attribution sur &quot;Le plus récent&quot;, 100 % de ces recettes sont associées à la valeur unique la plus récente. Cette association peut vous mener à des conclusions incorrectes.
>
>Pour éviter toute confusion, [!DNL Analytics] rend les données historiques indisponibles dans l’interface de création de rapports. Vous pouvez afficher les données historiques si vous redéfinissez le paramètre d’attribution initial [!DNL eVar], même si vous ne devez pas modifier les paramètres d’attribution [!DNL eVar] simplement pour accéder aux données historiques. Adobe recommande d’utiliser un nouveau [!DNL eVar] lorsque vous souhaitez appliquer un nouveau paramètre d’attribution pour les données déjà en cours d’enregistrement, plutôt que de modifier les paramètres d’attribution pour un [!DNL eVar] qui possède déjà une quantité significative de données historiques.

Consultez la liste des modèles d’attribution [!DNL Analytics] et leurs définitions sur [https://experienceleague.adobe.com/fr/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/fr/docs/analytics/analyze/analysis-workspace/attribution/models).

Si vous êtes connecté à [!DNL Search, Social, & Commerce], vous trouverez une liste

* (Utilisateurs en Amérique du Nord) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Tous les autres utilisateurs) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Attribution de date d’événement dans l’Adobe Advertising

Dans l’Adobe Advertising, vous pouvez signaler les données de conversion soit par date de clic/événement associé (date de l’événement de clic ou d’impression), soit par date de transaction (date de conversion). Le concept de rapport de date de clic/événement n’existe pas dans [!DNL Analytics] ; toutes les conversions suivies dans [!DNL Analytics] sont signalées par date de transaction. Par conséquent, une même conversion peut être signalée avec des dates différentes dans l’Adobe Advertising et [!DNL Analytics]. Prenons l’exemple d’un utilisateur qui clique sur une publicité le 1er janvier et effectue une conversion le 5 janvier. Si vous affichez les données de conversion par date d’événement dans l’Adobe Advertising, la conversion est signalée le 1er janvier, lorsque le clic a eu lieu. Dans [!DNL Analytics], la même conversion est signalée le 5 janvier.

![Exemple de conversion attribuée à des dates différentes](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution dans [!DNL Analytics Marketing Channels]

La [[!DNL Analytics Marketing Channels] création de rapports](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=fr) vous permet de configurer des règles pour identifier différents canaux marketing en fonction de différents aspects des informations sur les accès. Vous pouvez effectuer le suivi des canaux suivis par l’Adobe Advertising ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] et [!UICONTROL Paid Search]) sous la forme [!DNL Marketing Channels] en utilisant le paramètre de chaîne de requête `ef_id` pour identifier le canal. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Cependant, même si les rapports [!DNL Marketing Channels] peuvent effectuer le suivi des canaux d’Adobe Advertising, les données peuvent ne pas correspondre aux rapports d’Adobe Advertising pour plusieurs raisons. Pour plus d’informations, reportez-vous aux sections suivantes.

>[!NOTE]
>
> Les concepts de base suivants s’appliquent également à tout suivi multicanal qui implique des campagnes non suivies dans Adobe Advertising, comme la variable [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html?lang=fr) (également appelée dimension &quot;Code de suivi&quot; ou &quot;[!DNL eVar] 0&quot;) et le suivi personnalisé [!DNL eVar].

### Modèles d’attribution potentiellement différents dans [!DNL Marketing Channels]

La plupart des rapports [!DNL Marketing Channels] sont configurés avec l’attribution [!UICONTROL Last Touch], pour laquelle le dernier canal marketing détecté se voit attribuer 100 % de la valeur de conversion. L’utilisation de différents modèles d’attribution pour les rapports [!DNL Marketing Channels] et les rapports d’Adobe Advertising entraîne des incohérences dans les conversions attribuées.

### Une fenêtre de recherche en amont potentiellement différente dans [!DNL Marketing Channels]

L’intervalle de recherche en amont de [!DNL Marketing Channels] peut être personnalisé. En Adobe Advertising, l’intervalle de recherche en amont des clics est configurable, bien qu’une période de 60 jours fixe soit courante. Si les deux produits utilisent des intervalles de recherche en amont différents, vous pouvez vous attendre à des incohérences de données.

### Attribution de canal différente dans [!DNL Marketing Channels]

Les rapports d’Adobe Advertising capturent uniquement les médias payants qui transitent par l’Adobe Advertising (recherche payante de [!DNL Advertising Search, Social, & Commerce] publicités et affichage pour les publicités Advertising DSP), tandis que les rapports [!DNL Marketing Channels] peuvent effectuer le suivi de tous les canaux numériques. Cela peut entraîner une incohérence dans le canal pour lequel une conversion est attribuée.

Par exemple, les canaux de recherche payante et de recherche naturelle ont souvent une relation symbiotique, dans laquelle chaque canal s’aide l’autre. Le rapport [!DNL Marketing Channels] attribue certaines conversions à la recherche naturelle, ce qui n’est pas le cas de l’Adobe Advertising, car il ne suit pas la recherche naturelle.

Prenons également le cas d’un client qui consulte une publicité display, clique sur une publicité de recherche payante, clique dans un message électronique, puis passe une commande de 30 USD. Même si Adobe Advertising et [!DNL Marketing Channels] utilisent tous deux le modèle d’attribution Dernière touche, la conversion sera toujours attribuée différemment à chacun d’eux. Adobe Advertising n’a pas accès au canal [!UICONTROL Email], il créditerait donc la recherche payante pour la conversion. [!DNL Marketing Channels], en revanche, a accès aux trois canaux. Il créditerait donc [!UICONTROL Email] pour la conversion.

![Exemple d’attribution de conversion différente dans Adobe Advertising par rapport à [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Pour plus d’informations sur les raisons pour lesquelles les mesures peuvent varier, voir &quot;[Pourquoi les données de canal peuvent varier entre l’Adobe Advertising et  [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)&quot;.

## Différences de données dans Adobe Analytics [!DNL Paid Search Detection]

La fonction [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html?lang=fr) de [!DNL Analytics] permet aux entreprises de [ définir des règles pour suivre le trafic de recherche payante et organique ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html?lang=fr) pour les moteurs de recherche spécifiés. Les règles [!DNL Paid Search Detection] utilisent à la fois une chaîne de requête et le domaine référent pour identifier le trafic de recherche payante et naturelle. Les rapports [!DNL Paid Search Detection] font partie du groupe plus important de rapports [Méthodes de recherche](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html?lang=fr), qui expirent lorsqu’un événement spécifié (tel qu’un passage en caisse) se produit ou que la visite se termine.

Voici l’interface pour créer un jeu de règles [!DNL Paid Search Detection] :

![Exemple d’un jeu de règles de détection de recherche payante dans [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Les [!DNL Paid Search Detection] rapports résultants incluent les rapports [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] et [!UICONTROL Natural Search Keywords].

Notez les deux limitations suivantes avec les données dans les rapports [!DNL Paid Search Detection] :

* Les rapports [!UICONTROL Paid Search Keywords] et [!UICONTROL Natural Search Keywords] affichent les requêtes de recherche identifiées par les URL de référence, et non les mots-clés sur lesquels les utilisateurs enchérissent. Les rapports Adobe Advertising et [!DNL Analytics] affichent les mots-clés réels. De ce fait, ne vous attendez pas à ce qu’ils s’alignent sur les rapports sur les mots-clés [!DNL Paid Search Detection].

* Lors de la création initiale de la fonction [!DNL Paid Search Detection], la requête de recherche d’origine (la chaîne de caractères que l’utilisateur a saisie dans la barre de recherche du moteur de recherche) était plus facilement accessible aux annonceurs via l’URL de référence. Aujourd’hui, les moteurs de recherche obscurcissent largement la requête et les rapports sur les mots-clés [!DNL Paid Search Detection] ont une valeur limitée, car la plupart des données de requête sont sous &quot;non spécifié&quot;.

  Avec [!DNL Analytics for Advertising], les annonceurs peuvent toujours effectuer le suivi des mots-clés payants dans [!DNL Analytics]. Le domaine référent informe le moteur de recherche du moteur de recherche qui a généré le trafic. Puisque les informations de compte spécifiques à l’annonceur ne sont pas liées au domaine référent, tout le trafic est répertorié sous le moteur de recherche. Les annonceurs disposant de plusieurs comptes dans le même moteur de recherche doivent se référer à la création de rapports Adobe Advertising ou [!DNL Analytics] pour les rapports spécifiques aux comptes.

### Pourquoi configurer [!DNL Paid Search Detection] ?

Les rapports [!DNL Paid Search Detection] vous permettent d’identifier le trafic de recherche naturelle dans les [[!DNL Analytics Marketing Channels] rapports](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=fr). La séparation du trafic de recherche payante et du trafic de recherche naturelle est un excellent moyen de comprendre la valeur que la recherche naturelle apporte à l’écosystème marketing complet.

## Validation des données de clic publicitaire pour [!DNL Analytics for Advertising] {#data-validation}

Pour votre intégration, vous devez valider vos données de clics publicitaires afin de vous assurer que toutes les pages de votre site effectuent correctement le suivi des clics publicitaires.

Dans [!DNL Analytics], l’un des moyens les plus simples de valider le suivi [!DNL Analytics for Advertising] consiste à comparer les instances aux clics à l’aide d’une mesure calculée &quot;Instances AMO ID aux clics&quot;, qui est calculée comme suit :

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] représente le nombre de fois où les [AMO IDs](ids.md) sont suivis sur le site. Chaque fois qu’un utilisateur clique sur une publicité, un paramètre AMO ID (`s_kwcid`) est ajouté à l’URL de la page d’entrée. Par conséquent, le nombre de [!UICONTROL AMO ID Instances] est analogue au nombre de clics et peut être validé par rapport aux clics publicitaires réels. Nous constatons généralement un taux de correspondance de 85 % pour [!DNL Search, Social, & Commerce] et un taux de correspondance de 30 % pour le trafic [!DNL DSP] (lorsqu’il est filtré pour inclure uniquement les clics publicitaires [!UICONTROL AMO ID Instances]). La différence d’attentes entre la recherche et l’affichage peut s’expliquer par le comportement de trafic attendu. La recherche capture l’intention et, en tant que telle, les utilisateurs ont généralement l’intention de cliquer sur les résultats de la recherche à partir de leur requête. Toutefois, les utilisateurs qui voient un affichage ou une publicité vidéo en ligne sont plus susceptibles de cliquer dessus involontairement, puis de rebondir à partir du site ou de quitter la nouvelle fenêtre qui se charge avant le suivi de l’activité de page.

Dans les rapports d’Adobe Advertising, vous pouvez également comparer les instances aux clics à l’aide de la mesure &quot;[!UICONTROL EF ID Instances]&quot; au lieu de [!UICONTROL AMO ID Instances] :

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

Bien que vous attendiez un taux de correspondance élevé entre l’AMO ID et l’EF ID, ne vous attendez pas à une parité de 100 %, car AMO ID et l’EF ID effectuent un suivi fondamental de différentes données, et cette différence peut entraîner de légères différences dans le total [!UICONTROL AMO ID Instances] et [!UICONTROL EF ID Instances]. Si le total [!UICONTROL AMO ID Instances] de [!DNL Analytics] diffère de [!UICONTROL EF ID Instances] en Adobe Advertising de plus de 1 %, contactez votre équipe de compte d’Adobe pour obtenir de l’aide.

Pour plus d’informations sur l’AMO ID et l’EF ID, voir [ID d’Adobe Advertising utilisés par Analytics](ids.md).

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### Résolution des problèmes de disparité entre les clics et les instances

Si le rapport [!UICONTROL EF ID Instances]-clics est inférieur à 85 %, vérifiez les points suivants :

* Le suivi des clics est-il manquant pour le compte ou à un sous-niveau quelconque, ou avez-vous un suivi des clics en double (par exemple, aux niveaux du compte et de la campagne) ?

  Dans Search, Social et Commerce, [téléchargez une feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) pour que le compte vérifie les URL de suivi.

  En outre, dans [!DNL Analytics], vous pouvez voir si l’AMO ID et l’EF IF sont ajoutés de manière cohérente à l’aide d’une mesure calculée &quot;[!DNL AMO ID] à [!DNL EF ID]&quot;, qui est calculée comme suit :

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  Une valeur supérieure à 100 % indique qu’il manque plus d’ID EF que d’AMO ID.

* La page d’entrée présente-t-elle un problème de chargement de sorte que l’AMO ID et l’EF ID ne soient pas capturés ?

* L’URL de la page d’entrée est-elle redirigée de sorte que l’AMO ID et l’EF ID soient perdus ?

* Toutes les landing pages utilisent-elles la suite de rapports configurée ?

>[!NOTE]
>
>En théorie, il est possible qu&#39;une instance ait plusieurs clics. Veillez à rechercher les clics sur différents appareils (ordinateurs de bureau, appareils mobiles et tablette, par exemple).

## Comparaison des jeux de données dans [!DNL Analytics for Advertising] contre dans Adobe Advertising

Le [AMO ID](ids.md) (paramètre de chaîne de requête s_kwcid) est utilisé pour la création de rapports dans [!DNL Analytics] et le [EF ID](ids.md) (paramètre de chaîne de requête ef_id) est utilisé pour la création de rapports dans Adobe Advertising. Comme il s’agit de valeurs distinctes, il est possible qu’une valeur soit corrompue ou non ajoutée à la page d’entrée.

Par exemple, supposons que nous ayons la page d’entrée suivante :

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

où l’identifiant EF est &quot;`test_ef_id`&quot; et l’identifiant AMO est &quot;`test_amo_id`&quot;.

Si une redirection côté site se produit, l’URL peut se présenter comme suit :

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

où l’identifiant EF est &quot;`test_ef_id`&quot; et l’identifiant AMO est &quot;`test_amo_id#redirectAnchorTag`&quot;.

Dans cet exemple, l’ajout de la balise d’ancrage ajoute des caractères inattendus à l’AMO ID, ce qui entraîne la présence d’une valeur qu’Analytics ne reconnaît pas. Cet AMO ID ne serait pas classé et les conversions qui y sont associées tomberaient sous &quot;[!UICONTROL unspecified]&quot; ou &quot;[!UICONTROL none]&quot; dans les rapports [!DNL Analytics].

Heureusement, même si des problèmes comme celui-ci sont communs, ils ne génèrent généralement pas un fort pourcentage d&#39;incohérences. Cependant, si vous constatez une différence importante entre les AMO ID dans [!DNL Analytics] et les EF ID dans Adobe Advertising, contactez votre équipe de compte d’Adobe pour obtenir de l’aide.

## Autres considérations relatives aux mesures

### Différence entre les clics et les visites {#clicks-vs-visits}

Elles semblent similaires, mais les clics et les visites représentent des données différentes :

* **Cliquez sur :** [!DNL DSP] ou le moteur de recherche enregistre un clic lorsqu’un visiteur clique sur une publicité sur le site web d’un éditeur.

* **Visite :** [!DNL Analytics] définit une [visite](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=fr) comme une série de pages vues par un utilisateur, se terminant par l’un de plusieurs critères, comme 30 minutes d’inactivité.

Par définition, un clic peut conduire à plusieurs visites.

Prenons l’exemple suivant : l’utilisateur 1 et l’utilisateur 2 accèdent tous deux à un site en cliquant sur une publicité Adobe Advertising. L’utilisateur 1 affiche quatre pages, puis quitte le site pour la journée. Le clic initial se traduit donc par une visite. L’utilisateur 2 consulte deux pages, quitte un déjeuner de 45 minutes, revient, consulte deux pages supplémentaires, puis quitte le site ; dans ce cas, le clic initial entraîne deux visites.

![Exemple de différence entre des clics et des visites](/help/integrations/assets/a4adc-visits-example.png)

### Différence entre les clics et les clics publicitaires

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Les clics et les clics publicitaires sont deux mesures différentes :

* **Cliquez sur :** [!DNL DSP] ou le moteur de recherche enregistre un clic lorsqu’un visiteur clique sur une publicité sur le site web d’un éditeur.

* **Clics publicitaires :** [!DNL Analytics] enregistre un clic publicitaire lorsque le visiteur arrive sur le site web de destination, que la page d’entrée se charge et que la requête [!DNL Analytics] située au bas de la page envoie les données à [!DNL Analytics].

Les clics et les clics publicitaires peuvent varier sensiblement en raison de clics publicitaires accidentels. Nous avons observé que la plupart des clics sur les annonces affichées sont des clics accidentels et que ces visiteurs accidentels cliquent sur le bouton Précédent avant le chargement de la page d’entrée. Par conséquent, [!DNL Analytics] ne peut pas enregistrer de clic publicitaire. Cela est particulièrement vrai pour les annonces sur lesquelles un clic accidentel est plus probable, comme les annonces mobiles, les publicités vidéo et les publicités qui remplissent l’écran et qui doivent être fermées avant que l’utilisateur puisse afficher la page.

Les sites chargés sur des périphériques mobiles sont également moins susceptibles de générer des clics publicitaires en raison de largeurs de bande plus faibles ou de la puissance de traitement disponible, ce qui entraîne un chargement plus long des landing pages. Il n’est pas rare que 50 à 70 % des clics ne génèrent pas de clics publicitaires. Dans les environnements mobiles, la différence peut atteindre 90 % en raison de la combinaison d’un navigateur plus lent et de la plus grande probabilité que l’utilisateur clique accidentellement sur la publicité lors du défilement de la page ou de la tentative de fermeture de la publicité.

Les données de clic peuvent également être enregistrées dans des environnements qui ne peuvent pas enregistrer les clics publicitaires avec les mécanismes de suivi actuels (tels que les clics vers ou depuis une application mobile) ou pour lesquels l’annonceur a déployé une seule approche de suivi (par exemple, avec l’approche JavaScript d’affichage publicitaire, les navigateurs qui bloquent les cookies tiers effectuent le suivi des clics, mais pas les clics publicitaires). Adobe recommande de déployer les méthodes de suivi des URL de clics et des affichages publicitaires JavaScript pour une raison essentielle : optimiser la couverture des clics publicitaires pouvant faire l’objet d’un suivi.

### Utilisation de mesures de trafic Adobe Advertising pour les Dimensions non Adobes Advertising

Adobe Advertising fournit à Analytics des [ mesures de trafic spécifiques à la publicité et les dimensions associées provenant de  [!DNL DSP] et [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Les mesures fournies par l’Adobe Advertising s’appliquent uniquement aux dimensions d’Adobe Advertising spécifiées et les données ne sont pas disponibles pour les autres dimensions dans [!DNL Analytics].

Par exemple, si vous affichez les mesures [!UICONTROL Adobe Advertising Clicks] et [!UICONTROL Adobe Advertising Cost] par compte, qui est une dimension d’Adobe Advertising, alors le total [!UICONTROL Adobe Advertising Clicks] et [!UICONTROL Adobe Advertising Cost] est affiché par compte.

![Exemple de mesures d’Adobe Advertising dans un rapport utilisant une dimension d’Adobe Advertising](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Cependant, si vous affichez les mesures [!UICONTROL Adobe Advertising Clicks] et [!UICONTROL Adobe Advertising Cost] selon une dimension sur la page (telle que Page), pour laquelle l’Adobe Advertising ne fournit pas de données, alors les [!UICONTROL Adobe Advertising Clicks] et [!UICONTROL Adobe Advertising Cost] de chaque page sont nuls (0).

![Exemple de mesures d’Adobe Advertising dans un rapport utilisant une dimension non prise en charge](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Utilisation de [!UICONTROL AMO ID Instances] comme substitut pour les clics avec des Dimensions non Adobes Advertising

Puisque vous ne pouvez pas utiliser [!UICONTROL AMO Clicks] avec des dimensions sur site, vous pouvez trouver un équivalent aux clics. Vous pouvez être tenté d’utiliser les visites comme substitut, mais elles ne sont pas la meilleure option, car chaque visiteur peut avoir plusieurs visites. (Voir &quot;[Différence entre les clics et les visites](#clicks-vs-visits)&quot;. Nous vous recommandons plutôt d’utiliser [!UICONTROL AMO ID Instances], qui est le nombre de fois où l’AMO ID est capturé. Bien que [!UICONTROL AMO ID Instances] ne corresponde pas exactement à [!UICONTROL AMO Clicks], il s’agit de la meilleure option pour mesurer le trafic de clics sur le site. Pour plus d’informations, voir &quot;[Validation des données de clic publicitaire pour [!DNL Analytics for Advertising]](#data-validation)&quot;.

![Exemple de [!UICONTROL AMO ID Instances] au lieu de [!UICONTROL Adobe Advertising Clicks] pour une dimension non prise en charge](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Adobe Advertising des mesures dans Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Données en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [ Pourquoi les données peuvent varier entre l’Adobe Advertising et  [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
