---
title: Sécurité de la marque et qualité des médias
description: En savoir plus sur les fonctionnalités de sécurité de la marque et de qualité multimédia.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: 9b5c00cdb0942ec4e7fbf69d7ce638ab50439915
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# Sécurité de la marque et qualité des médias

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP fournit une suite de fonctionnalités de protection de marque pour vous assurer que chacune de vos campagnes atteint de vrais utilisateurs dans un environnement sûr pour la marque.

Notre équipe de surveillance de la fraude travaille en étroite collaboration avec des partenaires de premier plan de l&#39;industrie, tels que le [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] et [!DNL WhiteOps], pour traiter soigneusement l&#39;inventaire sur notre plateforme. Grâce à une gestion proactive de son approvisionnement, DSP s’assure que tous les annonceurs de la plateforme sont protégés contre le trafic non humain (robots, robots d&#39;exploration, trafic des centres de données et fraude) et ne diffusent que dans des contextes sécurisés par la marque.

En plus de fournir une gestion centralisée de la qualité, nous croyons en la possibilité pour les annonceurs de concevoir des contrôles qui s&#39;alignent sur leur marque. DSP propose des intégrations avec [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39], afin que chaque annonceur puisse choisir le niveau de protection contre la fraude, de filtrage contextuel et de ciblage par mot-clé souhaité.

## Initiatives de qualité

### Vérification des stocks avec prise en charge des [!DNL Ads.txt]

[[!DNL Ads.txt], qui signifie  [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) est une initiative lancée par le [!DNL Interactive Advertising Bureau] ([!DNL IAB]) en juin 2017 pour faciliter la représentation correcte des stocks sur le marché libre, et ainsi lutter contre les sources illégitimes de trafic et d&#39;usurpation de domaine. Les éditeurs et distributeurs participants déclarent publiquement les sociétés autorisées à vendre leur inventaire numérique, ainsi que la nature de ces relations, en maintenant une page `ads.txt` au niveau supérieur du domaine (comme `example.com/ads.txt`).

DSP prend en charge les [!DNL ads.txt] en lisant le fichier `ads.txt` de chaque éditeur et en vous offrant la possibilité d’acheter uniquement auprès de vendeurs [!DNL ads.txt] vérifiés. Par exemple, en faisant correspondre les vendeurs auxquels nous voyons l&#39;accès `nytimes.com` au fichier `ads.txt` du New York Times, nous pouvons identifier ceux qui sont légitimes et ceux qui ne le sont pas, et nous bloquerons les contrevenants si le placement est configuré pour acheter uniquement auprès de vendeurs vérifiés. <!-- can we actually mention NY Times? -->

Vous pouvez définir des commandes de [!DNL ads.txt] par défaut pour chaque annonceur<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> puis, éventuellement[&#x200B; personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md) pour :

* achetez uniquement des stocks auprès des vendeurs directs autorisés d’un domaine

* achetez uniquement des stocks auprès des vendeurs directs et revendeurs autorisés d’un domaine

* donnez la priorité à l’achat de stocks auprès des vendeurs directs et des revendeurs autorisés d’un domaine

* acheter des stocks auprès de tous les vendeurs

### Surveillance de la fraude sur les plateformes

DSP a développé des outils et des systèmes internes solides pour gérer la fraude sur l’ensemble de sa plateforme, en s’associant à des fournisseurs leaders du secteur tels que [!DNL Whiteops] et [!DNL Integral Ad Science].

En outre, Adobe travaille en étroite collaboration avec [!DNL IAB] et [!DNL TAG] pour assurer un blocage de la fraude robuste et standard afin de protéger nos annonceurs, en utilisant des outils tels que [!DNL ads.txt] (voir la section précédente), la liste des robots et des araignées [!DNL IAB] et la liste des adresses IP des centres de données [!DNL TAG].

Grâce à notre approche multidimensionnelle de la qualité, notre équipe surveille les anomalies et les modèles de trafic non valides, en veillant à ce que moins de 3 % du trafic non valide figure dans l&#39;inventaire protégé. Tout stock suspect, y compris l’inventaire sur des domaines spécifiques ou provenant d’éditeurs ou de vendeurs spécifiques, est immédiatement bloqué sur la plateforme.

### Mappage, hiérarchisation et catégorisation des stocks

Le mappage des stocks est le processus d’examen et d’intégration détaillé requis pour tous les nouveaux stocks avant qu’ils ne soient ajoutés à notre plateforme. Ce processus est conçu pour assurer la sécurité et la qualité de tous les inventaires sur DSP.

* **Mappage :** notre équipe d’inventaire examine attentivement chaque domaine et évalue des aspects tels que :

   * Sécurité de la marque

   * Vérification du type d’annonce publicitaire

   * Contenu générique, domaines en double et diffusion de fausses publicités

* **Hiérarchisation :** nous examinons de manière holistique la présence des marques dans l’écosystème global pour classer les stocks à différents niveaux. Vous pouvez [cibler vos emplacements](/help/dsp/campaign-management/placements/placement-settings.md) sur ces niveaux pour le niveau de portée souhaité :

   * **[!UICONTROL T1]** — Sites de marque reconnus internationalement

   * **[!UICONTROL T2]** : sites attrayants, actuels, à jour, sans contenu créé par l&#39;utilisateur et généralement dépourvus de reconnaissance internationale

   * **[!UICONTROL T3]** — Contenu créé par l&#39;utilisateur et contenu spécialisé

* **Catégorisation des sites :** pour faciliter le ciblage et le blocage du contenu, nous balisons chaque propriété avec une catégorie de site définie par DSP en fonction du contenu de la propriété. Vous pouvez [cibler ou exclure ces catégories de site pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md) en fonction des objectifs d’emplacement.

### Prise en charge complète du blocage de sites

DSP fournit à la fois une liste de sites bloqués globalement et la possibilité de créer des listes de sites bloqués personnalisées pour les annonceurs et les comptes.

#### Liste des sites bloqués globalement de DSP {#global-blocked-sites}

DSP conserve une liste de sites globalement bloqués sur lesquels il est jugé dangereux d’exécuter des publicités. Cette liste contient des sites au contenu répréhensible (comme la haine ou la terreur) et des sites infectés par des robots, de faux pré-roll, des domaines incompatibles et d’autres activités frauduleuses.

Dans le cadre de notre initiative Brand Safety visant à éradiquer les activités qui fraudent les annonceurs, tous les sites sont examinés à l&#39;aide des mesures de la liste des sites bloqués du graphique. Tous les sites qui ne réussissent pas les contrôles de sécurité de la marque sont ajoutés à la liste des sites bloqués. Comme DSP gère cette liste de manière dynamique, les sites peuvent être activés ou désactivés à tout moment, en fonction de la dernière analyse de sécurité de la marque.

Lorsque vous incluez un site dans la liste des sites bloqués globalement en tant que cible d’emplacement, le site est signalé par un point d’exclamation rouge (!). Cela indique que les publicités ne s’exécutent pas sur le site marqué d’un indicateur.

>[!NOTE]
>
>Vous pouvez éventuellement contourner la liste globale des sites bloqués pour les publicités display standard jointes à une offre privée approuvée en activant l’option « [!UICONTROL Allow unscreened sites] » dans les [&#x200B; paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Si nécessaire, l’équipe du compte Adobe peut également désactiver le blocage de site pour une transaction publique (au niveau des enchères) dans les paramètres de l’éditeur pour la transaction.

#### Listes de sites bloqués au niveau du compte et de l’annonceur

Les utilisateurs peuvent également gérer des listes de sites bloqués au niveau du compte et de l’annonceur<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) --> qui sont utilisées automatiquement pour tous les emplacements. La liste des sites bloqués de niveau inférieur est appliquée en plus de la liste des sites bloqués globalement.

## Intégrations tierces

### Filtrage contextuel

Le filtrage contextuel vous permet de cibler ou de bloquer des opportunités publicitaires en fonction du contexte de la page sur laquelle la publicité serait diffusée. Adobe fournit un filtrage contextuel par le biais d’intégrations avec les principaux fournisseurs du secteur : [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39]. Les filtres actuels incluent par exemple [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] et [!UICONTROL G-rated Sites].

Vous pouvez définir des contrôles de filtre contextuels par défaut pour chaque annonceur<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> puis, éventuellement[&#x200B; personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonctionnalité.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Blocage des fraudes avant enchères

Tirez parti de nos intégrations tierces à [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39] pour bloquer le trafic non humain provenant de vos campagnes. Ces intégrations fournissent des fonctionnalités de blocage de pré-enchères de pointe pour minimiser le trafic non valide général et sophistiqué (GIVT et SIVT) dans vos campagnes.

Vous pouvez définir des contrôles par défaut de blocage de la fraude avant enchères pour chaque annonceur<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> puis, éventuellement[&#x200B; personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonctionnalité.

Pour plus d’informations sur les fonctionnalités, contactez directement votre fournisseur préféré ou l’équipe chargée de votre compte Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilité des pré-enchères {#pre-bid-viewability}

Les filtres de visibilité de pré-enchères optimisés par nos partenaires leaders du secteur [!DNL DoubleVerify] et [!DNL Integral Ad Science] permettent aux annonceurs de s’assurer que leurs campagnes atteignent leurs objectifs de performance de visibilité souhaités sur la vidéo et l’inventaire des affichages.

Vous pouvez définir des filtres de visibilité par défaut pour chaque annonceur<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> puis éventuellement [&#x200B; personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonctionnalité.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo intégral Ad Science](/help/dsp/assets/ias-logo.png)

### Ciblage et mesure de l’attention

[!DNL Adobe's] partenariat avec [!DNL Adelaide] fournit aux annonceurs une prise en charge de la mesure d’Adélaïde « [!DNL Attention Units] », qui mesure la qualité des médias en fonction du suivi oculaire, de l’exposition et des données sur les résultats.

Le [ciblage de l’attention avant enchères au niveau du positionnement](/help/dsp/campaign-management/placements/placement-settings.md) permet aux annonceurs de cibler des niveaux d’attention spécifiques afin d’améliorer l’engagement du client.

En outre, les annonceurs peuvent activer le [suivi de la mesure de [!UICONTROL Attention Score] au niveau de l’emplacement](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (nombre moyen pondéré de [!DNL Attention Units] sur les impressions) pour toute campagne afin de comprendre quelles tactiques d’emplacement produisent les meilleurs résultats commerciaux.

Des frais supplémentaires s’appliquent pour chaque fonctionnalité distincte.

### Ciblage des rubriques

Le ciblage de sujets DSP vous permet de cibler ou de bloquer des listes de mots-clés en tirant parti de nos [!DNL Comscore] de partenaires contextuels de pointe. Le ciblage par sujet vous permet de vous assurer que vos publicités sont toujours diffusées dans un environnement qui correspond à votre marque, que ce soit en bloquant le contenu préjudiciable ou en veillant à ce que les dépenses soient effectuées dans un contexte qui garantit un meilleur résultat.

Le ciblage de rubrique nécessite que vous créiez des segments de rubrique personnalisés directement avec la plateforme du partenaire. Une fois les segments créés, vous pouvez [cibler ou exclure un identifiant de segment dans la section [!UICONTROL Audience Targeting] pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer pour cette fonctionnalité.

Pour créer un compte [!DNL Comscore] et des segments de rubrique personnalisés, vous pouvez demander une connexion pour [!DNL Activation Segment Manager] à l’adresse [https://agents.comscore.com](https://agents.comscore.com). Consultez le [[!DNL Comscore] centre d’aide](https://comscoreactivation.zendesk.com/hc/) pour obtenir des instructions complètes sur la configuration des segments personnalisés. Les frais des segments personnalisés sont visibles dans [!DNL Segment Manager] au fur et à mesure de leur création.

![&#x200B; Logo Comscore &#x200B;](/help/dsp/assets/comscore-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP s’est associé à [!DNL DoubleVerify] pour proposer sa solution de ciblage [!DNL Authentic Brand Safety], qui permet de créer un ensemble centralisé d’exigences de sécurité de marque à cibler sur toutes vos plateformes d’achat, par souci de cohérence.

Une fois que vous avez créé un segment de sécurité de marque [!DNL DoubleVerify] avec le ciblage nécessaire, vous pouvez l’utiliser dans DSP pour répliquer vos règles de blocs post-enchères avec pré-enchères dans les environnements web.

Vous pouvez spécifier un identifiant de segment [!DNL DoubleVerify] pour chaque annonceur<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> puis éventuellement [activer ou désactiver l’[!UICONTROL Authentic Brand Safety] pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). DSP facture votre compte pour l’utilisation de l’identifiant de segment.

Pour plus d’informations sur les fonctionnalités, contactez directement [!DNL DoubleVerify] ou l’équipe chargée de votre compte Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
