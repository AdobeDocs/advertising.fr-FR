---
title: Gestion des fichiers de ressources
description: Découvrez comment charger et gérer un fichier de ressource pour un annonceur.
feature: Creative Dynamic Creatives
exl-id: 2fe2d778-8456-490a-bf44-234dbc08649f
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Gestion des fichiers de ressources

* Les publicités dynamiques HTML5 nécessitent un fichier de flux au format de feuille de calcul Microsoft Excel (XLSX) et les ressources d’image réelles référencées dans la feuille de calcul.

* Les publicités HTML5 statiques ne nécessitent qu’une seule ressource image par publicité.

* Les publicités vidéo nécessitent un fichier de flux au format de feuille de calcul Microsoft Excel (XLSX) et les ressources vidéo réelles référencées dans la feuille de calcul.

>[!NOTE]
>
> Vous ne pouvez utiliser chaque fichier de flux que pour un seul catalogue.

## Exigences relatives aux fichiers

* Publicités dynamiques HTML5 :

   * Fichier de flux au format CSV, TSV ou feuille de calcul Microsoft Excel (XLSX), avec une ligne d’en-tête et une ligne de données pour chaque variation publicitaire. Incluez un nom d’image dans chaque ligne à l’aide du `images/image_name` de format (`images/300x250_acme_logo.png`, par exemple).

     Les noms de champ spécifiques à l’annonceur doivent correspondre aux [champs disponibles pour les fichiers de flux publicitaires dynamiques](/help/creative/appendix-available-feed-fields.md).

   * Ressources d’image associées au format GIF, JPEG, JPG ou PNG.<!-- Is this true: The maximum file size is two (2) MB. --> Voir les [tailles créatives prises en charge](/help/creative/creative-libraries/creative-sizes.md).

  Vous pouvez charger un seul fichier XLSX, un seul fichier image ou un seul fichier ZIP contenant n’importe quelle combinaison de fichiers XLSX et d’image.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Publicités HTML5 statiques :

   * Une ressource image par annonce au format GIF, JPG, JPEG ou PNG.

     Vous pouvez charger une ou plusieurs images dans un fichier ZIP.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Publicités vidéo dynamiques :

   * Fichier de flux au format CSV, TSV ou feuille de calcul Microsoft Excel (XLSX), avec une ligne d’en-tête et une ligne de données pour chaque variation publicitaire. Insérez un nom de vidéo dans chaque ligne à l’aide du `videos/image_name` de format (`videos/300x250_acme_logo.png`, par exemple). Le fichier ZIP ne peut pas dépasser 512 Mo avec un maximum de 500 lignes.

     Les noms de champ spécifiques à l’annonceur doivent correspondre aux [champs disponibles pour les fichiers de flux publicitaires dynamiques](/help/creative/appendix-available-feed-fields.md).

     Pour tous les comptes disposant de vidéos dynamiques, la bonne pratique consiste à [créer un catalogue](catalog-manage.md) à l’aide du fichier de ressource avec une copie du modèle de flux universel [[!UICONTROL Adobe Creative Template]](feed-template-manage.md), dans lequel vous mappez chaque champ du fichier de ressource à un champ du serveur principal d’Advertising Creative.

   * Ressources vidéo associées au format MP4, MOV ou WEBM. Les modèles d’annonce pris en charge sont les suivants : carte de départ, carte d’extrémité, superposition supérieure, superposition inférieure ou en forme de L. La durée de chaque vidéo doit être comprise entre 1 et 90 secondes. Consultez les [tailles créatives prises en charge](/help/creative/creative-libraries/creative-sizes.md).

  Vous pouvez charger un seul fichier XLSX, un seul fichier image ou un seul fichier ZIP contenant n’importe quelle combinaison de fichiers XLSX et vidéo.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Chargement d’un fichier de ressource

>[!NOTE]
>
>Au lieu de charger des fichiers de ressource, vous pouvez également charger directement un catalogue lorsque vous [ajoutez des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-dynamic.md). Tous les catalogues que vous y créez sont disponibles dans la vue [!UICONTROL Catalogs] pour une utilisation ultérieure.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Assets]** .

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]** > **[!UICONTROL Asset]**.

1. Configurez le fichier de ressource :

   1. Sélectionnez l’annonceur qui peut accéder au fichier de ressource.

   1. Spécifiez le fichier de ressource de l’une des manières suivantes :

      * Faites glisser et déposez un fichier sur votre appareil ou réseau dans la zone.

      * Cliquez sur **[!UICONTROL Select a file]** pour localiser le fichier sur votre appareil ou réseau.

   1. Cliquez sur **[!UICONTROL Upload]**.

Tous les fichiers ZIP sont décompressés automatiquement. Lorsque vous chargez un fichier de feuille de calcul, ce dernier est répertorié dans le sous-onglet [!UICONTROL Feeds]. Lorsque vous téléchargez un fichier image, ce dernier est répertorié dans le sous-onglet [!UICONTROL Images] .

## Télécharger un fichier de ressource

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Assets]** .

1. Placez le curseur au-dessus de la ligne de la ressource, puis cliquez sur **[!UICONTROL Download]**.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

## Suppression d’un fichier de ressource

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Cliquez sur l’onglet **[!UICONTROL Assets]** .

1. Placez le curseur au-dessus de la ligne de la ressource, puis cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Champs disponibles pour les fichiers de flux de publicités dynamiques](/help/creative/appendix-available-feed-fields.md)
>* [Workflows pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gérer les modèles de flux](/help/creative/feeds/feed-template-manage.md)
>* [Gérer les catalogues](/help/creative/feeds/catalog-manage.md)
>* [Gestion des modèles de publicité dynamique](/help/creative/ad-templates/ad-template-manage.md)
>* [Ajouter des contenus publicitaires dynamiques à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-dynamic.md)
