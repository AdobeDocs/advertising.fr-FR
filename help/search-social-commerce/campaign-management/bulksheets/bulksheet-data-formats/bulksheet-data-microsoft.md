---
title: Données de feuille d’envoi groupé requises pour [!DNL Microsoft Advertising] comptes
description: Référencez les champs d’en-tête et de données requis dans les feuilles d’envoi groupées pour [!DNL Microsoft Advertising] comptes.
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '6928'
ht-degree: 0%

---

# Annexe : Données de feuille d’envoi groupé requises pour [!DNL Microsoft Advertising] comptes

Pour créer et mettre à jour [!DNL Microsoft Advertising] les données de campagne en bloc, vous pouvez utiliser des fichiers de feuilles d’envoi groupé Search, Social et Commerce au format spécifique pour [!DNL Microsoft Advertising] comptes. Vous pouvez effectuer l’une des opérations suivantes : [générer des fichiers de feuille de support pour les comptes existants ;](../bulksheet-download.md) dans le format de fichier requis ou b) créez-les manuellement (voir &quot;[Formats de fichier de feuille de support pris en charge](bulksheet-file-formats.md)&quot; pour obtenir des informations générales sur les formats de fichiers pris en charge).

Chaque feuille d’envoi groupé doit inclure les champs d’en-tête et les champs de données correspondants requis pour la [opérations spécifiques que vous souhaitez effectuer](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (création d’une publicité, par exemple). Lorsqu’un champ n’est pas obligatoire, vous pouvez l’omettre dans les lignes d’en-tête et de données. Toutes les colonnes personnalisées sont supprimées lorsque vous chargez le fichier de feuille en bloc.

Vous trouverez ci-dessous un tableau de tous les champs de données disponibles et des tableaux supplémentaires indiquant les champs obligatoires pour ajouter, modifier ou supprimer des données pour des entités individuelles (telles que des campagnes et des mots-clés).

## Tous les champs de données disponibles {#bulksheet-fields-all-microsoft}

Le tableau suivant décrit tous les champs de données disponibles.

Pour les champs de données pertinents pour les entités de compte, voir &quot;[Champs requis pour créer, modifier ou supprimer chaque composant de compte](#bulksheet-fields-per-component-microsoft).&quot;

| Champ | Description |
|----|----|
| [!UICONTROL Platform] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) La plateforme publicitaire. Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Acct Name] | Nom unique qui identifie un compte réseau publicitaire. Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Nom unique qui identifie une campagne pour un compte. La longueur maximale est de 128 caractères. |
| [!UICONTROL Campaign Budget] | Le budget quotidien ou mensuel de la campagne, avec ou sans symboles monétaires et ponctuation. Elle ne peut pas être inférieure à 0,05. |
| [!UICONTROL Channel Type] | Type de canal ciblé par la campagne : <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i>, ou <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Campagnes avec budgets quotidiens uniquement) La vitesse à laquelle afficher les publicités pour la campagne chaque jour :<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (valeur par défaut pour les nouvelles campagnes) : pour diffuser vos impressions publicitaires tout au long de la journée.</li><li><i>[!UICONTROL Accelerated]:</i> Pour afficher vos publicités aussi souvent que possible jusqu&#39;à ce que votre budget soit atteint. Par conséquent, vos publicités peuvent ne pas apparaître plus tard dans la journée.</li></ul> |
| [!UICONTROL Campaign Priority] | (Campagnes d’achat uniquement) La priorité avec laquelle la campagne est utilisée lorsque plusieurs campagnes font de la publicité sur le même produit : <i>[!UICONTROL Low]</i> (valeur par défaut pour les nouvelles campagnes), <i>[!UICONTROL Medium]</i>, ou <i>[!UICONTROL High]</i>.<br><br>Lorsqu’un même produit est inclus dans plusieurs campagnes, le réseau publicitaire utilise d’abord la priorité de la campagne pour déterminer la campagne (et l’offre associée) éligible aux enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible. |
| [!UICONTROL Merchant ID] | (Campagnes d’achat et campagnes d’audience liées à un flux marchand uniquement) Identifiant client du compte marchand dont les produits sont utilisés pour la campagne. |
| [!UICONTROL Sales Country] | (Campagnes d’achat uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel les produits de la campagne sont vendus. Les produits étant associés aux pays cibles, ce paramètre détermine les produits faisant l’objet d’une publicité dans la campagne. |
| [!UICONTROL Product Scope Filter] | (Campagnes utilisant uniquement le réseau d’achat) Produits de votre compte marchand pour lesquels des publicités de produits peuvent être créées pour la campagne. Vous pouvez saisir jusqu’à sept combinaisons de dimensions et d’attributs de produit sur lesquelles filtrer vos produits, en utilisant le format dimension=attribut . Séparez plusieurs filtres par un délimiteur &quot;>&quot;. Pour obtenir la liste des dimensions de produit disponibles, voir &quot;[Filtres de produits de campagne d&#39;achat](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Exemple : &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Pour supprimer les valeurs existantes, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL DSA Domain Name] | (Campagnes de type a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; ou b) &quot;<i>[!UICONTROL Search]</i>&quot; lorsque la variable [!DNL ExperimentId] n’est pas défini) Le nom de domaine du site web vers lequel cibler les annonces de recherche dynamique. La longueur maximale est de 2 048 caractères. Si le nom de domaine comprend `www`, il est rogné et n’est pas utilisé.<br><br>Pour les campagnes existantes, vous ne pouvez pas modifier le domaine, mais vous devez l’inclure pour mettre à jour d’autres propriétés. |
| [!UICONTROL DSA Domain Language] | (Campagnes de type a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; ou b) &quot;<i>[!UICONTROL Search]</i>&quot; lorsque la variable [!DNL ExperimentId] n’est pas défini) Langue des pages du site web vers laquelle cibler les annonces de recherche dynamique. Les langues de domaine prises en charge sont : [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish], et [!UICONTROL Swedish].<br><br>Pour les campagnes existantes, vous ne pouvez pas modifier la langue, mais vous devez l’inclure pour mettre à jour d’autres propriétés. |
| [!UICONTROL Ad Group Name] | Nom unique qui identifie un groupe publicitaire. La longueur maximale est de 128 caractères. Les caractères vides de fin ne sont pas enregistrés (par exemple, &quot;Groupe d’annonces 1&quot; est enregistré comme &quot;Groupe d’annonces 1&quot;). |
| [!UICONTROL Ad Group Type] | (Campagnes sur le réseau de recherche ; lecture seule pour les groupes publicitaires existants) Type de groupe publicitaire : <i>[!UICONTROL Audience]</i> (pour les campagnes d’audience uniquement), <i>[!UICONTROL Search Dynamic]</i> (pour les annonces de recherche dynamique uniquement) et <i>[!UICONTROL Search Standard]</i> (pour les annonces responsives sur le Réseau de Recherche et les annonces textuelles étendues existantes uniquement). Certains types de campagne peuvent inclure plusieurs types de groupes d’annonces. |
| [!UICONTROL Keyword] | (Campagnes sur le réseau de recherche uniquement) Chaîne de mot-clé. La longueur maximale est de 50 caractères.<br><br><b>Remarques :</b><ul><li>Pour exclure un mot-clé au niveau du groupe publicitaire ou de la campagne, définissez la variable [!UICONTROL Match Type] to `Negative`. Si la ligne comprend le nom du groupe publicitaire, le mot-clé est exclu du groupe publicitaire. Si la ligne ne contient pas le nom du groupe publicitaire, le mot-clé est exclu pour l’ensemble de la campagne.</li><li>Modification d’un [!DNL Microsoft Advertising] Le mot-clé supprime le mot-clé existant et en crée un nouveau avec un nouvel identifiant de mot-clé. Toutefois, le fait de modifier le type de correspondance ne supprime pas le mot-clé existant.</li></ul> |
| Emplacement | Obsolète |
| [!UICONTROL Audience] | La liste de remarketing des annonces de recherche (RLSA) cible l’audience de la campagne ou du groupe publicitaire. |
| [!UICONTROL Target Type] | (Cibles RLSA uniquement) Le type de cible : <i>[!UICONTROL Inclusion]</i> ou <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Cibles de recherche dynamique pour le groupe publicitaire. Pour toutes les cibles, utilisez &quot;[!UICONTROL All Web Pages].&quot;<br><br>Pour cibler jusqu’à trois critères de recherche dynamique, utilisez le format `<category>=<target>`, où &lt;category> peut inclure l’une des catégories ci-dessous. Rejoindre plusieurs cibles pour une catégorie individuelle avec &quot;`[blank space] and [blank space]`&quot; et joindre plusieurs catégories à l’aide de &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Catégorie :</i> Pour afficher des annonces de recherche dynamique pour des pages indexées avec une catégorie de contenu Google spécifique.</li><li><i>URL :</i> Pour afficher des annonces de recherche dynamique pour des pages indexées avec une URL spécifique, où la valeur peut être incluse n’importe où dans l’URL.</li><li><i>Titre de la page :</i> Pour afficher des annonces de recherche dynamique pour des pages indexées avec du texte spécifique dans le titre de la page.</li><li><i>Contenu de la page :</i> Pour afficher des annonces de recherche dynamique pour des pages indexées avec du contenu spécifique.</li></ul>Exemple : url=shoes.example.com et page title=chaussures<br>Exemple : toutes les pages web |
| [!UICONTROL Location] | Emplacement géographique où placer des publicités pour la campagne ou le groupe publicitaire ; les valeurs ne sont pas sensibles à la casse. Si vous ne saisissez aucune valeur pour la campagne ou le groupe publicitaire, tous les emplacements sont ciblés. Pour cibler des emplacements spécifiques, saisissez l’emplacement à l’aide du [!DNL Microsoft Advertising] formats de code d’emplacement. Pour télécharger une liste d’emplacements, connectez-vous au [!DNL Microsoft Advertising] portail destiné aux développeurs utilisant votre [!DNL Microsoft Advertising] informations d’identification du compte publicitaire. <b>Remarque :</b> Pour exclure un emplacement, faites précéder le code de l’emplacement d’un signe moins (`-`), par exemple `-United States`. |
| [!UICONTROL Location Type] | Le type d’emplacement, par exemple Ville, Pays, Zone de métro, Code postal et État. Pour télécharger une liste d’emplacements, connectez-vous au [!DNL Microsoft Advertising] portail destiné aux développeurs utilisant votre [!DNL Microsoft Advertising] informations d’identification du compte publicitaire. |
| [!UICONTROL Match Type] | (Campagnes sur le réseau de recherche uniquement) La ou les options de correspondance des mots-clés. Cela peut inclure l’option de correspondance de mots-clés pour une cible de recherche dynamique ou un groupe de produits. Les valeurs sont les suivantes : <i>[!UICONTROL Broad]</i> (valeur par défaut des nouveaux mots-clés), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (définie automatiquement pour les mots-clés lorsque le groupe publicitaire cible le réseau de contenu), <i>[!UICONTROL Negative]</i> (pour exclure un mot-clé du réseau de contenu), <i>[!UICONTROL Dynamic Ad Target]</i> (valeur par défaut pour les nouvelles cibles de recherche dynamique), <i>[!UICONTROL Product Group]</i> (valeur par défaut pour les nouveaux groupes de produits) ou <i>[!UICONTROL Negative Product Group]</i> (pour exclure un groupe de produits).  Une valeur pour le type de correspondance ou l’ID de mot-clé est requise pour modifier ou supprimer un mot-clé avec plusieurs types de correspondance.<br><br>Pour le modificateur de correspondance large, sélectionnez &quot;Large&quot; et insérez une `+` avant tout mot du mot-clé requis (tel que &quot;`+red +shoes`&quot; pour exiger à la fois &quot;rouge&quot; et &quot;chaussures&quot;).<br><br>Modification du type de correspondance pour un [!DNL Microsoft Advertising] Le mot-clé ne supprime pas le mot-clé existant. |
| [!UICONTROL Max CPC] | (Campagnes sur le réseau de recherche) Coût par clic maximum, qui est le montant le plus élevé à payer pour un clic publicitaire en fonction du mot-clé, du groupe de produits ou de la cible de recherche dynamique, avec ou sans symboles monétaires et ponctuation.  Pour les mots-clés et les enregistrements de groupes de produits existants dans les portfolios optimisés, les mises à jour sont effectives une seule journée et sont remplacées au cours du cycle d’optimisation suivant. <b>Remarque :</b> Vous ne pouvez pas définir d’offres pour les mots-clés négatifs. |
| [!UICONTROL Max Content CPC] | (Lecture seule pour les campagnes CPC créées avant que le réseau de contenu ne devienne obsolète en 2017 uniquement ) Le coût maximum par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire sur un site de réseau d’affichage, avec ou sans symboles monétaires et ponctuation. |
| [!UICONTROL Audience Target Method] | (Groupes d’audiences) Si :<ul><li><i>[!UICONTROL Target and Bid]:</i> Pour afficher les publicités uniquement aux utilisateurs associés aux audiences cibles qui correspondent également à d’autres cibles du groupe publicitaire.</li><li><i>[!UICONTROL Bid Only]:</i>Afficher les publicités même aux personnes qui ne sont pas associées aux audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire.</li></ul> Vous pouvez toutefois augmenter les chances d&#39;affichage des publicités à des audiences spécifiques en définissant des offres plus élevées pour ces audiences. |
| [!UICONTROL Parent Product Groupings] | Hiérarchie de tous les groupes de produits parents.<br><br>Exemple : `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | Groupe de produits (par exemple &quot;marque=acme&quot; ou &quot;Tous les produits&quot;).<br><br><b>Remarques :</b><ul><li>Lorsqu’un groupe de produits spécifié n’existe pas dans la hiérarchie des groupes de produits parents, Search, Social et Commerce crée les parties de la hiérarchie qui sont nécessaires.</li><li>La recherche, Social et Commerce créent automatiquement un[!UICONTROL All Products]groupe &quot; chaque fois que vous créez un groupe publicitaire dans une campagne d’achat avec une offre par défaut définie sur l’offre par défaut du groupe publicitaire. La recherche, Social et Commerce créent automatiquement un[!UICONTROL Everything Else]groupe avec l’offre par défaut du groupe publicitaire à chaque niveau de la hiérarchie des groupes de produits. Vous pouvez toujours créer explicitement ces groupes et les exclure ou modifier leurs offres.</li><li>Chaque groupe d’annonces peut inclure jusqu’à huit niveaux de groupes de produits, y compris &quot;[!UICONTROL All Products]&quot; et sept autres niveaux.</li></ul> |
| [!UICONTROL Partition Type] | Type de partition pour le groupe de produits : <i>[!UICONTROL subdivision]</i> (s’il comporte des groupes de produits enfants) ou <i>[!UICONTROL unit]</i> (lorsqu’il n’a aucun groupe de produits enfant). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Publicités textuelles étendues, annonces multimédias, annonces réactives et annonces responsives uniquement) Les titres d’une publicité. La longueur maximale de chaque champ de titre de publicité est de 30 ou 15 caractères codés sur deux octets, y compris tout texte dynamique (comme les valeurs des mots-clés, `{Param2}` et `{Param3}` variables de substitution dynamiques et personnalisateurs de publicités).<br><br> Pour les annonces responsives sur le Réseau de Recherche, insérez un personnaliseur de Publicités au format suivant, où &quot;Texte par défaut&quot; est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide : `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Pour les publicités textuelles étendues, le titre de la publicité et le titre de la publicité 2 sont requis, et [!UICONTROL Ad Title 3] est facultatif. [!DNL Microsoft Advertising] publicités textuelles étendues obsolètes en août 2022. Vous pouvez désormais uniquement créer des rapports et les supprimer.<br><br>Pour les annonces multimédias, les annonces réactives et les annonces responsives sur la Recherche, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], et [!UICONTROL Ad Title 3] sont obligatoires et tous les autres champs de titre de publicité sont facultatifs.<br><br>Pour supprimer la valeur existante pour un champ non obligatoire, utilisez la valeur `[delete]` (y compris les crochets).<br><br>Pour tous les types d’annonces, à l’exception des publicités textuelles étendues, la modification de la copie de la publicité supprime la publicité existante et crée une nouvelle publicité avec les mêmes propriétés. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Publicités de recherche réactive uniquement ; facultatif) position à laquelle épingler le titre de publicité correspondant : `[null]` (aucune valeur, ce qui rend le titre de la publicité éligible pour tous les postes), 1, 2 ou 3. Par exemple, si [!UICONTROL Ad Title Position] a la valeur 1, puis [!UICONTROL Ad Title] peut apparaître uniquement dans la position 1. Par défaut, tous les titres de publicité sont nuls (ne comportent aucune valeur). Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets).<br><br><b>Remarque :</b> Vous pouvez épingler plusieurs titres de publicité à la même position. Le réseau publicitaire utilise l’un des titres de publicité épinglés à la position. Il se peut que les titres épinglés à la position 3 ne s’affichent pas avec la publicité. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Publicités texte, annonces dynamiques de recherche, annonces multimédias, annonces réactives, annonces responsives de recherche et liens de site améliorés au niveau de la campagne uniquement) Corps d’une publicité ou d’un lien de site.<br><br>Pour les liens de site, utilisez éventuellement les deux [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] pour inclure du texte supplémentaire que le réseau publicitaire peut afficher sous le texte du lien. Chaque champ de description peut contenir jusqu’à 35 caractères sur un ou 17 caractères sur deux octets.<br><br>Pour les publicités, la longueur maximale de chaque champ de description est de 90 caractères ou 45 caractères codés sur deux octets, y compris tout texte dynamique (comme les valeurs des mots-clés et des personnalisateurs de publicités).<br><br>Pour les annonces responsives sur le Réseau de Recherche, insérez un personnaliseur de Publicités au format suivant, où le Texte par défaut est une valeur facultative à insérer lorsque votre fichier de Flux n’inclut pas de valeur valide : `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Pour les annonces textuelles et les annonces de recherche dynamique, la ligne de description 1 est requise et [!UICONTROL Description Line 2] est facultatif.<br><br>Pour les annonces multimédias, les annonces réactives et les annonces responsives sur la Recherche, [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont requises, et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatives.<br><br>Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets).<br><br><b>Remarques :</b><ul><li>(Publicités textuelles standard) Le titre et le texte combinés doivent contenir au moins trois mots.</li><li>(Publicités textuelles étendues) Ce champ peut éventuellement inclure la variable {Param2} et {Param3} variables de substitution dynamiques. Si tel est le cas, la longueur maximale du texte de publicité est de 300 caractères sur un ou 150 caractères sur deux octets. [!DNL Microsoft Advertising] publicités textuelles étendues obsolètes en août 2022. Vous pouvez désormais uniquement créer des rapports et les supprimer.</li><li>(Publicités de recherche dynamique) Le texte de substitution dynamique n’est pas autorisé.</li><li>Pour tous les types d’annonces, à l’exception des publicités textuelles étendues, la modification de la copie d’annonce supprime la publicité existante et en crée une nouvelle.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Publicités de recherche réactive uniquement ; facultatif) position à laquelle épingler la description correspondante : `[null]` (aucune valeur, ce qui rend la description éligible pour tous les postes), 1, 2 ou 3. Par exemple, si [!UICONTROL Description 1 Position] a une valeur de 1, alors la description 1 ne peut apparaître que dans la position 1. Par défaut, aucune description n’est épinglée à une position.<br><br>Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets).<br><br><b>Remarque :</b> Vous pouvez épingler plusieurs descriptions à la même position. Le réseau publicitaire utilise l’une des descriptions épinglées à la position. Il se peut que les descriptions épinglées à la position 2 ne s’affichent pas avec la publicité. |
| [!UICONTROL Business Name] | (Publicités multimédias uniquement) Nom de l’entreprise, avec un maximum de 25 caractères. |
| [!UICONTROL Promotion Line] | (Publicités avec liste de produits uniquement) Ligne de promotion unique à inclure à la liste de produits dans les résultats de recherche (par exemple, &quot;Livraison gratuite maintenant !). La longueur maximale est de 45 caractères.<br><br>La ligne de promotion peut apparaître à différents emplacements par rapport à la publicité (par exemple sous la publicité), selon l’emplacement de la publicité sur la page. |
| [!UICONTROL Display URL] | URL incluse dans la publicité.<br><br>Pour les annonces de recherche dynamique étendues, le réseau publicitaire génère dynamiquement cette valeur à partir du domaine du site web et vous n’avez pas besoin de saisir de valeur.<br><br>Pour les annonces textuelles étendues et les annonces de recherche réactive, il n’est pas nécessaire de saisir une valeur. L’URL d’affichage est automatiquement extraite du domaine dans l’URL finale. Vous pouvez éventuellement personnaliser l’URL à l’aide des champs Chemin 1 et Chemin 2 .<br><br><b>Remarques :</b><ul><li>(Comptes avec URL finales) Les noms de domaine dans l’URL d’affichage et l’URL finale doivent correspondre.</li><li>[!DNL Microsoft Advertising] publicités textuelles étendues obsolètes en août 2022. Vous pouvez désormais uniquement créer des rapports et les supprimer.</li></ul> |
| [!UICONTROL Display Path 1] | (Publicités textuelles étendues, annonces de recherche dynamique et annonces de recherche réactive uniquement) Texte ajouté à l’URL d’affichage automatiquement extrait de l’URL finale. Chaque chemin est précédé d’une barre oblique (/) dans l’URL. Un chemin ne peut pas contenir de barre oblique (/) ou de caractères de saut de page (\n). La longueur maximale de chaque chemin est de 15 ou 7 caractères codés sur deux octets.<br><br>Pour insérer un personnalisateur de publicités, utilisez les formats suivants, où &quot;Texte par défaut&quot; est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide : `{CUSTOMIZER.Attribute name:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`<br><br>Par exemple, si [!UICONTROL Display Path 1] est &quot;offres&quot;, l’URL d’affichage serait &lt;display url=&quot;&quot;>/offres, par exemple www.example.com/deals.<br><br>[!DNL Microsoft Advertising] publicités textuelles étendues obsolètes en août 2022. Vous pouvez désormais uniquement créer des rapports et les supprimer. |
| [!UICONTROL Display Path 1] | (Publicités textuelles étendues, annonces de recherche dynamique et annonces de recherche réactive uniquement) Chemin d’affichage supplémentaire ; voir l’entrée pour [!UICONTROL Display Path 1].<br><br>Exemple : if [!UICONTROL Display Path 1] est &quot;offres&quot; et [!UICONTROL Display Path 2] est &quot;local&quot;, l’URL d’affichage est &lt;<i>URL d’affichage</i>>/offres/local, par exemple www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Liens de site améliorés uniquement) Date à laquelle les offres peuvent être placées pour le lien de site, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : m/j/aaaa, m/d/aa, m-d-aaaa ou m-d-yy. La valeur par défaut des nouveaux liens de site améliorés est la journée actuelle. <b>Remarque :</b> Les nouveaux liens de site améliorés ne peuvent être créés que dans les campagnes avec des liens de site améliorés existants ou sans lien de site. |
| [!UICONTROL End Date] | Dernière date à laquelle le lien du site peut apparaître avec les publicités, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : m/j/aaaa, m/d/aa, m-d-aaaa ou m-d-aaaa. Pour un nouveau lien de site, la valeur par défaut est `[blank]` (c’est-à-dire, aucune date de fin). |
| [!UICONTROL Call To Action] | Appel à l’action à inclure dans la publicité. Voir [Référence d’API pour une liste de valeurs possibles](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), mais saisissez des appels à l’action à plusieurs mots comme plusieurs mots (par exemple &quot;Pari maintenant&quot; au lieu de &quot;Pari maintenant&quot;) dans des feuilles d’envoi groupées. |
| [!UICONTROL Call To Action Language] | Langue des options d’appel à l’action. Voir [Référence de l’API pour une liste des langues possibles](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | URL de la page d’entrée vers laquelle les utilisateurs du moteur de recherche sont pris lorsqu’ils cliquent sur votre publicité, y compris les paramètres d’ajout configurés pour la campagne ou le compte. Les URL de base/finale au niveau du mot-clé remplacent celles au niveau de la publicité et supérieures.<br><br>Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Destination URL] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information ; non publiés dans le moteur de recherche) Pour les comptes avec des URL de destination, il s’agit de l’URL qui lie une publicité à une URL/page d’entrée de base sur le site web de l’annonceur (parfois via un autre site qui effectue le suivi des clics, puis redirige l’utilisateur vers la page d’entrée). Il comprend tous les paramètres d’ajout configurés pour la campagne ou le compte Search, Social et Commerce. Si vous avez généré des URL de suivi, elles sont basées sur les paramètres de suivi définis dans les paramètres de votre compte et de vos campagnes. Si vous avez ajouté des paramètres spécifiques au moteur de recherche, ils peuvent être remplacés par les paramètres équivalents pour Search, Social et Commerce.<br><br>Pour les comptes disposant d’URL finales, cette colonne affiche la même valeur que la colonne URL de base/URL finale. |
| [!UICONTROL Custom URL Param] | Données à remplacer par la variable `{custom_code}` variable dynamique lorsque la variable est incluse dans les paramètres de suivi pour le compte de recherche ou les paramètres de campagne. Pour insérer la valeur personnalisée dans l’URL de tracking, vous devez télécharger le fichier de feuille d’envoi groupé à l’aide de l’option Générer les URL de tracking . |
| [!UICONTROL Creative Type] | Format de la publicité : <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (publicités commerciales) ou <i>[!UICONTROL Responsive Search Ad]</i>, ou <i>[!UICONTROL Text ad]</i>. La valeur par défaut pour les nouvelles publicités est <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | Date à laquelle les offres peuvent être placées pour le groupe publicitaire, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : m/j/aaaa, m/d/aa, m-d-aaaa ou m-d-aa. Pour un nouveau groupe publicitaire, la date par défaut est la date actuelle. |
| [!UICONTROL Ad Group End Date] | Dernière date à laquelle les offres peuvent être placées pour le groupe publicitaire, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : m/j/aaaa, m/d/aa, m-d-aaaa ou m-d-yy. Pour un nouveau groupe publicitaire, la valeur par défaut est [blank] (c’est-à-dire, aucune date de fin). |
| [!UICONTROL Tracking Template] | (Facultatif) Le modèle de suivi, qui spécifie tous les paramètres de suivi et redirections de domaine hors d’entrée et incorpore l’URL finale dans un paramètre. Le modèle de suivi au niveau le plus granulaire (avec le mot-clé comme le plus granulaire) remplace les valeurs à tous les niveaux supérieurs.<br><br>Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.<br><br>Pour les redirections et le suivi tiers, saisissez une valeur.<br><br>Pour obtenir une liste des paramètres permettant d’indiquer les URL finales dans les modèles de suivi, voir la section [!DNL Microsoft Advertising] la documentation.<br><br> Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Landing Page Suffix] | Tous les paramètres à ajouter à la fin des URL finales pour suivre les informations. Exemple : `param2=value1&param3=value2`<br><br>Voir &quot;[Formats de suivi des clics pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>Les suffixes d’URL finaux aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez la méthode [!DNL Microsoft Advertising] éditeur. |
| État du réseau de recherche | Indique s’il faut placer des publicités pour le groupe sur différents éléments du réseau de recherche :<ul><li><i>Tous :</i> Pour placer des publicités sur tous les réseaux de recherche Bing et les partenaires de recherche syndiqués.</li><li><i>OwnedAndOperatedOnly :</i>Pour placer des publicités uniquement sur Bing et Yahoo! sites web.</li><li><i>SyndicationSearchOnly :</i> Pour placer des publicités uniquement sur Bing et Yahoo! partenaires de recherche syndiqués.</li><li><i>Désactivé :</i> Pour placer des publicités sur le réseau de contenu uniquement (et non sur le réseau de recherche).</li></ul> Pour les nouveaux groupes d’annonces, la valeur par défaut est Activé. |
| [!UICONTROL Content Network Status] | Obsolète |
| [!UICONTROL Languages] | Langue cible des publicités du groupe publicitaire : [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish], ou [!UICONTROL Swedish]. La valeur par défaut pour les nouvelles campagnes est [!UICONTROL English].<br><br>Ce paramètre détermine les pays et les régions dans lesquels votre publicité peut être affichée. Veillez à choisir une langue compatible avec les cibles de localisation de la campagne. |
| [!UICONTROL Budget Type] | Indique si le budget est <i>[!UICONTROL Daily]</i> (valeur par défaut) ou <i>[!UICONTROL Monthly]</i>.<br><br>Remarque : Si vous attribuez la campagne à un portfolio optimisé, cette valeur est automatiquement définie sur [!UICONTROL Daily]. |
| [!UICONTROL Device] | Type d’appareil pour lequel des ajustements d’offre sont effectués au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>, ou <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | Ajustement de l’offre pour un type de cible spécifié. Par exemple, si l’offre au niveau du mot-clé est de 1 USD et que l’ajustement de l’offre pour les smartphones est de 50 %, l’offre pour les smartphones est de 1,50 USD. Par défaut, toutes les cibles sont proposées au niveau de l’offre au niveau du mot-clé. Les pourcentages valides peuvent inclure :<ul><li>Smartphones et tablettes : -100 (pour ne pas enchérir pour le type d’appareil) et de -90 à 900</li><li>Bureau : de 0 à 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | Types d’appareils sur lesquels vous préférez afficher la publicité ou le lien de site : <i>[!UICONTROL All]</i> (valeur par défaut) ou <i>[!UICONTROL Mobile]</i>. Lorsque Mobile est spécifié, le réseau tente d’afficher la publicité ou le lien de site pour les utilisateurs d’appareils mobiles plutôt que pour les utilisateurs d’ordinateurs de bureau ou de tablettes. Sinon, le réseau affiche la publicité ou le lien de site sur n’importe quel type d’appareil. <b>Remarque :</b> Le réseau ne garantit pas qu’il affichera la publicité sur le type d’appareil préféré. |
| [!UICONTROL Param2] | Chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de la publicité contient le paramètre `{Param2}` chaîne de substitution dynamique. La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments de publicité dans lesquels vous l’utilisez (par exemple, le titre 1 et le titre 2 combinés peuvent contenir un maximum de 76 caractères). Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Param3] | Chaîne à utiliser comme valeur de substitution si l’URL de base du mot-clé ou le titre, la description ou l’URL de base de la publicité contient le paramètre `{Param3}` chaîne de substitution dynamique. La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments de publicité dans lesquels vous l’utilisez (par exemple, le titre 1 et le titre 2 combinés peuvent contenir un maximum de 76 caractères). Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Link Name] | Le texte du lien de site. Elle doit être unique dans la campagne. Si vous spécifiez Description1 et Description2, le texte du lien de site peut contenir jusqu’à 25 caractères codés sur un ou 12 caractères codés sur deux octets ; dans le cas contraire, le texte du lien de site peut contenir jusqu’à 35 caractères codés sur un ou 17 caractères codés sur deux octets.<br><br>[!DNL Microsoft Advertising] peut afficher deux, quatre ou six liens de site améliorés avec des descriptions, ou quatre ou six liens de site sur une seule ligne sans description, avec une publicité.<br><br>Vous pouvez créer de nouveaux liens de site améliorés uniquement dans les campagnes avec des liens de site améliorés existants ou pas de liens de site. |
| [!UICONTROL Campaign Status] | Etat d&#39;affichage de l&#39;opération : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, ou <i>[!UICONTROL Deleted]</i> (campagnes existantes uniquement). La valeur par défaut pour les nouvelles campagnes est [!UICONTROL Active]. Pour supprimer une campagne active ou suspendue, saisissez la valeur `Deleted`. |
| [!UICONTROL Ad Group Status] | État d’affichage du groupe publicitaire : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, ou <i>[!UICONTROL Deleted]</i> (groupes publicitaires existants uniquement). La valeur par défaut pour les nouveaux groupes publicitaires est [!UICONTROL Active]. Pour supprimer un groupe publicitaire actif ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Keyword Status] | L’état d’affichage du mot-clé : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, ou <i>[!UICONTROL Deleted]</i> (mots-clés existants uniquement). La valeur par défaut des nouveaux mots-clés est [!UICONTROL Active]. Pour supprimer un mot-clé actif ou en pause, saisissez la valeur `Deleted`. <b>Remarque :</b> Si vous créez des URL de suivi pour un mot-clé avec plusieurs types de correspondance, l’état du mot-clé pour chaque type de correspondance doit être le même. |
| [!UICONTROL Placement Status] | Obsolète |
| [!UICONTROL Ad Status] | État d’affichage de la publicité : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (publicités existantes uniquement), <i>[!UICONTROL Disapproved]</i> (non modifiable) ou <i>[!UICONTROL Paused]</i>. La valeur par défaut pour les nouvelles publicités est [!UICONTROL Active]. Pour supprimer une publicité active ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Target Status] | État d’une cible de recherche dynamique : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, ou <i>[!UICONTROL Deleted]</i> (cibles existantes uniquement). La valeur par défaut pour les nouvelles cibles est [!UICONTROL Active]. Pour supprimer une cible active ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Sitelink Status] | État d’affichage du lien de site : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (liens de site existants uniquement). La valeur par défaut pour les nouveaux liens de site est [!UICONTROL Active]. Pour supprimer un lien de site actif, saisissez la valeur `Deleted`. |
| [!UICONTROL Location Status] | État de la cible de l’emplacement : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (emplacements existants uniquement). La valeur par défaut pour les nouveaux emplacements est [!UICONTROL Active]. Pour supprimer un emplacement actif, saisissez la valeur `Deleted`. |
| [!UICONTROL Product Group Status] | État d’affichage du groupe de produits : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (groupes de produits existants uniquement). La valeur par défaut pour les nouveaux groupes de produits est [!UICONTROL Active]. Pour supprimer un groupe de produits actif, saisissez la valeur `Deleted`. |
| [!UICONTROL Device Target Status] | État de la cible d’appareil au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i>. Pour les nouvelles campagnes et les nouveaux groupes publicitaires, la valeur par défaut est [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | État de la cible RLSA au niveau de la campagne ou du groupe publicitaire ou de l’exclusion (publicités Google uniquement) : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (cibles existantes uniquement). La valeur par défaut des nouvelles cibles ou exclusions est [!UICONTROL Active]. Pour supprimer une cible ou une exclusion active, saisissez la valeur `Deleted`. |
| \[Classification d’étiquette spécifique au annonceur\] | (Nommé pour une classification d’étiquettes spécifique à l’annonceur, telle que &quot;Couleur&quot; pour une classification d’étiquettes appelée Couleur) Une valeur pour la classification spécifiée qui est associée à l’entité. Vous ne pouvez inclure qu’une seule valeur par classification par entité (par exemple, &quot;rouge&quot; pour la classification d’étiquettes &quot;Couleur&quot; pour la campagne A). La longueur maximale est de 100 caractères et la valeur peut inclure des caractères ASCII et non ASCII.<br><br>Les classifications d’étiquettes et leurs valeurs d’étiquettes sont appliquées à tous les composants enfants ; les nouveaux composants ajoutés ultérieurement sont automatiquement associés au libellé. Les classifications d’étiquettes pour les groupes de produits sont appliquées au niveau de l’unité (la plus granulaire).<br><br>Ni le nom de la classification, ni la valeur de la classification ne sont sensibles à la casse. |
| [!UICONTROL Constraints] | Contrainte affectée à l’entité. Vous ne pouvez affecter qu’une seule contrainte par entité.<br><b>>Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire de saisir des valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées. |
| [!UICONTROL Campaign ID] | Identifiant unique qui identifie une campagne existante. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour la campagne. |
| [!UICONTROL Ad Group ID] | Identifiant unique qui identifie un groupe publicitaire existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour le groupe publicitaire. |
| [!UICONTROL Placement ID] | Obsolète |
| [!UICONTROL Keyword ID] | Identifiant unique qui identifie un mot-clé existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le mot-clé, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le mot-clé ou b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>Identifiant unique qui identifie une publicité existante. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Pour les annonces de recherche réactive, l’ID de publicité ou l’AMO ID est requis pour modifier ou supprimer des données de publicité. Pour tous les autres types d’entité, l’AMO ID est requis uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) et &quot;[!UICONTROL AMO ID]&quot;.&quot; Cependant, si vous n’incluez ni la variable [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]et que les colonnes de propriétés de publicité correspondent à plusieurs publicités, l’état de l’une des publicités ne change que.</p><p><b>Remarque :</b> Si vous modifiez a) des colonnes de propriétés de publicité, à l’exception de l’état d’une publicité existante ou b) des données pour une publicité de recherche réactive, et que vous n’incluez ni l’ [!UICONTROL Ad ID] nor [!UICONTROL AMO ID], une nouvelle publicité est alors créée et la publicité existante n’est pas modifiée. </p> |
| [!UICONTROL Sitelink ID] | Identifiant unique qui identifie un lien de site existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez le lien du site, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le lien du site ou b) un &quot;[!UICONTROL AMO ID]&quot;.&quot; Cependant, si vous n’incluez aucun des [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID], et les colonnes de propriétés correspondent à plusieurs liens de site, puis l’état d’un seul lien de site change.</p><p><b>Remarque :</b> Si vous modifiez les colonnes de propriétés sitelink à l’exception de l’état d’un lien de site existant, et que vous n’incluez ni l’ [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID], un nouveau lien de site est alors créé et le lien de site existant n’est pas modifié. |
| [!UICONTROL Product Group ID] | Identifiant unique qui identifie un groupe de produits existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez le groupe de produits, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le groupe de produits ou b) et &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| Identifiant d’emplacement | L’unique [!DNL Microsoft Advertising] identifiant de la cible de l’emplacement. Pour télécharger une liste d’emplacements, connectez-vous au [!DNL Microsoft Advertising] portail destiné aux développeurs utilisant votre [!DNL Microsoft Advertising] informations d’identification du compte publicitaire. Obligatoire uniquement lorsque vous modifiez ou supprimez la cible de l’emplacement, sauf si la ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL Target ID] | Identifiant unique qui identifie une cible automatique existante. Obligatoire uniquement lorsque vous modifiez ou supprimez la cible automatique, sauf si la ligne comprend un[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL RLSA Target ID] | Identifiant unique qui identifie une cible RLSA existante au niveau de la campagne ou du groupe publicitaire. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez la cible ou l’exclusion, sauf si la ligne comprend un[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL AMO ID] | (Dans les feuilles d’envoi groupées générées) Identifiant unique généré par l’Adobe pour une entité synchronisée. Pour les publicités de recherche réactive, l’AMO ID est requis pour modifier ou supprimer les publicités, sauf si vous incluez l’ID de publicité. Pour modifier les données de tous les autres types d’entité avec un AMO ID, celui-ci doit les modifier ou les supprimer, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |
| [!UICONTROL EF Error Message] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans [!UICONTROL EF Errors] fichiers . Cette valeur n’est pas publiée sur le réseau publicitaire. |
| [!UICONTROL SE Error Message] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans [!UICONTROL SE Errors] fichiers . Cette valeur n’est pas publiée sur le réseau publicitaire. |
| [!UICONTROL Exemption Request] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des noms et du texte des stratégies publicitaires Google violées par une publicité. |
| [!UICONTROL Retail Hash] | (Inclus à des fins d’informations dans les feuilles d’envoi groupées générées à l’aide d’Advanced Campaign Management) Code de hachage alphanumérique (par exemple, f9639f40cdf56524b541e5dacf55a991) qui indique que l’élément a été généré à l’aide de la vue avancée (ACM). |

[^1]: [!DNL Excel] convertit les grands nombres en notation scientifique (2.12E+09 pour 2115585666, par exemple) lorsqu’il ouvre le fichier. Pour afficher les chiffres de la notation standard, sélectionnez n’importe quelle cellule de la colonne et cliquez dans la barre de formule.

## Champs requis pour créer, modifier ou supprimer chaque composant de compte {#bulksheet-fields-per-component-microsoft}

Les sections suivantes comprennent les champs relatifs à des entités de compte spécifiques.

>[!NOTE]
>
>Lorsqu’un champ n’est pas applicable à une action, toute valeur saisie dans le champ est ignorée.

### Champs de campagne

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire | Nom unique qui identifie une campagne pour un compte. |
| [!UICONTROL Campaign Budget] | Requis pour créer une campagne. | Une limite de dépenses journalière pour la campagne, avec ou sans symboles monétaires et ponctuation. Cette valeur remplace mais ne peut pas dépasser le budget du compte. |
| [!UICONTROL Channel Type] | Requis pour créer une campagne. |
| [!UICONTROL Delivery Method] | Facultatif |
| [!UICONTROL Campaign Priority] | Requis pour créer une campagne d’achat. |
| [!UICONTROL Merchant ID] | Requis pour créer une campagne d’achat. |
| [!UICONTROL Sales Country] | Requis pour créer une campagne d’achat. |
| [!UICONTROL Product Scope Filter] | (Campagnes commerciales) Facultatif |
| [!UICONTROL DSA Domain Name] | Requis pour créer une campagne de type a) &quot;[!UICONTROL DynamicSearchAds]&quot; ou b) &quot;[!UICONTROL Search]&quot; lorsque la variable [!DNL ExperimentId] n’est pas défini) |
| [!UICONTROL DSA Domain Language] | Requis pour créer une campagne de type a) &quot;[!UICONTROL DynamicSearchAds]&quot; ou b) &quot;[!UICONTROL Search]&quot; lorsque la variable [!DNL ExperimentId] n’est pas défini) |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Landing Page Suffix] | <p>Facultatif |
| [!UICONTROL Budget Type] | Requis pour créer une campagne. |
| [!UICONTROL Device] | Facultatif |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Campaign Status] | Requis uniquement pour supprimer une campagne. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour la campagne. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs d’un groupe publicitaire

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Group Type] | Requis pour créer un groupe publicitaire. |
| [!UICONTROL Audience Target Method] | Requis uniquement pour créer des groupes d’annonces d’audience. |
| [!UICONTROL Ad Group Start Date] | Facultatif |
| [!UICONTROL Ad Group End Date] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Search Network Status] | (Campagnes sur le réseau de recherche uniquement) Facultatif |
| [!UICONTROL Languages] | Facultatif |
| [!UICONTROL Device] | Facultatif |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Ad Group Status] | Requis uniquement pour supprimer un groupe publicitaire. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Ad Group ID] | Obligatoire uniquement lorsque vous modifiez le nom du groupe publicitaire, sauf si la ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour le groupe publicitaire. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de mot-clé

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
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
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Keyword ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le mot-clé, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le mot-clé ou b) et &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs d’annonces de recherche dynamique

>[!NOTE]
>
>La création de la prise en charge n’est pas disponible.

Pour ce type d’annonce, utilisez &quot;[!UICONTROL Creative (except RSA)]&quot; dans la ligne [!UICONTROL Download Bulksheet] boîte de dialogue.

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Obligatoire pour modifier la description. <b>Remarque :</b> Pour ce type d’annonce, la modification de la copie d’annonce supprime la publicité existante et en crée une nouvelle. |
| [!UICONTROL Display Path 1] | Requis pour modifier le champ. |
| [!UICONTROL Display Path 2] | Requis pour modifier le champ. |
| [!UICONTROL Creative Type] | Requis pour créer ou modifier l’état d’une publicité de produit. |
| [!UICONTROL Creative Preferred Devices] | Facultatif |
| [!UICONTROL Ad Status] | Requis pour supprimer une publicité. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) et &quot;[!UICONTROL AMO ID].&quot; Cependant, si vous n’incluez ni la variable [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]et que les colonnes de propriétés de l’annonce correspondent à plusieurs publicités, l’état de l’une des publicités uniquement change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de l’annonce de produit (achats)

Pour plus d’informations sur la création d’annonces de shopping, voir &quot;[Mise en oeuvre [!DNL Microsoft Advertising] campagnes d&#39;achat](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).&quot;

Pour ce type d’annonce, utilisez &quot;[!UICONTROL Creative (except RSA)]&quot; dans la ligne [!UICONTROL Download Bulksheet] boîte de dialogue.

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Promotion Line] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Creative Type] | Requis pour créer ou modifier l’état d’une publicité de produit. |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Ad Status] | Requis pour supprimer une publicité. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) et &quot;[!UICONTROL AMO ID].&quot; Cependant, si vous n’incluez ni la variable [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]et que les colonnes de propriétés de l’annonce correspondent à plusieurs publicités, l’état de l’une des publicités uniquement change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de publicité réactifs (multimédia)

Pour ce type d’annonce, utilisez &quot;[!UICONTROL Creative (except RSA)]&quot; dans la ligne [!UICONTROL Download Bulksheet] boîte de dialogue.

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Pour les annonces réactives, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], et [!UICONTROL Ad Title 3] sont nécessaires pour créer des publicités ; tous les autres champs de titre de publicité sont facultatifs. Pour supprimer la valeur existante pour un champ non obligatoire, utilisez la valeur `[delete]` (y compris les crochets). <b>Remarque :</b> Pour ce type d’annonce, la modification de la copie d’annonce supprime la publicité existante et en crée une nouvelle. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont nécessaires pour créer des publicités ; et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatives. <b>Remarque :</b> Pour ce type d’annonce, la modification de la copie d’annonce supprime la publicité existante et en crée une nouvelle. |
| [!UICONTROL Business Name] | Requis pour créer ou supprimer une publicité. |
| [!UICONTROL Call To Action] | Obligatoire pour créer une publicité. |
| [!UICONTROL Call To Action Language] | Obligatoire pour créer une publicité. |
| [!UICONTROL Base URL/Final URL] | Obligatoire pour créer une publicité. |
| [!UICONTROL Creative Type] | Facultatif. |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Ad Status] | Requis pour supprimer une publicité. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) et &quot;[!UICONTROL AMO ID].&quot; Cependant, si vous n’incluez ni la variable [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]et que les colonnes de propriétés de l’annonce correspondent à plusieurs publicités, l’état de l’une des publicités uniquement change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de publicité de recherche réactive

Pour ce type d’annonce, utilisez &quot;[!UICONTROL Responsive Search Ad]&quot; dans la ligne [!UICONTROL Download Bulksheet] boîte de dialogue.

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Pour les annonces de recherche réactive, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], et [!UICONTROL Ad Title 3] sont nécessaires pour créer une publicité ; tous les autres champs de titre de publicité sont facultatifs. Pour supprimer la valeur existante pour un champ non obligatoire, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Facultatif |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Pour les annonces de recherche réactive, [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont nécessaires pour créer une publicité, et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatives. Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Facultatif |
| [!UICONTROL Display Path 1] | Facultatif |
| [!UICONTROL Display Path 2] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire pour créer une publicité. |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Creative Type] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Ad Status] | Requis pour supprimer une publicité. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire pour modifier ou supprimer des publicités, sauf si la ligne comprend un &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer des publicités, sauf si vous incluez l’identifiant de publicité. |

### Champs de publicité textuelle

Pour ce type d’annonce, utilisez &quot;[!UICONTROL Creative (except RSA)]&quot; dans la ligne [!UICONTROL Download Bulksheet] boîte de dialogue.

>[!NOTE]
>
>Les publicités textuelles étendues étaient obsolètes. Vous pouvez uniquement supprimer des publicités textuelles existantes.

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Lecture seule |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Lecture seule |
| [!UICONTROL Display URL] | Lecture seule |
| [!UICONTROL Display Path 1] | Lecture seule |
| [!UICONTROL Display Path 2] | Lecture seule |
| [!UICONTROL Base URL/Final URL] | Lecture seule |
| [!UICONTROL Custom URL Param] | Lecture seule |
| [!UICONTROL Creative Type] | Facultatif |
| [!UICONTROL Tracking Template] | Lecture seule |
| [!UICONTROL Creative Preferred Devices] | Lecture seule |
| [!UICONTROL Ad Status] | Obligatoire |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend un &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant de publicité.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de cible de recherche dynamique (ciblage automatique)

>[!NOTE]
>
>La création de la prise en charge n’est pas disponible.

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Auto Target Expression] | Obligatoire. |
| [!UICONTROL Match Type] | Facultatif |
| [!UICONTROL Max CPC] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Target Status] | Obligatoire pour supprimer une cible |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible automatique, sauf si la ligne comprend un[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Shopping dans les champs du groupe de produits

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Match Type] | Requis pour créer un groupe de produits. |
| [!UICONTROL Max CPC] | Requis pour créer un groupe de produits. |
| [!UICONTROL Parent Product Groupings] | Obligatoire |
| [!UICONTROL Product Grouping] | Obligatoire |
| [!UICONTROL Partition Type] | Requis pour créer un groupe de produits. |
| [!UICONTROL Base URL/Final URL] | Obligatoire |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Product Group Status] | Requis uniquement pour supprimer un groupe de produits. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Product Group ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le groupe de produits, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le groupe de produits ou b) et &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de lien de site au niveau de la campagne

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| Description Ligne 1 | Facultatif |
| [!UICONTROL Description Line 2] | Facultatif |
| [!UICONTROL Start Date] | Facultatif |
| [!UICONTROL End Date] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Creative Preferred Devices] | Facultatif |
| [!UICONTROL Link Name] | Obligatoire |
| [!UICONTROL Sitelink Status] | Requis uniquement pour supprimer un lien de site. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Sitelink ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le lien du site, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le lien du site ou b) un &quot;[!UICONTROL AMO ID].&quot; Cependant, si vous n’incluez aucun des [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]  et les colonnes de propriétés correspondent à plusieurs liens de site, puis l’état d’un seul lien de site change.<br><br><b>Remarque :</b> Si vous modifiez les colonnes de propriétés sitelink à l’exception de l’état d’un lien de site existant, et que vous n’incluez pas le paramètre [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID], un nouveau lien de site est alors créé et le lien de site existant n’est pas modifié. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs cibles de l’emplacement

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Location] | Obligatoire |
| [!UICONTROL Location Type] | Obligatoire pour créer une cible |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Location Status] | Requis uniquement pour supprimer une cible d’emplacement. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant de campagne.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs cibles des appareils au niveau de la campagne et du groupe publicitaire

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Device] | Requis pour supprimer une cible d’appareil. |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Ad Group Name] | Requis pour les cibles d’appareil au niveau du groupe d’annonces. Non applicable pour les cibles d’appareil au niveau de la campagne. |
| [!UICONTROL Device Target Status] | Requis uniquement pour supprimer une cible d’appareil. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif ; applicable uniquement pour les cibles d’appareil au niveau du groupe d’annonces. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant cible du périphérique.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs cibles RLSA au niveau de la campagne et du groupe publicitaire

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-microsoft).&quot;

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Requis pour les cibles au niveau du groupe d’annonces. Non applicable pour les cibles au niveau de la campagne. |
| [!UICONTROL Audience] | Requis pour créer une cible. |
| [!UICONTROL Target Type] | Facultatif |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL RLSA Target Status] | Requis pour supprimer une cible. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif ; applicable uniquement pour les cibles au niveau du groupe d’annonces. |
| [!UICONTROL RLSA Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible, sauf si la ligne comprend un[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant cible RLSA.<br><br>Search, Social et Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

>[!MORELIKETHIS]
>
>* [Annexe : Erreurs de feuilles d’envoi groupé](../bulksheet-errors.md)
>* [Opérations que vous pouvez effectuer dans des feuilles d’envoi groupées](bulksheet-operations.md)
>* [Formats de fichiers de feuille d’envoi groupé pris en charge](bulksheet-file-formats.md)
>* [Téléchargement/création d’un fichier de feuille d’envoi groupé](../bulksheet-download.md)
>* [Formats de suivi des clics pour [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Télécharger un fichier de feuille d’envoi groupé ou un fichier d’erreur corrigé](../bulksheet-upload.md)
