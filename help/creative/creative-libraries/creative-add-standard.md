---
title: Ajout de contenus publicitaires standard à une bibliothèque de contenus publicitaires
description: Découvrez comment ajouter des contenus publicitaires standard (non dynamiques) à une bibliothèque de contenus publicitaires.
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 38ba8473eae3df204f618eac1f20e605e57ece5a
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Ajout de contenus publicitaires standard à une bibliothèque de contenus publicitaires

*Version bêta fermée*

Ajoutez des contenus publicitaires à vos [bibliothèques de contenu publicitaire](creative-library-manage.md) pour les utiliser avec les [expériences publicitaires](/help/creative/experiences/experience-about.md).

>[!NOTE]
>
> Vous pouvez inclure des contenus publicitaires individuels directement dans des expériences publicitaires pour lesquelles aucune cible utilisateur n’est définie. Vous pouvez également regrouper vos contenus publicitaires dans des [offres groupées](bundle-manage.md), que vous pouvez inclure dans des expériences publicitaires ciblées.

## Ajout d’annonces HTML flexibles à une bibliothèque de contenu créatif {#flexible-creative-add}

Vous pouvez effectuer l’une des opérations suivantes :

* Chargez vos propres contenus publicitaires flexibles dans des fichiers ZIP.

* Utilisez l’un des modèles de création flexibles prédéfinis chargés sur votre compte comme point de départ de votre propre contenu créatif flexible.

### Chargement de vos propres contenus publicitaires flexibles {#flexible-creative-upload}

Vous pouvez charger plusieurs unités de création flexibles. Les contenus publicitaires flexibles doivent être au format ZIP et peuvent atteindre 2 Mo. Pour connaître les exigences en matière de fichiers, consultez la spécification de création [HTML5](html5-creative-specification.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur le nom de la bibliothèque.

1. Dans l’onglet **[!UICONTROL Creatives]** , cliquez sur le sous-onglet **[!UICONTROL Standard Ads]** .

1. Cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Cliquez sur **[!UICONTROL Upload New]**.

1. Spécifiez les fichiers ZIP de l’une des manières suivantes :

   * Glissez-déposez des fichiers sur votre appareil ou réseau dans la zone.

   * Cliquez sur **[!UICONTROL select a file]** pour localiser les fichiers sur votre appareil ou réseau.

   Voir [spécifications d’annonces publicitaires flexibles](#flexible-ad-spec).

1. Ajoutez ou supprimez des fichiers créatifs flexibles :

   * Pour ajouter un fichier, cliquez sur ![Ajouter](/help/creative/assets/create.png "Ajouter") dans le coin supérieur gauche et recherchez le fichier sur votre appareil ou réseau.

   * Pour supprimer un fichier, décochez la case en regard de celui-ci.

1. Spécifiez les [paramètres de publicité HTML5 flexibles](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5).

   Par défaut, tous les contenus publicitaires que vous venez de télécharger sont sélectionnés. Tous les paramètres ne comportant qu’une seule valeur s’appliquent à tous les contenus publicitaires sélectionnés ; pour certains paramètres, vous pouvez spécifier des valeurs individuelles. Pour définir des paramètres pour des contenus publicitaires spécifiques, décochez la case en regard de chaque contenu publicitaire inapplicable.

1. Clic **[!UICONTROL Create]**

### Ajouter des contenus publicitaires flexibles à l’aide d’un modèle {#flexible-creative-use-template}

Vous pouvez utiliser l’un des modèles créatifs flexibles chargés sur votre compte pour créer des annonces d’une taille prédéfinie. Une fois que vous avez sélectionné un modèle à utiliser, vous modifiez les balises et les attributs de clic.&lt;!— Remplacez la dernière phrase par celle-ci si nous ajoutons à nouveau la fonction de téléchargement de modèle : vous pouvez a\) sélectionner un modèle à utiliser, puis modifier les balises et attributs de clic ; ou b\) [télécharger un modèle sous forme de fichier ZIP](#download-flexible-creative-template), modifier le contenu hors ligne pour créer votre propre contenu créatif, puis [charger le fichier modifié en tant que nouveau contenu créatif](flexible-creative-upload).>

<!-- Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur le nom de la bibliothèque.

1. Dans l’onglet **[!UICONTROL Creatives]** , cliquez sur le sous-onglet **[!UICONTROL Standard Ads]** .

1. Cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Cliquez sur **[!UICONTROL Browse System Flexible Templates]**.

<!-- Not options as of 5/22/25:

1. In the left panel, select the creative size to see all available templates for that size.

1. Select the template:

   * In card view, click **[!UICONTROL ...]** next to the template name, and then click **[!UICONTROL Use Selected]**.
     
   * In table view, hold the cursor over the row and click **[!UICONTROL Use Selected]**.
-->

1. (Facultatif) Pour prévisualiser le modèle, cliquez sur **[!UICONTROL ...]** en regard du nom du modèle, puis cliquez sur **[!UICONTROL Preview]**.

   Vous pouvez éventuellement télécharger le modèle

1. En regard du nom du modèle, cliquez sur **[!UICONTROL ...]** , puis sur **[!UICONTROL Use Selected]**.

1. Modifiez les [paramètres de création HTML5 flexibles](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) pour spécifier la langue et inclure vos propres balises de clic, images et autres attributs.

   La taille de fichier maximale du fichier créatif, une fois compressé, est de 2 Mo.<!-- Still true? -->

1. Cliquez sur **[!UICONTROL Create]**.

## Ajout d’un contenu créatif HTML5 à une bibliothèque de contenu créatif

Vous pouvez ajouter plusieurs contenus publicitaires HTML5 d’un seul type (simple ou statique) à la fois.

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>Vous pouvez également [ajouter des contenus publicitaires HTML5 flexibles](#flexible-creative-add), qui sont des contenus publicitaires HTML5 avec tous leurs attributs en tant que balises HTML standard que vous pouvez modifier directement dans [!DNL Creative].

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur le nom de la bibliothèque.

1. Dans l’onglet **[!UICONTROL Creatives]** , cliquez sur le sous-onglet **[!UICONTROL Standard Ads]** .

1. Cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL HTML5]**.

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. Spécifiez les fichiers de l’une des manières suivantes :

   * Glissez-déposez des fichiers sur votre appareil ou réseau dans la zone.

   * Cliquez sur **[!UICONTROL select a file]** pour localiser le fichier sur votre appareil ou réseau.

   Voir la spécification publicitaire [HTML5](/help/creative/creative-libraries/html5-creative-specification.md).

1. Spécifiez les [paramètres de publicité HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5).

Par défaut, tous les contenus publicitaires que vous venez de télécharger sont sélectionnés. Tous les paramètres ne comportant qu’une seule valeur s’appliquent à tous les contenus publicitaires sélectionnés ; pour certains paramètres, vous pouvez spécifier des valeurs individuelles. Pour définir des paramètres pour des contenus publicitaires spécifiques, décochez la case en regard de chaque contenu publicitaire inapplicable.

1. Clic **[!UICONTROL Create]**

## Ajout d’une image créative à une bibliothèque de contenu créatif

Les contenus publicitaires d’image peuvent être au format GIF, JPEG, JPG ou PNG. La taille de fichier maximale est de deux (2) Mo. Consultez les [tailles créatives prises en charge](/help/creative/creative-libraries/creative-sizes.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur le nom de la bibliothèque.

1. Dans l’onglet **[!UICONTROL Creatives]** , cliquez sur le sous-onglet **[!UICONTROL Standard Ads]** .

1. Cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Image]**.

1. Spécifiez les images :

   * Pour les ressources d’images locales, effectuez l’une des opérations suivantes :

      * Glissez-déposez des fichiers sur votre appareil ou réseau dans la zone.

      * Cliquez sur **[!UICONTROL select a file]** pour localiser les fichiers sur votre appareil ou réseau.

   * Pour les images de votre bibliothèque Adobe Experience Manager, procédez comme suit :

      1. Cliquez sur **[!UICONTROL AEM Asset Library]**.

      1. Connectez-vous à votre compte Experience Manager.

      1. Recherchez et sélectionnez les fichiers dans vos vues [!UICONTROL Assets] ou [!UICONTROL Collections], puis cliquez sur **[!UICONTROL Select]** en haut à droite.

1. Ajoutez ou supprimez des images :

   * Pour ajouter une image, cliquez sur ![Ajouter](/help/creative/assets/create.png "Ajouter") dans le coin supérieur gauche et recherchez le fichier sur votre appareil ou réseau.

   * Pour supprimer une image, décochez la case située en regard de celle-ci.

1. Spécifiez les [ paramètres de création d’image ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image).

   Par défaut, tous les contenus publicitaires que vous venez de charger sont sélectionnés et les paramètres que vous spécifiez s’appliquent à tous les contenus publicitaires sélectionnés. Les paramètres ne comportant qu’une seule valeur s’appliquent à tous les contenus publicitaires sélectionnés. Pour définir des paramètres pour des contenus publicitaires spécifiques, désélectionnez chaque contenu publicitaire inapplicable.

1. Clic **[!UICONTROL Create]**

## Ajout d’un contenu créatif tiers à une bibliothèque de contenu créatif {#creative-add-third-party}

[!DNL Creative] prend en charge les balises de suivi JavaScript pour les contenus publicitaires hébergés sur la plupart des serveurs de publicités tiers.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Cliquez sur le nom de la bibliothèque.

1. Dans l’onglet **[!UICONTROL Creatives]** , cliquez sur le sous-onglet **[!UICONTROL Standard Ads]** .

1. Cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL 3rd Party]**.

1. Spécifiez la balise JavaScript et d’autres paramètres pour les créatifs dans les [paramètres de création tiers](#creative-settings-third-party).

   Vous pouvez copier et coller l’une des [macros disponibles](/help/creative/creative-macros.md) dans la balise JavaScript.

1. Clic **[!UICONTROL Create]**

>[!MORELIKETHIS]
>
>* [Modification de contenus publicitaires standard](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Paramètres de création standard](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Macros disponibles pour le tracking des URL](/help/creative/creative-macros.md)
>* [Tailles créatives prises en charge](/help/creative/creative-libraries/creative-sizes.md)
>* [Prévisualisation d’une création](/help/creative/creative-libraries/creative-preview.md)
>* [Joindre et détacher des contenus publicitaires des offres groupées](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [À propos de vos bibliothèques de création](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Gestion des bibliothèques de création](/help/creative/creative-libraries/creative-library-manage.md)
