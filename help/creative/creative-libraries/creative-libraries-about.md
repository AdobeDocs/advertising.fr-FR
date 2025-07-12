---
title: À propos de vos bibliothèques de création
description: Découvrez comment gérer les contenus publicitaires pour vos expériences publicitaires.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 95e17af996cb3171667ef3cd5ac662f08112691b
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# À propos de vos bibliothèques de création

*Fonctionnalité bêta fermée*

Vos bibliothèques de contenu publicitaire vous permettent de gérer les contenus publicitaires que vous utiliserez dans vos expériences publicitaires. Vous pouvez créer plusieurs bibliothèques, chacune avec un ensemble de contenus publicitaires et *lots de contenus publicitaires*, qui sont des groupes de contenus publicitaires que vous pouvez ajouter à une expérience en tant qu’unité.

Vos bibliothèques peuvent inclure les éléments suivants :

* **Contenu publicitaire individuel :** vous pouvez inclure des contenus publicitaires individuels directement dans des expériences publicitaires pour lesquelles aucune cible utilisateur n’est définie. Vous pouvez également utiliser vos contenus publicitaires pour créer des offres groupées, que vous pouvez inclure dans des [expériences publicitaires](/help/creative/experiences/experience-about.md) ciblées.

   * **Contenu publicitaire standard :** vous pouvez charger et gérer des contenus publicitaires dans [différents formats](#creative-creative-formats). Pour chaque élément créatif, vous spécifiez la langue par défaut de chaque publicité à laquelle vous associez l’élément créatif, ainsi que la page de destination par défaut qui s’ouvre lorsqu’un utilisateur clique sur une publicité qui inclut l’élément créatif. Vous pouvez éventuellement spécifier des libellés à utiliser comme filtres dans différentes vues dans [!DNL Creative] et comme valeurs de colonne dans le [!UICONTROL Custom Creative Report] lorsque vous incluez à l’aide de la dimension [!UICONTROL Creative Label] .

   * **Contenu créatif dynamique :** (clients Adobe Advertising DCO existants uniquement) Les utilisateurs administrateurs peuvent créer des contenus créatifs générés dynamiquement en mappant les variables dynamiques d’un modèle d’annonce publicitaire aux valeurs d’un fichier de flux. Tous les utilisateurs peuvent prévisualiser, dupliquer et supprimer des annonces dynamiques existantes.

* **Lots de contenu publicitaire :** regroupez les contenus publicitaires en lots à utiliser dans plusieurs expériences avec des cibles utilisateur définies. Vous pouvez créer des *bundles d’affichage standard* qui consistent en des publicités d’affichage standard, des *bundles vidéo standard* qui consistent en des publicités vidéo standard et des *bundles d’affichage dynamique* qui consistent en des publicités d’affichage générées dynamiquement.

## Formats Creative pris en charge {#creative-creative-formats}

### Formats pour les contenus publicitaires standard

Vous pouvez ajouter et gérer les types de contenu créatif suivants dans les [tailles de contenu créatif prises en charge](creative-sizes.md).

>[!IMPORTANT]
>
>* Même si vous envisagez d’utiliser des contenus publicitaires HTML5, Flexible HTML5 ou tiers pour vos expériences d’affichage publicitaire standard, vous devez également ajouter des contenus publicitaires pour chaque taille de contenu créatif utilisée.
>* Chaque expérience d’affichage standard nécessite une image créative par défaut pour chaque taille de contenu créatif attribuée à l’expérience. Les contenus publicitaires d’image par défaut sont utilisés lorsqu’un navigateur n’est pas activé pour JavaScript ou lorsque le serveur de publicités ne peut pas personnaliser la publicité en raison de retards.
>* Chaque expérience vidéo standard nécessite une création vidéo par défaut pour chaque taille de création attribuée à l’expérience.<!-- when is it used? -->

#### HTML5 flexible

Les contenus créatifs HTML5 flexibles sont des contenus créatifs HTML5 avec toutes leurs images et autres attributs comme des balises HTML standard, que vous pouvez modifier directement dans [!DNL Creative], soit dans une bibliothèque de contenus créatifs, soit dans une expérience individuelle (ce qui crée une variante du contenu créatif d’origine). Dans DSP, les contenus publicitaires flexibles d’HTML5 sont destinés à une seule taille d’annonce spécifique (en pixels). Vous pouvez éventuellement modifier les valeurs par défaut des attributs spécifiés dans un élément créatif HTML5 flexible. Par la suite, vous pouvez spécifier des valeurs personnalisées pour les attributs dans une expérience spécifique, ce qui crée une variante du contenu créatif parent.

Vous pouvez charger des contenus publicitaires HTML5 flexibles sous forme de fichiers ZIP ou utiliser l’un des modèles disponibles pour votre compte comme point de départ. Consultez les [spécifications des contenus publicitaires HTML5 flexibles](html5-creative-specification.md).

#### Conceptions HTML5

Vous pouvez charger des contenus publicitaires HTML5 simples ou statiques, avec tous les attributs et images spécifiés, sous forme de fichiers ZIP. Vous ne pouvez pas modifier d’attributs ni ajouter d’images ; au lieu de cela, chargez un nouveau fichier ZIP pour ajouter un nouveau contenu créatif. Consultez les [spécifications des contenus publicitaires HTML5 simples et statiques](html5-creative-specification.md).

#### Conceptions d’image

Vous pouvez inclure des éléments créatifs d’image au format GIF, JPEG, JPG ou PNG. Vous pouvez charger des images approuvées à partir de vos comptes Adobe Experience Manager ou des images à partir de votre appareil ou réseau.

Chaque expérience d’affichage et de publicité standard nécessite une image créative par défaut pour chaque taille de création attribuée à l’expérience.

#### Contenus publicitaires tiers

Saisissez les balises de suivi JavaScript pour les contenus publicitaires hébergés sur des serveurs de publicités tiers. Le script varie selon le serveur de publicités. Voici un exemple :

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### Conceptions vidéo {#creative-video-specs}

Vous pouvez télécharger des contenus vidéo propriétaires pour le web, les appareils mobiles ou les télévisions connectées depuis votre appareil ou réseau. Chaque expérience publicitaire vidéo standard nécessite une création vidéo par défaut pour chaque taille de création attribuée à l’expérience. Toutes les vidéos créatives sont transcodées automatiquement par DSP sous la forme de balises VAST 2.0 afin que vous puissiez les prévisualiser. Dans [!UICONTROL Tag Manager], vous pouvez éventuellement [appliquer un transcodage spécifique à l’éditeur](/help/creative/experiences/experience-tag-video-transcoding.md) à n’importe quelle balise d’expérience d’annonce vidéo.

Consultez les exigences de création vidéo suivantes.

**Type de fichier :** .mov, .mp4, .webm

**Taille du fichier :** max. 512 Mo

**Format vidéo :** 16:9, 4:3

**Résolution vidéo :** 640x360 pour 360p, 1 280x720 pour 720p, 1 920x1 080 pour 1 080p

**Durée de la vidéo :** maximum de 90 secondes

**Débit :** 600 à 1 200 kbit/s pour 360p, 1 500 à 2 500 kbit/s pour 720p, 3 000 à 5 000+ kbit/s pour 1 080p

**Fréquence d’image vidéo :** 23,98 i/s. Des tarifs d&#39;images supplémentaires peuvent être acceptés en fonction des exigences régionales ou de l&#39;éditeur

**Codec vidéo :** H.264 (norme industrielle), AV1, H.265

**Format audio :** ACC (standard de l’industrie/MP4), Opus (WebM/AV1)

**Débit audio :** 16 à 512 kbit/s

**Fréquence d’échantillonnage audio :** 44100-48000 Hz

**Fréquence audio :** 44,1 kHz ou 48 kHz

**Audio Autre :** le fichier chargé doit être non entrelacé, mélangé et contenir une piste audio. Il se peut qu’il n’y ait pas de son, mais une piste audio doit être incluse dans le fichier vidéo.

### Format pour les publicités dynamiques

Les utilisateurs administrateurs peuvent générer dynamiquement des contenus publicitaires au format statique HTML5 et dynamique HTML5 en mappant les variables dynamiques d’un modèle d’annonce publicitaire aux valeurs d’un fichier de flux. Les contenus publicitaires dynamiques peuvent inclure ceux de vos expériences Adobe Advertising Dynamic Creative Optimization (DCO) héritées.

## Les vues [!UICONTROL Creative Libraries]

Voir « [ Personnaliser vos vues de données »](/help/creative/introduction/customize-data-views.md) pour plus d’informations sur la personnalisation de chaque vue.

### La vue principale [!UICONTROL Creative Libraries]

La vue principale [!UICONTROL Creative Libraries] affiche toutes vos bibliothèques de création. Les données de chaque bibliothèque incluent le nombre d’expériences auxquelles les lots de la bibliothèque sont affectés, le nombre de lots, le nombre de contenus publicitaires, le nombre de tailles de contenus publicitaires, le nombre de cibles linguistiques par défaut, la date de création et la date de dernière modification apportée à un élément de la bibliothèque. Le mode Tableau comprend également une colonne pour l’annonceur.

Lorsque vous êtes en mode Carte, vous pouvez faire défiler les images d’une bibliothèque comportant plusieurs contenus publicitaires à l’aide des boutons &lt; et >.

#### Actions disponibles

* [Création d’une bibliothèque](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* Pour chaque bibliothèque de contenu créatif :

   * [Modification du nom d’une bibliothèque](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Ouvrez une bibliothèque pour afficher les contenus publicitaires et les lots affectés à la bibliothèque](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [Suppression de bibliothèques](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### Les vues [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

L’onglet [!UICONTROL Standard Ads] affiche tous les contenus publicitaires standard que vous avez créés. Les données de chaque élément créatif incluent la taille de l’élément créatif, le type d’élément créatif et la date de création. Le mode Tableau comprend également des colonnes pour la langue par défaut et la page de destination par défaut.

##### Actions disponibles

* [Ajout de contenus publicitaires standard à une bibliothèque](creative-add-standard.md)

* [Modification d’un contenu créatif standard](creative-edit-standard.md)

* [Aperçu d’un contenu créatif standard](creative-preview.md)

* [Ajoutez des contenus publicitaires standard aux lots d’affichage standard et supprimez les contenus publicitaires standard des lots d’affichage standard](creative-attach-detach-bundles.md)

* [Ajoutez des contenus publicitaires vidéo aux lots vidéo standard et supprimez-en certains d’entre eux](creative-attach-detach-bundles.md)

* [Dupliquer les contenus publicitaires standard](creative-duplicate.md)

* [Téléchargement de contenus publicitaires standard](creative-download.md)

* [Supprimer les contenus publicitaires standard](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

L’onglet [!UICONTROL Dynamic Ads] affiche tous les contenus publicitaires dynamiques créés dynamiquement pour vos catalogues créatifs, à l’exception de ceux que vous [avez supprimés manuellement](creative-delete.md) dans l’onglet [!UICONTROL Dynamic Ads]. Si vous [avez dupliqué manuellement](creative-duplicate.md) des contenus publicitaires dynamiques depuis le dernier traitement d’un catalogue, la liste des contenus publicitaires de ce catalogue inclut également les contenus publicitaires dupliqués.

Les données de chaque élément créatif incluent le type d’élément créatif, la taille de l’élément créatif, le nombre de catalogues auxquels il appartient et la date de création. Le mode Tableau comprend également des colonnes pour le modèle à partir duquel la création a été générée et le nombre d’offres.

>[!NOTE]
>
>Chaque fois qu’un catalogue est traité, les données sont actualisées pour les contenus publicitaires dynamiques existants de ce catalogue.

##### Actions disponibles

Actuellement, la possibilité de créer et de modifier des contenus publicitaires dynamiques est réservée à l’équipe du compte Adobe. Cependant, tous les utilisateurs peuvent :

* [Aperçu de contenus publicitaires dynamiques](creative-preview.md)

* [Ajout de contenus publicitaires dynamiques à des lots d’affichage dynamique et suppression de contenus publicitaires dynamiques d’un lot d’affichage dynamique](creative-attach-detach-bundles.md)

* [Duplication de contenus publicitaires dynamiques](creative-duplicate.md)

* [Suppression de contenus publicitaires dynamiques](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### La vue [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

La vue [!UICONTROL Bundles] affiche tous vos conteneurs de lots standard et dynamiques. Vous pouvez voir les noms des contenus publicitaires, les tailles de contenu publicitaire et les langues des contenus publicitaires inclus dans chaque lot. Lorsque vous êtes en mode Carte, vous pouvez faire défiler les images d’un lot avec plusieurs contenus publicitaires à l’aide des boutons &lt; et >.

#### Actions disponibles

* Ajoutez des lots d’affichage standard, vidéo standard et dynamique à une bibliothèque

* Répertorier et prévisualiser les contenus publicitaires d’une offre groupée

* Modifier le nom d’un lot

* Ajouter des contenus publicitaires d’affichage standard aux lots d’affichage standard et supprimer les contenus publicitaires d’affichage standard d’un lot d’affichage standard

* Ajoutez des contenus vidéo standard aux lots vidéo standard et supprimez des contenus vidéo standard d’un lot vidéo standard

* Dupliquer les lots

* Supprimer des lots

>[!MORELIKETHIS]
>
>* [Gestion des bibliothèques de création](/help/creative/creative-libraries/creative-library-manage.md)
>* [Ajouter des contenus publicitaires standard à une bibliothèque de contenus publicitaires](creative-add-standard.md)
>* [Gestion des offres groupées de création](bundle-manage.md)
>* [Personnaliser les vues de données](/help/creative/introduction/customize-data-views.md)
