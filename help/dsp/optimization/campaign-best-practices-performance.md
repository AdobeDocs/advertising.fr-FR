---
title: Bonnes pratiques pour configurer des campagnes de performances
description: Découvrez les bonnes pratiques pour configurer vos campagnes axées sur les performances, qui incluent des emplacements optimisés pour le CPA le plus bas ou le ROAS le plus élevé.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 802c75920bb11f262cbe0d76d2554971aaf35831
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# Bonnes pratiques pour configurer des campagnes de performances

DSP peut optimiser vos campagnes axées sur les performances. Consultez les bonnes pratiques suivantes pour les campagnes de performances :

* Étape 1 - Définition de votre objectif
* Étape 2 - Définition de votre stratégie
* Étape 3 - Création de modules
* Étape 4 - Création de la structure de placement
* Étape 5 - Utilisation de la bonne Assets créative

## Étape 1 - Définition de votre objectif

Il est important de comprendre l&#39;objectif de la campagne, par exemple atteindre le meilleur retour sur investissement possible ou le CPA le plus bas possible. Les campagnes de performances ont les [objectifs d’optimisation](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;. Pour chaque package de l&#39;opération, définissez l&#39;objectif d&#39;optimisation en conséquence.

![objectif d’optimisation](/help/dsp/assets/optimization-goals.png)

Vous devez également déterminer le ou les événements de succès qui mènent à l’objectif global et créer des objectifs personnalisés en conséquence. Pour chaque module, spécifiez un objectif personnalisé à utiliser avec l’objectif d’optimisation général pour les rapports et l’optimisation algorithmique à l’aide de [!DNL Adobe Sensei]. Pour plus d’informations sur la création d’objectifs personnalisés, y compris les bonnes pratiques, voir [Objectifs personnalisés](custom-goal.md).

## Étape 2 - Définition de votre stratégie

### Stratégies de prospection

Les packages entonnoir supérieur incluent des emplacements avec un ciblage très large pour atteindre les nouveaux consommateurs nets.

#### Stratégies de positionnement recommandées pour la prospection

* Recherchez de nouvelles audiences susceptibles d’être converties à l’aide des tactiques suivantes :

   * Modélisation analogue à partir d’une plateforme de gestion de données (DMP), telle que Adobe Audience Manager.
   * Ciblage comportemental utilisant des données tierces.
   * Ciblage contextuel.
   * Ciblage de site/catégorie.

* Utiliser le ciblage d’exécution de réseau (RON) : il est important d’inclure une exécution de placement de réseau sans ciblage d’audience et avec un ciblage d’inventaire étendu. Cela permet à l’algorithme [!DNL Adobe Sensei] de rechercher des utilisateurs précieux qui peuvent avoir de nouveaux cookies qui n’ont pas encore été classés dans une audience.

### Stratégies de reciblage

Les modules d’entonnoir inférieurs incluent des emplacements qui ciblent les utilisateurs qui ont déjà consulté la page web de l’annonceur ou pour lesquels l’annonceur dispose de données CRM.

#### Stratégies de positionnement recommandées pour le reciblage

* Si l’annonceur est un client Adobe Analytics ou Adobe Audience Manager, vous pouvez créer des segments propriétaires (tels que les visiteurs de la page d’accueil, les pages de produits ou les personnes ayant abandonné leur panier) et les utiliser comme cibles d’emplacement dans DSP.

* Évitez d’affecter trop de budget à un emplacement ciblé sur l’audience. En règle générale, budgétez 30 $ pour 1 000 utilisateurs par mois.

## Étape 3 - Création de modules

La bonne pratique consiste à créer des modules distincts pour la prospection des entonnoirs supérieurs et pour le reciblage des entonnoirs inférieurs. L’optimisation se produit au niveau du module, de sorte que les données de performances de tous les emplacements d’un module soient regroupées. Par conséquent, regroupez les emplacements dans des modules avec des performances attendues similaires.

![exemple de packages distincts pour la prospection et le reciblage](/help/dsp/assets/p-r.png)

Utilisez également les paramètres suivants.

### Objectifs et budget

* **Traitement et limitation :** Pour sélectionner un objectif d’optimisation du CPA ou ROAS, le package doit utiliser un traitement au niveau du package. Cela permet de s’assurer que tous les emplacements du module sont optimisés pour répartir les dépenses selon les performances et l’échelle en fonction des objectifs sélectionnés.

* **Dates de vol :** (Packages de prospection) Lorsque votre campagne s’exécute pendant plus de 25 jours, utilisez la fonction [!UICONTROL Activate Custom Flighting]. Tout d&#39;abord, définissez un vol personnalisé pour les 10 premiers jours à environ 75 % du budget quotidien nécessaire pour réduire les dépenses pendant la *phase d&#39;apprentissage*. Définissez ensuite un second vol personnalisé pour le reste du budget.

  Par exemple, si vous avez 100 000 $ à dépenser en 30 jours, définissez le budget du vol 1 (Jours 1 à 10) sur 25 000 $ (75 % x 100 $,000/30 jours = 2 500 $ par jour). Utilisez le budget restant de 75 000 $ pour le vol 2 (jours 11-30).

* **Budget :** DSP toujours tenter d&#39;allouer 100 % du budget du package uniformément entre tous les emplacements d&#39;un package. Si un emplacement a de faibles dépenses ou pas de dépenses, nous vous recommandons de limiter le budget de l’emplacement afin de permettre une plus grande partie du budget à affecter aux emplacements à l’échelle. Prévoyez de 24 à 48 heures pour que les modifications du budget soient calibrées.

* **Objectifs d’optimisation :** utilisez l’un des deux objectifs d’optimisation des performances, *[!UICONTROL Highest Return on Ad Spend]* ou *[!UICONTROL Lowest Cost per Acquisition]*, selon l’objectif du module. Ces objectifs optimisent automatiquement le package vers les emplacements de CPA les plus élevés ou les plus bas, respectivement.

* **Objectifs personnalisés :**
   * Si un nouveau module a le même objectif qu’un module existant, vous pouvez éventuellement lier le module existant afin que l’algorithme puisse utiliser les données d’apprentissage automatique existantes.
   * Saisissez le [!UICONTROL Target CPA] ou [!UICONTROL Target ROAS] approprié.

* **Navigation de vol et fréquence intermédiaire :** Pour les deux types de fréquence, sélectionnez *[!UICONTROL Even]* pour optimiser vos objectifs de performances en effectuant un rythme uniforme tout au long de la journée et tout au long du vol.

  >[!CAUTION]
  >
  >Utilisez *[!UICONTROL FrontLoad]* et *[!UICONTROL Aggressive Front Load]* pour le rythme des vols et *[!UICONTROL ASAP]* le rythme des trajets uniquement lorsque vous priorisez entièrement la diffusion et dépensez sur l’optimisation des performances, car ces stratégies peuvent avoir une incidence négative sur les IPC de performances souhaités.

## Étape 4 - Création de la structure de placement

Moins c&#39;est plus. Si vous pouvez configurer moins de six emplacements par package, le budget disponible peut dynamiquement passer aux emplacements les plus performants plus facilement.

Veillez également à ajouter chaque emplacement à un package avec un type d’objectif de package *[!UICONTROL Prospecting]* ou *[!UICONTROL Retargeting]*, selon le cas.

Voici les paramètres d’emplacement recommandés pour les campagnes de performances.

### Objectifs

Vous devez configurer l’optimisation du CPA ou du RSDP au niveau du package (voir Etape 3 - Créer des packages), mais vous pouvez ajouter des paramètres de niveau de placement supplémentaires.

* **Offre maxi :**
   * Pour les emplacements de prospection, utilisez une offre maximale basse (5 $).
   * Pour recibler des emplacements, utilisez une offre maximale élevée (12 $).

* **Filtres avant offre :** limitez ou évitez idéalement de définir des filtres avant offre agressifs, ce qui empêche l’emplacement d’atteindre l’échelle. Les bonnes pratiques sont les suivantes :

   * Utilisez un (1) filtre pré-enchère par emplacement. L’utilisation de plusieurs filtres de pré-enchère requiert que les deux soient satisfaits, ce qui réduit l’échelle.

   * Envisagez de définir des filtres de pré-enchère moins stricts dans les cas où un ciblage supplémentaire (comme l’audience, la géolocalisation et le ciblage du site) est appliqué.

Consultez la description du moment où utiliser chaque filtre de pré-offre à l’adresse [Filtres de pré-offre de niveau emplacement et Comment les utiliser](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventaire

Pour agrandir l&#39;échelle, utilisez l&#39;inventaire [!UICONTROL Public] (Ouvrir l&#39;Exchange) et [!UICONTROL On Demand].

### Ciblage de site

* **[!UICONTROL Traffic Type]** : [!UICONTROL Websites] uniquement
* **[!UICONTROL Site Tier]** : [!UICONTROL All sites]

### Ciblage d’audience

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Pour la prospection d’emplacements, regroupez en un seul emplacement des catégories d’audience similaires et des tailles d’audience similaires. Ensuite, en fonction des performances, effectuez l’une des opérations suivantes :
      * Supprimez les audiences peu performantes des emplacements existants.
      * Déplacez les audiences les plus performantes dans un emplacement distinct afin de mieux contrôler les budgets.
   * Pour le reciblage des emplacements, vous devez idéalement inclure un segment d’audience par emplacement afin de contrôler facilement les offres et le budget.

>[!NOTE]
>
>Vos publicités fonctionnent mieux si un utilisateur ne peut être atteint que par un seul emplacement. Un chevauchement significatif entre les utilisateurs de différents emplacements peut entraîner une concurrence, ce qui entraîne un cycle d’augmentation continue des offres, ce qui augmente le coût par utilisateur. Par conséquent, si vous incluez plusieurs audiences, veillez à ne pas se composer d’utilisateurs/membres d’audience qui se chevauchent.
>
> Vous pouvez éviter le chevauchement d’audiences en créant vos audiences dans des niveaux afin de supprimer les niveaux plus élevés et plus inclusifs des emplacements, si nécessaire.

* **[!UICONTROL Frequency Capping]:**
   * Pour les emplacements de prospection, utilisez des plafonds de fréquence serrés (une impression par jour).
   * Pour le reciblage des emplacements, définissez la limite d’emplacement principal sur 6 à 10 impressions par jour et la limite secondaire sur une impression par heure.

* **[!UICONTROL Device Targeting]** :
   * Incluez [!UICONTROL Computer], [!UICONTROL Mobile] et [!UICONTROL Tablet].
   * Ne ciblez pas [!UICONTROL Firefox] et [!UICONTROL Safari] en raison des limites de ciblage et de mesure. Contactez votre équipe de compte d’Adobe pour plus d’informations sur la prise en charge de [!DNL Adobe] pour [!DNL Safari ITP].
   * Si vous ciblez le trafic web mobile, désactivez tous les navigateurs mobiles sauf [!UICONTROL Chrome] et [!UICONTROL Edge].

### Sécurité des marques et qualité des médias

Le filtrage contextuel, le blocage des fraudes avant offre et/ou le filtrage [!UICONTROL Ads.txt] limitent l’échelle de vos emplacements, mais les utilisent si nécessaire.

## Étape 5 - Utilisation de la bonne Assets créative

* La bonne pratique consiste à inclure autant de tailles d’annonces uniques que possible pour optimiser la portée. Le modèle d’affichage universel vous permet de télécharger n’importe quelle taille d’affichage standard.
* Assurez-vous que tous les emplacements contiennent *au moins* toutes les tailles d’affichage principales (300x250, 728x90, 160x600, 300x600, 320x50 et 300x50).
* Mettez fréquemment à jour les éléments créatifs pour éviter la fatigue créative.

>[!MORELIKETHIS]
>
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Comment DSP optimise vos campagnes](optimization-how-dsp-optimizes-campaigns.md)
>* [Objectifs d’optimisation et comment les utiliser](optimization-goals.md)
>* [Filtres de pré-offre de niveau placement et comment les utiliser](optimization-pre-bid-filters.md)
>* [Liste de contrôle de lancement de campagne](/help/dsp/campaign-management/campaign-launch-checklist.md)
