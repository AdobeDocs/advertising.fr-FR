---
title: Paramètres d’emplacement
description: Voir la description des paramètres d’emplacement disponibles.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: cbefed8dcf59038d57e145d511f2491dd928a788
workflow-type: tm+mt
source-wordcount: '3967'
ht-degree: 0%

---

# Paramètres d’emplacement

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Nom de l’emplacement.

>[!TIP]
>Utilisez une convention d’affectation des noms adaptée à votre situation. L’une des conventions d’affectation de nom suggérée est &quot;*\&lt;Nom de campagne\>: \&lt;Unité publicitaire\>: \&lt;Durée\>: \&lt;Ciblage\>*&quot;.

**[!UICONTROL Status]:** État de l’emplacement : *[!UICONTROL Active]* (valeur par défaut) ou *[!UICONTROL Paused]*.

>[!TIP]
>La bonne pratique consiste à suspendre l’emplacement jusqu’à ce que vous soyez prêt à le lancer.

**[!UICONTROL Details]:** (Lecture seule) type d’annonce applicable, compte qui crée ou a créé l’emplacement et la campagne parente. Pour afficher plus de détails, cliquez sur **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** ouvre une liste de modèles d’emplacement existants. Pour renseigner automatiquement les paramètres de ciblage à partir d’un modèle :

1. Effectuez l’une des opérations suivantes :

   * Pour réutiliser toute la cible depuis un modèle, cochez la case en regard du nom du modèle.

   * Pour réutiliser des types de cible individuels à partir d’un modèle, développez le nom du modèle et cochez la case en regard des types de cible que vous souhaitez réutiliser.

1. Cliquez sur **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Formats de publicité vidéo uniquement) Durée de la publicité et/ou spécifications de la publicité, qui sont utilisées pour calculer la projection de la prévision sur la droite. Les champs varient en fonction du type de publicité.

**[!UICONTROL Environment]:** (format de publicité vidéo universelle uniquement) Environnements de l’appareil (bureau, mobile, télévision connectée) à inclure comme cibles dans l’emplacement. Spécifiez au moins une valeur.

Dans les rapports personnalisés, la dimension &quot;Environnement de périphérique&quot; au niveau de l’emplacement indique l’environnement ciblé.

**[!UICONTROL Placement tags]:** (facultatif) mots-clés ou surnoms pour vous aider à localiser cet emplacement.

## Objectifs

**[!UICONTROL Package]:** (facultatif) package auquel l’emplacement est affecté. Cliquez sur ![Modifier](/help/dsp/assets/edit.png) pour sélectionner un package existant ou créer un package. Lorsque vous attribuez l’emplacement à un package, la section [!UICONTROL Goals] est mise à jour avec les dates de vol, l’objectif de livraison et le budget du package.

**[!UICONTROL Flight Dates]:** Date de début et date de fin de l’emplacement. Les publicités approuvées peuvent être exécutées pendant le vol lorsque l’emplacement est actif et affecté à un package ou à une campagne actif.

Les dates du kit (le cas échéant) ou de la campagne sont renseignées automatiquement par défaut.

>[!NOTE]
>
>* Les dates de vol doivent être incluses dans les dates de vol de l&#39;opération et dans les dates de vol du kit.

### Emplacements affectés aux modules avec un suivi au niveau du module

**[!UICONTROL Placement Funding]:** Comment budgéter l’emplacement :

* *[!UICONTROL Optimize based on performance]:* contrôle le budget au niveau du package.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Permet de définir un budget d’emplacement minimal et/ou maximal. Spécifiez au moins un type de budget :

   * *[!UICONTROL Maximum Budget]* : entrez une valeur et la durée (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]* : budget minimum en pourcentage du budget du package. Lorsqu’un plafond d’intervalle est spécifié, la valeur de budget minimale est toujours calculée en pourcentage du plafond d’intervalle. Sinon, il est calculé sous la forme d&#39;un pourcentage du budget de package.

**[!UICONTROL Max Bid]:** Montant maximum pour payer 1 000 impressions.

**[!UICONTROL Placement Pre-bid Filters]:** Jusqu’à cinq seuils d’indicateurs clés de performance (par exemple, une mesure de visibilité minimale ou un taux de clics) qui doivent être atteints pour que la soumission se produise. Vous pouvez utiliser des filtres avant offre comme tactiques d’optimisation, mais vous devez comprendre que chaque règle peut limiter les opportunités sur lesquelles cet emplacement peut enchérir. Pour ajouter ou modifier des filtres :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour ajouter un filtre :
      1. Cliquez sur **[!UICONTROL Add Filter]**.
      1. En regard de **[!UICONTROL Only bid if]**, sélectionnez une mesure, puis saisissez une valeur.
   * Pour supprimer un filtre, cliquez sur **[!UICONTROL X]** dans la ligne de filtre.
1. Cliquez sur **[!UICONTROL Save]**.

Consultez les descriptions de chaque filtre de pré-offre à l’adresse &quot;[Filtres de pré-offre de niveau emplacement et Comment les utiliser](/help/dsp/optimization/optimization-pre-bid-filters.md)&quot;.

### Tous les autres emplacements

**[!UICONTROL Budget Goal]:** Le budget maximal brut et l’intervalle de budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Emplacements dans des campagnes avec gestion des marges uniquement) Le plafond brut du budget et l’intervalle de budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** objectif d’optimisation du package. Consultez les descriptions de chaque objectif d’optimisation à l’adresse &quot;[Optimization Goals and How to Use Them](/help/dsp/optimization/optimization-goals.md)&quot; (Objectifs d’optimisation et comment les utiliser).

**[!UICONTROL Target Goal]:** L’objectif cible, utilisé pour effectuer le suivi des performances.

>[!NOTE]
>
>Ce champ n’est qu’une référence et n’est pas utilisé pour la prise de décision.

**[!UICONTROL Pace on]:** La base du rythme :

* **[!UICONTROL Budget goal]:** (Par défaut) Cette option diffuse autant d’impressions que possible dans le budget alloué.

* **[!UICONTROL Impressions]:** Cette option permet de délivrer des impressions jusqu’à ce qu’une quantité spécifiée soit atteinte dans un intervalle spécifié. Lorsque vous sélectionnez cette option, spécifiez le nombre d’impressions et l’intervalle : *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Montant maximum pour payer 1 000 impressions.

**[!UICONTROL Flight pacing]:** (Emplacements avec placement au niveau de l’emplacement uniquement) Comment accélérer la diffusion de la publicité :

* *[!UICONTROL Even]:* (valeur par défaut) Effectue un espacement uniforme dans chaque vol, avec une cible de 50 % de la diffusion dans la première moitié du vol.

* *[!UICONTROL Slightly Ahead]:* (valeur par défaut) accélère la diffusion de sorte qu’elle se termine à 55-65 % à mi-chemin de la durée du vol.

* *[!UICONTROL Frontload]:* accélère la diffusion de sorte qu’elle soit de 65 à 75 % à mi-chemin du vol.

* *[!UICONTROL Aggressive Frontload]:* accélère la diffusion de sorte qu’elle soit de 75 à 85 % à mi-chemin du vol.

**[!UICONTROL Intraday pacing]:** (Emplacements avec fréquence de placement uniquement) Comment espacer et diffuser chaque jour dans le vol :

* *[!UICONTROL Even]:* (valeur par défaut) met à l’échelle la diffusion en fonction de la disponibilité de l’inventaire. En règle générale, plus de publicités sont diffusées par heure dans la journée, lorsque le volume des enchères est plus élevé et moins de publicités sont diffusées le matin et le soir.

* *[!UICONTROL ASAP]:* (valeur par défaut) Accélère la diffusion à deux fois la vitesse de *Même*.

  >[!CAUTION]
  >
  >Cette option peut avoir une incidence négative sur les performances. Utilisez-le uniquement lorsque vous priorisez entièrement la diffusion et que vous dépensez plus que l’optimisation des performances.

**[!UICONTROL Placement Pre-bid Filters]:** (facultatif) Jusqu’à cinq filtres doivent être remplis pour que la soumission se produise. Vous pouvez utiliser des filtres avant offre comme tactiques d’optimisation, mais gardez à l’esprit que chaque règle peut limiter les opportunités sur lesquelles cet emplacement peut enchérir. Pour ajouter ou modifier des filtres :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour ajouter un filtre :
      1. Cliquez sur **[!UICONTROL Add Filter]**.
      1. En regard de **[!UICONTROL Only bid if]**, sélectionnez une mesure, puis saisissez une valeur.
   * Pour supprimer un filtre, cliquez sur **[!UICONTROL X]** dans la ligne de filtre.
1. Cliquez sur **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Facultatif) emplacements spécifiques dans lesquels inclure ou exclure des publicités à l’emplacement. Si vous ne spécifiez aucun emplacement, tous les emplacements sont ciblés.

>[!NOTE]
>
>Les emplacements de ville et de zone desservie ne sont pas disponibles pour les emplacements Roku.

Pour spécifier des emplacements :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour inclure ou exclure un pays, un État, une ville, une zone desservie, un district législatif fédéral ou un district législatif d’État :
      1. Sélectionnez le type d’emplacement dans la colonne de gauche.
      1. (Si nécessaire) Cliquez sur un emplacement pour le développer.
      1. En regard de l’emplacement, cliquez sur *[!UICONTROL Include]* pour l’inclure en tant que cible ou *[!UICONTROL Exclude]* pour l’exclure en tant que cible.
   * Pour rechercher un code postal et inclure ou exclure tous les résultats sélectionnés :
      1. Cliquez sur **[!UICONTROL Search Postal Code]**.
      1. Sélectionnez le pays.
      1. Saisissez le nom de la ville, puis cliquez sur ![Modifier](/help/dsp/assets/search.png).
      1. Cliquez sur le résultat de recherche approprié.
      1. Cliquez sur *[!UICONTROL Include All]* pour inclure tous les emplacements comme cibles ou sur *[!UICONTROL Exclude All]* pour exclure tous les emplacements comme cibles.
   * Pour saisir ou coller des codes postaux et les inclure ou les exclure tous :
      1. Cliquez sur **[!UICONTROL Paste Postal Code]**.
      1. Sélectionnez le pays.
      1. Saisissez ou collez jusqu’à 1 000 codes postaux.
Insérez un code postal par ligne ou saisissez plusieurs valeurs séparées par des virgules ou des onglets.
      1. Cliquez sur *[!UICONTROL Include All]* pour inclure tous les emplacements comme cibles ou sur *[!UICONTROL Exclude All]* pour exclure tous les emplacements comme cibles.
   * Pour supprimer un emplacement de la liste [!UICONTROL Included] ou [!UICONTROL Excluded], cliquez sur **[!UICONTROL X]** en regard de l’emplacement dans la colonne de droite.
1. Cliquez sur **[!UICONTROL Done]**.

>[!NOTE]
>
>* Tous les pays ne disposent pas d’emplacements de code postal ou d’État.
>* La zone de marché désignée, les districts législatifs fédéraux et les districts législatifs de l’État ne sont disponibles que pour les États-Unis.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Inventaire des sources à inclure ou à exclure en tant que cibles. Pour la plupart des types d’emplacements, tous les types d’inventaire et toutes les sources pour chaque type sont inclus par défaut. Pour les [!DNL Roku] emplacements, vous devez spécifier le type d’inventaire et les sources. Vous pouvez choisir parmi les types de stock suivants :

* [!UICONTROL Public] : (tous les types d’emplacement, à l’exception de Roku) Tous les exchanges ouverts auxquels DSP a accès. Vous pouvez inclure et exclure l’inventaire public.

  Vous pouvez afficher la liste par source ou par flux. Lorsque vous affichez la liste par flux, vous pouvez effectuer une recherche par nom de flux, clé de flux ou balise de caractéristique sélectionnée.

* [!UICONTROL Private] | [!UICONTROL Roku Private] : vos offres privées existantes (ou vos [!DNL Roku] offres privées existantes pour [!DNL Roku] emplacements) avec les éditeurs que vous avez configurés dans DSP. Vous pouvez inclure, mais pas exclure, l’inventaire public.

  Vous pouvez rechercher la liste par mot-clé, clé, identifiant de transaction ou balise personnalisée.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]* : (facultatif) remplace l’algorithme du prix de l’offre pour au moins offrir les prix fixes et plancher des offres.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand] : tous les [ [!UICONTROL On Demand] stocks ](/help/dsp/inventory/on-demand-inventory-about.md) non garantis  (ou [!UICONTROL On Demand] [!DNL Roku] offres pour [!DNL Roku] emplacements) auxquels vous vous êtes abonné dans [!DNL DSP]. Vous pouvez inclure et exclure l’inventaire [!UICONTROL On Demand].

  Vous pouvez afficher la liste par source ou par flux. Lorsque vous affichez la liste par flux, vous pouvez effectuer des recherches par nom de flux, clé de flux ou par région d’éditeur, balise de catégorie ou balise de caractéristique sélectionnée.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]* : (facultatif) remplace l’algorithme du prix de l’offre pour au moins offrir les prix fixes et plancher des offres.

Pour définir le ciblage des stocks :

* Pour exclure un type de stock, décochez la case en regard de son nom.
* Pour cibler un type de stock :
   1. Cochez la case en regard du nom du type de stock.
   1. (Facultatif) Modifiez les sources pour inclure :
      1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] et [!UICONTROL On Demand] inventaire) Cliquez sur **[!UICONTROL View by Source]** ou **[!UICONTROL View by Feed]** pour modifier la manière dont les sources sont répertoriées.
      1. (Le cas échéant) Filtrez l’inventaire selon vos besoins.
      1. Indiquez les sources à inclure et à exclure :
         * Pour inclure une source [!UICONTROL Public] ou [!UICONTROL On Demand], cliquez sur **[!UICONTROL Include]** en regard du nom de la source.
         * Pour inclure [!UICONTROL Private] sources :
            * Pour inclure tout l’inventaire dans une transaction, cliquez sur **[!UICONTROL Include all]** en regard de son nom.
            * Pour inclure une source de stock individuelle, développez le nom de l’opération, puis cochez la case en regard du nom de la source.
         * Pour exclure un [!UICONTROL Public] ou un [!UICONTROL On source], cliquez sur **[!UICONTROL Exclude]** en regard du nom de la source.
   1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage vers l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Save & Export]**.
   1. Cliquez sur **[!UICONTROL Save]**.

>[!TIP]
>
>Si vous vous êtes abonné à l’inventaire [!UICONTROL On Demand] mais que vous ne parvenez pas à localiser les éditeurs ou les offres à cibler, vérifiez le statut des offres. Pour plus d’informations sur les états, voir [À propos de [!DNL On Demand] Premium Inventory](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (emplacements de vidéos uniquement) Exclut le trafic sortant.

Les publicités sortantes apparaissent généralement sur le contenu sous la forme d’une fenêtre contextuelle ou d’un contenu (dans l’expérience native), plutôt que sous la forme de publicités vidéo standard dans un lecteur vidéo.

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** Types de trafic à cibler. Les options incluent **[!UICONTROL Websites]** et **[!UICONTROL Apps]**.

**[!UICONTROL Tier]:** (Disponible lorsque **[!UICONTROL Paste list of targeted sites]** est *[!UICONTROL Off]*) Qualité du trafic à cibler. Les niveaux 1 à 3 sont tous sécurisés pour la marque et ont été approuvés par l’équipe de mappage DSP.

* *[!UICONTROL Tier 1]:* sites et applications Premium reconnaissables au niveau national.

* *[!UICONTROL Tier 2]:* cible le niveau 1 ainsi que les sites et applications de qualité moins connus que le niveau 1.

* *[!UICONTROL Tier 3]:* Cibles niveaux 1 à 2 plus des sites et applications légitimes et sécurisés pour la marque qui répondent à une audience de niche. Utilisez le niveau 3 pour la portée ou les achats de ciblage de données.

* *[!UICONTROL All Sites or Apps]:* Cible les niveaux 1 à 3 et le nouvel inventaire qui n’a pas été analysé ou classé, que vous pouvez utiliser pour atteindre.

>[!NOTE]
>
>L’inventaire est spécifique aux unités publicitaires de l’emplacement.

>[!TIP]
>
>Pour les campagnes de performances, la bonne pratique consiste à sélectionner *[!UICONTROL All Sites]*.

**[!UICONTROL Site or App Categories]:** (Facultatif ; disponible lorsque **[!UICONTROL Paste list of targeted sites]** est *[!UICONTROL Off]*) Catégories de site au sein des niveaux de site sélectionnés pour inclure ou exclure (mais pas les deux) en tant que cibles. Effectuez un choix parmi les listes de sites verticales que DSP a mises en correspondance en fonction de l’objet :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les catégories de site à inclure ou à exclure :
   * Pour inclure des catégories de site :
      1. Cliquez sur **[!UICONTROL Include categories]**.
      1. Cochez la case en regard de chaque catégorie à cibler.
   * Pour exclure des catégories de site :
      1. Cliquez sur **[!UICONTROL Exclude categories]**.
      1. Cochez la case en regard de chaque catégorie à exclure.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage vers l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (facultatif ; disponible lorsque **[!UICONTROL Paste list of targeted sites]** est *[!UICONTROL Off]*) Sites à exclure. Vous pouvez rechercher et sélectionner des sites, ou saisir ou coller des noms de domaine :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les sites :
   * Pour rechercher un site :
      1. Cliquez sur **[!UICONTROL Search]**.
      1. Saisissez un mot-clé, sélectionnez un niveau de site et/ou sélectionnez une catégorie de site.
      1. Dans les résultats de recherche, sélectionnez les sites à exclure :
         * Pour exclure un site individuel, cochez la case adjacente.
         * (Lorsque plus de 50 résultats sont disponibles) Pour exclure les 50 premiers résultats, cliquez sur **[!UICONTROL Exclude these 50]**. Pour exclure tous les résultats de la recherche, cliquez sur **[!UICONTROL Exclude these \<*NN *\>]**.
   * Pour saisir les noms de domaine :
      1. Cliquez sur **[!UICONTROL Paste]**.
      1. Entrez un ou plusieurs noms de domaine sur des lignes distinctes.
      1. Cliquez sur **[!UICONTROL Exclude All]**.
1. Cliquez sur **[!UICONTROL Done]** lorsque vous avez terminé.

>[!NOTE]
>
>* Des listes de sites bloqués au niveau du compte et de l’annonceur sont également appliquées, en plus de la DSP [liste de sites bloqués globalement](/help/dsp/introduction/features/brand-safety-media-quality.md), qui inclut les sites considérés comme dangereux pour les publicités.
>* Les listes de sites bloquées remplacent toujours les listes de sites ciblées. Si un emplacement exclut et inclut la même cible pour une publicité, la cible est exclue.

**[!UICONTROL Language]:** (facultatif) Une seule langue à cibler.

**[!UICONTROL Site or App List Preview]:** (lecture seule) tous les sites ciblés et bloqués pour l’emplacement.

Vous pouvez éventuellement exporter la liste des sites ciblés et bloqués sous la forme d’un fichier CSV (valeurs séparées par des virgules). Pour exporter la liste, cliquez sur **[!UICONTROL Export full site list]**, puis ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur.

**[!UICONTROL Allow unscreened sites]:** (emplacements d’affichage standard uniquement) Active la diffusion publicitaire sur des sites non contrôlés. Lorsque l’emplacement cible l’inventaire privé, cette option peut diffuser des publicités sur les sites bloqués.

**[!UICONTROL Paste list of targeted sites]:** Permet de cibler des sites spécifiques uniquement. Lorsque vous activez cette option, les autres options de ciblage de site sont désactivées.

**[!UICONTROL Sites]:** (Disponible lorsque **[!UICONTROL Paste list of targeted sites]** est *[!UICONTROL On]*) Sites à cibler. Vous pouvez rechercher et sélectionner des sites, ou saisir ou coller des noms de domaine :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les sites :
   * Pour rechercher un site :
      1. Cliquez sur **[!UICONTROL Search]**.
      1. Saisissez un mot-clé, sélectionnez un niveau de site et/ou sélectionnez une catégorie de site.
      1. Dans les résultats de recherche, sélectionnez les sites à inclure :
         * Pour exclure un site individuel, cochez la case adjacente.
         * (Lorsque plus de 50 résultats sont disponibles) Pour inclure les 50 premiers résultats, cliquez sur **[!UICONTROL Include these 50]**. Pour inclure tous les résultats de la recherche, cliquez sur **[!UICONTROL Include these \<*NN *\>]**.
   * Pour saisir les noms de domaine :
      1. cliquez sur **[!UICONTROL Paste]**.
      1. Entrez un ou plusieurs noms de domaine sur des lignes distinctes.
      1. Cliquez sur **[!UICONTROL Include All]**.
1. Cliquez sur **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Toutes les cibles d’audience pour l’emplacement, y compris les [ segments tiers, segments propriétaires, segments d’Adobe, segments personnalisés et audiences enregistrées](/help/dsp/audiences/audience-settings.md). La taille totale et active de l’audience dédupliquée pour tous les segments sélectionnés et les audiences enregistrées s’affiche également. Vous pouvez sélectionner une audience existante, créer une audience que vous pourrez réutiliser ultérieurement ou sélectionner des segments d’audience spécifiques :

* Pour sélectionner une audience existante, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Included Audiences], puis sélectionnez l’audience.
* Pour créer une audience, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Included Audiences], puis sélectionnez **[!UICONTROL + Create Audience]**. Pour obtenir des instructions, reportez-vous à la section [Création d’une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md), en commençant par l’étape 3.
* Pour sélectionner des segments d’audience spécifiques, cliquez sur **[!UICONTROL Select segments for this placement only]**. Sélectionnez la logique de segment. Pour obtenir des instructions, reportez-vous à l’étape 6 de la section &quot;[Création d’une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md)&quot;. Une fois que vous avez terminé, cliquez sur **Enregistrer**.

**[!UICONTROL Excluded Audiences]:** Toutes les audiences à exclure pour l’emplacement, y compris les audiences avec [ segments tiers, segments propriétaires, segments Adobes, segments personnalisés et audiences enregistrées](/help/dsp/audiences/audience-settings.md). La taille totale et active de l’audience dédupliquée pour toutes les audiences exclues s’affiche également. Vous pouvez sélectionner une audience existante ou créer une nouvelle audience que vous pourrez réutiliser ultérieurement :

* Pour sélectionner une audience existante, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Excluded Audiences], puis sélectionnez l’audience.

* Pour créer une audience, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Excluded Audiences], puis sélectionnez **+ Créer une audience**. Pour obtenir des instructions, reportez-vous à la section [Création d’une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md), en commençant par l’étape 3.

**[!UICONTROL Targeting]:** Types d’ID utilisateur à cibler. Vous ne pouvez pas modifier ce paramètre une fois le placement actif (c’est-à-dire après le début du vol).

Lorsque vous sélectionnez à la fois des ID hérités et des ID universels, la préférence d’offre est accordée aux ID universels.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]* : (valeur par défaut) cible les utilisateurs en fonction de leurs cookies, identifiants de publicité mobile ou identifiants de télévision (CTV) connectés. Les identifiants sont sélectionnés en fonction de l’inventaire du navigateur, de l’application ou de la technologie CTV.

* *[!UICONTROL Universal ID Beta]* : cible les identifiants axés sur la confidentialité des utilisateurs ; sélectionnez un type d’identifiant. Les options disponibles sont déterminées par les cibles géographiques sélectionnées dans la section [!UICONTROL Geo-Targeting]. Utilisez avec les [[!DNL RampID] segments importés directement vers DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [ segments pour lesquels DSP convertit vos informations d’identification personnelles en identifiants universels](/help/dsp/audiences/sources/source-about.md) ou [segments personnalisés qui effectuent le suivi des identifiants universels](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]* : cible les [!DNL ID5] identifiants créés de manière probabiliste à partir d’adresses électroniques et d’autres signaux.<!-- What countries/geos are these available for? Everywhere?--> ID5 sont disponibles sans frais. **Remarque :** Les segments tiers de [!DNL Eyeota] peuvent inclure des ID5.

   * *[!UICONTROL RampID]* : cible [!DNL LiveRamp] [!DNL RampIDs] des utilisateurs connectés à votre site à l&#39;aide de leurs adresses électroniques.<!-- Verify --> [!DNL RampIDs] sont disponibles pour les utilisateurs en Amérique du Nord, en Australie et en Nouvelle-Zélande.

   * *[!UICONTROL Unified ID2.0]* : cible les identifiants [!DNL Unified ID2.0] (UID2) des utilisateurs connectés à votre site à l’aide de leurs adresses électroniques.<!-- Verify -->[!DNL UID2 IDs] ne sont pas disponibles pour les utilisateurs de l’Espace économique européen et de certains pays supplémentaires. Voir la [liste des pays interdits](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]** : Conditions d’utilisation des identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les termes une fois avant de pouvoir convertir les données en un nouveau type d’ID. Pour les clients disposant de contrats de service géré, votre équipe de compte d’Adobe obtiendra votre consentement et acceptera les conditions pour le compte de votre organisation. Pour lire les termes, cliquez sur **>**. Pour accepter les termes, faites défiler l’écran jusqu’au bas des termes et cliquez sur **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (Disponible lorsque la campagne [est configurée pour le ciblage multi-appareils basé sur les personnes](/help/dsp/campaign-management/campaigns/campaign-settings.md), vous ciblez les identifiants hérités uniquement (et non les identifiants universels) et vous sélectionnez au moins un segment ou une audience. Permet d’étendre le ciblage sur tous les appareils connus d’une personne (selon la représentation graphique des appareils spécifiée dans les paramètres de la campagne), même sur les appareils qui ne figurent pas dans les segments spécifiés. Les frais peuvent s&#39;appliquer en fonction du graphique spécifié pour l&#39;opération. Les données de Device Graph sont disponibles uniquement en Amérique du Nord.

**[!UICONTROL Placement Cap]:** (Facultatif) Le nombre de fois qu’un appareil unique, un identifiant universel ou une personne (selon le [!UICONTROL Cross Device Level] spécifié pour la campagne et le paramètre [!UICONTROL Targeting] de l’emplacement) peuvent recevoir des publicités à partir de l’emplacement. Les options incluent *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
> Vous pouvez définir des limites de fréquence aux niveaux de la campagne, du kit et de l’emplacement. DSP respecte la limite de fréquence la plus stricte de la hiérarchie de l&#39;opération.

**[!UICONTROL Secondary Cap]:** (Facultatif ; disponible lorsque vous incluez une valeur numérique [!UICONTROL Placement Cap]) Une limitation supplémentaire dans les limites de la limite d’emplacement principale. Sélectionnez le nombre d’impressions et la période (3 par 12 heures, par exemple).

**[!UICONTROL Day Parting]:** (Facultatif) jours spécifiques de la semaine et heure de la journée pendant lesquels les publicités peuvent s’exécuter. Pour définir des intervalles de créneaux horaires :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Sélectionnez le fuseau horaire applicable.
1. Spécifiez les intervalles :
   * Pour sélectionner un intervalle prédéfini, cliquez sur l’un des boutons de l’intervalle. Les options incluent *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* ou *[!UICONTROL Prime]* (primetime).
   * Pour sélectionner manuellement un intervalle, cliquez à l’intérieur d’une cellule, puis faites-le glisser pour sélectionner l’intervalle.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Facultatif ; disponible pour les annonceurs configurés avec [!DNL Proximic by Comscore] segments) noms ou identifiants de segments spécifiques de [!DNL Proximic by Comscore] à inclure en tant que cibles. Des frais supplémentaires peuvent s’appliquer pour cette fonctionnalité. Pour activer cette fonctionnalité et configurer les segments de rubrique, contactez votre équipe de compte d’Adobe.

Pour spécifier le ciblage de rubrique :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les segments à cibler :
   1. Dans la colonne de gauche, sélectionnez le partenaire : (*[!UICONTROL Comscore]*.
   1. Dans le champ de saisie, saisissez les noms ou les identifiants de segment.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de rubrique vers l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

>[!TIP]
>
>* Le ciblage de rubrique limite l’inventaire sur lequel l’emplacement peut enchérir. Par conséquent, utilisez le ciblage de rubrique pour seulement un faible pourcentage de votre achat global.
>
>* Configurez tout ciblage négatif dans le segment sur [!DNL Proximic by Comscore].

**[!UICONTROL Device Targeting]:** (Facultatif) Informations spécifiques sur les appareils, notamment les types d’appareils, les fabricants, les systèmes d’exploitation, les navigateurs et les types de connectivité, à inclure et exclure en tant que cibles. Les types varient en fonction du type d’emplacement. Pour spécifier le ciblage des périphériques :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les détails de l’appareil à inclure et à exclure :
   1. Dans la colonne de gauche, sélectionnez la catégorie.
   1. Spécifiez le ciblage :
      * Pour inclure une valeur, cliquez sur **[!UICONTROL Include]** en regard de son nom.
      * Pour exclure une valeur, cliquez sur **[!UICONTROL Exclude]** en regard de son nom.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage de l’appareil à l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Facultatif) Fournisseurs d’accès à Internet (FAI) spécifiques à inclure ou à exclure (mais pas les deux) comme cibles. Pour spécifier le ciblage des FAI :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les FAI à inclure ou à exclure :
   * Pour inclure des FAI :
      1. Cliquez sur **[!UICONTROL Include ISPs]**.
      1. (Facultatif) Filtrez la liste par mot-clé.
      1. Cochez la case en regard de chaque FAI à cibler.
   * Pour exclure les FAI :
      1. Cliquez sur **[!UICONTROL Exclude ISPs]**.
      1. (Facultatif) Filtrez la liste par mot-clé.
      1. Cochez la case en regard de chaque FAI à exclure.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage du FAI vers l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (facultatif ; clients [!DNL DoubleVerify] uniquement ; disponible uniquement pour l’affichage preroll de bureau, standard et clic pour lecture, ainsi que pour les emplacements d’affichage et vidéo natifs uniquement ; non pris en charge pour [ emplacements garantis par programmation par défaut pour les offres ](/help/dsp/inventory/programmatic-guaranteed-about.md)) Un identifiant de segment [!DNL DoubleVerify Authentic Brand Safety] associé au compte [!DNL DoubleVerify] de l’organisation à utiliser pour l’emplacement. La spécification d’un ID bloque les impressions après l’offre à l’aide des règles de sécurité de marque personnalisées configurées pour l’ID de segment spécifié. DSP facture votre compte pour l’utilisation de l’identifiant de segment.

L’ID doit commencer par &quot;51&quot; et se composer de huit chiffres. Par défaut, si un identifiant de segment est spécifié dans les paramètres du compte de l’annonceur, l’identifiant au niveau de l’annonceur est saisi, mais vous pouvez modifier l’identifiant pour utiliser un autre segment ou supprimer l’identifiant pour désactiver la fonctionnalité.

**[!UICONTROL Contextual filtering]:** Types de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39] filtres contextuels à appliquer. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour de nouveaux emplacements, mais vous pouvez modifier les paramètres :

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify] :

   * **[!UICONTROL Block sites that are]:** (facultatif) Un ou plusieurs types de contexte d’inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Peer 39] :

   * **Ciblez les sites qui sont :** (facultatif) Un ou plusieurs types d’attributs d’inventaire à cibler par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL ComScore] :

   * **Bloquer les sites qui sont :** (facultatif) Un ou plusieurs types d’attributs d’inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (facultatif) degré de contenu adulte pour lequel bloquer les publicités par défaut : *[!UICONTROL Do Not Block]* (valeur par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

   * **[!UICONTROL Alcohol Content]:** (Facultatif) Le degré de contenu d’alcool pour lequel bloquer les publicités par défaut : *[!UICONTROL Do Not Block]* (valeur par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Pre-bid fraud blocking]:** Types de sites à bloquer en fonction du trafic frauduleux et des activités suspectes mesurées par [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39]. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour de nouveaux emplacements, mais vous pouvez modifier les paramètres :

* [!UICONTROL DoubleVerify] :

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Par défaut, bloque tout le trafic non valide à 100 %, y compris le trafic sur les appareils détournés, pour les nouveaux emplacements. Des frais supplémentaires peuvent s’appliquer.

   * **[!UICONTROL Also block sites with]:** (Facultatif) Un niveau supplémentaire de fraude et de trafic non valide qui provoque DSP blocage des publicités par défaut : *[!UICONTROL None]* (valeur par défaut, qui ne bloque pas le trafic supplémentaire), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Peer 39] :

   * **[!UICONTROL Block sites that are]:** (Facultatif) Un ou plusieurs types de fraude qui DSP bloquer les publicités par défaut : *[!UICONTROL Fraud]* (qui bloque tous les sites présentant une fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* et/ou *[!UICONTROL Fraud: Zero Ads]*. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Integral Ad Science] :

   * **[!UICONTROL Block sites that are]:** (Facultatif) Type d’activité de site Web ou d’application suspecte qui entraîne DSP bloquer les publicités par défaut : *[!UICONTROL None]* (valeur par défaut, qui ne bloque pas les publicités en fonction d’activités suspectes), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Pre-bid viewability]:**

Les filtres de visibilité avant l’offre par [!DNL DoubleVerify] et [!DNL Integral Ad Science] à appliquer pour l’emplacement. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour de nouveaux emplacements, mais vous pouvez modifier les paramètres. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Ads.txt filtering]:**

Quel niveau de [Ads.txt](https://iabtechlab.com/ads-txt-about/) de filtrage pré-enchère utiliser en appliquant la liste des vendeurs numériques autorisés de chaque éditeur ? La valeur par défaut au niveau de l’annonceur est sélectionnée pour les nouveaux emplacements, mais vous pouvez modifier les paramètres :

* *[!UICONTROL Opt out of ads.txt (default)]* : pour acheter un stock à tous les vendeurs.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]* : pour donner la priorité à l’achat de l’inventaire auprès des revendeurs directs autorisés d’un domaine.
* *[!UICONTROL Ads.txt sellers only]* : pour acheter des stocks uniquement auprès des revendeurs directs et des revendeurs autorisés d’un domaine.
* *[!UICONTROL Ads.txt sellers only]* : pour acheter un inventaire uniquement auprès des vendeurs directs autorisés d’un domaine.

**[!UICONTROL Attention Targeting]:** (emplacements de télévision standard, d’affichage, de vidéo, de mobile et connectés) cible [!DNL Adelaide] les segments pré-enchérisés avec un niveau d’attention spécifique (élevé, moyen ou faible) en fonction du site, du format et de la taille de l’annonce spécifiés. Les segments sont mis à jour toutes les semaines. **Remarque :** L’utilisation de [!DNL Adelaide] segments pour le ciblage entraîne des frais CPM pour chaque impression fournie avec le ciblage de l’attention [!DNL Adelaide] ; ces frais sont différents des frais pour la [mesure de l’attention](/help/dsp/campaign-management/campaigns/campaign-settings.md). Pour les emplacements interactifs preroll, les frais sont facturés uniquement pour les impressions VAST.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] emplacements) Les fournisseurs de suivi tiers approuvés par [!DNL Roku] comprennent [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] et [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (facultatif) pixels de suivi d’événements tiers à joindre par défaut à toutes les nouvelles publicités de l’emplacement. Pour spécifier les pixels d’événement :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour sélectionner un pixel existant, cochez la case dans la ligne de pixel.
   * Pour créer un pixel :
      1. Cliquez sur **[!UICONTROL Create]**.
      1. Renseignez les informations suivantes :
         * **[!UICONTROL Pixel name]:** Nom du pixel ; la longueur maximale est de 500 caractères. Utilisez un nom qui vous aide à identifier facilement le pixel.
         * **[!UICONTROL Pixel event fires on]:** événement qui déclenche le déclenchement du pixel. Les événements disponibles varient en fonction du type de publicité.
         * **[!UICONTROL Pixel type]:** Indique si le pixel est un *[!UICONTROL IMG URL]* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** URL de l’image de pixel.
      1. Cliquez sur **[!UICONTROL Create and attach]**.
   1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (facultatif) pixels de suivi des conversions à joindre par défaut à toutes les nouvelles publicités de l’emplacement. Pour spécifier les pixels de conversion :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour sélectionner un pixel existant, cochez la case dans la ligne de pixel.
   * Pour créer un pixel :
      1. Cliquez sur **[!UICONTROL Create]**.
      1. Renseignez les informations suivantes :
         * **[!UICONTROL Conversion pixel name]:** Nom du pixel ; la longueur maximale est de 500 caractères. Utilisez un nom qui vous aide à identifier facilement le pixel.
         * **[!UICONTROL Conversion category]:** Type de conversion.
         * **[!UICONTROL Impression conversion window]:** nombre de jours après une impression publicitaire au cours desquels l’impression peut être attribuée à une conversion. La valeur par défaut est de 30 jours.
         * **[!UICONTROL Click conversion window]:** nombre de jours après un clic publicitaire pendant lesquels le clic peut être attribué à une conversion. La valeur par défaut est de 30 jours.
         * **[!UICONTROL Notes]:** (facultatif) description ou autre information sur le pixel.
      1. Cliquez sur **[!UICONTROL Create and attach]**.
      1. Implémentez le pixel de conversion sur les pages web appropriées :
         1. Dans le menu principal, accédez à **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Dans la ligne de pixel, cliquez sur **[!UICONTROL edit]**.
         1. Copiez la ou les valeurs dans les champs [!UICONTROL HTML Tag] et [!UICONTROL Flash Tag], si nécessaire, pour les fournir au contact de l’annonceur ou du site web.

            Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement de la balise ou d’être informé de ce déploiement.
   1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Facultatif) Taux de frais tiers statique qui doit être suivi en tant que coût non facturable pour 1 000 impressions. Le cas échéant, la valeur par défaut au niveau du package est automatiquement appliquée pour les nouveaux emplacements, sauf si vous saisissez une autre valeur.

>[!NOTE]
>
>Les frais facturables sont reflétés dans la mesure [!UICONTROL Net CPM].

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Créer un emplacement](placement-create.md)
>* [Modifier des emplacements](placement-edit.md)
>* [Gérer les multiplicateurs d’offre pour les emplacements](placement-manage-bid-multipliers.md)
>* [Afficher le journal des modifications d’un emplacement](placement-change-log.md)
>* [Raccourcis clavier](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [FAQ sur Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
