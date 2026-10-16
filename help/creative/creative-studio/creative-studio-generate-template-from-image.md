---
title: Générer un modèle d’annonce publicitaire à partir d’une image à l’aide de l’IA
description: Découvrez comment utiliser l’IA dans Creative Studio pour convertir une image d’annonce publicitaire à affichage statique existante en modèle d’annonce publicitaire modifiable.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: adc2fdc93f06b5459c19b08306d1e30ce00e7028
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---
# Générer un modèle d’annonce publicitaire à partir d’une image à l’aide de l’IA

*Fonction*

Utilisez l’IA dans [!UICONTROL Creative Studio] pour convertir une image d’annonce publicitaire à affichage statique existante en modèle d’annonce publicitaire à affichage modifiable. Passez en revue le modèle généré, demandez des modifications en langage naturel, puis ouvrez l’éditeur de modèles pour apporter des modifications manuelles et enregistrer le modèle.

## Avant de commencer

Vous avez besoin d’une publicité d’images statique existante dans une bibliothèque Creative. Ce workflow sélectionne des publicités dans vos bibliothèques ; il ne charge pas de nouvelle image directement dans la boîte de dialogue de génération.

## Génération et révision du modèle {#template-generate}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio]**.

1. Cliquez sur l’onglet **[!UICONTROL Templates]** .

1. (Facultatif) Sélectionnez un annonceur dans la liste des annonceurs située en haut de la page pour afficher ses bibliothèques.

1. Dans la zone de **[!UICONTROL Use AI to Generate a New Display Ad Template]**, cliquez sur **[!UICONTROL Generate]**.

1. Dans la boîte de dialogue **[!UICONTROL Generate New Ad Template]**, sélectionnez **[!UICONTROL Generate from Existing Standard Ad Image]** s’il n’est pas déjà sélectionné.

1. Sélectionnez la bibliothèque contenant l’annonce publicitaire d’image dans la liste **[!UICONTROL Ad Library]** .

1. Placez le curseur sur la carte publicitaire de l’image, puis cliquez sur **[!UICONTROL Use this Standard Ad]**.

   La génération commence automatiquement, en utilisant la largeur et la hauteur de l’annonce sélectionnée.

1. Attendez la fin de la génération, puis passez en revue l’aperçu du modèle et le panneau **[!UICONTROL Layers]**, le cas échéant.

   Vérifiez le texte, les images et la mise en page avant d’utiliser le modèle. Les calques affichés ici sont à réviser ; effectuez des modifications manuelles dans l’éditeur de modèles.

1. (Facultatif) Demandez des modifications au modèle généré :

   1. Dans le champ **[!UICONTROL Ask the AI for any changes]** , décrivez les modifications que vous souhaitez apporter. Par exemple, saisissez `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Cliquez sur **[!UICONTROL Regenerate]**.

   1. Vérifiez l’aperçu mis à jour. Répétez l’opération si nécessaire.

1. Lorsque vous êtes prêt à continuer, cliquez sur **[!UICONTROL Use this Ad Template]**.

   Le modèle généré s’ouvre dans l’éditeur de modèles d’affichage.

## Modifier et enregistrer le modèle {#template-save}

1. Dans l’éditeur de modèles, passez en revue les éléments générés et apportez les modifications restantes à l’aide des commandes de l’[éditeur de modèles](creative-studio-manage-templates.md#template-controls).

1. Cliquez sur **[!UICONTROL Save]**.

1. Dans la boîte de dialogue **[!UICONTROL Update Template]**, saisissez ou mettez à jour le **[!UICONTROL Template name]**, sélectionnez le **[!UICONTROL Advertiser]** et ajoutez éventuellement des balises.

1. Cliquez sur **[!UICONTROL Update]** pour enregistrer le modèle et revenir à la vue **[!UICONTROL Templates]**.

   Pour enregistrer une copie distincte à la place, cliquez sur **[!UICONTROL Save As New]**.

Vous pouvez ensuite utiliser le modèle pour [générer des variations d’annonce publicitaire](creative-studio-manage-templates.md#ad-variations-generate).

## Si vous ne pouvez pas générer de modèle {#troubleshooting}

* **Aucune bibliothèque ni publicité image n’est répertoriée :** vérifiez l’annonceur et le **[!UICONTROL Ad Library]** sélectionnés. Si la bibliothèque ne comporte pas d’images d’annonce publicitaire standard, sélectionnez une autre bibliothèque contenant une annonce d’image statique existante.

* **La génération échoue ou l’image ne peut pas être convertie :** Vérifiez le message affiché, cliquez sur **[!UICONTROL Back to library]**, puis sélectionnez une annonce publicitaire d’image pour réessayer.

>[!MORELIKETHIS]
>
>* [Gestion des modèles d’annonce publicitaire dans Creative Studio](creative-studio-manage-templates.md)
>* [Gestion des publicités standard dans Creative Studio](creative-studio-manage-standard-ads.md)