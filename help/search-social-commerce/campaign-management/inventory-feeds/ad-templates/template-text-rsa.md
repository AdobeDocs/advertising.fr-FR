---
title: Paramètres de modèle de publicité textuelle et de recherche réactive pour les flux de stock
description: Référencez les paramètres des annonces textuelles et des modèles d’annonces de recherche réactive pour les flux d’inventaire.
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# Paramètres de modèle de publicité textuelle et de recherche réactive pour les flux de stock


*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

>[!NOTE]
>
>* Les caractères suivants sont réservés à la désignation des noms de colonne et des noms de modificateur dans le modèle et sont donc interdits en tant que texte dans tous les champs d’attribut :  `[ ] < > `
>* Dans [!DNL Yandex templates], vous pouvez utiliser les paramètres dynamiques. `{param1}` et `{param2}` uniquement dans les URL et vous ne pouvez pas utiliser l’insertion dynamique de prix dans les descriptions d’annonce.

## \[Au-dessus de tous les onglets\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Panneau de gauche\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (Facultatif) Mappe tous les nouveaux groupes d’annonces (non disponible pour [!DNL Yandex]), des mots-clés et des publicités pour des campagnes existantes, plutôt que de créer des campagnes. Si vous activez cette option, sélectionnez la méthode de mappage.

Utilisation [!UICONTROL Map Only] au niveau de la campagne, une structure de compte existante est étroitement liée à la taxonomie du produit et est facilement mappée au flux de données.

**[!UICONTROL Map Method]:** (Lorsque [!UICONTROL Map Only] est activé pour la campagne) Méthode utilisée par les nouveaux groupes publicitaires (non disponible pour [!DNL Yandex]), les mots-clés et les publicités sont mappés aux campagnes existantes :

* *[!UICONTROL Contains Anywhere]:* Ajoute des données à une campagne existante dont le nom inclut la chaîne spécifiée, le cas échéant.

* *[!UICONTROL Contains Exactly]:* Ajoute des données à une campagne existante dont le nom inclut la chaîne spécifiée, le cas échéant.

* *[!UICONTROL Exactly Matches]* (valeur par défaut) : ajoute des données à une campagne existante portant le même nom, le cas échéant.

Lorsqu’aucune correspondance n’est trouvée, toutes les données de la campagne sont ignorées. Si plusieurs correspondances de campagne sont trouvées, les mots-clés et les publicités sont mappés à tous.

**[!UICONTROL Campaign Tracking Template]:** (Comptes avec URL finales/avancées uniquement ; facultatif) Le modèle de suivi au niveau de la campagne, qui spécifie toutes les redirections de domaine hors entrée et paramètres de suivi et incorpore l’URL finale dans un paramètre. Cette valeur remplace le paramètre au niveau du compte, mais les modèles de suivi à des niveaux plus granulaires (avec le mot-clé comme plus granulaire) remplacent cette valeur.

* Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour incorporer l’URL finale :

   * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Pour obtenir une liste des paramètres permettant d’indiquer les URL finales dans les modèles de suivi, voir ([!DNL Microsoft Advertising] uniquement) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799/2) ou ([!DNL Google Ads] uniquement) les paramètres &quot;Modèle de tracking uniquement&quot; dans la section &quot;Disponible&quot; [!DNL ValueTrack] Paramètres&quot; dans la variable [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] uniquement) Utiliser le paramètre `!{unescapedurl}` pour indiquer l&#39;URL de la landing page.

   * Vous pouvez éventuellement inclure des paramètres d’URL et des paramètres personnalisés définis pour la campagne, séparés par des esperluettes (&amp;), tels que `{lpurl}?matchtype={matchtype}&device={device}`.

* Pour les redirections et le suivi tiers, saisissez une valeur.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** (Dans [!DNL Google Ads] et [!DNL Yandex] Paramètres de campagne) Les réseaux sur lesquels placer des publicités :

* *[!UICONTROL Search]:* Pour placer des offres pour des listes de recherche sponsorisées.

  ([!DNL Google Ads] campagnes) Pour inclure des offres sur les listes pour [!DNL Google Ads] partenaires de recherche, cochez la case en regard de **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* Pour placer des offres pour des emplacements sur des listes réseau de contenu (affichage). **Remarque :** Vous ne pouvez pas créer d’emplacements à l’aide du modèle. Lorsque vous sélectionnez cette option, créez des emplacements pour chaque groupe d’annonces et spécifiez les pages du réseau d’affichage à cibler pour chaque groupe d’annonces à l’aide de l’une des options suivantes : <!-- insert link --> feuilles d’envoi groupées ou <!-- insert links --> les paramètres de groupe publicitaire et d’emplacement dans la variable [!UICONTROL Search] > [!UICONTROL Campaigns] vues.

**[!UICONTROL Languages]:** ([!DNL Google Ads] réseaux de recherche et d’affichage uniquement) Une ou plusieurs langues cibles pour les publicités dans la campagne.

[!DNL Google Ads] détermine la langue d’un utilisateur à partir de [!DNL Google] paramètre de langue ou de la langue de la requête de recherche, de la page active ou des pages récemment consultées sur la page [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Comptes avec URL finales/avancées uniquement) Le modèle de suivi au niveau du groupe publicitaire, qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi et incorpore l’URL finale dans un paramètre.

Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

Pour les redirections et le suivi tiers, saisissez une valeur. Pour indiquer l&#39;URL de la landing page :

* Pour Yahoo ! Comptes Japan Ads, utilisez le paramètre {lpurl}.

* Pour connaître les paramètres disponibles pour les comptes Microsoft Advertising et Google Ads, voir [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou les paramètres du &quot;Modèle de suivi uniquement&quot; dans la section sur &quot;Disponible [!DNL ValueTrack] Paramètres&quot; dans la variable [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

Cette valeur remplace les paramètres au niveau du compte et de la campagne, mais les modèles de suivi à des niveaux plus granulaires (avec le mot-clé comme mot-clé le plus granulaire) remplacent cette valeur.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Mots-clés du groupe publicitaire spécifié (ou campagne pour [!DNL Yandex] ), qui peut être constitué de n’importe quelle combinaison de texte statique, de colonnes dans le fichier spécifié et de modificateurs. Les noms et les modificateurs de colonne sont remplacés par des données réelles lorsque le fichier de flux spécifié est propagé par le modèle.

Pour insérer un nom de colonne ou un groupe de modificateurs en tant que paramètre dynamique, cliquez dans le champ de saisie, puis sur un nom de colonne dans la liste de colonnes ou dans un [modifier le nom](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) dans la liste Modificateurs. Pour spécifier plusieurs mots-clés ou types de correspondance pour un même mot-clé, saisissez-les sur des lignes distinctes. Pour spécifier le type de correspondance de mot-clé, utilisez la syntaxe de type de correspondance suivante autour du nom de la colonne :

* Pour [!DNL Google Ads], [!DNL Microsoft Advertising], et [!DNL Yahoo! Japan Ads] templates :

   * Pour les paramètres dynamiques : Correspondance large = `[keyword]`, modificateur de correspondance large pour le premier terme de la variable [!UICONTROL Keyword] colonne (par exemple, +chaussures de daim bleues) = `+[keyword]`, modificateur de correspondance large pour chaque terme de la colonne Mot-clé (comme +bleu +daim +chaussures) = `+[keyword]+`, Correspondance des expressions = `"[keyword]"`, Correspondance exacte = `[[keyword]]`

   * Pour les mots-clés statiques : Correspondance large = `keyword`, modificateur de correspondance large = `+keyword`, ou Expression Correspondance = `"keyword"`

     Vous ne pouvez pas saisir ici de mots-clés statiques avec une correspondance exacte et une syntaxe de correspondance standard, car ils sont entourés de crochets (`[]`), comme le sont les paramètres dynamiques.

* Pour [!DNL Yandex] templates :

   * Pour les paramètres dynamiques : insérez le nom de la colonne, par exemple `[keyword]`. Pour indiquer le type de correspondance, utilisez la variable [[!DNL Yandex]syntaxe spécifique](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Remarque :** Pour les termes à correspondance large, utilisez la syntaxe suivante : modificateur de correspondance large pour le premier terme de la colonne Mot-clé (chaussures + daim bleu, par exemple) = `+[keyword]`, modificateur de correspondance large pour chaque terme de la colonne Mot-clé (comme +bleu +daim +chaussures) = `+[keyword]+`

   * Pour les mots-clés statiques : seuls les mots-clés de recherche sont pris en charge. Utilisez la variable [[!DNL Yandex]syntaxe spécifique](https://yandex.com/support/direct/keywords/symbols-and-operators.html) pour le mot-clé. Brackets (`[]`) pour indiquer que l’ordre des mots n’est pas pris en charge.

>[!NOTE]
>
>* Vous pouvez inclure manuellement plusieurs valeurs de modificateur dans le champ Mots-clés en encadrant des valeurs séparées par des virgules entre parenthèses avant ou après un paramètre de mot-clé (mais pas aux deux endroits). Par exemple : `(cheap, discount, affordable)[product]` produit trois publicités distinctes pour chaque produit.
>* Si vous ne spécifiez pas de type de correspondance, le type de correspondance par défaut &quot;broad&quot; est utilisé.
>* Les correspondances négatives ne sont pas prises en charge.
>* Les modificateurs de correspondance large Google ont désormais le même comportement de correspondance que les correspondances d’expression pour certaines langues et vous ne pouvez pas créer de mots-clés de modification de correspondance large. Voir [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/10286719) pour plus d’informations.

**[!UICONTROL Map Only]:** Ajoute de nouvelles publicités aux groupes publicitaires (ou aux campagnes pour [!DNL Yandex] comptes) dans lesquels les mots-clés spécifiés sont trouvés, plutôt que de créer de nouveaux mots-clés. Pour activer cette option, cochez la case. Lorsque cette option est activée, les variables Param 1 et Param 2 des mots-clés spécifiés ne s’appliquent pas, car les mots-clés existent.

**[!UICONTROL Keyword Final URL]:** (Comptes avec URL finales/avancées ; facultatif) URL de la page d’entrée vers laquelle les utilisateurs du réseau publicitaire sont redirigés lorsqu’ils cliquent sur votre publicité. Il doit inclure le même domaine que l’URL d’affichage et tous les paramètres de l’URL finale doivent correspondre aux paramètres de l’URL de la page d’entrée après le clic publicitaire. Il peut contenir des redirections dans le domaine de la landing page ou le sous-domaine, mais aucune redirection en dehors du domaine de la landing page.

Si vous utilisez un [!DNL Google Merchant Center] flux et inclure cette valeur dans le[!DNL Link]&quot;, puis insérez cette colonne dans ce champ.

>[!NOTE]
>
>* Si vous générez des URL de suivi lorsque vous publiez des données propagées par le biais du modèle, les paramètres de suivi sont ajoutés à cette valeur en fonction des paramètres de suivi du compte.
>* ([!DNL Google Ads] ) Évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit travailler avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.

**[!UICONTROL Keyword Tracking Template]:** (Comptes avec URL finales/avancées ; facultatif) Le modèle de suivi, qui spécifie tous les paramètres de suivi et redirections de domaine hors d’entrée et incorpore l’URL finale dans un paramètre. Le modèle de suivi au niveau le plus granulaire (avec le mot-clé comme le plus granulaire) remplace les valeurs à tous les autres niveaux.

* Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Vous pouvez éventuellement saisir des redirections et un suivi tiers.

* Pour indiquer l&#39;URL de la landing page :

   * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Pour obtenir une liste des paramètres permettant d’indiquer les URL finales dans les modèles de suivi, voir ([!DNL Microsoft Advertising] uniquement) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou ([!DNL Google Ads] uniquement) les paramètres &quot;Modèle de tracking uniquement&quot; dans la section &quot;Disponible&quot; [!DNL ValueTrack] Paramètres&quot; dans la variable [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] uniquement) Utiliser le paramètre `!{lpurl}` pour indiquer l&#39;URL de la landing page.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] templates\] :** ([!DNL Google Ads] modèles uniquement) La colonne du fichier spécifié qui représente la variable [!DNL Google Ads] `{param1}` ou `{param2}` que vous pouvez inclure dans la copie de publicité ou dans l’URL d’affichage de toute publicité créée à partir du modèle. Pour insérer le paramètre dynamique, cliquez dans le champ de saisie, puis sur le nom d&#39;une colonne dans la liste des colonnes. Le nom de la colonne est remplacé par les données réelles lorsque le fichier de flux est propagé par le modèle.

Si vous utilisez l’un ou l’autre des paramètres, vous avez la possibilité d’appliquer uniquement le paramètre aux nouveaux mots-clés ou de mettre également à jour les valeurs des mots-clés existants qui n’ont pas été créés à partir du modèle :

* **[!UICONTROL Do Not Apply to Existing Keywords]** (valeur par défaut) : insère simplement la valeur du paramètre pour les nouveaux mots-clés créés à l’aide du modèle.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Outre la création de mots-clés à partir du flux, Search, Social et Commerce met également à jour la valeur du paramètre pour tous les mots-clés existants dans le groupe d’annonces qui n’ont pas été créés à l’aide du modèle. Saisissez une valeur numérique unique qui est utilisée pour tous ces mots-clés. Le modèle doit contenir au moins un mot-clé.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Outre la création de nouveaux mots-clés à partir du flux, Search, Social et Commerce met également à jour la valeur du paramètre pour tous les mots-clés existants dans le groupe publicitaire qui n’ont pas été créés à l’aide du modèle tant que le fichier de flux contient des valeurs numériques pour le paramètre, avec jusqu’à une décimale, mais sans virgules, symboles ou codes de devise, ou tout autre caractère. La valeur minimale du paramètre dans le fichier de flux est utilisée pour tous les mots-clés existants. Par exemple, si le fichier de flux contient [!UICONTROL Param1] de 21500 et 22000, puis la variable [!UICONTROL Param1] les valeurs des mots-clés existants sont remplacées par 21500. Le modèle doit contenir au moins un mot-clé. **Conseil :** Utilisez cette option uniquement lorsque vous avez des groupes d’annonces avec des thèmes très serrés afin qu’il soit logique que les mots-clés aient la même valeur.

Les champs de données du fichier de flux peuvent contenir, au maximum, 25 caractères et ne peuvent contenir que des données numériques avec les caractères non numériques suivants :

* (Lorsque vous utilisez le[!UICONTROL Apply to Existing Keywords: Min]&quot;) Jusqu’à un point décimal seulement.

* (Lorsque vous n’utilisez pas le paramètre &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot;) :

   * La valeur peut être précédée ou annexée d’un symbole ou d’un code de devise. Par exemple, £2 000 000 et 2 000 GBP sont valides.

   * La valeur peut inclure une virgule (,) ou un point (.) comme séparateur, avec un point facultatif (.) ou virgule (,) pour les valeurs fractionnaires. Par exemple, 1 000.00 et 2 000.10 sont valides.

   * La valeur peut être précédée d’un signe de pourcentage (%), d’un signe plus (+) ou d’un signe moins (-). Par exemple, 20 %, 208+ et -42.32 sont valides.

   * Deux nombres peuvent être incorporés avec une barre oblique. Par exemple, 4/1 et 0.95/0.45 sont valides.

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising] templates\] :** ([!DNL Microsoft Advertising] modèles uniquement) Chaîne à utiliser comme valeur de substitution dans une publicité si le titre, le texte, l’URL d’affichage ou l’URL finale contient le paramètre `{Param2}` chaîne de substitution dynamique. La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments de publicité dans lesquels vous l’utilisez (par exemple, un titre de publicité peut contenir jusqu’à 25 caractères).

**[!UICONTROL Param 3]:** ([!DNL Microsoft Advertising] modèles uniquement) Chaîne à utiliser comme valeur de substitution dans une publicité si le titre, le texte, l’URL d’affichage ou l’URL finale contient le paramètre `{Param3}` chaîne de substitution dynamique. La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments de publicité dans lesquels vous l’utilisez (par exemple, un titre de publicité peut contenir jusqu’à 25 caractères).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** L’offre initiale pour chaque mot-clé avec le type de correspondance ou de publicité spécifié.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] et [!DNL Microsoft Advertising] campagnes uniquement) Le type de publicités : *[!UICONTROL Expanded Search Ads]* ou *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Facultatif) Préremplit tous les autres champs de copie de publicité avec le texte des champs de copie de publicité d’origine.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Publicités de recherche réactive uniquement) Position de la publicité à laquelle le titre/le titre doit être inclus (par exemple : &quot;[!UICONTROL Pinned at position 1]&quot;). La valeur par défaut est [!UICONTROL Unpinned].

Au moins un titre doit être disponible pour chaque poste. Si vous épinglez plusieurs titres à la même position, la publicité finale inclut toujours l’un de ces titres à la position spécifiée. Il se peut que les titres épinglés à la position 3 ne s’affichent pas avec la publicité.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (Publicités de recherche réactives uniquement) Titres des publicités (titres). Chaque variante d’annonce doit comporter au moins trois titres, et jusqu’à 15 titres d’annonce. Le réseau publicitaire affiche des publicités avec trois titres au maximum. La longueur maximale de chaque titre est de 30 caractères, y compris tout texte dynamique (comme les valeurs des mots-clés et des personnalisateurs de publicités).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Publicités textuelles standard Microsoft Advertising existantes uniquement ; lecture seule) Titre, ou première ligne, d’une publicité. Microsoft Advertising a rendu obsolète la création et la modification d’annonces textuelles standard.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] et [!DNL Yahoo! Japan Ads] modèles de publicités textuelles étendues (uniquement) Titre d’une publicité. La longueur maximale de chaque ligne (après le remplacement de paramètres dynamiques) est de 30 caractères ou 15 caractères codés sur deux octets.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] modèle de publicité textuelle développée uniquement ; facultatif) Troisième titre d’une publicité. La longueur maximale (après le remplacement de tous les paramètres dynamiques) est de 30 caractères ou 15 caractères codés sur deux octets.

**[!UICONTROL Title]:** ([!DNL Yandex] uniquement) Titre, ou première ligne, d’une publicité. La limite est de 33 caractères.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (Publicités Microsoft publicités textuelles étendues uniquement) Titre d’une publicité. La longueur maximale de chaque ligne (après le remplacement de paramètres dynamiques) est de 30 caractères ou 15 caractères codés sur deux octets.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Publicité Microsoft publicités textuelles étendues uniquement) Corps d’une publicité. La longueur maximale (après le remplacement de paramètres dynamiques) est de 80 caractères ou de 40 caractères codés sur deux octets (chinois, japonais et coréen, par exemple).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** Corps de la publicité.

* (Modèles de publicités textuelles étendus Google Ads) La longueur maximale (après le remplacement de paramètres dynamiques) est de 90 caractères ou de 45 caractères codés sur deux octets.

* (Yahoo ! Modèles Japan Ads) La longueur maximale (après le remplacement de paramètres dynamiques) est de 80 caractères ou 40 caractères sur deux octets.

* (Modèles Yandex) La longueur maximale (après le remplacement de paramètres dynamiques) est de 75 caractères et un seul mot ne peut pas dépasser 22 caractères.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Publicités de recherche réactive uniquement) Position de la publicité à laquelle la description doit être incluse (comme &quot;[!UICONTROL Pinned at position 1]&quot;). La valeur par défaut est [!UICONTROL Unpinned]. Au moins une description doit être disponible pour chaque poste.

Si vous épinglez plusieurs descriptions à la même position, la publicité finale inclut toujours l’une de ces descriptions à la position spécifiée. Il se peut que les descriptions épinglées à la position 2 ne s’affichent pas avec la publicité.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (Publicités de recherche réactive uniquement) Description des publicités. Chaque variante d’annonce doit inclure au moins deux descriptions d’annonce, et jusqu’à quatre d’entre elles. Le réseau publicitaire affiche des publicités comportant jusqu’à deux descriptions ; saisissez au moins deux. La longueur maximale de chaque description est de 90 caractères, y compris tout texte dynamique (comme les valeurs des mots-clés et des personnalisateurs de publicités).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Modèles de publicités textuelles étendues Google uniquement ; facultatif) Seconde ligne de la publicité. La longueur maximale (après le remplacement de paramètres dynamiques) est de 90 caractères ou de 45 caractères codés sur deux octets.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Texte étendu et annonces responsives uniquement ; facultatif) Un ou deux chemins d’URL à inclure consécutivement après l’URL de base. Il doit décrire plus en détail le produit ou le service de l’annonce. Par exemple, si vous ajoutez une [!UICONTROL Display Path 1] de &quot;chaussures&quot; et [!UICONTROL Display Path 2] de &quot;Extérieur&quot; à l’URL de base www.example.com, l’URL est www.example.com/Shoes/Outdoor. La longueur maximale (après le remplacement de paramètres dynamiques) de chaque champ est de 15 caractères ou 7 caractères sur deux octets.

Pour les annonces responsives sur le Réseau de Recherche, insérez un personnalisateur de Publicités aux formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide :

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Existant [!DNL Microsoft Advertising] et [!DNL Yahoo! Japan Ads] publicités textuelles standard uniquement ; lecture seule) URL affichée dans une publicité.

[!DNL Microsoft Advertising] et [!DNL Yahoo! Japan Ads] ont rendu obsolètes la création et la modification d’annonces textuelles standard.

**[!UICONTROL Base URL]:** (Comptes avec URL de destination uniquement) Page à laquelle les utilisateurs sont redirigés. Il peut inclure un code de redirection et de suivi tiers. Si vous utilisez le service de suivi de conversion d’Adobe Advertising et que les paramètres de campagne incluent l’utilisation de la variable [!UICONTROL EF Redirect] et l’ajout d’un suivi au niveau de la publicité, puis de Search, Social et Commerce ajoute automatiquement son propre code de redirection et de suivi à la publicité.

Pour insérer un nom de colonne ou un groupe de modificateurs en tant que paramètre dynamique, cliquez dans le champ de saisie, puis sur un nom de colonne dans la liste de colonnes ou dans un [modifier le nom](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) dans le [!UICONTROL Modifiers] liste.

**[!UICONTROL Final URL]:** (Comptes avec URL finales/avancées) URL de la page d’entrée vers laquelle les utilisateurs sont redirigés lorsqu’ils cliquent sur votre publicité. Il doit inclure le même domaine que l’URL d’affichage et tous les paramètres de l’URL finale doivent correspondre aux paramètres de l’URL de la page d’entrée après le clic publicitaire. Il peut contenir des redirections dans le domaine de la landing page ou le sous-domaine, mais aucune redirection en dehors du domaine de la landing page.

Si vous utilisez un [!DNL Google Merchant] Centrer le flux et inclure cette valeur dans le[!UICONTROL Link]&quot;, puis insérez cette colonne dans ce champ.

>[!NOTE]
>
>* Si vous générez des URL de suivi lorsque vous publiez des données propagées par le biais du modèle, les paramètres de suivi sont ajoutés à cette valeur en fonction des paramètres de suivi du compte.
>* ([!DNL Google Ads] comptes ) Évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit collaborer avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.

**[!UICONTROL Tracking Template]:** (Comptes avec URL finales/avancées ; facultatif) Le modèle de suivi, qui spécifie tous les paramètres de suivi et redirections de domaine hors d’entrée et incorpore l’URL finale dans un paramètre. Le modèle de suivi au niveau le plus granulaire (avec le mot-clé comme le plus granulaire) remplace les valeurs à tous les autres niveaux.

Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

Pour les redirections et le suivi tiers, saisissez une valeur. Pour indiquer l&#39;URL de la landing page :

* Pour Yahoo ! Comptes Japan Ads, utilisez le paramètre {lpurl}.

* Pour connaître les paramètres disponibles pour les comptes Microsoft Advertising et Google Ads, voir [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou les paramètres du &quot;Modèle de suivi uniquement&quot; dans la section sur &quot;Disponible [!DNL ValueTrack] Paramètres&quot; dans la variable [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

**\[Autres champs de publicité sous les champs de publicité d’origine\] :** (Facultatif) Un autre ensemble de copies d’annonces pour une publicité, qui peut être utilisé si l’une des lignes de la copie d’annonce d’origine dépasse la longueur maximale autorisée une fois que des paramètres dynamiques sont remplis avec des données pendant la propagation.

>[!NOTE]
>
>* Si la variable [!UICONTROL Prefill] est sélectionnée, puis les champs alternatifs sont préremplis avec les champs originaux et vous pouvez les modifier si nécessaire.
>* Seuls les champs de copie de publicité qui dépassent la longueur maximale sont remplacés par la valeur alternative. Par exemple, si seul un titre ou un titre d’origine est trop long, la variation de publicité générée utilise le titre ou titre de remplacement et les descriptions d’origine. Par conséquent, assurez-vous que l’autre copie de publicité est logique lorsqu’elle est combinée à la copie de publicité d’origine.
>* Si la copie de publicité d’origine répond aux exigences de longueur du moteur de recherche, la copie de publicité alternative est ignorée.

**\[Composant\] [!UICONTROL Ad Label Classifications] > \[Classification et valeur d’étiquette\] :** (Facultatif) Valeurs de cinq classifications d’étiquettes existantes au maximum à affecter aux variations d’annonces créées ou modifiées à l’aide du modèle. Pour chaque composant de campagne auquel vous souhaitez affecter des classifications d’étiquettes :

1. Cochez la case .

1. Configurez les valeurs de classification des étiquettes pour le modèle de variation publicitaire :

   * Pour chaque classification et valeur d’étiquette à affecter au composant, procédez comme suit :

      1. Cliquez sur **[!UICONTROL Add Label Classification]**.

      1. Sélectionnez la classification de libellé existante, puis sélectionnez une valeur existante ou saisissez une nouvelle valeur.

         La longueur maximale de chaque valeur est de 100 caractères. Elle peut contenir des caractères ASCII et non ASCII.

         Pour insérer un nom de colonne en tant que paramètre dynamique pour une valeur de classification de libellé, cliquez dans le champ de saisie (le deuxième champ), puis cliquez sur un nom de colonne dans la liste des colonnes.

         Vous ne pouvez inclure qu’une seule valeur par classification par composant de campagne. Par exemple, une campagne peut avoir Color=Red mais pas Color=Red et Color=Blue.

         * Pour modifier une valeur de classification de libellé existante, sélectionnez ou saisissez une nouvelle valeur.

         * Pour supprimer une valeur de classification d’étiquette existante, cliquez sur **[!UICONTROL X]** en regard de la valeur .

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [A propos de l’automatisation de la gestion des publicités à l’aide des flux d’inventaire](../inventory-feeds-about.md)
>* [Gestion des modificateurs](../modifiers-manage.md)
>* [Gestion des fichiers de flux de données d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propager les données de flux par le biais de modèles](../feed-data-propagate.md)
>* [Publier les données de campagne des flux d’inventaire vers les réseaux publicitaires](../propagated-data-post.md)
