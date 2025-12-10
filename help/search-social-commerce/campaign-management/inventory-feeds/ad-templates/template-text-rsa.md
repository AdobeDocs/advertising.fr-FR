---
title: Paramètres d’annonce textuelle et de modèle d’annonce responsive sur le Réseau de recherche pour les flux d’inventaire
description: Référencez les paramètres des modèles d’annonce de texte et d’annonce de recherche responsive pour les flux d’inventaire.
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '3360'
ht-degree: 0%

---

# Paramètres d’annonce textuelle et de modèle d’annonce responsive sur le Réseau de recherche pour les flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

>[!NOTE]
>
>* Les caractères suivants sont réservés à la désignation des noms de colonne et de modificateur dans le modèle et sont donc interdits en tant que texte dans tous les champs d’attribut : `[ ] < > `
>* Dans [!DNL Yandex templates], vous ne pouvez utiliser les paramètres dynamiques `{param1}` et `{param2}` que dans les URL et vous ne pouvez pas utiliser l’insertion dynamique de prix dans les descriptions d’annonces.

## \[Surtout les onglets\]

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

**[!UICONTROL Map Only]:** (facultatif) Mappe tous les nouveaux groupes publicitaires (non disponibles pour les [!DNL Yandex]), mots-clés et annonces aux campagnes existantes, plutôt que de créer des campagnes. Si vous activez cette option, sélectionnez la méthode de mappage.

L’utilisation de [!UICONTROL Map Only] au niveau de la campagne nécessite une structure de compte existante étroitement liée à la taxonomie du produit et facilement mappée au flux de données.

**[!UICONTROL Map Method]:** (lorsque [!UICONTROL Map Only] est activé pour la campagne) Méthode par laquelle les nouveaux groupes d’annonces (non disponibles pour les [!DNL Yandex]), mots-clés et annonces sont mappés aux campagnes existantes :

* *[!UICONTROL Contains Anywhere]:* Ajoute des données à une campagne existante dont le nom inclut la chaîne spécifiée, si elle existe.

* *[!UICONTROL Contains Exactly]:* Ajoute des données à une campagne existante dont le nom inclut la chaîne spécifiée, si elle existe.

* *[!UICONTROL Exactly Matches]* (valeur par défaut) : ajoute des données à une campagne existante portant le même nom, si elle existe déjà.

Lorsqu’aucune correspondance n’est trouvée, toutes les données de la campagne sont ignorées. Si plusieurs correspondances de campagne sont trouvées, les mots-clés et les publicités sont mappés à toutes les correspondances.

**[!UICONTROL Campaign Tracking Template]:** (Comptes avec URL finales/avancées uniquement ; facultatif) Modèle de suivi au niveau de la campagne, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de l’atterrissage et incorpore l’URL finale dans un paramètre. Cette valeur remplace le paramètre au niveau du compte, mais les modèles de suivi à des niveaux plus granulaires (avec le mot-clé comme le plus granulaire) remplacent cette valeur.

* Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour incorporer l’URL finale :

   * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Pour obtenir une liste de paramètres indiquant les URL finales dans les modèles de tracking, reportez-vous à la [!DNL Microsoft Advertising]documentation[[!DNL Microsoft Advertising]  (](https://help.ads.microsoft.com/#apex/3/en/56799/2) uniquement) ou ([!DNL Google Ads] uniquement) aux paramètres « Modèle de tracking uniquement » dans la section Paramètres de [!DNL ValueTrack] disponibles dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] uniquement) Utilisez le `!{unescapedurl}` de paramètre pour indiquer l’URL de la page de destination.

   * Vous pouvez éventuellement inclure des paramètres d’URL et tout paramètre personnalisé défini pour la campagne, séparés par des esperluettes (&amp;), tel que `{lpurl}?matchtype={matchtype}&device={device}`.

* Pour les redirections et le suivi tiers, saisissez une valeur .

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

**[!UICONTROL Networks]:** (dans les paramètres de campagne [!DNL Google Ads] et [!DNL Yandex]) Les réseaux sur lesquels placer les annonces :

* *[!UICONTROL Search]:* Pour placer des enchères pour les annonces de recherche sponsorisée.

  ([!DNL Google Ads] des campagnes) Pour inclure des enchères sur des annonces de partenaires de recherche [!DNL Google Ads], cochez la case en regard de **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* pour placer des offres pour des emplacements sur des listes réseau de contenu (affichage). **Remarque :** vous ne pouvez pas créer d&#39;emplacements à l&#39;aide du modèle. Lorsque vous sélectionnez cette option, créez des emplacements pour chaque groupe publicitaire et spécifiez les pages du réseau d’affichage à cibler pour chaque groupe publicitaire à l’aide de feuilles d’envoi groupé <!-- insert link --> ou des paramètres de groupe publicitaire et d’emplacement <!-- insert links --> dans les vues [!UICONTROL Search] > [!UICONTROL Campaigns].

**[!UICONTROL Languages]:** ([!DNL Google Ads] les réseaux de recherche et d’affichage uniquement) Une ou plusieurs langues cibles pour les publicités de la campagne.

[!DNL Google Ads] détermine la langue d’un utilisateur à partir de son paramètre de langue [!DNL Google] ou de la langue de la requête de recherche, de la page active ou des pages récemment consultées sur le [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]:**(Campagnes [!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement ; applicable aux campagnes qui ciblent des audiences dans l’Union européenne (UE)) Que la campagne contienne ou non de la publicité politique selon les exigences pour les publicités diffusées dans l’Union européenne en vertu du règlement 2024/90 de l’UE : *[!UICONTROL Yes]* ou *[!UICONTROL No]*.

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Comptes avec URL finales/avancées uniquement) Modèle de suivi au niveau du groupe publicitaire, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de l’atterrissage et incorpore l’URL finale dans un paramètre.

Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

Pour les redirections et le suivi tiers, saisissez une valeur . Pour indiquer l’URL de la page de destination :

* Pour Yahoo ! Comptes Japan Ads, utilisez le paramètre {lpurl}.

* Pour connaître les paramètres disponibles pour les comptes Microsoft Advertising et Google Ads, consultez la [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou les paramètres du « Modèle de suivi uniquement » dans la section sur les « Paramètres de [!DNL ValueTrack] disponibles » dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

Cette valeur remplace les paramètres au niveau du compte et de la campagne, mais les modèles de suivi à des niveaux plus granulaires (avec le mot-clé comme plus granulaire) remplacent cette valeur.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Mots-clés pour le groupe publicitaire spécifié (ou la campagne pour les comptes [!DNL Yandex]), qui peut consister en n’importe quelle combinaison de texte statique, de colonnes du fichier spécifié et de modificateurs. Les noms de colonne et les modificateurs sont remplacés par des données réelles lorsque le fichier de flux spécifié se propage dans le modèle.

Pour insérer un nom de colonne ou un groupe de modificateurs en tant que paramètre dynamique, cliquez dans le champ de saisie, puis cliquez sur un nom de colonne dans la liste Colonne ou sur un [nom de modificateur](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) dans la liste Modificateurs. Pour spécifier plusieurs mots-clés ou plusieurs types de correspondance pour le même mot-clé, saisissez-les sur des lignes distinctes. Pour spécifier le type de correspondance de mot-clé, utilisez la syntaxe de type de correspondance suivante autour du nom de la colonne :

* Pour les modèles [!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Yahoo! Japan Ads] :

   * Pour les paramètres dynamiques : Correspondance large = `[keyword]`, Modificateur de correspondance large pour le premier terme de la colonne [!UICONTROL Keyword] (tel que +chaussures en daim bleu) = `+[keyword]`, Modificateur de correspondance large pour chaque terme de la colonne Mot-clé (tel que +bleu +daim +chaussures) = `+[keyword]+`, Correspondance d’expression = `"[keyword]"`, Correspondance exacte = `[[keyword]]`

   * Pour les mots-clés statiques : correspondance large = `keyword`, modificateur de correspondance large = `+keyword` ou correspondance d’expression = `"keyword"`

     Vous ne pouvez pas saisir de mots-clés statiques avec une correspondance exacte et une syntaxe de correspondance standard ici, car ils sont entourés de crochets (`[]`), comme le sont les paramètres dynamiques.

* Pour les modèles [!DNL Yandex] :

   * Pour les paramètres dynamiques : insérez le nom de la colonne, par exemple `[keyword]`. Pour indiquer le type de correspondance, utilisez la syntaxe spécifique au [[!DNL Yandex]](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Remarque :** pour les termes à correspondance large, utilisez la syntaxe suivante : Modificateur de correspondance large pour le premier terme de la colonne Mot-clé (tel que +chaussures bleu en daim) = `+[keyword]`, Modificateur de correspondance large pour chaque terme de la colonne Mot-clé (tel que +bleu +daim +chaussures) = `+[keyword]+`

   * Pour les mots-clés statiques : seuls les mots-clés de recherche sont pris en charge. Utilisez la syntaxe spécifique au [[!DNL Yandex]](https://yandex.com/support/direct/keywords/symbols-and-operators.html) pour le mot-clé . Les crochets (`[]`) pour indiquer l’ordre des mots ne sont pas pris en charge.

>[!NOTE]
>
>* Vous pouvez inclure manuellement plusieurs valeurs de modificateur dans le champ Mots-clés en plaçant les valeurs séparées par des virgules entre parenthèses avant ou après un paramètre de mot-clé (mais pas aux deux endroits). Par exemple, `(cheap, discount, affordable)[product]` produit trois annonces distinctes pour chaque produit.
>* Si vous ne spécifiez pas de type de correspondance, le type de correspondance par défaut « broad » est utilisé.
>* Les correspondances négatives ne sont pas prises en charge.
>* les modificateurs de correspondance large Google ont désormais le même comportement de correspondance que la correspondance d’expression pour certaines langues. Vous ne pouvez pas créer de nouveaux mots-clés de modificateur de correspondance large. Pour plus d’informations, consultez la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/10286719).

**[!UICONTROL Map Only]:** ajoute toutes les nouvelles annonces aux groupes publicitaires (ou aux campagnes pour les comptes [!DNL Yandex]) dans lesquels se trouvent les mots-clés spécifiés, plutôt que de créer de nouveaux mots-clés. Pour activer cette option, cochez la case. Lorsque cette option est activée, les variables Param 1 et Param 2 dans les mots-clés spécifiés ne s’appliquent pas, car les mots-clés existent.

**[!UICONTROL Keyword Final URL]:** (Comptes avec URL finales/avancées ; facultatif) URL de la page de destination vers laquelle les utilisateurs du réseau publicitaire sont redirigés lorsqu’ils cliquent sur votre publicité. Il doit inclure le même domaine que l’URL d’affichage et tous les paramètres de l’URL finale doivent correspondre aux paramètres de l’URL de la page de destination après le clic sur l’annonce. Il peut contenir des redirections dans le domaine ou le sous-domaine de la page de destination, mais aucune redirection en dehors du domaine de la page de destination.

Si vous utilisez un flux de [!DNL Google Merchant Center] et incluez cette valeur dans la colonne « [!DNL Link] », insérez cette colonne dans ce champ.

>[!NOTE]
>
>* Si vous générez des URL de tracking lors de la publication de données propagées par le modèle, des paramètres de tracking sont ajoutés à cette valeur en fonction des paramètres de tracking du compte.
>* (Comptes [!DNL Google Ads]) Évitez d’utiliser des macros qui ne remplacent pas les clics provenant de sources permettant le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte Adobe doit collaborer avec le service clientèle ou l’équipe d’implémentation pour les ajouter.

**[!UICONTROL Keyword Tracking Template]:** (Comptes avec URL finales/avancées ; facultatif) Modèle de tracking, qui spécifie toutes les redirections de domaine et tous les paramètres de tracking hors atterrissage et incorpore l’URL finale dans un paramètre. Le modèle de suivi au niveau le plus granulaire (avec le mot-clé comme plus granulaire) remplace les valeurs à tous les autres niveaux.

* Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Vous pouvez éventuellement saisir des redirections et un suivi tiers.

* Pour indiquer l’URL de la page de destination :

   * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Pour obtenir une liste de paramètres indiquant les URL finales dans les modèles de tracking, reportez-vous à la [!DNL Microsoft Advertising]documentation[[!DNL Microsoft Advertising]  (](https://help.ads.microsoft.com/#apex/3/en/56799) uniquement) ou ([!DNL Google Ads] uniquement) aux paramètres « Modèle de tracking uniquement » dans la section Paramètres de [!DNL ValueTrack] disponibles dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] uniquement) Utilisez le `!{lpurl}` de paramètre pour indiquer l’URL de la page de destination.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] modèles\]:** (modèles [!DNL Google Ads] uniquement) La colonne du fichier spécifié qui représente la variable [!DNL Google Ads] ou `{param1}` de `{param2}`, que vous pouvez inclure dans la copie de l’annonce ou l’URL d’affichage pour toute annonce créée à partir du modèle. Pour insérer le paramètre dynamique, cliquez dans le champ de saisie, puis cliquez sur le nom d&#39;une colonne dans la liste des colonnes. Le nom de la colonne est remplacé par les données réelles lorsque le fichier de flux se propage dans le modèle.

Si vous utilisez l’un de ces paramètres, vous avez la possibilité d’appliquer uniquement le paramètre aux nouveaux mots-clés ou de mettre également à jour les valeurs des mots-clés existants qui n’ont pas été créés à partir du modèle :

* **[!UICONTROL Do Not Apply to Existing Keywords]** (valeur par défaut) : insère simplement la valeur du paramètre pour les nouveaux mots-clés créés à l’aide du modèle.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** En plus de la création de mots-clés à partir du flux, Search, Social et Commerce met également à jour la valeur du paramètre pour tous les mots-clés existants du groupe publicitaire qui n’ont pas été créés à l’aide du modèle. Saisissez une valeur numérique unique utilisée pour tous ces mots-clés. Le modèle doit contenir au moins un mot-clé.

* **[!UICONTROL Apply to Existing Keywords: Min]:** En plus de la création de mots-clés à partir du flux, Search, Social et Commerce met également à jour la valeur du paramètre pour tous les mots-clés existants du groupe publicitaire qui n’ont pas été créés à l’aide du modèle, à condition que le fichier de flux contienne des valeurs numériques pour le paramètre, avec jusqu’à une décimale, mais sans virgules, symboles ou codes de devise, ou autres caractères. La valeur minimale du paramètre dans le fichier de flux est utilisée pour tous les mots-clés existants. Par exemple, si le fichier de flux possède [!UICONTROL Param1] valeurs de 21500 et 22000, les valeurs [!UICONTROL Param1] des mots-clés existants sont remplacées par 21500. Le modèle doit contenir au moins un mot-clé. **Conseil :** utilisez cette option uniquement lorsque vous disposez de groupes publicitaires avec un thème précis, de sorte qu’il soit logique que les mots-clés aient la même valeur.

Les champs de données du fichier de flux peuvent contenir au maximum 25 caractères et peuvent uniquement consister en des données numériques avec les caractères non numériques suivants :

* (Lorsque vous utilisez le paramètre « [!UICONTROL Apply to Existing Keywords: Min] ») Jusqu’à une décimale seulement.

* (Lorsque vous n’utilisez pas le paramètre « [!UICONTROL Apply to Existing Keywords: Min] ») :

   * La valeur peut être précédée ou ajoutée d’un symbole ou code de devise. Par exemple, 2 000 £ et 2000GBP sont valides.

   * La valeur peut inclure une virgule (,) ou un point (.) comme séparateur, avec un point facultatif (.) ou une virgule (,) pour les valeurs fractionnaires. Par exemple, 1 000,00 et 2 000,10 sont valides.

   * La valeur peut être précédée ou ajoutée d’un signe de pourcentage (%), de plus (+) ou de moins (-). Par exemple, 20 %, 208+ et -42,32 sont valides.

   * Deux nombres peuvent être incorporés avec une barre oblique. Par exemple, 4/1 et 0,95/0,45 sont valides.

**[!UICONTROL Param 2]\[modèles [!DNL Microsoft Advertising]\]:** (modèles [!DNL Microsoft Advertising] uniquement) Chaîne à utiliser comme valeur de substitution dans une publicité si le titre, le texte, l’URL d’affichage ou l’URL finale contient la chaîne de substitution dynamique `{Param2}`. La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments publicitaires dans lesquels vous l’utilisez (par exemple, un titre d’annonce peut contenir jusqu’à 25 caractères).

**[!UICONTROL Param 3]:** (modèles de [!DNL Microsoft Advertising] uniquement) Chaîne à utiliser comme valeur de substitution dans une publicité si le titre, le texte, l’URL d’affichage ou l’URL finale contient la chaîne de substitution dynamique `{Param3}`. La longueur maximale est de 70 caractères, mais gardez à l’esprit la longueur maximale des éléments publicitaires dans lesquels vous l’utilisez (par exemple, un titre d’annonce peut contenir jusqu’à 25 caractères).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** enchère initiale pour chaque mot-clé avec le type de correspondance ou le type d’annonce spécifié.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** (campagnes [!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Type d’annonces : *[!UICONTROL Expanded Search Ads]* ou *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (facultatif) préremplit tous les autres champs de copie publicitaire avec du texte des champs de copie publicitaire d’origine.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Annonces de recherche réactives uniquement) Position de l’annonce à laquelle le titre doit être inclus (par exemple, « [!UICONTROL Pinned at position 1] »). La valeur par défaut est [!UICONTROL Unpinned].

Au moins un titre doit être disponible pour chaque poste. Si vous épinglez plusieurs titres à la même position, la publicité finale inclut toujours l’un de ces titres à la position spécifiée. Les titres épinglés en position 3 peuvent ne pas être affichés avec la publicité.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (annonces responsive sur le Réseau de Recherche uniquement) Titres des annonces (titres). Chaque variation de publicité doit inclure au moins trois titres de publicité et jusqu’à 15. Le réseau publicitaire affiche des publicités avec jusqu’à trois titres. La longueur maximale de chaque titre est de 30 caractères, y compris tout texte dynamique (valeurs des mots-clés et personnalisateurs d’annonces, par exemple).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (annonces textuelles Microsoft Advertising standard existantes uniquement ; lecture seule) Titre, ou première ligne, d’une annonce. Microsoft Advertising a rendu obsolètes la création et la modification de publicités textuelles standard.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** (modèles d’annonces textuelles [!DNL Google Ads] et [!DNL Yahoo! Japan Ads] développés/étendus uniquement) Titre d’une annonce. La longueur maximale de chaque ligne (après remplacement des paramètres dynamiques) est de 30 caractères ou 15 caractères codés sur deux octets.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] modèles d’annonce texte développés uniquement ; facultatif) Troisième titre d’une annonce. La longueur maximale (après remplacement des paramètres dynamiques) est de 30 caractères ou 15 caractères codés sur deux octets.

**[!UICONTROL Title]:** ([!DNL Yandex] uniquement) Titre ou première ligne d’une annonce publicitaire. La longueur maximale est de 33 caractères.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (annonces en texte développé Microsoft Advertising uniquement) Titre d’une annonce. La longueur maximale de chaque ligne (après remplacement des paramètres dynamiques) est de 30 caractères ou 15 caractères codés sur deux octets.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (annonces en texte développé Microsoft Advertising uniquement) Corps d’une annonce. La longueur maximale (après remplacement des paramètres dynamiques) est de 80 caractères ou 40 caractères codés sur deux octets (chinois, japonais et coréen, par exemple).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** Le corps de la publicité.

* (Modèles d’annonce de texte développé Google Ads) La longueur maximale (après remplacement des paramètres dynamiques) est de 90 caractères ou 45 caractères codés sur deux octets.

* (Yahoo ! Modèles Japan Ads) La longueur maximale (après remplacement des paramètres dynamiques) est de 80 caractères ou 40 caractères codés sur deux octets.

* (Modèles Yandex) La longueur maximale (après remplacement des paramètres dynamiques) est de 75 caractères et un seul mot ne peut pas dépasser 22 caractères.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Annonces de recherche réactives uniquement) Position de l’annonce à laquelle la description doit être incluse (par exemple, « [!UICONTROL Pinned at position 1] »). La valeur par défaut est [!UICONTROL Unpinned]. Au moins une description doit être disponible pour chaque poste.

Si vous épinglez plusieurs descriptions à la même position, la publicité finale inclut toujours une de ces descriptions à la position spécifiée. Les descriptions épinglées en position 2 peuvent ne pas être affichées avec la publicité.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (Annonces de recherche réactives uniquement) Descriptions de l’annonce. Chaque variation d’annonce publicitaire doit inclure au moins deux descriptions d’annonce publicitaire et un maximum de quatre. Le réseau publicitaire affiche des publicités avec jusqu’à deux descriptions ; saisissez au moins deux descriptions. La longueur maximale de chaque description est de 90 caractères, y compris tout texte dynamique (valeurs des mots-clés et personnalisateurs d’annonces, par exemple).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (modèles d’annonce publicitaire texte développé Google uniquement ; facultatif) Deuxième ligne de l’annonce. La longueur maximale (après remplacement des paramètres dynamiques) est de 90 caractères ou 45 caractères codés sur deux octets.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (texte développé et annonces responsive sur le Réseau de Recherche uniquement ; facultatif) Un ou deux chemins d’accès à l’URL à inclure consécutivement après l’URL de base. Ils doivent décrire plus en détail le produit ou le service de la publicité. Par exemple, si vous ajoutez une [!UICONTROL Display Path 1] de « Chaussures » et une [!UICONTROL Display Path 2] de « Extérieur » à l’URL de base www.example.com, l’URL est www.example.com/Shoes/Outdoor. La longueur maximale (après remplacement des paramètres dynamiques) pour chaque champ est de 15 caractères ou 7 caractères codés sur deux octets.

Pour les annonces responsive sur le Réseau de Recherche, insérez un personnalisateur d’annonce publicitaire à l’aide des formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas une valeur valide :

* [!DNL Google Ads] : `{CUSTOMIZER.AdCustomizerName:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising] : `{CUSTOMIZER.Attribute name:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (annonces de texte standard [!DNL Microsoft Advertising] et [!DNL Yahoo! Japan Ads] existantes uniquement ; lecture seule) URL affichée dans une annonce.

[!DNL Microsoft Advertising] et [!DNL Yahoo! Japan Ads] ont rendu obsolètes la création et la modification d’annonces de texte standard.

**[!UICONTROL Base URL]:** (Comptes avec URL de destination uniquement) Page vers laquelle les utilisateurs sont redirigés. Il peut inclure du code de redirection et de suivi tiers. Si vous utilisez le service de suivi des conversions d’Adobe Advertising et que les paramètres de la campagne incluent l’utilisation du [!UICONTROL EF Redirect] et l’ajout du suivi au niveau de la publicité, Search, Social et Commerce ajoute automatiquement sa propre redirection et son propre code de suivi à la publicité.

Pour insérer un nom de colonne ou un groupe de modificateurs en tant que paramètre dynamique, cliquez dans le champ de saisie, puis cliquez sur un nom de colonne dans la liste des colonnes ou sur un [nom de modificateur](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) dans la liste des [!UICONTROL Modifiers].

**[!UICONTROL Final URL]:** (comptes avec URL finales/avancées) URL de la page de destination vers laquelle les utilisateurs sont redirigés lorsqu’ils cliquent sur votre annonce. Il doit inclure le même domaine que l’URL d’affichage et tous les paramètres de l’URL finale doivent correspondre aux paramètres de l’URL de la page de destination après le clic sur l’annonce. Il peut contenir des redirections dans le domaine ou le sous-domaine de la page de destination, mais aucune redirection en dehors du domaine de la page de destination.

Si vous utilisez un flux [!DNL Google Merchant] Center et incluez cette valeur dans la colonne « [!UICONTROL Link] », insérez cette colonne dans ce champ.

>[!NOTE]
>
>* Si vous générez des URL de tracking lors de la publication de données propagées par le modèle, des paramètres de tracking sont ajoutés à cette valeur en fonction des paramètres de tracking du compte.
>* (Comptes [!DNL Google Ads] ) Évitez d’utiliser des macros qui ne remplacent pas les clics provenant de sources permettant le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte Adobe doit collaborer avec le service clientèle ou l’équipe d’implémentation pour les ajouter.

**[!UICONTROL Tracking Template]:** (Comptes avec URL finales/avancées ; facultatif) Modèle de tracking, qui spécifie toutes les redirections de domaine et tous les paramètres de tracking hors atterrissage et incorpore l’URL finale dans un paramètre. Le modèle de suivi au niveau le plus granulaire (avec le mot-clé comme plus granulaire) remplace les valeurs à tous les autres niveaux.

Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement le code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

Pour les redirections et le suivi tiers, saisissez une valeur . Pour indiquer l’URL de la page de destination :

* Pour Yahoo ! Comptes Japan Ads, utilisez le paramètre {lpurl}.

* Pour connaître les paramètres disponibles pour les comptes Microsoft Advertising et Google Ads, consultez la [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou les paramètres du « Modèle de suivi uniquement » dans la section sur les « Paramètres de [!DNL ValueTrack] disponibles » dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

**\[Autres champs d’annonce publicitaire sous les champs d’annonce publicitaire d’origine\]:** (facultatif) Ensemble alternatif de copies d’annonce publicitaire pour une annonce publicitaire, qui peut être utilisé si l’une des lignes de la copie d’annonce d’origine dépasse la longueur maximale autorisée une fois que les paramètres dynamiques sont remplis de données pendant la propagation.

>[!NOTE]
>
>* Si l’option [!UICONTROL Prefill] est sélectionnée, les champs secondaires sont préremplis avec les champs d’origine et vous pouvez les modifier si nécessaire.
>* Seuls les champs de la copie publicitaire qui dépassent la longueur maximale sont remplacés par la valeur alternative. Par exemple, si seul un titre ou un titre d’origine est trop long, la variation publicitaire générée utilise le titre ou le titre secondaire et les descriptions d’origine. Par conséquent, assurez-vous que la copie alternative de l’annonce publicitaire a du sens lorsqu’elle est combinée avec la copie originale de l’annonce.
>* Si la copie de l’annonce originale répond aux exigences de longueur du moteur de recherche, la copie de l’annonce alternative est ignorée.

**\[Composant\] [!UICONTROL Ad Label Classifications] > \[Classification et valeur de libellé\]:** (facultatif) Valeurs pour un maximum de cinq classifications de libellé existantes à affecter aux variations d’annonces créées ou modifiées à l’aide du modèle. Pour chaque composant de campagne auquel vous souhaitez affecter des classifications de libellés :

1. Cochez la case.

1. Configurez les valeurs de classification de libellé pour le modèle de variation publicitaire :

   * Pour chaque classification de libellé et valeur à affecter au composant, procédez comme suit :

      1. Cliquez sur **[!UICONTROL Add Label Classification]**.

      1. Sélectionnez la classification d’étiquettes existante, puis sélectionnez une valeur existante ou saisissez-en une nouvelle.

         La longueur maximale de chaque valeur est de 100 caractères et peut inclure des caractères ASCII et non ASCII.

         Pour insérer un nom de colonne en tant que paramètre dynamique pour une valeur de classification d&#39;étiquette, cliquez dans le champ de saisie (deuxième champ), puis cliquez sur un nom de colonne dans la liste des colonnes.

         Vous ne pouvez inclure qu’une seule valeur par classification par composant de campagne. Par exemple, une campagne peut avoir Color=Red mais pas Color=Red et Color=Blue.

         * Pour modifier une valeur de classification de libellé existante, sélectionnez ou saisissez une nouvelle valeur.

         * Pour supprimer une valeur de classification de libellé existante, cliquez sur **[!UICONTROL X]** en regard de la valeur.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [À propos de l’automatisation de la gestion des annonces à l’aide des flux d’inventaire](../inventory-feeds-about.md)
>* [Gestion des modificateurs](../modifiers-manage.md)
>* [Gestion des fichiers de flux de données d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Propager les données de flux par le biais de modèles](../feed-data-propagate.md)
>* [Publier les données de campagne des flux d’inventaire dans les réseaux publicitaires](../propagated-data-post.md)
