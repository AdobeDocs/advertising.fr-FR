---
title: Paramètres de création
description: En savoir plus sur xxxx.
feature: Creative Standard Creatives
exl-id: 8eb66310-4860-4ca0-9678-a9e33639c529
source-git-commit: 40a8afc7ec8d880137493118efb122778704eb8c
workflow-type: tm+mt
source-wordcount: '1835'
ht-degree: 0%

---

# Paramètres de création

*Version bêta fermée*

Les paramètres varient selon le type de contenu créatif.

Lorsque vous modifiez plusieurs contenus publicitaires en même temps :

* Vous pouvez modifier les paramètres de chaque élément créatif en même temps ou individuellement. Par défaut, tous les contenus publicitaires sélectionnés sont sélectionnés et les paramètres que vous spécifiez s’appliquent à tous les contenus publicitaires sélectionnés. Pour modifier les paramètres de contenus publicitaires spécifiques, désélectionnez chaque contenu publicitaire inapplicable avant de modifier les champs ; répétez l’opération pour d’autres contenus publicitaires si nécessaire.

* Certains paramètres sont appliqués à tous les contenus publicitaires sélectionnés.

## Paramètres de création HTML5 flexibles {#creative-settings-flexible-html5}

### Onglet Détails

**Nom du contenu publicitaire :** le nom du contenu publicitaire. Le nom du modèle ou le nom du fichier chargé est utilisé par défaut, mais vous pouvez modifier le nom. Pour plusieurs contenus publicitaires, vous pouvez modifier les noms de chaque contenu publicitaire. **Conseil :** incluez la taille de l’annonce publicitaire dans le nom du contenu créatif et utilisez un nom qui sera facile à trouver lorsque vous incluez le contenu créatif dans une expérience.

**Langue :** langue par défaut de chaque publicité à laquelle vous associez les contenus publicitaires. Lorsque vous chargez ou modifiez plusieurs contenus publicitaires, la même valeur est appliquée à chaque contenu publicitaire sélectionné.

**Taille du contenu publicitaire :** (lecture seule pour les contenus publicitaires existants) Dimensions du contenu publicitaire. Si des images incluses dans le contenu créatif sont plus grandes que la taille spécifiée, elles sont redimensionnées en conséquence.

**[!UICONTROL Click Tags]:** variables qui permettent le suivi des clics redirigés depuis les bannières publicitaires incluses. Les noms des variables et les URL de page de destination correspondantes sont renseignés à partir de l’unité de création chargée, mais vous pouvez modifier les URL par défaut. Pour plusieurs contenus publicitaires, vous pouvez modifier les balises de clic individuelles.

<!-- I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**Libellé :** (facultatif) tous les libellés à appliquer à tous les contenus publicitaires sélectionnés. Vous pouvez filtrer les contenus publicitaires par libellé dans différentes vues de [!DNL Creative].

* Pour sélectionner des libellés existants, cliquez sur ![Bas](/help/creative/assets/chevron-down.png "Bas"), puis cochez la case en regard de chaque libellé à appliquer.

* Pour rechercher des libellés existants, commencez à saisir une chaîne de texte dans le nom du libellé.

* Pour créer une nouvelle étiquette à appliquer aux contenus publicitaires, ouvrez la liste, cliquez sur **+ Ajouter une étiquette**, saisissez un nouveau nom d’étiquette dans le champ [!UICONTROL Label], puis cliquez sur **Créer**.

* Pour supprimer un libellé, décochez la case en regard du nom du libellé.

### Onglet Attributs

**\[Tous les attributs de contenu par défaut applicables au contenu créatif\] :** les noms et valeurs d’attribut par défaut sont renseignés à partir de l’entité de création flexible, mais vous pouvez éventuellement modifier les valeurs.

>[!NOTE]
>
>Vous pouvez également remplacer la valeur par défaut de l’un des attributs de contenu créatif par une valeur personnalisée lorsque vous incluez le contenu créatif dans une expérience. La modification des attributs dans une expérience crée une variation du contenu créatif parent.

Pour plus d’informations sur les attributs disponibles dans les modèles prédéfinis, voir « [Modèles créatifs flexibles disponibles](#flexible-creative-templates-available) ».

### Onglet Modèle

*Contenu publicitaire existant uniquement*

Fichier de modèle HTML5 flexible pour les créatifs.

Vous pouvez éventuellement remplacer le modèle existant par un nouveau modèle avec une disposition différente, mais le même ensemble de noms d’attributs que le modèle d’origine. Le nouveau modèle doit être au format ZIP avec un maximum de 2 Mo. Lorsque le contenu créatif se trouve dans un lot, toutes les expériences qui utilisent le lot utiliseront ensuite la mise en page du nouveau modèle.

Lorsque vous mettez à jour le modèle d’un élément créatif parent avec des variations enfant, les variations sont mises à jour avec toutes les modifications apportées à la mise en page du modèle, mais les valeurs d’attribut de la variation ne sont pas modifiées.

Pour remplacer le modèle d’annonce publicitaire existant :

1. Cliquez sur **Mettre à jour le modèle**.

1. Cliquez sur **Continuer**.

1. Spécifiez un fichier ZIP de l’une des manières suivantes :

   * Faites glisser et déposez un fichier sur votre appareil ou réseau dans la zone.

   * Cliquez sur **[!UICONTROL select a file]** pour localiser le fichier sur votre appareil ou réseau.

   Voir [spécifications d’annonces publicitaires flexibles](#flexible-ad-spec).

1. Modifiez les nouveaux [paramètres flexibles des annonces HTML](#flexible-ad-settings) selon les besoins.

1. Clic **[!UICONTROL Edit]**

## Paramètres de création HTML5 {#creative-settings-html5}

## Onglet Détails

Pour les nouveaux créatifs, les paramètres suivants ne se trouvent pas dans un onglet nommé.

**Nom du contenu publicitaire :** le nom du contenu publicitaire. Pour une nouvelle création, le nom du fichier est utilisé par défaut, mais vous pouvez le modifier. Pour plusieurs contenus publicitaires, vous pouvez modifier les noms de chaque contenu publicitaire. **Conseil :** incluez la taille de l’annonce publicitaire dans le nom du contenu créatif et utilisez un nom qui sera facile à trouver lorsque vous incluez le contenu créatif dans une expérience.

**Langue :** langue par défaut de chaque publicité à laquelle vous associez les contenus publicitaires. Lorsque vous chargez ou modifiez plusieurs contenus publicitaires, la même valeur est appliquée à chaque contenu publicitaire sélectionné.

**Taille du contenu publicitaire :** (lecture seule pour les contenus publicitaires existants) Dimensions du contenu publicitaire. Si des images incluses dans le contenu créatif sont plus grandes que la taille spécifiée, elles sont redimensionnées en conséquence.

**[!UICONTROL Click Tags]:** (contenus publicitaires HTML5 statiques uniquement) Variables qui permettent les redirections du suivi des clics à partir des bannières publicitaires incluses. Les noms des variables et les URL de page de destination correspondantes sont renseignés à partir de l’unité de création chargée, mais vous pouvez modifier les URL par défaut. Pour plusieurs contenus publicitaires, vous pouvez modifier les balises de clic individuelles.

>[!NOTE]
>
>Lorsque vous incluez le contenu créatif dans une expérience, vous pouvez remplacer la valeur par défaut de l’une des balises de clic par une URL de page de destination personnalisée afin de générer une dérivation du contenu créatif de base.

**URL de la page de destination :** (contenu publicitaire HTML5 simple avec une seule page de destination) URL de la page de destination par défaut pour chaque publicité à laquelle vous associez les contenus publicitaires. Il doit s’agir d’une URL valide commençant par http:// ou https://. Il peut inclure des paramètres de suivi tiers ou des [[!DNL Creative] macros](/help/creative/creative-macros.md) pour votre propre usage.

Lorsque vous incluez un contenu créatif dans une offre groupée et que vous attribuez l’offre groupée à une expérience, vous pouvez éventuellement modifier l’URL de la page de destination, ainsi qu’ajouter des URL de suivi d’impression et de clics et des JavaScript, pour chaque contenu créatif de l’offre groupée. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Libellé :** (facultatif) tous les libellés à appliquer à tous les contenus publicitaires sélectionnés. Vous pouvez filtrer les contenus publicitaires par libellé dans différentes vues de [!DNL Creative].

* Pour sélectionner des libellés existants, cliquez sur ![Bas](/help/creative/assets/chevron-down.png "Bas"), puis cochez la case en regard de chaque libellé à appliquer.

* Pour rechercher des libellés existants, commencez à saisir une chaîne de texte dans le nom du libellé.

* Pour créer une nouvelle étiquette à appliquer aux contenus publicitaires, ouvrez la liste, cliquez sur **+ Ajouter une étiquette**, saisissez un nouveau nom d’étiquette dans le champ [!UICONTROL Label], puis cliquez sur **Créer**.

* Pour supprimer un libellé, décochez la case en regard du nom du libellé.

### Onglet Modèle

*Contenu créatif statique HTML5 existant uniquement*

Le fichier modèle HTML5 pour le créatif.

Vous pouvez éventuellement remplacer le modèle existant par un nouveau modèle avec une disposition différente, mais le même ensemble de noms d’attributs que le modèle d’origine. Le nouveau modèle doit être au format ZIP avec un maximum de 2 Mo. Lorsque le contenu créatif se trouve dans un lot, toutes les expériences qui utilisent le lot utiliseront ensuite la mise en page du nouveau modèle.

Lorsque vous mettez à jour le modèle d’un élément créatif parent avec des variations enfant, les variations sont mises à jour avec toutes les modifications apportées à la mise en page du modèle, mais les valeurs d’attribut de la variation ne sont pas modifiées.

Pour remplacer le modèle d’annonce publicitaire existant :

1. Cliquez sur **Mettre à jour le modèle**.

1. Cliquez sur **Continuer**.

1. Spécifiez un fichier ZIP de l’une des manières suivantes :

   * Faites glisser et déposez un fichier sur votre appareil ou réseau dans la zone.

   * Cliquez sur **[!UICONTROL select a file]** pour localiser le fichier sur votre appareil ou réseau.

   Voir les [spécifications de publicité HTML](html5-creative-specification.md).

1. Modifiez les nouveaux paramètres de publicité [HTML5](#creative-settings-html5) si nécessaire.

1. Clic **[!UICONTROL Edit]**

## Paramètres de création d’image {#creative-settings-image}

**Nom du contenu publicitaire :** le nom du contenu publicitaire. Pour une nouvelle création, le nom du fichier est utilisé par défaut, mais vous pouvez le modifier. Pour plusieurs images, vous pouvez modifier les noms des créations individuelles. **Conseil :** utilisez un nom qui sera facile à trouver lorsque vous inclurez le contenu créatif dans une expérience.

**Langue :** langue par défaut de chaque publicité à laquelle vous associez les contenus publicitaires. La même valeur s’applique à toutes les images sélectionnées. &lt;!— VÉRIFIER SI DES ÉVÉNEMENTS PEUVENT SE PRODUIRE AU NIVEAU DE L’OFFRE GROUPÉE, et si les paramètres d’expérience se trouvent uniquement au niveau de l’expérience : lorsque vous incluez les éléments créatifs dans une expérience, vous pouvez éventuellement personnaliser les préférences linguistiques de l’expérience.

**Creative Size :** (lecture seule) dimensions des images chargées.

**URL de la page de destination :** URL de la page de destination par défaut pour chaque publicité à laquelle vous associez les contenus publicitaires. L’URL de la page de destination doit être une URL valide commençant par http:// ou https://. Il peut inclure des paramètres de suivi tiers ou des [[!DNL Creative] macros](/help/creative/creative-macros.md) pour votre propre usage. La même valeur s’applique à toutes les images sélectionnées.

Lorsque vous incluez un contenu créatif dans une offre groupée et que vous attribuez l’offre groupée à une expérience, vous pouvez éventuellement modifier l’URL de la page de destination, ainsi qu’ajouter des URL de suivi d’impression et de clics et des JavaScript, pour chaque contenu créatif de l’offre groupée. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Libellé :** (facultatif) tous les libellés à appliquer à tous les contenus publicitaires sélectionnés. Vous pouvez filtrer les contenus publicitaires par libellé dans différentes vues de [!DNL Creative].

* Pour sélectionner des libellés existants, cliquez sur ![Bas](/help/creative/assets/chevron-down.png "Bas"), puis cochez la case en regard de chaque libellé à appliquer.

* Pour rechercher des libellés existants, commencez à saisir une chaîne de texte dans le nom du libellé.

* Pour créer une nouvelle étiquette à appliquer aux contenus publicitaires, ouvrez la liste, cliquez sur **+ Ajouter une étiquette**, saisissez un nouveau nom d’étiquette dans le champ [!UICONTROL Label], puis cliquez sur **Créer**.

* Pour supprimer un libellé, décochez la case en regard du nom du libellé.

## Paramètres de création tiers {#creative-settings-third-party}

**JavaScriptCode :** balise JavaScript (et éventuellement une autre balise pour les navigateurs qui ne prennent pas en charge JavaScript) qui pointe vers le contenu créatif sur le serveur de publicités tiers. Le script varie en fonction du serveur de publicités. Lorsque vous modifiez plusieurs contenus publicitaires, la même valeur est appliquée à chaque contenu publicitaire sélectionné.

Toutes les [macros disponibles](/help/creative/creative-macros.md) et les données auxquelles elles sont remplacées sont répertoriées sous le champ de saisie. Pour insérer l&#39;une des macros dans la balise, placez le curseur sur la description de la macro et cliquez sur ![Copier dans le presse-papiers](/help/creative/assets/copy-to-clipboard.png "Copier dans le presse-papiers"), puis collez l&#39;image où vous le souhaitez dans la balise.

Lorsque vous incluez cette contenu publicitaire dans une expérience que vous implémentez en tant qu’annonce publicitaire à partir d’un DSP, le DSP utilise les informations de cette balise pour afficher l’annonce publicitaire et effectuer le suivi des impressions et des clics sur celle-ci, puis envoie la balise vers l’échange publicitaire. Lorsque l’utilisateur clique sur l’annonce publicitaire et l’affiche, le serveur de publicités, le DSP et le [!DNL Creative] effectuent le suivi des événements.

**[!UICONTROL Advertiser]:** (Lecture seule) Annonceur pour lequel la bibliothèque est disponible.

**Nom du contenu publicitaire :** le nom du contenu publicitaire. **Conseil :** utilisez un nom qui sera facile à trouver lorsque vous inclurez le contenu créatif dans une expérience.

**Taille de la création :** (lecture seule pour les annonces existantes) Dimensions de la création. Pour les nouveaux contenus publicitaires, sélectionnez dans une liste de tailles d’annonce standard.
u
**Langue :** langue par défaut de chaque publicité à laquelle vous associez les contenus publicitaires.

**URL de la page de destination :** URL de la page de destination utilisée pour valider chaque publicité à laquelle vous associez les contenus publicitaires. La page de destination réelle de chaque publicité est déterminée par le serveur de publicités tiers.

**Libellé :** (facultatif) tous les libellés à appliquer à tous les contenus publicitaires sélectionnés. Vous pouvez filtrer les contenus publicitaires par libellé dans différentes vues de [!DNL Creative].

* Pour sélectionner des libellés existants, cliquez sur ![Bas](/help/creative/assets/chevron-down.png "Bas"), puis cochez la case en regard de chaque libellé à appliquer.

* Pour rechercher des libellés existants, commencez à saisir une chaîne de texte dans le nom du libellé.

* Pour créer une nouvelle étiquette à appliquer aux contenus publicitaires, ouvrez la liste, cliquez sur **+ Ajouter une étiquette**, saisissez un nouveau nom d’étiquette dans le champ [!UICONTROL Label], puis cliquez sur **Créer**.

* Pour supprimer un libellé, décochez la case en regard du nom du libellé.

>[!MORELIKETHIS]
>
>* [Ajouter des contenus publicitaires standard à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-standard.md)
>* [Modification de contenus publicitaires standard](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Macros disponibles pour le tracking des URL](/help/creative/creative-macros.md)
