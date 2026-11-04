---
title: Gestion des contenus créatifs dynamiques dans Creative Studio
description: Découvrez comment créer, vérifier la qualité, modifier, dupliquer et supprimer des contenus publicitaires dynamiques pilotés par catalogue dans Adobe Advertising Creative Studio.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: b9a68528b3c622aae44a46bca9b3bb747019bc95
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%
---
# Gestion des contenus publicitaires dynamiques dans [!UICONTROL Creative Studio]

L’onglet **[!UICONTROL Creatives]** dans [!UICONTROL Creative Studio] répertorie vos contenus publicitaires dynamiques par bibliothèque. À partir de là, vous pouvez créer des contenus publicitaires dynamiques pilotés par catalogue, vérifier la qualité des contenus publicitaires à l’aide de l’IA, modifier les détails et le mappage des attributs des contenus publicitaires existants, afficher les journaux des modifications, dupliquer des contenus publicitaires et supprimer des contenus publicitaires.

## Créer un contenu créatif dynamique {#build-dynamic-creative}

Utilisez ce workflow pour créer des contenus publicitaires dynamiques pilotés par catalogue. Un assistant guidé en quatre étapes vous guide tout au long de la sélection d’un modèle, de la connexion d’un catalogue et du mappage des champs du catalogue aux éléments du modèle. Après la configuration, le [!UICONTROL AI Assistant] vous permet de prévisualiser et de vérifier la qualité de chaque combinaison d’annonces générée à partir des données du catalogue.

Les contenus créatifs dynamiques diffèrent des publicités standard d’une manière essentielle : l’agent d’IA ne peut pas modifier le contenu provenant du catalogue. Il peut filtrer, analyser et signaler des problèmes, mais pour modifier le contenu de l’annonce, vous devez mettre à jour manuellement les valeurs du catalogue, à partir de l’écran d’assurance qualité ou dans le catalogue source.

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

   Si vous passez à l’assurance qualité, l’écran de **[!UICONTROL Dynamic Creative QA]** s’ouvre avec une zone de travail de prévisualisation et le panneau de conversation **[!UICONTROL AI Assistant]**.

1. Si vous continuez à effectuer un contrôle qualité, suivez les procédures de la section « [Vérification de la qualité d’un contenu créatif dynamique](#qa-dynamic-creative) » pour [analyser et filtrer les publicités](#analyze-ads), [consulter les aperçus et les alertes](#review-previews) et éventuellement [corriger les valeurs de catalogue](#correct-catalog-values). Lorsque vous avez terminé, [enregistrez la création dynamique](#save-or-exit).

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

## Vérification de la qualité d’une création dynamique {#qa-dynamic-creative}

Utilisez l’assistant d’assurance qualité pour analyser les lignes du catalogue par rapport au modèle d’un créatif dynamique, prévisualiser les publicités obtenues et identifier les problèmes de contenu potentiels. Vous pouvez filtrer et regrouper des annonces publicitaires à l’aide de l’**[!UICONTROL AI Assistant]**, passer en revue les alertes de catalogue et corriger manuellement les valeurs de catalogue avant de publier les modifications.

>[!NOTE]
>
>Vous pouvez vérifier la qualité des contenus publicitaires dynamiques depuis [!UICONTROL Creative Studio] ou [!UICONTROL Creative Libraries]. Bien que les libellés de menu diffèrent, les deux points d’entrée ouvrent le même écran de **[!UICONTROL Dynamic Creative QA]** avec la même fonctionnalité. L’analyse dépend du contenu créatif, du catalogue et de la requête sélectionnés. Pour l’autre point d’entrée, reportez-vous à « [Vérification de la qualité d’un élément créatif dynamique à partir des bibliothèques Creative](/help/creative/creative-libraries/creative-edit-dynamic.md#qa-dynamic-creative) ».

L’assistant QA est disponible pour les contenus publicitaires d’affichage dynamique, et non pour les contenus publicitaires standard ou vidéo dynamiques.

### Ouvrez l’assistant d’assurance qualité {#open-qa-agent}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , recherchez le contenu créatif dynamique dans sa bibliothèque de contenu créatif sous la section [!UICONTROL Generate or Build Creatives] .

1. Placez le curseur sur la carte de contenu créatif, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   L’écran de **[!UICONTROL Dynamic Creative QA]** s’ouvre avec une zone de travail de prévisualisation et le panneau de conversation **[!UICONTROL AI Assistant]**.

1. Si le contenu créatif utilise plusieurs catalogues, sélectionnez le catalogue à réviser dans les **[!UICONTROL Catalog]** de l’en-tête.

   L&#39;assistant analyse le catalogue sélectionné. Le sélecteur de catalogues est désactivé lorsque le contenu créatif n’utilise qu’un seul catalogue.

### Analyser et filtrer les publicités avec l’IA {#analyze-ads}

1. Dans le panneau **[!UICONTROL AI Assistant]**, saisissez une requête dans **[!UICONTROL Ask anything]** et appuyez sur **[!UICONTROL Enter]**, ou cliquez sur l’une des invites suggérées :

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   L’assistant répond dans le panneau de conversation et affiche les lignes de catalogue correspondantes sous forme d’aperçus publicitaires sur la zone de travail. Tant que vous n’avez pas envoyé de requête, la zone de travail vous invite à demander à l’assistant d’analyser le catalogue.

1. Continuer à affiner l’examen avec des demandes de suivi. L’assistant peut vous aider à :

   * Filtrez les annonces par segment d’audience, langue, zone géographique ou code postal.
   * Vérifiez la longueur des caractères à l’aide d’un seuil que vous spécifiez.
   * Recherchez les erreurs de flux, le contenu manquant et le contenu suspect.
   * Vérifiez le statut de la traduction.
   * Comparez les variantes des tests A/B.
   * Regroupez les publicités pour examen, par exemple par produit ou problème.

   Vérifiez les réponses de l&#39;assistant et examinez les aperçus avant d&#39;enregistrer les modifications.

### Prévisualisations et alertes de révision {#review-previews}

* Utilisez la barre d’outils de la zone de travail pour :

  * Ajustez le zoom.
  * Basculez entre **[!UICONTROL Thumbnail view]** et **[!UICONTROL Actual size]**.
  * Cliquez sur **[!UICONTROL Replay animations]** pour relire les aperçus.
  * Sélectionnez le nombre de lignes par page, un numéro de page ou utilisez **[!UICONTROL Previous page]** et **[!UICONTROL Next page]**.

* Lorsque l’assistant regroupe les résultats, cliquez sur le lien pour afficher tous les contenus publicitaires d’un groupe. Utilisez **[!UICONTROL Back to groups]** pour revenir aux résultats groupés ou **[!UICONTROL Catalog Rows]** pour quitter la vue groupée.

* Lorsqu’un aperçu s’affiche en **[!UICONTROL Issues detected]**, placez le curseur sur l’indicateur pour afficher les détails de l’événement.

* Lorsque des alertes de catalogue sont disponibles, cliquez sur **[!UICONTROL View Alerts]**. La boîte de dialogue **[!UICONTROL Alerts]** répertorie le catalogue, le numéro de ligne, la colonne et le message d’erreur pour chaque événement. Cliquez sur **[!UICONTROL Close]** pour revenir à la zone de travail.

### Valeurs de catalogue correctes {#correct-catalog-values}

Vous pouvez modifier manuellement les valeurs de catalogue à partir d’une prévisualisation d’annonce publicitaire sans quitter l’écran d’assurance qualité.

1. Dans l’aperçu à corriger, cliquez sur **[!UICONTROL Edit]**.

1. Dans la boîte de dialogue de modification, sélectionnez les colonnes à modifier sous **[!UICONTROL Catalog columns to edit]**. Pour rechercher une colonne, utilisez **[!UICONTROL Search columns]**.

1. Sous **[!UICONTROL Columns content]**, mettez à jour les valeurs de champ sélectionnées.

1. Cliquez sur **[!UICONTROL Update]**.

   L’aperçu s’actualise pour refléter les valeurs mises à jour. Les modifications du catalogue ne sont pas publiées tant que vous n’avez pas enregistré la création dynamique.

>[!IMPORTANT]
>
>Ces modifications mettent à jour les données du catalogue, et pas seulement la prévisualisation de l’annonce publicitaire. Passez en revue les valeurs avant de les publier.

### Enregistrer les modifications ou quitter {#save-or-exit}

* Pour enregistrer le contenu créatif dynamique et publier les modifications du catalogue :

  1. Cliquez sur **[!UICONTROL Save Dynamic Creative]** dans l’en-tête.

  1. Confirmez l’enregistrement :

     * Pour un nouvel élément créatif, dans la boîte de dialogue de confirmation de **[!UICONTROL Create Dynamic Creative]**, cliquez sur **[!UICONTROL Create]**.
     * Pour un élément créatif existant, dans la boîte de dialogue de confirmation de **[!UICONTROL Update Dynamic Creative]**, cliquez sur **[!UICONTROL Update]**.

     Vous revenez à [!UICONTROL Creative Studio].

* Pour quitter sans publier les modifications de catalogue en attente, cliquez sur **[!UICONTROL Cancel]** dans l’en-tête de la page.

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
