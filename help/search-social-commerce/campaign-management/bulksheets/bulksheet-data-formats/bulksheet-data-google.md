---
title: 'Données de feuille d’envoi groupé requises pour les comptes  [!DNL Google Ads] '
description: Référencez les champs d’en-tête et de données obligatoires dans les feuilles d’envoi groupé pour les comptes  [!DNL Google Ads] .
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '7898'
ht-degree: 0%

---

# Annexe - Données de feuille d’envoi groupé requises pour les comptes [!DNL Google Ads]

Pour créer et mettre à jour [!DNL Google Ads] données de campagne en bloc, vous pouvez utiliser des fichiers de feuille d’envoi groupé Search, Social et Commerce formatés spécifiquement pour les comptes [!DNL Google Ads]. Vous pouvez a) [générer des fichiers de feuilles de support pour les comptes existants](../bulksheet-download.md) au format de fichier requis ou b) les créer manuellement (voir « [Formats de fichiers de feuilles de support pris en charge](bulksheet-file-formats.md) » pour obtenir des informations générales sur les formats de fichiers pris en charge).

Chaque feuille d’envoi groupé doit inclure les champs d’en-tête et les champs de données correspondants requis pour les [ opérations spécifiques que vous souhaitez effectuer ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (telles que la création d’une annonce publicitaire). Lorsqu’un champ n’est pas obligatoire, vous pouvez l’omettre dans l’en-tête et les lignes de données. Toutes les colonnes personnalisées sont supprimées lorsque vous téléchargez le fichier de feuille en bloc.

Vous trouverez ci-dessous un tableau de tous les champs de données disponibles et des tableaux supplémentaires indiquant les champs nécessaires à l’ajout, la modification ou la suppression de données pour des entités individuelles (telles que des campagnes et des mots-clés).

## Tous les champs de données disponibles {#bulksheet-fields-all-google}

Le tableau suivant décrit tous les champs de données disponibles.

Pour les champs de données pertinents pour les entités de compte, reportez-vous à « [Champs requis pour créer, modifier ou supprimer chaque composant de compte](#bulksheet-fields-per-component-google) ».

>[!NOTE]
>
>* Les valeurs de toutes les colonnes de texte respectent la casse.
>* Lorsque vous créez un enregistrement et que vous n’incluez pas de valeurs pour tous les champs de données obligatoires, les valeurs par défaut spécifiées sont affectées à certains de ces champs.
>* Pour les champs qui ne sont pas spécifiés ci-dessous, la valeur par défaut pour le réseau publicitaire est utilisée.
>* Pour obtenir la liste des lignes de feuilles d’envoi groupé disponibles dans la boîte de dialogue [!UICONTROL Download Bulksheet], reportez-vous à « [Lignes de feuilles d’envoi groupé par réseau publicitaire](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network) ».

| Champ | Description |
| ---- | ---- |
| [!UICONTROL Platform] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) La plateforme publicitaire. Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Acct Name] | Nom unique qui identifie un compte réseau publicitaire. Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Nom unique qui identifie une campagne pour un compte. |
| [!UICONTROL Campaign Budget] | Une limite de dépenses quotidiennes pour la campagne, avec ou sans symboles monétaires et ponctuation. Cette valeur remplace mais ne peut pas dépasser le budget du compte. |
| [!UICONTROL Delivery Method] | <p>Vitesse à laquelle afficher les publicités de la campagne chaque jour :</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (valeur par défaut pour les nouvelles campagnes) : pour répartir vos impressions d’annonce publicitaire tout au long de la journée.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (obsolète en octobre 2019) Pour afficher vos annonces aussi souvent que possible jusqu’à ce que votre budget soit atteint. Par conséquent, il se peut que vos annonces n’apparaissent pas plus tard dans la journée.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>Canaux sur lesquels placer des annonces publicitaires. Spécifiez une ou plusieurs options :</p><ul><li><p><i>[!UICONTROL Search]</i> (valeur par défaut pour les nouvelles campagnes) : pour placer des annonces sur le réseau de recherche [!DNL Google Ads] (y compris les sites web de recherche [!DNL Google Ads] et de partenaires de recherche) et éventuellement également sur le réseau d’affichage [!DNL Google Ads]. <b>Remarque :</b> les campagnes qui ciblent à la fois le réseau de recherche et le réseau d’affichage ne peuvent pas être ajoutées à un portfolio pour l’optimisation des enchères.</p></li><li><p><i>[!UICONTROL Display]</i> : pour placer des annonces uniquement sur le réseau d’affichage [!DNL Google Ads].</p></li><li><p><i>[!UICONTROL Shopping]</i> : Pour placer des annonces sur [!DNL Google Ads] réseau d&#39;achat (dans certains pays) et le réseau de recherche [!DNL Google Ads] (y compris les sites Web de recherche de [!DNL Google Ads] et de partenaires de recherche). Pour créer des annonces d’achats, vous devez disposer de produits dans un compte [!DNL Google Merchant Center] et [autoriser Search, Social et Commerce à télécharger les données du compte](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Consultez « [Implémenter [!DNL Google Ads] des campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md) » pour plus d’informations sur le processus de création des annonces d’achat.</p></li></ul> |
| [!UICONTROL Networks] | <p>Où placer des annonces publicitaires. Spécifiez une ou plusieurs options :</p><ul><li><p><i>[!UICONTROL Google Search]</i> : recherches sponsorisées sur le réseau de recherche Google uniquement.</p></li><li><p><i>[!UICONTROL Search Partners]</i> : recherches sponsorisées sur les partenaires de recherche Google.</p></li><li><p><i>[!UICONTROL Content]</i> : pour placer des enchères pour afficher les listes réseau.</p></li><li><p><i>[!UICONTROL All]</i> (valeur par défaut pour les nouvelles campagnes) : cible la recherche Google, les partenaires de recherche et le contenu.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Réseau de recherche uniquement ; applicable aux annonces de recherche dynamique développées uniquement) Domaine racine (tel que example.com) ou sous-domaine (tel que shoes.example.com) du site web dont le contenu est utilisé par le réseau publicitaire pour cibler vos annonces de recherche dynamique.<br><br><b>Remarques :</b></p><ul><li><p>Les annonces de recherche dynamique étendues ciblent le contenu du site web plutôt que les mots-clés.</p></li><li><p>Votre domaine doit être indexé par l’index de recherche organique du réseau publicitaire pour être ciblé.</p></li><li><p>Si vous ne spécifiez pas de domaine, vous devez créer des cibles de recherche dynamique, qui ciblent toutes les pages de votre site web ou un sous-ensemble de celles-ci, pour chaque groupe publicitaire.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Réseau de recherche uniquement ; applicable aux annonces de recherche dynamique développées uniquement) Langue du domaine de site web spécifié. <b>Remarque :</b> si le domaine contient des pages dans plusieurs langues et que vous souhaitez cibler toutes les pages, créez une campagne distincte pour chaque langue. |
| [!UICONTROL GDN Custom Bid Level] | (Campagnes ciblant uniquement le réseau d’affichage) Comment enchérir : par <i>[!UICONTROL Ad Group]</i> (valeur par défaut), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (site web) ou <i>[!UICONTROL None]</i> (pour réinitialiser la valeur existante). D’autres dimensions (<i>Âge</i>, <i>Sexe</i>, <i>Intérêt et liste</i>, <i>Rubrique</i> et <i>Vertical</i>) sont disponibles dans l’interface [!DNL Google Ads]. Si vous avez utilisé l’interface [!DNL Google Ads] pour configurer les enchères selon une autre dimension, cette valeur s’affiche, mais vous ne pouvez pas sélectionner ni saisir ces dimensions ici.</p><p><b>Remarque :</b></p><ul><li><p>Lorsque vous enchérissez par mot-clé, créez des modèles de suivi au niveau du mot-clé. De même, lorsque vous enchérissez par emplacement, créez des modèles de suivi au niveau de l’emplacement. Pour toutes les autres dimensions, créez des modèles de suivi au niveau des annonces.</p></li><li><p>Lorsque vous enchérissez en fonction d’une dimension non prise en charge (âge, sexe, centre d’intérêt et liste ou rubrique), les options Recherche, Réseau social et Commerce n’optimisent pas les enchères pour la dimension et toutes les attributions sont appliquées au groupe publicitaire.</p></li><li><p>Les publicités sur le réseau de recherche utilisent toujours des offres par mot-clé.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Campagnes d’achat uniquement) Priorité d’utilisation de la campagne lorsque plusieurs campagnes font la publicité du même produit : <i>[!UICONTROL Low]</i> (valeur par défaut pour les nouvelles campagnes), <i>[!UICONTROL Medium]</i> ou <i>[!UICONTROL High]</i>.</p><p>Lorsque le même produit est inclus dans plusieurs campagnes, le réseau publicitaire utilise d’abord la priorité de campagne pour déterminer quelle campagne (et l’enchère associée) est éligible à la mise aux enchères publicitaire. Lorsque toutes les campagnes ont la même priorité, la campagne ayant la meilleure enchère est éligible. |
| [!UICONTROL Has EU Political Ads] | (Applicable aux campagnes qui ciblent un public dans l’Union européenne (UE)) Que la campagne contienne ou non de la publicité politique conformément aux exigences du règlement de l’UE 2024/90 concernant les publicités diffusées dans l’Union européenne : <i>[!UICONTROL Yes]</i> ou <i>[!UICONTROL No]</i>. |
| [!UICONTROL Merchant ID] | (Campagnes d’achat et campagnes d’audience liées à un flux de commerçant uniquement) ID de client du compte de commerçant dont les produits sont utilisés pour la campagne. |
| [!UICONTROL Sales Country] | (Campagnes d’achat uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel les produits de la campagne sont vendus. Comme les produits sont associés aux pays cibles, ce paramètre détermine les produits qui sont annoncés dans la campagne. |
| [!UICONTROL Product Scope Filter] | (Campagnes utilisant uniquement le réseau d’achats [!DNL Google Ads]) Les produits de votre compte [!DNL Google Merchant Center] pour lesquels des annonces d’achats peuvent être créées pour la campagne. Vous pouvez saisir jusqu’à sept combinaisons de dimensions de produit et d’attributs pour filtrer vos produits à l’aide du format dimension=attribute. Séparez plusieurs filtres avec un délimiteur « > ». Pour obtenir la liste des dimensions de produit disponibles, voir « [ Filtres de produit de campagne d’achat ](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md) ».</p><p>Exemple : « CategoryL1=activities>>CategoryL2=pet Supplies>>Brand=Acme Pet Supplies »</p><p>Pour supprimer les valeurs existantes, utilisez la valeur <code>[delete]</code> (y compris les crochets).</p> |
| [!UICONTROL Languages] | <p>(Rechercher et Afficher les réseaux uniquement) Langues cibles pour les annonces publicitaires dans la campagne.</p><p>Si vous ne saisissez pas de valeur pour ce champ ou le champ [!UICONTROL Geo Targeting] d’une nouvelle campagne, la devise spécifiée pour le compte détermine les langues par défaut. Toutefois, les campagnes avec des devises qui ne sont pas mappées à des langues spécifiques (par exemple, l’euro) sont ciblées sur toutes les langues. Si vous ne saisissez pas de valeur pour ce champ, mais saisissez une valeur dans le champ [!UICONTROL Geo Targeting] pour une nouvelle campagne, la valeur par défaut est <i>[!UICONTROL All]</i>. Si vous laissez ce champ vide pour une campagne existante, la valeur existante est conservée.</p><p>Pour cibler toutes les langues, saisissez <span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span>. Pour cibler des langues spécifiques, entrez des valeurs séparées par des points-virgules en utilisant soit <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] noms de langue</a> (par exemple <i>anglais;japonais</i>, qui sont remplacés par les codes numériques corrects), soit des codes numériques (par exemple <i>1000;1005</i>). Les valeurs ne respectent pas la casse.</p> |
| [!UICONTROL Location] | Emplacement géographique dans lequel placer des annonces pour la campagne ou pour lequel exclure des annonces. Si vous ne saisissez aucune valeur dans ce champ ou dans le champ Langues pour une nouvelle campagne, la devise spécifiée pour le compte détermine les emplacements par défaut. Toutefois, les campagnes avec des devises qui ne sont pas mappées à des emplacements spécifiques (par exemple, l’euro) sont ciblées sur tous les emplacements. Si vous ne saisissez pas de valeur pour ce champ, mais saisissez une valeur dans le champ [!UICONTROL Languages] pour une nouvelle campagne, la valeur par défaut est <i>[!UICONTROL All]</i>. Si vous laissez ce champ vide pour une campagne existante, la valeur existante est conservée.</p><p>Pour cibler un emplacement spécifique, utilisez l’un des [[!DNL Google Ads] noms d’emplacement](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (qui sont remplacés par le code numérique correct) ou des codes d’emplacement :</p><ul><li><p>Pays/territoires : saisissez les noms de pays/territoires (tels que <i>États-Unis, Japon</i>) ou les codes numériques (tels que <i>2840, 2392</i>).</p></li><li><p>États/provinces/régions : saisissez les noms d’État/province/région avec les abréviations de pays/territoire associées (telles que <i>Tokyo, JP ; New York, US</i>) ou les codes numériques (tels que <i>20636 ; 21167</i>).</p></li><li><p>Villes non américaines : saisissez le nom de la ville, le nom de l’État/province/région et les abréviations des pays/territoires (<i>Adachi, Tokyo, JP ; Kita, Tokyo, JP</i>) ou les codes numériques (<i>1028850, 1009293</i>)</p></li><li><p>Zones métropolitaines des États-Unis : saisissez les noms de ville, les noms d’État et les abréviations de pays (par exemple, <i>Buffalo NY, États-Unis ; New York NY, États-Unis</i>) ou les codes numériques (par exemple, <i>514 ; 501</i>).</p></li></ul><p>Pour exclure un emplacement, faites précéder le nom ou le code de l’emplacement d’un signe moins (`-`), tel que <i>-Japon</i>.</p><p><b>Remarque :</b> les valeurs ne respectent pas la casse.</p> |
| [!UICONTROL Location Type] | (Lorsque vous incluez un emplacement) Le [type d’emplacement](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Type d’appareil pour lequel des ajustements d’offre sont effectués au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> ou <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(Lorsque vous incluez une cible [!UICONTROL Location], [!UICONTROL Device] ou [!UICONTROL RLSA]) Ajuster les enchères pour des annonces à un emplacement spécifique, sur un type d’appareil spécifique ou avec une cible d’audience spécifique :</p><ul><li><p>Pour utiliser l&#39;enchère par mot-clé (différence de 0 %), entrez 0. Pour les nouvelles cibles, vous pouvez également laisser ce champ vide.</p></li><li><p>Pour utiliser une enchère différente pour cette cible, entrez le pourcentage d&#39;augmentation ou de diminution des enchères.</p></li><ul><li><p>Pour les cibles de localisation et de RLSA, les pourcentages valides sont compris entre -90 et 900.</p></li><li><p>Pour les ajustements d’enchères d’appareil, les pourcentages valides sont les suivants :</p></li><ul><li><p>(Campagnes)-100 (pour ne pas enchérir sur des annonces sur le type d’appareil) ou de -90 à 900.</p></li><li><p>(Groupes publicitaires) -100 pour les smartphones et les tablettes (pour ne pas enchérir sur le type d’appareil), et de -90 à 900 pour tous les types d’appareils.</p></li></ul></ul><li><p>(Campagnes et groupes publicitaires existants) Pour utiliser l’ajustement d’enchère existant, laissez ce champ vide.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Ajustement d’offre en lecture seule recommandé par Adobe pour la cible de l’emplacement au niveau de la campagne ou un RLSA. Il est calculé uniquement lorsque la campagne se trouve dans un portefeuille avec un objectif qui utilise des mesures de conversion pondérées (et non l’objectif [!UICONTROL Maximize Clicks]) et que la campagne contient au moins deux cibles d’emplacement ou RLSA avec au moins cinq clics ou un coût de 5 USD au cours des 90 derniers jours.</p><p>Si vous souhaitez modifier manuellement une cible d’emplacement ou un RLSA pour utiliser la valeur recommandée, attendez au moins deux semaines après avoir créé la cible d’emplacement ou le RLSA pour permettre une collecte de données suffisante, et ne modifiez pas la valeur plus d’une fois par semaine. |
| [!UICONTROL Device Targets] | <p>(Types de campagne hérités uniquement) Appareils sur lesquels la publicité peut être affichée : <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> ou <i>[!UICONTROL Tablets]</i>. Pour les nouvelles campagnes, la valeur par défaut est <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Types de campagne hérités uniquement ; applicable lorsque les cibles d’appareil incluent des « smartphones » ou des « tablettes ») Les systèmes d’exploitation sur lesquels l’annonce publicitaire peut être affichée : <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> ou <i>[!UICONTROL Palm]</i>. Pour les nouvelles campagnes, la valeur par défaut est <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Types de campagne hérités uniquement ; applicable lorsque les [!UICONTROL Device Targets] incluent « [!UICONTROL All] » ou « [!UICONTROL Smartphones] ») Opérateurs de téléphonie mobile auxquels les smartphones peuvent être connectés : <i>[!UICONTROL All]</i>, ou un ou plusieurs opérateurs indiqués par &lt;c<i>code d’opérateur</i>>,&lt;<i>code de pays</i>> (tels que T-Mobile, États-Unis) à l’aide de la liste des <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">opérateurs et codes disponibles pour les [!DNL Google Ads]</a>. Séparez plusieurs opérateurs par des points-virgules (tels que T-Mobile, US ; T-Mobile, GB). Pour les nouvelles campagnes, la valeur par défaut est <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>Nom unique qui identifie un groupe publicitaire. La longueur maximale est de 255 caractères ; les caractères vides de fin ne sont pas enregistrés (par exemple, « Groupe publicitaire 1 » est enregistré comme « Groupe publicitaire 1 »). Ce champ ne s’applique pas aux liens de site au niveau de la campagne ni aux cibles d’appareil au niveau de la campagne.</p> |
| [!UICONTROL Ad Group Type] | <p>Le type de groupe publicitaire : <i>[!UICONTROL Demand Gen]</i> (pour les campagnes de génération de la demande uniquement), <i>[!UICONTROL Display]</i> (pour les campagnes d’affichage), <i>[!UICONTROL Search Dynamic]</i> (pour les annonces de recherche dynamique étendue), <i>[!UICONTROL Search Standard]</i> (pour les annonces de recherche), <i>[!UICONTROL Shopping Product]</i> (pour les annonces de produits d’achat), <i>[!UICONTROL Shopping Showcase]</i> (création et modification non prises en charge) ou <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Campagnes CPC uniquement) Coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire sur le réseau publicitaire, avec ou sans symboles monétaires et ponctuation. Vous pouvez définir des valeurs pour les groupes publicitaires et les mots-clés, les groupes de produits et les cibles de recherche dynamique. La valeur par défaut d’un nouveau mot-clé est héritée du niveau du groupe publicitaire . Pour les groupes de produits, vous pouvez définir des valeurs pour le niveau de groupe de produits le plus bas ; la valeur par défaut d’un nouveau niveau est héritée du niveau parent.</p><p>Pour les groupes de produits existants et les cibles de recherche dynamiques dans les portfolios optimisés, les mises à jour ne sont efficaces que pendant une journée et sont remplacées lors du cycle d’optimisation suivant.</p> |
| [!UICONTROL Max Content CPC] | <p>(Campagnes CPC uniquement) Coût maximal du contenu par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire à partir d’un site réseau d’affichage, avec ou sans symboles monétaires et ponctuation. Vous pouvez définir et modifier des valeurs au niveau du groupe publicitaire dans les campagnes qui ne sont pas ciblées par emplacement.</p> |
| [!UICONTROL Audience Target Method] | <p>(Campagnes sur le réseau de recherche uniquement et campagnes de [!DNL Gmail] existantes en lecture seule sur le réseau d’affichage) Si :</p><ul><li><p><i>[!UICONTROL Target and Bid]</i> : affichage des publicités uniquement pour les utilisateurs et utilisatrices associés aux audiences cibles qui répondent également aux autres cibles du groupe publicitaire.</p></li><li><p><i>[!UICONTROL Bid Only]</i> : affichage des annonces même aux personnes qui ne sont pas associées aux audiences cibles, à condition qu’elles répondent aux objectifs d’autres groupes d’annonces.</p><p>Vous pouvez toutefois augmenter les chances que les publicités soient présentées à des audiences spécifiques en fixant des enchères plus élevées pour ces audiences.</p></li></ul> |
| [!UICONTROL Keyword] | Chaîne du mot-clé. La longueur maximale est de 80 caractères et de 10 mots au maximum. Elle ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : espace `# $ & _ - " [ ] ' + . / :`</p><p><b>Remarque :</b></p><ul><li><p>Pour exclure un mot-clé au niveau du groupe publicitaire ou de la campagne, définissez la [!UICONTROL Match Type] sur <i>[!UICONTROL Negative]</i>. Si la ligne contient le nom du groupe publicitaire, le mot-clé est exclu pour ce groupe publicitaire. Si la ligne n’inclut pas le nom du groupe publicitaire, le mot-clé est exclu pour l’ensemble de la campagne.</p></li><li><p>La modification d’un [!DNL Google Ads] mot-clé ou d’un type de correspondance supprime le mot-clé existant et en crée un nouveau.</p></li></ul> |
| [!UICONTROL Placement] | (Campagnes utilisant uniquement la correspondance de contenu) Emplacement dans le réseau d’affichage sur lequel vos publicités peuvent être affichées. Spécifiez l’une des options suivantes :</p><ul><li><p>Site web : saisissez une URL valide. Il peut s’agir d’un domaine de niveau supérieur, d’un sous-domaine de premier niveau ou d’un domaine avec un seul nom de répertoire. L&#39;URL ne peut pas contenir de point d&#39;interrogation (?). Exemples :<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>Une position d’annonce sur une page spécifique : utilisez le `<URL> >> <location,sublocation>` de format (`finance.google.com >> Company pages,Top right`, par exemple).</p></li><li><p>Une catégorie de rubrique : utilisez la syntaxe `<category::<category> > <subcategory>` etc. (telle que `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Remarque :</b> pour exclure un emplacement au niveau du groupe publicitaire ou de la campagne, définissez la [!UICONTROL Match Type] sur <i>[!UICONTROL Negative]</i>. Si la ligne contient le nom du groupe publicitaire, l’emplacement est exclu pour ce groupe publicitaire. Si la ligne n’inclut pas le nom du groupe publicitaire, l’emplacement est exclu pour l’ensemble de la campagne.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Obligatoire lorsque le paramètre de campagne défini sur « [!UICONTROL Use my website contents to target my ads] » n’est pas activé, facultatif dans le cas contraire) Recherche dynamique cible le groupe publicitaire.</p><p>Pour toutes les cibles, utilisez un astérisque (*).</p><p>Pour cibler jusqu’à trois critères de recherche dynamiques, utilisez le format `<category>=<target>`, où `<category>` pouvez inclure l’une des catégories ci-dessous. Rejoignez plusieurs cibles pour une catégorie individuelle avec « \[espace vide\] » et « \[espace vide\] », puis joignez plusieurs catégories avec « [espace vide] et [espace vide] ».</p><ul><li><p><i>[!UICONTROL Category]</i> : affichage d’annonces de recherche dynamique étendues pour les pages indexées avec une catégorie de contenu [!DNL Google Ads] spécifique.</p></li><li><p><i>[!UICONTROL URL]</i> : affichage d’annonces de recherche dynamique étendues pour les pages indexées avec une URL spécifique, où la valeur peut être incluse n’importe où dans l’URL.</p></li><li><p><i>[!UICONTROL Page Title]</i> : affichage d’annonces de recherche dynamique étendues pour les pages indexées avec un texte spécifique dans le titre de la page.</p></li><li><p><i>[!UICONTROL Page Content]</i> : affichage d’annonces de recherche dynamique étendues pour les pages indexées avec un contenu spécifique.</p></li></ul><p>Exemple : url=shoes.example.com et page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | La hiérarchie de tous les groupes de produits parents.<br><br>Exemple : `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>Le groupe de produits (par exemple, « brand=acme » ou « All Products »).</p><p><b>Remarque :</b></p><ul><li><p>Lorsqu’un groupe de produits spécifié n’existe pas dans la hiérarchie des [!UICONTROL Parent Product Groupings], Search, Social et Commerce crée les parties de la hiérarchie nécessaires.</p></li><li><p>Search, Social et Commerce crée automatiquement un groupe « [!UICONTROL All Products] » lorsque vous créez un groupe publicitaire dans une campagne [!DNL Google Ads] Shopping avec une enchère par défaut définie sur l’enchère par défaut du groupe publicitaire. Search, Social et Commerce crée automatiquement un groupe « [!UICONTROL Everything Else] » avec l’enchère par défaut du groupe publicitaire à chaque niveau de la hiérarchie du groupe de produits. Vous pouvez toujours créer explicitement ces groupes par défaut et les exclure ou modifier leurs enchères.</p></li><li><p>Chaque groupe publicitaire peut inclure jusqu’à huit niveaux de groupes de produits, y compris « [!UICONTROL All Products] » et sept autres niveaux.</p></li></ul> |
| [!UICONTROL Partition Type] | Type de répartition du groupe de produits : <i>subdivision</i> (s&#39;il a des groupes de produits enfants) ou <i>unité</i> (s&#39;il n&#39;a pas de groupes de produits enfants). |
| [!UICONTROL Match Type] | <p>Pour la cible de recherche dynamique ou les groupes de produits : option de correspondance de mots-clés pour la cible de recherche dynamique ou le groupe de produits : <i>[!UICONTROL Dynamic Ad Target]</i> (valeur par défaut pour les nouvelles cibles de recherche dynamique), <i>[!UICONTROL Product Group]</i> (valeur par défaut pour les nouveaux groupes de produits) ou <i>[!UICONTROL Negative Product Group]</i> (pour exclure un groupe de produits).</p><p>Pour les mots-clés : option de correspondance de mots-clés pour le mot-clé : <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> ou <i>[!UICONTROL Negative]</i> (pour exclure un mot-clé ou un emplacement sur le réseau d’affichage) ; les groupes de produits utilisés avec les annonces d’achats ont un type de correspondance de <i>[!UICONTROL Product Group]</i>. Si vous utilisez <i>[!UICONTROL Negative]</i>, vous devez également inclure le type de correspondance à exclure (par exemple, « Expression négative »).</p><p>Pour les nouveaux mots-clés, la valeur par défaut est <i>[!UICONTROL Broad]</i>. Une valeur pour le type de correspondance ou l’ID de mot-clé est requise uniquement pour modifier un mot-clé avec plusieurs types de correspondance.</p><p><b>Remarque :</b></p><ul><li><p>Les types de correspondance ne s’appliquent pas aux annonces de recherche dynamique étendue, qui n’utilisent pas de mots-clés.</p></li><li><p>La modification du type de correspondance d’un mot-clé [!DNL Google Ads] supprime le mot-clé existant et en crée un nouveau.</p></li><li><p>Pour le modificateur de correspondance large, choisissez « Large » et insérez un + avant tout mot dans le mot-clé pour lequel des variantes proches sont requises (par exemple, « + rouge + chaussures » pour exiger des variantes proches de « rouge » et « chaussures »). <b>Remarque :</b> les modificateurs de correspondance large ont désormais le même comportement de correspondance que la correspondance d’expression pour certaines langues. Vous n’avez pas pu créer de nouveaux mots-clés de modificateur de correspondance large depuis juillet 2021. Voir [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/7042511) pour plus d’informations.</p> |
| [!UICONTROL First Page Bid] | (Incluse dans les feuilles d&#39;envoi groupé générées à titre d&#39;information) Offre requise pour placer une annonce sur la première page des résultats de recherche. Cette valeur n&#39;est pas publiée sur le réseau publicitaire. |
| [!UICONTROL Quality Score] | (Incluse dans les feuilles d’envoi groupé générées à titre d’information) Note de qualité actuelle attribuée au mot-clé par le moteur de recherche. Cette valeur n&#39;est pas publiée sur le réseau publicitaire.) |
| [!UICONTROL Creative Preferred Devices] | (Annonces de texte, annonces de recherche dynamique étendue et liens de site améliorés ; facultatif) Types d’appareils sur lesquels vous préférez afficher l’annonce : <i>[!UICONTROL All]</i> (par défaut) ou <i>[!UICONTROL Mobile]</i>. Lorsque <i>[!UICONTROL Mobile]</i> est spécifié, le réseau tente d’afficher la publicité sur les utilisateurs d’appareils mobiles plutôt que sur les utilisateurs d’ordinateurs de bureau ou de tablettes. Sinon, le réseau affiche la publicité sur n’importe quel type d’appareil.</p><p><b>Remarque :</b></p><ul><li><p>Seuls les utilisateurs administrateurs et [!DNL Adobe] gestionnaires de comptes peuvent modifier ce paramètre.</p></li><li><p>Le réseau ne garantit pas qu&#39;il affichera la publicité sur le type d&#39;appareil préféré.</p></li><li><p>De nouveaux liens de site améliorés ne peuvent être créés que dans les campagnes avec des liens de site améliorés existants ou sans liens de site.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Annonces textuelles développées et annonces responsive sur le Réseau de Recherche uniquement) Titres d’une annonce, séparés chacun par une barre verticale (&amp;vert;). La longueur maximale de chaque champ de titre d’annonce est de 30 caractères ou 15 caractères codés sur deux octets, y compris tout texte dynamique (comme les valeurs des mots-clés et des personnalisateurs d’annonce).</p><p>Pour les annonces responsive sur le Réseau de Recherche, les champs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] et [!UICONTROL Ad Title 3] sont obligatoires et tous les autres champs de titre de l’annonce sont facultatifs. Pour supprimer la valeur existante d’un champ non obligatoire, utilisez la valeur <code>[delete]</code> (y compris les crochets).</p><p>Pour les annonces responsive sur le Réseau de Recherche, insérez un personnalisateur d’annonce publicitaire au format suivant : <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, par exemple <code>{CUSTOMIZER.Discount:10%}</code></p><p>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer les annonces au format texte développé, qui [!DNL Google Ads] obsolètes en juin 2022. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Annonces de recherche réactives uniquement ; facultatif) Position à laquelle épingler le titre d’annonce correspondant : `[null]` (aucune valeur, ce qui rend le titre d’annonce éligible à tous les postes), <i>1</i>, <i>2</i> ou <i>3</i>. Par exemple, si [!UICONTROL Ad Title Position] a une valeur de 1, alors le titre de l’annonce publicitaire s’affiche uniquement en position 1. Par défaut, tous les titres des annonces publicitaires sont nuls (n’ont pas de valeurs).</p><p>Pour supprimer la valeur existante, utilisez la valeur <code>[delete]</code> (y compris les crochets).</p><p><b>Remarque :</b> vous pouvez épingler plusieurs titres d’annonce publicitaire à la même position. Le réseau publicitaire utilise l’un des titres de publicité épinglés à la position . Les titres épinglés en position 3 peuvent ne pas être affichés avec la publicité.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Annonces de recherche dynamique étendues, annonces de texte étendues et annonces de recherche réactives uniquement) Le corps d’une annonce. La longueur maximale de chaque champ de description est de 90 caractères, soit 45 caractères codés sur deux octets, y compris tout texte dynamique (valeurs des mots-clés et personnalisateurs d’annonces, par exemple).</p><p>Pour les annonces responsive sur le Réseau de Recherche, insérez un personnalisateur d’annonce publicitaire au format suivant : `{CUSTOMIZER.AdCustomizerName:DefaultText}`, par exemple `{CUSTOMIZER.Discount:10%}`</p><p>Pour les annonces de recherche dynamique étendue, utilisez [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] uniquement. <b>Remarque :</b> pour ce type d’annonce, la modification de la copie d’annonce supprime l’annonce existante et en crée une nouvelle.</p><p>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer les annonces au format texte développé, qui [!DNL Google Ads] obsolètes en juin 2022.</p><p>Pour les annonces responsive sur le Réseau de Recherche, [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont obligatoires, et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatifs. Pour supprimer la valeur existante, utilisez la valeur <code>[delete]</code> (y compris les crochets).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Annonces de recherche réactives uniquement ; facultatif) Position à laquelle épingler la description correspondante : `[null]` (aucune valeur, ce qui rend la description éligible pour tous les postes), <i>1</i>, <i>2</i> ou <i>3</i>. Par exemple, si [!UICONTROL Description 1 Position] a une valeur de 1, alors [!UICONTROL Description 1] apparaît uniquement dans Position 1. Par défaut, aucune description n’est épinglée à une position.</p><p>Pour supprimer la valeur existante, utilisez l’`[delete]` de valeur (y compris les crochets).</p><p><b>Remarque :</b> vous pouvez épingler plusieurs descriptions à la même position. Le réseau publicitaire utilise l’une des descriptions épinglées à la position. Les descriptions épinglées en position 2 peuvent ne pas être affichées avec la publicité. |
| [!UICONTROL Display URL] | L’URL incluse dans la publicité.<br><br>Pour les annonces de recherche dynamique étendues, [!DNL Google Ads] génère cette valeur de manière dynamique à partir du domaine du site web et vous n’avez pas besoin d’entrer de valeur.<br><br>Pour les annonces responsive sur le Réseau de Recherche, il n’est pas nécessaire de saisir une valeur. L’URL affichée est automatiquement extraite du domaine dans l’URL finale. Vous pouvez éventuellement personnaliser l’URL à l’aide des champs Chemin 1 et Chemin 2 .<br><br>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer les annonces au format texte développé, qui [!DNL Google Ads] abandonnées en juin 2022.<br><br><b>Remarque :</b> (Comptes avec URL finales) Les noms de domaine dans l’URL d’affichage et l’URL finale doivent correspondre.</p> |
| [!UICONTROL Display Path 1] | <p>(Annonces textuelles développées<span> et annonces responsive sur le Réseau de Recherche</span> uniquement)</p><p>(Facultatif) Texte ajouté à l’URL d’affichage automatiquement extrait de l’URL finale. Elle est précédée dans l’URL d’une barre oblique (/). Un chemin ne peut pas contenir de barre oblique (/) ou de nouvelle ligne (\n). La longueur maximale est de 15 caractères ou 7 caractères codés sur deux octets.</p><p>Pour insérer un personnalisateur d’annonce publicitaire, utilisez les formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide :&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`</p><p>Par exemple, si [!UICONTROL Display Path 1] est « affaires », l’URL affichée est &lt;<i>display URL</i>>/affaires, comme www.example.com/deals.</p><p>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer les annonces au format texte développé, qui [!DNL Google Ads] obsolètes en juin 2022.</p> |
| [!UICONTROL Display Path 2] | Un second chemin d’affichage ; voir l’entrée pour [!UICONTROL Display Path 1].<br><br>Exemple : si [!UICONTROL Display Path 1] est « affaires » et [!UICONTROL Display Path 2] est « local », l’URL d’affichage est &lt;<i>display URL</i>>/affaires/local, par exemple www.example.com/deals/local.</p><p>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer les annonces au format texte développé, qui [!DNL Google Ads] obsolètes en juin 2022.</p> |
| [!UICONTROL Promotion Line] | (Annonces de liste de produits uniquement) Ligne de promotion facultative à inclure dans la liste de produits dans les résultats de recherche. La longueur maximale est de 45 caractères.</p><p>La ligne de promotion peut apparaître à différents emplacements par rapport à l’annonce (comme sous l’annonce), selon l’emplacement de l’annonce sur la page. |
| [!UICONTROL Link Name] | <p>Texte du lien du site. Il peut contenir jusqu’à 25 caractères.</p><p>Pour les nouveaux liens de site, vous devez inclure le nom de la campagne dans la ligne de lien du site. Pour les liens de site au niveau du groupe publicitaire, vous devez également inclure le nom du groupe publicitaire.</p><p><b>Remarque :</b> le texte existant de 35 caractères est toujours affiché dans les publicités sur les ordinateurs de bureau et les tablettes, mais pas sur les appareils mobiles.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Annonces d’installation d’application existantes uniquement) Système d’exploitation sur lequel l’application mobile s’exécute : <i>Android™</i> ou <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Annonces d’installation d’application existantes uniquement) <p>Identifiant de l’application ou nom du package. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Annonces d’installation d’application existantes uniquement) Nom de l’application. |
| [!UICONTROL Start Date] | <p>(Liens du site améliorés uniquement) Première date à laquelle des offres peuvent être placées pour le lien du site, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : <i>mm/j/aaaa</i>, <i>mm/j/aaaa</i>, <i>mm-j-aaaa</i> ou <i>mm-j-aaaa</i>. La valeur par défaut des nouveaux liens de site améliorés est la date du jour.</p><p><b>Remarque :</b> les nouveaux liens de site améliorés ne peuvent être créés que dans les campagnes avec des liens de site améliorés existants ou sans liens de site.</p> |
| [!UICONTROL End Date] | <p>(Liens du site améliorés uniquement) Dernière date à laquelle des offres peuvent être faites pour le lien du site, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants :  <i>m/j/aaaa</i>, <i>m/j/aa</i>, <i>m-j-aaaa</i> ou <i>m-j-aa</i>. La valeur par défaut est aucune (aucune date de fin).</p><p><b>Remarque :</b> les nouveaux liens de site améliorés ne peuvent être créés que dans les campagnes avec des liens de site améliorés existants ou sans liens de site.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Annonces d’installation d’application existantes uniquement)</p><p>(Facultatif) Empêche les [!DNL Google Ads] d’afficher la publicité sur les utilisateurs de tablettes. Les valeurs peuvent inclure <i>oui</i> et <i>non</i>. |
| [!UICONTROL Landing Page Suffix] | Tous les paramètres à ajouter à la fin des URL finales pour suivre les informations. Exemple : `param2=value1&param3=value2`<br><br>voir « [Formats de suivi des clics pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) ».<br><br>Les suffixes d’URL finaux aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent est nécessaire pour les composants de compte individuels. Pour configurer un suffixe au niveau du groupe publicitaire ou à un niveau inférieur, utilisez l’éditeur de [!DNL Google Ads]. |
| [!UICONTROL Tracking Template] | Le modèle de tracking , qui spécifie toutes les redirections de domaine et tous les paramètres de tracking hors de l’atterrissage et incorpore l’URL finale dans un paramètre de [!DNL ValueTrack]. Le modèle de suivi au niveau le plus granulaire (avec le mot-clé comme plus granulaire) remplace les valeurs à tous les niveaux supérieurs.<br><br>Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.<br><br>Pour les redirections et le suivi tiers, saisissez une valeur. Pour obtenir la liste des paramètres de [!DNL ValueTrack] permettant d’indiquer les URL finales dans les modèles de tracking, reportez-vous aux paramètres « Modèle de tracking uniquement » dans la section sur « Paramètres de [!DNL ValueTrack] disponibles » dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2375447).<br><br>Pour supprimer la valeur existante, utilisez le `[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Base URL/Final URL] | URL de la page de destination vers laquelle les utilisateurs et utilisatrices du moteur de recherche sont dirigés lorsqu’ils cliquent sur votre annonce, y compris tout paramètre d’ajout configuré pour la campagne ou le compte. Les URL de base/finales au niveau du mot-clé remplacent celles au niveau de l’annonce et aux niveaux supérieurs.<br><br>Pour supprimer la valeur existante, utilisez le `[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Destination URL] | (Incluse dans les feuilles d&#39;envoi groupé générées à titre d&#39;information ; non publiée dans le moteur de recherche) Pour les comptes avec des URL de destination, il s&#39;agit de l&#39;URL qui lie une annonce à une URL de base/page de destination sur le site Web de l&#39;annonceur (parfois via un autre site qui suit le clic et redirige ensuite l&#39;utilisateur vers la page de destination). Elle inclut tous les paramètres d’ajout configurés pour la campagne ou le compte Search, Social et Commerce. Si vous avez généré des URL de tracking, cela dépend des paramètres de tracking définis dans les paramètres de votre compte et de votre campagne. Si vous avez ajouté des paramètres spécifiques au moteur de recherche, ils peuvent être remplacés par des paramètres équivalents pour Recherche, Social et Commerce.<br><br>Pour les comptes avec des URL finales, cette colonne affiche la même valeur que la colonne URL de base/URL finale. |
| [!UICONTROL Custom URL Param] | Données à substituer à la variable dynamique `{custom_code}` lorsque la variable est incluse dans les paramètres de tracking du compte de recherche ou des paramètres de la campagne. Pour insérer la valeur personnalisée dans l&#39;URL de tracking, vous devez télécharger le fichier de feuille d&#39;envoi groupé via l&#39;option Générer les URL de tracking . |
| [!UICONTROL Creative Type] | Le format de l’annonce : <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Demand Gen Carousel Ad]</i> (annonces carrousel à plusieurs images), <i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>, <i>[!UICONTROL Demand Gen Product Ad]</i> et <i>[!UICONTROL Demand Gen Video Ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (type d’annonce obsolète), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (obsolète), <i>[!UICONTROL Image]</i>/i> (annonces d’achats) ou <i>[!UICONTROL Product ad<] <i>[!UICONTROL Responsive search ad]</i>. La valeur par défaut pour les nouvelles publicités est <i>[!UICONTROL Text ad]</i>.<br><br>Obligatoire pour créer ou modifier le statut d’une annonce publicitaire de produit. |
| [!UICONTROL Param1] | <p>Valeur numérique du paramètre d’annonce publicitaire `{param1}`, qui peut être incluse dans la copie de l’annonce ou l’URL d’affichage pour toute annonce publicitaire dans le fichier de feuille d’envoi groupé. La longueur maximale est de 25 caractères et vous pouvez inclure les caractères non numériques suivants :</p><ul><li><p>La valeur peut être précédée ou ajoutée d’un symbole ou code de devise. Par exemple, `£2.000,00` et `2000GBP` sont valides.</p></li><li><p>La valeur peut inclure une virgule (`,`) ou un point (`.`) comme séparateur, avec un point facultatif (`.`) ou une virgule (`,`) pour les valeurs fractionnaires. Par exemple, `1,000.00` et `2.000,10` sont valides.</p></li><li><p>La valeur peut être précédée ou ajoutée d’un signe de pourcentage (`%`), de signe plus (`+`) ou de signe moins (`- `). Par exemple, `20%`, `208+` et `-42.32` sont valides.</p></li><li><p>Deux nombres peuvent être incorporés avec une barre oblique. Par exemple, `4/1` et `0.95/0.45` sont valides.</p></li></ul><p>Pour supprimer la valeur existante, utilisez l’`[delete]` de valeur (y compris les crochets).</p> |
| [!UICONTROL Param2] | Valeur numérique du paramètre d’annonce publicitaire `{param2}`, qui peut être incluse dans la copie de l’annonce ou l’URL d’affichage pour toute annonce publicitaire dans le fichier de feuille d’envoi groupé. Voir l’entrée pour Param1 pour plus d’informations. |
| [!UICONTROL Audience] | La liste de remarketing pour les annonces de recherche (RLSA) cible l’audience ou l’audience exclue de la campagne ou du groupe publicitaire. Indiquez s’il s’agit d’une cible ou d’une exclusion dans le champ « Type de cible ». |
| [!UICONTROL Target Type] | (Lorsqu’une audience est spécifiée) Si l’audience spécifiée est une <i>Inclusion</i> (cible) ou une <i>Exclusion</i>. |
| [!UICONTROL Campaign Status] | Le statut d’affichage de la campagne : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (non modifiable) ou <i>[!UICONTROL Deleted]</i> (campagnes existantes uniquement). La valeur par défaut pour les nouvelles campagnes est <i>[!UICONTROL Active]</i>. Pour supprimer une campagne active ou en pause, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | Statut d’affichage du groupe publicitaire : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (groupes publicitaires existants uniquement). La valeur par défaut pour les nouveaux groupes publicitaires est [!UICONTROL Active]. Pour supprimer un groupe publicitaire actif ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Keyword Status] | Statut d’affichage du mot-clé : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (mots-clés existants uniquement). La valeur par défaut des nouveaux mots-clés est [!UICONTROL Active]. Pour supprimer un mot-clé actif ou en pause, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | Statut d’affichage de l’annonce publicitaire : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (annonces existantes uniquement), <i>[!UICONTROL Disapproved]</i> (non modifiable) ou <i>[!UICONTROL Paused]</i>. La valeur par défaut pour les nouvelles publicités est [!UICONTROL Active]. Pour supprimer une publicité active ou en pause, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | Statut de l’emplacement du site web : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (annonces existantes uniquement). La valeur par défaut pour les nouveaux sites Web est <i>Actif.</i> Pour supprimer un emplacement actif ou en pause, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | Statut d’une cible de recherche dynamique : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (cibles existantes uniquement). La valeur par défaut pour les nouvelles cibles est <i> Active.</i> Pour supprimer une cible active ou en pause, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | Statut d’affichage du groupe de produits : <i>[!UICONTROL Active]</i> <span> ou </span> <i>[!UICONTROL Deleted]</i> (groupes de produits existants uniquement). La valeur par défaut pour les nouveaux groupes de produits est <i>[!UICONTROL Active]</i>. Pour supprimer un groupe de produits actif, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | Statut d&#39;affichage du lien du site : <i>Actif ou Supprimé</i> (liens de site existants uniquement). La valeur par défaut des nouveaux liens de site est <i>[!UICONTROL Active]</i>. Pour supprimer un lien de site actif, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | Statut de la cible de l’emplacement : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (emplacements existants uniquement). La valeur par défaut pour les nouveaux emplacements est [!UICONTROL Active]. Pour supprimer un emplacement actif, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | Statut de la cible ou de l’exclusion du RLSA au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL Active]</i> ou [!UICONTROL Deleted]</i> (cibles existantes uniquement). La valeur par défaut pour les nouvelles cibles ou exclusions est <i>[!UICONTROL Active]</i>. Pour supprimer une cible active ou une exclusion, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>Statut de la cible de l’appareil au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i>. Pour les nouvelles campagnes et groupes publicitaires, la valeur par défaut est <i>[!UICONTROL Active]</i>.</p> |
| \[Classification d’étiquette spécifique à l’annonceur\] | (Nom pour une classification d’étiquettes spécifique à l’annonceur, telle que « Couleur » pour une classification d’étiquettes appelée Couleur) Valeur pour la classification spécifiée associée à l’entité. Vous ne pouvez inclure qu’une seule valeur par classification par entité (telle que « rouge » pour la classification de libellé « Couleur » pour la campagne A). La longueur maximale est de 100 caractères et la valeur peut inclure des caractères ASCII et non ASCII.<br><br>Les classifications de libellés et leurs valeurs de libellé sont appliqués à tous les composants enfants ; les nouveaux composants ajoutés ultérieurement sont automatiquement associés au libellé. Les classifications d’étiquettes pour les groupes de produits sont appliquées au niveau de l’unité (le plus granulaire).<br><br>Ni le nom de la classification, ni la valeur de classification ne sont sensibles à la casse. |
| [!UICONTROL Constraints] | Contrainte affectée à l&#39;entité. Vous ne pouvez affecter qu&#39;une seule contrainte par entité.<br><b>>Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire de saisir des valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées. |
| [!UICONTROL Campaign ID] | Identifiant unique qui identifie une campagne existante. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un « [!UICONTROL AMO ID] » pour la campagne. |
| [!UICONTROL Ad Group ID] | Identifiant unique qui identifie un groupe publicitaire existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un « [!UICONTROL AMO ID] » pour le groupe publicitaire. |
| [!UICONTROL Keyword ID] | Identifiant unique qui identifie un mot-clé existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez le mot-clé, à moins que la ligne ne contienne a) suffisamment de colonnes de propriétés pour identifier le mot-clé ou b) un « [!UICONTROL AMO ID] ». |
| [!UICONTROL Ad ID] | <p>Identifiant unique qui identifie une annonce publicitaire existante. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Pour les annonces responsive sur le Réseau de Recherche, l’ID d’annonce ou l’ID AMO est requis pour modifier ou supprimer les données d’annonce. Pour tous les autres types d’entité, l’ID d’annonce est requis uniquement lorsque vous modifiez le statut de l’annonce, sauf si la ligne inclut a) suffisamment de colonnes de propriétés d’annonce pour identifier l’annonce ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni la [!UICONTROL Ad ID] ni la [!UICONTROL AMO ID] et que les colonnes des propriétés de l’annonce correspondent à plusieurs annonces, le statut d’une seule des annonces change.</p><p><b>Remarque :</b> si vous modifiez a) les colonnes de propriétés de l’annonce, à l’exception de Statut pour une annonce publicitaire existante ou b) toute donnée pour une annonce responsive sur le Réseau de Recherche, et que vous n’incluez ni l’[!UICONTROL Ad ID] ni l’[!UICONTROL AMO ID], une nouvelle annonce est créée et l’annonce existante n’est pas modifiée.</p> |
| [!UICONTROL Placement ID] | Identifiant unique qui identifie un emplacement de site web. Obligatoire uniquement lorsque vous modifiez ou supprimez l’emplacement, sauf si la ligne comprend a) suffisamment de colonnes de propriété pour identifier l’emplacement ou b) un « [!UICONTROL AMO ID] ». |
| [!UICONTROL Target ID] | Identifiant unique qui identifie un ciblage automatique existant. Obligatoire uniquement lorsque vous modifiez ou supprimez la cible automatique, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL Product Group ID] | ID unique qui identifie un groupe de produits existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez le groupe de produits, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le groupe de produits ou b) un « [!UICONTROL AMO ID] ». |
| [!UICONTROL Sitelink ID] | Identifiant unique qui identifie un lien de site existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez ou supprimez le lien du site, sauf si la ligne contient a) suffisamment de colonnes de propriétés pour identifier le lien du site ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] et que les colonnes de propriété correspondent à plusieurs liens de site, le statut d’un seul des liens de site change.</p><p><b>Remarque :</b> si vous modifiez les colonnes de propriété du lien du site, à l&#39;exception de l&#39;état d&#39;un lien de site existant, et que vous n&#39;incluez ni le [!UICONTROL Sitelink ID] ni le [!UICONTROL AMO ID], un nouveau lien de site est créé et le lien existant n&#39;est pas modifié. |
| [!UICONTROL RLSA Target ID] | Identifiant unique qui identifie une cible ou une exclusion RLSA existante au niveau d’une campagne ou d’un groupe publicitaire. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez ou supprimez la cible ou l’exclusion, sauf si la ligne comprend un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL Device Target ID] | <p>Identifiant unique qui identifie une cible ou une exclusion d’appareil existante au niveau de la campagne ou du groupe publicitaire. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez ou supprimez la cible, sauf si la ligne contient un « [!UICONTROL AMO ID] » pour la cible.</p> |
| [!UICONTROL AMO ID] | (Dans les feuilles d’envoi groupé générées) Identifiant unique généré par Adobe pour une entité synchronisée. Pour les annonces responsive sur le Réseau de Recherche, l’AMO ID est requis pour modifier ou supprimer des annonces, sauf si vous incluez l’ID d’annonce. Pour modifier les données de tous les autres types d&#39;entités avec un ID AMO, l&#39;ID AMO est nécessaire pour modifier ou supprimer les données, sauf si vous incluez l&#39;ID d&#39;entité et l&#39;ID d&#39;entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |
| [!UICONTROL EF Error Message] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL EF Errors]. Cette valeur n&#39;est pas publiée sur le réseau publicitaire. |
| [!UICONTROL SE Error Message] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL SE Errors]. Cette valeur n&#39;est pas publiée sur le réseau publicitaire. |
| [!UICONTROL Exemption Request] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage du nom et du texte de toute politique publicitaire [!DNL Google Ads] enfreinte par une publicité. |
| [!UICONTROL Retail Hash] | (Inclus à titre d’information dans les feuilles d’envoi groupé générées à l’aide de la gestion avancée des campagnes) Code de hachage alphanumérique (tel que f9639f40cdf56524b541e5dacf55a991) qui indique que l’élément a été généré à l’aide de la vue Avancée (ACM). |

[^1] : [!DNL Excel] convertit les grands nombres en notation scientifique (par exemple 2.12E+09 pour 2115585666) lorsqu’il ouvre le fichier. Pour afficher les chiffres dans la notation standard, sélectionnez une cellule de la colonne et cliquez dans la barre de formule.

## Champs requis pour créer, modifier ou supprimer chaque composant de compte {#bulksheet-fields-per-component-google}

Les sections suivantes incluent les champs relatifs à des entités de compte spécifiques.

>[!NOTE]
>
>Lorsqu’un champ ne s’applique pas à une action, toute valeur saisie dans le champ est ignorée.

### Champs de campagne

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Campaign Budget] | Obligatoire pour créer une campagne. |
| [!UICONTROL Delivery Method] | Obligatoire pour créer une campagne. |
| [!UICONTROL Channel Type] | Obligatoire pour créer une campagne. |
| [!UICONTROL Networks] | Obligatoire pour créer une campagne. |
| [!UICONTROL DSA Domain Name] | Obligatoire pour créer une campagne avec des annonces de recherche dynamique sur le réseau de recherche. |
| [!UICONTROL DSA Domain Language] | Obligatoire pour créer une campagne avec des annonces de recherche dynamique sur le réseau de recherche. |
| [!UICONTROL Campaign Priority] | Obligatoire pour créer une campagne d’achat. |
| [!UICONTROL Has EU Political Ads] | Obligatoire pour créer une campagne. |
| [!UICONTROL Merchant ID] | Obligatoire pour créer une campagne d’achat. |
| [!UICONTROL Sales Country] | Obligatoire pour créer une campagne d’achat. |
| [!UICONTROL Product Scope Filter] | (Campagnes d’achat) Facultatif |
| [!UICONTROL Languages] | Facultatif |
| [!UICONTROL Device Targets] | Facultatif |
| [!UICONTROL Device Targets (Google Adwords)] | Facultatif |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Facultatif |
| [!UICONTROL Audience Target Method] | s.o. |
| [!UICONTROL Landing Page Suffix] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Campaign Status] | Obligatoire uniquement pour supprimer une campagne. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour la campagne. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de groupe publicitaire

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Networks] | s.o. |
| [!UICONTROL GDN Custom Bid Level] | Facultatif |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Group Type] | Obligatoire pour créer un groupe publicitaire. |
| [!UICONTROL Max CPC] | Facultatif |
| [!UICONTROL Max Content CPC] | Facultatif |
| [!UICONTROL Audience Target Method] | Obligatoire |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Ad Group Status] | Obligatoire uniquement pour supprimer un groupe publicitaire. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Ad Group ID] | Obligatoire uniquement lorsque vous modifiez le nom du groupe publicitaire, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour le groupe publicitaire. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de mot-clé

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Max CPC] | Facultatif |
| [!UICONTROL Keyword] | Obligatoire |
| [!UICONTROL Match Type] | Une valeur pour le type de correspondance ou l’ID de mot-clé est requise pour modifier ou supprimer un mot-clé avec plusieurs types de correspondance. |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Param1] | Facultatif |
| [!UICONTROL Param2] | Facultatif |
| [!UICONTROL Keyword Status] | Requis uniquement pour supprimer un mot-clé. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Keyword ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le mot-clé, sauf si la ligne inclut a) suffisamment de colonnes de propriété pour identifier le mot-clé ou b) un « [!UICONTROL AMO ID] ». |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs d’emplacement

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Max Placement CPC (Google Adwords)] | Facultatif |
| [!UICONTROL Max Placement CPM (Google Adwords)] | Facultatif |
| [!UICONTROL Placement] | Obligatoire |
| [!UICONTROL Match Type] | Obligatoire |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Placement Status] | Obligatoire uniquement pour supprimer un emplacement. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Placement ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez l’emplacement, sauf si la ligne comprend a) suffisamment de colonnes de propriété pour identifier l’emplacement ou b) un « [!UICONTROL AMO ID] ». |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Annonce de recherche dynamique étendue

Ce type d’annonce est désormais appelé « annonce de recherche dynamique » dans [!DNL Google Ads]. Pour plus d’informations sur la création d’annonces de recherches dynamiques, voir « [Implémenter [!DNL Google Ads] des annonces de recherches dynamiques](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html) ».

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Creative (except RSA)] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Creative Preferred Devices] | Facultatif |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Obligatoire pour créer une annonce publicitaire ou modifier la description. <b>Remarque :</b> pour ce type d’annonce, la modification de la copie d’annonce supprime l’annonce existante et en crée une nouvelle. |
| [!UICONTROL Display URL] | Obligatoire |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Creative Type] | Obligatoire pour créer ou modifier le statut d’une annonce de produit. |
| [!UICONTROL Ad Status] | Obligatoire pour supprimer une publicité. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez le statut de l’annonce, sauf si la ligne inclut a) suffisamment de colonnes de propriétés d’annonce pour identifier l’annonce ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni la [!UICONTROL Ad ID] ni la [!UICONTROL AMO ID] et que les colonnes des propriétés de l’annonce correspondent à plusieurs annonces, le statut d’une seule des annonces change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de liste de produits/d’annonces d’achats

Pour plus d’informations sur la création d’annonces d’achats, voir « [Implémenter [!DNL Google Ads] des campagnes d’achats](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html) ».

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Creative (except RSA)] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Promotion Line] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Creative Type] | Obligatoire pour créer ou modifier le statut d’une annonce de produit. |
| [!UICONTROL Ad Status] | Obligatoire pour supprimer une publicité. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez le statut de l’annonce, sauf si la ligne inclut a) suffisamment de colonnes de propriétés d’annonce pour identifier l’annonce ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni la [!UICONTROL Ad ID] ni la [!UICONTROL AMO ID] et que les colonnes des propriétés de l’annonce correspondent à plusieurs annonces, le statut d’une seule des annonces change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs publicitaires de recherche réactifs

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Responsive Search Ad] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | Pour les annonces responsive sur le Réseau de Recherche, les champs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] et [!UICONTROL Ad Title 3] sont obligatoires pour créer une annonce, et tous les autres champs de titre de l’annonce sont facultatifs. Pour supprimer la valeur existante d’un champ non obligatoire, utilisez l’`[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Facultatif |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Pour les annonces responsive sur le Réseau de Recherche, [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont nécessaires pour créer une annonce, et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatifs. Pour supprimer la valeur existante, utilisez l’`[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Facultatif |
| [!UICONTROL Display Path 1] | Facultatif |
| [!UICONTROL Display Path 2] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire pour créer une publicité. |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Creative Type] | Facultatif |
| [!UICONTROL Ad Status] | Obligatoire pour supprimer une publicité. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire pour modifier ou supprimer des annonces sauf si la ligne inclut un « [!UICONTROL AMO ID] ». |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer des annonces sauf si vous incluez l’ID d’annonce. |

### Champs d’annonce de texte

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Creative (except RSA)] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

>[!NOTE]
>
>Les annonces textuelles étendues ont été abandonnées en juin 2022. Vous pouvez uniquement supprimer les annonces de texte existantes.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Creative Preferred Devices] | Lecture seule |
| [!UICONTROL Ad Title], Titre De Publicité 2-3 | Lecture seule |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Lecture seule |
| [!UICONTROL Display URL] | Lecture seule |
| [!UICONTROL Display Path 1] | Lecture seule |
| [!UICONTROL Display Path 2] | Lecture seule |
| [!UICONTROL Tracking Template] | Lecture seule |
| [!UICONTROL Base URL/Final URL] | Lecture seule |
| [!UICONTROL Custom URL Param] | Lecture seule |
| [!UICONTROL Creative Type] | Facultatif |
| [!UICONTROL Ad Status] | Obligatoire |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez le statut de l’annonce, sauf si la ligne inclut a&amp;rpar ; suffisamment de colonnes de propriété d’annonce pour identifier l’annonce ou b&amp;rpar ; un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni la [!UICONTROL Ad ID] ni la [!UICONTROL AMO ID] et que les colonnes des propriétés de l’annonce correspondent à plusieurs annonces, le statut d’une seule des annonces change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de cible de recherche dynamique (ciblage automatique)

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Max CPC] | Facultatif |
| [!UICONTROL Auto Target Expression] | Obligatoire uniquement lorsque le paramètre de campagne « [!UICONTROL Use my website contents to target my ads] » n’est pas activé. |
| [!UICONTROL Match Type] | Facultatif |
| [!UICONTROL Target Status] | Obligatoire pour supprimer une cible |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible automatique, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs du groupe de produits d’achat

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Max CPC] | Obligatoire pour créer un groupe de produits. |
| [!UICONTROL Parent Product Groupings] | Obligatoire |
| [!UICONTROL Product Grouping] | Obligatoire |
| [!UICONTROL Partition Type] | Obligatoire pour créer un groupe de produits. |
| [!UICONTROL Match Type] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire |
| [!UICONTROL Product Group Status] | Obligatoire uniquement pour supprimer un groupe de produits. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Product Group ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le groupe de produits, à moins que la ligne ne contienne a) suffisamment de colonnes de propriétés pour identifier le groupe de produits ou b) une [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de lien de site au niveau de la campagne et du groupe publicitaire

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire pour les liens de site au niveau du groupe publicitaire. Non applicable aux liens de site au niveau de la campagne. |
| [!UICONTROL Creative Preferred Devices] | Facultatif |
| [!UICONTROL Link Name] | Obligatoire |
| [!UICONTROL Start Date] | Facultatif |
| [!UICONTROL End Date] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire |
| [!UICONTROL Sitelink Status] | Obligatoire uniquement pour supprimer un lien de site. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Sitelink ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le lien du site, sauf si la ligne inclut a) suffisamment de colonnes de propriété pour identifier le lien du site ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] et que les colonnes de propriété correspondent à plusieurs liens de site, le statut d’un seul des liens de site change.<br><br><b>Remarque :</b> si vous modifiez les colonnes des propriétés du lien du site, à l&#39;exception de [!UICONTROL Status] pour un lien de site existant, et que vous n&#39;incluez ni le [!UICONTROL Sitelink ID] ni le [!UICONTROL AMO ID], un nouveau lien de site est créé et le lien de site existant n&#39;est pas modifié. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Cible de l’emplacement

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Location] | Obligatoire |
| [!UICONTROL Location Type] | Facultatif |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Location Status] | Obligatoire uniquement pour supprimer une cible d’emplacement. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez les [!UICONTROL Campaign ID].<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs cibles d’appareil au niveau de la campagne et du groupe publicitaire

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Device] | Requis pour créer ou modifier une cible d’appareil. |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Ad Group Name] | Obligatoire pour les cibles d’appareils au niveau du groupe publicitaire. Non applicable aux cibles d’appareils au niveau de la campagne. |
| [!UICONTROL Device Target Status] | Requis uniquement pour supprimer une cible d’appareil. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif ; applicable uniquement pour les cibles d’appareils au niveau du groupe publicitaire. |
| [!UICONTROL Device Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible, sauf si la ligne comprend un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant cible de l’appareil.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de cible/exclusion du RLSA au niveau de la campagne et du groupe publicitaire

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-google) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Ad Group Name] | Obligatoire pour les cibles et exclusions au niveau du groupe publicitaire. Non applicable aux cibles et exclusions au niveau de la campagne. |
| [!UICONTROL Audience] | Obligatoire pour créer une nouvelle cible ou exclusion. |
| [!UICONTROL Target Type] | Obligatoire pour créer une nouvelle cible ou exclusion. |
| [!UICONTROL RLSA Target Status] | Obligatoire uniquement pour supprimer une cible ou une exclusion. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif ; applicable uniquement pour les cibles et exclusions au niveau du groupe publicitaire. |
| [!UICONTROL RLSA Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible, sauf si la ligne comprend un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’identifiant cible RLSA.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

>[!MORELIKETHIS]
>
>* [Annexe - Erreurs de feuille d’envoi groupé](../bulksheet-errors.md)
>* [Opérations que vous pouvez effectuer dans des feuilles d’envoi groupé](bulksheet-operations.md)
>* [Formats de fichiers de feuilles d’envoi groupé pris en charge](bulksheet-file-formats.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](../bulksheet-download.md)
>* [Formats de suivi des clics pour  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Charger un fichier de feuille d’envoi groupé ou un fichier d’erreur corrigé](../bulksheet-upload.md)
