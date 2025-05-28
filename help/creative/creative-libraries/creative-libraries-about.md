---
title: À propos de vos bibliothèques de création
description: Découvrez comment gérer les contenus publicitaires pour vos expériences publicitaires.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: d7e2403e13c0f9edf1505ca7c50aea3de34f1f3a
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 0%

---

# À propos de vos bibliothèques de création

*Fonctionnalité bêta fermée*

Vos bibliothèques de contenu publicitaire vous permettent de gérer les contenus publicitaires que vous utiliserez dans vos expériences publicitaires. Vous pouvez créer plusieurs bibliothèques, chacune avec un ensemble de contenus publicitaires et *lots de contenus publicitaires*, qui sont des groupes de contenus publicitaires que vous pouvez ajouter à une expérience en tant qu’unité.

Vos bibliothèques peuvent inclure les éléments suivants :

* **Contenu publicitaire individuel :** vous pouvez inclure des contenus publicitaires individuels directement dans des expériences publicitaires pour lesquelles aucune cible utilisateur n’est définie. Vous pouvez également utiliser vos contenus publicitaires pour créer des offres groupées, que vous pouvez inclure dans des [expériences publicitaires](/help/creative/experiences/experience-about.md) ciblées.

   * **Contenu publicitaire standard :** vous pouvez charger et gérer des contenus publicitaires dans [différents formats](#creative-creative-formats). Pour chaque élément créatif, vous spécifiez la langue par défaut de chaque annonce à laquelle vous associez l’élément créatif, la page de destination par défaut qui s’ouvre lorsqu’un utilisateur clique sur une annonce qui comprend l’élément créatif et les libellés facultatifs à utiliser comme filtres dans différentes vues dans [!DNL Creative].

   * **Contenu créatif dynamique :** (clients Adobe Advertising DCO existants uniquement) Les utilisateurs administrateurs peuvent créer des contenus créatifs générés dynamiquement en mappant les variables dynamiques d’un modèle d’annonce publicitaire aux valeurs d’un fichier de flux. Tous les utilisateurs peuvent prévisualiser, dupliquer et supprimer des annonces dynamiques existantes.

* **Lots de contenu publicitaire :** regroupez les contenus publicitaires en lots à utiliser dans plusieurs expériences avec des cibles utilisateur définies. Vous pouvez créer des *bundles standard* composés d’annonces standard et des *bundles dynamiques* composés d’annonces générées dynamiquement.

## Formats Creative pris en charge {#creative-creative-formats}

### Formats pour les contenus publicitaires standard

Vous pouvez ajouter et gérer les types de contenu créatif suivants dans les [tailles de contenu créatif prises en charge](creative-sizes.md).

>[!IMPORTANT]
>
>Même si vous avez l’intention d’utiliser des contenus publicitaires HTML5, Flexible HTML5 ou tiers pour vos expériences publicitaires, vous devez également ajouter des contenus publicitaires d’image pour chaque taille de contenu publicitaire que vous utilisez.
>
>Chaque expérience nécessite une image créative par défaut pour chaque taille de création attribuée à l’expérience. Les contenus publicitaires d’image par défaut sont utilisés lorsqu’un navigateur n’est pas activé pour JavaScript ou lorsque le serveur de publicités ne peut pas personnaliser la publicité en raison de retards.

#### HTML5 flexible

Les contenus créatifs HTML5 flexibles sont des contenus créatifs HTML5 avec toutes leurs images et autres attributs comme des balises HTML standard, que vous pouvez modifier directement dans [!DNL Creative], soit dans une bibliothèque de contenus créatifs, soit dans une expérience individuelle (ce qui crée une variante du contenu créatif d’origine). Les créatifs HTML5 flexibles utilisent la norme du laboratoire de technologie du Bureau de l’Advertising interactive (IAB) pour un [portfolio d’annonces](https://flexibleads.iabtechlab.com/)<!-- Change to https://iabtechlab.com/standards/iab-new-ad-portfolio-guidelines/ if the broken page isn't fixed --> pour lequel les tailles des annonces sont flexibles (plutôt que fixes) et basées sur les proportions et la plage de tailles de l’annonce, et pour lequel les annonces conservent leur résolution sur tous les appareils et sites d’édition.<!-- Yet our flexible creatives and templates are for a single specific ad size (in pixels), not an aspect ration with size range. Clarify -->

Vous pouvez charger des contenus publicitaires HTML5 flexibles sous forme de fichiers ZIP ou utiliser l’un des modèles disponibles pour votre compte comme point de départ. Consultez les [spécifications des contenus publicitaires HTML5 flexibles](html5-creative-specification.md).

<!-- Will flattening the view be possible later?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

Vous pouvez éventuellement modifier les valeurs par défaut des attributs spécifiés dans un élément créatif HTML5 flexible. Par la suite, vous pouvez spécifier des valeurs personnalisées pour les attributs dans une expérience spécifique, ce qui crée une variante du contenu créatif parent.

#### Conceptions HTML5

Vous pouvez charger des contenus publicitaires HTML5 simples ou statiques, avec tous les attributs et images spécifiés, sous forme de fichiers ZIP. Vous ne pouvez pas modifier d’attributs ni ajouter d’images ; au lieu de cela, chargez un nouveau fichier ZIP pour ajouter un nouveau contenu créatif. Consultez les [spécifications des contenus publicitaires HTML5 simples et statiques](html5-creative-specification.md).

#### Conceptions d’image

Vous pouvez inclure des éléments créatifs d’image au format GIF, JPEG, JPG ou PNG. Vous pouvez charger des images à partir de vos comptes Adobe Experience Manager ou des images à partir de votre appareil ou réseau.

Chaque expérience publicitaire nécessite une image créative par défaut pour chaque taille de contenu créatif attribuée à l’expérience.

#### Contenus publicitaires tiers

Saisissez les balises de suivi JavaScript pour les contenus publicitaires hébergés sur des serveurs de publicités tiers. Le script varie selon le serveur de publicités. Voici un exemple :

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### Format pour les publicités dynamiques

Les utilisateurs administrateurs peuvent générer dynamiquement des contenus publicitaires au format statique HTML5 et dynamique HTML5 en mappant les variables dynamiques d’un modèle d’annonce publicitaire aux valeurs d’un fichier de flux. Les contenus publicitaires dynamiques peuvent inclure ceux de vos expériences Adobe Advertising Dynamic Creative Optimization (DCO) héritées.

## Les vues [!UICONTROL Creative Libraries]

Voir « [ Personnaliser vos vues de données »](/help/creative/introduction/customize-data-views.md) pour plus d’informations sur la personnalisation de chaque vue.

### La vue principale [!UICONTROL Creative Libraries]

La vue principale [!UICONTROL Creative Libraries] affiche toutes vos bibliothèques de création. Les données de chaque bibliothèque incluent le nombre d’expériences auxquelles les lots de la bibliothèque sont affectés, le nombre de lots, le nombre de contenus publicitaires, le nombre de tailles de contenus publicitaires, le nombre de cibles linguistiques par défaut, la date de création et la date de dernière modification apportée à un élément de la bibliothèque. Le mode Tableau comprend également une colonne pour l’annonceur.

#### Actions disponibles

* Création de bibliothèques

* Pour chaque bibliothèque de contenu créatif :

   * Modifier le nom de la bibliothèque

   * Ouvrez la bibliothèque pour afficher les contenus publicitaires et les lots affectés à la bibliothèque

   * Suppression de la bibliothèque

### Les vues [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

L’onglet [!UICONTROL Standard Ads] affiche tous les contenus publicitaires standard que vous avez créés. Les données de chaque élément créatif incluent la taille de l’élément créatif, le type d’élément créatif et la date de création. Le mode Tableau comprend également des colonnes pour la langue par défaut et la page de destination par défaut.

##### Actions disponibles

* [Ajout de contenus publicitaires standard à une bibliothèque](creative-add-standard.md)

* [Modification d’un contenu créatif standard](creative-edit-standard.md)

* [Aperçu d’un contenu créatif standard](creative-preview.md)

* [Ajoutez des contenus publicitaires standard aux lots standard et supprimez des contenus publicitaires standard d’un lot standard](creative-attach-detach-bundles.md)

* [Dupliquer les contenus publicitaires standard](creative-duplicate.md)

* [Téléchargement de contenus publicitaires standard](creative-download.md)

* [Supprimer les contenus publicitaires standard](creative-delete.md)

<!-- Add in as separate actions?

add or remove labels, regenerate thumbnails for your creatives. When a creative has child creative variations, you can view the variations within the Card view.

-->

#### [!UICONTROL Dynamic Ads]

L’onglet [!UICONTROL Dynamic Ads] affiche tous les contenus publicitaires dynamiques créés dynamiquement pour vos catalogues créatifs, à l’exception de ceux que vous [avez supprimés manuellement](creative-delete.md) dans l’onglet [!UICONTROL Dynamic Ads]. Si vous [avez dupliqué manuellement](creative-duplicate.md) des contenus publicitaires dynamiques depuis le dernier traitement d’un catalogue, la liste des contenus publicitaires de ce catalogue inclut également les contenus publicitaires dupliqués.

Les données de chaque élément créatif incluent le type d’élément créatif, la taille de l’élément créatif, le nombre de catalogues auxquels il appartient et la date de création. Le mode Tableau comprend également des colonnes pour le modèle à partir duquel la création a été générée et le nombre d’offres.

>[!NOTE]
>
>Chaque fois qu’un catalogue est traité, les données sont actualisées pour les contenus publicitaires dynamiques existants de ce catalogue.

##### Actions disponibles

Actuellement, la possibilité de créer et de modifier des contenus publicitaires dynamiques est réservée à l’équipe du compte Adobe. Cependant, tous les utilisateurs peuvent :

* [Aperçu de contenus publicitaires dynamiques](creative-preview.md)

* [Ajoutez des contenus publicitaires dynamiques à des lots dynamiques et supprimez des contenus publicitaires dynamiques d’un lot dynamique](creative-attach-detach-bundles.md)

* [Duplication de contenus publicitaires dynamiques](creative-duplicate.md)

* [Suppression de contenus publicitaires dynamiques](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### La vue [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

La vue [!UICONTROL Bundles] affiche tous vos conteneurs de lots standard et dynamiques. Vous pouvez voir les noms des contenus publicitaires, les tailles de contenu publicitaire et les langues des contenus publicitaires inclus dans chaque lot.

#### Actions disponibles

* Ajout de lots standard et dynamiques à une bibliothèque

* Répertorier et prévisualiser les contenus publicitaires d’une offre groupée

* Modifier le nom d’un lot

* Ajoutez des contenus publicitaires standard aux lots standard et supprimez des contenus publicitaires standard d’un lot standard

* Dupliquer les lots

* Supprimer des lots

>[!MORELIKETHIS]
>
>* [Gestion des bibliothèques de création](/help/creative/creative-libraries/creative-library-manage.md)
>* [Ajouter des contenus publicitaires standard à une bibliothèque de contenus publicitaires](creative-add-standard.md)
>* [Gestion des offres groupées de création](bundle-manage.md)
>* [Personnaliser les vues de données](/help/creative/introduction/customize-data-views.md)
