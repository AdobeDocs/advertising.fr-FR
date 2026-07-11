---
title: Gestion des ressources dans Creative Studio
description: Découvrez comment charger, parcourir et gérer des ressources dans l’onglet Assets de Creative Studio dans Adobe Advertising Creative.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 292
ht-degree: 0%

---

# Gestion des ressources dans [!UICONTROL Creative Studio]

*Fonction*

Chargez des images, des vidéos, des fichiers audio et des polices pour les référencer dans les modèles publicitaires et les joindre aux messages de conversation de l’agent IA pendant les sessions de génération publicitaire.

## La vue [!UICONTROL Creative Studio] > [!UICONTROL Assets]

L’onglet **[!UICONTROL Assets]** répertorie les ressources existantes en mode Carte.

### Actions disponibles

<!--  * [Browse and search assets](#assets-search) -->

* [Chargement de ressources](#assets-upload)

* [Renommer une ressource](#assets-rename)

* [Téléchargement d’une ressource](#assets-download)

* [Suppression d’un élément](#assets-delete)

<!--

Should be in "Common Tasks" chapter

## Browse and search assets {#assets-search}

* Use the **[!UICONTROL Search assets]** field to find assets by name. Enter at least three characters to trigger a search; shorter queries don't filter results.
* Click **[!UICONTROL Filter]** to filter the asset library by type or other attributes.

-->

## Chargement de ressources {#assets-upload}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Assets]** .

1. Cliquez sur **[!UICONTROL Upload Assets]**.

1. Sélectionnez un ou plusieurs fichiers sur votre ordinateur ou votre réseau.

   Les types de fichiers pris en charge sont les suivants :

   <!-- Verified 2026-07-09 against creative-api TemplateMediaValidator.java (IMAGE_EXTENSIONS, VIDEO_EXTENSIONS, AUDIO_EXTENSIONS), which backs the /v1/creative/template-medias upload/initiate endpoint used by this tab. The Assets tab file input has no client-side accept restriction (TemplateBrowser.tsx) and relies entirely on this backend validator, so it is authoritative. -->

   | Type | Formats pris en charge | Taille de fichier maximale |
   | --- | --- | --- |
   | Images | JPG/JPEG, PNG, GIF, WebP, SVG | 10 MO |
   | Vidéo | MP4, MOV, AVI, WebM | 512 MO |
   | Audio | MP3, WAV, AAC, OGG | 50 MO |

   Les fichiers vides et les types de fichiers non pris en charge sont rejetés avec une notification d’erreur.

   Le nom de la ressource est enregistré comme nom de fichier chargé sans son extension. Les espaces et les caractères non-ASCII dans le nom de fichier sont remplacés par des traits de soulignement (par exemple, lors du chargement d’`My Logo.png`, une ressource nommée `My_Logo` est créée). Vous pouvez renommer la ressource par la suite.

<!--

maybe later:

   | Fonts | TTF, OTF, WOFF, WOFF2 | 5 MB |
   
-->

## Modification du nom d’une ressource {#asset-rename}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Assets]** .

1. Placez le curseur sur la carte de la ressource et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit name]**.

1. Mettre à jour le nom de la ressource

   Les noms de ressources peuvent contenir jusqu’à 512 caractères.

1. Cliquez sur **[!UICONTROL Update]**.

## Téléchargement d’une ressource {#asset-download}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Assets]** .

1. Placez le curseur sur la carte de la ressource et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   La ressource est téléchargée conformément à la procédure normale de votre navigateur.

## Suppression d’un élément {#asset-delete}

>[!NOTE]
>
>Vous ne pouvez pas réactiver une ressource supprimée.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative Studio].**

1. Cliquez sur l’onglet **[!UICONTROL Assets]** .

1. Placez le curseur sur la carte de la ressource et cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos de Creative Studio dans Advertising Creative](creative-studio-about.md)
>* [Gestion des modèles dans Creative Studio](creative-studio-manage-templates.md)
>* [Générer des publicités standard dans Creative Studio](creative-studio-manage-standard-ads.md)
