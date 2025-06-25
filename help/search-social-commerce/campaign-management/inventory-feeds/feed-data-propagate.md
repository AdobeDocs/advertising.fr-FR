---
title: Propager les données de flux d’inventaire par le biais de modèles
description: Découvrez comment propager les données de vos flux d’inventaire par le biais de modèles d’annonce pour gérer la structure de compte et diffuser des annonces dynamiques.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Propager les données de flux d’inventaire par le biais de modèles

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Après avoir créé un modèle de flux spécifique au réseau publicitaire et associé un fichier de flux ou un compte de centre commercial [!DNL Google] ou [!DNL Microsoft] à celui-ci, vous pouvez créer dynamiquement des publicités en propageant les données de flux à travers le modèle en fonction des [ paramètres des données de flux ](feed-settings-manage.md). Lors de la propagation, les noms des colonnes du modèle sont remplacés par les valeurs de données du flux. Les campagnes générées et leurs composants présentent les paramètres par défaut, sauf indication contraire du modèle. Selon les options du modèle, Search, Social et Commerce crée une structure de compte (campagnes, groupes publicitaires, mots-clés) pour les annonces ou mappe les annonces à la structure de compte existante.

Lorsque de nouvelles données de flux contiennent de nouvelles valeurs de données pour un élément ou que le modèle a été modifié, les publicités existantes sont supprimées et de nouvelles publicités sont créées. Si la seule modification est la désignation [!DNL Google Ads] paramètre 1 et du paramètre 2, seules ces valeurs sont mises à jour. Les publicités en double (la même copie de publicité et la même page de destination) ne sont jamais créées.

Lorsque vous propagez des données, vous pouvez éventuellement prévisualiser les données générées dans une vue hiérarchique de campagne, générer un fichier de feuille d&#39;envoi groupé pour révision ou générer un fichier de feuille d&#39;envoi groupé pour une validation immédiate sur le réseau publicitaire. Lorsque chaque action de propagation est terminée, un résumé de propagation est ajouté à l&#39;onglet Propagations, indiquant le nombre de chaque type d&#39;entité qui a été ou serait créé, mis en pause ou supprimé en fonction de la propagation. Si vous ne publiez pas les données immédiatement, vous pouvez les prévisualiser et les publier ultérieurement.

## Propager les fichiers de flux depuis l’onglet [!UICONTROL Templates]

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Cochez la case en regard des modèles à propager.

1. Dans la barre d’outils, cliquez sur **[!UICONTROL Propagate]**, puis sélectionnez l’une des options suivantes :

   * **[!UICONTROL Propagate Only]:** pour afficher les données propagées sur les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads]. Vous pouvez toujours publier les données de n’importe quel composant et ses sous-composants ultérieurement à partir de l’onglet [!UICONTROL Templates] .

   * **[!UICONTROL Propagate and Preview]:** pour créer un fichier de feuille d’envoi groupé (nommé « `<feed file name>_<template name>` »), disponible dans la vue [!UICONTROL Bulksheets] pour révision (mais pas dans les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads]). Vous pouvez ensuite publier le fichier de feuille d&#39;envoi groupé à partir de la vue [!UICONTROL Bulksheets].

     Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, le fichier est au format ZIP. Vous n’avez pas besoin de décompresser le fichier pour le publier.

   * **[!UICONTROL Propagate and Post to SE]:** pour créer un fichier de feuille d’envoi groupé (nommé « `<feed file name>_<template name>` ») qui est immédiatement mis en file d’attente pour la publication sur le réseau publicitaire. Le fichier de feuille d&#39;envoi groupé est disponible dans la vue [!UICONTROL Bulksheets], mais il n&#39;est pas disponible dans les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

     Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, le fichier est au format ZIP.

   La « Dernière Prop. Statut » indique le statut de la tâche pour les modèles applicables.

   Lorsque chaque action de propagation est terminée, un résumé de propagation est ajouté à l&#39;onglet [!UICONTROL Propagations], indiquant le nombre de chaque type d&#39;entité qui a été ou serait créé, mis en pause ou supprimé en fonction de la propagation. L’estimation n’inclut pas les modifications effectuées à partir du propre éditeur d’annonces du réseau publicitaire.

## Propager les fichiers de flux depuis la liste [!UICONTROL Feeds]

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]**.

1. Cochez la case en regard du fichier de flux.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Propagate/Post Feed Data]**, puis sélectionnez l’une des options suivantes :

   * **[!UICONTROL Propagate Only]:** pour afficher les données propagées sur les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads]. Vous pouvez toujours publier les données de n’importe quel composant et ses sous-composants ultérieurement à partir de l’onglet [!UICONTROL Templates] .

   * **[!UICONTROL Propagate and Preview]:** pour créer un fichier de feuille d’envoi groupé (nommé « `<feed file name>_<template name>` »), disponible dans la vue [!UICONTROL Bulksheets] pour révision (mais pas dans les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads]). Vous pouvez ensuite publier le fichier de feuille d&#39;envoi groupé à partir de la vue [!UICONTROL Bulksheets].

     Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, le fichier est au format ZIP. Vous n’avez pas besoin de décompresser le fichier pour le publier.

   * **[!UICONTROL Propagate and Post to SE]:** pour créer un fichier de feuille d’envoi groupé (nommé « `<feed file name>_<template name>` ») qui est immédiatement mis en file d’attente pour la publication sur le réseau publicitaire. Le fichier de feuille d&#39;envoi groupé est disponible dans la vue [!UICONTROL Bulksheets], mais il n&#39;est pas disponible dans les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

     Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, le fichier est au format ZIP.

1. Dans la fenêtre pop-up, cochez la case en regard de chaque modèle par lequel vous souhaitez propager les données du fichier de flux, puis cliquez sur **[!UICONTROL Propagate Feed]**.

   Tous les modèles associés au fichier sont répertoriés.

L’onglet [!UICONTROL Templates] s’ouvre et la colonne « [!UICONTROL Last Prop. Status] » affiche le statut de la tâche pour les modèles applicables.

Lorsque chaque action de propagation est terminée, un résumé de propagation est ajouté à l&#39;onglet [!UICONTROL Propagations], indiquant le nombre de chaque type d&#39;entité qui a été ou serait créé, mis en pause ou supprimé en fonction de la propagation. L’estimation n’inclut pas les modifications effectuées à partir du propre éditeur d’annonces du réseau publicitaire.

## Affichage d&#39;un résumé de la propagation

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Cliquez sur l’onglet **[!UICONTROL Propagations]** .

1. En regard du nom du modèle, cliquez sur ![icône Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "icône Afficher/modifier les paramètres") .

## Arrêt d&#39;un traitement de propagation

Vous pouvez arrêter un traitement de propagation pour les données de flux d&#39;inventaire pendant que le traitement est toujours en file d&#39;attente.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Dans la colonne « [!UICONTROL Last Prop. Status] » en regard du nom du modèle, cliquez sur **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Gérer les modèles publicitaires pour les flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Afficher les données générées à partir des flux](propagated-data-view.md)
>* [Modifier les données générées à partir des flux](propagated-data-edit.md)
>* [Publier les données de campagne générées à partir des flux sur les réseaux publicitaires](propagated-data-post.md)
>* [Arrêter un traitement de validation des données de flux de stock](stop-job.md)
>* [États des données générées à partir des flux](propagated-data-status.md)
