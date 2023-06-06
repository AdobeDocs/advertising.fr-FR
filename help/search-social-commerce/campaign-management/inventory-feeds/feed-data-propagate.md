---
title: Propager les données de flux d’inventaire par le biais de modèles
description: Découvrez comment propager des données de vos flux d’inventaire par le biais de modèles d’annonces afin de gérer la structure du compte et de diffuser des annonces dynamiques.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Propager les données de flux d’inventaire par le biais de modèles

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Après avoir créé un modèle de flux spécifique au réseau publicitaire et associé un fichier de flux ou un [!DNL Google] ou [!DNL Microsoft®] compte de centre commercial avec celui-ci, vous pouvez créer dynamiquement des publicités en propageant les données de flux par le biais du modèle en fonction de la variable [paramètres de données de flux](feed-settings-manage.md). Lors de la propagation, les noms des colonnes dans le modèle sont remplacés par des valeurs de données dans le flux. Les campagnes générées et leurs composants possèdent les paramètres par défaut, sauf indication contraire du modèle. Selon les options de modèle, Search, Social et Commerce crée une nouvelle structure de compte (campagnes, groupes publicitaires, mots-clés) pour les annonces ou mappe les annonces à la structure de compte existante.

Lorsque de nouvelles données de flux contiennent de nouvelles valeurs de données pour un élément ou que le modèle a changé, les publicités existantes sont supprimées et de nouvelles sont créées. Si la seule modification est la désignation de [!DNL Google Ads] Param 1 et Param 2, alors seules ces valeurs sont mises à jour. Les publicités en double (la même copie de publicité et la même page d’entrée) ne sont jamais créées.

Lorsque vous propagez des données, vous pouvez éventuellement prévisualiser les données générées dans une vue de hiérarchie de campagne, générer un fichier de feuille d’envoi groupé en vue de la révision ou générer un fichier de feuille d’envoi groupé en vue de la publication immédiate sur le réseau publicitaire. Une fois chaque action de propagation terminée, un résumé de propagation est ajouté à l’onglet Propagations , indiquant le nombre de chaque type d’entité qui a été créé, mis en pause ou supprimé en fonction de la propagation. Si vous ne publiez pas les données immédiatement, vous pouvez les prévisualiser et les publier ultérieurement.

## Propagation des fichiers de flux à partir du [!UICONTROL Templates] tab

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, qui s’ouvre sur le [!UICONTROL Templates] .

1. Cochez la case en regard des modèles à propager.

1. Dans la barre d’outils, cliquez sur **[!UICONTROL Propagate]**, puis sélectionnez l’une des options suivantes :

   * **[!UICONTROL Propagate Only]:** Pour afficher les données propagées sur la variable [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets. Vous pouvez toujours publier les données de n’importe quel composant et de ses sous-composants ultérieurement à partir de la fonction [!UICONTROL Templates] .

   * **[!UICONTROL Propagate and Preview]:** Pour créer un fichier de feuille d’envoi groupé (appelé &quot;`<feed file name>_<template name>`&quot;), qui est disponible dans la variable [!UICONTROL Bulksheets] à des fins de révision (mais pas sur la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets). Vous pouvez publier ultérieurement le fichier de feuille d’envoi groupé à partir de la [!UICONTROL Bulksheets] vue.

      Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, il est au format ZIP. Vous n’avez pas besoin de décompresser le fichier pour le publier.

   * **[!UICONTROL Propagate and Post to SE]:** Pour créer un fichier de feuille d’envoi groupé (appelé &quot;`<feed file name>_<template name>`&quot;) immédiatement placé en file d’attente pour publication sur le réseau publicitaire. Le fichier de feuille d’envoi groupé est disponible dans la [!UICONTROL Bulksheets] , mais elle n’est pas disponible sur la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets.

      Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, il est au format ZIP.
   La &quot;Dernière Prop&quot;. La colonne État indique l’état de la tâche pour les modèles applicables.

   Une fois chaque action de propagation terminée, un résumé de propagation est ajouté à la variable [!UICONTROL Propagations] , indiquant le nombre de chaque type d’entité qui a été créé, mis en pause ou supprimé en fonction de la propagation. L’estimation n’inclut pas les modifications effectuées à partir du propre éditeur d’annonces du réseau publicitaire.

## Propagation des fichiers de flux à partir du [!UICONTROL Feeds] list

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Feeds]**.

1. Cochez la case en regard du fichier de flux.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Propagate/Post Feed Data]**, puis sélectionnez l’une des options suivantes :

   * **[!UICONTROL Propagate Only]:** Pour afficher les données propagées sur la variable [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets. Vous pouvez toujours publier les données de n’importe quel composant et de ses sous-composants ultérieurement à partir de la fonction [!UICONTROL Templates] .

   * **[!UICONTROL Propagate and Preview]:** Pour créer un fichier de feuille d’envoi groupé (appelé &quot;`<feed file name>_<template name>`&quot;), qui est disponible dans la variable [!UICONTROL Bulksheets] à des fins de révision (mais pas sur la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets). Vous pouvez publier ultérieurement le fichier de feuille d’envoi groupé à partir de la [!UICONTROL Bulksheets] vue.

      Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, il est au format ZIP. Vous n’avez pas besoin de décompresser le fichier pour le publier.

   * **[!UICONTROL Propagate and Post to SE]:** Pour créer un fichier de feuille d’envoi groupé (appelé &quot;`<feed file name>_<template name>`&quot;) immédiatement placé en file d’attente pour publication sur le réseau publicitaire. Le fichier de feuille d’envoi groupé est disponible dans la [!UICONTROL Bulksheets] , mais elle n’est pas disponible sur la [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets.

      Lorsque le fichier de feuille d’envoi groupé obtenu fait plus de 2 Mo, il est au format ZIP.

1. Dans la fenêtre contextuelle, cochez la case en regard de chaque modèle par lequel vous souhaitez propager les données du fichier de flux, puis cliquez sur **[!UICONTROL Propagate Feed]**.

   Tous les modèles associés au fichier sont répertoriés.

Le [!UICONTROL Templates] s’ouvre, et le[!UICONTROL Last Prop. Status]&quot; affiche l’état de la tâche pour les modèles applicables.

Une fois chaque action de propagation terminée, un résumé de propagation est ajouté à la variable [!UICONTROL Propagations] , indiquant le nombre de chaque type d’entité qui a été créé, mis en pause ou supprimé en fonction de la propagation. L’estimation n’inclut pas les modifications effectuées à partir du propre éditeur d’annonces du réseau publicitaire.

## Affichage d’un résumé de propagation

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Cliquez sur le bouton **[!UICONTROL Propagations]** .

1. En regard du nom du modèle, cliquez sur ![Icône Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Icône Afficher/modifier les paramètres") .

## Arrêt d’une tâche de propagation

Vous pouvez arrêter une tâche de propagation pour les données de flux d’inventaire pendant que la tâche est toujours en file d’attente.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, qui s’ouvre sur le [!UICONTROL Templates] .

1. Dans le[!UICONTROL Last Prop. Status]&quot; en regard du nom du modèle, cliquez sur **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Gestion des modèles d’annonces pour les flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Affichage des données générées à partir de flux](propagated-data-view.md)
>* [Modification des données générées à partir de flux](propagated-data-edit.md)
>* [Données de campagne de publication générées à partir de flux vers les réseaux publicitaires](propagated-data-post.md)
>* [Arrêt d’une tâche de publication pour les données de flux d’inventaire](stop-job.md)
>* [Statuts des données générées à partir de flux](propagated-data-status.md)

