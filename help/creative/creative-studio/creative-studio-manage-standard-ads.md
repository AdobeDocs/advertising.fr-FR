---
title: Gestion des publicités standard dans Creative Studio
description: Découvrez comment créer, modifier, dupliquer, télécharger et supprimer des publicités display standard dans la bibliothèque de contenus publicitaires de Creative Studio.
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 0%

---

# Gestion des publicités standard dans [!UICONTROL Creative Studio]

*Fonction*

L’onglet **[!UICONTROL Creatives]** de [!UICONTROL Creative Studio] est votre bibliothèque d’annonces publicitaires standard générées à partir de modèles. À partir de là, vous pouvez créer des annonces à l’aide de l’[!UICONTROL Ad Variations Generator], modifier des annonces enregistrées, générer de nouvelles variantes d’une annonce existante, afficher le journal des modifications, dupliquer, télécharger et supprimer.

## Créer des publicités standard {#create-standard-ads}

Utilisez l’[!UICONTROL Ad Variations Generator] pour générer le contenu de l’annonce publicitaire d’affichage à partir d’un modèle. L’assistant d’IA génère et affine les titres, les appels à l’action, les images, les couleurs, etc. et peut créer de nouvelles variantes de taille en une seule session.

>[!NOTE]
>
>La génération d’annonces standard ne prend actuellement en charge que les modèles d’annonces. Les modèles d’annonce vidéo ne sont pas disponibles comme point de départ, que ce soit dans l’onglet **[!UICONTROL Creatives]** ou dans l’onglet **[!UICONTROL Templates]** .

### Conditions préalables

Au moins un modèle d’annonce publicitaire doit exister dans votre bibliothèque de modèles.

### Générer des publicités standard

1. Ouvrez le [!UICONTROL Ad Variations Generator] de l’une des manières suivantes :

   * **Dans l’onglet [!UICONTROL Creatives] :**

      1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

      1. Sur l’onglet **[!UICONTROL Creatives]** , cliquez sur **[!UICONTROL Generate]** dans la carte d’action rapide **[!UICONTROL Generate standard ads from templates]** .

      1. Dans la boîte de dialogue de sélection des modèles, cliquez sur un modèle pour le sélectionner, puis cliquez sur **[!UICONTROL Use this template]**.

   * (Affichage des publicités uniquement) **À partir de l’onglet [!UICONTROL Templates] :**

      1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

      1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

      1. Placez le curseur sur une carte de modèle, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**.

   La [!UICONTROL Ad Variations Generator] s’ouvre. La zone de travail affiche la section **[!UICONTROL Template Sizes]** avec les formats d’annonce disponibles pour le modèle et une section **[!UICONTROL Ad Concepts]** dans laquelle le contenu généré s’affiche.

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
      >L’assistant d’IA peut générer et modifier du texte (titres, sous-titres, CTA, copie du corps), échanger des images d’arrière-plan, appliquer des couleurs de marque, changer de version de logo et créer de nouveaux modèles de taille. Il ne peut pas modifier la structure du modèle : position des éléments, disposition, espacement, marge intérieure, famille de polices, taille de police ou bordures. Effectuez des modifications structurelles dans l’éditeur de modèles avant de démarrer la session. Voir [&#x200B; Modification d’un modèle &#x200B;](creative-studio-manage-templates.md#edit-template).

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

1. Lorsque les concepts générés vous conviennent, cliquez sur **[!UICONTROL Save Standard Ads]** dans l’en-tête.

   Le bouton est désactivé jusqu’à ce qu’au moins un concept existe.

1. Dans la boîte de dialogue **[!UICONTROL Save Standard Ads]**, spécifiez les paramètres suivants, puis cliquez sur **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** (obligatoire) L’annonceur pour enregistrer les contenus publicitaires sous.

   **[!UICONTROL Creative Library]:** (obligatoire) bibliothèque de contenus publicitaires dans laquelle enregistrer les contenus publicitaires. Le sélecteur de bibliothèque est activé une fois que vous avez sélectionné un annonceur.

   **[!UICONTROL Attach to Bundles]:** (facultatif) Lorsqu’ils sont activés, les contenus publicitaires enregistrés sont associés à un ou plusieurs lots. Pour chaque variation d’annonce publicitaire, sélectionnez un lot ou saisissez un nouveau nom de lot.

   **\[Paramètres de chaque publicité\]:** Pour chaque variation de publicité, vous pouvez afficher et éventuellement modifier les **[!UICONTROL Name],** **[!UICONTROL Language],** et **[!UICONTROL click URL].**

## Modification d’une publicité standard {#edit-standard-ad}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   Un éditeur plein écran s’ouvre avec un aperçu d’annonce publicitaire en direct sur la gauche et un panneau de paramètres sur la droite.

1. Modifiez les paramètres de l’annonce publicitaire à l’aide des onglets **[!UICONTROL Details]** et **[!UICONTROL Attributes]** :

   Onglet **[!UICONTROL Details]** :

   * **[!UICONTROL Creative Name]:** (obligatoire) nom d’affichage du contenu créatif.
   * **[!UICONTROL Language]:** (obligatoire) langue du contenu publicitaire.
   * **[!UICONTROL Creative Size]:** (Lecture seule) Les dimensions de l’annonce publicitaire.
   * **Balises de clic :** si le modèle définit des balises de clic, chaque balise de clic apparaît comme un champ obligatoire intitulé avec le nom de la balise. Saisissez l’URL de destination des clics publicitaires pour chaque balise.
   * **[!UICONTROL Label]:** (facultatif) Libellés pour l’organisation des contenus publicitaires. Sélectionnez des libellés existants ou saisissez une nouvelle balise et cliquez sur **[!UICONTROL Add tag].**

   Onglet **[!UICONTROL Attributes]** :

   L’aperçu en direct se met à jour en temps réel au fur et à mesure que vous le modifiez. L’onglet **[!UICONTROL Attributes]** n’est pas disponible pendant le chargement de l’aperçu.

   * **Attributs de texte :** saisissez la valeur de texte pour chaque calque de texte modifiable défini dans le modèle.
   * **Attributs d’image :** affiche une miniature de l’image actuelle. Cliquez sur **[!UICONTROL Replace Image]** pour charger un remplacement (PNG, JPEG, GIF, WebP ou SVG).

1. Cliquez sur **[!UICONTROL Update Creative]**.

## Générer des variations d’annonces publicitaires pour une annonce publicitaire standard {#generate-ad-variations}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   La [!UICONTROL Ad Variations Generator] s’ouvre avec l’annonce sélectionnée préchargée.

1. Utilisez l’interface de chat de l’IA pour générer et affiner des variations supplémentaires. Voir « [Créer des annonces publicitaires standard](#create-standard-ads) » pour le workflow complet.

## Dupliquer une publicité standard {#duplicate-standard-ad}

Dupliquez une annonce publicitaire standard pour ajouter un nouveau contenu créatif avec les mêmes paramètres à la bibliothèque. Vous pouvez ensuite renommer le nouveau contenu créatif et modifier les paramètres selon vos besoins.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   Le nouveau contenu créatif est nommé `<original name> (copy)`.

## Afficher le journal des modifications d&#39;une publicité standard {#view-change-log}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

   Une boîte de dialogue s’ouvre, affichant un tableau des modifications apportées à la publicité.

## Télécharger une publicité standard {#download-standard-ad}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Les téléchargements créatifs s’effectuent conformément à la procédure normale de votre navigateur.

## Suppression d’une publicité standard {#delete-standard-ad}

>[!NOTE]
>
>Cette action est irréversible.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Dans l’onglet **[!UICONTROL Creatives]** , placez le curseur sur la carte de contenu créatif et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos de Creative Studio dans Advertising Creative](creative-studio-about.md)
>* [Gestion des contenus créatifs dynamiques dans Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Gestion des modèles dans Creative Studio](creative-studio-manage-templates.md)
>* [Gestion des profils de marque dans Advertising Creative](/help/creative/brands/brand-manage.md)

