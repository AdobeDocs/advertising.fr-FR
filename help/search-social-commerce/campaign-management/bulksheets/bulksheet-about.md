---
title: À propos de la gestion des données de campagne à l'aide de feuilles d'envoi groupé
description: Découvrez les fonctionnalités des feuilles d’envoi groupé disponibles par réseau publicitaire, le workflow des feuilles d’envoi groupé et la gestion des erreurs.
exl-id: 34a16ee3-9eba-4b8b-a5ca-65318f4ee6c5
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# À propos de la gestion des données de campagne à l&#39;aide de feuilles d&#39;envoi groupé

Une feuille d’envoi groupé est un fichier qui contient des données de campagne dans un format spécifique et qui peut être utilisé pour créer ou modifier rapidement des données de structure de campagne et de groupe publicitaire, ainsi que des annonces textuelles. Vous pouvez générer (télécharger) des feuilles d’envoi groupé contenant des données pour un ou plusieurs comptes, pour des campagnes et des groupes publicitaires spécifiques, ou même pour des annonces textuelles, des emplacements et des groupes de produits spécifiques. Vous pouvez utiliser des feuilles d’envoi groupé pour gérer des jeux de données volumineux ou apporter de petites modifications. Chaque réseau publicitaire nécessite différentes colonnes d’informations.

Vous pouvez générer des feuilles d’envoi groupé avec autant de données que vous le souhaitez ou, facultativement, les créer manuellement et les charger (consultez le chapitre sur les « Données requises/incluses dans les feuilles d’envoi groupé »).

Une fois que vous avez créé une feuille d’envoi groupé, vous pouvez identifier les pages de destination endommagées qui doivent être corrigées, ou les données supplémentaires à ajouter ou modifier. Vous pouvez ensuite modifier le fichier et le charger dans Search, Social et Commerce, en le planifiant éventuellement pour qu’il soit publié immédiatement ou ultérieurement sur le réseau publicitaire approprié. Vous pouvez également publier une feuille d’envoi groupé disponible immédiatement ou ultérieurement.

Vous pouvez éventuellement charger des fichiers de feuilles d&#39;envoi groupé vers un compte FTP spécifié pour la récupération et la validation automatique. Le répertoire est analysé toutes les heures et les nouveaux fichiers sont publiés sur le réseau de recherche dans l&#39;ordre dans lequel ils sont reçus.

Toutes les feuilles d’envoi groupé, les fichiers d’erreur de validation de page de destination et les autres fichiers d’erreur sont automatiquement supprimés 30 jours après leur création, sauf si vous les supprimez plus tôt.

## Fonctionnalité par réseau publicitaire

* **Télécharger, charger et publier :** comptes [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Yandex]

* **Télécharger et charger uniquement :** comptes [!DNL Naver]

  Vous pouvez charger des données [!DNL Naver] pour les utiliser dans Search, Social et Commerce, mais vous ne pouvez pas les publier sur le réseau publicitaire. Vous pouvez également télécharger vos données existantes (non synchronisées).

* **Télécharger les données uniquement :** comptes [!DNL Pinterest], [!DNL Yahoo Native] et [!DNL Yahoo! Display Network]

  Vous pouvez télécharger vos données existantes (non synchronisées).

## Présentation de l’utilisation des feuilles d’envoi groupé

Les étapes standard d’utilisation des feuilles d’envoi groupé pour les comptes synchronisés sont les suivantes :

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Téléchargez les données d’un ou de plusieurs comptes, campagnes ou groupes publicitaires dans un fichier de feuille d’envoi groupé](bulksheet-download.md). Vous pouvez éventuellement remplir manuellement une feuille d’envoi groupé spécifique au réseau publicitaire et charger le fichier.

1. [Validez les pages de destination](bulksheet-validate-landing-pages.md) dans les URL de base (finales) ou de destination dans le fichier .

1. Lorsque vous devez ajouter des données ou apporter des corrections :

   1. [Exportez le fichier](bulksheet-export.md) sur votre bureau et modifiez-le dans [!DNL Microsoft Excel].

   1. [Chargez manuellement le fichier modifié](bulksheet-upload.md) dans Search, Social et Commerce, ou [chargez le fichier sur un compte FTP spécifié](bulksheet-ftp-account.md) pour une publication automatique.

1. (Pour les fichiers chargés manuellement) [Publiez le fichier](bulksheet-post.md) sur le réseau publicitaire au fur et à mesure de son chargement ou ultérieurement.

1. (Si nécessaire) Téléchargez les nouveaux fichiers d’erreur, corrigez les lignes et republiez le fichier.

## Gérer les erreurs de chargement et de publication des données de campagne

Les services Search, Social et Commerce chargent et publient autant de lignes de données que possible à partir d’une feuille de données de campagne, y compris les URL de tracking qu’ils génèrent si nécessaire.

Lorsque des erreurs se produisent pendant le fonctionnement de feuilles d&#39;envoi groupé, l&#39;un des deux types de fichiers d&#39;erreur suivants est généré :

* **[!UICONTROL EF Errors]:** lorsqu’un fichier ou des lignes individuelles du fichier ne peuvent pas être chargés ou traités, un fichier d’erreur appelé `<uploaded file name>_ef_errors.<extension used for the bulksheet>` est créé. Si le problème concerne des lignes individuelles, ces lignes sont incluses, avec une explication de chaque erreur afin qu’elle puisse être corrigée.

* **[!UICONTROL SE Errors]:** Lorsqu’un fichier est publié mais que le réseau publicitaire n’accepte pas une partie ou la totalité des données, un fichier d’erreur appelé `<uploaded file name>_se_errors.<extension used for the bulksheet>` est créé. Lorsque certaines lignes ont été acceptées, mais pas toutes, le fichier d’erreur affiche les lignes qui n’ont pas été publiées et une explication de chaque erreur afin qu’elle puisse être corrigée. Les messages d’erreur s’affichent dans les trois dernières colonnes de chaque ligne.

>[!NOTE]
>
>Si vous publiez des publicités [!DNL Google Ads] qui enfreignent les politiques publicitaires du réseau publicitaire, mais qui peuvent être admissibles à des exemptions, alors ces publicités sont automatiquement republiées avec des demandes d&#39;exemption. Si la demande d’exemption échoue, les informations sur la violation sont incluses dans le fichier d’erreur.

Vous pouvez télécharger l’un des types de fichier d’erreur, apporter des corrections directement dans les lignes, puis recharger et publier le fichier.

Les fichiers d’erreur sont automatiquement supprimés après 30 jours, sauf si vous les supprimez plus tôt.

## Informations sur chaque fichier

Tous les fichiers de données téléchargés, les fichiers téléchargés et les fichiers d’erreur sont disponibles à partir de [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets].

Les informations de chaque fichier incluent le statut actuel de la tâche, le pourcentage de la tâche qui est terminé, la date de création, (le cas échéant) la date à laquelle elle a été ou sera publiée sur le réseau publicitaire spécifié, la date de suppression prévue et le nom de connexion de l’utilisateur qui a initié la tâche.

>[!MORELIKETHIS]
>
>* [Télécharger/créer un fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Charger une feuille d’envoi groupé ou un fichier d’erreur corrigé](bulksheet-upload.md)
>* [Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](bulksheet-post.md)
>* [Exporter un fichier de feuille d’envoi groupé généré ou chargé](bulksheet-export.md)
