---
title: Sécurité des marques et qualité des médias
description: En savoir plus sur la sécurité de la marque et les fonctionnalités de qualité multimédia.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# Sécurité des marques et qualité des médias

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP fournit une suite de fonctionnalités de protection de la marque pour s’assurer que chacune de vos campagnes atteint des utilisateurs réels dans un environnement sécurisé.

Notre équipe de surveillance des fraudes travaille en étroite collaboration avec les principaux partenaires du secteur, tels que [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] et [!DNL WhiteOps], pour organiser soigneusement l’inventaire sur notre plateforme. Grâce à une gestion proactive de notre offre, DSP veille à ce que tous les annonceurs de la plate-forme soient protégés du trafic non humain (robots, robots d’indexation, trafic du centre de données et fraude) et à ne diffuser que dans des contextes sécurisés contre la marque.

En plus d’offrir une gestion centralisée de la qualité, nous pensons à donner aux annonceurs les moyens de concevoir les contrôles qui s’alignent sur leur marque. DSP propose des intégrations avec [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39], en veillant à ce que chaque annonceur puisse choisir le niveau de protection anti-fraude souhaité, le filtrage contextuel et le ciblage des mots-clés.

## Initiatives de qualité

### Vérification de l’inventaire avec prise en charge de [!DNL Ads.txt]

[[!DNL Ads.txt], qui signifie  [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) est une initiative lancée par [!DNL Interactive Advertising Bureau] ([!DNL IAB]) en juin 2017 pour faciliter la représentation correcte des stocks sur le marché ouvert, combattant ainsi les sources illégitimes de trafic et d&#39;usurpation de domaine. Les éditeurs et distributeurs participants déclarent publiquement les entreprises autorisées à vendre leur inventaire numérique, ainsi que la nature de ces relations, en conservant une page `ads.txt` au niveau supérieur du domaine (par exemple `example.com/ads.txt`).

DSP prend en charge [!DNL ads.txt] en lisant le fichier `ads.txt` de chaque éditeur et en vous donnant la possibilité de n&#39;acheter qu&#39;auprès de vendeurs [!DNL ads.txt] vérifiés. Par exemple, en faisant correspondre les vendeurs qui accèdent à `nytimes.com` au fichier `ads.txt` du New York Times, nous pouvons identifier ceux qui sont légitimes et ceux qui ne le sont pas, et nous bloquerons les contrevenants si l&#39;emplacement est configuré pour acheter uniquement auprès de vendeurs vérifiés. <!-- can we actually mention NY Times? -->

Vous pouvez définir des [!DNL ads.txt] contrôles par défaut pour chaque annonceur<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md) pour :

* acheter un stock à partir des vendeurs directs autorisés d’un domaine uniquement ;

* acheter un stock à partir des revendeurs directs et revendeurs autorisés d’un domaine uniquement ;

* donner la priorité à l’achat du stock à partir des revendeurs directs et revendeurs autorisés d’un domaine ;

* acheter un stock à tous les vendeurs ;

### Surveillance des fraudes sur les plateformes

DSP a créé des outils et des systèmes internes performants pour gérer la fraude sur notre plateforme, en partenariat avec des fournisseurs de pointe tels que [!DNL Whiteops] et [!DNL Integral Ad Science].

En outre, Adobe travaille en étroite collaboration avec [!DNL IAB] et [!DNL TAG] pour garantir un blocage des fraudes robuste et standard pour protéger nos annonceurs, en exploitant des outils tels que [!DNL ads.txt] (voir la section précédente), la liste [!DNL IAB] Robots et araignées et la liste d’adresses IP du centre de données [!DNL TAG].

Grâce à notre approche multidimensionnelle de la qualité, notre équipe surveille les anomalies et les schémas de trafic non valides, en assurant moins de 3 % de trafic non valide sur un inventaire protégé. Tout inventaire suspect, y compris les stocks sur des domaines spécifiques ou provenant d&#39;éditeurs ou de vendeurs spécifiques, est immédiatement bloqué sur l&#39;ensemble de la plateforme.

### Mappage, classement et catégorisation des stocks

Le mapping de l’inventaire est le processus détaillé de révision et d’intégration requis pour tous les nouveaux stocks avant de les ajouter à notre plateforme. Ce processus est conçu pour assurer la sécurité et la qualité de tous les inventaires sur DSP.

* **Mappage :** Notre équipe d’inventaire examine soigneusement chaque domaine, en évaluant des aspects tels que :

   * Sécurité des marques

   * Vérification du type d’annonce

   * Contenu générique, domaines en double et service de fausses publicités

* **Classement :** Nous examinons la présence de la marque dans l’écosystème global pour classer l’inventaire sur différents niveaux. Vous pouvez [cibler vos emplacements](/help/dsp/campaign-management/placements/placement-settings.md) sur ces niveaux pour le niveau de portée souhaité :

   * **[!UICONTROL T1]** - Nom de marque, sites reconnaissables internationalement

   * **[!UICONTROL T2]** : sites d’exception, à jour et actualisés, sans contenu généré par l’utilisateur, qui manquent généralement de reconnaissance globale

   * **[!UICONTROL T3]** — Contenu généré par l’utilisateur et contenu de niche

* **Classification de site :** Pour garantir un ciblage et un blocage faciles du contenu, nous balisons chaque propriété avec une catégorie de site définie DSP en fonction du contenu de la propriété. Vous pouvez [cibler ou exclure ces catégories de site pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md) en fonction des objectifs d’emplacement.

### Prise en charge complète du blocage de site

DSP fournit à la fois une liste de sites bloqués globalement et la possibilité de créer des listes de sites bloqués personnalisées pour les annonceurs et les comptes.

#### DSP Liste globale des sites bloqués {#global-blocked-sites}

DSP tient à jour une liste de sites bloqués à l’échelle mondiale de sites considérés comme dangereux pour l’exécution des publicités. Cette liste contient des sites présentant des contenus répréhensibles (tels que la haine ou la terreur) et des sites infectés par des robots, des faux preroll, des domaines discordants et d&#39;autres activités frauduleuses.

Dans le cadre de notre initiative de sécurité des marques (Brand Safety) visant à éradiquer les activités qui fraudent les publicitaires, tous les sites sont analysés à l’aide des mesures figurant dans la liste des sites bloqués du graphique. Tous les sites qui ne réussissent pas les contrôles de sécurité de la marque sont ajoutés à la liste des sites bloqués globalement. DSP gère cette liste de manière dynamique. Aussi, les sites peuvent-ils s’y placer ou la quitter à tout moment, en fonction des dernières analyses de sécurité de la marque.

Lorsque vous incluez un site sur la liste des sites bloqués globalement comme cible d’emplacement, le site est marqué d’un point d’exclamation rouge (!). Cela indique que les publicités ne s’exécutent pas sur le site marqué.

>[!NOTE]
>
>Vous pouvez éventuellement contourner la liste des sites bloqués globaux pour les annonces d’affichage standard associées à une transaction privée de confiance en activant l’option &quot;[!UICONTROL Allow unscreened sites]&quot; dans les [paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md). Si nécessaire, l’équipe du compte d’Adobe peut également, de manière facultative, désactiver le blocage du site pour une transaction publique (au niveau de l’enchère) dans les paramètres de l’éditeur pour l’opération.

#### Listes de sites bloqués au niveau du compte et des annonceurs

Les utilisateurs peuvent également gérer des listes de sites bloqués au niveau du compte et de l’annonceur <!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, qui sont utilisées automatiquement pour tous les emplacements. La liste des sites bloqués de niveau inférieur est appliquée en plus de la liste des sites bloqués globalement.

## Intégrations tierces

### Filtrage contextuel

Le filtrage contextuel vous permet de cibler ou de bloquer des opportunités publicitaires en fonction du contexte de la page sur laquelle la publicité serait diffusée. Adobe propose un filtrage contextuel via des intégrations avec des fournisseurs de premier plan du secteur : [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39]. Parmi les exemples de filtres actuels, citons [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] et [!UICONTROL G-rated Sites].

Vous pouvez définir des contrôles de filtre contextuel par défaut pour chaque annonceur<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis, éventuellement, [personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Blocage des fraudes avant offre

Tirez parti de nos intégrations tierces avec [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39] pour bloquer le trafic non humain de vos campagnes. Ces intégrations fournissent des fonctionnalités de blocage avant enchères leaders du secteur afin de minimiser le trafic général et sophistiqué non valide (GIVT et SIVT) dans vos campagnes.

Vous pouvez définir des contrôles par défaut de blocage de fraude avant offre pour chaque annonceur<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis, éventuellement, [personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

Pour plus d’informations sur les fonctionnalités, contactez directement votre fournisseur préféré ou contactez votre équipe de compte d’Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilité avant l’offre {#pre-bid-viewability}

Les filtres de visibilité avant l’offre, optimisés par nos partenaires de pointe [!DNL DoubleVerify] et [!DNL Integral Ad Science], permettent aux annonceurs de s’assurer que leurs campagnes correspondent aux objectifs de performances de visionnage souhaités dans l’inventaire vidéo et d’affichage.

Vous pouvez définir des filtres de visibilité par défaut pour chaque annonceur <!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis, éventuellement, [personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png)

### Ciblage et mesure de l’attention

Le partenariat [!DNL Adobe's] avec [!DNL Adelaide] fournit aux annonceurs la prise en charge de la mesure Adélaïde &quot;[!DNL Attention Units]&quot;, qui mesure la qualité des médias en fonction du suivi oculaire, de l’exposition et des données de résultat.

[Le ciblage de l’attention avant offre au niveau de l’emplacement](/help/dsp/campaign-management/placements/placement-settings.md) permet aux annonceurs de cibler des niveaux d’attention spécifiques pour améliorer l’engagement des clients.

En outre, les annonceurs peuvent activer le [suivi de la mesure [!UICONTROL Attention Score] de niveau emplacement](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (le nombre moyen pondéré de [!DNL Attention Units] sur toutes les impressions) pour n’importe quelle campagne afin de comprendre quelles tactiques de placement produisent les meilleurs résultats commerciaux.

Des frais supplémentaires s’appliquent pour chaque fonctionnalité distincte.

### Ciblage de rubrique

DSP ciblage de rubrique vous permet de cibler ou de bloquer des listes de mots-clés en exploitant notre partenaire contextuel de pointe [!DNL Comscore]. Le ciblage des rubriques vous permet de vous assurer que vos publicités sont toujours diffusées dans un environnement qui s’aligne sur votre marque, que ce soit en bloquant des contenus nocifs ou en veillant à dépenser dans un contexte qui garantit un meilleur résultat.

Le ciblage des rubriques nécessite de créer des segments de rubrique personnalisés directement avec la plateforme partenaire. Une fois les segments créés, vous pouvez [cibler ou exclure un identifiant de segment dans la section [!UICONTROL Audience Targeting] pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer pour cette fonctionnalité.

Pour créer un compte [!DNL Comscore] et des segments de rubrique personnalisés, vous pouvez demander un identifiant pour [!DNL Activation Segment Manager] à l’adresse [https://agents.comscore.com](https://agents.comscore.com). Pour obtenir des instructions complètes sur la configuration des segments personnalisés, consultez le [[!DNL Comscore] centre d’aide](https://comscoreactivation.zendesk.com/hc/) . Les frais pour les segments personnalisés sont visibles dans [!DNL Segment Manager] lors de leur création.

![Logo Comscore](/help/dsp/assets/comscore-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP s&#39;est associé à [!DNL DoubleVerify] pour proposer sa solution de ciblage [!DNL Authentic Brand Safety], qui vous permet de créer un ensemble centralisé d&#39;exigences de sécurité de la marque à cibler sur toutes vos plateformes d&#39;achat pour une cohérence.

Une fois que vous avez créé un segment de sécurité de marque [!DNL DoubleVerify] avec le ciblage nécessaire, vous pouvez l’utiliser dans DSP pour répliquer vos règles de blocage post-enchère avec pré-enchère dans les environnements web.

Vous pouvez spécifier un [!DNL DoubleVerify] identifiant de segment pour chaque annonceur<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [ activer ou désactiver [!UICONTROL Authentic Brand Safety] pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). DSP facture votre compte pour l’utilisation de l’identifiant de segment.

Pour plus d&#39;informations sur les fonctionnalités, contactez directement [!DNL DoubleVerify] ou contactez votre équipe de compte d&#39;Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
