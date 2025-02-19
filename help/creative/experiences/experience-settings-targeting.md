---
title: Paramètres de l’expérience ciblée
description: Voir les descriptions de tous les paramètres pour les expériences publicitaires ciblées.
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
source-git-commit: 75ecbf5309c21952fb4355be852f80100aa916ae
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 0%

---

# Paramètres d’expérience publicitaire ciblée

*Version bêta fermée*

## section [!UICONTROL Experience basics]

**[!UICONTROL Advertiser]:** (Lecture seule pour les expériences existantes) L’annonceur qui enchérira sur les combinaisons créatives et cibles incluses dans l’expérience. Une fois l’expérience enregistrée, vous ne pouvez plus modifier l’annonceur.

**[!UICONTROL Experience Name]:** nom unique de l’expérience. **Conseil :** utilisez un nom qui sera facile à trouver lorsque vous utiliserez l’expérience en tant qu’annonce dans Advertising DSP ou un autre DSP.

**[!UICONTROL Creative Library]:** (Lecture seule pour les expériences existantes) Bibliothèque de contenu créatif unique à utiliser pour l’expérience. Une fois l’expérience enregistrée, vous ne pouvez plus modifier la bibliothèque.

## section [!UICONTROL Default creatives]

**\[Contenu publicitaire par défaut spécifié\] :** contenu publicitaire d’image par défaut à utiliser lorsqu’un navigateur ne peut pas afficher les contenus publicitaires affectés à l’expérience, par exemple lorsque le navigateur n’est pas activé pour JavaScript ou que le serveur de publicités ne peut pas personnaliser l’annonce en raison de retards. Incluez une image créative par taille d’annonce pour laquelle l’expérience s’applique. Vos choix déterminent les tailles de contenu créatif qui peuvent être utilisées pour l’expérience.<!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. This feels a little wonky in that there isn't a distinct/obvious "Creative Sizes" setting to reference. -->

Pour les expériences avec le ciblage de l’arborescence de décision, vous pouvez remplacer les contenus publicitaires par défaut par des lots de contenus publicitaires qui contiennent des contenus publicitaires de la même taille depuis l’arborescence de décision<!-- verify -->

* Pour ajouter un élément créatif par défaut avec différentes dimensions, cliquez sur **[!UICONTROL + Add Sizes]**, cochez la case en regard de chaque élément créatif à ajouter dans le volet de droite, puis cliquez sur **[!UICONTROL Add Creatives]**.

* Pour supprimer un élément créatif par défaut, maintenez le curseur sur la miniature de l’élément créatif et cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer").

* Pour supprimer tous les contenus publicitaires par défaut, cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer") **[!UICONTROL Delete all]**.

* Pour afficher ou masquer le volet Contenu publicitaire à droite, cliquez sur ![Afficher/Masquer](/help/creative/assets/hide-show-creatives.png "Afficher/Masquer") dans le coin supérieur droit du volet de droite.

## section [!UICONTROL Targeting]

**[!UICONTROL Targeting]:** (Lecture seule pour les expériences existantes) Active le ciblage créatif à l’aide d’une arborescence de décision et de la création automatique de balises. Une fois l’expérience enregistrée, vous ne pouvez plus modifier ce paramètre.

**[!UICONTROL Dynamic ads]:** (Lecture seule pour les expériences existantes) Indique que l’expérience inclut des annonces dynamiques. **Remarque :** une expérience peut inclure toutes les publicités standard ou toutes les publicités dynamiques. Une fois l’expérience enregistrée, vous ne pouvez plus modifier ce paramètre.

**[!UICONTROL Language Targeting]:** (Expériences avec des annonces standard uniquement ; facultatif ; lecture seule pour les expériences existantes) Vérifie les paramètres de langue du navigateur de l’utilisateur et affiche un élément créatif dans la langue spécifiée lorsqu’un élément créatif dans cette langue est disponible. Lorsqu’une création dans la langue spécifiée par le navigateur n’est pas disponible, le paramètre [!UICONTROL Preferred language] est utilisé à la place.

Une fois l’expérience enregistrée, vous ne pouvez plus modifier ce paramètre.

**[!UICONTROL Preferred language]:** (Expériences avec des annonces standard uniquement ; lecture seule pour les expériences existantes) Langue de toutes les annonces créées à partir de l’expérience, sauf lorsque [!UICONTROL Language Targeting] est activé. Une fois l’expérience enregistrée, vous ne pouvez plus modifier ce paramètre.

## section [!UICONTROL Advanced]

**Transmission de données :** (lecture seule pour les expériences existantes, facultatif) pour cibler les utilisateurs en fonction de paires clé-valeur spécifiques que le DSP, l’éditeur ou le partenaire transmet en temps réel à l’impression. Vous pouvez spécifier jusqu’à cinq clés de transmission de données (paramètres). Lorsque vous configurez le ciblage dans l’arborescence de décision, vous pouvez inclure un niveau de données pour transmettre les nœuds cibles et spécifier les valeurs à cibler pour chaque nœud. Si vous ne spécifiez pas de clé dans ce champ lors de la création de l’expérience, vous pouvez toujours en spécifier une dans l’arborescence de décision.<!-- May move this to just within the decision tree.  -->

Chaque clé est ajoutée en tant que macro dans l’expérience publicitaire
, que vous pouvez générer pour implémenter en tant qu’annonce publicitaire dans votre DSP.

**Rayon :** (Expériences avec les annonces dynamiques uniquement ; facultatif) Rayon d’un code postal des États-Unis spécifié dans le fichier de flux à cibler ; sélectionnez un rayon compris entre 0 et 200 miles. Le fichier de flux utilisé pour créer les annonces dynamiques pour l’expérience doit inclure une colonne [!UICONTROL ZIP]<!-- or a user-named column mapped to a ZIP column --> avec une valeur pour chaque ligne de produit dans le fichier. Par exemple, pour un rayon de 10 milles, une annonce publicitaire pour un produit disponible en 95110 peut être affichée aux utilisateurs dans un rayon de 10 milles à partir de 95110.

**Pixel RT :** (lecture seule pour les expériences existantes, facultatif) pixel de reciblage [!UICONTROL Creative] à cibler potentiellement. Lorsque vous configurez le ciblage dans l’arborescence de décision, vous pouvez inclure un niveau de nœuds cibles de pixels RT et spécifier le pixel à cibler pour chaque nœud ainsi que les valeurs requises pour les attributs de pixels qui doivent être présents pour afficher les éléments créatifs dans les lots de création attribués. Si vous ne spécifiez pas de pixel dans ce champ lors de la création de l’expérience, vous pouvez toujours en spécifier un dans l’arborescence de décision.<!-- May move this to just within the decision tree. -->

**Libellé :** <!-- should be "Labels" --> (facultatif) tous les libellés spécifiques aux [!DNL Creative] à appliquer à l’expérience. Vous pouvez filtrer les expériences par libellé dans la vue Expériences <!-- sic --> .

* Pour sélectionner des libellés existants, cliquez sur ![Bas](/help/creative/assets/chevron-down.png "Bas"), puis cochez la case en regard de chaque libellé à appliquer.

* Pour rechercher des libellés existants, commencez à saisir une chaîne de texte dans le nom du libellé.

* Pour créer une nouvelle étiquette à appliquer, ouvrez la liste, cliquez sur **+ Ajouter une étiquette**, saisissez un nouveau nom d&#39;étiquette dans le champ [!UICONTROL Label], puis cliquez sur **Créer**.

* Pour supprimer un libellé, décochez la case en regard du nom du libellé.

**URL de suivi d’impression :** (facultatif) URL de suivi d’impression tierce à ajouter à l’URL de la page de destination pour toute publicité créée à partir de l’expérience. Vous pouvez inclure jusqu’à cinq URL. Pour ajouter une URL supplémentaire, cliquez sur ![icône](/help/creative/assets/create.png) **[!UICONTROL Add More] et saisissez l’URL.

Une fois que vous avez saisi une URL, toutes les [macros disponibles](/help/creative/creative-macros.md) ainsi que les données auxquelles elles sont remplacées sont répertoriées plus bas dans la page. Pour insérer l&#39;une des macros dans l&#39;URL, placez le curseur sur la description de la macro et cliquez sur ![Copier dans le presse-papiers](/help/creative/assets/copy-to-clipboard.png "Copier dans le presse-papiers"), puis collez la macro où vous le souhaitez dans le champ URL.

>[!NOTE]
>
>* [!DNL Creative] préfixe automatiquement ses propres balises de suivi des impressions sur l’URL de la page de destination.
>* Vous pouvez [remplacer cette URL pour tout contenu créatif de l’expérience](experience-tracking-urls-targeting.md).
>* Vous pouvez également saisir le code de suivi d’impression JavaScript tiers dans le champ [!UICONTROL Client JS] .

**URL de suivi des clics :** (facultatif) URL de suivi des clics tierce à ajouter à l’URL de la page de destination. Vous pouvez inclure jusqu’à cinq URL. Pour ajouter une URL supplémentaire, cliquez sur ![icône](/help/creative/assets/create.png) **[!UICONTROL Add More] et saisissez l’URL.

Une fois que vous avez saisi une URL, toutes les [macros disponibles](/help/creative/creative-macros.md) ainsi que les données auxquelles elles sont remplacées sont répertoriées plus bas dans la page. Pour insérer l&#39;une des macros dans l&#39;URL, placez le curseur sur la description de la macro et cliquez sur ![Copier dans le presse-papiers](/help/creative/assets/copy-to-clipboard.png "Copier dans le presse-papiers"), puis collez la macro où vous le souhaitez dans le champ URL.

>[!NOTE]
>
>* [!DNL Creative] préfixe automatiquement ses propres balises de suivi des impressions sur l’URL de la page de destination.
>* Vous pouvez [remplacer cette URL pour tout contenu créatif de l’expérience](experience-tracking-urls-targeting.md).

**Client JS:** (facultatif) L’un des éléments suivants :

* (Lorsque l’annonceur fait appel à un fournisseur de conformité OBA pour les publicités) Code JavaScript pointant vers la superposition de publicité qui permet aux utilisateurs de se désabonner du ciblage comportemental en ligne (OBA).

* Tout code de suivi d’impression JavaScript tiers à ajouter à la page de destination. **Remarque :** vous pouvez également saisir une URL de suivi d’impression tierce dans le champ [!UICONTROL Impression Tracking URL] .

>[!MORELIKETHIS]
>
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Modifier une expérience avec le ciblage d’arborescence de décision](experience-edit-targeting.md)
>* [Macros disponibles pour le tracking des URL](/help/creative/creative-macros.md)
