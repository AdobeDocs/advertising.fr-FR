---
title: Gestion des contenus créatifs dynamiques dans Creative Studio
description: Découvrez comment créer, modifier, dupliquer et supprimer des contenus publicitaires dynamiques pilotés par catalogue dans Adobe Advertising Creative Studio.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 0%

---

# Gestion des contenus publicitaires dynamiques dans [!UICONTROL Creative Studio]

*Fonction*

L’onglet **[!UICONTROL Creatives]** dans [!UICONTROL Creative Studio] répertorie vos contenus publicitaires dynamiques par bibliothèque. À partir de là, vous pouvez créer des contenus publicitaires dynamiques pilotés par catalogue, modifier les détails et le mappage des attributs des contenus publicitaires existants, afficher les journaux des modifications, dupliquer des contenus publicitaires et supprimer des contenus publicitaires.

## Créer un contenu créatif dynamique {#build-dynamic-creative}

Utilisez ce workflow pour créer des contenus publicitaires dynamiques pilotés par catalogue. Un assistant guidé en quatre étapes vous guide tout au long de la sélection d’un modèle, de la connexion d’un catalogue et du mappage des champs du catalogue aux éléments du modèle. Après la configuration, le [!UICONTROL AI Assistant] vous permet de prévisualiser et de vérifier la qualité de chaque combinaison d’annonces générée à partir des données du catalogue.

Les contenus créatifs dynamiques diffèrent des publicités standard d’une manière essentielle : l’agent d’IA ne peut pas modifier le contenu provenant du catalogue. Il peut filtrer, analyser et signaler des problèmes, mais pour modifier le contenu de l’annonce, vous devez mettre à jour le catalogue source.

### Conditions préalables

* Au moins un modèle d’annonce publicitaire créé par l’utilisateur (et non un modèle système) doit exister dans votre bibliothèque de modèles.
* Un catalogue de produits ou de contenu (flux) est disponible dans votre compte .

### Étape 1 : ouvrir l’assistant [!UICONTROL Build Dynamic Creative] {#open-wizard}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Sur l’onglet **[!UICONTROL Creatives]** , cliquez sur **[!UICONTROL Build]** dans la carte d’action rapide **[!UICONTROL Build dynamic creatives from catalog data]** .

   La boîte de dialogue de **[!UICONTROL Build Dynamic Creative]** en quatre étapes s’ouvre.

### Étape 2 : sélectionner un modèle {#select-template}

>[!NOTE]
>
>La galerie de modèles répertorie uniquement les modèles d’annonces publicitaires que vous avez créés. Les modèles système et les modèles d’annonces vidéo ne sont pas disponibles comme point de départ pour les créatifs dynamiques.

1. Dans la galerie de modèles, cliquez sur un modèle pour le sélectionner.

   Le bouton **[!UICONTROL Next]** est désactivé jusqu’à ce qu’un modèle soit sélectionné.

1. Cliquez sur **[!UICONTROL Use this template]**.

### Étape 3 : sélectionner un catalogue {#select-catalog}

1. Configurez les paramètres de contenu créatif :

   * **[!UICONTROL Ad Library]:** sélectionnez la bibliothèque de contenu créatif dans laquelle enregistrer le contenu créatif.
   * **[!UICONTROL Dynamic creative name]:** saisissez un nom pour le contenu créatif dynamique.
   * **[!UICONTROL Number of cards]:** Entrez le nombre d’offres de catalogue à inclure dans chaque combinaison d’annonces (1-50).
   * **[!UICONTROL Assign dynamic creative to a bundle]:** (facultatif) Lorsque cette option est activée, les contenus publicitaires enregistrés sont associés à un lot. Sélectionnez un lot dans la bibliothèque.

1. Sélectionnez un ou plusieurs catalogues :

   1. (Facultatif) Utilisez **[!UICONTROL Catalog template]** pour filtrer la liste du catalogue selon une famille de modèles spécifique. Pour éventuellement télécharger le fichier modèle pour le réviser, cliquez sur **[!UICONTROL Download feed template]**.

   1. Recherchez et sélectionnez des catalogues dans la liste. Tous les catalogues sélectionnés doivent appartenir à la même famille de modèles de catalogue ; un avertissement s&#39;affiche si vous tentez de mélanger des familles.

   1. (Facultatif) Pour charger un nouveau fichier catalogue, faites-le glisser et déposez-le dans la zone de chargement ou cliquez sur **[!UICONTROL Browse Files]**. Formats pris en charge : JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP et MP4. Taille de fichier maximale : 25 Mo. Vous pouvez charger un fichier à la fois. Les catalogues chargés apparaissent dans la liste des puces intitulée **(uploaded)**.

1. Cliquez sur **[!UICONTROL Continue]**.

### Étape 4 : Mapper les champs du catalogue aux éléments du modèle {#attribute-mapping}

Mappez chaque champ du catalogue à l’élément correspondant de votre modèle. Par exemple, mappez le champ nom du produit du catalogue à l’élément d’en-tête du modèle et le champ image du produit à l’élément image d’arrière-plan.

1. Sous **[!UICONTROL Targeting]**, sélectionnez au moins une source de données pour personnaliser le contenu créatif : **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** ou **[!UICONTROL Audience Segment]**.

1. Pour chaque élément de modèle, sélectionnez le champ de catalogue correspondant dans la liste déroulante.

1. Cliquez sur **[!UICONTROL Continue]**.

### Étape 5 : prévisualisation et contrôle qualité avec l’IA {#qa}

1. Choisissez s’il faut *[!UICONTROL Save Dynamic Creative & Skip QA]* ou *[!UICONTROL Continue to QA]*.

   Si vous continuez à effectuer un contrôle qualité, la zone de travail affiche toutes les combinaisons d’annonces générées à partir du catalogue, affichées sous forme de lignes avec un aperçu de chaque entrée du catalogue rendue dans le modèle.

1. Si vous continuez le contrôle qualité :

   1. Effectuez l’une des opérations suivantes :

      * Utilisez les commandes **[!UICONTROL Zoom in]** et **[!UICONTROL Zoom out]** pour ajuster la vue de la zone de travail.

      * Utilisez les commandes de pagination (**X-Y sur Z**) pour parcourir les lignes du catalogue.

      * Pour modifier une combinaison d’annonces :

         1. Placez le curseur sur la ligne du catalogue et cliquez sur **[!UICONTROL Edit]**.

         1. Dans la boîte de dialogue **[!UICONTROL Edit Row]**, mettez à jour les valeurs de champ.

         1. Cliquez sur **[!UICONTROL Save]**.

        La zone de travail s’actualise pour refléter les valeurs mises à jour.

      * Utilisez le panneau de conversation **[!UICONTROL AI Assistant]** pour analyser et filtrer les combinaisons de catalogues. Saisissez votre demande dans le champ **[!UICONTROL Ask anything]** ou cliquez sur l’une des invites suggérées :

         * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
         * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
         * **[!UICONTROL Show me all ads for millennial women in urban markets]**

        L’agent AI peut :

         * Filtrez la zone de travail pour afficher les annonces correspondant à un segment d’audience, une zone géographique, une langue, une catégorie ou un autre champ de catalogue spécifique.
         * Vérifiez les problèmes de qualité tels que les dépassements de limite de caractères, le débordement ou le fond perdu du contenu, les liens d’image rompus et la visibilité de clause de non-responsabilité.
         * Comparez les combinaisons d’annonces pour l’analyse des tests A/B.
         * Organisez les annonces en groupes pour une révision côte à côte.

        L’agent d’IA ne peut pas modifier le contenu provenant du catalogue. Pour modifier le contenu de l’annonce publicitaire, mettez à jour le catalogue source.

   1. Enregistrez le **[!UICONTROL Save Dynamic Creative]** dans l’en-tête.

   1. Dans le message de confirmation, cliquez sur **[!UICONTROL Create]**.

## Modification d’un élément créatif dynamique {#edit-dynamic-creative}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   Un éditeur plein écran s’ouvre avec un aperçu d’annonce publicitaire à gauche et un panneau de paramètres à droite.

1. Modifiez les paramètres créatifs à l’aide des onglets **[!UICONTROL Details]** et **[!UICONTROL Attribute Mapping]** :

   Onglet **[!UICONTROL Details]** :

   * **[!UICONTROL Advertiser]**, **[!UICONTROL Ad Library]** et **[!UICONTROL Ad template]** sont en lecture seule.
   * **[!UICONTROL Dynamic creative name]:** nom d’affichage du contenu créatif.
   * **[!UICONTROL Number of cards]:** nombre d’offres de catalogue incluses dans chaque combinaison d’annonces (1-50).
   * (Facultatif) Sous **[!UICONTROL Catalogs]**, mettez à jour la sélection de catalogue :
      * Utilisez **[!UICONTROL Catalog template]** pour filtrer les catalogues disponibles. Pour télécharger éventuellement le fichier de modèle, cliquez sur **[!UICONTROL Download feed template]**.
      * Recherchez et sélectionnez des catalogues dans la liste, ou chargez un nouveau fichier catalogue en le faisant glisser vers la zone de chargement ou en cliquant sur **[!UICONTROL Browse Files]** (formats pris en charge : JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP, MP4 ; 25 Mo maximum ; un fichier à la fois). Les catalogues chargés sont étiquetés **(chargés)** dans la liste des puces.

     Tous les catalogues doivent appartenir à la même famille de modèles de catalogue.

   Onglet **[!UICONTROL Attribute Mapping]** :

   * Sous **[!UICONTROL Targeting]**, sélectionnez au moins une source de données : **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** ou **[!UICONTROL Audience Segment]**.
   * Sous **[!UICONTROL Attribute Mapping]**, mettez à jour le mappage de chaque nom de calque de modèle vers le libellé de colonne de catalogue correspondant.

1. Cliquez sur **[!UICONTROL Update Creative]**.

## Rouvrez l’assistant de contrôle qualité pour une création dynamique {#qa-dynamic-creative}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   L’écran d’assurance qualité s’ouvre. Consultez « [Étape 5 : prévisualisation et assurance qualité avec l’IA ](#qa) » pour connaître les commandes de la zone de travail disponibles et les fonctionnalités de l’assistant d’IA.

## Affichage du journal des modifications d’un élément créatif dynamique {#view-change-log}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

## Duplication d’un contenu créatif dynamique {#duplicate-dynamic-creative}

Dupliquez un contenu créatif dynamique pour ajouter un nouveau contenu créatif avec les mêmes paramètres à la bibliothèque. Vous pouvez ensuite renommer le nouveau contenu créatif et modifier les paramètres selon vos besoins.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   Le nouveau contenu créatif est nommé `<original name> (copy)`.

## Suppression d’un élément créatif dynamique {#delete-dynamic-creative}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos de Creative Studio dans Advertising Creative](creative-studio-about.md)
>* [Gestion des publicités standard dans Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gestion des modèles dans Creative Studio](creative-studio-manage-templates.md)
