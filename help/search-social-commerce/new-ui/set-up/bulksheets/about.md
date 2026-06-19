---
title: (Nouvelle interface utilisateur) À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupé
description: Découvrez les fonctionnalités des feuilles d’envoi groupé disponibles par réseau publicitaire, le workflow des feuilles d’envoi groupé et la gestion des erreurs dans la nouvelle interface utilisateur de Search, Social et Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 772
ht-degree: 0%

---

# (Nouvelle interface utilisateur) À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupé

Une feuille d’envoi groupé est un fichier qui contient des données de campagne dans un format spécifique et qui peut être utilisé pour créer ou modifier rapidement des données de structure de campagne et de groupe publicitaire, ainsi que des annonces textuelles. Vous pouvez générer (télécharger) des feuilles d’envoi groupé contenant des données pour un ou plusieurs comptes, pour des campagnes et des groupes publicitaires spécifiques, ou même pour des annonces textuelles, des emplacements et des groupes de produits spécifiques. Vous pouvez utiliser des feuilles d’envoi groupé pour gérer des jeux de données volumineux ou apporter de petites modifications. Chaque réseau publicitaire nécessite différentes colonnes d’informations.

Vous pouvez générer des feuilles d’envoi groupé contenant autant de données que vous le souhaitez ou, éventuellement, les créer manuellement et les charger. Consultez les sections « [Données requises et incluses dans les feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-file-formats.md) » pour connaître les exigences en matière de format de fichier, et « [Opérations que vous pouvez effectuer dans les feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) » pour connaître les opérations prises en charge par le réseau publicitaire.

Une fois que vous avez créé une feuille d’envoi groupé, vous pouvez identifier les pages de destination endommagées qui doivent être corrigées, ou les données supplémentaires à ajouter ou modifier. Vous pouvez ensuite modifier le fichier et le charger dans Search, Social et Commerce, en le planifiant éventuellement pour qu’il soit publié immédiatement ou ultérieurement sur le réseau publicitaire approprié. Vous pouvez également publier une feuille d’envoi groupé disponible immédiatement ou ultérieurement.

Toutes les feuilles d’envoi groupé, les fichiers d’erreur de validation de page de destination et les autres fichiers d’erreur sont automatiquement supprimés 30 jours après leur création, sauf si vous les supprimez plus tôt.

## Fonctionnalité par réseau publicitaire {#bulksheet-functionality-by-network}

* **Télécharger, charger et publier :** comptes [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Yandex]

* **Télécharger et charger uniquement :** comptes [!DNL Naver]

  Vous pouvez charger des données [!DNL Naver] pour les utiliser dans Search, Social et Commerce, mais vous ne pouvez pas les publier sur le réseau publicitaire. Vous pouvez également télécharger vos données existantes (non synchronisées).

* **Télécharger les données uniquement :** comptes [!DNL Pinterest], [!DNL Yahoo DSP] [!DNL Yahoo Native]

  Vous pouvez télécharger vos données existantes (non synchronisées).

## Présentation de l’utilisation des feuilles d’envoi groupé

Les étapes standard d’utilisation des feuilles d’envoi groupé avec des comptes synchronisés sont les suivantes :

1. [Téléchargez les données d’un ou de plusieurs comptes, campagnes ou groupes publicitaires dans un fichier de feuille d’envoi groupé](download.md). Vous pouvez éventuellement remplir manuellement une feuille d’envoi groupé spécifique au réseau publicitaire et charger le fichier.

1. [Validez les pages de destination](validate-landing-pages.md) dans les URL de base (finales) ou de destination dans le fichier .

1. Lorsque vous devez ajouter des données ou apporter des corrections :

   1. Exportez le fichier sur votre bureau et modifiez-le dans [!DNL Microsoft Excel].

   1. [Chargez manuellement le fichier modifié](upload.md) dans Search, Social et Commerce.

1. (Pour les fichiers chargés manuellement) [Publiez le fichier](post.md) sur le réseau publicitaire au fur et à mesure de son chargement ou ultérieurement.

1. (Si nécessaire) Téléchargez les nouveaux fichiers d’erreur, corrigez les lignes et republiez le fichier.

## Gérer les erreurs de chargement et de publication des données de campagne

Les services Search, Social et Commerce chargent et publient autant de lignes de données que possible à partir d’une feuille d’envoi groupé de campagne, y compris les URL de tracking qu’ils génèrent si nécessaire.

Lorsque des erreurs se produisent au cours d’une opération de feuilles d’envoi groupé, l’un des deux types de fichiers d’erreur suivants est généré :

* **[!UICONTROL EF Errors]:** lorsqu’un fichier ou des lignes individuelles du fichier ne peuvent pas être chargés ou traités, un fichier d’erreur appelé `<uploaded file name>_ef_errors.<extension used for the bulksheet>` est créé. Si le problème concerne des lignes individuelles, ces lignes sont incluses, avec une explication de chaque erreur afin qu’elle puisse être corrigée.

* **[!UICONTROL SE Errors]:** Lorsqu’un fichier est publié mais que le réseau publicitaire n’accepte pas une partie ou la totalité des données, un fichier d’erreur appelé `<uploaded file name>_se_errors.<extension used for the bulksheet>` est créé. Lorsque certaines lignes ont été acceptées, mais pas toutes, le fichier d’erreur affiche les lignes qui n’ont pas été publiées et une explication de chaque erreur afin qu’elle puisse être corrigée. Les messages d’erreur s’affichent dans les trois dernières colonnes de chaque ligne.

>[!NOTE]
>
>Si vous publiez des publicités [!DNL Google Ads] qui enfreignent les politiques publicitaires du réseau publicitaire mais qui peuvent être admissibles à des exemptions, ces publicités sont automatiquement republiées avec des demandes d&#39;exemption. Si la demande d’exemption échoue, les informations sur la violation sont incluses dans le fichier d’erreur.

Vous pouvez télécharger l’un des types de fichier d’erreur, apporter des corrections directement dans les lignes, puis recharger et publier le fichier.

Les fichiers d’erreur sont automatiquement supprimés après 30 jours, sauf si vous les supprimez plus tôt.

## Informations sur chaque fichier

Tous les fichiers de données téléchargés, les fichiers téléchargés et les fichiers d&#39;erreur sont disponibles à partir de [!UICONTROL Setup] \> [!UICONTROL Bulksheets].

Les informations de chaque fichier incluent le statut actuel de la tâche, le pourcentage de la tâche qui est terminé, la date de création, (le cas échéant) la date à laquelle elle a été ou sera publiée sur le réseau publicitaire spécifié, la date de suppression prévue et le nom de connexion de l’utilisateur qui a initié la tâche.

>[!MORELIKETHIS]
>
>* [(nouvelle interface utilisateur) Télécharger/créer un fichier de feuille d’envoi groupé](download.md)
>* [(Nouvelle interface utilisateur) Chargez une feuille d’envoi groupé ou un fichier d’erreur corrigé](upload.md)
>* [(Nouvelle interface utilisateur) Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](post.md)
>* [(nouvelle interface utilisateur) Valider les pages de destination dans des fichiers de feuille d’envoi groupé](validate-landing-pages.md)
>* [(Nouvelle interface utilisateur) Supprimer les feuilles d’envoi groupé et les fichiers d’erreur chargés](delete.md)
>* [(nouvelle interface utilisateur) Arrêter un traitement groupé en cours](stop-job.md)
