---
title: A propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées
description: Découvrez la fonctionnalité de feuille d’envoi groupé disponible par le réseau publicitaire, le workflow de feuille d’envoi groupé et la gestion des erreurs.
exl-id: 34a16ee3-9eba-4b8b-a5ca-65318f4ee6c5
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# A propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées

Une feuille d’envoi groupé est un fichier qui contient des données de campagne dans un format spécifique et qui peut être utilisé pour créer ou modifier rapidement des données de structure de campagne et de groupe publicitaire et des publicités textuelles. Vous pouvez générer (télécharger) des feuilles d’envoi groupées avec des données pour un ou plusieurs comptes, pour des campagnes et des groupes publicitaires spécifiques, ou même pour des annonces textuelles, des emplacements et des groupes de produits spécifiques. Vous pouvez utiliser des feuilles d’envoi groupées pour gérer des jeux de données volumineux ou apporter de petites modifications. Chaque réseau d’annonces nécessite différentes colonnes d’informations.

Vous pouvez générer des feuilles d’envoi groupées avec autant de données que vous le souhaitez, ou éventuellement les créer manuellement et les charger (reportez-vous au chapitre &quot;Données obligatoires/incluses dans les feuilles d’envoi groupées&quot;).

Une fois que vous avez créé une feuille d’envoi groupée, vous pouvez identifier toutes les pages d’entrée rompues qui doivent être corrigées ou les données supplémentaires à ajouter ou à modifier. Vous pouvez ensuite modifier le fichier et le charger dans Search, Social et Commerce, en programmant éventuellement sa publication sur le réseau publicitaire approprié immédiatement ou ultérieurement. Vous pouvez également publier une feuille d’envoi groupé disponible immédiatement ou ultérieurement.

Vous pouvez éventuellement charger des fichiers de feuille d’envoi groupé vers un compte FTP spécifié pour récupération et publication automatique. Le répertoire est analysé toutes les heures et de nouveaux fichiers sont publiés sur le réseau de recherche dans l’ordre dans lequel ils sont reçus.

Toutes les feuilles d’envoi groupé, les fichiers d’erreur de validation de page d’entrée et les autres fichiers d’erreur sont automatiquement supprimés 30 jours après leur création, sauf si vous les supprimez plus tôt.

## Fonctionnalité par réseau publicitaire

* **Téléchargez, chargez et publiez :**  [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], et [!DNL Yandex] comptes

* **Télécharger et télécharger uniquement :** [!DNL Naver] comptes

  Vous pouvez télécharger des [!DNL Naver] données à utiliser dans Search, Social et Commerce, mais ne peuvent pas les publier sur le réseau publicitaire. Vous pouvez également télécharger vos données existantes (non synchronisées).

* **Téléchargement des données uniquement :**  [!DNL Pinterest], [!DNL Yahoo Native], et [!DNL Yahoo! Display Network] comptes

  Vous pouvez télécharger vos données existantes (non synchronisées).

## Présentation de l’utilisation des feuilles d’envoi groupées

Les étapes standard d’utilisation des feuilles d’envoi groupées pour les comptes synchronisés sont les suivantes :

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Télécharger des données pour un ou plusieurs comptes, campagnes ou groupes publicitaires dans un fichier de feuille d’envoi groupé](bulksheet-download.md). Vous pouvez éventuellement remplir manuellement une feuille d’envoi groupé spécifique au réseau publicitaire et télécharger le fichier.

1. [Validation des landing pages](bulksheet-validate-landing-pages.md) dans les URL de base (finales) ou de destination du fichier.

1. Lorsque vous devez ajouter des données ou apporter des corrections :

   1. [Exporter le fichier](bulksheet-export.md) sur votre bureau et modifiez-le dans [!DNL Microsoft Excel].

   1. [Chargement manuel du fichier modifié](bulksheet-upload.md) vers Search, Social &amp; Commerce ou [télécharger le fichier vers un compte FTP spécifié ;](bulksheet-ftp-account.md) pour la publication automatique.

1. (Pour les fichiers chargés manuellement) [Publier le fichier](bulksheet-post.md) sur le réseau publicitaire au fur et à mesure que vous le téléchargez ou plus tard.

1. (Si nécessaire) Téléchargez de nouveaux fichiers d’erreur, corrigez les lignes et republiez le fichier.

## Gestion des erreurs lors du transfert et de la publication de données de campagne

Le module de recherche, Social et Commerce télécharge et publie autant de lignes de données que possible à partir d’une feuille de calcul de campagne, y compris les URL de suivi qu’il génère si nécessaire.

Lorsque des erreurs se produisent lors de l’opération de feuille d’envoi groupé, l’un des deux types de fichiers d’erreur suivants est généré :

* **[!UICONTROL EF Errors]:**  Lorsqu’un fichier ou des lignes individuelles du fichier ne peuvent pas être chargés ou traités, un fichier d’erreur appelé `<uploaded file name>_ef_errors.<extension used for the bulksheet>` est créée. Si le problème concerne des lignes individuelles, ces lignes sont incluses, avec une explication de chaque erreur afin qu’elles puissent être corrigées.

* **[!UICONTROL SE Errors]:**  Lorsqu’un fichier est publié mais que le réseau publicitaire n’accepte pas toutes ou une partie des données, un fichier d’erreur appelé `<uploaded file name>_se_errors.<extension used for the bulksheet>` est créée. Lorsque certaines lignes ont été acceptées, mais pas toutes, le fichier d’erreur affiche les lignes qui n’ont pas été publiées et une explication de chaque erreur afin qu’elles puissent être corrigées. Les messages d’erreur sont affichés dans les trois dernières colonnes de chaque ligne.

>[!NOTE]
>
>Si vous publiez des [!DNL Google Ads] les publicités qui enfreignent les politiques publicitaires du réseau publicitaire, mais qui peuvent être admissibles à des exemptions, sont alors automatiquement republiées avec les demandes d’exemption. Si la demande d’exemption échoue, les informations sur la violation sont incluses dans le fichier d’erreur.

Vous pouvez télécharger l’un ou l’autre des types de fichiers d’erreur, apporter des corrections directement dans les lignes, puis télécharger à nouveau et publier le fichier.

Les fichiers d’erreur sont automatiquement supprimés au bout de 30 jours, sauf si vous les supprimez plus tôt.

## Informations sur chaque fichier

Tous les fichiers de données, fichiers et fichiers d’erreur téléchargés sont disponibles à partir de [!UICONTROL Search] > [!UICONTROL Bulksheets].

Les informations de chaque fichier incluent l’état actuel de la tâche et le pourcentage de la tâche terminée, la date de création, (le cas échéant) la date à laquelle elle a été ou sera publiée sur le réseau publicitaire spécifié, la date de suppression planifiée et le nom de connexion de l’utilisateur qui a lancé la tâche.

>[!MORELIKETHIS]
>
>* [Téléchargement/création d’un fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Télécharger une feuille d’envoi groupé ou un fichier d’erreur corrigé](bulksheet-upload.md)
>* [Publier des feuilles d’envoi groupées ou des fichiers d’erreur corrigés](bulksheet-post.md)
>* [Exportation d’un fichier de feuille d’envoi groupé généré ou transféré](bulksheet-export.md)
