---
title: Paramètres des expériences non ciblées
description: Voir les descriptions de tous les paramètres pour les expériences publicitaires sans ciblage d’arborescence de décision.
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: e070e676b9ae321ddc73acfff0dfc05ea91f9715
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 0%

---

# Paramètres des expériences non ciblées

*Version bêta fermée*

## section [!UICONTROL Experience basics]

**[!UICONTROL Advertiser]:** (Lecture seule pour les expériences existantes) L’annonceur qui enchérira sur les contenus publicitaires inclus dans l’expérience. Une fois l’expérience enregistrée, vous ne pouvez plus modifier l’annonceur.

**[!UICONTROL Experience Name]:** nom unique de l’expérience. **Conseil :** utilisez un nom que vous pouvez facilement retrouver lorsque vous utilisez l’expérience comme publicité dans Advertising DSP ou d’autres DSP.

**[!UICONTROL Creative Library]:** (Lecture seule pour les expériences existantes) Bibliothèque de contenu créatif unique à utiliser pour l’expérience. Une fois l’expérience enregistrée, vous ne pouvez plus modifier la bibliothèque.

## section [!UICONTROL Default creatives]

**\[Contenu publicitaire par défaut spécifié\] :** contenu publicitaire d’image par défaut à utiliser lorsqu’un navigateur ne peut pas afficher les contenus publicitaires affectés à l’expérience, par exemple lorsque le navigateur n’est pas activé pour JavaScript ou que le serveur de publicités ne peut pas personnaliser l’annonce en raison de retards. Incluez une image créative par taille d’annonce pour laquelle l’expérience s’applique. Vos choix déterminent les tailles de contenu créatif qui peuvent être utilisées pour l’expérience. <!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

Pour les expériences sans ciblage d’arborescence de décision, vous pouvez remplacer les contenus publicitaires par défaut par des contenus publicitaires de même taille dans [!UICONTROL Tag Manager].

* Pour ajouter un élément créatif par défaut avec différentes dimensions, cliquez sur **[!UICONTROL + Add Sizes]**, cochez la case en regard de chaque élément créatif à ajouter dans le volet de droite, puis cliquez sur **[!UICONTROL Add Creatives]**.

* Pour supprimer un élément créatif par défaut, maintenez le curseur sur la miniature de l’élément créatif et cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer").

* Pour supprimer tous les contenus publicitaires par défaut, cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer") **[!UICONTROL Delete all]**.

* Pour afficher ou masquer le volet Contenu publicitaire à droite, cliquez sur ![Afficher/Masquer](/help/creative/assets/hide-show-creatives.png "Afficher/Masquer") dans le coin supérieur droit du volet de droite.

## section [!UICONTROL Targeting]

**[!UICONTROL Targeting]:** (lecture seule pour les expériences existantes) Non applicable lorsque vous n’activez pas le ciblage à l’aide d’une arborescence de décision ; gardez cette option désactivée. **Remarque :** une fois que vous avez enregistré une expérience sans ciblage, vous ne pouvez plus ajouter de ciblage.

**[!UICONTROL Dynamic ads]:** (Lecture seule pour les expériences existantes) Indique que l’expérience comprend des annonces dynamiques. **Remarque :** une expérience peut inclure toutes les publicités standard ou toutes les publicités dynamiques.

**[!UICONTROL Language Targeting]:** (Expériences avec des annonces standard uniquement ; facultatif ; lecture seule pour les expériences existantes) Vérifie les paramètres de langue du navigateur de l’utilisateur et affiche un élément créatif dans la langue spécifiée lorsqu’un élément créatif dans cette langue est disponible. Lorsqu’une création dans la langue spécifiée par le navigateur n’est pas disponible, le paramètre [!UICONTROL Preferred language] est utilisé à la place. Une fois l’expérience enregistrée, vous ne pouvez plus modifier ce paramètre.

**[!UICONTROL Preferred language]:** (Expériences avec des annonces standard uniquement ; lecture seule pour les expériences existantes) Langue de toutes les annonces créées à partir de l’expérience, sauf lorsque [!UICONTROL Language Targeting] est activé. Une fois l’expérience enregistrée, vous ne pouvez plus modifier ce paramètre.

## section [!UICONTROL Advanced]

**Transmission de données :** (expériences avec des annonces dynamiques uniquement ; facultatif) pour cibler les utilisateurs en fonction de paires clé-valeur spécifiques que le DSP, l’éditeur ou le partenaire transmet en temps réel à l’impression. Vous pouvez spécifier jusqu’à cinq clés de transmission de données (paramètres).<!-- May move this to just within the decision tree. -->

Lorsque vous créez une balise d’expérience publicitaire pour une taille de contenu créatif spécifique, chaque clé spécifiée dans ce champ est ajoutée sous la forme d’une macro dans la balise . Saisissez la valeur de chaque paire clé-valeur dans la balise avant d’implémenter la balise en tant qu’annonce publicitaire dans votre DSP.

**Rayon :** (Expériences avec les annonces dynamiques uniquement ; facultatif) Rayon d’un code postal des États-Unis spécifié dans le fichier de flux à cibler ; sélectionnez un rayon compris entre 0 et 200 miles. Le fichier de flux utilisé pour créer les annonces dynamiques pour l’expérience doit inclure une colonne [!UICONTROL ZIP]<!-- or a user-named column mapped to a ZIP column --> avec une valeur pour chaque ligne de produit dans le fichier. Par exemple, pour un rayon de 10 miles, une annonce publicitaire pour un produit disponible en 95110 peut être affichée pour les utilisateurs dans un rayon de 10 miles (déterminé par l’adresse IP de l’utilisateur) 95110.

**Pixel RT :** (expériences avec des annonces dynamiques uniquement ; facultatif) pixel de reciblage [!UICONTROL Creative] à cibler potentiellement. Lorsque vous configurez le ciblage dans l’arborescence de décision, vous pouvez inclure un niveau de nœuds cibles de pixels RT. Pour chaque nœud, vous spécifiez le pixel à cibler et les valeurs des attributs de pixel requis pour afficher les contenus publicitaires dans les lots de contenus publicitaires attribués. Si vous ne spécifiez pas de pixel dans ce champ, vous pouvez toujours en spécifier un dans l’arborescence de décision.<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup." Clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]:**<!-- should be "Labels" --> (facultatif) libellés spécifiques à l’[!DNL Creative] à appliquer à l’expérience. Vous pouvez filtrer les expériences par libellé dans la vue Expériences <!-- sic --> .

* Pour sélectionner des libellés existants, cliquez sur ![Bas](/help/creative/assets/chevron-down.png "Bas"), puis cochez la case en regard de chaque libellé à appliquer.

* Pour rechercher des libellés existants, commencez à saisir une chaîne de texte dans le nom du libellé.

* Pour créer une nouvelle étiquette à appliquer, ouvrez la liste, cliquez sur **+ Ajouter une étiquette**, saisissez un nouveau nom d&#39;étiquette dans le champ [!UICONTROL Label], puis cliquez sur **Créer**.

* Pour supprimer un libellé, décochez la case en regard du nom du libellé.

**[!UICONTROL Impression Tracking URL]:** (facultatif) URL de suivi d’impression tierce à ajouter à l’URL de la page de destination pour toute publicité créée à partir de l’expérience. Vous pouvez inclure jusqu’à cinq URL. Pour ajouter une URL supplémentaire, cliquez sur ![icône](/help/creative/assets/create.png) **[!UICONTROL Add More] et saisissez l’URL.

Une fois que vous avez saisi une URL, toutes les [macros disponibles](/help/creative/creative-macros.md) ainsi que les données auxquelles elles sont remplacées sont répertoriées plus bas dans la page. Pour insérer l&#39;une des macros dans l&#39;URL, placez le curseur sur la description de la macro et cliquez sur ![Copier dans le presse-papiers](/help/creative/assets/copy-to-clipboard.png "Copier dans le presse-papiers"), puis collez la macro où vous le souhaitez dans le champ URL.

>[!NOTE]
>
>* [!DNL Creative] préfixe automatiquement ses propres balises de suivi des impressions sur l’URL de la page de destination.
>* Vous pouvez remplacer cette URL pour tout contenu créatif de l’expérience.
>* Vous pouvez également saisir le code de suivi d’impression JavaScript tiers dans le champ [!UICONTROL Client JS] .

**[!UICONTROL Click Tracking URL]:** (facultatif) URL de suivi des clics tierce à ajouter à l’URL de la page de destination. Vous pouvez inclure jusqu’à cinq URL. Pour ajouter une URL supplémentaire, cliquez sur ![icône](/help/creative/assets/create.png) **[!UICONTROL Add More]** et saisissez l’URL.

Une fois que vous avez saisi une URL, toutes les [macros disponibles](/help/creative/creative-macros.md) ainsi que les données auxquelles elles sont remplacées sont répertoriées plus bas dans la page. Pour insérer l&#39;une des macros dans l&#39;URL, placez le curseur sur la description de la macro et cliquez sur ![Copier dans le presse-papiers](/help/creative/assets/copy-to-clipboard.png "Copier dans le presse-papiers"), puis collez la macro où vous le souhaitez dans le champ URL.

>[!NOTE]
>
>* [!DNL Creative] préfixe automatiquement ses propres balises de suivi des impressions sur l’URL de la page de destination.
>* Vous pouvez remplacer cette URL pour toutes les <!-- creative bundle for targeted experiences --> créatives de l’expérience.

**[!UICONTROL Client JS]:** (facultatif) L’un des éléments suivants :

* (Lorsque l’annonceur fait appel à un fournisseur de conformité OBA pour les publicités) Code JavaScript pointant vers la superposition de publicité qui permet aux utilisateurs de se désabonner du ciblage comportemental en ligne (OBA).

* Tout code de suivi d’impression JavaScript tiers à ajouter à la page de destination. **Remarque :** vous pouvez également saisir une URL de suivi d’impression tierce dans le champ [!UICONTROL Impression Tracking URL] .

>[!MORELIKETHIS]
>
>* [Création d’une expérience sans ciblage d’arborescence de décision](experience-create-no-targeting.md)
>* [Modification d’une expérience sans ciblage d’arbre de décision](experience-edit-no-targeting.md)
>* [Macros disponibles pour le tracking des URL](/help/creative/creative-macros.md)
>* [Créez manuellement une balise d’annonce publicitaire pour une taille de contenu créatif applicable](experience-tag-create-manually.md)
>* [Affecter des contenus publicitaires à une balise publicitaire pour des expériences sans ciblage](experience-tag-assign-creatives.md)
>* [Personnaliser les URL de tracking pour une expérience sans ciblage](experience-tracking-urls-no-targeting.md)
>* [Personnaliser l’optimisation créative et la planification d’une expérience sans ciblage](experience-optimization-scheduling-no-targeting.md)
