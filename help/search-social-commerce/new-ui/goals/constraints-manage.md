---
title: Gérer les contraintes pour les unités d’offres de recherche
description: Découvrez les contraintes permettant de restreindre les offres d’unités d’offre dans les campagnes CPC des portefeuilles hérités au niveau des mots-clés.
feature: Search Campaign Management, Search Optimization
source-git-commit: 327f2214d601849008a3e6c8b804ea0f109b53d0
workflow-type: tm+mt
source-wordcount: '2636'
ht-degree: 0%

---

# Gérer les contraintes pour les unités d’offres de recherche

<!-- Read through all and edit as appropriate -->

*Applicable uniquement aux unités d’enchères dans les campagnes CPC des portefeuilles hérités de niveau mot-clé*

Les contraintes d&#39;unité d&#39;offres sont des règles qui limitent les offres optimisées pour toutes les [unités d&#39;offres](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html) avec des modèles de coût et de chiffre d&#39;affaires associés à la contrainte.

## À propos des contraintes

Chaque contrainte s’applique à une devise spécifique et inclut éventuellement des conditions de déclenchement qui doivent être remplies au cours d’une période d’évaluation des données spécifiée pour que la règle s’applique. Les données à évaluer peuvent inclure le type de canal, le type de correspondance, les données de clic, les données de conversion ou les mesures dérivées. Par exemple, vous pouvez limiter les offres à une fourchette monétaire spécifique, augmenter ou diminuer les offres de façon continue d&#39;un montant spécifié ou encore les enchérir en fonction de l&#39;enchère moyenne pour le portefeuille. Chaque contrainte comporte une date de début applicable et expire à une date spécifique ou est appliquée indéfiniment.

Après avoir configuré une contrainte, vous pouvez l&#39;affecter à des unités d&#39;enchères spécifiques ou à toutes les unités d&#39;enchères au sein de groupes d&#39;annonces ou de campagnes spécifiques. Chaque unité d’offre peut avoir une contrainte. Les contraintes sont héritées par les entités enfants mais peuvent être remplacées. Une contrainte affectée au niveau le plus bas remplace toujours une contrainte affectée à un niveau parent. Lorsque vous affectez une contrainte à une unité d&#39;offre, l&#39;offre fonctionne dans les contraintes spécifiées pour cette unité d&#39;offre, quel que soit le chiffre d&#39;affaires généré par l&#39;unité d&#39;offre, lorsque l&#39;unité d&#39;offre comporte des modèles de coût et de chiffre d&#39;affaires.

>[!CAUTION]
>
>Lorsque vous affectez des contraintes à une unité d&#39;offre, vous remplacez la décision du système d&#39;optimisation des offres et assumez vous-même la responsabilité du retour sur investissement de cette unité d&#39;offre.

>[!NOTE]
>
>* Les contraintes actives limitent les enchères uniquement pour les unités d’offre affectées dans les portefeuilles optimisés au niveau des mots-clés hérités. Elles sont ignorées pour les unités d&#39;enchères qui se trouvent dans des portefeuilles hybrides, dans des portefeuilles actifs ou qui ne se trouvent pas dans des portefeuilles. **Conseil :** dans les paramètres du portfolio, activez l’option du portfolio pour ajuster automatiquement les limites du budget de la campagne. La valeur « Multiple » recommandée est « 1 ».
> * Les contraintes d’offre sont ignorées pour les unités d’offre sans suffisamment de données pour générer des modèles de coût et de chiffre d’affaires.
>* (Campagnes avec une stratégie d’enchères CPC ou eCPC) Lorsqu’une contrainte d’offre entre en conflit avec une limite d’offre au niveau du portefeuille, la contrainte remplace la limite au niveau du portefeuille. Par exemple, si l&#39;offre minimale d&#39;un portefeuille est de 5 USD mais que vous limitez une unité d&#39;offre du portefeuille à une offre minimale de 3 USD, l&#39;unité d&#39;offre est alors de 3 USD ou plus. Toutefois, les dépenses globales pour les unités d&#39;enchères avec contraintes sont déterminées par le paramètre [ du portefeuille « Dépenser en fonction des contraintes »](#spend-around-constraints).
>* Les contraintes opèrent sur l&#39;offre de base. Tout type d’ajustement de l’offre de base (tel que l’augmentation de l’offre pour les utilisateurs finaux sur des appareils mobiles) peut faire sortir l’offre de la plage autorisée pour la contrainte. Par exemple, si la contrainte nécessite un CPC maximum de 6 USD, l’enchère de base est déjà de 6 USD et le portefeuille optimise automatiquement les ajustements d’enchère pour les appareils mobiles à 50 %-60 %, alors le CPC maximum est de 9,00-9,60 USD, et non de 6 USD.

### Types de contrainte {#constraint-types}

* **[!UICONTROL Bid]:** Limite les offres à une plage monétaire.

* **[!UICONTROL Bid Shift]:** modifie en permanence les enchères optimisées pour toutes les unités d&#39;enchères associées d&#39;un montant spécifié, dans les limites d&#39;enchères. Un changement d’offre entraîne une sur-dépense ou une sous-dépense des portefeuilles concernés par le montant total provoqué par le changement d’offre, quel que soit le paramètre du portefeuille pour « Dépenser en fonction des contraintes ». Remarque : Si l&#39;offre CPC actuelle est déjà supérieure ou égale à l&#39;offre maximale, ou inférieure ou égale à l&#39;offre minimale, la contrainte est ignorée et l&#39;offre n&#39;est pas modifiée. En outre, les contraintes de changement d&#39;offre ne sont pas appliquées aux unités d&#39;offre sans suffisamment de données pour générer des modèles de coût et de chiffre d&#39;affaires.

* **[!UICONTROL Incremental Bidding]:** (applicable uniquement aux mots-clés sans impressions) Augmente ou réduit l’offre de manière incrémentielle à un taux spécifié jusqu’à ce que l’offre atteigne une cible désignée.

* **[!UICONTROL Search Engine Min Bid]:** (comptes [!DNL Google Ads] uniquement) Utilise les enchères CPC minimales déterminées par le moteur de recherche comme enchères minimales. Lorsque le moteur de recherche modifie ses enchères minimales, votre enchère change en conséquence. Vous pouvez éventuellement spécifier des limites d&#39;enchères supplémentaires pour toutes les unités d&#39;enchères associées.

* **[!UICONTROL Impression Share]:** (campagnes CPC [!DNL Google Ads] et [!DNL Microsoft Advertising] avec correspondance exacte uniquement) Limite les offres à une plage monétaire lorsque les annonces se situent entre un partage d’impression minimum et maximum. **Remarque :** lorsque la contrainte n&#39;est pas rentable, la fonctionnalité d&#39;optimisation peut la remplacer.

### Quand appliquer des contraintes

Voici quelques raisons de limiter les unités d&#39;enchères :

* Exposer rapidement les mots-clés et les publicités non testés.

* Pour atténuer les risques liés aux nouveaux portfolios, comptes, campagnes et groupes publicitaires. Par exemple, avant de lancer un portefeuille, vous pouvez définir des enchères maximales sur les unités d’enchères à trafic élevé, puis augmenter progressivement les valeurs chaque jour. Cela permet au modèle d&#39;offres de s&#39;ajuster chaque jour sans risque d&#39;augmentation importante des offres.

* Pour vous assurer que les mots-clés avec des taux de conversion élevés ne sont pas utilisés à la baisse.

* Pour enchérir sur des conditions spécifiques qui sont essentielles pour votre marque ou lors de promotions.

### Où afficher des informations sur les contraintes dans toute l’interface utilisateur <!-- wording? -->

Outre l&#39;ouverture de la vue [[!UICONTROL Constraints] vous pouvez également afficher les informations relatives à vos contraintes des manières suivantes :](#constraints-view)

* Toutes vos contraintes sont des valeurs de libellé pour une seule [classification de libellé](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html) appelée « [!UICONTROL Constraints] ».

   * « [!UICONTROL Constraints] » est inclus dans la liste « [!UICONTROL Classifications] » dans vos paramètres d&#39;affichage par défaut et personnalisés et dans les rapports planifiés. Vous pouvez ajouter la colonne où vous souhaitez voir les contraintes affectées aux entités pertinentes.

   * Lorsque vous téléchargez une feuille d’envoi groupé, « [!UICONTROL Constraints] » est répertorié sous la colonne « [!UICONTROL Classifications] » pour les entités applicables dans la boîte de dialogue [!UICONTROL Download Bulksheet]. Lorsque vous incluez la colonne , la feuille d’envoi groupé téléchargée inclut toutes les contraintes affectées aux entités pertinentes.

  La classification [!UICONTROL Constraints] n’est pas incluse dans la vue [!UICONTROL Label Classifications] ; la vue [!UICONTROL Constraints] est distincte. La classification [!UICONTROL Constraints] n’est pas non plus incluse dans la limite de classification de 30 étiquettes.

* [ La [!UICONTROL Constraint Report]](/help/search-social-commerce/reports/management/basic-advanced/constraint-report.md) inclut les données de coût, de clic et (éventuellement) de conversion pour les contraintes qui utilisent l’architecture de classification de libellés.

### La vue [!UICONTROL Constraints] {#constraints-view}

La vue [!UICONTROL Goals] > [!UICONTROL Constraints] répertorie toutes vos contraintes. Les colonnes disponibles incluent le statut de la contrainte ; le type de contrainte, les dates de début et de fin ; le nombre de campagnes, de groupes publicitaires, de mots-clés, d’annonces, d’emplacements, de cibles automatiques et de groupes de produits auxquels la contrainte est associée ; les impressions, les clics et les données de coût ; ainsi que les données sur le chiffre d’affaires pour toutes les mesures de conversion visibles.<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>Les données de performances d&#39;une ligne dans la vue [!UICONTROL Constraints] peuvent ne pas correspondre aux données de performances de l&#39;entité de niveau supérieur à laquelle la contrainte est affectée. Étant donné qu’une contrainte attribuée au niveau le plus bas remplace toujours une contrainte attribuée au niveau parent, une contrainte attribuée à une campagne ou à un groupe publicitaire peut ne pas rester attribuée aux groupes publicitaires et mots-clés enfants. Par exemple, si la campagne A se voit attribuer la contrainte A, tous les groupes publicitaires et tous les mots-clés de la campagne A héritent automatiquement de la contrainte A. Cependant, ces groupes publicitaires et mots-clés pourraient être affectés ultérieurement à d&#39;autres contraintes, telles que la contrainte B, et ils perdraient alors leur association avec la contrainte A.

Vous pouvez créer, modifier et modifier le statut des contraintes à partir de la vue [!UICONTROL Constraints].

>[!NOTE]
>
>Vous pouvez affecter des contraintes aux unités d&#39;enchères et annuler leur affectation à partir de la vue de gestion des entités appropriée (par exemple de la vue [!UICONTROL Campaigns] pour les contraintes au niveau de la campagne).

#### Actions disponibles

* [Créer une contrainte](#constraint-create).

* [Modifier les paramètres de contrainte](#constraint-edit).

* [Modifier le statut des contraintes](#constraint-change-status).

## Créer une contrainte {#constraint-create}

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. Dans la barre d’outils supérieure droite, au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Constraint]**.

1. Saisissez les [paramètres de contrainte](#constraint-settings).

   Pour passer de l’onglet [!UICONTROL Constraint Type] à l’onglet [!UICONTROL Conditions], cliquez sur l’onglet à ouvrir ou sur les boutons [!UICONTROL Next] et [!UICONTROL Back] .

1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

1. Cliquez sur **[!UICONTROL Save]**.

Une fois une contrainte créée, vous pouvez l&#39;[affecter](#constraint-assign) aux campagnes, aux groupes publicitaires, aux mots-clés, aux emplacements et aux groupes de produits au niveau de l&#39;unité.

## Modifier les paramètres de contrainte {#constraint-edit}

Vous pouvez modifier les paramètres d&#39;une contrainte à la fois.

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Facultatif) Filtrez la liste [à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou d’un en-tête de colonne [](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Cochez la case en regard de la contrainte à modifier.

1. Dans la barre d’outils des actions en bloc, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier").

1. Modifiez les [paramètres de contrainte](#constraint-settings).

   Pour passer de l’onglet [!UICONTROL Constraint Type] à l’onglet [!UICONTROL Conditions], cliquez sur l’onglet à ouvrir ou sur les boutons [!UICONTROL Next] et [!UICONTROL Back] .

1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

1. Cliquez sur **[!UICONTROL Save]**.

## Modifier le statut des contraintes {#constraint-change-status}

Vous pouvez suspendre toute contrainte active pour la désactiver. Vous pouvez l’activer ultérieurement en redéfinissant son statut sur *actif*.

Vous pouvez également supprimer une contrainte, ce qui supprime toutes les associations avec les composants de compte et rend la contrainte indisponible pour une utilisation ultérieure. Les données de rapport pour la contrainte ne sont plus disponibles. **Remarque :** pour dissocier simplement une contrainte d&#39;un composant de compte, reportez-vous à la rubrique [Annuler l&#39;affectation de contraintes des unités d&#39;enchères de recherche](#constraints-unassign). »

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Facultatif) Filtrez la liste [à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou d’un en-tête de colonne [](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Cochez la case en regard de chaque contrainte dont vous souhaitez modifier le statut.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur le bouton Statut :

   * Pour activer toutes les lignes sélectionnées, cliquez sur ![Activer](/help/search-social-commerce/assets/activate-new.png "Activer").

   * Pour suspendre toutes les lignes sélectionnées, cliquez sur ![Pause](/help/search-social-commerce/assets/pause-new.png "Pause").

   * Pour supprimer toutes les lignes sélectionnées, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer").

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Paramètres des contraintes {#constraint-settings}

| Tabulation | Paramètre | Description |
|---|---|---|
| \[Informations de base\] | [!UICONTROL Constraint Name] | Nom unique de la contrainte. |
| | [!UICONTROL Currency] | Devise dans laquelle toutes les unités d&#39;offre applicables sont proposées. Les unités d&#39;enchères pour lesquelles une devise différente est utilisée sont ignorées. |
| | [!UICONTROL Status] | Statut de la contrainte :<ul><li>**Actif :** (valeur par défaut) la contrainte est appliquée pendant les conditions et la période spécifiées.</li><li>**En pause :** la contrainte n’est pas appliquée.</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | Type de contrainte. Pour obtenir une description des types de contrainte et des réseaux publicitaires éligibles pour chacun d&#39;eux, reportez-vous à la rubrique [Types de contrainte](#constraint-types). |
| | [!UICONTROL Start Date] | Premier jour où la contrainte prend effet. La valeur par défaut est la date actuelle. Pour modifier la date, saisissez une date ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar-new.png "Calendrier") pour ouvrir le calendrier et sélectionner une date. |
| | [Date de fin] | Indique si la contrainte deviendra ineffective à une date spécifique. Pour appliquer la contrainte indéfiniment, par exemple lorsque l’unité d’offre est au cœur de la marque de l’entreprise, laissez le champ vide. Pour mettre fin à la contrainte à une date spécifique, saisissez une date ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar-new.png "Calendrier") pour ouvrir le calendrier et sélectionner une date. **Remarque :** la contrainte ne peut pas expirer avant demain. |
| | [!UICONTROL Set constraint options for Bid] | (Contraintes [!UICONTROL Bid] uniquement) Les paramètres incluent :<ul><li>**[!UICONTROL Min Bid]:** Offre de base minimale pour les unités d&#39;offre associées.</li><li>**[!UICONTROL Max Bid]:** enchère de base maximale pour les unités d&#39;enchère associées.</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | (Contraintes de [!UICONTROL Bid Shift] uniquement) Type et montant du changement d’offre à appliquer en continu à l’offre de base :<ul><li>*[!UICONTROL Increases]:* augmente les enchères d&#39;un pourcentage ou d&#39;une valeur monétaire spécifiés. Saisissez le montant à modifier, puis sélectionnez *$* ou *%*. Saisissez également un **[!UICONTROL Max Limit]**, qui est l&#39;offre la plus élevée possible (plafond) lorsque la contrainte est appliquée. **Remarque :** si l&#39;offre CPC actuelle est déjà égale ou supérieure à l&#39;[!UICONTROL Max Limit], la contrainte est ignorée et l&#39;offre n&#39;est pas modifiée.</li><li>*[!UICONTROL Decreases]:* réduit les enchères d&#39;un pourcentage ou d&#39;une valeur monétaire spécifiés. Saisissez le montant à modifier, puis sélectionnez *$ ou %*. Saisissez également un **[!UICONTROL Min Limit]**, qui est l&#39;offre la plus basse possible (plancher) lorsque la contrainte est appliquée. **Remarque :** si l&#39;offre CPC actuelle est déjà inférieure ou égale à l&#39;[!UICONTROL Min Limit], la contrainte est ignorée et l&#39;offre n&#39;est pas modifiée.</li></ul>**Remarques :**<ul><li>Un changement d&#39;offre entraînera une sur-utilisation ou une sous-utilisation des portefeuilles concernés par rapport au montant total causé par le changement d&#39;offre, quel que soit le paramètre du portefeuille pour « [!UICONTROL Spend Around Constraints] ».</li><li>Si vous spécifiez une date de fin pour la contrainte et que la fonctionnalité d’optimisation ajuste automatiquement les limites de dépenses pour les campagnes du portefeuille, les offres ne reviennent pas simplement aux montants d’origine après la date de fin, mais sont ajustées comme optimales.</li><li>Les décalages d&#39;offres ne sont pas appliqués aux unités d&#39;offres sans données suffisantes pour générer des modèles de coûts et de revenus.</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | (Contraintes de [!UICONTROL Incremental Bidding] uniquement) Une cible d’offre, ainsi que le montant et la fréquence des augmentations ou diminutions progressives de l’offre jusqu’à ce qu’elle atteigne la cible :<ul><li>**[!UICONTROL Bid target]:** Montant de l’enchère cible.</li><li>**[!UICONTROL Incrementally change bids by]** et **[Type] :** combien augmenter ou diminuer progressivement les offres et s’il faut modifier les offres en fonction d’une valeur de devise (**$**) ou d’un pourcentage (*%*).</li><li>**[!UICONTROL Every __ days]:** Fréquence d’incrémentation des enchères.</li></ul>Supposons, par exemple, que l’enchère en cours pour l’un des mots-clés soit de 100 cents et que vous souhaitiez modifier l’enchère de 10 % tous les jours jusqu’à ce que vous atteigniez l’objectif d’enchère de 500 cents. Au Jour 1 suivant la définition de la contrainte, l’enchère pour ce mot-clé est de 110 cents (enchère actuelle + 10 %). Au Jour 2, l’enchère est de 120 cents (enchère actuelle pour le Jour 1 + 20 %), etc. Cependant, si l&#39;objectif de l&#39;offre est de 50 cents et que les autres paramètres sont les mêmes, les offres diminuent progressivement jusqu&#39;à ce que l&#39;offre atteigne 50 cents. |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | (Contraintes de [!UICONTROL Search Engine Min Bid]) Utilise l’enchère minimale requise pour afficher une unité d’enchère sur la première page des résultats de recherche dans Google ([!UICONTROL Google First Page CPC]). Le cas échéant, saisissez une valeur **[!UICONTROL Min Bid]** et/ou une valeur **[!UICONTROL Max Bid]** pour définir la plage d&#39;offres éligibles pour la contrainte. Par exemple, si vous indiquez une [!UICONTROL Min Bid] de 2,50 USD et une [!UICONTROL Max Bid] de 4 USD, vous n&#39;enchérirez pas sur l&#39;unité d&#39;enchère si l&#39;enchère de la [!DNL Google Ads] première page est inférieure à 2,50 USD ou supérieure à 4 USD. |
| | [!UICONTROL Set constraint options for Impression Share] | (Contraintes [!UICONTROL Impression Share] uniquement) Les paramètres incluent :<ul><li>**[!UICONTROL Min Bid]** (Facultatif) Enchère de base minimale pour les unités d’offre associées.</li><li>**[!UICONTROL Max Bid]:** (facultatif) Enchère de base maximale pour les unités d&#39;enchères associées.</li><li>**[!UICONTROL Min Impression Share]:** taux d’impressions le plus bas, en pourcentage, qui déclenchera la contrainte pour les unités d’offre applicables. Il doit être entre 10 et 90. **Remarque :** lorsque la contrainte n&#39;est pas rentable, la fonctionnalité d&#39;optimisation peut la remplacer.</li><li>**[!UICONTROL Max Impression Share]:** pourcentage d&#39;impression le plus élevé, en pourcentage, qui déclenchera la contrainte pour les unités d&#39;offre applicables. Il doit être entre 10 et 90.**Remarque :** lorsque la contrainte n&#39;est pas rentable, la fonctionnalité d&#39;optimisation peut la remplacer.</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | Application de conditions à la contrainte :<ul><li>*[!UICONTROL No Condition]:* (valeur par défaut) La contrainte est appliquée sans condition pendant la période spécifiée.</li><li>*[!UICONTROL Satisfy]:* la contrainte n&#39;est appliquée que lorsque des conditions spécifiées sont remplies au cours d&#39;une période d&#39;évaluation des données spécifiée.</li></ul> |
| | [!UICONTROL Data Evaluation Period] | (Lorsque des conditions sont définies) Période pendant laquelle les données doivent être évaluées pour les critères spécifiés. Si vous sélectionnez *[!UICONTROL Custom date range],** spécifiez le **[!UICONTROL Start Date]** et la **[!UICONTROL End Date]** en saisissant chaque date au format `MM-DD-YYYY` (par exemple, 03-29-2026 pour le 29 mars 2026) ou en cliquant sur ![bouton Calendrier](/help/search-social-commerce/assets/calendar-new.png "bouton Calendrier") pour ouvrir le calendrier et sélectionner chaque date. |
| | [!UICONTROL When to Apply Constraints] | (Lorsque des conditions sont définies) Nombre de conditions de filtre qui doivent être remplies pour appliquer la contrainte :<ul><li>*[!UICONTROL Match All Filters]:* applique la contrainte lorsque chaque condition de filtre spécifiée est remplie.</li><li>*[!UICONTROL Match Any Filters]:* applique la contrainte lorsqu’au moins l’une des conditions de filtre spécifiées est remplie.</li></ul> |
| | [!UICONTROL Filters] | (Lorsque des conditions sont définies) Un ou plusieurs critères qui doivent être remplis. Pour créer un filtre, sélectionnez une propriété ou une mesure dans la liste. Pour les propriétés (telles que [!UICONTROL Channel Type]), sélectionnez les valeurs applicables dans la liste. Pour les mesures (telles que [!UICONTROL Clicks]), sélectionnez un opérateur, puis saisissez la valeur applicable. Par exemple, pour renvoyer uniquement les unités d’enchères comportant plus de 100 clics, sélectionnez **Clics**, **supérieur à**, puis saisissez `100` dans le champ de saisie.</li></ul> |

## Affecter des contraintes à la recherche d’unités d’enchères {#constraint-assign}

Vous pouvez appliquer des contraintes d’unité d’offre à n’importe quelle campagne, groupe publicitaire, mot-clé, emplacement, groupe de produits d’achat au niveau de l’unité (le niveau de subdivision le plus bas) ou cible de recherche dynamique.

Chaque entité ne peut avoir qu&#39;une seule contrainte. Vous pouvez affecter une seule contrainte à une ou plusieurs entités en même temps.

>[!NOTE]
>
>Si vous modifiez par la suite un mot-clé ou la copie d’une publicité, créant ainsi un nouveau mot-clé ou une nouvelle publicité, la contrainte n’est pas affectée à la nouvelle entité.

1. Dans le menu principal, ouvrez la vue de gestion correspondante.

   Par exemple, pour attribuer des contraintes au niveau de la campagne, accédez à [!UICONTROL Manage] > [!UICONTROL Campaigns].

   <!-- for [campaigns](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md), [ad groups](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md), [keywords](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md), or [placements](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md). And ADD LINKS WHEN AVAILABLE for shopping product groups and dynamic search targets. -->

1. (Facultatif) Filtrez la liste [à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou d’un en-tête de colonne [](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Cochez la case en regard de chaque entité à laquelle vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

## Annuler l’affectation des contraintes des unités d’enchères de recherche {#constraints-unassign}

**Remarque :** pour supprimer une contrainte, ce qui la rend indisponible pour une utilisation ultérieure, voir « [Modifier le statut des contraintes](#constraint-change-status). »

1. Dans le menu principal, ouvrez la vue de gestion correspondante.

   Par exemple, pour annuler l’affectation des contraintes au niveau de la campagne, accédez à [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. Cochez la case en regard de chaque entité à partir de laquelle vous annulerez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Gérer les affectations de contrainte pour les campagnes](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Gérer les affectations de contraintes pour les groupes publicitaires](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Gérer les affectations de contraintes pour les mots-clés](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
>* [Gérer les affectations de contrainte pour les emplacements](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)
>* [Le [!UICONTROL Constraint Report]](/help/search-social-commerce/reports/management/basic-advanced/constraint-report.md)
