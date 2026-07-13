---
title: Gestion des modèles d’annonces publicitaires dans Creative Studio
description: Découvrez comment créer, importer, organiser et gérer des modèles d’annonce publicitaire dans l’onglet Modèles de Creative Studio dans Adobe Advertising Creative.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d4a041529615006a79093dccb8690f3b9f5e8cba
workflow-type: tm+mt
source-wordcount: 2512
ht-degree: 2%

---

# Gestion des modèles d’annonce publicitaire dans [!UICONTROL Creative Studio]

*Fonction*

Créez, importez et gérez des modèles d’annonces vidéo et d’affichage à utiliser dans les sessions de génération d’annonces.

## La vue [!UICONTROL Creative Studio] > [!UICONTROL Templates]

L’onglet **[!UICONTROL Templates]** propose des actions rapides pour créer ou importer de nouveaux modèles d’annonces.

L’onglet répertorie également vos modèles d’annonce publicitaire existants au bas de la page <!-- Only in the Templates tab -->en tant que [ cartes individuelles (valeur par défaut) ou tableaux/listes](/help/creative/introduction/customize-data-views.md). La liste des modèles de publicité comprend des onglets pour [!UICONTROL All], [!UICONTROL System Templates] (qui sont chargés sur votre compte par l’équipe chargée de votre compte Adobe) et [!UICONTROL User Templates]. Par défaut, les modèles d’annonces pour tous vos annonceurs s’affichent. Pour afficher uniquement les modèles d’annonce pour un annonceur spécifique, sélectionnez dans la liste des annonceurs en haut de la page.

<!-- 
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### Actions disponibles

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Création :

* [Importer des modèles d’annonces HTML5](#templates-import)

* [Création manuelle d’un modèle d’annonce](#template-create)

Actions sur vos modèles existants :

* [Générer des variations d’annonce publicitaire à partir d’un modèle d’annonce publicitaire affichée](#ad-variations-generate)

* [Modification d’un modèle de publicité](#template-edit)

* [Ajout ou suppression de libellés pour un modèle d’annonce publicitaire](#template-labels)

* [Aperçu d’un modèle d’annonce publicitaire](#template-preview)

* [Télécharger un modèle d’annonce publicitaire](#template-download)

* [Ajouter ou supprimer un modèle d’annonce publicitaire en tant que favori](#template-favorite)

* [Supprimer un modèle d’annonce publicitaire](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## Importer des modèles d’annonces HTML5 {#templates-import}

Chargez un ou plusieurs modèles HTML5 préconfigurés sous forme de fichiers ZIP. Les modèles sont validés lors de l’importation. L’importation échoue si l’HTML dépasse 200 000 caractères, le CSS dépasse 60 000 caractères, le modèle contient plus de 5 000 éléments DOM ou le modèle inclut des balises de script non prises en charge.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Sélectionnez l’annonceur en haut de la page.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Dans la zone de **[!UICONTROL Upload HTML5 Templates]**, cliquez sur **[!UICONTROL Upload]**, puis sélectionnez **[!UICONTROL Display Ad Template]** ou **[!UICONTROL Video Ad Template]**.

1. Sélectionnez un ou plusieurs fichiers ZIP sur votre appareil ou réseau.

1. Dans la boîte de dialogue **[!UICONTROL Import Templates]** :

   1. Sélectionnez un **[!UICONTROL Advertiser]**.

      Si vous avez déjà sélectionné un annonceur spécifique en haut de la page, cet annonceur est présélectionné.

   1. (Facultatif) Modifiez le **[!UICONTROL Template Name]** pour chaque fichier.

      Le nom de fichier est utilisé par défaut.

   1. (Facultatif) Pour ajouter d’autres fichiers, cliquez sur **[!UICONTROL Add more]** et sélectionnez des fichiers ZIP supplémentaires. Spécifiez le **[!UICONTROL Template Name]** pour chaque fichier supplémentaire.

1. Cliquez sur **[!UICONTROL Import Templates]**.

>[!NOTE]
>
>Si l’importation échoue, simplifiez le modèle ou contactez l’équipe chargée de votre compte Adobe.

## Création manuelle d’un modèle d’annonce {#template-create}

Créez un modèle d’affichage ou de vidéo vierge à l’aide de l’éditeur de modèles.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Dans la zone de **[!UICONTROL Create New Ad Template]**, cliquez sur **[!UICONTROL Create]**, puis sélectionnez **[!UICONTROL Display Ad Template]** ou **[!UICONTROL Video Ad Template]**.

1. (Afficher les publicités) Sélectionnez la taille du modèle de publicité, puis cliquez sur **[!UICONTROL Continue]**.

1. Configurez les paramètres du modèle à l’aide des commandes [dans l’éditeur de modèles](#template-controls).

1. (Facultatif) Pour télécharger une copie du modèle tel que défini, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

1. Enregistrez le modèle :

   1. Effectuez l’une des opérations suivantes :

      * Cliquez sur **[!UICONTROL Save]**.

      * Pour enregistrer le modèle en tant que brouillon, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**.

   1. Saisissez la **[!UICONTROL Template name]**, sélectionnez le **[!UICONTROL Advertiser]**, sélectionnez éventuellement les balises existantes ou ajoutez de nouvelles balises au modèle, puis cliquez sur **[!UICONTROL Save]**.

## Modification d’un modèle de publicité {#template-edit}

*Afficher uniquement les modèles d’annonce publicitaire.*

>[!IMPORTANT]
>
>L’agent AI ne peut pas modifier la disposition du modèle, la position des éléments, l’espacement ou la typographie. Apportez les modifications structurelles nécessaires dans l’éditeur de modèles avant de générer le contenu.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de carte ou de tableau du modèle, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Template]**.

1. Modifiez la disposition du modèle ou les éléments à l’aide des contrôles [dans l’éditeur de modèles](#template-controls).

1. (Facultatif) Pour télécharger une copie du modèle tel que défini, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

1. Enregistrez le modèle :

   * Cliquez sur **[!UICONTROL Save]**.

   * Pour enregistrer le modèle en tant que brouillon, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**. Saisissez la **[!UICONTROL Template name]**, sélectionnez le **[!UICONTROL Advertiser]**, sélectionnez éventuellement les balises existantes ou ajoutez de nouvelles balises au modèle, puis cliquez sur **[!UICONTROL Save]**.

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## Contrôles de l’éditeur de modèles {#template-controls}

Les éditeurs de modèle d’affichage et de vidéo partagent la même barre d’outils d’actions générales au-dessus de la zone de travail d’édition et du panneau [!UICONTROL Layers] à droite. Le panneau de gauche, les commandes de modification des modèles et la chronologie diffèrent entre les modèles d’affichage et vidéo.

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### Barre d’outils des actions générales

La barre d’outils des actions générales se trouve au-dessus de la zone de travail d’édition de l’éditeur de modèles d’annonces et est divisée en deux parties (gauche et droite).

#### Afficher les modèles de publicité

| Contrôle | Description |
| --- | --- |
| **[!UICONTROL Undo]** | Annule la dernière action. |
| ![Rétablir](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | Rétablit la dernière action annulée. |
| **[!UICONTROL Links]** | Ouvre un panneau permettant de gérer les URL de clics publicitaires associées aux éléments du modèle. |
| Contrôles de zoom | Cliquez sur **[!UICONTROL Zoom out]** ou **[!UICONTROL Zoom in]** pour ajuster le zoom de la zone de travail (10 à 150 %, par incréments de 10 %). Cliquez sur le libellé de niveau de zoom, qui indique **[!UICONTROL Auto]** lorsque la zone de travail s’ajuste automatiquement, ou un pourcentage lorsqu’il est défini manuellement, pour ouvrir un menu avec des options : **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** et **[!UICONTROL Zoom Out]**. |
| Taille de l’annonce | Affiche les dimensions d’annonce publicitaire actuelles (par exemple, 300 × 250). Cliquez pour ouvrir le sélecteur de taille, qui propose six tailles standard IAB couramment utilisées en tant que cartes, ainsi qu&#39;une liste déroulante avec les 19 tailles standard d&#39;annonces publicitaires IAB. La taille par défaut des nouveaux modèles est de 300 × 250 (rectangle Medium). |
| ![Ouverture du panneau Calques](/help/creative/assets/layers-panel-open.png "ouverture du panneau Calques") | Ouvre le panneau [!UICONTROL Layers]. S’affiche uniquement lorsque le panneau [!UICONTROL Layers] est fermé. |

#### Modèles de publicité vidéo

| Contrôle | Description |
| --- | --- |
| **[!UICONTROL Undo]** / ![Rétablir](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | Annule ou rétablisse la dernière action. |
| Contrôles de zoom | Cliquez sur **[!UICONTROL Zoom out]** ou **[!UICONTROL Zoom in]** pour ajuster le zoom de la zone de travail. Cliquez sur le niveau de zoom pour ouvrir un menu avec les options suivantes : **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** et **[!UICONTROL Zoom Out]**. |
| ![Ouverture du panneau Calques](/help/creative/assets/layers-panel-open.png "ouverture du panneau Calques") | Ouvre le panneau [!UICONTROL Layers]. S’affiche uniquement lorsque le panneau [!UICONTROL Layers] est fermé. |

<!-- Not there as of 7/10:  | **[!UICONTROL Preview]** | Opens a preview of the video template. | -->

### Panneau de gauche

Le panneau de gauche contient une colonne d’icônes. Cliquez sur une icône pour ouvrir son panneau de contenu ; cliquez de nouveau sur la même icône pour le fermer.

#### Afficher les modèles de publicité

| Icon | Description |
| --- | --- |
| **[!UICONTROL Search]** | Effectuez une recherche dans tous les types de ressources de votre bibliothèque. |
| **[!UICONTROL Upload]** | Chargez des images ou des fichiers de polices dans l’éditeur pour les utiliser dans le modèle actif. Vous pouvez charger jusqu’à 20 fichiers à la fois. |
| **[!UICONTROL Templates]** | Parcourez les modèles d’annonces de votre bibliothèque Creative Studio à utiliser comme calque de base ou élément de référence. |
| **[!UICONTROL My Assets]** | Parcourez toutes les ressources que vous avez chargées dans l’onglet Assets de Creative Studio. |
| **[!UICONTROL Images]** | Parcourez uniquement les ressources d’image que vous avez chargées dans l’onglet Assets de Creative Studio. |
| **[!UICONTROL Text]** | Ajoutez un élément de texte à la zone de travail, y compris les polices personnalisées que vous avez chargées. |
| **[!UICONTROL Elements]** | Ajouter des formes et des éléments de disposition tels que des boutons et des rectangles. |

Vous pouvez faire glisser un élément de n’importe quel panneau directement sur la zone de travail ou cliquer dessus pour le placer à une position par défaut.

#### Modèles de publicité vidéo

| Icon | Description |
| --- | --- |
| **[!UICONTROL Search]** | Effectuez une recherche dans tous les types de ressources de votre bibliothèque. |
| **[!UICONTROL Upload]** | Chargez les fichiers image, vidéo, audio ou de police (TTF, OTF, WOFF, WOFF2) dans l’éditeur pour les utiliser dans le modèle actif. Vous pouvez charger jusqu’à 20 fichiers à la fois. |
| **[!UICONTROL Templates]** | Parcourez les modèles d’annonces publicitaires depuis votre bibliothèque Creative Studio. |
| **[!UICONTROL My Assets]** | Parcourez toutes les ressources que vous avez chargées dans l’onglet Assets de Creative Studio. |
| **[!UICONTROL Images]** | Parcourez uniquement les ressources d’image que vous avez chargées dans l’onglet Assets de Creative Studio. |
| **[!UICONTROL Video]** | Parcourez uniquement les ressources vidéo que vous avez chargées dans l’onglet Assets de Creative Studio. |
| **[!UICONTROL Audio]** | Parcourez uniquement les ressources audio que vous avez chargées dans l’onglet Assets de Creative Studio. |
| **[!UICONTROL Text]** | Ajoutez un élément de texte à la zone de travail, y compris les polices personnalisées que vous avez chargées. |
| **[!UICONTROL Elements]** | Ajoutez des formes et des éléments vectoriels. |

Vous pouvez faire glisser un élément de n’importe quel panneau directement sur la zone de travail ou cliquer dessus pour le placer à une position par défaut.

### Ajouter des contrôles d&#39;édition de modèles

Cliquez sur un élément de la zone de travail d’édition pour le sélectionner. Selon le type de modèle, une ou plusieurs barres d’outils s’affichent avec des contrôles pour cet élément.

#### Barre d’outils et panneau Inspecteur

Les commandes varient selon le type d’élément.

<!-- From inspectorbar.ts -->

##### Afficher les modèles de publicité

| Contrôle | Types d’éléments | Description |
| --- | --- | --- |
| **[!UICONTROL Properties]** | Tous | Ouvre un panneau pour modifier le nom du calque, marquer le calque comme dynamique (permutable pendant la génération de la publicité) et définir une URL de clic publicitaire (liens uniquement). En dessous, choisissez un état **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** ou **[!UICONTROL Focus]** pour mettre en forme l’élément pour cet état d’interaction, puis ajustez le style (typographie (texte et liens uniquement), les décorations (remplissage, bordure, rayon de coin), les dimensions, la position) en fonction du type d’élément. |
| **[!UICONTROL Effects]** | Tous | Ouvre un panneau dans lequel vous choisissez un état **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** ou **[!UICONTROL Focus]** auquel appliquer des effets pour cet état d’interaction, puis ajustez les sections **[!UICONTROL Transform]**, **[!UICONTROL Transition]**, **[!UICONTROL Box Shadow]**, **[!UICONTROL Filter]**, **[!UICONTROL Blend Mode]** et **[!UICONTROL Cursor]**. Les éléments de texte incluent également une section **[!UICONTROL Text Shadow]**. |
| **[!UICONTROL Animations]** | Tous | Ouvre un panneau pour définir l’heure d’entrée et de sortie du calque sur le montage et pour configurer les paramètres prédéfinis de **[!UICONTROL Entrance Animation]**, de **[!UICONTROL Loop Animation]** et de **[!UICONTROL Exit Animation]** avec la durée et l’accélération. Inclut des actions **[!UICONTROL Copy]**, **[!UICONTROL Paste]** et **[!UICONTROL Reset]**. |
| **[!UICONTROL Crop]** | Images | Ouvre une barre d’outils pour recadrer l’image. Sélectionnez un paramètre prédéfini de **[!UICONTROL Aspect Ratio]** (ou **[!UICONTROL Free]**), puis cliquez sur **[!UICONTROL Apply]** ou **[!UICONTROL Cancel]**. |
| **[!UICONTROL Position]** | Tous | Ouvre un menu avec des options **[!UICONTROL Move]** (**[!UICONTROL Forward]**, **[!UICONTROL Backward]**, **[!UICONTROL To front]**, **[!UICONTROL To back]**), des options **[!UICONTROL Align to Page]** (**[!UICONTROL Top]**, **[!UICONTROL Left]**, **[!UICONTROL Middle]**, **[!UICONTROL Center]**, **[!UICONTROL Bottom]**, **[!UICONTROL Right]**, **[!UICONTROL Fit Vertically]**, **[!UICONTROL Fit Horizontally]**, **[!UICONTROL Fit to Page]**, **[!UICONTROL Layer Level Alignment]**, **[!UICONTROL Fit to Content]**) et, pour les éléments qui ne sont pas des images, des options (les mêmes six options d’alignement, plus). |

##### Modèles de publicité vidéo

| Contrôle | Types d’éléments | Description |
| --- | --- | --- |
| **[!UICONTROL Shape]** | Formes | Définit des options spécifiques à la forme. |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | Plusieurs éléments sélectionnés ou un groupe | Regroupe les éléments sélectionnés ou dissocie un groupe sélectionné. |
| **[!UICONTROL Combine]** | Formes compatibles | Combine les formes sélectionnées en une seule forme. |
| **[!UICONTROL Audio replace]** | Audio et vidéo | Remplace la piste audio par un fichier de votre bibliothèque de ressources. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | Texte | Ajuste la famille de polices, l’épaisseur, la taille, l’alignement horizontal et d’autres paramètres de typographie avancés. |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | Images et vidéo | Définit l’image de remplissage ou la source vidéo de l’élément. |
| **[!UICONTROL Trim]** | Vidéo et audio | Ouvre le mode de rognage pour définir les points de début et de fin de l’élément. |
| ![Volume](/help/creative/assets/volume.png "Volume") ([!UICONTROL Volume]) | Vidéo et audio | Ajuste le niveau audio. |
| ![Vitesse de lecture](/help/creative/assets/speed.png "Vitesse de lecture") ([!UICONTROL Playback speed]) | Vidéo et audio | Ajuste le taux de lecture. |
| ![Crop](/help/creative/assets/crop.png "Crop") ([!UICONTROL Crop]) | Tous | Recadre l’élément dans une zone personnalisée. |
| ![Contour](/help/creative/assets/stroke.png "Contour") ([!UICONTROL Stroke]) | Tous | Définit la couleur et la largeur de la bordure. |
| **[!UICONTROL Text Background]** | Texte | Ajoute une couleur de fond derrière le texte. |
| **[!UICONTROL Animations]** | Tous | Ajoute ou modifie des animations d’entrée, de sortie ou en boucle. |
| **[!UICONTROL Style]** | Tous | Ouvre un menu avec des options **[!UICONTROL Adjustments]**, **[!UICONTROL Filter]**, **[!UICONTROL Effect]** et **[!UICONTROL Blur]**. |
| **[!UICONTROL Shadow]** | Tous | Ajoute ou modifie une ombre portée. |
| **[!UICONTROL Opacity]** | Tous | Définit le niveau de transparence de l’élément. |
| **[!UICONTROL Position]** | Tous | Ajuste numériquement la taille, la position et la rotation de l’élément. |

#### Contrôles généraux d&#39;édition

##### Afficher les modèles de publicité

| Action | Description |
| --- | --- |
| **[!UICONTROL Replace]** | (Éléments d’image uniquement) Ouvre le panneau Images afin que vous puissiez remplacer l’image par une de votre bibliothèque de ressources. |
| ![Avancer](/help/creative/assets/cs-icon-move-forward.png) **[!UICONTROL Move forward]** | Déplace l’élément d’un pas en avant dans l’ordre d’empilement (vers l’avant). |
| ![Revenir en arrière](/help/creative/assets/cs-icon-move-backward.png) **[!UICONTROL Move backward]** | Déplace l’élément d’un pas en arrière dans l’ordre d’empilement (vers l’arrière). |
| ![Dupliquer](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate]** | Crée une copie de l’élément. |
| ![Supprimer](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete]** | Supprime l’élément de la zone de travail. |

Vous pouvez également faire glisser un élément sélectionné pour le repositionner et faire glisser les poignées autour pour le redimensionner.

##### Modèles de publicité vidéo

| Action | Description |
| --- | --- |
| **[!UICONTROL Edit text]** | (Éléments de texte uniquement) Passe en mode d’édition de texte afin que vous puissiez saisir et mettre en forme du texte directement sur la zone de travail. En mode d’édition de texte, un menu secondaire fournit des **[!UICONTROL Text color]**, des **[!UICONTROL Bold]**, des **[!UICONTROL Italic]** et des **[!UICONTROL Text variables]** (espaces réservés de modèle). |
| **[!UICONTROL Replace]** | (Éléments d’image uniquement) Ouvre la bibliothèque de ressources afin que vous puissiez intervertir l’image. |
| **[!UICONTROL Bring forward]** | Déplace l’élément d’un pas en avant dans l’ordre d’empilement. |
| **[!UICONTROL Send backward]** | Déplace l’élément d’un pas en arrière dans l’ordre d’empilement. |
| **[!UICONTROL Duplicate]** | Crée une copie de l’élément. |
| **[!UICONTROL Delete]** | Supprime l’élément de la zone de travail. |
| **... >[!UICONTROL Flip horizontal]** | Retourne l&#39;élément horizontalement de 180 degrés. |
| **... >[!UICONTROL Flip vertical]** | Retourne l&#39;élément verticalement de 180 degrés. |
| **... >[!UICONTROL Copy Element]** | Copie l’élément dans le presse-papiers de la zone de travail. |
| **... >[!UICONTROL Pastes Element]** | Colle l’élément copié. |

Vous pouvez également faire glisser un élément sélectionné pour le repositionner et faire glisser les poignées autour pour le redimensionner.

### Chronologie

Les éditeurs vidéo et d’affichage affichent tous deux un panneau Chronologie au bas de la zone de travail.

#### Afficher les modèles de publicité

La chronologie affiche une piste pour chaque calque de la zone de travail, couvrant la période pendant laquelle le calque est visible en fonction de sa synchronisation d’animation d’entrée et de sortie. Faites glisser la poignée de début ou de fin d’une piste pour ajuster son heure d’entrée ou de sortie, ou faites glisser une piste pour réorganiser les calques. Cliquez sur la règle ou faites glisser le curseur de lecture pour vous déplacer vers un point dans le temps.

La barre d’outils de la chronologie comprend un champ **[!UICONTROL Duration]** (0 à 60 secondes), **[!UICONTROL Play]**/**[!UICONTROL Pause]**, un affichage de la durée actuelle/totale, un bouton bascule de boucle, des commandes de zoom **[!UICONTROL Timeline Scale]**, un bouton de **[!UICONTROL Fit View]** et un bouton bascule de réduction/développement.

#### Modèles de publicité vidéo

La chronologie affiche tous les clips vidéo et audio du modèle. Utilisez la chronologie pour vérifier la disposition des éléments dans le temps et les rogner en faisant glisser leurs poignées de début et de fin. Vous ne pouvez pas ajouter un nouvel élément directement sur le montage ; ajoutez-le plutôt à partir du panneau de gauche ou de la zone de travail, puis il s’affiche sous la forme d’un élément sur le montage.

### panneau [!UICONTROL Layers]

Le panneau [!UICONTROL Layers] sur le côté droit de la zone de travail répertorie tous les éléments du modèle et vous permet de gérer leur ordre, leur visibilité et leurs propriétés. Pour les modèles d’affichage, cliquez sur **[!UICONTROL Open Layers]** dans la barre d’outils de la zone de travail pour l’ouvrir. Pour les modèles vidéo, le panneau est ouvert par défaut.

Cliquez sur un calque pour sélectionner l’élément correspondant sur la zone de travail.

**Onglets (modèles d’annonce publicitaire affichés uniquement)**

Les modèles d’affichage comportent deux onglets dans la partie supérieure du panneau [!UICONTROL Layers] :

* **[!UICONTROL Dynamic]** : répertorie uniquement les calques qui peuvent être permutés pendant la génération de l’annonce, tels que les images et le texte que l’agent d’IA peut remplacer. Il s’agit de la vue par défaut pour la génération des variations de publicité.
* **[!UICONTROL All]** : affiche la hiérarchie complète des calques du modèle, y compris les conteneurs structurels. Utilisez cette vue pour examiner ou réorganiser la manière dont les éléments sont imbriqués.

Les modèles vidéo affichent tous les calques dans une seule liste sans onglets.

**Actions par couche**

Placez le curseur sur un calque pour afficher les actions suivantes :

| Action | Description |
| --- | --- |
| ![Renommer le calque](/help/creative/assets/edit.png) **[!UICONTROL Rename layer]** | Permet de saisir un nouveau nom de calque dans le panneau. |
| ![Verrouiller le calque](/help/creative/assets/cs-icon-lock.png) **[!UICONTROL Lock layer]** / ![Déverrouiller le calque](/help/creative/assets/cs-icon-unlock.png) **[!UICONTROL Unlock layer]** | Empêche ou autorise le déplacement, la modification ou la réorganisation du calque. |
| ![Masquer le calque](/help/creative/assets/cs-icon-hidden.png) **[!UICONTROL Hide layer]** / ![Afficher le calque](/help/creative/assets/cs-icon-visible.png) **[!UICONTROL Show layer]** | Masque ou affiche le calque sur la zone de travail. Les calques masqués sont conservés dans le modèle, mais n’apparaissent pas lors du rendu du modèle. |
| ![Faire glisser pour réorganiser](/help/creative/assets/cs-icon-drag.png) Faire glisser pour réorganiser | (Affichage des modèles publicitaires uniquement) Faites glisser l’icône de réorganisation pour modifier la position du calque dans l’ordre d’empilement. Le calque doit être déverrouillé pour le réorganiser. |

**Pied de page du panneau**

| Action | Description |
| --- | --- |
| ![Dupliquer le calque sélectionné](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate selected layer]** | Crée une copie du calque sélectionné. |
| ![Supprimer le calque sélectionné](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete selected layer]** | Supprime le calque sélectionné. |
| **[!UICONTROL Group selected layers]** (modèles vidéo uniquement) | Regroupe plusieurs calques sélectionnés en un seul groupe. S’affiche uniquement lorsque plusieurs calques sont sélectionnés. Vous pouvez dissocier des calques groupés ou supprimer des calques individuels du groupe à l’aide des commandes de la ligne du groupe. |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

## Générer des variations d’annonce publicitaire à partir d’un modèle d’annonce publicitaire affichée {#ad-variations-generate}

*Afficher uniquement les modèles d’annonce publicitaire.*

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de carte ou de tableau du modèle, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   La [!UICONTROL Ad Variations Generator] s’ouvre avec le modèle préchargé.

1. Utilisez l’interface de chat de l’IA pour générer et affiner le contenu publicitaire. Voir « [ Gérer les publicités standard dans Creative Studio ](creative-studio-manage-standard-ads.md) » pour le workflow complet.

## Ajout ou suppression de libellés pour un modèle d’annonce publicitaire {#template-labels}

*Afficher uniquement les modèles d’annonce publicitaire.*

Les libellés vous permettent d’organiser et de filtrer les modèles utilisateur. Vous ne pouvez pas ajouter de libellés aux modèles système.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de carte ou de tableau du modèle, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**.

1. Dans la boîte de dialogue **[!UICONTROL Edit Labels]** :

   * Pour ajouter un libellé, sélectionnez un libellé existant ou saisissez un nom dans le champ de saisie, puis cliquez sur **[!UICONTROL Add Tag]**.

   * Pour supprimer un libellé, cliquez sur **[!UICONTROL X]** en regard de la balise de libellé.

1. Cliquez sur **[!UICONTROL Save]**.

## Aperçu d’un modèle d’annonce publicitaire {#template-preview}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la carte du modèle.

1. Effectuez l’une des opérations suivantes :

   * (Mode Carte) Cliquez sur l’icône **[!UICONTROL Preview template]** ou sur **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

   * (Vue Tableau) Cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

1. Pour les modèles vidéo, cliquez sur ![Lire](/help/creative/assets/play.png "Lire").

## Télécharger un modèle d’annonce publicitaire {#template-download}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de carte ou de tableau du modèle, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Le modèle est téléchargé sous la forme d’un fichier ZIP conformément à la procédure normale de votre navigateur.

## Ajouter ou supprimer un modèle d’annonce publicitaire en tant que favori {#template-favorite}

*Mode Carte uniquement*

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la carte du modèle.

1. Effectuez l’une des opérations suivantes :

   * Pour ajouter un modèle en tant que favori, cliquez sur ![Favori](/help/creative/assets/favorite-null.png).

   * Pour supprimer un modèle en tant que favori, cliquez sur ![Favori](/help/creative/assets/favorite.png).

## Supprimer un modèle d’annonce publicitaire {#template-delete}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de carte ou de tableau du modèle, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos de Creative Studio dans Advertising Creative](creative-studio-about.md)
>* [Gestion des ressources dans Creative Studio](creative-studio-manage-assets.md)
>* [Gestion des publicités standard dans Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gestion des contenus créatifs dynamiques dans Creative Studio](creative-studio-manage-dynamic-ads.md)

