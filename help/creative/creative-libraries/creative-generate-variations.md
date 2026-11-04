---
title: Générer des variantes de contenus publicitaires HTML5 flexibles
description: Découvrez comment générer et enregistrer des variations assistées par l’IA de contenus publicitaires HTML5 flexibles à partir d’une bibliothèque de contenus publicitaires.
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 1cc477f531051d94ea88eaae0a4fb83918e95ea5
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%
---
# Générer des variantes de contenus publicitaires HTML5 flexibles

Utilisez l’[!UICONTROL Ad Variations Generator] pour créer des variantes d’une création HTML5 flexible existante. L’assistant d’IA génère et affine les titres, les appels à l’action, les images, les couleurs, etc. et peut créer de nouvelles variantes de taille en une seule session. Enregistrez les variations résultantes en tant que nouvelles annonces standard dans la bibliothèque de contenu créatif.

>[!NOTE]
>
>Vous pouvez également générer des variations d’annonces publicitaires à partir de [!UICONTROL Creative Studio]. Les deux points d’entrée ouvrent la même [!UICONTROL Ad Variations Generator]. Pour l’autre point d’entrée, voir « [Générer des variations d’annonce publicitaire pour une annonce publicitaire standard dans Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations) ».

## Disponibilité {#availability}

L’action **[!UICONTROL Generate Variations]** est disponible pour les créatifs HTML5 flexibles, y compris ceux basés sur des modèles système, dans la nouvelle interface utilisateur de [!UICONTROL Creative Libraries]. Il n’est pas disponible pour les autres types de contenu créatif, y compris les contenus dynamiques.

L’action est désactivée lorsque le contenu créatif ne dispose pas de la référence de modèle d’annonce publicitaire parent interne requise par le générateur. Cette référence n’est pas un paramètre que vous pouvez modifier. Le téléchargement ou le remplacement d’un fichier dans l’onglet **[!UICONTROL Template]** du contenu créatif ne le définit pas explicitement.

## Ouvrez le générateur de variantes d’annonces {#open-generator}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Ouvrez la bibliothèque de l’une des manières suivantes :

   * Cliquez sur le nom de la bibliothèque.
   * En regard du nom de la bibliothèque, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , cliquez sur **[!UICONTROL ...]** en regard du nom du contenu créatif HTML5 flexible, puis cliquez sur **[!UICONTROL Generate Variations]**.

   La [!UICONTROL Ad Variations Generator] s’ouvre avec le contenu de l’élément créatif sélectionné. La zone de travail affiche la section **[!UICONTROL Template Sizes]** avec les formats d’annonce disponibles pour le modèle et une section **[!UICONTROL Ad Concepts]** dans laquelle le contenu généré s’affiche.

## Générer et affiner les variations {#generate-variations}

1. (Facultatif) Pour appliquer un profil de marque aux publicités, sélectionnez un **[!UICONTROL Brand Profile]** dans la barre d’outils de la zone de travail.

   L’assistant d’IA utilise le logo, la palette de couleurs, les directives vocales, les normes d’image et les directives de canal de votre marque lors de la génération de contenu.

1. Créez des variations d’annonce publicitaire à l’aide du [!UICONTROL AI Assistant] :

   1. Dans le champ **[!UICONTROL Ask AI to generate ad variations…]** , saisissez une demande et appuyez sur **[!UICONTROL Enter]**, ou cliquez sur l’une des invites présentées :

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      L’IA génère des résultats sur la zone de travail et les organise en *concepts*, chacun représentant une variation de contenu distincte. Le compteur de concepts de la section **[!UICONTROL Ad Concepts]** permet de suivre le nombre de concepts existants (par exemple, **(2/10)**). Jusqu’à 10 concepts sont autorisés par session.

   1. Continuez à affiner en envoyant des messages de relance. Exemples :

      * « Rendez toute la copie plus ludique et moins corporative. »
      * « Remplacez le logo par la version blanche. »
      * « Définissez le CTA sur « Acheter maintenant » pour tous les concepts. »
      * « Redimensionnez cette annonce publicitaire pour les 6 formats d’affichage standard de l’IAB. »
      * « Donnez-moi trois concepts d’en-tête différents avec une image d’arrière-plan correspondante pour chacun. »

      >[!NOTE]
      >
      >L’assistant d’IA peut générer et modifier du texte (titres, sous-titres, CTA, copie du corps), échanger des images d’arrière-plan, appliquer des couleurs de marque, changer de version de logo et créer de nouveaux modèles de taille. Il ne peut pas modifier la structure du modèle : position des éléments, disposition, espacement, marge intérieure, famille de polices, taille de police ou bordures. Effectuez des modifications structurelles dans l’éditeur de modèles avant de démarrer la session. Voir [&#x200B; Modification d’un modèle &#x200B;](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template).

   1. (Facultatif) Pour inclure une référence visuelle dans une requête, cliquez sur le bouton **[!UICONTROL +]** dans la zone de saisie de conversation. Dans la boîte de dialogue **[!UICONTROL Select from Asset Library]** :

      * Pour utiliser une ressource de votre bibliothèque de ressources, cliquez sur la ressource, puis sur **[!UICONTROL Add to chat]**. Envoyez votre message pour inclure la ressource en tant que contexte.

      * Pour charger une ou plusieurs ressources, cliquez sur **[!UICONTROL Upload Assets]** et sélectionnez les fichiers sur votre appareil ou réseau.

1. (Facultatif) Utilisez la barre d’outils de la zone de travail pour consulter les annonces générées :

   * **[!UICONTROL Brand]:** permet de sélectionner ou de modifier le profil de marque appliqué à la session.
   * **[!UICONTROL Zoom in]**/**[!UICONTROL Zoom out]:** permet d’ajuster le niveau de zoom de la zone de travail.
   * **[!UICONTROL Fit to screen]:** Réinitialiser l’affichage pour afficher toutes les tailles.
   * **[!UICONTROL Replay animations]:** Relire les animations de modèles.

   Lorsque l’IA crée une nouvelle taille, les commandes **[!UICONTROL Adjust]**, **[!UICONTROL Keep]** et Supprimer s’affichent sur la nouvelle carte de taille. Cliquez sur **[!UICONTROL Keep]** pour accepter la taille telle quelle, sur **[!UICONTROL Adjust]** pour ouvrir le modèle dans l’éditeur d’affichage où vous pouvez apporter des modifications structurelles, puis cliquez sur **[!UICONTROL Update Ad Format]** pour l’enregistrer, ou cliquez sur l’icône de suppression pour supprimer la nouvelle taille.

1. (Facultatif) Gérez les concepts et les variations :

   * Pour gérer un concept, placez le curseur sur le libellé du concept (par exemple, **[!UICONTROL Concept 3]**), cliquez sur **[!UICONTROL ...]**, puis sélectionnez une option :

     * **[!UICONTROL Add to chat]:** fait référence au concept dans votre invite suivante.
     * **[!UICONTROL Delete]:** Supprime le concept.

   * Pour gérer une variation individuelle, placez le curseur sur la carte de variation, cliquez sur **[!UICONTROL ...]**, puis sélectionnez une option :

     * **[!UICONTROL Add to Chat]:** fait référence à la variation dans votre invite suivante. Vous pouvez également cliquer directement sur le corps de la carte de variation pour activer/désactiver la mention.
     * **[!UICONTROL Edit Data]:** ouvre une boîte de dialogue dans laquelle vous pouvez mettre à jour les **[!UICONTROL Name]** de variation et l’URL de clic publicitaire pour chaque balise de clic définie dans le modèle. Cliquez sur **[!UICONTROL Save]** pour appliquer.
     * **[!UICONTROL Delete]:** supprime la variation.

## Enregistrer les variations {#save-variations}

1. Lorsque les concepts générés vous conviennent, cliquez sur **[!UICONTROL Save Standard Ads]** dans l’en-tête.

   Le bouton est désactivé jusqu’à ce qu’au moins un concept existe.

1. Dans la boîte de dialogue **[!UICONTROL Save Standard Ads]**, vérifiez les paramètres suivants, puis cliquez sur **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** annonceur associé à la bibliothèque de contenu créatif source. Vous ne pouvez pas modifier cette valeur.

   **[!UICONTROL Creative Library]:** la bibliothèque de contenu créatif source dans laquelle les nouvelles annonces sont enregistrées. Vous ne pouvez pas modifier cette valeur.

   **[!UICONTROL Attach to Bundles]:** (facultatif) Lorsqu’ils sont activés, les contenus publicitaires enregistrés sont associés à un ou plusieurs lots. Pour chaque variation d’annonce publicitaire, sélectionnez un lot ou saisissez un nouveau nom de lot.

   **\[Paramètres de chaque publicité\]:** Pour chaque variation de publicité, vous pouvez afficher et éventuellement modifier l’URL de **[!UICONTROL Name]**, de **[!UICONTROL Language]** et de clic publicitaire pour chaque balise de clic.

   Vous revenez à la bibliothèque de contenu créatif.

>[!MORELIKETHIS]
>
>* [Modification de contenus publicitaires standard](creative-edit-standard.md)
>* [Gestion des publicités standard dans Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [Gestion des profils de marque dans Advertising Creative](/help/creative/brands/brand-manage.md)
>* Métadonnées [C2PA dans [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-content-credentials.md)
