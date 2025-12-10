---
title: 'Données de feuille d’envoi groupé requises pour les comptes  [!DNL Microsoft Advertising] '
description: Référencez les champs d’en-tête et de données obligatoires dans les feuilles d’envoi groupé pour les comptes  [!DNL Microsoft Advertising] .
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '6934'
ht-degree: 0%

---

# Annexe - Données de feuille d’envoi groupé requises pour les comptes [!DNL Microsoft Advertising]

Pour créer et mettre à jour [!DNL Microsoft Advertising] données de campagne en bloc, vous pouvez utiliser des fichiers de feuille d’envoi groupé Search, Social et Commerce formatés spécifiquement pour les comptes [!DNL Microsoft Advertising]. Vous pouvez a) [générer des fichiers de feuilles de support pour les comptes existants](../bulksheet-download.md) au format de fichier requis ou b) les créer manuellement (voir « [Formats de fichiers de feuilles de support pris en charge](bulksheet-file-formats.md) » pour obtenir des informations générales sur les formats de fichiers pris en charge).

Chaque feuille d’envoi groupé doit inclure les champs d’en-tête et les champs de données correspondants requis pour les [&#x200B; opérations spécifiques que vous souhaitez effectuer &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (telles que la création d’une annonce publicitaire). Lorsqu’un champ n’est pas obligatoire, vous pouvez l’omettre dans l’en-tête et les lignes de données. Toutes les colonnes personnalisées sont supprimées lorsque vous téléchargez le fichier de feuille en bloc.

Vous trouverez ci-dessous un tableau de tous les champs de données disponibles et des tableaux supplémentaires indiquant les champs nécessaires à l’ajout, la modification ou la suppression de données pour des entités individuelles (telles que des campagnes et des mots-clés).

## Tous les champs de données disponibles {#bulksheet-fields-all-microsoft}

Le tableau suivant décrit tous les champs de données disponibles.

Pour les champs de données pertinents pour les entités de compte, reportez-vous à « [Champs requis pour créer, modifier ou supprimer chaque composant de compte](#bulksheet-fields-per-component-microsoft) ».

| Champ | Description |
|----|----|
| [!UICONTROL Platform] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) La plateforme publicitaire. Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Acct Name] | Nom unique qui identifie un compte réseau publicitaire. Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Nom unique qui identifie une campagne pour un compte. La longueur maximale est de 128 caractères. |
| [!UICONTROL Campaign Budget] | Le budget quotidien ou mensuel de la campagne, avec ou sans symboles monétaires et ponctuation. Il ne peut pas être inférieur à 0,05. |
| [!UICONTROL Channel Type] | Type de canal ciblé par la campagne : <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i> ou <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Campagnes avec budgets quotidiens uniquement) À quelle vitesse afficher les annonces publicitaires de la campagne chaque jour :<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (valeur par défaut pour les nouvelles campagnes) : pour répartir vos impressions d’annonce publicitaire tout au long de la journée.</li><li><i>[!UICONTROL Accelerated]:</i> Affichez vos publicités aussi souvent que possible jusqu&#39;à ce que votre budget soit atteint. Par conséquent, il se peut que vos annonces n’apparaissent pas plus tard dans la journée.</li></ul> |
| [!UICONTROL Campaign Priority] | (Campagnes d’achat uniquement) Priorité d’utilisation de la campagne lorsque plusieurs campagnes font la publicité du même produit : <i>[!UICONTROL Low]</i> (valeur par défaut pour les nouvelles campagnes), <i>[!UICONTROL Medium]</i> ou <i>[!UICONTROL High]</i>.<br><br>Lorsque le même produit est inclus dans plusieurs campagnes, le réseau publicitaire utilise d’abord la priorité de campagne pour déterminer quelle campagne (et l’enchère associée) est éligible à la mise aux enchères publicitaire. Lorsque toutes les campagnes ont la même priorité, celle qui a reçu la meilleure enchère est éligible. |
| [!UICONTROL Has EU Political Ads] | (Applicable aux campagnes qui ciblent un public dans l’Union européenne (UE)) Que la campagne contienne ou non de la publicité politique conformément aux exigences du règlement de l’UE 2024/90 concernant les publicités diffusées dans l’Union européenne : <i>[!UICONTROL Yes]</i> ou <i>[!UICONTROL No]</i>. |
| [!UICONTROL Merchant ID] | (Campagnes d’achat et campagnes d’audience liées à un flux de commerçant uniquement) ID de client du compte de commerçant dont les produits sont utilisés pour la campagne. |
| [!UICONTROL Sales Country] | (Campagnes d’achat uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel les produits de la campagne sont vendus. Comme les produits sont associés aux pays cibles, ce paramètre détermine les produits qui sont annoncés dans la campagne. |
| [!UICONTROL Product Scope Filter] | (Campagnes utilisant uniquement le réseau d’achats) Produits de votre compte commercial pour lesquels des annonces de produits peuvent être créées pour la campagne. Vous pouvez saisir jusqu’à sept combinaisons de dimensions de produit et d’attributs pour filtrer vos produits à l’aide du format dimension=attribute. Séparez plusieurs filtres avec un délimiteur « > ». Pour obtenir la liste des dimensions de produit disponibles, voir « [&#x200B; Filtres de produit de campagne d’achat &#x200B;](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md) ».<br><br> Exemple : « `CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies` »<br><br> Pour supprimer les valeurs existantes, utilisez l’`[delete]` de valeur (y compris les crochets). |
| [!UICONTROL DSA Domain Name] | (Campagnes de type a) « <i>[!UICONTROL DynamicSearchAds]</i> » ou b) « <i>[!UICONTROL Search]</i> » lorsque l’élément [!DNL ExperimentId] n’est pas défini) Nom de domaine du site web à cibler pour les annonces de recherche dynamique. La longueur maximale est de 2 048 caractères. Si le nom de domaine comprend `www`, il est tronqué et n’est pas utilisé.<br><br>Pour les campagnes existantes, vous ne pouvez pas modifier le domaine, mais vous devez l’inclure pour mettre à jour d’autres propriétés. |
| [!UICONTROL DSA Domain Language] | (Campagnes de type a) « <i>[!UICONTROL DynamicSearchAds]</i> » ou b) « <i>[!UICONTROL Search]</i> » lorsque l’élément [!DNL ExperimentId] n’est pas défini) Langue des pages du site web à cibler pour les annonces de recherche dynamique. Les langues de domaine prises en charge sont [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish] et [!UICONTROL Swedish].<br><br>Pour les campagnes existantes, vous ne pouvez pas modifier la langue, mais vous devez l’inclure pour mettre à jour d’autres propriétés. |
| [!UICONTROL Ad Group Name] | Nom unique qui identifie un groupe publicitaire. La longueur maximale est de 128 caractères. Les caractères vides de fin ne sont pas enregistrés (par exemple, « Groupe publicitaire 1 » est enregistré comme « Groupe publicitaire 1 »). |
| [!UICONTROL Ad Group Type] | (Campagnes sur le réseau de recherche ; lecture seule pour les groupes publicitaires existants) Le type de groupe publicitaire : <i>[!UICONTROL Audience]</i> (pour les campagnes d’audience uniquement), <i>[!UICONTROL Search Dynamic]</i> (pour les annonces de recherche dynamique uniquement) et <i>[!UICONTROL Search Standard]</i> (pour les annonces de recherche réactives et les annonces de texte développé existantes uniquement). Certains types de campagne peuvent inclure plusieurs types de groupes publicitaires. |
| [!UICONTROL Keyword] | (Campagnes sur le réseau de recherche uniquement) Chaîne de mots-clés. La longueur maximale est de 50 caractères.<br><br><b>Remarques :</b><ul><li>Pour exclure un mot-clé au niveau du groupe publicitaire ou de la campagne, définissez la [!UICONTROL Match Type] sur `Negative`. Si la ligne contient le nom du groupe publicitaire, le mot-clé est exclu pour ce groupe publicitaire. Si la ligne n’inclut pas le nom du groupe publicitaire, le mot-clé est exclu pour l’ensemble de la campagne.</li><li>La modification d’un mot-clé [!DNL Microsoft Advertising] supprime le mot-clé existant et en crée un nouveau avec un nouvel ID de mot-clé. Toutefois, la modification du type de correspondance ne supprime pas le mot-clé existant.</li></ul> |
| Placement | Obsolète |
| [!UICONTROL Audience] | La liste de remarketing pour les annonces de recherche (RLSA) cible l’audience de la campagne ou du groupe d’annonces. |
| [!UICONTROL Target Type] | (Cibles RLSA uniquement) Type de cible : <i>[!UICONTROL Inclusion]</i> ou <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Cibles de recherche dynamique pour le groupe publicitaire. Pour toutes les cibles, utilisez « [!UICONTROL All Web Pages] ».<br><br>Pour cibler jusqu’à trois critères de recherche dynamique, utilisez le format `<category>=<target>`, où &lt;category> peut inclure l’une des catégories ci-dessous. Rejoignez plusieurs cibles pour une catégorie individuelle avec « `[blank space] and [blank space]` » et rejoignez plusieurs catégories avec « `[blank space] and [blank space]` ».<br><ul><li><i>Catégorie :</i> pour afficher des annonces de recherche dynamique pour des pages indexées avec une catégorie de contenu Google spécifique.</li><li><i>URL :</i> pour afficher des annonces de recherche dynamique pour des pages indexées avec une URL spécifique, où la valeur peut être incluse n’importe où dans l’URL.</li><li><i>Titre de la page :</i> pour afficher des annonces de recherche dynamique pour des pages indexées avec un texte spécifique dans le titre de la page.</li><li><i>Contenu de la page :</i> pour afficher des annonces de recherche dynamique pour des pages indexées avec un contenu spécifique.</li></ul>Exemple : url=shoes.example.com et page title=chaussures<br>Exemple : toutes les pages web |
| [!UICONTROL Location] | Emplacement géographique où placer des annonces pour la campagne ou le groupe d’annonces ; les valeurs ne sont pas sensibles à la casse. Si vous ne saisissez aucune valeur pour la campagne ou le groupe publicitaire, tous les emplacements sont ciblés. Pour cibler des emplacements spécifiques, saisissez l’emplacement à l’aide des formats de code d’emplacement [!DNL Microsoft Advertising]. Pour télécharger une liste d’emplacements, connectez-vous au portail de développement [!DNL Microsoft Advertising] à l’aide des informations d’identification de votre compte publicitaire [!DNL Microsoft Advertising]. <b>Remarque :</b> pour exclure un emplacement, faites précéder le code d’emplacement d’un signe moins (`-`), tel que `-United States`. |
| [!UICONTROL Location Type] | Type d’emplacement, tel que la ville, le pays, la zone métropolitaine, le code postal et l’état. Pour télécharger une liste d’emplacements, connectez-vous au portail de développement [!DNL Microsoft Advertising] à l’aide des informations d’identification de votre compte publicitaire [!DNL Microsoft Advertising]. |
| [!UICONTROL Match Type] | (Campagnes sur le réseau de recherche uniquement) Option(s) de correspondance de mots-clés. Cela peut inclure l’option de correspondance de mots-clés pour une cible de recherche dynamique ou un groupe de produits. Les valeurs sont les suivantes : <i>[!UICONTROL Broad]</i> (valeur par défaut pour les nouveaux mots-clés), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (défini automatiquement pour les mots-clés lorsque le groupe publicitaire cible le réseau de contenu), <i>[!UICONTROL Negative]</i> (pour exclure un mot-clé du réseau de contenu), <i>[!UICONTROL Dynamic Ad Target]</i> (valeur par défaut pour les nouvelles cibles de recherche dynamique), <i>[!UICONTROL Product Group]</i> (valeur par défaut pour les nouveaux groupes de produits) ou <i>[!UICONTROL Negative Product Group]</i> (pour exclure un groupe de produits).  Une valeur pour le type de correspondance ou l’ID de mot-clé est requise pour modifier ou supprimer un mot-clé avec plusieurs types de correspondance.<br><br>Pour le modificateur de correspondance large, choisissez « Large » et insérez un `+` avant tout mot requis dans le mot-clé (par exemple, « `+red +shoes` » pour exiger à la fois « rouge » et « chaussures »).<br><br>La modification du type de correspondance pour un mot-clé [!DNL Microsoft Advertising] ne supprime pas le mot-clé existant. |
| [!UICONTROL Max CPC] | (Campagnes sur le réseau de recherche) Coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire en fonction du mot-clé, du groupe de produits ou de la cible de recherche dynamique, avec ou sans symboles monétaires et ponctuation.  Pour les enregistrements de mots-clés et de groupes de produits existants dans les portfolios optimisés, les mises à jour ne sont effectives que pendant un jour et sont remplacées lors du cycle d’optimisation suivant. <b>Remarque :</b> vous ne pouvez pas enchérir sur des mots-clés négatifs. |
| [!UICONTROL Max Content CPC] | (Lecture seule pour les campagnes CPC créées avant l’abandon du réseau de contenu en 2017 uniquement ) Coût maximal du contenu par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire à partir d’un site de réseau d’affichage, avec ou sans symboles monétaires et ponctuation. |
| [!UICONTROL Audience Target Method] | (Audience et groupes) S’il faut :<ul><li><i>[!UICONTROL Target and Bid]:</i> pour afficher les annonces uniquement aux utilisateurs et utilisatrices associés aux audiences cibles qui répondent également à d’autres cibles du groupe publicitaire.</li><li><i>[!UICONTROL Bid Only]:</i>pour afficher des annonces même à des personnes qui ne sont pas associées à des audiences cibles, à condition qu’elles répondent aux cibles d’autres groupes d’annonces.</li></ul> Vous pouvez toutefois augmenter les chances que les publicités soient présentées à des audiences spécifiques en fixant des enchères plus élevées pour ces audiences. |
| [!UICONTROL Parent Product Groupings] | La hiérarchie de tous les groupes de produits parents.<br><br>Exemple : `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | Le groupe de produits (par exemple, « brand=acme » ou « All Products »).<br><br><b>Remarques :</b><ul><li>Lorsqu’un groupe de produits spécifié n’existe pas dans la hiérarchie des regroupements de produits parents, Search, Social et Commerce crée les parties de la hiérarchie nécessaires.</li><li>Search, Social et Commerce crée automatiquement un groupe « [!UICONTROL All Products] » chaque fois que vous créez un groupe publicitaire dans une campagne d’achats avec une enchère par défaut définie sur l’enchère par défaut du groupe publicitaire. Search, Social et Commerce crée automatiquement un groupe « [!UICONTROL Everything Else] » avec l’enchère par défaut du groupe publicitaire à chaque niveau de la hiérarchie des groupes de produits. Vous pouvez toujours créer explicitement ces groupes par défaut et les exclure ou modifier leurs enchères.</li><li>Chaque groupe publicitaire peut inclure jusqu’à huit niveaux de groupes de produits, y compris « [!UICONTROL All Products] » et sept autres niveaux.</li></ul> |
| [!UICONTROL Partition Type] | Type de partition du groupe de produits : <i>[!UICONTROL subdivision]</i> (s’il a des groupes de produits enfants) ou <i>[!UICONTROL unit]</i> (s’il n’a pas de groupes de produits enfants). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Annonces textuelles développées, annonces multimédias, annonces responsive et annonces responsive sur le Réseau de Recherche uniquement) Les titres d’une annonce. La longueur maximale de chaque champ de titre d’annonce est de 30 caractères ou 15 caractères codés sur deux octets, y compris tout texte dynamique (comme les valeurs des mots-clés, les variables de substitution dynamiques `{Param2}` et `{Param3}`, et les personnalisateurs d’annonce).<br><br> Pour les annonces responsive sur le Réseau de Recherche, insérez un personnalisateur d’annonce publicitaire au format suivant, où « Texte par défaut » est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide : `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Pour les annonces au format texte développé, les champs Titre de l’annonce et Titre de l’annonce 2 sont obligatoires, et [!UICONTROL Ad Title 3] est facultatif. [!DNL Microsoft Advertising] des annonces de texte développé obsolètes en août 2022. Vous ne pouvez désormais créer des rapports que sur et les supprimer.<br><br>Pour les annonces multimédias, les annonces responsive et les annonces de recherches responsive, les champs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] et [!UICONTROL Ad Title 3] sont obligatoires et tous les autres champs de titre d’annonce sont facultatifs.<br><br>Pour supprimer la valeur existante d’un champ non obligatoire, utilisez le `[delete]` de valeur (y compris les crochets).<br><br>Pour tous les types d’annonces, à l’exception des annonces au texte développé, la modification de la copie de l’annonce supprime l’annonce existante et crée une annonce avec les mêmes propriétés. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Annonces de recherche réactives uniquement ; facultatif) Position à laquelle épingler le titre d’annonce correspondant : `[null]` (aucune valeur, ce qui rend le titre d’annonce éligible à tous les postes), 1, 2 ou 3. Par exemple, si [!UICONTROL Ad Title Position] a une valeur égale à 1, [!UICONTROL Ad Title] ne peut apparaître qu’en position 1. Par défaut, tous les titres des annonces publicitaires sont nuls (n’ont pas de valeurs). Pour supprimer la valeur existante, utilisez l’`[delete]` de valeur (y compris les crochets).<br><br><b>Remarque :</b> vous pouvez épingler plusieurs titres d’annonce publicitaire à la même position. Le réseau publicitaire utilise l’un des titres de publicité épinglés à la position . Les titres épinglés en position 3 peuvent ne pas être affichés avec la publicité. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Annonces textuelles, annonces de recherche dynamique, annonces multimédias, annonces responsive, annonces de recherche réactives et liens de site au niveau de la campagne améliorés uniquement) Corps d’une annonce ou d’un lien de site.<br><br>Pour les liens de site, vous pouvez éventuellement utiliser à la fois [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] pour inclure un texte supplémentaire que le réseau publicitaire peut afficher sous le texte du lien. Chaque champ de description peut contenir jusqu’à 35 caractères codés sur un octet ou 17 caractères codés sur deux octets.<br><br>Pour les publicités, la longueur maximale de chaque champ de description est de 90 caractères ou 45 caractères codés sur deux octets, y compris tout texte dynamique (valeurs des mots-clés et personnalisateurs de publicités, par exemple).<br><br>Pour les annonces responsive sur le Réseau de Recherche, insérez un personnalisateur d’annonce publicitaire au format suivant, où Texte par défaut est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide : `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Pour les annonces textuelles et les annonces de Recherche dynamique, la ligne de description 1 est obligatoire et la [!UICONTROL Description Line 2] est facultative.<br><br>Pour les publicités multimédias, les publicités réactives et les publicités de recherche réactives, les [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont requis, et les [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatifs.<br><br>Pour supprimer la valeur existante, utilisez le `[delete]` de valeur (y compris les crochets).<br><br><b>Remarques :</b><ul><li>(Annonces de texte standard) Le titre et le texte combinés doivent comporter au moins trois mots.</li><li>(Annonces de texte développé) Ce champ peut éventuellement inclure les variables de substitution dynamiques {Param2} et {Param3}. Si c’est le cas, la longueur maximale du texte de l’annonce publicitaire est de 300 caractères codés sur un octet ou de 150 caractères codés sur deux octets. [!DNL Microsoft Advertising] des annonces de texte développé obsolètes en août 2022. Vous ne pouvez désormais créer des rapports que sur et les supprimer.</li><li>(Annonces de recherche dynamique) Le texte de substitution dynamique n’est pas autorisé.</li><li>Pour tous les types d’annonces, à l’exception des annonces au texte développé, la modification de la copie d’annonce supprime l’annonce existante et en crée une nouvelle.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Annonces de recherche réactives uniquement ; facultatif) Position à laquelle épingler la description correspondante : `[null]` (aucune valeur, ce qui rend la description éligible à toutes les positions), 1, 2 ou 3. Par exemple, si [!UICONTROL Description 1 Position] a une valeur de 1, alors la Description 1 ne peut apparaître que dans la Position 1. Par défaut, aucune description n’est épinglée à une position.<br><br>Pour supprimer la valeur existante, utilisez le `[delete]` de valeur (y compris les crochets).<br><br><b>Remarque :</b> vous pouvez épingler plusieurs descriptions à la même position. Le réseau publicitaire utilise l’une des descriptions épinglées à la position. Les descriptions épinglées en position 2 peuvent ne pas être affichées avec la publicité. |
| [!UICONTROL Business Name] | (Annonces multimédias uniquement) Nom de l’entreprise, avec un maximum de 25 caractères. |
| [!UICONTROL Promotion Line] | (Annonces de la liste de produits uniquement) Une ligne de promotion unique à inclure dans la liste de produits dans les résultats de recherche (par exemple, « Livraison gratuite maintenant! »). La longueur maximale est de 45 caractères.<br><br>La ligne de promotion peut apparaître à différents emplacements par rapport à l’annonce (comme sous l’annonce), selon l’emplacement de l’annonce sur la page. |
| [!UICONTROL Display URL] | L’URL incluse dans la publicité.<br><br>Pour les annonces de recherche dynamique étendues, le réseau publicitaire génère dynamiquement cette valeur à partir du domaine du site web et vous n’avez pas besoin de saisir de valeur.<br><br>Pour les annonces au format texte développé et les annonces de recherches réactives, il n’est pas nécessaire de saisir une valeur. L’URL affichée est automatiquement extraite du domaine dans l’URL finale. Vous pouvez éventuellement personnaliser l’URL à l’aide des champs Chemin 1 et Chemin 2 .<br><br><b>Remarques :</b><ul><li>(Comptes avec URL finales) Les noms de domaine dans l’URL d’affichage et l’URL finale doivent correspondre.</li><li>[!DNL Microsoft Advertising] des annonces de texte développé obsolètes en août 2022. Vous ne pouvez désormais créer des rapports que sur et les supprimer.</li></ul> |
| [!UICONTROL Display Path 1] | (Annonces textuelles développées, annonces de recherches dynamiques et annonces de recherches réactives uniquement) Texte ajouté à l’URL d’affichage qui est automatiquement extraite de l’URL finale. Chaque chemin est précédé dans l’URL d’une barre oblique (/). Un chemin ne peut pas contenir de barre oblique (/) ou de nouvelle ligne (\n). La longueur maximale de chaque chemin d’accès est de 15 caractères ou 7 caractères codés sur deux octets.<br><br>Pour insérer un personnalisateur d’annonce publicitaire, utilisez les formats suivants, où « Texte par défaut » est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide : `{CUSTOMIZER.Attribute name:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`<br><br>Par exemple, si [!UICONTROL Display Path 1] est « offres », l’URL d’affichage serait &lt;afficher l’URL>/offres, par exemple www.example.com/deals.<br><br>[!DNL Microsoft Advertising] des annonces de texte développé obsolètes en août 2022. Vous ne pouvez désormais créer des rapports que sur et les supprimer. |
| [!UICONTROL Display Path 1] | (Annonces textuelles développées, annonces de recherches dynamiques et annonces de recherches réactives uniquement) Un chemin d’affichage supplémentaire ; voir l’entrée pour [!UICONTROL Display Path 1].<br><br>Exemple : si [!UICONTROL Display Path 1] est « leads » et [!UICONTROL Display Path 2] est « local », l’URL d’affichage est &lt;<i>display URL</i>>/offers/local, par exemple www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Liens du site améliorés uniquement) Première date à laquelle des offres peuvent être faites pour le lien du site, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : aaaa/mm/aaaa, jj/aa, jj-aaaa ou jj-aa. La valeur par défaut des nouveaux liens de site améliorés est la date du jour. <b>Remarque :</b> les nouveaux liens de site améliorés ne peuvent être créés que dans les campagnes avec des liens de site améliorés existants ou sans liens de site. |
| [!UICONTROL End Date] | Dernière date à laquelle le lien du site peut apparaître avec des annonces, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : j/mm/aaaa, j/j/aaaa, j-j-aaaa ou j-j-aaaa. Pour un nouveau lien du site, la valeur par défaut est `[blank]` (c’est-à-dire aucune date de fin). |
| [!UICONTROL Call To Action] | Call to action à inclure dans la publicité. Consultez la [Référence d’API pour obtenir une liste des valeurs possibles](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), mais saisissez des appels à l’action à mots multiples sous la forme de mots multiples (tels que « Bet Now » au lieu de « BetNow ») dans les feuilles d’envoi groupé. |
| [!UICONTROL Call To Action Language] | Langue des options call to action. Consultez la section [&#x200B; Référence d’API pour obtenir une liste des langues possibles](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | URL de la page de destination vers laquelle les utilisateurs et utilisatrices du moteur de recherche sont dirigés lorsqu’ils cliquent sur votre annonce, y compris tout paramètre d’ajout configuré pour la campagne ou le compte. Les URL de base/finales au niveau du mot-clé remplacent celles au niveau de l’annonce et aux niveaux supérieurs.<br><br>Pour supprimer la valeur existante, utilisez le `[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Destination URL] | (Incluse dans les feuilles d&#39;envoi groupé générées à titre d&#39;information ; non publiée dans le moteur de recherche) Pour les comptes avec des URL de destination, il s&#39;agit de l&#39;URL qui lie une annonce à une URL de base/page de destination sur le site Web de l&#39;annonceur (parfois via un autre site qui suit le clic et redirige ensuite l&#39;utilisateur vers la page de destination). Elle inclut tous les paramètres d’ajout configurés pour la campagne ou le compte Search, Social et Commerce. Si vous avez généré des URL de tracking, cela dépend des paramètres de tracking définis dans les paramètres de votre compte et de votre campagne. Si vous avez ajouté des paramètres spécifiques au moteur de recherche, ils peuvent être remplacés par des paramètres équivalents pour Recherche, Social et Commerce.<br><br>Pour les comptes avec des URL finales, cette colonne affiche la même valeur que la colonne URL de base/URL finale. |
| [!UICONTROL Custom URL Param] | Données à substituer à la variable dynamique `{custom_code}` lorsque la variable est incluse dans les paramètres de tracking du compte de recherche ou des paramètres de la campagne. Pour insérer la valeur personnalisée dans l&#39;URL de tracking, vous devez télécharger le fichier de feuille d&#39;envoi groupé via l&#39;option Générer les URL de tracking . |
| [!UICONTROL Creative Type] | Le format de l’annonce : <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (annonces d’achats) ou <i>[!UICONTROL Responsive Search Ad]</i>, ou <i>[!UICONTROL Text ad]</i>. La valeur par défaut pour les nouvelles publicités est <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | Première date à laquelle les offres peuvent être placées pour le groupe publicitaire, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : jj/mm/aaaa, jj/aa, jj-aaaa ou jj-aa. Pour un nouveau groupe publicitaire, la valeur par défaut est la date actuelle. |
| [!UICONTROL Ad Group End Date] | Dernière date à laquelle les offres peuvent être placées pour le groupe publicitaire, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : jj/mm/aaaa, jj/aa, jj-aaaa ou jj-aa. Pour un nouveau groupe publicitaire, la valeur par défaut est [vide] (c’est-à-dire sans date de fin). |
| [!UICONTROL Tracking Template] | (Facultatif) Le modèle de tracking, qui spécifie toutes les redirections de domaine et tous les paramètres de tracking hors de l’atterrissage et incorpore l’URL finale dans un paramètre. Le modèle de suivi au niveau le plus granulaire (avec le mot-clé comme plus granulaire) remplace les valeurs à tous les niveaux supérieurs.<br><br>Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.<br><br>Pour les redirections et le suivi tiers, saisissez une valeur.<br><br>Pour obtenir la liste des paramètres permettant d’indiquer les URL finales dans les modèles de tracking, consultez la documentation [!DNL Microsoft Advertising].<br><br> Pour supprimer la valeur existante, utilisez le `[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Landing Page Suffix] | Tous les paramètres à ajouter à la fin des URL finales pour suivre les informations. Exemple : `param2=value1&param3=value2`<br><br>voir « [Formats de suivi des clics pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) ».<br><br>Les suffixes d’URL finaux aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent est nécessaire pour les composants de compte individuels. Pour configurer un suffixe au niveau du groupe publicitaire ou à un niveau inférieur, utilisez l’éditeur de [!DNL Microsoft Advertising]. |
| Rechercher statut réseau | S’il faut placer des annonces pour le groupe publicitaire sur différents éléments du réseau de recherche :<ul><li><i>Tous :</i> placer des annonces sur tous les réseaux de recherche Bing et les partenaires de recherche syndiqués.</li><li><i>OwnedAndOperatedOnly:</i>Pour placer des annonces uniquement sur Bing et Yahoo ! sites web.</li><li><i>SyndicationSearchOnly :</i> pour placer des annonces uniquement sur Bing et Yahoo ! partenaires de recherche syndiqués.</li><li><i>Désactivé :</i> pour placer des annonces uniquement sur le réseau de contenu (et non sur le réseau de recherche).</li></ul> Pour les nouveaux groupes d’annonces, la valeur par défaut est Activé. |
| [!UICONTROL Content Network Status] | Obsolète |
| [!UICONTROL Languages] | Langue cible des publicités du groupe publicitaire : [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish] ou [!UICONTROL Swedish]. La valeur par défaut pour les nouvelles campagnes est [!UICONTROL English].<br><br>Ce paramètre détermine les pays et les régions dans lesquels votre publicité peut être affichée. Veillez à choisir une langue compatible avec les cibles de localisation de la campagne. |
| [!UICONTROL Budget Type] | Indique si le budget est <i>[!UICONTROL Daily]</i> (par défaut) ou <i>[!UICONTROL Monthly]</i>.<br><br>Remarque : si vous affectez la campagne à un portfolio optimisé, cette valeur est automatiquement définie sur [!UICONTROL Daily]. |
| [!UICONTROL Device] | Type d’appareil pour lequel des ajustements d’offre sont effectués au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> ou <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | Ajustement d&#39;offre pour un type de cible spécifié. Par exemple, si l’enchère au niveau du mot-clé est de 1 USD et que l’ajustement de l’enchère pour les smartphones est de 50 %, l’enchère pour les smartphones est de 1,50 USD. Par défaut, toutes les cibles sont enchéries au niveau de l’enchère par mot-clé. Les pourcentages valides peuvent inclure :<ul><li>Smartphones et tablettes : -100 (pour ne pas enchérir sur le type d&#39;appareil) et de -90 à 900</li><li>Bureau : de 0 à 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | Types d’appareils sur lesquels vous préférez afficher la publicité ou le lien du site : <i>[!UICONTROL All]</i> (valeur par défaut) ou <i>[!UICONTROL Mobile]</i>. Lorsque Mobile est spécifié, le réseau tente d’afficher la publicité ou le lien du site aux utilisateurs d’appareils mobiles plutôt qu’aux utilisateurs d’ordinateurs de bureau ou de tablettes. Dans le cas contraire, le réseau affiche la publicité ou le lien du site sur n’importe quel type d’appareil. <b>Remarque :</b> Le réseau ne garantit pas qu&#39;il affichera la publicité sur le type d&#39;appareil préféré. |
| [!UICONTROL Param2] | Chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de l’annonce publicitaire contient la chaîne de substitution dynamique `{Param2}`. La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments publicitaires dans lesquels vous l’utilisez (par exemple, les titres 1 et 2 combinés peuvent contenir un maximum de 76 caractères). Pour supprimer la valeur existante, utilisez l’`[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Param3] | Chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de l’annonce publicitaire contient la chaîne de substitution dynamique `{Param3}`. La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments publicitaires dans lesquels vous l’utilisez (par exemple, les titres 1 et 2 combinés peuvent contenir un maximum de 76 caractères). Pour supprimer la valeur existante, utilisez l’`[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Link Name] | Texte du lien du site. Il doit être unique dans la campagne. Si vous spécifiez Description1 et Description2, le texte du lien du site peut contenir jusqu&#39;à 25 caractères codés sur un octet ou 12 caractères codés sur deux octets. Sinon, le texte du lien du site peut contenir jusqu&#39;à 35 caractères codés sur un octet ou 17 caractères codés sur deux octets.<br><br>[!DNL Microsoft Advertising] pouvez afficher deux, quatre ou six liens de site améliorés avec des descriptions, ou quatre ou six liens de site dans une seule ligne sans description, avec une annonce.<br><br>Vous pouvez créer des liens de site améliorés uniquement dans les campagnes avec des liens de site améliorés existants ou sans liens de site. |
| [!UICONTROL Campaign Status] | Le statut d’affichage de la campagne : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (campagnes existantes uniquement). La valeur par défaut pour les nouvelles campagnes est [!UICONTROL Active]. Pour supprimer une campagne active ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Ad Group Status] | Statut d’affichage du groupe publicitaire : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (groupes publicitaires existants uniquement). La valeur par défaut pour les nouveaux groupes publicitaires est [!UICONTROL Active]. Pour supprimer un groupe publicitaire actif ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Keyword Status] | Statut d’affichage du mot-clé : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (mots-clés existants uniquement). La valeur par défaut des nouveaux mots-clés est [!UICONTROL Active]. Pour supprimer un mot-clé actif ou en pause, saisissez la valeur `Deleted`. <b>Remarque :</b> si vous créez des URL de suivi pour un mot-clé avec plusieurs types de correspondance, le statut du mot-clé pour chaque type de correspondance doit être le même. |
| [!UICONTROL Placement Status] | Obsolète |
| [!UICONTROL Ad Status] | Statut d’affichage de l’annonce publicitaire : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (annonces existantes uniquement), <i>[!UICONTROL Disapproved]</i> (non modifiable) ou <i>[!UICONTROL Paused]</i>. La valeur par défaut pour les nouvelles publicités est [!UICONTROL Active]. Pour supprimer une publicité active ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Target Status] | Statut d’une cible de recherche dynamique : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (cibles existantes uniquement). La valeur par défaut pour les nouvelles cibles est [!UICONTROL Active]. Pour supprimer une cible active ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Sitelink Status] | Statut d&#39;affichage du lien du site : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (liens de site existants uniquement). La valeur par défaut des nouveaux liens de site est [!UICONTROL Active]. Pour supprimer un lien de site actif, saisissez la valeur `Deleted`. |
| [!UICONTROL Location Status] | Statut de la cible de l’emplacement : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (emplacements existants uniquement). La valeur par défaut pour les nouveaux emplacements est [!UICONTROL Active]. Pour supprimer un emplacement actif, saisissez la valeur `Deleted`. |
| [!UICONTROL Product Group Status] | Statut d’affichage du groupe de produits : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (groupes de produits existants uniquement). La valeur par défaut pour les nouveaux groupes de produits est [!UICONTROL Active]. Pour supprimer un groupe de produits actif, saisissez la valeur `Deleted`. |
| [!UICONTROL Device Target Status] | Statut de la cible de l’appareil au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i>. Pour les nouvelles campagnes et groupes publicitaires, la valeur par défaut est [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | Statut de la cible RLSA au niveau de la campagne ou du groupe publicitaire ou de l’exclusion (Google Ads uniquement) : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (cibles existantes uniquement). La valeur par défaut pour les nouvelles cibles ou exclusions est [!UICONTROL Active]. Pour supprimer une cible active ou une exclusion, saisissez la valeur `Deleted`. |
| \[Classification d’étiquette spécifique à l’annonceur\] | (Nom pour une classification d’étiquettes spécifique à l’annonceur, telle que « Couleur » pour une classification d’étiquettes appelée Couleur) Valeur pour la classification spécifiée associée à l’entité. Vous ne pouvez inclure qu’une seule valeur par classification par entité (telle que « rouge » pour la classification de libellé « Couleur » pour la campagne A). La longueur maximale est de 100 caractères et la valeur peut inclure des caractères ASCII et non ASCII.<br><br>Les classifications de libellés et leurs valeurs de libellé sont appliqués à tous les composants enfants ; les nouveaux composants ajoutés ultérieurement sont automatiquement associés au libellé. Les classifications d’étiquettes pour les groupes de produits sont appliquées au niveau de l’unité (le plus granulaire).<br><br>Ni le nom de la classification, ni la valeur de classification ne sont sensibles à la casse. |
| [!UICONTROL Constraints] | Contrainte affectée à l&#39;entité. Vous ne pouvez affecter qu&#39;une seule contrainte par entité.<br><b>>Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire de saisir des valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées. |
| [!UICONTROL Campaign ID] | Identifiant unique qui identifie une campagne existante. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un « [!UICONTROL AMO ID] » pour la campagne. |
| [!UICONTROL Ad Group ID] | Identifiant unique qui identifie un groupe publicitaire existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un « [!UICONTROL AMO ID] » pour le groupe publicitaire. |
| [!UICONTROL Placement ID] | Obsolète |
| [!UICONTROL Keyword ID] | Identifiant unique qui identifie un mot-clé existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez le mot-clé, à moins que la ligne ne contienne a) suffisamment de colonnes de propriétés pour identifier le mot-clé ou b) un « [!UICONTROL AMO ID] ». |
| [!UICONTROL Ad ID] | <p>Identifiant unique qui identifie une annonce publicitaire existante. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Pour les annonces responsive sur le Réseau de Recherche, l’ID d’annonce ou l’ID AMO est requis pour modifier ou supprimer les données d’annonce. Pour tous les autres types d’entités, l’ID AMO est requis uniquement lorsque vous modifiez le statut de la publicité, sauf si la ligne inclut a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni la [!UICONTROL Ad ID] ni la [!UICONTROL AMO ID] et que les colonnes des propriétés de l’annonce correspondent à plusieurs annonces, le statut d’une seule des annonces change.</p><p><b>Remarque :</b> si vous modifiez a) les colonnes de propriétés de l’annonce, à l’exception de Statut pour une annonce publicitaire existante ou b) toute donnée pour une annonce responsive sur le Réseau de Recherche, et que vous n’incluez ni l’[!UICONTROL Ad ID] ni l’[!UICONTROL AMO ID], une nouvelle annonce est créée et l’annonce existante n’est pas modifiée. </p> |
| [!UICONTROL Sitelink ID] | Identifiant unique qui identifie un lien de site existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez ou supprimez le lien du site, sauf si la ligne contient a) suffisamment de colonnes de propriétés pour identifier le lien du site ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] et que les colonnes de propriété correspondent à plusieurs liens de site, le statut d’un seul des liens de site change.</p><p><b>Remarque :</b> si vous modifiez les colonnes de propriété du lien du site, à l&#39;exception de l&#39;état d&#39;un lien de site existant, et que vous n&#39;incluez ni le [!UICONTROL Sitelink ID] ni le [!UICONTROL AMO ID], un nouveau lien de site est créé et le lien existant n&#39;est pas modifié. |
| [!UICONTROL Product Group ID] | ID unique qui identifie un groupe de produits existant. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez le groupe de produits, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le groupe de produits ou b) un « [!UICONTROL AMO ID] ». |
| Identifiant de l’emplacement | Identifiant [!DNL Microsoft Advertising] unique de la cible de l’emplacement. Pour télécharger une liste d’emplacements, connectez-vous au portail de développement [!DNL Microsoft Advertising] à l’aide des informations d’identification de votre compte publicitaire [!DNL Microsoft Advertising]. Obligatoire uniquement lorsque vous modifiez ou supprimez la cible d’emplacement, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL Target ID] | Identifiant unique qui identifie un ciblage automatique existant. Obligatoire uniquement lorsque vous modifiez ou supprimez la cible automatique, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL RLSA Target ID] | Identifiant unique qui identifie une cible RLSA existante au niveau d’une campagne ou d’un groupe publicitaire. Dans les fichiers CSV et TSV, il doit être précédé d&#39;un guillemet simple (&#39;).[^1] Requis uniquement lorsque vous modifiez ou supprimez la cible ou l’exclusion, sauf si la ligne comprend un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL AMO ID] | (Dans les feuilles d’envoi groupé générées) Identifiant unique généré par Adobe pour une entité synchronisée. Pour les annonces responsive sur le Réseau de Recherche, l’AMO ID est requis pour modifier ou supprimer des annonces, sauf si vous incluez l’ID d’annonce. Pour modifier les données de tous les autres types d&#39;entités avec un ID AMO, l&#39;ID AMO est nécessaire pour modifier ou supprimer les données, sauf si vous incluez l&#39;ID d&#39;entité et l&#39;ID d&#39;entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |
| [!UICONTROL EF Error Message] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL EF Errors]. Cette valeur n&#39;est pas publiée sur le réseau publicitaire. |
| [!UICONTROL SE Error Message] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL SE Errors]. Cette valeur n&#39;est pas publiée sur le réseau publicitaire. |
| [!UICONTROL Exemption Request] | (Inclus dans les feuilles d’envoi groupé générées à titre d’information) Espace réservé pour l’affichage des noms et du texte des politiques publicitaires de Google enfreintes par une publicité. |
| [!UICONTROL Retail Hash] | (Inclus à titre d’information dans les feuilles d’envoi groupé générées à l’aide de la gestion avancée des campagnes) Code de hachage alphanumérique (tel que f9639f40cdf56524b541e5dacf55a991) qui indique que l’élément a été généré à l’aide de la vue Avancée (ACM). |

[^1] : [!DNL Excel] convertit les grands nombres en notation scientifique (par exemple 2.12E+09 pour 2115585666) lorsqu’il ouvre le fichier. Pour afficher les chiffres dans la notation standard, sélectionnez une cellule de la colonne et cliquez dans la barre de formule.

## Champs requis pour créer, modifier ou supprimer chaque composant de compte {#bulksheet-fields-per-component-microsoft}

Les sections suivantes incluent les champs relatifs à des entités de compte spécifiques.

>[!NOTE]
>
>Lorsqu’un champ ne s’applique pas à une action, toute valeur saisie dans le champ est ignorée.

### Champs de campagne

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire. |
| [!UICONTROL Campaign Budget] | Obligatoire pour créer une campagne. |
| [!UICONTROL Channel Type] | Obligatoire pour créer une campagne. |
| [!UICONTROL Delivery Method] | Facultatif |
| [!UICONTROL Campaign Priority] | Obligatoire pour créer une campagne d’achat. |
| [!UICONTROL Has EU Political Ads] | Obligatoire pour créer une campagne. |
| [!UICONTROL Merchant ID] | Obligatoire pour créer une campagne d’achat. |
| [!UICONTROL Sales Country] | Obligatoire pour créer une campagne d’achat. |
| [!UICONTROL Product Scope Filter] | (Campagnes d’achat) Facultatif |
| [!UICONTROL DSA Domain Name] | Obligatoire pour créer une campagne de type a) « [!UICONTROL DynamicSearchAds] » ou b) « [!UICONTROL Search] » lorsque l&#39;élément [!DNL ExperimentId] n&#39;est pas défini) |
| [!UICONTROL DSA Domain Language] | Obligatoire pour créer une campagne de type a) « [!UICONTROL DynamicSearchAds] » ou b) « [!UICONTROL Search] » lorsque l&#39;élément [!DNL ExperimentId] n&#39;est pas défini) |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Landing Page Suffix] | <p>Facultatif |
| [!UICONTROL Budget Type] | Obligatoire pour créer une campagne. |
| [!UICONTROL Device] | Facultatif |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Campaign Status] | Obligatoire uniquement pour supprimer une campagne. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour la campagne. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de groupe publicitaire

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Group Type] | Obligatoire pour créer un groupe publicitaire. |
| [!UICONTROL Audience Target Method] | Obligatoire uniquement pour créer une audience et des groupes. |
| [!UICONTROL Ad Group Start Date] | Facultatif |
| [!UICONTROL Ad Group End Date] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Search Network Status] | (Campagnes sur le réseau de recherche uniquement) Facultatif |
| [!UICONTROL Languages] | Facultatif |
| [!UICONTROL Device] | Facultatif |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Ad Group Status] | Obligatoire uniquement pour supprimer un groupe publicitaire. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Ad Group ID] | Obligatoire uniquement lorsque vous modifiez le nom du groupe publicitaire, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour le groupe publicitaire. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de mot-clé

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Keyword] | Obligatoire |
| [!UICONTROL Match Type] | Une valeur pour le type de correspondance ou l’ID de mot-clé est requise pour modifier ou supprimer un mot-clé avec plusieurs types de correspondance. |
| [!UICONTROL Max CPC] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Param1] | Facultatif |
| [!UICONTROL Param2] | Facultatif |
| [!UICONTROL Keyword Status] | Requis uniquement pour supprimer un mot-clé. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Keyword ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le mot-clé, sauf si la ligne inclut a) suffisamment de colonnes de propriété pour identifier le mot-clé ou b) un « [!UICONTROL AMO ID] ». |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs publicitaires de recherche dynamique

>[!NOTE]
>
>La prise en charge de la création n’est pas disponible.

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Creative (except RSA)] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Obligatoire pour modifier la description. <b>Remarque :</b> pour ce type d’annonce, la modification de la copie d’annonce supprime l’annonce existante et en crée une nouvelle. |
| [!UICONTROL Display Path 1] | Obligatoire pour modifier le champ. |
| [!UICONTROL Display Path 2] | Obligatoire pour modifier le champ. |
| [!UICONTROL Creative Type] | Obligatoire pour créer ou modifier le statut d’une annonce de produit. |
| [!UICONTROL Creative Preferred Devices] | Facultatif |
| [!UICONTROL Ad Status] | Obligatoire pour supprimer une publicité. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez le statut de l’annonce, sauf si la ligne inclut a&amp;rpar ; suffisamment de colonnes de propriété d’annonce pour identifier l’annonce ou b&amp;rpar ; un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni la [!UICONTROL Ad ID] ni la [!UICONTROL AMO ID] et que les colonnes des propriétés de l’annonce correspondent à plusieurs annonces, le statut d’une seule des annonces change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs d’annonce de produit (achats)

Pour plus d’informations sur la création d’annonces d’achats, voir « [Implémenter [!DNL Microsoft Advertising] des campagnes d’achats](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html) ».

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Creative (except RSA)] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Promotion Line] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Creative Type] | Obligatoire pour créer ou modifier le statut d’une annonce de produit. |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Ad Status] | Obligatoire pour supprimer une publicité. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez le statut de l’annonce, sauf si la ligne inclut a) suffisamment de colonnes de propriétés d’annonce pour identifier l’annonce ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni la [!UICONTROL Ad ID] ni la [!UICONTROL AMO ID] et que les colonnes des propriétés de l’annonce correspondent à plusieurs annonces, le statut d’une seule des annonces change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs d’annonce publicitaire réactifs (multimédia)

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Creative (except RSA)] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Pour les annonces responsive, les champs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] et [!UICONTROL Ad Title 3] sont obligatoires pour créer des annonces et tous les autres champs de titre d’annonce sont facultatifs. Pour supprimer la valeur existante d’un champ non obligatoire, utilisez l’`[delete]` de valeur (y compris les crochets). <b>Remarque :</b> pour ce type d’annonce, la modification de la copie d’annonce supprime l’annonce existante et en crée une nouvelle. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont nécessaires pour créer des annonces, et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatifs. <b>Remarque :</b> pour ce type d’annonce, la modification de la copie d’annonce supprime l’annonce existante et en crée une nouvelle. |
| [!UICONTROL Business Name] | Obligatoire pour créer ou supprimer une publicité. |
| [!UICONTROL Call To Action] | Obligatoire pour créer une publicité. |
| [!UICONTROL Call To Action Language] | Obligatoire pour créer une publicité. |
| [!UICONTROL Base URL/Final URL] | Obligatoire pour créer une publicité. |
| [!UICONTROL Creative Type] | Facultatif. |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Ad Status] | Obligatoire pour supprimer une publicité. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez le statut de l’annonce, sauf si la ligne inclut a) suffisamment de colonnes de propriétés d’annonce pour identifier l’annonce ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni la [!UICONTROL Ad ID] ni la [!UICONTROL AMO ID] et que les colonnes des propriétés de l’annonce correspondent à plusieurs annonces, le statut d’une seule des annonces change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs publicitaires de recherche réactifs

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Responsive Search Ad] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Pour les annonces responsive sur le Réseau de Recherche, les champs [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] et [!UICONTROL Ad Title 3] sont obligatoires pour créer une annonce, et tous les autres champs de titre de l’annonce sont facultatifs. Pour supprimer la valeur existante d’un champ non obligatoire, utilisez l’`[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Facultatif |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Pour les annonces responsive sur le Réseau de Recherche, [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont nécessaires pour créer une annonce, et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatifs. Pour supprimer la valeur existante, utilisez l’`[delete]` de valeur (y compris les crochets). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Facultatif |
| [!UICONTROL Display Path 1] | Facultatif |
| [!UICONTROL Display Path 2] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire pour créer une publicité. |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Creative Type] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Ad Status] | Obligatoire pour supprimer une publicité. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire pour modifier ou supprimer des annonces sauf si la ligne inclut un « [!UICONTROL AMO ID] ». |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer des annonces sauf si vous incluez l’ID d’annonce. |

### Champs d’annonce de texte

Pour ce type d’annonce, utilisez la ligne « [!UICONTROL Creative (except RSA)] » dans la boîte de dialogue [!UICONTROL Download Bulksheet].

>[!NOTE]
>
>Les annonces de texte développé étaient obsolètes. Vous pouvez uniquement supprimer les annonces de texte existantes.

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Lecture seule |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Lecture seule |
| [!UICONTROL Display URL] | Lecture seule |
| [!UICONTROL Display Path 1] | Lecture seule |
| [!UICONTROL Display Path 2] | Lecture seule |
| [!UICONTROL Base URL/Final URL] | Lecture seule |
| [!UICONTROL Custom URL Param] | Lecture seule |
| [!UICONTROL Creative Type] | Facultatif |
| [!UICONTROL Tracking Template] | Lecture seule |
| [!UICONTROL Creative Preferred Devices] | Lecture seule |
| [!UICONTROL Ad Status] | Obligatoire |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez le statut de l’annonce publicitaire, sauf si la ligne comprend un « [!UICONTROL AMO ID] ». |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’annonce.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de cible de recherche dynamique (ciblage automatique)

>[!NOTE]
>
>La prise en charge de la création n’est pas disponible.

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Auto Target Expression] | Obligatoire. |
| [!UICONTROL Match Type] | Facultatif |
| [!UICONTROL Max CPC] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Target Status] | Obligatoire pour supprimer une cible |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible automatique, sauf si la ligne inclut un « [!UICONTROL AMO ID] » pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs du groupe de produits d’achat

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Match Type] | Obligatoire pour créer un groupe de produits. |
| [!UICONTROL Max CPC] | Obligatoire pour créer un groupe de produits. |
| [!UICONTROL Parent Product Groupings] | Obligatoire |
| [!UICONTROL Product Grouping] | Obligatoire |
| [!UICONTROL Partition Type] | Obligatoire pour créer un groupe de produits. |
| [!UICONTROL Base URL/Final URL] | Obligatoire |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Product Group Status] | Obligatoire uniquement pour supprimer un groupe de produits. |
| \[Classification d’étiquette spécifique à l’annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Product Group ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le groupe de produits, à moins que la ligne ne contienne a) suffisamment de colonnes de propriétés pour identifier le groupe de produits ou b) une [!UICONTROL AMO ID]. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs de lien de site au niveau de la campagne

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| Ligne de description 1 | Facultatif |
| [!UICONTROL Description Line 2] | Facultatif |
| [!UICONTROL Start Date] | Facultatif |
| [!UICONTROL End Date] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Creative Preferred Devices] | Facultatif |
| [!UICONTROL Link Name] | Obligatoire |
| [!UICONTROL Sitelink Status] | Obligatoire uniquement pour supprimer un lien de site. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Sitelink ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le lien du site, sauf si la ligne inclut a) suffisamment de colonnes de propriété pour identifier le lien du site ou b) un « [!UICONTROL AMO ID] ». Cependant, si vous n’incluez ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] et que les colonnes de propriété correspondent à plusieurs liens de site, le statut d’un seul des liens de site change.<br><br><b>Remarque :</b> si vous modifiez les colonnes de propriété du lien du site, à l&#39;exception de l&#39;état d&#39;un lien de site existant, et que vous n&#39;incluez ni le [!UICONTROL Sitelink ID] ni le [!UICONTROL AMO ID], un nouveau lien de site est créé et le lien existant n&#39;est pas modifié. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs cibles de l’emplacement

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Location] | Obligatoire |
| [!UICONTROL Location Type] | Obligatoire pour créer une cible |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Location Status] | Obligatoire uniquement pour supprimer une cible d’emplacement. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant de campagne.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs cibles d’appareil au niveau de la campagne et du groupe publicitaire

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Device] | Requis pour supprimer une cible d’appareil. |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Ad Group Name] | Obligatoire pour les cibles d’appareils au niveau du groupe publicitaire. Non applicable aux cibles d’appareils au niveau de la campagne. |
| [!UICONTROL Device Target Status] | Requis uniquement pour supprimer une cible d’appareil. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif ; applicable uniquement pour les cibles d’appareils au niveau du groupe publicitaire. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant cible de l’appareil.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’ID sur le réseau publicitaire. |

### Champs cibles RLSA au niveau de la campagne et du groupe publicitaire

Pour obtenir une description de chaque champ de données, voir « [Tous les champs de données disponibles](#bulksheet-fields-all-microsoft) ».

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire sauf si chaque ligne inclut un « [!UICONTROL AMO ID] » pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire pour les cibles au niveau du groupe publicitaire. Non applicable aux cibles au niveau de la campagne. |
| [!UICONTROL Audience] | Obligatoire pour créer une cible. |
| [!UICONTROL Target Type] | Facultatif |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL RLSA Target Status] | Obligatoire pour supprimer une cible. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif ; applicable uniquement pour les cibles au niveau du groupe publicitaire. |
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
