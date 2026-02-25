---
title: Chargement des données de compte hors ligne pour les rapports et les simulations
description: Découvrez comment charger manuellement des données de compte hors ligne ou les transférer vers un compartiment  [!DNL Amazon] [!DNL S3] pour la prise en charge des rapports et de la simulation. Les fichiers journaux consignent la progression des tâches de chargement.
source-git-commit: bfa5403ff66bed73797fc4c7115b8c043856745d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Chargement des données de compte hors ligne pour les rapports et les simulations

*Annonceurs activés pour les chargements de données de compte*

Chargez le contenu de la campagne et les données de coût, de clic et de conversion hors ligne pour un compte sans prise en charge d’API pour les rapports et les simulations de performances.

Vous pouvez suivre la progression de vos tâches de chargement à l’aide de la fonctionnalité [!UICONTROL Upload Logs] :

* Affichez la liste de chaque fichier chargé pour le compte. Les informations sur chaque tâche de chargement de fichier comprennent le nom du fichier, le canal de chargement (*[!UICONTROL Cloud Storage]* ou *[!UICONTROL Drag & Drop]*), la date et le statut de synchronisation, ainsi que les raisons des chargements incomplets.

* Téléchargez un fichier contenant les entités de compte et les mesures associées chargées pour n’importe quelle tâche. Les fichiers sont au format CSV (valeurs séparées par des virgules).

## Chargement manuel des données de compte

Vous pouvez renseigner un compte avec le contenu et le coût de la campagne, les clics et les données de conversion en chargeant manuellement les données dans un fichier .

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Effectuez l’une des opérations suivantes :

   * (Vue [!UICONTROL Accounts]) :

      1. Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Upload]** dans la barre d’outils des actions en masse.

      1. Faites glisser un fichier dans la zone ou cliquez sur **[!UICONTROL Browse Files]** et choisissez un fichier sur votre appareil ou réseau.

      1. Cliquez sur **[!UICONTROL Upload Files]**.

   * (Dans les paramètres du compte) :

      1. Sélectionnez le compte de l’une des manières suivantes :

         * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

         * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

      1. Cliquez sur l’onglet **[!UICONTROL Upload File]** .

      1. Faites glisser un fichier dans la zone ou cliquez sur **[!UICONTROL Browse Files]** et choisissez un fichier sur votre appareil ou réseau.

      1. Cliquez sur **[!UICONTROL Save]**.

&#x200B;# Charger les données de compte dans un compartiment de [!DNL Amazon] [!DNL S3] {#data-upload-s3}

Vous pouvez renseigner un compte avec du contenu et des données de coût de campagne, de clics et de conversion en chargeant les données dans un dossier Search, Social et Commerce affecté dans un compartiment [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]).

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Contactez l’équipe chargée de votre compte Adobe pour activer le chargement des données de compte pour votre compte d’annonceur Search, Social et Commerce. L’équipe facilitera la création d’un dossier spécifique à l’organisation dans un compartiment [!DNL S3] et vous informera une fois l’opération terminée.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* Récupérez le chemin d’accès de stockage dans le cloud [!DNL S3], l’ID de clé d’accès et la clé d’accès secrète pour votre compte. Le même ID de clé d’accès et la même clé d’accès secrète sont utilisés pour tous les comptes <!-- naming convention?--> de chargement de données de l’organisation.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Effectuez l’une des opérations suivantes :

   * (Vue [!UICONTROL Accounts]) :

      1. Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Upload]** dans la barre d’outils des actions en masse.

      1. Dans la zone de [!UICONTROL Cloud Storage Link], cliquez sur **[!UICONTROL Go to the Link]**.

      1. Cliquez sur **[!UICONTROL Show Access Key and Secret]**.

      1. En regard du champ [!UICONTROL Storage Link] , cliquez sur **[!UICONTROL Copy]** pour copier le lien dans le presse-papiers et le stocker dans un emplacement sécurisé.

      1. De même, copiez et stockez en toute sécurité les valeurs [!UICONTROL Access Key] et [!UICONTROL Secret Key].

      1. Cliquez sur **[!UICONTROL Done]**.

   * (Dans les paramètres du compte) :

      1. Sélectionnez le compte de l’une des manières suivantes :

         * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

         * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

      1. Cliquez sur l’onglet **[!UICONTROL Upload File]** .

      1. Dans la zone de [!UICONTROL Cloud Storage Link], cliquez sur **[!UICONTROL Go to the Link]**.

      1. Cliquez sur **[!UICONTROL Show Access Key and Secret]**.

      1. En regard du champ [!UICONTROL Storage Link] , cliquez sur **[!UICONTROL Copy]** pour copier le lien dans le presse-papiers et le stocker dans un emplacement sécurisé.

      1. De même, copiez et stockez en toute sécurité les valeurs [!UICONTROL Access Key] et [!UICONTROL Secret Key].

      1. Cliquez sur **[!UICONTROL Done]**.

      1. Cliquez sur **[!UICONTROL Save]**.

1. (Une fois par organisation) Configurez votre environnement AWS local :

   1. Téléchargez et installez [!DNL AWS Command Line Interface] (interface de ligne de commande AWS) à l’emplacement suivant : [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Configurez vos informations d’identification AWS :

      1. Créez un fichier en texte brut et nommez-le `~/.aws/credentials` (sans extension de fichier).

      1. Ouvrez le fichier dans n’importe quel éditeur de texte et saisissez l’ID de clé d’accès et la clé d’accès secrète de l’organisation comme suit :

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Téléchargez le rapport de données de votre compte depuis le réseau publicitaire et enregistrez-le.

1. Dans l’interface de ligne de commande d’AWS, exécutez la commande suivante pour charger les données de votre compte vers votre emplacement cloud [!DNL S3].

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Exemple : `aws s3 cp filename.txt s3://cloud-location/`

## Afficher un journal des fichiers de données de compte chargés

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Upload Logs]**.

1. (Facultatif) Pour télécharger les données d’un fichier téléchargé, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") dans la colonne [!UICONTROL Download] et téléchargez le fichier conformément à la procédure normale de votre navigateur.

## Données requises

Les données doivent respecter les exigences en matière de données pour le réseau publicitaire. Les champs de données de chaque entité peuvent varier en fonction du réseau publicitaire.
