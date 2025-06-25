---
title: Gestion des fichiers de flux de données d’inventaire
description: Découvrez comment configurer les paramètres qui contrôlent le traitement des données de flux.
exl-id: 7d19ecc0-c939-4996-b22b-970ce8644b09
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Gestion des fichiers de flux de données d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Si vous envoyez vos propres données de flux, vous devez charger des fichiers contenant vos données de produit pour créer de manière dynamique une structure de campagne, des publicités et des mots-clés en fonction de vos données de produit. Vous pouvez ensuite les associer à des modèles d’annonces publicitaires spécifiques au réseau publicitaire et traiter les données par le biais des modèles, puis publier les données sur les réseaux publicitaires appropriés. Vous pouvez associer plusieurs modèles à un fichier de flux, mais chaque modèle ne peut être associé qu’à un seul fichier de flux.

>[!NOTE]
>
>Ne téléchargez pas de fichiers si vous utilisez des données directement à partir d’un compte de centre commercial.

Vous pouvez charger et traiter des fichiers de flux de données de l’une des manières suivantes :

* **Automatiquement par FTP :** vous pouvez charger des fichiers directement dans un répertoire FTP ; le service de flux recherche les nouveaux fichiers toutes les deux heures. Après avoir chargé un fichier pour la première fois, vous pouvez l’associer à un modèle spécifique au réseau publicitaire. Par la suite, tous les fichiers que vous téléchargez portant le même nom sont automatiquement associés au même modèle. Selon la manière dont vous [configurez les paramètres des données de flux](feed-settings-manage.md), Search, Social et Commerce peuvent propager automatiquement les données de flux à travers tous les modèles applicables et éventuellement publier la campagne et les données publicitaires obtenues sur les réseaux publicitaires appropriés.

  Pour configurer un répertoire FTP afin de déposer et de traiter automatiquement les fichiers de données, contactez l’équipe chargée de votre compte Adobe.

* **Traitement manuel :** vous pouvez [charger manuellement des fichiers de flux](#feed-file-upload) à partir de la vue [!UICONTROL Advanced] (ACM). Après avoir associé un fichier de flux à un ou plusieurs [modèles](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) spécifiques au réseau publicitaire, vous pouvez générer des données de campagne et d’annonce publicitaire en [propageant les données de flux à travers les modèles](feed-data-propagate.md) en fonction des paramètres des données de flux [](feed-settings-manage.md). Vous pouvez également prévisualiser les données générées dans les vues de hiérarchie de campagne, générer un fichier de feuille d&#39;envoi groupé pour révision ou générer un fichier de feuille d&#39;envoi groupé pour une validation immédiate sur le réseau publicitaire. Si vous ne publiez pas les données immédiatement, vous pouvez [prévisualiser](propagated-data-view.md) et [les publier](propagated-data-post.md) plus tard. Vous pouvez ensuite [remplacer le fichier de flux existant par un nouveau fichier](#feed-file-replace) sans perdre les associations de modèles existantes.

## Exigences relatives aux fichiers de flux

Aucun champ de données spécifique n’est requis dans un fichier individuel, mais les éléments suivants sont requis pour chaque fichier :

* La première ligne du fichier doit contenir les noms des colonnes (également appelées *headers*), qui correspondent aux paramètres dynamiques dans les modèles associés. Les lignes restantes doivent inclure des données qui correspondent aux noms des colonnes. Chaque ligne de données (ligne) ne doit se rapporter qu’à un seul composant de compte, comme une campagne ou une annonce publicitaire. Les valeurs sur toutes les lignes doivent être séparées par des tabulations ou des virgules. Voir [fichier d’exemple CSV](#example-csv-feed-file) et [fichier d’exemple TSV](#example-tsv-feed-file) ci-dessous.

* Le fichier peut être de n’importe quelle taille, mais doit avoir l’une des extensions de fichier suivantes : `.tsv` (pour les valeurs séparées par des tabulations), `.txt` (pour le texte ASCII conforme à la norme [!DNL Unicode]), `.csv` (pour les valeurs séparées par des virgules) ou `.zip` (pour un seul fichier au format ZIP compressé, qui est décompressé en fichier TSV).

* Le nom de fichier est sensible à la casse et ne peut pas contenir les caractères suivants : `# % & * | \ : " < > . ? /`

* Si vous déposez des fichiers dans un répertoire FTP, vous devez utiliser le même nom de fichier pour chaque version du fichier.

* ([!DNL Google Ads] modèles uniquement) Si votre modèle utilise le paramètre Param2 ou Param2 ad dans les annonces textuelles, les champs de données correspondants dans le fichier de flux doivent inclure des données numériques, sans symboles monétaires.

* Pour mettre à jour les composants de compte existants, incluez le nom de la campagne existante (et ses composants, le cas échéant). Si la structure existante n’est pas spécifiée, de nouveaux composants sont créés.

### Exemple de fichier de flux séparé par des virgules {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### Exemple de fichier de flux séparé par des tabulations {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## Bonnes pratiques

* Pour les données qui incluent des caractères internationaux, utilisez des fichiers au format TSV ou TXT.

* Pour réaliser un processus répétable avec une révision ou une modification manuelle limitée, configurez les fichiers de flux et leurs données de structure de compte comme suit :

   * Incluez des colonnes et des lignes contenant suffisamment de données pour créer une structure de compte ou mapper à la structure de compte existante. Idéalement, utilisez une structure de compte existante étroitement liée à la taxonomie du produit et à laquelle les données de flux sont facilement mappées.

   * Incluez des descriptions suffisamment courtes pour être utilisées dans la copie publicitaire.

   * Utilisez des modèles de données et des conventions de nommage cohérents entre les lignes de produits.

   * Supprimez tous les espaces précédents et les espaces de fin.

   * Supprimez tous les caractères illisibles.

## Affichage ou téléchargement d’un fichier de flux

Vous pouvez ouvrir ou télécharger n’importe quel fichier de flux chargé manuellement ou par FTP.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Recherchez le fichier de flux :

1. Dans la liste des modèles, recherchez un modèle qui utilise le fichier de flux.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]** pour ouvrir une liste de tous les fichiers de flux.

1. Cliquez sur le nom du fichier de flux.

1. Ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur.

Pour plus d’informations, consultez l’aide en ligne de votre navigateur.

## Charger manuellement un fichier de flux {#feed-file-upload}

>[!NOTE]
> Si vous associez un modèle à un fichier téléchargé manuellement, puis que vous téléchargez par FTP un autre fichier portant le même nom, ayant la même extension et la même casse grammaticale, alors le fichier FTP est utilisé lorsque vous propagez les données par le biais du modèle. Par exemple, myfile.csv remplace myfile.csv, mais pas Myfile.CSV.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Upload]**.

1. Indiquez le fichier à charger en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur **[!UICONTROL Browse]** pour localiser le fichier sur votre appareil ou réseau.

1. Cliquez sur **[!UICONTROL Upload].

Tous les champs du fichier sont validés. Vous ne pouvez pas valider ultérieurement des éléments dont la longueur des champs n’est pas valide tant que vous n’avez pas corrigé les valeurs. Tous les noms de colonne du fichier sont disponibles dans les modèles en tant que paramètres dynamiques.

## Remplacer un fichier de flux {#feed-file-replace}

Lorsque vous remplacez un fichier de flux (même si le nouveau fichier a un nom ou une extension de fichier différent), toutes les associations de modèles existantes restent. Le nouveau fichier est utilisé lorsque vous propagez des données à travers tous les modèles initialement associés au fichier précédent.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Effectuez l’une des opérations suivantes :

   * Dans la colonne [!UICONTROL Feed] de tout modèle applicable, cliquez sur ![Plus d’options](/help/search-social-commerce/assets/options.png "Plus d’options") et sélectionnez **[!UICONTROL Re-upload]**.

   * Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]**. Dans la liste des fichiers de flux, cochez la case en regard du nom de fichier existant. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Upload]**.

   >[!NOTE]
   >
   >La source du fichier de flux (« [!UICONTROL FTP] » ou « &amp;mdash » pour les fichiers chargés manuellement) est incluse dans la colonne [!UICONTROL Source] .

1. Indiquez le fichier à charger en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur **[!UICONTROL Browse]** pour localiser le fichier sur votre appareil ou réseau.

Même si le nouveau fichier porte un nom ou une extension différent, le fichier existant est remplacé par le nouveau fichier.

1. Cliquez sur **[!UICONTROL Re-Upload]**.

Tous les champs du fichier sont validés. Vous ne pouvez pas valider ultérieurement des éléments dont la longueur des champs n’est pas valide tant que vous n’avez pas corrigé les valeurs. Tous les noms de colonne du fichier sont disponibles dans les modèles en tant que paramètres dynamiques.

## Supprimer les fichiers de flux

Vous pouvez supprimer n’importe quel fichier de flux chargé manuellement ou par FTP. Lorsque vous supprimez un fichier de flux, il n’est plus associé à aucun modèle.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]**.

1. Cochez la case en regard de chaque fichier à supprimer.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propager les données de flux par le biais de modèles](feed-data-propagate.md)
>* [Afficher les données générées à partir des flux](propagated-data-view.md)
>* [Modifier les données générées à partir des flux](propagated-data-edit.md)
>* [Publier les données de campagne générées à partir des flux sur les réseaux publicitaires](propagated-data-post.md)
>* [Arrêter un traitement de validation des données de flux de stock](stop-job.md)
>* [États des données générées à partir des flux](propagated-data-status.md)
