---
title: Modification et vérification de la qualité des contenus publicitaires dynamiques
description: Découvrez comment modifier des paramètres de création dynamiques et vérifier la qualité du contenu du catalogue dans une bibliothèque de contenu créatif.
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ed1682eff9ce28df30a5314de90f6f67c10f338a
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%
---
# Modification et vérification de la qualité des contenus publicitaires dynamiques

Modifiez les paramètres de contenu créatif pour modifier la configuration du contenu créatif, comme son nom, ses catalogues et le mappage d’attributs. Utilisez l’agent d’assurance qualité pour passer en revue les annonces résultantes et corriger les valeurs de catalogue.

## Modifier les paramètres de création {#edit-creative-settings}

### Dans la nouvelle interface utilisateur {#from-the-new-ui}

1. Ouvrez les paramètres de création :

   * À partir d’une bibliothèque de contenu créatif :

     1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Ouvrez la bibliothèque de l’une des manières suivantes :

        * Cliquez sur le nom de la bibliothèque.

        * En regard du nom de la bibliothèque, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Open]**.

     1. Dans l’onglet **[!UICONTROL Creatives]** , cliquez sur **[!UICONTROL ...]** en regard du nom du contenu créatif, puis cliquez sur **[!UICONTROL Edit]**.

   * Depuis le [!UICONTROL Creative Studio] :

     1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]>[!UICONTROL Creative Studio]**.

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

### À partir de l’interface utilisateur héritée {#from-the-legacy-ui}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur **[!UICONTROL Switch to classic UI]**.

1. Cliquez sur le nom de la bibliothèque.

1. Placez le curseur sur la ligne de contenu créatif et cliquez sur **[!UICONTROL Edit]**.

1. Modifiez le [paramètres des annonces dynamiques](creative-settings-dynamic.md).

1. Cliquez sur **[!UICONTROL Continue]** pour prévisualiser les contenus publicitaires à générer. Vous pouvez effectuer l’une des opérations suivantes dans l’aperçu :

   * Pour filtrer les contenus publicitaires par catalogue<!-- explain more--> valeur de filtre et taille d’annonce, utilisez les filtres situés au-dessus de la zone d’aperçu.

   * Pour rechercher un produit par son identifiant unique dans le champ de recherche situé sous la zone d’aperçu.

   * Pour modifier les colonnes affichées, cliquez sur ![Filtre de colonne](/help/creative/assets/custom-columns.png "Filtre de colonne") sous la zone d’aperçu.

   * Pour prévisualiser un contenu créatif spécifique, cochez la case de la ligne.

   * Modifiez le contenu :

     * (Affichage des annonces uniquement) Pour modifier la valeur d’une cellule dans le tableau, cliquez à l’intérieur de la cellule et modifiez la valeur. Cliquez en dehors de la cellule ou appuyez sur la touche **[!DNL Enter]** pour enregistrer vos modifications.

     * Pour marquer un seul produit comme produit par défaut<!--Explain what this means. --> maintenez le curseur au-dessus de la ligne et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

     * (Lorsque l’annonce publicitaire comprend plusieurs offres) Pour marquer plusieurs produits comme produits par défaut, sélectionnez les lignes (jusqu’au nombre d’offres) et cliquez sur **[!UICONTROL Set as Default]** dans la barre d’outils des actions en masse.

     * Pour supprimer un produit du catalogue, maintenez le curseur sur la ligne et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

     * (Lorsque l’annonce publicitaire comprend plusieurs offres) Pour supprimer plusieurs produits du catalogue, sélectionnez les lignes (jusqu’au nombre d’offres) et cliquez sur **[!UICONTROL Delete Row]** dans la barre d’outils d’actions en masse.

1. Enregistrez les contenus publicitaires :

   * Pour enregistrer les publicités et les ajouter à un [lot de contenu créatif](bundle-manage.md) dans la bibliothèque :

     1. Cliquez sur **[!UICONTROL Save and Attach to Bundle]**.

     1. Cliquez sur **[!UICONTROL Save]** pour enregistrer les publicités.

     1. Sélectionnez les lots, puis cliquez sur **[!UICONTROL Attach Creative to Bundles]**.

   * Pour enregistrer les publicités et quitter la configuration, cliquez sur **[!UICONTROL Save]**, puis cliquez de nouveau sur **[!UICONTROL Save]**.

## Vérification de la qualité d’une création dynamique (nouvelle interface utilisateur uniquement) {#qa-dynamic-creative}

Utilisez l’agent d’assurance qualité dans la nouvelle interface utilisateur pour analyser les lignes du catalogue par rapport au modèle d’un créatif dynamique, prévisualiser les publicités obtenues et identifier les problèmes de contenu potentiels. Vous pouvez filtrer et regrouper des annonces publicitaires à l’aide de l’**[!UICONTROL AI Assistant]**, passer en revue les alertes de catalogue et corriger manuellement les valeurs de catalogue avant de publier les modifications.

>[!NOTE]
>
>Vous pouvez vérifier la qualité des contenus publicitaires dynamiques depuis [!UICONTROL Creative Libraries] ou [!UICONTROL Creative Studio]. Pour l’autre point d’entrée, reportez-vous à « [Vérification de la qualité d’un contenu créatif dynamique dans Creative Studio](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#qa-dynamic-creative) ».

L’agent d’assurance qualité est disponible uniquement pour les contenus publicitaires à affichage dynamique basés sur des modèles dynamiques, et non pour les contenus publicitaires standard ou vidéo dynamiques.

### Ouvrez l’agent d’assurance qualité. {#open-qa-agent}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Ouvrez la bibliothèque de l’une des manières suivantes :

   * Cliquez sur le nom de la bibliothèque.
   * En regard du nom de la bibliothèque, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , cliquez sur **[!UICONTROL ...]** en regard du nom du contenu créatif dynamique, puis cliquez sur **[!UICONTROL QA Agent]**.

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

* Pour enregistrer le contenu créatif dynamique existant et publier les modifications du catalogue :

  1. Cliquez sur **[!UICONTROL Save Dynamic Creative]** dans l’en-tête.

  1. Dans la boîte de dialogue de confirmation de **[!UICONTROL Update Dynamic Creative]**, cliquez sur **[!UICONTROL Update]**.

     Vous revenez à la bibliothèque de contenu créatif.

* Pour quitter sans publier les modifications de catalogue en attente, cliquez sur **[!UICONTROL Cancel]** dans l’en-tête de la page.

>[!MORELIKETHIS]
>
>* [&#x200B; Paramètres de création dynamique &#x200B;](creative-settings-dynamic.md)
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](creative-add-dynamic.md)
>* [Afficher le journal des modifications d’un élément créatif](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Workflows pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
