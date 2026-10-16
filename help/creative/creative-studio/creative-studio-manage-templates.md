---
title: Gestion des modèles d’annonces publicitaires dans Creative Studio
description: Découvrez comment créer, importer, organiser et gérer des modèles d’annonces publicitaires dans Adobe Advertising Creative.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8fa8d6c66228d3a0af1de2514dd016d8f50262e8
workflow-type: tm+mt
source-wordcount: '3702'
ht-degree: 1%
---
# Gestion des modèles d’annonce publicitaire dans [!UICONTROL Creative Studio]

Créez, importez et gérez des modèles d’annonces vidéo et d’affichage à utiliser dans les sessions de génération d’annonces.

## La vue [!UICONTROL Creative Studio] > [!UICONTROL Templates]

L’onglet **[!UICONTROL Templates]** propose des actions rapides pour créer ou importer de nouveaux modèles d’annonces.

L’onglet [!UICONTROL Templates] répertorie également vos modèles d’annonces existants au bas de la page <!-- Only in the Templates tab -->en tant que [&#x200B; cartes individuelles (valeur par défaut) ou tableaux/listes](/help/creative/introduction/customize-data-views.md). La liste des modèles de publicité comprend des onglets pour [!UICONTROL All], [!UICONTROL System Templates] (que l’équipe chargée de votre compte Adobe charge sur votre compte) et [!UICONTROL User Templates]. Par défaut, les modèles d’annonces pour tous vos annonceurs s’affichent. Pour afficher uniquement les modèles d’annonce pour un annonceur spécifique, sélectionnez dans la liste des annonceurs en haut de la page.

<!--
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### Actions disponibles

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Création :

* [Générer un modèle d’annonce publicitaire à l’aide de l’IA](#template-generate)

* [Création manuelle d’un modèle d’annonce](#template-create)

* [Importer des modèles d’annonces HTML5](#templates-import)

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

## Générer un modèle d’annonce publicitaire à l’aide de l’IA {#template-generate}

*Fonction*

Utilisez l’IA dans [!UICONTROL Creative Studio] pour convertir une image d’annonce publicitaire à affichage statique existante en modèle d’annonce publicitaire à affichage modifiable. Un assistant en trois étapes vous permet de générer et de réviser le modèle, de demander des modifications à l’aide du langage naturel et d’ouvrir l’éditeur de modèles pour apporter des modifications manuelles et enregistrer le modèle.

### Conditions préalables

Vous avez besoin d’une publicité d’images statique dans une bibliothèque Creative. Ce workflow sélectionne des publicités dans vos bibliothèques ; il ne charge pas de nouvelle image directement dans la boîte de dialogue de génération.

<!--

Publish this when prompt-based generation becomes available:

To generate a template from an existing image, you need a static image ad in a Creative Library. This option selects ads from your libraries; it doesn't upload a new image directly in the generation dialog. You don't need an existing ad image to generate a template from a prompt.

-->

### Étape 1 : générer et réviser le modèle

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. (Facultatif) Sélectionnez un annonceur dans la liste des annonceurs située en haut de la page pour afficher ses bibliothèques.

1. Dans la zone de **[!UICONTROL Use AI to Generate a New Display Ad Template]**, cliquez sur **[!UICONTROL Generate]**.

1. Dans la boîte de dialogue **[!UICONTROL Generate New Ad Template]**, sélectionnez **[!UICONTROL Generate from Existing Standard Ad Image]** s’il n’est pas déjà sélectionné.

1. Sélectionnez la bibliothèque contenant l’annonce publicitaire d’image dans la liste **[!UICONTROL Ad Library]** .

1. Placez le curseur sur la carte publicitaire de l’image, puis cliquez sur **[!UICONTROL Use this Standard Ad]**.

   La génération commence automatiquement, en utilisant la largeur et la hauteur de l’annonce sélectionnée.

<!--

Switch to this when prompt-based generation becomes available:

1. In the **[!UICONTROL Generate New Ad Template]** dialog, choose how to generate the template:

   * **[!UICONTROL Generate from Prompt]:** Describe the ad template you want to create using a text prompt.

   * **[!UICONTROL Generate from Existing Standard Ad Image]:** Convert an existing static image ad into an editable template.

1. Follow the steps for your selected option:

   * From a prompt:

      1. Enter a description of the template you want to create. Include details such as the layout, headline, call to action, and visual style.

      1. Follow the on-screen instructions to generate the template.

   * From an existing standard ad image:

      1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

      1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

         Generation begins automatically, using the selected ad's width and height.

-->

1. [Examinez et affinez le modèle généré](#template-review).

### Étape 2 : examiner et affiner le modèle {#template-review}

1. Attendez la fin de la génération, puis passez en revue l’aperçu du modèle et le panneau **[!UICONTROL Layers]**, le cas échéant.

   Vérifiez le texte, les images et la mise en page avant d’utiliser le modèle. Les calques affichés ici sont à réviser ; effectuez des modifications manuelles dans l’éditeur de modèles.

1. (Facultatif) Demandez des modifications au modèle généré :

   1. Dans le champ **[!UICONTROL Ask the AI for any changes]** , décrivez les modifications que vous souhaitez apporter. Par exemple, saisissez `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Cliquez sur **[!UICONTROL Regenerate]**.

   1. Vérifiez l’aperçu mis à jour. Répétez l’opération si nécessaire.

1. Lorsque vous êtes prêt à continuer, cliquez sur **[!UICONTROL Use this Ad Template]**.

   Le modèle généré s’ouvre dans l’éditeur de modèles d’affichage.

### Étape 3 : modifier et enregistrer le modèle {#template-save}

>[!TIP]
>
> L’assistant d’IA utilise une bibliothèque de polices open source pour trouver une correspondance proche pour la police de votre publicité. Pour utiliser votre propre police, chargez-la dans l’onglet [!UICONTROL Assets] ou à partir de l’éditeur de modèles, puis remplacez la police générée dans l’éditeur.
>
> Pour de meilleurs résultats, remplacez le logo généré par l’IA par votre logo original, parfait en pixels, dans l’éditeur de modèles.

1. Dans l’éditeur de modèles, passez en revue les éléments générés et apportez les modifications restantes à l’aide des commandes de l’[éditeur de modèles](#template-controls).

1. Cliquez sur **[!UICONTROL Save]**.

1. Dans la boîte de dialogue **[!UICONTROL Update Template]**, saisissez ou mettez à jour le **[!UICONTROL Template name]**, sélectionnez le **[!UICONTROL Advertiser]** et ajoutez éventuellement des balises.

1. Cliquez sur **[!UICONTROL Update]** pour enregistrer le modèle et revenir à la vue **[!UICONTROL Templates]**.

   Pour enregistrer une copie distincte à la place, cliquez sur **[!UICONTROL Save As New]**.

Vous pouvez ensuite utiliser le modèle pour [générer des variations d’annonce publicitaire](#ad-variations-generate).

### Si vous ne pouvez pas générer de modèle {#troubleshooting}

| Problème | Que faire |
| --- | --- |
| Aucune bibliothèque ni publicité d’images n’est répertoriée lors de la génération à partir d’une image | Vérifiez l’annonceur et le **[!UICONTROL Ad Library]** sélectionnés. Si la bibliothèque ne comporte pas d’images d’annonce publicitaire standard, sélectionnez une autre bibliothèque contenant une annonce d’image statique existante. |
| La génération basée sur l’image échoue ou l’image ne peut pas être convertie | Vérifiez le message affiché, cliquez sur **[!UICONTROL Back to library]**, puis sélectionnez une annonce publicitaire d’image pour réessayer. |

<!--

Add when prompt-based generation is available:

| Prompt-based generation fails | Review the displayed message and revise your prompt before trying again. |

-->

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

## Générer des variations d’annonce publicitaire à partir d’un modèle d’annonce publicitaire affichée {#ad-variations-generate}

*Afficher uniquement les modèles d’annonce publicitaire.*

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de carte ou de tableau du modèle, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   La [!UICONTROL Ad Variations Generator] s’ouvre avec le modèle préchargé.

1. Utilisez l’interface de chat de l’IA pour générer et affiner le contenu publicitaire. Voir « [&#x200B; Gérer les publicités standard dans Creative Studio &#x200B;](creative-studio-manage-standard-ads.md) » pour le workflow complet.

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

   * Pour ajouter un modèle comme favori, cliquez sur ![Favori](/help/creative/assets/favorite-null.png "Favori").

   * Pour supprimer un modèle comme favori, cliquez sur ![Favori](/help/creative/assets/favorite.png "Favori").

## Supprimer un modèle d’annonce publicitaire {#template-delete}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. Placez le curseur sur la ligne de carte ou de tableau du modèle, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Contrôles de l’éditeur de modèles {#template-controls}

Les éditeurs de modèle d’affichage et de vidéo fournissent une barre d’outils au-dessus de la zone de travail pour annuler les modifications et ajuster l’affichage, des panneaux à gauche pour ajouter des ressources et des éléments et un panneau [!UICONTROL Layers] à droite pour gérer les calques. Les outils de modification des éléments sélectionnés et de contrôle de la durée et de la lecture diffèrent entre les modèles d’affichage et vidéo.

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

### Annuler les modifications et ajuster la vue de la zone de travail

La barre d’outils des actions générales se trouve au-dessus de la zone de travail d’édition de l’éditeur de modèles d’annonces et est divisée en deux parties (gauche et droite).

#### Afficher les modèles de publicité

| Contrôle | Description |
| --- | --- |
| **[!UICONTROL Undo]** | Annule la dernière action. |
| ![Rétablir](/help/creative/assets/cs-icon-redo.png "Rétablir") **[!UICONTROL Redo]** | Rétablit la dernière action annulée. |
| **[!UICONTROL Links]** | Ouvre un panneau permettant de gérer les URL de clics publicitaires associées aux éléments du modèle. |
| Contrôles de zoom | Cliquez sur **[!UICONTROL Zoom out]** ou **[!UICONTROL Zoom in]** pour ajuster le zoom de la zone de travail (10 à 150 %, par incréments de 10 %). Cliquez sur le libellé de niveau de zoom, qui indique **[!UICONTROL Auto]** lorsque la zone de travail s’ajuste automatiquement, ou un pourcentage lorsqu’il est défini manuellement, pour ouvrir un menu avec des options : **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** et **[!UICONTROL Zoom Out]**. |
| Taille de l’annonce | Affiche les dimensions d’annonce publicitaire actuelles (par exemple, 300 × 250). Cliquez pour ouvrir le sélecteur de taille, qui propose six tailles standard IAB couramment utilisées en tant que cartes, ainsi qu&#39;une liste déroulante avec les 19 tailles standard d&#39;annonces publicitaires IAB. La taille par défaut des nouveaux modèles est de 300 × 250 (rectangle Medium). |
| ![Ouverture du panneau Calques](/help/creative/assets/layers-panel-open.png "ouverture du panneau Calques") | Ouvre le panneau [!UICONTROL Layers]. S’affiche uniquement lorsque le panneau [!UICONTROL Layers] est fermé. |

#### Modèles de publicité vidéo

| Contrôle | Description |
| --- | --- |
| **[!UICONTROL Undo]** / ![Rétablir](/help/creative/assets/cs-icon-redo.png "Rétablir") **[!UICONTROL Redo]** | Annule ou rétablisse la dernière action. |
| Contrôles de zoom | Cliquez sur **[!UICONTROL Zoom out]** ou **[!UICONTROL Zoom in]** pour ajuster le zoom de la zone de travail. Cliquez sur le niveau de zoom pour ouvrir un menu avec les options suivantes : **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** et **[!UICONTROL Zoom Out]**. |
| ![Ouverture du panneau Calques](/help/creative/assets/layers-panel-open.png "ouverture du panneau Calques") | Ouvre le panneau [!UICONTROL Layers]. S’affiche uniquement lorsque le panneau [!UICONTROL Layers] est fermé. |

<!--

Not there as of 10/15:

| Page resize | Opens the page-size controls to change the video template dimensions. |
| **[!UICONTROL Preview]** | Opens a preview of the video template. |

   -->

### Ajout de ressources et d’éléments

Le panneau de gauche vous permet d’ajouter des ressources et des éléments au modèle. Cliquez sur une icône pour ouvrir son panneau de contenu ; cliquez de nouveau sur la même icône pour le fermer.

#### Afficher les modèles de publicité

| Icon | Description |
| --- | --- |
| **[!UICONTROL Search]** | Effectuez une recherche dans tous les types de ressources de votre bibliothèque. |
| **[!UICONTROL Upload]** | Chargez des images ou des fichiers de polices dans l’éditeur pour les utiliser dans le modèle actif. Vous pouvez charger jusqu’à 20 fichiers à la fois. |
| **[!UICONTROL Templates]** | Parcourez les modèles d’annonces de votre bibliothèque Creative Studio à utiliser comme calque de base ou élément de référence. |
| **[!UICONTROL My Assets]** | Parcourez toutes les ressources que vous avez chargées dans l’onglet [!UICONTROL Assets] de Creative Studio. |
| **[!UICONTROL Images]** | Parcourez uniquement les ressources d’image que vous avez chargées dans l’onglet [!UICONTROL Assets] de Creative Studio. |
| **[!UICONTROL Text]** | Ajoutez un élément de texte à la zone de travail, y compris les polices personnalisées que vous avez chargées. |
| **[!UICONTROL Elements]** | Ajouter des formes et des éléments de disposition tels que des boutons et des rectangles. |

Vous pouvez faire glisser un élément de n’importe quel panneau directement sur la zone de travail ou cliquer dessus pour le placer à une position par défaut.

#### Modèles de publicité vidéo

| Icon | Description |
| --- | --- |
| **[!UICONTROL Search]** | Effectuez une recherche dans tous les types de ressources de votre bibliothèque. |
| **[!UICONTROL Upload]** | Chargez les fichiers image, vidéo, audio ou de police (TTF, OTF, WOFF, WOFF2) dans l’éditeur pour les utiliser dans le modèle actif. Vous pouvez charger jusqu’à 20 fichiers à la fois. |
| **[!UICONTROL Templates]** | Parcourez les modèles d’annonces publicitaires depuis votre bibliothèque Creative Studio. |
| **[!UICONTROL My Assets]** | Parcourez toutes les ressources que vous avez chargées dans l’onglet [!UICONTROL Assets] de Creative Studio. |
| **[!UICONTROL Images]** | Parcourez uniquement les ressources d’image que vous avez chargées dans l’onglet [!UICONTROL Assets] de Creative Studio. |
| **[!UICONTROL Video]** | Parcourez uniquement les ressources vidéo que vous avez chargées dans l’onglet [!UICONTROL Assets] de Creative Studio. |
| **[!UICONTROL Audio]** | Parcourez uniquement les ressources audio que vous avez chargées dans l’onglet [!UICONTROL Assets] de Creative Studio. |
| **[!UICONTROL Text]** | Ajoutez un élément de texte à la zone de travail, y compris les polices personnalisées que vous avez chargées. |
| **[!UICONTROL Elements]** | Ajoutez des formes et des éléments vectoriels. |

Vous pouvez faire glisser un élément de n’importe quel panneau directement sur la zone de travail ou cliquer dessus pour le placer à une position par défaut.

### Modifier les éléments sélectionnés

Cliquez sur un élément de la zone de travail d’édition pour le sélectionner. Selon le type de modèle, une ou plusieurs barres d’outils s’affichent avec des contrôles pour cet élément.

Les commandes varient selon le type d’élément.

<!-- From inspectorbar.ts -->

#### Afficher la barre d&#39;outils d&#39;édition de modèles

| Contrôle | Types d’éléments | Description |
| --- | --- | --- |
| **[!UICONTROL Properties]** | Tous | Ouvre un panneau pour modifier le nom du calque, marquer le calque comme dynamique (permutable pendant la génération de la publicité) et définir une URL de clic publicitaire (liens uniquement). En dessous, choisissez un état **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** ou **[!UICONTROL Focus]** pour mettre en forme l’élément pour cet état d’interaction, puis ajustez le style (typographie (texte et liens uniquement), les décorations (remplissage, bordure, rayon de coin), les dimensions, la position) en fonction du type d’élément. |
| **[!UICONTROL Effects]** | Tous | Ouvre un panneau dans lequel vous choisissez un état **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]** ou **[!UICONTROL Focus]** auquel appliquer des effets pour cet état d’interaction, puis ajustez les sections **[!UICONTROL Transform]**, **[!UICONTROL Transition]**, **[!UICONTROL Box Shadow]**, **[!UICONTROL Filter]**, **[!UICONTROL Blend Mode]** et **[!UICONTROL Cursor]**. Les éléments de texte incluent également une section **[!UICONTROL Text Shadow]**. |
| **[!UICONTROL Animations]** | Tous | Ouvre un panneau pour définir l’heure d’entrée et de sortie du calque sur le montage et pour configurer les paramètres prédéfinis de **[!UICONTROL Entrance Animation]**, de **[!UICONTROL Loop Animation]** et de **[!UICONTROL Exit Animation]** avec la durée et l’accélération. Inclut des actions **[!UICONTROL Copy]**, **[!UICONTROL Paste]** et **[!UICONTROL Reset]**. |
| **[!UICONTROL Crop]** | Images | Ouvre une barre d’outils pour recadrer l’image. Sélectionnez un paramètre prédéfini de **[!UICONTROL Aspect Ratio]** (ou **[!UICONTROL Free]**), puis cliquez sur **[!UICONTROL Apply]** ou **[!UICONTROL Cancel]**. |
| **[!UICONTROL Position]** | Tous | Ouvre un menu avec des options **[!UICONTROL Move]** (**[!UICONTROL Forward]**, **[!UICONTROL Backward]**, **[!UICONTROL To front]**, **[!UICONTROL To back]**), des options **[!UICONTROL Align to Page]** (**[!UICONTROL Top]**, **[!UICONTROL Left]**, **[!UICONTROL Middle]**, **[!UICONTROL Center]**, **[!UICONTROL Bottom]**, **[!UICONTROL Right]**, **[!UICONTROL Fit Vertically]**, **[!UICONTROL Fit Horizontally]**, **[!UICONTROL Fit to Page]**, **[!UICONTROL Layer Level Alignment]**, **[!UICONTROL Fit to Content]**) et, pour les éléments qui ne sont pas des images, des options (les mêmes six options d’alignement, plus). |

#### Barre d’outils d’édition de modèle vidéo

| Contrôle | Types d’éléments | Description |
| --- | --- | --- |
| **[!UICONTROL Shape]** | Formes | Définit des options spécifiques à la forme. |
| Contrôles de découpe | Images | Ajustez le type de découpe, le décalage et le lissage. |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | Plusieurs éléments sélectionnés ou un groupe | Regroupe les éléments sélectionnés ou dissocie un groupe sélectionné. |
| **[!UICONTROL Combine]** | Formes compatibles | Combine les formes sélectionnées en une seule forme. |
| **[!UICONTROL Audio replace]** | Audio et vidéo | Remplace la piste audio par un fichier de votre bibliothèque de ressources. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | Texte | Ajuste la famille de polices, l’épaisseur, la taille, l’alignement horizontal et d’autres paramètres de typographie avancés. |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | Images et vidéo | Définit l’image de remplissage ou la source vidéo de l’élément. |
| **[!UICONTROL Trim]** | Vidéo et audio | Ouvre le mode de rognage pour définir les points de début et de fin de l’élément. |
| ![Volume](/help/creative/assets/volume.png "Volume") ([!UICONTROL Volume]) | Vidéo et audio | Ajuste le niveau audio. |
| ![Vitesse de lecture](/help/creative/assets/speed.png "Vitesse de lecture") ([!UICONTROL Playback speed]) | Vidéo et audio | Ajuste le taux de lecture. |
| ![Crop](/help/creative/assets/crop.png "Crop") ([!UICONTROL Crop]) | Tous | Recadre l’élément dans une zone personnalisée. |
| Commandes de rotation et de basculement | Tous | Faire pivoter ou retourner l’élément sélectionné. |
| ![Contour](/help/creative/assets/stroke.png "Contour") ([!UICONTROL Stroke]) | Tous | Définit la couleur et la largeur de la bordure. |
| **[!UICONTROL Text Background]** | Texte | Ajoute une couleur de fond derrière le texte. |
| **[!UICONTROL Animations]** | Tous | Ajoute ou modifie des animations d’entrée, de sortie ou en boucle. |
| **[!UICONTROL Style]** | Tous | Ouvre un menu avec des options **[!UICONTROL Adjustments]**, **[!UICONTROL Filter]**, **[!UICONTROL Effect]** et **[!UICONTROL Blur]**. |
| **[!UICONTROL Shadow]** | Tous | Ajoute ou modifie une ombre portée. |
| **[!UICONTROL Opacity]** | Tous | Définit le niveau de transparence de l’élément. |
| **[!UICONTROL Position]** | Tous | Ajuste numériquement la taille, la position et la rotation de l’élément. |
| ![Panneau d’édition](/help/creative/assets/cs-template-video-editing-panel.png "Panneau d’édition") | Tous | Ouvre ou ferme un panneau [édition](#detailed-element-properties-for-video-templates) pour l’élément sélectionné avec davantage de fonctionnalités d’édition. |

#### Propriétés d’élément détaillées pour les modèles vidéo

Dans l’éditeur de modèles vidéo, cliquez sur ![Panneau d’édition](/help/creative/assets/cs-template-video-editing-panel.png "Panneau d’édition") dans la barre d’outils pour ouvrir un panneau d’édition pour l’élément sélectionné avec davantage de fonctionnalités d’édition. Le panneau Modification s’affiche à gauche de la zone de travail et est distinct du panneau [!UICONTROL Layers], qui répertorie les calques du modèle.

##### Éléments individuels

Lorsque vous sélectionnez un seul élément d’image, de vidéo, de forme ou de texte, le panneau Modification affiche les sections applicables ci-dessous.

| Section Panneau | Outil | Contrôles |
| --- | --- | --- |
| [!UICONTROL Layer] | Alignement et positionnement des calques | Aligne le calque sélectionné sur la gauche, le centre horizontal, la droite, le haut, le centre vertical ou le bas. Le menu d’arrangement modifie son ordre d’empilage avant-arrière. Ces commandes positionnent le calque lui-même ; elles ne justifient pas le texte à l’intérieur du calque. |
| | [!UICONTROL Rotate & Flip] | Saisissez un angle de rotation en degrés. Utilisez ![Retourner horizontal](/help/creative/assets/cs-template-video-flip.png "Retourner horizontal") pour refléter le calque horizontalement ou ![Retourner vertical](/help/creative/assets/cs-template-video-flip-vertical.png "Retourner vertical") pour le refléter verticalement. |
| | ![Opacité](/help/creative/assets/cs-template-video-opacity.png "Opacité") [!UICONTROL Opacity] | Rend le calque sélectionné plus ou moins transparent. |
| | ![Mode de fusion](/help/creative/assets/cs-template-video-blend-mode.png "Mode de fusion") [!UICONTROL Blend Mode] | Modifie la façon dont les couleurs du calque sélectionné se combinent avec les calques situés derrière lui. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Ouvre des commandes supplémentaires pour la position et les cotes du calque. La disponibilité dépend des autorisations de transformation du calque sélectionné. |
| [!UICONTROL Shape] | ![Options de forme](/help/creative/assets/cs-template-video-shape-options.png "Options de forme") [!UICONTROL Shape] et propriétés spécifiques à la forme | Modifie la forme et ses propriétés disponibles, telles que les points, les côtés, le diamètre interne, la largeur de trait ou le rayon de coin. Les commandes dépendent de la forme sélectionnée. |
| | [!UICONTROL Vector]: [!UICONTROL Edit Path] | Active le mode de modification vectorielle pour modifier le chemin d&#39;accès de la forme, le cas échéant. |
| [!UICONTROL Character] | ![Typeface](/help/creative/assets/cs-template-video-typeface.png "Typeface") Typeface, ![Style de texte](/help/creative/assets/cs-template-video-text-style.png "Style de texte") Style de texte, ![Bold](/help/creative/assets/cs-template-video-text-bold.png "Bold") gras, ![Italic](/help/creative/assets/cs-template-video-text-italic.png "Italic") italic et ![Font size](/help/creative/assets/cs-template-video-font-size.png "Font size") taille de police | (Calques de texte) Modifie la famille, le style et la taille de la police du texte sélectionné. |
| | ![Aligner à gauche](/help/creative/assets/cs-template-video-text-align-l.png "Aligner à gauche") / ![Aligner au centre](/help/creative/assets/cs-template-video-text-align-c.png "Aligner au centre") / ![Aligner à droite](/help/creative/assets/cs-template-video-text-align-r.png "Aligner à droite") Alignement du texte | (Calques de texte) Aligne le texte de son bloc à gauche, au centre ou à droite, ou détecte automatiquement l’alignement. |
| | ![Paramètres de texte avancés](/help/creative/assets/cs-template-video-advanced-text.png "Paramètres de texte avancés") Paramètres de texte avancés | (Calques de texte) Ouvre des paramètres de typographie supplémentaires. |
| [!UICONTROL Fill] | Contrôles de remplissage ![Fill](/help/creative/assets/cs-template-video-fill.png "Fill") | Modifie la couleur, l’image ou le remplissage vidéo du calque sélectionné. Les contrôles reflètent le type de remplissage actuel et ouvrent ses paramètres. Pour le texte, modifie la couleur du texte. |
| [!UICONTROL Stroke] | Contrôles ![Stroke](/help/creative/assets/cs-template-video-stroke.png "Stroke") Stroke | Active ou désactive le contour et modifie sa couleur, sa largeur, son style et son emplacement. Des commandes supplémentaires apparaissent lorsque le trait est activé. |
| [!UICONTROL Text Background] | ![Arrière-plan texte](/help/creative/assets/cs-template-video-text-bg.png "Arrière-plan texte") Contrôles d&#39;arrière-plan | (Calques de texte) Ajoute ou modifie l’arrière-plan derrière le texte. |
| [!UICONTROL Animations] | ![Animation](/help/creative/assets/cs-template-video-animation.png "Animation") [!UICONTROL Presets] | Ouvre les paramètres prédéfinis d’animation du calque sélectionné, y compris les animations d’entrée, de sortie et en boucle. |
| [!UICONTROL Appearance] | ![Ajustements](/help/creative/assets/cs-template-video-adjustments.png "Ajustements") [!UICONTROL Adjustments] | Modifie les propriétés visuelles du calque sélectionné. |
| | ![Filter](/help/creative/assets/cs-template-video-filter.png "Filter") [!UICONTROL Filter] | Applique un filtre visuel au calque sélectionné. |
| | ![Effets](/help/creative/assets/cs-template-video-effects.png "Effets") [!UICONTROL Effect] | Applique un effet au calque sélectionné. |
| | ![Flou](/help/creative/assets/cs-template-video-blur.png "Flou") [!UICONTROL Blur] | Applique un flou au calque sélectionné. |
| | ![Ombre](/help/creative/assets/cs-template-video-shadow.png "Ombre") [!UICONTROL Shadow] | Ajoute ou modifie l&#39;ombre du calque sélectionné. |

##### Sélections multiples et éléments spécialisés

Lorsque vous sélectionnez plusieurs éléments, un groupe, un élément découpé ou un clip audio, le panneau d&#39;édition affiche les sections spécifiques à la sélection ci-dessous. Plusieurs éléments, groupes et découpes conservent également la section [!UICONTROL Layer].

| Section Panneau | Outil | Contrôles |
| --- | --- | --- |
| [!UICONTROL Layer] | Alignement et positionnement des calques | Aligne plusieurs éléments sélectionnés ou un groupe. Le menu d’arrangement modifie l’ordre d’empilage de l’avant vers l’arrière. |
| | [!UICONTROL Rotate & Flip] | Fait pivoter ou retourne les éléments ou le groupe sélectionnés. |
| | ![Opacité](/help/creative/assets/cs-template-video-opacity.png "Opacité") [!UICONTROL Opacity] | Rend les éléments ou groupes sélectionnés plus ou moins transparents. |
| | ![Mode de fusion](/help/creative/assets/cs-template-video-blend-mode.png "Mode de fusion") [!UICONTROL Blend Mode] | Modifie la manière dont les couleurs des éléments ou des groupes sélectionnés se combinent avec les calques situés derrière eux. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Ouvre les contrôles relatifs à la position et aux cotes des éléments ou groupes sélectionnés. Les contrôles disponibles dépendent des éléments sélectionnés. |
| [!UICONTROL Selection] | ![Group](/help/creative/assets/cs-template-video-group.png "Group") Group / ![Ungroup](/help/creative/assets/cs-template-video-ungroup.png "Ungroup") Ungroup | S’affiche sous [!UICONTROL Layer] pour plusieurs calques sélectionnés ou un groupe sélectionné. Regroupe les calques sélectionnés afin qu’ils puissent être gérés ensemble ou sépare un groupe en calques individuels. |
| [!UICONTROL Settings] | ![Clip découpé](/help/creative/assets/cs-template-video-cutout-clip.png "Clip découpé") / ![Superposition découpée](/help/creative/assets/cs-template-video-cutout-overlay.png "Superposition découpée") Contrôles découpés | (Calques découpés) Apparaît sous [!UICONTROL Layer]. Sélectionne le type de découpe et ajuste son décalage et le lissage des arêtes. |
| [!UICONTROL Audio Properties] | ![Rogner](/help/creative/assets/cs-template-video-trim.png "Rogner") Rogner, ![Volume](/help/creative/assets/cs-template-video-volume.png "Volume") volume et ![Vitesse de lecture](/help/creative/assets/cs-template-video-playback-speed.png "Vitesse de lecture") vitesse de lecture | (Calques audio) Définit les points de début et de fin de l’élément, le niveau audio et la vitesse de lecture. |

#### Modifier les éléments directement sur la zone de travail

##### Afficher les modèles de publicité

| Action | Description |
| --- | --- |
| **[!UICONTROL Replace]** | (Éléments d’image uniquement) Ouvre le panneau Images afin que vous puissiez remplacer l’image par une de votre bibliothèque de ressources. |
| ![Avancer](/help/creative/assets/cs-icon-move-forward.png "Avancer") **[!UICONTROL Move forward]** | Déplace l’élément d’un pas en avant dans l’ordre d’empilement (vers l’avant). |
| ![Reculer](/help/creative/assets/cs-icon-move-backward.png "Reculer") **[!UICONTROL Move backward]** | Déplace l’élément d’un pas en arrière dans l’ordre d’empilement (vers l’arrière). |
| ![Dupliquer](/help/creative/assets/cs-icon-duplicate.png "Dupliquer") **[!UICONTROL Duplicate]** | Crée une copie de l’élément. |
| ![Delete](/help/creative/assets/cs-icon-delete.png "Delete") **[!UICONTROL Delete]** | Supprime l’élément de la zone de travail. |
| Poignée de rotation | Cliquez et faites glisser la poignée au-dessus d’un élément sélectionné pour le faire pivoter. Maintenez la touche **[!UICONTROL Shift]** enfoncée tout en faisant glisser pour aligner la rotation sur des incréments de 15 degrés. |

Vous pouvez également cliquer et faire glisser un élément sélectionné pour le repositionner, puis cliquer et faire glisser les poignées autour pour le redimensionner.

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

Vous pouvez également cliquer et faire glisser un élément sélectionné pour le repositionner, puis cliquer et faire glisser les poignées autour pour le redimensionner.

### Contrôle du minutage et de la lecture

Les éditeurs vidéo et d’affichage affichent tous deux un panneau Chronologie au bas de la zone de travail.

#### Afficher les modèles de publicité

La chronologie affiche une piste pour chaque calque de la zone de travail, couvrant la période pendant laquelle le calque est visible en fonction de sa synchronisation d’animation d’entrée et de sortie. Faites glisser la poignée de début ou de fin d’une piste pour ajuster son heure d’entrée ou de sortie, ou faites glisser une piste pour réorganiser les calques. Cliquez sur la règle ou faites glisser le curseur de lecture pour vous déplacer vers un point dans le temps.

La barre d’outils de la chronologie comprend un champ **[!UICONTROL Duration]** (0 à 60 secondes), **[!UICONTROL Play]**/**[!UICONTROL Pause]**, un affichage de la durée actuelle/totale, un bouton bascule de boucle, des commandes de zoom **[!UICONTROL Timeline Scale]**, un bouton de **[!UICONTROL Fit View]** et un bouton bascule de réduction/développement.

#### Modèles de publicité vidéo

La chronologie affiche tous les clips vidéo et audio du modèle. Utilisez la chronologie pour vérifier la disposition des éléments dans le temps et les rogner en faisant glisser leurs poignées de début et de fin. Vous ne pouvez pas ajouter un nouvel élément directement sur le montage ; ajoutez-le plutôt à partir du panneau de gauche ou de la zone de travail, puis il s’affiche sous la forme d’un élément sur le montage.

### Gestion des calques

Le panneau [!UICONTROL Layers] sur le côté droit de la zone de travail répertorie tous les éléments du modèle et vous permet de gérer leur ordre, leur visibilité et leurs propriétés. Pour les modèles d’affichage, cliquez sur **[!UICONTROL Open Layers]** dans la barre d’outils de la zone de travail pour l’ouvrir. Pour les modèles vidéo, le panneau est ouvert par défaut.

Cliquez sur un calque pour sélectionner l’élément correspondant sur la zone de travail.

**Onglets (modèles d’annonce publicitaire affichés uniquement)**

Les modèles d’affichage comportent deux onglets dans la partie supérieure du panneau [!UICONTROL Layers] :

* **[!UICONTROL Dynamic]** : répertorie uniquement les calques qui peuvent être permutés pendant la génération de l’annonce, tels que les images et le texte que l’agent d’IA peut remplacer. Il s’agit de la vue par défaut pour la génération des variations de publicité.
* **[!UICONTROL All]** : affiche la hiérarchie complète des calques du modèle, y compris les conteneurs structurels. Utilisez cette vue pour examiner ou réorganiser la manière dont les éléments sont imbriqués.

Les modèles vidéo affichent tous les calques dans une seule liste sans onglets.

**Actions par couche**

Placez le curseur sur un calque pour afficher les actions suivantes.

| Action | Description |
| --- | --- |
| ![Renommer le calque](/help/creative/assets/edit.png "Renommer le calque") **[!UICONTROL Rename layer]** | Permet de saisir un nouveau nom de calque dans le panneau. |
| ![Verrouiller le calque](/help/creative/assets/cs-icon-lock.png "Verrouiller le calque") **[!UICONTROL Lock layer]** / ![Déverrouiller le calque](/help/creative/assets/cs-icon-unlock.png "Déverrouiller le calque") **[!UICONTROL Unlock layer]** | Empêche ou autorise le déplacement, la modification ou la réorganisation du calque. |
| ![Masquer le calque](/help/creative/assets/cs-icon-hidden.png "Masquer le calque") **[!UICONTROL Hide layer]** / ![Afficher le calque](/help/creative/assets/cs-icon-visible.png "Afficher le calque") **[!UICONTROL Show layer]** | Masque ou affiche le calque sur la zone de travail. Les calques masqués sont conservés dans le modèle, mais n’apparaissent pas lors du rendu du modèle. |
| ![Faire glisser pour réorganiser](/help/creative/assets/cs-icon-drag.png "Faire glisser pour réorganiser") Faire glisser pour réorganiser | (Affichage des modèles publicitaires uniquement) Faites glisser l’icône de réorganisation pour modifier la position du calque dans l’ordre d’empilement. Le calque doit être déverrouillé pour le réorganiser. |

**Pied de page du panneau**

| Action | Description |
| --- | --- |
| ![Dupliquer le calque sélectionné](/help/creative/assets/cs-icon-duplicate.png "Dupliquer le calque sélectionné") **[!UICONTROL Duplicate selected layer]** | Crée une copie du calque sélectionné. |
| ![Supprimer le calque sélectionné](/help/creative/assets/cs-icon-delete.png "Supprimer le calque sélectionné") **[!UICONTROL Delete selected layer]** | Supprime le calque sélectionné. |
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

>[!MORELIKETHIS]
>
>* [À propos de Creative Studio dans Advertising Creative](creative-studio-about.md)
>* [Gestion des ressources dans Creative Studio](creative-studio-manage-assets.md)
>* [Gestion des publicités standard dans Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gestion des contenus créatifs dynamiques dans Creative Studio](creative-studio-manage-dynamic-ads.md)
