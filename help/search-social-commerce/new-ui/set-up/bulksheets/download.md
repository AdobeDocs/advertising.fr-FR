---
title: (Nouvelle interface utilisateur) Télécharger/créer un fichier de feuille d’envoi groupé
description: Découvrez comment créer des fichiers de feuilles d’envoi groupé en téléchargeant les données de compte pour vos réseaux publicitaires dans la nouvelle interface utilisateur de Search, Social et Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 1637
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Télécharger/créer un fichier de feuille d’envoi groupé

Vous pouvez créer des feuilles d’envoi groupé à l’aide de paramètres personnalisés pour un ou plusieurs comptes sur un ou plusieurs [réseaux publicitaires pris en charge](about.md#bulksheet-functionality-by-network). Les feuilles d’envoi groupé incluent des données dans Search, Social et Commerce.

Pour les campagnes synchronisées, vous pouvez éventuellement effectuer une synchronisation avec le réseau publicitaire avant de télécharger les données afin de vous assurer que les modifications récentes des données du côté du réseau publicitaire sont incluses. Pour tous les réseaux publicitaires, vous pouvez éventuellement générer de nouvelles URL de suivi des clics à inclure dans le fichier .

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Dans la barre d’outils, cliquez sur **[!UICONTROL Bulk Operations]** \> **[!UICONTROL Download Bulksheet]**.

1. Spécifiez les paramètres [bulksheet](#bulksheet-settings) :

   1. Dans l’onglet **[!UICONTROL Selections]** , sélectionnez les comptes, campagnes ou groupes publicitaires à inclure et configurez les options de la feuille d’envoi groupé.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Rows and Columns]** , spécifiez les composants de compte et les statuts de composant pour lesquels inclure des lignes dans la feuille d’envoi groupé, puis spécifiez les colonnes à inclure pour chaque composant sélectionné.

      Pour obtenir la liste des lignes de feuilles d&#39;envoi groupé disponibles, reportez-vous à « [Lignes de feuilles d&#39;envoi groupé par réseau publicitaire](#bulksheet-rows-by-ad-network) ».

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Filters]** , puis spécifiez les critères pour les campagnes spécifiques, les groupes publicitaires, les annonces/contenus publicitaires, les mots-clés, les emplacements et autres entités à inclure dans la feuille d’envoi groupé.

1. Cliquez sur **[!UICONTROL Download]**.

Lorsque la tâche commence, la fenêtre affiche une notification mais reste ouverte afin que vous puissiez continuer à créer des feuilles d’envoi groupé supplémentaires si nécessaire. Une fois le fichier créé, vous recevez une notification par e-mail avec un lien vers le fichier ; selon la quantité de données compilées, la notification peut prendre plusieurs minutes ou plus. Si la génération du fichier échoue, un fichier d’erreur est répertorié dans la vue Feuilles d’envoi groupé et vous recevez une notification par e-mail avec un lien vers le fichier d’erreur.

## Paramètres des feuilles d’envoi groupé {#bulksheet-settings}

### Onglet Sélections {#bulksheet-selections-settings}

**\[Sélection de compte, de campagne et de groupe publicitaire\]**

Développez la hiérarchie du réseau et des comptes, puis cochez la case en regard de chaque compte, campagne ou groupe publicitaire dont les données doivent être incluses dans la feuille d’envoi groupé :

* Pour inclure toutes les campagnes et tous les groupes publicitaires pour un compte, cochez la case en regard du nom du compte.

* Pour inclure des campagnes spécifiques, développez le compte , puis cochez la case en regard de chaque campagne à inclure. Pour inclure des groupes publicitaires spécifiques, développez davantage une campagne et cochez la case en regard de chaque groupe publicitaire.

>[!NOTE]
>
>* Une seule feuille d’envoi groupé peut s’appliquer à plusieurs comptes au sein de plusieurs réseaux publicitaires. Les colonnes spécifiques au réseau publicitaire sont libellées dans des feuilles d’envoi groupé avec le nom du réseau publicitaire (par exemple, « Opérateurs mobiles (Google Ads) »).
>* Pour voir le type de composant d’un élément, placez le curseur dessus.
>* Par défaut, seuls les comptes actifs et activés et leurs composants actifs sont répertoriés.

**[!UICONTROL Generate Tracking URLs]:** (facultatif) Inclut des modèles de tracking et des suffixes de page de destination (pour les réseaux publicitaires applicables) dans les comptes avec modèles de tracking, ou des URL de destination avec codes de tracking incorporés dans les comptes avec URL de destination, pour les mots-clés, les annonces, les emplacements, les liens de site et les groupes de produits [!DNL Google Ads] dans la feuille d’envoi groupé. Par défaut, cette option est sélectionnée.

Lorsque cette option est sélectionnée, les URL sont générées en fonction des paramètres de la section [!UICONTROL Campaign Tracking] des paramètres du compte ou des paramètres de la campagne. Par défaut, si les URL de tracking existent déjà, elles ne sont pas régénérées, sauf si de nouvelles URL sont nécessaires (par exemple, si le type de correspondance de mot-clé, le texte de l’annonce ou les paramètres de tracking du compte ont changé).

>[!NOTE]
>
>* Si l’annonceur utilise le suivi des conversions Adobe Advertising et que le compte approprié n’est pas configuré pour générer et charger automatiquement des URL de suivi, vous devez générer de nouvelles URL de suivi lorsque les URL de base ont été modifiées.
>* Si vous ne sélectionnez pas cette option, vous pourrez toujours générer des URL de tracking ultérieurement, lors du chargement ou de la publication du fichier.

**[!UICONTROL Perform pre-sync]:** (facultatif) indique à Search, Social et Commerce de synchroniser ses fichiers avec les campagnes spécifiées afin de s’assurer que toutes les données sont identiques. Par défaut, cette option n’est pas sélectionnée.

>[!NOTE]
>
>Search, Social et Commerce se synchronise automatiquement avec le réseau publicitaire une fois par jour, chaque fois qu’il détecte une nouvelle campagne sur le réseau publicitaire et chaque fois que vous modifiez les données de la campagne à partir de Search, Social et Commerce. Sélectionnez cette option si vous pensez que des modifications récentes apportées aux données de la campagne ou du compte ont été effectuées directement dans le réseau publicitaire ou à l’aide de l’éditeur de bureau du réseau publicitaire. La création de feuilles d&#39;envoi groupé prend plus de temps lorsque vous sélectionnez cette option.

**[!UICONTROL Bulksheet Name]:** nom de la nouvelle feuille d’envoi groupé et type de fichier. Par défaut, le fichier est créé au format de valeurs séparées par des tabulations et nommé comme suit :

* (Pour tous les comptes d’un réseau publicitaire) `<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (Pour un seul compte) `<account name>_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* (Pour les comptes multiples) `MultipleAccounts_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`

Vous pouvez renommer le fichier. Le nom ne peut pas contenir les caractères suivants : `# % & * | \ : " < > . ? /`

Vous pouvez éventuellement modifier le type de fichier. Les options incluent *[!UICONTROL .tsv]* (pour les valeurs séparées par des tabulations), *[!UICONTROL .txt (unicode)]* (pour le texte ASCII conforme à Unicode), *[!UICONTROL .csv]* (pour les valeurs séparées par des virgules) ou *[!UICONTROL .zip]* (pour le format ZIP compressé, qui est décompressé en fichier TSV).

>[!TIP]
>
>Pour les feuilles d’envoi groupé contenant des caractères internationaux, utilisez le format TSV ou TXT.

### Onglet Lignes et Colonnes {#bulksheet-rows-columns-settings}

**[!UICONTROL Bulksheet Rows]:** les entités et leurs statuts correspondants à inclure en tant que lignes de données dans la feuille d’envoi groupé, avec une ligne par entrée. Par exemple, si vous incluez des campagnes actives, la feuille d’envoi groupé comprend une ligne par campagne active. Seules les entités sélectionnées avec les statuts sélectionnés sont incluses. Les valeurs par défaut sont présélectionnées en fonction du réseau publicitaire spécifié. Par défaut, seules les instances actives des entités sélectionnées sont incluses.

Pour ajouter ou supprimer des entités, activez ou désactivez les cases à cocher en regard des entités. Pour ajouter ou supprimer des statuts pour une entité, cliquez sur le menu Statut en regard de l’entité, puis activez ou désactivez les cases à cocher correspondant aux statuts applicables.

Pour obtenir la liste des lignes disponibles par réseau publicitaire, reportez-vous à « [Lignes de feuille d’envoi groupé par réseau publicitaire](#bulksheet-rows-by-ad-network) ».

**[!UICONTROL Cascading Status Hierarchy]:** filtre les entités enfant sur celles ayant les statuts d’entité parent spécifiés, à l’aide d’une opération AND. Par exemple, si vous sélectionnez « Campagne active », « Groupe publicitaire actif » et « Mot-clé actif », la feuille d’envoi groupé inclut uniquement les mots-clés actifs dans les groupes publicitaires actifs des campagnes actives.

Si vous ne sélectionnez pas cette option, le statut parent n’est pas pris en compte et le filtre utilise une opération OR. Par exemple, si vous sélectionnez « Campagne active », « Groupe publicitaire actif » et « Mot-clé actif », la feuille d’envoi groupé inclut toutes les campagnes actives ; tous les groupes publicitaires actifs, quel que soit le statut de la campagne parente ; et tous les mots-clés actifs, quel que soit le statut de la campagne parente et du groupe publicitaire.

**[!UICONTROL Bulksheet Columns]:** les colonnes à inclure dans le fichier de feuille d’envoi groupé téléchargé :

* *[!UICONTROL AMO ID]:* (Obligatoire si « [!UICONTROL SE ID] » n’est pas sélectionné) Inclut un identifiant unique généré par [!DNL Adobe] pour chaque entité/ligne. Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne la publie pas sur le réseau publicitaire. Par la suite, vous pourrez modifier les données de l&#39;entité en utilisant le [!UICONTROL AMO ID] comme identifiant, plutôt que l&#39;identifiant de l&#39;entité et les identifiants de l&#39;entité parent.

* *[!UICONTROL SE ID]:* (Obligatoire si « [!UICONTROL AMO ID] » n’est pas sélectionné) Inclut l’identifiant unique du réseau publicitaire pour chaque colonne incluse et ses entités parentes. Par la suite, si vous modifiez les données d’une entité en utilisant le [!UICONTROL SE ID] comme identifiant, vous devez également inclure des lignes pour les entités parents (y compris leurs valeurs [!UICONTROL SE ID]).

* *[!UICONTROL Platform]:* comprend une colonne [!UICONTROL Platform] au début de chaque ligne pour indiquer la plateforme publicitaire (telle que « Baidu »).

* *[!UICONTROL Acct Name]:* (Obligatoire si « [!UICONTROL AMO ID] » n’est pas sélectionné) Inclut le nom du compte réseau publicitaire pour chaque entité/ligne.

* \[Colonnes spécifiques à l’entité\] : pour inclure toutes les colonnes, aucune ou uniquement les colonnes sélectionnées relatives à chaque entité sélectionnée dans [!UICONTROL Bulksheet Rows], cliquez sur ![Flèche droite](/help/search-social-commerce/assets/compressed-item.png "Flèche droite") en regard du nom de l’entité pour le développer, puis activez ou désactivez les cases à cocher de chaque colonne. Par défaut, toutes les colonnes pertinentes sont incluses pour chaque ligne d&#39;entité sélectionnée.

>[!TIP]
>
>Veillez à inclure des colonnes adéquates pour identifier l&#39;élément dans chaque ligne du fichier de feuille d&#39;envoi groupé. Par exemple, si vous incluez des lignes de mots-clés par sélecteur de [!UICONTROL Bulksheet Rows], mais que vous excluez toutes les colonnes liées aux mots-clés, la feuille d’envoi groupé obtenue inclut une ligne pour chaque instance de mot-clé, sans moyen d’identifier quelle instance de mot-clé appartient à une ligne spécifique. Dans ce cas, vous ne pouvez pas utiliser la feuille d’envoi groupé pour mettre à jour les données à moins d’ajouter manuellement la colonne d’identifiant et les valeurs appropriées.

### Onglet Filtres {#bulksheet-filters-settings}

Critères pour les campagnes, groupes publicitaires, annonces/contenus publicitaires, mots-clés et/ou emplacements spécifiques à inclure dans la feuille d’envoi groupé :

1. Sélectionnez un paramètre (nom ou ID d’entité ; ou tout élément d’un élément créatif, d’un mot-clé ou d’un emplacement), sélectionnez un opérateur, puis saisissez la valeur applicable.

   Par exemple, pour renvoyer uniquement les annonces avec « chaussures » dans le titre d’un compte [!DNL Google Ads], sélectionnez *[!UICONTROL Headline]*, *[!UICONTROL contains]*, puis saisissez `shoes` dans le champ de saisie.

1. (Pour appliquer des filtres supplémentaires) Pour chaque filtre supplémentaire, cliquez sur **[!UICONTROL +Add Filter]**, sélectionnez **[!UICONTROL AND]** ou **[!UICONTROL OR]**, sélectionnez un élément publicitaire ou un mot-clé et un opérateur, puis saisissez la valeur applicable.

## Lignes de feuilles d&#39;envoi groupé par réseau publicitaire {#bulksheet-rows-by-ad-network}

| Ligne de feuille d&#39;envoi groupé | [!DNL Baidu] | [!DNL Google Ads] | [!DNL LY Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo DSP] | [!DNL Yahoo Native] | [!DNL Yandex] | Remarques |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui | — |
| [!UICONTROL Adgroup] | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui | Oui | — |
| [!UICONTROL Creative] *ou* [!UICONTROL Creative (except RSA)] | Oui | Oui | Oui | Oui | — | — | Oui | Oui | Oui | ([!DNL Google Ads]) Utilisez pour tous les types d’annonces, à l’exception des annonces en responsive design de recherche, disponibles dans la ligne [!UICONTROL Responsive Search Ad]. |
| [!UICONTROL Responsive Search Ad] | — | Oui | — | Oui | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Oui | Oui | Oui | Oui | Oui | Oui | — | Oui | Oui | À utiliser uniquement pour les mots-clés non négatifs. Pour afficher les mots-clés négatifs créés au niveau de la campagne ou du groupe publicitaire, utilisez la ligne [!UICONTROL Campaign Negative Keyword] ou [!UICONTROL Adgroup Negative Keyword], le cas échéant. |
| [!UICONTROL Promoted Pin] | — | — | — | — | — | Oui | — | — | — | — |
| [!UICONTROL Placement] | — | Oui | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Oui | — | Oui | — | — | — | — | — | Utilisez pour les cibles de recherche dynamique d’un groupe publicitaire. |
| [!UICONTROL Shopping Product Group] | — | Oui | — | Oui | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Oui | — | Oui | — | — | — | Oui | — | — |
| [!UICONTROL Campaign Negative Keyword] | Oui | Oui | Oui | Oui | — | — | — | Oui | — | À utiliser uniquement pour les mots-clés négatifs créés au niveau de la campagne ou du groupe publicitaire. Pour afficher les mots-clés non négatifs, utilisez la ligne [!UICONTROL Keyword] si disponible. |
| [!UICONTROL Campaign Negative Website] | — | Oui | — | Oui | — | — | — | Oui | — | — |
| [!UICONTROL Adgroup Site Link] | — | Oui | — | — | — | — | — | Oui | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Oui | — |
| [!UICONTROL Adgroup Negative Keyword] | Oui | Oui | Oui | Oui | — | — | — | Oui | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Oui | — | Oui | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Oui | Oui | Oui | Oui | — | — | — | Oui | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | — | Oui | — | — | — | Oui | — | — |
| [!UICONTROL Campaign Device Target] | — | Oui | — | Oui | — | — | — | Oui | — | — |
| [!UICONTROL Adgroup Device Target] | — | Oui | — | Oui | — | — | — | Oui | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Oui | — | Oui | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Oui | — | Oui | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Oui | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Oui | — | — | — | — | — | — | — | — |

Pour plus d’informations sur les colonnes obligatoires et facultatives pour chaque réseau publicitaire, reportez-vous aux articles relatifs au format de données de feuille d’envoi groupé spécifique au réseau publicitaire :

* [Données de feuille d’envoi groupé obligatoires et facultatives pour les comptes  [!DNL Baidu] ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)
* [Données de feuille d’envoi groupé obligatoires et facultatives pour les comptes  [!DNL Google Ads] ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
* [Données de feuille d’envoi groupé obligatoires et facultatives pour les comptes  [!DNL LY Ads] ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)
* [Données de feuille d’envoi groupé obligatoires et facultatives pour les comptes  [!DNL Microsoft Advertising] ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
* [Données de feuille d’envoi groupé obligatoires et facultatives pour les comptes  [!DNL Naver] ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
* [Données de feuille d’envoi groupé obligatoires et facultatives pour les comptes  [!DNL Yahoo DSP] ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)
* [Données de feuille d’envoi groupé obligatoires et facultatives pour les comptes  [!DNL Yandex] ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)

>[!MORELIKETHIS]
>
>* [ (nouvelle interface utilisateur) À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupé](about.md)
>* [(Nouvelle interface utilisateur) Chargez une feuille d’envoi groupé ou un fichier d’erreur corrigé](upload.md)
>* [(Nouvelle interface utilisateur) Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](post.md)
>* [(nouvelle interface utilisateur) Valider les pages de destination dans des fichiers de feuille d’envoi groupé](validate-landing-pages.md)
