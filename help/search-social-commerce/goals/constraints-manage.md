---
title: Gérer les contraintes pour les unités d’offres de recherche
description: Découvrez les contraintes permettant de restreindre les offres d’unités d’offre dans les campagnes CPC des portefeuilles hérités au niveau des mots-clés.
feature: Search Campaign Management, Search Optimization
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
subfeature_v2:
  - id: c800239a-06eb-4249-9aef-771973d24d35
    internal-label: Portfolios
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '2662'
ht-degree: 0%
---
# Gérer les contraintes pour les unités d’offres de recherche

*Applicable aux unités d&#39;enchères dans les campagnes CPC des portefeuilles hérités de niveau mot-clé uniquement*

Les contraintes d’unités d’offres sont des règles qui limitent les offres optimisées pour toutes les [unités d’offres](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html?lang=fr) avec les modèles de coût et de chiffre d’affaires associés à la contrainte.

## À propos des contraintes

Chaque contrainte s’applique à une devise spécifique et inclut éventuellement des conditions de déclenchement qui doivent être remplies au cours d’une période d’évaluation des données spécifiée pour que la règle s’applique. Les données à évaluer peuvent inclure le type de canal, le type de correspondance, les données de clic, les données de conversion ou les mesures dérivées. Par exemple, vous pouvez limiter les offres à une fourchette monétaire spécifique, augmenter ou diminuer les offres de façon continue d&#39;un montant spécifié ou encore les enchérir en fonction de l&#39;enchère moyenne pour le portefeuille. Chaque contrainte comporte une date de début applicable et expire à une date spécifique ou est appliquée indéfiniment.

Après avoir configuré une contrainte, vous pouvez l&#39;affecter à des unités d&#39;enchères spécifiques ou à toutes les unités d&#39;enchères au sein de groupes d&#39;annonces ou de campagnes spécifiques. Chaque unité d’offre peut avoir une contrainte. Les contraintes sont héritées par les entités enfants mais peuvent être remplacées. Une contrainte affectée au niveau le plus bas remplace toujours une contrainte affectée à un niveau parent. Lorsque vous affectez une contrainte à une unité d&#39;offre, l&#39;offre fonctionne dans les contraintes spécifiées pour cette unité d&#39;offre, quel que soit le chiffre d&#39;affaires généré par l&#39;unité d&#39;offre, lorsque l&#39;unité d&#39;offre comporte des modèles de coût et de chiffre d&#39;affaires.

>[!CAUTION]
>
>Lorsque vous affectez des contraintes à une unité d&#39;offre, vous remplacez la décision du système d&#39;optimisation des offres et assumez vous-même la responsabilité du retour sur investissement de cette unité d&#39;offre.

>[!NOTE]
>
>* Les contraintes actives limitent les enchères uniquement pour les unités d’offre affectées dans les portefeuilles optimisés au niveau des mots-clés hérités. Elles sont ignorées pour les unités d&#39;enchères qui se trouvent dans des portefeuilles hybrides, dans des portefeuilles actifs ou qui ne se trouvent pas dans des portefeuilles. **Conseil :** dans les paramètres du portefeuille, activez l&#39;option du portefeuille pour ajuster automatiquement les limites du budget de la campagne. La valeur « Multiple » recommandée est « 1 ».
>* Les contraintes d’offre sont ignorées pour les unités d’offre sans suffisamment de données pour générer des modèles de coût et de chiffre d’affaires.
>* (Campagnes avec une stratégie d’enchères CPC ou eCPC) Lorsqu’une contrainte d’offre entre en conflit avec une limite d’offre au niveau du portefeuille, la contrainte remplace la limite au niveau du portefeuille. Par exemple, si l’enchère minimale d’un portefeuille est de 5 USD, mais que vous limitez une unité d’enchère du portefeuille à une enchère minimale de 3 USD, l’unité d’enchère est de 3 USD ou plus. Toutefois, les dépenses globales pour les unités d&#39;enchères avec contraintes sont déterminées par le paramètre [&#x200B; « Dépenser en fonction des contraintes » du portefeuille](#spend-around-constraints).
>* Les contraintes opèrent sur l&#39;offre de base. Tout type d’ajustement de l’offre de base (tel que l’augmentation de l’offre pour les utilisateurs finaux sur des appareils mobiles) peut faire sortir l’offre de la plage autorisée pour la contrainte. Par exemple, si la contrainte nécessite un CPC maximum de 6 USD, l’enchère de base est déjà de 6 USD et le portefeuille optimise automatiquement les ajustements d’enchère pour les appareils mobiles à 50 %-60 %, alors le CPC maximum est de 9,00-9,60 USD, et non de 6 USD.

### Types de contrainte {#constraint-types}

* **[!UICONTROL Bid]:** Limite les enchères à une plage monétaire.

* **[!UICONTROL Bid Shift]:** modifie en permanence les enchères optimisées pour toutes les unités d’enchères associées d’un montant spécifié, dans les limites d’enchères. Un changement d’offre entraîne une sur-dépense ou une sous-dépense des portefeuilles concernés par le montant total provoqué par le changement d’offre, quel que soit le paramètre du portefeuille pour « Dépenser en fonction des contraintes ». Remarque : Si l&#39;offre CPC actuelle est déjà supérieure ou égale à l&#39;offre maximale, ou inférieure ou égale à l&#39;offre minimale, la contrainte est ignorée et l&#39;offre n&#39;est pas modifiée. En outre, les contraintes de changement d&#39;offre ne sont pas appliquées aux unités d&#39;offre sans suffisamment de données pour générer des modèles de coût et de chiffre d&#39;affaires.

* **[!UICONTROL Incremental Bidding]:** (applicable uniquement aux mots-clés sans impressions) Augmente ou réduit l’offre de manière incrémentielle à un taux spécifié jusqu’à ce que l’offre atteigne une cible désignée.

* **[!UICONTROL Search Engine Min Bid]:** ([!DNL Google Ads] comptes uniquement) Utilise les enchères CPC minimales déterminées par le moteur de recherche comme enchères minimales. Lorsque le moteur de recherche modifie ses enchères minimales, votre enchère change en conséquence. Vous pouvez éventuellement spécifier des limites d&#39;enchères supplémentaires pour toutes les unités d&#39;enchères associées.

* **[!UICONTROL Impression Share]:** ([!DNL Google Ads] et [!DNL Microsoft Advertising] campagnes CPC avec correspondance exacte uniquement) Limite les enchères à une plage monétaire lorsque les annonces sont comprises entre un partage d’impression minimum et maximum. **Remarque :** Lorsque la contrainte n&#39;est pas rentable, la fonctionnalité d&#39;optimisation peut la remplacer.

### Quand appliquer des contraintes

Voici quelques raisons de limiter les unités d&#39;enchères :

* Exposer rapidement les mots-clés et les publicités non testés.

* Pour atténuer les risques liés aux nouveaux portfolios, comptes, campagnes et groupes publicitaires. Par exemple, avant de lancer un portefeuille, vous pouvez définir des enchères maximales sur les unités d’enchères à trafic élevé, puis augmenter progressivement les valeurs chaque jour. Cela permet au modèle d&#39;offres de s&#39;ajuster chaque jour sans risque d&#39;augmentation importante des offres.

* Pour vous assurer que les mots-clés avec des taux de conversion élevés ne sont pas utilisés à la baisse.

* Pour enchérir sur des conditions spécifiques qui sont essentielles pour votre marque ou lors de promotions.

### Où afficher des informations sur les contraintes dans l’interface utilisateur

Outre l’ouverture de la vue [[!UICONTROL Constraints]](#constraints-view), vous pouvez également afficher les informations relatives à vos contraintes des manières suivantes :

* Toutes vos contraintes sont des valeurs de libellé pour une [classification de libellé](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/legacy-ui/campaign-management/label-classifications/classification-about.html) unique appelée « [!UICONTROL Constraints] ».

  * « [!UICONTROL Constraints] » est inclus dans la liste « [!UICONTROL Classifications] » dans vos paramètres d’affichage par défaut et personnalisés, ainsi que dans les rapports planifiés. Vous pouvez ajouter la colonne où vous souhaitez voir les contraintes affectées aux entités pertinentes.

  * Lorsque vous téléchargez une feuille d’envoi groupé, « [!UICONTROL Constraints] » est répertorié sous la colonne « [!UICONTROL Classifications] » pour les entités applicables dans la boîte de dialogue [!UICONTROL Download Bulksheet]. Lorsque vous incluez la colonne , la feuille d’envoi groupé téléchargée inclut toutes les contraintes affectées aux entités pertinentes.

  La classification [!UICONTROL Constraints] n’est pas incluse dans la vue [!UICONTROL Label Classifications] - la vue [!UICONTROL Constraints] est distincte. La classification [!UICONTROL Constraints] n’est pas non plus incluse dans la limite de classification de 30 libellés.

* [Le [!UICONTROL Constraint Report]](/help/search-social-commerce/reports/management/basic-advanced/constraint-report.md) inclut les données de coût, de clic et (éventuellement) de conversion pour les contraintes qui utilisent l’architecture de classification de libellés.

### La vue [!UICONTROL Constraints] {#constraints-view}

La vue [!UICONTROL Goals] > [!UICONTROL Constraints] répertorie toutes vos contraintes. Les colonnes disponibles incluent le statut de la contrainte, le type de contrainte, les dates de début et de fin, le nombre de campagnes, de groupes publicitaires, de mots-clés, d&#39;annonces, d&#39;emplacements, de cibles automatiques et de groupes de produits auxquels la contrainte est associée, les impressions, les clics et les données de coût, ainsi que les données de chiffre d&#39;affaires pour toutes les mesures de conversion visibles.<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>Les données de performances d&#39;une ligne dans la vue [!UICONTROL Constraints] peuvent ne pas correspondre aux données de performances de l&#39;entité de niveau supérieur à laquelle la contrainte est affectée. Étant donné qu’une contrainte attribuée au niveau le plus bas remplace toujours une contrainte attribuée au niveau parent, une contrainte attribuée à une campagne ou à un groupe publicitaire peut ne pas rester attribuée aux groupes publicitaires et mots-clés enfants. Par exemple, si la campagne A se voit attribuer la contrainte A, tous les groupes publicitaires et tous les mots-clés de la campagne A héritent automatiquement de la contrainte A. Cependant, ces groupes publicitaires et mots-clés pourraient être affectés ultérieurement à d&#39;autres contraintes, telles que la contrainte B, et ils perdraient alors leur association avec la contrainte A.

>[!NOTE]
>
>Affectez des contraintes aux unités d&#39;enchères et annulez leur affectation dans la vue de gestion des entités appropriée (par exemple dans la vue [!UICONTROL Campaigns] pour les contraintes au niveau de la campagne).

#### Actions disponibles

* [Créer une contrainte](#constraint-create).

* [Modifier les paramètres de contrainte](#constraint-edit).

* [Modifier le statut des contraintes](#constraint-change-status).

## Créer une contrainte {#constraint-create}

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. Dans la barre d&#39;outils supérieure droite au-dessus du tableau de données, cliquez sur **[!UICONTROL Create Constraint]**.

1. Saisissez les [paramètres de contrainte](#constraint-settings).

   Pour passer de l’onglet [!UICONTROL Constraint Type] à l’onglet [!UICONTROL Conditions], cliquez sur l’onglet que vous souhaitez ouvrir ou cliquez sur les boutons [!UICONTROL Next] et [!UICONTROL Back].

1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

1. Cliquez sur **[!UICONTROL Save]**.

Une fois une contrainte créée, vous pouvez [l&#39;affecter](#constraint-assign) à des campagnes, des groupes publicitaires, des mots-clés, des emplacements et des groupes de produits au niveau de l&#39;unité.

## Modifier les paramètres de contrainte {#constraint-edit}

Vous pouvez modifier les paramètres d&#39;une contrainte à la fois.

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Facultatif) Filtrez la liste [&#x200B; à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou d’un en-tête de colonne [&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Cochez la case en regard de la contrainte à modifier.

1. Dans la barre d’outils des actions en bloc, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier").

1. Modifiez les [paramètres de contrainte](#constraint-settings).

   Pour passer de l’onglet [!UICONTROL Constraint Type] à l’onglet [!UICONTROL Conditions], cliquez sur l’onglet que vous souhaitez ouvrir ou cliquez sur les boutons [!UICONTROL Next] et [!UICONTROL Back].

1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

1. Cliquez sur **[!UICONTROL Save]**.

## Modifier le statut des contraintes {#constraint-change-status}

Vous pouvez suspendre toute contrainte active pour la désactiver. Vous pouvez l&#39;activer ultérieurement en redéfinissant le statut sur *actif*.

Vous pouvez également supprimer une contrainte, ce qui supprime toutes les associations avec les composants de compte et rend la contrainte indisponible pour une utilisation ultérieure. Les données de rapport pour la contrainte ne sont plus disponibles. **Remarque :** Pour dissocier simplement une contrainte d’un composant de compte, voir « [Supprimer des contraintes des unités d’enchères de recherche](#constraints-unassign) ».

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Constraints]**.

1. (Facultatif) Filtrez la liste [&#x200B; à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou d’un en-tête de colonne [&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Cochez la case en regard de chaque contrainte dont vous souhaitez modifier le statut.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, voir « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

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
| | [!UICONTROL Status] | Statut de la contrainte :<ul><li>**Actif :** (valeur par défaut) La contrainte est appliquée pendant les conditions et la période spécifiées.</li><li>**En pause :** La contrainte n&#39;est pas appliquée.</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | Type de contrainte. Pour les descriptions des types de contraintes et des réseaux publicitaires éligibles pour chacun, voir « [Types de contraintes](#constraint-types) ». |
| | [!UICONTROL Start Date] | Premier jour où la contrainte prend effet. La valeur par défaut est la date actuelle. Pour modifier la date, saisissez une date ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar-new.png "Calendrier") pour ouvrir le calendrier et sélectionner une date. |
| | [Date De Fin] | Indique si la contrainte deviendra ineffective à une date spécifique. Pour appliquer la contrainte indéfiniment, par exemple lorsque l’unité d’offre est au cœur de la marque de l’entreprise, laissez le champ vide. Pour mettre fin à la contrainte à une date spécifique, saisissez une date ou cliquez sur ![Calendrier](/help/search-social-commerce/assets/calendar-new.png "Calendrier") pour ouvrir le calendrier et sélectionner une date. **Remarque :** La contrainte ne peut pas expirer avant demain. |
| | [!UICONTROL Set constraint options for Bid] | ([!UICONTROL Bid] contraintes uniquement) Les paramètres incluent :<ul><li>**[!UICONTROL Min Bid]:** Offre de base minimale pour les unités d&#39;offre associées.</li><li>**[!UICONTROL Max Bid]:** enchère de base maximale pour les unités d&#39;enchère associées.</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | ([!UICONTROL Bid Shift] contraintes uniquement) Le type et le montant du changement d’offre à appliquer en continu à l’offre de base :<ul><li>*[!UICONTROL Increases]:* augmente les enchères d&#39;un pourcentage ou d&#39;une valeur de devise spécifié. Saisissez le montant à modifier, puis sélectionnez *$* ou *%*. Saisissez également un **[!UICONTROL Max Limit]**, qui est l’enchère la plus élevée possible (plafond) lorsque la contrainte est appliquée. **Remarque :** Si l&#39;enchère CPC actuelle est déjà égale ou supérieure à [!UICONTROL Max Limit], la contrainte est ignorée et l&#39;enchère n&#39;est pas modifiée.</li><li>*[!UICONTROL Decreases]:* réduit les enchères d&#39;un pourcentage ou d&#39;une valeur de devise spécifié. Saisissez le montant à modifier, puis sélectionnez *$ ou %*. Saisissez également un **[!UICONTROL Min Limit]**, qui est l’enchère la plus basse possible (plancher) lorsque la contrainte est appliquée. **Remarque :** Si l&#39;offre CPC actuelle est déjà inférieure ou égale à [!UICONTROL Min Limit], la contrainte est ignorée et l&#39;offre n&#39;est pas modifiée.</li></ul>**Notes :**<ul><li>Un changement d&#39;enchères entraînera une sur-utilisation ou une sous-utilisation des portefeuilles concernés par rapport au montant total causé par le changement d&#39;enchères, quel que soit le paramètre du portefeuille pour « [!UICONTROL Spend Around Constraints] ».</li><li>Si vous spécifiez une date de fin pour la contrainte et que la fonctionnalité d’optimisation ajuste automatiquement les limites de dépenses pour les campagnes du portefeuille, les offres ne reviennent pas simplement aux montants d’origine après la date de fin, mais sont ajustées comme optimales.</li><li>Les décalages d&#39;offres ne sont pas appliqués aux unités d&#39;offres sans données suffisantes pour générer des modèles de coûts et de revenus.</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | ([!UICONTROL Incremental Bidding] contraintes uniquement) Une cible d’offre, ainsi que le montant et la fréquence d’augmentation ou de diminution incrémentielle de l’offre jusqu’à ce qu’elle atteigne la cible :<ul><li>**[!UICONTROL Bid target]:** Montant de l’enchère cible.</li><li>**[!UICONTROL Incrementally change bids by]** et **[Type] :** Montant de l&#39;augmentation ou de la diminution incrémentielle des offres, et s&#39;il faut modifier les offres en fonction d&#39;une valeur de devise (**$**) ou d&#39;un pourcentage (*%*).</li><li>**[!UICONTROL Every __ days]:** Fréquence d&#39;incrémentation des enchères.</li></ul>Supposons, par exemple, que l’enchère en cours pour l’un des mots-clés soit de 100 cents et que vous souhaitiez modifier l’enchère de 10 % tous les jours jusqu’à ce que vous atteigniez l’objectif d’enchère de 500 cents. Au Jour 1 suivant la définition de la contrainte, l’enchère pour ce mot-clé est de 110 cents (enchère actuelle + 10 %). Au Jour 2, l’enchère est de 120 cents (enchère actuelle pour le Jour 1 + 20 %), etc. Cependant, si l&#39;objectif de l&#39;offre est de 50 cents et que les autres paramètres sont les mêmes, les offres diminuent progressivement jusqu&#39;à ce que l&#39;offre atteigne 50 cents. |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | ([!UICONTROL Search Engine Min Bid] contraintes) Utilise l’enchère minimale requise pour afficher une unité d’enchère sur la première page des résultats de recherche sur Google ([!UICONTROL Google First Page CPC]). Vous pouvez éventuellement saisir une valeur **[!UICONTROL Min Bid]** et/ou une valeur **[!UICONTROL Max Bid]** pour définir la plage d’offres éligibles pour la contrainte. Par exemple, si vous spécifiez un [!UICONTROL Min Bid] de 2,50 USD et un [!UICONTROL Max Bid] de 4 USD, vous ne pourrez pas enchérir sur l’entité d’enchères si l’enchère de la première page [!DNL Google Ads] est inférieure à 2,50 USD ou supérieure à 4 USD. |
| | [!UICONTROL Set constraint options for Impression Share] | ([!UICONTROL Impression Share] contraintes uniquement) Les paramètres incluent :<ul><li>**[!UICONTROL Min Bid]** (Facultatif) Enchère de base minimale pour les unités d&#39;enchères associées.</li><li>**[!UICONTROL Max Bid]:** (facultatif) enchère de base maximale pour les unités d’enchère associées.</li><li>**[!UICONTROL Min Impression Share]:** taux d&#39;impressions le plus bas, en pourcentage, qui déclenchera la contrainte pour les unités d&#39;enchères applicables. Il doit être entre 10 et 90. **Remarque :** Lorsque la contrainte n&#39;est pas rentable, la fonctionnalité d&#39;optimisation peut la remplacer.</li><li>**[!UICONTROL Max Impression Share]:** taux d&#39;impressions le plus élevé, en pourcentage, qui déclenchera la contrainte pour les unités d&#39;enchères applicables. Il doit être entre 10 et 90. **Remarque :** Lorsque la contrainte n&#39;est pas rentable, la fonctionnalité d&#39;optimisation peut la remplacer.</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | Application de conditions à la contrainte :<ul><li>*[!UICONTROL No Condition]:* (valeur par défaut) La contrainte est appliquée sans condition pendant la période spécifiée.</li><li>*[!UICONTROL Satisfy]:* La contrainte n&#39;est appliquée que lorsque des conditions spécifiées sont remplies au cours d&#39;une période d&#39;évaluation des données spécifiée.</li></ul> |
| | [!UICONTROL Data Evaluation Period] | (Lorsque des conditions sont définies) Période pendant laquelle les données doivent être évaluées pour les critères spécifiés. Si vous sélectionnez *[!UICONTROL Custom date range],**&#x200B; spécifiez le &#x200B;** [!UICONTROL Start Date] **&#x200B; et le &#x200B;** [!UICONTROL End Date]** en saisissant chaque date au format `MM-DD-YYYY` (par exemple, 03-29-2026 pour le 29 mars 2026) ou en cliquant sur ![Bouton Calendrier](/help/search-social-commerce/assets/calendar-new.png "Bouton Calendrier") pour ouvrir le calendrier et sélectionner chaque date. |
| | [!UICONTROL When to Apply Constraints] | (Lorsque des conditions sont définies) Nombre de conditions de filtre qui doivent être remplies pour appliquer la contrainte :<ul><li>*[!UICONTROL Match All Filters]:* applique la contrainte lorsque chaque condition de filtre spécifiée est remplie.</li><li>*[!UICONTROL Match Any Filters]:* applique la contrainte lorsqu&#39;au moins une des conditions de filtre spécifiées est remplie.</li></ul> |
| | [!UICONTROL Filters] | (Lorsque des conditions sont définies) Un ou plusieurs critères qui doivent être remplis. Pour créer un filtre, sélectionnez une propriété ou une mesure dans la liste. Pour les propriétés (telles que [!UICONTROL Channel Type]), sélectionnez les valeurs applicables dans la liste. Pour les mesures (telles que [!UICONTROL Clicks]), sélectionnez un opérateur, puis saisissez la valeur applicable. Par exemple, pour renvoyer uniquement les unités d’enchères comportant plus de 100 clics, sélectionnez **Clics**, **supérieur à**, puis saisissez `100` dans le champ de saisie.</li></ul> |

## Affecter des contraintes à la recherche d’unités d’enchères {#constraint-assign}

Vous pouvez appliquer des contraintes d’unité d’enchères à n’importe quelle campagne, groupe publicitaire, mot-clé, emplacement ou cible de recherche dynamique (ciblage automatique).

Chaque entité ne peut avoir qu&#39;une seule contrainte. Vous pouvez affecter une seule contrainte à une ou plusieurs entités en même temps.

>[!NOTE]
>
>* Si vous modifiez par la suite un mot-clé ou la copie d’une publicité, créant ainsi un nouveau mot-clé ou une nouvelle publicité, la contrainte n’est pas affectée à la nouvelle entité.
>* Voir les mêmes instructions dans la vue [[!UICONTROL Campaigns] &#x200B;](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-constraints), la vue [[!UICONTROL Ad Groups] &#x200B;](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md#ad-group-constraints), la vue [[!UICONTROL Keywords] &#x200B;](/help/search-social-commerce/manage/keywords/keyword-manage.md#keyword-constraint-assign) ou la vue [[!UICONTROL Placements] &#x200B;](/help/search-social-commerce/targeting/placement-manage.md#placement-constraint-assign). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. Dans le menu principal, ouvrez la vue de gestion correspondante.

   Par exemple, pour attribuer des contraintes au niveau de la campagne, accédez à [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. (Facultatif) Filtrez la liste [&#x200B; à partir de la barre d’outils](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) ou d’un en-tête de colonne [&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Cochez la case en regard de chaque entité à laquelle vous affecterez une seule contrainte.

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Sélectionnez la contrainte.

1. Cliquez sur **[!UICONTROL Assign Now]**.

## Annuler l’affectation des contraintes des unités d’enchères de recherche {#constraints-unassign}

>[!NOTE]
>
>* Pour supprimer une contrainte, ce qui la rend indisponible pour une utilisation ultérieure, voir « [Modifier le statut des contraintes](#constraint-change-status) ».
>* Voir les mêmes instructions dans la vue [[!UICONTROL Campaigns] &#x200B;](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-constraints), la vue [[!UICONTROL Ad Groups] &#x200B;](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md#ad-group-constraints), la vue [[!UICONTROL Keywords] &#x200B;](/help/search-social-commerce/manage/keywords/keyword-manage.md#keyword-constraint-unassign) ou la vue [[!UICONTROL Placements] &#x200B;](/help/search-social-commerce/targeting/placement-manage.md#placement-constraint-unassign). <!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. Dans le menu principal, ouvrez la vue de gestion correspondante.

   Par exemple, pour annuler l’affectation des contraintes au niveau de la campagne, accédez à [!UICONTROL Manage] > [!UICONTROL Campaigns].

1. Cochez la case en regard de chaque entité à partir de laquelle vous annulerez l’affectation des contraintes.

1. Dans la barre d’outils des actions en bloc, cliquez sur **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Cliquez sur **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Gérer les affectations de contrainte pour les campagnes](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-constraints)
>* [Gérer les affectations de contraintes pour les groupes publicitaires](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md#ad-group-constraints)
>* [Gérer les affectations de contraintes pour les mots-clés](/help/search-social-commerce/manage/keywords/keyword-manage.md#keyword-constraints)
>* [Gérer les affectations de contraintes pour les emplacements](/help/search-social-commerce/targeting/placement-manage.md#placement-constraints)
>* [Le [!UICONTROL Constraint Report]](/help/search-social-commerce/reports/management/basic-advanced/constraint-report.md)
