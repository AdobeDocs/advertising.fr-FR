---
title: Données de feuille d’envoi groupé requises pour les comptes  [!DNL Google Ads]
description: Référencez les champs d’en-tête et de données requis dans les feuilles d’envoi groupées pour les comptes  [!DNL Google Ads] .
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '7855'
ht-degree: 0%

---

# Annexe : Données de feuille d’envoi groupé requises pour les comptes [!DNL Google Ads]

Pour créer et mettre à jour des données de campagne [!DNL Google Ads] en bloc, vous pouvez utiliser des fichiers de feuille d’envoi groupé Search, Social et Commerce formatés spécifiquement pour les comptes [!DNL Google Ads]. Vous pouvez : a) [générer des fichiers de feuille pour les comptes existants](../bulksheet-download.md) au format de fichier requis ou b) les créer manuellement (voir &quot;[Formats de fichier de feuille d’envoi groupé pris en charge](bulksheet-file-formats.md)&quot; pour obtenir des informations générales sur les formats de fichier pris en charge).

Chaque feuille d’envoi groupé doit inclure les champs d’en-tête et les champs de données correspondants requis pour les [ opérations spécifiques que vous souhaitez effectuer ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (création d’une publicité, par exemple). Lorsqu’un champ n’est pas obligatoire, vous pouvez l’omettre dans les lignes d’en-tête et de données. Toutes les colonnes personnalisées sont supprimées lorsque vous chargez le fichier de feuille en bloc.

Vous trouverez ci-dessous un tableau de tous les champs de données disponibles et des tableaux supplémentaires indiquant les champs obligatoires pour ajouter, modifier ou supprimer des données pour des entités individuelles (telles que des campagnes et des mots-clés).

## Tous les champs de données disponibles {#bulksheet-fields-all-google}

Le tableau suivant décrit tous les champs de données disponibles.

Pour les champs de données pertinents pour les entités de compte, voir &quot;[Champs requis pour créer, modifier ou supprimer chaque composant de compte](#bulksheet-fields-per-component-google)&quot;.

>[!NOTE]
>
>* Les valeurs de toutes les colonnes de texte sont sensibles à la casse.
>* Lorsque vous créez un nouvel enregistrement sans inclure de valeurs pour tous les champs de données requis, les valeurs par défaut spécifiées sont alors attribuées à certains de ces champs.
>* Pour les champs qui ne sont pas spécifiés ci-dessous, la valeur par défaut du réseau publicitaire est utilisée.
>* Pour obtenir la liste des lignes de feuille d’envoi groupé disponibles dans la boîte de dialogue [!UICONTROL Download Bulksheet], voir &quot;[Lignes de feuille d’envoi groupé par réseau publicitaire](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network)&quot;.

| Champ | Description |
| ---- | ---- |
| [!UICONTROL Platform] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) La plateforme publicitaire. Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Acct Name] | Nom unique qui identifie un compte réseau publicitaire. Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Nom unique qui identifie une campagne pour un compte. |
| [!UICONTROL Campaign Budget] | Une limite de dépenses journalière pour la campagne, avec ou sans symboles monétaires et ponctuation. Cette valeur remplace mais ne peut pas dépasser le budget du compte. |
| [!UICONTROL Delivery Method] | <p>La vitesse d’affichage des publicités pour la campagne, chaque jour :</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (valeur par défaut pour les nouvelles campagnes) : pour diffuser vos impressions publicitaires tout au long de la journée.</p></li><li><p><i>[!UICONTROL Accelerated] :</i> (obsolète en octobre 2019) Pour afficher vos publicités aussi souvent que possible jusqu’à ce que votre budget soit atteint. Par conséquent, vos publicités peuvent ne pas apparaître plus tard dans la journée.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>Canaux sur lesquels placer des publicités. Spécifiez une ou plusieurs options :</p><ul><li><p><i>[!UICONTROL Search]</i> (valeur par défaut pour les nouvelles campagnes) : pour placer des publicités sur le réseau de recherche [!DNL Google Ads] (y compris [!DNL Google Ads] sites Web de partenaires de recherche et de recherche) et éventuellement sur le réseau d’affichage [!DNL Google Ads]. <b>Remarque :</b> Les campagnes qui ciblent à la fois le réseau de recherche et le réseau d’affichage ne peuvent pas être ajoutées à un portefeuille pour l’optimisation des offres.</p></li><li><p><i>[!UICONTROL Display]</i> : pour placer des publicités uniquement sur le réseau d’affichage [!DNL Google Ads].</p></li><li><p><i>[!UICONTROL Shopping]</i> : pour placer des publicités commerciales sur le réseau commercial [!DNL Google Ads] (dans certains pays) et le réseau de recherche [!DNL Google Ads] (y compris les [!DNL Google Ads] sites Web de partenaires de recherche et de recherche). Pour créer des publicités commerciales, vous devez disposer de produits dans un compte [!DNL Google Merchant Center] et [autoriser Search, Social et Commerce à télécharger les données du compte](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Pour plus d’informations sur le processus de création de publicités commerciales, voir &quot;[Mise en oeuvre [!DNL Google Ads] campagnes d’achat](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot;.</p></li></ul> |
| [!UICONTROL Networks] | <p>Où placer des publicités. Spécifiez une ou plusieurs options :</p><ul><li><p><i>[!UICONTROL Google Search]</i> : listes de recherche sponsorisée sur le réseau de recherche Google uniquement.</p></li><li><p><i>[!UICONTROL Search Partners]</i> : Listes de recherche sponsorisées sur Google des partenaires de recherche.</p></li><li><p><i>[!UICONTROL Content]</i> : pour placer des offres pour les listes réseau d’affichage.</p></li><li><p><i>[!UICONTROL All]</i> (valeur par défaut pour les nouvelles campagnes) : cible la recherche Google, les partenaires de recherche et le contenu.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Réseau de recherche uniquement ; applicable aux annonces de recherche dynamique étendues uniquement) Domaine racine (tel que example.com) ou sous-domaine (tel que shoes.example.com) du site web dont le contenu est utilisé par le réseau publicitaire pour cibler vos annonces de recherche dynamique.<br><br><b>Notes :</b></p><ul><li><p>Les annonces de recherche dynamique étendues ciblent le contenu du site web plutôt que les mots-clés.</p></li><li><p>Votre domaine doit être indexé par l’index de recherche organique du réseau publicitaire pour être ciblé.</p></li><li><p>Si vous ne spécifiez pas de domaine, vous devez créer des cibles de recherche dynamique, qui ciblent toutes les pages de votre site web ou un sous-ensemble d’entre elles, pour chaque groupe publicitaire.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Réseau de recherche uniquement ; applicable aux annonces de recherche dynamique étendue uniquement) Langue du domaine de site web spécifié. <b>Remarque :</b> Si le domaine contient des pages dans plusieurs langues et que vous souhaitez tous les cibler, créez une campagne distincte pour chaque langue. |
| [!UICONTROL GDN Custom Bid Level] | (Campagnes ciblant le réseau d’affichage uniquement) Comment enchérir : par <i>[!UICONTROL Ad Group]</i> (valeur par défaut), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (site web) ou <i>[!UICONTROL None]</i> (pour réinitialiser la valeur existante). D’autres dimensions (<i>Age</i>, <i>Genre</i>, <i>Intérêt et Liste</i>, <i>Sujet</i> et <i>Vertical</i>) sont disponibles à partir de l’interface [!DNL Google Ads]. Si vous avez utilisé l’interface [!DNL Google Ads] pour configurer l’offre selon une autre dimension, cette valeur s’affiche, mais vous ne pouvez pas sélectionner ni saisir ces dimensions ici.</p><p><b>Remarque :</b></p><ul><li><p>Lorsque vous enchérissez par mot-clé, créez des modèles de suivi au niveau du mot-clé. De même, lorsque vous enchérissez par emplacement, créez des modèles de suivi au niveau de l’emplacement. Pour toutes les autres dimensions, créez des modèles de suivi au niveau de l’annonce.</p></li><li><p>Lorsque vous enchérissez selon une dimension non prise en charge (Age, Genre, Intérêt et Liste ou Rubrique), Search, Social et Commerce n’optimise pas les offres pour la dimension et toutes les attributions sont appliquées au groupe publicitaire.</p></li><li><p>Les publicités sur le réseau de recherche utilisent toujours des offres sur les mots-clés.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Campagnes d’achat uniquement) La priorité avec laquelle la campagne est utilisée lorsque plusieurs campagnes font la publicité du même produit : <i>[!UICONTROL Low]</i> (valeur par défaut pour les nouvelles campagnes), <i>[!UICONTROL Medium]</i> ou <i>[!UICONTROL High]</i>.</p><p>Lorsqu’un même produit est inclus dans plusieurs campagnes, le réseau publicitaire utilise d’abord la priorité de la campagne pour déterminer la campagne (et l’offre associée) éligible aux enchères publicitaires. Lorsque toutes les campagnes ont la même priorité, la campagne avec l&#39;offre la plus élevée est éligible. |
| [!UICONTROL Merchant ID] | (Campagnes d’achat et campagnes d’audience liées à un flux marchand uniquement) Identifiant client du compte marchand dont les produits sont utilisés pour la campagne. |  |
| [!UICONTROL Sales Country] | (Campagnes d’achat uniquement ; lecture seule pour les campagnes existantes) Pays dans lequel les produits de la campagne sont vendus. Les produits étant associés aux pays cibles, ce paramètre détermine les produits faisant l’objet d’une publicité dans la campagne. |
| [!UICONTROL Product Scope Filter] | (Campagnes utilisant uniquement le réseau d’achat [!DNL Google Ads]) Les produits de votre compte [!DNL Google Merchant Center] pour lesquels des publicités commerciales peuvent être créées pour la campagne. Vous pouvez saisir jusqu’à sept combinaisons de dimensions et d’attributs de produit sur lesquelles filtrer vos produits, en utilisant le format dimension=attribut . Séparez plusieurs filtres par un délimiteur &quot;>&quot;. Pour obtenir la liste des dimensions de produit disponibles, voir &quot;[Shopping campaign product filters](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)&quot;.</p><p>Exemple : &quot;CategoryL1=animal&quot;CategoryL2=animal de compagnie&quot;Marque=Acme animal Fourniture&quot;</p><p>Pour supprimer les valeurs existantes, utilisez la valeur <code>[delete]</code> (y compris les crochets).</p> |
| [!UICONTROL Languages] | <p>(Recherche et affichage des réseaux uniquement) Les langues cibles des publicités dans la campagne.</p><p>Si vous ne saisissez pas de valeur pour ce champ ou le champ [!UICONTROL Geo Targeting] pour une nouvelle campagne, la devise spécifiée pour le compte détermine les langues par défaut, sauf que les campagnes avec des devises qui ne sont pas mappées à des langues spécifiques (par exemple, EUR) sont ciblées sur toutes les langues. Si vous ne saisissez pas de valeur pour ce champ, mais que vous saisissez une valeur dans le champ [!UICONTROL Geo Targeting] pour une nouvelle campagne, la valeur par défaut est <i>[!UICONTROL All]</i>. Si vous laissez ce champ vide pour une campagne existante, la valeur existante est conservée.</p><p>Pour cibler toutes les langues, saisissez <span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span>. Pour cibler des langues spécifiques, saisissez des valeurs séparées par des points-virgules à l’aide des <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] noms de langue</a> (par exemple <i>Anglais;Japonais</i>, qui sont remplacés par les codes numériques corrects) ou des codes numériques (par exemple <i>1000;1005</i>). Les valeurs ne respectent pas la casse.</p> |
| [!UICONTROL Location] | Emplacement géographique où placer des publicités, ou pour lesquelles exclure des publicités, pour la campagne. Si vous ne saisissez aucune valeur pour ce champ ou le champ Langues d’une nouvelle campagne, la devise spécifiée pour le compte détermine les emplacements par défaut, sauf que les campagnes avec des devises qui ne sont pas mappées à des emplacements spécifiques (par exemple, EUR) sont ciblées sur tous les emplacements. Si vous ne saisissez pas de valeur pour ce champ, mais que vous saisissez une valeur dans le champ [!UICONTROL Languages] pour une nouvelle campagne, la valeur par défaut est <i>[!UICONTROL All]</i>. Si vous laissez ce champ vide pour une campagne existante, la valeur existante est conservée.</p><p>Pour cibler un emplacement spécifique, utilisez l’un des [[!DNL Google Ads] noms d’emplacement](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (qui sont remplacés par le code numérique approprié) ou des codes d’emplacement :</p><ul><li><p>Pays/territoires : Entrez les noms des pays/territoires (par exemple, <i>États-Unis;Japon</i>) ou les codes numériques (par exemple, <i>2840;2392</i>).</p></li><li><p>Etats/provinces/régions : saisissez les noms des états/provinces/régions avec les abréviations de pays/territoires associés (par exemple <i>Tokyo, JP;New York, US</i>) ou les codes numériques (par exemple <i>20636;21167</i>).</p></li><li><p>Villes hors États-Unis : entrez le nom de la ville, le nom de l’état/de la province/région et les abréviations du pays/territoire (par exemple, <i>Adachi, Tokyo, JP;Kita, Tokyo, JP</i>) ou les codes numériques (par exemple, <i>1028850;1009293</i>)</p></li><li><p>Zone métropolitaine américaine : entrez les noms des villes, les noms des états et les abréviations des pays (par exemple, <i>Buffalo NY, US;New York NY, US</i>) ou les codes numériques (tels que <i>514;501</i>).</p></li></ul><p>Pour exclure un emplacement, faites précéder le nom ou le code de l’emplacement d’un signe moins (`-`), tel que <i>-Japan</i>.</p><p><b>Remarque :</b> Les valeurs ne sont pas sensibles à la casse.</p> |
| [!UICONTROL Location Type] | (Lorsque vous incluez un emplacement) [type d’emplacement](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Type d’appareil pour lequel des ajustements d’offre sont effectués au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> ou <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(Lorsque vous incluez une cible [!UICONTROL Location], [!UICONTROL Device] ou [!UICONTROL RLSA]) Si vous souhaitez ajuster les offres pour les publicités à un emplacement spécifique, sur un type d’appareil spécifique ou avec une cible d’audience spécifique :</p><ul><li><p>Pour utiliser l’offre au niveau du mot-clé (0 % de différence), saisissez 0. Pour les nouvelles cibles, vous pouvez également laisser ce champ vide.</p></li><li><p>Pour utiliser une autre offre pour cette cible, saisissez le pourcentage d’augmentation ou de diminution des offres.</p></li><ul><li><p>Pour les cibles d’emplacement et de RLSA, les pourcentages valides sont compris entre -90 et 900.</p></li><li><p>Pour les ajustements d’offres des périphériques, les pourcentages valides sont les suivants :</p></li><ul><li><p>(Campagnes)-100 (pour ne pas enchérir pour les publicités du type d’appareil) ou de -90 à 900.</p></li><li><p>(Groupes publicitaires) -100 pour smartphones et tablettes (pour ne pas enchérir pour le type d’appareil) et de -90 à 900 pour tous les types d’appareils.</p></li></ul></ul><li><p>(Campagnes et groupes d’annonces existants) Pour utiliser l’ajustement d’offre existant, laissez ce champ vide.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Ajustement d’offre en lecture seule recommandé par Adobe pour la cible d’emplacement au niveau de la campagne ou une RLSA. Elle est calculée uniquement lorsque la campagne fait partie d’un portefeuille dont l’objectif est d’utiliser des mesures de conversion pondérées (et non l’objectif [!UICONTROL Maximize Clicks]) et que la campagne contient au moins deux cibles de localisation ou des RLSA avec au moins cinq clics ou 5 USD de coût au cours des 90 derniers jours.</p><p>Si vous souhaitez modifier manuellement une cible d’emplacement ou une RLSA pour utiliser la valeur recommandée, patientez au moins deux semaines après avoir créé la cible d’emplacement ou la RLSA pour permettre une collecte de données suffisante, et ne modifiez pas la valeur plus d’une fois par semaine. |
| [!UICONTROL Device Targets] | <p>(Types de campagne hérités uniquement) Appareils sur lesquels la publicité peut être affichée : <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> ou <i>[!UICONTROL Tablets]</i>. Pour les nouvelles campagnes, la valeur par défaut est <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Types de campagne hérités uniquement ; applicables lorsque les cibles de périphérique incluent &quot;Smartphones&quot; ou &quot;tablettes&quot;) Les systèmes d’exploitation sur lesquels la publicité peut être affichée : <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> ou <i>[!UICONTROL Palm]</i>. Pour les nouvelles campagnes, la valeur par défaut est <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Types de campagne hérités uniquement ; applicable lorsque [!UICONTROL Device Targets] comprend &quot;[!UICONTROL All]&quot; ou &quot;[!UICONTROL Smartphones]&quot;) Opérateurs de téléphonie mobile auxquels les smartphones peuvent être connectés : <i>[!UICONTROL All]</i>, ou un ou plusieurs opérateurs indiqués par &lt;c<i>carrier code</i>>,&lt;<i>country code</i>> (T-Mobile,US, par exemple) à l’aide de la liste <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">opérateurs et codes disponibles pour [!DNL Google Ads]</a>. Séparez plusieurs opérateurs par des points-virgules (tels que T-Mobile, US, T-Mobile, GB). Pour les nouvelles campagnes, la valeur par défaut est <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>Nom unique qui identifie un groupe publicitaire. La longueur maximale est de 255 caractères ; les caractères vides à la fin ne sont pas enregistrés (par exemple, &quot;Groupe d’annonces 1&quot; est enregistré comme &quot;Groupe d’annonces 1&quot;). Ce champ ne s’applique pas aux liens de site au niveau de la campagne ou aux cibles d’appareil au niveau de la campagne.</p> |
| [!UICONTROL Ad Group Type] | <p>Type de groupe d’annonces : <i>[!UICONTROL Discovery]</i> (pour les campagnes de découverte uniquement), <i>[!UICONTROL Display]</i> (pour les campagnes d’affichage), <i>[!UICONTROL Search Dynamic]</i> (pour les publicités de recherche dynamique étendues), <i>[!UICONTROL Search Standard]</i> (pour les publicités de recherche), <i>[!UICONTROL Shopping Product]</i> (pour les publicités de produits d’achat), <i>[!UICONTROL Shopping Showcase]</i> (création et modification non prise en charge) ou <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Campagnes CPC uniquement) Coût par clic maximum, qui est le montant le plus élevé à payer pour un clic publicitaire sur le réseau publicitaire, avec ou sans symboles monétaires et ponctuation. Vous pouvez définir des valeurs pour les groupes publicitaires et les mots-clés, les groupes de produits et les cibles de recherche dynamique. La valeur par défaut d’un nouveau mot-clé est héritée du niveau du groupe d’annonces. Pour les groupes de produits, vous pouvez définir des valeurs pour le niveau de groupe de produits le plus bas ; la valeur par défaut d’un nouveau niveau est héritée du niveau parent.</p><p>Pour les groupes de produits existants et les cibles de recherche dynamique dans les portefeuilles optimisés, les mises à jour ne sont effectives que pendant une journée et sont remplacées au cours du cycle d’optimisation suivant.</p> |
| [!UICONTROL Max Content CPC] | <p>(Campagnes CPC uniquement) Coût maximum du contenu par clic (CPC), qui est le montant le plus élevé à payer pour un clic publicitaire sur un site de réseau d’affichage, avec ou sans symboles monétaires et ponctuation. Vous pouvez définir et modifier des valeurs au niveau du groupe d’annonces dans les campagnes qui ne sont pas ciblées par les emplacements.</p> |
| [!UICONTROL Audience Target Method] | <p>(Campagnes uniquement sur le réseau de recherche et campagnes [!DNL Gmail] existantes en lecture seule sur le réseau d’affichage) Indique si :</p><ul><li><p><i>[!UICONTROL Target and Bid]</i> : pour afficher uniquement les publicités aux utilisateurs associés aux audiences cibles qui correspondent également à d’autres cibles pour le groupe publicitaire.</p></li><li><p><i>[!UICONTROL Bid Only]</i> : pour afficher les publicités même aux personnes qui ne sont pas associées aux audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire.</p><p>Vous pouvez toutefois augmenter les chances d&#39;affichage des publicités à des audiences spécifiques en définissant des offres plus élevées pour ces audiences.</p></li></ul> |
| [!UICONTROL Keyword] | Chaîne du mot-clé. La longueur maximale est de 80 caractères et pas plus de 10 mots. Elle ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : espace `# $ & _ - " [ ] ' + . / :`</p><p><b>Remarque :</b></p><ul><li><p>Pour exclure un mot-clé au niveau du groupe publicitaire ou de la campagne, définissez [!UICONTROL Match Type] sur <i>[!UICONTROL Negative]</i>. Si la ligne comprend le nom du groupe publicitaire, le mot-clé est exclu du groupe publicitaire. Si la ligne ne contient pas le nom du groupe publicitaire, le mot-clé est exclu pour l’ensemble de la campagne.</p></li><li><p>La modification d’un mot-clé ou d’un type de correspondance [!DNL Google Ads] supprime le mot-clé existant et en crée un nouveau.</p></li></ul> |
| [!UICONTROL Placement] | (Campagnes utilisant la correspondance de contenu uniquement) Un emplacement sur le réseau d’affichage sur lequel vos publicités peuvent être affichées. Spécifiez l’une des options suivantes :</p><ul><li><p>Site Web : saisissez une URL valide. Il peut s’agir d’un domaine de niveau supérieur, d’un sous-domaine de premier niveau ou d’un domaine avec un seul nom de répertoire. L’URL ne peut pas inclure de point d’interrogation (?). Exemples :<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>Position de la publicité sur une page spécifique : utilisez le format `<URL> >> <location,sublocation>` (tel que `finance.google.com >> Company pages,Top right`).</p></li><li><p>Une catégorie de rubrique : utilisez la syntaxe `<category::<category> > <subcategory>`, etc. (par exemple `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Remarque : </b> Pour exclure un emplacement au niveau du groupe publicitaire ou de la campagne, définissez [!UICONTROL Match Type] sur <i>[!UICONTROL Negative]</i>. Si la ligne comprend le nom du groupe publicitaire, l’emplacement est exclu du groupe publicitaire. Si la ligne ne contient pas le nom du groupe publicitaire, l’emplacement est exclu pour l’ensemble de la campagne.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Obligatoire lorsque le paramètre de campagne &quot;[!UICONTROL Use my website contents to target my ads]&quot; n’est pas activé ; facultatif dans le cas contraire) Cibles de recherche dynamique pour le groupe publicitaire.</p><p>Pour toutes les cibles, utilisez un astérisque (*).</p><p>Pour cibler jusqu’à trois critères de recherche dynamique, utilisez le format `<category>=<target>`, où `<category>` peut inclure n’importe quelle catégorie ci-dessous. Rejoindre plusieurs cibles pour une catégorie individuelle avec &quot;\[espace vide\] et \[espace vide\]&quot; et rejoindre plusieurs catégories avec &quot;[espace vide] et [ espace vide]&quot;.</p><ul><li><p><i>[!UICONTROL Category]</i> : pour afficher des annonces de recherche dynamique étendues pour des pages indexées avec une catégorie de contenu [!DNL Google Ads] spécifique.</p></li><li><p><i>[!UICONTROL URL]</i> : pour afficher des annonces de recherche dynamique étendues pour des pages indexées avec une URL spécifique, où la valeur peut être incluse n’importe où dans l’URL.</p></li><li><p><i>[!UICONTROL Page Title]</i> : pour afficher des annonces de recherche dynamique étendues pour des pages indexées avec du texte spécifique dans le titre de la page.</p></li><li><p><i>[!UICONTROL Page Content]</i> : pour afficher des annonces de recherche dynamique étendues pour des pages indexées avec du contenu spécifique.</p></li></ul><p>Exemple : url=shoes.example.com et page title=chaussures</p> |
| [!UICONTROL Parent Product Groupings] | Hiérarchie de tous les groupes de produits parents.<br><br>Exemple : `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>Groupe de produits (par exemple &quot;marque=acme&quot; ou &quot;Tous les produits&quot;).</p><p><b>Remarque :</b></p><ul><li><p>Lorsqu’un groupe de produits spécifié n’existe pas dans la hiérarchie [!UICONTROL Parent Product Groupings], Search, Social et Commerce crée les parties de la hiérarchie qui sont nécessaires.</p></li><li><p>Search, Social et Commerce crée automatiquement un groupe &quot;[!UICONTROL All Products]&quot; lorsque vous créez un groupe publicitaire dans une campagne d’achat [!DNL Google Ads] avec une offre par défaut définie sur l’offre par défaut du groupe publicitaire. Search, Social et Commerce crée automatiquement un groupe &quot;[!UICONTROL Everything Else]&quot; avec l’offre par défaut du groupe publicitaire à chaque niveau de la hiérarchie du groupe de produits. Vous pouvez toujours créer explicitement ces groupes et les exclure ou modifier leurs offres.</p></li><li><p>Chaque groupe d’annonces peut inclure jusqu’à huit niveaux de groupes de produits, dont &quot;[!UICONTROL All Products]&quot; et sept autres niveaux.</p></li></ul> |
| [!UICONTROL Partition Type] | Type de partition pour le groupe de produits : <i>subdivisions</i> (lorsqu’il a des groupes de produits enfants) ou <i>unité</i> (lorsqu’il n’a aucun groupe de produits enfant). |
| [!UICONTROL Match Type] | <p>Pour la cible de recherche dynamique ou les groupes de produits : l’option de correspondance des mots-clés pour la cible de recherche dynamique ou le groupe de produits : <i>[!UICONTROL Dynamic Ad Target]</i> (valeur par défaut pour les nouvelles cibles de recherche dynamique), <i>[!UICONTROL Product Group]</i> (valeur par défaut pour les nouveaux groupes de produits) ou <i>[!UICONTROL Negative Product Group]</i> (pour exclure un groupe de produits).</p><p>Pour les mots-clés : option de correspondance des mots-clés pour le mot-clé : <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> ou <i>[!UICONTROL Negative]</i> (pour exclure un mot-clé ou un emplacement sur le réseau d’affichage) ; les groupes de produits utilisés avec les publicités commerciales ont un type de correspondance <i>[!UICONTROL Product Group]</i>. Si vous utilisez <i>[!UICONTROL Negative]</i>, vous devez également inclure le type de correspondance à exclure (par exemple, &quot;Expression négative&quot;).</p><p>Pour les nouveaux mots-clés, la valeur par défaut est <i>[!UICONTROL Broad]</i>. Une valeur pour le type de correspondance ou l’ID de mot-clé est nécessaire uniquement pour modifier un mot-clé avec plusieurs types de correspondance.</p><p><b>Remarque :</b></p><ul><li><p>Les types de correspondance ne s’appliquent pas aux annonces de recherche dynamique étendues qui n’utilisent pas de mots-clés.</p></li><li><p>La modification du type de correspondance pour un mot-clé [!DNL Google Ads] supprime le mot-clé existant et en crée un nouveau.</p></li><li><p>Pour le modificateur de correspondance large, sélectionnez &quot;Large&quot; et insérez un + avant tout mot du mot-clé pour lequel des variantes de fermeture sont requises (par exemple &quot;+red+chaussures&quot; pour exiger des variantes de &quot;rouge&quot; et &quot;chaussures&quot; de fermeture). <b>Remarque : </b> Les modificateurs de correspondance large ont désormais le même comportement de correspondance que les correspondances d’expression pour certaines langues et vous n’avez pas pu créer de mots-clés de modification de correspondance large depuis juillet 2021. Pour plus d’informations, voir [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/7042511) .</p> |
| [!UICONTROL First Page Bid] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Offre requise pour placer une publicité sur la première page des résultats de recherche. Cette valeur n’est pas publiée sur le réseau publicitaire. |
| [!UICONTROL Quality Score] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Score de qualité actuel attribué au mot-clé par le moteur de recherche. Cette valeur n’est pas publiée sur le réseau publicitaire.) |
| [!UICONTROL Creative Preferred Devices] | (Publicités texte, annonces de recherche dynamique étendues et liens de site améliorés ; facultatif) Types d’appareils sur lesquels vous préférez afficher la publicité : <i>[!UICONTROL All]</i> (valeur par défaut) ou <i>[!UICONTROL Mobile]</i>. Lorsque <i>[!UICONTROL Mobile]</i> est spécifié, le réseau tente d’afficher la publicité pour les utilisateurs d’appareils mobiles plutôt que pour les utilisateurs d’ordinateurs de bureau ou de tablettes. Sinon, le réseau affiche la publicité sur n’importe quel type d’appareil.</p><p><b>Remarque :</b></p><ul><li><p>Seuls les utilisateurs administrateur et gestionnaire de compte [!DNL Adobe] peuvent modifier ce paramètre.</p></li><li><p>Le réseau ne garantit pas qu’il affichera la publicité sur le type d’appareil préféré.</p></li><li><p>Les nouveaux liens de site améliorés ne peuvent être créés que dans les campagnes avec des liens de site améliorés existants ou sans lien de site.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Publicités textuelles étendues et annonces de recherche réactive uniquement) Les titres d’une publicité, chacun séparé par une barre verticale (&amp;vert;). Pour chaque champ de titre de publicité, la longueur maximale est de 30 caractères ou 15 caractères codés sur deux octets, y compris tout texte dynamique (comme les valeurs des mots-clés et des personnalisateurs de publicités).</p><p>Pour les annonces responsives sur le Réseau de Recherche, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] et [!UICONTROL Ad Title 3] sont obligatoires, et tous les autres champs de Titre de la Publicité sont facultatifs. Pour supprimer la valeur existante pour un champ non obligatoire, utilisez la valeur <code>[delete]</code> (y compris les crochets).</p><p>Pour les annonces de recherche réactive, insérez un personnaliseur de publicité au format suivant : <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, par exemple <code>{CUSTOMIZER.Discount:10%}</code></p><p>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer des publicités textuelles étendues, qui [!DNL Google Ads] sont devenues obsolètes en juin 2022. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Publicités de recherche réactive uniquement ; facultatif) Position à laquelle épingler le titre de publicité correspondant : `[null]` (aucune valeur, qui rend le titre de publicité éligible pour toutes les positions), <i>1</i>, <i>2</i> ou <i>3</i>. Par exemple, si [!UICONTROL Ad Title Position] a une valeur de 1, alors le Titre de la publicité apparaît uniquement dans la Position 1. Par défaut, tous les titres de publicité sont nuls (ne comportent aucune valeur).</p><p>Pour supprimer la valeur existante, utilisez la valeur <code>[delete]</code> (y compris les crochets).</p><p><b>Remarque : </b> Vous pouvez épingler plusieurs titres de publicité à la même position. Le réseau publicitaire utilise l’un des titres de publicité épinglés à la position. Il se peut que les titres épinglés à la position 3 ne s’affichent pas avec la publicité.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Publicités de recherche dynamique étendues, annonces textuelles étendues et annonces de recherche réactive uniquement) Corps d’une publicité. Pour chaque champ de description, la longueur maximale est de 90 caractères ou 45 caractères codés sur deux octets, y compris tout texte dynamique (comme les valeurs des mots-clés et des personnalisateurs de publicités).</p><p>Pour les annonces responsives sur le Réseau de Recherche, insérez un personnalisateur de Publicités au format suivant : `{CUSTOMIZER.AdCustomizerName:DefaultText}`, par exemple `{CUSTOMIZER.Discount:10%}`</p><p>Pour les annonces de recherche dynamique étendues, utilisez uniquement [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2]. <b>Remarque : </b> Pour ce type de publicité, la modification de la copie de publicité supprime la publicité existante et en crée une nouvelle.</p><p>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer des publicités textuelles étendues, qui [!DNL Google Ads] sont devenues obsolètes en juin 2022.</p><p>Pour les annonces responsives sur le Réseau de Recherche, [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont requis, et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatifs. Pour supprimer la valeur existante, utilisez la valeur <code>[delete]</code> (y compris les crochets).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Publicités de recherche réactive uniquement ; facultatif) Position à laquelle épingler la description correspondante : `[null]` (aucune valeur, qui rend la description éligible pour toutes les positions), <i>1</i>, <i>2</i> ou <i>3</i>. Par exemple, si [!UICONTROL Description 1 Position] a une valeur de 1, alors [!UICONTROL Description 1] apparaît uniquement dans la position 1. Par défaut, aucune description n’est épinglée à une position.</p><p>Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets).</p><p><b>Remarque : </b> Vous pouvez épingler plusieurs descriptions à la même position. Le réseau publicitaire utilise l’une des descriptions épinglées à la position. Il se peut que les descriptions épinglées à la position 2 ne s’affichent pas avec la publicité. |
| [!UICONTROL Display URL] | URL incluse dans la publicité.<br><br>Pour les annonces de recherche dynamique étendues, [!DNL Google Ads] génère dynamiquement cette valeur à partir du domaine du site web et vous n’avez pas besoin de saisir de valeur.<br><br> Pour les annonces responsives sur le Réseau de Recherche, il n&#39;est pas nécessaire de saisir une valeur. L’URL d’affichage est automatiquement extraite du domaine dans l’URL finale. Vous pouvez éventuellement personnaliser l’URL à l’aide des champs Chemin 1 et Chemin 2 .<br><br>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer des publicités textuelles étendues, qui [!DNL Google Ads] sont devenues obsolètes en juin 2022.<br><br><b>Remarque :</b> (Comptes avec URL finales) Les noms de domaine dans l’URL d’affichage et l’URL finale doivent correspondre.</p> |
| [!UICONTROL Display Path 1] | <p>(Publicités textuelles étendues<span> et annonces responsives </span> uniquement)</p><p>(Facultatif) Texte ajouté à l’URL d’affichage automatiquement extraite de l’URL finale. Il est précédé dans l’URL d’une barre oblique (/). Un chemin ne peut pas contenir de barre oblique (/) ou de caractères de saut de page (\n). La longueur maximale est de 15 caractères ou 7 caractères sur deux octets.</p><p>Pour insérer un personnalisateur de publicités, utilisez les formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide :&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`</p><p>Par exemple, si [!UICONTROL Display Path 1] est &quot;offres&quot;, l’URL d’affichage est &lt;<i>URL d’affichage</i>>/offres, telles que www.example.com/deals.</p><p>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer des publicités textuelles étendues, qui [!DNL Google Ads] sont devenues obsolètes en juin 2022.</p> |
| [!UICONTROL Display Path 2] | Un deuxième chemin d’affichage ; voir l’entrée pour [!UICONTROL Display Path 1].<br><br>Exemple : si [!UICONTROL Display Path 1] est &quot;offres&quot; et [!UICONTROL Display Path 2] est &quot;local&quot;, alors l’URL d’affichage est &lt;<i>URL d’affichage</i>>/offres/local, comme www.example.com/deals/local.</p><p>Vous ne pouvez pas créer ni modifier, mais vous pouvez supprimer des publicités textuelles étendues, qui [!DNL Google Ads] sont devenues obsolètes en juin 2022.</p> |
| [!UICONTROL Promotion Line] | (Listes de produits uniquement) Une ligne de promotion facultative à inclure à la liste de produits dans les résultats de recherche. La longueur maximale est de 45 caractères.</p><p>La ligne de promotion peut apparaître à différents emplacements par rapport à la publicité (par exemple sous la publicité), selon l’emplacement de la publicité sur la page. |
| [!UICONTROL Link Name] | <p>Le texte du lien de site. Elle peut contenir jusqu’à 25 caractères.</p><p>Pour les nouveaux liens de site, vous devez inclure le nom de la campagne dans la ligne lien de site. Pour les liens de site au niveau du groupe d’annonces, vous devez également inclure le nom du groupe d’annonces.</p><p><b>Remarque :</b> Le texte existant de 35 caractères est toujours affiché dans les publicités sur les ordinateurs de bureau et les tablettes, mais pas sur les appareils mobiles.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Publicités d’installation d’application existantes uniquement) Système d’exploitation sur lequel s’exécute l’application mobile : <i>Android™</i> ou <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Publicités d’installation d’applications existantes uniquement) <p>ID de l’application ou nom du package. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Publicités d’installation d’application existantes uniquement) Nom de l’application. |
| [!UICONTROL Start Date] | <p>(Liens de site améliorés uniquement) Date à laquelle les offres peuvent être placées pour le lien de site, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants : <i>m/d/yyy</i>, <i>m/d/yy</i>, <i>m-d-yyy</i> ou <i>m-d-yy</i>}. La valeur par défaut des nouveaux liens de site améliorés est la journée actuelle.</p><p><b>Remarque :</b> De nouveaux liens de site améliorés ne peuvent être créés que dans les campagnes avec des liens de site améliorés existants ou sans lien de site.</p> |
| [!UICONTROL End Date] | <p>(Liens de site améliorés uniquement) Date à laquelle les offres peuvent être placées pour le lien de site, dans le fuseau horaire de l’annonceur et dans l’un des formats suivants :  <i>m/d/yyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i> ou <i>m-d-yy</i>. La valeur par défaut est none (pas de date de fin).</p><p><b>Remarque :</b> De nouveaux liens de site améliorés ne peuvent être créés que dans les campagnes avec des liens de site améliorés existants ou sans lien de site.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Publicités d’installation d’applications existantes uniquement)</p><p>(Facultatif) Empêche [!DNL Google Ads] d’afficher la publicité pour les utilisateurs de tablette. Les valeurs peuvent inclure <i>yes</i> et <i>no</i>. |
| [!UICONTROL Landing Page Suffix] | Tous les paramètres à ajouter à la fin des URL finales pour suivre les informations. Exemple : `param2=value1&param3=value2`<br><br>Voir &quot;[Formats de suivi des clics pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)&quot;.<br><br>Les suffixes d’URL finale aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur [!DNL Google Ads]. |
| [!UICONTROL Tracking Template] | Le modèle de suivi, qui spécifie tous les paramètres de suivi et les redirections hors domaine d’entrée et incorpore l’URL finale dans un paramètre [!DNL ValueTrack]. Le modèle de suivi au niveau le plus granulaire (avec le mot-clé comme le plus granulaire) remplace les valeurs à tous les niveaux supérieurs.<br><br>Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload]&quot;, Search, Social et Commerce ajoute automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.<br><br>Pour les redirections et le suivi tiers, saisissez une valeur. Pour obtenir la liste des paramètres [!DNL ValueTrack] permettant d’indiquer les URL finales dans les modèles de suivi, reportez-vous aux paramètres &quot;Modèle de suivi uniquement&quot; de la section &quot;Paramètres disponibles [!DNL ValueTrack]&quot; dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2375447).<br><br>Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Base URL/Final URL] | URL de la page d’entrée vers laquelle les utilisateurs du moteur de recherche sont pris lorsqu’ils cliquent sur votre publicité, y compris les paramètres d’ajout configurés pour la campagne ou le compte. Les URL de base/finale au niveau du mot-clé remplacent celles au niveau de la publicité et supérieures.<br><br>Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Destination URL] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information ; non publiés dans le moteur de recherche) Pour les comptes avec des URL de destination, il s’agit de l’URL qui lie une publicité à une URL/page d’entrée de base sur le site web de l’annonceur (parfois via un autre site qui effectue le suivi des clics, puis redirige l’utilisateur vers la page d’entrée). Il comprend tous les paramètres d’ajout configurés pour la campagne ou le compte Search, Social et Commerce. Si vous avez généré des URL de suivi, elles sont basées sur les paramètres de suivi définis dans les paramètres de votre compte et de vos campagnes. Si vous avez ajouté des paramètres spécifiques au moteur de recherche, ils peuvent être remplacés par les paramètres équivalents pour Search, Social et Commerce.<br><br>Pour les comptes avec URL finales, cette colonne affiche la même valeur que la colonne URL de base/URL finale. |
| [!UICONTROL Custom URL Param] | Données à remplacer par la variable dynamique `{custom_code}` lorsque la variable est incluse dans les paramètres de suivi pour le compte de recherche ou les paramètres de campagne. Pour insérer la valeur personnalisée dans l’URL de tracking, vous devez télécharger le fichier de feuille d’envoi groupé à l’aide de l’option Générer les URL de tracking . |
| [!UICONTROL Creative Type] | Le format de publicité : <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (type de publicité obsolète), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (obsolète), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (publicités commerciales) ou <i>[!UICONTROL Responsive search ad]</i>. La valeur par défaut des nouvelles publicités est <i>[!UICONTROL Text ad]</i>.<br><br>Obligatoire pour créer ou modifier l’état d’une publicité de produit. |
| [!UICONTROL Param1] | <p>Valeur numérique du paramètre de publicité `{param1}`, qui peut être incluse dans la copie de publicité ou dans l’URL d’affichage de toute publicité dans le fichier de feuille d’envoi groupé. La longueur maximale est de 25 caractères. Vous pouvez inclure les caractères non numériques suivants :</p><ul><li><p>La valeur peut être précédée ou annexée d’un symbole ou d’un code de devise. Par exemple, `£2.000,00` et `2000GBP` sont valides.</p></li><li><p>La valeur peut inclure une virgule (`,`) ou un point (`.`) comme séparateur, avec un point facultatif (`.`) ou une virgule (`,`) pour les valeurs fractionnaires. Par exemple, `1,000.00` et `2.000,10` sont valides.</p></li><li><p>La valeur peut être précédée d’un signe de pourcentage (`%`), d’un signe plus (`+`) ou d’un signe moins (`- `). Par exemple, `20%`, `208+` et `-42.32` sont valides.</p></li><li><p>Deux nombres peuvent être incorporés avec une barre oblique. Par exemple, `4/1` et `0.95/0.45` sont valides.</p></li></ul><p>Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets).</p> |
| [!UICONTROL Param2] | Valeur numérique du paramètre de publicité `{param2}`, qui peut être incluse dans la copie de publicité ou dans l’URL d’affichage de toute publicité dans le fichier de feuille d’envoi groupé. Pour plus d’informations, voir l’entrée de Param1 . |
| [!UICONTROL Audience] | La liste de remarketing pour les annonces de recherche (RLSA) cible l’audience cible ou exclue pour la campagne ou le groupe publicitaire. Indiquez s’il s’agit d’une cible ou d’une exclusion dans le champ &quot;Type de cible&quot;. |
| [!UICONTROL Target Type] | (Lorsqu’une audience est spécifiée) Indique si l’audience spécifiée est une <i>inclusion</i> (cible) ou une <i>exclusion</i>. |
| [!UICONTROL Campaign Status] | État d’affichage de la campagne : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (non modifiable) ou <i>[!UICONTROL Deleted]</i> (campagnes existantes uniquement). La valeur par défaut des nouvelles campagnes est <i>[!UICONTROL Active]</i>. Pour supprimer une campagne active ou suspendue, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | État d’affichage du groupe publicitaire : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (groupes publicitaires existants uniquement). La valeur par défaut des nouveaux groupes publicitaires est [!UICONTROL Active]. Pour supprimer un groupe publicitaire actif ou en pause, saisissez la valeur `Deleted`. |
| [!UICONTROL Keyword Status] | État d’affichage du mot-clé : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (mots-clés existants uniquement). La valeur par défaut des nouveaux mots-clés est [!UICONTROL Active]. Pour supprimer un mot-clé actif ou en pause, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | État d’affichage de la publicité : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (publicités existantes uniquement), <i>[!UICONTROL Disapproved]</i> (non modifiable) ou <i>[!UICONTROL Paused]</i>. La valeur par défaut des nouvelles publicités est [!UICONTROL Active]. Pour supprimer une publicité active ou en pause, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | État de l’emplacement du site web : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (publicités existantes uniquement). La valeur par défaut des nouveaux sites web est <i>Active.</i> Pour supprimer un emplacement actif ou en pause, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | État d’une cible de recherche dynamique : <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> ou <i>[!UICONTROL Deleted]</i> (cibles existantes uniquement). La valeur par défaut des nouvelles cibles est <i>Active.</i> Pour supprimer une cible active ou suspendue, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | État d’affichage du groupe de produits : <i>[!UICONTROL Active]</i> <span>ou</span> <i>[!UICONTROL Deleted]</i> (groupes de produits existants uniquement). La valeur par défaut des nouveaux groupes de produits est <i>[!UICONTROL Active]</i>. Pour supprimer un groupe de produits actif, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | État d’affichage du lien de site : <i>Actif ou supprimé</i> (liens de site existants uniquement). La valeur par défaut des nouveaux liens de site est <i>[!UICONTROL Active]</i>. Pour supprimer un lien de site actif, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | État de la cible de l’emplacement : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i> (emplacements existants uniquement). La valeur par défaut des nouveaux emplacements est [!UICONTROL Active]. Pour supprimer un emplacement actif, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | État de la cible ou de l’exclusion RLSA au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL Active]</i> ou [!UICONTROL Deleted]</i> (cibles existantes uniquement). La valeur par défaut des nouvelles cibles ou exclusions est <i>[!UICONTROL Active]</i>. Pour supprimer une cible ou une exclusion active, saisissez la valeur <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>État de la cible d’appareil au niveau de la campagne ou du groupe publicitaire : <i>[!UICONTROL Active]</i> ou <i>[!UICONTROL Deleted]</i>. Pour les nouvelles campagnes et les nouveaux groupes publicitaires, la valeur par défaut est <i>[!UICONTROL Active]</i>.</p> |
| \[Classification d’étiquette spécifique au annonceur\] | (Nommé pour une classification d’étiquettes spécifique à l’annonceur, telle que &quot;Couleur&quot; pour une classification d’étiquettes appelée Couleur) Une valeur pour la classification spécifiée qui est associée à l’entité. Vous ne pouvez inclure qu’une seule valeur par classification par entité (par exemple, &quot;rouge&quot; pour la classification d’étiquettes &quot;Couleur&quot; pour la campagne A). La longueur maximale est de 100 caractères et la valeur peut inclure des caractères ASCII et non ASCII.<br><br>Les classifications d’étiquettes et leurs valeurs d’étiquettes sont appliquées à tous les composants enfants ; les nouveaux composants ajoutés ultérieurement sont automatiquement associés au libellé. Les classifications d’étiquettes pour les groupes de produits sont appliquées au niveau de l’unité (la plus granulaire).<br><br>Ni le nom de la classification ni la valeur de la classification ne sont sensibles à la casse. |
| [!UICONTROL Constraints] | Contrainte affectée à l’entité. Vous ne pouvez affecter qu’une seule contrainte par entité.<br><b>>Les contraintes sont héritées par les entités enfants. Il n’est donc pas nécessaire de saisir des valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées. |
| [!UICONTROL Campaign ID] | Identifiant unique qui identifie une campagne existante. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour la campagne. |
| [!UICONTROL Ad Group ID] | Identifiant unique qui identifie un groupe publicitaire existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour le groupe publicitaire. |
| [!UICONTROL Keyword ID] | Identifiant unique qui identifie un mot-clé existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez le mot-clé, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le mot-clé ou b) une &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Ad ID] | <p>Identifiant unique qui identifie une publicité existante. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Pour les annonces responsives sur le Réseau de Recherche, l&#39;identifiant de la publicité ou l&#39;AMO ID est requis pour modifier ou supprimer des données de publicité. Pour tous les autres types d’entité, l’ID de publicité est requis uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) et &quot;[!UICONTROL AMO ID]&quot;. Cependant, si vous n’incluez ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID] et que les colonnes de propriétés de publicité correspondent à plusieurs publicités, l’état d’une seule des publicités change.</p><p><b>Remarque : </b> Si vous modifiez a) des colonnes de propriétés de publicité à l’exception de l’état d’une publicité existante ou b) des données pour une publicité de recherche réactive, et que vous n’incluez ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID], alors une nouvelle publicité est créée et la publicité existante n’est pas modifiée.</p> |
| [!UICONTROL Placement ID] | Identifiant unique qui identifie un emplacement de site web. Obligatoire uniquement lorsque vous modifiez ou supprimez l’emplacement, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier l’emplacement ou b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Target ID] | Identifiant unique qui identifie une cible automatique existante. Obligatoire uniquement lorsque vous modifiez ou supprimez la cible automatique, sauf si la ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL Product Group ID] | Identifiant unique qui identifie un groupe de produits existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez le groupe de produits, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le groupe de produits ou b) et &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL Sitelink ID] | Identifiant unique qui identifie un lien de site existant. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez le lien de site, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le lien de site ou b) et &quot;[!UICONTROL AMO ID]&quot;.&quot; Cependant, si vous n’incluez ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] et que les colonnes de propriétés correspondent à plusieurs liens de site, l’état d’un seul lien de site change.</p><p><b>Remarque : </b> Si vous modifiez les colonnes de propriétés sitelink à l’exception de Status pour un lien de site existant, et que vous n’incluez ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID], un nouveau lien de site est créé et le lien de site existant n’est pas modifié. |
| [!UICONTROL RLSA Target ID] | Identifiant unique qui identifie une cible ou une exclusion RLSA existante au niveau d’une campagne ou d’un groupe publicitaire. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez la cible ou l’exclusion, sauf si la ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL Device Target ID] | <p>Identifiant unique qui identifie une cible ou une exclusion d’appareil existante au niveau de la campagne ou du groupe publicitaire. Dans les fichiers CSV et TSV, il doit être précédé d’un guillemet simple (’).[^1] Obligatoire uniquement lorsque vous modifiez ou supprimez la cible, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour la cible.</p> |
| [!UICONTROL AMO ID] | (Dans les feuilles d’envoi groupées générées) Identifiant unique généré par l’Adobe pour une entité synchronisée. Pour les publicités de recherche réactive, l’AMO ID est requis pour modifier ou supprimer les publicités, sauf si vous incluez l’ID de publicité. Pour modifier les données de tous les autres types d’entité avec un AMO ID, celui-ci doit les modifier ou les supprimer, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |
| [!UICONTROL EF Error Message] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL EF Errors]. Cette valeur n’est pas publiée sur le réseau publicitaire. |
| [!UICONTROL SE Error Message] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des messages d’erreur du réseau publicitaire concernant les données de la ligne ; les messages d’erreur sont inclus dans les fichiers [!UICONTROL SE Errors]. Cette valeur n’est pas publiée sur le réseau publicitaire. |
| [!UICONTROL Exemption Request] | (Inclus dans les feuilles d’envoi groupées générées à des fins d’information) Espace réservé pour l’affichage des noms et du texte des stratégies publicitaires [!DNL Google Ads] violées par une publicité. |
| [!UICONTROL Retail Hash] | (Inclus à des fins d’informations dans les feuilles d’envoi groupées générées à l’aide d’Advanced Campaign Management) Code de hachage alphanumérique (par exemple, f9639f40cdf56524b541e5dacf55a991) qui indique que l’élément a été généré à l’aide de la vue avancée (ACM). |

[^1] : [!DNL Excel] convertit les grands nombres en notation scientifique (par exemple, 2.12E+09 pour 2115585666) lorsqu’il ouvre le fichier. Pour afficher les chiffres de la notation standard, sélectionnez n’importe quelle cellule de la colonne et cliquez dans la barre de formule.

## Champs requis pour créer, modifier ou supprimer chaque composant de compte {#bulksheet-fields-per-component-google}

Les sections suivantes comprennent les champs relatifs à des entités de compte spécifiques.

>[!NOTE]
>
>Lorsqu’un champ n’est pas applicable à une action, toute valeur saisie dans le champ est ignorée.

### Champs de campagne

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Campaign Budget] | Requis pour créer une campagne. |
| [!UICONTROL Delivery Method] | Requis pour créer une campagne. |
| [!UICONTROL Channel Type] | Requis pour créer une campagne. |
| [!UICONTROL Networks] | Requis pour créer une campagne. |
| [!UICONTROL DSA Domain Name] | Requis pour créer une campagne avec des annonces de recherche dynamique sur le réseau de recherche. |
| [!UICONTROL DSA Domain Language] | Requis pour créer une campagne avec des annonces de recherche dynamique sur le réseau de recherche. |
| [!UICONTROL Campaign Priority] | Requis pour créer une campagne d’achat. |
| [!UICONTROL Merchant ID] | Requis pour créer une campagne d’achat. |
| [!UICONTROL Sales Country] | Requis pour créer une campagne d’achat. |
| [!UICONTROL Product Scope Filter] | (Campagnes commerciales) Facultatif |
| [!UICONTROL Languages] | Facultatif |
| [!UICONTROL Device Targets] | Facultatif |
| [!UICONTROL Device Targets (Google Adwords)] | Facultatif |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Facultatif |
| [!UICONTROL Audience Target Method] | n/a |
| [!UICONTROL Landing Page Suffix] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Campaign Status] | Requis uniquement pour supprimer une campagne. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Obligatoire uniquement lorsque vous modifiez le nom de la campagne, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour la campagne. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs d’un groupe publicitaire

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Networks] | n/a |
| [!UICONTROL GDN Custom Bid Level] | Facultatif |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Ad Group Type] | Requis pour créer un groupe publicitaire. |
| [!UICONTROL Max CPC] | Facultatif |
| [!UICONTROL Max Content CPC] | Facultatif |
| [!UICONTROL Audience Target Method] | Obligatoire |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Ad Group Status] | Requis uniquement pour supprimer un groupe publicitaire. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Ad Group ID] | Obligatoire uniquement lorsque vous modifiez le nom du groupe publicitaire, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour le groupe publicitaire. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de mot-clé

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
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
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Keyword ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le mot-clé, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le mot-clé ou b) et &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de placement

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
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
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Placement ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez l’emplacement, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier l’emplacement ou b) un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Annonce de recherche dynamique étendue

Ce type d’annonce est désormais appelé &quot;publicité de recherche dynamique&quot; dans [!DNL Google Ads]. Pour plus d’informations sur la création d’annonces de recherche dynamique, voir &quot;[Implémentation [!DNL Google Ads] de publicités de recherche dynamique](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html)&quot;.

Pour ce type d’annonce, utilisez la ligne &quot;[!UICONTROL Creative (except RSA)]&quot; dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Creative Preferred Devices] | Facultatif |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Obligatoire pour créer une publicité ou modifier la description. <b>Remarque : </b> Pour ce type de publicité, la modification de la copie de publicité supprime la publicité existante et en crée une nouvelle. |
| [!UICONTROL Display URL] | Obligatoire |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Creative Type] | Requis pour créer ou modifier l’état d’une publicité de produit. |
| [!UICONTROL Ad Status] | Requis pour supprimer une publicité. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) et &quot;[!UICONTROL AMO ID]&quot;. Cependant, si vous n’incluez ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID] et que les colonnes de propriétés de publicité correspondent à plusieurs publicités, l’état d’une seule des publicités change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de publicité de liste de produits/achats

Pour plus d’informations sur la création de publicités commerciales, voir &quot;[Implémentation [!DNL Google Ads] campagnes commerciales](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html)&quot;.

Pour ce type d’annonce, utilisez la ligne &quot;[!UICONTROL Creative (except RSA)]&quot; dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Promotion Line] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Facultatif |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Creative Type] | Requis pour créer ou modifier l’état d’une publicité de produit. |
| [!UICONTROL Ad Status] | Requis pour supprimer une publicité. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) et &quot;[!UICONTROL AMO ID]&quot;. Cependant, si vous n’incluez ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID] et que les colonnes de propriétés de publicité correspondent à plusieurs publicités, l’état d’une seule des publicités change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de publicité de recherche réactive

Pour ce type d’annonce, utilisez la ligne &quot;[!UICONTROL Responsive Search Ad]&quot; dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | Pour les annonces responsives sur le Réseau de Recherche, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] et [!UICONTROL Ad Title 3] sont nécessaires pour créer une publicité, et tous les autres champs de Titre de la publicité sont facultatifs. Pour supprimer la valeur existante pour un champ non obligatoire, utilisez la valeur `[delete]` (crochets compris). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Facultatif |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Pour les annonces responsives sur le Réseau de Recherche, [!UICONTROL Description Line 1] et [!UICONTROL Description Line 2] sont nécessaires pour créer une publicité, et [!UICONTROL Description Line 3] et [!UICONTROL Description Line 4] sont facultatifs. Pour supprimer la valeur existante, utilisez la valeur `[delete]` (y compris les crochets). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Facultatif |
| [!UICONTROL Display Path 1] | Facultatif |
| [!UICONTROL Display Path 2] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire pour créer une publicité. |
| [!UICONTROL Custom URL Param] | Facultatif |
| [!UICONTROL Creative Type] | Facultatif |
| [!UICONTROL Ad Status] | Requis pour supprimer une publicité. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire pour modifier ou supprimer des publicités, sauf si la ligne comprend un &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer des publicités, sauf si vous incluez l’identifiant de publicité. |

### Champs de publicité textuelle

Pour ce type d’annonce, utilisez la ligne &quot;[!UICONTROL Creative (except RSA)]&quot; dans la boîte de dialogue [!UICONTROL Download Bulksheet].

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

>[!NOTE]
>
>Les publicités textuelles étendues ont été abandonnées en juin 2022. Vous pouvez uniquement supprimer des publicités textuelles existantes.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Creative Preferred Devices] | Lecture seule |
| [!UICONTROL Ad Title], Titre de la publicité 2-3 | Lecture seule |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Lecture seule |
| [!UICONTROL Display URL] | Lecture seule |
| [!UICONTROL Display Path 1] | Lecture seule |
| [!UICONTROL Display Path 2] | Lecture seule |
| [!UICONTROL Tracking Template] | Lecture seule |
| [!UICONTROL Base URL/Final URL] | Lecture seule |
| [!UICONTROL Custom URL Param] | Lecture seule |
| [!UICONTROL Creative Type] | Facultatif |
| [!UICONTROL Ad Status] | Obligatoire |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Ad ID] | Obligatoire uniquement lorsque vous modifiez l’état de la publicité, sauf si la ligne comprend a) suffisamment de colonnes de propriétés de publicité pour identifier la publicité ou b) et &quot;[!UICONTROL AMO ID]&quot;. Cependant, si vous n’incluez ni [!UICONTROL Ad ID] ni [!UICONTROL AMO ID] et que les colonnes de propriétés de publicité correspondent à plusieurs publicités, l’état d’une seule des publicités change. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de cible de recherche dynamique (ciblage automatique)

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Max CPC] | Facultatif |
| [!UICONTROL Auto Target Expression] | Obligatoire uniquement lorsque le paramètre de campagne sur &quot;[!UICONTROL Use my website contents to target my ads]&quot; n’est pas activé. |
| [!UICONTROL Match Type] | Facultatif |
| [!UICONTROL Target Status] | Obligatoire pour supprimer une cible |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible automatique, sauf si la ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Shopping dans les champs du groupe de produits

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Obligatoire |
| [!UICONTROL Max CPC] | Requis pour créer un groupe de produits. |
| [!UICONTROL Parent Product Groupings] | Obligatoire |
| [!UICONTROL Product Grouping] | Obligatoire |
| [!UICONTROL Partition Type] | Requis pour créer un groupe de produits. |
| [!UICONTROL Match Type] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire |
| [!UICONTROL Product Group Status] | Requis uniquement pour supprimer un groupe de produits. |
| \[Classification d’étiquette spécifique au annonceur\] | Facultatif |
| [!UICONTROL Constraints] | Facultatif |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Product Group ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le groupe de produits, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le groupe de produits ou b) et &quot;[!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de lien de site au niveau de la campagne et du groupe d’annonces

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Ad Group Name] | Requis pour les liens de site au niveau du groupe d’annonces. Non applicable pour les liens de site au niveau de la campagne. |
| [!UICONTROL Creative Preferred Devices] | Facultatif |
| [!UICONTROL Link Name] | Obligatoire |
| [!UICONTROL Start Date] | Facultatif |
| [!UICONTROL End Date] | Facultatif |
| [!UICONTROL Tracking Template] | Facultatif |
| [!UICONTROL Base URL/Final URL] | Obligatoire |
| [!UICONTROL Sitelink Status] | Requis uniquement pour supprimer un lien de site. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif |
| [!UICONTROL Sitelink ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez le lien de site, sauf si la ligne comprend a) suffisamment de colonnes de propriétés pour identifier le lien de site ou b) un &quot;[!UICONTROL AMO ID]&quot;. Cependant, si vous n’incluez ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID] et que les colonnes de propriétés correspondent à plusieurs liens de site, l’état d’un seul lien de site change.<br><br><b>Remarque : </b> Si vous modifiez les colonnes de propriétés sitelink à l’exception de [!UICONTROL Status] pour un lien de site existant et que vous n’incluez ni [!UICONTROL Sitelink ID] ni [!UICONTROL AMO ID], un nouveau lien de site est créé et le lien de site existant n’est pas modifié. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’ID d’entité et l’ID d’entité parent.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Cible de l’emplacement

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Location] | Obligatoire |
| [!UICONTROL Location Type] | Facultatif |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Location Status] | Requis uniquement pour supprimer une cible d’emplacement. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez le [!UICONTROL Campaign ID].<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs cibles des appareils au niveau de la campagne et du groupe publicitaire

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Device] | Requis pour créer ou modifier une cible d’appareil. |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Ad Group Name] | Requis pour les cibles d’appareil au niveau du groupe d’annonces. Non applicable pour les cibles d’appareil au niveau de la campagne. |
| [!UICONTROL Device Target Status] | Requis uniquement pour supprimer une cible d’appareil. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif ; applicable uniquement pour les cibles d’appareil au niveau du groupe d’annonces. |
| [!UICONTROL Device Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant cible du périphérique.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

### Champs de ciblage/exclusion au niveau de la campagne et au niveau du groupe publicitaire

Pour une description de chaque champ de données, voir &quot;[Tous les champs de données disponibles](#bulksheet-fields-all-google)&quot;.

| Champ | Obligatoire ? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Obligatoire, sauf si chaque ligne comprend un &quot;[!UICONTROL AMO ID]&quot; pour l’entité. |
| [!UICONTROL Campaign Name] | Obligatoire |
| [!UICONTROL Bid Adjustment] | Facultatif |
| [!UICONTROL Ad Group Name] | Requis pour les cibles et exclusions au niveau du groupe d’annonces. Non applicable pour les cibles et exclusions au niveau de la campagne. |
| [!UICONTROL Audience] | Requis pour créer une cible ou une exclusion. |
| [!UICONTROL Target Type] | Requis pour créer une cible ou une exclusion. |
| [!UICONTROL RLSA Target Status] | Requis uniquement pour supprimer une cible ou une exclusion. |
| [!UICONTROL Campaign ID] | Facultatif |
| [!UICONTROL Ad Group ID] | Facultatif ; applicable uniquement pour les cibles et exclusions au niveau du groupe d’annonces. |
| [!UICONTROL RLSA Target ID] | Obligatoire uniquement lorsque vous modifiez ou supprimez la cible, sauf si la ligne contient un &quot;[!UICONTROL AMO ID]&quot; pour la cible. |
| [!UICONTROL AMO ID] | Obligatoire pour modifier ou supprimer les données, sauf si vous incluez l’identifiant cible RLSA.<br><br>Search, Social &amp; Commerce utilise la valeur pour déterminer l’identité correcte à modifier, mais ne publie pas l’identifiant sur le réseau publicitaire. |

>[!MORELIKETHIS]
>
>* [Annexe - Erreurs de feuilles d’envoi groupé](../bulksheet-errors.md)
>* [Opérations que vous pouvez effectuer dans les feuilles d’envoi groupé](bulksheet-operations.md)
>* [ Formats de fichiers de feuille d’envoi groupé pris en charge](bulksheet-file-formats.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](../bulksheet-download.md)
>* [Formats de suivi des clics pour [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Télécharger un fichier de feuille d’envoi groupé ou un fichier d’erreur corrigé](../bulksheet-upload.md)
