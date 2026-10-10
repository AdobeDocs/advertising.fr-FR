---
title: Modification d’un élément créatif dynamique dans une bibliothèque de contenu créatif
description: Découvrez comment modifier un contenu créatif dynamique dans une bibliothèque de contenu créatif.
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
source-git-commit: b7bf89dafd678490acc0749e2755ea7f0fec67f4
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%
---
# Modification d’un élément créatif dynamique dans une bibliothèque de contenu créatif

## Dans la nouvelle interface utilisateur

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

## À partir de l’interface utilisateur héritée

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

>[!MORELIKETHIS]
>
>* [ Paramètres de création dynamique ](creative-settings-dynamic.md)
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](creative-add-dynamic.md)
>* [Afficher le journal des modifications d’un élément créatif](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Workflows pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
