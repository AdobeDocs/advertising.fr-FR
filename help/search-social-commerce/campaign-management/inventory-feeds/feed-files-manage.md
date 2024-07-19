---
title: Gestion des fichiers de flux de données d’inventaire
description: Découvrez comment configurer les paramètres qui contrôlent le traitement des données de flux.
exl-id: 7d19ecc0-c939-4996-b22b-970ce8644b09
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Gestion des fichiers de flux de données d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Si vous envoyez vos propres données de flux, vous devez charger des fichiers contenant les données de votre produit pour créer dynamiquement la structure de campagne, les publicités et les mots-clés, en fonction des données de votre produit. Vous pouvez ensuite les associer à des modèles de publicité spécifiques au réseau et traiter les données par le biais des modèles, puis publier les données sur les réseaux publicitaires appropriés. Vous pouvez associer plusieurs modèles à un fichier de flux, mais chaque modèle peut être associé à un seul fichier de flux.

>[!NOTE]
>
>Ne transférez pas de fichiers si vous utilisez des données directement à partir d’un compte de centre commercial.

Vous pouvez charger et traiter des fichiers de flux de données de l’une des manières suivantes :

* **Automatiquement par FTP :** vous pouvez télécharger des fichiers directement dans un répertoire FTP ; le service de flux recherche les nouveaux fichiers toutes les deux heures. Après avoir chargé un fichier pour la première fois, vous pouvez l’associer à un modèle spécifique au réseau publicitaire. Par la suite, tous les fichiers que vous chargez portant le même nom sont automatiquement associés au même modèle. Selon la façon dont vous [configurez les paramètres de données de flux](feed-settings-manage.md), Search, Social et Commerce peut propager automatiquement les données de flux à l’aide de tous les modèles applicables et éventuellement publier les données de campagne et de publicité qui en résultent sur les réseaux publicitaires appropriés.

  Pour configurer un répertoire FTP afin de déposer et de traiter automatiquement les fichiers de données, contactez votre équipe de compte d’Adobe.

* **Traitement manuel :** Vous pouvez [ charger manuellement des fichiers de flux](#feed-file-upload) à partir de la vue [!UICONTROL Advanced] (ACM). Après avoir associé un fichier de flux à un ou plusieurs [modèles](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) spécifiques au réseau publicitaire, vous pouvez générer des données de campagne et de publicité en [propageant les données de flux par le biais des modèles](feed-data-propagate.md) en fonction des [ paramètres de données de flux](feed-settings-manage.md). Vous pouvez éventuellement prévisualiser les données générées dans les vues de hiérarchie de campagne, générer un fichier de feuille d’envoi groupé à des fins de révision ou générer un fichier de feuille d’envoi groupé en vue d’une publication immédiate sur le réseau publicitaire. Si vous ne publiez pas les données immédiatement, vous pouvez [les prévisualiser](propagated-data-view.md) et [les publier](propagated-data-post.md) ultérieurement. Vous pouvez ensuite [remplacer le fichier de flux existant par un nouveau fichier](#feed-file-replace) sans perdre aucune association de modèle existante.

## Exigences relatives aux fichiers de flux

Aucun champ de données spécifique n’est requis dans un fichier individuel, mais les éléments suivants sont requis pour chaque fichier :

* La première ligne du fichier doit contenir des noms de colonne (également appelés *headers*), qui correspondent aux paramètres dynamiques des modèles associés. Les lignes restantes doivent inclure des données correspondant aux noms des colonnes. Chaque ligne de données (ligne) ne doit se rapporte qu’à un seul composant de compte, tel qu’une campagne ou une publicité. Les valeurs de toutes les lignes doivent être séparées par des tabulations ou des virgules. Voir les [fichiers d’exemple CSV](#example-csv-feed-file) et [fichier d’exemple TSV](#example-tsv-feed-file) ci-dessous.

* Le fichier peut être de n’importe quelle taille, mais doit avoir l’une des extensions de fichier suivantes : `.tsv` (pour les valeurs séparées par des tabulations), `.txt` (pour le texte ASCII conforme à [!DNL Unicode]), `.csv` (pour les valeurs séparées par des virgules) ou `.zip` (pour un fichier unique au format ZIP compressé, qui se décompresse vers un fichier TSV).

* Le nom de fichier est sensible à la casse et ne peut pas contenir les caractères suivants : `# % & * | \ : " < > . ? /`

* Si vous déposez des fichiers dans un répertoire FTP, vous devez utiliser le même nom de fichier pour chaque version du fichier.

* ([!DNL Google Ads] modèles uniquement) Si votre modèle utilise le paramètre de publicité Param2 ou Param2 dans les publicités textuelles, les champs de données correspondants du fichier de flux doivent inclure des données numériques, sans symboles monétaires.

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

* Pour les données contenant des caractères internationaux, utilisez des fichiers au format TSV ou TXT.

* Pour obtenir un processus répétable avec une révision ou une modification manuelle limitée, configurez les fichiers de flux et les données de structure de compte comme suit :

   * Insérez des colonnes et des lignes qui contiennent suffisamment de données pour créer la structure du compte ou les mapper à la structure de compte existante. Idéalement, utilisez une structure de compte existante étroitement liée à la taxonomie du produit et à laquelle les données de flux sont facilement mappées.

   * Incluez des descriptions suffisamment courtes pour être utilisées dans la copie de publicité.

   * Utilisez des modèles de données cohérents et des conventions d’affectation de noms sur toutes les lignes de produits.

   * Supprimez tous les espaces précédents et les espaces à la fin.

   * Supprimez les caractères altérés.

## Afficher ou télécharger un fichier de flux

Vous pouvez ouvrir ou télécharger un fichier de flux qui a été chargé manuellement ou à l’aide de FTP.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

1. Recherchez le fichier de flux :

1. Dans la liste des modèles, recherchez un modèle qui utilise le fichier de flux.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]** pour ouvrir la liste de tous les fichiers de flux.

1. Cliquez sur le nom du fichier de flux.

1. Ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur.

Pour plus d’informations, voir l’aide en ligne de votre navigateur.

## Chargement manuel d’un fichier de flux {#feed-file-upload}

>[!NOTE]
> Si vous associez un modèle à un fichier téléchargé manuellement, puis que vous transférez par FTP un autre fichier portant le même nom, l’extension de fichier et la même casse grammaticale, le fichier FTP est alors utilisé lorsque vous propagez les données par le biais du modèle. Par exemple, myfile.csv remplace myfile.csv, mais Myfile.CSV ne le remplace pas.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Upload]**.

1. Indiquez le fichier à télécharger en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur **[!UICONTROL Browse]** pour localiser le fichier sur votre appareil ou votre réseau.

1. Cliquez sur **[!UICONTROL Upload].

Tous les champs du fichier sont validés. Vous ne pouvez pas publier les éléments dont la longueur de champ n’est pas valide plus tard tant que vous n’avez pas corrigé les valeurs. Tous les noms de colonne du fichier deviennent disponibles dans les modèles sous la forme de paramètres dynamiques.

## Remplacer un fichier de flux {#feed-file-replace}

Lorsque vous remplacez un fichier de flux (même si le nouveau fichier a un nom ou une extension de fichier différent), toutes les associations de modèles existantes restent inchangées. Le nouveau fichier est utilisé lorsque vous propagez des données à l’aide de tous les modèles qui étaient initialement associés au fichier précédent.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

1. Effectuez l’une des opérations suivantes :

   * Dans la colonne [!UICONTROL Feed] de tout modèle applicable, cliquez sur ![Plus d&#39;options](/help/search-social-commerce/assets/options.png "Plus d&#39;options") et sélectionnez **[!UICONTROL Re-upload]**.

   * Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]**. Dans la liste des fichiers de flux, cochez la case en regard du nom de fichier existant. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Upload]**.

   >[!NOTE]
   >
   >La source du fichier de flux (&quot;[!UICONTROL FTP]&quot; ou &quot;&amp;mdash&quot; pour les fichiers chargés manuellement) est incluse dans la colonne [!UICONTROL Source].

1. Indiquez le fichier à télécharger en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur **[!UICONTROL Browse]** pour localiser le fichier sur votre appareil ou votre réseau.

Même si le nouveau fichier porte un nom ou une extension de fichier différent, le fichier existant est remplacé par le nouveau fichier.

1. Cliquez sur **[!UICONTROL Re-Upload]**.

Tous les champs du fichier sont validés. Vous ne pouvez pas publier les éléments dont la longueur de champ n’est pas valide plus tard tant que vous n’avez pas corrigé les valeurs. Tous les noms de colonne du fichier deviennent disponibles dans les modèles sous la forme de paramètres dynamiques.

## Suppression de fichiers de flux

Vous pouvez supprimer tout fichier de flux qui a été chargé manuellement ou par FTP. Lorsque vous supprimez un fichier de flux, il n’est plus associé à aucun modèle.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]**.

1. Cochez la case en regard de chaque fichier à supprimer.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propager les données de flux par le biais de modèles](feed-data-propagate.md)
>* [Affichage des données générées à partir de flux](propagated-data-view.md)
>* [Modifier les données générées à partir de flux](propagated-data-edit.md)
>* [Données de campagne de publication générées à partir de flux vers les réseaux publicitaires](propagated-data-post.md)
>* [Arrêter une tâche de publication pour les données de flux d’inventaire](stop-job.md)
>* [États des données générées à partir de flux](propagated-data-status.md)
