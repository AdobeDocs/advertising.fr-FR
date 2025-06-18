---
title: Paramètres d’emplacement
description: Voir les descriptions des paramètres d’emplacement disponibles.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 1478e61ebd7dac59cac7566b86e5b1ea97838508
workflow-type: tm+mt
source-wordcount: '4477'
ht-degree: 0%

---

# Paramètres d’emplacement

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Nom de l’emplacement.

>[!TIP]
>Utilisez une convention de nommage adaptée à votre situation. Une convention de nommage suggérée est la suivante : « *\&lt;Nom de la campagne\> : \&lt;Unité publicitaire\> : \&lt;Durée\> : \&lt;Ciblage\>* ».

**[!UICONTROL Status]:** statut de l’emplacement : *[!UICONTROL Active]* (par défaut) ou *[!UICONTROL Paused]*.

>[!TIP]
>La bonne pratique consiste à suspendre l’emplacement jusqu’à ce que vous soyez prêt à le lancer.

**[!UICONTROL Details]:** (Lecture seule) Le type d’annonce applicable, le compte qui crée l’emplacement et la campagne parente. Pour afficher plus de détails, cliquez sur **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** ouvre une liste de modèles d&#39;emplacement existants. Pour renseigner automatiquement les paramètres de ciblage à partir d’un modèle :

1. Effectuez l’une des opérations suivantes :

   * Pour réutiliser toutes les cibles d’un modèle, cochez la case en regard du nom du modèle.

   * Pour réutiliser des types de cible individuels à partir d’un modèle, développez le nom du modèle et cochez la case en regard des types de cible à réutiliser.

1. Cliquez sur **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (formats d’annonce vidéo uniquement) Durée et/ou spécifications de l’annonce publicitaire, utilisées pour calculer la projection de la prévision sur la droite. Les champs varient selon le type d’annonce.

**[!UICONTROL Environment]:** (format d’annonce vidéo universel uniquement) Environnements d’appareils (bureau, mobile, télévision connectée) à inclure en tant que cibles dans l’emplacement. Spécifiez au moins un paramètre.

Dans les rapports personnalisés, la dimension au niveau de l’emplacement « Environnement de l’appareil » indique l’environnement ciblé.

**[!UICONTROL Placement tags]:** (facultatif) Mots-clés ou surnoms pour vous aider à localiser cet emplacement.

## Objectifs

**[!UICONTROL Package]:** (facultatif) Package auquel l’emplacement est affecté. Cliquez sur ![Modifier](/help/dsp/assets/edit.png) pour sélectionner un package existant ou créer un package. Lorsque vous affectez l&#39;emplacement à un package, la section [!UICONTROL Goals] est mise à jour avec les dates de vol, l&#39;objectif de diffusion et le budget du package.

**[!UICONTROL Flight Dates]:** date de début et date de fin de l’emplacement. Les publicités approuvées peuvent être exécutées pendant le vol lorsque l’emplacement est actif et affecté à un package ou une campagne actif.

Les dates du package (le cas échéant) ou de la campagne sont automatiquement renseignées par défaut.

>[!NOTE]
>
>* Les dates de vol doivent être incluses dans les dates de vol de la campagne et les dates de vol du package.

### Emplacements affectés à des packages avec fréquence au niveau du package

**[!UICONTROL Placement Funding]:** Comment budgéter l&#39;emplacement :

* *[!UICONTROL Optimize based on performance]:* contrôle le budget au niveau du package.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* permet de définir un budget d’emplacement minimal et/ou maximal. Spécifiez au moins un type de budget :

   * *[!UICONTROL Maximum Budget]* : saisissez une valeur et la durée (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]* : budget minimum en pourcentage du budget du package. Lorsqu&#39;une limite d&#39;intervalle est spécifiée, la valeur du budget minimum est toujours calculée en tant que pourcentage de la limite d&#39;intervalle. Sinon, c&#39;est calculé en pourcentage du budget de l&#39;ensemble.

**[!UICONTROL Max Bid]:** Le maximum à payer pour 1000 impressions.

**[!UICONTROL Placement Pre-bid Filters]:** jusqu’à cinq seuils d’indicateurs clés de performance (tels qu’une mesure de visibilité minimale ou un taux de clic publicitaire) qui doivent être atteints pour que les enchères se produisent. Vous pouvez utiliser des filtres de pré-enchères comme tactiques d’optimisation, mais sachez que chaque règle peut limiter les opportunités pour cet emplacement de soumettre des enchères. Pour ajouter ou modifier des filtres :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour ajouter un filtre :
      1. Cliquez sur **[!UICONTROL Add Filter]**.
      1. En regard de **[!UICONTROL Only bid if]**, sélectionnez une mesure, puis saisissez une valeur.
   * Pour supprimer un filtre, cliquez sur **[!UICONTROL X]** dans la ligne de filtre.
1. Cliquez sur **[!UICONTROL Save]**.

Consultez les descriptions de chaque filtre de pré-enchères à la rubrique [ Filtres de pré-enchères au niveau du positionnement et utilisation ](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Tous les autres emplacements

**[!UICONTROL Budget Goal]:** plafond budgétaire brut et intervalle budgétaire (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Emplacements dans des campagnes avec gestion des marges uniquement) Limite budgétaire brute et intervalle budgétaire (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** objectif d’optimisation du package. Consultez les descriptions de chaque objectif d’optimisation dans « [ Objectifs d’optimisation et comment les utiliser ](/help/dsp/optimization/optimization-goals.md) ».

**[!UICONTROL Target Goal]:** objectif cible, qui est utilisé pour effectuer le suivi des performances.

>[!NOTE]
>
>Ce champ n’est qu’un repère et n’est pas utilisé pour la prise de décision.

**[!UICONTROL Pace on]:** Base de la fréquence :

* **[!UICONTROL Budget goal]:** (par défaut) Cette option génère autant d’impressions que possible dans le budget alloué.

* **[!UICONTROL Impressions]:** cette option génère des impressions jusqu’à ce qu’une quantité spécifiée soit atteinte dans un intervalle spécifié. Lorsque vous sélectionnez cette option, indiquez le nombre d’impressions et l’intervalle : *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Le maximum à payer pour 1000 impressions.

**[!UICONTROL Flight pacing]:** (emplacements avec fréquence au niveau de l’emplacement uniquement) Comment fréquence de la diffusion publicitaire :

* *[!UICONTROL Even]:* (valeur par défaut) Place la diffusion de manière uniforme tout au long de chaque vol, avec un objectif de 50 % de la diffusion au cours de la première moitié du vol.

* *[!UICONTROL Slightly Ahead]:* (valeur par défaut) Accélère la diffusion afin qu’elle soit achevée à 55-65 % au milieu de la durée du vol.

* *[!UICONTROL Frontload]:* Accélère la livraison de sorte qu&#39;elle soit terminée à 65-75% au milieu du vol.

* *[!UICONTROL Aggressive Frontload]:* Accélère la livraison afin qu&#39;elle soit terminée à 75-85% au milieu du vol.

**[!UICONTROL Intraday pacing]:** (emplacements avec fréquence au niveau de l’emplacement uniquement) Comment fréquence de diffusion de l’annonce publicitaire sur chaque jour du vol :

* *[!UICONTROL Even]:* (valeur par défaut) met la diffusion à l’échelle en fonction de la disponibilité du stock. Généralement, plus de publicités sont diffusées par heure pendant la journée, lorsque le volume des enchères est plus élevé, et moins de publicités sont diffusées le matin et le soir.

* *[!UICONTROL ASAP]:* (valeur par défaut) accélère la diffusion à une vitesse deux fois supérieure à *pair*.

  >[!CAUTION]
  >
  >Cette option peut avoir une incidence négative sur les performances. Utilisez-le uniquement lorsque vous donnez entièrement la priorité à la diffusion et aux dépenses plutôt qu’à l’optimisation des performances.

**[!UICONTROL Placement Pre-bid Filters]:** (facultatif) Jusqu’à cinq filtres qui doivent être respectés pour que l’enchère se produise. Vous pouvez utiliser des filtres de pré-enchères comme tactiques d’optimisation, mais gardez à l’esprit que chaque règle peut limiter les opportunités sur lesquelles cet emplacement peut enchérir. Pour ajouter ou modifier des filtres :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour ajouter un filtre :
      1. Cliquez sur **[!UICONTROL Add Filter]**.
      1. En regard de **[!UICONTROL Only bid if]**, sélectionnez une mesure, puis saisissez une valeur.
   * Pour supprimer un filtre, cliquez sur **[!UICONTROL X]** dans la ligne de filtre.
1. Cliquez sur **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (facultatif) Emplacements spécifiques dans lesquels inclure ou exclure des annonces dans l’emplacement. Si vous ne spécifiez aucun emplacement, tous les emplacements sont ciblés.

>[!NOTE]
>
>Les emplacements de ville et de DMA ne sont pas disponibles pour les emplacements Roku.

Pour spécifier des emplacements :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour inclure ou exclure un pays, un État, une ville, une DMA, un district législatif fédéral ou un district législatif d’État :
      1. Sélectionnez le type d’emplacement dans la colonne de gauche.
      1. (Si nécessaire) Cliquez sur un emplacement pour le développer.
      1. En regard de l’emplacement, cliquez sur *[!UICONTROL Include]* pour l’inclure en tant que cible ou *[!UICONTROL Exclude]* pour l’exclure en tant que cible.
   * Pour rechercher un code postal et inclure ou exclure tous les résultats sélectionnés :
      1. Cliquez sur **[!UICONTROL Search Postal Code]**.
      1. Sélectionnez le pays.
      1. Saisissez le nom de la ville, puis cliquez sur ![Modifier](/help/dsp/assets/search.png).
      1. Cliquez sur le résultat de recherche approprié.
      1. Cliquez sur *[!UICONTROL Include All]* pour inclure tous les emplacements en tant que cibles ou sur *[!UICONTROL Exclude All]* pour exclure tous les emplacements en tant que cibles.
   * Pour saisir ou coller des codes postaux et les inclure ou les exclure tous :
      1. Cliquez sur **[!UICONTROL Paste Postal Code]**.
      1. Sélectionnez le pays.
      1. Saisissez ou collez jusqu’à 1 000 codes postaux.
Incluez un code postal par ligne ou saisissez plusieurs valeurs séparées par des virgules ou des tabulations.
      1. Cliquez sur *[!UICONTROL Include All]* pour inclure tous les emplacements en tant que cibles ou sur *[!UICONTROL Exclude All]* pour exclure tous les emplacements en tant que cibles.
   * Pour supprimer un emplacement de la liste [!UICONTROL Included] ou [!UICONTROL Excluded], cliquez sur **[!UICONTROL X]** en regard de l’emplacement dans la colonne de droite.
1. Cliquez sur **[!UICONTROL Done]**.

>[!NOTE]
>
>* Tous les pays ne disposent pas d’un État, d’une ville ou d’un code postal.
>* DMA (zone de marché désignée), Districts législatifs fédéraux et Districts législatifs des États sont disponibles uniquement pour les emplacements aux États-Unis.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Sources d&#39;inventaire à inclure ou à exclure en tant que cibles. Pour la plupart des types d&#39;emplacement, tous les types de stock et toutes les origines pour chaque type sont inclus par défaut. Pour les emplacements [!DNL Roku], vous devez spécifier le type de stock et les origines. Vous pouvez choisir parmi les types d&#39;inventaire suivants :

* [!UICONTROL Public] : (tous les types d’emplacement, à l’exception de Roku) tous les stocks Exchange ouverts auxquels DSP a accès. Vous pouvez inclure et exclure l’inventaire public.

  Vous pouvez afficher la liste par source ou par flux. Lorsque vous affichez la liste par flux, vous pouvez effectuer une recherche par nom de flux, clé de flux ou balise de caractéristique sélectionnée.

* [!UICONTROL Private] | [!UICONTROL Roku Private] : les offres privées que vous avez conclues (ou les offres de [!DNL Roku] privées existantes pour les emplacements [!DNL Roku]) avec les éditeurs que vous avez configurés dans DSP, ainsi que vos listes d’offres privées [ existantes](/help/dsp/inventory/lists-deals-manage.md). Vous pouvez inclure, mais pas exclure, les stocks publics.

  Dans l’onglet [!UICONTROL Deals] , vous pouvez rechercher la liste par mot-clé, clé, ID d’offre ou balise personnalisée. Dans l&#39;onglet [!UICONTROL Deal Lists], vous pouvez rechercher la liste par nom ou ID de liste d&#39;offres.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]* : (Facultatif) remplace l&#39;algorithme des prix offerts pour proposer au moins les prix fixes et les prix plancher pour les opérations.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand] : tous les [stocks de [!UICONTROL On Demand] premium non garantis](/help/dsp/inventory/on-demand-inventory-about.md) (ou [!UICONTROL On Demand] offres [!DNL Roku] pour les emplacements [!DNL Roku]) auxquels vous êtes abonné en [!DNL DSP]. Vous pouvez inclure et exclure le stock [!UICONTROL On Demand].

  Vous pouvez afficher la liste par source ou par flux. Lorsque vous affichez la liste par flux, vous pouvez effectuer une recherche par nom de flux, clé de flux ou région de l’éditeur, balise de catégorie ou balise de caractéristique sélectionnée.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]* : (Facultatif) remplace l&#39;algorithme des prix offerts pour proposer au moins les prix fixes et les prix plancher pour les opérations.

Pour définir le ciblage de l&#39;inventaire :

* Pour exclure un type d&#39;inventaire, décochez la case en regard du nom.
* Pour cibler un type de stock :
   1. Cochez la case en regard du nom du type d’inventaire.
   1. (Facultatif) Modifiez les sources pour inclure :
      1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] et inventaire [!UICONTROL On Demand]) Cliquez sur **[!UICONTROL View by Source]** ou **[!UICONTROL View by Feed]** pour modifier la façon dont les sources sont répertoriées.
      1. (Le cas échéant) Filtrez l’inventaire selon les besoins.
      1. Spécifiez les sources à inclure et à exclure :
         * Pour l&#39;inventaire des [!UICONTROL Public] ou des [!UICONTROL On Demand] :
            * Pour inclure une source, cliquez sur **[!UICONTROL Include]** en regard du nom de la source.
            * Pour exclure une source, cliquez sur **[!UICONTROL Exclude]** en regard du nom de la source.
         * Pour [!UICONTROL Private] inventaire :
            * Dans l’onglet [!UICONTROL Deals] :
               * Pour inclure tous les stocks dans une offre, cliquez sur **[!UICONTROL Include all]** en regard du nom de l’offre.
               * Pour inclure une origine de stock individuelle, développez le nom de l&#39;opération, puis cochez la case en regard du nom de l&#39;origine.
            * Dans l’onglet [!UICONTROL Deal Lists] , cochez la case en regard du nom de la liste des offres.
   1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage à l’emplacement des téléchargements de votre navigateur, cliquez sur **[!UICONTROL Export]**.
   1. Cliquez sur **[!UICONTROL Save]**.

>[!TIP]
>
>Si vous vous êtes abonné à [!UICONTROL On Demand] inventaire mais que vous ne parvenez pas à localiser les éditeurs ou les offres à cibler, vérifiez le statut des offres. Pour plus d’informations sur les statuts, voir [À propos [!DNL On Demand] de l’inventaire Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Video targeting]:** cibler (sans exclure) l’inventaire par attributs d’inventaire. Lorsque vous ciblez plusieurs valeurs pour le même attribut vidéo, n’importe lequel des attributs sélectionnés peut être ciblé (par exemple, \[Taille du lecteur = grande OU Taille du lecteur = HD\]). Lorsque vous ciblez plusieurs attributs, chacun des attributs spécifiés doit être présent (par exemple, \[Durée = 30-60 min] ET \[Taille du lecteur = grand OU Taille du lecteur = HD\]).

* **[!UICONTROL Player size]:** Inventaire de Target (sans exclure) par taille de lecteur. Le paramètre s’applique aux emplacements de prévisualisation, aux emplacements de prévisualisation standard mobiles et aux emplacements vidéo universels pour les environnements de bureau et mobiles. Par défaut, toutes les tailles sont ciblées. Pour réduire les cibles, sélectionnez des tailles de cible spécifiques et/ou *Inconnu*.

* **[!UICONTROL Playback mode]:** inventaire de la cible (sans l’exclure) en fonction du mode de lancement de la lecture. Le paramètre s’applique aux emplacements de prévisualisation, aux emplacements de prévisualisation standard mobiles et aux emplacements vidéo universels pour les environnements de bureau et mobiles. Par défaut, tous les modes sont ciblés. Pour réduire les cibles, sélectionnez des modes de cible spécifiques et/ou *Inconnu*.

* **[!UICONTROL Skippability]:** cible (sans l’exclure) l’inventaire, qu’il puisse être ignoré ou non. Le paramètre s’applique à tous les emplacements VAST/PAYANT, y compris les emplacements preroll, mobile standard preroll, TV connectée et vidéo universelle. Par défaut, toutes les options sont ciblées. Pour réduire les cibles, sélectionnez des cibles spécifiques et/ou *Inconnu*.

**[!UICONTROL Position targeting]:** cibler (mais pas exclure) l’inventaire par position publicitaire. Le paramètre s’applique à tous les emplacements VAST/PAYANT, y compris les emplacements preroll, mobile standard preroll, TV connectée et vidéo universelle. Par défaut, tous les postes sont ciblés. Pour réduire les cibles, sélectionnez des positions cibles spécifiques et/ou *Inconnu*.

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** types de trafic à cibler. Les options incluent **[!UICONTROL Websites]** et **[!UICONTROL Apps]**.

**[!UICONTROL Tier]:** (disponible lorsque **[!UICONTROL Paste list of targeted sites]** est *[!UICONTROL Off]*) Qualité du trafic à cibler. Les niveaux 1 à 3 sont tous sûrs et ont été approuvés par l’équipe de mappage de DSP.

* *[!UICONTROL Tier 1]:* Sites et applications Premium reconnus au niveau national.

* *[!UICONTROL Tier 2]:* cible le niveau 1 ainsi que les sites de qualité et les applications moins connus que le niveau 1.

* *[!UICONTROL Tier 3]:* cible les niveaux 1 à 2 ainsi que les sites et applications légitimes et sécurisés par la marque qui s’adressent à une audience de niche. Utilisez le niveau 3 pour les achats de ciblage de portée ou de données.

* *[!UICONTROL All Sites or Apps]:* cible les niveaux 1 à 3 et le nouvel inventaire qui n’a pas été filtré ou catégorisé, que vous pouvez utiliser pour la portée.

>[!NOTE]
>
>L’inventaire est spécifique aux unités publicitaires de l’emplacement.

>[!TIP]
>
>Pour les campagnes de performances, il est recommandé de sélectionner *[!UICONTROL All Sites]*.

**[!UICONTROL Site or App Categories]:** (facultatif ; disponible lorsque **[!UICONTROL Paste list of targeted sites]** est *[!UICONTROL Off]*) Catégories de sites au niveau du site sélectionné à inclure ou à exclure (mais pas les deux) en tant que cibles. Choisissez parmi les listes de sites verticales que DSP a mappées en fonction de l’objet :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Spécifiez les catégories de site à inclure ou à exclure :
   * Pour inclure des catégories de site :
      1. Cliquez sur **[!UICONTROL Include categories]**.
      1. Cochez la case en regard de chaque catégorie à cibler.
   * Pour exclure des catégories de site :
      1. Cliquez sur **[!UICONTROL Exclude categories]**.
      1. Cochez la case en regard de chaque catégorie à exclure.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage à l’emplacement des téléchargements de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (facultatif ; disponible lorsque **[!UICONTROL Paste list of targeted sites]** est *[!UICONTROL Off]*) Sites/applications et [listes d’URL](/help/dsp/resources/lists-url-manage.md) à exclure. Dans l’onglet [!UICONTROL Paste URL] , vous pouvez rechercher et sélectionner des sites, ou saisir ou coller des noms de domaine. Dans l’onglet [!UICONTROL URL Lists] , vous pouvez sélectionner des listes d’URL.

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Spécifiez les sites :
   * Dans l’onglet [!UICONTROL Paste URL] :
      * Pour rechercher un site :
         1. Cliquez sur **[!UICONTROL Search]**.
         1. Saisissez un mot-clé, sélectionnez un niveau de site et/ou sélectionnez une catégorie de site.
         1. Dans les résultats de la recherche, sélectionnez les sites à exclure :
            * Pour exclure un site individuel, cochez la case adjacente.
            * (Lorsque plus de 50 résultats sont disponibles) Pour exclure les 50 premiers résultats, cliquez sur **[!UICONTROL Exclude these 50]**. Pour exclure tous les résultats de la recherche, cliquez sur **[!UICONTROL Exclude these \<*NN *\>]**.
      * Pour saisir des noms de domaine :
         1. Cliquez sur **[!UICONTROL Paste]**.
         1. Entrez un ou plusieurs noms de domaine sur des lignes distinctes.
         1. Cliquez sur **[!UICONTROL Exclude All]**.
   * Dans l’onglet [!UICONTROL URL Lists] :
      1. (Facultatif) Recherchez une liste d’URL en saisissant tout ou partie du nom de la liste dans le champ de recherche.
      1. Cochez la case en regard de chaque liste d’URL à exclure.
1. Cliquez sur **[!UICONTROL Done]** lorsque vous avez terminé.

>[!NOTE]
>
>* Les listes de sites bloqués au niveau du compte et de l’annonceur sont également appliquées, en plus de la [liste des sites bloqués au niveau mondial](/help/dsp/introduction/features/brand-safety-media-quality.md) de DSP, qui inclut les sites considérés comme dangereux pour les publicités.
>* Les listes de sites bloqués remplacent toujours les sites ciblés et les listes de sites. Si un emplacement exclut et inclut la même cible pour une annonce publicitaire, la cible est exclue.

**[!UICONTROL Language]:** (facultatif) Une seule langue à cibler.

**[!UICONTROL Site or app list preview]:** (Lecture seule) Tous les sites/applications ciblés et bloqués pour l’emplacement, y compris les sites/applications au niveau du compte, au niveau de l’annonceur et les listes globales de sites bloqués de DSP.

Vous pouvez éventuellement exporter la liste des sites ciblés et bloqués dans un fichier de valeurs séparées par des virgules (CSV). Pour exporter la liste, cliquez sur **[!UICONTROL Export full site list]**, puis ouvrez ou enregistrez le fichier conformément à la procédure normale de votre navigateur.

**[!UICONTROL Allow unscreened sites]:** (emplacements d’affichage standard uniquement) Active la diffusion d’annonces sur des sites non audités. Lorsque l’emplacement cible un inventaire privé, cette option peut diffuser des annonces sur les sites bloqués.

**[!UICONTROL Paste list of targeted sites]:** vous permet de cibler des sites spécifiques uniquement. Lorsque vous activez cette option, les autres options de ciblage de site sont désactivées.

**[!UICONTROL Sites or Apps]:** (disponible lorsque **[!UICONTROL Paste list of targeted sites]** est *[!UICONTROL On]*) Sites à cibler. Dans l’onglet [!UICONTROL Paste URL] , vous pouvez rechercher et sélectionner des sites, ou saisir ou coller des noms de domaine. Dans l’onglet [!UICONTROL URL Lists] , vous pouvez sélectionner des listes d’URL.

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Spécifiez les sites :
   * Dans l’onglet [!UICONTROL Paste URL] :
      * Pour rechercher un site :
         1. Cliquez sur **[!UICONTROL Search]**.
         1. Saisissez un mot-clé, sélectionnez un niveau de site et/ou sélectionnez une catégorie de site.
         1. Dans les résultats de la recherche, sélectionnez les sites à inclure :
            * Pour inclure un site individuel, cochez la case adjacente.
            * (Lorsque plus de 50 résultats sont disponibles) Pour inclure les 50 premiers résultats, cliquez sur **[!UICONTROL Include these 50]**. Pour inclure tous les résultats de la recherche, cliquez sur **[!UICONTROL Include these \<*NN *\>]**.
      * Pour saisir des noms de domaine :
         1. Cliquez sur **[!UICONTROL Paste]**.
         1. Entrez un ou plusieurs noms de domaine sur des lignes distinctes.
         1. Cliquez sur **[!UICONTROL Include All]**.
   * Dans l’onglet [!UICONTROL URL Lists] :
      1. (Facultatif) Recherchez une liste d’URL en saisissant tout ou partie du nom de la liste dans le champ de recherche.
      1. Cochez la case en regard de chaque liste d’URL à inclure.
1. Cliquez sur **[!UICONTROL Done]** lorsque vous avez terminé.

>[!NOTE]
>
>* Les listes de sites bloqués au niveau du compte et de l’annonceur sont également appliquées, en plus de la [liste des sites bloqués au niveau mondial](/help/dsp/introduction/features/brand-safety-media-quality.md) de DSP, qui inclut les sites considérés comme dangereux pour les publicités.
>* Les listes de sites bloqués remplacent toujours les sites ciblés et les listes de sites. Si un emplacement exclut et inclut la même cible pour une annonce publicitaire, la cible est exclue. Vous pouvez rechercher et sélectionner des sites ou saisir ou coller des noms de domaine :

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** toute cible d’audience pour l’emplacement, y compris les [segments tiers, segments propriétaires, segments Adobe, segments personnalisés et audiences enregistrées](/help/dsp/audiences/audience-settings.md). La taille totale et active de l’audience dédupliquée sur tous les segments sélectionnés et les audiences enregistrées s’affiche également. Vous pouvez sélectionner une audience existante, créer une audience que vous pourrez réutiliser ultérieurement ou sélectionner des segments d’audience spécifiques :

* Pour sélectionner une audience existante, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Included Audiences], puis sélectionnez l’audience.
* Pour créer une audience, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Included Audiences], puis sélectionnez **[!UICONTROL + Create Audience]**. Pour obtenir des instructions, voir [Création d’une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md), en commençant par l’étape 3.
* Pour sélectionner des segments d’audience spécifiques, cliquez sur **[!UICONTROL Select segments for this placement only]**. Sélectionnez la logique du segment. Pour obtenir des instructions, reportez-vous à l’étape 6 de la section « [ Création d’une audience réutilisable ](/help/dsp/audiences/reusable-audience-create.md) ». Lorsque vous avez terminé, cliquez sur **Enregistrer**.

**[!UICONTROL Excluded Audiences]:** toutes les audiences à exclure de l&#39;emplacement, y compris les audiences avec des [segments tiers, segments propriétaires, segments Adobe, segments personnalisés et audiences enregistrées](/help/dsp/audiences/audience-settings.md). La taille totale et active de l’audience dédupliquée pour toutes les audiences exclues s’affiche également. Vous pouvez sélectionner une audience existante ou en créer une nouvelle que vous pourrez réutiliser ultérieurement :

* Pour sélectionner une audience existante, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Excluded Audiences], puis sélectionnez l’audience.

* Pour créer une audience, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Excluded Audiences], puis sélectionnez **+ Créer une audience**. Pour obtenir des instructions, voir [Création d’une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md), en commençant par l’étape 3.

**[!UICONTROL Targeting]:** types d’ID utilisateur à cibler. Vous ne pouvez pas modifier ce paramètre après la mise en ligne de l’emplacement (c’est-à-dire après le début du vol).

Lorsque vous sélectionnez à la fois des identifiants hérités et universels, la préférence d’enchères est donnée aux identifiants universels.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]* : (valeur par défaut) cible les utilisateurs en fonction de leurs cookies, identifiants de publicité mobile ou identifiants de télévision connectée (CTV). Les identifiants sont sélectionnés en fonction de l’inventaire du navigateur, in-app ou CTV.

* *[!UICONTROL Universal ID Beta]* : cible les identifiants axés sur la confidentialité des utilisateurs et utilisatrices ; sélectionnez un type d’identifiant. Les options disponibles sont déterminées par les cibles géographiques sélectionnées dans la section [!UICONTROL Geo-Targeting]. Utilisez avec les [[!DNL RampID] segments importés directement dans DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [segments pour lesquels DSP convertit vos informations d’identification personnelles en identifiants universels](/help/dsp/audiences/sources/source-about.md) ou [segments personnalisés qui effectuent le suivi des identifiants universels](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]* : cible [!DNL ID5] identifiants créés de manière probabiliste à partir d’adresses e-mail et d’autres signaux.Les identifiants <!-- What countries/geos are these available for? Everywhere?--> ID5 sont disponibles sans frais. **Remarque :** les segments tiers provenant de l’[!DNL Eyeota] peuvent inclure des ID5.

   * *[!UICONTROL RampID]* : cible [!DNL LiveRamp] [!DNL RampIDs] d’utilisateurs connectés à votre site à l’aide de leur adresse e-mail.<!-- Verify --> [!DNL RampIDs] sont disponibles pour les utilisateurs en Amérique du Nord, en Australie et en Nouvelle-Zélande.

   * *[!UICONTROL Unified ID2.0]* : cible [!DNL Unified ID2.0] identifiants (UID2) des utilisateurs connectés à votre site à l’aide de leurs adresses e-mail.<!-- Verify -->[!DNL UID2 IDs] ne sont pas disponibles pour les utilisateurs dans l&#39;Espace économique européen et dans certains autres pays. Voir la [liste des pays interdits](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]** : termes de l’accord de service pour l’utilisation des identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les conditions une seule fois avant de pouvoir convertir des données en un nouveau type d’identifiant. Pour les clients qui disposent de contrats de service géré, l’équipe chargée de votre compte Adobe obtiendra votre consentement et acceptera les conditions au nom de votre entreprise. Pour lire les termes, cliquez sur **>**. Pour accepter les conditions, faites défiler l’écran jusqu’au bas des conditions et cliquez sur **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (disponible lorsque la campagne [campaign est configurée pour le ciblage inter-appareils basé sur les personnes](/help/dsp/campaign-management/campaigns/campaign-settings.md), vous ciblez uniquement les identifiants hérités (et non les identifiants universels) et vous sélectionnez au moins un segment ou une audience. Vous permet d’étendre votre ciblage sur tous les appareils connus d’une personne (selon le graphique d’appareil spécifié dans les paramètres de campagne), même les appareils qui ne figurent pas dans les segments spécifiés. Des frais peuvent s’appliquer en fonction du graphique spécifié pour la campagne. Les données des graphiques des appareils ne sont disponibles qu’en Amérique du Nord.

**[!UICONTROL Placement Cap]:** (facultatif) Le nombre de fois qu’un appareil, un ID universel ou une personne unique (selon le [!UICONTROL Cross Device Level] spécifié pour la campagne et le paramètre de [!UICONTROL Targeting] de l’emplacement) peut recevoir des annonces publicitaires à partir de l’emplacement. Les options incluent le *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
> Vous pouvez définir des limites de fréquence au niveau de la campagne, du package et de l’emplacement. DSP respecte la limite de fréquence la plus stricte dans la hiérarchie de la campagne.

**[!UICONTROL Secondary Cap]:** (facultatif ; disponible lorsque vous incluez une [!UICONTROL Placement Cap] numérique) Limitation supplémentaire dans les limites de la limite d’emplacement principale. Sélectionnez le nombre d’impressions et la période (3 par 12 heures, par exemple).

**[!UICONTROL Day Parting]:** (facultatif) Jours spécifiques de la semaine et heure d’exécution des publicités. Pour définir des intervalles de répartition :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Sélectionnez le fuseau horaire applicable.
1. Spécifiez les intervalles :
   * Pour sélectionner un intervalle prédéfini, cliquez sur l’un des boutons d’intervalle. Les options incluent *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* ou *[!UICONTROL Prime]* (primetime).
   * Pour sélectionner manuellement un intervalle, cliquez dans une cellule et éventuellement faites glisser pour sélectionner l’intervalle.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (facultatif ; disponible pour les annonceurs configurés avec des segments [!DNL Proximic by Comscore]) Noms ou identifiants de segment spécifiques de [!DNL Proximic by Comscore] à inclure en tant que cibles. Des frais supplémentaires peuvent s’appliquer pour cette fonctionnalité. Pour activer cette fonctionnalité et configurer des segments de rubrique, contactez l’équipe chargée de votre compte Adobe.

Pour spécifier le ciblage de rubrique :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Spécifiez les segments à cibler :
   1. Dans la colonne de gauche, sélectionnez le partenaire : (*[!UICONTROL Comscore]*.
   1. Dans le champ de saisie, saisissez les noms ou les identifiants de segment.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de la rubrique à l’emplacement des téléchargements de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

>[!TIP]
>
>* Le ciblage de rubrique limite l’inventaire sur lequel l’emplacement peut enchérir. Utilisez donc le ciblage de rubrique uniquement pour un petit pourcentage de votre achat global.
>
>* Configurez tout ciblage négatif dans le segment sur [!DNL Proximic by Comscore].

**[!UICONTROL Device Targeting]:** (facultatif) Informations spécifiques sur les appareils, notamment les types d’appareils, les fabricants, les systèmes d’exploitation, les navigateurs et les types de connectivité, à inclure et à exclure en tant que cibles. Les types varient selon le type d’emplacement. Pour spécifier le ciblage de l’appareil :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Spécifiez les détails de l’appareil à inclure et à exclure :
   1. Dans la colonne de gauche, sélectionnez la catégorie.
   1. Spécifiez le ciblage :
      * Pour inclure une valeur, cliquez sur **[!UICONTROL Include]** en regard du nom de la valeur.
      * Pour exclure une valeur, cliquez sur **[!UICONTROL Exclude]** en regard du nom de la valeur.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage de l’appareil à l’emplacement des téléchargements de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (facultatif) Fournisseurs de services Internet (FAI) spécifiques à inclure ou exclure (mais pas les deux) en tant que cibles. Pour spécifier le ciblage du FAI :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Spécifiez les FAI à inclure ou à exclure :
   * Pour inclure les FAI :
      1. Cliquez sur **[!UICONTROL Include ISPs]**.
      1. (Facultatif) Filtrez la liste par mot-clé.
      1. Cochez la case en regard de chaque FAI à cibler.
   * Pour exclure les FAI :
      1. Cliquez sur **[!UICONTROL Exclude ISPs]**.
      1. (Facultatif) Filtrez la liste par mot-clé.
      1. Cochez la case en regard de chaque FAI à exclure.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage du FAI à l’emplacement des téléchargements de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (facultatif ; clients [!DNL DoubleVerify] uniquement ; disponible pour les emplacements de bureau pré-roll, standard et d’affichage par clic, ainsi que pour les emplacements d’affichage et de vidéo natifs uniquement ; non pris en charge pour [emplacements programmatiques garantis par défaut pour les offres](/help/dsp/inventory/programmatic-guaranteed-about.md)) Un identifiant de segment [!DNL DoubleVerify Authentic Brand Safety] associé au compte [!DNL DoubleVerify] de l’entreprise à utiliser pour l’emplacement. La spécification d’un ID bloque les impressions après l’enchère à l’aide des règles de sécurité de marque personnalisées configurées pour l’ID de segment spécifié. DSP facture votre compte pour l’utilisation de l’identifiant de segment.

L’identifiant doit commencer par « 51 » et se composer de huit chiffres. Par défaut, si un identifiant de segment est spécifié dans les paramètres du compte de l’annonceur, l’identifiant au niveau de l’annonceur est saisi, mais vous pouvez modifier l’identifiant pour utiliser un autre segment ou le supprimer pour désactiver la fonction.

**[!UICONTROL Contextual filtering]:** (applicable aux publicités pour appareils de bureau, mobiles et natives) Types de filtres contextuels [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39] à appliquer. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour les nouveaux emplacements, mais vous pouvez modifier les paramètres :

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify] :

   * **[!UICONTROL Block sites that are]:** (facultatif) Un ou plusieurs types de contexte d&#39;inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Peer 39] :

   * **Sites cibles qui sont :** (facultatif) Un ou plusieurs types d’attributs d’inventaire à cibler par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL ComScore] :

   * **Bloquer les sites qui sont :** (facultatif) Un ou plusieurs types d’attributs d’inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (facultatif) Degré de contenu pour adultes pour lequel les annonces doivent être bloquées par défaut : *[!UICONTROL Do Not Block]* (par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

   * **[!UICONTROL Alcohol Content]:** (facultatif) Degré de teneur en alcool pour lequel bloquer les publicités par défaut : *[!UICONTROL Do Not Block]* (par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Pre-bid fraud blocking]:** Types de sites à bloquer en fonction du trafic frauduleux et des activités suspectes mesurées par [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39]. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour les nouveaux emplacements, mais vous pouvez modifier les paramètres :

* [!UICONTROL DoubleVerify] : (applicable aux publicités pour ordinateurs de bureau et écrans web mobiles, aux publicités natives, aux vidéos et aux publicités TV connectées standard)

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Par défaut, bloque tout le trafic 100 % non valide, y compris le trafic sur les appareils détournés, pour les nouveaux emplacements. Des frais supplémentaires peuvent s’appliquer.

   * **[!UICONTROL Also block sites with]:** (facultatif) niveau supplémentaire de fraude et de trafic non valide qui entraîne le blocage des publicités par défaut par DSP : *[!UICONTROL None]* (la valeur par défaut, qui ne bloque pas le trafic supplémentaire), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Peer 39] : (applicable aux publicités pour ordinateurs de bureau et pour appareils mobiles, natives et vidéo)

   * **[!UICONTROL Block sites that are]:** (facultatif) Un ou plusieurs types de fraude qui entraînent le blocage des publicités par défaut par DSP : *[!UICONTROL Fraud]* (qui bloque tous les sites comportant une fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* et/ou *[!UICONTROL Fraud: Zero Ads]*. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Integral Ad Science] : (applicable aux publicités pour ordinateurs de bureau et pour appareils mobiles, natives et vidéo)

   * **[!UICONTROL Block sites that are]:** (facultatif) Type d’activité suspecte de site web ou d’application qui entraîne le blocage des annonces par défaut par DSP : *[!UICONTROL None]* (valeur par défaut, qui ne bloque pas les annonces en raison d’une activité suspecte), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Pre-bid viewability]:** (applicable pour les publicités pour appareils de bureau et web mobiles, natives et vidéo) qui filtrent la visibilité avant enchères par [!DNL DoubleVerify] et [!DNL Integral Ad Science] à appliquer pour l’emplacement. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour les nouveaux emplacements, mais vous pouvez modifier les paramètres. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Ads.txt filtering]:** (applicable aux publicités pour appareils de bureau et mobiles, aux publicités natives, vidéo et audio) Quel niveau de filtrage des [publicités.txt](https://iabtechlab.com/ads-txt-about/) de pré-enchères utiliser en appliquant la liste de vendeurs numériques autorisés de chaque éditeur. La valeur par défaut au niveau de l’annonceur est sélectionnée pour les nouveaux emplacements, mais vous pouvez modifier les paramètres :

* *[!UICONTROL Opt out of ads.txt (default)]* : Pour acheter des stocks auprès de tous les vendeurs.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]* : pour donner la priorité à l’achat de stocks auprès des vendeurs directs et des revendeurs autorisés d’un domaine.
* *[!UICONTROL Ads.txt sellers only]* : Pour acheter des stocks uniquement auprès des vendeurs directs et des revendeurs autorisés d&#39;un domaine.
* *[!UICONTROL Ads.txt sellers only]* : Pour acheter des stocks uniquement auprès des vendeurs directs autorisés d&#39;un domaine.

**[!UICONTROL Attention Targeting]:** (applicable aux publicités pour ordinateurs de bureau et appareils mobiles, aux vidéos et aux publicités TV connectées standard) Cible [!DNL Adelaide] segments de pré-enchères avec un niveau d’attention spécifique (élevé, moyen ou faible) en fonction du site, du format et de la taille de la publicité spécifiés. Les segments sont mis à jour chaque semaine. **Remarque :** l’utilisation de segments [!DNL Adelaide] pour le ciblage engendre des frais CPM pour chaque impression fournie avec le ciblage d’attention [!DNL Adelaide]. Ces frais sont distincts des frais pour la [mesure d’attention](/help/dsp/campaign-management/campaigns/campaign-settings.md). Pour les emplacements interactifs de pré-roll, vous n’êtes facturé que pour les IMPRESSIONS VAST.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>(emplacements [!DNL Roku]) Les fournisseurs de suivi tiers approuvés par [!DNL Roku] comprennent [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], [!DNL Research Now],, et.

**[!UICONTROL Event Pixels]:** (facultatif) pixels de suivi d’événement tiers à joindre par défaut à toutes les nouvelles annonces de l’emplacement. Pour spécifier des pixels d’événement :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour sélectionner un pixel existant, activez la case à cocher dans la ligne de pixel.
   * Pour créer un pixel :
      1. Cliquez sur **[!UICONTROL Create]**.
      1. Saisissez les informations suivantes :
         * **[!UICONTROL Pixel name]:** Nom du pixel ; la longueur maximale est de 500 caractères. Utilisez un nom qui vous permet d’identifier facilement le pixel.
         * **[!UICONTROL Pixel event fires on]:** Événement qui déclenche le déclenchement du pixel. Les événements disponibles varient selon le type d’annonce.
         * **[!UICONTROL Pixel type]:** indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image de 1x1 pixel), un *[!UICONTROL HTML]* ou un *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** URL de l’image en pixels.
      1. Cliquez sur **[!UICONTROL Create and attach]**.
   1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (facultatif) Pixels de suivi des conversions à joindre par défaut à toutes les nouvelles annonces de l’emplacement. Pour définir les pixels de conversion, procédez comme suit :

1. Cliquez sur ![ Modifier ](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour sélectionner un pixel existant, activez la case à cocher dans la ligne de pixel.
   * Pour créer un pixel :
      1. Cliquez sur **[!UICONTROL Create]**.
      1. Saisissez les informations suivantes :
         * **[!UICONTROL Conversion pixel name]:** Nom du pixel ; la longueur maximale est de 500 caractères. Utilisez un nom qui vous permet d’identifier facilement le pixel.
         * **[!UICONTROL Conversion category]:** type de conversion.
         * **[!UICONTROL Impression conversion window]:** nombre de jours après la survenue d’une impression publicitaire dans lequel l’impression peut être attribuée à une conversion. La valeur par défaut est de 30 jours.
         * **[!UICONTROL Click conversion window]:** nombre de jours après un clic publicitaire pendant lesquels le clic peut être attribué à une conversion. La valeur par défaut est de 30 jours.
         * **[!UICONTROL Notes]:** (facultatif) Description ou autres informations relatives au pixel.
      1. Cliquez sur **[!UICONTROL Create and attach]**.
      1. Mettez en œuvre le pixel de conversion sur les pages web appropriées :
         1. Dans le menu principal, accédez à **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Dans la ligne des pixels, cliquez sur **[!UICONTROL edit]**.
         1. Copiez la ou les valeurs dans les champs [!UICONTROL HTML Tag] et [!UICONTROL Flash Tag], si nécessaire, pour les fournir à l’annonceur ou au contact du site web.

            Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé de celui-ci.
   1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (facultatif) Taux de frais tiers statique à suivre en tant que coût non facturable pour 1 000 impressions. La valeur par défaut au niveau du package est automatiquement appliquée aux nouveaux emplacements, le cas échéant, sauf si vous saisissez une valeur différente.

>[!NOTE]
>
>Les frais facturables sont reflétés dans la mesure [!UICONTROL Net CPM].

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Créer un emplacement](placement-create.md)
>* [Modifier les emplacements](placement-edit.md)
>* [Gérer les multiplicateurs d&#39;offres pour les placements](placement-manage-bid-multipliers.md)
>* [Afficher le journal des modifications pour un emplacement](placement-change-log.md)
>* [Raccourcis clavier](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [FAQ sur la gestion de campagnes](/help/dsp/campaign-management/faq-campaign-management.md)
